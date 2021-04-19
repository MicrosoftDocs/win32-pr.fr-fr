---
description: Définition des propriétés de plusieurs objets
ms.assetid: 0686ba54-4782-42a4-8fdb-2325fc8d8bc2
title: Définition des propriétés de plusieurs objets
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e951662d9920cb22db0a417f1af94f3eb7eb4d7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106520693"
---
# <a name="setting-properties-for-multiple-objects"></a><span data-ttu-id="6e30c-103">Définition des propriétés de plusieurs objets</span><span class="sxs-lookup"><span data-stu-id="6e30c-103">Setting Properties for Multiple Objects</span></span>

<span data-ttu-id="6e30c-104">Certains pilotes de périphériques prennent en charge la définition des propriétés de plusieurs objets dans un appel de fonction unique, appelée écriture en bloc.</span><span class="sxs-lookup"><span data-stu-id="6e30c-104">Some device drivers support setting properties for multiple objects in a single function call—this is referred to as a bulk write.</span></span> <span data-ttu-id="6e30c-105">Votre application peut effectuer une écriture en bloc à l’aide des interfaces décrites dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="6e30c-105">Your application can perform a bulk write using the interfaces described in the following table.</span></span>



| <span data-ttu-id="6e30c-106">Interface</span><span class="sxs-lookup"><span data-stu-id="6e30c-106">Interface</span></span>                                                                                      | <span data-ttu-id="6e30c-107">Description</span><span class="sxs-lookup"><span data-stu-id="6e30c-107">Description</span></span>                                                  |
|------------------------------------------------------------------------------------------------|--------------------------------------------------------------|
| [<span data-ttu-id="6e30c-108">**Interface IPortableDeviceContent**</span><span class="sxs-lookup"><span data-stu-id="6e30c-108">**IPortableDeviceContent Interface**</span></span>](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecontent)                             | <span data-ttu-id="6e30c-109">Fournit l’accès aux méthodes spécifiques au contenu.</span><span class="sxs-lookup"><span data-stu-id="6e30c-109">Provides access to the content-specific methods.</span></span>             |
| [<span data-ttu-id="6e30c-110">**Interface IPortableDeviceProperties**</span><span class="sxs-lookup"><span data-stu-id="6e30c-110">**IPortableDeviceProperties Interface**</span></span>](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledeviceproperties)                       | <span data-ttu-id="6e30c-111">Fournit l’accès aux méthodes spécifiques à la propriété.</span><span class="sxs-lookup"><span data-stu-id="6e30c-111">Provides access to the property-specific methods.</span></span>            |
| [<span data-ttu-id="6e30c-112">**Interface IPortableDevicePropertiesBulk**</span><span class="sxs-lookup"><span data-stu-id="6e30c-112">**IPortableDevicePropertiesBulk Interface**</span></span>](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevicepropertiesbulk)               | <span data-ttu-id="6e30c-113">Prend en charge l’opération d’écriture en bloc.</span><span class="sxs-lookup"><span data-stu-id="6e30c-113">Supports the bulk write operation.</span></span>                           |
| [<span data-ttu-id="6e30c-114">**Interface IPortableDevicePropVariantCollection**</span><span class="sxs-lookup"><span data-stu-id="6e30c-114">**IPortableDevicePropVariantCollection Interface**</span></span>](iportabledevicepropvariantcollection.md) | <span data-ttu-id="6e30c-115">Utilisé pour stocker les identificateurs d’objet pour l’opération en bloc.</span><span class="sxs-lookup"><span data-stu-id="6e30c-115">Used to store the object identifiers for the bulk operation.</span></span> |
| [<span data-ttu-id="6e30c-116">**Interface IPortableDeviceValuesCollection**</span><span class="sxs-lookup"><span data-stu-id="6e30c-116">**IPortableDeviceValuesCollection Interface**</span></span>](iportabledevicevaluescollection.md)           | <span data-ttu-id="6e30c-117">Utilisé pour identifier les propriétés à écrire.</span><span class="sxs-lookup"><span data-stu-id="6e30c-117">Used to identify the properties to be written.</span></span>               |



 

<span data-ttu-id="6e30c-118">La `WriteContentPropertiesBulk` fonction dans le module ContentProperties. cpp de l’exemple d’application illustre une opération d’écriture en bloc.</span><span class="sxs-lookup"><span data-stu-id="6e30c-118">The `WriteContentPropertiesBulk` function in the sample application's ContentProperties.cpp module demonstrates a bulk write operation.</span></span>

<span data-ttu-id="6e30c-119">La première tâche accomplie dans cet exemple consiste à déterminer si le pilote donné prend en charge les opérations en bloc.</span><span class="sxs-lookup"><span data-stu-id="6e30c-119">The first task accomplished in this sample is determining whether or not the given driver supports bulk operations.</span></span> <span data-ttu-id="6e30c-120">Pour ce faire, appelez QueryInterface sur un objet **IPortableDeviceProperties** et vérifiez l’existence de **IPortableDevicePropertiesBulk**.</span><span class="sxs-lookup"><span data-stu-id="6e30c-120">This is accomplished by calling QueryInterface on an **IPortableDeviceProperties** object and checking for the existence of **IPortableDevicePropertiesBulk**.</span></span>


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



<span data-ttu-id="6e30c-121">La tâche suivante entraîne la création d’un objet **IPortableDeviceValuesCollection** .</span><span class="sxs-lookup"><span data-stu-id="6e30c-121">The next task entails creating an **IPortableDeviceValuesCollection** object.</span></span> <span data-ttu-id="6e30c-122">Il s’agit de l’objet qui contient les valeurs de propriété que l’exemple écrira.</span><span class="sxs-lookup"><span data-stu-id="6e30c-122">This is the object that contains the property values that the sample will write.</span></span>


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



<span data-ttu-id="6e30c-123">Après cela, l’exemple crée une instance de l' [**interface IPortableDevicePropertiesBulkCallback**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevicepropertiesbulk).</span><span class="sxs-lookup"><span data-stu-id="6e30c-123">After this, the sample creates an instance of the [**IPortableDevicePropertiesBulkCallback interface**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevicepropertiesbulk).</span></span> <span data-ttu-id="6e30c-124">L’application utilisera les méthodes dans cette interface pour suivre la progression de l’opération asynchrone d’écriture en bloc.</span><span class="sxs-lookup"><span data-stu-id="6e30c-124">The application will use the methods in this interface to track the progress of the asynchronous bulk-write operation.</span></span>


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



<span data-ttu-id="6e30c-125">La fonction suivante appelée par l’exemple d’application est la `CreateIPortableDevicePropVariantCollectionWithAllObjectIDs` fonction d’assistance.</span><span class="sxs-lookup"><span data-stu-id="6e30c-125">The next function that the sample application calls is the `CreateIPortableDevicePropVariantCollectionWithAllObjectIDs` helper function.</span></span> <span data-ttu-id="6e30c-126">Cette fonction énumère de manière récursive tous les objets sur un appareil donné et retourne une [**interface IPortableDevicePropVariantCollection**](iportabledevicepropvariantcollection.md) qui contient un identificateur pour chaque objet trouvé.</span><span class="sxs-lookup"><span data-stu-id="6e30c-126">This function recursively enumerates all objects on a given device and returns an [**IPortableDevicePropVariantCollection interface**](iportabledevicepropvariantcollection.md) that contains an identifier for each object that it found.</span></span> <span data-ttu-id="6e30c-127">Cette fonction est définie dans le module ContentEnumeration. cpp.</span><span class="sxs-lookup"><span data-stu-id="6e30c-127">This function is defined in the module ContentEnumeration.cpp.</span></span>


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



<span data-ttu-id="6e30c-128">L’objet **IPortableDevicePropVariantCollection** contient une collection de valeurs **PROPVARIANT** indexées du même VarType.</span><span class="sxs-lookup"><span data-stu-id="6e30c-128">The **IPortableDevicePropVariantCollection** object holds a collection of indexed **PROPVARIANT** values of the same VARTYPE.</span></span> <span data-ttu-id="6e30c-129">Dans ce cas, ces valeurs contiennent un identificateur d’objet donné pour chaque objet trouvé sur l’appareil.</span><span class="sxs-lookup"><span data-stu-id="6e30c-129">In this case, these values contain a given object identifier for each object found on the device.</span></span>

<span data-ttu-id="6e30c-130">Les identificateurs d’objet et leurs propriétés de nom respectives sont stockés dans un objet [**IPortableDeviceValuesCollection**](iportabledevicevalues.md) .</span><span class="sxs-lookup"><span data-stu-id="6e30c-130">The object identifiers and their respective name properties are stored in an [**IPortableDeviceValuesCollection**](iportabledevicevalues.md) object.</span></span> <span data-ttu-id="6e30c-131">Les propriétés de nom sont organisées afin que le premier objet soit affecté à la propriété Name de « NewName0 », que la propriété Name de « NewName1 » soit affectée au deuxième objet, et ainsi de suite.</span><span class="sxs-lookup"><span data-stu-id="6e30c-131">The name properties are organized so that the first object is assigned a name property of "NewName0", the second object is assigned a name property of "NewName1", and so on.</span></span>

<span data-ttu-id="6e30c-132">L’extrait suivant de l’exemple montre comment l’objet **IPortableDeviceValuesCollection** a été initialisé avec des identificateurs d’objet et de nouvelles chaînes de nom.</span><span class="sxs-lookup"><span data-stu-id="6e30c-132">The following excerpt from the sample demonstrates how the **IPortableDeviceValuesCollection** object was initialized with object identifiers and new name strings.</span></span>


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



<span data-ttu-id="6e30c-133">Une fois que l’exemple a créé l’objet **IPortableDeviceValuesCollection** qui contient l’identificateur d’objet et les paires de noms, il peut commencer l’opération asynchrone.</span><span class="sxs-lookup"><span data-stu-id="6e30c-133">Once the sample creates the **IPortableDeviceValuesCollection** object that contains the object identifier and name pairs, it can begin the asynchronous operation.</span></span>

<span data-ttu-id="6e30c-134">L’opération d’écriture asynchrone commence lorsque l’exemple appelle la méthode [**IPortableDevicePropertiesBulk :: QueueSetValuesByObjectList**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicepropertiesbulk-queuesetvaluesbyobjectlist) .</span><span class="sxs-lookup"><span data-stu-id="6e30c-134">The asynchronous write operation begins when the sample calls the [**IPortableDevicePropertiesBulk::QueueSetValuesByObjectList**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicepropertiesbulk-queuesetvaluesbyobjectlist) method.</span></span> <span data-ttu-id="6e30c-135">Cette méthode avertit le pilote qu’une opération en bloc va commencer.</span><span class="sxs-lookup"><span data-stu-id="6e30c-135">This method notifies the driver that a bulk operation is about to begin.</span></span> <span data-ttu-id="6e30c-136">Après cela, l’exemple appelle la méthode [**IPortableDeviceBulk :: Start**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicepropertiesbulk-start) pour commencer à écrire les nouvelles valeurs de nom.</span><span class="sxs-lookup"><span data-stu-id="6e30c-136">After this, the sample calls the [**IPortableDeviceBulk::Start**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicepropertiesbulk-start) method to begin actually writing the new name values.</span></span>


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



<span data-ttu-id="6e30c-137">Notez que l’exemple attend un laps de temps infini pour terminer l’opération.</span><span class="sxs-lookup"><span data-stu-id="6e30c-137">Note that the sample waits an infinitely long period of time for the operation to complete.</span></span> <span data-ttu-id="6e30c-138">S’il s’agissait d’une application de production, le code doit être modifié.</span><span class="sxs-lookup"><span data-stu-id="6e30c-138">If this were a production application, the code would need to be modified.</span></span>

## <a name="related-topics"></a><span data-ttu-id="6e30c-139">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="6e30c-139">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6e30c-140">**Interface IPortableDevice**</span><span class="sxs-lookup"><span data-stu-id="6e30c-140">**IPortableDevice Interface**</span></span>](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevice)
</dt> <dt>

[<span data-ttu-id="6e30c-141">**Interface IPortableDeviceContent**</span><span class="sxs-lookup"><span data-stu-id="6e30c-141">**IPortableDeviceContent Interface**</span></span>](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecontent)
</dt> <dt>

[<span data-ttu-id="6e30c-142">**Interface IPortableDeviceProperties**</span><span class="sxs-lookup"><span data-stu-id="6e30c-142">**IPortableDeviceProperties Interface**</span></span>](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledeviceproperties)
</dt> <dt>

[<span data-ttu-id="6e30c-143">**Interface IPortableDevicePropertiesBulk**</span><span class="sxs-lookup"><span data-stu-id="6e30c-143">**IPortableDevicePropertiesBulk Interface**</span></span>](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevicepropertiesbulk)
</dt> <dt>

[<span data-ttu-id="6e30c-144">**Interface IPortableDevicePropVariantCollection**</span><span class="sxs-lookup"><span data-stu-id="6e30c-144">**IPortableDevicePropVariantCollection Interface**</span></span>](iportabledevicepropvariantcollection.md)
</dt> <dt>

[<span data-ttu-id="6e30c-145">**Guide de programmation**</span><span class="sxs-lookup"><span data-stu-id="6e30c-145">**Programming Guide**</span></span>](programming-guide.md)
</dt> </dl>

 

 



