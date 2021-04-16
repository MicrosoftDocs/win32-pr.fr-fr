---
description: Récupération des événements pris en charge par un appareil
ms.assetid: 951b300f-03de-4a3d-9356-e3a7b5b17fdb
title: Récupération des événements pris en charge par un appareil
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a542a34d0938c7e2ff86118818714f18b1224f7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104530250"
---
# <a name="retrieving-the-events-supported-by-a-device"></a><span data-ttu-id="44205-103">Récupération des événements pris en charge par un appareil</span><span class="sxs-lookup"><span data-stu-id="44205-103">Retrieving the Events Supported by a Device</span></span>

<span data-ttu-id="44205-104">Certains pilotes WPD prennent en charge la notification d’événement.</span><span class="sxs-lookup"><span data-stu-id="44205-104">Some WPD drivers support event notification.</span></span> <span data-ttu-id="44205-105">Cela signifie qu’une application peut s’inscrire auprès du pilote pour recevoir une notification lorsqu’une action spécifique se produit.</span><span class="sxs-lookup"><span data-stu-id="44205-105">This means that an application can register with the driver to receive a notification when a specific action occurs.</span></span> <span data-ttu-id="44205-106">Par exemple, une application peut s’inscrire pour recevoir une notification lors de l’ajout ou de la suppression d’un objet.</span><span class="sxs-lookup"><span data-stu-id="44205-106">For example, an application can register to receive a notification when an object is added or removed.</span></span>

<span data-ttu-id="44205-107">Une application peut surveiller dix événements prédéfinis.</span><span class="sxs-lookup"><span data-stu-id="44205-107">There are ten predefined events that an application can monitor.</span></span> <span data-ttu-id="44205-108">Ils sont décrits dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="44205-108">They are described in the following table.</span></span>



| <span data-ttu-id="44205-109">Événement</span><span class="sxs-lookup"><span data-stu-id="44205-109">Event</span></span>                       | <span data-ttu-id="44205-110">Description</span><span class="sxs-lookup"><span data-stu-id="44205-110">Description</span></span>                                                                                                                            |
|-----------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="44205-111">Fonctionnalités de l’appareil mises à jour</span><span class="sxs-lookup"><span data-stu-id="44205-111">Device capabilities updated</span></span> | <span data-ttu-id="44205-112">Se produit lorsque les fonctionnalités de l’appareil ont été modifiées.</span><span class="sxs-lookup"><span data-stu-id="44205-112">Occurs when the device capabilities have changed.</span></span>                                                                                      |
| <span data-ttu-id="44205-113">Appareil supprimé</span><span class="sxs-lookup"><span data-stu-id="44205-113">Device removed</span></span>              | <span data-ttu-id="44205-114">Se produit lorsque l’appareil est débranché.</span><span class="sxs-lookup"><span data-stu-id="44205-114">Occurs when the device is unplugged.</span></span>                                                                                                   |
| <span data-ttu-id="44205-115">Réinitialisation d’appareil</span><span class="sxs-lookup"><span data-stu-id="44205-115">Device reset</span></span>                | <span data-ttu-id="44205-116">Se produit lorsque l’appareil a été réinitialisé.</span><span class="sxs-lookup"><span data-stu-id="44205-116">Occurs when the device has been reset.</span></span>                                                                                                 |
| <span data-ttu-id="44205-117">Objet ajouté</span><span class="sxs-lookup"><span data-stu-id="44205-117">Object added</span></span>                | <span data-ttu-id="44205-118">Se produit lorsqu’un nouvel objet est disponible sur l’appareil.</span><span class="sxs-lookup"><span data-stu-id="44205-118">Occurs after a new object becomes available on the device.</span></span>                                                                             |
| <span data-ttu-id="44205-119">Objet supprimé</span><span class="sxs-lookup"><span data-stu-id="44205-119">Object removed</span></span>              | <span data-ttu-id="44205-120">Se produit après la suppression d’un objet de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="44205-120">Occurs after an object has been removed from the device.</span></span>                                                                               |
| <span data-ttu-id="44205-121">Transfert d’objets demandé</span><span class="sxs-lookup"><span data-stu-id="44205-121">Object transfer requested</span></span>   | <span data-ttu-id="44205-122">Indique qu’une demande a été effectuée pour transférer un objet.</span><span class="sxs-lookup"><span data-stu-id="44205-122">Indicates that a request has been made to transfer an object.</span></span>                                                                          |
| <span data-ttu-id="44205-123">Objet mis à jour</span><span class="sxs-lookup"><span data-stu-id="44205-123">Object updated</span></span>              | <span data-ttu-id="44205-124">Se produit après la mise à jour d’un objet ou de ses enfants.</span><span class="sxs-lookup"><span data-stu-id="44205-124">Occurs after either an object or its children has been updated.</span></span> <span data-ttu-id="44205-125">(Les clients connectés doivent ensuite mettre à jour leur vue de l’objet donné.)</span><span class="sxs-lookup"><span data-stu-id="44205-125">(Connected clients should then update their view of the given object.)</span></span> |
| <span data-ttu-id="44205-126">Format de stockage en cours</span><span class="sxs-lookup"><span data-stu-id="44205-126">Storage format in progress</span></span>  | <span data-ttu-id="44205-127">Se produit lorsque le stockage de l’appareil est mis en forme.</span><span class="sxs-lookup"><span data-stu-id="44205-127">Occurs when the device storage is being formatted.</span></span>                                                                                     |



 

<span data-ttu-id="44205-128">Pour obtenir la liste des constantes associées à ces événements, consultez la rubrique sur les [constantes d’événement](event-constants.md) .</span><span class="sxs-lookup"><span data-stu-id="44205-128">For a list of the constants associated with these events, see the [Event Constants](event-constants.md) topic.</span></span>

<span data-ttu-id="44205-129">La fonction ListSupportedEvents dans le module DeviceCapabilities. cpp illustre la récupération des événements pris en charge par un appareil donné.</span><span class="sxs-lookup"><span data-stu-id="44205-129">The ListSupportedEvents function in the DeviceCapabilities.cpp module demonstrates the retrieval of events supported by a given device.</span></span>

<span data-ttu-id="44205-130">Votre application peut récupérer les identificateurs des événements pris en charge par un appareil à l’aide des interfaces décrites dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="44205-130">Your application can retrieve the identifiers for events supported by a device using the interfaces described in the following table.</span></span>



| <span data-ttu-id="44205-131">Interface</span><span class="sxs-lookup"><span data-stu-id="44205-131">Interface</span></span>                                                                                      | <span data-ttu-id="44205-132">Description</span><span class="sxs-lookup"><span data-stu-id="44205-132">Description</span></span>                                               |
|------------------------------------------------------------------------------------------------|-----------------------------------------------------------|
| [<span data-ttu-id="44205-133">**Interface IPortableDeviceCapabilities**</span><span class="sxs-lookup"><span data-stu-id="44205-133">**IPortableDeviceCapabilities Interface**</span></span>](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecapabilities)                   | <span data-ttu-id="44205-134">Fournit l’accès aux méthodes de récupération d’événements prises en charge.</span><span class="sxs-lookup"><span data-stu-id="44205-134">Provides access to the supported-event retrieval methods.</span></span> |
| [<span data-ttu-id="44205-135">**Interface IPortableDevicePropVariantCollection**</span><span class="sxs-lookup"><span data-stu-id="44205-135">**IPortableDevicePropVariantCollection Interface**</span></span>](iportabledevicepropvariantcollection.md) | <span data-ttu-id="44205-136">Permet d’énumérer et de stocker les données de catégorie fonctionnelle.</span><span class="sxs-lookup"><span data-stu-id="44205-136">Used to enumerate and store functional-category data.</span></span>     |



 

<span data-ttu-id="44205-137">La première tâche accomplie par l’exemple d’application est la récupération d’un objet [**IPortableDeviceCapabilities**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecapabilities) , qui est utilisé pour récupérer les événements pris en charge par l’appareil donné.</span><span class="sxs-lookup"><span data-stu-id="44205-137">The first task accomplished by the sample application is the retrieval of an [**IPortableDeviceCapabilities**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecapabilities) object, which is used to retrieve the events supported by the given device.</span></span>


```C++
HRESULT hr = S_OK;
CComPtr<IPortableDeviceCapabilities>            pCapabilities;
CComPtr<IPortableDevicePropVariantCollection>   pEvents;
DWORD dwNumEvents = 0;

if (pDevice == NULL)
{
    printf("! A NULL IPortableDevice interface pointer was received\n");
    return;
}


// Get an IPortableDeviceCapabilities interface from the IPortableDevice interface to
// access the device capabilities-specific methods.
hr = pDevice->Capabilities(&pCapabilities);
if (FAILED(hr))
{
    printf("! Failed to get IPortableDeviceCapabilities from IPortableDevice, hr = 0x%lx\n",hr);
}
```



<span data-ttu-id="44205-138">Les événements pris en charge sont récupérés en appelant la méthode [**IPortableDeviceCapabilities :: GetSupportedEvents**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicecapabilities-getsupportedevents) .</span><span class="sxs-lookup"><span data-stu-id="44205-138">The supported events are retrieved by calling the [**IPortableDeviceCapabilities::GetSupportedEvents**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicecapabilities-getsupportedevents) method.</span></span> <span data-ttu-id="44205-139">Cette méthode récupère une collection d’identificateurs d’événements pour le périphérique donné et les stocke dans un objet [**IPortableDevicePropVariantCollection**](iportabledevicepropvariantcollection.md) pointé par l’argument pEvents.</span><span class="sxs-lookup"><span data-stu-id="44205-139">This method retrieves a collection of event identifiers for the given device and stores them in an [**IPortableDevicePropVariantCollection**](iportabledevicepropvariantcollection.md) object pointed to by the pEvents argument.</span></span>


```C++
if (SUCCEEDED(hr))
{
    hr = pCapabilities->GetSupportedEvents(&pEvents);
    if (FAILED(hr))
    {
        printf("! Failed to get supported events from the device, hr = 0x%lx\n",hr);
    }
}
```



<span data-ttu-id="44205-140">L’étape suivante consiste à récupérer le nombre d’événements pris en charge afin que l’application puisse itérer au sein de l’objet [**IPortableDevicePropVariantCollection**](iportabledevicepropvariantcollection.md) et récupérer l’identificateur pour chacun d’eux.</span><span class="sxs-lookup"><span data-stu-id="44205-140">The next step is to retrieve the count of supported events so that the application can iterate through the [**IPortableDevicePropVariantCollection**](iportabledevicepropvariantcollection.md) object and retrieve the identifier for each.</span></span>


```C++
if (SUCCEEDED(hr))
{
    hr = pEvents->GetCount(&dwNumEvents);
    if (FAILED(hr))
    {
        printf("! Failed to get number of supported events, hr = 0x%lx\n",hr);
    }
}

printf("\n%d Supported Events Found on the device\n\n", dwNumEvents);

// Loop through each event and display its name
if (SUCCEEDED(hr))
{
    for (DWORD dwIndex = 0; dwIndex < dwNumEvents; dwIndex++)
    {
        PROPVARIANT pv = {0};
        PropVariantInit(&pv);
        hr = pEvents->GetAt(dwIndex, &pv);
        if (SUCCEEDED(hr))
        {
            // We have an event.  It is assumed that
            // events are returned as VT_CLSID VarTypes.

            if (pv.puuid != NULL)
            {
                // Display the event name
                DisplayEvent(*pv.puuid);
                printf("\n");
                // Display the event options
                DisplayEventOptions(pCapabilities, *pv.puuid);
                printf("\n");
            }
        }

        PropVariantClear(&pv);
    }
}
```



## <a name="related-topics"></a><span data-ttu-id="44205-141">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="44205-141">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="44205-142">**Constantes d’événement**</span><span class="sxs-lookup"><span data-stu-id="44205-142">**Event Constants**</span></span>](event-constants.md)
</dt> <dt>

[<span data-ttu-id="44205-143">**Interface IPortableDevice**</span><span class="sxs-lookup"><span data-stu-id="44205-143">**IPortableDevice Interface**</span></span>](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevice)
</dt> <dt>

[<span data-ttu-id="44205-144">**Interface IPortableDeviceCapabilities**</span><span class="sxs-lookup"><span data-stu-id="44205-144">**IPortableDeviceCapabilities Interface**</span></span>](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecapabilities)
</dt> <dt>

[<span data-ttu-id="44205-145">**Interface IPortableDevicePropVariantCollection**</span><span class="sxs-lookup"><span data-stu-id="44205-145">**IPortableDevicePropVariantCollection Interface**</span></span>](iportabledevicepropvariantcollection.md)
</dt> <dt>

[<span data-ttu-id="44205-146">**Guide de programmation**</span><span class="sxs-lookup"><span data-stu-id="44205-146">**Programming Guide**</span></span>](programming-guide.md)
</dt> </dl>

 

 



