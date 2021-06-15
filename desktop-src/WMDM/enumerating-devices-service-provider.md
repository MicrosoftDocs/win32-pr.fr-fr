---
title: Énumération des appareils (WMDM)
description: Windows Media Gestionnaire de périphériques gère un cache d’appareils connectés. Découvrez comment Windows Media Gestionnaire de périphériques gère ou met à jour son cache.
ms.assetid: 7602da65-4c98-4766-b206-2129dad4cc2a
keywords:
- Gestionnaire de périphériques Windows Media, énumération des appareils
- Gestionnaire de périphériques, énumération des appareils
- Guide de programmation, énumération des appareils
- fournisseurs de services, énumération des appareils
- création de fournisseurs de services, énumération d’appareils
- énumération des appareils
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6f9b2fd3a891e2c52710bd9a2f6d46a78e9eb238
ms.sourcegitcommit: 51ef825fb48f15e1aa30e8795988f10dc2b2155c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/14/2021
ms.locfileid: "112067906"
---
# <a name="enumerating-devices-wmdm"></a><span data-ttu-id="812da-110">Énumération des appareils (WMDM)</span><span class="sxs-lookup"><span data-stu-id="812da-110">Enumerating devices (WMDM)</span></span>

<span data-ttu-id="812da-111">Windows Media Gestionnaire de périphériques conserve un cache de périphériques connectés qui est mis à jour lorsqu’une application Windows Media Gestionnaire de périphériques démarre, lorsqu’un appareil Plug-and-Play (PnP) se connecte ou se déconnecte, ou lorsque l’application appelle [**IWMDeviceManager2 :: Reinitialize**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdevicemanager2-reinitialize).</span><span class="sxs-lookup"><span data-stu-id="812da-111">Windows Media Device Manager maintains a cache of connected devices that is updated when a Windows Media Device Manager application starts, when a Plug and Play (PnP) device connects or disconnects, or when the application calls [**IWMDeviceManager2::Reinitialize**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdevicemanager2-reinitialize).</span></span> <span data-ttu-id="812da-112">Ce cache est exposé à l’application lorsqu’il appelle [**IWMDeviceManager :: EnumDevices**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdevicemanager-enumdevices) ou [**IWMDeviceManager2 :: EnumDevices2**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdevicemanager2-enumdevices2).</span><span class="sxs-lookup"><span data-stu-id="812da-112">This cache is exposed to the application when it calls [**IWMDeviceManager::EnumDevices**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdevicemanager-enumdevices) or [**IWMDeviceManager2::EnumDevices2**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdevicemanager2-enumdevices2).</span></span> <span data-ttu-id="812da-113">Chaque appareil est exposé à l’application en tant qu’interface [**IWMDMDevice**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmdevice) .</span><span class="sxs-lookup"><span data-stu-id="812da-113">Each device is exposed to the application as an [**IWMDMDevice**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmdevice) interface.</span></span> <span data-ttu-id="812da-114">Si le fournisseur de services est inscrit pour gérer les périphériques PnP, les Gestionnaire de périphériques Windows Media prennent connaissance de la liste actuelle des appareils connectés.</span><span class="sxs-lookup"><span data-stu-id="812da-114">If the service provider is registered to handle PnP devices, Windows Media Device Manager will be aware of the current list of connected devices.</span></span> <span data-ttu-id="812da-115">Si le fournisseur de services est inscrit pour gérer les périphériques non Plug-and-Play, le fournisseur de services est responsable de la détection des appareils attachés.</span><span class="sxs-lookup"><span data-stu-id="812da-115">If the service provider is registered to handle non-PnP devices, the service provider is responsible for discovering attached devices.</span></span> <span data-ttu-id="812da-116">Un fournisseur de services ne peut être inscrit que pour des appareils PnP ou non Plug-and-Play, jamais les deux à la fois.</span><span class="sxs-lookup"><span data-stu-id="812da-116">A service provider can only be registered for PnP or non-PnP devices, never both.</span></span>

<span data-ttu-id="812da-117">Les actions suivantes montrent comment Windows Media Gestionnaire de périphériques gère ou met à jour son cache.</span><span class="sxs-lookup"><span data-stu-id="812da-117">The following actions show how Windows Media Device Manager maintains or updates its cache.</span></span> <span data-ttu-id="812da-118">Notez que le cache n’est jamais mis à jour lorsqu’un appareil non Plug-and-Play se connecte ou se déconnecte.</span><span class="sxs-lookup"><span data-stu-id="812da-118">Notice that the cache is never updated when a non-PnP device connects or disconnects.</span></span>

<span data-ttu-id="812da-119">Une application Gestionnaire de périphériques Windows Media démarre</span><span class="sxs-lookup"><span data-stu-id="812da-119">A Windows Media Device Manager application starts</span></span>

-   <span data-ttu-id="812da-120">Windows Media Gestionnaire de périphériques récupère une liste des périphériques PnP attachés à partir du sous-système PnP et appelle [**IMDServiceProvider2 :: CreateDevice**](/windows/desktop/api/mswmdm/nf-mswmdm-imdserviceprovider2-createdevice) sur le SP inscrit pour chaque périphérique connecté.</span><span class="sxs-lookup"><span data-stu-id="812da-120">Windows Media Device Manager retrieves a list of attached PnP devices from the PnP subsystem, and calls [**IMDServiceProvider2::CreateDevice**](/windows/desktop/api/mswmdm/nf-mswmdm-imdserviceprovider2-createdevice) on the SP registered for each connected device.</span></span> <span data-ttu-id="812da-121">(Il découvre le fournisseur de services approprié en interrogeant le paramètre d’appareil WMDMSPCLSID pour l’ID de classe du fournisseur de services responsable de cet appareil.</span><span class="sxs-lookup"><span data-stu-id="812da-121">(It discovers the correct service provider by querying the WMDMSPCLSID device parameter for the class ID of the service provider responsible for this device.</span></span> <span data-ttu-id="812da-122">Pour plus d’informations, consultez Paramètres de l' [appareil](device-parameters.md) .) Tous les appareils renvoyés sont ajoutés au cache Windows Media Gestionnaire de périphériques des appareils.</span><span class="sxs-lookup"><span data-stu-id="812da-122">See [Device Parameters](device-parameters.md) for more information.) All devices returned are added to the Windows Media Device Manager cache of devices.</span></span>
-   <span data-ttu-id="812da-123">Windows Media Gestionnaire de périphériques trouve tous les fournisseurs de services non Plug-and-PnP inscrits auprès de celui-ci et appelle [**IMDServiceProvider :: EnumDevices**](/windows/desktop/api/mswmdm/nf-mswmdm-imdserviceprovider-enumdevices) sur chaque fournisseur de services pour obtenir une liste d’appareils de chacun d’eux.</span><span class="sxs-lookup"><span data-stu-id="812da-123">Windows Media Device Manager finds all non-PnP service providers registered with it and calls [**IMDServiceProvider::EnumDevices**](/windows/desktop/api/mswmdm/nf-mswmdm-imdserviceprovider-enumdevices) on each service provider to get a list devices from each one.</span></span> <span data-ttu-id="812da-124">Tous les appareils retournés sont ajoutés au cache.</span><span class="sxs-lookup"><span data-stu-id="812da-124">All devices returned are added to the cache.</span></span>

<span data-ttu-id="812da-125">L’application appelle IWMDeviceManager/2 :: EnumDevices/2</span><span class="sxs-lookup"><span data-stu-id="812da-125">The application calls IWMDeviceManager/2::EnumDevices/2</span></span>

-   <span data-ttu-id="812da-126">Windows Media Gestionnaire de périphériques retourne sa liste de périphériques mis en cache.</span><span class="sxs-lookup"><span data-stu-id="812da-126">Windows Media Device Manager returns its cached device list.</span></span>

<span data-ttu-id="812da-127">Connexion d’un appareil PnP</span><span class="sxs-lookup"><span data-stu-id="812da-127">A PnP device connects</span></span>

-   <span data-ttu-id="812da-128">Windows Media Gestionnaire de périphériques recherche le fournisseur de services approprié et appelle **IMDServiceProvider2 :: CreateDevice**, puis ajoute l’appareil à son cache.</span><span class="sxs-lookup"><span data-stu-id="812da-128">Windows Media Device Manager finds the relevant service provider and calls **IMDServiceProvider2::CreateDevice**, and adds the device to its cache.</span></span>
-   <span data-ttu-id="812da-129">Si l’application implémente [**IWMDMNotification**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmnotification), Windows Media gestionnaire de périphériques appelle [**IWMDMNotification :: WMDMMessage**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmnotification-wmdmmessage) avec une notification d’arrivée.</span><span class="sxs-lookup"><span data-stu-id="812da-129">If the application implements [**IWMDMNotification**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmnotification), Windows Media Device Manager calls [**IWMDMNotification::WMDMMessage**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmnotification-wmdmmessage) with an arrival notification.</span></span>

<span data-ttu-id="812da-130">Déconnexion d’un appareil PnP</span><span class="sxs-lookup"><span data-stu-id="812da-130">A PnP device disconnects</span></span>

-   <span data-ttu-id="812da-131">Windows Media Gestionnaire de périphériques supprime l’élément de son cache.</span><span class="sxs-lookup"><span data-stu-id="812da-131">Windows Media Device Manager removes the item from its cache.</span></span>
-   <span data-ttu-id="812da-132">Si l’application implémente IWMDMNotification, Windows Media Gestionnaire de périphériques appelle IWMDMNotification :: WMDMMessage avec une notification de départ.</span><span class="sxs-lookup"><span data-stu-id="812da-132">If the application implements IWMDMNotification, Windows Media Device Manager calls IWMDMNotification::WMDMMessage with a departure notification.</span></span>

<span data-ttu-id="812da-133">L’application appelle IWMDeviceManager2 :: Reinitialize</span><span class="sxs-lookup"><span data-stu-id="812da-133">The application calls IWMDeviceManager2::Reinitialize</span></span>

-   <span data-ttu-id="812da-134">Actualise le cache avec tous les appareils connectés.</span><span class="sxs-lookup"><span data-stu-id="812da-134">Refreshes the cache with all connected devices.</span></span>

<span data-ttu-id="812da-135">Un appareil non PnP se connecte ou se déconnecte</span><span class="sxs-lookup"><span data-stu-id="812da-135">A non-PnP device connects or disconnects</span></span>

-   <span data-ttu-id="812da-136">Windows Media Gestionnaire de périphériques n’est pas informé de l’arrivée ou du départ et n’entreprend aucune action.</span><span class="sxs-lookup"><span data-stu-id="812da-136">Windows Media Device Manager is not informed of the arrival or departure, and takes no action.</span></span>

## <a name="related-topics"></a><span data-ttu-id="812da-137">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="812da-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="812da-138">**Création d’un fournisseur de services**</span><span class="sxs-lookup"><span data-stu-id="812da-138">**Creating a Service Provider**</span></span>](creating-a-service-provider.md)
</dt> </dl>

 

 




