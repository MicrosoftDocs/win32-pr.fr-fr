---
title: Nouveautés de Windows Vista
description: La version 1,0 de la gestion des couleurs des images (ICM) a été fournie dans Microsoft Windows 95 et fournit des fonctionnalités de gestion des couleurs de base dans les contextes de périphérique Windows.
ms.assetid: 3079f84c-0d6c-4f87-a041-de86f5f7d99b
keywords:
- Windows Color System (WCS), Windows Vista
- WCS (Windows Color System), Windows Vista
- gestion des couleurs des images, Windows Vista
- gestion des couleurs, Windows Vista
- couleurs, Windows Vista
- Windows Color System (WCS), systèmes d’exploitation
- WCS (système de couleurs Windows), systèmes d’exploitation
- gestion des couleurs des images, systèmes d’exploitation
- gestion des couleurs, systèmes d’exploitation
- couleurs, systèmes d’exploitation
- ICM (Image Color Management)
- ICM (gestion des couleurs d’image)
- Gestion des couleurs de Windows Vista
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b889dd0ba3b044f0d0f158bd2364f5c3216ec39
ms.sourcegitcommit: 3f366316c02c411c4c5e14620a699f6f30608634
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/04/2021
ms.locfileid: "106525775"
---
# <a name="whats-new-in-windows-vista"></a><span data-ttu-id="71077-116">Nouveautés de Windows Vista</span><span class="sxs-lookup"><span data-stu-id="71077-116">What's New in Windows Vista</span></span>

<span data-ttu-id="71077-117">La version 1,0 de la gestion des couleurs des images (ICM) a été fournie dans Microsoft Windows 95 et fournit des fonctionnalités de gestion des couleurs de base dans les contextes de périphérique Windows.</span><span class="sxs-lookup"><span data-stu-id="71077-117">Version 1.0 of Image Color Management (ICM) was delivered in Microsoft Windows 95, and provides basic color management capabilities within Windows device contexts.</span></span>

<span data-ttu-id="71077-118">ICM version 2,0 a été fourni dans Windows 98, Windows Millennium Edition, Windows 2000 et WindowsXP. il comprenait une variété de nouvelles fonctions qui implémentaient la gestion des couleurs en dehors des contextes de périphérique.</span><span class="sxs-lookup"><span data-stu-id="71077-118">ICM version 2.0 was delivered in Windows 98, Windows Millennium Edition, Windows 2000, and WindowsXP and included a variety of new functions that implemented color management outside of device contexts.</span></span> <span data-ttu-id="71077-119">Ces nouvelles fonctions étaient appropriées pour des exigences de gestion des couleurs plus exigeantes et permettaient aux applications de mieux contrôler le processus de gestion des couleurs.</span><span class="sxs-lookup"><span data-stu-id="71077-119">These new functions were suitable for more demanding color management requirements, and gave applications greater control over the color-management process.</span></span>

<span data-ttu-id="71077-120">Avec la sortie de Windows Vista, ICM 2,0 est désormais inclus dans Windows Color System (WCS) 1,0, qui offre davantage de fonctionnalités.</span><span class="sxs-lookup"><span data-stu-id="71077-120">With the release of Windows Vista, ICM 2.0 is now included in Windows Color System (WCS) 1.0, which adds more functionality.</span></span> <span data-ttu-id="71077-121">Le tableau suivant répertorie les nouvelles interfaces de programmation d’applications (API) fournies dans Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="71077-121">The following table lists new application programming interfaces (API) that ship in Windows Vista.</span></span>

## <a name="new-api-shipping-in-windows-vista"></a><span data-ttu-id="71077-122">Nouvelle API d’expédition dans Windows Vista</span><span class="sxs-lookup"><span data-stu-id="71077-122">New API Shipping in Windows Vista</span></span>



<span data-ttu-id="71077-123">Énumérations</span><span class="sxs-lookup"><span data-stu-id="71077-123">Enumerations</span></span>

<span data-ttu-id="71077-124">Nom de l’API</span><span class="sxs-lookup"><span data-stu-id="71077-124">API Name</span></span>

<span data-ttu-id="71077-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="71077-125">Header</span></span>

<span data-ttu-id="71077-126">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="71077-126">Library</span></span>

[<span data-ttu-id="71077-127">**COLORDATATYPE**</span><span class="sxs-lookup"><span data-stu-id="71077-127">**COLORDATATYPE**</span></span>](/windows/win32/api/icm/ne-icm-colordatatype)

<span data-ttu-id="71077-128">ICM. h</span><span class="sxs-lookup"><span data-stu-id="71077-128">icm.h</span></span>

<span data-ttu-id="71077-129">MSCMS. lib</span><span class="sxs-lookup"><span data-stu-id="71077-129">mscms.lib</span></span>

[<span data-ttu-id="71077-130">**COLORPROFILESUBTYPE**</span><span class="sxs-lookup"><span data-stu-id="71077-130">**COLORPROFILESUBTYPE**</span></span>](/windows/win32/api/icm/ne-icm-colorprofilesubtype)

<span data-ttu-id="71077-131">ICM. h</span><span class="sxs-lookup"><span data-stu-id="71077-131">icm.h</span></span>

<span data-ttu-id="71077-132">MSCMS. lib</span><span class="sxs-lookup"><span data-stu-id="71077-132">mscms.lib</span></span>

[<span data-ttu-id="71077-133">**COLORPROFILETYPE**</span><span class="sxs-lookup"><span data-stu-id="71077-133">**COLORPROFILETYPE**</span></span>](/windows/win32/api/icm/ne-icm-colorprofiletype)

<span data-ttu-id="71077-134">ICM. h</span><span class="sxs-lookup"><span data-stu-id="71077-134">icm.h</span></span>

<span data-ttu-id="71077-135">MSCMS. lib</span><span class="sxs-lookup"><span data-stu-id="71077-135">mscms.lib</span></span>

[<span data-ttu-id="71077-136">**\_étendue de \_ gestion des profils WCS \_**</span><span class="sxs-lookup"><span data-stu-id="71077-136">**WCS\_PROFILE\_MANAGEMENT\_SCOPE**</span></span>](/windows/win32/api/icm/ne-icm-wcs_profile_management_scope)

<span data-ttu-id="71077-137">ICM. h</span><span class="sxs-lookup"><span data-stu-id="71077-137">icm.h</span></span>

<span data-ttu-id="71077-138">MSCMS. lib</span><span class="sxs-lookup"><span data-stu-id="71077-138">mscms.lib</span></span>



 



<span data-ttu-id="71077-139">Fonctions</span><span class="sxs-lookup"><span data-stu-id="71077-139">Functions</span></span>

<span data-ttu-id="71077-140">Nom de l’API</span><span class="sxs-lookup"><span data-stu-id="71077-140">API Name</span></span>

<span data-ttu-id="71077-141">En-tête</span><span class="sxs-lookup"><span data-stu-id="71077-141">Header</span></span>

<span data-ttu-id="71077-142">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="71077-142">Library</span></span>

[<span data-ttu-id="71077-143">**WcsAssociateColorProfileWithDevice**</span><span class="sxs-lookup"><span data-stu-id="71077-143">**WcsAssociateColorProfileWithDevice**</span></span>](/windows/win32/api/icm/nf-icm-wcsassociatecolorprofilewithdevice)

<span data-ttu-id="71077-144">ICM. h</span><span class="sxs-lookup"><span data-stu-id="71077-144">icm.h</span></span>

<span data-ttu-id="71077-145">MSCMS. lib</span><span class="sxs-lookup"><span data-stu-id="71077-145">mscms.lib</span></span>

[<span data-ttu-id="71077-146">**WcsCheckColors**</span><span class="sxs-lookup"><span data-stu-id="71077-146">**WcsCheckColors**</span></span>](/windows/win32/api/icm/nf-icm-wcsassociatecolorprofilewithdevice)

<span data-ttu-id="71077-147">ICM. h</span><span class="sxs-lookup"><span data-stu-id="71077-147">icm.h</span></span>

<span data-ttu-id="71077-148">MSCMS. lib</span><span class="sxs-lookup"><span data-stu-id="71077-148">mscms.lib</span></span>

[<span data-ttu-id="71077-149">**WcsCreateIccProfile**</span><span class="sxs-lookup"><span data-stu-id="71077-149">**WcsCreateIccProfile**</span></span>](/windows/win32/api/icm/nf-icm-wcscreateiccprofile)

<span data-ttu-id="71077-150">ICM. h</span><span class="sxs-lookup"><span data-stu-id="71077-150">icm.h</span></span>

<span data-ttu-id="71077-151">MSCMS. lib</span><span class="sxs-lookup"><span data-stu-id="71077-151">mscms.lib</span></span>

[<span data-ttu-id="71077-152">**WcsDisassociateColorProfileFromDevice**</span><span class="sxs-lookup"><span data-stu-id="71077-152">**WcsDisassociateColorProfileFromDevice**</span></span>](/windows/win32/api/icm/nf-icm-wcsdisassociatecolorprofilefromdevice)

<span data-ttu-id="71077-153">ICM. h</span><span class="sxs-lookup"><span data-stu-id="71077-153">icm.h</span></span>

<span data-ttu-id="71077-154">MSCMS. lib</span><span class="sxs-lookup"><span data-stu-id="71077-154">mscms.lib</span></span>

[<span data-ttu-id="71077-155">**WcsEnumColorProfiles**</span><span class="sxs-lookup"><span data-stu-id="71077-155">**WcsEnumColorProfiles**</span></span>](/windows/win32/api/icm/nf-icm-wcsenumcolorprofiles)

<span data-ttu-id="71077-156">ICM. h</span><span class="sxs-lookup"><span data-stu-id="71077-156">icm.h</span></span>

<span data-ttu-id="71077-157">MSCMS. lib</span><span class="sxs-lookup"><span data-stu-id="71077-157">mscms.lib</span></span>

[<span data-ttu-id="71077-158">**WcsEnumColorProfilesSize**</span><span class="sxs-lookup"><span data-stu-id="71077-158">**WcsEnumColorProfilesSize**</span></span>](/windows/win32/api/icm/nf-icm-wcsenumcolorprofilessize)

<span data-ttu-id="71077-159">ICM. h</span><span class="sxs-lookup"><span data-stu-id="71077-159">icm.h</span></span>

<span data-ttu-id="71077-160">MSCMS. lib</span><span class="sxs-lookup"><span data-stu-id="71077-160">mscms.lib</span></span>

[<span data-ttu-id="71077-161">**WcsGetDefaultColorProfile**</span><span class="sxs-lookup"><span data-stu-id="71077-161">**WcsGetDefaultColorProfile**</span></span>](/windows/win32/api/icm/nf-icm-wcsgetdefaultcolorprofile)

<span data-ttu-id="71077-162">ICM. h</span><span class="sxs-lookup"><span data-stu-id="71077-162">icm.h</span></span>

<span data-ttu-id="71077-163">MSCMS. lib</span><span class="sxs-lookup"><span data-stu-id="71077-163">mscms.lib</span></span>

[<span data-ttu-id="71077-164">**WcsGetDefaultColorProfileSize**</span><span class="sxs-lookup"><span data-stu-id="71077-164">**WcsGetDefaultColorProfileSize**</span></span>](/windows/win32/api/icm/nf-icm-wcsgetdefaultcolorprofilesize)

<span data-ttu-id="71077-165">ICM. h</span><span class="sxs-lookup"><span data-stu-id="71077-165">icm.h</span></span>

<span data-ttu-id="71077-166">MSCMS. lib</span><span class="sxs-lookup"><span data-stu-id="71077-166">mscms.lib</span></span>

[<span data-ttu-id="71077-167">**WcsGetDefaultRenderingIntent**</span><span class="sxs-lookup"><span data-stu-id="71077-167">**WcsGetDefaultRenderingIntent**</span></span>](/windows/win32/api/icm/nf-icm-wcsgetdefaultrenderingintent)

<span data-ttu-id="71077-168">ICM. h</span><span class="sxs-lookup"><span data-stu-id="71077-168">icm.h</span></span>

<span data-ttu-id="71077-169">MSCMS. lib</span><span class="sxs-lookup"><span data-stu-id="71077-169">mscms.lib</span></span>

[<span data-ttu-id="71077-170">**WcsGetUsePerUserProfiles**</span><span class="sxs-lookup"><span data-stu-id="71077-170">**WcsGetUsePerUserProfiles**</span></span>](/windows/win32/api/icm/nf-icm-wcsgetdefaultrenderingintent)

<span data-ttu-id="71077-171">ICM. h</span><span class="sxs-lookup"><span data-stu-id="71077-171">icm.h</span></span>

<span data-ttu-id="71077-172">MSCMS. lib</span><span class="sxs-lookup"><span data-stu-id="71077-172">mscms.lib</span></span>

[<span data-ttu-id="71077-173">**WcsOpenColorProfileW**</span><span class="sxs-lookup"><span data-stu-id="71077-173">**WcsOpenColorProfileW**</span></span>](/windows/win32/api/icm/nf-icm-wcsopencolorprofilew)

<span data-ttu-id="71077-174">ICM. h</span><span class="sxs-lookup"><span data-stu-id="71077-174">icm.h</span></span>

<span data-ttu-id="71077-175">MSCMS. lib</span><span class="sxs-lookup"><span data-stu-id="71077-175">mscms.lib</span></span>

[<span data-ttu-id="71077-176">**WcsSetDefaultColorProfile**</span><span class="sxs-lookup"><span data-stu-id="71077-176">**WcsSetDefaultColorProfile**</span></span>](/windows/win32/api/icm/nf-icm-wcssetdefaultcolorprofile)

<span data-ttu-id="71077-177">ICM. h</span><span class="sxs-lookup"><span data-stu-id="71077-177">icm.h</span></span>

<span data-ttu-id="71077-178">MSCMS. lib</span><span class="sxs-lookup"><span data-stu-id="71077-178">mscms.lib</span></span>

[<span data-ttu-id="71077-179">**WcsSetDefaultRenderingIntent**</span><span class="sxs-lookup"><span data-stu-id="71077-179">**WcsSetDefaultRenderingIntent**</span></span>](/windows/win32/api/icm/nf-icm-wcssetdefaultrenderingintent)

<span data-ttu-id="71077-180">ICM. h</span><span class="sxs-lookup"><span data-stu-id="71077-180">icm.h</span></span>

<span data-ttu-id="71077-181">MSCMS. lib</span><span class="sxs-lookup"><span data-stu-id="71077-181">mscms.lib</span></span>

[<span data-ttu-id="71077-182">**WcsSetUsePerUserProfiles**</span><span class="sxs-lookup"><span data-stu-id="71077-182">**WcsSetUsePerUserProfiles**</span></span>](/windows/win32/api/icm/nf-icm-wcssetuseperuserprofiles)

<span data-ttu-id="71077-183">ICM. h</span><span class="sxs-lookup"><span data-stu-id="71077-183">icm.h</span></span>

<span data-ttu-id="71077-184">MSCMS. lib</span><span class="sxs-lookup"><span data-stu-id="71077-184">mscms.lib</span></span>

[<span data-ttu-id="71077-185">**WcsTranslateColors**</span><span class="sxs-lookup"><span data-stu-id="71077-185">**WcsTranslateColors**</span></span>](/windows/win32/api/icm/nf-icm-wcstranslatecolors)

<span data-ttu-id="71077-186">ICM. h</span><span class="sxs-lookup"><span data-stu-id="71077-186">icm.h</span></span>

<span data-ttu-id="71077-187">MSCMS. lib</span><span class="sxs-lookup"><span data-stu-id="71077-187">mscms.lib</span></span>



 



<span data-ttu-id="71077-188">Interfaces et leurs fonctions</span><span class="sxs-lookup"><span data-stu-id="71077-188">Interfaces and Their Functions</span></span>

<span data-ttu-id="71077-189">Nom de l’API</span><span class="sxs-lookup"><span data-stu-id="71077-189">API Name</span></span>

<span data-ttu-id="71077-190">En-tête</span><span class="sxs-lookup"><span data-stu-id="71077-190">Header</span></span>

<span data-ttu-id="71077-191">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="71077-191">Library</span></span>

[<span data-ttu-id="71077-192">**IDeviceModelPlugin**</span><span class="sxs-lookup"><span data-stu-id="71077-192">**IDeviceModelPlugin**</span></span>](/previous-versions/windows/desktop/api/wcsplugin/nn-wcsplugin-idevicemodelplugin)

<span data-ttu-id="71077-193">WcsPlugIn. h</span><span class="sxs-lookup"><span data-stu-id="71077-193">WcsPlugIn.h</span></span>

<span data-ttu-id="71077-194">N/A</span><span class="sxs-lookup"><span data-stu-id="71077-194">N/A</span></span>

[<span data-ttu-id="71077-195">**IDeviceModelPlugin::ColorimetricToDeviceColors**</span><span class="sxs-lookup"><span data-stu-id="71077-195">**IDeviceModelPlugin::ColorimetricToDeviceColors**</span></span>](/windows/win32/api/wcsplugin/nf-wcsplugin-idevicemodelplugin-colorimetrictodevicecolors)

<span data-ttu-id="71077-196">WcsPlugIn. h</span><span class="sxs-lookup"><span data-stu-id="71077-196">WcsPlugIn.h</span></span>

<span data-ttu-id="71077-197">N/A</span><span class="sxs-lookup"><span data-stu-id="71077-197">N/A</span></span>

[<span data-ttu-id="71077-198">**IDeviceModelPlugin::ColorimetricToDeviceColorsWithBlack**</span><span class="sxs-lookup"><span data-stu-id="71077-198">**IDeviceModelPlugin::ColorimetricToDeviceColorsWithBlack**</span></span>](/windows/win32/api/wcsplugin/nf-wcsplugin-idevicemodelplugin-colorimetrictodevicecolorswithblack)

<span data-ttu-id="71077-199">WcsPlugIn. h</span><span class="sxs-lookup"><span data-stu-id="71077-199">WcsPlugIn.h</span></span>

<span data-ttu-id="71077-200">N/A</span><span class="sxs-lookup"><span data-stu-id="71077-200">N/A</span></span>

[<span data-ttu-id="71077-201">**IDeviceModelPlugin ::D eviceToColorimetricColors**</span><span class="sxs-lookup"><span data-stu-id="71077-201">**IDeviceModelPlugin::DeviceToColorimetricColors**</span></span>](/windows/win32/api/wcsplugin/nf-wcsplugin-idevicemodelplugin-devicetocolorimetriccolors)

<span data-ttu-id="71077-202">WcsPlugIn. h</span><span class="sxs-lookup"><span data-stu-id="71077-202">WcsPlugIn.h</span></span>

<span data-ttu-id="71077-203">N/A</span><span class="sxs-lookup"><span data-stu-id="71077-203">N/A</span></span>

[<span data-ttu-id="71077-204">**IDeviceModelPlugin::GetGamutBoundaryMesh**</span><span class="sxs-lookup"><span data-stu-id="71077-204">**IDeviceModelPlugin::GetGamutBoundaryMesh**</span></span>](/windows/win32/api/wcsplugin/nf-wcsplugin-idevicemodelplugin-getgamutboundarymesh)

<span data-ttu-id="71077-205">WcsPlugIn. h</span><span class="sxs-lookup"><span data-stu-id="71077-205">WcsPlugIn.h</span></span>

<span data-ttu-id="71077-206">N/A</span><span class="sxs-lookup"><span data-stu-id="71077-206">N/A</span></span>

[<span data-ttu-id="71077-207">**IDeviceModelPlugin::GetGamutBoundaryMeshSize**</span><span class="sxs-lookup"><span data-stu-id="71077-207">**IDeviceModelPlugin::GetGamutBoundaryMeshSize**</span></span>](/windows/win32/api/wcsplugin/nf-wcsplugin-idevicemodelplugin-getgamutboundarymeshsize)

<span data-ttu-id="71077-208">WcsPlugIn. h</span><span class="sxs-lookup"><span data-stu-id="71077-208">WcsPlugIn.h</span></span>

<span data-ttu-id="71077-209">N/A</span><span class="sxs-lookup"><span data-stu-id="71077-209">N/A</span></span>

[<span data-ttu-id="71077-210">**IDeviceModelPlugin::GetNeutralAxis**</span><span class="sxs-lookup"><span data-stu-id="71077-210">**IDeviceModelPlugin::GetNeutralAxis**</span></span>](/windows/win32/api/wcsplugin/nf-wcsplugin-idevicemodelplugin-getneutralaxis)

<span data-ttu-id="71077-211">WcsPlugIn. h</span><span class="sxs-lookup"><span data-stu-id="71077-211">WcsPlugIn.h</span></span>

<span data-ttu-id="71077-212">N/A</span><span class="sxs-lookup"><span data-stu-id="71077-212">N/A</span></span>

[<span data-ttu-id="71077-213">**IDeviceModelPlugin::GetNeutralAxisSize**</span><span class="sxs-lookup"><span data-stu-id="71077-213">**IDeviceModelPlugin::GetNeutralAxisSize**</span></span>](/windows/win32/api/wcsplugin/nf-wcsplugin-idevicemodelplugin-getneutralaxissize)

<span data-ttu-id="71077-214">WcsPlugIn. h</span><span class="sxs-lookup"><span data-stu-id="71077-214">WcsPlugIn.h</span></span>

<span data-ttu-id="71077-215">N/A</span><span class="sxs-lookup"><span data-stu-id="71077-215">N/A</span></span>

[<span data-ttu-id="71077-216">**IDeviceModelPlugin::GetNumChannels**</span><span class="sxs-lookup"><span data-stu-id="71077-216">**IDeviceModelPlugin::GetNumChannels**</span></span>](/windows/win32/api/wcsplugin/nf-wcsplugin-idevicemodelplugin-getnumchannels)

<span data-ttu-id="71077-217">WcsPlugIn. h</span><span class="sxs-lookup"><span data-stu-id="71077-217">WcsPlugIn.h</span></span>

<span data-ttu-id="71077-218">N/A</span><span class="sxs-lookup"><span data-stu-id="71077-218">N/A</span></span>

[<span data-ttu-id="71077-219">**IDeviceModelPlugin::GetPrimarySamples**</span><span class="sxs-lookup"><span data-stu-id="71077-219">**IDeviceModelPlugin::GetPrimarySamples**</span></span>](/windows/win32/api/wcsplugin/nf-wcsplugin-idevicemodelplugin-getprimarysamples)

<span data-ttu-id="71077-220">WcsPlugIn. h</span><span class="sxs-lookup"><span data-stu-id="71077-220">WcsPlugIn.h</span></span>

<span data-ttu-id="71077-221">N/A</span><span class="sxs-lookup"><span data-stu-id="71077-221">N/A</span></span>

[<span data-ttu-id="71077-222">**IDeviceModelPlugin :: Initialize**</span><span class="sxs-lookup"><span data-stu-id="71077-222">**IDeviceModelPlugin::Initialize**</span></span>](/windows/win32/api/wcsplugin/nf-wcsplugin-idevicemodelplugin-initialize)

<span data-ttu-id="71077-223">WcsPlugIn. h</span><span class="sxs-lookup"><span data-stu-id="71077-223">WcsPlugIn.h</span></span>

<span data-ttu-id="71077-224">N/A</span><span class="sxs-lookup"><span data-stu-id="71077-224">N/A</span></span>

[<span data-ttu-id="71077-225">**IDeviceModelPlugin::SetTransformDeviceModelInfo**</span><span class="sxs-lookup"><span data-stu-id="71077-225">**IDeviceModelPlugin::SetTransformDeviceModelInfo**</span></span>](/windows/win32/api/wcsplugin/nf-wcsplugin-idevicemodelplugin-settransformdevicemodelinfo)

<span data-ttu-id="71077-226">WcsPlugIn. h</span><span class="sxs-lookup"><span data-stu-id="71077-226">WcsPlugIn.h</span></span>

<span data-ttu-id="71077-227">N/A</span><span class="sxs-lookup"><span data-stu-id="71077-227">N/A</span></span>

[<span data-ttu-id="71077-228">**IGamutMapModelPlugin**</span><span class="sxs-lookup"><span data-stu-id="71077-228">**IGamutMapModelPlugin**</span></span>](/previous-versions/windows/desktop/api/wcsplugin/nn-wcsplugin-igamutmapmodelplugin)

<span data-ttu-id="71077-229">WcsPlugIn. h</span><span class="sxs-lookup"><span data-stu-id="71077-229">WcsPlugIn.h</span></span>

<span data-ttu-id="71077-230">N/A</span><span class="sxs-lookup"><span data-stu-id="71077-230">N/A</span></span>

[<span data-ttu-id="71077-231">**IGamutMapModelPlugin :: Initialize**</span><span class="sxs-lookup"><span data-stu-id="71077-231">**IGamutMapModelPlugin::Initialize**</span></span>](/windows/win32/api/wcsplugin/nf-wcsplugin-igamutmapmodelplugin-initialize)

<span data-ttu-id="71077-232">WcsPlugIn. h</span><span class="sxs-lookup"><span data-stu-id="71077-232">WcsPlugIn.h</span></span>

<span data-ttu-id="71077-233">N/A</span><span class="sxs-lookup"><span data-stu-id="71077-233">N/A</span></span>

[<span data-ttu-id="71077-234">**IGamutMapModelPlugin::SourceToDestinationAppearanceColors**</span><span class="sxs-lookup"><span data-stu-id="71077-234">**IGamutMapModelPlugin::SourceToDestinationAppearanceColors**</span></span>](/windows/win32/api/wcsplugin/nf-wcsplugin-igamutmapmodelplugin-sourcetodestinationappearancecolors)

<span data-ttu-id="71077-235">WcsPlugIn. h</span><span class="sxs-lookup"><span data-stu-id="71077-235">WcsPlugIn.h</span></span>

<span data-ttu-id="71077-236">N/A</span><span class="sxs-lookup"><span data-stu-id="71077-236">N/A</span></span>



 



<span data-ttu-id="71077-237">Structures</span><span class="sxs-lookup"><span data-stu-id="71077-237">Structures</span></span>

<span data-ttu-id="71077-238">Nom de l’API</span><span class="sxs-lookup"><span data-stu-id="71077-238">API Name</span></span>

<span data-ttu-id="71077-239">En-tête</span><span class="sxs-lookup"><span data-stu-id="71077-239">Header</span></span>

<span data-ttu-id="71077-240">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="71077-240">Library</span></span>

[<span data-ttu-id="71077-241">**BlackInformation**</span><span class="sxs-lookup"><span data-stu-id="71077-241">**BlackInformation**</span></span>](/previous-versions/windows/desktop/api/WcsPlugIn/ns-wcsplugin-_blackinformation)

<span data-ttu-id="71077-242">WcsPlugIn. h</span><span class="sxs-lookup"><span data-stu-id="71077-242">WcsPlugIn.h</span></span>

<span data-ttu-id="71077-243">N/A</span><span class="sxs-lookup"><span data-stu-id="71077-243">N/A</span></span>

[<span data-ttu-id="71077-244">**GamutBoundaryDescription**</span><span class="sxs-lookup"><span data-stu-id="71077-244">**GamutBoundaryDescription**</span></span>](/previous-versions/windows/desktop/api/WcsPlugIn/ns-wcsplugin-_gamutboundarydescription)

<span data-ttu-id="71077-245">WcsPlugIn. h</span><span class="sxs-lookup"><span data-stu-id="71077-245">WcsPlugIn.h</span></span>

<span data-ttu-id="71077-246">N/A</span><span class="sxs-lookup"><span data-stu-id="71077-246">N/A</span></span>

[<span data-ttu-id="71077-247">**XYZColorF**</span><span class="sxs-lookup"><span data-stu-id="71077-247">**XYZColorF**</span></span>](https://www.bing.com/search?q=**XYZColorF**)

<span data-ttu-id="71077-248">WcsPlugIn. h</span><span class="sxs-lookup"><span data-stu-id="71077-248">WcsPlugIn.h</span></span>

<span data-ttu-id="71077-249">N/A</span><span class="sxs-lookup"><span data-stu-id="71077-249">N/A</span></span>

[<span data-ttu-id="71077-250">**JChColorF**</span><span class="sxs-lookup"><span data-stu-id="71077-250">**JChColorF**</span></span>](https://www.bing.com/search?q=**JChColorF**)

<span data-ttu-id="71077-251">WcsPlugIn. h</span><span class="sxs-lookup"><span data-stu-id="71077-251">WcsPlugIn.h</span></span>

<span data-ttu-id="71077-252">N/A</span><span class="sxs-lookup"><span data-stu-id="71077-252">N/A</span></span>

[<span data-ttu-id="71077-253">**JabColorF**</span><span class="sxs-lookup"><span data-stu-id="71077-253">**JabColorF**</span></span>](https://www.bing.com/search?q=**JabColorF**)

<span data-ttu-id="71077-254">WcsPlugIn. h</span><span class="sxs-lookup"><span data-stu-id="71077-254">WcsPlugIn.h</span></span>

<span data-ttu-id="71077-255">N/A</span><span class="sxs-lookup"><span data-stu-id="71077-255">N/A</span></span>

[<span data-ttu-id="71077-256">**GamutShell**</span><span class="sxs-lookup"><span data-stu-id="71077-256">**GamutShell**</span></span>](/previous-versions/windows/desktop/api/WcsPlugIn/ns-wcsplugin-_gamutshell)

<span data-ttu-id="71077-257">WcsPlugIn. h</span><span class="sxs-lookup"><span data-stu-id="71077-257">WcsPlugIn.h</span></span>

<span data-ttu-id="71077-258">N/A</span><span class="sxs-lookup"><span data-stu-id="71077-258">N/A</span></span>

[<span data-ttu-id="71077-259">**GamutShellTriangle**</span><span class="sxs-lookup"><span data-stu-id="71077-259">**GamutShellTriangle**</span></span>](/previous-versions/windows/desktop/api/WcsPlugIn/ns-wcsplugin-_gamutshelltriangle)

<span data-ttu-id="71077-260">WcsPlugIn. h</span><span class="sxs-lookup"><span data-stu-id="71077-260">WcsPlugIn.h</span></span>

<span data-ttu-id="71077-261">N/A</span><span class="sxs-lookup"><span data-stu-id="71077-261">N/A</span></span>

[<span data-ttu-id="71077-262">**PrimaryJabColors**</span><span class="sxs-lookup"><span data-stu-id="71077-262">**PrimaryJabColors**</span></span>](/previous-versions/windows/desktop/api/WcsPlugIn/ns-wcsplugin-_primaryjabcolors)

<span data-ttu-id="71077-263">WcsPlugIn. h</span><span class="sxs-lookup"><span data-stu-id="71077-263">WcsPlugIn.h</span></span>

<span data-ttu-id="71077-264">N/A</span><span class="sxs-lookup"><span data-stu-id="71077-264">N/A</span></span>

[<span data-ttu-id="71077-265">**PrimaryXYZColors**</span><span class="sxs-lookup"><span data-stu-id="71077-265">**PrimaryXYZColors**</span></span>](/previous-versions/windows/desktop/api/WcsPlugIn/ns-wcsplugin-_primaryxyzcolors)

<span data-ttu-id="71077-266">WcsPlugIn. h</span><span class="sxs-lookup"><span data-stu-id="71077-266">WcsPlugIn.h</span></span>

<span data-ttu-id="71077-267">N/A</span><span class="sxs-lookup"><span data-stu-id="71077-267">N/A</span></span>



 

 

 