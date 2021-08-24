---
description: Récupération des propriétés de plusieurs objets
ms.assetid: 0d0c6b3d-23bc-4628-a684-14bb9e18967f
title: Récupération des propriétés de plusieurs objets
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d1ad9ec397daa90c149fe950c1fc4777c407e3f5f3a359f46cf8bef56e18b9f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119083513"
---
# <a name="retrieving-properties-for-multiple-objects"></a>Récupération des propriétés de plusieurs objets

Certains pilotes de périphériques prennent en charge la récupération des propriétés de plusieurs objets dans un appel de fonction unique. C’est ce qu’on appelle une récupération en bloc. Il existe deux types d’opérations de récupération en bloc : le premier type récupère les propriétés d’une liste d’objets, et le deuxième type récupère les propriétés pour tous les objets d’un format donné. L’exemple décrit dans cette section illustre la première.

Votre application peut effectuer une récupération en bloc à l’aide des interfaces décrites dans le tableau suivant.



| Interface                                                                                      | Description                                                        |
|------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| [**Interface IPortableDeviceContent**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecontent)                             | Fournit l’accès aux méthodes spécifiques au contenu.                   |
| [**Interface IPortableDeviceKeyCollection**](iportabledevicekeycollection.md)                 | Utilisé pour identifier les propriétés à récupérer.                   |
| [**Interface IPortableDeviceProperties**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledeviceproperties)                       | Utilisé pour déterminer si un pilote donné prend en charge les opérations en bloc. |
| [**Interface IPortableDevicePropertiesBulk**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevicepropertiesbulk)               | Prend en charge l’opération de récupération en bloc.                             |
| [**Interface IPortableDevicePropVariantCollection**](iportabledevicepropvariantcollection.md) | Utilisé pour stocker les identificateurs d’objet pour l’opération en bloc.       |



 

La fonction ReadContentPropertiesBulk dans le module ContentProperties. cpp de l’exemple d’application illustre une opération de récupération en bloc.

La première tâche accomplie dans cet exemple consiste à déterminer si le pilote donné prend en charge les opérations en bloc. Cela s’effectue en appelant QueryInterface sur l’interface IPortableDeviceProperties et en vérifiant l’existence de IPortableDevicePropertiesBulk.


```C++
HRESULT                                       hr                = S_OK;
GUID                                          guidContext       = GUID_NULL;
CGetBulkValuesCallback*                       pCallback         = NULL;
CComPtr<IPortableDeviceProperties>            pProperties;
CComPtr<IPortableDevicePropertiesBulk>        pPropertiesBulk;
CComPtr<IPortableDeviceValues>                pObjectProperties;
CComPtr<IPortableDeviceContent>               pContent;
CComPtr<IPortableDeviceKeyCollection>         pPropertiesToRead;
CComPtr<IPortableDevicePropVariantCollection> pObjectIDs;


if (SUCCEEDED(hr))
{
    hr = pDevice->Content(&pContent);
    if (FAILED(hr))
    {
        printf("! Failed to get IPortableDeviceContent from IPortableDevice, hr = 0x%lx\n",hr);
    }
}



if (SUCCEEDED(hr))
{
    hr = pContent->Properties(&pProperties);
    if (FAILED(hr))
    {
        printf("! Failed to get IPortableDeviceProperties from IPortableDevice, hr = 0x%lx\n",hr);
    }
}



if (SUCCEEDED(hr))
{
    hr = pProperties->QueryInterface(IID_PPV_ARGS(&pPropertiesBulk));
    if (FAILED(hr))
    {
        printf("This driver does not support BULK property operations.\n");
    }
}
```



Si le pilote prend en charge les opérations en bloc, l’étape suivante consiste à créer une instance de l' [**interface IPortableDeviceKeyCollection**](iportabledevicekeycollection.md) et à spécifier les clés qui correspondent aux propriétés que l’application doit récupérer. Pour obtenir une description de ce processus, consultez la rubrique [extraction des propriétés pour un seul objet](retrieving-properties-for-a-single-object.md) .

Une fois les clés appropriées spécifiées, l’exemple d’application crée une instance de l' [**interface IPortableDevicePropertiesBulkCallback**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevicepropertiesbulk). L’application utilisera les méthodes dans cette interface pour suivre la progression de l’opération asynchrone de récupération en bloc.


```C++
if (SUCCEEDED(hr))
{
    pCallback = new CGetBulkValuesCallback();
    if (pCallback == NULL)
    {
        hr = E_OUTOFMEMORY;
        printf("! Failed to allocate CGetBulkValuesCallback, hr = 0x%lx\n", hr);
    }
}
```



La fonction suivante appelée par l’exemple d’application est la fonction d’assistance CreateIPortableDevicePropVariantCollectionWithAllObjectIDs. Cette fonction crée une liste de tous les identificateurs d’objets disponibles à titre d’exemple. (Une application réelle limiterait la liste des identificateurs à un ensemble d’objets particulier. Par exemple, une application peut créer une liste d’identificateurs pour tous les objets actuellement dans une vue de dossier donnée.)

Comme indiqué ci-dessus, la fonction d’assistance énumère de manière récursive tous les objets sur un appareil donné. Elle retourne cette liste dans une [**interface IPortableDevicePropVariantCollection**](iportabledevicepropvariantcollection.md) qui contient un identificateur pour chaque objet trouvé. La fonction d’assistance est définie dans le module ContentEnumeration. cpp.


```C++
// 7) Call our helper function CreateIPortableDevicePropVariantCollectionWithAllObjectIDs
// to enumerate and create an IPortableDevicePropVariantCollection with the object
// identifiers needed to perform the bulk operation on.
if (SUCCEEDED(hr))
{
    hr = CreateIPortableDevicePropVariantCollectionWithAllObjectIDs(pDevice,
                                                                    pContent,
                                                                    &pObjectIDs);
}
```



Une fois les étapes précédentes effectuées, l’exemple d’application lance la récupération de propriété asynchrone. Pour ce faire, procédez comme suit :

1.  Appel de IPortableDevicePropertiesBulk :: QueueGetValuesByObjectList, qui met en file d’attente une demande pour la récupération de propriété en bloc. (Notez que même si la demande est mise en file d’attente, elle n’est pas démarrée.)
2.  Appel de IPortableDevicePropertiesBulk :: Start pour initier la demande en file d’attente.

Ces étapes sont présentées dans l’extrait de code suivant de l’exemple d’application.


```C++
   if (SUCCEEDED(hr))
   {
       hr = pPropertiesBulk->QueueGetValuesByObjectList(pObjectIDs,
                                                        pPropertiesToRead,
                                                        pCallback,
                                                        &guidContext);


       if(SUCCEEDED(hr))
       {
           // Cleanup any previously created global event handles.
           if (g_hBulkPropertyOperationEvent != NULL)
           {
               CloseHandle(g_hBulkPropertyOperationEvent);
               g_hBulkPropertyOperationEvent = NULL;
           }

           // In order to create a simpler to follow example we create and wait infinitly
           // for the bulk property operation to complete and ignore any errors.
           // Production code should be written in a more robust manner.
           // Create the global event handle to wait on for the bulk operation
           // to complete.
           g_hBulkPropertyOperationEvent = CreateEvent(NULL, FALSE, FALSE, NULL);
           if (g_hBulkPropertyOperationEvent != NULL)
           {
               // Call Start() to actually being the Asynchronous bulk operation.
               hr = pPropertiesBulk->Start(guidContext);
               if(FAILED(hr))
               {
                   printf("! Failed to start property operation, hr = 0x%lx\n", hr);
               }
           }
           else
           {
               printf("! Failed to create the global event handle to wait on for the bulk operation. Aborting operation.\n");
           }
       }
       else
       {
           printf("! QueueGetValuesByObjectList Failed, hr = 0x%lx\n", hr);
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

 

 



