---
title: Fonctions d’inscription MDM
description: Les fonctions suivantes sont utilisées par l’inscription MDM.
ms.assetid: 1b063a56-f59f-4b02-949f-c8b6bbf45a13
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 821e08d9c6631bbb300a86ab6b9c480a3af0c25b
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/08/2020
ms.locfileid: "104316608"
---
# <a name="mdm-registration-functions"></a><span data-ttu-id="5f7e2-103">Fonctions d’inscription MDM</span><span class="sxs-lookup"><span data-stu-id="5f7e2-103">MDM Registration Functions</span></span>

<span data-ttu-id="5f7e2-104">Les fonctions suivantes sont utilisées par l’inscription MDM.</span><span class="sxs-lookup"><span data-stu-id="5f7e2-104">The following functions are used by MDM Registration.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="5f7e2-105">Dans cette section</span><span class="sxs-lookup"><span data-stu-id="5f7e2-105">In this section</span></span>

<dl> <dt>

[<span data-ttu-id="5f7e2-106">**DiscoverManagementService**</span><span class="sxs-lookup"><span data-stu-id="5f7e2-106">**DiscoverManagementService**</span></span>](/windows/desktop/api/MDMRegistration/nf-mdmregistration-discovermanagementservice)
</dt> <dd>

<span data-ttu-id="5f7e2-107">Découvre le service MDM.</span><span class="sxs-lookup"><span data-stu-id="5f7e2-107">Discovers the MDM service.</span></span>

</dd> <dt>

[<span data-ttu-id="5f7e2-108">**DiscoverManagementServiceEx**</span><span class="sxs-lookup"><span data-stu-id="5f7e2-108">**DiscoverManagementServiceEx**</span></span>](/windows/desktop/api/MDMRegistration/nf-mdmregistration-discovermanagementserviceex)
</dt> <dd>

<span data-ttu-id="5f7e2-109">Découvre le service MDM à l’aide d’un serveur candidat.</span><span class="sxs-lookup"><span data-stu-id="5f7e2-109">Discovers the MDM service using a candidate server.</span></span>

</dd> <dt>

[<span data-ttu-id="5f7e2-110">**GetDeviceRegistrationInfo**</span><span class="sxs-lookup"><span data-stu-id="5f7e2-110">**GetDeviceRegistrationInfo**</span></span>](/windows/desktop/api/MDMRegistration/nf-mdmregistration-getdeviceregistrationinfo)
</dt> <dd>

<span data-ttu-id="5f7e2-111">Récupère les informations d’inscription de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="5f7e2-111">Retrieves the device registration information.</span></span>

</dd> <dt>

[<span data-ttu-id="5f7e2-112">**GetManagementAppHyperlink**</span><span class="sxs-lookup"><span data-stu-id="5f7e2-112">**GetManagementAppHyperlink**</span></span>](/windows/desktop/api/MDMRegistration/nf-mdmregistration-getmanagementapphyperlink)
</dt> <dd>

<span data-ttu-id="5f7e2-113">Récupère le lien hypertexte de l’application de gestion associé au service MDM.</span><span class="sxs-lookup"><span data-stu-id="5f7e2-113">Retrieves the management app hyperlink associated with the MDM service.</span></span>

</dd> <dt>

[<span data-ttu-id="5f7e2-114">**IsDeviceRegisteredWithManagement**</span><span class="sxs-lookup"><span data-stu-id="5f7e2-114">**IsDeviceRegisteredWithManagement**</span></span>](/windows/desktop/api/MDMRegistration/nf-mdmregistration-isdeviceregisteredwithmanagement)
</dt> <dd>

<span data-ttu-id="5f7e2-115">Vérifie si l’appareil est inscrit auprès d’un service MDM.</span><span class="sxs-lookup"><span data-stu-id="5f7e2-115">Checks whether the device is registered with an MDM service.</span></span>

</dd> <dt>

[<span data-ttu-id="5f7e2-116">**IsManagementRegistrationAllowed**</span><span class="sxs-lookup"><span data-stu-id="5f7e2-116">**IsManagementRegistrationAllowed**</span></span>](/windows/desktop/api/MDMRegistration/nf-mdmregistration-ismanagementregistrationallowed)
</dt> <dd>

<span data-ttu-id="5f7e2-117">Vérifie si l’inscription MDM est autorisée par la stratégie locale.</span><span class="sxs-lookup"><span data-stu-id="5f7e2-117">Checks whether MDM registration is allowed by local policy.</span></span>

</dd> <dt>

[<span data-ttu-id="5f7e2-118">**RegisterDeviceWithManagement**</span><span class="sxs-lookup"><span data-stu-id="5f7e2-118">**RegisterDeviceWithManagement**</span></span>](/windows/desktop/api/MDMRegistration/nf-mdmregistration-registerdevicewithmanagement)
</dt> <dd>

<span data-ttu-id="5f7e2-119">Inscrit un appareil auprès d’un service de gestion des appareils mobiles à l’aide du [ \[ protocole d’inscription MS-MDE \] : Mobile Device](/openspecs/windows_protocols/ms-mde/5c841535-042e-489e-913c-9d783d741267).</span><span class="sxs-lookup"><span data-stu-id="5f7e2-119">Registers a device with a MDM service, using the [\[MS-MDE\]: Mobile Device Enrollment Protocol](/openspecs/windows_protocols/ms-mde/5c841535-042e-489e-913c-9d783d741267).</span></span>

</dd> <dt>

[<span data-ttu-id="5f7e2-120">**RegisterDeviceWithManagementUsingAADCredentials**</span><span class="sxs-lookup"><span data-stu-id="5f7e2-120">**RegisterDeviceWithManagementUsingAADCredentials**</span></span>](/windows/desktop/api/MDMRegistration/nf-mdmregistration-registerdevicewithmanagementusingaadcredentials)
</dt> <dd>

<span data-ttu-id="5f7e2-121">Inscrit un appareil auprès d’un service MDM, à l’aide des informations d’identification de Azure Active Directory (AAD).</span><span class="sxs-lookup"><span data-stu-id="5f7e2-121">Registers a device with a MDM service, using Azure Active Directory (AAD) credentials.</span></span>

</dd> <dt>

[<span data-ttu-id="5f7e2-122">**SetManagedExternally**</span><span class="sxs-lookup"><span data-stu-id="5f7e2-122">**SetManagedExternally**</span></span>](/windows/desktop/api/MDMRegistration/nf-mdmregistration-setmanagedexternally)
</dt> <dd>

<span data-ttu-id="5f7e2-123">Indique à l’agent MDM que l’appareil est géré en externe et qu’il ne doit pas être inscrit auprès d’un service MDM.</span><span class="sxs-lookup"><span data-stu-id="5f7e2-123">Indicates to the MDM agent that the device is managed externally and is not to be registered with an MDM service.</span></span>

</dd> <dt>

[<span data-ttu-id="5f7e2-124">**UnregisterDeviceWithManagement**</span><span class="sxs-lookup"><span data-stu-id="5f7e2-124">**UnregisterDeviceWithManagement**</span></span>](/windows/desktop/api/MDMRegistration/nf-mdmregistration-unregisterdevicewithmanagement)
</dt> <dd>

<span data-ttu-id="5f7e2-125">Annule l’inscription d’un appareil auprès du service MDM</span><span class="sxs-lookup"><span data-stu-id="5f7e2-125">Unregisters a device with the MDM service</span></span>

</dd> </dl>

 

 