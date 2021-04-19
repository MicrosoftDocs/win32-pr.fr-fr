---
title: Clés de Registre WCS
description: WCS utilise des clés de Registre pour signaler que certains événements de profil de couleurs se sont produits. Les applications doivent interroger ces clés de Registre pour mettre à jour l’état du profil de couleurs système.
ms.assetid: e728efa0-e547-45b9-af85-1312766d2fe7
keywords:
- Windows Color System (WCS), clés de Registre
- WCS (Windows Color System), clés de Registre
- gestion des couleurs des images, clés de Registre
- gestion des couleurs, clés de Registre
- couleurs, clés de Registre
- Référence WCS, clés de Registre
- référence pour WCS, clés de Registre
- Système de couleurs Windows (WCS), registre
- WCS (système de couleurs Windows), registre
- gestion des couleurs des images, registre
- gestion des couleurs, registre
- couleurs, registre
- Référence WCS, registre
- référence pour WCS, registre
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 95a1c0072d9a00fe0cff4a4dbe57af839f65731b
ms.sourcegitcommit: 3f366316c02c411c4c5e14620a699f6f30608634
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/04/2021
ms.locfileid: "106538418"
---
# <a name="wcs-registry-keys"></a><span data-ttu-id="6d686-118">Clés de Registre WCS</span><span class="sxs-lookup"><span data-stu-id="6d686-118">WCS Registry Keys</span></span>

<span data-ttu-id="6d686-119">WCS utilise des clés de Registre pour signaler que certains événements de profil de couleurs se sont produits.</span><span class="sxs-lookup"><span data-stu-id="6d686-119">WCS uses registry keys to signal that certain color profile events have occurred.</span></span> <span data-ttu-id="6d686-120">Les applications doivent interroger ces clés de Registre pour mettre à jour l’état du profil de couleurs système.</span><span class="sxs-lookup"><span data-stu-id="6d686-120">Apps should query these registry keys for updated system color profile state.</span></span>

## <a name="active-color-profile-changed"></a><span data-ttu-id="6d686-121">Profil de couleurs actif modifié</span><span class="sxs-lookup"><span data-stu-id="6d686-121">Active color profile changed</span></span>

<span data-ttu-id="6d686-122">Les applications peuvent souhaiter répondre aux événements de modification du profil de couleurs pour un appareil moniteur ; Cela garantit qu’ils disposent toujours d’informations de couleur précises pour leur cible, même si l’utilisateur ou une autre application a modifié le profil actif de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="6d686-122">Apps may want to respond to color profile change events for a monitor device; this ensures that they always have accurate color information for their target, even if the user or another app has changed the active profile for the device.</span></span>

### <a name="desktop-applications"></a><span data-ttu-id="6d686-123">Applications de bureau</span><span class="sxs-lookup"><span data-stu-id="6d686-123">Desktop applications</span></span>

<span data-ttu-id="6d686-124">Les applications de bureau doivent écouter les modifications apportées au registre pour déterminer quand des associations de profil de couleurs ont été modifiées à l’aide de [**RegNotifyChangeKeyValue**](/windows/win32/api/winreg/nf-winreg-regnotifychangekeyvalue).</span><span class="sxs-lookup"><span data-stu-id="6d686-124">Desktop apps should listen for changes to the registry to determine when a color profile associations has changed using [**RegNotifyChangeKeyValue**](/windows/win32/api/winreg/nf-winreg-regnotifychangekeyvalue).</span></span> <span data-ttu-id="6d686-125">Une application doit s’inscrire à la fois pour les modifications d’association de profil par utilisateur et pour les modifications à l’ensemble du système.</span><span class="sxs-lookup"><span data-stu-id="6d686-125">An app should register both for per-user profile association changes, and for system-wide changes.</span></span>

<span data-ttu-id="6d686-126">[**RegNotifyChangeKeyValue**](/windows/win32/api/winreg/nf-winreg-regnotifychangekeyvalue) doit être initialisé avec un HKEY fourni par [**RegOpenKeyEx**](/windows/win32/api/winreg/nf-winreg-regopenkeyexa).</span><span class="sxs-lookup"><span data-stu-id="6d686-126">[**RegNotifyChangeKeyValue**](/windows/win32/api/winreg/nf-winreg-regnotifychangekeyvalue) should be initialized with an HKEY provided by [**RegOpenKeyEx**](/windows/win32/api/winreg/nf-winreg-regopenkeyexa).</span></span> <span data-ttu-id="6d686-127">**RegOpenKeyEx** doit être initialisé à l’aide des emplacements de l’arborescence du registre suivants :</span><span class="sxs-lookup"><span data-stu-id="6d686-127">**RegOpenKeyEx** should be initialized using the following registry tree locations:</span></span>



|                                  |                                                                                                                                                    |
|----------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6d686-128">Associations de profils par utilisateur</span><span class="sxs-lookup"><span data-stu-id="6d686-128">Per-user profile associations</span></span>    | <span data-ttu-id="6d686-129">**HKEY \_ Current \_ User Software \\ Microsoft \\ Windows NT \\ CurrentVersion \\ ICM \\ ProfileAssociations \\ Display \\ {4d36e96e-E325-11CE-BFC1-08002BE10318}**</span><span class="sxs-lookup"><span data-stu-id="6d686-129">**HKEY\_CURRENT\_USER SOFTWARE\\Microsoft\\Windows NT\\CurrentVersion\\ICM\\ProfileAssociations\\Display\\{4d36e96e-e325-11ce-bfc1-08002be10318}**</span></span> |
| <span data-ttu-id="6d686-130">Associations de profils à l’ensemble du système</span><span class="sxs-lookup"><span data-stu-id="6d686-130">System-wide profile associations</span></span> | <span data-ttu-id="6d686-131">**HKEY \_ local \_ machine \\ System \\ CurrentControlSet \\ Control \\ Class \\ {4d36e96e-E325-11CE-BFC1-08002BE10318}**</span><span class="sxs-lookup"><span data-stu-id="6d686-131">**HKEY\_LOCAL\_MACHINE\\SYSTEM\\CurrentControlSet\\Control\\Class\\{4d36e96e-e325-11ce-bfc1-08002be10318}**</span></span>                                        |



 

<span data-ttu-id="6d686-132">Lorsque l’application est avertie d’une modification de clé de Registre, elle doit d’abord demander si des associations par utilisateur ou au niveau du système sont utilisées en appelant [**WcsGetUsePerUserProfiles**](/windows/win32/api/icm/nf-icm-wcsgetdefaultrenderingintent).</span><span class="sxs-lookup"><span data-stu-id="6d686-132">When the app is notified of a registry key change, it should first query whether per-user or system-wide associations are being used by calling [**WcsGetUsePerUserProfiles**](/windows/win32/api/icm/nf-icm-wcsgetdefaultrenderingintent).</span></span> <span data-ttu-id="6d686-133">Elle doit ensuite appeler [**WcsGetDefaultColorProfile**](/windows/win32/api/icm/nf-icm-wcsgetdefaultcolorprofile) avec la valeur de l' [**\_ étendue de \_ gestion \_ du profil WCS**](/windows/win32/api/icm/ne-icm-wcs_profile_management_scope) approprié pour obtenir le nouveau profil de couleurs actif pour l’analyse.</span><span class="sxs-lookup"><span data-stu-id="6d686-133">It should then call [**WcsGetDefaultColorProfile**](/windows/win32/api/icm/nf-icm-wcsgetdefaultcolorprofile) with the right [**WCS\_PROFILE\_MANAGEMENT\_SCOPE**](/windows/win32/api/icm/ne-icm-wcs_profile_management_scope) value to obtain the new active color profile for the monitor.</span></span> <span data-ttu-id="6d686-134">Notez que toutes les modifications apportées à la clé de registre ne correspondent pas à une modification réelle du profil de couleurs actuellement actif ; l’application doit vérifie si le profil retourné par **WcsGetDefaultColorProfile** a réellement changé.</span><span class="sxs-lookup"><span data-stu-id="6d686-134">Note that not all registry key changes will correspond to an actual change in the currently active color profile; the app mush check whether the profile returned by **WcsGetDefaultColorProfile** has actually changed.</span></span>

### <a name="universal-windows-uwp-apps"></a><span data-ttu-id="6d686-135">Applications Windows universelles (UWP)</span><span class="sxs-lookup"><span data-stu-id="6d686-135">Universal Windows (UWP) apps</span></span>

<span data-ttu-id="6d686-136">Les applications Windows universelles n’ont pas accès aux clés de Registre ci-dessus.</span><span class="sxs-lookup"><span data-stu-id="6d686-136">Universal Windows Apps do not have access to the above registry keys.</span></span> <span data-ttu-id="6d686-137">Au lieu de cela, ils doivent inscrire un gestionnaire pour l’événement [**DisplayInformation. ColorProfileChanged**](/uwp/api/Windows.Graphics.Display.DisplayInformation) .</span><span class="sxs-lookup"><span data-stu-id="6d686-137">Instead, they should register a handler for the [**DisplayInformation.ColorProfileChanged**](/uwp/api/Windows.Graphics.Display.DisplayInformation) event.</span></span> <span data-ttu-id="6d686-138">Cet événement se déclenche chaque fois que le profil de couleurs actif du moniteur sur lequel l’application s’exécute a changé.</span><span class="sxs-lookup"><span data-stu-id="6d686-138">This event fires whenever the active color profile for the monitor on which the application is running has changed.</span></span> <span data-ttu-id="6d686-139">ColorProfileChanged prend en compte si les associations de profils par utilisateur ou au niveau du système sont utilisées ; ces informations sont extraites des applications UWP.</span><span class="sxs-lookup"><span data-stu-id="6d686-139">ColorProfileChanged takes into account whether per-user or system-wide profile associations are being used; this information is abstracted from UWP apps.</span></span>

<span data-ttu-id="6d686-140">Lors de la réponse à l’événement ColorProfileChanged, l’application doit interroger le profil actuellement actif à l’aide de [**DisplayInformation. GetColorProfileAsync**](/uwp/api/Windows.Graphics.Display.DisplayInformation).</span><span class="sxs-lookup"><span data-stu-id="6d686-140">When responding to the ColorProfileChanged event, the app should query the currently active profile using [**DisplayInformation.GetColorProfileAsync**](/uwp/api/Windows.Graphics.Display.DisplayInformation).</span></span>

 

 