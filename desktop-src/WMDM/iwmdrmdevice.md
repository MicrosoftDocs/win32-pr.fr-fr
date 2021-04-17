---
title: Interface IWMDRMDevice
description: Cette interface n’est pas destinée à être implémentée par un fournisseur de services, mais elle est fournie à des fins de documentation complète. L’interface IWMDRMDevice permet à un fournisseur de contenu sécurisé de communiquer avec des appareils qui utilisent Windows Media DRM 10 pour les appareils mobiles.
ms.assetid: ebad4acd-16cc-433f-a5e0-fcae59030f55
keywords:
- Interface IWMDRMDevice Windows Media Gestionnaire de périphériques
- Interface IWMDRMDevice Windows Media Gestionnaire de périphériques, Description
topic_type:
- apiref
api_name:
- IWMDRMDevice
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ca240f01f552dfdedb0145e49f61f2ead1f18832
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104315474"
---
# <a name="iwmdrmdevice-interface"></a><span data-ttu-id="7c6b6-105">Interface IWMDRMDevice</span><span class="sxs-lookup"><span data-stu-id="7c6b6-105">IWMDRMDevice interface</span></span>

<span data-ttu-id="7c6b6-106">Cette interface n’est pas destinée à être implémentée par un fournisseur de services, mais elle est fournie à des fins de documentation complète.</span><span class="sxs-lookup"><span data-stu-id="7c6b6-106">This interface is not intended to be implemented by a service provider, but is provided for purposes of complete documentation.</span></span>

<span data-ttu-id="7c6b6-107">L’interface **IWMDRMDevice** permet à un fournisseur de contenu sécurisé de communiquer avec des appareils qui utilisent Windows Media DRM 10 pour les appareils mobiles.</span><span class="sxs-lookup"><span data-stu-id="7c6b6-107">The **IWMDRMDevice** interface enables a secure content provider to communicate with devices that use Windows Media DRM 10 for Portable Devices.</span></span>

## <a name="members"></a><span data-ttu-id="7c6b6-108">Membres</span><span class="sxs-lookup"><span data-stu-id="7c6b6-108">Members</span></span>

<span data-ttu-id="7c6b6-109">L’interface **IWMDRMDevice** hérite de l’interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="7c6b6-109">The **IWMDRMDevice** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="7c6b6-110">**IWMDRMDevice** a également les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="7c6b6-110">**IWMDRMDevice** also has these types of members:</span></span>

-   [<span data-ttu-id="7c6b6-111">Méthodes</span><span class="sxs-lookup"><span data-stu-id="7c6b6-111">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="7c6b6-112">Méthodes</span><span class="sxs-lookup"><span data-stu-id="7c6b6-112">Methods</span></span>

<span data-ttu-id="7c6b6-113">L’interface **IWMDRMDevice** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="7c6b6-113">The **IWMDRMDevice** interface has these methods.</span></span>



| <span data-ttu-id="7c6b6-114">Méthode</span><span class="sxs-lookup"><span data-stu-id="7c6b6-114">Method</span></span>                                                                  | <span data-ttu-id="7c6b6-115">Description</span><span class="sxs-lookup"><span data-stu-id="7c6b6-115">Description</span></span>                                                                                  |
|:------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------|
| [<span data-ttu-id="7c6b6-116">**CleanDataStore**</span><span class="sxs-lookup"><span data-stu-id="7c6b6-116">**CleanDataStore**</span></span>](iwmdrmdevice-cleandatastore.md)                   | <span data-ttu-id="7c6b6-117">Démarre le processus de nettoyage de la Banque de données DRM sur l’appareil.</span><span class="sxs-lookup"><span data-stu-id="7c6b6-117">Starts the process of cleaning the DRM data store on the device.</span></span><br/>                  |
| [<span data-ttu-id="7c6b6-118">**GetDeviceCertificate**</span><span class="sxs-lookup"><span data-stu-id="7c6b6-118">**GetDeviceCertificate**</span></span>](iwmdrmdevice-getdevicecertificate.md)       | <span data-ttu-id="7c6b6-119">Récupère le certificat de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="7c6b6-119">Retrieves the device certificate.</span></span><br/>                                                 |
| [<span data-ttu-id="7c6b6-120">**GetMeterChallenge**</span><span class="sxs-lookup"><span data-stu-id="7c6b6-120">**GetMeterChallenge**</span></span>](iwmdrmdevice-getmeterchallenge.md)             | <span data-ttu-id="7c6b6-121">Récupère le test de contrôle.</span><span class="sxs-lookup"><span data-stu-id="7c6b6-121">Retrieves the metering challenge.</span></span><br/>                                                 |
| [<span data-ttu-id="7c6b6-122">**GetSecureClock**</span><span class="sxs-lookup"><span data-stu-id="7c6b6-122">**GetSecureClock**</span></span>](iwmdrmdevice-getsecureclock.md)                   | <span data-ttu-id="7c6b6-123">Récupère l’horloge sécurisée.</span><span class="sxs-lookup"><span data-stu-id="7c6b6-123">Retrieves the secure clock.</span></span><br/>                                                       |
| [<span data-ttu-id="7c6b6-124">**GetSecureClockChallenge**</span><span class="sxs-lookup"><span data-stu-id="7c6b6-124">**GetSecureClockChallenge**</span></span>](iwmdrmdevice-getsecureclockchallenge.md) | <span data-ttu-id="7c6b6-125">Récupère le challenge d’horloge sécurisé.</span><span class="sxs-lookup"><span data-stu-id="7c6b6-125">Retrieves the secure clock challenge.</span></span><br/>                                             |
| [<span data-ttu-id="7c6b6-126">**GetSyncList**</span><span class="sxs-lookup"><span data-stu-id="7c6b6-126">**GetSyncList**</span></span>](iwmdrmdevice-getsynclist.md)                         | <span data-ttu-id="7c6b6-127">Récupère la liste de synchronisation de licence.</span><span class="sxs-lookup"><span data-stu-id="7c6b6-127">Retrieves the license synchronization list.</span></span><br/>                                       |
| [<span data-ttu-id="7c6b6-128">**IsWMDRMDevice**</span><span class="sxs-lookup"><span data-stu-id="7c6b6-128">**IsWMDRMDevice**</span></span>](iwmdrmdevice-iswmdrmdevice.md)                     | <span data-ttu-id="7c6b6-129">Détermine si l’appareil prend en charge Windows Media DRM 10 pour les appareils mobiles.</span><span class="sxs-lookup"><span data-stu-id="7c6b6-129">Determines whether the device supports Windows Media DRM 10 for Portable Devices.</span></span><br/> |
| [<span data-ttu-id="7c6b6-130">**SetLicenseResponse**</span><span class="sxs-lookup"><span data-stu-id="7c6b6-130">**SetLicenseResponse**</span></span>](iwmdrmdevice-setlicenseresponse.md)           | <span data-ttu-id="7c6b6-131">Définit la réponse de la licence.</span><span class="sxs-lookup"><span data-stu-id="7c6b6-131">Sets the license response.</span></span><br/>                                                        |
| [<span data-ttu-id="7c6b6-132">**SetMeterResponse**</span><span class="sxs-lookup"><span data-stu-id="7c6b6-132">**SetMeterResponse**</span></span>](iwmdrmdevice-setmeterresponse.md)               | <span data-ttu-id="7c6b6-133">Définit la réponse de contrôle.</span><span class="sxs-lookup"><span data-stu-id="7c6b6-133">Sets the metering response.</span></span><br/>                                                       |
| [<span data-ttu-id="7c6b6-134">**SetSecureClockResponse**</span><span class="sxs-lookup"><span data-stu-id="7c6b6-134">**SetSecureClockResponse**</span></span>](iwmdrmdevice-setsecureclockresponse.md)   | <span data-ttu-id="7c6b6-135">Définit la réponse de l’horloge sécurisée.</span><span class="sxs-lookup"><span data-stu-id="7c6b6-135">Sets the secure clock response.</span></span><br/>                                                   |



 

## <a name="see-also"></a><span data-ttu-id="7c6b6-136">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7c6b6-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7c6b6-137">**Interfaces pour les fournisseurs de services**</span><span class="sxs-lookup"><span data-stu-id="7c6b6-137">**Interfaces for Service Providers**</span></span>](interfaces-for-service-providers.md)
</dt> </dl>

 

