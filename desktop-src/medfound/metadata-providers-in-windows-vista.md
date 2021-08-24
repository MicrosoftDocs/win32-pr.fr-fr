---
description: dans Windows Vista, Microsoft Media Foundation expose des métadonnées par le biais de l’interface IMFMetadata.
ms.assetid: a26e40c2-1717-4a13-8bf0-e41376a8d317
title: fournisseurs de métadonnées dans Windows Vista
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1edf65b59e0f47e603b057f49a76d8721b8733849937cb29fd0afbe0b9b44920
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119827069"
---
# <a name="metadata-providers-in-windows-vista"></a>fournisseurs de métadonnées dans Windows Vista

dans Windows Vista, Microsoft Media Foundation expose des métadonnées par le biais de l’interface [**IMFMetadata**](/windows/desktop/api/mfidl/nn-mfidl-imfmetadata) .

## <a name="reading-metadata"></a>Lecture des métadonnées

Pour lire les métadonnées d’une source de média, procédez comme suit :

1.  Obtient un pointeur vers l’interface [**IMFMediaSource**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource) de la source du média. Vous pouvez utiliser l’interface [**IMFSourceResolver**](/windows/desktop/api/mfidl/nn-mfidl-imfsourceresolver) pour récupérer un pointeur **IMFMediaSource** .
2.  Appelez [**IMFMediaSource :: CreatePresentationDescriptor**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor) pour récupérer le descripteur de présentation de la source du média.
3.  Appelez [**MFGetService**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice) sur la source du média pour obtenir un pointeur vers l’interface [**IMFMetadataProvider**](/windows/desktop/api/mfidl/nn-mfidl-imfmetadataprovider) . Dans le paramètre *guidService* de **MFGetService**, spécifiez la **valeur \_ \_ \_ service du fournisseur de métadonnées MF**. Si la source ne prend pas en charge l’interface **IMFMetadataProvider** , **MFGetService** retourne le **\_ service MF E \_ non pris en charge \_**.
4.  Appelez [**IMFMetadataProvider :: GetMFMetadata**](/windows/desktop/api/mfidl/nf-mfidl-imfmetadataprovider-getmfmetadata) et transmettez un pointeur vers le descripteur de présentation. Cette méthode retourne un pointeur vers l’interface [**IMFMetadata**](/windows/desktop/api/mfidl/nn-mfidl-imfmetadata) .
    -   Pour récupérer les métadonnées au niveau du flux, appelez d’abord [**IMFStreamDescriptor :: GetStreamIdentifier**](/windows/desktop/api/mfidl/nf-mfidl-imfstreamdescriptor-getstreamidentifier) pour récupérer l’identificateur de flux. Transmettez ensuite l’identificateur de flux dans le paramètre *dwStreamIdentifier* de [**GetMFMetadata**](/windows/desktop/api/mfidl/nf-mfidl-imfmetadataprovider-getmfmetadata).
    -   Pour récupérer les métadonnées au niveau de la présentation, définissez *dwStreamIdentifier* sur zéro.
5.  \[\]Appelez [**IMFMetadata :: GetAllLanguages**](/windows/desktop/api/mfidl/nf-mfidl-imfmetadata-getalllanguages) facultatif pour obtenir la liste des langues dans lesquelles les métadonnées sont disponibles. Les langues sont identifiées à l’aide de balises de langue conformes à RFC 1766.
6.  \[\]Appelez [**IMFMetadata :: SetLanguage**](/windows/desktop/api/mfidl/nf-mfidl-imfmetadata-setlanguage) facultatif pour sélectionner la langue.
7.  \[\]Appelez [**IMFMetadata :: GetAllPropertyNames**](/windows/desktop/api/mfidl/nf-mfidl-imfmetadata-getallpropertynames) facultatif pour obtenir la liste des noms de toutes les propriétés de métadonnées pour ce flux ou cette présentation.
8.  Appelez [**IMFMetadata :: GetProperty**](/windows/desktop/api/mfidl/nf-mfidl-imfmetadata-getproperty) pour obtenir une valeur de propriété de métadonnées spécifique, en passant le nom de la propriété.

Le code suivant montre les étapes 2 à 4 :


```C++
HRESULT GetMetadata(
    IMFMediaSource *pSource, IMFMetadata **ppMetadata, DWORD dwStream = 0)
{
    IMFPresentationDescriptor *pPD = NULL;
    IMFMetadataProvider *pProvider = NULL;

    HRESULT hr = pSource->CreatePresentationDescriptor(&pPD);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = MFGetService(
        pSource, MF_METADATA_PROVIDER_SERVICE, IID_PPV_ARGS(&pProvider));

    if (FAILED(hr))
    {
        goto done;
    }

    hr = pProvider->GetMFMetadata(pPD, dwStream, 0, ppMetadata);

done:
    SafeRelease(&pPD);
    SafeRelease(&pProvider);
    return hr;
}
```



Le code suivant montre les étapes 7 à 8. Supposons que `DisplayProperty` est une fonction qui affiche une valeur **PROPVARIANT** .


```C++
HRESULT DisplayMetadata(IMFMetadata *pMetadata)
{
    PROPVARIANT varNames;
    HRESULT hr = pMetadata->GetAllPropertyNames(&varNames);
    if (FAILED(hr))
    {
        return hr;
    }

    for (ULONG i = 0; i < varNames.calpwstr.cElems; i++)
    {
        wprintf(L"%s\n", varNames.calpwstr.pElems[i]);

        PROPVARIANT varValue;
        hr = pMetadata->GetProperty( varNames.calpwstr.pElems[i], &varValue );
        if (SUCCEEDED(hr))
        {
            DisplayProperty(varValue);
            PropVariantClear(&varValue);
        }
    }

    PropVariantClear(&varNames);
    return hr;
}
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Métadonnées de média](media-metadata.md)
</dt> <dt>

[Fournisseurs de métadonnées de Shell](shell-metadata-providers.md)
</dt> </dl>

 

 



