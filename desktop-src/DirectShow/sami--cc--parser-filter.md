---
description: Filtre de l’analyseur SAMI (CC)
ms.assetid: 9b09dd86-3c22-4565-82a0-106d5ca2e42d
title: Filtre de l’analyseur SAMI (CC)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d93cb5f55ebbcd70359f5e2e9b57084752f6a6d8c8325a6d7037d52e5cf3cec4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120102329"
---
# <a name="sami-cc-parser-filter"></a>Filtre de l’analyseur SAMI (CC)

Analyse les données de sous-titrage des fichiers SAMI (Synchronized Accessible Media Interchange).

SAMI est un format de texte similaire à HTML et est utilisé pour l’encodage des légendes basées sur le temps. Ce filtre convertit les données SAMI en un flux de texte. Chaque échantillon du flux contient une entrée de légende, ainsi que des informations de format. Les horodatages des échantillons sont générés à partir des informations d’heure dans le fichier SAMI.

Ce filtre est conçu pour être utilisé avec le filtre de [convertisseur de commande de script interne](internal-script-command-renderer-filter.md) . Le convertisseur de commande de script interne reçoit les exemples de texte et les envoie à l’application, sous la forme de notifications d’événements. Pour plus d'informations, consultez la section Notes.



| Étiquette | Valeur |
|------------------------------------------|----------------------------------------------------------------------------------------------------------|
| Interfaces de filtre                        | [**IAMStreamSelect**](/windows/desktop/api/Strmif/nn-strmif-iamstreamselect), [ **IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter)                           |
| Types de média de broche d’entrée                    | Flux de MEDIATYPE \_                                                                                        |
| Interfaces pin d’entrée                     | [**IPIN**](/windows/desktop/api/Strmif/nn-strmif-ipin), [ **IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)                                         |
| Types de média de broche de sortie                   | \_Texte de MediaType, MEDIASUBTYPE \_ null                                                                      |
| Interfaces de broche de sortie                    | [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking), [**IPIN**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol) |
| CLSID du filtre                             | {33FACFE0-A9BE-11D0-A520-00A0D10129C0}                                                                   |
| CLSID de page de propriétés                      | Aucune page de propriétés                                                                                         |
| Exécutable                               | quartz.dll                                                                                               |
| [Mérite](merit.md)                       | MÉRITE \_ improbable                                                                                          |
| [Catégorie de filtre](filter-categories.md) | CLSID \_ LegacyAmFilterCategory                                                                            |



 

## <a name="remarks"></a>Remarques

Voici un fichier SAMI simple :


```C++
<SAMI>
<Head>
<STYLE TYPE="text/css"> <!--
    .ENCC {Name: English; lang:en-US; SAMI_TYPE: CC;}
    .FRCC {Name: French; lang:fr-FR; SAMI_TYPE: CC;}
    #NORMAL {Name: Normal; font-family: arial;}
    #GREENTEXT {Name: GreenText; color:green; font-family: verdana;}
-->
</STYLE>
</Head>
<BODY>
<Sync Start=1000>
    <P CLASS="ENCC">One
    <P CLASS="FRCC">Un

<Sync Start=2000>
    <P CLASS="ENCC">Two
    <P CLASS="FRCC">Deux

<Sync Start=3000>
    <P CLASS="ENCC">Three
    <P CLASS="FRCC">Trois
</BODY>
</SAMI>
```



La balise **style** définit deux paramètres de langue, anglais (. ENCC) et français (. FRCC). Il définit également deux styles, \# normal et \# GREENTEXT. Chaque balise de **synchronisation** définit l’heure de début d’une légende, en millisecondes. Les balises **P** contiennent le texte de légende, tandis que l’attribut de **classe** spécifie le paramètre de langue auquel la légende s’applique.

Pour chaque langue et chaque style, le filtre crée un flux logique. À tout moment, un seul flux de langage et un seul flux de style sont activés. Quand le filtre génère un exemple, il sélectionne la légende de la langue active et applique le style actuel. Par défaut, la première langue et le style déclarés dans le fichier sont activés. Une application peut utiliser la méthode [**IAMStreamSelect :: Enable**](/windows/desktop/api/Strmif/nf-strmif-iamstreamselect-enable) pour activer un autre flux.

Avec les paramètres par défaut, la première légende de l’exemple de fichier produit la sortie suivante :


```C++
<P STYLE=" Name: English; lang:en-US; SAMI_TYPE: CC; Name: Normal; font-family: arial;">One
```



Si la sortie est envoyée vers le convertisseur de commande de script interne, ce filtre envoie une notification d’événement d' [**\_ \_ événement OLE EC**](ec-ole-event.md) . Le deuxième paramètre d’événement est un BSTR avec le texte de légende. L’application peut récupérer l’événement et afficher la légende.

L’exemple suivant montre comment restituer un fichier SAMI, récupérer des informations de flux, activer des flux et afficher le texte de légende. L’exemple suppose que le fichier SAMI précédent est enregistré en tant que C : \\ sami \_ test \_ file. sami.

Par souci de concision, cet exemple utilise des index de flux codés en dur lorsqu’il appelle la méthode **IAMStreamSelect :: Enable** . Il effectue également une vérification des erreurs minimale.


```C++
void __cdecl main()
{
    HRESULT hr;
    IGraphBuilder *pGraph;
    IMediaControl *pMediaControl;
    IMediaEventEx *pEv;
    IBaseFilter   *pSAMI;

    CoInitialize(NULL);
    
    // Create the filter graph manager.
    CoCreateInstance(CLSID_FilterGraph, NULL, CLSCTX_INPROC, 
                        IID_IGraphBuilder, (void **)&pGraph);
    pGraph->QueryInterface(IID_IMediaControl, (void **)&pMediaControl);
    pGraph->QueryInterface(IID_IMediaEventEx, (void**)&pEv);

    // Create the graph and find the SAMI parser.
    pGraph->RenderFile(L"C:\\Sami_test_file.sami", NULL);
    hr = pGraph->FindFilterByName(L"SAMI (CC) Parser", &pSAMI);
    if (SUCCEEDED(hr)) 
    {
        IAMStreamSelect *pStrm = NULL;
        hr = pSAMI->QueryInterface(IID_IAMStreamSelect, (void**)&pStrm);
        if (SUCCEEDED(hr)) 
        {
            DWORD dwStreams = 0;
            pStrm->Count(&dwStreams);
            printf("Stream count: %d\n", dwStreams);

            // Select French and "GreenText"
            hr = pStrm->Enable(1, AMSTREAMSELECTENABLE_ENABLE);
            hr = pStrm->Enable(3, AMSTREAMSELECTENABLE_ENABLE);

            // Print the name of each logical stream.
            for (DWORD index = 0; index < dwStreams; index++)
            {
                DWORD dwFlags;
                WCHAR *wszName;
                hr = pStrm->Info(index, NULL, &dwFlags, NULL, NULL,
                    &wszName, NULL, NULL);
                if (hr == S_OK)
                {
                    wprintf(L"Stream %d: %s [%s]\n", index, wszName, 
                        (dwFlags ?  L"ENABLED" : L"DISABLED"));
                    CoTaskMemFree(wszName);
                }
            }
            pStrm->Release();
        }
        pSAMI->Release();
    }

    // Run the graph and display the captions.
    pMediaControl->Run();
    while (1)
    {
        long evCode, lParam1, lParam2;
        pEv->GetEvent(&evCode, &lParam1, &lParam2, 100);
        
        if (evCode == EC_OLE_EVENT) {
            wprintf(L"%s\n", (BSTR)lParam2);
        }
        pEv->FreeEventParams(evCode, lParam1, lParam2);

        if (evCode == EC_USERABORT || evCode == EC_COMPLETE || evCode == EC_ERRORABORT)
            break;
    }

    // Clean up.
    pMediaControl->Release();
    pEv->Release();
    pGraph->Release();
    CoUninitialize();
}
```



Ce filtre utilise l’interface [**IAsyncReader**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader) pour extraire des échantillons du filtre source. Par conséquent, il ne prend pas en charge l’interface [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) sur sa broche d’entrée.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[DirectShow Filtres](directshow-filters.md)
</dt> </dl>

 

 



