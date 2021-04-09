---
title: Classe MDM_BitLocker
description: La \_ classe MDM BitLocker est utilisée par l’entreprise pour gérer le chiffrement des PC et des appareils.
ms.assetid: e8bea6dc-8d3d-46d2-b2e3-9a4c547a639f
keywords:
- Classe MDM_BitLocker
- Classe MDM_BitLocker, Description
topic_type:
- apiref
api_name:
- MDM_BitLocker
- MDM_BitLocker.InstanceID
- MDM_BitLocker.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b94db491333cada64b6287dc87ec233b420bf0f6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104106138"
---
# <a name="mdm_bitlocker-class"></a><span data-ttu-id="ba7e0-105">\_Classe MDM BitLocker</span><span class="sxs-lookup"><span data-stu-id="ba7e0-105">MDM\_BitLocker class</span></span>

<span data-ttu-id="ba7e0-106">\[Certaines informations relatives aux produits précommercialisés peuvent être substantiellement modifiées avant leur commercialisation.</span><span class="sxs-lookup"><span data-stu-id="ba7e0-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="ba7e0-107">Microsoft ne donne aucune garantie, expresse ou implicite, concernant les informations fournies ici.\]</span><span class="sxs-lookup"><span data-stu-id="ba7e0-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="ba7e0-108">La \_ classe MDM BitLocker est utilisée par l’entreprise pour gérer le chiffrement des PC et des appareils.</span><span class="sxs-lookup"><span data-stu-id="ba7e0-108">The MDM\_BitLocker class is used by the enterprise to manage encryption of PCs and devices.</span></span>

<span data-ttu-id="ba7e0-109">La syntaxe suivante issue du code MOF est simplifiée et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="ba7e0-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="ba7e0-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ba7e0-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv1")]
class MDM_BitLocker
{
  string InstanceID;
  string ParentID;
  sint32 RequireStorageCardEncryption;
  sint32 RequireDeviceEncryption;
  string EncryptionMethodByDriveType;
  string SystemDrivesRequireStartupAuthentication;
  string SystemDrivesMinimumPINLength;
  string SystemDrivesRecoveryMessage;
  string SystemDrivesRecoveryOptions;
  string FixedDrivesRecoveryOptions;
  string FixedDrivesRequireEncryption;
  string RemovableDrivesRequireEncryption;
  sint32 AllowWarningForOtherDiskEncryption;
};
```

## <a name="members"></a><span data-ttu-id="ba7e0-111">Membres</span><span class="sxs-lookup"><span data-stu-id="ba7e0-111">Members</span></span>

<span data-ttu-id="ba7e0-112">La classe **MDM \_ BitLocker** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="ba7e0-112">The **MDM\_BitLocker** class has these types of members:</span></span>

-   [<span data-ttu-id="ba7e0-113">Propriétés</span><span class="sxs-lookup"><span data-stu-id="ba7e0-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="ba7e0-114">Propriétés</span><span class="sxs-lookup"><span data-stu-id="ba7e0-114">Properties</span></span>

<span data-ttu-id="ba7e0-115">La classe **MDM \_ BitLocker** possède ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="ba7e0-115">The **MDM\_BitLocker** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="ba7e0-116">AllowWarningForOtherDiskEncryption</span><span class="sxs-lookup"><span data-stu-id="ba7e0-116">AllowWarningForOtherDiskEncryption</span></span>](/windows/client-management/mdm/bitlocker-csp#allowwarningforotherdiskencryption)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ba7e0-117">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="ba7e0-117">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="ba7e0-118">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="ba7e0-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ba7e0-119">EncryptionMethodByDriveType</span><span class="sxs-lookup"><span data-stu-id="ba7e0-119">EncryptionMethodByDriveType</span></span>](/windows/client-management/mdm/bitlocker-csp#encryptionmethodbydrivetype)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ba7e0-120">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="ba7e0-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ba7e0-121">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="ba7e0-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ba7e0-122">FixedDrivesRecoveryOptions</span><span class="sxs-lookup"><span data-stu-id="ba7e0-122">FixedDrivesRecoveryOptions</span></span>](/windows/client-management/mdm/bitlocker-csp#fixeddrivesrecoveryoptions)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ba7e0-123">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="ba7e0-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ba7e0-124">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="ba7e0-124">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ba7e0-125">FixedDrivesRequireEncryption</span><span class="sxs-lookup"><span data-stu-id="ba7e0-125">FixedDrivesRequireEncryption</span></span>](/windows/client-management/mdm/bitlocker-csp#fixeddrivesrequireencryption)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ba7e0-126">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="ba7e0-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ba7e0-127">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="ba7e0-127">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="ba7e0-128">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="ba7e0-128">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ba7e0-129">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="ba7e0-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ba7e0-130">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ba7e0-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ba7e0-131">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="ba7e0-131">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="ba7e0-132">**ID**</span><span class="sxs-lookup"><span data-stu-id="ba7e0-132">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ba7e0-133">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="ba7e0-133">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ba7e0-134">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ba7e0-134">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ba7e0-135">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="ba7e0-135">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ba7e0-136">RemovableDrivesRequireEncryption</span><span class="sxs-lookup"><span data-stu-id="ba7e0-136">RemovableDrivesRequireEncryption</span></span>](/windows/client-management/mdm/bitlocker-csp#removabledrivesrequireencryption)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ba7e0-137">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="ba7e0-137">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ba7e0-138">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="ba7e0-138">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ba7e0-139">RequireDeviceEncryption</span><span class="sxs-lookup"><span data-stu-id="ba7e0-139">RequireDeviceEncryption</span></span>](/windows/client-management/mdm/bitlocker-csp#requiredeviceencryption)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ba7e0-140">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="ba7e0-140">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="ba7e0-141">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="ba7e0-141">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ba7e0-142">RequireStorageCardEncryption</span><span class="sxs-lookup"><span data-stu-id="ba7e0-142">RequireStorageCardEncryption</span></span>](/windows/client-management/mdm/bitlocker-csp#requirestoragecardencryption)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ba7e0-143">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="ba7e0-143">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="ba7e0-144">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="ba7e0-144">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ba7e0-145">SystemDrivesMinimumPINLength</span><span class="sxs-lookup"><span data-stu-id="ba7e0-145">SystemDrivesMinimumPINLength</span></span>](/windows/client-management/mdm/bitlocker-csp#systemdrivesminimumpinlength)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ba7e0-146">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="ba7e0-146">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ba7e0-147">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="ba7e0-147">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ba7e0-148">SystemDrivesRecoveryMessage</span><span class="sxs-lookup"><span data-stu-id="ba7e0-148">SystemDrivesRecoveryMessage</span></span>](/windows/client-management/mdm/bitlocker-csp#systemdrivesrecoverymessage)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ba7e0-149">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="ba7e0-149">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ba7e0-150">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="ba7e0-150">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ba7e0-151">SystemDrivesRecoveryOptions</span><span class="sxs-lookup"><span data-stu-id="ba7e0-151">SystemDrivesRecoveryOptions</span></span>](/windows/client-management/mdm/bitlocker-csp#systemdrivesrecoveryoptions)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ba7e0-152">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="ba7e0-152">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ba7e0-153">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="ba7e0-153">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ba7e0-154">SystemDrivesRequireStartupAuthentication</span><span class="sxs-lookup"><span data-stu-id="ba7e0-154">SystemDrivesRequireStartupAuthentication</span></span>](/windows/client-management/mdm/bitlocker-csp#systemdrivesrequirestartupauthentication)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ba7e0-155">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="ba7e0-155">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ba7e0-156">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="ba7e0-156">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="ba7e0-157">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ba7e0-157">Requirements</span></span>



| <span data-ttu-id="ba7e0-158">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ba7e0-158">Requirement</span></span> | <span data-ttu-id="ba7e0-159">Valeur</span><span class="sxs-lookup"><span data-stu-id="ba7e0-159">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ba7e0-160">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ba7e0-160">Minimum supported client</span></span><br/> | <span data-ttu-id="ba7e0-161">Applications de \[ Bureau Windows 10 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ba7e0-161">Windows 10 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="ba7e0-162">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ba7e0-162">Minimum supported server</span></span><br/> | <span data-ttu-id="ba7e0-163">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="ba7e0-163">None supported</span></span><br/>                                                                       |
| <span data-ttu-id="ba7e0-164">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="ba7e0-164">Namespace</span></span><br/>                | <span data-ttu-id="ba7e0-165">Racine dmmap de gestion des appareils mobiles \\ \\ \\</span><span class="sxs-lookup"><span data-stu-id="ba7e0-165">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                              |
| <span data-ttu-id="ba7e0-166">MOF</span><span class="sxs-lookup"><span data-stu-id="ba7e0-166">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ba7e0-167"><dt>DMWmiBridgeProv1. mof</dt></span><span class="sxs-lookup"><span data-stu-id="ba7e0-167"><dt>DMWmiBridgeProv1.mof</dt></span></span> </dl> |
| <span data-ttu-id="ba7e0-168">DLL</span><span class="sxs-lookup"><span data-stu-id="ba7e0-168">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ba7e0-169"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ba7e0-169"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl>  |



 

