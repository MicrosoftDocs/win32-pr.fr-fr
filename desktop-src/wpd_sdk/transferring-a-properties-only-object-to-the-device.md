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
# <a name="transferring-a-properties-only-object-to-the-device"></a><span data-ttu-id="7afc7-103">Transfert d’un objet Properties-Only sur l’appareil</span><span class="sxs-lookup"><span data-stu-id="7afc7-103">Transferring a Properties-Only Object to the Device</span></span>

<span data-ttu-id="7afc7-104">Bien que l’exemple de la rubrique précédente ait démontré la création de contenu sur un appareil constitué de propriétés et de données, cette rubrique se concentre sur la création d’un objet de propriétés uniquement.</span><span class="sxs-lookup"><span data-stu-id="7afc7-104">While the example in the previous topic demonstrated the creation of content on a device consisting of both properties and data, this topic focuses on the creation of a properties-only object.</span></span>

<span data-ttu-id="7afc7-105">Les transferts de propriété uniquement sont effectués à l’aide des interfaces décrites dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="7afc7-105">Property-only transfers are accomplished using the interfaces described in the following table.</span></span>



| <span data-ttu-id="7afc7-106">Interface</span><span class="sxs-lookup"><span data-stu-id="7afc7-106">Interface</span></span>                                                          | <span data-ttu-id="7afc7-107">Description</span><span class="sxs-lookup"><span data-stu-id="7afc7-107">Description</span></span>                                            |
|--------------------------------------------------------------------|--------------------------------------------------------|
| [<span data-ttu-id="7afc7-108">**Interface IPortableDeviceContent**</span><span class="sxs-lookup"><span data-stu-id="7afc7-108">**IPortableDeviceContent Interface**</span></span>](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecontent) | <span data-ttu-id="7afc7-109">Fournit l’accès aux méthodes spécifiques au contenu.</span><span class="sxs-lookup"><span data-stu-id="7afc7-109">Provides access to the content-specific methods.</span></span>       |
| [<span data-ttu-id="7afc7-110">**Interface IPortableDeviceValues**</span><span class="sxs-lookup"><span data-stu-id="7afc7-110">**IPortableDeviceValues Interface**</span></span>](iportabledevicevalues.md)   | <span data-ttu-id="7afc7-111">Utilisé pour récupérer des propriétés qui décrivent le contenu.</span><span class="sxs-lookup"><span data-stu-id="7afc7-111">Used to retrieve properties that describe the content.</span></span> |



 

<span data-ttu-id="7afc7-112">La `TransferContactToDevice` fonction dans le module ContentTransfer. cpp de l’exemple d’application montre comment une application peut transférer les informations de contact d’un PC vers un appareil connecté.</span><span class="sxs-lookup"><span data-stu-id="7afc7-112">The `TransferContactToDevice` function in the sample application's ContentTransfer.cpp module demonstrates how an application could transfer contact information from a PC to a connected device.</span></span> <span data-ttu-id="7afc7-113">Dans cet exemple, le nom du contact transféré est un « John Kane » codé en dur et le numéro de téléphone du contact transféré est toujours « 425-555-0123 ».</span><span class="sxs-lookup"><span data-stu-id="7afc7-113">In this particular sample, the transferred contact name is a hard-coded "John Kane" and the transferred contact phone number is always "425-555-0123".</span></span>

<span data-ttu-id="7afc7-114">La première tâche accomplie par la `TransferContactToDevice` fonction consiste à inviter l’utilisateur à entrer un identificateur d’objet pour l’objet parent sur l’appareil (sous lequel le contenu sera transféré).</span><span class="sxs-lookup"><span data-stu-id="7afc7-114">The first task accomplished by the `TransferContactToDevice` function is to prompt the user to enter an object identifier for the parent object on the device (under which the content will be transferred).</span></span>


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



<span data-ttu-id="7afc7-115">L’étape suivante est la récupération des propriétés de contact, qui sera utilisée lorsque l’exemple écrit le nouveau contact sur l’appareil.</span><span class="sxs-lookup"><span data-stu-id="7afc7-115">The next step is the retrieval of contact properties, which will be used when the sample writes the new contact to the device.</span></span> <span data-ttu-id="7afc7-116">La récupération des propriétés de contact est effectuée par la `GetRequiredPropertiesForPropertiesOnlyContact` fonction d’assistance.</span><span class="sxs-lookup"><span data-stu-id="7afc7-116">The retrieval of contact properties is performed by the `GetRequiredPropertiesForPropertiesOnlyContact` helper function.</span></span>


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



<span data-ttu-id="7afc7-117">Cette fonction écrit les données suivantes dans un objet **IPortableDeviceValues** .</span><span class="sxs-lookup"><span data-stu-id="7afc7-117">This function writes the following data to an **IPortableDeviceValues** object.</span></span>

-   <span data-ttu-id="7afc7-118">Identificateur d’objet pour le parent du contact sur l’appareil.</span><span class="sxs-lookup"><span data-stu-id="7afc7-118">The object identifier for the contact's parent on the device.</span></span> <span data-ttu-id="7afc7-119">(Il s’agit de la destination dans laquelle l’appareil stockera l’objet.)</span><span class="sxs-lookup"><span data-stu-id="7afc7-119">(This is the destination where the device will store the object.)</span></span>
-   <span data-ttu-id="7afc7-120">Type d’objet (un contact).</span><span class="sxs-lookup"><span data-stu-id="7afc7-120">The object type (a contact).</span></span>
-   <span data-ttu-id="7afc7-121">Nom du contact (chaîne codée en dur de « John Kane »).</span><span class="sxs-lookup"><span data-stu-id="7afc7-121">The contact name (a hard coded string of "John Kane").</span></span>
-   <span data-ttu-id="7afc7-122">Numéro de téléphone du contact (chaîne codée en dur « 425-555-0123 »).</span><span class="sxs-lookup"><span data-stu-id="7afc7-122">The contact phone number (a hard-coded string of "425-555-0123").</span></span>

<span data-ttu-id="7afc7-123">La dernière étape crée l’objet Propriétés uniquement sur l’appareil (à l’aide des propriétés définies par la `GetRequiredPropertiesForPropertiesOnlyContact` fonction d’assistance).</span><span class="sxs-lookup"><span data-stu-id="7afc7-123">The final step creates the properties-only object on the device (using the properties set by the `GetRequiredPropertiesForPropertiesOnlyContact` helper function).</span></span> <span data-ttu-id="7afc7-124">Pour ce faire, vous devez appeler la méthode **IPortableDeviceContent :: CreateObjectWithPropertiesOnly** .</span><span class="sxs-lookup"><span data-stu-id="7afc7-124">This is accomplished by calling the **IPortableDeviceContent::CreateObjectWithPropertiesOnly** method.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="7afc7-125">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="7afc7-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7afc7-126">**Interface IPortableDevice**</span><span class="sxs-lookup"><span data-stu-id="7afc7-126">**IPortableDevice Interface**</span></span>](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevice)
</dt> <dt>

[<span data-ttu-id="7afc7-127">**Interface IPortableDeviceContent**</span><span class="sxs-lookup"><span data-stu-id="7afc7-127">**IPortableDeviceContent Interface**</span></span>](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecontent)
</dt> <dt>

[<span data-ttu-id="7afc7-128">**Interface IPortableDeviceValues**</span><span class="sxs-lookup"><span data-stu-id="7afc7-128">**IPortableDeviceValues Interface**</span></span>](iportabledevicevalues.md)
</dt> <dt>

[<span data-ttu-id="7afc7-129">**Guide de programmation**</span><span class="sxs-lookup"><span data-stu-id="7afc7-129">**Programming Guide**</span></span>](programming-guide.md)
</dt> </dl>

 

 



