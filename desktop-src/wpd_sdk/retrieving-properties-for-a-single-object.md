---
description: Récupération des propriétés d’un objet unique
ms.assetid: e4e3b286-6330-4147-a367-57accf5beae6
title: Récupération des propriétés d’un objet unique
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5851b31256659c2ca036bac504a53fa51a20ee14
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127522912"
---
# <a name="retrieving-properties-for-a-single-object"></a>Récupération des propriétés d’un objet unique

Une fois que votre application a récupéré un identificateur d’objet (voir la rubrique [énumération du contenu](enumerating-content.md) ) pour un objet donné, elle peut récupérer des informations descriptives sur cet objet en appelant des méthodes dans l' [**interface IPortableDeviceProperties**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledeviceproperties) et l' [**interface IPortableDeviceKeyCollection**](iportabledevicekeycollection.md).

La méthode [**IPortableDeviceProperties :: GetValues**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledeviceproperties-getvalues) récupère une liste des propriétés spécifiées pour un objet donné. (Votre application peut également appeler la méthode GetValues et spécifier une valeur **null** pour le paramètre pKeys pour récupérer toutes les propriétés d’un objet donné ; toutefois, les performances de cette méthode peuvent être beaucoup plus lentes lors de la récupération de toutes les propriétés.)

Toutefois, avant que votre application appelle GetValue, il doit identifier les propriétés à récupérer en définissant les clés correspondantes dans un [**objet IPortableDeviceKeyCollection**](iportabledevicekeycollection.md). Votre application identifie les propriétés qui vous intéressent en appelant la méthode [**IPortableDeviceKeyCollection :: Add**](iportabledevicekeycollection-add.md) et en fournissant une valeur PROPERTYKEY qui identifie chaque propriété qu’elle va récupérer.

La fonction ReadContentProperties dans le module ContentProperties. cpp de l’exemple d’application montre comment les cinq propriétés ont été récupérées pour un objet sélectionné. Le tableau suivant décrit chacune de ces propriétés et leur valeur REFPROPERTYKEY correspondante.



| Propriété                     | Description                                                                                                                                      | PROPERTYKEY                         |
|------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------|
| Identificateur de l’objet parent     | Chaîne qui spécifie l’identificateur pour le parent de l’objet donné.                                                                            | \_ \_ ID parent de l’objet wpd \_             |
| Nom d’objet                  | Chaîne qui spécifie le nom de l’objet donné.                                                                                            | nom de l' \_ objet wpd \_                   |
| Identificateur unique persistant | Chaîne qui spécifie un identificateur unique pour l’objet donné. (Cet identificateur est persistant entre les sessions, contrairement à l’identificateur d’objet.) | \_ \_ \_ ID unique persistant de l’objet wpd \_ |
| Format de l’objet                | Identificateur global unique (GUID) qui spécifie le format du fichier correspondant à un objet donné.                                       | \_format d’objet wpd \_                 |
| Type de contenu d’objet          | GUID qui spécifie le type de contenu associé à un objet donné.                                                                        | TYPE de contenu de l' \_ objet wpd \_ \_          |



 

L’extrait suivant de la fonction ReadContentProperties montre comment l’exemple d’application a utilisé l' [**interface IPortableDeviceKeyCollection**](iportabledevicekeycollection.md) et la méthode [**IPortableDeviceKeyCollection :: Add**](iportabledevicekeycollection-add.md) pour identifier les propriétés qu’elle récupérerait.


```C++
hr = CoCreateInstance(CLSID_PortableDeviceKeyCollection,
                      NULL,
                      CLSCTX_INPROC_SERVER,
                      IID_PPV_ARGS(&pPropertiesToRead));
if (SUCCEEDED(hr))
{
    // 4) Populate the IPortableDeviceKeyCollection with the keys we wish to read.
    // NOTE: We are not handling any special error cases here so we can proceed with
    // adding as many of the target properties as we can.
    if (pPropertiesToRead != NULL)
    {
        HRESULT hrTemp = S_OK;
        hrTemp = pPropertiesToRead->Add(WPD_OBJECT_PARENT_ID);
        if (FAILED(hrTemp))
        {
            printf("! Failed to add WPD_OBJECT_PARENT_ID to IPortableDeviceKeyCollection, hr= 0x%lx\n", hrTemp);
        }

        hrTemp = pPropertiesToRead->Add(WPD_OBJECT_NAME);
        if (FAILED(hrTemp))
        {
            printf("! Failed to add WPD_OBJECT_NAME to IPortableDeviceKeyCollection, hr= 0x%lx\n", hrTemp);
        }

        hrTemp = pPropertiesToRead->Add(WPD_OBJECT_PERSISTENT_UNIQUE_ID);
        if (FAILED(hrTemp))
        {
            printf("! Failed to add WPD_OBJECT_PERSISTENT_UNIQUE_ID to IPortableDeviceKeyCollection, hr= 0x%lx\n", hrTemp);
        }

        hrTemp = pPropertiesToRead->Add(WPD_OBJECT_FORMAT);
        if (FAILED(hrTemp))
        {
            printf("! Failed to add WPD_OBJECT_FORMAT to IPortableDeviceKeyCollection, hr= 0x%lx\n", hrTemp);
        }

        hrTemp = pPropertiesToRead->Add(WPD_OBJECT_CONTENT_TYPE);
        if (FAILED(hrTemp))
        {
            printf("! Failed to add WPD_OBJECT_CONTENT_TYPE to IPortableDeviceKeyCollection, hr= 0x%lx\n", hrTemp);
        }
    }
}
```



Une fois que l’exemple d’application a défini les clés appropriées, il a appelé la méthode [**IPortableDeviceProperties :: GetValues**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledeviceproperties-getvalues) pour récupérer les valeurs spécifiées pour l’objet donné.


```C++
if (SUCCEEDED(hr))
{
    hr = pProperties->GetValues(szSelection,         // The object whose properties we are reading
                                pPropertiesToRead,   // The properties we want to read
                                &pObjectProperties); // Driver supplied property values for the specified object
    if (FAILED(hr))
    {
        printf("! Failed to get all properties for object '%ws', hr= 0x%lx\n", szSelection, hr);
    }
}
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Interface IPortableDevice**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevice)
</dt> <dt>

[**Interface IPortableDeviceKeyCollection**](iportabledevicekeycollection.md)
</dt> <dt>

[**Interface IPortableDeviceProperties**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledeviceproperties)
</dt> <dt>

[**Guide de programmation**](programming-guide.md)
</dt> </dl>

 

 



