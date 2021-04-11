---
title: Classe MDM_Policy_Result01_Search02
description: La \_ classe Search02 de la stratégie MDM \_ Result01 \_ représente les stratégies de recherche disponibles.
ms.assetid: 3025753f-a3cc-430c-bc73-438085ef5c51
keywords:
- Classe MDM_Policy_Result01_Search02
- Classe MDM_Policy_Result01_Search02, Description
topic_type:
- apiref
api_name:
- MDM_Policy_Result01_Search02
- MDM_Policy_Result01_Search02.InstanceID
- MDM_Policy_Result01_Search02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 94a0e25e7f5aa47abcc2b39d9a30a764c5dc9c34
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104032558"
---
# <a name="mdm_policy_result01_search02-class"></a><span data-ttu-id="b6467-105">\_Classe Search02 de la stratégie MDM \_ Result01 \_</span><span class="sxs-lookup"><span data-stu-id="b6467-105">MDM\_Policy\_Result01\_Search02 class</span></span>

<span data-ttu-id="b6467-106">\[Certaines informations relatives aux produits précommercialisés peuvent être substantiellement modifiées avant leur commercialisation.</span><span class="sxs-lookup"><span data-stu-id="b6467-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="b6467-107">Microsoft ne donne aucune garantie, expresse ou implicite, concernant les informations fournies ici.\]</span><span class="sxs-lookup"><span data-stu-id="b6467-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="b6467-108">La classe Search02 de la **\_ stratégie MDM \_ Result01 \_** représente les stratégies de recherche disponibles.</span><span class="sxs-lookup"><span data-stu-id="b6467-108">The **MDM\_Policy\_Result01\_Search02** class represents the search policies available.</span></span>

<span data-ttu-id="b6467-109">La syntaxe suivante issue du code MOF est simplifiée et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="b6467-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="b6467-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b6467-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Result01_Search02
{
  string InstanceID;
  string ParentID;
  sint32 AllowCloudSearch;
  sint32 AllowSearchToUseLocation;
  sint32 AllowStoringImagesFromVisionSearch;
  sint32 AlwaysUseAutoLangDetection;
  sint32 PreventRemoteQueries;
  sint32 PreventIndexingLowDiskSpaceMB;
  sint32 DisableRemovableDriveIndexing;
  sint32 DisableBackoff;
  sint32 AllowUsingDiacritics;
  sint32 AllowWindowsIndexer;
  sint32 AllowIndexingEncryptedStoresOrItems;
};
```

## <a name="members"></a><span data-ttu-id="b6467-111">Membres</span><span class="sxs-lookup"><span data-stu-id="b6467-111">Members</span></span>

<span data-ttu-id="b6467-112">La **classe \_ \_ Result01 \_ Search02 de la stratégie MDM** a les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="b6467-112">The **MDM\_Policy\_Result01\_Search02** class has these types of members:</span></span>

-   [<span data-ttu-id="b6467-113">Propriétés</span><span class="sxs-lookup"><span data-stu-id="b6467-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="b6467-114">Propriétés</span><span class="sxs-lookup"><span data-stu-id="b6467-114">Properties</span></span>

<span data-ttu-id="b6467-115">La **classe \_ \_ Result01 \_ Search02 de la stratégie MDM** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="b6467-115">The **MDM\_Policy\_Result01\_Search02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="b6467-116">AllowCloudSearch</span><span class="sxs-lookup"><span data-stu-id="b6467-116">AllowCloudSearch</span></span>](/windows/client-management/mdm/policy-csp-search#search-allowcloudsearch)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b6467-117">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="b6467-117">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="b6467-118">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="b6467-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b6467-119">AllowIndexingEncryptedStoresOrItems</span><span class="sxs-lookup"><span data-stu-id="b6467-119">AllowIndexingEncryptedStoresOrItems</span></span>](/windows/client-management/mdm/policy-csp-search#search-allowindexingencryptedstoresoritems)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b6467-120">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="b6467-120">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="b6467-121">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="b6467-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b6467-122">AllowSearchToUseLocation</span><span class="sxs-lookup"><span data-stu-id="b6467-122">AllowSearchToUseLocation</span></span>](/windows/client-management/mdm/policy-csp-search#search-allowsearchtouselocation)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b6467-123">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="b6467-123">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="b6467-124">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="b6467-124">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b6467-125">AllowStoringImagesFromVisionSearch</span><span class="sxs-lookup"><span data-stu-id="b6467-125">AllowStoringImagesFromVisionSearch</span></span>](/windows/client-management/mdm/policy-csp-search#search-allowstoringimagesfromvisionsearch)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b6467-126">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="b6467-126">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="b6467-127">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="b6467-127">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b6467-128">AllowUsingDiacritics</span><span class="sxs-lookup"><span data-stu-id="b6467-128">AllowUsingDiacritics</span></span>](/windows/client-management/mdm/policy-csp-search#search-allowusingdiacritics)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b6467-129">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="b6467-129">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="b6467-130">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="b6467-130">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b6467-131">AllowWindowsIndexer</span><span class="sxs-lookup"><span data-stu-id="b6467-131">AllowWindowsIndexer</span></span>](/windows/client-management/mdm/policy-csp-search#search-allowwindowsindexer)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b6467-132">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="b6467-132">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="b6467-133">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="b6467-133">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b6467-134">AlwaysUseAutoLangDetection</span><span class="sxs-lookup"><span data-stu-id="b6467-134">AlwaysUseAutoLangDetection</span></span>](/windows/client-management/mdm/policy-csp-search#search-alwaysuseautolangdetection)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b6467-135">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="b6467-135">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="b6467-136">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="b6467-136">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b6467-137">DisableBackoff</span><span class="sxs-lookup"><span data-stu-id="b6467-137">DisableBackoff</span></span>](/windows/client-management/mdm/policy-csp-search#search-disablebackoff)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b6467-138">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="b6467-138">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="b6467-139">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="b6467-139">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b6467-140">DisableRemovableDriveIndexing</span><span class="sxs-lookup"><span data-stu-id="b6467-140">DisableRemovableDriveIndexing</span></span>](/windows/client-management/mdm/policy-csp-search#search-disableremovabledriveindexing)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b6467-141">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="b6467-141">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="b6467-142">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="b6467-142">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="b6467-143">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="b6467-143">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b6467-144">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="b6467-144">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b6467-145">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="b6467-145">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b6467-146">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="b6467-146">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="b6467-147">Identifie le nom du nœud parent.</span><span class="sxs-lookup"><span data-stu-id="b6467-147">Identifies the name of the parent node.</span></span> <span data-ttu-id="b6467-148">Pour cette classe, la chaîne est « Search ».</span><span class="sxs-lookup"><span data-stu-id="b6467-148">For this class, the string is "Search".</span></span>

</dd> <dt>

<span data-ttu-id="b6467-149">**ID**</span><span class="sxs-lookup"><span data-stu-id="b6467-149">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b6467-150">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="b6467-150">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b6467-151">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="b6467-151">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b6467-152">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="b6467-152">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="b6467-153">Décrit le chemin d’accès complet au nœud parent.</span><span class="sxs-lookup"><span data-stu-id="b6467-153">Describes the full path to the parent node.</span></span> <span data-ttu-id="b6467-154">Pour cette classe, la chaîne est « ./Vendor/MSFT/Policy/Result »</span><span class="sxs-lookup"><span data-stu-id="b6467-154">For this class, the string is "./Vendor/MSFT/Policy/Result"</span></span>

</dd> <dt>

[<span data-ttu-id="b6467-155">PreventIndexingLowDiskSpaceMB</span><span class="sxs-lookup"><span data-stu-id="b6467-155">PreventIndexingLowDiskSpaceMB</span></span>](/windows/client-management/mdm/policy-csp-search#search-preventindexinglowdiskspacemb)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b6467-156">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="b6467-156">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="b6467-157">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="b6467-157">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b6467-158">PreventRemoteQueries</span><span class="sxs-lookup"><span data-stu-id="b6467-158">PreventRemoteQueries</span></span>](/windows/client-management/mdm/policy-csp-search#search-preventremotequeries)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b6467-159">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="b6467-159">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="b6467-160">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="b6467-160">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="b6467-161">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b6467-161">Requirements</span></span>



| <span data-ttu-id="b6467-162">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b6467-162">Requirement</span></span> | <span data-ttu-id="b6467-163">Valeur</span><span class="sxs-lookup"><span data-stu-id="b6467-163">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b6467-164">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b6467-164">Minimum supported client</span></span><br/> | <span data-ttu-id="b6467-165">Applications de \[ Bureau Windows 10 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b6467-165">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="b6467-166">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b6467-166">Minimum supported server</span></span><br/> | <span data-ttu-id="b6467-167">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="b6467-167">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="b6467-168">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="b6467-168">Namespace</span></span><br/>                | <span data-ttu-id="b6467-169">Racine DMMap de gestion des appareils mobiles \\ \\ \\</span><span class="sxs-lookup"><span data-stu-id="b6467-169">Root\\CIMv2\\MDM\\DMMap</span></span><br/>                                                             |
| <span data-ttu-id="b6467-170">MOF</span><span class="sxs-lookup"><span data-stu-id="b6467-170">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b6467-171"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="b6467-171"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="b6467-172">DLL</span><span class="sxs-lookup"><span data-stu-id="b6467-172">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b6467-173"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b6467-173"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b6467-174">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b6467-174">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b6467-175">Utilisation de scripts PowerShell avec le fournisseur de pont WMI</span><span class="sxs-lookup"><span data-stu-id="b6467-175">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

