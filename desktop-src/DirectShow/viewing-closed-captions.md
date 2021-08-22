---
description: Affichage des sous-titres
ms.assetid: 86c0c553-af35-4ad1-8918-63d9e4577c73
title: Affichage des sous-titres
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f52288b1c4fa5c43f7e0419d81bd9727a4db86848d368b600e1d713c53dc1593
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119903427"
---
# <a name="viewing-closed-captions"></a>Affichage des sous-titres

Pour prendre en charge les sous-titres dans la télévision analogique, le filtre de capture expose un code confidentiel qui remet les données de sous-titres VBI ou Closed. Le code PIN aura l’une des catégories de code confidentiel suivantes :

-   Code confidentiel VBI ( \_ catégorie de pin \_ VBI). Fournit un flux d’exemples de forme d’onde VBI. Ils sont passés à un filtre de décodeur qui extrait les données de sous-titrage.
-   Code PIN CC (code confidentiel de \_ catégorie \_ cc). Fournit des paires d’octets à légende fermée, extraites des données de la ligne-21.
-   Découpage matériel code confidentiel CC (PINNAME \_ vidéo \_ cc \_ capture).

Pour afficher un aperçu des sous-titres, appelez [**ICaptureGraphBuilder2 :: RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) avec la catégorie de code confidentiel VBI et, si cela échoue, rappelez-le avec la catégorie CC.


```C++
hr = pBuild->RenderStream(&PIN_CATEGORY_VBI, 0, pCap, 0, 0);
if (FAILED(hr))
{
    hr = pBuild->RenderStream(&PIN_CATEGORY_CC, 0, pCap, 0, 0);
}
```



Le diagramme suivant montre un graphique de filtre classique pour l’affichage des sous-titres.

![graphique de prévisualisation du sous-titrage](images/vidcap08.png)

Ce graphique utilise les filtres suivants pour l’affichage des sous-titres :

-   [Convertisseur de tee/récepteur à récepteur](tee-sink-to-sink-converter.md). Accepte les informations VBI du filtre de capture et les divise en flux distincts pour chaque service de données présent sur le signal. Microsoft fournit des codecs VBI pour les sous-titres, les NABTS et le Teletext standard (WST).
-   [Décodeur CC](cc-decoder-filter.md). Décode les données CC à partir des formes d’onde VBI échantillonnées fournies par le filtre de capture.
-   [Décodeur de ligne 21](line-21-decoder-filter.md). Traduit les paires d’octets CC et dessine le texte de légende sur les bitmaps. le filtre en aval (dans ce cas, la superposition Mixer) recouvre les bitmaps dans la vidéo.

la méthode [**RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) de Capture Graph Builder ajoute automatiquement ces filtres. Si le filtre de capture a un pin CC au lieu d’un code confidentiel VBI, le code PIN CC est directement connecté au filtre de décodeur de ligne 21.

> [!Note]  
> Si vous utilisez le filtre de convertisseur de mixage vidéo (VMR) pour le rendu, utilisez le filtre de décodeur de ligne 21 2. Ce filtre a les mêmes fonctionnalités que le décodeur de ligne 21, mais le CLSID est CLSID \_ Line21Decoder2.

 

> [!Note]  
> le filtre de décodage CC a été supprimé dans Windows Vista. Les nouvelles applications doivent utiliser le filtre VBICodec, qui est documenté dans la documentation Microsoft TV technologies.

 

Si le périphérique de capture utilise un port vidéo, le filtre de capture peut avoir une broche de port vidéo VBI (catégorie de broche \_ \_ VIDEOPORT \_ VBI). Ce code confidentiel doit être connecté au filtre [allocateur de surface VBI](vbi-surface-allocator.md) , qui alloue des surfaces pour contenir les données VBI capturées. La méthode [**RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) ajoute ce filtre si nécessaire. Le diagramme suivant montre un graphique de filtre avec l’allocateur de surface VBI.

![graphique de prévisualisation de sous-titrage avec un allocateur de surface VBI](images/vidcap09.png)

### <a name="enabling-and-disabling-the-captions"></a>Activation et désactivation des légendes

Pour contrôler l’affichage des sous-titres, utilisez l’interface [**IAMLine21Decoder**](/previous-versions/windows/desktop/api/il21dec/nn-il21dec-iamline21decoder) sur le filtre de décodeur de la ligne 21. Par exemple, vous pouvez désactiver l’affichage des sous-titres à l’aide de la méthode [**IAMLine21Decoder :: SetServiceState**](/previous-versions/windows/desktop/api/il21dec/nf-il21dec-iamline21decoder-setservicestate) , comme suit :


```C++
// Use the FindInterface method to find the interface.
IAMLine21Decoder *pLine21 = NULL;
hr = pBuild->FindInterface(
    &LOOK_DOWNSTREAM_ONLY, // Look downstream from pCap 
    NULL,                  // No particular media type
    pCap,                  // Pointer to the capture filter.
    IID_IAMLine21Decoder, (void**)&pLine21);
if (SUCCEEDED(hr))
{
    pLine21->SetServiceState(AM_L21_CCSTATE_Off);
    // (Use AM_L21_CCSTATE_On to enable.)
    pLine21->Release();
}
```



Cet exemple utilise la méthode [**ICaptureGraphBuilder2 :: FindInterface**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-findinterface) pour localiser l’interface [**IAMLine21Decoder**](/previous-versions/windows/desktop/api/il21dec/nn-il21dec-iamline21decoder) . Le premier paramètre de **FindInterface** est **&Rechercher en \_ aval \_ uniquement**, qui spécifie de rechercher en aval à partir du filtre de capture (*pCap*).

### <a name="capturing-closed-caption-bitmaps"></a>Capturer des bitmaps de sous-titres

Vous pouvez capturer les bitmaps de légende dans un fichier. Pour ce faire, ajoutez la section d’écriture de fichiers du graphique de filtre, comme décrit dans [capture de la vidéo dans un fichier](capturing-video-to-a-file.md). Ensuite, affichez le code confidentiel CC ou VBI dans le filtre Mux :


```C++
hr = pBuild->RenderStream(&PIN_CATEGORY_VBI, 0, pCap, 0, pMux);
if (FAILED(hr))
{
    hr = pBuild->RenderStream(&PIN_CATEGORY_CC, 0, pCap, 0, pMux);
}
```



Si vous capturez également la vidéo, cette opération crée un fichier avec deux flux vidéo distincts. Il ne capture pas de vidéo avec des sous-titres superposés au-dessus de l’image.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Sous-titres et télétexte](closed-captions-and-teletext.md)
</dt> </dl>

 

 



