---
description: Définition des propriétés d’un objet unique
ms.assetid: 1c003534-96b4-419b-94d1-73b5ffa2eba1
title: Définition des propriétés d’un objet unique
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5649d05ccadfeaef0dd8805abd7d556f7725f175
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106520779"
---
# <a name="setting-properties-for-a-single-object"></a>Définition des propriétés d’un objet unique

Une fois que votre application a récupéré un identificateur d’objet (voir la rubrique [énumération du contenu](enumerating-content.md) ) pour un objet donné, elle peut définir des propriétés pour cet objet en appelant des méthodes dans les interfaces décrites dans le tableau suivant.



| Interface                                                                | Description                                                                                                                                                 |
|--------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Interface IPortableDeviceProperties**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledeviceproperties) | Utilisé pour déterminer si une propriété donnée peut être écrite et pour envoyer l’opération d’écriture.                                                                  |
| [**Interface IPortableDeviceContent**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecontent)       | Fournit l’accès aux méthodes spécifiques au contenu.                                                                                                            |
| [**Interface IPortableDeviceValues**](iportabledevicevalues.md)         | Utilisé pour contenir les valeurs à écrire, déterminer les résultats de l’opération d’écriture et récupérer les attributs des propriétés (pour déterminer la capacité d’écriture). |



 

Les applications définissent des propriétés sur un objet en créant d’abord un jeu de propriétés qui spécifie les nouvelles valeurs à l’aide de l' [**interface IPortableDeviceValues**](iportabledevicevalues.md). Une fois que le conteneur de propriétés est créé, une application définit ces propriétés en appelant la méthode [**IPortableDeviceProperties :: SetValues**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledeviceproperties-setvalues) .

La `WriteContentProperties` fonction dans le module ContentProperties. cpp de l’exemple d’application montre comment une application peut définir une nouvelle propriété Object-Name pour un objet sélectionné.

La première tâche accomplie par la `WriteContentProperties` fonction consiste à inviter l’utilisateur à entrer un identificateur d’objet pour l’objet pour lequel l’application écrira le nouveau nom.


```C++
HRESULT                               hr                   = S_OK;
WCHAR                                 szSelection[81]      = {0};
WCHAR                                 szNewObjectName[81]  = {0};
CComPtr<IPortableDeviceProperties>    pProperties;
CComPtr<IPortableDeviceContent>       pContent;
CComPtr<IPortableDeviceValues>        pObjectPropertiesToWrite;
CComPtr<IPortableDeviceValues>        pPropertyWriteResults;
CComPtr<IPortableDeviceValues>        pAttributes;
BOOL                                  bCanWrite            = FALSE;

// Prompt user to enter an object identifier on the device to write properties on.
printf("Enter the identifer of the object you wish to write properties on.\n>");
hr = StringCbGetsW(szSelection,sizeof(szSelection));
if (FAILED(hr))
{
    printf("An invalid object identifier was specified, aborting property reading\n");
}
```



Après cela, l’application extrait l' \_ \_ attribut de propriété wpd \_ peut \_ écrire la valeur de la \_ propriété de nom d’objet wpd \_ pour déterminer si la propriété peut être écrite. (Notez que votre application peut définir n’importe quelle propriété pour laquelle l’API WPD \_ L' \_ attribut de propriété \_ peut \_ écrire la valeur true.)


```C++
if (SUCCEEDED(hr))
{
    hr = pDevice->Content(&pContent);
    if (FAILED(hr))
    {
        printf("! Failed to get IPortableDeviceContent from IPortableDevice, hr = 0x%lx\n",hr);
    }
}

// 2) Get an IPortableDeviceProperties interface from the IPortableDeviceContent interface
// to access the property-specific methods.
if (SUCCEEDED(hr))
{
    hr = pContent->Properties(&pProperties);
    if (FAILED(hr))
    {
        printf("! Failed to get IPortableDeviceProperties from IPortableDevice, hr = 0x%lx\n",hr);
    }
}

// 3) Check the property attributes to see if we can write/change the WPD_OBJECT_NAME property.
if (SUCCEEDED(hr))
{
    hr = pProperties->GetPropertyAttributes(szSelection,
                                            WPD_OBJECT_NAME,
                                            &pAttributes);
    if (SUCCEEDED(hr))
    {
        hr = pAttributes->GetBoolValue(WPD_PROPERTY_ATTRIBUTE_CAN_WRITE, &bCanWrite);
        if (SUCCEEDED(hr))
        {
            if (bCanWrite)
            {
                printf("The attribute WPD_PROPERTY_ATTRIBUTE_CAN_WRITE for the WPD_OBJECT_NAME reports TRUE\nThis means that the property can be changed/updated\n\n");
            }
            else
            {
                printf("The attribute WPD_PROPERTY_ATTRIBUTE_CAN_WRITE for the WPD_OBJECT_NAME reports FALSE\nThis means that the property cannot be changed/updated\n\n");
            }
        }
        else
        {
            printf("! Failed to get the WPD_PROPERTY_ATTRIBUTE_CAN_WRITE value from WPD_OBJECT_NAME on object '%ws', hr = 0x%lx\n",szSelection, hr);
        }
    }
}
```



L’étape suivante consiste à demander à l’utilisateur la nouvelle chaîne de nom. (Notez que l’appel à la méthode [**IPortableDeviceValues :: SetStringValue**](iportabledevicevalues-setstringvalue.md) crée simplement le conteneur de propriétés ; la propriété réelle n’a pas encore été écrite.)


```C++
if (bCanWrite)
{
    printf("Enter the new WPD_OBJECT_NAME for the object '%ws'.\n>",szSelection);
    hr = StringCbGetsW(szNewObjectName,sizeof(szNewObjectName));
    if (FAILED(hr))
    {
        printf("An invalid object name was specified, aborting property writing\n");
    }

    // 5) CoCreate an IPortableDeviceValues interface to hold the property values
    // we wish to write.
    if (SUCCEEDED(hr))
    {
        hr = CoCreateInstance(CLSID_PortableDeviceValues,
                              NULL,
                              CLSCTX_INPROC_SERVER,
                              IID_PPV_ARGS(&pObjectPropertiesToWrite));
        if (SUCCEEDED(hr))
        {
            if (pObjectPropertiesToWrite != NULL)
            {
                hr = pObjectPropertiesToWrite->SetStringValue(WPD_OBJECT_NAME, szNewObjectName);
                if (FAILED(hr))
                {
                    printf("! Failed to add WPD_OBJECT_NAME to IPortableDeviceValues, hr= 0x%lx\n", hr);
                }
            }
        }
    }
```



Enfin, la nouvelle valeur, spécifiée par l’utilisateur, est appliquée à l’objet.


```C++
if (SUCCEEDED(hr))
{
    hr = pProperties->SetValues(szSelection,                // The object whose properties we are reading
                                pObjectPropertiesToWrite,   // The properties we want to read
                                &pPropertyWriteResults);    // Driver supplied property result values for the property read operation
    if (FAILED(hr))
    {
        printf("! Failed to set properties for object '%ws', hr= 0x%lx\n", szSelection, hr);
    }
    else
    {
        printf("The WPD_OBJECT_NAME property on object '%ws' was written successfully (Read the properties again to see the updated value)\n", szSelection);
    }
}
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Interface IPortableDevice**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevice)
</dt> <dt>

[**Interface IPortableDeviceContent**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecontent)
</dt> <dt>

[**Interface IPortableDeviceKeyCollection**](iportabledevicekeycollection.md)
</dt> <dt>

[**Interface IPortableDeviceProperties**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledeviceproperties)
</dt> <dt>

[**Interface IPortableDevicePropertiesBulk**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevicepropertiesbulk)
</dt> <dt>

[**Interface IPortableDevicePropVariantCollection**](iportabledevicepropvariantcollection.md)
</dt> <dt>

[**Guide de programmation**](programming-guide.md)
</dt> </dl>

 

 



