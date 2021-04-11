---
description: Décrit un appareil de Module de plateforme sécurisée (TPM) (TPM).
ms.assetid: c923106f-126e-4e7e-822a-2fb715bbbc26
title: Classe CIM_TPM
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_TPM
- CIM_TPM.TPMSpecMajorVersion
- CIM_TPM.TPMSpecMinorVersion
- CIM_TPM.TPMManafucturerMajorRevision
- CIM_TPM.TPMManufacturerMinorRevision
- CIM_TPM.TPMManufacturerInfo
- CIM_TPM.TPMManufacturerId
- CIM_TPM.TPMState
- CIM_TPM.TransitioningToTPMState
- CIM_TPM.AvailableRequestedTPMStates
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 0f2d35d42e864a247ca042ec81813ff7d1ac5c35
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104034326"
---
# <a name="cim_tpm-class"></a><span data-ttu-id="26ed6-103">\_Classe TPM CIM</span><span class="sxs-lookup"><span data-stu-id="26ed6-103">CIM\_TPM class</span></span>

<span data-ttu-id="26ed6-104">Décrit un appareil de Module de plateforme sécurisée (TPM) (TPM).</span><span class="sxs-lookup"><span data-stu-id="26ed6-104">Describes a Trusted Platform Module (TPM) device.</span></span>

## <a name="syntax"></a><span data-ttu-id="26ed6-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="26ed6-105">Syntax</span></span>

``` syntax
[Experimental, Abstract, Version("2.21.0"), UMLPackagePath("CIM::Device::TPM"), AMENDMENT]
class CIM_TPM : CIM_LogicalDevice
{
  uint32 TPMSpecMajorVersion;
  uint32 TPMSpecMinorVersion;
  uint32 TPMManafucturerMajorRevision;
  uint32 TPMManufacturerMinorRevision;
  string TPMManufacturerInfo;
  uint32 TPMManufacturerId;
  uint16 TPMState;
  uint16 TransitioningToTPMState = 12;
  uint16 AvailableRequestedTPMStates[];
};
```

## <a name="members"></a><span data-ttu-id="26ed6-106">Membres</span><span class="sxs-lookup"><span data-stu-id="26ed6-106">Members</span></span>

<span data-ttu-id="26ed6-107">La classe de **\_ module de plateforme sécurisée CIM** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="26ed6-107">The **CIM\_TPM** class has these types of members:</span></span>

-   [<span data-ttu-id="26ed6-108">Méthodes</span><span class="sxs-lookup"><span data-stu-id="26ed6-108">Methods</span></span>](#methods)
-   [<span data-ttu-id="26ed6-109">Propriétés</span><span class="sxs-lookup"><span data-stu-id="26ed6-109">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="26ed6-110">Méthodes</span><span class="sxs-lookup"><span data-stu-id="26ed6-110">Methods</span></span>

<span data-ttu-id="26ed6-111">La classe de **\_ module de plateforme sécurisée CIM** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="26ed6-111">The **CIM\_TPM** class has these methods.</span></span>



| <span data-ttu-id="26ed6-112">Méthode</span><span class="sxs-lookup"><span data-stu-id="26ed6-112">Method</span></span>                                                         | <span data-ttu-id="26ed6-113">Description</span><span class="sxs-lookup"><span data-stu-id="26ed6-113">Description</span></span>                                                                                                             |
|:---------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="26ed6-114">**ChangeOwnerAuth**</span><span class="sxs-lookup"><span data-stu-id="26ed6-114">**ChangeOwnerAuth**</span></span>](cim-tpm-changeownerauth.md)             | <span data-ttu-id="26ed6-115">Modifie les informations d’identification d’autorisation du propriétaire d’un appareil TPM.</span><span class="sxs-lookup"><span data-stu-id="26ed6-115">Changes the owner authorization credential of a TPM device.</span></span><br/>                                                  |
| [<span data-ttu-id="26ed6-116">**RequestTPMStateChange**</span><span class="sxs-lookup"><span data-stu-id="26ed6-116">**RequestTPMStateChange**</span></span>](cim-tpm-requesttpmstatechange.md) | <span data-ttu-id="26ed6-117">Demande que l’état du module de plateforme sécurisée soit remplacé par la valeur spécifiée dans le paramètre **RequestedTPMState** .</span><span class="sxs-lookup"><span data-stu-id="26ed6-117">Requests that the state of the TPM be changed to the value specified in the **RequestedTPMState** parameter.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="26ed6-118">Propriétés</span><span class="sxs-lookup"><span data-stu-id="26ed6-118">Properties</span></span>

<span data-ttu-id="26ed6-119">La classe de **\_ module de plateforme sécurisée CIM** possède ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="26ed6-119">The **CIM\_TPM** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="26ed6-120">**AvailableRequestedTPMStates**</span><span class="sxs-lookup"><span data-stu-id="26ed6-120">**AvailableRequestedTPMStates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="26ed6-121">Type de données : tableau **UInt16**</span><span class="sxs-lookup"><span data-stu-id="26ed6-121">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="26ed6-122">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="26ed6-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="26ed6-123">Qualificateurs : [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ TPM**.**RequestTPMStateChange**, CIM \_ TPMCapabilities. RequestedTPMStatesSupported ")</span><span class="sxs-lookup"><span data-stu-id="26ed6-123">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_TPM**.**RequestTPMStateChange**, CIM\_TPMCapabilities.RequestedTPMStatesSupported")</span></span>
</dt> </dl>

<span data-ttu-id="26ed6-124">Valeurs possibles pour le paramètre *RequestedTPMState* de la méthode [**RequestTPMStateChange**](cim-tpm-requesttpmstatechange.md) .</span><span class="sxs-lookup"><span data-stu-id="26ed6-124">The possible values for the *RequestedTPMState* parameter of the [**RequestTPMStateChange**](cim-tpm-requesttpmstatechange.md) method.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="26ed6-125">**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="26ed6-125">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="S1_Enabled-Active-Owned"></span><span id="s1_enabled-active-owned"></span><span id="S1_ENABLED-ACTIVE-OWNED"></span>

<span data-ttu-id="26ed6-126">**S1 activé-propriétaire actif** (2)</span><span class="sxs-lookup"><span data-stu-id="26ed6-126">**S1 Enabled-Active-Owned** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="S2_Disabled-Active-Owned"></span><span id="s2_disabled-active-owned"></span><span id="S2_DISABLED-ACTIVE-OWNED"></span>

<span data-ttu-id="26ed6-127">**S2 désactivé-actif-propriétaire** (3)</span><span class="sxs-lookup"><span data-stu-id="26ed6-127">**S2 Disabled-Active-Owned** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="S3_Enabled-Inactive-Owned"></span><span id="s3_enabled-inactive-owned"></span><span id="S3_ENABLED-INACTIVE-OWNED"></span>

<span data-ttu-id="26ed6-128">**S3 activé-inactif-détenu** (4)</span><span class="sxs-lookup"><span data-stu-id="26ed6-128">**S3 Enabled-Inactive-Owned** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="S4_Disabled-Inactive-Owned"></span><span id="s4_disabled-inactive-owned"></span><span id="S4_DISABLED-INACTIVE-OWNED"></span>

<span data-ttu-id="26ed6-129">**S4 désactivé-inactif-détenu** (5)</span><span class="sxs-lookup"><span data-stu-id="26ed6-129">**S4 Disabled-Inactive-Owned** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="S5_Enabled-Active-Unowned"></span><span id="s5_enabled-active-unowned"></span><span id="S5_ENABLED-ACTIVE-UNOWNED"></span>

<span data-ttu-id="26ed6-130">**S5 activé-actif-sans propriétaire** (6)</span><span class="sxs-lookup"><span data-stu-id="26ed6-130">**S5 Enabled-Active-Unowned** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="S6_Disabled-Active-Unowned"></span><span id="s6_disabled-active-unowned"></span><span id="S6_DISABLED-ACTIVE-UNOWNED"></span>

<span data-ttu-id="26ed6-131">**S6 désactivé-actif-non détenu** (7)</span><span class="sxs-lookup"><span data-stu-id="26ed6-131">**S6 Disabled-Active-Unowned** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="S7_Enabled-Inactive-Unowned"></span><span id="s7_enabled-inactive-unowned"></span><span id="S7_ENABLED-INACTIVE-UNOWNED"></span>

<span data-ttu-id="26ed6-132">**S7 activé-inactif-sans propriétaire** (8)</span><span class="sxs-lookup"><span data-stu-id="26ed6-132">**S7 Enabled-Inactive-Unowned** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="S8_Disabled-Inactive-Unowned"></span><span id="s8_disabled-inactive-unowned"></span><span id="S8_DISABLED-INACTIVE-UNOWNED"></span>

<span data-ttu-id="26ed6-133">**S8 désactivé-inactif-sans propriétaire** (9)</span><span class="sxs-lookup"><span data-stu-id="26ed6-133">**S8 Disabled-Inactive-Unowned** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="26ed6-134">**DMTF réservé** (..)</span><span class="sxs-lookup"><span data-stu-id="26ed6-134">**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="26ed6-135">**Fournisseur réservé** (32768.. 65535)</span><span class="sxs-lookup"><span data-stu-id="26ed6-135">**Vendor Reserved** (32768..65535)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="26ed6-136">**TPMManafucturerMajorRevision**</span><span class="sxs-lookup"><span data-stu-id="26ed6-136">**TPMManafucturerMajorRevision**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="26ed6-137">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="26ed6-137">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="26ed6-138">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="26ed6-138">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="26ed6-139">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("TPM. TCG \| part 2 v1dot2 \| section 5,3 \| version \| revMajor»)</span><span class="sxs-lookup"><span data-stu-id="26ed6-139">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("TPM.TCG\|Part 2 v1dot2\|Section 5.3\|version\|revMajor")</span></span>
</dt> </dl>

<span data-ttu-id="26ed6-140">Révision majeure du fabricant du module de plateforme sécurisée.</span><span class="sxs-lookup"><span data-stu-id="26ed6-140">The manufacturer major revision of the TPM.</span></span>

</dd> <dt>

<span data-ttu-id="26ed6-141">**TPMManufacturerId**</span><span class="sxs-lookup"><span data-stu-id="26ed6-141">**TPMManufacturerId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="26ed6-142">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="26ed6-142">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="26ed6-143">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="26ed6-143">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="26ed6-144">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("TPM. TCG \| part 2 v1dot2 \| section 21,6 \| TPM \_ Cap \_ version \_ info \| tpmVendorID»)</span><span class="sxs-lookup"><span data-stu-id="26ed6-144">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("TPM.TCG\|Part 2 v1dot2\|Section 21.6\|TPM\_CAP\_VERSION\_INFO\|tpmVendorID")</span></span>
</dt> </dl>

<span data-ttu-id="26ed6-145">ID du fabricant du module de plateforme sécurisée.</span><span class="sxs-lookup"><span data-stu-id="26ed6-145">The TPM manufacturer ID.</span></span>

</dd> <dt>

<span data-ttu-id="26ed6-146">**TPMManufacturerInfo**</span><span class="sxs-lookup"><span data-stu-id="26ed6-146">**TPMManufacturerInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="26ed6-147">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="26ed6-147">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="26ed6-148">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="26ed6-148">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="26ed6-149">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("TPM. TCG \| , partie 2 v 1.2. TCG \| section 21,6 \| TPM \_ Cap \_ version \_ info \| vendorSpecific ")</span><span class="sxs-lookup"><span data-stu-id="26ed6-149">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("TPM.TCG\|Part 2 v1.2.TCG\|Section 21.6\|TPM\_CAP\_VERSION\_INFO\|vendorSpecific")</span></span>
</dt> </dl>

<span data-ttu-id="26ed6-150">Informations supplémentaires définies par le fabricant du module de plateforme sécurisée.</span><span class="sxs-lookup"><span data-stu-id="26ed6-150">The additional information defined by the TPM manufacturer.</span></span>

</dd> <dt>

<span data-ttu-id="26ed6-151">**TPMManufacturerMinorRevision**</span><span class="sxs-lookup"><span data-stu-id="26ed6-151">**TPMManufacturerMinorRevision**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="26ed6-152">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="26ed6-152">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="26ed6-153">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="26ed6-153">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="26ed6-154">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("TPM. TCG \| part 2 v1dot2 \| section 5,3 \| version \| revMinor»)</span><span class="sxs-lookup"><span data-stu-id="26ed6-154">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("TPM.TCG\|Part 2 v1dot2\|Section 5.3\|version\|revMinor")</span></span>
</dt> </dl>

<span data-ttu-id="26ed6-155">Révision mineure du fabricant du module de plateforme sécurisée.</span><span class="sxs-lookup"><span data-stu-id="26ed6-155">The manufacturer minor revision of the TPM.</span></span>

</dd> <dt>

<span data-ttu-id="26ed6-156">**TPMSpecMajorVersion**</span><span class="sxs-lookup"><span data-stu-id="26ed6-156">**TPMSpecMajorVersion**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="26ed6-157">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="26ed6-157">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="26ed6-158">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="26ed6-158">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="26ed6-159">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("TPM. TCG \| part 2 v1dot2 \| section 5,3 \| version \| majeure "," TSS. \|2.3.2.18 de niveau TCG 1 v 1.2 \| »)</span><span class="sxs-lookup"><span data-stu-id="26ed6-159">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("TPM.TCG\|Part 2 v1dot2\|Section 5.3\|version\|major", "TSS.TCG\|Level 1 v1.2\|Section 2.3.2.18")</span></span>
</dt> </dl>

<span data-ttu-id="26ed6-160">Version principale du module de plateforme sécurisée.</span><span class="sxs-lookup"><span data-stu-id="26ed6-160">The major version of the TPM.</span></span>

</dd> <dt>

<span data-ttu-id="26ed6-161">**TPMSpecMinorVersion**</span><span class="sxs-lookup"><span data-stu-id="26ed6-161">**TPMSpecMinorVersion**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="26ed6-162">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="26ed6-162">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="26ed6-163">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="26ed6-163">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="26ed6-164">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("TPM. TCG \| part 2 v1dot2 \| section 5,3 \| version \| mineure», «TSS. \|2.3.2.18 de niveau TCG 1 v 1.2 \| »)</span><span class="sxs-lookup"><span data-stu-id="26ed6-164">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("TPM.TCG\|Part 2 v1dot2\|Section 5.3\|version\|minor", "TSS.TCG\|Level 1 v1.2\|Section 2.3.2.18")</span></span>
</dt> </dl>

<span data-ttu-id="26ed6-165">Version mineure du module de plateforme sécurisée.</span><span class="sxs-lookup"><span data-stu-id="26ed6-165">The minor version of the TPM.</span></span>

</dd> <dt>

<span data-ttu-id="26ed6-166">**TPMState**</span><span class="sxs-lookup"><span data-stu-id="26ed6-166">**TPMState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="26ed6-167">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="26ed6-167">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="26ed6-168">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="26ed6-168">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="26ed6-169">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("TPM. TCG \| part 1 v1dot2 \| section 9,4 "," TPM. TCG \| part 2 v1dot2 \| section 7,1 \| \_ indicateurs permanents TPM \_ "), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**\_ TPM TPM**.**RequestTPMStateChange**","**CIM \_ TPM**.**TransitioningToTPMState**")</span><span class="sxs-lookup"><span data-stu-id="26ed6-169">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("TPM.TCG\|Part 1 v1dot2\|Section 9.4", "TPM.TCG\|Part 2 v1dot2\|Section 7.1\|TPM\_PERMANENT\_FLAGS"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_TPM**.**RequestTPMStateChange**", "**CIM\_TPM**.**TransitioningToTPMState**")</span></span>
</dt> </dl>

<span data-ttu-id="26ed6-170">État opérationnel du module de plateforme sécurisée.</span><span class="sxs-lookup"><span data-stu-id="26ed6-170">The operational state of the TPM.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="26ed6-171">**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="26ed6-171">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="S1_Enabled-Active-Owned"></span><span id="s1_enabled-active-owned"></span><span id="S1_ENABLED-ACTIVE-OWNED"></span>

<span data-ttu-id="26ed6-172">**S1 activé-propriétaire actif** (2)</span><span class="sxs-lookup"><span data-stu-id="26ed6-172">**S1 Enabled-Active-Owned** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="S2_Disabled-Active-Owned"></span><span id="s2_disabled-active-owned"></span><span id="S2_DISABLED-ACTIVE-OWNED"></span>

<span data-ttu-id="26ed6-173">**S2 désactivé-actif-propriétaire** (3)</span><span class="sxs-lookup"><span data-stu-id="26ed6-173">**S2 Disabled-Active-Owned** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="S3_Enabled-Inactive-Owned"></span><span id="s3_enabled-inactive-owned"></span><span id="S3_ENABLED-INACTIVE-OWNED"></span>

<span data-ttu-id="26ed6-174">**S3 activé-inactif-détenu** (4)</span><span class="sxs-lookup"><span data-stu-id="26ed6-174">**S3 Enabled-Inactive-Owned** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="S4_Disabled-Inactive-Owned"></span><span id="s4_disabled-inactive-owned"></span><span id="S4_DISABLED-INACTIVE-OWNED"></span>

<span data-ttu-id="26ed6-175">**S4 désactivé-inactif-détenu** (5)</span><span class="sxs-lookup"><span data-stu-id="26ed6-175">**S4 Disabled-Inactive-Owned** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="S5_Enabled-Active-Unowned"></span><span id="s5_enabled-active-unowned"></span><span id="S5_ENABLED-ACTIVE-UNOWNED"></span>

<span data-ttu-id="26ed6-176">**S5 activé-actif-sans propriétaire** (6)</span><span class="sxs-lookup"><span data-stu-id="26ed6-176">**S5 Enabled-Active-Unowned** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="S6_Disabled-Active-Unowned"></span><span id="s6_disabled-active-unowned"></span><span id="S6_DISABLED-ACTIVE-UNOWNED"></span>

<span data-ttu-id="26ed6-177">**S6 désactivé-actif-non détenu** (7)</span><span class="sxs-lookup"><span data-stu-id="26ed6-177">**S6 Disabled-Active-Unowned** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="S7_Enabled-Inactive-Unowned"></span><span id="s7_enabled-inactive-unowned"></span><span id="S7_ENABLED-INACTIVE-UNOWNED"></span>

<span data-ttu-id="26ed6-178">**S7 activé-inactif-sans propriétaire** (8)</span><span class="sxs-lookup"><span data-stu-id="26ed6-178">**S7 Enabled-Inactive-Unowned** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="S8_Disabled-Inactive-Unowned"></span><span id="s8_disabled-inactive-unowned"></span><span id="S8_DISABLED-INACTIVE-UNOWNED"></span>

<span data-ttu-id="26ed6-179">**S8 désactivé-inactif-sans propriétaire** (9)</span><span class="sxs-lookup"><span data-stu-id="26ed6-179">**S8 Disabled-Inactive-Unowned** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="26ed6-180">**Non applicable** (10)</span><span class="sxs-lookup"><span data-stu-id="26ed6-180">**Not Applicable** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="26ed6-181">**DMTF réservé** (..)</span><span class="sxs-lookup"><span data-stu-id="26ed6-181">**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="26ed6-182">**Fournisseur réservé** (32768.. 65535)</span><span class="sxs-lookup"><span data-stu-id="26ed6-182">**Vendor Reserved** (32768..65535)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="26ed6-183">**TransitioningToTPMState**</span><span class="sxs-lookup"><span data-stu-id="26ed6-183">**TransitioningToTPMState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="26ed6-184">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="26ed6-184">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="26ed6-185">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="26ed6-185">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="26ed6-186">Qualificateurs : [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ TPM**.**RequestTPMStateChange**","**CIM \_ TPM**.**TPMState**")</span><span class="sxs-lookup"><span data-stu-id="26ed6-186">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_TPM**.**RequestTPMStateChange**", "**CIM\_TPM**.**TPMState**")</span></span>
</dt> </dl>

<span data-ttu-id="26ed6-187">État cible vers lequel le module de plateforme sécurisée (TPM) passe.</span><span class="sxs-lookup"><span data-stu-id="26ed6-187">The target state to which the TPM is transitioning.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="26ed6-188"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (0)</span><span class="sxs-lookup"><span data-stu-id="26ed6-188"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="S1_Enabled-Active-Owned"></span><span id="s1_enabled-active-owned"></span><span id="S1_ENABLED-ACTIVE-OWNED"></span>

<span data-ttu-id="26ed6-189"><span id="S1_Enabled-Active-Owned"></span><span id="s1_enabled-active-owned"></span><span id="S1_ENABLED-ACTIVE-OWNED"></span>**S1 activé-propriétaire actif** (2)</span><span class="sxs-lookup"><span data-stu-id="26ed6-189"><span id="S1_Enabled-Active-Owned"></span><span id="s1_enabled-active-owned"></span><span id="S1_ENABLED-ACTIVE-OWNED"></span>**S1 Enabled-Active-Owned** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="S2_Disabled-Active-Owned"></span><span id="s2_disabled-active-owned"></span><span id="S2_DISABLED-ACTIVE-OWNED"></span>

<span data-ttu-id="26ed6-190"><span id="S2_Disabled-Active-Owned"></span><span id="s2_disabled-active-owned"></span><span id="S2_DISABLED-ACTIVE-OWNED"></span>**S2 désactivé-actif-propriétaire** (3)</span><span class="sxs-lookup"><span data-stu-id="26ed6-190"><span id="S2_Disabled-Active-Owned"></span><span id="s2_disabled-active-owned"></span><span id="S2_DISABLED-ACTIVE-OWNED"></span>**S2 Disabled-Active-Owned** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="S3_Enabled-Inactive-Owned"></span><span id="s3_enabled-inactive-owned"></span><span id="S3_ENABLED-INACTIVE-OWNED"></span>

<span data-ttu-id="26ed6-191"><span id="S3_Enabled-Inactive-Owned"></span><span id="s3_enabled-inactive-owned"></span><span id="S3_ENABLED-INACTIVE-OWNED"></span>**S3 activé-inactif-détenu** (4)</span><span class="sxs-lookup"><span data-stu-id="26ed6-191"><span id="S3_Enabled-Inactive-Owned"></span><span id="s3_enabled-inactive-owned"></span><span id="S3_ENABLED-INACTIVE-OWNED"></span>**S3 Enabled-Inactive-Owned** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="S4_Disabled-Inactive-Owned"></span><span id="s4_disabled-inactive-owned"></span><span id="S4_DISABLED-INACTIVE-OWNED"></span>

<span data-ttu-id="26ed6-192"><span id="S4_Disabled-Inactive-Owned"></span><span id="s4_disabled-inactive-owned"></span><span id="S4_DISABLED-INACTIVE-OWNED"></span>**S4 désactivé-inactif-détenu** (5)</span><span class="sxs-lookup"><span data-stu-id="26ed6-192"><span id="S4_Disabled-Inactive-Owned"></span><span id="s4_disabled-inactive-owned"></span><span id="S4_DISABLED-INACTIVE-OWNED"></span>**S4 Disabled-Inactive-Owned** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="S5_Enabled-Active-Unowned"></span><span id="s5_enabled-active-unowned"></span><span id="S5_ENABLED-ACTIVE-UNOWNED"></span>

<span data-ttu-id="26ed6-193"><span id="S5_Enabled-Active-Unowned"></span><span id="s5_enabled-active-unowned"></span><span id="S5_ENABLED-ACTIVE-UNOWNED"></span>**S5 activé-actif-sans propriétaire** (6)</span><span class="sxs-lookup"><span data-stu-id="26ed6-193"><span id="S5_Enabled-Active-Unowned"></span><span id="s5_enabled-active-unowned"></span><span id="S5_ENABLED-ACTIVE-UNOWNED"></span>**S5 Enabled-Active-Unowned** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="S6_Disabled-Active-Unowned"></span><span id="s6_disabled-active-unowned"></span><span id="S6_DISABLED-ACTIVE-UNOWNED"></span>

<span data-ttu-id="26ed6-194"><span id="S6_Disabled-Active-Unowned"></span><span id="s6_disabled-active-unowned"></span><span id="S6_DISABLED-ACTIVE-UNOWNED"></span>**S6 désactivé-actif-non détenu** (7)</span><span class="sxs-lookup"><span data-stu-id="26ed6-194"><span id="S6_Disabled-Active-Unowned"></span><span id="s6_disabled-active-unowned"></span><span id="S6_DISABLED-ACTIVE-UNOWNED"></span>**S6 Disabled-Active-Unowned** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="S7_Enabled-Inactive-Unowned"></span><span id="s7_enabled-inactive-unowned"></span><span id="S7_ENABLED-INACTIVE-UNOWNED"></span>

<span data-ttu-id="26ed6-195"><span id="S7_Enabled-Inactive-Unowned"></span><span id="s7_enabled-inactive-unowned"></span><span id="S7_ENABLED-INACTIVE-UNOWNED"></span>**S7 activé-inactif-sans propriétaire** (8)</span><span class="sxs-lookup"><span data-stu-id="26ed6-195"><span id="S7_Enabled-Inactive-Unowned"></span><span id="s7_enabled-inactive-unowned"></span><span id="S7_ENABLED-INACTIVE-UNOWNED"></span>**S7 Enabled-Inactive-Unowned** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="S8_Disabled-Inactive-Unowned"></span><span id="s8_disabled-inactive-unowned"></span><span id="S8_DISABLED-INACTIVE-UNOWNED"></span>

<span data-ttu-id="26ed6-196"><span id="S8_Disabled-Inactive-Unowned"></span><span id="s8_disabled-inactive-unowned"></span><span id="S8_DISABLED-INACTIVE-UNOWNED"></span>**S8 désactivé-inactif-sans propriétaire** (9)</span><span class="sxs-lookup"><span data-stu-id="26ed6-196"><span id="S8_Disabled-Inactive-Unowned"></span><span id="s8_disabled-inactive-unowned"></span><span id="S8_DISABLED-INACTIVE-UNOWNED"></span>**S8 Disabled-Inactive-Unowned** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="26ed6-197"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Non applicable** (10)</span><span class="sxs-lookup"><span data-stu-id="26ed6-197"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="No_Change"></span><span id="no_change"></span><span id="NO_CHANGE"></span>

<span data-ttu-id="26ed6-198"><span id="No_Change"></span><span id="no_change"></span><span id="NO_CHANGE"></span>**Aucune modification** (11)</span><span class="sxs-lookup"><span data-stu-id="26ed6-198"><span id="No_Change"></span><span id="no_change"></span><span id="NO_CHANGE"></span>**No Change** (11)</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="26ed6-199">douze</span><span class="sxs-lookup"><span data-stu-id="26ed6-199">(12)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="26ed6-200"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF réservé** (..)</span><span class="sxs-lookup"><span data-stu-id="26ed6-200"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="26ed6-201"><span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Fournisseur réservé** (32768.. 65535)</span><span class="sxs-lookup"><span data-stu-id="26ed6-201"><span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Vendor Reserved** (32768..65535)</span></span>


<span data-ttu-id="26ed6-202"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="26ed6-202"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="26ed6-203">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="26ed6-203">Requirements</span></span>



| <span data-ttu-id="26ed6-204">Condition requise</span><span class="sxs-lookup"><span data-stu-id="26ed6-204">Requirement</span></span> | <span data-ttu-id="26ed6-205">Valeur</span><span class="sxs-lookup"><span data-stu-id="26ed6-205">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="26ed6-206">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="26ed6-206">Minimum supported client</span></span><br/> | <span data-ttu-id="26ed6-207">Applications de \[ Bureau Windows 10 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="26ed6-207">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="26ed6-208">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="26ed6-208">Minimum supported server</span></span><br/> | <span data-ttu-id="26ed6-209">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="26ed6-209">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="26ed6-210">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="26ed6-210">Namespace</span></span><br/>                | <span data-ttu-id="26ed6-211">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="26ed6-211">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="26ed6-212">MOF</span><span class="sxs-lookup"><span data-stu-id="26ed6-212">MOF</span></span><br/>                      | <dl> <span data-ttu-id="26ed6-213"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="26ed6-213"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="26ed6-214">DLL</span><span class="sxs-lookup"><span data-stu-id="26ed6-214">DLL</span></span><br/>                      | <dl> <span data-ttu-id="26ed6-215"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="26ed6-215"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="26ed6-216">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="26ed6-216">See also</span></span>

<dl> <dt>

[<span data-ttu-id="26ed6-217">**\_LOGICALDEVICE CIM**</span><span class="sxs-lookup"><span data-stu-id="26ed6-217">**CIM\_LogicalDevice**</span></span>](cim-logicaldevice.md)
</dt> </dl>

 

