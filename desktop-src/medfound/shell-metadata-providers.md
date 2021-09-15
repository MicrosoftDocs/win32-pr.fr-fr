---
description: à partir de Windows 7, Microsoft Media Foundation expose des métadonnées par le biais de l’interface IPropertyStore.
ms.assetid: d219d3f1-3940-46ed-9811-3cf8bf1eec55
title: Fournisseurs de métadonnées de Shell
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 35488e750531a5ee7bac7dc915990593ecee1d10
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127525632"
---
# <a name="shell-metadata-providers"></a>Fournisseurs de métadonnées de Shell

à partir de Windows 7, Microsoft Media Foundation expose des métadonnées par le biais de l’interface [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) .

Les métadonnées obtenues à l’aide du processus défini dans cette rubrique doivent être utilisées uniquement pour l’accès en lecture seule. L’écriture de données à l’aide de ce processus n’est pas prise en charge. Vous pouvez créer un objet [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) à des fins d’écriture à l’aide d’un identificateur de classe (CLSID) obtenu à partir de [**PSLookupPropertyHandlerCLSID**](/windows/win32/api/propsys/nf-propsys-pslookuppropertyhandlerclsid).

## <a name="reading-metadata"></a>Lecture des métadonnées

Pour lire les métadonnées d’une source de média, procédez comme suit :

1.  Obtient un pointeur vers l’interface [**IMFMediaSource**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource) de la source du média. Vous pouvez utiliser l’interface [**IMFSourceResolver**](/windows/desktop/api/mfidl/nn-mfidl-imfsourceresolver) pour récupérer un pointeur **IMFMediaSource** .
2.  Appelez [**MFGetService**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice) sur la source du média pour obtenir un pointeur vers l’interface [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) . Dans le paramètre *guidService* de **MFGetService**, spécifiez la **valeur \_ \_ \_ service du gestionnaire de propriétés MF**. Si la source ne prend pas en charge l’interface **IPropertyStore** , **MFGetService** retourne le **\_ service MF E \_ non pris en charge \_**.
3.  Appelez les méthodes [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) pour énumérer les propriétés de métadonnées.

Le code suivant illustre ces étapes. Supposons que `DisplayProperty` est une fonction qui affiche une valeur **PROPVARIANT** .


```C++
HRESULT EnumerateMetadata(IMFMediaSource *pSource)
{
    IPropertyStore *pProps = NULL;

    HRESULT hr = MFGetService(
        pSource, MF_PROPERTY_HANDLER_SERVICE, IID_PPV_ARGS(&pProps));

    if (FAILED(hr))
    {
        goto done;
    }

    DWORD cProps;

    hr = pProps->GetCount(&cProps);
    if (FAILED(hr))
    {
        goto done;
    }

    for (DWORD i = 0; i < cProps; i++)
    {
        PROPERTYKEY key;
        hr = pProps->GetAt(i, &key);
        if (FAILED(hr))
        {
            goto done;
        }

        PROPVARIANT pv;

        hr = pProps->GetValue(key, &pv);
        if (FAILED(hr))
        {
            goto done;
        }

        DisplayProperty(key, pv);
        PropVariantClear(&pv);
    }

done:
    SafeRelease(&pProps);
    return hr;
}
```



Pour obtenir la liste des clés de propriété de métadonnées, consultez [Propriétés de métadonnées pour les fichiers multimédias](metadata-properties-for-media-files.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Métadonnées de média](media-metadata.md)
</dt> </dl>

 

 
