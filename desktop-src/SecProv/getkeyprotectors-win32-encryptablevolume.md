---
description: Répertorie les protecteurs utilisés pour sécuriser la clé de chiffrement du volume.
ms.assetid: ea88f128-c835-49e3-a395-c5ba472fff4b
title: Méthode GetKeyProtectors de la classe Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.GetKeyProtectors
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 3a7d6a4110953d905b10eb4f7ef9a255af77897a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106512948"
---
# <a name="getkeyprotectors-method-of-the-win32_encryptablevolume-class"></a><span data-ttu-id="1e9b8-103">Méthode GetKeyProtectors de la \_ classe Win32 EncryptableVolume</span><span class="sxs-lookup"><span data-stu-id="1e9b8-103">GetKeyProtectors method of the Win32\_EncryptableVolume class</span></span>

<span data-ttu-id="1e9b8-104">La méthode **GetKeyProtectors** de la classe [**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md) répertorie les protecteurs utilisés pour sécuriser la clé de chiffrement du volume.</span><span class="sxs-lookup"><span data-stu-id="1e9b8-104">The **GetKeyProtectors** method of the [**Win32\_EncryptableVolume**](win32-encryptablevolume.md) class lists the protectors used to secure the volume's encryption key.</span></span> <span data-ttu-id="1e9b8-105">Si un type de protecteur est fourni, seuls les protecteurs de clé de volume du type spécifié sont retournés.</span><span class="sxs-lookup"><span data-stu-id="1e9b8-105">If a protector type is provided, then only volume key protectors of the specified type are returned.</span></span>

## <a name="syntax"></a><span data-ttu-id="1e9b8-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1e9b8-106">Syntax</span></span>


```mof
uint32 GetKeyProtectors(
  [in, optional] uint32 KeyProtectorType,
  [out]          string VolumeKeyProtectorID[]
);
```



## <a name="parameters"></a><span data-ttu-id="1e9b8-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="1e9b8-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1e9b8-108">*KeyProtectorType* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="1e9b8-108">*KeyProtectorType* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="1e9b8-109">Type : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="1e9b8-109">Type: **uint32**</span></span>

<span data-ttu-id="1e9b8-110">Entier non signé qui spécifie le type de protecteur de clé à retourner.</span><span class="sxs-lookup"><span data-stu-id="1e9b8-110">An unsigned integer that specifies the type of key protector to return.</span></span>

<span data-ttu-id="1e9b8-111">Si ce paramètre n’est pas spécifié, tous les protecteurs de clé disponibles du volume sont retournés.</span><span class="sxs-lookup"><span data-stu-id="1e9b8-111">If this parameter is not specified, all available key protectors of the volume are returned.</span></span>



| <span data-ttu-id="1e9b8-112">Valeur</span><span class="sxs-lookup"><span data-stu-id="1e9b8-112">Value</span></span>                                                                         | <span data-ttu-id="1e9b8-113">Signification</span><span class="sxs-lookup"><span data-stu-id="1e9b8-113">Meaning</span></span>                                                           |
|-------------------------------------------------------------------------------|-------------------------------------------------------------------|
| <dl> <span data-ttu-id="1e9b8-114"><dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="1e9b8-114"><dt>0</dt></span></span> </dl>  | <span data-ttu-id="1e9b8-115">Tous les types.</span><span class="sxs-lookup"><span data-stu-id="1e9b8-115">All types.</span></span><br/> <span data-ttu-id="1e9b8-116">Tous les protecteurs de clé sont retournés.</span><span class="sxs-lookup"><span data-stu-id="1e9b8-116">All key protectors are returned.</span></span><br/> |
| <dl> <span data-ttu-id="1e9b8-117"><dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="1e9b8-117"><dt>1</dt></span></span> </dl>  | <span data-ttu-id="1e9b8-118">Module de plateforme sécurisée (TPM) (TPM).</span><span class="sxs-lookup"><span data-stu-id="1e9b8-118">Trusted Platform Module (TPM).</span></span><br/>                         |
| <dl> <span data-ttu-id="1e9b8-119"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="1e9b8-119"><dt>2</dt></span></span> </dl>  | <span data-ttu-id="1e9b8-120">Clé externe.</span><span class="sxs-lookup"><span data-stu-id="1e9b8-120">External key.</span></span><br/>                                          |
| <dl> <span data-ttu-id="1e9b8-121"><dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="1e9b8-121"><dt>3</dt></span></span> </dl>  | <span data-ttu-id="1e9b8-122">Mot de passe numérique.</span><span class="sxs-lookup"><span data-stu-id="1e9b8-122">Numeric password.</span></span><br/>                                      |
| <dl> <span data-ttu-id="1e9b8-123"><dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="1e9b8-123"><dt>4</dt></span></span> </dl>  | <span data-ttu-id="1e9b8-124">TPM et code confidentiel.</span><span class="sxs-lookup"><span data-stu-id="1e9b8-124">TPM And PIN.</span></span><br/>                                           |
| <dl> <span data-ttu-id="1e9b8-125"><dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="1e9b8-125"><dt>5</dt></span></span> </dl>  | <span data-ttu-id="1e9b8-126">TPM et clé de démarrage.</span><span class="sxs-lookup"><span data-stu-id="1e9b8-126">TPM And Startup Key.</span></span><br/>                                   |
| <dl> <span data-ttu-id="1e9b8-127"><dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="1e9b8-127"><dt>6</dt></span></span> </dl>  | <span data-ttu-id="1e9b8-128">TPM et code confidentiel et clé de démarrage.</span><span class="sxs-lookup"><span data-stu-id="1e9b8-128">TPM And PIN And Startup Key.</span></span><br/>                           |
| <dl> <span data-ttu-id="1e9b8-129"><dt>7</dt></span><span class="sxs-lookup"><span data-stu-id="1e9b8-129"><dt>7</dt></span></span> </dl>  | <span data-ttu-id="1e9b8-130">Clé publique.</span><span class="sxs-lookup"><span data-stu-id="1e9b8-130">Public Key.</span></span><br/>                                            |
| <dl> <span data-ttu-id="1e9b8-131"><dt>8</dt></span><span class="sxs-lookup"><span data-stu-id="1e9b8-131"><dt>8</dt></span></span> </dl>  | <span data-ttu-id="1e9b8-132">Risquent.</span><span class="sxs-lookup"><span data-stu-id="1e9b8-132">Passphrase.</span></span><br/>                                            |
| <dl> <span data-ttu-id="1e9b8-133"><dt>9</dt></span><span class="sxs-lookup"><span data-stu-id="1e9b8-133"><dt>9</dt></span></span> </dl>  | <span data-ttu-id="1e9b8-134">Certificat TPM</span><span class="sxs-lookup"><span data-stu-id="1e9b8-134">TPM Certificate</span></span><br/>                                        |
| <dl> <span data-ttu-id="1e9b8-135"><dt>10</dt></span><span class="sxs-lookup"><span data-stu-id="1e9b8-135"><dt>10</dt></span></span> </dl> | <span data-ttu-id="1e9b8-136">Identificateur de sécurité (SID)</span><span class="sxs-lookup"><span data-stu-id="1e9b8-136">Security Identifier (SID)</span></span><br/>                              |



 

</dd> <dt>

<span data-ttu-id="1e9b8-137">*VolumeKeyProtectorID* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="1e9b8-137">*VolumeKeyProtectorID* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1e9b8-138">Type : **chaîne \[ \]**</span><span class="sxs-lookup"><span data-stu-id="1e9b8-138">Type: **string\[\]**</span></span>

<span data-ttu-id="1e9b8-139">Tableau de chaînes qui identifient les protecteurs de clé utilisés pour sécuriser la clé de chiffrement du volume.</span><span class="sxs-lookup"><span data-stu-id="1e9b8-139">An array of strings that identify the key protectors used to secure the volume's encryption key.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1e9b8-140">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="1e9b8-140">Return value</span></span>

<span data-ttu-id="1e9b8-141">Type : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="1e9b8-141">Type: **uint32**</span></span>

<span data-ttu-id="1e9b8-142">Cette méthode retourne l’un des codes suivants, ou un autre code d’erreur en cas d’échec.</span><span class="sxs-lookup"><span data-stu-id="1e9b8-142">This method returns one of the following codes or another error code if it fails.</span></span>



| <span data-ttu-id="1e9b8-143">Code/valeur de retour</span><span class="sxs-lookup"><span data-stu-id="1e9b8-143">Return code/value</span></span>                                                                                                                                                                  | <span data-ttu-id="1e9b8-144">Description</span><span class="sxs-lookup"><span data-stu-id="1e9b8-144">Description</span></span>                                                                                                    |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="1e9b8-145"><dt>**S \_ OK**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="1e9b8-145"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl>                                  | <span data-ttu-id="1e9b8-146">La méthode a réussi.</span><span class="sxs-lookup"><span data-stu-id="1e9b8-146">The method was successful.</span></span><br/>                                                                          |
| <dl> <span data-ttu-id="1e9b8-147"><dt>**E \_ INVALIDARG**</dt> <dt>2147942487 (0x80070057)</dt></span><span class="sxs-lookup"><span data-stu-id="1e9b8-147"><dt>**E\_INVALIDARG**</dt> <dt>2147942487 (0x80070057)</dt></span></span> </dl>          | <span data-ttu-id="1e9b8-148">Le paramètre *VolumeKeyProtectorID* est spécifié, mais ne fait pas référence à un *KeyProtectorType* valide.</span><span class="sxs-lookup"><span data-stu-id="1e9b8-148">The *VolumeKeyProtectorID* parameter is specified but does not refer to a valid *KeyProtectorType*.</span></span><br/> |
| <dl> <span data-ttu-id="1e9b8-149"><dt>**FVE \_ E \_ non \_ activée**</dt> <dt>2150694920 (0x80310008)</dt></span><span class="sxs-lookup"><span data-stu-id="1e9b8-149"><dt>**FVE\_E\_NOT\_ACTIVATED**</dt> <dt>2150694920 (0x80310008)</dt></span></span> </dl> | <span data-ttu-id="1e9b8-150">BitLocker n’est pas activé sur le volume.</span><span class="sxs-lookup"><span data-stu-id="1e9b8-150">BitLocker is not enabled on the volume.</span></span> <span data-ttu-id="1e9b8-151">Ajoutez un protecteur de clé pour activer BitLocker.</span><span class="sxs-lookup"><span data-stu-id="1e9b8-151">Add a key protector to enable BitLocker.</span></span> <br/>                   |



 

## <a name="remarks"></a><span data-ttu-id="1e9b8-152">Notes</span><span class="sxs-lookup"><span data-stu-id="1e9b8-152">Remarks</span></span>

<span data-ttu-id="1e9b8-153">Les fichiers format MOF (MOF) contiennent les définitions des classes Windows Management Instrumentation (WMI).</span><span class="sxs-lookup"><span data-stu-id="1e9b8-153">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="1e9b8-154">Les fichiers MOF ne sont pas installés dans le cadre de la SDK Windows.</span><span class="sxs-lookup"><span data-stu-id="1e9b8-154">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="1e9b8-155">Ils sont installés sur le serveur lorsque vous ajoutez le rôle associé à l’aide de l’Gestionnaire de serveur.</span><span class="sxs-lookup"><span data-stu-id="1e9b8-155">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="1e9b8-156">Pour plus d’informations sur les fichiers MOF, consultez [format MOF (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="1e9b8-156">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="1e9b8-157">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1e9b8-157">Requirements</span></span>



| <span data-ttu-id="1e9b8-158">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1e9b8-158">Requirement</span></span> | <span data-ttu-id="1e9b8-159">Valeur</span><span class="sxs-lookup"><span data-stu-id="1e9b8-159">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1e9b8-160">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1e9b8-160">Minimum supported client</span></span><br/> | <span data-ttu-id="1e9b8-161">Windows Vista entreprise, les applications de bureau Windows Vista Édition intégrale \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="1e9b8-161">Windows Vista Enterprise, Windows Vista Ultimate \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="1e9b8-162">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1e9b8-162">Minimum supported server</span></span><br/> | <span data-ttu-id="1e9b8-163">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="1e9b8-163">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="1e9b8-164">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="1e9b8-164">Namespace</span></span><br/>                | <span data-ttu-id="1e9b8-165">Racine \\ de \\ sécurité cimv2 \\ MicrosoftVolumeEncryption</span><span class="sxs-lookup"><span data-stu-id="1e9b8-165">Root\\CIMV2\\Security\\MicrosoftVolumeEncryption</span></span><br/>                                             |
| <span data-ttu-id="1e9b8-166">MOF</span><span class="sxs-lookup"><span data-stu-id="1e9b8-166">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1e9b8-167"><dt>Win32 \_ encryptablevolume. mof</dt></span><span class="sxs-lookup"><span data-stu-id="1e9b8-167"><dt>Win32\_encryptablevolume.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1e9b8-168">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1e9b8-168">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1e9b8-169">**\_EncryptableVolume Win32**</span><span class="sxs-lookup"><span data-stu-id="1e9b8-169">**Win32\_EncryptableVolume**</span></span>](win32-encryptablevolume.md)
</dt> </dl>

 

 
