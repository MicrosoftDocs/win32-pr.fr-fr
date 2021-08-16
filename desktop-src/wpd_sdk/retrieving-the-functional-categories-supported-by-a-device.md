---
description: Récupération des catégories fonctionnelles prises en charge par un appareil
ms.assetid: 7748e111-9987-4685-8fc8-10c5d4631080
title: Récupération des catégories fonctionnelles prises en charge par un appareil
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d410788616cc20563b914a293afcd8e2bbbd87099f738ae21463d2092c620597
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117842691"
---
# <a name="retrieving-the-functional-categories-supported-by-a-device"></a>Récupération des catégories fonctionnelles prises en charge par un appareil

Windows Les appareils mobiles peuvent prendre en charge une ou plusieurs catégories fonctionnelles. Ces catégories sont décrites dans le tableau suivant.



| Category                    | Description                                                                          |
|-----------------------------|--------------------------------------------------------------------------------------|
| Capture audio               | L’appareil peut être utilisé pour enregistrer l’audio.                                              |
| Informations de rendu       | L’appareil fournit des données décrivant les fichiers multimédias qu’il est capable de rendre. |
| SMS (Short Message Service) | L’appareil prend en charge la messagerie texte.                                                  |
| Capture d’image continue         | L’appareil peut être utilisé pour capturer des images fixes.                                      |
| Stockage                     | L’appareil peut être utilisé pour stocker des fichiers.                                               |



 

La fonction ListFunctionalCategories dans le module DeviceCapabilities. cpp illustre la récupération des catégories fonctionnelles pour un appareil sélectionné.

Votre application peut récupérer les catégories fonctionnelles prises en charge par un appareil à l’aide des interfaces décrites dans le tableau suivant.



| Interface                                                                                      | Description                                                   |
|------------------------------------------------------------------------------------------------|---------------------------------------------------------------|
| [**Interface IPortableDeviceCapabilities**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecapabilities)                   | Fournit l’accès aux méthodes de récupération de catégorie fonctionnelle. |
| [**Interface IPortableDevicePropVariantCollection**](iportabledevicepropvariantcollection.md) | Permet d’énumérer et de stocker les données de catégorie fonctionnelle.         |



 

La première tâche accomplie par l’exemple d’application est la récupération d’un objet [**IPortableDeviceCapabilities**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecapabilities) , qui est utilisé pour récupérer les catégories fonctionnelles sur l’appareil sélectionné.


```C++
HRESULT hr = S_OK;
CComPtr<IPortableDeviceCapabilities>            pCapabilities;
CComPtr<IPortableDevicePropVariantCollection>   pCategories;
DWORD dwNumCategories = 0;

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
if (SUCCEEDED(hr))
{
    hr = pCapabilities->GetFunctionalCategories(&pCategories);
    if (FAILED(hr))
    {
        printf("! Failed to get functional categories from the device, hr = 0x%lx\n",hr);
    }
}
```



Les catégories récupérées sont stockées dans un objet [**IPortableDevicePropVariantCollection**](iportabledevicepropvariantcollection.md) .

L’étape suivante est l’énumération et l’affichage des catégories prises en charge. La première étape que l’exemple d’application effectue est de récupérer le nombre de catégories prises en charge. Il utilise ensuite ce nombre pour itérer au sein de l’objet [**IPortableDevicePropVariantCollection**](iportabledevicepropvariantcollection.md) qui contient les catégories prises en charge.


```C++
if (SUCCEEDED(hr))
{
    hr = pCategories->GetCount(&dwNumCategories);
    if (FAILED(hr))
    {
        printf("! Failed to get number of functional categories, hr = 0x%lx\n",hr);
    }
}

printf("\n%d Functional Categories Found on the device\n\n", dwNumCategories);

// Loop through each functional category and display its name
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

            if (pv.puuid != NULL)
            {
                // Display the functional category name
                DisplayFunctionalCategory(*pv.puuid);
                printf("\n");
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

 

 



