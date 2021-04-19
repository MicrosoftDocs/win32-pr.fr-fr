---
description: Récupère le mot de passe numérique d’un protecteur de clé donné.
ms.assetid: 5c4663fb-285d-471c-b355-82d553a7e686
title: Méthode GetKeyProtectorNumericalPassword de la classe Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.GetKeyProtectorNumericalPassword
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 73a6c774386cd88195074092323969d97f4d7563
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106513379"
---
# <a name="getkeyprotectornumericalpassword-method-of-the-win32_encryptablevolume-class"></a><span data-ttu-id="4b2de-103">Méthode GetKeyProtectorNumericalPassword de la \_ classe Win32 EncryptableVolume</span><span class="sxs-lookup"><span data-stu-id="4b2de-103">GetKeyProtectorNumericalPassword method of the Win32\_EncryptableVolume class</span></span>

<span data-ttu-id="4b2de-104">La méthode **GetKeyProtectorNumericalPassword** de la classe [**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md) récupère le mot de passe numérique d’un protecteur de clé donné du type approprié.</span><span class="sxs-lookup"><span data-stu-id="4b2de-104">The **GetKeyProtectorNumericalPassword** method of the [**Win32\_EncryptableVolume**](win32-encryptablevolume.md) class retrieves the numerical password for a given key protector of the appropriate type.</span></span>

<span data-ttu-id="4b2de-105">L’identificateur de protecteur de clé doit faire référence à un protecteur de clé de type « numérique Password ».</span><span class="sxs-lookup"><span data-stu-id="4b2de-105">The key protector identifier must refer to a key protector of type "Numerical Password".</span></span>

## <a name="syntax"></a><span data-ttu-id="4b2de-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="4b2de-106">Syntax</span></span>


```mof
uint32 GetKeyProtectorNumericalPassword(
  [in]  string VolumeKeyProtectorID,
  [out] string NumericalPassword
);
```



## <a name="parameters"></a><span data-ttu-id="4b2de-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="4b2de-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4b2de-108">*VolumeKeyProtectorID* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="4b2de-108">*VolumeKeyProtectorID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4b2de-109">Type : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="4b2de-109">Type: **string**</span></span>

<span data-ttu-id="4b2de-110">Identificateur de chaîne unique utilisé pour gérer un protecteur de clé de volume chiffré.</span><span class="sxs-lookup"><span data-stu-id="4b2de-110">A unique string identifier used to manage an encrypted volume key protector.</span></span>

</dd> <dt>

<span data-ttu-id="4b2de-111">*NumericalPassword* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="4b2de-111">*NumericalPassword* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4b2de-112">Type : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="4b2de-112">Type: **string**</span></span>

<span data-ttu-id="4b2de-113">Chaîne qui représente le mot de passe qui peut être utilisé pour déverrouiller le volume correspondant.</span><span class="sxs-lookup"><span data-stu-id="4b2de-113">A string that represents the password that can be used to unlock the corresponding volume.</span></span>

<span data-ttu-id="4b2de-114">Le mot de passe numérique est 48 chiffres.</span><span class="sxs-lookup"><span data-stu-id="4b2de-114">The numerical password is 48 digits.</span></span> <span data-ttu-id="4b2de-115">Ces chiffres sont divisés en 8 groupes de 6 chiffres, le dernier chiffre de chaque groupe indiquant une valeur de somme de contrôle pour le groupe.</span><span class="sxs-lookup"><span data-stu-id="4b2de-115">These digits are divided into 8 groups of 6 digits, with the last digit in each group indicating a checksum value for the group.</span></span> <span data-ttu-id="4b2de-116">En supposant qu’un groupe de six chiffres est étiqueté x1, x2, x3, x4, x5 et x6, le chiffre de la somme de contrôle x6 est calculé sous la forme-x1 + x2 – x3 + x4 – x5 Mod 11.</span><span class="sxs-lookup"><span data-stu-id="4b2de-116">Assuming that a group of six digits is labeled as x1, x2, x3, x4, x5, and x6, the checksum x6 digit is calculated as –x1+x2–x3+x4–x5 mod 11.</span></span>

<span data-ttu-id="4b2de-117">Les groupes de chiffres sont séparés par un trait d’Union.</span><span class="sxs-lookup"><span data-stu-id="4b2de-117">The groups of digits are separated by a hyphen.</span></span> <span data-ttu-id="4b2de-118">Par conséquent, « XXXXXX-XXXXXX-XXXXXX-XXXXXX-XXXXXX-XXXXXX-XXXXXX-XXXXXX » est le format du mot de passe retourné.</span><span class="sxs-lookup"><span data-stu-id="4b2de-118">Therefore, "xxxxxx-xxxxxx-xxxxxx-xxxxxx-xxxxxx-xxxxxx-xxxxxx-xxxxxx" is the format of the returned password.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4b2de-119">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="4b2de-119">Return value</span></span>

<span data-ttu-id="4b2de-120">Type : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="4b2de-120">Type: **uint32**</span></span>

<span data-ttu-id="4b2de-121">Cette méthode retourne l’un des codes suivants, ou un autre code d’erreur en cas d’échec.</span><span class="sxs-lookup"><span data-stu-id="4b2de-121">This method returns one of the following codes or another error code if it fails.</span></span>



| <span data-ttu-id="4b2de-122">Code/valeur de retour</span><span class="sxs-lookup"><span data-stu-id="4b2de-122">Return code/value</span></span>                                                                                                                                                                  | <span data-ttu-id="4b2de-123">Description</span><span class="sxs-lookup"><span data-stu-id="4b2de-123">Description</span></span>                                                                                                         |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="4b2de-124"><dt>**S \_ OK**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="4b2de-124"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl>                                  | <span data-ttu-id="4b2de-125">La méthode a réussi.</span><span class="sxs-lookup"><span data-stu-id="4b2de-125">The method was successful.</span></span><br/>                                                                               |
| <dl> <span data-ttu-id="4b2de-126"><dt>**FVE \_ E \_ Locked \_ volume**</dt> <dt>2150694912 (0x80310000)</dt></span><span class="sxs-lookup"><span data-stu-id="4b2de-126"><dt>**FVE\_E\_LOCKED\_VOLUME**</dt> <dt>2150694912 (0x80310000)</dt></span></span> </dl> | <span data-ttu-id="4b2de-127">Le volume est verrouillé.</span><span class="sxs-lookup"><span data-stu-id="4b2de-127">The volume is locked.</span></span><br/>                                                                                    |
| <dl> <span data-ttu-id="4b2de-128"><dt>**E \_ INVALIDARG**</dt> <dt>2147942487 (0x80070057)</dt></span><span class="sxs-lookup"><span data-stu-id="4b2de-128"><dt>**E\_INVALIDARG**</dt> <dt>2147942487 (0x80070057)</dt></span></span> </dl>          | <span data-ttu-id="4b2de-129">Le paramètre *VolumeKeyProtectorID* ne fait pas référence à un protecteur de clé du type « numérique Password ».</span><span class="sxs-lookup"><span data-stu-id="4b2de-129">The *VolumeKeyProtectorID* parameter does not refer to a key protector of the type "Numerical Password".</span></span><br/> |
| <dl> <span data-ttu-id="4b2de-130"><dt>**FVE \_ E \_ non \_ activée**</dt> <dt>2150694920 (0x80310008)</dt></span><span class="sxs-lookup"><span data-stu-id="4b2de-130"><dt>**FVE\_E\_NOT\_ACTIVATED**</dt> <dt>2150694920 (0x80310008)</dt></span></span> </dl> | <span data-ttu-id="4b2de-131">BitLocker n’est pas activé sur le volume.</span><span class="sxs-lookup"><span data-stu-id="4b2de-131">BitLocker is not enabled on the volume.</span></span> <span data-ttu-id="4b2de-132">Ajoutez un protecteur de clé pour activer BitLocker.</span><span class="sxs-lookup"><span data-stu-id="4b2de-132">Add a key protector to enable BitLocker.</span></span> <br/>                        |



 

## <a name="remarks"></a><span data-ttu-id="4b2de-133">Notes</span><span class="sxs-lookup"><span data-stu-id="4b2de-133">Remarks</span></span>

<span data-ttu-id="4b2de-134">Les fichiers format MOF (MOF) contiennent les définitions des classes Windows Management Instrumentation (WMI).</span><span class="sxs-lookup"><span data-stu-id="4b2de-134">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="4b2de-135">Les fichiers MOF ne sont pas installés dans le cadre de la SDK Windows.</span><span class="sxs-lookup"><span data-stu-id="4b2de-135">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="4b2de-136">Ils sont installés sur le serveur lorsque vous ajoutez le rôle associé à l’aide de l’Gestionnaire de serveur.</span><span class="sxs-lookup"><span data-stu-id="4b2de-136">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="4b2de-137">Pour plus d’informations sur les fichiers MOF, consultez [format MOF (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="4b2de-137">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="4b2de-138">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="4b2de-138">Requirements</span></span>



| <span data-ttu-id="4b2de-139">Condition requise</span><span class="sxs-lookup"><span data-stu-id="4b2de-139">Requirement</span></span> | <span data-ttu-id="4b2de-140">Valeur</span><span class="sxs-lookup"><span data-stu-id="4b2de-140">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4b2de-141">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4b2de-141">Minimum supported client</span></span><br/> | <span data-ttu-id="4b2de-142">Windows Vista entreprise, les applications de bureau Windows Vista Édition intégrale \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="4b2de-142">Windows Vista Enterprise, Windows Vista Ultimate \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="4b2de-143">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4b2de-143">Minimum supported server</span></span><br/> | <span data-ttu-id="4b2de-144">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="4b2de-144">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="4b2de-145">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="4b2de-145">Namespace</span></span><br/>                | <span data-ttu-id="4b2de-146">Racine \\ de \\ sécurité cimv2 \\ MicrosoftVolumeEncryption</span><span class="sxs-lookup"><span data-stu-id="4b2de-146">Root\\CIMV2\\Security\\MicrosoftVolumeEncryption</span></span><br/>                                             |
| <span data-ttu-id="4b2de-147">MOF</span><span class="sxs-lookup"><span data-stu-id="4b2de-147">MOF</span></span><br/>                      | <dl> <span data-ttu-id="4b2de-148"><dt>Win32 \_ encryptablevolume. mof</dt></span><span class="sxs-lookup"><span data-stu-id="4b2de-148"><dt>Win32\_encryptablevolume.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4b2de-149">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4b2de-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4b2de-150">**\_EncryptableVolume Win32**</span><span class="sxs-lookup"><span data-stu-id="4b2de-150">**Win32\_EncryptableVolume**</span></span>](win32-encryptablevolume.md)
</dt> </dl>

 

 
