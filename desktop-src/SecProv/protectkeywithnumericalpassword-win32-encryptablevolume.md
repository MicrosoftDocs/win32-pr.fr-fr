---
description: Sécurise la clé de chiffrement du volume avec un mot de passe à 48 chiffres spécialement mis en forme.
ms.assetid: 23e0b79a-2feb-441a-9785-7ecd3bb4b6c6
title: Méthode ProtectKeyWithNumericalPassword de la classe Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.ProtectKeyWithNumericalPassword
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: fd17727bc71dbbe517b6424135e1205035027a00
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103866953"
---
# <a name="protectkeywithnumericalpassword-method-of-the-win32_encryptablevolume-class"></a><span data-ttu-id="5583d-103">Méthode ProtectKeyWithNumericalPassword de la \_ classe Win32 EncryptableVolume</span><span class="sxs-lookup"><span data-stu-id="5583d-103">ProtectKeyWithNumericalPassword method of the Win32\_EncryptableVolume class</span></span>

<span data-ttu-id="5583d-104">La méthode **ProtectKeyWithNumericalPassword** de la classe [**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md) sécurise la clé de chiffrement du volume avec un mot de passe à 48 chiffres spécialement mis en forme.</span><span class="sxs-lookup"><span data-stu-id="5583d-104">The **ProtectKeyWithNumericalPassword** method of the [**Win32\_EncryptableVolume**](win32-encryptablevolume.md) class secures the volume's encryption key with a specially formatted 48-digit password.</span></span> <span data-ttu-id="5583d-105">Ce mot de passe numérique peut être utilisé pour récupérer des échecs d’authentification d’autres protecteurs de clé (par exemple, TPM).</span><span class="sxs-lookup"><span data-stu-id="5583d-105">This numerical password can be used to recover from the authentication failures of other key protectors (for example, TPM).</span></span>

<span data-ttu-id="5583d-106">Un protecteur de clé de type « numérique Password » est créé pour le volume.</span><span class="sxs-lookup"><span data-stu-id="5583d-106">A key protector of type "Numerical Password" is created for the volume.</span></span>

<span data-ttu-id="5583d-107">Utilisez la méthode [**IsNumericalPasswordValid**](isnumericalpasswordvalid-win32-encryptablevolume.md) pour valider le format du mot de passe numérique.</span><span class="sxs-lookup"><span data-stu-id="5583d-107">Use the [**IsNumericalPasswordValid**](isnumericalpasswordvalid-win32-encryptablevolume.md) method to validate the format of the numerical password.</span></span>

## <a name="syntax"></a><span data-ttu-id="5583d-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="5583d-108">Syntax</span></span>


```mof
uint32 ProtectKeyWithNumericalPassword(
  [in, optional] string FriendlyName,
  [in, optional] string NumericalPassword,
  [out]          string VolumeKeyProtectorID
);
```



## <a name="parameters"></a><span data-ttu-id="5583d-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="5583d-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5583d-110">*FriendlyName* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="5583d-110">*FriendlyName* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="5583d-111">Type : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="5583d-111">Type: **string**</span></span>

<span data-ttu-id="5583d-112">Chaîne qui spécifie un identificateur affecté à l’utilisateur pour ce protecteur de clé.</span><span class="sxs-lookup"><span data-stu-id="5583d-112">A string that specifies a user-assigned identifier for this key protector.</span></span> <span data-ttu-id="5583d-113">Si ce paramètre n’est pas spécifié, une valeur vide est utilisée.</span><span class="sxs-lookup"><span data-stu-id="5583d-113">If this parameter is not specified, a blank value is used.</span></span>

</dd> <dt>

<span data-ttu-id="5583d-114">*NumericalPassword* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="5583d-114">*NumericalPassword* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="5583d-115">Type : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="5583d-115">Type: **string**</span></span>

<span data-ttu-id="5583d-116">Chaîne qui spécifie le mot de passe numérique à 48 chiffres spécialement mis en forme.</span><span class="sxs-lookup"><span data-stu-id="5583d-116">A string that specifies the specially formatted 48-digit numerical password.</span></span>

<span data-ttu-id="5583d-117">Le mot de passe numérique doit contenir 48 chiffres.</span><span class="sxs-lookup"><span data-stu-id="5583d-117">The numerical password must contain 48 digits.</span></span> <span data-ttu-id="5583d-118">Ces chiffres peuvent être divisés en 8 groupes de 6 chiffres, le dernier chiffre de chaque groupe indiquant une valeur de somme de contrôle pour le groupe.</span><span class="sxs-lookup"><span data-stu-id="5583d-118">These digits can be divided into 8 groups of 6 digits, with the last digit in each group indicating a checksum value for the group.</span></span> <span data-ttu-id="5583d-119">Chaque groupe de 6 chiffres doit être divisible par 11 et doit être inférieur à 720896.</span><span class="sxs-lookup"><span data-stu-id="5583d-119">Each group of 6 digits must be divisible by 11 and must be less than 720896.</span></span> <span data-ttu-id="5583d-120">En supposant qu’un groupe de six chiffres s’intitule x1, x2, x3, x4, x5 et x6, le chiffre de la somme de contrôle x6 est calculé comme-x1 + x2 – x3 + x4 – x5 Mod 11.</span><span class="sxs-lookup"><span data-stu-id="5583d-120">Assuming a group of six digits is labeled as x1, x2, x3, x4, x5, and x6, the checksum x6 digit is calculated as –x1+x2–x3+x4–x5 mod 11.</span></span>

<span data-ttu-id="5583d-121">Les groupes de chiffres peuvent éventuellement être séparés par un espace ou un trait d’Union.</span><span class="sxs-lookup"><span data-stu-id="5583d-121">The groups of digits can optionally be separated by a space or hyphen.</span></span> <span data-ttu-id="5583d-122">Par conséquent, « XXXXXX-XXXXXX-XXXXXX-XXXXXX-XXXXXX-XXXXXX-XXXXXX-XXXXXX » ou « xxxxxx XXXXXX XXXXXX XXXXXX XXXXXX XXXXXX XXXXXX XXXXXX » peut également contenir des mots de passe numériques valides.</span><span class="sxs-lookup"><span data-stu-id="5583d-122">Therefore, "xxxxxx-xxxxxx-xxxxxx-xxxxxx-xxxxxx-xxxxxx-xxxxxx-xxxxxx" or "xxxxxx xxxxxx xxxxxx xxxxxx xxxxxx xxxxxx xxxxxx xxxxxx" may also contain valid numerical passwords.</span></span>

<span data-ttu-id="5583d-123">Si aucun mot de passe numérique n’est spécifié, un mot de passe est généré de façon aléatoire.</span><span class="sxs-lookup"><span data-stu-id="5583d-123">If no numerical password is specified, one is randomly generated.</span></span> <span data-ttu-id="5583d-124">Utilisez la méthode [**GetKeyProtectorNumericalPassword**](getkeyprotectornumericalpassword-win32-encryptablevolume.md) pour obtenir le mot de passe généré de manière aléatoire.</span><span class="sxs-lookup"><span data-stu-id="5583d-124">Use the [**GetKeyProtectorNumericalPassword**](getkeyprotectornumericalpassword-win32-encryptablevolume.md) method to obtain the randomly generated password.</span></span>

</dd> <dt>

<span data-ttu-id="5583d-125">*VolumeKeyProtectorID* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="5583d-125">*VolumeKeyProtectorID* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5583d-126">Type : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="5583d-126">Type: **string**</span></span>

<span data-ttu-id="5583d-127">Chaîne qui est l’identificateur unique associé au protecteur créé et qui peut être utilisé pour gérer le protecteur de clé.</span><span class="sxs-lookup"><span data-stu-id="5583d-127">A string that is the unique identifier associated with the created protector and that can be used to manage the key protector.</span></span>

<span data-ttu-id="5583d-128">Si le lecteur prend en charge le chiffrement matériel et que BitLocker n’a pas pris possession de la bande, la chaîne d’ID est définie sur « BitLocker » et le protecteur de clé est écrit dans les métadonnées par bande.</span><span class="sxs-lookup"><span data-stu-id="5583d-128">If the drive supports hardware encryption and BitLocker has not taken band ownership, the ID string is set to "BitLocker" and the key protector is written to per band metadata.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5583d-129">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="5583d-129">Return value</span></span>

<span data-ttu-id="5583d-130">Type : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="5583d-130">Type: **uint32**</span></span>

<span data-ttu-id="5583d-131">Cette méthode retourne l’un des codes suivants, ou un autre code d’erreur en cas d’échec.</span><span class="sxs-lookup"><span data-stu-id="5583d-131">This method returns one of the following codes or another error code if it fails.</span></span>



| <span data-ttu-id="5583d-132">Code/valeur de retour</span><span class="sxs-lookup"><span data-stu-id="5583d-132">Return code/value</span></span>                                                                                                                                                                  | <span data-ttu-id="5583d-133">Description</span><span class="sxs-lookup"><span data-stu-id="5583d-133">Description</span></span>                                                                |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| <dl> <span data-ttu-id="5583d-134"><dt>**S \_ OK**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="5583d-134"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl>                                  | <span data-ttu-id="5583d-135">La méthode a réussi.</span><span class="sxs-lookup"><span data-stu-id="5583d-135">The method was successful.</span></span><br/>                                      |
| <dl> <span data-ttu-id="5583d-136"><dt>**E \_ INVALIDARG**</dt> <dt>2147942487 (0x80070057)</dt></span><span class="sxs-lookup"><span data-stu-id="5583d-136"><dt>**E\_INVALIDARG**</dt> <dt>2147942487 (0x80070057)</dt></span></span> </dl>          | <span data-ttu-id="5583d-137">Le format du paramètre *NumericalPassword* n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="5583d-137">The *NumericalPassword* parameter does not have a valid format.</span></span><br/> |
| <dl> <span data-ttu-id="5583d-138"><dt>**FVE \_ E \_ Locked \_ volume**</dt> <dt>2150694912 (0x80310000)</dt></span><span class="sxs-lookup"><span data-stu-id="5583d-138"><dt>**FVE\_E\_LOCKED\_VOLUME**</dt> <dt>2150694912 (0x80310000)</dt></span></span> </dl> | <span data-ttu-id="5583d-139">Le volume est verrouillé.</span><span class="sxs-lookup"><span data-stu-id="5583d-139">The volume is locked.</span></span><br/>                                           |
| <dl> <span data-ttu-id="5583d-140"><dt>**FVE \_ E \_ \_ \_ format de mot de passe non valide**</dt> <dt>2150694965 (0x80310035)</dt></span><span class="sxs-lookup"><span data-stu-id="5583d-140"><dt>**FVE\_E\_INVALID\_PASSWORD\_FORMAT**</dt> <dt>2150694965 (0x80310035)</dt></span></span> </dl> | <span data-ttu-id="5583d-141">Le format du paramètre *NumericalPassword* n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="5583d-141">The *NumericalPassword* parameter does not have a valid format.</span></span><br/>                                                                                                                                                     |



 

## <a name="remarks"></a><span data-ttu-id="5583d-142">Notes</span><span class="sxs-lookup"><span data-stu-id="5583d-142">Remarks</span></span>

<span data-ttu-id="5583d-143">Les fichiers format MOF (MOF) contiennent les définitions des classes Windows Management Instrumentation (WMI).</span><span class="sxs-lookup"><span data-stu-id="5583d-143">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="5583d-144">Les fichiers MOF ne sont pas installés dans le cadre de la SDK Windows.</span><span class="sxs-lookup"><span data-stu-id="5583d-144">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="5583d-145">Ils sont installés sur le serveur lorsque vous ajoutez le rôle associé à l’aide de l’Gestionnaire de serveur.</span><span class="sxs-lookup"><span data-stu-id="5583d-145">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="5583d-146">Pour plus d’informations sur les fichiers MOF, consultez [format MOF (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="5583d-146">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="5583d-147">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5583d-147">Requirements</span></span>



| <span data-ttu-id="5583d-148">Condition requise</span><span class="sxs-lookup"><span data-stu-id="5583d-148">Requirement</span></span> | <span data-ttu-id="5583d-149">Valeur</span><span class="sxs-lookup"><span data-stu-id="5583d-149">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5583d-150">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5583d-150">Minimum supported client</span></span><br/> | <span data-ttu-id="5583d-151">Windows Vista entreprise, les applications de bureau Windows Vista Édition intégrale \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="5583d-151">Windows Vista Enterprise, Windows Vista Ultimate \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="5583d-152">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5583d-152">Minimum supported server</span></span><br/> | <span data-ttu-id="5583d-153">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="5583d-153">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="5583d-154">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="5583d-154">Namespace</span></span><br/>                | <span data-ttu-id="5583d-155">Racine \\ de \\ sécurité cimv2 \\ MicrosoftVolumeEncryption</span><span class="sxs-lookup"><span data-stu-id="5583d-155">Root\\CIMV2\\Security\\MicrosoftVolumeEncryption</span></span><br/>                                             |
| <span data-ttu-id="5583d-156">MOF</span><span class="sxs-lookup"><span data-stu-id="5583d-156">MOF</span></span><br/>                      | <dl> <span data-ttu-id="5583d-157"><dt>Win32 \_ encryptablevolume. mof</dt></span><span class="sxs-lookup"><span data-stu-id="5583d-157"><dt>Win32\_encryptablevolume.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5583d-158">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5583d-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5583d-159">**\_EncryptableVolume Win32**</span><span class="sxs-lookup"><span data-stu-id="5583d-159">**Win32\_EncryptableVolume**</span></span>](win32-encryptablevolume.md)
</dt> </dl>

 

 
