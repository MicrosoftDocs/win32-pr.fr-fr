---
title: Fonctions de gestion des profils
description: Fonctions de gestion des profils
ms.assetid: 185863b7-0b74-4c65-97c3-3c60b86d37fd
keywords:
- Windows Color System (WCS), fonctions
- WCS (système de couleurs Windows), fonctions
- gestion des couleurs des images, fonctions
- gestion des couleurs, fonctions
- couleurs, fonctions
- Référence WCS, fonctions
- référence pour WCS, functions
- Système de couleurs Windows (WCS), profils
- WCS (système de couleurs Windows), profils
- gestion des couleurs des images, profils
- gestion des couleurs, profils
- couleurs, profils
- Référence WCS, profils
- référence pour WCS, profils
- gestion des profils
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8a0e80e300532b20148eef6d9dc362438b6714a3
ms.sourcegitcommit: 3f366316c02c411c4c5e14620a699f6f30608634
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/04/2021
ms.locfileid: "106531764"
---
# <a name="profile-management-functions"></a><span data-ttu-id="05ffa-118">Fonctions de gestion des profils</span><span class="sxs-lookup"><span data-stu-id="05ffa-118">Profile Management Functions</span></span>

## <a name="profile-management-functions"></a><span data-ttu-id="05ffa-119">Fonctions de gestion des profils</span><span class="sxs-lookup"><span data-stu-id="05ffa-119">Profile Management Functions</span></span>

<span data-ttu-id="05ffa-120">Les fonctions d’API suivantes sont utiles pour la gestion des profils.</span><span class="sxs-lookup"><span data-stu-id="05ffa-120">The following API functions are useful in profile management.</span></span>



| <span data-ttu-id="05ffa-121">Fonction</span><span class="sxs-lookup"><span data-stu-id="05ffa-121">Function</span></span>                                                                               | <span data-ttu-id="05ffa-122">Description</span><span class="sxs-lookup"><span data-stu-id="05ffa-122">Description</span></span>                                                                                                                                          |
|----------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="05ffa-123">**AssociateColorProfileWithDeviceW**</span><span class="sxs-lookup"><span data-stu-id="05ffa-123">**AssociateColorProfileWithDeviceW**</span></span>](/windows/win32/api/icm/nf-icm-associatecolorprofilewithdevicew)             | <span data-ttu-id="05ffa-124">Associe un profil de couleurs spécifié à un périphérique spécifié.</span><span class="sxs-lookup"><span data-stu-id="05ffa-124">Associates a specified color profile with a specified device.</span></span>                                                              |
| <span data-ttu-id="05ffa-125">[**CreateProfileFromLogColorSpaceW**] ((/windows/win32/api/icm/nf-icm-createprofilefromlogcolorspacew)</span><span class="sxs-lookup"><span data-stu-id="05ffa-125">[**CreateProfileFromLogColorSpaceW**]((/windows/win32/api/icm/nf-icm-createprofilefromlogcolorspacew)</span></span> | <span data-ttu-id="05ffa-126">Convertit un [espace de couleurs](c.md) logique en un [profil de périphérique](d.md).</span><span class="sxs-lookup"><span data-stu-id="05ffa-126">Converts a logical [color space](c.md) to a [device profile](d.md).</span></span> |
| [<span data-ttu-id="05ffa-127">**DisassociateColorProfileFromDeviceW**</span><span class="sxs-lookup"><span data-stu-id="05ffa-127">**DisassociateColorProfileFromDeviceW**</span></span>](/windows/win32/api/icm/nf-icm-disassociatecolorprofilefromdevicew) | <span data-ttu-id="05ffa-128">Dissocie un profil de couleurs spécifié avec un périphérique spécifié sur un ordinateur spécifié.</span><span class="sxs-lookup"><span data-stu-id="05ffa-128">Disassociates a specified color profile with a specified device on a specified computer.</span></span> |
| [<span data-ttu-id="05ffa-129">**EnumColorProfilesW**</span><span class="sxs-lookup"><span data-stu-id="05ffa-129">**EnumColorProfilesW**</span></span>](/windows/win32/api/icm/nf-icm-enumcolorprofilesw) | <span data-ttu-id="05ffa-130">Énumère tous les profils qui remplissent les critères d’énumération donnés.</span><span class="sxs-lookup"><span data-stu-id="05ffa-130">Enumerates all the profiles satisfying the given enumeration criteria.</span></span> |
| [<span data-ttu-id="05ffa-131">**GetColorDirectoryW**</span><span class="sxs-lookup"><span data-stu-id="05ffa-131">**GetColorDirectoryW**</span></span>](/windows/win32/api/icm/nf-icm-getcolordirectoryw) | <span data-ttu-id="05ffa-132">Récupère le chemin d’accès du répertoire de couleurs Windows sur un ordinateur spécifié.</span><span class="sxs-lookup"><span data-stu-id="05ffa-132">Retrieves the path of the Windows COLOR directory on a specified machine.</span></span> |
| [<span data-ttu-id="05ffa-133">**GetDeviceGammaRamp**</span><span class="sxs-lookup"><span data-stu-id="05ffa-133">**GetDeviceGammaRamp**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-getdevicegammaramp)                                       | <span data-ttu-id="05ffa-134">Obtient la rampe gamma à partir des panneaux d’affichage de couleur directe.</span><span class="sxs-lookup"><span data-stu-id="05ffa-134">Gets the gamma ramp from direct color display boards.</span></span>                                                                                                |
| [<span data-ttu-id="05ffa-135">**GetStandardColorSpaceProfileW**</span><span class="sxs-lookup"><span data-stu-id="05ffa-135">**GetStandardColorSpaceProfileW**</span></span>](/windows/win32/api/icm/nf-icm-getstandardcolorspaceprofilew) | <span data-ttu-id="05ffa-136">Récupère le profil de couleurs inscrit pour l’espace de [couleurs](c.md)standard spécifié.</span><span class="sxs-lookup"><span data-stu-id="05ffa-136">Retrieves the color profile registered for the specified standard [color space](c.md).</span></span> |
| [<span data-ttu-id="05ffa-137">**InstallColorProfileW**</span><span class="sxs-lookup"><span data-stu-id="05ffa-137">**InstallColorProfileW**</span></span>](/windows/win32/api/icm/nf-icm-installcolorprofilew) | <span data-ttu-id="05ffa-138">Installe un profil donné pour une utilisation sur un ordinateur spécifié.</span><span class="sxs-lookup"><span data-stu-id="05ffa-138">Installs a given profile for use on a specified machine.</span></span> <span data-ttu-id="05ffa-139">Le profil est également copié dans le répertoire des couleurs.</span><span class="sxs-lookup"><span data-stu-id="05ffa-139">The profile is also copied to the COLOR directory.</span></span> |
| [<span data-ttu-id="05ffa-140">**RegisterCMMW**</span><span class="sxs-lookup"><span data-stu-id="05ffa-140">**RegisterCMMW**</span></span>](/windows/win32/api/icm/nf-icm-registercmmw) | <span data-ttu-id="05ffa-141">Associe une valeur d’identification spécifiée à la bibliothèque de liens dynamiques du module de gestion des couleurs spécifiée (DLL CMM).</span><span class="sxs-lookup"><span data-stu-id="05ffa-141">Associates a specified identification value with the specified color management module dynamic link library (CMM DLL).</span></span> <span data-ttu-id="05ffa-142">Lorsque cet ID apparaît dans un profil de couleurs, Windows peut localiser le CMM correspondant afin de créer une transformation.</span><span class="sxs-lookup"><span data-stu-id="05ffa-142">When this ID appears in a color profile, Windows can then locate the corresponding CMM so as to create a transform.</span></span> |
| [<span data-ttu-id="05ffa-143">**SetDeviceGammaRamp**</span><span class="sxs-lookup"><span data-stu-id="05ffa-143">**SetDeviceGammaRamp**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-setdevicegammaramp)                                       | <span data-ttu-id="05ffa-144">Définit la rampe gamma sur les panneaux d’affichage de couleur directe.</span><span class="sxs-lookup"><span data-stu-id="05ffa-144">Sets the gamma ramp on direct color display boards.</span></span>                                                                                                  |
| [<span data-ttu-id="05ffa-145">**SetStandardColorSpaceProfileW**</span><span class="sxs-lookup"><span data-stu-id="05ffa-145">**SetStandardColorSpaceProfileW**</span></span>](/windows/win32/api/icm/nf-icm-setstandardcolorspaceprofilew) | <span data-ttu-id="05ffa-146">Inscrit un profil spécifié pour un [espace de couleurs](c.md)standard donné.</span><span class="sxs-lookup"><span data-stu-id="05ffa-146">Registers a specified profile for a given standard [color space](c.md).</span></span> <span data-ttu-id="05ffa-147">Le profil peut être interrogé à l’aide de [GetStandardColorSpaceProfileW](/windows/win32/api/icm/nf-icm-getstandardcolorspaceprofilew).</span><span class="sxs-lookup"><span data-stu-id="05ffa-147">The profile can be queried using [GetStandardColorSpaceProfileW](/windows/win32/api/icm/nf-icm-getstandardcolorspaceprofilew).</span></span> |
| [<span data-ttu-id="05ffa-148">**UninstallColorProfileW**</span><span class="sxs-lookup"><span data-stu-id="05ffa-148">**UninstallColorProfileW**</span></span>](/windows/win32/api/icm/nf-icm-uninstallcolorprofilew) | <span data-ttu-id="05ffa-149">Supprime un profil de couleurs spécifié d’un ordinateur spécifié.</span><span class="sxs-lookup"><span data-stu-id="05ffa-149">Removes a specified color profile from a specified computer.</span></span> <span data-ttu-id="05ffa-150">Les fichiers associés sont éventuellement supprimés du système.</span><span class="sxs-lookup"><span data-stu-id="05ffa-150">Associated files are optionally deleted from the system.</span></span> |
| [<span data-ttu-id="05ffa-151">**UnregisterCMMW**</span><span class="sxs-lookup"><span data-stu-id="05ffa-151">**UnregisterCMMW**</span></span>](/windows/win32/api/icm/nf-icm-unregistercmmw) | <span data-ttu-id="05ffa-152">Dissocie une valeur d’ID spécifiée d’une bibliothèque de liens dynamiques (DLL) de module de gestion des couleurs donnée.</span><span class="sxs-lookup"><span data-stu-id="05ffa-152">Dissociates a specified ID value from a given color management module dynamic-link library (CMM DLL).</span></span> |
| [<span data-ttu-id="05ffa-153">**WcsAssociateColorProfileWithDevice**</span><span class="sxs-lookup"><span data-stu-id="05ffa-153">**WcsAssociateColorProfileWithDevice**</span></span>](/windows/win32/api/icm/nf-icm-wcsassociatecolorprofilewithdevice)       | <span data-ttu-id="05ffa-154">Associe un profil de couleurs WCS spécifié à un périphérique spécifié.</span><span class="sxs-lookup"><span data-stu-id="05ffa-154">Associates a specified WCS color profile with a specified device.</span></span>                                                                                    |
| [<span data-ttu-id="05ffa-155">**WcsCreateIccProfile**</span><span class="sxs-lookup"><span data-stu-id="05ffa-155">**WcsCreateIccProfile**</span></span>](/windows/win32/api/icm/nf-icm-wcscreateiccprofile)                                     | <span data-ttu-id="05ffa-156">Convertit un profil WCS en profil ICC.</span><span class="sxs-lookup"><span data-stu-id="05ffa-156">Converts a WCS profile into an ICC profile.</span></span>                                                                                                          |
| [<span data-ttu-id="05ffa-157">**WcsDisassociateColorProfileFromDevice**</span><span class="sxs-lookup"><span data-stu-id="05ffa-157">**WcsDisassociateColorProfileFromDevice**</span></span>](/windows/win32/api/icm/nf-icm-wcsdisassociatecolorprofilefromdevice) | <span data-ttu-id="05ffa-158">Dissocie un profil de couleurs WCS spécifié avec un périphérique spécifié sur un ordinateur spécifié.</span><span class="sxs-lookup"><span data-stu-id="05ffa-158">Disassociates a specified WCS color profile with a specified device on a specified computer.</span></span>                                                         |
| [<span data-ttu-id="05ffa-159">**WcsEnumColorProfiles**</span><span class="sxs-lookup"><span data-stu-id="05ffa-159">**WcsEnumColorProfiles**</span></span>](/windows/win32/api/icm/nf-icm-wcsenumcolorprofiles)                                   | <span data-ttu-id="05ffa-160">Énumère tous les profils de couleurs qui répondent aux critères d’énumération dans la portée de gestion des profils spécifiée.</span><span class="sxs-lookup"><span data-stu-id="05ffa-160">Enumerates all color profiles that satisfy the enumeration criteria in the specified profile management scope.</span></span>                                       |
| [<span data-ttu-id="05ffa-161">**WcsEnumColorProfilesSize**</span><span class="sxs-lookup"><span data-stu-id="05ffa-161">**WcsEnumColorProfilesSize**</span></span>](/windows/win32/api/icm/nf-icm-wcsenumcolorprofilessize)                           | <span data-ttu-id="05ffa-162">Retourne la taille, en octets, de la mémoire tampon requise par la fonction [**WcsEnumColorProfiles**](/windows/win32/api/icm/nf-icm-wcsenumcolorprofiles) pour énumérer les profils de couleurs.</span><span class="sxs-lookup"><span data-stu-id="05ffa-162">Returns the size, in bytes, of the buffer required by the [**WcsEnumColorProfiles**](/windows/win32/api/icm/nf-icm-wcsenumcolorprofiles) function to enumerate color profiles.</span></span> |
| [<span data-ttu-id="05ffa-163">**WcsGetDefaultColorProfile**</span><span class="sxs-lookup"><span data-stu-id="05ffa-163">**WcsGetDefaultColorProfile**</span></span>](/windows/win32/api/icm/nf-icm-wcsgetdefaultcolorprofile)                         | <span data-ttu-id="05ffa-164">Récupère le profil de couleurs par défaut pour un appareil ou la valeur par défaut indépendante du périphérique si l’appareil n’est pas spécifié.</span><span class="sxs-lookup"><span data-stu-id="05ffa-164">Retrieves the default color profile for a device, or the device-independent default if the device is not specified.</span></span>                                  |
| [<span data-ttu-id="05ffa-165">**WcsGetDefaultColorProfileSize**</span><span class="sxs-lookup"><span data-stu-id="05ffa-165">**WcsGetDefaultColorProfileSize**</span></span>](/windows/win32/api/icm/nf-icm-wcsgetdefaultcolorprofilesize) | <span data-ttu-id="05ffa-166">Retourne la taille, en octets, du nom du profil de couleurs par défaut d’un appareil, y compris la marque de fin **null** .</span><span class="sxs-lookup"><span data-stu-id="05ffa-166">Returns the size, in bytes, of the default color profile name for a device, including the **NULL** terminator.</span></span>                                       |
| [<span data-ttu-id="05ffa-167">**WcsGetDefaultRenderingIntent**</span><span class="sxs-lookup"><span data-stu-id="05ffa-167">**WcsGetDefaultRenderingIntent**</span></span>](/windows/win32/api/icm/nf-icm-wcsgetdefaultrenderingintent) | <span data-ttu-id="05ffa-168">Récupère l’intention de rendu par défaut dans la portée de gestion des profils spécifiée.</span><span class="sxs-lookup"><span data-stu-id="05ffa-168">Retrieves the default rendering intent in the specified profile management scope.</span></span>                                                                    |
| [<span data-ttu-id="05ffa-169">**WcsGetUsePerUserProfiles**</span><span class="sxs-lookup"><span data-stu-id="05ffa-169">**WcsGetUsePerUserProfiles**</span></span>](/windows/win32/api/icm/nf-icm-wcsgetdefaultrenderingintent) | <span data-ttu-id="05ffa-170">Détermine si l’utilisateur a choisi d’utiliser une liste d’association de profils par utilisateur pour l’appareil spécifié.</span><span class="sxs-lookup"><span data-stu-id="05ffa-170">Determines whether the user has chosen to use a per-user profile association list for the specified device.</span></span>                                          |
| [<span data-ttu-id="05ffa-171">**WcsOpenColorProfileW**</span><span class="sxs-lookup"><span data-stu-id="05ffa-171">**WcsOpenColorProfileW**</span></span>](/windows/win32/api/icm/nf-icm-wcsopencolorprofilew) | <span data-ttu-id="05ffa-172">Crée un handle vers un profil de couleurs spécifié.</span><span class="sxs-lookup"><span data-stu-id="05ffa-172">Creates a handle to a specified color profile.</span></span>                                                                                                       |
| [<span data-ttu-id="05ffa-173">**WcsSetDefaultColorProfile**</span><span class="sxs-lookup"><span data-stu-id="05ffa-173">**WcsSetDefaultColorProfile**</span></span>](/windows/win32/api/icm/nf-icm-wcssetdefaultcolorprofile) | <span data-ttu-id="05ffa-174">Définit le nom du profil de couleurs par défaut du type de profil spécifié dans l’étendue de gestion des profils spécifiée.</span><span class="sxs-lookup"><span data-stu-id="05ffa-174">Sets the default color profile name of the specified profile type in the specified profile management scope.</span></span>                                         |
| [<span data-ttu-id="05ffa-175">**WcsSetDefaultRenderingIntent**</span><span class="sxs-lookup"><span data-stu-id="05ffa-175">**WcsSetDefaultRenderingIntent**</span></span>](/windows/win32/api/icm/nf-icm-wcssetdefaultrenderingintent) | <span data-ttu-id="05ffa-176">Définit l’intention de rendu par défaut dans la portée de gestion des profils spécifiée.</span><span class="sxs-lookup"><span data-stu-id="05ffa-176">Sets the default rendering intent in the specified profile management scope.</span></span>                                                                         |
| [<span data-ttu-id="05ffa-177">**WcsSetUsePerUserProfiles**</span><span class="sxs-lookup"><span data-stu-id="05ffa-177">**WcsSetUsePerUserProfiles**</span></span>](/windows/win32/api/icm/nf-icm-wcssetuseperuserprofiles)                           | <span data-ttu-id="05ffa-178">Permet à l’utilisateur de spécifier s’il faut utiliser une liste d’association de profils par utilisateur pour l’appareil spécifié.</span><span class="sxs-lookup"><span data-stu-id="05ffa-178">Allows the user to specify whether to use a per-user profile association list for the specified device.</span></span>                                              |



 

## <a name="profile-consumption-functions"></a><span data-ttu-id="05ffa-179">Fonctions de consommation des profils</span><span class="sxs-lookup"><span data-stu-id="05ffa-179">Profile Consumption Functions</span></span>

<span data-ttu-id="05ffa-180">Les API de consommation des profils sont les API de ICM2 qui prennent des profils XML ICC ou WCS, des handles de profil ou des intentions de rendu en tant que paramètres, et un ensemble de nouvelles API pour la prise en charge des profils WCS pour le code de gestion des couleurs des applications.</span><span class="sxs-lookup"><span data-stu-id="05ffa-180">The profile consumption APIs are those APIs in ICM2 that take ICC or WCS XML profiles, profile handles, or rendering intents as parameters, and a set of new APIs for WCS profile support for application color management code.</span></span>

 

## <a name="profiles-and-profile-management-functions"></a><span data-ttu-id="05ffa-181">Fonctions de gestion des profils et des profils</span><span class="sxs-lookup"><span data-stu-id="05ffa-181">Profiles and Profile Management Functions</span></span>

<span data-ttu-id="05ffa-182">Le flux de travail de gestion des profils est basé sur les API ICM2 existantes qui sont augmentées pour fournir des fonctionnalités supplémentaires pour la révision du code de l’application.</span><span class="sxs-lookup"><span data-stu-id="05ffa-182">The profile management workflow is based on existing ICM2 APIs that are augmented to provide additional functionality for revising application code.</span></span>

<span data-ttu-id="05ffa-183">Les profils contiennent des informations utilisées par les algorithmes de traitement des couleurs pour convertir la couleur entre différents espaces de couleurs.</span><span class="sxs-lookup"><span data-stu-id="05ffa-183">Profiles contain information used by color processing algorithms to translate color between different color spaces.</span></span> <span data-ttu-id="05ffa-184">La gestion des profils permet d’interroger et de spécifier les profils qui sont utilisés à différentes étapes par le modèle de traitement des couleurs pour gérer la sortie en couleurs des différents périphériques avec des caractéristiques de couleur différentes.</span><span class="sxs-lookup"><span data-stu-id="05ffa-184">Profile management provides a way to query and specify which profiles get used at different stages by the color processing model to manage color output of various peripheral devices with diverse color characteristics.</span></span>

<span data-ttu-id="05ffa-185">La gestion des profils fournit l’ensemble de fonctionnalités suivant :</span><span class="sxs-lookup"><span data-stu-id="05ffa-185">Profile management provides the following set of functionalities:</span></span>

 

1. <span data-ttu-id="05ffa-186">Installation des profils de couleurs à utiliser dans le système.</span><span class="sxs-lookup"><span data-stu-id="05ffa-186">Installing color profiles for use in the system.</span></span>

 

2. <span data-ttu-id="05ffa-187">Association d’un ou plusieurs profils de couleurs installés à un appareil particulier.</span><span class="sxs-lookup"><span data-stu-id="05ffa-187">Associating one or more installed color profiles with any particular device.</span></span>

 

3. <span data-ttu-id="05ffa-188">Choix d’un profil de couleurs par défaut d’un type particulier parmi les profils pouvant être utilisés dans une étape particulière du traitement des couleurs.</span><span class="sxs-lookup"><span data-stu-id="05ffa-188">Choosing a default color profile of a particular type among the profiles available for use in a particular stage of color processing.</span></span> <span data-ttu-id="05ffa-189">Il peut s’agir d’un appareil parmi les profils qui lui sont associés, ou parmi les profils installés dans le système, et non spécifiques à l’appareil.</span><span class="sxs-lookup"><span data-stu-id="05ffa-189">This could be for a device among the profiles associated with it, or among the profiles installed in the system and not device specific.</span></span>

 

4. <span data-ttu-id="05ffa-190">Énumération des profils de couleurs qui répondent à des critères particuliers parmi les profils installés dans le système.</span><span class="sxs-lookup"><span data-stu-id="05ffa-190">Enumerating color profiles that satisfy particular criteria among the profiles installed in the system.</span></span>

<span data-ttu-id="05ffa-191">Les extensions de nom de fichier de profil WCS sont « . CDMP » pour DMPs, « . camp » pour les CAMPs et « . GMMP » pour GMMPs.</span><span class="sxs-lookup"><span data-stu-id="05ffa-191">The WCS profile filename extensions are ".cdmp" for DMPs, ".camp" for CAMPs, and ".gmmp" for GMMPs.</span></span>

 

<span data-ttu-id="05ffa-192">**Gestion des profils par utilisateur et activation de l’exécution dans le contexte LUA**</span><span class="sxs-lookup"><span data-stu-id="05ffa-192">**Per-user profile management and enabling execution in LUA context**</span></span>

<span data-ttu-id="05ffa-193">L’objectif de la conception décrite dans le document actif est le suivant :</span><span class="sxs-lookup"><span data-stu-id="05ffa-193">The goal of the design described in the current document is as follows:</span></span>

 

1. <span data-ttu-id="05ffa-194">L’implémentation ICM2 héritée ne prend pas en charge la gestion des profils par utilisateur.</span><span class="sxs-lookup"><span data-stu-id="05ffa-194">Legacy ICM2 implementation does not provide support for per-user profile management.</span></span> <span data-ttu-id="05ffa-195">Les différents utilisateurs ne peuvent pas avoir leurs propres paramètres de profil.</span><span class="sxs-lookup"><span data-stu-id="05ffa-195">Different users cannot have their own profile settings.</span></span> <span data-ttu-id="05ffa-196">Dans Vista, l’infrastructure de gestion des profils WCS permet aux utilisateurs de configurer des paramètres de profil individuels pour la plupart des fonctionnalités.</span><span class="sxs-lookup"><span data-stu-id="05ffa-196">In Vista, the WCS profile management infrastructure enables users to configure individual profile settings for most functionalities.</span></span>

 

2. <span data-ttu-id="05ffa-197">Toutes les API de gestion des profils ICM2 héritées modifient les paramètres au niveau du système et nécessitent des privilèges d’administrateur.</span><span class="sxs-lookup"><span data-stu-id="05ffa-197">All legacy ICM2 profile management APIs modify settings system-wide and require administrative privileges.</span></span> <span data-ttu-id="05ffa-198">Dans Windows Vista, tous les utilisateurs s’exécutent dans les paramètres de compte d’utilisateur à faibles privilèges (LUA) la plupart du temps, et les administrateurs peuvent élever les privilèges de manière sélective pour exécuter des applications qui modifient les paramètres au niveau du système.</span><span class="sxs-lookup"><span data-stu-id="05ffa-198">In Windows Vista, all users run in Least-privileged User Account (LUA) settings most of the time, and administrators can elevate privilege selectively to run applications that modify system-wide settings.</span></span> <span data-ttu-id="05ffa-199">Dans la gestion des profils WCS, tous les paramètres de profil par utilisateur sont configurables dans le contexte LUA.</span><span class="sxs-lookup"><span data-stu-id="05ffa-199">In WCS profile management, all per-user profile settings are configurable in LUA context.</span></span> <span data-ttu-id="05ffa-200">Les applications de gestion des profils peuvent s’exécuter en tant que paramètres LUA, en renforçant leur portée d’utilisation et en veillant à ce que la sécurité du système ne soit pas compromise.</span><span class="sxs-lookup"><span data-stu-id="05ffa-200">Profile management applications can run as LUA settings, increasing their scope of use and ensuring that security of the system is not compromised.</span></span>

<span data-ttu-id="05ffa-201">La gestion des profils dans Vista offre les améliorations suivantes par rapport à l’infrastructure ICM2 héritée :</span><span class="sxs-lookup"><span data-stu-id="05ffa-201">Profile management in Vista provides the following enhancements over legacy ICM2 infrastructure:</span></span>

 

1. <span data-ttu-id="05ffa-202">Il permet l’Association de profils à des appareils, les paramètres de profil par défaut et l’énumération de profils dans une étendue par utilisateur et à l’échelle du système.</span><span class="sxs-lookup"><span data-stu-id="05ffa-202">It enables profile association with devices, default profile settings, and enumeration of profiles in both per-user and system-wide scope.</span></span>

 

2. <span data-ttu-id="05ffa-203">L’installation d’un profil reste au niveau du système et nécessite des privilèges d’administrateur.</span><span class="sxs-lookup"><span data-stu-id="05ffa-203">Installing a profile remains system wide and requires administrator privileges.</span></span> <span data-ttu-id="05ffa-204">Cela est cohérent avec l’installation du profil lors de l’installation du périphérique, car l’installation de l’appareil est à l’ensemble du système et nécessite des privilèges d’administrateur.</span><span class="sxs-lookup"><span data-stu-id="05ffa-204">This is consistent with profile installation during device installation because device installation is system wide and requires administrative privileges.</span></span>

 

<span data-ttu-id="05ffa-205">Le fait que les appareils puissent être installés à partir du contexte LUA est spécifique à ce qui est pris en charge pour cette classe d’appareil.</span><span class="sxs-lookup"><span data-stu-id="05ffa-205">Whether devices can be installed from LUA context is particular to what is supported for that class of device.</span></span> <span data-ttu-id="05ffa-206">Par exemple, dans Vista, il est possible d’installer une imprimante à partir du contexte LUA si l’utilisateur dispose des droits nécessaires pour copier des fichiers dans le magasin de pilotes par un administrateur de domaine à l’aide des stratégies du magasin de pilotes.</span><span class="sxs-lookup"><span data-stu-id="05ffa-206">For example, in Vista, it is possible to do printer installation from LUA context if the user has been granted rights to copy files into the driver store by a domain administrator using driver store policies.</span></span> <span data-ttu-id="05ffa-207">L’infrastructure de gestion des profils de couleurs n’a rien à faire à ce sujet, car l’installation s’effectue dans le contexte du spouleur.</span><span class="sxs-lookup"><span data-stu-id="05ffa-207">Color profile management infrastructure doesn't need to do anything special in this regard since the installation happens in spooler context.</span></span>

 

3. <span data-ttu-id="05ffa-208">La modification des paramètres de profil dans l’étendue par utilisateur peut être effectuée dans le contexte LUA. les modifications à l’ensemble du système nécessitaient des privilèges d’administrateur.</span><span class="sxs-lookup"><span data-stu-id="05ffa-208">Modifying profile settings in per-user scope can be done in LUA context; system-wide modifications required administrative privileges.</span></span> <span data-ttu-id="05ffa-209">Les opérations de gestion des profils qui nécessitent la lecture des informations de configuration peuvent être effectuées dans un contexte LUA pour les paramètres par utilisateur et à l’ensemble du système.</span><span class="sxs-lookup"><span data-stu-id="05ffa-209">Profile management operations that require reading configuration information can be done in LUA context for both per-user and system-wide settings.</span></span>

<span data-ttu-id="05ffa-210">La portée de gestion des profils indique l’étendue des opérations effectuées. à l’ensemble du système ou par utilisateur.</span><span class="sxs-lookup"><span data-stu-id="05ffa-210">Profile management scope indicates the scope of the operations performed; either per-user or system wide.</span></span>

<span data-ttu-id="05ffa-211">Pour chaque opération, il est indiqué s’il peut être effectué à partir du contexte LUA.</span><span class="sxs-lookup"><span data-stu-id="05ffa-211">For each operation, it is indicated whether it can be done from LUA context.</span></span> <span data-ttu-id="05ffa-212">Si une opération ne peut pas être effectuée dans le contexte LUA, l’API de gestion des profils correspondante retourne un échec avec accès refusé.</span><span class="sxs-lookup"><span data-stu-id="05ffa-212">If an operation cannot be performed in LUA context, the corresponding profile management API returns failure with access denied.</span></span> <span data-ttu-id="05ffa-213">Les applications qui utilisent l’API, telles que le panneau de configuration de la gestion des couleurs, peuvent permettre à l’utilisateur d’élever au contexte d’administration (à l’aide de OTS ou de l’interface utilisateur de consentement), puis d’appeler l’API à partir du contexte élevé pour que l’opération aboutisse.</span><span class="sxs-lookup"><span data-stu-id="05ffa-213">Applications using the API, such as Color Management Control Panel, can enable the user to elevate to administrative context (using OTS or Consent UI), and then call the API from the elevated context so that the operation will succeed.</span></span>



<span data-ttu-id="05ffa-214">Opération</span><span class="sxs-lookup"><span data-stu-id="05ffa-214">Operation</span></span>

<span data-ttu-id="05ffa-215">Étendue de gestion des profils</span><span class="sxs-lookup"><span data-stu-id="05ffa-215">Profile Management Scope</span></span>

<span data-ttu-id="05ffa-216">Condition préalable</span><span class="sxs-lookup"><span data-stu-id="05ffa-216">Pre-condition</span></span>

<span data-ttu-id="05ffa-217">Après condition</span><span class="sxs-lookup"><span data-stu-id="05ffa-217">Post-condition</span></span>

<span data-ttu-id="05ffa-218">Exécutable dans le contexte LUA</span><span class="sxs-lookup"><span data-stu-id="05ffa-218">Executable in LUA context</span></span>

<span data-ttu-id="05ffa-219">$ {ROWSPAN2} $Install profil $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="05ffa-219">${ROWSPAN2}$Install profile${REMOVE}$</span></span>  

<span data-ttu-id="05ffa-220">À l’ensemble du système</span><span class="sxs-lookup"><span data-stu-id="05ffa-220">System wide</span></span>

<span data-ttu-id="05ffa-221">Le profil a été copié, installé dans le système et peut être utilisé.</span><span class="sxs-lookup"><span data-stu-id="05ffa-221">Profile copied, installed into the system, and available for use.</span></span> <span data-ttu-id="05ffa-222">Le profil est énumérable dans l’étendue à l’échelle du système et de l’utilisateur actuel pour tous les utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="05ffa-222">Profile is enumerable in system-wide and current-user scope for all users.</span></span>

<span data-ttu-id="05ffa-223">Lors de l’installation du pilote de périphérique, régie par les stratégies d’installation du pilote.</span><span class="sxs-lookup"><span data-stu-id="05ffa-223">During device driver installation, governed by driver installation policies.</span></span> <span data-ttu-id="05ffa-224">« NON » dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="05ffa-224">No, otherwise.</span></span>

<span data-ttu-id="05ffa-225">Utilisateur actuel</span><span class="sxs-lookup"><span data-stu-id="05ffa-225">Current user</span></span>

<span data-ttu-id="05ffa-226">Non pris en charge</span><span class="sxs-lookup"><span data-stu-id="05ffa-226">Not supported</span></span>

<span data-ttu-id="05ffa-227">$ {ROWSPAN2} $Uninstall profil $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="05ffa-227">${ROWSPAN2}$Uninstall profile${REMOVE}$</span></span>  

<span data-ttu-id="05ffa-228">À l’ensemble du système</span><span class="sxs-lookup"><span data-stu-id="05ffa-228">System wide</span></span>

<span data-ttu-id="05ffa-229">Le profil est installé dans le système</span><span class="sxs-lookup"><span data-stu-id="05ffa-229">Profile is installed in the system</span></span>

<span data-ttu-id="05ffa-230">Profil désinstallé du système et éventuellement supprimé du magasin de profils.</span><span class="sxs-lookup"><span data-stu-id="05ffa-230">Profile uninstalled from the system and optionally deleted from the profile store.</span></span> <span data-ttu-id="05ffa-231">Le profil n’est plus disponible et n’est pas énumérable dans une étendue.</span><span class="sxs-lookup"><span data-stu-id="05ffa-231">Profile is no longer available for use and is not enumerable in any scope.</span></span>

<span data-ttu-id="05ffa-232">Non</span><span class="sxs-lookup"><span data-stu-id="05ffa-232">No</span></span>

<span data-ttu-id="05ffa-233">Utilisateur actuel</span><span class="sxs-lookup"><span data-stu-id="05ffa-233">Current user</span></span>

<span data-ttu-id="05ffa-234">Non pris en charge</span><span class="sxs-lookup"><span data-stu-id="05ffa-234">Not supported</span></span>

<span data-ttu-id="05ffa-235">$ {ROWSPAN2} profil $Associate avec l’appareil $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="05ffa-235">${ROWSPAN2}$Associate profile with device${REMOVE}$</span></span>  

<span data-ttu-id="05ffa-236">À l’ensemble du système</span><span class="sxs-lookup"><span data-stu-id="05ffa-236">System wide</span></span>

<span data-ttu-id="05ffa-237">Le profil est installé et est de type ICC ou CDMP</span><span class="sxs-lookup"><span data-stu-id="05ffa-237">Profile is installed and is of type ICC or CDMP</span></span>

<span data-ttu-id="05ffa-238">Le profil peut être utilisé avec l’appareil par tous les utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="05ffa-238">Profile is available for use with the device by all users.</span></span> <span data-ttu-id="05ffa-239">Il est énumérable, dans une portée à l’échelle du système et également pour l’étendue de l’utilisateur actuel pour tous les utilisateurs, comme associé à l’appareil.</span><span class="sxs-lookup"><span data-stu-id="05ffa-239">It is enumerable, in system-wide scope and also current-user scope for all users, as associated with the device.</span></span>

<span data-ttu-id="05ffa-240">Non</span><span class="sxs-lookup"><span data-stu-id="05ffa-240">No</span></span>

<span data-ttu-id="05ffa-241">Utilisateur actuel</span><span class="sxs-lookup"><span data-stu-id="05ffa-241">Current user</span></span>

<span data-ttu-id="05ffa-242">Le profil est installé.</span><span class="sxs-lookup"><span data-stu-id="05ffa-242">Profile is installed.</span></span> <span data-ttu-id="05ffa-243">Peu importe si le profil est déjà associé à l’appareil dans l’étendue à l’échelle du système et s’il est de type ICC ou CDMP.</span><span class="sxs-lookup"><span data-stu-id="05ffa-243">It does not matter whether the profile is already associated to the device in system-wide scope and is of type ICC or CDMP.</span></span>

<span data-ttu-id="05ffa-244">Le profil peut être utilisé avec l’appareil par l’utilisateur actuel.</span><span class="sxs-lookup"><span data-stu-id="05ffa-244">Profile is available for use with the device by current user.</span></span> <span data-ttu-id="05ffa-245">Elle est énumérable uniquement dans l’étendue de l’utilisateur actuel (à moins qu’il y ait également une association à l’échelle du système) associée à l’appareil.</span><span class="sxs-lookup"><span data-stu-id="05ffa-245">It is enumerable only in current-user scope (unless there is a system-wide association as well) as associated with the device.</span></span>

<span data-ttu-id="05ffa-246">Oui</span><span class="sxs-lookup"><span data-stu-id="05ffa-246">Yes</span></span>

<span data-ttu-id="05ffa-247">Profil de $Disassociate $ {ROWSPAN2} du périphérique $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="05ffa-247">${ROWSPAN2}$Disassociate profile from device${REMOVE}$</span></span>  

<span data-ttu-id="05ffa-248">À l’ensemble du système</span><span class="sxs-lookup"><span data-stu-id="05ffa-248">System wide</span></span>

<span data-ttu-id="05ffa-249">Le profil est associé à l’appareil dans l’étendue à l’échelle du système et est de type ICC ou CDMP</span><span class="sxs-lookup"><span data-stu-id="05ffa-249">Profile is associated with the device in system-wide scope and is of type ICC or CDMP</span></span>

<span data-ttu-id="05ffa-250">Le profil n’est plus disponible pour une utilisation (sauf pour les utilisateurs qui ont également cette association dans leur étendue d’utilisateur actuel).</span><span class="sxs-lookup"><span data-stu-id="05ffa-250">Profile is no longer available for use (except for users who have this association in their current-user scope as well).</span></span> <span data-ttu-id="05ffa-251">Elle n’est pas énumérable dans une portée à l’échelle du système.</span><span class="sxs-lookup"><span data-stu-id="05ffa-251">It is not enumerable in system-wide scope.</span></span> <span data-ttu-id="05ffa-252">Toutefois, elle peut être énumérable dans l’étendue de l’utilisateur actuel pour un utilisateur qui a cette association dans son étendue.</span><span class="sxs-lookup"><span data-stu-id="05ffa-252">It could be enumerable in current-user scope though, for a user who has this association in its scope.</span></span>

<span data-ttu-id="05ffa-253">Non</span><span class="sxs-lookup"><span data-stu-id="05ffa-253">No</span></span>

<span data-ttu-id="05ffa-254">Utilisateur actuel</span><span class="sxs-lookup"><span data-stu-id="05ffa-254">Current user</span></span>

<span data-ttu-id="05ffa-255">Le profil est associé à l’appareil dans l’étendue de l’utilisateur actuel (qu’il soit associé à l’étendue système) et est de type ICC ou CDMP.</span><span class="sxs-lookup"><span data-stu-id="05ffa-255">Profile is associated with the device in current-user scope (irrespective of whether it is associated in system-wide scope) and is of type ICC or CDMP.</span></span>

<span data-ttu-id="05ffa-256">Le profil n’est plus disponible ou est énumérable comme associé à l’appareil, par l’utilisateur actuel (sauf s’il est également associé à l’appareil à l’échelle du système).</span><span class="sxs-lookup"><span data-stu-id="05ffa-256">Profile is no longer available for use, or enumerable as associated to the device, by current user (unless it is also associated in system-wide scope to the device).</span></span>

<span data-ttu-id="05ffa-257">Oui</span><span class="sxs-lookup"><span data-stu-id="05ffa-257">Yes</span></span>

<span data-ttu-id="05ffa-258">$ {ROWSPAN2} $Set profil pour un type (DMP ou ICC) comme valeur par défaut pour un appareil $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="05ffa-258">${ROWSPAN2}$Set profile for a type (DMP or ICC) as default for a device${REMOVE}$</span></span>  

<span data-ttu-id="05ffa-259">À l’ensemble du système</span><span class="sxs-lookup"><span data-stu-id="05ffa-259">System wide</span></span>

<span data-ttu-id="05ffa-260">Le profil est de type ICC ou CDMP</span><span class="sxs-lookup"><span data-stu-id="05ffa-260">Profile is of type ICC or CDMP</span></span>

<span data-ttu-id="05ffa-261">Le profil est utilisé par défaut pour le type particulier avec l’appareil, pour tous les utilisateurs, à l’exception de ceux qui ont remplacé ce paramètre dans l’étendue de l’utilisateur actuel.</span><span class="sxs-lookup"><span data-stu-id="05ffa-261">The profile is used by default, for the particular type with the device, for all users except for those who have overridden this setting in their current-user scope.</span></span> <span data-ttu-id="05ffa-262">(Le profil est installé et associé au système d’appareil en largeur, si ce n’est pas déjà le cas.)</span><span class="sxs-lookup"><span data-stu-id="05ffa-262">(The profile is installed and associated to the device system wide, if that is not already the case.)</span></span>

<span data-ttu-id="05ffa-263">Non</span><span class="sxs-lookup"><span data-stu-id="05ffa-263">No</span></span>

<span data-ttu-id="05ffa-264">Utilisateur actuel</span><span class="sxs-lookup"><span data-stu-id="05ffa-264">Current user</span></span>

<span data-ttu-id="05ffa-265">Le profil est de type ICC ou CDMP</span><span class="sxs-lookup"><span data-stu-id="05ffa-265">Profile is of type ICC or CDMP</span></span>

<span data-ttu-id="05ffa-266">Le profil est utilisé par défaut pour le type particulier avec l’appareil dans le cas de l’utilisateur actuel, quelle que soit la valeur par défaut à l’ensemble du système pour ce.</span><span class="sxs-lookup"><span data-stu-id="05ffa-266">The profile is used by default for the particular type with the device in case of current user, irrespective of the system-wide default for this.</span></span> <span data-ttu-id="05ffa-267">(Le profil est installé et associé à l’appareil pour l’utilisateur actuel, si ce n’est pas déjà le cas.)</span><span class="sxs-lookup"><span data-stu-id="05ffa-267">(The profile is installed and associated to the device for current user, if that is not already the case.)</span></span>

<span data-ttu-id="05ffa-268">Oui, si le profil est déjà installé</span><span class="sxs-lookup"><span data-stu-id="05ffa-268">Yes, if the profile is already installed</span></span>

<span data-ttu-id="05ffa-269">$ {ROWSPAN2} $Set profil pour un type (ICC, DMP, CAMP, GMMP) et une combinaison de sous-type en tant que valeur globale par défaut $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="05ffa-269">${ROWSPAN2}$Set profile for a type (ICC, DMP, CAMP, GMMP) and subtype combination as global default${REMOVE}$</span></span>  

<span data-ttu-id="05ffa-270">À l’ensemble du système</span><span class="sxs-lookup"><span data-stu-id="05ffa-270">System wide</span></span>

<span data-ttu-id="05ffa-271">Seuls les profils ICC et CDMP peuvent être associés à des appareils.</span><span class="sxs-lookup"><span data-stu-id="05ffa-271">Only ICC and CDMP profiles can be associated with devices.</span></span>

<span data-ttu-id="05ffa-272">Le profil est utilisé par défaut pour le type particulier.</span><span class="sxs-lookup"><span data-stu-id="05ffa-272">The profile is used by default for the particular type.</span></span> <span data-ttu-id="05ffa-273">Les utilisateurs peuvent remplacer ce paramètre dans l’étendue de l’utilisateur actuel.</span><span class="sxs-lookup"><span data-stu-id="05ffa-273">Users can override this setting in the current-user scope.</span></span> <span data-ttu-id="05ffa-274">(Le profil est installé, si ce n’est pas déjà le cas.)</span><span class="sxs-lookup"><span data-stu-id="05ffa-274">(The profile is installed, if that is not already the case.)</span></span>

<span data-ttu-id="05ffa-275">Non</span><span class="sxs-lookup"><span data-stu-id="05ffa-275">No</span></span>

<span data-ttu-id="05ffa-276">Utilisateur actuel</span><span class="sxs-lookup"><span data-stu-id="05ffa-276">Current user</span></span>

<span data-ttu-id="05ffa-277">Seuls les profils ICC et CDMP peuvent être associés à des appareils.</span><span class="sxs-lookup"><span data-stu-id="05ffa-277">Only ICC and CDMP profiles can be associated with devices.</span></span>

<span data-ttu-id="05ffa-278">Le profil est utilisé par défaut pour le type particulier de l’utilisateur actuel.</span><span class="sxs-lookup"><span data-stu-id="05ffa-278">The profile is used by default for the particular type for current user.</span></span> <span data-ttu-id="05ffa-279">(Le profil est installé, si ce n’est pas déjà le cas.)</span><span class="sxs-lookup"><span data-stu-id="05ffa-279">(The profile is installed, if that is not already the case.)</span></span>

<span data-ttu-id="05ffa-280">Oui, si le profil est déjà installé.</span><span class="sxs-lookup"><span data-stu-id="05ffa-280">Yes, if the profile is already installed.</span></span>

<span data-ttu-id="05ffa-281">$ {ROWSPAN2} $Erase la substitution de l’utilisateur actuel pour un paramètre de profil par défaut particulier, afin que la valeur système par défaut soit toujours utilisée (comme secours) même pour l’étendue de l’utilisateur actuel. $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="05ffa-281">${ROWSPAN2}$Erase the current-user override for a particular default profile setting, so that the system default always gets used (as fallback) even for current-user scope.${REMOVE}$</span></span>  

<span data-ttu-id="05ffa-282">À l’ensemble du système</span><span class="sxs-lookup"><span data-stu-id="05ffa-282">System wide</span></span>

<span data-ttu-id="05ffa-283">Non applicable</span><span class="sxs-lookup"><span data-stu-id="05ffa-283">Not applicable</span></span>

<span data-ttu-id="05ffa-284">Utilisateur actuel</span><span class="sxs-lookup"><span data-stu-id="05ffa-284">Current user</span></span>

<span data-ttu-id="05ffa-285">Même pour les requêtes de l’utilisateur actuel sur les paramètres de profil par défaut, les paramètres à l’ensemble du système sont retournés pour être utilisés.</span><span class="sxs-lookup"><span data-stu-id="05ffa-285">Even for current-user queries on default profile settings, system-wide settings are returned for use.</span></span>

<span data-ttu-id="05ffa-286">Oui</span><span class="sxs-lookup"><span data-stu-id="05ffa-286">Yes</span></span>

<span data-ttu-id="05ffa-287">$ {ROWSPAN2} $Enumerate les profils installés répondant à des critères particuliers (tels que la classe de périphérique, la classe de profil, etc.) $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="05ffa-287">${ROWSPAN2}$Enumerate installed profiles satisfying particular criteria (like device class, profile class, etc.)${REMOVE}$</span></span>  

<span data-ttu-id="05ffa-288">À l’ensemble du système</span><span class="sxs-lookup"><span data-stu-id="05ffa-288">System wide</span></span>

<span data-ttu-id="05ffa-289">Seuls les profils ICC et CDMP peuvent être associés et énumérés pour les appareils.</span><span class="sxs-lookup"><span data-stu-id="05ffa-289">Only ICC and CDMP profiles can be associated with and enumerated for devices.</span></span>

<span data-ttu-id="05ffa-290">Les profils qui sont installés et qui répondent aux critères spécifiés dans l’étendue à l’échelle du système sont énumérés.</span><span class="sxs-lookup"><span data-stu-id="05ffa-290">Profiles that are installed and satisfy the specified criteria in system-wide scope are enumerated.</span></span>

<span data-ttu-id="05ffa-291">Oui</span><span class="sxs-lookup"><span data-stu-id="05ffa-291">Yes</span></span>

<span data-ttu-id="05ffa-292">Utilisateur actuel</span><span class="sxs-lookup"><span data-stu-id="05ffa-292">Current user</span></span>

<span data-ttu-id="05ffa-293">Seuls les profils ICC et CDMP peuvent être associés à des appareils et, par conséquent, énumérés pour les appareils.</span><span class="sxs-lookup"><span data-stu-id="05ffa-293">Only ICC and CDMP profiles can be associated with devices and thus enumerated for devices.</span></span>

<span data-ttu-id="05ffa-294">Les profils qui sont installés et qui répondent aux critères spécifiés dans l’étendue à l’échelle du système sont énumérés.</span><span class="sxs-lookup"><span data-stu-id="05ffa-294">Profiles which are installed and satisfy the specified criteria in system-wide scope are enumerated.</span></span>

<span data-ttu-id="05ffa-295">Oui</span><span class="sxs-lookup"><span data-stu-id="05ffa-295">Yes</span></span>

<span data-ttu-id="05ffa-296">$ {ROWSPAN2} $Enumerate profils associés à un appareil particulier répondant à des critères particuliers, tels que la classe de périphérique et la classe de profil $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="05ffa-296">${ROWSPAN2}$Enumerate profiles associated with a particular device satisfying particular criteria, such as device class, and profile class${REMOVE}$</span></span>  

<span data-ttu-id="05ffa-297">À l’ensemble du système</span><span class="sxs-lookup"><span data-stu-id="05ffa-297">System wide</span></span>

<span data-ttu-id="05ffa-298">Seuls les profils ICC et CDMP peuvent être associés et énumérés pour les appareils.</span><span class="sxs-lookup"><span data-stu-id="05ffa-298">Only ICC and CDMP profiles can be associated with and enumerated for devices.</span></span>

<span data-ttu-id="05ffa-299">Les profils associés à l’appareil dans une étendue à l’échelle du système et satisfont aux critères spécifiés dans l’étendue à l’échelle du système sont énumérés.</span><span class="sxs-lookup"><span data-stu-id="05ffa-299">Profiles that are associated with the device in system-wide scope and satisfies the specified criteria in system-wide scope are enumerated.</span></span>

<span data-ttu-id="05ffa-300">Oui</span><span class="sxs-lookup"><span data-stu-id="05ffa-300">Yes</span></span>

<span data-ttu-id="05ffa-301">Utilisateur actuel</span><span class="sxs-lookup"><span data-stu-id="05ffa-301">Current user</span></span>

<span data-ttu-id="05ffa-302">Seuls les profils ICC et CDMP peuvent être associés et énumérés pour les appareils.</span><span class="sxs-lookup"><span data-stu-id="05ffa-302">Only ICC and CDMP profiles can be associated with and enumerated for devices.</span></span>

<span data-ttu-id="05ffa-303">Les profils qui sont disponibles comme associés à l’appareil dans l’étendue de l’utilisateur actuel, y compris les associations à l’échelle du système et satisfont aux critères spécifiés dans l’étendue de l’utilisateur actuel sont énumérés.</span><span class="sxs-lookup"><span data-stu-id="05ffa-303">Profiles that are available as associated with the device in current-user scope, which includes the system-wide associations and satisfies the specified criteria in current-user scope are enumerated.</span></span>

<span data-ttu-id="05ffa-304">Oui</span><span class="sxs-lookup"><span data-stu-id="05ffa-304">Yes</span></span>



 

<span data-ttu-id="05ffa-305">Les types de profil de couleurs valides sont fournis par l’énumération COLORPROFILETYPE.</span><span class="sxs-lookup"><span data-stu-id="05ffa-305">The valid color profile types are provided by the COLORPROFILETYPE enumeration.</span></span>

<span data-ttu-id="05ffa-306">Les sous-types de profil de couleurs valides sont fournis par l’énumération COLORPROFILESUBTYPE.</span><span class="sxs-lookup"><span data-stu-id="05ffa-306">The valid color profile subtypes are provided by the COLORPROFILESUBTYPE enumeration.</span></span>

<span data-ttu-id="05ffa-307">Les combinaisons valides de type de profil/sous-type sont indiquées dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="05ffa-307">The valid profile type/subtype combinations are shown in the following table.</span></span>



<span data-ttu-id="05ffa-308">COLORPROFILETYPE </span><span class="sxs-lookup"><span data-stu-id="05ffa-308">COLORPROFILETYPE</span></span>

<span data-ttu-id="05ffa-309">COLORPROFILESUBTYPE valide</span><span class="sxs-lookup"><span data-stu-id="05ffa-309">Valid COLORPROFILESUBTYPE</span></span>

<span data-ttu-id="05ffa-310">Notes</span><span class="sxs-lookup"><span data-stu-id="05ffa-310">Notes</span></span>

<span data-ttu-id="05ffa-311">Paramètre par défaut de l’appareil</span><span class="sxs-lookup"><span data-stu-id="05ffa-311">Device Default</span></span>

<span data-ttu-id="05ffa-312">Valeur par défaut globale</span><span class="sxs-lookup"><span data-stu-id="05ffa-312">Global Default</span></span>

<span data-ttu-id="05ffa-313">Utilisation prévue</span><span class="sxs-lookup"><span data-stu-id="05ffa-313">Intended Use</span></span>

<span data-ttu-id="05ffa-314">Utilisation prévue</span><span class="sxs-lookup"><span data-stu-id="05ffa-314">Intended Use</span></span>

<span data-ttu-id="05ffa-315">\_CCI CPT</span><span class="sxs-lookup"><span data-stu-id="05ffa-315">CPT\_ICC</span></span>

<span data-ttu-id="05ffa-316">CPST \_ aucun</span><span class="sxs-lookup"><span data-stu-id="05ffa-316">CPST\_NONE</span></span>

<span data-ttu-id="05ffa-317">Obtenir/définir le profil ICC par défaut associé à un appareil</span><span class="sxs-lookup"><span data-stu-id="05ffa-317">Get/Set default ICC profile associated with a device</span></span>

<span data-ttu-id="05ffa-318">CPST \_ RGBWorkingSpace ou CPST \_ CustomWorkingSpace</span><span class="sxs-lookup"><span data-stu-id="05ffa-318">CPST\_RGBWorkingSpace or CPST\_CustomWorkingSpace</span></span>

<span data-ttu-id="05ffa-319">Obtient/définit le profil ICC en tant que profil d’espace de travail RVB global ou personnalisé.</span><span class="sxs-lookup"><span data-stu-id="05ffa-319">Get/Set ICC profile as global RGB or custom working space profile.</span></span> <span data-ttu-id="05ffa-320">Consultez Remarque.</span><span class="sxs-lookup"><span data-stu-id="05ffa-320">See Note.</span></span>

<span data-ttu-id="05ffa-321">Les COLORPROFILETYPE CPT \_ ICC et CPT \_ DMP s’excluent mutuellement.</span><span class="sxs-lookup"><span data-stu-id="05ffa-321">The COLORPROFILETYPE CPT\_ICC and CPT\_DMP are mutually exclusive.</span></span> <span data-ttu-id="05ffa-322">Le profil de couleurs par défaut que vous définissez pour un espace de travail donné (RVB ou personnalisé) peut être un profil ICC ou DMP, mais pas les deux.</span><span class="sxs-lookup"><span data-stu-id="05ffa-322">The default color profile you set for a given working space (RGB or Custom) can be either an ICC profile or a DMP profile, but not both.</span></span>

<span data-ttu-id="05ffa-323">CPT \_ DMP</span><span class="sxs-lookup"><span data-stu-id="05ffa-323">CPT\_DMP</span></span>

<span data-ttu-id="05ffa-324">CPST \_ aucun</span><span class="sxs-lookup"><span data-stu-id="05ffa-324">CPST\_NONE</span></span>

<span data-ttu-id="05ffa-325">Obtenir/définir le profil DMP par défaut associé à un appareil</span><span class="sxs-lookup"><span data-stu-id="05ffa-325">Get/Set default DMP profile associated with a device</span></span>

<span data-ttu-id="05ffa-326">CPST \_ RGBWorkingSpace ou CPST \_ CustomWorkingSpace</span><span class="sxs-lookup"><span data-stu-id="05ffa-326">CPST\_RGBWorkingSpace or CPST\_CustomWorkingSpace</span></span>

<span data-ttu-id="05ffa-327">Obtient/définit le profil DMP en tant que profil d’espace de travail RVB global ou personnalisé.</span><span class="sxs-lookup"><span data-stu-id="05ffa-327">Get/Set DMP profile as global RGB or custom working space profile.</span></span> <span data-ttu-id="05ffa-328">Consultez Remarque.</span><span class="sxs-lookup"><span data-stu-id="05ffa-328">See Note.</span></span>

<span data-ttu-id="05ffa-329">Les COLORPROFILETYPE CPT \_ ICC et CPT \_ DMP s’excluent mutuellement.</span><span class="sxs-lookup"><span data-stu-id="05ffa-329">The COLORPROFILETYPE CPT\_ICC and CPT\_DMP are mutually exclusive.</span></span> <span data-ttu-id="05ffa-330">Le profil de couleurs par défaut que vous définissez pour un espace de travail donné (RVB ou personnalisé) peut être un profil ICC ou DMP, mais pas les deux.</span><span class="sxs-lookup"><span data-stu-id="05ffa-330">The default color profile you set for a given working space (RGB or Custom) can be either an ICC profile or a DMP profile, but not both.</span></span>



 

> [!Note]  
> <span data-ttu-id="05ffa-331">Quand WcsSetDefaultColorProfile est appelé pour définir un profil DMP comme profil par défaut pour l’espace de travail RVB ou un espace de travail personnalisé, seul un profil DMP de type RGBVirtualDevice, LCD ou CRT est valide.</span><span class="sxs-lookup"><span data-stu-id="05ffa-331">When WcsSetDefaultColorProfile is called to set a DMP profile as the default profile for the RGB working space or a custom working space, only a DMP profile that is of type RGBVirtualDevice, LCD, or CRT is valid.</span></span>
>
>  
>
> <span data-ttu-id="05ffa-332">Quand WcsSetDefaultColorProfile est appelé pour définir un profil ICC comme profil par défaut pour l’espace de travail RVB ou un espace de travail personnalisé, seul un profil ICC dont la classe est « SPAC » ou « DISP » et dont l’espace colorimétrique est « RGB » est valide.</span><span class="sxs-lookup"><span data-stu-id="05ffa-332">When WcsSetDefaultColorProfile is called to set an ICC profile as the default profile for the RGB working space or a custom working space, only an ICC profile whose class is "spac" or "disp," and whose color space is "RGB" is valid.</span></span>

 

<span data-ttu-id="05ffa-333">L’architecture est conçue conformément aux exigences des opérations, comme indiqué dans les énumérations et les tables ci-dessus.</span><span class="sxs-lookup"><span data-stu-id="05ffa-333">The architecture is designed according to the requirements of the operations as mentioned in the enumerations and tables above.</span></span>

### <a name="profile-management-public-api-layer"></a><span data-ttu-id="05ffa-334">Couche API publique de gestion des profils</span><span class="sxs-lookup"><span data-stu-id="05ffa-334">Profile management public API layer</span></span>

<span data-ttu-id="05ffa-335">Étant donné que l’étendue de gestion des profils n’est pas prise en charge par les API ICM2 héritées, un nouvel ensemble d’API de gestion des profils WCS est requis, qui définit l’étendue de gestion des profils en tant qu’utilisateur à l’échelle du système ou</span><span class="sxs-lookup"><span data-stu-id="05ffa-335">Because profile management scope is not supported by legacy ICM2 APIs, a new set of WCS profile management APIs is required that defines profile management scope as system wide or current user.</span></span> <span data-ttu-id="05ffa-336">?</span><span class="sxs-lookup"><span data-stu-id="05ffa-336">?</span></span> <span data-ttu-id="05ffa-337">Les API ICM2 héritées continuent à être prises en charge pour la compatibilité descendante et fonctionnent sur l’étendue de gestion des profils qui est implicite pour l’appel.</span><span class="sxs-lookup"><span data-stu-id="05ffa-337">Legacy ICM2 APIs continue to be supported for backward compatibility, and work on profile management scope that is implicit for the call.</span></span> <span data-ttu-id="05ffa-338">o ICM2 API qui fonctionnent sur l’étendue de l’utilisateur actuel ?</span><span class="sxs-lookup"><span data-stu-id="05ffa-338">o ICM2 APIs that work on current-user scope ?</span></span> <span data-ttu-id="05ffa-339">Cela concerne les opérations qui sont prises en charge à la fois pour l’étendue de l’utilisateur au niveau du système et de l’utilisateur actuel dans la gestion des profils WCS.</span><span class="sxs-lookup"><span data-stu-id="05ffa-339">This is for operations that are supported for both system wide and current-user scope in WCS profile management.</span></span> <span data-ttu-id="05ffa-340">Les API ICM2 héritées appellent sur les nouvelles API WCS avec une étendue de gestion de profil en tant qu’utilisateur actuel.</span><span class="sxs-lookup"><span data-stu-id="05ffa-340">Legacy ICM2 APIs call on new WCS APIs with profile management scope as current user.</span></span> <span data-ttu-id="05ffa-341">Cela est logique du point de vue de l’utilisateur, car cela permet d’activer des paramètres par utilisateur à partir d’applications héritées et d’exécuter la plupart des opérations dans le contexte LUA.</span><span class="sxs-lookup"><span data-stu-id="05ffa-341">This makes sense from user perspective because this enables per-user settings from legacy applications and also executing most of the operations in LUA context.</span></span> <span data-ttu-id="05ffa-342">o ICM2 API qui fonctionnent sur une étendue à l’échelle du système ?</span><span class="sxs-lookup"><span data-stu-id="05ffa-342">o ICM2 APIs that work on system-wide scope ?</span></span> <span data-ttu-id="05ffa-343">Cela concerne les opérations (installer les profils et les profils de désinstallation) qui prennent uniquement en charge l’étendue à l’échelle du système.</span><span class="sxs-lookup"><span data-stu-id="05ffa-343">This is for operations (install profiles and uninstall profiles) that support only system-wide scope.</span></span> <span data-ttu-id="05ffa-344">Aucune nouvelle API de gestion des profils WCS n’est créée et les API existantes peuvent être modifiées.</span><span class="sxs-lookup"><span data-stu-id="05ffa-344">No new WCS profile management APIs are created and existing APIs can be modified.</span></span>

<span data-ttu-id="05ffa-345">Les implémentations sous-jacentes des opérations de gestion des profils fonctionnent sur les entités de données de configuration suivantes pour créer le contexte des algorithmes de traitement des couleurs afin de fournir des fonctionnalités de gestion des couleurs.</span><span class="sxs-lookup"><span data-stu-id="05ffa-345">The underlying implementations of the profile management operations work on the following configuration data entities to create the context for color processing algorithms to provide color management functionalities.</span></span> <span data-ttu-id="05ffa-346">Il s’agit de paramètres spécifiques à l’appareil ou globaux (indépendants du périphérique).</span><span class="sxs-lookup"><span data-stu-id="05ffa-346">They are either device specific or global (device independent) settings.</span></span> <span data-ttu-id="05ffa-347">o données de configuration spécifiques à l’appareil :?</span><span class="sxs-lookup"><span data-stu-id="05ffa-347">o Device specific configuration data: ?</span></span> <span data-ttu-id="05ffa-348">Liste des profils associés à un appareil particulier.</span><span class="sxs-lookup"><span data-stu-id="05ffa-348">List of profiles associated with a particular device.</span></span> <span data-ttu-id="05ffa-349">?</span><span class="sxs-lookup"><span data-stu-id="05ffa-349">?</span></span> <span data-ttu-id="05ffa-350">Profil par défaut pour les différents types de profils associés à un appareil.</span><span class="sxs-lookup"><span data-stu-id="05ffa-350">Default profile for different profile types associated with a device.</span></span> <span data-ttu-id="05ffa-351">?</span><span class="sxs-lookup"><span data-stu-id="05ffa-351">?</span></span> <span data-ttu-id="05ffa-352">Mode de correspondance des profils utilisé pour l’énumération.</span><span class="sxs-lookup"><span data-stu-id="05ffa-352">Matching mode of profiles used for enumeration.</span></span> <span data-ttu-id="05ffa-353">o données de configuration globale :?</span><span class="sxs-lookup"><span data-stu-id="05ffa-353">o Global configuration data: ?</span></span> <span data-ttu-id="05ffa-354">Liste des profils installés dans le système.</span><span class="sxs-lookup"><span data-stu-id="05ffa-354">List of profiles installed in the system.</span></span> <span data-ttu-id="05ffa-355">?</span><span class="sxs-lookup"><span data-stu-id="05ffa-355">?</span></span> <span data-ttu-id="05ffa-356">Profil global par défaut pour les différents types de profils.</span><span class="sxs-lookup"><span data-stu-id="05ffa-356">Global default profile for different profile types.</span></span> <span data-ttu-id="05ffa-357">?</span><span class="sxs-lookup"><span data-stu-id="05ffa-357">?</span></span> <span data-ttu-id="05ffa-358">Les implémentations sous-jacentes du stockage de données de configuration prennent la portée de stockage pour les données de configuration (indépendantes des appareils ou des appareils), qui peuvent être à l’échelle du système ou de l’utilisateur actuel.</span><span class="sxs-lookup"><span data-stu-id="05ffa-358">The underlying implementations of configuration data storage take in storage scope for configuration data (either device independent or device specific), which can be either system wide or current user.</span></span> <span data-ttu-id="05ffa-359">Cela diffère de l’étendue de gestion des profils.</span><span class="sxs-lookup"><span data-stu-id="05ffa-359">This is different from profile management scope.</span></span> <span data-ttu-id="05ffa-360">Une opération avec l’étendue de gestion du profil utilisateur actuel peut entraîner une lecture à partir d’une étendue de stockage à l’échelle du système si le paramètre de l’utilisateur actuel pour cette opération n’est pas présent.</span><span class="sxs-lookup"><span data-stu-id="05ffa-360">An operation with current-user profile management scope can cause a read from a system-wide storage scope if the current-user setting for that operation is not present.</span></span> <span data-ttu-id="05ffa-361">?</span><span class="sxs-lookup"><span data-stu-id="05ffa-361">?</span></span> <span data-ttu-id="05ffa-362">La couche d’API ICM2/WCS appelle dans cette couche de stockage pour obtenir et définir des données avec une étendue de stockage appropriée.</span><span class="sxs-lookup"><span data-stu-id="05ffa-362">The ICM2/WCS API layer calls in this storage layer for getting and setting data with appropriate storage scope.</span></span> <span data-ttu-id="05ffa-363">La couche de stockage est transparente pour l’étendue de gestion des profils.</span><span class="sxs-lookup"><span data-stu-id="05ffa-363">The storage layer is transparent to profile management scope.</span></span> <span data-ttu-id="05ffa-364">La logique permettant de combiner des données à partir d’étendues de stockage à l’échelle de l’utilisateur et du système pour créer ou mettre à jour une configuration en fonction de l’étendue de gestion des profils spécifiée par l’appelant de l’API.</span><span class="sxs-lookup"><span data-stu-id="05ffa-364">The logic for combining data from current-user and system-wide storage scopes to create or update a configuration according to the profile management scope specified by the API caller.</span></span> <span data-ttu-id="05ffa-365">Cette logique est présente dans la couche API ICM2/WCS.</span><span class="sxs-lookup"><span data-stu-id="05ffa-365">This logic is present in the ICM2/WCS API layer.</span></span>

### <a name="device-specific-storage-layer"></a><span data-ttu-id="05ffa-366">Couche de stockage spécifique à l’appareil</span><span class="sxs-lookup"><span data-stu-id="05ffa-366">Device-specific storage layer</span></span>

<span data-ttu-id="05ffa-367">Le stockage de différentes classes d’appareils, tels que l’impression, la capture ou l’affichage, peut être différent.</span><span class="sxs-lookup"><span data-stu-id="05ffa-367">The storage for different classes of devices like print, capture or display could be different from each other.</span></span> <span data-ttu-id="05ffa-368">Par exemple, les données de configuration d’un périphérique d’impression doivent être stockées à l’aide d’API d’impression standard, telles que SetPrinterDataEx et GetPrinterDataEx, pour permettre la copie des profils et le transfert des paramètres vers un ordinateur client pendant la connexion point-à-impression.</span><span class="sxs-lookup"><span data-stu-id="05ffa-368">For example, configuration data for a print device must be stored using standard print APIs, such as SetPrinterDataEx and GetPrinterDataEx, to enable the profiles to be copied and settings to be transferred to a client machine during Point-and-Print connection.</span></span> <span data-ttu-id="05ffa-369">?</span><span class="sxs-lookup"><span data-stu-id="05ffa-369">?</span></span> <span data-ttu-id="05ffa-370">Cette couche exporte les fonctionnalités pour ouvrir le magasin, obtenir des données, définir des données et fermer le magasin à l’aide d’interfaces prédéfinies communes afin que la couche de stockage de configuration de la gestion des profils puisse les appeler tout en étant transparente pour la façon dont les données sont stockées pour cet appareil.</span><span class="sxs-lookup"><span data-stu-id="05ffa-370">This layer exports functionality to open store, get data, set data and close store using common pre-defined interfaces so that the profile management configuration storage layer can call into them while being transparent to the way the data gets stored for that device.</span></span>

<span data-ttu-id="05ffa-371">Le diagramme suivant illustre cette architecture.</span><span class="sxs-lookup"><span data-stu-id="05ffa-371">The following diagram illustrates this architecture.</span></span>



<span data-ttu-id="05ffa-372">Couche API publique de gestion des profils</span><span class="sxs-lookup"><span data-stu-id="05ffa-372">Profile Management Public API Layer</span></span>

<span data-ttu-id="05ffa-373">$ {ROWSPAN2} $Legacy les API ICM2 pour les opérations qui prennent uniquement en charge l’étendue de gestion des profils à l’échelle du système dans Vista (installer, désinstaller et obtenir le répertoire de couleurs).</span><span class="sxs-lookup"><span data-stu-id="05ffa-373">${ROWSPAN2}$Legacy ICM2 APIs for operations that support only system-wide profile management scope in Vista (install, uninstall, and get color directory).</span></span> <span data-ttu-id="05ffa-374">Ils appellent la couche de stockage de configurations avec une étendue de stockage appropriée. $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="05ffa-374">They call the configuration storage layer with appropriate storage scope.${REMOVE}$</span></span>  

<span data-ttu-id="05ffa-375">API ICM2 héritée pour les opérations qui prennent en charge à la fois l’étendue de gestion du profil utilisateur et à l’échelle du système dans Vista (toutes les opérations autres que installer, désinstaller et obtenir le répertoire de couleurs).</span><span class="sxs-lookup"><span data-stu-id="05ffa-375">Legacy ICM2 API for operations that support both system-wide and current-user profile management scope in Vista (all operations other than install, uninstall, and get color directory).</span></span> <span data-ttu-id="05ffa-376">Ils fonctionnent implicitement sur l’étendue de l’utilisateur actuel et appellent la nouvelle API WCS avec l’étendue de gestion des profils comme utilisateur actuel.</span><span class="sxs-lookup"><span data-stu-id="05ffa-376">They implicitly work on current-user scope, and call into new WCS API with profile management scope as current user.</span></span>

<span data-ttu-id="05ffa-377">Nouvelle API WCS avec prise en charge de l’étendue de gestion du profil à l’échelle du système et de l’utilisateur actuel.</span><span class="sxs-lookup"><span data-stu-id="05ffa-377">New WCS API with system-wide and current-user profile management scope support.</span></span> <span data-ttu-id="05ffa-378">Ils appellent la couche de stockage de configurations avec une étendue de stockage appropriée.</span><span class="sxs-lookup"><span data-stu-id="05ffa-378">They call the configuration storage layer with appropriate storage scope.</span></span>



 



<span data-ttu-id="05ffa-379">Couche de stockage configuration de la gestion des profils</span><span class="sxs-lookup"><span data-stu-id="05ffa-379">Profile Management Configuration Storage Layer</span></span>

<span data-ttu-id="05ffa-380">Routines de configuration globale indépendantes du périphérique</span><span class="sxs-lookup"><span data-stu-id="05ffa-380">Device-independent global configuration routines</span></span>

<span data-ttu-id="05ffa-381">Routines de configuration spécifiques à l’appareil</span><span class="sxs-lookup"><span data-stu-id="05ffa-381">Device-specific configuration routines</span></span>

<span data-ttu-id="05ffa-382">$ {ROWSPAN3} $Profile l’installation et la gestion des paramètres de profil par défaut indépendants du périphérique, pris en charge dans l’étendue du stockage à l’échelle du système et de l’utilisateur actuel. $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="05ffa-382">${ROWSPAN3}$Profile installation and device-independent default profile settings management, supported in system-wide and current-user storage scope.${REMOVE}$</span></span>  

<span data-ttu-id="05ffa-383">L’Association d’appareils et la gestion des paramètres de profil par défaut spécifiques au périphérique, pris en charge dans l’étendue du stockage à l’échelle du système et de l’utilisateur actuel.</span><span class="sxs-lookup"><span data-stu-id="05ffa-383">Device association and device-specific default profile settings management, supported in system-wide and current-user storage scope.</span></span>

<span data-ttu-id="05ffa-384">Couche de stockage Device-Specific</span><span class="sxs-lookup"><span data-stu-id="05ffa-384">Device-Specific Storage layer</span></span>

<span data-ttu-id="05ffa-385">Imprimer un stockage spécifique</span><span class="sxs-lookup"><span data-stu-id="05ffa-385">Print specific storage</span></span>

<span data-ttu-id="05ffa-386">Afficher un stockage spécifique</span><span class="sxs-lookup"><span data-stu-id="05ffa-386">Display specific storage</span></span>

<span data-ttu-id="05ffa-387">Capturer un stockage spécifique</span><span class="sxs-lookup"><span data-stu-id="05ffa-387">Capture specific storage</span></span>



 

<span data-ttu-id="05ffa-388">Les API ICM2 héritées pour les opérations qui prennent uniquement en charge l’étendue de gestion des profils à l’échelle du système dans Vista n’ont aucune modification de comportement.</span><span class="sxs-lookup"><span data-stu-id="05ffa-388">Legacy ICM2 APIs for operations that support only system-wide profile management scope in Vista have no changes in behavior.</span></span> <span data-ttu-id="05ffa-389">Les opérations d’installation et de désinstallation appartiennent à cette catégorie.</span><span class="sxs-lookup"><span data-stu-id="05ffa-389">Install and uninstall operations fall in this category.</span></span>

<span data-ttu-id="05ffa-390">Les API ICM2 héritées pour les opérations qui prennent en charge à la fois l’étendue de gestion du profil à l’échelle du système et de l’utilisateur actuel ont un comportement modifié pour interroger et configurer les paramètres de l’utilisateur actuel.</span><span class="sxs-lookup"><span data-stu-id="05ffa-390">Legacy ICM2 APIs for operations that support both system-wide and current-user profile management scope have their behavior changed to query and configure current-user settings.</span></span> <span data-ttu-id="05ffa-391">Toutes les opérations autres que install et Uninstall appartiennent à cette catégorie.</span><span class="sxs-lookup"><span data-stu-id="05ffa-391">All operations other than install and uninstall fall in this category.</span></span>

 

 




