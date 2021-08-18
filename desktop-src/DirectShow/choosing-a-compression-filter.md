---
description: Choix d’un filtre de compression
ms.assetid: 9a2c3c48-771e-44db-a042-3db0fd9a6c76
title: Choix d’un filtre de compression
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cf964aa3647086efe569263e5fb36b4e0db60ebfad73c9d2fe9dcb14f3bcf125
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119999219"
---
# <a name="choosing-a-compression-filter"></a>Choix d’un filtre de compression

Plusieurs types de composants logiciels peuvent effectuer une compression vidéo ou audio, par exemple :

-   filtres de DirectShow natifs
-   Codecs du gestionnaire de compression vidéo (VCM)
-   Codecs de gestionnaire de compression audio (ACM)
-   Objets DMOs (DirectX Media Objects)

dans DirectShow, les codecs VCM sont encapsulés par le [filtre de compresseur AVI](avi-compressor-filter.md), et les codecs acm sont encapsulés par le [filtre de wrappers acm](acm-wrapper-filter.md). les DMOs sont encapsulés par le [filtre de Wrapper DMO](dmo-wrapper-filter.md). L’énumérateur de périphérique système fournit une méthode cohérente pour énumérer et créer l’un de ces types de compresseur, sans vous soucier du modèle sous-jacent.

Pour plus d’informations sur l’énumérateur de périphérique système, consultez [utilisation de l’énumérateur de périphérique système](using-the-system-device-enumerator.md). brièvement, tous les filtres de DirectShow sont classés par catégorie, et chaque catégorie est identifiée par un GUID. Pour les compresseurs vidéo, le GUID de la catégorie est CLSID \_ VideoCompressorCategory. Pour les compresseurs audio, il s’agit du CLSID \_ AudioCompressorCategory. Pour énumérer une catégorie particulière, l’énumérateur de périphérique système crée un objet *énumérateur* qui prend en charge l’interface [**IEnumMoniker**](/windows/desktop/api/objidl/nn-objidl-ienummoniker) . l’application utilise cette interface pour récupérer des monikers de périphérique, où chaque moniker de périphérique représente une instance d’un filtre de DirectShow. Vous pouvez utiliser le moniker pour créer le filtre, ou pour récupérer le nom convivial de l’appareil sans créer le filtre.

Pour énumérer les compresseurs vidéo ou audio disponibles sur le système de l’utilisateur, procédez comme suit :

1.  Appelez [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) pour créer l’énumérateur du périphérique système, qui a l’ID de classe CLSID \_ SystemDeviceEnum.
2.  Appelez [**ICreateDevEnum :: CreateClassEnumerator**](/windows/desktop/api/Strmif/nf-strmif-icreatedevenum-createclassenumerator) avec le GUID de catégorie de filtre. La méthode retourne un pointeur d’interface **IEnumMoniker** .
3.  Utilisez la méthode IEnumMoniker :: Next pour énumérer les monikers d’appareil. Cette méthode retourne une interface [**IMoniker**](/windows/desktop/api/objidl/nn-objidl-imoniker) , qui représente le moniker.

Pour obtenir le nom convivial d’un moniker, procédez comme suit :

1.  Appelez la méthode **IMoniker :: BindToStorage** . Cette méthode retourne un pointeur d’interface **IPropertyBag** .
2.  Utilisez la méthode **IPropertyBag :: Read** pour lire la propriété **FriendlyName** .

En règle générale, une application affiche une liste de compresseurs, afin que l’utilisateur puisse en choisir une. Par exemple, le code suivant remplit une zone de liste avec les noms des compressions vidéo disponibles.


```C++
void OnInitDialog(HWND hDlg)
{
    HRESULT hr;
    ICreateDevEnum *pSysDevEnum = NULL;
    IEnumMoniker *pEnum = NULL;
    IMoniker *pMoniker = NULL;

    hr = CoCreateInstance(CLSID_SystemDeviceEnum, NULL, 
        CLSCTX_INPROC_SERVER, IID_ICreateDevEnum, 
        (void**)&pSysDevEnum);
    if (FAILED(hr))
    {
        // Handle the error.
    }    

    hr = pSysDevEnum->CreateClassEnumerator(
             CLSID_VideoCompressorCategory, &pEnum, 0);
    if (hr == S_OK)  // S_FALSE means nothing in this category.
    {
        while (S_OK == pEnum->Next(1, &pMoniker, NULL))
        {
            IPropertyBag *pPropBag = NULL;
            pMoniker->BindToStorage(0, 0, IID_IPropertyBag, 
                (void **)&pPropBag);
            VARIANT var;
            VariantInit(&var);
            hr = pPropBag->Read(L"FriendlyName", &var, 0);
            if (SUCCEEDED(hr))
            {
                LRESULT iSel = AddString(GetDlgItem(hDlg, 
                    IDC_CODEC_LIST), var.bstrVal);
            }   
            VariantClear(&var); 
            pPropBag->Release();
            pMoniker->Release();
        }
    }

    SendDlgItemMessage(hDlg, IDC_CODEC_LIST, 
                       LB_SETCURSEL, 0, 0);
    pSysDevEnum->Release();
    pEnum->Release();
}
```



Pour créer une instance de filtre à partir du moniker, appelez la méthode **IMoniker :: BindToObject** . La méthode retourne un pointeur [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) .


```C++
IBaseFilter *pFilter = NULL;
hr = pMoniker->BindToObject(NULL, NULL, IID_IBaseFilter, 
                                       (void**)&pFilter);
if (SUCCEEDED(hr))
{
    // Use the filter. 
    // Remember to release the IBaseFilter interface.
}
```



Pour les codecs VCM, chaque moniker représente un codec particulier, même si tous les codecs sont encapsulés par le même filtre de compression AVI. L’appel de **BindToObject** crée une instance de ce filtre, initialisée pour ce codec. Pour cette raison, vous ne pouvez pas appeler **CoCreateInstance** directement sur le filtre de compression avi. Vous devez passer par l’énumérateur du périphérique système.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Recompression d’un fichier AVI](recompressing-an-avi-file.md)
</dt> </dl>

 

 
