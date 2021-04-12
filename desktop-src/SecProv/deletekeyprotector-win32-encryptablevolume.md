---
description: Supprime un protecteur de clé donné pour le volume.
ms.assetid: fa6b89b0-83b6-4be2-8b7b-61b0501747d2
title: Méthode DeleteKeyProtector de la classe Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.DeleteKeyProtector
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: b1f539683bb76559d08066d01de6aeca0394ced3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104318206"
---
# <a name="deletekeyprotector-method-of-the-win32_encryptablevolume-class"></a><span data-ttu-id="f16e2-103">Méthode DeleteKeyProtector de la \_ classe Win32 EncryptableVolume</span><span class="sxs-lookup"><span data-stu-id="f16e2-103">DeleteKeyProtector method of the Win32\_EncryptableVolume class</span></span>

<span data-ttu-id="f16e2-104">La méthode **DeleteKeyProtector** de la [**classe \_ EncryptableVolume Win32**](win32-encryptablevolume.md) supprime un protecteur de clé donné pour le volume.</span><span class="sxs-lookup"><span data-stu-id="f16e2-104">The **DeleteKeyProtector** method of the [**Win32\_EncryptableVolume**](win32-encryptablevolume.md) class deletes a given key protector for the volume.</span></span>

<span data-ttu-id="f16e2-105">Si un volume non chiffré possède des protecteurs de clés, lorsque **DeleteKeyProtector** supprime le dernier protecteur de clé, le volume est rétabli dans un système de fichiers NTFS standard.</span><span class="sxs-lookup"><span data-stu-id="f16e2-105">If an unencrypted volume has key protectors, when **DeleteKeyProtector** removes the last key protector, the volume reverts to a standard NTFS file system.</span></span>

<span data-ttu-id="f16e2-106">Si un volume n’a jamais été chiffré, le fait de supprimer le protecteur de clé sera rétabli en NTFS.</span><span class="sxs-lookup"><span data-stu-id="f16e2-106">If a volume has never been encrypted, deleting the key protector will revert to NTFS.</span></span>

<span data-ttu-id="f16e2-107">Si le volume n’est pas encore complètement déchiffré, utilisez [**DisableKeyProtectors**](disablekeyprotectors-win32-encryptablevolume.md) avant de supprimer le dernier protecteur de clé du volume pour vous assurer que les parties chiffrées du volume restent accessibles.</span><span class="sxs-lookup"><span data-stu-id="f16e2-107">If the volume is not yet fully decrypted, use [**DisableKeyProtectors**](disablekeyprotectors-win32-encryptablevolume.md) before removing the volume's last key protector to ensure that encrypted portions of the volume remain accessible.</span></span>

## <a name="syntax"></a><span data-ttu-id="f16e2-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f16e2-108">Syntax</span></span>


```mof
uint32 DeleteKeyProtector(
  [in] string VolumeKeyProtectorID
);
```



## <a name="parameters"></a><span data-ttu-id="f16e2-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f16e2-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f16e2-110">*VolumeKeyProtectorID* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="f16e2-110">*VolumeKeyProtectorID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f16e2-111">Type : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="f16e2-111">Type: **string**</span></span>

<span data-ttu-id="f16e2-112">Identificateur de chaîne unique utilisé pour gérer un protecteur de clé de volume chiffré.</span><span class="sxs-lookup"><span data-stu-id="f16e2-112">A unique string identifier used to manage an encrypted volume key protector.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f16e2-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="f16e2-113">Return value</span></span>

<span data-ttu-id="f16e2-114">Type : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f16e2-114">Type: **uint32**</span></span>

<span data-ttu-id="f16e2-115">Cette méthode retourne l’un des codes suivants, ou un autre code d’erreur en cas d’échec.</span><span class="sxs-lookup"><span data-stu-id="f16e2-115">This method returns one of the following codes or another error code if it fails.</span></span>



| <span data-ttu-id="f16e2-116">Code/valeur de retour</span><span class="sxs-lookup"><span data-stu-id="f16e2-116">Return code/value</span></span>                                                                                                                                                                          | <span data-ttu-id="f16e2-117">Description</span><span class="sxs-lookup"><span data-stu-id="f16e2-117">Description</span></span>                                                                                                                                                                                                                                                                                                               |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="f16e2-118"><dt>**S \_ OK**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="f16e2-118"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl>                                          | <span data-ttu-id="f16e2-119">La méthode a réussi.</span><span class="sxs-lookup"><span data-stu-id="f16e2-119">The method was successful.</span></span><br/>                                                                                                                                                                                                                                                                                     |
| <dl> <span data-ttu-id="f16e2-120"><dt>**FVE \_ E \_ Locked \_ volume**</dt> <dt>2150694912 (0x80310000)</dt></span><span class="sxs-lookup"><span data-stu-id="f16e2-120"><dt>**FVE\_E\_LOCKED\_VOLUME**</dt> <dt>2150694912 (0x80310000)</dt></span></span> </dl>         | <span data-ttu-id="f16e2-121">Le volume est verrouillé.</span><span class="sxs-lookup"><span data-stu-id="f16e2-121">The volume is locked.</span></span><br/>                                                                                                                                                                                                                                                                                          |
| <dl> <span data-ttu-id="f16e2-122"><dt>**FVE \_ E \_ non \_ activée**</dt> <dt>2150694920 (0x80310008)</dt></span><span class="sxs-lookup"><span data-stu-id="f16e2-122"><dt>**FVE\_E\_NOT\_ACTIVATED**</dt> <dt>2150694920 (0x80310008)</dt></span></span> </dl>         | <span data-ttu-id="f16e2-123">BitLocker n’est pas activé sur le volume.</span><span class="sxs-lookup"><span data-stu-id="f16e2-123">BitLocker is not enabled on the volume.</span></span> <span data-ttu-id="f16e2-124">Ajoutez un protecteur de clé pour activer BitLocker.</span><span class="sxs-lookup"><span data-stu-id="f16e2-124">Add a key protector to enable BitLocker.</span></span> <br/>                                                                                                                                                                                                                              |
| <dl> <span data-ttu-id="f16e2-125"><dt>**E \_ INVALIDARG**</dt> <dt>2147942487 (0x80070057)</dt></span><span class="sxs-lookup"><span data-stu-id="f16e2-125"><dt>**E\_INVALIDARG**</dt> <dt>2147942487 (0x80070057)</dt></span></span> </dl>                  | <span data-ttu-id="f16e2-126">Le paramètre *VolumeKeyProtectorID* ne fait pas référence à un protecteur de clé valide.</span><span class="sxs-lookup"><span data-stu-id="f16e2-126">The *VolumeKeyProtectorID* parameter does not refer to a valid key protector.</span></span><br/>                                                                                                                                                                                                                                  |
| <dl> <span data-ttu-id="f16e2-127"><dt>**FVE \_ \_Clé E \_ requise**</dt> <dt>2150694941 (0x8031001D)</dt></span><span class="sxs-lookup"><span data-stu-id="f16e2-127"><dt>**FVE\_E\_KEY\_REQUIRED**</dt> <dt>2150694941 (0x8031001D)</dt></span></span> </dl>          | <span data-ttu-id="f16e2-128">Le dernier protecteur de clé pour un volume partiellement ou entièrement chiffré ne peut pas être supprimé si les protecteurs de clé sont activés.</span><span class="sxs-lookup"><span data-stu-id="f16e2-128">The last key protector for a partially or fully encrypted volume cannot be removed if key protectors are enabled.</span></span> <span data-ttu-id="f16e2-129">Utilisez [**DisableKeyProtectors**](disablekeyprotectors-win32-encryptablevolume.md) avant de supprimer ce dernier protecteur de clé pour vous assurer que les parties chiffrées du volume restent accessibles.</span><span class="sxs-lookup"><span data-stu-id="f16e2-129">Use [**DisableKeyProtectors**](disablekeyprotectors-win32-encryptablevolume.md) before removing this last key protector to ensure that encrypted portions of the volume remain accessible.</span></span> <br/> |
| <dl> <span data-ttu-id="f16e2-130"><dt>**FVE \_ \_Limite de volume E \_ \_ déjà**</dt> <dt>2150694943 (0x8031001F)</dt></span><span class="sxs-lookup"><span data-stu-id="f16e2-130"><dt>**FVE\_E\_VOLUME\_BOUND\_ALREADY**</dt> <dt>2150694943 (0x8031001F)</dt></span></span> </dl> | <span data-ttu-id="f16e2-131">Ce protecteur de clé ne peut pas être supprimé car il est utilisé pour déverrouiller automatiquement le volume.</span><span class="sxs-lookup"><span data-stu-id="f16e2-131">This key protector cannot be deleted because it is being used to automatically unlock the volume.</span></span> <br/> <span data-ttu-id="f16e2-132">Utilisez [**DisableAutoUnlock**](disableautounlock-win32-encryptablevolume.md) pour désactiver le déverrouillage automatique avant de supprimer ce protecteur de clé.</span><span class="sxs-lookup"><span data-stu-id="f16e2-132">Use [**DisableAutoUnlock**](disableautounlock-win32-encryptablevolume.md) to disable automatic unlocking before deleting this key protector.</span></span><br/>                                                    |



 

## <a name="remarks"></a><span data-ttu-id="f16e2-133">Notes</span><span class="sxs-lookup"><span data-stu-id="f16e2-133">Remarks</span></span>

<span data-ttu-id="f16e2-134">Les fichiers format MOF (MOF) contiennent les définitions des classes Windows Management Instrumentation (WMI).</span><span class="sxs-lookup"><span data-stu-id="f16e2-134">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="f16e2-135">Les fichiers MOF ne sont pas installés dans le cadre de la SDK Windows.</span><span class="sxs-lookup"><span data-stu-id="f16e2-135">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="f16e2-136">Ils sont installés sur le serveur lorsque vous ajoutez le rôle associé à l’aide de l’Gestionnaire de serveur.</span><span class="sxs-lookup"><span data-stu-id="f16e2-136">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="f16e2-137">Pour plus d’informations sur les fichiers MOF, consultez [format MOF (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="f16e2-137">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="f16e2-138">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f16e2-138">Requirements</span></span>



| <span data-ttu-id="f16e2-139">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f16e2-139">Requirement</span></span> | <span data-ttu-id="f16e2-140">Valeur</span><span class="sxs-lookup"><span data-stu-id="f16e2-140">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f16e2-141">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f16e2-141">Minimum supported client</span></span><br/> | <span data-ttu-id="f16e2-142">Windows Vista entreprise, les applications de bureau Windows Vista Édition intégrale \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f16e2-142">Windows Vista Enterprise, Windows Vista Ultimate \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="f16e2-143">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f16e2-143">Minimum supported server</span></span><br/> | <span data-ttu-id="f16e2-144">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f16e2-144">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="f16e2-145">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="f16e2-145">Namespace</span></span><br/>                | <span data-ttu-id="f16e2-146">Racine \\ de \\ sécurité cimv2 \\ MicrosoftVolumeEncryption</span><span class="sxs-lookup"><span data-stu-id="f16e2-146">Root\\CIMV2\\Security\\MicrosoftVolumeEncryption</span></span><br/>                                             |
| <span data-ttu-id="f16e2-147">MOF</span><span class="sxs-lookup"><span data-stu-id="f16e2-147">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f16e2-148"><dt>Win32 \_ encryptablevolume. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f16e2-148"><dt>Win32\_encryptablevolume.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f16e2-149">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f16e2-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f16e2-150">**\_EncryptableVolume Win32**</span><span class="sxs-lookup"><span data-stu-id="f16e2-150">**Win32\_EncryptableVolume**</span></span>](win32-encryptablevolume.md)
</dt> </dl>

 

 
