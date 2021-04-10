---
title: Valeurs de Registre du protocole d’authentification
description: Le logiciel d’installation de la DLL EAP peut créer les valeurs de Registre suivantes sous eaptypeid.
ms.assetid: a5f6674d-77c8-4b88-af0e-bb62f84d8a2b
keywords:
- RAS_EAP_VALUENAME_PATH
- RAS_EAP_VALUENAME_FRIENDLY_NAME
- RAS_EAP_VALUENAME_CONFIGUI
- RAS_EAP_VALUENAME_DEFAULT_DATA
- RAS_EAP_VALUENAME_REQUIRE_CONFIGUI
- RAS_EAP_VALUENAME_CONFIG_CLSID
- RAS_EAP_VALUENAME_IDENTITY
- RAS_EAP_VALUENAME_INTERACTIVEUI
- RAS_EAP_VALUENAME_INVOKE_NAMEDLG
- RAS_EAP_VALUENAME_INVOKE_PWDDLG
- RAS_EAP_VALUENAME_ENCRYPTION
- RAS_EAP_VALUENAME_STANDALONE_SUPPORTED
- RAS_EAP_VALUENAME_ROLES_SUPPORTED
- RAS_EAP_VALUENAME_PER_POLICY_CONFIG
- RAS_EAP_VALUENAME_ISTUNNEL_METHOD
- RAS_EAP_VALUENAME_FILTER_INNERMETHODS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8091197c7b0d5c5a208bf3658bbc15284a29ac9e
ms.sourcegitcommit: c20a43b333f03175ac23823c55f3204bfe8cd243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2019
ms.locfileid: "104030650"
---
# <a name="authentication-protocol-registry-values"></a><span data-ttu-id="55233-119">Valeurs de Registre du protocole d’authentification</span><span class="sxs-lookup"><span data-stu-id="55233-119">Authentication Protocol Registry Values</span></span>

<span data-ttu-id="55233-120">Le logiciel d’installation de la DLL EAP peut créer les valeurs de Registre suivantes sous **&lt; eaptypeid &gt;**.</span><span class="sxs-lookup"><span data-stu-id="55233-120">The setup software for the EAP DLL may create the following registry values below **&lt;eaptypeid&gt;**.</span></span> <span data-ttu-id="55233-121">Ces valeurs de Registre sont définies dans le fichier d’en-tête Raseapif. h.</span><span class="sxs-lookup"><span data-stu-id="55233-121">These registry values are defined in the Raseapif.h header file.</span></span> <span data-ttu-id="55233-122">Les valeurs **RAS_EAP_VALUENAME_PATH** et **RAS_EAP_VALUENAME_FRIENDLY_NAME** sont requises.</span><span class="sxs-lookup"><span data-stu-id="55233-122">The **RAS_EAP_VALUENAME_PATH** and **RAS_EAP_VALUENAME_FRIENDLY_NAME** values are required.</span></span> <span data-ttu-id="55233-123">Le logiciel d’installation peut également créer d’autres clés et valeurs.</span><span class="sxs-lookup"><span data-stu-id="55233-123">The setup software may create other keys and values as well.</span></span> <span data-ttu-id="55233-124">Ils peuvent être utilisés par le protocole d’authentification lui-même.</span><span class="sxs-lookup"><span data-stu-id="55233-124">These could be used by the authentication protocol itself.</span></span> <span data-ttu-id="55233-125">Pour plus d’informations et pour obtenir un exemple de configuration du Registre, consultez [exemple de valeurs de Registre](registry-values-example.md).</span><span class="sxs-lookup"><span data-stu-id="55233-125">For more information and an example of registry configuration, see [Registry Values Example](registry-values-example.md).</span></span>

[<span data-ttu-id="55233-126">RAS_EAP_VALUENAME_PATH</span><span class="sxs-lookup"><span data-stu-id="55233-126">RAS_EAP_VALUENAME_PATH</span></span>](#ras_eap_valuename_path)

[<span data-ttu-id="55233-127">RAS_EAP_VALUENAME_FRIENDLY_NAME</span><span class="sxs-lookup"><span data-stu-id="55233-127">RAS_EAP_VALUENAME_FRIENDLY_NAME</span></span>](#ras_eap_valuename_friendly_name)

[<span data-ttu-id="55233-128">RAS_EAP_VALUENAME_CONFIGUI</span><span class="sxs-lookup"><span data-stu-id="55233-128">RAS_EAP_VALUENAME_CONFIGUI</span></span>](#ras_eap_valuename_configui)

[<span data-ttu-id="55233-129">RAS_EAP_VALUENAME_DEFAULT_DATA</span><span class="sxs-lookup"><span data-stu-id="55233-129">RAS_EAP_VALUENAME_DEFAULT_DATA</span></span>](#ras_eap_valuename_default_data)

[<span data-ttu-id="55233-130">RAS_EAP_VALUENAME_REQUIRE_CONFIGUI</span><span class="sxs-lookup"><span data-stu-id="55233-130">RAS_EAP_VALUENAME_REQUIRE_CONFIGUI</span></span>](#ras_eap_valuename_require_configui)

[<span data-ttu-id="55233-131">RAS_EAP_VALUENAME_CONFIG_CLSID</span><span class="sxs-lookup"><span data-stu-id="55233-131">RAS_EAP_VALUENAME_CONFIG_CLSID</span></span>](#ras_eap_valuename_config_clsid)

[<span data-ttu-id="55233-132">RAS_EAP_VALUENAME_IDENTITY</span><span class="sxs-lookup"><span data-stu-id="55233-132">RAS_EAP_VALUENAME_IDENTITY</span></span>](#ras_eap_valuename_identity)

<span data-ttu-id="55233-133">[RAS_EAP_VALUENAME_INTERACTIVEUI](#ras_eap_valuename_interactiveui) Cliqu</span><span class="sxs-lookup"><span data-stu-id="55233-133">[RAS_EAP_VALUENAME_INTERACTIVEUI](#ras_eap_valuename_interactiveui)I</span></span>

[<span data-ttu-id="55233-134">RAS_EAP_VALUENAME_INVOKE_NAMEDLG</span><span class="sxs-lookup"><span data-stu-id="55233-134">RAS_EAP_VALUENAME_INVOKE_NAMEDLG</span></span>](#ras_eap_valuename_invoke_namedlg)

[<span data-ttu-id="55233-135">RAS_EAP_VALUENAME_INVOKE_PWDDLG</span><span class="sxs-lookup"><span data-stu-id="55233-135">RAS_EAP_VALUENAME_INVOKE_PWDDLG</span></span>](#ras_eap_valuename_invoke_pwddlg)

[<span data-ttu-id="55233-136">RAS_EAP_VALUENAME_ENCRYPTION</span><span class="sxs-lookup"><span data-stu-id="55233-136">RAS_EAP_VALUENAME_ENCRYPTION</span></span>](#ras_eap_valuename_encryption)

[<span data-ttu-id="55233-137">RAS_EAP_VALUENAME_STANDALONE_SUPPORTED</span><span class="sxs-lookup"><span data-stu-id="55233-137">RAS_EAP_VALUENAME_STANDALONE_SUPPORTED</span></span>](#ras_eap_valuename_standalone_supported)

[<span data-ttu-id="55233-138">RAS_EAP_VALUENAME_ROLES_SUPPORTED</span><span class="sxs-lookup"><span data-stu-id="55233-138">RAS_EAP_VALUENAME_ROLES_SUPPORTED</span></span>](#ras_eap_valuename_roles_supported)

[<span data-ttu-id="55233-139">RAS_EAP_VALUENAME_PER_POLICY_CONFIG</span><span class="sxs-lookup"><span data-stu-id="55233-139">RAS_EAP_VALUENAME_PER_POLICY_CONFIG</span></span>](#ras_eap_valuename_per_policy_config)

[<span data-ttu-id="55233-140">RAS_EAP_VALUENAME_ISTUNNEL_METHOD</span><span class="sxs-lookup"><span data-stu-id="55233-140">RAS_EAP_VALUENAME_ISTUNNEL_METHOD</span></span>](#ras_eap_valuename_istunnel_method)

[<span data-ttu-id="55233-141">RAS_EAP_VALUENAME_FILTER_INNERMETHODS</span><span class="sxs-lookup"><span data-stu-id="55233-141">RAS_EAP_VALUENAME_FILTER_INNERMETHODS</span></span>](#ras_eap_valuename_filter_innermethods)

## <a name="ras_eap_valuename_path"></a><span data-ttu-id="55233-142">RAS_EAP_VALUENAME_PATH</span><span class="sxs-lookup"><span data-stu-id="55233-142">RAS_EAP_VALUENAME_PATH</span></span>

| <span data-ttu-id="55233-143">Valeur constante</span><span class="sxs-lookup"><span data-stu-id="55233-143">Constant value</span></span> | <span data-ttu-id="55233-144">Path</span><span class="sxs-lookup"><span data-stu-id="55233-144">Path</span></span>                               |
|----------------|------------------------------------|
| <span data-ttu-id="55233-145">Type</span><span class="sxs-lookup"><span data-stu-id="55233-145">Type</span></span>           | <span data-ttu-id="55233-146">REG_EXPAND_SZ</span><span class="sxs-lookup"><span data-stu-id="55233-146">REG_EXPAND_SZ</span></span>                    |
| <span data-ttu-id="55233-147">Description</span><span class="sxs-lookup"><span data-stu-id="55233-147">Description</span></span>    | <span data-ttu-id="55233-148">Spécifie le chemin d’accès à la DLL EAP.</span><span class="sxs-lookup"><span data-stu-id="55233-148">Specifies the path to the EAP DLL.</span></span> |

## <a name="ras_eap_valuename_friendly_name"></a><span data-ttu-id="55233-149">RAS_EAP_VALUENAME_FRIENDLY_NAME</span><span class="sxs-lookup"><span data-stu-id="55233-149">RAS_EAP_VALUENAME_FRIENDLY_NAME</span></span>

| <span data-ttu-id="55233-150">Valeur constante</span><span class="sxs-lookup"><span data-stu-id="55233-150">Constant value</span></span> | <span data-ttu-id="55233-151">FriendlyName</span><span class="sxs-lookup"><span data-stu-id="55233-151">FriendlyName</span></span>                                                                                                                                                      |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="55233-152">Type</span><span class="sxs-lookup"><span data-stu-id="55233-152">Type</span></span>           | <span data-ttu-id="55233-153">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="55233-153">REG_SZ</span></span>                                                                                                                                                           |
| <span data-ttu-id="55233-154">Description</span><span class="sxs-lookup"><span data-stu-id="55233-154">Description</span></span>    | <span data-ttu-id="55233-155">Spécifie un nom convivial pour le protocole d’authentification.</span><span class="sxs-lookup"><span data-stu-id="55233-155">Specifies a friendly name for the authentication protocol.</span></span> <span data-ttu-id="55233-156">Ce nom s’affiche dans l’interface utilisateur de l’application EAP pour les implémentations d’accès à distance et sans fil.</span><span class="sxs-lookup"><span data-stu-id="55233-156">This name appears in the EAP application user interface for both dial-up and wireless implementations.</span></span> |

## <a name="ras_eap_valuename_configui"></a><span data-ttu-id="55233-157">RAS_EAP_VALUENAME_CONFIGUI</span><span class="sxs-lookup"><span data-stu-id="55233-157">RAS_EAP_VALUENAME_CONFIGUI</span></span>

| <span data-ttu-id="55233-158">Valeur constante</span><span class="sxs-lookup"><span data-stu-id="55233-158">Constant value</span></span> | <span data-ttu-id="55233-159">ConfigUIPath</span><span class="sxs-lookup"><span data-stu-id="55233-159">ConfigUIPath</span></span>                                                                                                                      |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="55233-160">Type</span><span class="sxs-lookup"><span data-stu-id="55233-160">Type</span></span>           | <span data-ttu-id="55233-161">REG_EXPAND_SZ</span><span class="sxs-lookup"><span data-stu-id="55233-161">REG_EXPAND_SZ</span></span>                                                                                                                   |
| <span data-ttu-id="55233-162">Description</span><span class="sxs-lookup"><span data-stu-id="55233-162">Description</span></span>    | <span data-ttu-id="55233-163">Spécifie le chemin d’accès à la DLL qui implémente l’interface utilisateur de configuration sur le client, car cette interface utilisateur est destinée au client uniquement.</span><span class="sxs-lookup"><span data-stu-id="55233-163">Specifies the path to the DLL that implements the configuration user interface on the client, because this UI is for client only.</span></span> |

## <a name="ras_eap_valuename_default_data"></a><span data-ttu-id="55233-164">RAS_EAP_VALUENAME_DEFAULT_DATA</span><span class="sxs-lookup"><span data-stu-id="55233-164">RAS_EAP_VALUENAME_DEFAULT_DATA</span></span>

| <span data-ttu-id="55233-165">Valeur constante</span><span class="sxs-lookup"><span data-stu-id="55233-165">Constant value</span></span> | <span data-ttu-id="55233-166">ConfigData</span><span class="sxs-lookup"><span data-stu-id="55233-166">ConfigData</span></span>                                                            |
|----------------|-----------------------------------------------------------------------|
| <span data-ttu-id="55233-167">Type</span><span class="sxs-lookup"><span data-stu-id="55233-167">Type</span></span>           | <span data-ttu-id="55233-168">REG_BINARY</span><span class="sxs-lookup"><span data-stu-id="55233-168">REG_BINARY</span></span>                                                           |
| <span data-ttu-id="55233-169">Description</span><span class="sxs-lookup"><span data-stu-id="55233-169">Description</span></span>    | <span data-ttu-id="55233-170">Spécifie les données de configuration par défaut pour le protocole d’authentification.</span><span class="sxs-lookup"><span data-stu-id="55233-170">Specifies default configuration data for the authentication protocol.</span></span> |

## <a name="ras_eap_valuename_require_configui"></a><span data-ttu-id="55233-171">RAS_EAP_VALUENAME_REQUIRE_CONFIGUI</span><span class="sxs-lookup"><span data-stu-id="55233-171">RAS_EAP_VALUENAME_REQUIRE_CONFIGUI</span></span>

| <span data-ttu-id="55233-172">Valeur constante</span><span class="sxs-lookup"><span data-stu-id="55233-172">Constant value</span></span> | <span data-ttu-id="55233-173">RequireConfigUI</span><span class="sxs-lookup"><span data-stu-id="55233-173">RequireConfigUI</span></span>                                                                                                                                                                                                                                          |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="55233-174">Type</span><span class="sxs-lookup"><span data-stu-id="55233-174">Type</span></span>           | <span data-ttu-id="55233-175">REG_DWORD</span><span class="sxs-lookup"><span data-stu-id="55233-175">REG_DWORD</span></span>                                                                                                                                                                                                                                               |
| <span data-ttu-id="55233-176">Description</span><span class="sxs-lookup"><span data-stu-id="55233-176">Description</span></span>    | <span data-ttu-id="55233-177">Spécifie si l’utilisateur doit fournir des données de configuration dans l’interface utilisateur de l’application cliente EAP.</span><span class="sxs-lookup"><span data-stu-id="55233-177">Specifies whether the user must provide configuration data in the EAP client application user interface.</span></span> <span data-ttu-id="55233-178">Si cette valeur est 1, l’utilisateur n’est pas autorisé à quitter l’interface utilisateur de l’application cliente EAP sans fournir de données de configuration.</span><span class="sxs-lookup"><span data-stu-id="55233-178">If this value is 1, the user is not allowed to exit the EAP client application UI without providing configuration data.</span></span> <span data-ttu-id="55233-179">La valeur par défaut est 0.</span><span class="sxs-lookup"><span data-stu-id="55233-179">The default value is 0.</span></span> |

## <a name="ras_eap_valuename_config_clsid"></a><span data-ttu-id="55233-180">RAS_EAP_VALUENAME_CONFIG_CLSID</span><span class="sxs-lookup"><span data-stu-id="55233-180">RAS_EAP_VALUENAME_CONFIG_CLSID</span></span>

| <span data-ttu-id="55233-181">Valeur constante</span><span class="sxs-lookup"><span data-stu-id="55233-181">Constant value</span></span> | <span data-ttu-id="55233-182">ConfigCLSID</span><span class="sxs-lookup"><span data-stu-id="55233-182">ConfigCLSID</span></span>                                                   |
|----------------|---------------------------------------------------------------|
| <span data-ttu-id="55233-183">Type</span><span class="sxs-lookup"><span data-stu-id="55233-183">Type</span></span>           | <span data-ttu-id="55233-184">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="55233-184">REG_SZ</span></span>                                                       |
| <span data-ttu-id="55233-185">Description</span><span class="sxs-lookup"><span data-stu-id="55233-185">Description</span></span>    | <span data-ttu-id="55233-186">Spécifie l’ID de classe de l’interface utilisateur de configuration sur le serveur.</span><span class="sxs-lookup"><span data-stu-id="55233-186">Specifies the class ID of the configuration UI on the server.</span></span> |

## <a name="ras_eap_valuename_identity"></a><span data-ttu-id="55233-187">RAS_EAP_VALUENAME_IDENTITY</span><span class="sxs-lookup"><span data-stu-id="55233-187">RAS_EAP_VALUENAME_IDENTITY</span></span>

| <span data-ttu-id="55233-188">Valeur constante</span><span class="sxs-lookup"><span data-stu-id="55233-188">Constant value</span></span> | <span data-ttu-id="55233-189">IdentityPath</span><span class="sxs-lookup"><span data-stu-id="55233-189">IdentityPath</span></span>                                                                                                                           |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="55233-190">Type</span><span class="sxs-lookup"><span data-stu-id="55233-190">Type</span></span>           | <span data-ttu-id="55233-191">REG_EXPAND_SZ</span><span class="sxs-lookup"><span data-stu-id="55233-191">REG_EXPAND_SZ</span></span>                                                                                                                        |
| <span data-ttu-id="55233-192">Description</span><span class="sxs-lookup"><span data-stu-id="55233-192">Description</span></span>    | <span data-ttu-id="55233-193">Spécifie le chemin d’accès à la DLL qui implémente les fonctions pour obtenir l’identité de l’utilisateur sur le client, car cette interface utilisateur est destinée au client uniquement.</span><span class="sxs-lookup"><span data-stu-id="55233-193">Specifies the path to the DLL that implements functions to obtain the user identity on the client, because this UI is for client only.</span></span> |

## <a name="ras_eap_valuename_interactiveui"></a><span data-ttu-id="55233-194">RAS_EAP_VALUENAME_INTERACTIVEUI</span><span class="sxs-lookup"><span data-stu-id="55233-194">RAS_EAP_VALUENAME_INTERACTIVEUI</span></span>

| <span data-ttu-id="55233-195">Valeur constante</span><span class="sxs-lookup"><span data-stu-id="55233-195">Constant value</span></span> | <span data-ttu-id="55233-196">InteractiveUIPath</span><span class="sxs-lookup"><span data-stu-id="55233-196">InteractiveUIPath</span></span>                                                                                                               |
|----------------|---------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="55233-197">Type</span><span class="sxs-lookup"><span data-stu-id="55233-197">Type</span></span>           | <span data-ttu-id="55233-198">REG_EXPAND_SZ</span><span class="sxs-lookup"><span data-stu-id="55233-198">REG_EXPAND_SZ</span></span>                                                                                                                 |
| <span data-ttu-id="55233-199">Description</span><span class="sxs-lookup"><span data-stu-id="55233-199">Description</span></span>    | <span data-ttu-id="55233-200">Spécifie le chemin d’accès à la DLL qui implémente l’interface utilisateur interactive sur le client, car cette interface utilisateur est destinée au client uniquement.</span><span class="sxs-lookup"><span data-stu-id="55233-200">Specifies the path to the DLL that implements the interactive user interface on the client, because this UI is for client only.</span></span> |

## <a name="ras_eap_valuename_invoke_namedlg"></a><span data-ttu-id="55233-201">RAS_EAP_VALUENAME_INVOKE_NAMEDLG</span><span class="sxs-lookup"><span data-stu-id="55233-201">RAS_EAP_VALUENAME_INVOKE_NAMEDLG</span></span>

| <span data-ttu-id="55233-202">Valeur constante</span><span class="sxs-lookup"><span data-stu-id="55233-202">Constant value</span></span> | <span data-ttu-id="55233-203">InvokeUsernameDialog</span><span class="sxs-lookup"><span data-stu-id="55233-203">InvokeUsernameDialog</span></span>                                                                                                                                                                                   |
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="55233-204">Type</span><span class="sxs-lookup"><span data-stu-id="55233-204">Type</span></span>           | <span data-ttu-id="55233-205">REG_DWORD</span><span class="sxs-lookup"><span data-stu-id="55233-205">REG_DWORD</span></span>                                                                                                                                                                                             |
| <span data-ttu-id="55233-206">Description</span><span class="sxs-lookup"><span data-stu-id="55233-206">Description</span></span>    | <span data-ttu-id="55233-207">Spécifie si RAS doit afficher la boîte de dialogue du nom d’utilisateur Windows NT/Windows 2000 standard (valeur 1) ou appeler [**RasEapGetIdentity**](/previous-versions/windows/desktop/api/Raseapif/nf-raseapif-raseapgetidentity) (valeur 0).</span><span class="sxs-lookup"><span data-stu-id="55233-207">Specifies whether RAS should display the standard Windows NT/Windows 2000 user name dialog (value of 1) or invoke [**RasEapGetIdentity**](/previous-versions/windows/desktop/api/Raseapif/nf-raseapif-raseapgetidentity) (value of 0).</span></span> <span data-ttu-id="55233-208">La valeur par défaut est 1.</span><span class="sxs-lookup"><span data-stu-id="55233-208">The default value is 1.</span></span> |

## <a name="ras_eap_valuename_invoke_pwddlg"></a><span data-ttu-id="55233-209">RAS_EAP_VALUENAME_INVOKE_PWDDLG</span><span class="sxs-lookup"><span data-stu-id="55233-209">RAS_EAP_VALUENAME_INVOKE_PWDDLG</span></span>

| <span data-ttu-id="55233-210">Valeur constante</span><span class="sxs-lookup"><span data-stu-id="55233-210">Constant value</span></span> | <span data-ttu-id="55233-211">InvokePasswordDialog</span><span class="sxs-lookup"><span data-stu-id="55233-211">InvokePasswordDialog</span></span>                                                                                                                                                                        |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="55233-212">Type</span><span class="sxs-lookup"><span data-stu-id="55233-212">Type</span></span>           | <span data-ttu-id="55233-213">REG_DWORD</span><span class="sxs-lookup"><span data-stu-id="55233-213">REG_DWORD</span></span>                                                                                                                                                                                  |
| <span data-ttu-id="55233-214">Description</span><span class="sxs-lookup"><span data-stu-id="55233-214">Description</span></span>    | <span data-ttu-id="55233-215">Spécifie si RAS doit afficher la boîte de dialogue de mot de passe Windows NT/Windows 2000 standard.</span><span class="sxs-lookup"><span data-stu-id="55233-215">Specifies whether RAS should display the standard Windows NT/Windows 2000 password dialog.</span></span> <span data-ttu-id="55233-216">Si cette valeur existe et qu’elle est égale à 0, RAS n’affiche pas la boîte de dialogue de mot de passe.</span><span class="sxs-lookup"><span data-stu-id="55233-216">If this value exists and is 0, RAS will not display the password dialog.</span></span> <span data-ttu-id="55233-217">La valeur par défaut est 1.</span><span class="sxs-lookup"><span data-stu-id="55233-217">The default value is 1.</span></span> |


## <a name="ras_eap_valuename_encryption"></a><span data-ttu-id="55233-218">RAS_EAP_VALUENAME_ENCRYPTION</span><span class="sxs-lookup"><span data-stu-id="55233-218">RAS_EAP_VALUENAME_ENCRYPTION</span></span>

| <span data-ttu-id="55233-219">Valeur constante</span><span class="sxs-lookup"><span data-stu-id="55233-219">Constant value</span></span> | <span data-ttu-id="55233-220">MPPEEncryptionSupported</span><span class="sxs-lookup"><span data-stu-id="55233-220">MPPEEncryptionSupported</span></span>                                                                                                                                                                       |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="55233-221">Type</span><span class="sxs-lookup"><span data-stu-id="55233-221">Type</span></span>           | <span data-ttu-id="55233-222">REG_DWORD</span><span class="sxs-lookup"><span data-stu-id="55233-222">REG_DWORD</span></span>                                                                                                                                                                                    |
| <span data-ttu-id="55233-223">Description</span><span class="sxs-lookup"><span data-stu-id="55233-223">Description</span></span>    | <span data-ttu-id="55233-224">Si cette valeur est 1, le protocole d’authentification peut générer des clés pour le style de chiffrement MPPE (Microsoft Point-to-Point Encryption).</span><span class="sxs-lookup"><span data-stu-id="55233-224">If this value is 1, the authentication protocol can generate keys for the Microsoft Point-to-Point Encryption (MPPE) style of encryption.</span></span> <span data-ttu-id="55233-225">Les valeurs possibles sont 0 ou 1.</span><span class="sxs-lookup"><span data-stu-id="55233-225">Possible values are 0 or 1.</span></span> <span data-ttu-id="55233-226">La valeur par défaut est 0.</span><span class="sxs-lookup"><span data-stu-id="55233-226">The default value is 0.</span></span> |

## <a name="ras_eap_valuename_standalone_supported"></a><span data-ttu-id="55233-227">RAS_EAP_VALUENAME_STANDALONE_SUPPORTED</span><span class="sxs-lookup"><span data-stu-id="55233-227">RAS_EAP_VALUENAME_STANDALONE_SUPPORTED</span></span>

| <span data-ttu-id="55233-228">Valeur constante</span><span class="sxs-lookup"><span data-stu-id="55233-228">Constant value</span></span> | <span data-ttu-id="55233-229">StandaloneSupported</span><span class="sxs-lookup"><span data-stu-id="55233-229">StandaloneSupported</span></span>                                                                                                                                                            |
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="55233-230">Type</span><span class="sxs-lookup"><span data-stu-id="55233-230">Type</span></span>           | <span data-ttu-id="55233-231">REG_DWORD</span><span class="sxs-lookup"><span data-stu-id="55233-231">REG_DWORD</span></span>                                                                                                                                                                     |
| <span data-ttu-id="55233-232">Description</span><span class="sxs-lookup"><span data-stu-id="55233-232">Description</span></span>    | <span data-ttu-id="55233-233">Spécifie si ce protocole d’authentification est pris en charge sur un serveur Windows 2000 autonome.</span><span class="sxs-lookup"><span data-stu-id="55233-233">Specifies whether this authentication protocol is supported on a standalone Windows 2000 Server.</span></span> <span data-ttu-id="55233-234">La valeur 0 indique que le protocole EAP n’est pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="55233-234">A value of 0 indicates that the EAP is not supported.</span></span> <span data-ttu-id="55233-235">La valeur par défaut est 1.</span><span class="sxs-lookup"><span data-stu-id="55233-235">The default value is 1.</span></span> |

## <a name="ras_eap_valuename_roles_supported"></a><span data-ttu-id="55233-236">RAS_EAP_VALUENAME_ROLES_SUPPORTED</span><span class="sxs-lookup"><span data-stu-id="55233-236">RAS_EAP_VALUENAME_ROLES_SUPPORTED</span></span>

| <span data-ttu-id="55233-237">Valeur constante</span><span class="sxs-lookup"><span data-stu-id="55233-237">Constant Value</span></span> | <span data-ttu-id="55233-238">RolesSupported</span><span class="sxs-lookup"><span data-stu-id="55233-238">RolesSupported</span></span>                                                                                                                                                                                                                             |
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="55233-239">Type</span><span class="sxs-lookup"><span data-stu-id="55233-239">Type</span></span>           | <span data-ttu-id="55233-240">REG_DWORD</span><span class="sxs-lookup"><span data-stu-id="55233-240">REG_DWORD</span></span>                                                                                                                                                                                                                                 |
| <span data-ttu-id="55233-241">Description</span><span class="sxs-lookup"><span data-stu-id="55233-241">Description</span></span>    | <span data-ttu-id="55233-242">Spécifie les différents rôles pris en charge par EAP.</span><span class="sxs-lookup"><span data-stu-id="55233-242">Specifies the various roles the EAP supports.</span></span> <span data-ttu-id="55233-243">Cela indique s’il peut être utilisé sur un serveur ou un client, s’il est pris en charge pour les connexions RAS (VPN) ou PEAP.</span><span class="sxs-lookup"><span data-stu-id="55233-243">This indicates whether it can be used on a server or a client, whether it is supported for RAS connections (VPN) or PEAP.</span></span> <span data-ttu-id="55233-244">Le comportement par défaut consiste à afficher la méthode EAP dans PEAP et dans EAP.</span><span class="sxs-lookup"><span data-stu-id="55233-244">The default behavior is to show the EAP method in PEAP and in EAP.</span></span> |

## <a name="ras_eap_valuename_per_policy_config"></a><span data-ttu-id="55233-245">RAS_EAP_VALUENAME_PER_POLICY_CONFIG</span><span class="sxs-lookup"><span data-stu-id="55233-245">RAS_EAP_VALUENAME_PER_POLICY_CONFIG</span></span>

| <span data-ttu-id="55233-246">Valeur constante</span><span class="sxs-lookup"><span data-stu-id="55233-246">Constant Value</span></span> | <span data-ttu-id="55233-247">PerPolicyConfig</span><span class="sxs-lookup"><span data-stu-id="55233-247">PerPolicyConfig</span></span> |
|----------------|-----------------|
| <span data-ttu-id="55233-248">Type</span><span class="sxs-lookup"><span data-stu-id="55233-248">Type</span></span>           | <span data-ttu-id="55233-249">REG_DWORD</span><span class="sxs-lookup"><span data-stu-id="55233-249">REG_DWORD</span></span>      |
| <span data-ttu-id="55233-250">Description</span><span class="sxs-lookup"><span data-stu-id="55233-250">Description</span></span>    |                 |

## <a name="ras_eap_valuename_istunnel_method"></a><span data-ttu-id="55233-251">RAS_EAP_VALUENAME_ISTUNNEL_METHOD</span><span class="sxs-lookup"><span data-stu-id="55233-251">RAS_EAP_VALUENAME_ISTUNNEL_METHOD</span></span>

<span data-ttu-id="55233-252">Cette valeur de Registre n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="55233-252">This registry value is not in use.</span></span>

## <a name="ras_eap_valuename_filter_innermethods"></a><span data-ttu-id="55233-253">RAS_EAP_VALUENAME_FILTER_INNERMETHODS</span><span class="sxs-lookup"><span data-stu-id="55233-253">RAS_EAP_VALUENAME_FILTER_INNERMETHODS</span></span>

<span data-ttu-id="55233-254">Cette valeur de Registre n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="55233-254">This registry value is not in use.</span></span>

