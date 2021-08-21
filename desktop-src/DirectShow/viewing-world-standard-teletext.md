---
description: Affichage du télétexte standard du monde
ms.assetid: 99b3395b-8775-4fe8-b173-187fa359978f
title: Affichage du télétexte standard du monde
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2129538d91a7ac48fea26fd5f1987473896760c164fb3e2b1d4a2b1d142a1f04
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120078543"
---
# <a name="viewing-world-standard-teletext"></a>Affichage du télétexte standard du monde

> [!Note]  
> cette fonctionnalité a été supprimée de Windows Vista et des systèmes d’exploitation ultérieurs. il peut être utilisé dans les systèmes d’exploitation Microsoft Windows 2000, Windows XP et Windows Server 2003.

 

Le WST (World standard Teletext) est encodé dans l’intervalle de blanc vertical (VBI) du signal de télévision analogique. Le graphique de filtre pour afficher un aperçu du télétexte est similaire au graphique utilisé pour afficher les sous-titres. Le diagramme suivant illustre ce graphique.

![graphique d’aperçu WST](images/vidcap10.png)

Ce graphique utilise les filtres suivants pour l’affichage de WST :

-   [Convertisseur de tee/récepteur à récepteur](tee-sink-to-sink-converter.md). Accepte les informations VBI du filtre de capture et les divise en flux distincts pour chaque service de données présent sur le signal.
-   [Codec WST](wst-codec-filter.md). Décode les données de télétexte à partir des exemples VBI.
-   [Décodeur WST](wst-decoder-filter.md). Convertit les données de télétexte et dessine le texte sur des bitmaps. le filtre en aval (dans ce cas, la superposition Mixer) recouvre les bitmaps dans la vidéo.

la méthode **RenderStream** de Capture Graph Builder ne prend pas en charge directement les filtres WST, de sorte que votre application doit effectuer un travail supplémentaire.

1.  ajoutez la superposition Mixer filtre au graphique de filtre. Le code suivant utilise la fonction AddFilterByCLSID décrite dans [Ajouter un filtre par CLSID](add-a-filter-by-clsid.md). (AddFilterByCLSID n’est pas une API DirectShow.)
    ```C++
    IBaseFilter *pOvMix = NULL;  // Pointer to the Overlay Mixer filter.
    hr = AddFilterByCLSID(pGraph, CLSID_OverlayMixer, L"OVMix", &pOvMix);
    if (FAILED(hr)) 
    {
        // Handle the error ...
    }
    ```

    

2.  Connecter la préversion du filtre de rendu vidéo via le Mixer de superposition. Vous pouvez utiliser la méthode **RenderStream** , comme suit :
    ```C++
    hr = pBuild->RenderStream(&PIN_CATEGORY_PREVIEW, &MEDIATYPE_Video, 
        pCap, pOvMix, 0);
    ```

    

3.  Ajoutez le filtre de convertisseur de tee/récepteur-à-récepteur au graphique de filtre. Le code suivant utilise la fonction CreateKernelFilter décrite dans [création de filtres de Kernel-Mode](creating-kernel-mode-filters.md). (CreateKernelFilter n’est pas une API DirectShow.)
    ```C++
    IBaseFilter* pKernelTee = NULL;
    hr = CreateKernelFilter(AM_KSCATEGORY_SPLITTER, 
        OLESTR("Tee/Sink-to-Sink Converter"), &pKernelTee);
    if (SUCCEEDED(hr))
    {
        hr = pGraph->AddFilter(pKernelTee, L"Kernel Tee");
    }
    ```

    

4.  Ajoutez le filtre de codec WST au graphique de filtre :
    ```C++
    IBaseFilter* pWstCodec = NULL;
    hr = CreateKernelFilter(AM_KSCATEGORY_VBICODEC, 
        OLESTR("WST Codec"), &pWstCodec);
    if (SUCCEEDED(hr))
    {
        hr = pGraph->AddFilter(pWstCodec, L"WST Codec");
    }
    ```

    

5.  Appelez **RenderStream** pour connecter le code confidentiel de filtre de capture au convertisseur tee/Sink-to-récepteur, et le convertisseur de tee/récepteur-à-récepteur au filtre de codec WST :
    ```C++
    hr = pBuild->RenderStream(&PIN_CATEGORY_VBI, 0, pCap, 
        pKernelTee, pWstCodec);
    ```

    

6.  Appelez à nouveau **RenderStream** pour connecter le filtre de codec WST au mixer de recouvrement. Le filtre de décodage WST est automatiquement placé dans le graphique.
    ```C++
    hr = pBuild->RenderStream(0, 0, pWstCodec, 0, pOvMix);
    ```

    

7.  N’oubliez pas de libérer toutes les interfaces de filtre.
    ```C++
    pOvMix->Release();
    pKernelTee->Release();
    pWstCodec->Release();
    ```

    

> [!Note]  
> Actuellement, le filtre de décodage WST ne prend pas en charge les connexions au filtre de convertisseur de mixage vidéo (VMR). Par conséquent, vous devez utiliser le filtre de convertisseur vidéo hérité pour afficher Teletext.

 

Si le filtre de capture possède un code vidéo (PIN \_ CATEGPORY \_ VIDEOPORT \_ VBI), connectez-le au filtre d' [allocateur de surface VBI](vbi-surface-allocator.md) . Dans le cas contraire, le graphique ne s’exécutera pas correctement. L’exemple de code suivant utilise la fonction AddFilterByCLSID, décrite dans [Ajouter un filtre par CLSID](add-a-filter-by-clsid.md)et la fonction FindPinByCategory, décrite dans [utilisation des catégories de code confidentiel](working-with-pin-categories.md). (aucune des fonctions n’est une API DirectShow.)


```C++
// Look for a video port VBI pin on the capture filter.
IPin *pVPVBI = NULL;
hr = FindPinByCategory(pCap, PINDIR_OUTPUT, 
    PIN_CATEGORY_VIDEOPORT_VBI, &pVPVBI);
if (FAILED(hr))
{
    // No video port VBI pin; nothing else to do. OK to run the graph.
}
else
{
    // Found one. Connect it to the VBI Surface Allocator.
    IBaseFilter *pSurf = NULL;
    hr = AddFilterByCLSID(pGraph, CLSID_VBISurfaces, L"VBI Surf", &pSurf);
    if (SUCCEEDED(hr))
    {
        hr = pBuild->RenderStream(NULL, NULL, pVPVBI, 0, pSurf);
        pSurf->Release();
    }
    if (FAILED(hr))
    {
        // Handle the error (not shown). It is probably not safe to 
        // run the graph at this point.
    }
    pVPVBI->Release();
}
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Sous-titres et télétexte](closed-captions-and-teletext.md)
</dt> </dl>

 

 



