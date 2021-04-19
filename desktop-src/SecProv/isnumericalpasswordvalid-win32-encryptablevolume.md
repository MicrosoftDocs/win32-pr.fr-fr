---
description: Indique si le mot de passe numérique répond aux exigences de format spéciales pour cette valeur d’authentification.
ms.assetid: 3995405f-db4d-4f72-98dc-133a09f9cf65
title: Méthode IsNumericalPasswordValid de la classe Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.IsNumericalPasswordValid
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 7cec4aa31ae9ff6aee90c0f46ded935b3d553783
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106535478"
---
# <a name="isnumericalpasswordvalid-method-of-the-win32_encryptablevolume-class"></a><span data-ttu-id="a474d-103">Méthode IsNumericalPasswordValid de la \_ classe Win32 EncryptableVolume</span><span class="sxs-lookup"><span data-stu-id="a474d-103">IsNumericalPasswordValid method of the Win32\_EncryptableVolume class</span></span>

<span data-ttu-id="a474d-104">La méthode **IsNumericalPasswordValid** de la [**classe \_ EncryptableVolume Win32**](win32-encryptablevolume.md) indique si le mot de passe numérique répond aux exigences de format spéciales pour cette valeur d’authentification.</span><span class="sxs-lookup"><span data-stu-id="a474d-104">The **IsNumericalPasswordValid** method of the [**Win32\_EncryptableVolume**](win32-encryptablevolume.md) class indicates whether the numerical password meets the special format requirements for this authentication value.</span></span>

## <a name="syntax"></a><span data-ttu-id="a474d-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a474d-105">Syntax</span></span>


```mof
uint32 IsNumericalPasswordValid(
  [in]  string  NumericalPassword,
  [out] boolean IsNumericalPasswordValid
);
```



## <a name="parameters"></a><span data-ttu-id="a474d-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a474d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a474d-107">*NumericalPassword* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="a474d-107">*NumericalPassword* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a474d-108">Type : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="a474d-108">Type: **string**</span></span>

<span data-ttu-id="a474d-109">Chaîne qui spécifie le mot de passe numérique.</span><span class="sxs-lookup"><span data-stu-id="a474d-109">A string that specifies the numerical password.</span></span>

<span data-ttu-id="a474d-110">Le mot de passe numérique doit contenir 48 chiffres.</span><span class="sxs-lookup"><span data-stu-id="a474d-110">The numerical password must contain 48 digits.</span></span> <span data-ttu-id="a474d-111">Ces chiffres peuvent être divisés en 8 groupes de 6 chiffres, le dernier chiffre de chaque groupe indiquant une valeur de somme de contrôle pour le groupe.</span><span class="sxs-lookup"><span data-stu-id="a474d-111">These digits can be divided into 8 groups of 6 digits, with the last digit in each group indicating a checksum value for the group.</span></span> <span data-ttu-id="a474d-112">Chaque groupe de 6 chiffres doit être divisible par 11 et doit être inférieur à 720896.</span><span class="sxs-lookup"><span data-stu-id="a474d-112">Each group of 6 digits must be divisible by 11 and must be less than 720896.</span></span> <span data-ttu-id="a474d-113">En supposant qu’un groupe de six chiffres s’intitule x1, x2, x3, x4, x5 et x6, le chiffre de la somme de contrôle x6 est calculé comme-x1 + x2 – x3 + x4 – x5 Mod 11.</span><span class="sxs-lookup"><span data-stu-id="a474d-113">Assuming a group of six digits is labeled as x1, x2, x3, x4, x5, and x6, the checksum x6 digit is calculated as –x1+x2–x3+x4–x5 mod 11.</span></span>

<span data-ttu-id="a474d-114">Les groupes de chiffres peuvent éventuellement être séparés par un espace ou un trait d’Union.</span><span class="sxs-lookup"><span data-stu-id="a474d-114">The groups of digits can optionally be separated by a space or hyphen.</span></span> <span data-ttu-id="a474d-115">Par conséquent, « XXXXXX-XXXXXX-XXXXXX-XXXXXX-XXXXXX-XXXXXX-XXXXXX-XXXXXX » ou « xxxxxx XXXXXX XXXXXX XXXXXX XXXXXX XXXXXX XXXXXX XXXXXX » peut également contenir des mots de passe numériques valides.</span><span class="sxs-lookup"><span data-stu-id="a474d-115">Therefore, "xxxxxx-xxxxxx-xxxxxx-xxxxxx-xxxxxx-xxxxxx-xxxxxx-xxxxxx" or "xxxxxx xxxxxx xxxxxx xxxxxx xxxxxx xxxxxx xxxxxx xxxxxx" may also contain valid numerical passwords.</span></span>

</dd> <dt>

<span data-ttu-id="a474d-116">*IsNumericalPasswordValid* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="a474d-116">*IsNumericalPasswordValid* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a474d-117">Type : **booléen**</span><span class="sxs-lookup"><span data-stu-id="a474d-117">Type: **boolean**</span></span>

<span data-ttu-id="a474d-118">Valeur booléenne qui est true si le mot de passe numérique remplit les conditions de format spéciales pour cette valeur d’authentification ; sinon, la valeur est false.</span><span class="sxs-lookup"><span data-stu-id="a474d-118">A Boolean value that is true if the numerical password meets the special format requirements for this authentication value, otherwise the value is false.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a474d-119">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="a474d-119">Return value</span></span>

<span data-ttu-id="a474d-120">Type : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="a474d-120">Type: **uint32**</span></span>

<span data-ttu-id="a474d-121">Cette méthode retourne l’un des codes suivants, ou un autre code d’erreur en cas d’échec.</span><span class="sxs-lookup"><span data-stu-id="a474d-121">This method returns one of the following codes or another error code if it fails.</span></span>



| <span data-ttu-id="a474d-122">Code/valeur de retour</span><span class="sxs-lookup"><span data-stu-id="a474d-122">Return code/value</span></span>                                                                                                                                 | <span data-ttu-id="a474d-123">Description</span><span class="sxs-lookup"><span data-stu-id="a474d-123">Description</span></span>                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <span data-ttu-id="a474d-124"><dt>**S \_ OK**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="a474d-124"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl> | <span data-ttu-id="a474d-125">La méthode a réussi.</span><span class="sxs-lookup"><span data-stu-id="a474d-125">The method was successful.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="a474d-126">Notes</span><span class="sxs-lookup"><span data-stu-id="a474d-126">Remarks</span></span>

<span data-ttu-id="a474d-127">Les fichiers format MOF (MOF) contiennent les définitions des classes Windows Management Instrumentation (WMI).</span><span class="sxs-lookup"><span data-stu-id="a474d-127">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="a474d-128">Les fichiers MOF ne sont pas installés dans le cadre de la SDK Windows.</span><span class="sxs-lookup"><span data-stu-id="a474d-128">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="a474d-129">Ils sont installés sur le serveur lorsque vous ajoutez le rôle associé à l’aide de l’Gestionnaire de serveur.</span><span class="sxs-lookup"><span data-stu-id="a474d-129">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="a474d-130">Pour plus d’informations sur les fichiers MOF, consultez [format MOF (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="a474d-130">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="a474d-131">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a474d-131">Requirements</span></span>



| <span data-ttu-id="a474d-132">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a474d-132">Requirement</span></span> | <span data-ttu-id="a474d-133">Valeur</span><span class="sxs-lookup"><span data-stu-id="a474d-133">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a474d-134">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a474d-134">Minimum supported client</span></span><br/> | <span data-ttu-id="a474d-135">Windows Vista entreprise, les applications de bureau Windows Vista Édition intégrale \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a474d-135">Windows Vista Enterprise, Windows Vista Ultimate \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="a474d-136">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a474d-136">Minimum supported server</span></span><br/> | <span data-ttu-id="a474d-137">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a474d-137">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="a474d-138">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="a474d-138">Namespace</span></span><br/>                | <span data-ttu-id="a474d-139">Racine \\ de \\ sécurité cimv2 \\ MicrosoftVolumeEncryption</span><span class="sxs-lookup"><span data-stu-id="a474d-139">Root\\CIMV2\\Security\\MicrosoftVolumeEncryption</span></span><br/>                                             |
| <span data-ttu-id="a474d-140">MOF</span><span class="sxs-lookup"><span data-stu-id="a474d-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a474d-141"><dt>Win32 \_ encryptablevolume. mof</dt></span><span class="sxs-lookup"><span data-stu-id="a474d-141"><dt>Win32\_encryptablevolume.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a474d-142">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a474d-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a474d-143">**\_EncryptableVolume Win32**</span><span class="sxs-lookup"><span data-stu-id="a474d-143">**Win32\_EncryptableVolume**</span></span>](win32-encryptablevolume.md)
</dt> </dl>

 

 
