---
title: Interface IWMDRMDeviceApp
description: L’interface IWMDRMDeviceApp permet à une application de mesurer, de synchroniser des licences et de mettre à jour les composants DRM d’un appareil.
ms.assetid: e47167c2-ea14-4173-8ce9-8d8540a0fc73
keywords:
- Interface IWMDRMDeviceApp Windows Media Gestionnaire de périphériques
- Interface IWMDRMDeviceApp Windows Media Gestionnaire de périphériques, Description
topic_type:
- apiref
api_name:
- IWMDRMDeviceApp
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 9cf44295c9972d7549eb4a82fda7c415ba81c31d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "106544157"
---
# <a name="iwmdrmdeviceapp-interface"></a><span data-ttu-id="ebe4b-105">Interface IWMDRMDeviceApp</span><span class="sxs-lookup"><span data-stu-id="ebe4b-105">IWMDRMDeviceApp interface</span></span>

<span data-ttu-id="ebe4b-106">\[La fonctionnalité Windows Media DRM est déconseillée et ne doit pas être utilisée.</span><span class="sxs-lookup"><span data-stu-id="ebe4b-106">\[The Windows Media DRM feature is deprecated and should not be used.</span></span> <span data-ttu-id="ebe4b-107">Utilisez plutôt [Microsoft PlayReady](/windows/uwp/audio-video-camera/playready-client-sdk) .\]</span><span class="sxs-lookup"><span data-stu-id="ebe4b-107">Use [Microsoft PlayReady](/windows/uwp/audio-video-camera/playready-client-sdk) instead.\]</span></span>

<span data-ttu-id="ebe4b-108">L’interface **IWMDRMDeviceApp** permet à une application de mesurer, de synchroniser des licences et de mettre à jour les composants DRM d’un appareil.</span><span class="sxs-lookup"><span data-stu-id="ebe4b-108">The **IWMDRMDeviceApp** interface enables an application to meter, synchronize licenses, and update a device's DRM components.</span></span> <span data-ttu-id="ebe4b-109">Cette interface ne fonctionne que pour les appareils qui prennent en charge Windows Media DRM 10 pour les appareils mobiles.</span><span class="sxs-lookup"><span data-stu-id="ebe4b-109">This interface will only work with devices that support Windows Media DRM 10 for Portable Devices.</span></span>

<span data-ttu-id="ebe4b-110">Pour accéder à cette interface, appelez **CoCreateInstance**, en transmettant CLSID \_ WMDRMDeviceApp.</span><span class="sxs-lookup"><span data-stu-id="ebe4b-110">To get this interface, call **CoCreateInstance**, passing in CLSID\_WMDRMDeviceApp.</span></span>

> [!Note]  
> <span data-ttu-id="ebe4b-111">Cette interface est définie dans le fichier d’en-tête généré à partir de WMDRMDeviceApp. idl.</span><span class="sxs-lookup"><span data-stu-id="ebe4b-111">This interface is defined in the header file built from WMDRMDeviceApp.idl.</span></span> <span data-ttu-id="ebe4b-112">Cet en-tête **\# inclut**« WMDM. h ».</span><span class="sxs-lookup"><span data-stu-id="ebe4b-112">This header **\#include** s "wmdm.h".</span></span> <span data-ttu-id="ebe4b-113">Vous devrez peut-être modifier ce nom de fichier pour qu’il corresponde à l’en-tête généré à partir de WMDM. idl.</span><span class="sxs-lookup"><span data-stu-id="ebe4b-113">You might need to change this file name to match the header built from WMDM.idl.</span></span>

 

## <a name="members"></a><span data-ttu-id="ebe4b-114">Membres</span><span class="sxs-lookup"><span data-stu-id="ebe4b-114">Members</span></span>

<span data-ttu-id="ebe4b-115">L’interface **IWMDRMDeviceApp** hérite de l’interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="ebe4b-115">The **IWMDRMDeviceApp** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="ebe4b-116">**IWMDRMDeviceApp** a également les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="ebe4b-116">**IWMDRMDeviceApp** also has these types of members:</span></span>

-   [<span data-ttu-id="ebe4b-117">Méthodes</span><span class="sxs-lookup"><span data-stu-id="ebe4b-117">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="ebe4b-118">Méthodes</span><span class="sxs-lookup"><span data-stu-id="ebe4b-118">Methods</span></span>

<span data-ttu-id="ebe4b-119">L’interface **IWMDRMDeviceApp** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="ebe4b-119">The **IWMDRMDeviceApp** interface has these methods.</span></span>



| <span data-ttu-id="ebe4b-120">Méthode</span><span class="sxs-lookup"><span data-stu-id="ebe4b-120">Method</span></span>                                                                   | <span data-ttu-id="ebe4b-121">Description</span><span class="sxs-lookup"><span data-stu-id="ebe4b-121">Description</span></span>                                                                                                                                |
|:-------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="ebe4b-122">**AcquireDeviceData**</span><span class="sxs-lookup"><span data-stu-id="ebe4b-122">**AcquireDeviceData**</span></span>](iwmdrmdeviceapp-acquiredevicedata.md)           | <span data-ttu-id="ebe4b-123">Initialise ou réinitialise une horloge sécurisée de l’appareil</span><span class="sxs-lookup"><span data-stu-id="ebe4b-123">Initializes or resets a device secure clock</span></span><br/>                                                                                     |
| [<span data-ttu-id="ebe4b-124">**GenerateMeterChallenge**</span><span class="sxs-lookup"><span data-stu-id="ebe4b-124">**GenerateMeterChallenge**</span></span>](iwmdrmdeviceapp-generatemeterchallenge.md) | <span data-ttu-id="ebe4b-125">Acquiert des données de contrôle à partir d’un appareil.</span><span class="sxs-lookup"><span data-stu-id="ebe4b-125">Acquires metering data from a device.</span></span><br/>                                                                                           |
| [<span data-ttu-id="ebe4b-126">**ProcessMeterResponse**</span><span class="sxs-lookup"><span data-stu-id="ebe4b-126">**ProcessMeterResponse**</span></span>](iwmdrmdeviceapp-processmeterresponse.md)     | <span data-ttu-id="ebe4b-127">Réinitialise tout ou partie des nombres de contrôle sur un appareil, une fois que les données de l’appareil ont été envoyées et traitées par le serveur.</span><span class="sxs-lookup"><span data-stu-id="ebe4b-127">Resets some or all of the metering counts on a device, after data from the device has been sent to and processed by the server.</span></span><br/> |
| [<span data-ttu-id="ebe4b-128">**QueryDeviceStatus**</span><span class="sxs-lookup"><span data-stu-id="ebe4b-128">**QueryDeviceStatus**</span></span>](iwmdrmdeviceapp-querydevicestatus.md)           | <span data-ttu-id="ebe4b-129">Interroge un appareil pour obtenir son état et ses capacités DRM actuels.</span><span class="sxs-lookup"><span data-stu-id="ebe4b-129">Queries a device for its current DRM status and capabilities.</span></span><br/>                                                                   |
| [<span data-ttu-id="ebe4b-130">**SynchronizeLicenses**</span><span class="sxs-lookup"><span data-stu-id="ebe4b-130">**SynchronizeLicenses**</span></span>](iwmdrmdeviceapp-synchronizelicenses.md)       | <span data-ttu-id="ebe4b-131">Met à jour les licences sur un appareil lorsqu’elles arrivent à expiration.</span><span class="sxs-lookup"><span data-stu-id="ebe4b-131">Updates licenses on a device when they are close to expiring.</span></span><br/>                                                                   |



 

## <a name="see-also"></a><span data-ttu-id="ebe4b-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ebe4b-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ebe4b-133">**Gestion du contenu protégé dans l’application**</span><span class="sxs-lookup"><span data-stu-id="ebe4b-133">**Handling Protected Content in the Application**</span></span>](handling-protected-content-in-the-application.md)
</dt> <dt>

[<span data-ttu-id="ebe4b-134">**Interfaces pour les applications**</span><span class="sxs-lookup"><span data-stu-id="ebe4b-134">**Interfaces for Applications**</span></span>](interfaces-for-applications.md)
</dt> <dt>

[<span data-ttu-id="ebe4b-135">**Contrôle de l’utilisation du contenu**</span><span class="sxs-lookup"><span data-stu-id="ebe4b-135">**Metering Content Usage**</span></span>](metering-content-usage.md)
</dt> </dl>

 

