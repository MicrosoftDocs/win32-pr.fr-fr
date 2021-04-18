---
description: Valeurs HRESULT personnalisées pour l’interface de capture Graphics Diagnostics.
MS-HAID: vspixengine.Hresult
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Énumération HRESULT
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 246FA53F-FF5B-44E1-BABB-F45AE0212687
api_name:
- Hresult
api_type:
- HeaderDef
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 3d5419feb0acb5967132fbb804a9bbc11bfa4248
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104521567"
---
# <a name="span-idvspixenginehresultspanhresult-enumeration"></a><span data-ttu-id="522c2-103"><span id="vspixengine.hresult"></span>Énumération HRESULT</span><span class="sxs-lookup"><span data-stu-id="522c2-103"><span id="vspixengine.hresult"></span>Hresult enumeration</span></span>

<span data-ttu-id="522c2-104">Valeurs HRESULT personnalisées pour l’interface de capture Graphics Diagnostics.</span><span class="sxs-lookup"><span data-stu-id="522c2-104">Custom HRESULT values for the graphics diagnostics capture interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="522c2-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="522c2-105">Syntax</span></span>


```C++
};
```

## <a name="constants"></a><span data-ttu-id="522c2-106">Constantes</span><span class="sxs-lookup"><span data-stu-id="522c2-106">Constants</span></span>

<span data-ttu-id="522c2-107"><span id="PIX_S_OK"></span><span id="pix_s_ok"></span>**PIX \_ S \_ OK**</span><span class="sxs-lookup"><span data-stu-id="522c2-107"><span id="PIX_S_OK"></span><span id="pix_s_ok"></span>**PIX\_S\_OK**</span></span>  
<span data-ttu-id="522c2-108">HRESULT commun qui indique que l’opération a réussi comme prévu.</span><span class="sxs-lookup"><span data-stu-id="522c2-108">A common HRESULT which indicates that the operation succeeded as expected.</span></span>

<span data-ttu-id="522c2-109"><span id="PIX_S_FALSE"></span><span id="pix_s_false"></span>**PIX \_ S \_ faux**</span><span class="sxs-lookup"><span data-stu-id="522c2-109"><span id="PIX_S_FALSE"></span><span id="pix_s_false"></span>**PIX\_S\_FALSE**</span></span>  
<span data-ttu-id="522c2-110">HRESULT commun qui indique que l’opération a réussi, mais d’une manière différente de celle attendue.</span><span class="sxs-lookup"><span data-stu-id="522c2-110">A common HRESULT which indicates that the operation succeeded, but in a different way than was expected.</span></span>

<span data-ttu-id="522c2-111"><span id="PIX_ERROR_FILE_NOT_FOUND"></span><span id="pix_error_file_not_found"></span>**\_fichier d’erreur pix \_ \_ \_ introuvable**</span><span class="sxs-lookup"><span data-stu-id="522c2-111"><span id="PIX_ERROR_FILE_NOT_FOUND"></span><span id="pix_error_file_not_found"></span>**PIX\_ERROR\_FILE\_NOT\_FOUND**</span></span>  
<span data-ttu-id="522c2-112">HRESULT personnalisé qui est \_ \_ introuvable dans le fichier d’erreur renvoie \_ .</span><span class="sxs-lookup"><span data-stu-id="522c2-112">A custom HRESULT that echos ERROR\_FILE\_NOT\_FOUND.</span></span>

<span data-ttu-id="522c2-113"><span id="PIX_ERROR_BAD_ENVIRONMENT"></span><span id="pix_error_bad_environment"></span>**erreur PIX- \_ \_ environnement incorrect \_**</span><span class="sxs-lookup"><span data-stu-id="522c2-113"><span id="PIX_ERROR_BAD_ENVIRONMENT"></span><span id="pix_error_bad_environment"></span>**PIX\_ERROR\_BAD\_ENVIRONMENT**</span></span>  
<span data-ttu-id="522c2-114">HRESULT personnalisé qui renvoie l’erreur de l' \_ environnement est incorrect \_ .</span><span class="sxs-lookup"><span data-stu-id="522c2-114">A custom HRESULT that echos ERROR\_BAD\_ENVIRONMENT.</span></span>

<span data-ttu-id="522c2-115"><span id="PIX_ERROR_BAD_FORMAT"></span><span id="pix_error_bad_format"></span>**\_ \_ format incorrect de l’erreur pix \_**</span><span class="sxs-lookup"><span data-stu-id="522c2-115"><span id="PIX_ERROR_BAD_FORMAT"></span><span id="pix_error_bad_format"></span>**PIX\_ERROR\_BAD\_FORMAT**</span></span>  
<span data-ttu-id="522c2-116">HRESULT personnalisé qui renvoie le \_ format incorrect de l’erreur \_ .</span><span class="sxs-lookup"><span data-stu-id="522c2-116">A custom HRESULT that echos ERROR\_BAD\_FORMAT.</span></span>

<span data-ttu-id="522c2-117"><span id="PIX_ERROR_SHARING_VIOLATION"></span><span id="pix_error_sharing_violation"></span>**\_violation de \_ partage d’erreurs pix \_**</span><span class="sxs-lookup"><span data-stu-id="522c2-117"><span id="PIX_ERROR_SHARING_VIOLATION"></span><span id="pix_error_sharing_violation"></span>**PIX\_ERROR\_SHARING\_VIOLATION**</span></span>  
<span data-ttu-id="522c2-118">HRESULT personnalisé qui renvoie une violation de partage d’erreur \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="522c2-118">A custom HRESULT that echos ERROR\_SHARING\_VIOLATION.</span></span>

<span data-ttu-id="522c2-119"><span id="PIX_ERROR_DISK_FULL"></span><span id="pix_error_disk_full"></span>**\_disque d’erreur pix \_ \_ plein**</span><span class="sxs-lookup"><span data-stu-id="522c2-119"><span id="PIX_ERROR_DISK_FULL"></span><span id="pix_error_disk_full"></span>**PIX\_ERROR\_DISK\_FULL**</span></span>  
<span data-ttu-id="522c2-120">HRESULT personnalisé qui renvoie le disque d’erreur \_ \_ saturé.</span><span class="sxs-lookup"><span data-stu-id="522c2-120">A custom HRESULT that echos ERROR\_DISK\_FULL.</span></span>

<span data-ttu-id="522c2-121"><span id="PIX_ERROR_MORE_DATA"></span><span id="pix_error_more_data"></span>**\_erreur pix \_ - \_ données supplémentaires**</span><span class="sxs-lookup"><span data-stu-id="522c2-121"><span id="PIX_ERROR_MORE_DATA"></span><span id="pix_error_more_data"></span>**PIX\_ERROR\_MORE\_DATA**</span></span>  
<span data-ttu-id="522c2-122">HRESULT personnalisé qui renvoie une erreur \_ plus de \_ données.</span><span class="sxs-lookup"><span data-stu-id="522c2-122">A custom HRESULT that echos ERROR\_MORE\_DATA.</span></span>

<span data-ttu-id="522c2-123"><span id="PIX_E_MISSING_DEBUG_KITS_POLICY"></span><span id="pix_e_missing_debug_kits_policy"></span>**\_stratégie de \_ \_ Kits de débogage manquants dans \_ pix E \_**</span><span class="sxs-lookup"><span data-stu-id="522c2-123"><span id="PIX_E_MISSING_DEBUG_KITS_POLICY"></span><span id="pix_e_missing_debug_kits_policy"></span>**PIX\_E\_MISSING\_DEBUG\_KITS\_POLICY**</span></span>  
<span data-ttu-id="522c2-124">HRESULT personnalisé qui indique que la stratégie de kits de débogage est manquante.</span><span class="sxs-lookup"><span data-stu-id="522c2-124">A custom HRESULT which indicates that the Debug Kits policy is missing.</span></span>

<span data-ttu-id="522c2-125"><span id="PIX_E_INVALID_VERSION"></span><span id="pix_e_invalid_version"></span>**PIX \_ E \_ version non valide \_**</span><span class="sxs-lookup"><span data-stu-id="522c2-125"><span id="PIX_E_INVALID_VERSION"></span><span id="pix_e_invalid_version"></span>**PIX\_E\_INVALID\_VERSION**</span></span>  
<span data-ttu-id="522c2-126">HRESULT personnalisé qui indique qu’une version non valide est utilisée.</span><span class="sxs-lookup"><span data-stu-id="522c2-126">A custom HRESULT which indicates that an invalid version is being used.</span></span>

<span data-ttu-id="522c2-127"><span id="PIX_E_USING_DCOMP"></span><span id="pix_e_using_dcomp"></span>**PIX \_ E \_ utilisant \_ DCOMP**</span><span class="sxs-lookup"><span data-stu-id="522c2-127"><span id="PIX_E_USING_DCOMP"></span><span id="pix_e_using_dcomp"></span>**PIX\_E\_USING\_DCOMP**</span></span>  
<span data-ttu-id="522c2-128">HRESULT personnalisé qui indique que DirectComposition est en cours d’utilisation (la capture de DirectComposition n’est pas prise en charge.)</span><span class="sxs-lookup"><span data-stu-id="522c2-128">A custom HRESULT which indicates that DirectComposition is in use (capture of DirectComposition is not supported.)</span></span>

<span data-ttu-id="522c2-129"><span id="PIX_E_USING_DIRECTWRITE"></span><span id="pix_e_using_directwrite"></span>**PIX \_ E \_ à l’aide de \_ DIRECTWRITE**</span><span class="sxs-lookup"><span data-stu-id="522c2-129"><span id="PIX_E_USING_DIRECTWRITE"></span><span id="pix_e_using_directwrite"></span>**PIX\_E\_USING\_DIRECTWRITE**</span></span>  
<span data-ttu-id="522c2-130">HRESULT personnalisé qui indique que DirectWrite est en cours d’utilisation (la capture de DirectWrite n’est pas prise en charge.)</span><span class="sxs-lookup"><span data-stu-id="522c2-130">A custom HRESULT which indicates that DirectWrite is in use (capture of DirectWrite is not supported.)</span></span>

<span data-ttu-id="522c2-131"><span id="PIX_E_USING_D3D9"></span><span id="pix_e_using_d3d9"></span>**PIX \_ E \_ utilisant \_ d3d9**</span><span class="sxs-lookup"><span data-stu-id="522c2-131"><span id="PIX_E_USING_D3D9"></span><span id="pix_e_using_d3d9"></span>**PIX\_E\_USING\_D3D9**</span></span>  
<span data-ttu-id="522c2-132">HRESULT personnalisé qui indique que Direct3D9 est en cours d’utilisation (la capture de Direct3D9 n’est pas prise en charge dans Windows 10.)</span><span class="sxs-lookup"><span data-stu-id="522c2-132">A custom HRESULT which indicates that Direct3D9 is in use (capture of Direct3D9 is not supported in Windows 10.)</span></span>

<span data-ttu-id="522c2-133"><span id="PIX_E_CANT_CREATE_SHADER"></span><span id="pix_e_cant_create_shader"></span>**PIX \_ E \_ Impossible de \_ créer un \_ nuanceur**</span><span class="sxs-lookup"><span data-stu-id="522c2-133"><span id="PIX_E_CANT_CREATE_SHADER"></span><span id="pix_e_cant_create_shader"></span>**PIX\_E\_CANT\_CREATE\_SHADER**</span></span>  
<span data-ttu-id="522c2-134">HRESULT personnalisé qui indique qu’un nuanceur spécifié ne peut pas être créé.</span><span class="sxs-lookup"><span data-stu-id="522c2-134">A custom HRESULT which indicates that a specified shader can't be created.</span></span>

<span data-ttu-id="522c2-135"><span id="PIX_E_USING_D2D"></span><span id="pix_e_using_d2d"></span>**PIX \_ E \_ utilisant \_ D2D**</span><span class="sxs-lookup"><span data-stu-id="522c2-135"><span id="PIX_E_USING_D2D"></span><span id="pix_e_using_d2d"></span>**PIX\_E\_USING\_D2D**</span></span>  
<span data-ttu-id="522c2-136">HRESULT personnalisé qui indique que Direct2D est en cours d’utilisation (la capture de Direct2D n’est pas prise en charge.)</span><span class="sxs-lookup"><span data-stu-id="522c2-136">A custom HRESULT which indicates that Direct2D is in use (capture of Direct2D is not supported.)</span></span>

<span data-ttu-id="522c2-137"><span id="PIX_E_NO_FRAMES"></span><span id="pix_e_no_frames"></span>**PIX \_ E \_ aucune \_ trame**</span><span class="sxs-lookup"><span data-stu-id="522c2-137"><span id="PIX_E_NO_FRAMES"></span><span id="pix_e_no_frames"></span>**PIX\_E\_NO\_FRAMES**</span></span>  
<span data-ttu-id="522c2-138">HRESULT personnalisé qui indique qu’aucun frame n’a été capturé.</span><span class="sxs-lookup"><span data-stu-id="522c2-138">A custom HRESULT which indicates that no frames have been captured.</span></span>

<span data-ttu-id="522c2-139"><span id="PIX_E_DISABLE_SPY"></span><span id="pix_e_disable_spy"></span>**PIX \_ E \_ désactiver \_ Spy**</span><span class="sxs-lookup"><span data-stu-id="522c2-139"><span id="PIX_E_DISABLE_SPY"></span><span id="pix_e_disable_spy"></span>**PIX\_E\_DISABLE\_SPY**</span></span>  

<span data-ttu-id="522c2-140"><span id="PIX_E_WIN8LOG_ON_WIN7"></span><span id="pix_e_win8log_on_win7"></span>**PIX \_ E \_ WIN8LOG \_ sur \_ win7**</span><span class="sxs-lookup"><span data-stu-id="522c2-140"><span id="PIX_E_WIN8LOG_ON_WIN7"></span><span id="pix_e_win8log_on_win7"></span>**PIX\_E\_WIN8LOG\_ON\_WIN7**</span></span>  
<span data-ttu-id="522c2-141">HRESULT personnalisé qui indique qu’un vsglog Windows 8 ne peut pas être lu sur Windows 7.</span><span class="sxs-lookup"><span data-stu-id="522c2-141">A custom HRESULT which indicates that a Windows 8 vsglog cannot be played back on Windows 7.</span></span>

<span data-ttu-id="522c2-142"><span id="PIX_E_BUILD_SHADER_TRACE"></span><span id="pix_e_build_shader_trace"></span>**\_trace du \_ \_ nuanceur de nuance pix E \_**</span><span class="sxs-lookup"><span data-stu-id="522c2-142"><span id="PIX_E_BUILD_SHADER_TRACE"></span><span id="pix_e_build_shader_trace"></span>**PIX\_E\_BUILD\_SHADER\_TRACE**</span></span>  
<span data-ttu-id="522c2-143">HRESULT personnalisé qui indique qu’une erreur s’est produite lors de la création de la trace du nuanceur.</span><span class="sxs-lookup"><span data-stu-id="522c2-143">A custom HRESULT which indicates that there was an error building the shader trace.</span></span>

<span data-ttu-id="522c2-144"><span id="PIX_E_NO_CS_DATA_VISUALIZATION"></span><span id="pix_e_no_cs_data_visualization"></span>**PIX \_ E \_ aucune \_ \_ visualisation des données cs \_**</span><span class="sxs-lookup"><span data-stu-id="522c2-144"><span id="PIX_E_NO_CS_DATA_VISUALIZATION"></span><span id="pix_e_no_cs_data_visualization"></span>**PIX\_E\_NO\_CS\_DATA\_VISUALIZATION**</span></span>  
<span data-ttu-id="522c2-145">HRESULT personnalisé qui indique qu’il n’existe aucune visualisation des données de nuanceur de calcul.</span><span class="sxs-lookup"><span data-stu-id="522c2-145">A custom HRESULT which indicates that there is no compute shader data visualization.</span></span>

<span data-ttu-id="522c2-146"><span id="PIX_E_MISMATCH_SDK"></span><span id="pix_e_mismatch_sdk"></span>**\_SDK pix E \_ incompatibilité \_**</span><span class="sxs-lookup"><span data-stu-id="522c2-146"><span id="PIX_E_MISMATCH_SDK"></span><span id="pix_e_mismatch_sdk"></span>**PIX\_E\_MISMATCH\_SDK**</span></span>  
<span data-ttu-id="522c2-147">HRESULT personnalisé qui indique qu’il existe une incompatibilité avec le kit de développement logiciel (SDK) actuel.</span><span class="sxs-lookup"><span data-stu-id="522c2-147">A custom HRESULT which indicates that there is a mismatch with the current SDK.</span></span>

<span data-ttu-id="522c2-148"><span id="PIX_E_POSSIBLE_MISMATCH_SDK"></span><span id="pix_e_possible_mismatch_sdk"></span>**le \_ \_ Kit de \_ \_ développement logiciel (SDK) pix est possible**</span><span class="sxs-lookup"><span data-stu-id="522c2-148"><span id="PIX_E_POSSIBLE_MISMATCH_SDK"></span><span id="pix_e_possible_mismatch_sdk"></span>**PIX\_E\_POSSIBLE\_MISMATCH\_SDK**</span></span>  
<span data-ttu-id="522c2-149">HRESULT personnalisé qui indique qu’il existe une discordance possible avec le kit de développement logiciel (SDK) actuel.</span><span class="sxs-lookup"><span data-stu-id="522c2-149">A custom HRESULT which indicates that there is a possible mismatch with the current SDK.</span></span>

<span data-ttu-id="522c2-150"><span id="PIX_E_UNDETECTABLE_PIXEL"></span><span id="pix_e_undetectable_pixel"></span>**PIX \_ E \_ Pixel non détectable \_**</span><span class="sxs-lookup"><span data-stu-id="522c2-150"><span id="PIX_E_UNDETECTABLE_PIXEL"></span><span id="pix_e_undetectable_pixel"></span>**PIX\_E\_UNDETECTABLE\_PIXEL**</span></span>  
<span data-ttu-id="522c2-151">HRESULT personnalisé qui indique qu’il existe un pixel non détectable.</span><span class="sxs-lookup"><span data-stu-id="522c2-151">A custom HRESULT which indicates that there is an undetectable pixel.</span></span>

<span data-ttu-id="522c2-152"><span id="PIX_E_CANT_DEBUG_SHADER_USING_SYSTEM_VALUE_SEMANTICS"></span><span id="pix_e_cant_debug_shader_using_system_value_semantics"></span>**PIX \_ E ne pas \_ \_ déboguer le \_ nuanceur \_ à l’aide de la \_ sémantique de \_ valeur système \_**</span><span class="sxs-lookup"><span data-stu-id="522c2-152"><span id="PIX_E_CANT_DEBUG_SHADER_USING_SYSTEM_VALUE_SEMANTICS"></span><span id="pix_e_cant_debug_shader_using_system_value_semantics"></span>**PIX\_E\_CANT\_DEBUG\_SHADER\_USING\_SYSTEM\_VALUE\_SEMANTICS**</span></span>  
<span data-ttu-id="522c2-153">HRESULT personnalisé qui indique que le Sahder ne peut pas être débogué à l’aide de la sémantique de valeur système.</span><span class="sxs-lookup"><span data-stu-id="522c2-153">A custom HRESULT which indicates that the sahder can't be debugged using system value semantics.</span></span>

<span data-ttu-id="522c2-154"><span id="PIX_S_UPDATEAVAILABLE"></span><span id="pix_s_updateavailable"></span>**PIX \_ S \_ UPDATEAVAILABLE**</span><span class="sxs-lookup"><span data-stu-id="522c2-154"><span id="PIX_S_UPDATEAVAILABLE"></span><span id="pix_s_updateavailable"></span>**PIX\_S\_UPDATEAVAILABLE**</span></span>  
<span data-ttu-id="522c2-155">HRESULT personnalisé qui indique qu’une mise à jour est disponible.</span><span class="sxs-lookup"><span data-stu-id="522c2-155">A custom HRESULT which indicates that there is an update available.</span></span>

<span data-ttu-id="522c2-156"><span id="PIX_DXGI_STATUS_NO_REDIRECTION"></span><span id="pix_dxgi_status_no_redirection"></span>**État de dxgi PIX- \_ \_ \_ aucune \_ redirection**</span><span class="sxs-lookup"><span data-stu-id="522c2-156"><span id="PIX_DXGI_STATUS_NO_REDIRECTION"></span><span id="pix_dxgi_status_no_redirection"></span>**PIX\_DXGI\_STATUS\_NO\_REDIRECTION**</span></span>  
<span data-ttu-id="522c2-157">HRESULT personnalisé qui renvoie DXGI \_ Status \_ no \_ redirection.</span><span class="sxs-lookup"><span data-stu-id="522c2-157">A custom HRESULT that echos DXGI\_STATUS\_NO\_REDIRECTION.</span></span>

<span data-ttu-id="522c2-158"><span id="PIX_DXGI_STATUS_NO_DESKTOP_ACCESS"></span><span id="pix_dxgi_status_no_desktop_access"></span>**État de dxgi PIX- \_ \_ \_ aucun \_ \_ accès au bureau**</span><span class="sxs-lookup"><span data-stu-id="522c2-158"><span id="PIX_DXGI_STATUS_NO_DESKTOP_ACCESS"></span><span id="pix_dxgi_status_no_desktop_access"></span>**PIX\_DXGI\_STATUS\_NO\_DESKTOP\_ACCESS**</span></span>  
<span data-ttu-id="522c2-159">HRESULT personnalisé qui renvoie DXGI \_ Status \_ no \_ Desktop \_ Access.</span><span class="sxs-lookup"><span data-stu-id="522c2-159">A custom HRESULT that echos DXGI\_STATUS\_NO\_DESKTOP\_ACCESS.</span></span>

<span data-ttu-id="522c2-160"><span id="PIX_DXGI_STATUS_GRAPHICS_VIDPN_SOURCE_IN_USE"></span><span id="pix_dxgi_status_graphics_vidpn_source_in_use"></span>**\_ \_ \_ image de la source VIDPN Graphics de l’État dxgi pix \_ \_ \_ en cours d' \_ utilisation**</span><span class="sxs-lookup"><span data-stu-id="522c2-160"><span id="PIX_DXGI_STATUS_GRAPHICS_VIDPN_SOURCE_IN_USE"></span><span id="pix_dxgi_status_graphics_vidpn_source_in_use"></span>**PIX\_DXGI\_STATUS\_GRAPHICS\_VIDPN\_SOURCE\_IN\_USE**</span></span>  
<span data-ttu-id="522c2-161">HRESULT personnalisé qui renvoie la \_ \_ source VIDPN Graphics dxgi status \_ \_ \_ \_ use.</span><span class="sxs-lookup"><span data-stu-id="522c2-161">A custom HRESULT that echos DXGI\_STATUS\_GRAPHICS\_VIDPN\_SOURCE\_IN\_USE.</span></span>

<span data-ttu-id="522c2-162"><span id="PIX_DXGI_STATUS_MODE_CHANGED"></span><span id="pix_dxgi_status_mode_changed"></span>**\_mode d' \_ État dxgi pix \_ \_ modifié**</span><span class="sxs-lookup"><span data-stu-id="522c2-162"><span id="PIX_DXGI_STATUS_MODE_CHANGED"></span><span id="pix_dxgi_status_mode_changed"></span>**PIX\_DXGI\_STATUS\_MODE\_CHANGED**</span></span>  
<span data-ttu-id="522c2-163">HRESULT personnalisé qui renvoie le \_ mode d’État dxgi \_ \_ modifié.</span><span class="sxs-lookup"><span data-stu-id="522c2-163">A custom HRESULT that echos DXGI\_STATUS\_MODE\_CHANGED.</span></span>

<span data-ttu-id="522c2-164"><span id="PIX_DXGI_STATUS_MODE_CHANGE_IN_PROGRESS"></span><span id="pix_dxgi_status_mode_change_in_progress"></span>**\_ \_ \_ modification du mode d’État dxgi pix \_ \_ en \_ cours**</span><span class="sxs-lookup"><span data-stu-id="522c2-164"><span id="PIX_DXGI_STATUS_MODE_CHANGE_IN_PROGRESS"></span><span id="pix_dxgi_status_mode_change_in_progress"></span>**PIX\_DXGI\_STATUS\_MODE\_CHANGE\_IN\_PROGRESS**</span></span>  
<span data-ttu-id="522c2-165">HRESULT personnalisé qui renvoie le \_ \_ mode d’État dxgi \_ change \_ en \_ cours.</span><span class="sxs-lookup"><span data-stu-id="522c2-165">A custom HRESULT that echos DXGI\_STATUS\_MODE\_CHANGE\_IN\_PROGRESS.</span></span>

<span data-ttu-id="522c2-166"><span id="PIX_DXGI_STATUS_UNOCCLUDED"></span><span id="pix_dxgi_status_unoccluded"></span>**\_État dxgi \_ pix \_ UNOCCLUDED**</span><span class="sxs-lookup"><span data-stu-id="522c2-166"><span id="PIX_DXGI_STATUS_UNOCCLUDED"></span><span id="pix_dxgi_status_unoccluded"></span>**PIX\_DXGI\_STATUS\_UNOCCLUDED**</span></span>  
<span data-ttu-id="522c2-167">HRESULT personnalisé qui renvoie DXGI \_ Status \_ UNOCCLUDED.</span><span class="sxs-lookup"><span data-stu-id="522c2-167">A custom HRESULT that echos DXGI\_STATUS\_UNOCCLUDED.</span></span>

<span data-ttu-id="522c2-168"><span id="PIX_DXGI_STATUS_DDA_WAS_STILL_DRAWING"></span><span id="pix_dxgi_status_dda_was_still_drawing"></span>**État de PIX \_ dxgi le \_ \_ DDA \_ est \_ encore \_ en cours de dessin**</span><span class="sxs-lookup"><span data-stu-id="522c2-168"><span id="PIX_DXGI_STATUS_DDA_WAS_STILL_DRAWING"></span><span id="pix_dxgi_status_dda_was_still_drawing"></span>**PIX\_DXGI\_STATUS\_DDA\_WAS\_STILL\_DRAWING**</span></span>  
<span data-ttu-id="522c2-169">HRESULT personnalisé sur lequel renvoie DXGI \_ Status \_ \_ a \_ encore été \_ dessiné.</span><span class="sxs-lookup"><span data-stu-id="522c2-169">A custom HRESULT that echos DXGI\_STATUS\_DDA\_WAS\_STILL\_DRAWING.</span></span>

<span data-ttu-id="522c2-170"><span id="PIX_E_NOTIMPL"></span><span id="pix_e_notimpl"></span>**\_NOTIMPL pix \_**</span><span class="sxs-lookup"><span data-stu-id="522c2-170"><span id="PIX_E_NOTIMPL"></span><span id="pix_e_notimpl"></span>**PIX\_E\_NOTIMPL**</span></span>  
<span data-ttu-id="522c2-171">HRESULT personnalisé qui renvoie E \_ NOTIMPL.</span><span class="sxs-lookup"><span data-stu-id="522c2-171">A custom HRESULT that echos E\_NOTIMPL.</span></span>

<span data-ttu-id="522c2-172"><span id="PIX_E_NOINTERFACE"></span><span id="pix_e_nointerface"></span>**PIX \_ E \_ nointerface**</span><span class="sxs-lookup"><span data-stu-id="522c2-172"><span id="PIX_E_NOINTERFACE"></span><span id="pix_e_nointerface"></span>**PIX\_E\_NOINTERFACE**</span></span>  
<span data-ttu-id="522c2-173">HRESULT personnalisé qui renvoie E \_ nointerface.</span><span class="sxs-lookup"><span data-stu-id="522c2-173">A custom HRESULT that echos E\_NOINTERFACE.</span></span>

<span data-ttu-id="522c2-174"><span id="PIX_E_POINTER"></span><span id="pix_e_pointer"></span>**\_pointeur pix E \_**</span><span class="sxs-lookup"><span data-stu-id="522c2-174"><span id="PIX_E_POINTER"></span><span id="pix_e_pointer"></span>**PIX\_E\_POINTER**</span></span>  
<span data-ttu-id="522c2-175">HRESULT personnalisé qui renvoie pointeur E \_ .</span><span class="sxs-lookup"><span data-stu-id="522c2-175">A custom HRESULT that echos E\_POINTER.</span></span>

<span data-ttu-id="522c2-176"><span id="PIX_E_ABORT"></span><span id="pix_e_abort"></span>**\_abandonner pix \_**</span><span class="sxs-lookup"><span data-stu-id="522c2-176"><span id="PIX_E_ABORT"></span><span id="pix_e_abort"></span>**PIX\_E\_ABORT**</span></span>  
<span data-ttu-id="522c2-177">HRESULT personnalisé qui renvoie E \_ Abort.</span><span class="sxs-lookup"><span data-stu-id="522c2-177">A custom HRESULT that echos E\_ABORT.</span></span>

<span data-ttu-id="522c2-178"><span id="PIX_E_FAIL"></span><span id="pix_e_fail"></span>**échec de PIX \_ E \_**</span><span class="sxs-lookup"><span data-stu-id="522c2-178"><span id="PIX_E_FAIL"></span><span id="pix_e_fail"></span>**PIX\_E\_FAIL**</span></span>  
<span data-ttu-id="522c2-179">Un HRESULT personnalisé qui renvoie E \_ échoue.</span><span class="sxs-lookup"><span data-stu-id="522c2-179">A custom HRESULT that echos E\_FAIL.</span></span>

<span data-ttu-id="522c2-180"><span id="PIX_E_UNEXPECTED"></span><span id="pix_e_unexpected"></span>**PIX \_ E \_ inattendu**</span><span class="sxs-lookup"><span data-stu-id="522c2-180"><span id="PIX_E_UNEXPECTED"></span><span id="pix_e_unexpected"></span>**PIX\_E\_UNEXPECTED**</span></span>  
<span data-ttu-id="522c2-181">HRESULT personnalisé qui renvoie E \_ inattendu.</span><span class="sxs-lookup"><span data-stu-id="522c2-181">A custom HRESULT that echos E\_UNEXPECTED.</span></span>

<span data-ttu-id="522c2-182"><span id="PIX_E_ACCESSDENIED"></span><span id="pix_e_accessdenied"></span>**\_ACCESSDENIED pix \_**</span><span class="sxs-lookup"><span data-stu-id="522c2-182"><span id="PIX_E_ACCESSDENIED"></span><span id="pix_e_accessdenied"></span>**PIX\_E\_ACCESSDENIED**</span></span>  
<span data-ttu-id="522c2-183">HRESULT personnalisé qui renvoie E \_ ACCESSDENIED.</span><span class="sxs-lookup"><span data-stu-id="522c2-183">A custom HRESULT that echos E\_ACCESSDENIED.</span></span>

<span data-ttu-id="522c2-184"><span id="PIX_E_HANDLE"></span><span id="pix_e_handle"></span>**\_handle pix E \_**</span><span class="sxs-lookup"><span data-stu-id="522c2-184"><span id="PIX_E_HANDLE"></span><span id="pix_e_handle"></span>**PIX\_E\_HANDLE**</span></span>  
<span data-ttu-id="522c2-185">HRESULT personnalisé qui renvoie E \_ .</span><span class="sxs-lookup"><span data-stu-id="522c2-185">A custom HRESULT that echos E\_HANDLE.</span></span>

<span data-ttu-id="522c2-186"><span id="PIX_E_OUTOFMEMORY"></span><span id="pix_e_outofmemory"></span>**\_OUTOFMEMORY pix \_**</span><span class="sxs-lookup"><span data-stu-id="522c2-186"><span id="PIX_E_OUTOFMEMORY"></span><span id="pix_e_outofmemory"></span>**PIX\_E\_OUTOFMEMORY**</span></span>  
<span data-ttu-id="522c2-187">HRESULT personnalisé qui renvoie E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="522c2-187">A custom HRESULT that echos E\_OUTOFMEMORY.</span></span>

<span data-ttu-id="522c2-188"><span id="PIX_E_INVALIDARG"></span><span id="pix_e_invalidarg"></span>**PIX \_ E \_ INVALIDARG**</span><span class="sxs-lookup"><span data-stu-id="522c2-188"><span id="PIX_E_INVALIDARG"></span><span id="pix_e_invalidarg"></span>**PIX\_E\_INVALIDARG**</span></span>  
<span data-ttu-id="522c2-189">HRESULT personnalisé qui renvoie E \_ INVALIDARG.</span><span class="sxs-lookup"><span data-stu-id="522c2-189">A custom HRESULT that echos E\_INVALIDARG.</span></span>

<span data-ttu-id="522c2-190"><span id="PIX_XBOX_ERROR_DISK_FULL"></span><span id="pix_xbox_error_disk_full"></span>**\_disque d' \_ erreur Xbox pix \_ \_ plein**</span><span class="sxs-lookup"><span data-stu-id="522c2-190"><span id="PIX_XBOX_ERROR_DISK_FULL"></span><span id="pix_xbox_error_disk_full"></span>**PIX\_XBOX\_ERROR\_DISK\_FULL**</span></span>  
<span data-ttu-id="522c2-191">HRESULT personnalisé qui indique que le disque est plein.</span><span class="sxs-lookup"><span data-stu-id="522c2-191">A custom HRESULT which indicates that the disk is full.</span></span>

<span data-ttu-id="522c2-192"><span id="PIX_WS_E_ADDRESS_IN_USE"></span><span id="pix_ws_e_address_in_use"></span>**\_adresse pix \_ WS \_ E \_ en cours d' \_ utilisation**</span><span class="sxs-lookup"><span data-stu-id="522c2-192"><span id="PIX_WS_E_ADDRESS_IN_USE"></span><span id="pix_ws_e_address_in_use"></span>**PIX\_WS\_E\_ADDRESS\_IN\_USE**</span></span>  
<span data-ttu-id="522c2-193">HRESULT personnalisé qui indique que l’adresse est déjà utilisée.</span><span class="sxs-lookup"><span data-stu-id="522c2-193">A custom HRESULT which indicates that the address is already in use.</span></span>

<span data-ttu-id="522c2-194"><span id="PIX_WS_E_MISSING_KITS_POLICY"></span><span id="pix_ws_e_missing_kits_policy"></span>**\_stratégie des kits pix WS \_ E \_ manquant \_ \_**</span><span class="sxs-lookup"><span data-stu-id="522c2-194"><span id="PIX_WS_E_MISSING_KITS_POLICY"></span><span id="pix_ws_e_missing_kits_policy"></span>**PIX\_WS\_E\_MISSING\_KITS\_POLICY**</span></span>  
<span data-ttu-id="522c2-195">HRESULT personnalisé qui indique que l’adresse n’est pas disponible.</span><span class="sxs-lookup"><span data-stu-id="522c2-195">A custom HRESULT which indicates that the address is not available.</span></span>

<span data-ttu-id="522c2-196"><span id="PIX_TE_FAILEDTOLOADSOFTWAREMODULE"></span><span id="pix_te_failedtoloadsoftwaremodule"></span>**\_FAILEDTOLOADSOFTWAREMODULE pix \_**</span><span class="sxs-lookup"><span data-stu-id="522c2-196"><span id="PIX_TE_FAILEDTOLOADSOFTWAREMODULE"></span><span id="pix_te_failedtoloadsoftwaremodule"></span>**PIX\_TE\_FAILEDTOLOADSOFTWAREMODULE**</span></span>  
<span data-ttu-id="522c2-197">HRESULT personnalisé qui indique qu’un module logiciel nécessaire n’a pas pu se charger.</span><span class="sxs-lookup"><span data-stu-id="522c2-197">A custom HRESULT which indicates that a necessary software module failed to load.</span></span>

<span data-ttu-id="522c2-198"><span id="PIX_TE_USEDSOFTWAREMODULETHATWASNTWARPORREF"></span><span id="pix_te_usedsoftwaremodulethatwasntwarporref"></span>**\_USEDSOFTWAREMODULETHATWASNTWARPORREF pix \_**</span><span class="sxs-lookup"><span data-stu-id="522c2-198"><span id="PIX_TE_USEDSOFTWAREMODULETHATWASNTWARPORREF"></span><span id="pix_te_usedsoftwaremodulethatwasntwarporref"></span>**PIX\_TE\_USEDSOFTWAREMODULETHATWASNTWARPORREF**</span></span>  
<span data-ttu-id="522c2-199">HRESULT personnalisé qui indique que le module de logiciel utilisé n’était pas le pilote WARP ou REF.</span><span class="sxs-lookup"><span data-stu-id="522c2-199">A custom HRESULT which indicates that the used software module was not the WARP or REF driver.</span></span>

<span data-ttu-id="522c2-200"><span id="PIX_TE_CORRUPTEDFILE"></span><span id="pix_te_corruptedfile"></span>**\_CORRUPTEDFILE pix \_**</span><span class="sxs-lookup"><span data-stu-id="522c2-200"><span id="PIX_TE_CORRUPTEDFILE"></span><span id="pix_te_corruptedfile"></span>**PIX\_TE\_CORRUPTEDFILE**</span></span>  
<span data-ttu-id="522c2-201">HRESULT personnalisé qui indique que le fichier est endommagé.</span><span class="sxs-lookup"><span data-stu-id="522c2-201">A custom HRESULT which indicates that the file is corrupted.</span></span>

<span data-ttu-id="522c2-202"><span id="PIX_TE_FAILEDTOOPENFILE"></span><span id="pix_te_failedtoopenfile"></span>**\_FAILEDTOOPENFILE pix \_**</span><span class="sxs-lookup"><span data-stu-id="522c2-202"><span id="PIX_TE_FAILEDTOOPENFILE"></span><span id="pix_te_failedtoopenfile"></span>**PIX\_TE\_FAILEDTOOPENFILE**</span></span>  
<span data-ttu-id="522c2-203">HRESULT personnalisé qui indique que le fichier n’a pas pu s’ouvrir.</span><span class="sxs-lookup"><span data-stu-id="522c2-203">A custom HRESULT which indicates that the file failed to open.</span></span>

<span data-ttu-id="522c2-204"><span id="PIX_TE_CALLFAILEDONPLAYBACK"></span><span id="pix_te_callfailedonplayback"></span>**\_CALLFAILEDONPLAYBACK pix \_**</span><span class="sxs-lookup"><span data-stu-id="522c2-204"><span id="PIX_TE_CALLFAILEDONPLAYBACK"></span><span id="pix_te_callfailedonplayback"></span>**PIX\_TE\_CALLFAILEDONPLAYBACK**</span></span>  
<span data-ttu-id="522c2-205">HRESULT personnalisé qui indique qu’un appel a échoué lors de la lecture.</span><span class="sxs-lookup"><span data-stu-id="522c2-205">A custom HRESULT which indicates that a call failed during playback.</span></span>

<span data-ttu-id="522c2-206"><span id="PIX_TE_UNKNOWNUUID"></span><span id="pix_te_unknownuuid"></span>**\_UNKNOWNUUID pix \_**</span><span class="sxs-lookup"><span data-stu-id="522c2-206"><span id="PIX_TE_UNKNOWNUUID"></span><span id="pix_te_unknownuuid"></span>**PIX\_TE\_UNKNOWNUUID**</span></span>  
<span data-ttu-id="522c2-207">HRESULT personnalisé qui indique qu’un UUID inconnu a été rencontré ; Cela ne doit jamais se produire.</span><span class="sxs-lookup"><span data-stu-id="522c2-207">A custom HRESULT which indicates that an unknown UUID was encountered; this should never occur.</span></span>

<span data-ttu-id="522c2-208"><span id="PIX_TE_NOTCAPTUREFILEORCORRUPTED"></span><span id="pix_te_notcapturefileorcorrupted"></span>**\_NOTCAPTUREFILEORCORRUPTED pix \_**</span><span class="sxs-lookup"><span data-stu-id="522c2-208"><span id="PIX_TE_NOTCAPTUREFILEORCORRUPTED"></span><span id="pix_te_notcapturefileorcorrupted"></span>**PIX\_TE\_NOTCAPTUREFILEORCORRUPTED**</span></span>  
<span data-ttu-id="522c2-209">HRESULT personnalisé qui indique que le fichier n’est pas un fichier de capture ou est endommagé.</span><span class="sxs-lookup"><span data-stu-id="522c2-209">A custom HRESULT which indicates that the file is not a capture file or is corrupted.</span></span>

<span data-ttu-id="522c2-210"><span id="PIX_TE_NEWERFILE"></span><span id="pix_te_newerfile"></span>**\_NEWERFILE pix \_**</span><span class="sxs-lookup"><span data-stu-id="522c2-210"><span id="PIX_TE_NEWERFILE"></span><span id="pix_te_newerfile"></span>**PIX\_TE\_NEWERFILE**</span></span>  

<span data-ttu-id="522c2-211"><span id="PIX_TE_OLDERFILE"></span><span id="pix_te_olderfile"></span>**\_OLDERFILE pix \_**</span><span class="sxs-lookup"><span data-stu-id="522c2-211"><span id="PIX_TE_OLDERFILE"></span><span id="pix_te_olderfile"></span>**PIX\_TE\_OLDERFILE**</span></span>  

<span data-ttu-id="522c2-212"><span id="PIX_TE_INVALIDMOMENT"></span><span id="pix_te_invalidmoment"></span>**\_INVALIDMOMENT pix \_**</span><span class="sxs-lookup"><span data-stu-id="522c2-212"><span id="PIX_TE_INVALIDMOMENT"></span><span id="pix_te_invalidmoment"></span>**PIX\_TE\_INVALIDMOMENT**</span></span>  

<span data-ttu-id="522c2-213"><span id="PIX_TE_BAD_DRIVER"></span><span id="pix_te_bad_driver"></span>**lecteur PIX- \_ \_ pilote incorrect \_**</span><span class="sxs-lookup"><span data-stu-id="522c2-213"><span id="PIX_TE_BAD_DRIVER"></span><span id="pix_te_bad_driver"></span>**PIX\_TE\_BAD\_DRIVER**</span></span>  
<span data-ttu-id="522c2-214">HRESULT personnalisé qui indique que le pilote est incorrect.</span><span class="sxs-lookup"><span data-stu-id="522c2-214">A custom HRESULT which indicates that the driver is bad.</span></span>

<span data-ttu-id="522c2-215"><span id="PIX_ERROR_CANT_ACCESS_DEPTHSTENCIL_IN_CPU"></span><span id="pix_error_cant_access_depthstencil_in_cpu"></span>**\_erreur pix \_ Impossible \_ \_ d’accéder \_ à DEPTHSTENCIL dans le \_ processeur**</span><span class="sxs-lookup"><span data-stu-id="522c2-215"><span id="PIX_ERROR_CANT_ACCESS_DEPTHSTENCIL_IN_CPU"></span><span id="pix_error_cant_access_depthstencil_in_cpu"></span>**PIX\_ERROR\_CANT\_ACCESS\_DEPTHSTENCIL\_IN\_CPU**</span></span>  
<span data-ttu-id="522c2-216">HRESULT personnalisé qui indique que l’UC a tenté d’accéder à la mémoire tampon du stencil de profondeur, provoquant une erreur.</span><span class="sxs-lookup"><span data-stu-id="522c2-216">A custom HRESULT which indicates that the CPU attempted to access the depth-stencil buffer, resulting in an error.</span></span>

<span data-ttu-id="522c2-217"><span id="PIX_ERROR_CANT_RESOLVE_MULTISAMPLED_TEXTURE"></span><span id="pix_error_cant_resolve_multisampled_texture"></span>**\_erreur pix \_ Impossible de résoudre la \_ texture à \_ échantillonnages \_**</span><span class="sxs-lookup"><span data-stu-id="522c2-217"><span id="PIX_ERROR_CANT_RESOLVE_MULTISAMPLED_TEXTURE"></span><span id="pix_error_cant_resolve_multisampled_texture"></span>**PIX\_ERROR\_CANT\_RESOLVE\_MULTISAMPLED\_TEXTURE**</span></span>  
<span data-ttu-id="522c2-218">HRESULT personnalisé qui indique qu’il y a eu une tentative de résolution d’une texture à échantillonnage multiple, provoquant une erreur.</span><span class="sxs-lookup"><span data-stu-id="522c2-218">A custom HRESULT which indicates that there was an attempt to resolve a multi-sampled texture, resulting in an error.</span></span>

<span data-ttu-id="522c2-219"><span id="PIX_DXGI_ERROR_INVALID_CALL"></span><span id="pix_dxgi_error_invalid_call"></span>**\_erreur dxgi de l' \_ \_ appel non valide \_**</span><span class="sxs-lookup"><span data-stu-id="522c2-219"><span id="PIX_DXGI_ERROR_INVALID_CALL"></span><span id="pix_dxgi_error_invalid_call"></span>**PIX\_DXGI\_ERROR\_INVALID\_CALL**</span></span>  
<span data-ttu-id="522c2-220">HRESULT personnalisé qui renvoie DXGI \_ erreur d' \_ appel non valide \_ .</span><span class="sxs-lookup"><span data-stu-id="522c2-220">A custom HRESULT that echos DXGI\_ERROR\_INVALID\_CALL.</span></span>

<span data-ttu-id="522c2-221"><span id="PIX_DXGI_ERROR_NOT_FOUND"></span><span id="pix_dxgi_error_not_found"></span>**\_erreur dxgi \_ pix \_ \_ introuvable**</span><span class="sxs-lookup"><span data-stu-id="522c2-221"><span id="PIX_DXGI_ERROR_NOT_FOUND"></span><span id="pix_dxgi_error_not_found"></span>**PIX\_DXGI\_ERROR\_NOT\_FOUND**</span></span>  
<span data-ttu-id="522c2-222">HRESULT personnalisé qui renvoie DXGI \_ erreur \_ \_ introuvable.</span><span class="sxs-lookup"><span data-stu-id="522c2-222">A custom HRESULT that echos DXGI\_ERROR\_NOT\_FOUND.</span></span>

<span data-ttu-id="522c2-223"><span id="PIX_DXGI_ERROR_MORE_DATA"></span><span id="pix_dxgi_error_more_data"></span>**\_erreur dxgi \_ de \_ plus \_ données dans pix**</span><span class="sxs-lookup"><span data-stu-id="522c2-223"><span id="PIX_DXGI_ERROR_MORE_DATA"></span><span id="pix_dxgi_error_more_data"></span>**PIX\_DXGI\_ERROR\_MORE\_DATA**</span></span>  
<span data-ttu-id="522c2-224">HRESULT personnalisé qui renvoie DXGI \_ erreur \_ plus de \_ données.</span><span class="sxs-lookup"><span data-stu-id="522c2-224">A custom HRESULT that echos DXGI\_ERROR\_MORE\_DATA.</span></span>

<span data-ttu-id="522c2-225"><span id="PIX_DXGI_ERROR_UNSUPPORTED"></span><span id="pix_dxgi_error_unsupported"></span>**\_erreur dxgi \_ pix \_ non prise en charge**</span><span class="sxs-lookup"><span data-stu-id="522c2-225"><span id="PIX_DXGI_ERROR_UNSUPPORTED"></span><span id="pix_dxgi_error_unsupported"></span>**PIX\_DXGI\_ERROR\_UNSUPPORTED**</span></span>  
<span data-ttu-id="522c2-226">HRESULT personnalisé qui ne \_ \_ prend pas en charge l’erreur renvoie DXGI.</span><span class="sxs-lookup"><span data-stu-id="522c2-226">A custom HRESULT that echos DXGI\_ERROR\_UNSUPPORTED.</span></span>

<span data-ttu-id="522c2-227"><span id="PIX_DXGI_ERROR_DEVICE_REMOVED"></span><span id="pix_dxgi_error_device_removed"></span>**\_périphérique d' \_ erreur pix dxgi \_ \_ supprimé**</span><span class="sxs-lookup"><span data-stu-id="522c2-227"><span id="PIX_DXGI_ERROR_DEVICE_REMOVED"></span><span id="pix_dxgi_error_device_removed"></span>**PIX\_DXGI\_ERROR\_DEVICE\_REMOVED**</span></span>  
<span data-ttu-id="522c2-228">HRESULT personnalisé qui renvoie l' \_ appareil d’erreur dxgi \_ \_ supprimé.</span><span class="sxs-lookup"><span data-stu-id="522c2-228">A custom HRESULT that echos DXGI\_ERROR\_DEVICE\_REMOVED.</span></span>

<span data-ttu-id="522c2-229"><span id="PIX_DXGI_ERROR_DEVICE_HUNG"></span><span id="pix_dxgi_error_device_hung"></span>**\_périphérique d' \_ erreur pix dxgi \_ \_ bloqué**</span><span class="sxs-lookup"><span data-stu-id="522c2-229"><span id="PIX_DXGI_ERROR_DEVICE_HUNG"></span><span id="pix_dxgi_error_device_hung"></span>**PIX\_DXGI\_ERROR\_DEVICE\_HUNG**</span></span>  
<span data-ttu-id="522c2-230">HRESULT personnalisé qui renvoie le \_ blocage du périphérique d’erreur dxgi \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="522c2-230">A custom HRESULT that echos DXGI\_ERROR\_DEVICE\_HUNG.</span></span>

<span data-ttu-id="522c2-231"><span id="PIX_DXGI_ERROR_DEVICE_RESET"></span><span id="pix_dxgi_error_device_reset"></span>**\_erreur de \_ \_ \_ réinitialisation de l’appareil pix dxgi**</span><span class="sxs-lookup"><span data-stu-id="522c2-231"><span id="PIX_DXGI_ERROR_DEVICE_RESET"></span><span id="pix_dxgi_error_device_reset"></span>**PIX\_DXGI\_ERROR\_DEVICE\_RESET**</span></span>  
<span data-ttu-id="522c2-232">HRESULT personnalisé qui renvoie la \_ \_ réinitialisation de l’appareil d’erreur dxgi \_ .</span><span class="sxs-lookup"><span data-stu-id="522c2-232">A custom HRESULT that echos DXGI\_ERROR\_DEVICE\_RESET.</span></span>

<span data-ttu-id="522c2-233"><span id="PIX_DXGI_ERROR_WAS_STILL_DRAWING"></span><span id="pix_dxgi_error_was_still_drawing"></span>**l' \_ erreur dxgi pix \_ \_ est \_ encore en cours de \_ dessin**</span><span class="sxs-lookup"><span data-stu-id="522c2-233"><span id="PIX_DXGI_ERROR_WAS_STILL_DRAWING"></span><span id="pix_dxgi_error_was_still_drawing"></span>**PIX\_DXGI\_ERROR\_WAS\_STILL\_DRAWING**</span></span>  
<span data-ttu-id="522c2-234">Un HRESULT personnalisé qui renvoie l' \_ erreur dxgi était encore en cours de \_ \_ \_ dessin.</span><span class="sxs-lookup"><span data-stu-id="522c2-234">A custom HRESULT that echos DXGI\_ERROR\_WAS\_STILL\_DRAWING.</span></span>

<span data-ttu-id="522c2-235"><span id="PIX_DXGI_ERROR_FRAME_STATISTICS_DISJOINT"></span><span id="pix_dxgi_error_frame_statistics_disjoint"></span>**\_statistiques de \_ trame d’erreur dxgi pix \_ \_ \_ disjointes**</span><span class="sxs-lookup"><span data-stu-id="522c2-235"><span id="PIX_DXGI_ERROR_FRAME_STATISTICS_DISJOINT"></span><span id="pix_dxgi_error_frame_statistics_disjoint"></span>**PIX\_DXGI\_ERROR\_FRAME\_STATISTICS\_DISJOINT**</span></span>  
<span data-ttu-id="522c2-236">HRESULT personnalisé qui renvoie les \_ statistiques de \_ trame d’erreur dxgi \_ \_ disjointes.</span><span class="sxs-lookup"><span data-stu-id="522c2-236">A custom HRESULT that echos DXGI\_ERROR\_FRAME\_STATISTICS\_DISJOINT.</span></span>

<span data-ttu-id="522c2-237"><span id="PIX_DXGI_ERROR_GRAPHICS_VIDPN_SOURCE_IN_USE"></span><span id="pix_dxgi_error_graphics_vidpn_source_in_use"></span>**\_ \_ \_ source VIDPN d’erreur Graphics dxgi \_ \_ \_ en cours d' \_ utilisation**</span><span class="sxs-lookup"><span data-stu-id="522c2-237"><span id="PIX_DXGI_ERROR_GRAPHICS_VIDPN_SOURCE_IN_USE"></span><span id="pix_dxgi_error_graphics_vidpn_source_in_use"></span>**PIX\_DXGI\_ERROR\_GRAPHICS\_VIDPN\_SOURCE\_IN\_USE**</span></span>  
<span data-ttu-id="522c2-238">HRESULT personnalisé qui renvoie la \_ \_ source VIDPN Graphics Error dxgi \_ \_ \_ en cours d' \_ utilisation.</span><span class="sxs-lookup"><span data-stu-id="522c2-238">A custom HRESULT that echos DXGI\_ERROR\_GRAPHICS\_VIDPN\_SOURCE\_IN\_USE.</span></span>

<span data-ttu-id="522c2-239"><span id="PIX_DXGI_ERROR_DRIVER_INTERNAL_ERROR"></span><span id="pix_dxgi_error_driver_internal_error"></span>**\_ \_ \_ erreur interne du pilote d’erreur \_ pix dxgi \_**</span><span class="sxs-lookup"><span data-stu-id="522c2-239"><span id="PIX_DXGI_ERROR_DRIVER_INTERNAL_ERROR"></span><span id="pix_dxgi_error_driver_internal_error"></span>**PIX\_DXGI\_ERROR\_DRIVER\_INTERNAL\_ERROR**</span></span>  
<span data-ttu-id="522c2-240">HRESULT personnalisé qui renvoie DXGI erreur \_ interne du pilote d’erreur \_ \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="522c2-240">A custom HRESULT that echos DXGI\_ERROR\_DRIVER\_INTERNAL\_ERROR.</span></span>

<span data-ttu-id="522c2-241"><span id="PIX_DXGI_ERROR_NONEXCLUSIVE"></span><span id="pix_dxgi_error_nonexclusive"></span>**erreur de dxgi PIX non \_ \_ \_ exclusive**</span><span class="sxs-lookup"><span data-stu-id="522c2-241"><span id="PIX_DXGI_ERROR_NONEXCLUSIVE"></span><span id="pix_dxgi_error_nonexclusive"></span>**PIX\_DXGI\_ERROR\_NONEXCLUSIVE**</span></span>  
<span data-ttu-id="522c2-242">HRESULT personnalisé qui renvoie DXGI \_ erreur non \_ exclusive.</span><span class="sxs-lookup"><span data-stu-id="522c2-242">A custom HRESULT that echos DXGI\_ERROR\_NONEXCLUSIVE.</span></span>

<span data-ttu-id="522c2-243"><span id="PIX_DXGI_ERROR_NOT_CURRENTLY_AVAILABLE"></span><span id="pix_dxgi_error_not_currently_available"></span>**\_erreur de dxgi pix \_ \_ non \_ \_ disponible actuellement**</span><span class="sxs-lookup"><span data-stu-id="522c2-243"><span id="PIX_DXGI_ERROR_NOT_CURRENTLY_AVAILABLE"></span><span id="pix_dxgi_error_not_currently_available"></span>**PIX\_DXGI\_ERROR\_NOT\_CURRENTLY\_AVAILABLE**</span></span>  
<span data-ttu-id="522c2-244">HRESULT personnalisé qui renvoie DXGI \_ erreur \_ non \_ disponible actuellement \_ .</span><span class="sxs-lookup"><span data-stu-id="522c2-244">A custom HRESULT that echos DXGI\_ERROR\_NOT\_CURRENTLY\_AVAILABLE.</span></span>

<span data-ttu-id="522c2-245"><span id="PIX_DXGI_ERROR_REMOTE_CLIENT_DISCONNECTED"></span><span id="pix_dxgi_error_remote_client_disconnected"></span>**\_Erreur du \_ client distant pix dxgi \_ \_ \_ déconnectée**</span><span class="sxs-lookup"><span data-stu-id="522c2-245"><span id="PIX_DXGI_ERROR_REMOTE_CLIENT_DISCONNECTED"></span><span id="pix_dxgi_error_remote_client_disconnected"></span>**PIX\_DXGI\_ERROR\_REMOTE\_CLIENT\_DISCONNECTED**</span></span>  
<span data-ttu-id="522c2-246">HRESULT personnalisé qui renvoie DXGI \_ erreur \_ \_ \_ déconnectée du client distant.</span><span class="sxs-lookup"><span data-stu-id="522c2-246">A custom HRESULT that echos DXGI\_ERROR\_REMOTE\_CLIENT\_DISCONNECTED.</span></span>

<span data-ttu-id="522c2-247"><span id="PIX_DXGI_ERROR_REMOTE_OUTOFMEMORY"></span><span id="pix_dxgi_error_remote_outofmemory"></span>**\_erreur dxgi \_ à distance de pix \_ \_ OUTOFMEMORY**</span><span class="sxs-lookup"><span data-stu-id="522c2-247"><span id="PIX_DXGI_ERROR_REMOTE_OUTOFMEMORY"></span><span id="pix_dxgi_error_remote_outofmemory"></span>**PIX\_DXGI\_ERROR\_REMOTE\_OUTOFMEMORY**</span></span>  
<span data-ttu-id="522c2-248">HRESULT personnalisé qui renvoie DXGI \_ Error \_ OUTOFMEMORY à distance \_ .</span><span class="sxs-lookup"><span data-stu-id="522c2-248">A custom HRESULT that echos DXGI\_ERROR\_REMOTE\_OUTOFMEMORY.</span></span>

<span data-ttu-id="522c2-249"><span id="PIX_DXGI_ERROR_MODE_CHANGE_IN_PROGRESS"></span><span id="pix_dxgi_error_mode_change_in_progress"></span>**\_ \_ \_ modification du mode d’erreur dxgi pix \_ \_ en \_ cours**</span><span class="sxs-lookup"><span data-stu-id="522c2-249"><span id="PIX_DXGI_ERROR_MODE_CHANGE_IN_PROGRESS"></span><span id="pix_dxgi_error_mode_change_in_progress"></span>**PIX\_DXGI\_ERROR\_MODE\_CHANGE\_IN\_PROGRESS**</span></span>  
<span data-ttu-id="522c2-250">HRESULT personnalisé qui renvoie le \_ \_ mode d’erreur dxgi \_ change \_ en \_ cours.</span><span class="sxs-lookup"><span data-stu-id="522c2-250">A custom HRESULT that echos DXGI\_ERROR\_MODE\_CHANGE\_IN\_PROGRESS.</span></span>

<span data-ttu-id="522c2-251"><span id="PIX_DXGI_ERROR_ACCESS_LOST"></span><span id="pix_dxgi_error_access_lost"></span>**\_erreur de \_ \_ perte d’accès dxgi \_ pix**</span><span class="sxs-lookup"><span data-stu-id="522c2-251"><span id="PIX_DXGI_ERROR_ACCESS_LOST"></span><span id="pix_dxgi_error_access_lost"></span>**PIX\_DXGI\_ERROR\_ACCESS\_LOST**</span></span>  
<span data-ttu-id="522c2-252">HRESULT personnalisé qui renvoie \_ l’erreur d' \_ accès dxgi \_ .</span><span class="sxs-lookup"><span data-stu-id="522c2-252">A custom HRESULT that echos DXGI\_ERROR\_ACCESS\_LOST.</span></span>

<span data-ttu-id="522c2-253"><span id="PIX_DXGI_ERROR_WAIT_TIMEOUT"></span><span id="pix_dxgi_error_wait_timeout"></span>**\_ \_ \_ \_ délai d’attente d’erreur dxgi pix**</span><span class="sxs-lookup"><span data-stu-id="522c2-253"><span id="PIX_DXGI_ERROR_WAIT_TIMEOUT"></span><span id="pix_dxgi_error_wait_timeout"></span>**PIX\_DXGI\_ERROR\_WAIT\_TIMEOUT**</span></span>  
<span data-ttu-id="522c2-254">HRESULT personnalisé qui renvoie l' \_ \_ \_ expiration du délai d’attente d’erreur DXGI.</span><span class="sxs-lookup"><span data-stu-id="522c2-254">A custom HRESULT that echos DXGI\_ERROR\_WAIT\_TIMEOUT.</span></span>

<span data-ttu-id="522c2-255"><span id="PIX_DXGI_ERROR_SESSION_DISCONNECTED"></span><span id="pix_dxgi_error_session_disconnected"></span>**\_session d’erreur pix dxgi \_ \_ \_ déconnectée**</span><span class="sxs-lookup"><span data-stu-id="522c2-255"><span id="PIX_DXGI_ERROR_SESSION_DISCONNECTED"></span><span id="pix_dxgi_error_session_disconnected"></span>**PIX\_DXGI\_ERROR\_SESSION\_DISCONNECTED**</span></span>  
<span data-ttu-id="522c2-256">HRESULT personnalisé qui \_ \_ déconnecte la session d’erreur dxgi renvoie \_ .</span><span class="sxs-lookup"><span data-stu-id="522c2-256">A custom HRESULT that echos DXGI\_ERROR\_SESSION\_DISCONNECTED.</span></span>

<span data-ttu-id="522c2-257"><span id="PIX_DXGI_ERROR_RESTRICT_TO_OUTPUT_STALE"></span><span id="pix_dxgi_error_restrict_to_output_stale"></span>**\_ \_ erreur de dxgi pix pour la \_ \_ \_ sortie \_ obsolète**</span><span class="sxs-lookup"><span data-stu-id="522c2-257"><span id="PIX_DXGI_ERROR_RESTRICT_TO_OUTPUT_STALE"></span><span id="pix_dxgi_error_restrict_to_output_stale"></span>**PIX\_DXGI\_ERROR\_RESTRICT\_TO\_OUTPUT\_STALE**</span></span>  
<span data-ttu-id="522c2-258">Un HRESULT personnalisé qui renvoie l' \_ erreur dxgi \_ limite \_ à la \_ sortie \_ obsolète.</span><span class="sxs-lookup"><span data-stu-id="522c2-258">A custom HRESULT that echos DXGI\_ERROR\_RESTRICT\_TO\_OUTPUT\_STALE.</span></span>

<span data-ttu-id="522c2-259"><span id="PIX_DXGI_ERROR_CANNOT_PROTECT_CONTENT"></span><span id="pix_dxgi_error_cannot_protect_content"></span>**l' \_ erreur dxgi pix \_ \_ ne peut pas \_ protéger le \_ contenu**</span><span class="sxs-lookup"><span data-stu-id="522c2-259"><span id="PIX_DXGI_ERROR_CANNOT_PROTECT_CONTENT"></span><span id="pix_dxgi_error_cannot_protect_content"></span>**PIX\_DXGI\_ERROR\_CANNOT\_PROTECT\_CONTENT**</span></span>  
<span data-ttu-id="522c2-260">Un HRESULT personnalisé qui renvoie l' \_ erreur dxgi \_ ne peut pas \_ protéger du \_ contenu.</span><span class="sxs-lookup"><span data-stu-id="522c2-260">A custom HRESULT that echos DXGI\_ERROR\_CANNOT\_PROTECT\_CONTENT.</span></span>

<span data-ttu-id="522c2-261"><span id="PIX_DXGI_ERROR_ACCESS_DENIED"></span><span id="pix_dxgi_error_access_denied"></span>**\_ \_ \_ accès à l’erreur pix dxgi \_ refusé**</span><span class="sxs-lookup"><span data-stu-id="522c2-261"><span id="PIX_DXGI_ERROR_ACCESS_DENIED"></span><span id="pix_dxgi_error_access_denied"></span>**PIX\_DXGI\_ERROR\_ACCESS\_DENIED**</span></span>  
<span data-ttu-id="522c2-262">HRESULT personnalisé qui renvoie \_ \_ l’accès à l’erreur dxgi \_ .</span><span class="sxs-lookup"><span data-stu-id="522c2-262">A custom HRESULT that echos DXGI\_ERROR\_ACCESS\_DENIED.</span></span>

<span data-ttu-id="522c2-263"><span id="PIX_DXGI_ERROR_NAME_ALREADY_EXISTS"></span><span id="pix_dxgi_error_name_already_exists"></span>**un \_ nom d’erreur dxgi pix \_ \_ \_ \_ existe déjà**</span><span class="sxs-lookup"><span data-stu-id="522c2-263"><span id="PIX_DXGI_ERROR_NAME_ALREADY_EXISTS"></span><span id="pix_dxgi_error_name_already_exists"></span>**PIX\_DXGI\_ERROR\_NAME\_ALREADY\_EXISTS**</span></span>  
<span data-ttu-id="522c2-264">Un HRESULT personnalisé qui renvoie \_ nom d’erreur dxgi \_ \_ \_ existe déjà.</span><span class="sxs-lookup"><span data-stu-id="522c2-264">A custom HRESULT that echos DXGI\_ERROR\_NAME\_ALREADY\_EXISTS.</span></span>

<span data-ttu-id="522c2-265"><span id="PIX_DXGI_ERROR_SDK_COMPONENT_MISSING"></span><span id="pix_dxgi_error_sdk_component_missing"></span>**\_composant du \_ Kit de \_ développement logiciel (SDK) pix dxgi \_ \_ manquant**</span><span class="sxs-lookup"><span data-stu-id="522c2-265"><span id="PIX_DXGI_ERROR_SDK_COMPONENT_MISSING"></span><span id="pix_dxgi_error_sdk_component_missing"></span>**PIX\_DXGI\_ERROR\_SDK\_COMPONENT\_MISSING**</span></span>  
<span data-ttu-id="522c2-266">HRESULT personnalisé qui est manquant dans le composant renvoie DXGI \_ Error \_ SDK \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="522c2-266">A custom HRESULT that echos DXGI\_ERROR\_SDK\_COMPONENT\_MISSING.</span></span>

<span data-ttu-id="522c2-267"><span id="PIX_DXGI_DDI_ERR_WASSTILLDRAWING"></span><span id="pix_dxgi_ddi_err_wasstilldrawing"></span>**PIX \_ dxgi \_ DDI \_ Err \_ WASSTILLDRAWING**</span><span class="sxs-lookup"><span data-stu-id="522c2-267"><span id="PIX_DXGI_DDI_ERR_WASSTILLDRAWING"></span><span id="pix_dxgi_ddi_err_wasstilldrawing"></span>**PIX\_DXGI\_DDI\_ERR\_WASSTILLDRAWING**</span></span>  
<span data-ttu-id="522c2-268">HRESULT personnalisé qui renvoie DXGI \_ DDI \_ Err \_ WASSTILLDRAWING.</span><span class="sxs-lookup"><span data-stu-id="522c2-268">A custom HRESULT that echos DXGI\_DDI\_ERR\_WASSTILLDRAWING.</span></span>

<span data-ttu-id="522c2-269"><span id="PIX_DXGI_DDI_ERR_UNSUPPORTED"></span><span id="pix_dxgi_ddi_err_unsupported"></span>**\_erreur dxgi \_ DDI \_ pix \_ non prise en charge**</span><span class="sxs-lookup"><span data-stu-id="522c2-269"><span id="PIX_DXGI_DDI_ERR_UNSUPPORTED"></span><span id="pix_dxgi_ddi_err_unsupported"></span>**PIX\_DXGI\_DDI\_ERR\_UNSUPPORTED**</span></span>  
<span data-ttu-id="522c2-270">HRESULT personnalisé que renvoie DXGI \_ DDI Err n’est \_ \_ pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="522c2-270">A custom HRESULT that echos DXGI\_DDI\_ERR\_UNSUPPORTED.</span></span>

<span data-ttu-id="522c2-271"><span id="PIX_DXGI_DDI_ERR_NONEXCLUSIVE"></span><span id="pix_dxgi_ddi_err_nonexclusive"></span>**\_ \_ erreur DDI dxgi DDI non \_ \_ exclusive**</span><span class="sxs-lookup"><span data-stu-id="522c2-271"><span id="PIX_DXGI_DDI_ERR_NONEXCLUSIVE"></span><span id="pix_dxgi_ddi_err_nonexclusive"></span>**PIX\_DXGI\_DDI\_ERR\_NONEXCLUSIVE**</span></span>  
<span data-ttu-id="522c2-272">HRESULT personnalisé qui renvoie DXGI \_ DDI \_ Err non \_ exclusif.</span><span class="sxs-lookup"><span data-stu-id="522c2-272">A custom HRESULT that echos DXGI\_DDI\_ERR\_NONEXCLUSIVE.</span></span>

<span data-ttu-id="522c2-273"><span id="PIX_D3D10_ERROR_TOO_MANY_UNIQUE_STATE_OBJECTS"></span><span id="pix_d3d10_error_too_many_unique_state_objects"></span>**Erreur de D3D10 PIX- \_ nombre d’objets d' \_ \_ \_ \_ État uniques trop nombreux \_ \_**</span><span class="sxs-lookup"><span data-stu-id="522c2-273"><span id="PIX_D3D10_ERROR_TOO_MANY_UNIQUE_STATE_OBJECTS"></span><span id="pix_d3d10_error_too_many_unique_state_objects"></span>**PIX\_D3D10\_ERROR\_TOO\_MANY\_UNIQUE\_STATE\_OBJECTS**</span></span>  
<span data-ttu-id="522c2-274">HRESULT personnalisé qui renvoie D3D10 d' \_ un \_ trop \_ grand nombre d' \_ \_ objets d’État uniques \_ .</span><span class="sxs-lookup"><span data-stu-id="522c2-274">A custom HRESULT that echos D3D10\_ERROR\_TOO\_MANY\_UNIQUE\_STATE\_OBJECTS.</span></span>

<span data-ttu-id="522c2-275"><span id="PIX_D3D10_ERROR_FILE_NOT_FOUND"></span><span id="pix_d3d10_error_file_not_found"></span>**\_Fichier d' \_ erreur D3D10 pix \_ \_ \_ introuvable**</span><span class="sxs-lookup"><span data-stu-id="522c2-275"><span id="PIX_D3D10_ERROR_FILE_NOT_FOUND"></span><span id="pix_d3d10_error_file_not_found"></span>**PIX\_D3D10\_ERROR\_FILE\_NOT\_FOUND**</span></span>  
<span data-ttu-id="522c2-276">HRESULT personnalisé qui renvoie fichier d' \_ erreur \_ D3D10 \_ \_ introuvable.</span><span class="sxs-lookup"><span data-stu-id="522c2-276">A custom HRESULT that echos D3D10\_ERROR\_FILE\_NOT\_FOUND.</span></span>

<span data-ttu-id="522c2-277"><span id="PIX_D3D11_ERROR_TOO_MANY_UNIQUE_STATE_OBJECTS"></span><span id="pix_d3d11_error_too_many_unique_state_objects"></span>**Erreur de d3d11 PIX- \_ nombre d’objets d' \_ \_ \_ \_ État uniques trop nombreux \_ \_**</span><span class="sxs-lookup"><span data-stu-id="522c2-277"><span id="PIX_D3D11_ERROR_TOO_MANY_UNIQUE_STATE_OBJECTS"></span><span id="pix_d3d11_error_too_many_unique_state_objects"></span>**PIX\_D3D11\_ERROR\_TOO\_MANY\_UNIQUE\_STATE\_OBJECTS**</span></span>  
<span data-ttu-id="522c2-278">HRESULT personnalisé qui renvoie D3D11 d' \_ un \_ trop \_ grand nombre d' \_ \_ objets d’État uniques \_ .</span><span class="sxs-lookup"><span data-stu-id="522c2-278">A custom HRESULT that echos D3D11\_ERROR\_TOO\_MANY\_UNIQUE\_STATE\_OBJECTS.</span></span>

<span data-ttu-id="522c2-279"><span id="PIX_D3D11_ERROR_FILE_NOT_FOUND"></span><span id="pix_d3d11_error_file_not_found"></span>**\_Fichier d' \_ erreur d3d11 pix \_ \_ \_ introuvable**</span><span class="sxs-lookup"><span data-stu-id="522c2-279"><span id="PIX_D3D11_ERROR_FILE_NOT_FOUND"></span><span id="pix_d3d11_error_file_not_found"></span>**PIX\_D3D11\_ERROR\_FILE\_NOT\_FOUND**</span></span>  
<span data-ttu-id="522c2-280">HRESULT personnalisé qui renvoie fichier d' \_ erreur \_ d3d11 \_ \_ introuvable.</span><span class="sxs-lookup"><span data-stu-id="522c2-280">A custom HRESULT that echos D3D11\_ERROR\_FILE\_NOT\_FOUND.</span></span>

<span data-ttu-id="522c2-281"><span id="PIX_D3D11_ERROR_TOO_MANY_UNIQUE_VIEW_OBJECTS"></span><span id="pix_d3d11_error_too_many_unique_view_objects"></span>**\_Erreur d3d11 pix- \_ nombre d' \_ \_ \_ \_ objets de vue uniques trop nombreux \_**</span><span class="sxs-lookup"><span data-stu-id="522c2-281"><span id="PIX_D3D11_ERROR_TOO_MANY_UNIQUE_VIEW_OBJECTS"></span><span id="pix_d3d11_error_too_many_unique_view_objects"></span>**PIX\_D3D11\_ERROR\_TOO\_MANY\_UNIQUE\_VIEW\_OBJECTS**</span></span>  
<span data-ttu-id="522c2-282">HRESULT personnalisé qui renvoie D3D11 \_ erreur \_ trop \_ nombreux objets de \_ \_ vue uniques \_ .</span><span class="sxs-lookup"><span data-stu-id="522c2-282">A custom HRESULT that echos D3D11\_ERROR\_TOO\_MANY\_UNIQUE\_VIEW\_OBJECTS.</span></span>

<span data-ttu-id="522c2-283"><span id="PIX_D3D11_ERROR_DEFERRED_CONTEXT_MAP_WITHOUT_INITIAL_DISCARD"></span><span id="pix_d3d11_error_deferred_context_map_without_initial_discard"></span>**\_Erreur de \_ mappage de contexte différé d3d11 de pix \_ \_ \_ \_ sans \_ ignorer la première \_ fois**</span><span class="sxs-lookup"><span data-stu-id="522c2-283"><span id="PIX_D3D11_ERROR_DEFERRED_CONTEXT_MAP_WITHOUT_INITIAL_DISCARD"></span><span id="pix_d3d11_error_deferred_context_map_without_initial_discard"></span>**PIX\_D3D11\_ERROR\_DEFERRED\_CONTEXT\_MAP\_WITHOUT\_INITIAL\_DISCARD**</span></span>  
<span data-ttu-id="522c2-284">HRESULT personnalisé qui renvoie le \_ mappage de \_ contexte différé \_ d’erreur d3d11 \_ \_ sans \_ l' \_ annulation initiale.</span><span class="sxs-lookup"><span data-stu-id="522c2-284">A custom HRESULT that echos D3D11\_ERROR\_DEFERRED\_CONTEXT\_MAP\_WITHOUT\_INITIAL\_DISCARD.</span></span>

<span data-ttu-id="522c2-285"><span id="PIX_ERROR_OCCLUDED_DRAW_CALL"></span><span id="pix_error_occluded_draw_call"></span>**erreur PIX bloqués de l' \_ \_ \_ appel de dessin \_**</span><span class="sxs-lookup"><span data-stu-id="522c2-285"><span id="PIX_ERROR_OCCLUDED_DRAW_CALL"></span><span id="pix_error_occluded_draw_call"></span>**PIX\_ERROR\_OCCLUDED\_DRAW\_CALL**</span></span>  
<span data-ttu-id="522c2-286">HRESULT personnalisé qui indique qu’un appel de dessin a été entièrement bloqués, provoquant une erreur.</span><span class="sxs-lookup"><span data-stu-id="522c2-286">A custom HRESULT which indicates that a draw call was entirely occluded, resulting in an error.</span></span>

## <a name="requirements"></a><span data-ttu-id="522c2-287">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="522c2-287">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="522c2-288">En-tête</span><span class="sxs-lookup"><span data-stu-id="522c2-288">Header</span></span></p></td><td><span data-ttu-id="522c2-289">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="522c2-289">Vspixengine.h</span></span></td></tr></tbody></table>

 

 



