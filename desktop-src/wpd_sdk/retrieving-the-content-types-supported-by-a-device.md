---
description: Récupération des types de contenu pris en charge par un appareil
ms.assetid: 1cedb8d9-2476-420c-bab4-c8a032af781b
title: Récupération des types de contenu pris en charge par un appareil
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4e1b37160065be3130fca687f5f3277d9108a6ea
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127522900"
---
# <a name="retrieving-the-content-types-supported-by-a-device"></a>Récupération des types de contenu pris en charge par un appareil

comme indiqué dans la rubrique [récupération des catégories fonctionnelles prises en charge par un périphérique](retrieving-the-functional-categories-supported-by-a-device.md) , Windows appareils mobiles peuvent prendre en charge une ou plusieurs catégories fonctionnelles. Toute catégorie fonctionnelle donnée peut prendre en charge un ou plusieurs types de contenu. Par exemple, la catégorie stockage peut prendre en charge les types de contenu de dossier, audio et image.

Pour obtenir une description des types de contenu pris en charge par WPD, consultez la rubrique [**\_ type de contenu wpd \_ \_ tout**](wpd-content-type-all.md) .

La fonction ListSupportedContentTypes dans le module DeviceCapabilities. cpp illustre la récupération des types de contenu pour les catégories fonctionnelles prises en charge par un périphérique sélectionné.

Votre application peut récupérer les catégories fonctionnelles prises en charge par un appareil à l’aide des interfaces décrites dans le tableau suivant.



| Interface                                                                                      | Description                                                   |
|------------------------------------------------------------------------------------------------|---------------------------------------------------------------|
| [**Interface IPortableDeviceCapabilities**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecapabilities)                   | Fournit l’accès aux méthodes de récupération de catégorie fonctionnelle. |
| [**Interface IPortableDevicePropVariantCollection**](iportabledevicepropvariantcollection.md) | Permet d’énumérer et de stocker les données de catégorie fonctionnelle.         |



 

Le code trouvé dans la fonction ListSupportedContentTypes est presque identique au code trouvé dans la fonction ListFunctionalCategories. (Voir la rubrique [récupération des catégories fonctionnelles prises en charge par un appareil](retrieving-the-functional-categories-supported-by-a-device.md) .) La seule différence est l’appel à la méthode [**IPortableDeviceCapabilities :: GetSupportedContentTypes**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicecapabilities-getsupportedcontenttypes) , qui apparaît dans la boucle qui itère au sein des catégories fonctionnelles.


```C++
HRESULT hr = S_OK;
CComPtr<IPortableDeviceCapabilities>            pCapabilities;
CComPtr<IPortableDevicePropVariantCollection>   pCategories;
DWORD dwNumCategories   = 0;

if (pDevice == NULL)
{
    printf("! A NULL IPortableDevice interface pointer was received\n");
    return;
}

// Get an IPortableDeviceCapabilities interface from the IPortableDevice interface to
// access the device capabilities-specific methods.
hr = pDevice->Capabilities(&pCapabilities);
if (FAILED(hr))
{
    printf("! Failed to get IPortableDeviceCapabilities from IPortableDevice, hr = 0x%lx\n",hr);
}

// Get all functional categories supported by the device.
// We will use these categories to enumerate functional objects
// that fall within them.
if (SUCCEEDED(hr))
{
    hr = pCapabilities->GetFunctionalCategories(&pCategories);
    if (FAILED(hr))
    {
        printf("! Failed to get functional categories from the device, hr = 0x%lx\n",hr);
    }
}

// Get the number of functional categories found on the device.
if (SUCCEEDED(hr))
{
    hr = pCategories->GetCount(&dwNumCategories);
    if (FAILED(hr))
    {
        printf("! Failed to get number of functional categories, hr = 0x%lx\n",hr);
    }
}

printf("\n%d Functional Categories Found on the device\n\n", dwNumCategories);

// Loop through each functional category and display its name and supported content types.
if (SUCCEEDED(hr))
{
    for (DWORD dwIndex = 0; dwIndex < dwNumCategories; dwIndex++)
    {
        PROPVARIANT pv = {0};
        PropVariantInit(&pv);
        hr = pCategories->GetAt(dwIndex, &pv);
        if (SUCCEEDED(hr))
        {
            // We have a functional category.  It is assumed that
            // functional categories are returned as VT_CLSID
            // VarTypes.

            if ((pv.puuid != NULL)      &&
                (pv.vt    == VT_CLSID))
            {
                // Display the functional category name
                printf("Functional Category: ");
                DisplayFunctionalCategory(*pv.puuid);
                printf("\n");

                // Display the content types supported for this category
                CComPtr<IPortableDevicePropVariantCollection> pContentTypes;
                hr = pCapabilities->GetSupportedContentTypes(*pv.puuid, &pContentTypes);
                if (SUCCEEDED(hr))
                {
                    printf("Supported Content Types: ");
                    DisplayContentTypes(pContentTypes);
                    printf("\n\n");
                }
                else
                {
                    printf("! Failed to get supported content types from the device, hr = 0x%lx\n",hr);
                }
            }
            else
            {
                printf("! Invalid functional category found\n");
            }
        }

        PropVariantClear(&pv);
    }
}
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Interface IPortableDevice**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevice)
</dt> <dt>

[**Interface IPortableDeviceCapabilities**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecapabilities)
</dt> <dt>

[**Interface IPortableDevicePropVariantCollection**](iportabledevicepropvariantcollection.md)
</dt> <dt>

[**Guide de programmation**](programming-guide.md)
</dt> </dl>

 

 



