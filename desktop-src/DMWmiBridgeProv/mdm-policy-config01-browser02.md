---
title: Classe MDM_Policy_Config01_Browser02
description: La \_ classe Config01 Browser02 de la stratégie MDM \_ \_ représente les stratégies de navigateur disponibles.
ms.assetid: 296e3be4-3bc1-4e06-9e31-532639a0b912
keywords:
- Classe MDM_Policy_Config01_Browser02
- Classe MDM_Policy_Config01_Browser02, Description
topic_type:
- apiref
api_name:
- MDM_Policy_Config01_Browser02
- MDM_Policy_Config01_Browser02.InstanceID
- MDM_Policy_Config01_Browser02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ba68b4d3f6798a448447e7773dc299977c54434c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104032668"
---
# <a name="mdm_policy_config01_browser02-class"></a><span data-ttu-id="0c7b6-105">\_Classe Browser02 de la stratégie MDM \_ Config01 \_</span><span class="sxs-lookup"><span data-stu-id="0c7b6-105">MDM\_Policy\_Config01\_Browser02 class</span></span>

<span data-ttu-id="0c7b6-106">\[Certaines informations relatives aux produits précommercialisés peuvent être substantiellement modifiées avant leur commercialisation.</span><span class="sxs-lookup"><span data-stu-id="0c7b6-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="0c7b6-107">Microsoft ne donne aucune garantie, expresse ou implicite, concernant les informations fournies ici.\]</span><span class="sxs-lookup"><span data-stu-id="0c7b6-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="0c7b6-108">La **classe \_ \_ Config01 \_ Browser02 de la stratégie MDM** représente les stratégies de navigateur disponibles.</span><span class="sxs-lookup"><span data-stu-id="0c7b6-108">The **MDM\_Policy\_Config01\_Browser02** class represents the browser policies available.</span></span>

<span data-ttu-id="0c7b6-109">La syntaxe suivante issue du code MOF est simplifiée et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="0c7b6-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="0c7b6-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0c7b6-110">Syntax</span></span>

``` syntax
[InPartition("local-system", "local-user"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Config01_Browser02
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

## <a name="members"></a><span data-ttu-id="0c7b6-111">Membres</span><span class="sxs-lookup"><span data-stu-id="0c7b6-111">Members</span></span>

<span data-ttu-id="0c7b6-112">La **classe \_ \_ Config01 \_ Browser02 de la stratégie MDM** a les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="0c7b6-112">The **MDM\_Policy\_Config01\_Browser02** class has these types of members:</span></span>

-   [<span data-ttu-id="0c7b6-113">Propriétés</span><span class="sxs-lookup"><span data-stu-id="0c7b6-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="0c7b6-114">Propriétés</span><span class="sxs-lookup"><span data-stu-id="0c7b6-114">Properties</span></span>

<span data-ttu-id="0c7b6-115">La **classe \_ \_ Config01 \_ Browser02 de la stratégie MDM** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="0c7b6-115">The **MDM\_Policy\_Config01\_Browser02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="0c7b6-116">AllowAddressBarDropdown</span><span class="sxs-lookup"><span data-stu-id="0c7b6-116">AllowAddressBarDropdown</span></span>](/windows/client-management/mdm/policy-csp-browser#browser-allowaddressbardropdown)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0c7b6-117">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="0c7b6-117">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="0c7b6-118">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="0c7b6-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0c7b6-119">AllowAutofill</span><span class="sxs-lookup"><span data-stu-id="0c7b6-119">AllowAutofill</span></span>](/windows/client-management/mdm/policy-configuration-service-provider)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0c7b6-120">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="0c7b6-120">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="0c7b6-121">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="0c7b6-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0c7b6-122">AllowCookies</span><span class="sxs-lookup"><span data-stu-id="0c7b6-122">AllowCookies</span></span>](/windows/client-management/mdm/policy-configuration-service-provider)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0c7b6-123">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="0c7b6-123">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="0c7b6-124">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="0c7b6-124">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0c7b6-125">AllowDeveloperTools</span><span class="sxs-lookup"><span data-stu-id="0c7b6-125">AllowDeveloperTools</span></span>](/windows/client-management/mdm/policy-configuration-service-provider)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0c7b6-126">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="0c7b6-126">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="0c7b6-127">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="0c7b6-127">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0c7b6-128">AllowDoNotTrack</span><span class="sxs-lookup"><span data-stu-id="0c7b6-128">AllowDoNotTrack</span></span>](/windows/client-management/mdm/policy-csp-browser#browser-allowdonottrack)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0c7b6-129">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="0c7b6-129">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="0c7b6-130">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="0c7b6-130">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0c7b6-131">AllowExtensions</span><span class="sxs-lookup"><span data-stu-id="0c7b6-131">AllowExtensions</span></span>](/windows/client-management/mdm/policy-csp-browser#browser-allowextensions)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0c7b6-132">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="0c7b6-132">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="0c7b6-133">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="0c7b6-133">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0c7b6-134">AllowFlash</span><span class="sxs-lookup"><span data-stu-id="0c7b6-134">AllowFlash</span></span>](/windows/client-management/mdm/policy-csp-browser#browser-allowflash)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0c7b6-135">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="0c7b6-135">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="0c7b6-136">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="0c7b6-136">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0c7b6-137">AllowFlashClickToRun</span><span class="sxs-lookup"><span data-stu-id="0c7b6-137">AllowFlashClickToRun</span></span>](/windows/client-management/mdm/policy-csp-browser#browser-allowflashclicktorun)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0c7b6-138">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="0c7b6-138">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="0c7b6-139">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="0c7b6-139">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0c7b6-140">AllowInPrivate</span><span class="sxs-lookup"><span data-stu-id="0c7b6-140">AllowInPrivate</span></span>](/windows/client-management/mdm/policy-csp-browser#browser-allowinprivate)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0c7b6-141">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="0c7b6-141">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="0c7b6-142">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="0c7b6-142">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0c7b6-143">AllowMicrosoftCompatibilityList</span><span class="sxs-lookup"><span data-stu-id="0c7b6-143">AllowMicrosoftCompatibilityList</span></span>](/windows/client-management/mdm/policy-csp-browser#browser-allowmicrosoftcompatibilitylist)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0c7b6-144">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="0c7b6-144">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="0c7b6-145">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="0c7b6-145">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0c7b6-146">AllowPasswordManager</span><span class="sxs-lookup"><span data-stu-id="0c7b6-146">AllowPasswordManager</span></span>](/windows/client-management/mdm/policy-csp-browser#browser-allowpasswordmanager)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0c7b6-147">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="0c7b6-147">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="0c7b6-148">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="0c7b6-148">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0c7b6-149">AllowPopups</span><span class="sxs-lookup"><span data-stu-id="0c7b6-149">AllowPopups</span></span>](/windows/client-management/mdm/policy-csp-browser#browser-allowpopups)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0c7b6-150">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="0c7b6-150">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="0c7b6-151">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="0c7b6-151">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0c7b6-152">AllowSearchEngineCustomization</span><span class="sxs-lookup"><span data-stu-id="0c7b6-152">AllowSearchEngineCustomization</span></span>](/windows/client-management/mdm/policy-csp-browser#browser-allowsearchenginecustomization)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0c7b6-153">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="0c7b6-153">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="0c7b6-154">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="0c7b6-154">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0c7b6-155">AllowSearchSuggestionsinAddressBar</span><span class="sxs-lookup"><span data-stu-id="0c7b6-155">AllowSearchSuggestionsinAddressBar</span></span>](/windows/client-management/mdm/policy-csp-browser#browser-allowsearchsuggestionsinaddressbar)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0c7b6-156">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="0c7b6-156">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="0c7b6-157">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="0c7b6-157">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0c7b6-158">AllowSmartScreen</span><span class="sxs-lookup"><span data-stu-id="0c7b6-158">AllowSmartScreen</span></span>](/windows/client-management/mdm/policy-csp-browser#browser-allowsmartscreen)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0c7b6-159">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="0c7b6-159">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="0c7b6-160">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="0c7b6-160">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0c7b6-161">AlwaysEnableBooksLibrary</span><span class="sxs-lookup"><span data-stu-id="0c7b6-161">AlwaysEnableBooksLibrary</span></span>](/windows/client-management/mdm/policy-csp-browser#browser-alwaysenablebookslibrary)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0c7b6-162">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="0c7b6-162">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="0c7b6-163">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="0c7b6-163">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0c7b6-164">ClearBrowsingDataOnExit</span><span class="sxs-lookup"><span data-stu-id="0c7b6-164">ClearBrowsingDataOnExit</span></span>](/windows/client-management/mdm/policy-csp-browser#browser-clearbrowsingdataonexit)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0c7b6-165">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="0c7b6-165">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="0c7b6-166">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="0c7b6-166">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0c7b6-167">ConfigureAdditionalSearchEngines</span><span class="sxs-lookup"><span data-stu-id="0c7b6-167">ConfigureAdditionalSearchEngines</span></span>](/windows/client-management/mdm/policy-csp-browser#browser-configureadditionalsearchengines)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0c7b6-168">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="0c7b6-168">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0c7b6-169">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="0c7b6-169">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0c7b6-170">DisableLockdownOfStartPages</span><span class="sxs-lookup"><span data-stu-id="0c7b6-170">DisableLockdownOfStartPages</span></span>](/windows/client-management/mdm/policy-csp-browser#browser-disablelockdownofstartpages)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0c7b6-171">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="0c7b6-171">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="0c7b6-172">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="0c7b6-172">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0c7b6-173">EnterpriseModeSiteList</span><span class="sxs-lookup"><span data-stu-id="0c7b6-173">EnterpriseModeSiteList</span></span>](/windows/client-management/mdm/policy-csp-browser#browser-enterprisemodesitelist)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0c7b6-174">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="0c7b6-174">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0c7b6-175">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="0c7b6-175">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0c7b6-176">EnterpriseSiteListServiceUrl</span><span class="sxs-lookup"><span data-stu-id="0c7b6-176">EnterpriseSiteListServiceUrl</span></span>](/windows/client-management/mdm/policy-csp-browser#browser-enterprisesitelistserviceurl)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0c7b6-177">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="0c7b6-177">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0c7b6-178">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="0c7b6-178">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0c7b6-179">Accueil</span><span class="sxs-lookup"><span data-stu-id="0c7b6-179">Homepages</span></span>](/windows/client-management/mdm/policy-csp-browser#browser-homepages)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0c7b6-180">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="0c7b6-180">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0c7b6-181">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="0c7b6-181">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="0c7b6-182">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="0c7b6-182">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0c7b6-183">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="0c7b6-183">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0c7b6-184">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="0c7b6-184">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0c7b6-185">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="0c7b6-185">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="0c7b6-186">Identifie le nom du nœud parent.</span><span class="sxs-lookup"><span data-stu-id="0c7b6-186">Identifies the name of the parent node.</span></span> <span data-ttu-id="0c7b6-187">Pour cette classe, la chaîne est « Browser ».</span><span class="sxs-lookup"><span data-stu-id="0c7b6-187">For this class, the string is "Browser".</span></span>

</dd> <dt>

[<span data-ttu-id="0c7b6-188">LockdownFavorites</span><span class="sxs-lookup"><span data-stu-id="0c7b6-188">LockdownFavorites</span></span>](/windows/client-management/mdm/policy-csp-browser#browser-lockdownfavorites)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0c7b6-189">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="0c7b6-189">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="0c7b6-190">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="0c7b6-190">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="0c7b6-191">**ID**</span><span class="sxs-lookup"><span data-stu-id="0c7b6-191">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0c7b6-192">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="0c7b6-192">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0c7b6-193">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="0c7b6-193">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0c7b6-194">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="0c7b6-194">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="0c7b6-195">Décrit le chemin d’accès complet au nœud parent.</span><span class="sxs-lookup"><span data-stu-id="0c7b6-195">Describes the full path to the parent node.</span></span> <span data-ttu-id="0c7b6-196">Pour cette classe, la chaîne est « ./Vendor/MSFT/Policy/Config »</span><span class="sxs-lookup"><span data-stu-id="0c7b6-196">For this class, the string is "./Vendor/MSFT/Policy/Config"</span></span>

</dd> <dt>

[<span data-ttu-id="0c7b6-197">PreventAccessToAboutFlagsInMicrosoftEdge</span><span class="sxs-lookup"><span data-stu-id="0c7b6-197">PreventAccessToAboutFlagsInMicrosoftEdge</span></span>](/windows/client-management/mdm/policy-csp-browser#browser-preventaccesstoaboutflagsinmicrosoftedge)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0c7b6-198">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="0c7b6-198">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="0c7b6-199">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="0c7b6-199">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0c7b6-200">PreventFirstRunPage</span><span class="sxs-lookup"><span data-stu-id="0c7b6-200">PreventFirstRunPage</span></span>](/windows/client-management/mdm/policy-csp-browser#browser-preventfirstrunpage)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0c7b6-201">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="0c7b6-201">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="0c7b6-202">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="0c7b6-202">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0c7b6-203">PreventLiveTileDataCollection</span><span class="sxs-lookup"><span data-stu-id="0c7b6-203">PreventLiveTileDataCollection</span></span>](/windows/client-management/mdm/policy-csp-browser#browser-preventlivetiledatacollection)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0c7b6-204">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="0c7b6-204">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="0c7b6-205">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="0c7b6-205">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0c7b6-206">PreventSmartScreenPromptOverride</span><span class="sxs-lookup"><span data-stu-id="0c7b6-206">PreventSmartScreenPromptOverride</span></span>](/windows/client-management/mdm/policy-csp-browser#browser-preventsmartscreenpromptoverride)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0c7b6-207">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="0c7b6-207">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="0c7b6-208">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="0c7b6-208">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0c7b6-209">PreventSmartScreenPromptOverrideForFiles</span><span class="sxs-lookup"><span data-stu-id="0c7b6-209">PreventSmartScreenPromptOverrideForFiles</span></span>](/windows/client-management/mdm/policy-csp-browser#browser-preventsmartscreenpromptoverrideforfiles)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0c7b6-210">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="0c7b6-210">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="0c7b6-211">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="0c7b6-211">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0c7b6-212">PreventUsingLocalHostIPAddressForWebRTC</span><span class="sxs-lookup"><span data-stu-id="0c7b6-212">PreventUsingLocalHostIPAddressForWebRTC</span></span>](/windows/client-management/mdm/policy-csp-browser#browser-preventusinglocalhostipaddressforwebrtc)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0c7b6-213">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="0c7b6-213">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="0c7b6-214">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="0c7b6-214">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0c7b6-215">ProvisionFavorites</span><span class="sxs-lookup"><span data-stu-id="0c7b6-215">ProvisionFavorites</span></span>](/windows/client-management/mdm/policy-csp-browser#browser-provisionfavorites)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0c7b6-216">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="0c7b6-216">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0c7b6-217">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="0c7b6-217">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0c7b6-218">SendIntranetTraffictoInternetExplorer</span><span class="sxs-lookup"><span data-stu-id="0c7b6-218">SendIntranetTraffictoInternetExplorer</span></span>](/windows/client-management/mdm/policy-csp-browser#browser-sendintranettraffictointernetexplorer)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0c7b6-219">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="0c7b6-219">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="0c7b6-220">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="0c7b6-220">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0c7b6-221">SetDefaultSearchEngine</span><span class="sxs-lookup"><span data-stu-id="0c7b6-221">SetDefaultSearchEngine</span></span>](/windows/client-management/mdm/policy-csp-browser#browser-setdefaultsearchengine)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0c7b6-222">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="0c7b6-222">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0c7b6-223">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="0c7b6-223">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0c7b6-224">ShowMessageWhenOpeningSitesInInternetExplorer</span><span class="sxs-lookup"><span data-stu-id="0c7b6-224">ShowMessageWhenOpeningSitesInInternetExplorer</span></span>](/windows/client-management/mdm/policy-csp-browser#browser-showmessagewhenopeningsitesininternetexplorer)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0c7b6-225">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="0c7b6-225">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="0c7b6-226">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="0c7b6-226">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0c7b6-227">SyncFavoritesBetweenIEAndMicrosoftEdge</span><span class="sxs-lookup"><span data-stu-id="0c7b6-227">SyncFavoritesBetweenIEAndMicrosoftEdge</span></span>](/windows/client-management/mdm/policy-csp-browser#browser-syncfavoritesbetweenieandmicrosoftedge)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0c7b6-228">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="0c7b6-228">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="0c7b6-229">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="0c7b6-229">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="0c7b6-230">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0c7b6-230">Requirements</span></span>



| <span data-ttu-id="0c7b6-231">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0c7b6-231">Requirement</span></span> | <span data-ttu-id="0c7b6-232">Valeur</span><span class="sxs-lookup"><span data-stu-id="0c7b6-232">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0c7b6-233">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0c7b6-233">Minimum supported client</span></span><br/> | <span data-ttu-id="0c7b6-234">Applications de \[ Bureau Windows 10 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="0c7b6-234">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="0c7b6-235">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0c7b6-235">Minimum supported server</span></span><br/> | <span data-ttu-id="0c7b6-236">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="0c7b6-236">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="0c7b6-237">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="0c7b6-237">Namespace</span></span><br/>                | <span data-ttu-id="0c7b6-238">Racine DMMap de gestion des appareils mobiles \\ \\ \\</span><span class="sxs-lookup"><span data-stu-id="0c7b6-238">Root\\CIMv2\\MDM\\DMMap</span></span><br/>                                                             |
| <span data-ttu-id="0c7b6-239">MOF</span><span class="sxs-lookup"><span data-stu-id="0c7b6-239">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0c7b6-240"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="0c7b6-240"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="0c7b6-241">DLL</span><span class="sxs-lookup"><span data-stu-id="0c7b6-241">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0c7b6-242"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0c7b6-242"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0c7b6-243">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0c7b6-243">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0c7b6-244">Utilisation de scripts PowerShell avec le fournisseur de pont WMI</span><span class="sxs-lookup"><span data-stu-id="0c7b6-244">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

