---
title: Activation de PnP pour les appareils
description: Activation de PnP pour les appareils
ms.assetid: 510237a9-2b74-4c2e-ad45-3f45117289a6
keywords:
- Gestionnaire de périphériques Windows Media, appareils PnP
- Gestionnaire de périphériques, appareils PnP
- Guide de programmation, appareils PnP
- fournisseurs de services, appareils PnP
- création de fournisseurs de services, de périphériques PnP
- Périphériques PnP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d44c7ccdfd29453c1ab28e970c1b054d1278e620
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103839774"
---
# <a name="enabling-pnp-for-devices"></a><span data-ttu-id="1d9dc-109">Activation de PnP pour les appareils</span><span class="sxs-lookup"><span data-stu-id="1d9dc-109">Enabling PnP for Devices</span></span>

<span data-ttu-id="1d9dc-110">Windows Media Gestionnaire de périphériques surveille les notifications d’arrivée et de suppression des appareils qui publient une interface de périphérique de lecteur audio portable.</span><span class="sxs-lookup"><span data-stu-id="1d9dc-110">Windows Media Device Manager monitors arrival and removal notifications of devices that advertise a Portable Audio Player device interface.</span></span> <span data-ttu-id="1d9dc-111">À l’arrivée d’un tel appareil, Windows Media Gestionnaire de périphériques interroge un paramètre d’appareil nommé *WMDMSPCLSID* pour obtenir l’ID de classe du fournisseur de services responsable de cet appareil.</span><span class="sxs-lookup"><span data-stu-id="1d9dc-111">On the arrival of such a device, Windows Media Device Manager queries a device parameter named *WMDMSPCLSID* for the class ID of the service provider responsible for this device.</span></span> <span data-ttu-id="1d9dc-112">Windows Media Gestionnaire de périphériques appelle [**IMDServiceProvider2 :: CreateDevice**](/windows/desktop/api/mswmdm/nf-mswmdm-imdserviceprovider2-createdevice) sur ce fournisseur de services pour créer un objet appareil, qui est exposé à l’application sous la forme d’un objet [**IWMDMDevice**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmdevice) .</span><span class="sxs-lookup"><span data-stu-id="1d9dc-112">Windows Media Device Manager calls [**IMDServiceProvider2::CreateDevice**](/windows/desktop/api/mswmdm/nf-mswmdm-imdserviceprovider2-createdevice) on this service provider to create a device object, which is exposed to the application as an [**IWMDMDevice**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmdevice) object.</span></span>

<span data-ttu-id="1d9dc-113">Un fournisseur de services peut soit gérer des appareils PnP, soit des appareils non Plug-and-Play ; il ne peut pas gérer les deux types.</span><span class="sxs-lookup"><span data-stu-id="1d9dc-113">A service provider can either handle PnP devices, or non-PnP devices; it cannot handle both types.</span></span>

<span data-ttu-id="1d9dc-114">Pour qu’un appareil fonctionne avec le mécanisme précédent (et qui, par conséquent, active les notifications d’arrivée et de suppression pour l’appareil sous les applications Windows Media Gestionnaire de périphériques), les conditions suivantes doivent être remplies :</span><span class="sxs-lookup"><span data-stu-id="1d9dc-114">For a device to work with the preceding mechanism (and thus enable arrival and removal notifications for the device under Windows Media Device Manager applications), the following requirements must be met:</span></span>

-   <span data-ttu-id="1d9dc-115">Le pilote de périphérique de cet appareil doit publier l’interface du périphérique lecteur audio portable Windows Media Gestionnaire de périphériques.</span><span class="sxs-lookup"><span data-stu-id="1d9dc-115">The device driver of this device must advertise the Windows Media Device Manager Portable Audio Player device interface.</span></span> <span data-ttu-id="1d9dc-116">Le GUID de cette interface d’appareil est défini comme suit :</span><span class="sxs-lookup"><span data-stu-id="1d9dc-116">The GUID for this device interface is defined as:</span></span>

    ```
    {0xf33fdc04, 0xd1ac, 0x4e8e, {0x9a, 0x30, 0x19, 0xbb, 0xd4, 0xb1, 0x8, 0xae} }
    ```

    

    > [!Note]  
    > <span data-ttu-id="1d9dc-117">Un appareil ne doit pas publier cette interface si l’appareil publie l’interface de volume (définie en tant que VolumeClassGuid ou \_ volume DEVINTERFACE GUID \_ dans winioctl. h).</span><span class="sxs-lookup"><span data-stu-id="1d9dc-117">A device should not advertise this interface if the device advertises the Volume interface (defined as VolumeClassGuid or GUID\_DEVINTERFACE\_VOLUME in winioctl.h).</span></span> <span data-ttu-id="1d9dc-118">Si l’appareil publie l’interface du volume, il est déjà compatible avec PnP sous Windows Media Gestionnaire de périphériques.</span><span class="sxs-lookup"><span data-stu-id="1d9dc-118">If the device advertises the Volume Interface, it is already PnP-enabled under Windows Media Device Manager.</span></span>

     

    <span data-ttu-id="1d9dc-119">-ET/OU-</span><span class="sxs-lookup"><span data-stu-id="1d9dc-119">-AND/OR-</span></span>

    <span data-ttu-id="1d9dc-120">Une nouvelle sous-clé de Registre pour le fournisseur de services doit être créée à l’intérieur de la sous-clé HKEY \_ local \_ machine \\ Software \\ Microsoft \\ Windows Media gestionnaire de périphériques \\ KnownDevices.</span><span class="sxs-lookup"><span data-stu-id="1d9dc-120">A new registry subkey for the service provider must be created inside the subkey HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\Windows Media Device Manager\\KnownDevices.</span></span> <span data-ttu-id="1d9dc-121">Cette clé doit avoir le nom de votre fournisseur de services et doit avoir les deux entrées de valeur de Registre \_ SZ suivantes :</span><span class="sxs-lookup"><span data-stu-id="1d9dc-121">This key should have the name of your service provider and must have the following two Reg\_SZ value entries:</span></span>

    ```
    DeviceInterface         {25DBCE51-6C8F-4A72-8A6D-B54C2B4FC835}
    WMDMSPCLSID             {067B4B81-B1EC-489F-B111-940EBDC44EBE}
    ```

    

-   <span data-ttu-id="1d9dc-122">L’appareil doit avoir un paramètre d’appareil nommé WMDMSPCLSID.</span><span class="sxs-lookup"><span data-stu-id="1d9dc-122">The device must have a device parameter named WMDMSPCLSID.</span></span> <span data-ttu-id="1d9dc-123">La valeur de ce paramètre doit être définie comme CLSID du fournisseur de services sous la forme d’une chaîne.</span><span class="sxs-lookup"><span data-stu-id="1d9dc-123">The value of this parameter should be set as the CLSID of the service provider in a string form.</span></span> <span data-ttu-id="1d9dc-124">Pour plus d’informations sur les paramètres d’appareil, consultez Paramètres de l' [appareil](device-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="1d9dc-124">For more information about device parameters, see [Device Parameters](device-parameters.md).</span></span>

    > [!Note]  
    > <span data-ttu-id="1d9dc-125">La valeur du paramètre doit être le CLSID, et non le ProgID du fournisseur de services.</span><span class="sxs-lookup"><span data-stu-id="1d9dc-125">The parameter value must be the CLSID, not the ProgID of the service provider.</span></span>

     

-   <span data-ttu-id="1d9dc-126">Le fournisseur de services de cet appareil doit implémenter l’interface IMDServiceProvider2.</span><span class="sxs-lookup"><span data-stu-id="1d9dc-126">The service provider for this device must implement the IMDServiceProvider2 interface.</span></span>
-   <span data-ttu-id="1d9dc-127">La clé du fournisseur de services sous HKEY \_ local \_ machine \\ Software \\ Microsoft \\ Windows Media gestionnaire de périphériques \\ plugins \\ SP \\ baname doit contenir la valeur DWORD suivante</span><span class="sxs-lookup"><span data-stu-id="1d9dc-127">The service provider key under HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\Windows Media Device Manager\\Plugins\\SP\\SPName must contain the following DWORD value</span></span>
    ```
    PnPAware    1
    ```

    

## <a name="related-topics"></a><span data-ttu-id="1d9dc-128">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="1d9dc-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1d9dc-129">**Création d’un fournisseur de services**</span><span class="sxs-lookup"><span data-stu-id="1d9dc-129">**Creating a Service Provider**</span></span>](creating-a-service-provider.md)
</dt> </dl>

 

 




