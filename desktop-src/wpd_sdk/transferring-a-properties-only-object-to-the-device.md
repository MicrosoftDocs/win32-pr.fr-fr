---
description: Transfert d’un objet Properties-Only sur l’appareil
ms.assetid: 6305cff9-c0ce-4ef5-a129-bc329b9c563f
title: Transfert d’un objet Properties-Only sur l’appareil
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e20f9bcfecd46ea3047310ea5b946a366b35b9c7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103758451"
---
# <a name="transferring-a-properties-only-object-to-the-device"></a>Transfert d’un objet Properties-Only sur l’appareil

Bien que l’exemple de la rubrique précédente ait démontré la création de contenu sur un appareil constitué de propriétés et de données, cette rubrique se concentre sur la création d’un objet de propriétés uniquement.

Les transferts de propriété uniquement sont effectués à l’aide des interfaces décrites dans le tableau suivant.



| Interface                                                          | Description                                            |
|--------------------------------------------------------------------|--------------------------------------------------------|
| [**Interface IPortableDeviceContent**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecontent) | Fournit l’accès aux méthodes spécifiques au contenu.       |
| [**Interface IPortableDeviceValues**](iportabledevicevalues.md)   | Utilisé pour récupérer des propriétés qui décrivent le contenu. |



 

La `TransferContactToDevice` fonction dans le module ContentTransfer. cpp de l’exemple d’application montre comment une application peut transférer les informations de contact d’un PC vers un appareil connecté. Dans cet exemple, le nom du contact transféré est un « John Kane » codé en dur et le numéro de téléphone du contact transféré est toujours « 425-555-0123 ».

La première tâche accomplie par la `TransferContactToDevice` fonction consiste à inviter l’utilisateur à entrer un identificateur d’objet pour l’objet parent sur l’appareil (sous lequel le contenu sera transféré).


```C++
HRESULT                             hr = S_OK;
WCHAR                               szSelection[81]        = {0};
CComPtr<IPortableDeviceValues>      pFinalObjectProperties;
CComPtr<IPortableDeviceContent>     pContent;

// Prompt user to enter an object identifier for the parent object on the device to transfer.
printf("Enter the identifer of the parent object which the contact will be transferred under.\n>");
hr = StringCbGetsW(szSelection,sizeof(szSelection));
if (FAILED(hr))
{
    printf("An invalid object identifier was specified, aborting content transfer\n");
}
```



L’étape suivante est la récupération des propriétés de contact, qui sera utilisée lorsque l’exemple écrit le nouveau contact sur l’appareil. La récupération des propriétés de contact est effectuée par la `GetRequiredPropertiesForPropertiesOnlyContact` fonction d’assistance.


```C++
// 2) Get the properties that describe the object being created on the device

if (SUCCEEDED(hr))
{
    hr = GetRequiredPropertiesForPropertiesOnlyContact(szSelection,              // Parent to transfer the data under
                                                       &pFinalObjectProperties);  // Returned properties describing the data
    if (FAILED(hr))
    {
        printf("! Failed to get required properties needed to transfer an image file to the device, hr = 0x%lx\n", hr);
    }
}
```



Cette fonction écrit les données suivantes dans un objet **IPortableDeviceValues** .

-   Identificateur d’objet pour le parent du contact sur l’appareil. (Il s’agit de la destination dans laquelle l’appareil stockera l’objet.)
-   Type d’objet (un contact).
-   Nom du contact (chaîne codée en dur de « John Kane »).
-   Numéro de téléphone du contact (chaîne codée en dur « 425-555-0123 »).

La dernière étape crée l’objet Propriétés uniquement sur l’appareil (à l’aide des propriétés définies par la `GetRequiredPropertiesForPropertiesOnlyContact` fonction d’assistance). Pour ce faire, vous devez appeler la méthode **IPortableDeviceContent :: CreateObjectWithPropertiesOnly** .


```C++
if (SUCCEEDED(hr))
{
    PWSTR pszNewlyCreatedObject = NULL;
    hr = pContent->CreateObjectWithPropertiesOnly(pFinalObjectProperties,    // Properties describing the object data
                                                  &pszNewlyCreatedObject);
    if (SUCCEEDED(hr))
    {
        printf("The contact was transferred to the device.\nThe newly created object's ID is '%ws'\n",pszNewlyCreatedObject);
    }

    if (FAILED(hr))
    {
        printf("! Failed to transfer contact object to the device, hr = 0x%lx\n",hr);
    }

    // Free the object identifier string returned from CreateObjectWithPropertiesOnly
    CoTaskMemFree(pszNewlyCreatedObject);
    pszNewlyCreatedObject = NULL;
}
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Interface IPortableDevice**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevice)
</dt> <dt>

[**Interface IPortableDeviceContent**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecontent)
</dt> <dt>

[**Interface IPortableDeviceValues**](iportabledevicevalues.md)
</dt> <dt>

[**Guide de programmation**](programming-guide.md)
</dt> </dl>

 

 



