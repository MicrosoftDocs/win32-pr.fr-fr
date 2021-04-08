---
description: Permet de déverrouiller automatiquement un volume de données lorsque le volume est monté.
ms.assetid: ec77b17f-545b-40a7-91b2-ff0b32b8370d
title: Méthode EnableAutoUnlock de la classe Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.EnableAutoUnlock
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 39456e9130081e52820cd91ba3e191ee40ab2374
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103865425"
---
# <a name="enableautounlock-method-of-the-win32_encryptablevolume-class"></a><span data-ttu-id="25402-103">Méthode EnableAutoUnlock de la \_ classe Win32 EncryptableVolume</span><span class="sxs-lookup"><span data-stu-id="25402-103">EnableAutoUnlock method of the Win32\_EncryptableVolume class</span></span>

<span data-ttu-id="25402-104">La méthode **EnableAutoUnlock** de la classe [**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md) permet de déverrouiller automatiquement un volume de données lorsque le volume est monté.</span><span class="sxs-lookup"><span data-stu-id="25402-104">The **EnableAutoUnlock** method of the [**Win32\_EncryptableVolume**](win32-encryptablevolume.md) class allows a data volume to be automatically unlocked when the volume is mounted.</span></span>

<span data-ttu-id="25402-105">Le déverrouillage automatique enregistre une clé externe sur le système d’exploitation qui peut déverrouiller automatiquement le volume sur le volume du système d’exploitation en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="25402-105">Automatic unlocking saves an external key to the operating system that can automatically unlock the volume onto the currently running operating system volume.</span></span>

<span data-ttu-id="25402-106">Pour utiliser cette méthode, le volume du système d’exploitation doit déjà être protégé par Chiffrement de lecteur BitLocker ou doit avoir un chiffrement en cours.</span><span class="sxs-lookup"><span data-stu-id="25402-106">To use this method, the operating system volume must already be protected by BitLocker Drive Encryption or must have encryption in progress.</span></span> <span data-ttu-id="25402-107">En outre, il doit déjà exister une clé externe pour le volume de données.</span><span class="sxs-lookup"><span data-stu-id="25402-107">In addition, there must already exist an external key for the data volume.</span></span> <span data-ttu-id="25402-108">Utilisez [**ProtectKeyWithExternalKey**](protectkeywithexternalkey-win32-encryptablevolume.md) pour créer la clé externe qui peut déverrouiller automatiquement le volume.</span><span class="sxs-lookup"><span data-stu-id="25402-108">Use [**ProtectKeyWithExternalKey**](protectkeywithexternalkey-win32-encryptablevolume.md) to create the external key that can automatically unlock the volume.</span></span>

## <a name="syntax"></a><span data-ttu-id="25402-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="25402-109">Syntax</span></span>


```mof
uint32 EnableAutoUnlock(
  [in] string VolumeKeyProtectorID
);
```



## <a name="parameters"></a><span data-ttu-id="25402-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="25402-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="25402-111">*VolumeKeyProtectorID* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="25402-111">*VolumeKeyProtectorID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="25402-112">Type : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="25402-112">Type: **string**</span></span>

<span data-ttu-id="25402-113">Chaîne qui identifie le protecteur de clé du type « clé externe » utilisé pour déverrouiller automatiquement le volume.</span><span class="sxs-lookup"><span data-stu-id="25402-113">A string that identifies the key protector of the type "External Key" used to automatically unlock the volume.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="25402-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="25402-114">Return value</span></span>

<span data-ttu-id="25402-115">Type : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="25402-115">Type: **uint32**</span></span>

<span data-ttu-id="25402-116">Cette méthode retourne l’un des codes suivants, ou un autre code d’erreur en cas d’échec.</span><span class="sxs-lookup"><span data-stu-id="25402-116">This method returns one of the following codes or another error code if it fails.</span></span>



| <span data-ttu-id="25402-117">Code/valeur de retour</span><span class="sxs-lookup"><span data-stu-id="25402-117">Return code/value</span></span>                                                                                                                                                                           | <span data-ttu-id="25402-118">Description</span><span class="sxs-lookup"><span data-stu-id="25402-118">Description</span></span>                                                                                                                                                                  |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="25402-119"><dt>**S \_ OK**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="25402-119"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl>                                           | <span data-ttu-id="25402-120">La méthode a réussi.</span><span class="sxs-lookup"><span data-stu-id="25402-120">The method was successful.</span></span><br/>                                                                                                                                        |
| <dl> <span data-ttu-id="25402-121"><dt>**FVE \_ E \_ Locked \_ volume**</dt> <dt>2150694912 (0x80310000)</dt></span><span class="sxs-lookup"><span data-stu-id="25402-121"><dt>**FVE\_E\_LOCKED\_VOLUME**</dt> <dt>2150694912 (0x80310000)</dt></span></span> </dl>          | <span data-ttu-id="25402-122">Le volume est verrouillé.</span><span class="sxs-lookup"><span data-stu-id="25402-122">The volume is locked.</span></span><br/>                                                                                                                                             |
| <dl> <span data-ttu-id="25402-123"><dt>**FVE \_ E \_ non \_ activée**</dt> <dt>2150694920 (0x80310008)</dt></span><span class="sxs-lookup"><span data-stu-id="25402-123"><dt>**FVE\_E\_NOT\_ACTIVATED**</dt> <dt>2150694920 (0x80310008)</dt></span></span> </dl>          | <span data-ttu-id="25402-124">BitLocker n’est pas activé sur le volume.</span><span class="sxs-lookup"><span data-stu-id="25402-124">BitLocker is not enabled on the volume.</span></span> <span data-ttu-id="25402-125">Ajoutez un protecteur de clé pour activer BitLocker.</span><span class="sxs-lookup"><span data-stu-id="25402-125">Add a key protector to enable BitLocker.</span></span> <br/>                                                                                 |
| <dl> <span data-ttu-id="25402-126"><dt>**E \_ INVALIDARG**</dt> <dt>2147942487 (0x80070057)</dt></span><span class="sxs-lookup"><span data-stu-id="25402-126"><dt>**E\_INVALIDARG**</dt> <dt>2147942487 (0x80070057)</dt></span></span> </dl>                   | <span data-ttu-id="25402-127">Le paramètre *VolumeKeyProtectorID* ne fait pas référence à un protecteur de clé valide du type « clé externe ».</span><span class="sxs-lookup"><span data-stu-id="25402-127">The *VolumeKeyProtectorID* parameter does not refer to a valid key protector of the type "External Key".</span></span><br/>                                                          |
| <dl> <span data-ttu-id="25402-128"><dt>**FVE \_ E \_ non \_ \_ VOLUME de données**</dt> <dt>2150694937 (0x80310019)</dt></span><span class="sxs-lookup"><span data-stu-id="25402-128"><dt>**FVE\_E\_NOT\_DATA\_VOLUME**</dt> <dt>2150694937 (0x80310019)</dt></span></span> </dl>       | <span data-ttu-id="25402-129">La méthode ne peut pas être exécutée pour le volume du système d’exploitation en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="25402-129">The method cannot be run for the currently running operating system volume.</span></span><br/>                                                                                       |
| <dl> <span data-ttu-id="25402-130"><dt>**FVE \_ E/ \_ s \_ non \_ protégé**</dt> <dt>2150694944 (0x80310020)</dt></span><span class="sxs-lookup"><span data-stu-id="25402-130"><dt>**FVE\_E\_OS\_NOT\_PROTECTED**</dt> <dt>2150694944 (0x80310020)</dt></span></span> </dl>      | <span data-ttu-id="25402-131">La méthode ne peut pas être exécutée si le volume du système d’exploitation en cours d’exécution n’est pas protégé par Chiffrement de lecteur BitLocker ou si le chiffrement n’est pas en cours.</span><span class="sxs-lookup"><span data-stu-id="25402-131">The method cannot be run if the currently running operating system volume is not protected by BitLocker Drive Encryption or does not have encryption in progress.</span></span><br/> |
| <dl> <span data-ttu-id="25402-132"><dt> **\_ Limite du \_ volume E FVE \_ \_ déjà**</dt> <dt>2150694943 (0x8031001F)</dt></span><span class="sxs-lookup"><span data-stu-id="25402-132"><dt>**FVE\_E\_VOLUME\_BOUND\_ALREADY** </dt> <dt>2150694943 (0x8031001F)</dt></span></span> </dl> | <span data-ttu-id="25402-133">Le déverrouillage automatique sur le volume a déjà été activé.</span><span class="sxs-lookup"><span data-stu-id="25402-133">Automatic unlocking on the volume has previously been enabled.</span></span><br/>                                                                                                    |



 

## <a name="remarks"></a><span data-ttu-id="25402-134">Notes</span><span class="sxs-lookup"><span data-stu-id="25402-134">Remarks</span></span>

<span data-ttu-id="25402-135">En fonction d’un protecteur de clé de volume valide du type « clé externe », la clé externe 256 bits associée est extraite du protecteur et stockée dans le Registre du système d’exploitation en cours d’exécution, avec l’ID de protecteur de clé de volume.</span><span class="sxs-lookup"><span data-stu-id="25402-135">Given a valid volume key protector of the type "External Key", the related 256-bit external key is extracted from the protector and stored into the registry of the currently running operating system, along with the volume key protector ID.</span></span>

<span data-ttu-id="25402-136">Si la clé externe associée à l’ID de protecteur de clé de volume est supprimée, la fonctionnalité de déverrouillage automatique du volume est désactivée ou suspendue.</span><span class="sxs-lookup"><span data-stu-id="25402-136">If the external key associated with the volume key protector ID is deleted, the functionality to automatically unlock the volume is disabled or suspended.</span></span>

> [!Note]  
> <span data-ttu-id="25402-137">Le support amovible n’est pas pris en charge actuellement.</span><span class="sxs-lookup"><span data-stu-id="25402-137">Removable media is not currently supported.</span></span>

 

<span data-ttu-id="25402-138">Les fichiers format MOF (MOF) contiennent les définitions des classes Windows Management Instrumentation (WMI).</span><span class="sxs-lookup"><span data-stu-id="25402-138">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="25402-139">Les fichiers MOF ne sont pas installés dans le cadre de la SDK Windows.</span><span class="sxs-lookup"><span data-stu-id="25402-139">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="25402-140">Ils sont installés sur le serveur lorsque vous ajoutez le rôle associé à l’aide de l’Gestionnaire de serveur.</span><span class="sxs-lookup"><span data-stu-id="25402-140">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="25402-141">Pour plus d’informations sur les fichiers MOF, consultez [format MOF (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="25402-141">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="25402-142">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="25402-142">Requirements</span></span>



| <span data-ttu-id="25402-143">Condition requise</span><span class="sxs-lookup"><span data-stu-id="25402-143">Requirement</span></span> | <span data-ttu-id="25402-144">Valeur</span><span class="sxs-lookup"><span data-stu-id="25402-144">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="25402-145">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="25402-145">Minimum supported client</span></span><br/> | <span data-ttu-id="25402-146">Windows Vista entreprise, les applications de bureau Windows Vista Édition intégrale \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="25402-146">Windows Vista Enterprise, Windows Vista Ultimate \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="25402-147">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="25402-147">Minimum supported server</span></span><br/> | <span data-ttu-id="25402-148">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="25402-148">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="25402-149">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="25402-149">Namespace</span></span><br/>                | <span data-ttu-id="25402-150">Racine \\ de \\ sécurité cimv2 \\ MicrosoftVolumeEncryption</span><span class="sxs-lookup"><span data-stu-id="25402-150">Root\\CIMV2\\Security\\MicrosoftVolumeEncryption</span></span><br/>                                             |
| <span data-ttu-id="25402-151">MOF</span><span class="sxs-lookup"><span data-stu-id="25402-151">MOF</span></span><br/>                      | <dl> <span data-ttu-id="25402-152"><dt>Win32 \_ encryptablevolume. mof</dt></span><span class="sxs-lookup"><span data-stu-id="25402-152"><dt>Win32\_encryptablevolume.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="25402-153">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="25402-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="25402-154">**\_EncryptableVolume Win32**</span><span class="sxs-lookup"><span data-stu-id="25402-154">**Win32\_EncryptableVolume**</span></span>](win32-encryptablevolume.md)
</dt> </dl>

 

 
