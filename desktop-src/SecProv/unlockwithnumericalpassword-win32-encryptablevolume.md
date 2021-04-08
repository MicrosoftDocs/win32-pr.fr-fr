---
description: Utilise un mot de passe numérique fourni pour accéder au contenu d’un volume de données.
ms.assetid: ee968372-18a4-4748-ab18-2f1b8d297f0e
title: Méthode UnlockWithNumericalPassword de la classe Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.UnlockWithNumericalPassword
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 09676e4a57e03f86b18259a7ffb472a6682eafd7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862274"
---
# <a name="unlockwithnumericalpassword-method-of-the-win32_encryptablevolume-class"></a><span data-ttu-id="1ee64-103">Méthode UnlockWithNumericalPassword de la \_ classe Win32 EncryptableVolume</span><span class="sxs-lookup"><span data-stu-id="1ee64-103">UnlockWithNumericalPassword method of the Win32\_EncryptableVolume class</span></span>

<span data-ttu-id="1ee64-104">La méthode **UnlockWithNumericalPassword** de la [**classe \_ EncryptableVolume Win32**](win32-encryptablevolume.md) utilise un mot de passe numérique fourni pour accéder au contenu d’un volume de données.</span><span class="sxs-lookup"><span data-stu-id="1ee64-104">The **UnlockWithNumericalPassword** method of the [**Win32\_EncryptableVolume**](win32-encryptablevolume.md) class uses a provided numerical password to access the contents of a data volume.</span></span>

<span data-ttu-id="1ee64-105">La clé de chiffrement du volume doit avoir été sécurisée avec un ou plusieurs protecteurs de clé du type « mot de passe numérique » (à l’aide de la méthode [**ProtectKeyWithNumericalPassword**](protectkeywithnumericalpassword-win32-encryptablevolume.md) ) pour pouvoir déverrouiller le volume avec cette méthode.</span><span class="sxs-lookup"><span data-stu-id="1ee64-105">The volume's encryption key must have been secured with one or more key protectors of the type "Numerical Password" (by using the [**ProtectKeyWithNumericalPassword**](protectkeywithnumericalpassword-win32-encryptablevolume.md) method) to be able to unlock the volume with this method.</span></span>

> [!Note]  
> <span data-ttu-id="1ee64-106">Si le disque prend en charge le chiffrement matériel, cette fonction définit l’état de la bande sur « déverrouillé ».</span><span class="sxs-lookup"><span data-stu-id="1ee64-106">If the disc supports hardware encryption this function sets the band status to "unlocked""</span></span>

 

## <a name="syntax"></a><span data-ttu-id="1ee64-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1ee64-107">Syntax</span></span>


```mof
uint32 UnlockWithNumericalPassword(
  [in] string NumericalPassword
);
```



## <a name="parameters"></a><span data-ttu-id="1ee64-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="1ee64-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1ee64-109">*NumericalPassword* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="1ee64-109">*NumericalPassword* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1ee64-110">Type : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="1ee64-110">Type: **string**</span></span>

<span data-ttu-id="1ee64-111">Chaîne qui spécifie le mot de passe numérique.</span><span class="sxs-lookup"><span data-stu-id="1ee64-111">A string that specifies the numerical password.</span></span>

<span data-ttu-id="1ee64-112">Le mot de passe numérique doit contenir 48 chiffres.</span><span class="sxs-lookup"><span data-stu-id="1ee64-112">The numerical password must contain 48 digits.</span></span> <span data-ttu-id="1ee64-113">Ces chiffres peuvent être divisés en 8 groupes de 6 chiffres, le dernier chiffre de chaque groupe indiquant une valeur de somme de contrôle pour le groupe.</span><span class="sxs-lookup"><span data-stu-id="1ee64-113">These digits can be divided into 8 groups of 6 digits, with the last digit in each group indicating a checksum value for the group.</span></span> <span data-ttu-id="1ee64-114">Chaque groupe de 6 chiffres doit être divisible par 11 et doit être inférieur à 65536.</span><span class="sxs-lookup"><span data-stu-id="1ee64-114">Each group of 6 digits must be divisible by 11 and must be less than 65536.</span></span> <span data-ttu-id="1ee64-115">En supposant qu’un groupe de six chiffres s’intitule x1, x2, x3, x4, x5 et x6, le chiffre de la somme de contrôle x6 est calculé comme-x1 + x2 – x3 + x4 – x5 Mod 11.</span><span class="sxs-lookup"><span data-stu-id="1ee64-115">Assuming a group of six digits is labeled as x1, x2, x3, x4, x5, and x6, the checksum x6 digit is calculated as –x1+x2–x3+x4–x5 mod 11.</span></span>

<span data-ttu-id="1ee64-116">Les groupes de chiffres peuvent éventuellement être séparés par un espace ou un trait d’Union.</span><span class="sxs-lookup"><span data-stu-id="1ee64-116">The groups of digits can optionally be separated by a space or hyphen.</span></span> <span data-ttu-id="1ee64-117">Par conséquent, « XXXXXX-XXXXXX-XXXXXX-XXXXXX-XXXXXX-XXXXXX-XXXXXX-XXXXXX » ou « xxxxxx XXXXXX XXXXXX XXXXXX XXXXXX XXXXXX XXXXXX XXXXXX » peut également contenir des mots de passe numériques valides.</span><span class="sxs-lookup"><span data-stu-id="1ee64-117">Therefore, "xxxxxx-xxxxxx-xxxxxx-xxxxxx-xxxxxx-xxxxxx-xxxxxx-xxxxxx" or "xxxxxx xxxxxx xxxxxx xxxxxx xxxxxx xxxxxx xxxxxx xxxxxx" may also contain valid numerical passwords.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1ee64-118">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="1ee64-118">Return value</span></span>

<span data-ttu-id="1ee64-119">Type : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="1ee64-119">Type: **uint32**</span></span>

<span data-ttu-id="1ee64-120">Cette méthode retourne l’un des codes suivants, ou un autre code d’erreur en cas d’échec.</span><span class="sxs-lookup"><span data-stu-id="1ee64-120">This method returns one of the following codes or another error code if it fails.</span></span>

<span data-ttu-id="1ee64-121">Si le volume est déjà déverrouillé et qu’aucune autre erreur ne se produit, cette méthode retourne 0.</span><span class="sxs-lookup"><span data-stu-id="1ee64-121">If the volume is already unlocked and no other errors occur, this method returns 0.</span></span>



| <span data-ttu-id="1ee64-122">Code/valeur de retour</span><span class="sxs-lookup"><span data-stu-id="1ee64-122">Return code/value</span></span>                                                                                                                                                                             | <span data-ttu-id="1ee64-123">Description</span><span class="sxs-lookup"><span data-stu-id="1ee64-123">Description</span></span>                                                                                                                                                                                                                    |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="1ee64-124"><dt>**S \_ OK**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="1ee64-124"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl>                                             | <span data-ttu-id="1ee64-125">La méthode a réussi.</span><span class="sxs-lookup"><span data-stu-id="1ee64-125">The method was successful.</span></span><br/>                                                                                                                                                                                          |
| <dl> <span data-ttu-id="1ee64-126"><dt>**FVE \_ E \_ non \_ activée**</dt> <dt>2150694920 (0x80310008)</dt></span><span class="sxs-lookup"><span data-stu-id="1ee64-126"><dt>**FVE\_E\_NOT\_ACTIVATED**</dt> <dt>2150694920 (0x80310008)</dt></span></span> </dl>            | <span data-ttu-id="1ee64-127">BitLocker n’est pas activé sur le volume.</span><span class="sxs-lookup"><span data-stu-id="1ee64-127">BitLocker is not enabled on the volume.</span></span> <span data-ttu-id="1ee64-128">Ajoutez un protecteur de clé pour activer BitLocker.</span><span class="sxs-lookup"><span data-stu-id="1ee64-128">Add a key protector to enable BitLocker.</span></span> <br/>                                                                                                                                   |
| <dl> <span data-ttu-id="1ee64-129"><dt>**FVE \_ \_Protecteur E \_ \_ introuvable**</dt> <dt>2150694963 (0x80310033)</dt></span><span class="sxs-lookup"><span data-stu-id="1ee64-129"><dt>**FVE\_E\_PROTECTOR\_NOT\_FOUND**</dt> <dt>2150694963 (0x80310033)</dt></span></span> </dl>     | <span data-ttu-id="1ee64-130">Le volume n’a pas de protecteur de clé du type « mot de passe numérique ».</span><span class="sxs-lookup"><span data-stu-id="1ee64-130">The volume does not have a key protector of the type "Numerical Password".</span></span><br/> <span data-ttu-id="1ee64-131">Le format du paramètre *NumericalPassword* est valide, mais vous ne pouvez pas utiliser un mot de passe numérique pour déverrouiller le volume.</span><span class="sxs-lookup"><span data-stu-id="1ee64-131">The *NumericalPassword* parameter has a valid format, but you cannot use a numerical password to unlock the volume.</span></span><br/>           |
| <dl> <span data-ttu-id="1ee64-132"><dt>**FVE \_ E \_ échec de \_ l’authentification**</dt> <dt>2150694951 (0x80310027)</dt></span><span class="sxs-lookup"><span data-stu-id="1ee64-132"><dt>**FVE\_E\_FAILED\_AUTHENTICATION**</dt> <dt>2150694951 (0x80310027)</dt></span></span> </dl>    | <span data-ttu-id="1ee64-133">Le paramètre *NumericalPassword* ne peut pas déverrouiller le volume.</span><span class="sxs-lookup"><span data-stu-id="1ee64-133">The *NumericalPassword* parameter cannot unlock the volume.</span></span><br/> <span data-ttu-id="1ee64-134">Un ou plusieurs protecteurs de clé du type « mot de passe numérique » existent, mais le paramètre *NumericalPassword* spécifié ne peut pas déverrouiller le volume.</span><span class="sxs-lookup"><span data-stu-id="1ee64-134">One or more key protectors of the type "Numerical Password" exist, but the specified *NumericalPassword* parameter cannot unlock the volume.</span></span><br/> |
| <dl> <span data-ttu-id="1ee64-135"><dt>**FVE \_ E \_ \_ \_ format de mot de passe non valide**</dt> <dt>2150694965 (0x80310035)</dt></span><span class="sxs-lookup"><span data-stu-id="1ee64-135"><dt>**FVE\_E\_INVALID\_PASSWORD\_FORMAT**</dt> <dt>2150694965 (0x80310035)</dt></span></span> </dl> | <span data-ttu-id="1ee64-136">Le format du paramètre *NumericalPassword* n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="1ee64-136">The *NumericalPassword* parameter does not have a valid format.</span></span><br/>                                                                                                                                                     |



 

## <a name="remarks"></a><span data-ttu-id="1ee64-137">Notes</span><span class="sxs-lookup"><span data-stu-id="1ee64-137">Remarks</span></span>

<span data-ttu-id="1ee64-138">Les fichiers format MOF (MOF) contiennent les définitions des classes Windows Management Instrumentation (WMI).</span><span class="sxs-lookup"><span data-stu-id="1ee64-138">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="1ee64-139">Les fichiers MOF ne sont pas installés dans le cadre de la SDK Windows.</span><span class="sxs-lookup"><span data-stu-id="1ee64-139">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="1ee64-140">Ils sont installés sur le serveur lorsque vous ajoutez le rôle associé à l’aide de l’Gestionnaire de serveur.</span><span class="sxs-lookup"><span data-stu-id="1ee64-140">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="1ee64-141">Pour plus d’informations sur les fichiers MOF, consultez [format MOF (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="1ee64-141">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="1ee64-142">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1ee64-142">Requirements</span></span>



| <span data-ttu-id="1ee64-143">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1ee64-143">Requirement</span></span> | <span data-ttu-id="1ee64-144">Valeur</span><span class="sxs-lookup"><span data-stu-id="1ee64-144">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1ee64-145">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1ee64-145">Minimum supported client</span></span><br/> | <span data-ttu-id="1ee64-146">Windows Vista entreprise, les applications de bureau Windows Vista Édition intégrale \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="1ee64-146">Windows Vista Enterprise, Windows Vista Ultimate \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="1ee64-147">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1ee64-147">Minimum supported server</span></span><br/> | <span data-ttu-id="1ee64-148">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="1ee64-148">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="1ee64-149">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="1ee64-149">Namespace</span></span><br/>                | <span data-ttu-id="1ee64-150">Racine \\ de \\ sécurité cimv2 \\ MicrosoftVolumeEncryption</span><span class="sxs-lookup"><span data-stu-id="1ee64-150">Root\\CIMV2\\Security\\MicrosoftVolumeEncryption</span></span><br/>                                             |
| <span data-ttu-id="1ee64-151">MOF</span><span class="sxs-lookup"><span data-stu-id="1ee64-151">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1ee64-152"><dt>Win32 \_ encryptablevolume. mof</dt></span><span class="sxs-lookup"><span data-stu-id="1ee64-152"><dt>Win32\_encryptablevolume.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1ee64-153">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1ee64-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1ee64-154">**\_EncryptableVolume Win32**</span><span class="sxs-lookup"><span data-stu-id="1ee64-154">**Win32\_EncryptableVolume**</span></span>](win32-encryptablevolume.md)
</dt> </dl>

 

 
