---
description: Indique si les protecteurs sont disponibles pour le volume.
ms.assetid: 92a959ea-27ec-4d38-a955-846bfd7b3a60
title: Méthode IsKeyProtectorAvailable de la classe Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.IsKeyProtectorAvailable
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: a80f731bf77a39d1e16c7dfe9cca4884b80eec49
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104201350"
---
# <a name="iskeyprotectoravailable-method-of-the-win32_encryptablevolume-class"></a><span data-ttu-id="f5bf0-103">Méthode IsKeyProtectorAvailable de la \_ classe Win32 EncryptableVolume</span><span class="sxs-lookup"><span data-stu-id="f5bf0-103">IsKeyProtectorAvailable method of the Win32\_EncryptableVolume class</span></span>

<span data-ttu-id="f5bf0-104">La méthode **IsKeyProtectorAvailable** de la [**classe \_ EncryptableVolume Win32**](win32-encryptablevolume.md) indique si des protecteurs sont disponibles pour le volume.</span><span class="sxs-lookup"><span data-stu-id="f5bf0-104">The **IsKeyProtectorAvailable** method of the [**Win32\_EncryptableVolume**](win32-encryptablevolume.md) class indicates whether protectors are available for the volume.</span></span>

<span data-ttu-id="f5bf0-105">Si un type de protecteur est fourni, la méthode indique si les protecteurs du type spécifié sont disponibles pour le volume.</span><span class="sxs-lookup"><span data-stu-id="f5bf0-105">If a protector type is provided, then the method indicates whether protectors of the specified type are available for the volume.</span></span>

## <a name="syntax"></a><span data-ttu-id="f5bf0-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f5bf0-106">Syntax</span></span>


```mof
uint32 IsKeyProtectorAvailable(
  [in, optional] uint32  KeyProtectorType,
  [out]          boolean IsKeyProtectorAvailable
);
```



## <a name="parameters"></a><span data-ttu-id="f5bf0-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f5bf0-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f5bf0-108">*KeyProtectorType* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="f5bf0-108">*KeyProtectorType* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="f5bf0-109">Type : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f5bf0-109">Type: **uint32**</span></span>

<span data-ttu-id="f5bf0-110">Entier non signé qui indique le type de protecteur de clé de volume interrogé.</span><span class="sxs-lookup"><span data-stu-id="f5bf0-110">An unsigned integer that indicates the type of volume key protector queried.</span></span>

<span data-ttu-id="f5bf0-111">Si ce paramètre n’est pas spécifié, tous les protecteurs de clés disponibles du volume sont interrogés.</span><span class="sxs-lookup"><span data-stu-id="f5bf0-111">If this parameter is not specified, all available key protectors of the volume are queried.</span></span>



| <span data-ttu-id="f5bf0-112">Valeur</span><span class="sxs-lookup"><span data-stu-id="f5bf0-112">Value</span></span>                                                                         | <span data-ttu-id="f5bf0-113">Signification</span><span class="sxs-lookup"><span data-stu-id="f5bf0-113">Meaning</span></span>                                                          |
|-------------------------------------------------------------------------------|------------------------------------------------------------------|
| <dl> <span data-ttu-id="f5bf0-114"><dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="f5bf0-114"><dt>0</dt></span></span> </dl>  | <span data-ttu-id="f5bf0-115">Tous les types.</span><span class="sxs-lookup"><span data-stu-id="f5bf0-115">All types.</span></span><br/> <span data-ttu-id="f5bf0-116">Tous les protecteurs de clé sont interrogés.</span><span class="sxs-lookup"><span data-stu-id="f5bf0-116">All key protectors are queried.</span></span><br/> |
| <dl> <span data-ttu-id="f5bf0-117"><dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="f5bf0-117"><dt>1</dt></span></span> </dl>  | <span data-ttu-id="f5bf0-118">Module de plateforme sécurisée (TPM) (TPM).</span><span class="sxs-lookup"><span data-stu-id="f5bf0-118">Trusted Platform Module (TPM).</span></span><br/>                        |
| <dl> <span data-ttu-id="f5bf0-119"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="f5bf0-119"><dt>2</dt></span></span> </dl>  | <span data-ttu-id="f5bf0-120">Clé externe.</span><span class="sxs-lookup"><span data-stu-id="f5bf0-120">External key.</span></span><br/>                                         |
| <dl> <span data-ttu-id="f5bf0-121"><dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="f5bf0-121"><dt>3</dt></span></span> </dl>  | <span data-ttu-id="f5bf0-122">Mot de passe numérique.</span><span class="sxs-lookup"><span data-stu-id="f5bf0-122">Numerical password.</span></span><br/>                                   |
| <dl> <span data-ttu-id="f5bf0-123"><dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="f5bf0-123"><dt>4</dt></span></span> </dl>  | <span data-ttu-id="f5bf0-124">TPM et code confidentiel.</span><span class="sxs-lookup"><span data-stu-id="f5bf0-124">TPM And PIN.</span></span><br/>                                          |
| <dl> <span data-ttu-id="f5bf0-125"><dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="f5bf0-125"><dt>5</dt></span></span> </dl>  | <span data-ttu-id="f5bf0-126">TPM et clé de démarrage.</span><span class="sxs-lookup"><span data-stu-id="f5bf0-126">TPM And Startup Key.</span></span><br/>                                  |
| <dl> <span data-ttu-id="f5bf0-127"><dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="f5bf0-127"><dt>6</dt></span></span> </dl>  | <span data-ttu-id="f5bf0-128">TPM et code confidentiel et clé de démarrage.</span><span class="sxs-lookup"><span data-stu-id="f5bf0-128">TPM And PIN And Startup Key.</span></span><br/>                          |
| <dl> <span data-ttu-id="f5bf0-129"><dt>7</dt></span><span class="sxs-lookup"><span data-stu-id="f5bf0-129"><dt>7</dt></span></span> </dl>  | <span data-ttu-id="f5bf0-130">Clé publique.</span><span class="sxs-lookup"><span data-stu-id="f5bf0-130">Public Key.</span></span><br/>                                           |
| <dl> <span data-ttu-id="f5bf0-131"><dt>8</dt></span><span class="sxs-lookup"><span data-stu-id="f5bf0-131"><dt>8</dt></span></span> </dl>  | <span data-ttu-id="f5bf0-132">Risquent.</span><span class="sxs-lookup"><span data-stu-id="f5bf0-132">Passphrase.</span></span><br/>                                           |
| <dl> <span data-ttu-id="f5bf0-133"><dt>9</dt></span><span class="sxs-lookup"><span data-stu-id="f5bf0-133"><dt>9</dt></span></span> </dl>  | <span data-ttu-id="f5bf0-134">Certificat TPM</span><span class="sxs-lookup"><span data-stu-id="f5bf0-134">TPM Certificate</span></span><br/>                                       |
| <dl> <span data-ttu-id="f5bf0-135"><dt>10</dt></span><span class="sxs-lookup"><span data-stu-id="f5bf0-135"><dt>10</dt></span></span> </dl> | <span data-ttu-id="f5bf0-136">Identificateur de sécurité (SID)</span><span class="sxs-lookup"><span data-stu-id="f5bf0-136">Security Identifier (SID)</span></span><br/>                             |



 

</dd> <dt>

<span data-ttu-id="f5bf0-137">*IsKeyProtectorAvailable* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="f5bf0-137">*IsKeyProtectorAvailable* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f5bf0-138">Type : **booléen**</span><span class="sxs-lookup"><span data-stu-id="f5bf0-138">Type: **boolean**</span></span>

<span data-ttu-id="f5bf0-139">Valeur booléenne qui indique si un protecteur de clé de volume du type spécifié existe sur le volume.</span><span class="sxs-lookup"><span data-stu-id="f5bf0-139">A Boolean value that indicates whether a volume key protector of the specified type exists on the volume.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f5bf0-140">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="f5bf0-140">Return value</span></span>

<span data-ttu-id="f5bf0-141">Type : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f5bf0-141">Type: **uint32**</span></span>

<span data-ttu-id="f5bf0-142">Cette méthode retourne l’un des codes suivants, ou un autre code d’erreur en cas d’échec.</span><span class="sxs-lookup"><span data-stu-id="f5bf0-142">This method returns one of the following codes or another error code if it fails.</span></span>



| <span data-ttu-id="f5bf0-143">Code/valeur de retour</span><span class="sxs-lookup"><span data-stu-id="f5bf0-143">Return code/value</span></span>                                                                                                                                                         | <span data-ttu-id="f5bf0-144">Description</span><span class="sxs-lookup"><span data-stu-id="f5bf0-144">Description</span></span>                                                                                                |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="f5bf0-145"><dt>**S \_ OK**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="f5bf0-145"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl>                         | <span data-ttu-id="f5bf0-146">La méthode a réussi.</span><span class="sxs-lookup"><span data-stu-id="f5bf0-146">The method was successful.</span></span><br/>                                                                      |
| <dl> <span data-ttu-id="f5bf0-147"><dt>**E \_ INVALIDARG**</dt> <dt>2147942487 (0x80070057)</dt></span><span class="sxs-lookup"><span data-stu-id="f5bf0-147"><dt>**E\_INVALIDARG**</dt> <dt>2147942487 (0x80070057)</dt></span></span> </dl> | <span data-ttu-id="f5bf0-148">Le paramètre *KeyProtectorType* est spécifié, mais ne fait pas référence à un type de protecteur de clé valide.</span><span class="sxs-lookup"><span data-stu-id="f5bf0-148">The *KeyProtectorType* parameter is specified but does not refer to a valid key protector type.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="f5bf0-149">Notes</span><span class="sxs-lookup"><span data-stu-id="f5bf0-149">Remarks</span></span>

<span data-ttu-id="f5bf0-150">Les fichiers format MOF (MOF) contiennent les définitions des classes Windows Management Instrumentation (WMI).</span><span class="sxs-lookup"><span data-stu-id="f5bf0-150">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="f5bf0-151">Les fichiers MOF ne sont pas installés dans le cadre de la SDK Windows.</span><span class="sxs-lookup"><span data-stu-id="f5bf0-151">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="f5bf0-152">Ils sont installés sur le serveur lorsque vous ajoutez le rôle associé à l’aide de l’Gestionnaire de serveur.</span><span class="sxs-lookup"><span data-stu-id="f5bf0-152">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="f5bf0-153">Pour plus d’informations sur les fichiers MOF, consultez [format MOF (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="f5bf0-153">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="f5bf0-154">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f5bf0-154">Requirements</span></span>



| <span data-ttu-id="f5bf0-155">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f5bf0-155">Requirement</span></span> | <span data-ttu-id="f5bf0-156">Valeur</span><span class="sxs-lookup"><span data-stu-id="f5bf0-156">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f5bf0-157">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f5bf0-157">Minimum supported client</span></span><br/> | <span data-ttu-id="f5bf0-158">Windows Vista entreprise, les applications de bureau Windows Vista Édition intégrale \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f5bf0-158">Windows Vista Enterprise, Windows Vista Ultimate \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="f5bf0-159">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f5bf0-159">Minimum supported server</span></span><br/> | <span data-ttu-id="f5bf0-160">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f5bf0-160">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="f5bf0-161">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="f5bf0-161">Namespace</span></span><br/>                | <span data-ttu-id="f5bf0-162">Racine \\ de \\ sécurité cimv2 \\ MicrosoftVolumeEncryption</span><span class="sxs-lookup"><span data-stu-id="f5bf0-162">Root\\CIMV2\\Security\\MicrosoftVolumeEncryption</span></span><br/>                                             |
| <span data-ttu-id="f5bf0-163">MOF</span><span class="sxs-lookup"><span data-stu-id="f5bf0-163">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f5bf0-164"><dt>Win32 \_ encryptablevolume. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f5bf0-164"><dt>Win32\_encryptablevolume.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f5bf0-165">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f5bf0-165">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f5bf0-166">**\_EncryptableVolume Win32**</span><span class="sxs-lookup"><span data-stu-id="f5bf0-166">**Win32\_EncryptableVolume**</span></span>](win32-encryptablevolume.md)
</dt> </dl>

 

 
