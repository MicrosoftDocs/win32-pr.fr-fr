---
title: Objet d’inscription de l’appareil
description: Objet d’inscription de l’appareil
ms.assetid: 6a23b314-deec-47aa-b12e-cb8f4ff71fb6
keywords:
- Windows Media Format SDK, objets d’inscription d’appareils
- ASF (Advanced Systems Format), objets d’inscription des appareils
- ASF (format des systèmes avancés), objets d’inscription des appareils
- objets, objets d’inscription de l’appareil
- objets d’inscription d’appareil
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 67ba6b72637cf7ba439d0bb38109645742cda4ac
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/19/2020
ms.locfileid: "106509634"
---
# <a name="device-registration-object"></a><span data-ttu-id="d9f1b-108">Objet d’inscription de l’appareil</span><span class="sxs-lookup"><span data-stu-id="d9f1b-108">Device Registration Object</span></span>

<span data-ttu-id="d9f1b-109">L’objet d’inscription de l’appareil gère la base de données d’inscription des appareils.</span><span class="sxs-lookup"><span data-stu-id="d9f1b-109">The device registration object manages the device registration database.</span></span> <span data-ttu-id="d9f1b-110">Cette base de données stocke des informations sur les périphériques réseau, tels que les lecteurs vidéo configurés, qui sont connectés à l’ordinateur client.</span><span class="sxs-lookup"><span data-stu-id="d9f1b-110">This database stores information about network devices, such as set-top video players, that are connected to the client computer.</span></span> <span data-ttu-id="d9f1b-111">L’objectif principal de la base de données d’inscription des appareils est de gérer les appareils qui utilisent le protocole Windows Media DRM 10 pour les périphériques réseau pour recevoir des flux de données sécurisés.</span><span class="sxs-lookup"><span data-stu-id="d9f1b-111">The primary purpose of the device registration database is to manage devices that use the Windows Media DRM 10 for Network Devices protocol to receive secured data streams.</span></span>

<span data-ttu-id="d9f1b-112">Si votre application prend en charge Windows Media DRM 10 pour les périphériques réseau, vous devez utiliser les interfaces de cet objet pour inscrire des périphériques réseau et valider ces appareils.</span><span class="sxs-lookup"><span data-stu-id="d9f1b-112">If your application supports Windows Media DRM 10 for Network Devices, you must use the interfaces of this object to register network devices, and to validate those devices.</span></span> <span data-ttu-id="d9f1b-113">Vous pouvez également utiliser la base de données d’inscription d’appareils pour stocker des informations sur les périphériques réseau qui n’utilisent pas Windows Media DRM 10 pour les périphériques réseau, bien que toutes les informations de la base de données ne s’appliquent pas à ces appareils.</span><span class="sxs-lookup"><span data-stu-id="d9f1b-113">You can also use the device registration database to store information about network devices that do not use Windows Media DRM 10 for Network Devices, although not all of the information in the database will apply to such devices.</span></span>

<span data-ttu-id="d9f1b-114">L’objet d’inscription de l’appareil est créé par la fonction [**WMCreateDeviceRegistration**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatedeviceregistration) , qui définit un pointeur vers une interface **IWMDeviceRegistration** .</span><span class="sxs-lookup"><span data-stu-id="d9f1b-114">The device registration object is created by the [**WMCreateDeviceRegistration**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatedeviceregistration) function, which sets a pointer to an **IWMDeviceRegistration** interface.</span></span> <span data-ttu-id="d9f1b-115">Les autres méthodes de l’objet d’inscription de l’appareil peuvent être obtenues en appelant la méthode **QueryInterface** .</span><span class="sxs-lookup"><span data-stu-id="d9f1b-115">The other methods of the device registration object can be obtained by calling the **QueryInterface** method.</span></span>

<span data-ttu-id="d9f1b-116">Les interfaces suivantes sont prises en charge par l’objet d’inscription de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="d9f1b-116">The following interfaces are supported by the device registration object.</span></span>



| <span data-ttu-id="d9f1b-117">Interface</span><span class="sxs-lookup"><span data-stu-id="d9f1b-117">Interface</span></span>                                              | <span data-ttu-id="d9f1b-118">Description</span><span class="sxs-lookup"><span data-stu-id="d9f1b-118">Description</span></span>                               |
|--------------------------------------------------------|-------------------------------------------|
| [<span data-ttu-id="d9f1b-119">**IWMDeviceRegistration**</span><span class="sxs-lookup"><span data-stu-id="d9f1b-119">**IWMDeviceRegistration**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdeviceregistration) | <span data-ttu-id="d9f1b-120">Gère la base de données d’inscription des appareils.</span><span class="sxs-lookup"><span data-stu-id="d9f1b-120">Manages the device registration database.</span></span> |
| [<span data-ttu-id="d9f1b-121">**IWMDRMMessageParser**</span><span class="sxs-lookup"><span data-stu-id="d9f1b-121">**IWMDRMMessageParser**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmmessageparser)     | <span data-ttu-id="d9f1b-122">Analyse les messages envoyés par les appareils.</span><span class="sxs-lookup"><span data-stu-id="d9f1b-122">Parses messages sent by devices.</span></span>          |
| [<span data-ttu-id="d9f1b-123">**IWMProximityDetection**</span><span class="sxs-lookup"><span data-stu-id="d9f1b-123">**IWMProximityDetection**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmproximitydetection) | <span data-ttu-id="d9f1b-124">Gère la validation de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="d9f1b-124">Manages device validation.</span></span>                |



 

<span data-ttu-id="d9f1b-125">L’interface de rappel suivante doit être implémentée par l’application afin d’utiliser les méthodes de l’interface **IWMProximityDetection** .</span><span class="sxs-lookup"><span data-stu-id="d9f1b-125">The following callback interface must be implemented by the application in order to use the methods of the **IWMProximityDetection** interface.</span></span>



| <span data-ttu-id="d9f1b-126">Interface</span><span class="sxs-lookup"><span data-stu-id="d9f1b-126">Interface</span></span>                                      | <span data-ttu-id="d9f1b-127">Description</span><span class="sxs-lookup"><span data-stu-id="d9f1b-127">Description</span></span>                                                                |
|------------------------------------------------|----------------------------------------------------------------------------|
| [<span data-ttu-id="d9f1b-128">**IWMStatusCallback**</span><span class="sxs-lookup"><span data-stu-id="d9f1b-128">**IWMStatusCallback**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstatuscallback) | <span data-ttu-id="d9f1b-129">Reçoit des messages d’état des processus qui s’exécutent dans un thread séparé.</span><span class="sxs-lookup"><span data-stu-id="d9f1b-129">Receives status messages from processes that execute in a separate thread.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="d9f1b-130">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="d9f1b-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d9f1b-131">**Objets**</span><span class="sxs-lookup"><span data-stu-id="d9f1b-131">**Objects**</span></span>](objects.md)
</dt> </dl>

 

 




