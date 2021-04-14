---
title: Interface IBasicDevice
description: Encapsule les méthodes et les événements nécessaires pour modéliser un appareil DLNA.
ms.assetid: E4F99A11-4ED5-44CB-BE16-CBB558412ED4
keywords:
- API de diffusion multimédia en continu de l’interface IBasicDevice
- API de diffusion multimédia en continu de l’interface IBasicDevice, décrite
topic_type:
- apiref
api_name:
- IBasicDevice
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 1567605fb160fc69ac933bb94a0b0282e35616d5
ms.sourcegitcommit: 89f99926f946dc6c5ea600fb7c41f6b19ceac516
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/21/2020
ms.locfileid: "104383244"
---
# <a name="ibasicdevice-interface"></a><span data-ttu-id="a97c6-105">Interface IBasicDevice</span><span class="sxs-lookup"><span data-stu-id="a97c6-105">IBasicDevice interface</span></span>

<span data-ttu-id="a97c6-106">Encapsule les méthodes et les événements nécessaires pour modéliser un appareil DLNA.</span><span class="sxs-lookup"><span data-stu-id="a97c6-106">Encapsulates the methods and events needed to model a DLNA Device.</span></span>

## <a name="members"></a><span data-ttu-id="a97c6-107">Membres</span><span class="sxs-lookup"><span data-stu-id="a97c6-107">Members</span></span>

<span data-ttu-id="a97c6-108">L’interface **IBasicDevice** hérite de [**IInspectable**](/windows/desktop/api/inspectable/nn-inspectable-iinspectable).</span><span class="sxs-lookup"><span data-stu-id="a97c6-108">The **IBasicDevice** interface inherits from [**IInspectable**](/windows/desktop/api/inspectable/nn-inspectable-iinspectable).</span></span> <span data-ttu-id="a97c6-109">**IBasicDevice** a également les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="a97c6-109">**IBasicDevice** also has these types of members:</span></span>

-   [<span data-ttu-id="a97c6-110">Méthodes</span><span class="sxs-lookup"><span data-stu-id="a97c6-110">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="a97c6-111">Méthodes</span><span class="sxs-lookup"><span data-stu-id="a97c6-111">Methods</span></span>

<span data-ttu-id="a97c6-112">L’interface **IBasicDevice** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="a97c6-112">The **IBasicDevice** interface has these methods.</span></span>



| <span data-ttu-id="a97c6-113">Méthode</span><span class="sxs-lookup"><span data-stu-id="a97c6-113">Method</span></span>                                                                                 | <span data-ttu-id="a97c6-114">Description</span><span class="sxs-lookup"><span data-stu-id="a97c6-114">Description</span></span>                                                                                                                    |
|:---------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a97c6-115">**Ajouter \_ ConnectionStatusChanged**</span><span class="sxs-lookup"><span data-stu-id="a97c6-115">**add\_ConnectionStatusChanged**</span></span>](ibasicdevice-add-connectionstatuschanged.md)       | <span data-ttu-id="a97c6-116">Inscrit un gestionnaire d’événements pour l’événement [**ConnectionStatusChanged**](connectionstatuschanged.md) .</span><span class="sxs-lookup"><span data-stu-id="a97c6-116">Registers an event handler for the [**ConnectionStatusChanged**](connectionstatuschanged.md) event.</span></span><br/>                |
| [<span data-ttu-id="a97c6-117">**CanWakeDevices**</span><span class="sxs-lookup"><span data-stu-id="a97c6-117">**CanWakeDevices**</span></span>](ibasicdevice-canwakedevices.md)                                  | <span data-ttu-id="a97c6-118">Récupère une valeur qui indique si l’appareil peut sortir de veille.</span><span class="sxs-lookup"><span data-stu-id="a97c6-118">Retrieves a value that indicates if the device can wake.</span></span><br/>                                                            |
| <span data-ttu-id="a97c6-119">[**ConnectionStatus**](/previous-versions/windows/desktop/legacy/hh828873(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="a97c6-119">[**ConnectionStatus**](/previous-versions/windows/desktop/legacy/hh828873(v=vs.85))</span></span>                              | <span data-ttu-id="a97c6-120">Retourne une valeur d’énumération indiquant si l’appareil est actuellement en ligne, hors ligne ou en veille, mais en éveil.</span><span class="sxs-lookup"><span data-stu-id="a97c6-120">Returns an enumeration value indicating whether the device is currently on-line, off-line or sleeping but wakeable.</span></span><br/> |
| [<span data-ttu-id="a97c6-121">**Description**</span><span class="sxs-lookup"><span data-stu-id="a97c6-121">**Description**</span></span>](ibasicdevice-description.md)                                        | <span data-ttu-id="a97c6-122">Récupère une description de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="a97c6-122">Retrieves a description of the device.</span></span><br/>                                                                              |
| [<span data-ttu-id="a97c6-123">**DiscoveredOnCurrentNetwork**</span><span class="sxs-lookup"><span data-stu-id="a97c6-123">**DiscoveredOnCurrentNetwork**</span></span>](ibasicdevice-discoveredoncurrentnetwork.md)          | <span data-ttu-id="a97c6-124">Récupère une valeur qui indique si l’appareil se trouve sur le réseau actuel.</span><span class="sxs-lookup"><span data-stu-id="a97c6-124">Retrieves a value that indicates if the device is on the current network.</span></span><br/>                                           |
| [<span data-ttu-id="a97c6-125">**FriendlyName**</span><span class="sxs-lookup"><span data-stu-id="a97c6-125">**FriendlyName**</span></span>](ibasicdevice-friendlyname.md)                                      | <span data-ttu-id="a97c6-126">Récupère le nom convivial de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="a97c6-126">Retrieves the device s friendly name.</span></span><br/>                                                                               |
| [<span data-ttu-id="a97c6-127">**Icônes**</span><span class="sxs-lookup"><span data-stu-id="a97c6-127">**Icons**</span></span>](ibasicdevice-icons.md)                                                    | <span data-ttu-id="a97c6-128">Retourne un vecteur d’interfaces [**IDeviceIcon**](/previous-versions/windows/desktop/api/windows.media.streaming/nn-windows-media-streaming-ideviceicon) .</span><span class="sxs-lookup"><span data-stu-id="a97c6-128">Returns a vector of [**IDeviceIcon**](/previous-versions/windows/desktop/api/windows.media.streaming/nn-windows-media-streaming-ideviceicon) interfaces.</span></span><br/>                                                  |
| [<span data-ttu-id="a97c6-129">**AdressesIP**</span><span class="sxs-lookup"><span data-stu-id="a97c6-129">**IpAddresses**</span></span>](ibasicdevice-ipaddresses.md)                                        | <span data-ttu-id="a97c6-130">Retourne un vecteur d’adresses IP.</span><span class="sxs-lookup"><span data-stu-id="a97c6-130">Returns a vector of IP addresses.</span></span><br/>                                                                                   |
| [<span data-ttu-id="a97c6-131">**ManufacturerName**</span><span class="sxs-lookup"><span data-stu-id="a97c6-131">**ManufacturerName**</span></span>](ibasicdevice-manufacturername.md)                              | <span data-ttu-id="a97c6-132">Récupère le nom du fabricant de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="a97c6-132">Retrieves the device s manufacturer name.</span></span><br/>                                                                           |
| [<span data-ttu-id="a97c6-133">**ManufacturerUrl**</span><span class="sxs-lookup"><span data-stu-id="a97c6-133">**ManufacturerUrl**</span></span>](ibasicdevice-manufacturerurl.md)                                | <span data-ttu-id="a97c6-134">Récupère l’URL du fabricant de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="a97c6-134">Retrieves the device s manufacturer URL.</span></span><br/>                                                                            |
| [<span data-ttu-id="a97c6-135">**ModelName**</span><span class="sxs-lookup"><span data-stu-id="a97c6-135">**ModelName**</span></span>](ibasicdevice-modelname.md)                                            | <span data-ttu-id="a97c6-136">Récupère le nom du modèle de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="a97c6-136">Retrieves the device s model name.</span></span><br/>                                                                                  |
| [<span data-ttu-id="a97c6-137">**ModelNumber**</span><span class="sxs-lookup"><span data-stu-id="a97c6-137">**ModelNumber**</span></span>](ibasicdevice-modelnumber.md)                                        | <span data-ttu-id="a97c6-138">Récupère le numéro de modèle de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="a97c6-138">Retrieves the device s model number.</span></span><br/>                                                                                |
| [<span data-ttu-id="a97c6-139">**ModelUrl**</span><span class="sxs-lookup"><span data-stu-id="a97c6-139">**ModelUrl**</span></span>](ibasicdevice-modelurl.md)                                              | <span data-ttu-id="a97c6-140">Récupère l’URL du modèle de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="a97c6-140">Retrieves the device s model URL.</span></span><br/>                                                                                   |
| [<span data-ttu-id="a97c6-141">**PhysicalAddresses**</span><span class="sxs-lookup"><span data-stu-id="a97c6-141">**PhysicalAddresses**</span></span>](ibasicdevice-physicaladdresses.md)                            | <span data-ttu-id="a97c6-142">Retourne un vecteur d’adresses physiques.</span><span class="sxs-lookup"><span data-stu-id="a97c6-142">Returns a vector of physical addresses.</span></span><br/>                                                                             |
| [<span data-ttu-id="a97c6-143">**PresentationUrl**</span><span class="sxs-lookup"><span data-stu-id="a97c6-143">**PresentationUrl**</span></span>](ibasicdevice-presentationurl.md)                                | <span data-ttu-id="a97c6-144">Récupère l’URL de présentation de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="a97c6-144">Retrieves the device s presentation URL.</span></span><br/>                                                                            |
| [<span data-ttu-id="a97c6-145">**RemoteStreamingUrls**</span><span class="sxs-lookup"><span data-stu-id="a97c6-145">**RemoteStreamingUrls**</span></span>](ibasicdevice-remotestreamingurls.md)                        | <span data-ttu-id="a97c6-146">Retourne un vecteur d’URL de diffusion en continu à distance.</span><span class="sxs-lookup"><span data-stu-id="a97c6-146">Returns a vector of remote streaming URLs.</span></span><br/>                                                                          |
| [<span data-ttu-id="a97c6-147">**supprimer \_ ConnectionStatusChanged**</span><span class="sxs-lookup"><span data-stu-id="a97c6-147">**remove\_ConnectionStatusChanged**</span></span>](ibasicdevice-remove-connectionstatuschanged.md) | <span data-ttu-id="a97c6-148">Annule l’inscription d’un gestionnaire d’événements pour l’événement [**ConnectionStatusChanged**](connectionstatuschanged.md) .</span><span class="sxs-lookup"><span data-stu-id="a97c6-148">Unregisters an event handler for the [**ConnectionStatusChanged**](connectionstatuschanged.md) event.</span></span><br/>              |
| [<span data-ttu-id="a97c6-149">**SerialNumber**</span><span class="sxs-lookup"><span data-stu-id="a97c6-149">**SerialNumber**</span></span>](ibasicdevice-serialnumber.md)                                      | <span data-ttu-id="a97c6-150">Récupère le numéro de série de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="a97c6-150">Retrieves the device s serial number.</span></span><br/>                                                                               |
| [<span data-ttu-id="a97c6-151">**Entrer**</span><span class="sxs-lookup"><span data-stu-id="a97c6-151">**Type**</span></span>](ibasicdevice-type.md)                                                      | <span data-ttu-id="a97c6-152">Récupère une valeur d’énumération indiquant le type d’appareil de l’appareil DLNA.</span><span class="sxs-lookup"><span data-stu-id="a97c6-152">Retrieves an enumeration value indicating the device type of the DLNA device.</span></span><br/>                                       |
| [<span data-ttu-id="a97c6-153">**UniqueDeviceName**</span><span class="sxs-lookup"><span data-stu-id="a97c6-153">**UniqueDeviceName**</span></span>](ibasicdevice-uniquedevicename.md)                              | <span data-ttu-id="a97c6-154">Récupère le nom d’appareil unique de l’appareil (UDN).</span><span class="sxs-lookup"><span data-stu-id="a97c6-154">Retrieves the device s unique device name (UDN).</span></span><br/>                                                                    |



 

## <a name="see-also"></a><span data-ttu-id="a97c6-155">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a97c6-155">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a97c6-156">**IInspectable**</span><span class="sxs-lookup"><span data-stu-id="a97c6-156">**IInspectable**</span></span>](/windows/desktop/api/inspectable/nn-inspectable-iinspectable)
</dt> </dl>

 

