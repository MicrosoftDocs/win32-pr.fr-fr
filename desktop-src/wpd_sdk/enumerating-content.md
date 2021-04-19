---
description: Énumération du contenu
ms.assetid: 86782a09-4fca-4ae0-beaf-296069e061dc
title: Énumération du contenu
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1b2e724b451d714516c4723edcd56936b71e4e50
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106536967"
---
# <a name="enumerating-content"></a>Énumération du contenu

Le contenu d’un appareil (qu’il s’agisse d’un dossier, d’un annuaire, d’une vidéo ou d’une image fixe) est appelé un objet dans l’API WPD. Ces objets sont référencés par des identificateurs d’objet et décrits par des propriétés. Vous pouvez énumérer les objets sur un appareil en appelant des méthodes dans l' [**interface IPortableDevice**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevice), l' [**interface IPortableDeviceContent**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecontent)et l' [**interface IEnumPortableDeviceObjectIDs**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-ienumportabledeviceobjectids).

L’exemple d’application montre l’énumération du contenu dans la fonction EnumerateAllContent, qui se trouve dans le module ContentEnumeration. cpp. Cette fonction appelle à son tour une fonction RecursiveEnumerate qui parcourt la hiérarchie des objets trouvés sur l’appareil sélectionné et retourne un identificateur d’objet pour chaque objet.

Comme indiqué, la fonction RecursiveEnumerate récupère un identificateur d’objet pour chaque objet trouvé sur l’appareil. L’identificateur d’objet est une valeur de chaîne. Une fois que votre application a récupéré cet identificateur, elle peut obtenir des informations plus descriptives sur l’objet (par exemple, le nom de l’objet, l’identificateur pour le parent de l’objet, etc.). Ces informations descriptives sont appelées propriétés d’objet (ou métadonnées). Votre application peut récupérer ces propriétés en appelant les membres de l' [**interface IPortableDeviceProperties**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledeviceproperties).

La fonction EnumerateAllContent commence par récupérer un pointeur vers une [**interface IPortableDeviceContent**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecontent). Il récupère ce pointeur en appelant la méthode [**IPortableDevice :: content**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-content) .


```C++
void EnumerateAllContent(
    IPortableDevice* pDevice)
{
    HRESULT                         hr = S_OK;
    CComPtr<IPortableDeviceContent> pContent;

    if (pDevice == NULL)
    {
        printf("! A NULL IPortableDevice interface pointer was received\n");
        return;
    }

    // Get an IPortableDeviceContent interface from the IPortableDevice interface to
    // access the content-specific methods.
    hr = pDevice->Content(&pContent);
    if (FAILED(hr))
    {
        printf("! Failed to get IPortableDeviceContent from IPortableDevice, hr = 0x%lx\n",hr);
    }

    // Enumerate content starting from the "DEVICE" object.
    if (SUCCEEDED(hr))
    {
        printf("\n");
        RecursiveEnumerate(WPD_DEVICE_OBJECT_ID, pContent);
    }
}
```



Une fois qu’il a récupéré le pointeur vers l’interface IPortableDeviceContent, la fonction EnumerateAllContent appelle la fonction RecursiveEnumerate, qui parcourt la hiérarchie des objets trouvés sur le périphérique donné et retourne un identificateur d’objet pour chacun d’eux.

La fonction RecursiveEnumerate commence par récupérer un pointeur vers une [**interface IEnumPortableDeviceObjectIDs**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-ienumportabledeviceobjectids). Cette interface expose les méthodes utilisées par une application pour naviguer dans la liste des objets trouvés sur un appareil donné.

Dans cet exemple, la fonction RecursiveEnumerate appelle la méthode [**IEnumPortableDeviceObjectIDs :: Next**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-ienumportabledeviceobjectids-next) pour parcourir la liste d’objets.

Chaque appel à la méthode [**IEnumPortableDeviceObjects :: Next**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-ienumportabledeviceobjectids-next) demande un lot de 10 identificateurs. (Cette valeur est spécifiée par le nombre \_ OBJETS \_ pour \_ demander une constante fournie comme premier argument.)


```C++
#define NUM_OBJECTS_TO_REQUEST  10

// Recursively called function which enumerates using the specified
// object identifier as the parent.
void RecursiveEnumerate(
    PCWSTR                  pszObjectID,
    IPortableDeviceContent* pContent)
{
    CComPtr<IEnumPortableDeviceObjectIDs> pEnumObjectIDs;

    // Print the object identifier being used as the parent during enumeration.
    printf("%ws\n",pszObjectID);

    // Get an IEnumPortableDeviceObjectIDs interface by calling EnumObjects with the
    // specified parent object identifier.
    HRESULT hr = pContent->EnumObjects(0,               // Flags are unused
                                       pszObjectID,     // Starting from the passed in object
                                       NULL,            // Filter is unused
                                       &pEnumObjectIDs);
    if (FAILED(hr))
    {
        printf("! Failed to get IEnumPortableDeviceObjectIDs from IPortableDeviceContent, hr = 0x%lx\n",hr);
    }

    // Loop calling Next() while S_OK is being returned.
    while(hr == S_OK)
    {
        DWORD  cFetched = 0;
        PWSTR  szObjectIDArray[NUM_OBJECTS_TO_REQUEST] = {0};
        hr = pEnumObjectIDs->Next(NUM_OBJECTS_TO_REQUEST,   // Number of objects to request on each NEXT call
                                  szObjectIDArray,          // Array of PWSTR array which will be populated on each NEXT call
                                  &cFetched);               // Number of objects written to the PWSTR array
        if (SUCCEEDED(hr))
        {
            // Traverse the results of the Next() operation and recursively enumerate
            // Remember to free all returned object identifiers using CoTaskMemFree()
            for (DWORD dwIndex = 0; dwIndex < cFetched; dwIndex++)
            {
                RecursiveEnumerate(szObjectIDArray[dwIndex],pContent);

                // Free allocated PWSTRs after the recursive enumeration call has completed.
                CoTaskMemFree(szObjectIDArray[dwIndex]);
                szObjectIDArray[dwIndex] = NULL;
            }
        }
    }
}
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Interface IEnumPortableDeviceObjectIDs**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-ienumportabledeviceobjectids)
</dt> <dt>

[**Interface IPortableDevice**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevice)
</dt> <dt>

[**Interface IPortableDeviceContent**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecontent)
</dt> <dt>

[**Interface IPortableDeviceProperties**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledeviceproperties)
</dt> <dt>

[**Guide de programmation**](programming-guide.md)
</dt> </dl>

 

 



