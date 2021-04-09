---
title: Classe MDM_SharedPC
description: La \_ classe SHAREDPC MDM est utilisée pour configurer les paramètres d’utilisation des PC partagés.
ms.assetid: 90985c4d-601e-4827-aee0-13524a69f759
keywords:
- Classe MDM_SharedPC
- Classe MDM_SharedPC, Description
topic_type:
- apiref
api_name:
- MDM_SharedPC
- MDM_SharedPC.InstanceID
- MDM_SharedPC.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8c7b515e4b794e2048ab26c8e1a32bfe7d3c4b50
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104032390"
---
# <a name="mdm_sharedpc-class"></a><span data-ttu-id="b3efd-105">\_Classe SHAREDPC MDM</span><span class="sxs-lookup"><span data-stu-id="b3efd-105">MDM\_SharedPC class</span></span>

<span data-ttu-id="b3efd-106">\[Certaines informations relatives aux produits précommercialisés peuvent être substantiellement modifiées avant leur commercialisation.</span><span class="sxs-lookup"><span data-stu-id="b3efd-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="b3efd-107">Microsoft ne donne aucune garantie, expresse ou implicite, concernant les informations fournies ici.\]</span><span class="sxs-lookup"><span data-stu-id="b3efd-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="b3efd-108">La \_ classe SHAREDPC MDM est utilisée pour configurer les paramètres d’utilisation des PC partagés.</span><span class="sxs-lookup"><span data-stu-id="b3efd-108">The MDM\_SharedPC class is used to configure settings for shared PC usage.</span></span>

<span data-ttu-id="b3efd-109">La syntaxe suivante issue du code MOF est simplifiée et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="b3efd-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="b3efd-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b3efd-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv1")]
class MDM_SharedPC
{
  string  InstanceID;
  string  ParentID;
  boolean EnableSharedPCMode;
  boolean SetEduPolicies;
  boolean SetPowerPolicies;
  sint32  MaintenanceStartTime;
  boolean SignInOnResume;
  sint32  SleepTimeout;
  boolean EnableAccountManager;
  sint32  AccountModel;
  sint32  DeletionPolicy;
  sint32  DiskLevelDeletion;
  sint32  DiskLevelCaching;
  boolean RestrictLocalStorage;
  string  KioskModeAUMID;
  string  KioskModeUserTileDisplayText;
  sint32  InactiveThreshold;
  sint32  MaxPageFileSizeMB;
};
```

## <a name="members"></a><span data-ttu-id="b3efd-111">Membres</span><span class="sxs-lookup"><span data-stu-id="b3efd-111">Members</span></span>

<span data-ttu-id="b3efd-112">La **classe \_ SharedPC MDM** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="b3efd-112">The **MDM\_SharedPC** class has these types of members:</span></span>

-   [<span data-ttu-id="b3efd-113">Propriétés</span><span class="sxs-lookup"><span data-stu-id="b3efd-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="b3efd-114">Propriétés</span><span class="sxs-lookup"><span data-stu-id="b3efd-114">Properties</span></span>

<span data-ttu-id="b3efd-115">La **classe \_ SharedPC MDM** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="b3efd-115">The **MDM\_SharedPC** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="b3efd-116">AccountModel</span><span class="sxs-lookup"><span data-stu-id="b3efd-116">AccountModel</span></span>](/windows/client-management/mdm/sharedpc-csp#accountmodel)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b3efd-117">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="b3efd-117">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="b3efd-118">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="b3efd-118">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="b3efd-119">Pour plus d’informations, consultez [SHAREDPC CSP](/windows/client-management/mdm/sharedpc-csp).</span><span class="sxs-lookup"><span data-stu-id="b3efd-119">For additional information, see [SharedPC CSP](/windows/client-management/mdm/sharedpc-csp).</span></span>

</dd> <dt>

[<span data-ttu-id="b3efd-120">DeletionPolicy</span><span class="sxs-lookup"><span data-stu-id="b3efd-120">DeletionPolicy</span></span>](/windows/client-management/mdm/sharedpc-csp#deletionpolicy)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b3efd-121">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="b3efd-121">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="b3efd-122">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="b3efd-122">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="b3efd-123">Pour plus d’informations, consultez [SHAREDPC CSP](/windows/client-management/mdm/sharedpc-csp).</span><span class="sxs-lookup"><span data-stu-id="b3efd-123">For additional information, see [SharedPC CSP](/windows/client-management/mdm/sharedpc-csp).</span></span>

</dd> <dt>

[<span data-ttu-id="b3efd-124">DiskLevelCaching</span><span class="sxs-lookup"><span data-stu-id="b3efd-124">DiskLevelCaching</span></span>](/windows/client-management/mdm/sharedpc-csp#disklevelcaching)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b3efd-125">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="b3efd-125">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="b3efd-126">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="b3efd-126">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="b3efd-127">Pour plus d’informations, consultez [SHAREDPC CSP](/windows/client-management/mdm/sharedpc-csp).</span><span class="sxs-lookup"><span data-stu-id="b3efd-127">For additional information, see [SharedPC CSP](/windows/client-management/mdm/sharedpc-csp).</span></span>

</dd> <dt>

[<span data-ttu-id="b3efd-128">DiskLevelDeletion</span><span class="sxs-lookup"><span data-stu-id="b3efd-128">DiskLevelDeletion</span></span>](/windows/client-management/mdm/sharedpc-csp#diskleveldeletion)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b3efd-129">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="b3efd-129">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="b3efd-130">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="b3efd-130">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="b3efd-131">Pour plus d’informations, consultez [SHAREDPC CSP](/windows/client-management/mdm/sharedpc-csp).</span><span class="sxs-lookup"><span data-stu-id="b3efd-131">For additional information, see [SharedPC CSP](/windows/client-management/mdm/sharedpc-csp).</span></span>

</dd> <dt>

[<span data-ttu-id="b3efd-132">EnableAccountManager</span><span class="sxs-lookup"><span data-stu-id="b3efd-132">EnableAccountManager</span></span>](/windows/client-management/mdm/sharedpc-csp#enableaccountmanager)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b3efd-133">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="b3efd-133">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="b3efd-134">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="b3efd-134">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="b3efd-135">Pour plus d’informations, consultez [SHAREDPC CSP](/windows/client-management/mdm/sharedpc-csp).</span><span class="sxs-lookup"><span data-stu-id="b3efd-135">For additional information, see [SharedPC CSP](/windows/client-management/mdm/sharedpc-csp).</span></span>

</dd> <dt>

[<span data-ttu-id="b3efd-136">EnableSharedPCMode</span><span class="sxs-lookup"><span data-stu-id="b3efd-136">EnableSharedPCMode</span></span>](/windows/client-management/mdm/sharedpc-csp#enablesharedpcmode)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b3efd-137">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="b3efd-137">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="b3efd-138">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="b3efd-138">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="b3efd-139">Pour plus d’informations, consultez [SHAREDPC CSP](/windows/client-management/mdm/sharedpc-csp).</span><span class="sxs-lookup"><span data-stu-id="b3efd-139">For additional information, see [SharedPC CSP](/windows/client-management/mdm/sharedpc-csp).</span></span>

</dd> <dt>

[<span data-ttu-id="b3efd-140">InactiveThreshold</span><span class="sxs-lookup"><span data-stu-id="b3efd-140">InactiveThreshold</span></span>](/windows/client-management/mdm/sharedpc-csp#inactivethreshold)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b3efd-141">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="b3efd-141">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="b3efd-142">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="b3efd-142">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="b3efd-143">Pour plus d’informations, consultez [SHAREDPC CSP](/windows/client-management/mdm/sharedpc-csp).</span><span class="sxs-lookup"><span data-stu-id="b3efd-143">For additional information, see [SharedPC CSP](/windows/client-management/mdm/sharedpc-csp).</span></span>

</dd> <dt>

<span data-ttu-id="b3efd-144">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="b3efd-144">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b3efd-145">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="b3efd-145">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b3efd-146">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="b3efd-146">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b3efd-147">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="b3efd-147">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b3efd-148">KioskModeAUMID</span><span class="sxs-lookup"><span data-stu-id="b3efd-148">KioskModeAUMID</span></span>](/windows/client-management/mdm/sharedpc-csp#kioskmodeaumid)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b3efd-149">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="b3efd-149">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b3efd-150">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="b3efd-150">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="b3efd-151">Pour plus d’informations, consultez [SHAREDPC CSP](/windows/client-management/mdm/sharedpc-csp).</span><span class="sxs-lookup"><span data-stu-id="b3efd-151">For additional information, see [SharedPC CSP](/windows/client-management/mdm/sharedpc-csp).</span></span>

</dd> <dt>

[<span data-ttu-id="b3efd-152">KioskModeUserTileDisplayText</span><span class="sxs-lookup"><span data-stu-id="b3efd-152">KioskModeUserTileDisplayText</span></span>](/windows/client-management/mdm/sharedpc-csp#kioskmodeusertiledisplaytext)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b3efd-153">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="b3efd-153">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b3efd-154">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="b3efd-154">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="b3efd-155">Pour plus d’informations, consultez [SHAREDPC CSP](/windows/client-management/mdm/sharedpc-csp).</span><span class="sxs-lookup"><span data-stu-id="b3efd-155">For additional information, see [SharedPC CSP](/windows/client-management/mdm/sharedpc-csp).</span></span>

</dd> <dt>

[<span data-ttu-id="b3efd-156">MaintenanceStartTime</span><span class="sxs-lookup"><span data-stu-id="b3efd-156">MaintenanceStartTime</span></span>](/windows/client-management/mdm/sharedpc-csp#maintenancestarttime)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b3efd-157">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="b3efd-157">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="b3efd-158">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="b3efd-158">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="b3efd-159">Pour plus d’informations, consultez [SHAREDPC CSP](/windows/client-management/mdm/sharedpc-csp).</span><span class="sxs-lookup"><span data-stu-id="b3efd-159">For additional information, see [SharedPC CSP](/windows/client-management/mdm/sharedpc-csp).</span></span>

</dd> <dt>

[<span data-ttu-id="b3efd-160">MaxPageFileSizeMB</span><span class="sxs-lookup"><span data-stu-id="b3efd-160">MaxPageFileSizeMB</span></span>](/windows/client-management/mdm/sharedpc-csp#maxpagefilesizemb)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b3efd-161">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="b3efd-161">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="b3efd-162">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="b3efd-162">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="b3efd-163">Pour plus d’informations, consultez [SHAREDPC CSP](/windows/client-management/mdm/sharedpc-csp).</span><span class="sxs-lookup"><span data-stu-id="b3efd-163">For additional information, see [SharedPC CSP](/windows/client-management/mdm/sharedpc-csp).</span></span>

</dd> <dt>

<span data-ttu-id="b3efd-164">**ID**</span><span class="sxs-lookup"><span data-stu-id="b3efd-164">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b3efd-165">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="b3efd-165">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b3efd-166">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="b3efd-166">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b3efd-167">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="b3efd-167">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b3efd-168">RestrictLocalStorage</span><span class="sxs-lookup"><span data-stu-id="b3efd-168">RestrictLocalStorage</span></span>](/windows/client-management/mdm/sharedpc-csp#restrictlocalstorage)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b3efd-169">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="b3efd-169">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="b3efd-170">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="b3efd-170">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="b3efd-171">Pour plus d’informations, consultez [SHAREDPC CSP](/windows/client-management/mdm/sharedpc-csp).</span><span class="sxs-lookup"><span data-stu-id="b3efd-171">For additional information, see [SharedPC CSP](/windows/client-management/mdm/sharedpc-csp).</span></span>

</dd> <dt>

[<span data-ttu-id="b3efd-172">SetEduPolicies</span><span class="sxs-lookup"><span data-stu-id="b3efd-172">SetEduPolicies</span></span>](/windows/client-management/mdm/sharedpc-csp#setedupolicies)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b3efd-173">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="b3efd-173">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="b3efd-174">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="b3efd-174">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="b3efd-175">Pour plus d’informations, consultez [SHAREDPC CSP](/windows/client-management/mdm/sharedpc-csp).</span><span class="sxs-lookup"><span data-stu-id="b3efd-175">For additional information, see [SharedPC CSP](/windows/client-management/mdm/sharedpc-csp).</span></span>

</dd> <dt>

[<span data-ttu-id="b3efd-176">SetPowerPolicies</span><span class="sxs-lookup"><span data-stu-id="b3efd-176">SetPowerPolicies</span></span>](/windows/client-management/mdm/sharedpc-csp#setpowerpolicies)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b3efd-177">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="b3efd-177">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="b3efd-178">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="b3efd-178">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="b3efd-179">Pour plus d’informations, consultez [SHAREDPC CSP](/windows/client-management/mdm/sharedpc-csp).</span><span class="sxs-lookup"><span data-stu-id="b3efd-179">For additional information, see [SharedPC CSP](/windows/client-management/mdm/sharedpc-csp).</span></span>

</dd> <dt>

[<span data-ttu-id="b3efd-180">SignInOnResume</span><span class="sxs-lookup"><span data-stu-id="b3efd-180">SignInOnResume</span></span>](/windows/client-management/mdm/sharedpc-csp#signinonresume)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b3efd-181">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="b3efd-181">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="b3efd-182">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="b3efd-182">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="b3efd-183">Pour plus d’informations, consultez [SHAREDPC CSP](/windows/client-management/mdm/sharedpc-csp).</span><span class="sxs-lookup"><span data-stu-id="b3efd-183">For additional information, see [SharedPC CSP](/windows/client-management/mdm/sharedpc-csp).</span></span>

</dd> <dt>

[<span data-ttu-id="b3efd-184">SleepTimeout</span><span class="sxs-lookup"><span data-stu-id="b3efd-184">SleepTimeout</span></span>](/windows/client-management/mdm/sharedpc-csp#sleeptimeout)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b3efd-185">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="b3efd-185">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="b3efd-186">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="b3efd-186">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="b3efd-187">Pour plus d’informations, consultez [SHAREDPC CSP](/windows/client-management/mdm/sharedpc-csp).</span><span class="sxs-lookup"><span data-stu-id="b3efd-187">For additional information, see [SharedPC CSP](/windows/client-management/mdm/sharedpc-csp).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="b3efd-188">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b3efd-188">Requirements</span></span>



| <span data-ttu-id="b3efd-189">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b3efd-189">Requirement</span></span> | <span data-ttu-id="b3efd-190">Valeur</span><span class="sxs-lookup"><span data-stu-id="b3efd-190">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b3efd-191">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b3efd-191">Minimum supported client</span></span><br/> | <span data-ttu-id="b3efd-192">Applications de \[ Bureau Windows 10 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b3efd-192">Windows 10 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="b3efd-193">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b3efd-193">Minimum supported server</span></span><br/> | <span data-ttu-id="b3efd-194">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="b3efd-194">None supported</span></span><br/>                                                                       |
| <span data-ttu-id="b3efd-195">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="b3efd-195">Namespace</span></span><br/>                | <span data-ttu-id="b3efd-196">Racine dmmap de gestion des appareils mobiles \\ \\ \\</span><span class="sxs-lookup"><span data-stu-id="b3efd-196">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                              |
| <span data-ttu-id="b3efd-197">MOF</span><span class="sxs-lookup"><span data-stu-id="b3efd-197">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b3efd-198"><dt>DMWmiBridgeProv1. mof</dt></span><span class="sxs-lookup"><span data-stu-id="b3efd-198"><dt>DMWmiBridgeProv1.mof</dt></span></span> </dl> |
| <span data-ttu-id="b3efd-199">DLL</span><span class="sxs-lookup"><span data-stu-id="b3efd-199">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b3efd-200"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b3efd-200"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl>  |



 

