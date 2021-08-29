---
description: Découvrez comment ajouter des métadonnées au récepteur de fichiers ASF, qu’une application peut utiliser pour archiver des données de média ASF dans un fichier.
ms.assetid: ecfddf4e-71b4-42c4-8b54-9868cec6ed9b
title: Ajout de métadonnées au récepteur de fichiers
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 65e25ddc12b406987de4ec95d3183309e8453696d1bb5b2816054407f1ced4b8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119606719"
---
# <a name="adding-metadata-to-the-file-sink"></a>Ajout de métadonnées au récepteur de fichiers

Le récepteur de fichiers ASF est une implémentation de [**IMFMediaSink**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasink) fournie par Media Foundation qu’une application peut utiliser pour archiver des données de média ASF dans un fichier. Pour plus d’informations sur le modèle objet et l’utilisation générale des récepteurs de média ASF, consultez [récepteurs de média ASF](asf-media-sinks.md).

Une fois [le récepteur de fichiers ASF créé](creating-the-asf-file-sink.md), il doit être configuré avec des informations sur les flux et les informations d’encodage dans le fichier de sortie. Ces procédures sont décrites dans [Ajout d’informations de flux au récepteur de fichiers ASF](adding-stream-information-to-the-asf-file-sink.md) et [définition des propriétés dans le récepteur de fichiers](setting-properties-in-the-file-sink.md). En outre, vous pouvez également ajouter des informations de métadonnées avec des paires nom/valeur, telles que « auteur », titre. Cette rubrique décrit le processus d’ajout d’informations de métadonnées au récepteur de fichiers afin qu’il apparaisse dans l' [objet d’en-tête ASF](asf-file-structure.md)final.

Vous pouvez ajouter des informations de métadonnées au récepteur de fichiers ASF avant de générer la topologie d’encodage. L’objet ASF ContentInfo pour le récepteur de fichiers effectue le suivi des propriétés de métadonnées et est exposé à l’application via l’interface [**IMFMetadata**](/windows/desktop/api/mfidl/nn-mfidl-imfmetadata) . Certaines de ces propriétés, telles que « IsVBR », qui indiquent si le fichier contient des flux à débit binaire variable (VBR), sont définies automatiquement par le récepteur de fichiers en analysant les propriétés d’encodage de flux définies.

Pour obtenir la liste complète des propriétés, consultez la rubrique « liste d’attributs » dans la documentation du kit de développement logiciel (SDK).

## <a name="using-the-imfmetadata-interface-on-the-asf-file-sink"></a>Utilisation de l’interface IMFMetadata sur le récepteur de fichiers ASF

1.  Interrogez l’objet de récepteur de fichiers ASF pour obtenir un pointeur vers son implémentation de l’interface [**IMFMetadataProvider**](/windows/desktop/api/mfidl/nn-mfidl-imfmetadataprovider) .
2.  Appelez [**IMFMetadataProvider :: GetMFMetadata**](/windows/desktop/api/mfidl/nf-mfidl-imfmetadataprovider-getmfmetadata) pour accéder à un pointeur [**IMFMetadata**](/windows/desktop/api/mfidl/nn-mfidl-imfmetadata) .

    Le paramètre *pPresentationDescriptor* est ignoré et l’application peut passer la **valeur null**. Si l’application passe zéro comme identificateur de flux dans le paramètre *dwStreamIdentifier* , la méthode récupère les métadonnées qui s’appliquent à l’ensemble du fichier ASF. Dans le cas contraire, seules les métadonnées du flux sont récupérées.

3.  Appelez [**IMFMetadata :: GetAllPropertyNames**](/windows/desktop/api/mfidl/nf-mfidl-imfmetadata-getallpropertynames) pour récupérer la liste des propriétés de codage de fichiers définies sur le contenu multimédia.
4.  Appelez [**IMFMetadata :: GetProperty**](/windows/desktop/api/mfidl/nf-mfidl-imfmetadata-getproperty) pour récupérer les valeurs de propriété.

## <a name="example"></a>Exemples

L’exemple de code suivant montre comment énumérer les noms et les valeurs des propriétés qui sont définis sur le fichier ASF.


```C++
/////////////////////////////////////////////////////////////////////
// Name: ListASFProperties
//
// Enumerates the metadata properties of the ASF file. 
//
// pContentInfo: Pointer to the ASF ContentInfo object.
/////////////////////////////////////////////////////////////////////

HRESULT ListASFProperties(IMFASFContentInfo *pContentInfo)
{
    HRESULT hr = S_OK;
    
    PROPVARIANT varNames;
    PropVariantInit(&varNames);

    PROPVARIANT varValue;
    PropVariantInit(&varValue);

    IMFMetadataProvider* pProvider = NULL;
    IMFMetadata* pMetadata = NULL;

    // Query the ContentInfo object for IMFMetadataProvider.
    CHECK_HR(hr = pContentInfo->QueryInterface(IID_IMFMetadataProvider,
        (void**)&pProvider));

    // Get a pointer to IMFMetadata for file-wide metadata.
    CHECK_HR(hr = pProvider->GetMFMetadata(NULL, 0, 0, &pMetadata));

    // Get the property names that are stored in the metadata object.
    CHECK_HR(hr = pMetadata->GetAllPropertyNames(&varNames));

    // Loop through the properties and get their values.
    if (varNames.vt == (VT_VECTOR | VT_LPWSTR))
    {
        ULONG cElements = varNames.calpwstr.cElems;
        for (ULONG i = 0; i < cElements; i++)
        {
            const WCHAR* sName = varNames.calpwstr.pElems[i];
            CHECK_HR(hr = pMetadata->GetProperty(sName, &varValue));
            //Use the property values. Not shown.
            PropVariantClear(&varValue);
        }
    }
done:
    PropVariantClear(&varNames);
    PropVariantClear(&varValue);
    SAFE_RELEASE (pMetaData);
    SAFE_RELEASE (pProvider);
    return hr;
}
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Récepteurs de média ASF](asf-media-sinks.md)
</dt> <dt>

[Composants ASF de couche de pipeline](pipeline-layer-asf-components.md)
</dt> <dt>

[Prise en charge ASF dans Media Foundation](asf-support-in-media-foundation.md)
</dt> </dl>

 

 



