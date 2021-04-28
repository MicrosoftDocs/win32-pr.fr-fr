---
description: Méthode ProtectKeyWithPassphrase de la classe Win32_EncryptableVolume-utilise la phrase secrète pour obtenir la clé dérivée.
ms.assetid: 62b070ec-4788-47cc-bfa4-6811a712ddbd
title: Méthode ProtectKeyWithPassphrase de la classe Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.ProtectKeyWithPassphrase
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 2a7772b1b65890fedbdbb8dcced1ad851f3845b3
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108098347"
---
# <a name="protectkeywithpassphrase-method-of-the-win32_encryptablevolume-class"></a><span data-ttu-id="4fa15-103">Méthode ProtectKeyWithPassphrase de la \_ classe Win32 EncryptableVolume</span><span class="sxs-lookup"><span data-stu-id="4fa15-103">ProtectKeyWithPassphrase method of the Win32\_EncryptableVolume class</span></span>

<span data-ttu-id="4fa15-104">La méthode **ProtectKeyWithPassphrase** de la [**classe \_ EncryptableVolume Win32**](win32-encryptablevolume.md) utilise la phrase secrète pour obtenir la clé dérivée.</span><span class="sxs-lookup"><span data-stu-id="4fa15-104">The **ProtectKeyWithPassphrase** method of the [**Win32\_EncryptableVolume**](win32-encryptablevolume.md) class uses the passphrase to obtain the derived key.</span></span> <span data-ttu-id="4fa15-105">Une fois la clé dérivée calculée, la clé dérivée est utilisée pour sécuriser la clé principale du volume chiffré.</span><span class="sxs-lookup"><span data-stu-id="4fa15-105">After the derived key is calculated, the derived key is used to secure the encrypted volume's master key.</span></span>

## <a name="syntax"></a><span data-ttu-id="4fa15-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="4fa15-106">Syntax</span></span>


```mof
uint32 ProtectKeyWithPassphrase(
  [in, optional] string FriendlyName,
  [in]           string Passphrase,
  [out]          string VolumeKeyProtectorID
);
```



## <a name="parameters"></a><span data-ttu-id="4fa15-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="4fa15-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4fa15-108">*FriendlyName* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="4fa15-108">*FriendlyName* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="4fa15-109">Type : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="4fa15-109">Type: **string**</span></span>

<span data-ttu-id="4fa15-110">Chaîne qui spécifie un identificateur de chaîne assigné par l’utilisateur pour ce protecteur de clé.</span><span class="sxs-lookup"><span data-stu-id="4fa15-110">A string that specifies a user-assigned string identifier for this key protector.</span></span> <span data-ttu-id="4fa15-111">Si ce paramètre n’est pas spécifié, une valeur vide est utilisée.</span><span class="sxs-lookup"><span data-stu-id="4fa15-111">If this parameter is not specified, a blank value is used.</span></span>

</dd> <dt>

<span data-ttu-id="4fa15-112">*Phrase secrète* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="4fa15-112">*Passphrase* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4fa15-113">Type : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="4fa15-113">Type: **string**</span></span>

<span data-ttu-id="4fa15-114">Chaîne qui spécifie la phrase secrète.</span><span class="sxs-lookup"><span data-stu-id="4fa15-114">A string that specifies the passphrase.</span></span>

</dd> <dt>

<span data-ttu-id="4fa15-115">*VolumeKeyProtectorID* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="4fa15-115">*VolumeKeyProtectorID* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4fa15-116">Type : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="4fa15-116">Type: **string**</span></span>

<span data-ttu-id="4fa15-117">Chaîne qui identifie de façon unique le protecteur de clé créé.</span><span class="sxs-lookup"><span data-stu-id="4fa15-117">A string that uniquely identifies the created key protector.</span></span>

<span data-ttu-id="4fa15-118">Si le lecteur prend en charge le chiffrement matériel et que BitLocker n’a pas pris possession de la bande, la chaîne d’ID est définie sur « BitLocker » et le protecteur de clé est écrit dans les métadonnées par bande.</span><span class="sxs-lookup"><span data-stu-id="4fa15-118">If the drive supports hardware encryption and BitLocker has not taken band ownership, the ID string is set to "BitLocker" and the key protector is written to per band metadata.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4fa15-119">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="4fa15-119">Return value</span></span>

<span data-ttu-id="4fa15-120">Type : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="4fa15-120">Type: **uint32**</span></span>

<span data-ttu-id="4fa15-121">Cette méthode retourne l’un des codes suivants, ou un autre code d’erreur en cas d’échec.</span><span class="sxs-lookup"><span data-stu-id="4fa15-121">This method returns one of the following codes or another error code if it fails.</span></span>



| <span data-ttu-id="4fa15-122">Code/valeur de retour</span><span class="sxs-lookup"><span data-stu-id="4fa15-122">Return code/value</span></span>                                                                                                                                                                                        | <span data-ttu-id="4fa15-123">Description</span><span class="sxs-lookup"><span data-stu-id="4fa15-123">Description</span></span>                                                                                                              |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="4fa15-124"><dt>**S \_ OK**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="4fa15-124"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl>                                                        | <span data-ttu-id="4fa15-125">La méthode a réussi.</span><span class="sxs-lookup"><span data-stu-id="4fa15-125">The method was successful.</span></span><br/>                                                                                    |
| <dl> <span data-ttu-id="4fa15-126"><dt>**FVE \_ E \_ non \_ autorisé \_ en \_ \_ mode sans échec**</dt> <dt>2150694976 (0x80310040)</dt></span><span class="sxs-lookup"><span data-stu-id="4fa15-126"><dt>**FVE\_E\_NOT\_ALLOWED\_IN\_SAFE\_MODE**</dt> <dt>2150694976 (0x80310040)</dt></span></span> </dl>         | <span data-ttu-id="4fa15-127">Les Chiffrement de lecteur BitLocker peuvent être utilisés uniquement à des fins de récupération lorsqu’ils sont utilisés en mode sans échec.</span><span class="sxs-lookup"><span data-stu-id="4fa15-127">BitLocker Drive Encryption can only be used for recovery purposes when used in Safe Mode.</span></span><br/>                     |
| <dl> <span data-ttu-id="4fa15-128"><dt>**FVE \_ \_Phrase secrète de la stratégie E \_ \_ non \_ autorisée**</dt> <dt>2150695018 (0x8031006A)</dt></span><span class="sxs-lookup"><span data-stu-id="4fa15-128"><dt>**FVE\_E\_POLICY\_PASSPHRASE\_NOT\_ALLOWED**</dt> <dt>2150695018 (0x8031006A)</dt></span></span> </dl>     | <span data-ttu-id="4fa15-129">La stratégie de groupe n’autorise pas la création d’une phrase secrète.</span><span class="sxs-lookup"><span data-stu-id="4fa15-129">Group policy does not permit the creation of a passphrase.</span></span><br/>                                                    |
| <dl> <span data-ttu-id="4fa15-130"><dt>**FVE \_ E \_ FIPS \_ empêche la \_ phrase secrète**</dt> <dt>2150695020 (0x8031006C)</dt></span><span class="sxs-lookup"><span data-stu-id="4fa15-130"><dt>**FVE\_E\_FIPS\_PREVENTS\_PASSPHRASE**</dt> <dt>2150695020 (0x8031006C)</dt></span></span> </dl>           | <span data-ttu-id="4fa15-131">Le paramètre de stratégie de groupe qui requiert la conformité FIPS a empêché la création ou l’utilisation de la phrase secrète.</span><span class="sxs-lookup"><span data-stu-id="4fa15-131">The group policy setting that requires FIPS compliance prevented the passphrase from being generated or used.</span></span><br/> |
| <dl> <span data-ttu-id="4fa15-132"><dt>**FVE \_ \_Longueur de \_ la \_ phrase \_ secrète non valide de la stratégie E**</dt> <dt>2150695040 (0x80310080)</dt></span><span class="sxs-lookup"><span data-stu-id="4fa15-132"><dt>**FVE\_E\_POLICY\_INVALID\_PASSPHRASE\_LENGTH**</dt> <dt>2150695040 (0x80310080)</dt></span></span> </dl>  | <span data-ttu-id="4fa15-133">La phrase secrète fournie ne répond pas aux exigences de longueur minimale ou maximale.</span><span class="sxs-lookup"><span data-stu-id="4fa15-133">The passphrase provided does not meet the minimum or maximum length requirements.</span></span><br/>                             |
| <dl> <span data-ttu-id="4fa15-134"><dt>**FVE \_ \_Phrase secrète de la stratégie E \_ \_ trop \_ simple**</dt> <dt>2150695041 (0x80310081)</dt></span><span class="sxs-lookup"><span data-stu-id="4fa15-134"><dt>**FVE\_E\_POLICY\_PASSPHRASE\_TOO\_SIMPLE**</dt> <dt>2150695041 (0x80310081)</dt></span></span> </dl>      | <span data-ttu-id="4fa15-135">La phrase secrète ne respecte pas les exigences de complexité définies par l’administrateur dans la stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="4fa15-135">The passphrase does not meet the complexity requirements set by the administrator in group policy.</span></span><br/>            |
| <dl> <span data-ttu-id="4fa15-136"><dt>**FVE \_ E \_ Locked \_ volume**</dt> <dt>2150694912 (0x80310000)</dt></span><span class="sxs-lookup"><span data-stu-id="4fa15-136"><dt>**FVE\_E\_LOCKED\_VOLUME**</dt> <dt>2150694912 (0x80310000)</dt></span></span> </dl>                       | <span data-ttu-id="4fa15-137">Le volume est déjà verrouillé par Chiffrement de lecteur BitLocker.</span><span class="sxs-lookup"><span data-stu-id="4fa15-137">The volume is already locked by BitLocker Drive Encryption.</span></span> <span data-ttu-id="4fa15-138">Vous devez déverrouiller le lecteur à partir du panneau de configuration.</span><span class="sxs-lookup"><span data-stu-id="4fa15-138">You must unlock the drive from Control Panel.</span></span><br/>     |
| <dl> <span data-ttu-id="4fa15-139"><dt>**FVE \_ E \_ \_ mise à jour**</dt> <dt>2150694948 (0x80310024)</dt></span><span class="sxs-lookup"><span data-stu-id="4fa15-139"><dt>**FVE\_E\_OVERLAPPED\_UPDATE**</dt> <dt>2150694948 (0x80310024)</dt></span></span> </dl>                   | <span data-ttu-id="4fa15-140">Le bloc de contrôle du volume chiffré a été mis à jour par un autre thread.</span><span class="sxs-lookup"><span data-stu-id="4fa15-140">The control block for the encrypted volume was updated by another thread.</span></span><br/>                                     |
| <dl> <span data-ttu-id="4fa15-141"><dt>**FVE \_ Le \_ protecteur de clé E \_ n’est \_ pas \_ pris en charge**</dt> <dt>2150695017 (0x80310069)</dt></span><span class="sxs-lookup"><span data-stu-id="4fa15-141"><dt>**FVE\_E\_KEY\_PROTECTOR\_NOT\_SUPPORTED**</dt> <dt>2150695017 (0x80310069)</dt></span></span> </dl>       | <span data-ttu-id="4fa15-142">Le protecteur de clé n’est pas pris en charge par la version de Chiffrement de lecteur BitLocker actuellement sur le volume.</span><span class="sxs-lookup"><span data-stu-id="4fa15-142">The key protector is not supported by the version of BitLocker Drive Encryption currently on the volume.</span></span><br/>      |
| <dl> <span data-ttu-id="4fa15-143"><dt>**FVE \_ \_Phrase secrète du volume du système d’exploitation \_ \_ \_ non \_ autorisée**</dt> <dt>2150695021 (0x8031006D)</dt></span><span class="sxs-lookup"><span data-stu-id="4fa15-143"><dt>**FVE\_E\_OS\_VOLUME\_PASSPHRASE\_NOT\_ALLOWED**</dt> <dt>2150695021 (0x8031006D)</dt></span></span> </dl> | <span data-ttu-id="4fa15-144">La phrase secrète ne peut pas être ajoutée au volume du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="4fa15-144">The passphrase cannot be added to the operating system volume.</span></span> <br/>                                               |
| <dl> <span data-ttu-id="4fa15-145"><dt>**FVE \_ Le \_ protecteur E \_ existe**</dt> <dt>2150694960 (0x80310030)</dt></span><span class="sxs-lookup"><span data-stu-id="4fa15-145"><dt>**FVE\_E\_PROTECTOR\_EXISTS**</dt> <dt>2150694960 (0x80310030)</dt></span></span> </dl>                    | <span data-ttu-id="4fa15-146">Le protecteur de clé fourni existe déjà sur ce volume.</span><span class="sxs-lookup"><span data-stu-id="4fa15-146">The provided key protector already exists on this volume.</span></span><br/>                                                     |



 

## <a name="requirements"></a><span data-ttu-id="4fa15-147">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="4fa15-147">Requirements</span></span>



| <span data-ttu-id="4fa15-148">Condition requise</span><span class="sxs-lookup"><span data-stu-id="4fa15-148">Requirement</span></span> | <span data-ttu-id="4fa15-149">Valeur</span><span class="sxs-lookup"><span data-stu-id="4fa15-149">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4fa15-150">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4fa15-150">Minimum supported client</span></span><br/> | <span data-ttu-id="4fa15-151">Windows 7 entreprise, les applications de bureau Windows 7 édition intégrale \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="4fa15-151">Windows 7 Enterprise, Windows 7 Ultimate \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="4fa15-152">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4fa15-152">Minimum supported server</span></span><br/> | <span data-ttu-id="4fa15-153">Applications de bureau Windows Server 2008 R2 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="4fa15-153">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="4fa15-154">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="4fa15-154">Namespace</span></span><br/>                | <span data-ttu-id="4fa15-155">Racine \\ de \\ sécurité cimv2 \\ MicrosoftVolumeEncryption</span><span class="sxs-lookup"><span data-stu-id="4fa15-155">Root\\CIMV2\\Security\\MicrosoftVolumeEncryption</span></span><br/>                                             |
| <span data-ttu-id="4fa15-156">MOF</span><span class="sxs-lookup"><span data-stu-id="4fa15-156">MOF</span></span><br/>                      | <dl> <span data-ttu-id="4fa15-157"><dt>Win32 \_ encryptablevolume. mof</dt></span><span class="sxs-lookup"><span data-stu-id="4fa15-157"><dt>Win32\_encryptablevolume.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4fa15-158">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4fa15-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4fa15-159">**\_EncryptableVolume Win32**</span><span class="sxs-lookup"><span data-stu-id="4fa15-159">**Win32\_EncryptableVolume**</span></span>](win32-encryptablevolume.md)
</dt> </dl>

 

 




