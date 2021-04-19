---
description: Utilise la nouvelle phrase secrète pour obtenir une nouvelle clé dérivée.
ms.assetid: 89398bae-a2a2-466c-8a1e-a702018d679f
title: Méthode ChangePassphrase de la classe Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.ChangePassphrase
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: f28a78c6cb923b4f8934ec5cc8962b91b7f5139f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106523343"
---
# <a name="changepassphrase-method-of-the-win32_encryptablevolume-class"></a><span data-ttu-id="c92d0-103">Méthode ChangePassphrase de la \_ classe Win32 EncryptableVolume</span><span class="sxs-lookup"><span data-stu-id="c92d0-103">ChangePassphrase method of the Win32\_EncryptableVolume class</span></span>

<span data-ttu-id="c92d0-104">La méthode **ChangePassphrase** de la [**classe \_ EncryptableVolume Win32**](win32-encryptablevolume.md) utilise la nouvelle phrase secrète pour obtenir une nouvelle clé dérivée.</span><span class="sxs-lookup"><span data-stu-id="c92d0-104">The **ChangePassphrase** method of the [**Win32\_EncryptableVolume**](win32-encryptablevolume.md) class uses the new passphrase to obtain a new derived key.</span></span> <span data-ttu-id="c92d0-105">Une fois la clé dérivée calculée, la nouvelle clé dérivée est utilisée pour sécuriser la clé principale du volume chiffré.</span><span class="sxs-lookup"><span data-stu-id="c92d0-105">After the derived key is calculated, the new derived key is used to secure the encrypted volume's master key.</span></span>

## <a name="syntax"></a><span data-ttu-id="c92d0-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c92d0-106">Syntax</span></span>


```mof
uint32 ChangePassphrase(
  [in]  string VolumeKeyProtectorID,
  [in]  string NewPassphrase,
  [out] string NewProtectorID
);
```



## <a name="parameters"></a><span data-ttu-id="c92d0-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c92d0-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c92d0-108">*VolumeKeyProtectorID* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="c92d0-108">*VolumeKeyProtectorID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c92d0-109">Type : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="c92d0-109">Type: **string**</span></span>

<span data-ttu-id="c92d0-110">Identificateur de chaîne unique utilisé pour gérer un protecteur de clé de volume chiffré.</span><span class="sxs-lookup"><span data-stu-id="c92d0-110">A unique string identifier that is used to manage an encrypted volume key protector.</span></span>

</dd> <dt>

<span data-ttu-id="c92d0-111">*NewPassphrase* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="c92d0-111">*NewPassphrase* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c92d0-112">Type : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="c92d0-112">Type: **string**</span></span>

<span data-ttu-id="c92d0-113">Chaîne mise à jour qui spécifie la phrase secrète.</span><span class="sxs-lookup"><span data-stu-id="c92d0-113">An updated string that specifies the passphrase.</span></span>

</dd> <dt>

<span data-ttu-id="c92d0-114">*NewProtectorID* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="c92d0-114">*NewProtectorID* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c92d0-115">Type : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="c92d0-115">Type: **string**</span></span>

<span data-ttu-id="c92d0-116">Identificateur de chaîne unique mis à jour, utilisé pour gérer un protecteur de clé de volume chiffré.</span><span class="sxs-lookup"><span data-stu-id="c92d0-116">An updated unique string identifier used to manage an encrypted volume key protector.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c92d0-117">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="c92d0-117">Return value</span></span>

<span data-ttu-id="c92d0-118">Type : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c92d0-118">Type: **uint32**</span></span>

<span data-ttu-id="c92d0-119">Cette méthode retourne l’un des codes suivants, ou un autre code d’erreur en cas d’échec.</span><span class="sxs-lookup"><span data-stu-id="c92d0-119">This method returns one of the following codes or another error code if it fails.</span></span>



| <span data-ttu-id="c92d0-120">Code/valeur de retour</span><span class="sxs-lookup"><span data-stu-id="c92d0-120">Return code/value</span></span>                                                                                                                                                                                       | <span data-ttu-id="c92d0-121">Description</span><span class="sxs-lookup"><span data-stu-id="c92d0-121">Description</span></span>                                                                                                            |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="c92d0-122"><dt>**S \_ OK**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="c92d0-122"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl>                                                       | <span data-ttu-id="c92d0-123">La méthode a réussi.</span><span class="sxs-lookup"><span data-stu-id="c92d0-123">The method was successful.</span></span><br/>                                                                                  |
| <dl> <span data-ttu-id="c92d0-124"><dt>**FVE \_ E \_ Locked \_ volume**</dt> <dt>2150694912 (0x80310000)</dt></span><span class="sxs-lookup"><span data-stu-id="c92d0-124"><dt>**FVE\_E\_LOCKED\_VOLUME**</dt> <dt>2150694912 (0x80310000)</dt></span></span> </dl>                      | <span data-ttu-id="c92d0-125">Le volume est déjà verrouillé par Chiffrement de lecteur BitLocker.</span><span class="sxs-lookup"><span data-stu-id="c92d0-125">The volume is already locked by BitLocker Drive Encryption.</span></span> <span data-ttu-id="c92d0-126">Vous devez déverrouiller le lecteur à partir du panneau de configuration.</span><span class="sxs-lookup"><span data-stu-id="c92d0-126">You must unlock the drive from Control Panel.</span></span><br/>   |
| <dl> <span data-ttu-id="c92d0-127"><dt>**FVE \_ E \_ non \_ activée**</dt> <dt>2150694920 (0x80310008)</dt></span><span class="sxs-lookup"><span data-stu-id="c92d0-127"><dt>**FVE\_E\_NOT\_ACTIVATED**</dt> <dt>2150694920 (0x80310008)</dt></span></span> </dl>                      | <span data-ttu-id="c92d0-128">BitLocker n’est pas activé sur le volume.</span><span class="sxs-lookup"><span data-stu-id="c92d0-128">BitLocker is not enabled on the volume.</span></span> <span data-ttu-id="c92d0-129">Ajoutez un protecteur de clé pour activer BitLocker.</span><span class="sxs-lookup"><span data-stu-id="c92d0-129">Add a key protector to enable BitLocker.</span></span> <br/>                           |
| <dl> <span data-ttu-id="c92d0-130"><dt>**FVE \_ E \_ \_ mise à jour**</dt> <dt>2150694948 (0x80310024)</dt></span><span class="sxs-lookup"><span data-stu-id="c92d0-130"><dt>**FVE\_E\_OVERLAPPED\_UPDATE**</dt> <dt>2150694948 (0x80310024)</dt></span></span> </dl>                  | <span data-ttu-id="c92d0-131">Le bloc de contrôle du volume chiffré a été mis à jour par un autre thread.</span><span class="sxs-lookup"><span data-stu-id="c92d0-131">The control block for the encrypted volume was updated by another thread.</span></span><br/>                                   |
| <dl> <span data-ttu-id="c92d0-132"><dt>**FVE \_ E \_ \_ \_ type de protecteur non valide**</dt> <dt>2150694970 (0x8031003A)</dt></span><span class="sxs-lookup"><span data-stu-id="c92d0-132"><dt>**FVE\_E\_INVALID\_PROTECTOR\_TYPE**</dt> <dt>2150694970 (0x8031003A)</dt></span></span> </dl>            | <span data-ttu-id="c92d0-133">Le type de protecteur de clé spécifié n’est pas correct.</span><span class="sxs-lookup"><span data-stu-id="c92d0-133">The specified key protector is not of the correct type.</span></span> <br/>                                                    |
| <dl> <span data-ttu-id="c92d0-134"><dt>**FVE \_ \_Longueur de \_ la \_ phrase \_ secrète non valide de la stratégie E**</dt> <dt>2150695040 (0x80310080)</dt></span><span class="sxs-lookup"><span data-stu-id="c92d0-134"><dt>**FVE\_E\_POLICY\_INVALID\_PASSPHRASE\_LENGTH**</dt> <dt>2150695040 (0x80310080)</dt></span></span> </dl> | <span data-ttu-id="c92d0-135">La phrase secrète mise à jour fournie ne répond pas aux exigences de longueur minimale ou maximale.</span><span class="sxs-lookup"><span data-stu-id="c92d0-135">The updated passphrase provided does not meet the minimum or maximum length requirements.</span></span> <br/>                  |
| <dl> <span data-ttu-id="c92d0-136"><dt>**FVE \_ \_Phrase secrète de la stratégie E \_ \_ trop \_ simple**</dt> <dt>2150695041 (0x80310081)</dt></span><span class="sxs-lookup"><span data-stu-id="c92d0-136"><dt>**FVE\_E\_POLICY\_PASSPHRASE\_TOO\_SIMPLE**</dt> <dt>2150695041 (0x80310081)</dt></span></span> </dl>     | <span data-ttu-id="c92d0-137">La phrase secrète mise à jour ne répond pas aux exigences de complexité définies par l’administrateur dans la stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="c92d0-137">The updated passphrase does not meet the complexity requirements set by the administrator in group policy.</span></span> <br/> |



 

## <a name="requirements"></a><span data-ttu-id="c92d0-138">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c92d0-138">Requirements</span></span>



| <span data-ttu-id="c92d0-139">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c92d0-139">Requirement</span></span> | <span data-ttu-id="c92d0-140">Valeur</span><span class="sxs-lookup"><span data-stu-id="c92d0-140">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c92d0-141">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c92d0-141">Minimum supported client</span></span><br/> | <span data-ttu-id="c92d0-142">Windows 7 entreprise, les applications de bureau Windows 7 édition intégrale \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c92d0-142">Windows 7 Enterprise, Windows 7 Ultimate \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="c92d0-143">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c92d0-143">Minimum supported server</span></span><br/> | <span data-ttu-id="c92d0-144">Applications de bureau Windows Server 2008 R2 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c92d0-144">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="c92d0-145">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="c92d0-145">Namespace</span></span><br/>                | <span data-ttu-id="c92d0-146">Racine \\ de \\ sécurité cimv2 \\ MicrosoftVolumeEncryption</span><span class="sxs-lookup"><span data-stu-id="c92d0-146">Root\\CIMV2\\Security\\MicrosoftVolumeEncryption</span></span><br/>                                             |
| <span data-ttu-id="c92d0-147">MOF</span><span class="sxs-lookup"><span data-stu-id="c92d0-147">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c92d0-148"><dt>Win32 \_ encryptablevolume. mof</dt></span><span class="sxs-lookup"><span data-stu-id="c92d0-148"><dt>Win32\_encryptablevolume.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c92d0-149">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c92d0-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c92d0-150">**\_EncryptableVolume Win32**</span><span class="sxs-lookup"><span data-stu-id="c92d0-150">**Win32\_EncryptableVolume**</span></span>](win32-encryptablevolume.md)
</dt> </dl>

 

 




