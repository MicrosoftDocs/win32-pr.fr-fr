---
title: Inscription des appareils
description: Inscription des appareils
ms.assetid: 64a6f366-1317-47b6-94a2-ca2ef14d1f88
keywords:
- Windows Media Format SDK, inscription de l’appareil
- Windows Media Format SDK, inscription des appareils
- ASF (Advanced Systems Format), inscription de l’appareil
- ASF (format avancé des systèmes), inscription de l’appareil
- ASF (Advanced Systems Format), inscription des appareils
- ASF (format des systèmes avancés), inscription des appareils
- gestion des droits numériques (DRM), inscription de l’appareil
- DRM (gestion des droits numériques), inscription de l’appareil
- gestion des droits numériques (DRM), inscription des appareils
- DRM (gestion des droits numériques), inscription des appareils
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fcf4954d9b59abfb62f3a86127a387299d45cb4a
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/19/2020
ms.locfileid: "104030802"
---
# <a name="device-registration"></a><span data-ttu-id="b2e25-113">Inscription des appareils</span><span class="sxs-lookup"><span data-stu-id="b2e25-113">Device Registration</span></span>

<span data-ttu-id="b2e25-114">Le kit de développement logiciel (SDK) Windows Media format permet d’accéder à la base de données d’inscription des appareils.</span><span class="sxs-lookup"><span data-stu-id="b2e25-114">The Windows Media Format SDK provides access to the device registration database.</span></span> <span data-ttu-id="b2e25-115">Cette base de données est sécurisée sur l’ordinateur client et est utilisée pour inscrire les appareils qui prennent en charge Windows Media DRM 10 pour les périphériques réseau.</span><span class="sxs-lookup"><span data-stu-id="b2e25-115">This database is secured on the client computer and is used to register devices that support Windows Media DRM 10 for Network Devices.</span></span>

<span data-ttu-id="b2e25-116">Quand un appareil est ajouté à un réseau auquel est connecté l’ordinateur client, ce dernier tente de contacter une application Windows Media DRM 10 pour les périphériques réseau.</span><span class="sxs-lookup"><span data-stu-id="b2e25-116">When a device is added to a network to which the client computer is connected, the device attempts to contact a Windows Media DRM 10 for Network Devices transmitter application.</span></span> <span data-ttu-id="b2e25-117">Après avoir établi la communication, l’appareil envoie un message de demande d’inscription.</span><span class="sxs-lookup"><span data-stu-id="b2e25-117">After establishing communications, the device sends a registration request message.</span></span>

<span data-ttu-id="b2e25-118">Votre application doit effectuer les étapes suivantes lorsqu’elle reçoit un message de demande d’inscription :</span><span class="sxs-lookup"><span data-stu-id="b2e25-118">Your application should perform the following steps when it receives a registration request message:</span></span>

1.  <span data-ttu-id="b2e25-119">Analysez le message en appelant la méthode [**IWMDRMMessageParser ::P arseregistrationreqmsg**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmmessageparser-parseregistrationreqmsg) .</span><span class="sxs-lookup"><span data-stu-id="b2e25-119">Parse the message by calling the [**IWMDRMMessageParser::ParseRegistrationReqMsg**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmmessageparser-parseregistrationreqmsg) method.</span></span> <span data-ttu-id="b2e25-120">Cette méthode récupère le certificat de l’appareil et le numéro de série de l’appareil, qui sont tous deux nécessaires pour identifier l’appareil.</span><span class="sxs-lookup"><span data-stu-id="b2e25-120">This method retrieves the device certificate and the device serial number, both of which are needed to identify the device.</span></span>
2.  <span data-ttu-id="b2e25-121">Appelez la méthode [**IWMDeviceRegistration :: GetRegisteredDeviceByID**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdeviceregistration-getregistereddevicebyid) , en passant le certificat et le numéro de série de l’appareil récupérés à l’étape 1.</span><span class="sxs-lookup"><span data-stu-id="b2e25-121">Call the [**IWMDeviceRegistration::GetRegisteredDeviceByID**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdeviceregistration-getregistereddevicebyid) method, passing in the certificate and device serial number retrieved in step 1.</span></span> <span data-ttu-id="b2e25-122">Si le périphérique est trouvé, il est déjà inscrit et vous pouvez ignorer l’étape suivante.</span><span class="sxs-lookup"><span data-stu-id="b2e25-122">If the device is found, it is already registered and you can skip the next step.</span></span>
3.  <span data-ttu-id="b2e25-123">Appelez la méthode [**IWMDeviceRegistration :: RegisterDevice**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdeviceregistration-registerdevice) pour ajouter l’appareil à la base de données d’inscription des appareils.</span><span class="sxs-lookup"><span data-stu-id="b2e25-123">Call the [**IWMDeviceRegistration::RegisterDevice**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdeviceregistration-registerdevice) method to add the device to the device registration database.</span></span>

<span data-ttu-id="b2e25-124">Vous pouvez accéder aux informations sur n’importe quel appareil de la base de données d’inscription en extrayant l’objet d’appareil inscrit qui lui est associé.</span><span class="sxs-lookup"><span data-stu-id="b2e25-124">You can access information about any device in the registration database by retrieving the registered device object associated with it.</span></span> <span data-ttu-id="b2e25-125">Il existe deux façons d’obtenir un objet d’appareil inscrit.</span><span class="sxs-lookup"><span data-stu-id="b2e25-125">There are two ways to get a registered device object.</span></span> <span data-ttu-id="b2e25-126">Si vous avez le certificat et le numéro de série de l’appareil, vous pouvez appeler la méthode [**IWMDeviceRegistration :: GetRegisteredDeviceByID**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdeviceregistration-getregistereddevicebyid) .</span><span class="sxs-lookup"><span data-stu-id="b2e25-126">If you have the certificate and serial number of the device, you can call the [**IWMDeviceRegistration::GetRegisteredDeviceByID**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdeviceregistration-getregistereddevicebyid) method.</span></span> <span data-ttu-id="b2e25-127">Si vous n’avez pas le certificat et le numéro de série de l’appareil, vous pouvez énumérer tous les appareils dans la base de données en appelant [**IWMDeviceRegistration :: GetFirstRegisteredDevice**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdeviceregistration-getfirstregistereddevice) suivi d’appels répétés à [**IWMDeviceRegistration :: GetNextRegisteredDevice**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdeviceregistration-getnextregistereddevice) jusqu’à ce qu’un appel retourne la \_ valeur false.</span><span class="sxs-lookup"><span data-stu-id="b2e25-127">If you do not have the certificate and serial number of the device, you can enumerate all the devices in the database by calling [**IWMDeviceRegistration::GetFirstRegisteredDevice**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdeviceregistration-getfirstregistereddevice) followed by repeated calls to [**IWMDeviceRegistration::GetNextRegisteredDevice**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdeviceregistration-getnextregistereddevice) until a call returns S\_FALSE.</span></span>

<span data-ttu-id="b2e25-128">Pour que votre application puisse envoyer des données à un appareil, vous devez vous assurer que l’appareil est approuvé, validé et ouvert.</span><span class="sxs-lookup"><span data-stu-id="b2e25-128">Before your application can send data to a device, you must ensure that the device is approved, validated, and open.</span></span>

<span data-ttu-id="b2e25-129">L’approbation de l’appareil doit impliquer l’interaction avec l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="b2e25-129">Device approval should involve interaction with the user.</span></span> <span data-ttu-id="b2e25-130">Lorsqu’un appareil envoie un message d’inscription, votre application peut inviter l’utilisateur à décider s’il s’agit d’un appareil qui doit recevoir les données de cet utilisateur.</span><span class="sxs-lookup"><span data-stu-id="b2e25-130">When a device sends a registration message, your application can prompt the user to decide whether the device is one that should receive that user's data.</span></span> <span data-ttu-id="b2e25-131">Ensuite, mettez à jour la base de données d’inscription des appareils en appelant la méthode [**IWMRegisteredDevice :: Approve**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmregistereddevice-approve) , en passant **true** ou **false** selon le cas.</span><span class="sxs-lookup"><span data-stu-id="b2e25-131">Then update the device registration database by calling the [**IWMRegisteredDevice::Approve**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmregistereddevice-approve) method, passing **TRUE** or **FALSE** as appropriate.</span></span>

<span data-ttu-id="b2e25-132">La validation est également appelée détection de proximité.</span><span class="sxs-lookup"><span data-stu-id="b2e25-132">Validation is also called proximity detection.</span></span> <span data-ttu-id="b2e25-133">Il s’agit d’un processus par lequel les objets DRM internes du kit de développement logiciel (SDK) de format Windows Media déterminent si l’appareil est « presque » suffisant pour l’ordinateur exécutant votre application afin de transmettre en toute sécurité des médias.</span><span class="sxs-lookup"><span data-stu-id="b2e25-133">This is a process by which the internal DRM objects of the Windows Media Format SDK determine whether the device is "near" enough to the computer running your application to securely transmit media.</span></span> <span data-ttu-id="b2e25-134">La proximité est déterminée par le temps nécessaire pour obtenir une réponse à un message.</span><span class="sxs-lookup"><span data-stu-id="b2e25-134">Nearness is determined by the time it takes to get a response to a message.</span></span> <span data-ttu-id="b2e25-135">Cette fonctionnalité est conçue pour empêcher les utilisateurs non autorisés d’accéder à votre réseau et d’obtenir votre support sécurisé.</span><span class="sxs-lookup"><span data-stu-id="b2e25-135">This feature is intended to prevent unauthorized users from accessing your network and obtaining your secured media.</span></span> <span data-ttu-id="b2e25-136">Pour plus d’informations, consultez exécution de la [détection de proximité](performing-proximity-detection.md).</span><span class="sxs-lookup"><span data-stu-id="b2e25-136">For more information, see [Performing Proximity Detection](performing-proximity-detection.md).</span></span>

<span data-ttu-id="b2e25-137">Pour ouvrir un appareil, appelez [**IWMRegisteredDevice :: Open**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmregistereddevice-open).</span><span class="sxs-lookup"><span data-stu-id="b2e25-137">To open a device, call [**IWMRegisteredDevice::Open**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmregistereddevice-open).</span></span>

> [!Note]  
> <span data-ttu-id="b2e25-138">DRM n’est pas pris en charge par la version x64 de ce kit de développement logiciel (SDK).</span><span class="sxs-lookup"><span data-stu-id="b2e25-138">DRM is not supported by the x64-based version of this SDK.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="b2e25-139">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="b2e25-139">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b2e25-140">**IWMRegisteredDevice**</span><span class="sxs-lookup"><span data-stu-id="b2e25-140">**IWMRegisteredDevice**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmregistereddevice)
</dt> <dt>

[<span data-ttu-id="b2e25-141">**Utilisation du protocole Windows Media DRM 10 pour les périphériques réseau**</span><span class="sxs-lookup"><span data-stu-id="b2e25-141">**Using the Windows Media DRM 10 for Network Devices Protocol**</span></span>](using-the-windows-media-drm-10-for-network-devices-protocol.md)
</dt> </dl>

 

 




