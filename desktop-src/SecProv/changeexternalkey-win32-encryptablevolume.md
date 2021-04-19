---
description: Modifie une clé externe qui est associée à un volume chiffré.
ms.assetid: 14c7e643-f685-40bb-be86-aabc5b883d7e
title: Méthode ChangeExternalKey de la classe Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.ChangeExternalKey
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 7441666ded1acc2234df84fc98ce6d02a117167d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106529360"
---
# <a name="changeexternalkey-method-of-the-win32_encryptablevolume-class"></a><span data-ttu-id="9beb1-103">Méthode ChangeExternalKey de la \_ classe Win32 EncryptableVolume</span><span class="sxs-lookup"><span data-stu-id="9beb1-103">ChangeExternalKey method of the Win32\_EncryptableVolume class</span></span>

<span data-ttu-id="9beb1-104">La méthode **ChangeExternalKey** de la [**classe \_ EncryptableVolume Win32**](win32-encryptablevolume.md) modifie une clé externe qui est associée à un volume chiffré.</span><span class="sxs-lookup"><span data-stu-id="9beb1-104">The **ChangeExternalKey** method of the [**Win32\_EncryptableVolume**](win32-encryptablevolume.md) class changes an external key that is associated with an encrypted volume.</span></span>

## <a name="syntax"></a><span data-ttu-id="9beb1-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9beb1-105">Syntax</span></span>


```mof
uint32 ChangeExternalKey(
  [in]           string VolumeKeyProtectorID,
  [in, optional] uint8   NewExternalKey[],
  [out]          string NewVolumeKeyProtectorID
);
```



## <a name="parameters"></a><span data-ttu-id="9beb1-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="9beb1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9beb1-107">*VolumeKeyProtectorID* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="9beb1-107">*VolumeKeyProtectorID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9beb1-108">Type : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="9beb1-108">Type: **string**</span></span>

<span data-ttu-id="9beb1-109">Identificateur de chaîne unique utilisé pour gérer un protecteur de clé de volume chiffré.</span><span class="sxs-lookup"><span data-stu-id="9beb1-109">A unique string identifier used to manage an encrypted volume key protector.</span></span>

</dd> <dt>

 <span data-ttu-id="9beb1-110">*NewExternalKey* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="9beb1-110">*NewExternalKey* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="9beb1-111">Type : **UInt8 \[ \]**</span><span class="sxs-lookup"><span data-stu-id="9beb1-111">Type: **uint8\[\]**</span></span>

<span data-ttu-id="9beb1-112">Tableau d’octets qui spécifie la clé externe 256 bits utilisée pour déverrouiller le volume.</span><span class="sxs-lookup"><span data-stu-id="9beb1-112">An array of bytes that specifies the 256-bit external key used to unlock the volume.</span></span>

</dd> <dt>

<span data-ttu-id="9beb1-113">*NewVolumeKeyProtectorID* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="9beb1-113">*NewVolumeKeyProtectorID* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9beb1-114">Type : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="9beb1-114">Type: **string**</span></span>

<span data-ttu-id="9beb1-115">Identificateur de chaîne unique mis à jour qui est utilisé pour gérer un protecteur de clé de volume chiffré.</span><span class="sxs-lookup"><span data-stu-id="9beb1-115">An updated unique string identifier that is used to manage an encrypted volume key protector.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9beb1-116">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="9beb1-116">Return value</span></span>

<span data-ttu-id="9beb1-117">Type : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="9beb1-117">Type: **uint32**</span></span>

<span data-ttu-id="9beb1-118">Cette méthode retourne l’un des codes suivants, ou un autre code d’erreur en cas d’échec.</span><span class="sxs-lookup"><span data-stu-id="9beb1-118">This method returns one of the following codes or another error code if it fails.</span></span>



| <span data-ttu-id="9beb1-119">Code/valeur de retour</span><span class="sxs-lookup"><span data-stu-id="9beb1-119">Return code/value</span></span>                                                                                                                                                                            | <span data-ttu-id="9beb1-120">Description</span><span class="sxs-lookup"><span data-stu-id="9beb1-120">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                 |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="9beb1-121"><dt>**S \_ OK**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="9beb1-121"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl>                                            | <span data-ttu-id="9beb1-122">La méthode a réussi.</span><span class="sxs-lookup"><span data-stu-id="9beb1-122">The method was successful.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                       |
| <dl> <span data-ttu-id="9beb1-123"><dt>**E \_ INVALIDARG**</dt> <dt>2147942487 (0x80070057)</dt></span><span class="sxs-lookup"><span data-stu-id="9beb1-123"><dt>**E\_INVALIDARG**</dt> <dt>2147942487 (0x80070057)</dt></span></span> </dl>                    | <span data-ttu-id="9beb1-124">Le paramètre *NewExternalKey* n’est pas un tableau de taille 32.</span><span class="sxs-lookup"><span data-stu-id="9beb1-124">The *NewExternalKey* parameter is not an array of size 32.</span></span><br/>                                                                                                                                                                                                                                                                                                                                       |
| <dl> <span data-ttu-id="9beb1-125"><dt>**FVE \_ E \_ Locked \_ volume**</dt> <dt>2150694912 (0x80310000)</dt></span><span class="sxs-lookup"><span data-stu-id="9beb1-125"><dt>**FVE\_E\_LOCKED\_VOLUME**</dt> <dt>2150694912 (0x80310000)</dt></span></span> </dl>           | <span data-ttu-id="9beb1-126">Le volume est verrouillé.</span><span class="sxs-lookup"><span data-stu-id="9beb1-126">The volume is locked.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                            |
| <dl> <span data-ttu-id="9beb1-127"><dt>**FVE \_ E \_ non \_ activée**</dt> <dt>2150694920 (0x80310008)</dt></span><span class="sxs-lookup"><span data-stu-id="9beb1-127"><dt>**FVE\_E\_NOT\_ACTIVATED**</dt> <dt>2150694920 (0x80310008)</dt></span></span> </dl>           | <span data-ttu-id="9beb1-128">BitLocker n’est pas activé sur le volume.</span><span class="sxs-lookup"><span data-stu-id="9beb1-128">BitLocker is not enabled on the volume.</span></span> <span data-ttu-id="9beb1-129">Ajoutez un protecteur de clé pour activer BitLocker.</span><span class="sxs-lookup"><span data-stu-id="9beb1-129">Add a key protector to enable BitLocker.</span></span> <br/>                                                                                                                                                                                                                                                                                                                |
| <dl> <span data-ttu-id="9beb1-130"><dt>**FVE \_ E \_ amorçable \_ CDDVD**</dt> <dt>2150694960 (0x80310030)</dt></span><span class="sxs-lookup"><span data-stu-id="9beb1-130"><dt>**FVE\_E\_BOOTABLE\_CDDVD**</dt> <dt>2150694960 (0x80310030)</dt></span></span> </dl>          | <span data-ttu-id="9beb1-131">Un CD/DVD de démarrage est détecté sur cet ordinateur.</span><span class="sxs-lookup"><span data-stu-id="9beb1-131">A bootable CD/DVD is found in this computer.</span></span> <span data-ttu-id="9beb1-132">Retirez le CD/DVD et redémarrez l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="9beb1-132">Remove the CD/DVD and restart the computer.</span></span><br/>                                                                                                                                                                                                                                                                                                         |
| <dl> <span data-ttu-id="9beb1-133"><dt>**FVE \_ \_Protecteur E \_ \_ introuvable**</dt> <dt>2150694963 (0x80310033)</dt></span><span class="sxs-lookup"><span data-stu-id="9beb1-133"><dt>**FVE\_E\_PROTECTOR\_NOT\_FOUND**</dt> <dt>2150694963 (0x80310033)</dt></span></span> </dl>    | <span data-ttu-id="9beb1-134">Le protecteur de clé fourni n’existe pas sur le volume.</span><span class="sxs-lookup"><span data-stu-id="9beb1-134">The provided key protector does not exist on the volume.</span></span><br/>                                                                                                                                                                                                                                                                                                                                         |
| <dl> <span data-ttu-id="9beb1-135"><dt>**FVE \_ E \_ \_ \_ type de protecteur non valide**</dt> <dt>2150694970 (0x8031003A)</dt></span><span class="sxs-lookup"><span data-stu-id="9beb1-135"><dt>**FVE\_E\_INVALID\_PROTECTOR\_TYPE**</dt> <dt>2150694970 (0x8031003A)</dt></span></span> </dl> | <span data-ttu-id="9beb1-136">Le paramètre *VolumeKeyProtectorID* ne fait pas référence à un protecteur de clé du type « mot de passe numérique » ou « clé externe ».</span><span class="sxs-lookup"><span data-stu-id="9beb1-136">The *VolumeKeyProtectorID* parameter does not refer to a key protector of the type "Numerical Password" or "External Key".</span></span> <span data-ttu-id="9beb1-137">Utilisez la méthode [**ProtectKeyWithNumericalPassword**](protectkeywithnumericalpassword-win32-encryptablevolume.md) ou [**ProtectKeyWithExternalKey**](protectkeywithexternalkey-win32-encryptablevolume.md) pour créer un protecteur de clé du type approprié.</span><span class="sxs-lookup"><span data-stu-id="9beb1-137">Use either the [**ProtectKeyWithNumericalPassword**](protectkeywithnumericalpassword-win32-encryptablevolume.md) or [**ProtectKeyWithExternalKey**](protectkeywithexternalkey-win32-encryptablevolume.md) method to create a key protector of the appropriate type.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="9beb1-138">Notes</span><span class="sxs-lookup"><span data-stu-id="9beb1-138">Remarks</span></span>

<span data-ttu-id="9beb1-139">Cette méthode peut être utilisée pour modifier la clé externe pour tout protecteur de clé qui utilise une clé externe.</span><span class="sxs-lookup"><span data-stu-id="9beb1-139">This method can be used to change the external key for any key protector that uses an external key.</span></span>

## <a name="requirements"></a><span data-ttu-id="9beb1-140">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="9beb1-140">Requirements</span></span>



| <span data-ttu-id="9beb1-141">Condition requise</span><span class="sxs-lookup"><span data-stu-id="9beb1-141">Requirement</span></span> | <span data-ttu-id="9beb1-142">Valeur</span><span class="sxs-lookup"><span data-stu-id="9beb1-142">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9beb1-143">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9beb1-143">Minimum supported client</span></span><br/> | <span data-ttu-id="9beb1-144">Windows 7 entreprise, les applications de bureau Windows 7 édition intégrale \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="9beb1-144">Windows 7 Enterprise, Windows 7 Ultimate \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="9beb1-145">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9beb1-145">Minimum supported server</span></span><br/> | <span data-ttu-id="9beb1-146">Applications de bureau Windows Server 2008 R2 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="9beb1-146">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="9beb1-147">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="9beb1-147">Namespace</span></span><br/>                | <span data-ttu-id="9beb1-148">Racine \\ de \\ sécurité cimv2 \\ MicrosoftVolumeEncryption</span><span class="sxs-lookup"><span data-stu-id="9beb1-148">Root\\CIMV2\\Security\\MicrosoftVolumeEncryption</span></span><br/>                                             |
| <span data-ttu-id="9beb1-149">MOF</span><span class="sxs-lookup"><span data-stu-id="9beb1-149">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9beb1-150"><dt>Win32 \_ encryptablevolume. mof</dt></span><span class="sxs-lookup"><span data-stu-id="9beb1-150"><dt>Win32\_encryptablevolume.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9beb1-151">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9beb1-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9beb1-152">**\_EncryptableVolume Win32**</span><span class="sxs-lookup"><span data-stu-id="9beb1-152">**Win32\_EncryptableVolume**</span></span>](win32-encryptablevolume.md)
</dt> </dl>

 

 




