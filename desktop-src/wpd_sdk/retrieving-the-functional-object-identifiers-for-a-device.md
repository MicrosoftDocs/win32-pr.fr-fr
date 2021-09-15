---
description: Récupération des identificateurs d’objets fonctionnels pour un appareil
ms.assetid: 9a13071a-95a1-4330-92d5-11fa72a8f211
title: Récupération des identificateurs d’objets fonctionnels pour un appareil
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f6a753324e24a6b78625a78b4128380288b6672f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127522016"
---
# <a name="retrieving-the-functional-object-identifiers-for-a-device"></a>Récupération des identificateurs d’objets fonctionnels pour un appareil

comme indiqué dans la rubrique [récupération des catégories fonctionnelles prises en charge par un périphérique](retrieving-the-functional-categories-supported-by-a-device.md) , Windows appareils mobiles peuvent prendre en charge une ou plusieurs catégories fonctionnelles. Toute catégorie fonctionnelle donnée peut prendre en charge un ou plusieurs objets fonctionnels. Par exemple, la catégorie de stockage peut prendre en charge trois objets de stockage fonctionnels, chacun étant identifié par une chaîne d’identificateur unique. Le premier objet de stockage peut ensuite être identifié par la chaîne « Storage1 », le deuxième par la chaîne « Storage2 » et le troisième par la chaîne « Storage3 ».

La fonction ListFunctionalObjects dans le module DeviceCapabilities. cpp illustre la récupération des types de contenu pour les catégories fonctionnelles prises en charge par un périphérique sélectionné.

Votre application peut récupérer les catégories fonctionnelles prises en charge par un appareil à l’aide des interfaces décrites dans le tableau suivant.



| Interface                                                                                      | Description                                                   |
|------------------------------------------------------------------------------------------------|---------------------------------------------------------------|
| [**Interface IPortableDeviceCapabilities**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecapabilities)                   | Fournit l’accès aux méthodes de récupération de catégorie fonctionnelle. |
| [**Interface IPortableDevicePropVariantCollection**](iportabledevicepropvariantcollection.md) | Permet d’énumérer et de stocker les données de catégorie fonctionnelle.         |



 

Le code trouvé dans la fonction ListFunctionalObjects est presque identique au code trouvé dans la fonction ListFunctionalCategories. (Voir la rubrique [récupération des catégories fonctionnelles prises en charge par un appareil](retrieving-the-functional-categories-supported-by-a-device.md) .) La seule différence est l’appel à la méthode [**IPortableDeviceCapabilities :: GetFunctionalObjects**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicecapabilities-getfunctionalobjects) , qui apparaît dans la boucle qui itère au sein des catégories fonctionnelles.


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

// Loop through each functional category and get the list of
// functional object identifiers associated with a particular
// category.
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

                // Display the object identifiers for all
                // functional objects within this category
                CComPtr<IPortableDevicePropVariantCollection> pFunctionalObjectIds;
                hr = pCapabilities->GetFunctionalObjects(*pv.puuid, &pFunctionalObjectIds);
                if (SUCCEEDED(hr))
                {
                    printf("Functional Objects: ");
                    DisplayFunctionalObjectIDs(pFunctionalObjectIds);
                    printf("\n\n");
                }
                else
                {
                    printf("! Failed to get functional objects, hr = 0x%lx\n", hr);
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

 

 



