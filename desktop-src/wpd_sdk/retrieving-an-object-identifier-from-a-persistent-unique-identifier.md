---
description: Récupération d’un identificateur d’objet à partir d’un identificateur unique persistant
ms.assetid: 146f8943-d4e1-4b87-a812-e534082a4f14
title: Récupération d’un ID d’objet à partir d’un ID unique persistant
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c4f997f0faf586a374e5a83c6f96b6508f02eb41
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106522119"
---
# <a name="retrieving-an-object-id-from-a-persistent-unique-id"></a><span data-ttu-id="9b60f-103">Récupération d’un ID d’objet à partir d’un ID unique persistant</span><span class="sxs-lookup"><span data-stu-id="9b60f-103">Retrieving an Object Id from a Persistent Unique Id</span></span>

<span data-ttu-id="9b60f-104">L’unicité des identificateurs d’objets n’est garantie que pour une session d’appareil donnée ; Si l’utilisateur établit une nouvelle connexion, les identificateurs d’une session précédente peuvent ne pas correspondre aux identificateurs de la session active.</span><span class="sxs-lookup"><span data-stu-id="9b60f-104">Object identifiers are only guaranteed to be unique for a given device session; if the user establishes a new connection, identifiers from a previous session may not match identifiers for the current session.</span></span> <span data-ttu-id="9b60f-105">Pour résoudre ce problème, l’API WPD prend en charge les identificateurs uniques persistants (PUID), qui persistent sur les sessions de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="9b60f-105">To resolve this issue, the WPD API supports persistent unique identifiers (PUIDs), which persist across device sessions.</span></span>

<span data-ttu-id="9b60f-106">Certains appareils stockent leurs PUID en mode natif avec un objet donné.</span><span class="sxs-lookup"><span data-stu-id="9b60f-106">Some devices store their PUIDs natively with a given object.</span></span> <span data-ttu-id="9b60f-107">D’autres peuvent générer le PUID en se basant sur le hachage des données de l’objet sélectionné.</span><span class="sxs-lookup"><span data-stu-id="9b60f-107">Others may generate the PUID based on a hash of selected object data.</span></span> <span data-ttu-id="9b60f-108">D’autres peuvent traiter les identificateurs d’objets comme des PUID (car ils peuvent garantir que ces identificateurs ne changent jamais).</span><span class="sxs-lookup"><span data-stu-id="9b60f-108">Others may treat object identifiers as PUIDs (because they can guarantee that these identifiers never change).</span></span>

<span data-ttu-id="9b60f-109">La fonction GetObjectIdentifierFromPersistentUniqueIdentifier dans le module ContentProperties. cpp illustre la récupération d’un identificateur d’objet pour un PUID donné.</span><span class="sxs-lookup"><span data-stu-id="9b60f-109">The GetObjectIdentifierFromPersistentUniqueIdentifier function in the ContentProperties.cpp module demonstrates the retrieval of an object identifier for a given PUID.</span></span>

<span data-ttu-id="9b60f-110">Votre application peut récupérer un identificateur d’objet pour un PUID correspondant à l’aide des interfaces décrites dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="9b60f-110">Your application can retrieve an object identifier for a corresponding PUID using the interfaces described in the following table.</span></span>



| <span data-ttu-id="9b60f-111">Interface</span><span class="sxs-lookup"><span data-stu-id="9b60f-111">Interface</span></span>                                                                                      | <span data-ttu-id="9b60f-112">Description</span><span class="sxs-lookup"><span data-stu-id="9b60f-112">Description</span></span>                                                                                         |
|------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="9b60f-113">**Interface IPortableDeviceContent**</span><span class="sxs-lookup"><span data-stu-id="9b60f-113">**IPortableDeviceContent Interface**</span></span>](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecontent)                             | <span data-ttu-id="9b60f-114">Fournit l’accès à la méthode de récupération.</span><span class="sxs-lookup"><span data-stu-id="9b60f-114">Provides access to the retrieval method.</span></span>                                                            |
| [<span data-ttu-id="9b60f-115">**Interface IPortableDevicePropVariantCollection**</span><span class="sxs-lookup"><span data-stu-id="9b60f-115">**IPortableDevicePropVariantCollection Interface**</span></span>](iportabledevicepropvariantcollection.md) | <span data-ttu-id="9b60f-116">Utilisé pour stocker l’identificateur d’objet et l’identificateur unique persistant (PUID) correspondant.</span><span class="sxs-lookup"><span data-stu-id="9b60f-116">Used to store both the object identifier and the corresponding persistent unique identifier (PUID).</span></span> |



 

<span data-ttu-id="9b60f-117">La première tâche que l’exemple d’application effectue est d’obtenir un PUID auprès de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="9b60f-117">The first task that the sample application accomplishes is to obtain a PUID from the user.</span></span>


```C++
// Prompt user to enter an unique identifier to convert to an object idenifier.
printf("Enter the Persistant Unique Identifier of the object you wish to convert into an object identifier.\n>");
hr = StringCbGetsW(szSelection,sizeof(szSelection));
if (FAILED(hr))
{
    printf("An invalid persistent object identifier was specified, aborting the query operation\n");
}
```



<span data-ttu-id="9b60f-118">Après cela, l’exemple d’application récupère un objet [**IPortableDeviceContent**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecontent) , qu’il utilisera pour appeler la méthode [**GetObjectIDsFromPersistentUniqueIDs**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicecontent-getobjectidsfrompersistentuniqueids) .</span><span class="sxs-lookup"><span data-stu-id="9b60f-118">After this, the sample application retrieves an [**IPortableDeviceContent**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecontent) object, which it will use to invoke the [**GetObjectIDsFromPersistentUniqueIDs**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicecontent-getobjectidsfrompersistentuniqueids) method.</span></span>


```C++
if (SUCCEEDED(hr))
{
    hr = pDevice->Content(&pContent);
    if (FAILED(hr))
    {
        printf("! Failed to get IPortableDeviceContent from IPortableDevice, hr = 0x%lx\n",hr);
    }
}
```



<span data-ttu-id="9b60f-119">Ensuite, il crée un objet [**IPortableDevicePropVariantCollection**](iportabledevicepropvariantcollection.md) qui contiendra le PUID fourni par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="9b60f-119">Next, it creates an [**IPortableDevicePropVariantCollection**](iportabledevicepropvariantcollection.md) object that will hold the PUID supplied by the user.</span></span>


```C++
hr = CoCreateInstance(CLSID_PortableDevicePropVariantCollection,
                      NULL,
                      CLSCTX_INPROC_SERVER,
                      IID_PPV_ARGS(&pPersistentUniqueIDs));
```



<span data-ttu-id="9b60f-120">Une fois les trois étapes précédentes effectuées, l’exemple est prêt à récupérer l’identificateur d’objet qui correspond au PUID fourni par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="9b60f-120">Once the previous three steps are taken, the sample is ready to retrieve the object identifier that matches the PUID supplied by the user.</span></span> <span data-ttu-id="9b60f-121">Pour ce faire, vous devez appeler la méthode [**IPortableDeviceContent :: GetObjectIDsFromPersistentUniqueIDs**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicecontent-getobjectidsfrompersistentuniqueids) .</span><span class="sxs-lookup"><span data-stu-id="9b60f-121">This is accomplished by calling the [**IPortableDeviceContent::GetObjectIDsFromPersistentUniqueIDs**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicecontent-getobjectidsfrompersistentuniqueids) method.</span></span> <span data-ttu-id="9b60f-122">Avant d’appeler cette méthode, l’exemple Initialise une structure PROPVARIANT, écrit le PUID fourni par l’utilisateur dans cette structure, puis l’ajoute à l’objet IPortableDevicePropVariantCollection à partir duquel pPersistentUniqueIDs pointe.</span><span class="sxs-lookup"><span data-stu-id="9b60f-122">Prior to calling this method, the sample initializes a PROPVARIANT structure, writes the PUID supplied by the user to this structure, and adds it to the IPortableDevicePropVariantCollection object at which pPersistentUniqueIDs points.</span></span> <span data-ttu-id="9b60f-123">Ce pointeur est passé comme premier argument à la méthode GetObjectIDsFromPersistentUniqueIDs.</span><span class="sxs-lookup"><span data-stu-id="9b60f-123">This pointer is passed as the first argument to the GetObjectIDsFromPersistentUniqueIDs method.</span></span> <span data-ttu-id="9b60f-124">Le deuxième argument de GetObjectIDsFromPersistentUniqueIDs est un objet IPortableDevicePropVariantCollection qui reçoit l’identificateur d’objet correspondant.</span><span class="sxs-lookup"><span data-stu-id="9b60f-124">The second argument of GetObjectIDsFromPersistentUniqueIDs is an IPortableDevicePropVariantCollection object that receives the matching object identifier.</span></span>


```C++
if (SUCCEEDED(hr))
{
    if (pPersistentUniqueIDs != NULL)
    {
        PROPVARIANT pv = {0};
        PropVariantInit(&pv);

        // Initialize a PROPVARIANT structure with the object identifier string
        // that the user selected above. Notice we are allocating memory for the
        // PWSTR value.  This memory will be freed when PropVariantClear() is
        // called below.
        pv.vt      = VT_LPWSTR;
        pv.pwszVal = AtlAllocTaskWideString(szSelection);
        if (pv.pwszVal != NULL)
        {
            // Add the object identifier to the objects-to-delete list
            // (We are only deleting 1 in this example)
            hr = pPersistentUniqueIDs->Add(&pv);
            if (SUCCEEDED(hr))
            {
                // 3) Attempt to get the unique idenifier for the object from the device
                hr = pContent->GetObjectIDsFromPersistentUniqueIDs(pPersistentUniqueIDs,
                                                                   &pObjectIDs);
                if (SUCCEEDED(hr))
                {
                    PROPVARIANT pvId = {0};
                    hr = pObjectIDs->GetAt(0, &pvId);
                    if (SUCCEEDED(hr))
                    {
                        printf("The persistent unique identifier '%ws' relates to object identifier '%ws' on the device.\n", szSelection, pvId.pwszVal);
                    }
                    else
                    {
                        printf("! Failed to get the object identifier for '%ws' from the IPortableDevicePropVariantCollection, hr = 0x%lx\n",szSelection, hr);
                    }

                    // Free the returned allocated string from the GetAt() call
                    PropVariantClear(&pvId);
                }
                else
                {
                    printf("! Failed to get the object identifier from persistent object idenifier '%ws', hr = 0x%lx\n",szSelection, hr);
                }
            }
            else
            {
                printf("! Failed to get the object identifier from persistent object idenifier because we could no add the persistent object identifier string to the IPortableDevicePropVariantCollection, hr = 0x%lx\n",hr);
            }
        }
        else
        {
            hr = E_OUTOFMEMORY;
            printf("! Failed to get the object identifier because we could no allocate memory for the persistent object identifier string, hr = 0x%lx\n",hr);
        }

        // Free any allocated values in the PROPVARIANT before exiting
        PropVariantClear(&pv);
    }
}
```



## <a name="related-topics"></a><span data-ttu-id="9b60f-125">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="9b60f-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9b60f-126">**Interface IPortableDevice**</span><span class="sxs-lookup"><span data-stu-id="9b60f-126">**IPortableDevice Interface**</span></span>](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevice)
</dt> <dt>

[<span data-ttu-id="9b60f-127">**Interface IPortableDeviceContent**</span><span class="sxs-lookup"><span data-stu-id="9b60f-127">**IPortableDeviceContent Interface**</span></span>](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecontent)
</dt> <dt>

[<span data-ttu-id="9b60f-128">**Interface IPortableDevicePropVariantCollection**</span><span class="sxs-lookup"><span data-stu-id="9b60f-128">**IPortableDevicePropVariantCollection Interface**</span></span>](iportabledevicepropvariantcollection.md)
</dt> <dt>

[<span data-ttu-id="9b60f-129">**Guide de programmation**</span><span class="sxs-lookup"><span data-stu-id="9b60f-129">**Programming Guide**</span></span>](programming-guide.md)
</dt> </dl>

 

 



