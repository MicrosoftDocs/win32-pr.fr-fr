---
title: Référence WMDM
description: Le kit de développement logiciel (SDK) Windows Media Gestionnaire de périphériques se compose d’une collection d’interfaces, de structures, d’énumérations et de constantes. Utilisez ces Articles de référence.
ms.assetid: 1d2260a8-bc9f-41b3-a3b0-0176b45fff1f
keywords:
- Windows Media Gestionnaire de périphériques, informations de référence sur la programmation
- Gestionnaire de périphériques, référence de programmation
- Windows Media Gestionnaire de périphériques, applications de bureau
- Gestionnaire de périphériques, applications de bureau
- Gestionnaire de périphériques Windows Media, fournisseurs de services
- Gestionnaire de périphériques, fournisseurs de services
- applications de bureau, informations de référence sur la programmation
- fournisseurs de services, informations de référence sur la programmation
- Référence de programmation, applications de bureau
- Référence de programmation, fournisseurs de services
- informations de référence sur la programmation, Windows Media Gestionnaire de périphériques
- référence pour Windows Media Gestionnaire de périphériques, à propos de
- informations de référence sur les Gestionnaire de périphériques Windows Media, applications de bureau
- référence pour Windows Media Gestionnaire de périphériques, fournisseurs de services
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e624bbc445d5d5e376cad926248ae4ee4db17a6e
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112406522"
---
# <a name="wmdm-reference"></a><span data-ttu-id="00f90-118">Référence WMDM</span><span class="sxs-lookup"><span data-stu-id="00f90-118">WMDM reference</span></span>

<span data-ttu-id="00f90-119">Le kit de développement logiciel (SDK) Windows Media Gestionnaire de périphériques se compose d’une collection d’interfaces, de structures, d’énumérations et de constantes.</span><span class="sxs-lookup"><span data-stu-id="00f90-119">The Windows Media Device Manager SDK consists of a collection of interfaces, structures, enumerations, and constants.</span></span> <span data-ttu-id="00f90-120">La section de référence divise les interfaces en groupes en fonction du type d’objet qui les utilise.</span><span class="sxs-lookup"><span data-stu-id="00f90-120">The reference section divides the interfaces into groups according to the type of object that uses them.</span></span>



| <span data-ttu-id="00f90-121">Section</span><span class="sxs-lookup"><span data-stu-id="00f90-121">Section</span></span>                                                                                                    | <span data-ttu-id="00f90-122">Description</span><span class="sxs-lookup"><span data-stu-id="00f90-122">Description</span></span>                                                                                                                                                                                         |
|------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="00f90-123">Interfaces pour les applications</span><span class="sxs-lookup"><span data-stu-id="00f90-123">Interfaces for Applications</span></span>](interfaces-for-applications.md)                                             | <span data-ttu-id="00f90-124">Décrit les interfaces utilisées ou implémentées uniquement par les applications de bureau, les plug-ins du lecteur Windows Media ou les objets COM qui ont besoin d’un accès de haut niveau à un appareil mobile.</span><span class="sxs-lookup"><span data-stu-id="00f90-124">Describes interfaces that are used or implemented only by desktop applications, Windows Media Player plug-ins, or COM objects that need high-level access to a portable device.</span></span>                     |
| [<span data-ttu-id="00f90-125">Interfaces pour les fournisseurs de services</span><span class="sxs-lookup"><span data-stu-id="00f90-125">Interfaces for Service Providers</span></span>](interfaces-for-service-providers.md)                                   | <span data-ttu-id="00f90-126">Décrit les interfaces utilisées ou implémentées uniquement par les fournisseurs de services, qui gèrent la communication de bas niveau réelle avec un appareil mobile.</span><span class="sxs-lookup"><span data-stu-id="00f90-126">Describes interfaces that are used or implemented only by service providers, which handle the actual low-level communication with a portable device.</span></span>                                                |
| [<span data-ttu-id="00f90-127">Interfaces Windows Media DRM-Implemented</span><span class="sxs-lookup"><span data-stu-id="00f90-127">Windows Media DRM-Implemented Interfaces</span></span>](windows-media-drm-implemented-interfaces.md)                   | <span data-ttu-id="00f90-128">Décrit les interfaces qui ne sont pas destinées à être implémentées par des fournisseurs de services tiers, mais qui sont implémentées et appelées en interne par le Windows Media DRM et Windows Media Gestionnaire de périphériques.</span><span class="sxs-lookup"><span data-stu-id="00f90-128">Describes interfaces that are not intended to be implemented by third-party service providers, but are implemented and called internally by the Windows Media DRM and Windows Media Device Manager.</span></span> |
| [<span data-ttu-id="00f90-129">Interfaces pour les fournisseurs de services et les applications</span><span class="sxs-lookup"><span data-stu-id="00f90-129">Interfaces for Service Providers and Applications</span></span>](interfaces-for-service-providers-and-applications.md) | <span data-ttu-id="00f90-130">Décrit les interfaces qui peuvent être utilisées par des applications ou par des fournisseurs de services.</span><span class="sxs-lookup"><span data-stu-id="00f90-130">Describes interfaces that can be used either by applications or by service providers.</span></span>                                                                                                               |
| [<span data-ttu-id="00f90-131">Interfaces pour les fournisseurs de contenu sécurisés</span><span class="sxs-lookup"><span data-stu-id="00f90-131">Interfaces for Secure Content Providers</span></span>](interfaces-for-secure-content-providers.md)                     | <span data-ttu-id="00f90-132">Décrit les interfaces qui doivent être implémentées par un périphérique ou une application qui utilisera un contenu DRM protégé.</span><span class="sxs-lookup"><span data-stu-id="00f90-132">Describes interfaces that must be implemented by a device or application that will use DRM-protected content.</span></span>                                                                                       |
| [<span data-ttu-id="00f90-133">Structures</span><span class="sxs-lookup"><span data-stu-id="00f90-133">Structures</span></span>](structures.md)                                                                               | <span data-ttu-id="00f90-134">Décrit les structures utilisées pour les méthodes de Gestionnaire de périphériques Windows Media.</span><span class="sxs-lookup"><span data-stu-id="00f90-134">Describes structures used for Windows Media Device Manager methods.</span></span>                                                                                                                                 |
| [<span data-ttu-id="00f90-135">Types énumération</span><span class="sxs-lookup"><span data-stu-id="00f90-135">Enumeration Types</span></span>](enumeration-types.md)                                                                 | <span data-ttu-id="00f90-136">Décrit les énumérations utilisées pour les méthodes Windows Media Gestionnaire de périphériques.</span><span class="sxs-lookup"><span data-stu-id="00f90-136">Describes enumerations used for Windows Media Device Manager methods.</span></span>                                                                                                                               |
| [<span data-ttu-id="00f90-137">Constantes de métadonnées</span><span class="sxs-lookup"><span data-stu-id="00f90-137">Metadata Constants</span></span>](metadata-constants.md)                                                               | <span data-ttu-id="00f90-138">Décrit les constantes définies par le kit de développement logiciel (SDK) Windows Media Gestionnaire de périphériques pour la définition ou la récupération de diverses propriétés de métadonnées pour un appareil ou un objet sur l’appareil.</span><span class="sxs-lookup"><span data-stu-id="00f90-138">Describes the constants defined by the Windows Media Device Manager SDK for setting or retrieving various metadata properties for a device or object on the device.</span></span>                                 |
| [<span data-ttu-id="00f90-139">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="00f90-139">Error Codes</span></span>](error-codes.md)                                                                             | <span data-ttu-id="00f90-140">Décrit les codes d’erreur qui peuvent être retournés par les méthodes du kit de développement logiciel (SDK) Windows Media Gestionnaire de périphériques.</span><span class="sxs-lookup"><span data-stu-id="00f90-140">Describes the error codes that can be returned by Windows Media Device Manager SDK methods.</span></span>                                                                                                         |



 

 

 




