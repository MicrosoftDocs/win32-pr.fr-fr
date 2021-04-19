---
description: Récupération des propriétés de plusieurs objets
ms.assetid: 0d0c6b3d-23bc-4628-a684-14bb9e18967f
title: Récupération des propriétés de plusieurs objets
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 56c069f6a28b923339f66f8423f211eff4704ef6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106537064"
---
# <a name="retrieving-properties-for-multiple-objects"></a><span data-ttu-id="1102b-103">Récupération des propriétés de plusieurs objets</span><span class="sxs-lookup"><span data-stu-id="1102b-103">Retrieving Properties for Multiple Objects</span></span>

<span data-ttu-id="1102b-104">Certains pilotes de périphériques prennent en charge la récupération des propriétés de plusieurs objets dans un appel de fonction unique. C’est ce qu’on appelle une récupération en bloc.</span><span class="sxs-lookup"><span data-stu-id="1102b-104">Some device drivers support the retrieval of properties for multiple objects in a single function call; this is referred to as a bulk retrieval.</span></span> <span data-ttu-id="1102b-105">Il existe deux types d’opérations de récupération en bloc : le premier type récupère les propriétés d’une liste d’objets, et le deuxième type récupère les propriétés pour tous les objets d’un format donné.</span><span class="sxs-lookup"><span data-stu-id="1102b-105">There are two types of bulk retrieval operations: the first type retrieves properties for a list of objects, and the second type retrieves properties for all objects of a given format.</span></span> <span data-ttu-id="1102b-106">L’exemple décrit dans cette section illustre la première.</span><span class="sxs-lookup"><span data-stu-id="1102b-106">The example described in this section demonstrates the former.</span></span>

<span data-ttu-id="1102b-107">Votre application peut effectuer une récupération en bloc à l’aide des interfaces décrites dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="1102b-107">Your application can perform a bulk retrieval using the interfaces described in the following table.</span></span>



| <span data-ttu-id="1102b-108">Interface</span><span class="sxs-lookup"><span data-stu-id="1102b-108">Interface</span></span>                                                                                      | <span data-ttu-id="1102b-109">Description</span><span class="sxs-lookup"><span data-stu-id="1102b-109">Description</span></span>                                                        |
|------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| [<span data-ttu-id="1102b-110">**Interface IPortableDeviceContent**</span><span class="sxs-lookup"><span data-stu-id="1102b-110">**IPortableDeviceContent Interface**</span></span>](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecontent)                             | <span data-ttu-id="1102b-111">Fournit l’accès aux méthodes spécifiques au contenu.</span><span class="sxs-lookup"><span data-stu-id="1102b-111">Provides access to the content-specific methods.</span></span>                   |
| [<span data-ttu-id="1102b-112">**Interface IPortableDeviceKeyCollection**</span><span class="sxs-lookup"><span data-stu-id="1102b-112">**IPortableDeviceKeyCollection Interface**</span></span>](iportabledevicekeycollection.md)                 | <span data-ttu-id="1102b-113">Utilisé pour identifier les propriétés à récupérer.</span><span class="sxs-lookup"><span data-stu-id="1102b-113">Used to identify the properties to be retrieved.</span></span>                   |
| [<span data-ttu-id="1102b-114">**Interface IPortableDeviceProperties**</span><span class="sxs-lookup"><span data-stu-id="1102b-114">**IPortableDeviceProperties Interface**</span></span>](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledeviceproperties)                       | <span data-ttu-id="1102b-115">Utilisé pour déterminer si un pilote donné prend en charge les opérations en bloc.</span><span class="sxs-lookup"><span data-stu-id="1102b-115">Used to determine whether a given driver supports bulk operations.</span></span> |
| [<span data-ttu-id="1102b-116">**Interface IPortableDevicePropertiesBulk**</span><span class="sxs-lookup"><span data-stu-id="1102b-116">**IPortableDevicePropertiesBulk Interface**</span></span>](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevicepropertiesbulk)               | <span data-ttu-id="1102b-117">Prend en charge l’opération de récupération en bloc.</span><span class="sxs-lookup"><span data-stu-id="1102b-117">Supports the bulk retrieval operation.</span></span>                             |
| [<span data-ttu-id="1102b-118">**Interface IPortableDevicePropVariantCollection**</span><span class="sxs-lookup"><span data-stu-id="1102b-118">**IPortableDevicePropVariantCollection Interface**</span></span>](iportabledevicepropvariantcollection.md) | <span data-ttu-id="1102b-119">Utilisé pour stocker les identificateurs d’objet pour l’opération en bloc.</span><span class="sxs-lookup"><span data-stu-id="1102b-119">Used to store the object identifiers for the bulk operation.</span></span>       |



 

<span data-ttu-id="1102b-120">La fonction ReadContentPropertiesBulk dans le module ContentProperties. cpp de l’exemple d’application illustre une opération de récupération en bloc.</span><span class="sxs-lookup"><span data-stu-id="1102b-120">The ReadContentPropertiesBulk function in the sample application's ContentProperties.cpp module demonstrates a bulk retrieval operation.</span></span>

<span data-ttu-id="1102b-121">La première tâche accomplie dans cet exemple consiste à déterminer si le pilote donné prend en charge les opérations en bloc.</span><span class="sxs-lookup"><span data-stu-id="1102b-121">The first task accomplished in this sample is determining whether or not the given driver supports bulk operations.</span></span> <span data-ttu-id="1102b-122">Cela s’effectue en appelant QueryInterface sur l’interface IPortableDeviceProperties et en vérifiant l’existence de IPortableDevicePropertiesBulk.</span><span class="sxs-lookup"><span data-stu-id="1102b-122">This is accomplished by calling QueryInterface on the IPortableDeviceProperties interface and checking for the existence of IPortableDevicePropertiesBulk.</span></span>


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



<span data-ttu-id="1102b-123">Si le pilote prend en charge les opérations en bloc, l’étape suivante consiste à créer une instance de l' [**interface IPortableDeviceKeyCollection**](iportabledevicekeycollection.md) et à spécifier les clés qui correspondent aux propriétés que l’application doit récupérer.</span><span class="sxs-lookup"><span data-stu-id="1102b-123">If the driver supports bulk operations, the next step is to create an instance of the [**IPortableDeviceKeyCollection interface**](iportabledevicekeycollection.md) and to specify the keys that correspond to the properties that the application will retrieve.</span></span> <span data-ttu-id="1102b-124">Pour obtenir une description de ce processus, consultez la rubrique [extraction des propriétés pour un seul objet](retrieving-properties-for-a-single-object.md) .</span><span class="sxs-lookup"><span data-stu-id="1102b-124">For a description of this process, see the [Retrieving Properties for a Single Object](retrieving-properties-for-a-single-object.md) topic.</span></span>

<span data-ttu-id="1102b-125">Une fois les clés appropriées spécifiées, l’exemple d’application crée une instance de l' [**interface IPortableDevicePropertiesBulkCallback**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevicepropertiesbulk).</span><span class="sxs-lookup"><span data-stu-id="1102b-125">After the appropriate keys are specified, the sample application creates an instance of the [**IPortableDevicePropertiesBulkCallback interface**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevicepropertiesbulk).</span></span> <span data-ttu-id="1102b-126">L’application utilisera les méthodes dans cette interface pour suivre la progression de l’opération asynchrone de récupération en bloc.</span><span class="sxs-lookup"><span data-stu-id="1102b-126">The application will use the methods in this interface to track the progress of the asynchronous bulk-retrieval operation.</span></span>


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



<span data-ttu-id="1102b-127">La fonction suivante appelée par l’exemple d’application est la fonction d’assistance CreateIPortableDevicePropVariantCollectionWithAllObjectIDs.</span><span class="sxs-lookup"><span data-stu-id="1102b-127">The next function that the sample application calls is the CreateIPortableDevicePropVariantCollectionWithAllObjectIDs helper function.</span></span> <span data-ttu-id="1102b-128">Cette fonction crée une liste de tous les identificateurs d’objets disponibles à titre d’exemple.</span><span class="sxs-lookup"><span data-stu-id="1102b-128">This function creates a list of all available object identifiers for example purposes.</span></span> <span data-ttu-id="1102b-129">(Une application réelle limiterait la liste des identificateurs à un ensemble d’objets particulier.</span><span class="sxs-lookup"><span data-stu-id="1102b-129">(A real-world application would limit the list of identifiers to a particular set of objects.</span></span> <span data-ttu-id="1102b-130">Par exemple, une application peut créer une liste d’identificateurs pour tous les objets actuellement dans une vue de dossier donnée.)</span><span class="sxs-lookup"><span data-stu-id="1102b-130">For instance, an application may create a list of identifiers for all of the objects currently in a given folder view.)</span></span>

<span data-ttu-id="1102b-131">Comme indiqué ci-dessus, la fonction d’assistance énumère de manière récursive tous les objets sur un appareil donné.</span><span class="sxs-lookup"><span data-stu-id="1102b-131">As noted above, the helper function recursively enumerates all objects on a given device.</span></span> <span data-ttu-id="1102b-132">Elle retourne cette liste dans une [**interface IPortableDevicePropVariantCollection**](iportabledevicepropvariantcollection.md) qui contient un identificateur pour chaque objet trouvé.</span><span class="sxs-lookup"><span data-stu-id="1102b-132">It returns this list in an [**IPortableDevicePropVariantCollection interface**](iportabledevicepropvariantcollection.md) that contains an identifier for each object that it found.</span></span> <span data-ttu-id="1102b-133">La fonction d’assistance est définie dans le module ContentEnumeration. cpp.</span><span class="sxs-lookup"><span data-stu-id="1102b-133">The helper function is defined in the module ContentEnumeration.cpp.</span></span>


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



<span data-ttu-id="1102b-134">Une fois les étapes précédentes effectuées, l’exemple d’application lance la récupération de propriété asynchrone.</span><span class="sxs-lookup"><span data-stu-id="1102b-134">Once the previous steps are accomplished, the sample application initiates the asynchronous property retrieval.</span></span> <span data-ttu-id="1102b-135">Pour ce faire, procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="1102b-135">This is accomplished by doing the following:</span></span>

1.  <span data-ttu-id="1102b-136">Appel de IPortableDevicePropertiesBulk :: QueueGetValuesByObjectList, qui met en file d’attente une demande pour la récupération de propriété en bloc.</span><span class="sxs-lookup"><span data-stu-id="1102b-136">Calling IPortableDevicePropertiesBulk::QueueGetValuesByObjectList, which queues a request for the bulk property retrieval.</span></span> <span data-ttu-id="1102b-137">(Notez que même si la demande est mise en file d’attente, elle n’est pas démarrée.)</span><span class="sxs-lookup"><span data-stu-id="1102b-137">(Note that although the request is queued, it is not started.)</span></span>
2.  <span data-ttu-id="1102b-138">Appel de IPortableDevicePropertiesBulk :: Start pour initier la demande en file d’attente.</span><span class="sxs-lookup"><span data-stu-id="1102b-138">Calling IPortableDevicePropertiesBulk::Start to initiate the queued request.</span></span>

<span data-ttu-id="1102b-139">Ces étapes sont présentées dans l’extrait de code suivant de l’exemple d’application.</span><span class="sxs-lookup"><span data-stu-id="1102b-139">These steps are demonstrated in the following code excerpt from the sample application.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="1102b-140">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="1102b-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1102b-141">**Interface IPortableDevice**</span><span class="sxs-lookup"><span data-stu-id="1102b-141">**IPortableDevice Interface**</span></span>](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevice)
</dt> <dt>

[<span data-ttu-id="1102b-142">**Interface IPortableDeviceContent**</span><span class="sxs-lookup"><span data-stu-id="1102b-142">**IPortableDeviceContent Interface**</span></span>](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecontent)
</dt> <dt>

[<span data-ttu-id="1102b-143">**Interface IPortableDeviceKeyCollection**</span><span class="sxs-lookup"><span data-stu-id="1102b-143">**IPortableDeviceKeyCollection Interface**</span></span>](iportabledevicekeycollection.md)
</dt> <dt>

[<span data-ttu-id="1102b-144">**Interface IPortableDeviceProperties**</span><span class="sxs-lookup"><span data-stu-id="1102b-144">**IPortableDeviceProperties Interface**</span></span>](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledeviceproperties)
</dt> <dt>

[<span data-ttu-id="1102b-145">**Interface IPortableDevicePropertiesBulk**</span><span class="sxs-lookup"><span data-stu-id="1102b-145">**IPortableDevicePropertiesBulk Interface**</span></span>](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevicepropertiesbulk)
</dt> <dt>

[<span data-ttu-id="1102b-146">**Interface IPortableDevicePropVariantCollection**</span><span class="sxs-lookup"><span data-stu-id="1102b-146">**IPortableDevicePropVariantCollection Interface**</span></span>](iportabledevicepropvariantcollection.md)
</dt> <dt>

[<span data-ttu-id="1102b-147">**Guide de programmation**</span><span class="sxs-lookup"><span data-stu-id="1102b-147">**Programming Guide**</span></span>](programming-guide.md)
</dt> </dl>

 

 



