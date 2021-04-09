---
title: Classe MDM_Policy_Result01_Browser02
description: La \_ classe Result01 Browser02 de la stratégie MDM \_ \_ représente les stratégies de navigateur disponibles. \_ \_ \_ La classe Browser02 de la stratégie MDM Result01 représente les stratégies de navigateur disponibles.
ms.assetid: 06dc9f68-d9ea-4eec-93cb-1f26e8a6050d
keywords:
- Classe MDM_Policy_Result01_Browser02
- Classe MDM_Policy_Result01_Browser02, Description
topic_type:
- apiref
api_name:
- MDM_Policy_Result01_Browser02
- MDM_Policy_Result01_Browser02.InstanceID
- MDM_Policy_Result01_Browser02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 19d132c43b88b242864e248b705a0f6bca02e546
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843133"
---
# <a name="mdm_policy_result01_browser02-class"></a><span data-ttu-id="54a5c-105">\_Classe Browser02 de la stratégie MDM \_ Result01 \_</span><span class="sxs-lookup"><span data-stu-id="54a5c-105">MDM\_Policy\_Result01\_Browser02 class</span></span>

<span data-ttu-id="54a5c-106">\[Certaines informations relatives aux produits précommercialisés peuvent être substantiellement modifiées avant leur commercialisation.</span><span class="sxs-lookup"><span data-stu-id="54a5c-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="54a5c-107">Microsoft ne donne aucune garantie, expresse ou implicite, concernant les informations fournies ici.\]</span><span class="sxs-lookup"><span data-stu-id="54a5c-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="54a5c-108">La **classe \_ \_ Result01 \_ Browser02 de la stratégie MDM** représente les stratégies de navigateur disponibles.</span><span class="sxs-lookup"><span data-stu-id="54a5c-108">The **MDM\_Policy\_Result01\_Browser02** class represents the browser policies available.</span></span>

<span data-ttu-id="54a5c-109">La syntaxe suivante issue du code MOF est simplifiée et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="54a5c-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="54a5c-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="54a5c-110">Syntax</span></span>

``` syntax
[InPartition("local-system", "local-user"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Result01_Browser02
{
  string InstanceID;
  string ParentID;
  sint32 AllowAddressBarDropdown;
  sint32 AllowAutofill;
  sint32 AllowCookies;
  sint32 AllowDeveloperTools;
  sint32 AllowInPrivate;
  sint32 AllowMicrosoftCompatibilityList;
  sint32 AllowDoNotTrack;
  sint32 AllowFlashClickToRun;
  sint32 AllowFlash;
  sint32 AllowExtensions;
  sint32 AllowPasswordManager;
  sint32 AllowPopups;
  sint32 AllowSearchEngineCustomization;
  sint32 AllowSearchSuggestionsinAddressBar;
  sint32 AllowSmartScreen;
  sint32 AlwaysEnableBooksLibrary;
  sint32 DisableLockdownOfStartPages;
  string ConfigureAdditionalSearchEngines;
  sint32 ClearBrowsingDataOnExit;
  string EnterpriseModeSiteList;
  string EnterpriseSiteListServiceUrl;
  string Homepages;
  sint32 LockdownFavorites;
  sint32 PreventAccessToAboutFlagsInMicrosoftEdge;
  sint32 PreventLiveTileDataCollection;
  sint32 PreventFirstRunPage;
  sint32 PreventSmartScreenPromptOverride;
  sint32 PreventSmartScreenPromptOverrideForFiles;
  sint32 PreventUsingLocalHostIPAddressForWebRTC;
  string ProvisionFavorites;
  sint32 SendIntranetTraffictoInternetExplorer;
  string SetDefaultSearchEngine;
  sint32 ShowMessageWhenOpeningSitesInInternetExplorer;
  sint32 SyncFavoritesBetweenIEAndMicrosoftEdge;
};
```

## <a name="members"></a><span data-ttu-id="54a5c-111">Membres</span><span class="sxs-lookup"><span data-stu-id="54a5c-111">Members</span></span>

<span data-ttu-id="54a5c-112">La **classe \_ \_ Result01 \_ Browser02 de la stratégie MDM** a les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="54a5c-112">The **MDM\_Policy\_Result01\_Browser02** class has these types of members:</span></span>

-   [<span data-ttu-id="54a5c-113">Propriétés</span><span class="sxs-lookup"><span data-stu-id="54a5c-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="54a5c-114">Propriétés</span><span class="sxs-lookup"><span data-stu-id="54a5c-114">Properties</span></span>

<span data-ttu-id="54a5c-115">La **classe \_ \_ Result01 \_ Browser02 de la stratégie MDM** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="54a5c-115">The **MDM\_Policy\_Result01\_Browser02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="54a5c-116">AllowAddressBarDropdown</span><span class="sxs-lookup"><span data-stu-id="54a5c-116">AllowAddressBarDropdown</span></span>](/windows/client-management/mdm/policy-csp-browser#browser-allowaddressbardropdown)
</dt> <dd> <dl> <dt>

<span data-ttu-id="54a5c-117">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="54a5c-117">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="54a5c-118">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="54a5c-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="54a5c-119">AllowAutofill</span><span class="sxs-lookup"><span data-stu-id="54a5c-119">AllowAutofill</span></span>](/windows/client-management/mdm/policy-csp-browser#browser-allowautofill)
</dt> <dd> <dl> <dt>

<span data-ttu-id="54a5c-120">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="54a5c-120">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="54a5c-121">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="54a5c-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="54a5c-122">AllowCookies</span><span class="sxs-lookup"><span data-stu-id="54a5c-122">AllowCookies</span></span>](/windows/client-management/mdm/policy-csp-browser#browser-allowcookies)
</dt> <dd> <dl> <dt>

<span data-ttu-id="54a5c-123">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="54a5c-123">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="54a5c-124">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="54a5c-124">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="54a5c-125">AllowDeveloperTools</span><span class="sxs-lookup"><span data-stu-id="54a5c-125">AllowDeveloperTools</span></span>](/windows/client-management/mdm/policy-csp-browser#browser-allowdevelopertools)
</dt> <dd> <dl> <dt>

<span data-ttu-id="54a5c-126">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="54a5c-126">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="54a5c-127">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="54a5c-127">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="54a5c-128">AllowDoNotTrack</span><span class="sxs-lookup"><span data-stu-id="54a5c-128">AllowDoNotTrack</span></span>](/windows/client-management/mdm/policy-csp-browser#browser-allowdonottrack)
</dt> <dd> <dl> <dt>

<span data-ttu-id="54a5c-129">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="54a5c-129">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="54a5c-130">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="54a5c-130">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="54a5c-131">AllowExtensions</span><span class="sxs-lookup"><span data-stu-id="54a5c-131">AllowExtensions</span></span>](/windows/client-management/mdm/policy-csp-browser#browser-allowextensions)
</dt> <dd> <dl> <dt>

<span data-ttu-id="54a5c-132">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="54a5c-132">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="54a5c-133">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="54a5c-133">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="54a5c-134">AllowFlash</span><span class="sxs-lookup"><span data-stu-id="54a5c-134">AllowFlash</span></span>](/windows/client-management/mdm/policy-csp-browser#browser-allowflash)
</dt> <dd> <dl> <dt>

<span data-ttu-id="54a5c-135">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="54a5c-135">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="54a5c-136">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="54a5c-136">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="54a5c-137">AllowFlashClickToRun</span><span class="sxs-lookup"><span data-stu-id="54a5c-137">AllowFlashClickToRun</span></span>](/windows/client-management/mdm/policy-csp-browser#browser-allowflashclicktorun)
</dt> <dd> <dl> <dt>

<span data-ttu-id="54a5c-138">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="54a5c-138">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="54a5c-139">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="54a5c-139">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="54a5c-140">AllowInPrivate</span><span class="sxs-lookup"><span data-stu-id="54a5c-140">AllowInPrivate</span></span>](/windows/client-management/mdm/policy-csp-browser#browser-allowinprivate)
</dt> <dd> <dl> <dt>

<span data-ttu-id="54a5c-141">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="54a5c-141">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="54a5c-142">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="54a5c-142">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="54a5c-143">AllowMicrosoftCompatibilityList</span><span class="sxs-lookup"><span data-stu-id="54a5c-143">AllowMicrosoftCompatibilityList</span></span>](/windows/client-management/mdm/policy-csp-browser#browser-allowmicrosoftcompatibilitylist)
</dt> <dd> <dl> <dt>

<span data-ttu-id="54a5c-144">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="54a5c-144">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="54a5c-145">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="54a5c-145">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="54a5c-146">AllowPasswordManager</span><span class="sxs-lookup"><span data-stu-id="54a5c-146">AllowPasswordManager</span></span>](/windows/client-management/mdm/policy-csp-browser#browser-allowpasswordmanager)
</dt> <dd> <dl> <dt>

<span data-ttu-id="54a5c-147">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="54a5c-147">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="54a5c-148">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="54a5c-148">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="54a5c-149">AllowPopups</span><span class="sxs-lookup"><span data-stu-id="54a5c-149">AllowPopups</span></span>](/windows/client-management/mdm/policy-csp-browser#browser-allowpopups)
</dt> <dd> <dl> <dt>

<span data-ttu-id="54a5c-150">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="54a5c-150">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="54a5c-151">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="54a5c-151">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="54a5c-152">AllowSearchEngineCustomization</span><span class="sxs-lookup"><span data-stu-id="54a5c-152">AllowSearchEngineCustomization</span></span>](/windows/client-management/mdm/policy-csp-browser#browser-allowsearchenginecustomization)
</dt> <dd> <dl> <dt>

<span data-ttu-id="54a5c-153">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="54a5c-153">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="54a5c-154">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="54a5c-154">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="54a5c-155">AllowSearchSuggestionsinAddressBar</span><span class="sxs-lookup"><span data-stu-id="54a5c-155">AllowSearchSuggestionsinAddressBar</span></span>](/windows/client-management/mdm/policy-csp-browser#browser-allowsearchsuggestionsinaddressbar)
</dt> <dd> <dl> <dt>

<span data-ttu-id="54a5c-156">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="54a5c-156">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="54a5c-157">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="54a5c-157">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="54a5c-158">AllowSmartScreen</span><span class="sxs-lookup"><span data-stu-id="54a5c-158">AllowSmartScreen</span></span>](/windows/client-management/mdm/policy-csp-browser#browser-allowsmartscreen)
</dt> <dd> <dl> <dt>

<span data-ttu-id="54a5c-159">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="54a5c-159">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="54a5c-160">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="54a5c-160">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="54a5c-161">AlwaysEnableBooksLibrary</span><span class="sxs-lookup"><span data-stu-id="54a5c-161">AlwaysEnableBooksLibrary</span></span>](/windows/client-management/mdm/policy-csp-browser#browser-alwaysenablebookslibrary)
</dt> <dd> <dl> <dt>

<span data-ttu-id="54a5c-162">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="54a5c-162">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="54a5c-163">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="54a5c-163">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="54a5c-164">ClearBrowsingDataOnExit</span><span class="sxs-lookup"><span data-stu-id="54a5c-164">ClearBrowsingDataOnExit</span></span>](/windows/client-management/mdm/policy-csp-browser#browser-clearbrowsingdataonexit)
</dt> <dd> <dl> <dt>

<span data-ttu-id="54a5c-165">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="54a5c-165">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="54a5c-166">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="54a5c-166">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="54a5c-167">ConfigureAdditionalSearchEngines</span><span class="sxs-lookup"><span data-stu-id="54a5c-167">ConfigureAdditionalSearchEngines</span></span>](/windows/client-management/mdm/policy-csp-browser#browser-configureadditionalsearchengines)
</dt> <dd> <dl> <dt>

<span data-ttu-id="54a5c-168">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="54a5c-168">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="54a5c-169">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="54a5c-169">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="54a5c-170">DisableLockdownOfStartPages</span><span class="sxs-lookup"><span data-stu-id="54a5c-170">DisableLockdownOfStartPages</span></span>](/windows/client-management/mdm/policy-csp-browser#browser-disablelockdownofstartpages)
</dt> <dd> <dl> <dt>

<span data-ttu-id="54a5c-171">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="54a5c-171">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="54a5c-172">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="54a5c-172">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="54a5c-173">EnterpriseModeSiteList</span><span class="sxs-lookup"><span data-stu-id="54a5c-173">EnterpriseModeSiteList</span></span>](/windows/client-management/mdm/policy-csp-browser#browser-enterprisemodesitelist)
</dt> <dd> <dl> <dt>

<span data-ttu-id="54a5c-174">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="54a5c-174">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="54a5c-175">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="54a5c-175">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="54a5c-176">EnterpriseSiteListServiceUrl</span><span class="sxs-lookup"><span data-stu-id="54a5c-176">EnterpriseSiteListServiceUrl</span></span>](/windows/client-management/mdm/policy-csp-browser#browser-enterprisesitelistserviceurl)
</dt> <dd> <dl> <dt>

<span data-ttu-id="54a5c-177">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="54a5c-177">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="54a5c-178">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="54a5c-178">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="54a5c-179">Accueil</span><span class="sxs-lookup"><span data-stu-id="54a5c-179">Homepages</span></span>](/windows/client-management/mdm/policy-csp-browser#browser-homepages)
</dt> <dd> <dl> <dt>

<span data-ttu-id="54a5c-180">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="54a5c-180">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="54a5c-181">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="54a5c-181">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="54a5c-182">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="54a5c-182">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="54a5c-183">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="54a5c-183">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="54a5c-184">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="54a5c-184">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="54a5c-185">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="54a5c-185">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="54a5c-186">Identifie le nom du nœud parent.</span><span class="sxs-lookup"><span data-stu-id="54a5c-186">Identifies the name of the parent node.</span></span> <span data-ttu-id="54a5c-187">Pour cette classe, la chaîne est « Browser ».</span><span class="sxs-lookup"><span data-stu-id="54a5c-187">For this class, the string is "Browser".</span></span>

</dd> <dt>

[<span data-ttu-id="54a5c-188">LockdownFavorites</span><span class="sxs-lookup"><span data-stu-id="54a5c-188">LockdownFavorites</span></span>](/windows/client-management/mdm/policy-csp-browser#browser-lockdownfavorites)
</dt> <dd> <dl> <dt>

<span data-ttu-id="54a5c-189">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="54a5c-189">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="54a5c-190">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="54a5c-190">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="54a5c-191">**ID**</span><span class="sxs-lookup"><span data-stu-id="54a5c-191">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="54a5c-192">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="54a5c-192">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="54a5c-193">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="54a5c-193">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="54a5c-194">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="54a5c-194">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="54a5c-195">Décrit le chemin d’accès complet au nœud parent.</span><span class="sxs-lookup"><span data-stu-id="54a5c-195">Describes the full path to the parent node.</span></span> <span data-ttu-id="54a5c-196">Pour cette classe, la chaîne est « ./Vendor/MSFT/Policy/Result »</span><span class="sxs-lookup"><span data-stu-id="54a5c-196">For this class, the string is "./Vendor/MSFT/Policy/Result"</span></span>

</dd> <dt>

[<span data-ttu-id="54a5c-197">PreventAccessToAboutFlagsInMicrosoftEdge</span><span class="sxs-lookup"><span data-stu-id="54a5c-197">PreventAccessToAboutFlagsInMicrosoftEdge</span></span>](/windows/client-management/mdm/policy-csp-browser#browser-preventaccesstoaboutflagsinmicrosoftedge)
</dt> <dd> <dl> <dt>

<span data-ttu-id="54a5c-198">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="54a5c-198">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="54a5c-199">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="54a5c-199">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="54a5c-200">PreventFirstRunPage</span><span class="sxs-lookup"><span data-stu-id="54a5c-200">PreventFirstRunPage</span></span>](/windows/client-management/mdm/policy-csp-browser#browser-preventfirstrunpage)
</dt> <dd> <dl> <dt>

<span data-ttu-id="54a5c-201">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="54a5c-201">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="54a5c-202">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="54a5c-202">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="54a5c-203">PreventLiveTileDataCollection</span><span class="sxs-lookup"><span data-stu-id="54a5c-203">PreventLiveTileDataCollection</span></span>](/windows/client-management/mdm/policy-csp-browser#browser-preventlivetiledatacollection)
</dt> <dd> <dl> <dt>

<span data-ttu-id="54a5c-204">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="54a5c-204">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="54a5c-205">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="54a5c-205">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="54a5c-206">PreventSmartScreenPromptOverride</span><span class="sxs-lookup"><span data-stu-id="54a5c-206">PreventSmartScreenPromptOverride</span></span>](/windows/client-management/mdm/policy-csp-browser#browser-preventsmartscreenpromptoverride)
</dt> <dd> <dl> <dt>

<span data-ttu-id="54a5c-207">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="54a5c-207">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="54a5c-208">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="54a5c-208">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="54a5c-209">PreventSmartScreenPromptOverrideForFiles</span><span class="sxs-lookup"><span data-stu-id="54a5c-209">PreventSmartScreenPromptOverrideForFiles</span></span>](/windows/client-management/mdm/policy-csp-browser#browser-preventsmartscreenpromptoverrideforfiles)
</dt> <dd> <dl> <dt>

<span data-ttu-id="54a5c-210">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="54a5c-210">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="54a5c-211">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="54a5c-211">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="54a5c-212">PreventUsingLocalHostIPAddressForWebRTC</span><span class="sxs-lookup"><span data-stu-id="54a5c-212">PreventUsingLocalHostIPAddressForWebRTC</span></span>](/windows/client-management/mdm/policy-csp-browser#browser-preventusinglocalhostipaddressforwebrtc)
</dt> <dd> <dl> <dt>

<span data-ttu-id="54a5c-213">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="54a5c-213">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="54a5c-214">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="54a5c-214">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="54a5c-215">ProvisionFavorites</span><span class="sxs-lookup"><span data-stu-id="54a5c-215">ProvisionFavorites</span></span>](/windows/client-management/mdm/policy-csp-browser#browser-provisionfavorites)
</dt> <dd> <dl> <dt>

<span data-ttu-id="54a5c-216">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="54a5c-216">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="54a5c-217">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="54a5c-217">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="54a5c-218">SendIntranetTraffictoInternetExplorer</span><span class="sxs-lookup"><span data-stu-id="54a5c-218">SendIntranetTraffictoInternetExplorer</span></span>](/windows/client-management/mdm/policy-csp-browser#browser-sendintranettraffictointernetexplorer)
</dt> <dd> <dl> <dt>

<span data-ttu-id="54a5c-219">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="54a5c-219">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="54a5c-220">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="54a5c-220">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="54a5c-221">SetDefaultSearchEngine</span><span class="sxs-lookup"><span data-stu-id="54a5c-221">SetDefaultSearchEngine</span></span>](/windows/client-management/mdm/policy-csp-browser#browser-setdefaultsearchengine)
</dt> <dd> <dl> <dt>

<span data-ttu-id="54a5c-222">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="54a5c-222">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="54a5c-223">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="54a5c-223">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="54a5c-224">ShowMessageWhenOpeningSitesInInternetExplorer</span><span class="sxs-lookup"><span data-stu-id="54a5c-224">ShowMessageWhenOpeningSitesInInternetExplorer</span></span>](/windows/client-management/mdm/policy-csp-browser#browser-showmessagewhenopeningsitesininternetexplorer)
</dt> <dd> <dl> <dt>

<span data-ttu-id="54a5c-225">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="54a5c-225">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="54a5c-226">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="54a5c-226">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="54a5c-227">SyncFavoritesBetweenIEAndMicrosoftEdge</span><span class="sxs-lookup"><span data-stu-id="54a5c-227">SyncFavoritesBetweenIEAndMicrosoftEdge</span></span>](/windows/client-management/mdm/policy-csp-browser#browser-syncfavoritesbetweenieandmicrosoftedge)
</dt> <dd> <dl> <dt>

<span data-ttu-id="54a5c-228">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="54a5c-228">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="54a5c-229">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="54a5c-229">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="54a5c-230">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="54a5c-230">Requirements</span></span>



| <span data-ttu-id="54a5c-231">Condition requise</span><span class="sxs-lookup"><span data-stu-id="54a5c-231">Requirement</span></span> | <span data-ttu-id="54a5c-232">Valeur</span><span class="sxs-lookup"><span data-stu-id="54a5c-232">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="54a5c-233">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="54a5c-233">Minimum supported client</span></span><br/> | <span data-ttu-id="54a5c-234">Applications de \[ Bureau Windows 10 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="54a5c-234">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="54a5c-235">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="54a5c-235">Minimum supported server</span></span><br/> | <span data-ttu-id="54a5c-236">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="54a5c-236">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="54a5c-237">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="54a5c-237">Namespace</span></span><br/>                | <span data-ttu-id="54a5c-238">Racine DMMap de gestion des appareils mobiles \\ \\ \\</span><span class="sxs-lookup"><span data-stu-id="54a5c-238">Root\\CIMv2\\MDM\\DMMap</span></span><br/>                                                             |
| <span data-ttu-id="54a5c-239">MOF</span><span class="sxs-lookup"><span data-stu-id="54a5c-239">MOF</span></span><br/>                      | <dl> <span data-ttu-id="54a5c-240"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="54a5c-240"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="54a5c-241">DLL</span><span class="sxs-lookup"><span data-stu-id="54a5c-241">DLL</span></span><br/>                      | <dl> <span data-ttu-id="54a5c-242"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="54a5c-242"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="54a5c-243">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="54a5c-243">See also</span></span>

<dl> <dt>

[<span data-ttu-id="54a5c-244">Utilisation de scripts PowerShell avec le fournisseur de pont WMI</span><span class="sxs-lookup"><span data-stu-id="54a5c-244">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

