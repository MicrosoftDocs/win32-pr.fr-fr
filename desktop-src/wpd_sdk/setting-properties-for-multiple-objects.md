---
description: Définition des propriétés de plusieurs objets
ms.assetid: 0686ba54-4782-42a4-8fdb-2325fc8d8bc2
title: Définition des propriétés de plusieurs objets
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e951662d9920cb22db0a417f1af94f3eb7eb4d7
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127522889"
---
# <a name="setting-properties-for-multiple-objects"></a>Définition des propriétés de plusieurs objets

Certains pilotes de périphériques prennent en charge la définition des propriétés de plusieurs objets dans un appel de fonction unique, appelée écriture en bloc. Votre application peut effectuer une écriture en bloc à l’aide des interfaces décrites dans le tableau suivant.



| Interface                                                                                      | Description                                                  |
|------------------------------------------------------------------------------------------------|--------------------------------------------------------------|
| [**Interface IPortableDeviceContent**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecontent)                             | Fournit l’accès aux méthodes spécifiques au contenu.             |
| [**Interface IPortableDeviceProperties**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledeviceproperties)                       | Fournit l’accès aux méthodes spécifiques à la propriété.            |
| [**Interface IPortableDevicePropertiesBulk**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevicepropertiesbulk)               | Prend en charge l’opération d’écriture en bloc.                           |
| [**Interface IPortableDevicePropVariantCollection**](iportabledevicepropvariantcollection.md) | Utilisé pour stocker les identificateurs d’objet pour l’opération en bloc. |
| [**Interface IPortableDeviceValuesCollection**](iportabledevicevaluescollection.md)           | Utilisé pour identifier les propriétés à écrire.               |



 

La `WriteContentPropertiesBulk` fonction dans le module ContentProperties. cpp de l’exemple d’application illustre une opération d’écriture en bloc.

La première tâche accomplie dans cet exemple consiste à déterminer si le pilote donné prend en charge les opérations en bloc. Pour ce faire, appelez QueryInterface sur un objet **IPortableDeviceProperties** et vérifiez l’existence de **IPortableDevicePropertiesBulk**.


```C++
HRESULT                                       hr                = S_OK;
GUID                                          guidContext       = GUID_NULL;
CSetBulkValuesCallback*                       pCallback         = NULL;
CComPtr<IPortableDeviceProperties>            pProperties;
CComPtr<IPortableDevicePropertiesBulk>        pPropertiesBulk;
CComPtr<IPortableDeviceValues>                pObjectProperties;
CComPtr<IPortableDeviceContent>               pContent;
CComPtr<IPortableDeviceValuesCollection>      pPropertiesToWrite;
CComPtr<IPortableDevicePropVariantCollection> pObjectIDs;
DWORD                                         cObjectIDs        = 0;
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



La tâche suivante entraîne la création d’un objet **IPortableDeviceValuesCollection** . Il s’agit de l’objet qui contient les valeurs de propriété que l’exemple écrira.


```C++
HRESULT                                       hr                = S_OK;
GUID                                          guidContext       = GUID_NULL;
CSetBulkValuesCallback*                       pCallback         = NULL;
CComPtr<IPortableDeviceProperties>            pProperties;
CComPtr<IPortableDevicePropertiesBulk>        pPropertiesBulk;
CComPtr<IPortableDeviceValues>                pObjectProperties;
CComPtr<IPortableDeviceContent>               pContent;
CComPtr<IPortableDeviceValuesCollection>      pPropertiesToWrite;
CComPtr<IPortableDevicePropVariantCollection> pObjectIDs;
DWORD                                         cObjectIDs        = 0;
if (SUCCEEDED(hr))
{
    hr = CoCreateInstance(CLSID_PortableDeviceValuesCollection,
                          NULL,
                          CLSCTX_INPROC_SERVER,
                          IID_IPortableDeviceValuesCollection,
                          (VOID**) &pPropertiesToWrite);
    if (FAILED(hr))
    {
        printf("! Failed to CoCreate IPortableDeviceValuesCollection for bulk property values, hr = 0x%lx\n", hr);
    }
}
```



Après cela, l’exemple crée une instance de l' [**interface IPortableDevicePropertiesBulkCallback**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevicepropertiesbulk). L’application utilisera les méthodes dans cette interface pour suivre la progression de l’opération asynchrone d’écriture en bloc.


```C++
HRESULT                                       hr                = S_OK;
GUID                                          guidContext       = GUID_NULL;
CSetBulkValuesCallback*                       pCallback         = NULL;
CComPtr<IPortableDeviceProperties>            pProperties;
CComPtr<IPortableDevicePropertiesBulk>        pPropertiesBulk;
CComPtr<IPortableDeviceValues>                pObjectProperties;
CComPtr<IPortableDeviceContent>               pContent;
CComPtr<IPortableDeviceValuesCollection>      pPropertiesToWrite;
CComPtr<IPortableDevicePropVariantCollection> pObjectIDs;
DWORD                                         cObjectIDs        = 0;
if (SUCCEEDED(hr))
{
    pCallback = new CSetBulkValuesCallback();
    if (pCallback == NULL)
    {
        hr = E_OUTOFMEMORY;
        printf("! Failed to allocate CSetBulkValuesCallback, hr = 0x%lx\n", hr);
    }
}
```



La fonction suivante appelée par l’exemple d’application est la `CreateIPortableDevicePropVariantCollectionWithAllObjectIDs` fonction d’assistance. Cette fonction énumère de manière récursive tous les objets sur un appareil donné et retourne une [**interface IPortableDevicePropVariantCollection**](iportabledevicepropvariantcollection.md) qui contient un identificateur pour chaque objet trouvé. Cette fonction est définie dans le module ContentEnumeration. cpp.


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



L’objet **IPortableDevicePropVariantCollection** contient une collection de valeurs **PROPVARIANT** indexées du même VarType. Dans ce cas, ces valeurs contiennent un identificateur d’objet donné pour chaque objet trouvé sur l’appareil.

Les identificateurs d’objet et leurs propriétés de nom respectives sont stockés dans un objet [**IPortableDeviceValuesCollection**](iportabledevicevalues.md) . Les propriétés de nom sont organisées afin que le premier objet soit affecté à la propriété Name de « NewName0 », que la propriété Name de « NewName1 » soit affectée au deuxième objet, et ainsi de suite.

L’extrait suivant de l’exemple montre comment l’objet **IPortableDeviceValuesCollection** a été initialisé avec des identificateurs d’objet et de nouvelles chaînes de nom.


```C++
HRESULT                                       hr                = S_OK;
GUID                                          guidContext       = GUID_NULL;
CSetBulkValuesCallback*                       pCallback         = NULL;
CComPtr<IPortableDeviceProperties>            pProperties;
CComPtr<IPortableDevicePropertiesBulk>        pPropertiesBulk;
CComPtr<IPortableDeviceValues>                pObjectProperties;
CComPtr<IPortableDeviceContent>               pContent;
CComPtr<IPortableDeviceValuesCollection>      pPropertiesToWrite;
CComPtr<IPortableDevicePropVariantCollection> pObjectIDs;
DWORD                                         cObjectIDs        = 0;
if (SUCCEEDED(hr))
{
    hr = pObjectIDs->GetCount(&cObjectIDs);
    if (FAILED(hr))
    {
        printf("! Failed to get number of objectIDs from IPortableDevicePropVariantCollection, hr = 0x%lx\n", hr);
    }
}


if (SUCCEEDED(hr))
{
    for(DWORD dwIndex = 0; (dwIndex < cObjectIDs) && (hr == S_OK); dwIndex++)
    {
        CComPtr<IPortableDeviceValues>  pValues;
        PROPVARIANT                     pv = {0};

        PropVariantInit(&pv);
        hr = CoCreateInstance(CLSID_PortableDeviceValues,
                              NULL,
                              CLSCTX_INPROC_SERVER,
                              IID_IPortableDeviceValues,
                              (VOID**) &pValues);
        if (FAILED(hr))
        {
            printf("! Failed to CoCreate CLSID_PortableDeviceValues, hr = 0x%lx\n", hr);
        }

        // Get the Object ID whose properties we will set
        if (hr == S_OK)
        {
            hr = pObjectIDs->GetAt(dwIndex, &pv);
            if (FAILED(hr))
            {
                printf("! Failed to get next Object ID from list, hr = 0x%lx\n", hr);
            }
        }

        // Save them into the IPortableDeviceValues so the driver knows which object this proeprty set belongs to
        if (hr == S_OK)
        {
            hr = pValues->SetStringValue(WPD_OBJECT_ID, pv.pwszVal);
            if (FAILED(hr))
            {
                printf("! Failed to set WPD_OBJECT_ID, hr = 0x%lx\n", hr);
            }
        }

        // Set the new values.  In this sample, we attempt to set the name property.
        if (hr == S_OK)
        {
            CAtlStringW strValue;
            strValue.Format(L"NewName%d", dwIndex);

            hr = pValues->SetStringValue(WPD_OBJECT_NAME, strValue.GetString());
            if (FAILED(hr))
            {
                printf("! Failed to set WPD_OBJECT_NAME, hr = 0x%lx\n", hr);
            }
        }

        // Add this property set to the collection
        if (hr == S_OK)
        {
            hr = pPropertiesToWrite->Add(pValues);
            if (FAILED(hr))
            {
                printf("! Failed to add values to collection, hr = 0x%lx\n", hr);
            }
        }
        PropVariantClear(&pv);
    }
}
```



Une fois que l’exemple a créé l’objet **IPortableDeviceValuesCollection** qui contient l’identificateur d’objet et les paires de noms, il peut commencer l’opération asynchrone.

L’opération d’écriture asynchrone commence lorsque l’exemple appelle la méthode [**IPortableDevicePropertiesBulk :: QueueSetValuesByObjectList**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicepropertiesbulk-queuesetvaluesbyobjectlist) . Cette méthode avertit le pilote qu’une opération en bloc va commencer. Après cela, l’exemple appelle la méthode [**IPortableDeviceBulk :: Start**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicepropertiesbulk-start) pour commencer à écrire les nouvelles valeurs de nom.


```C++
   HRESULT                                       hr                = S_OK;
   GUID                                          guidContext       = GUID_NULL;
   CSetBulkValuesCallback*                       pCallback         = NULL;
   CComPtr<IPortableDeviceProperties>            pProperties;
   CComPtr<IPortableDevicePropertiesBulk>        pPropertiesBulk;
   CComPtr<IPortableDeviceValues>                pObjectProperties;
   CComPtr<IPortableDeviceContent>               pContent;
   CComPtr<IPortableDeviceValuesCollection>      pPropertiesToWrite;
   CComPtr<IPortableDevicePropVariantCollection> pObjectIDs;
   DWORD                                         cObjectIDs        = 0;
   if (SUCCEEDED(hr))
   {
       hr = pPropertiesBulk->QueueSetValuesByObjectList(pPropertiesToWrite,
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
           printf("! QueueSetValuesByObjectList Failed, hr = 0x%lx\n", hr);
       }
   }
```



Notez que l’exemple attend un laps de temps infini pour terminer l’opération. S’il s’agissait d’une application de production, le code doit être modifié.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Interface IPortableDevice**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevice)
</dt> <dt>

[**Interface IPortableDeviceContent**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecontent)
</dt> <dt>

[**Interface IPortableDeviceProperties**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledeviceproperties)
</dt> <dt>

[**Interface IPortableDevicePropertiesBulk**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevicepropertiesbulk)
</dt> <dt>

[**Interface IPortableDevicePropVariantCollection**](iportabledevicepropvariantcollection.md)
</dt> <dt>

[**Guide de programmation**](programming-guide.md)
</dt> </dl>

 

 



