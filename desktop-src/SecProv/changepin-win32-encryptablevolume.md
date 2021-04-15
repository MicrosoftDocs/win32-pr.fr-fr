---
description: Modifie le code confidentiel associé à un volume chiffré.
ms.assetid: 8b0043cc-cf86-44e5-ab7c-038a6782f347
title: Méthode ChangePIN de la classe Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.ChangePIN
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 385f8cc66eb08bc020cc126cec587eee57a14ca2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525695"
---
# <a name="changepin-method-of-the-win32_encryptablevolume-class"></a><span data-ttu-id="bbd76-103">Méthode ChangePIN de la \_ classe Win32 EncryptableVolume</span><span class="sxs-lookup"><span data-stu-id="bbd76-103">ChangePIN method of the Win32\_EncryptableVolume class</span></span>

<span data-ttu-id="bbd76-104">La méthode **ChangePIN** de la [**classe \_ EncryptableVolume Win32**](win32-encryptablevolume.md) modifie le code confidentiel associé à un volume chiffré.</span><span class="sxs-lookup"><span data-stu-id="bbd76-104">The **ChangePIN** method of the [**Win32\_EncryptableVolume**](win32-encryptablevolume.md) class changes the PIN associated with an encrypted volume.</span></span> <span data-ttu-id="bbd76-105">Si la stratégie de groupe « autoriser les codes confidentiels améliorés au démarrage » est activée, un code confidentiel peut contenir des lettres, des symboles et des espaces, en plus des nombres.</span><span class="sxs-lookup"><span data-stu-id="bbd76-105">If the "Allow enhanced PINs for startup" group policy is enabled, a PIN can contain letters, symbols, and spaces in addition to numbers.</span></span>

## <a name="syntax"></a><span data-ttu-id="bbd76-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="bbd76-106">Syntax</span></span>


```mof
uint32 ChangePIN(
  [in] string VolumeKeyProtectorID,
  [in] string NewPIN
);
```



## <a name="parameters"></a><span data-ttu-id="bbd76-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="bbd76-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bbd76-108">*VolumeKeyProtectorID* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="bbd76-108">*VolumeKeyProtectorID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bbd76-109">Type : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="bbd76-109">Type: **string**</span></span>

<span data-ttu-id="bbd76-110">Identificateur de chaîne unique utilisé pour gérer un protecteur de clé de volume chiffré.</span><span class="sxs-lookup"><span data-stu-id="bbd76-110">The unique string identifier used to manage an encrypted volume key protector.</span></span>

</dd> <dt>

<span data-ttu-id="bbd76-111">*NewPIN* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="bbd76-111">*NewPIN* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bbd76-112">Type : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="bbd76-112">Type: **string**</span></span>

<span data-ttu-id="bbd76-113">Chaîne d’identification personnelle spécifiée par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="bbd76-113">A user-specified personal identification string.</span></span> <span data-ttu-id="bbd76-114">Cette chaîne doit être composée d’une séquence de 4 à 20 chiffres ou, si la stratégie de groupe « autoriser les codes confidentiels améliorés pour le démarrage » est activée, de 4 à 20 lettres, de symboles, d’espaces ou de nombres.</span><span class="sxs-lookup"><span data-stu-id="bbd76-114">This string must consist of a sequence of 4 to 20 digits or, if the "Allow enhanced PINs for startup" group policy is enabled, 4 to 20 letters, symbols, spaces, or numbers.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bbd76-115">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="bbd76-115">Return value</span></span>

<span data-ttu-id="bbd76-116">Type : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="bbd76-116">Type: **uint32**</span></span>

<span data-ttu-id="bbd76-117">Cette méthode retourne l’un des codes suivants, ou un autre code d’erreur en cas d’échec.</span><span class="sxs-lookup"><span data-stu-id="bbd76-117">This method returns one of the following codes or another error code if it fails.</span></span>



| <span data-ttu-id="bbd76-118">Code/valeur de retour</span><span class="sxs-lookup"><span data-stu-id="bbd76-118">Return code/value</span></span>                                                                                                                                                                                | <span data-ttu-id="bbd76-119">Description</span><span class="sxs-lookup"><span data-stu-id="bbd76-119">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                 |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="bbd76-120"><dt>**S \_ OK**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="bbd76-120"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl>                                                | <span data-ttu-id="bbd76-121">La méthode a réussi.</span><span class="sxs-lookup"><span data-stu-id="bbd76-121">The method was successful.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                       |
| <dl> <span data-ttu-id="bbd76-122"><dt>**FVE \_ E \_ amorçable \_ CDDVD**</dt> <dt>2150694960 (0x80310030)</dt></span><span class="sxs-lookup"><span data-stu-id="bbd76-122"><dt>**FVE\_E\_BOOTABLE\_CDDVD**</dt> <dt>2150694960 (0x80310030)</dt></span></span> </dl>              | <span data-ttu-id="bbd76-123">Un CD/DVD de démarrage est détecté sur cet ordinateur.</span><span class="sxs-lookup"><span data-stu-id="bbd76-123">A bootable CD/DVD is found in this computer.</span></span> <span data-ttu-id="bbd76-124">Retirez le CD/DVD et redémarrez l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="bbd76-124">Remove the CD/DVD and restart the computer.</span></span><br/>                                                                                                                                                                                                                                                                                                         |
| <dl> <span data-ttu-id="bbd76-125"><dt>**FVE \_ E \_ \_ \_ caractères pin non valides**</dt> <dt>2150695066 (0x8031009A)</dt></span><span class="sxs-lookup"><span data-stu-id="bbd76-125"><dt>**FVE\_E\_INVALID\_PIN\_CHARS**</dt> <dt>2150695066 (0x8031009A)</dt></span></span> </dl>          | <span data-ttu-id="bbd76-126">Le paramètre *NewPIN* contient des caractères qui ne sont pas valides.</span><span class="sxs-lookup"><span data-stu-id="bbd76-126">The *NewPIN* parameter contains characters that are not valid.</span></span> <span data-ttu-id="bbd76-127">Lorsque l’stratégie de groupe « autoriser les codes confidentiels améliorés au démarrage » est désactivée, seuls les nombres sont pris en charge.</span><span class="sxs-lookup"><span data-stu-id="bbd76-127">When the "Allow enhanced PINs for startup" Group Policy is disabled, only numbers are supported.</span></span><br/>                                                                                                                                                                                                                                  |
| <dl> <span data-ttu-id="bbd76-128"><dt>**FVE \_ E \_ \_ \_ type de protecteur non valide**</dt> <dt>2150694970 (0x8031003A)</dt></span><span class="sxs-lookup"><span data-stu-id="bbd76-128"><dt>**FVE\_E\_INVALID\_PROTECTOR\_TYPE**</dt> <dt>2150694970 (0x8031003A)</dt></span></span> </dl>     | <span data-ttu-id="bbd76-129">Le paramètre *VolumeKeyProtectorID* ne fait pas référence à un protecteur de clé du type « mot de passe numérique » ou « clé externe ».</span><span class="sxs-lookup"><span data-stu-id="bbd76-129">The *VolumeKeyProtectorID* parameter does not refer to a key protector of the type "Numerical Password" or "External Key".</span></span> <span data-ttu-id="bbd76-130">Utilisez la méthode [**ProtectKeyWithNumericalPassword**](protectkeywithnumericalpassword-win32-encryptablevolume.md) ou [**ProtectKeyWithExternalKey**](protectkeywithexternalkey-win32-encryptablevolume.md) pour créer un protecteur de clé du type approprié.</span><span class="sxs-lookup"><span data-stu-id="bbd76-130">Use either the [**ProtectKeyWithNumericalPassword**](protectkeywithnumericalpassword-win32-encryptablevolume.md) or [**ProtectKeyWithExternalKey**](protectkeywithexternalkey-win32-encryptablevolume.md) method to create a key protector of the appropriate type.</span></span><br/> |
| <dl> <span data-ttu-id="bbd76-131"><dt>**FVE \_ E \_ Locked \_ volume**</dt> <dt>2150694912 (0x80310000)</dt></span><span class="sxs-lookup"><span data-stu-id="bbd76-131"><dt>**FVE\_E\_LOCKED\_VOLUME**</dt> <dt>2150694912 (0x80310000)</dt></span></span> </dl>               | <span data-ttu-id="bbd76-132">Le volume est verrouillé.</span><span class="sxs-lookup"><span data-stu-id="bbd76-132">The volume is locked.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                            |
| <dl> <span data-ttu-id="bbd76-133"><dt>**FVE \_ E \_ non \_ activée**</dt> <dt>2150694920 (0x80310008)</dt></span><span class="sxs-lookup"><span data-stu-id="bbd76-133"><dt>**FVE\_E\_NOT\_ACTIVATED**</dt> <dt>2150694920 (0x80310008)</dt></span></span> </dl>               | <span data-ttu-id="bbd76-134">BitLocker n’est pas activé sur le volume.</span><span class="sxs-lookup"><span data-stu-id="bbd76-134">BitLocker is not enabled on the volume.</span></span> <span data-ttu-id="bbd76-135">Ajoutez un protecteur de clé pour activer BitLocker.</span><span class="sxs-lookup"><span data-stu-id="bbd76-135">Add a key protector to enable BitLocker.</span></span> <br/>                                                                                                                                                                                                                                                                                                                |
| <dl> <span data-ttu-id="bbd76-136"><dt>**FVE \_ \_Longueur de \_ \_ code confidentiel \_ non valide pour la stratégie E**</dt> <dt>2150695016 (0x80310068)</dt></span><span class="sxs-lookup"><span data-stu-id="bbd76-136"><dt>**FVE\_E\_POLICY\_INVALID\_PIN\_LENGTH**</dt> <dt>2150695016 (0x80310068)</dt></span></span> </dl> | <span data-ttu-id="bbd76-137">Le paramètre *NewPIN* fourni comporte plus de 20 caractères, moins de 4 caractères, ou une longueur inférieure à la longueur minimale spécifiée par stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="bbd76-137">The *NewPIN* parameter supplied is either longer than 20 characters, shorter than 4 characters, or shorter than the minimum length specified by Group Policy.</span></span><br/>                                                                                                                                                                                                                                    |
| <dl> <span data-ttu-id="bbd76-138"><dt>**FVE \_ \_Protecteur E \_ \_ introuvable**</dt> <dt>2150694963 (0x80310033)</dt></span><span class="sxs-lookup"><span data-stu-id="bbd76-138"><dt>**FVE\_E\_PROTECTOR\_NOT\_FOUND**</dt> <dt>2150694963 (0x80310033)</dt></span></span> </dl>        | <span data-ttu-id="bbd76-139">Le protecteur de clé fourni n’existe pas sur le volume.</span><span class="sxs-lookup"><span data-stu-id="bbd76-139">The provided key protector does not exist on the volume.</span></span><br/>                                                                                                                                                                                                                                                                                                                                         |
| <dl> <span data-ttu-id="bbd76-140"><dt>**Tbs \_ \_Service E \_ non \_ exécuté**</dt> <dt>2150121480 (0x80284008)</dt></span><span class="sxs-lookup"><span data-stu-id="bbd76-140"><dt>**TBS\_E\_SERVICE\_NOT\_RUNNING**</dt> <dt>2150121480 (0x80284008)</dt></span></span> </dl>        | <span data-ttu-id="bbd76-141">Aucun Module de plateforme sécurisée (TPM) compatible (TPM) n’a été trouvé sur cet ordinateur.</span><span class="sxs-lookup"><span data-stu-id="bbd76-141">No compatible Trusted Platform Module (TPM) is found on this computer.</span></span><br/>                                                                                                                                                                                                                                                                                                                           |



 

## <a name="remarks"></a><span data-ttu-id="bbd76-142">Notes</span><span class="sxs-lookup"><span data-stu-id="bbd76-142">Remarks</span></span>

<span data-ttu-id="bbd76-143">La méthode **ChangePIN** crée un nouveau module de plateforme sécurisée et un protecteur de code confidentiel basés sur les informations de protecteur existantes et le code PIN nouvellement fourni.</span><span class="sxs-lookup"><span data-stu-id="bbd76-143">The **ChangePIN** method creates a new TPM and PIN protector based on the existing protector information and the newly provided PIN.</span></span> <span data-ttu-id="bbd76-144">Le nouveau protecteur aura le même GUID.</span><span class="sxs-lookup"><span data-stu-id="bbd76-144">The new protector will have the same GUID.</span></span> <span data-ttu-id="bbd76-145">La méthode **ChangePIN** peut également être appelée pour modifier le code confidentiel d’un protecteur de clé qui utilise un code confidentiel, par exemple TPM et pin ou TPM avec pin et USB.</span><span class="sxs-lookup"><span data-stu-id="bbd76-145">The **ChangePIN** method can also be called to change the PIN of any key protector that uses a PIN, for example, TPM and PIN or TPM with PIN and USB.</span></span>

<span data-ttu-id="bbd76-146">Les fichiers format MOF (MOF) contiennent les définitions des classes Windows Management Instrumentation (WMI).</span><span class="sxs-lookup"><span data-stu-id="bbd76-146">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="bbd76-147">Les fichiers MOF ne sont pas installés dans le cadre de la SDK Windows.</span><span class="sxs-lookup"><span data-stu-id="bbd76-147">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="bbd76-148">Ils sont installés sur le serveur lorsque vous ajoutez le rôle associé à l’aide de l’Gestionnaire de serveur.</span><span class="sxs-lookup"><span data-stu-id="bbd76-148">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="bbd76-149">Pour plus d’informations sur les fichiers MOF, consultez [format MOF (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="bbd76-149">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="bbd76-150">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="bbd76-150">Requirements</span></span>



| <span data-ttu-id="bbd76-151">Condition requise</span><span class="sxs-lookup"><span data-stu-id="bbd76-151">Requirement</span></span> | <span data-ttu-id="bbd76-152">Valeur</span><span class="sxs-lookup"><span data-stu-id="bbd76-152">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bbd76-153">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="bbd76-153">Minimum supported client</span></span><br/> | <span data-ttu-id="bbd76-154">Windows 7 entreprise, les applications de bureau Windows 7 édition intégrale \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="bbd76-154">Windows 7 Enterprise, Windows 7 Ultimate \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="bbd76-155">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="bbd76-155">Minimum supported server</span></span><br/> | <span data-ttu-id="bbd76-156">Applications de bureau Windows Server 2008 R2 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="bbd76-156">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="bbd76-157">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="bbd76-157">Namespace</span></span><br/>                | <span data-ttu-id="bbd76-158">Racine \\ de \\ sécurité cimv2 \\ MicrosoftVolumeEncryption</span><span class="sxs-lookup"><span data-stu-id="bbd76-158">Root\\CIMV2\\Security\\MicrosoftVolumeEncryption</span></span><br/>                                             |
| <span data-ttu-id="bbd76-159">MOF</span><span class="sxs-lookup"><span data-stu-id="bbd76-159">MOF</span></span><br/>                      | <dl> <span data-ttu-id="bbd76-160"><dt>Win32 \_ encryptablevolume. mof</dt></span><span class="sxs-lookup"><span data-stu-id="bbd76-160"><dt>Win32\_encryptablevolume.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bbd76-161">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="bbd76-161">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bbd76-162">**\_EncryptableVolume Win32**</span><span class="sxs-lookup"><span data-stu-id="bbd76-162">**Win32\_EncryptableVolume**</span></span>](win32-encryptablevolume.md)
</dt> </dl>

 

 
