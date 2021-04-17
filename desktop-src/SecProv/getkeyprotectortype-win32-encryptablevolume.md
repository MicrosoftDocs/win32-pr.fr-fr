---
description: Indique le type d’un protecteur de clé donné.
ms.assetid: 17cdde18-3979-4a19-b36e-aa71994148c9
title: Méthode GetKeyProtectorType de la classe Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.GetKeyProtectorType
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 483394f2e1c80f97442a9e6758f604093d513c3b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104529787"
---
# <a name="getkeyprotectortype-method-of-the-win32_encryptablevolume-class"></a><span data-ttu-id="415de-103">Méthode GetKeyProtectorType de la \_ classe Win32 EncryptableVolume</span><span class="sxs-lookup"><span data-stu-id="415de-103">GetKeyProtectorType method of the Win32\_EncryptableVolume class</span></span>

<span data-ttu-id="415de-104">La méthode **GetKeyProtectorType** de la [**classe \_ EncryptableVolume Win32**](win32-encryptablevolume.md) indique le type d’un protecteur de clé donné.</span><span class="sxs-lookup"><span data-stu-id="415de-104">The **GetKeyProtectorType** method of the [**Win32\_EncryptableVolume**](win32-encryptablevolume.md) class indicates the type of a given key protector.</span></span>

## <a name="syntax"></a><span data-ttu-id="415de-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="415de-105">Syntax</span></span>


```mof
uint32 GetKeyProtectorType(
  [in]  string VolumeKeyProtectorID,
  [out] uint32 KeyProtectorType
);
```



## <a name="parameters"></a><span data-ttu-id="415de-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="415de-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="415de-107">*VolumeKeyProtectorID* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="415de-107">*VolumeKeyProtectorID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="415de-108">Type : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="415de-108">Type: **string**</span></span>

<span data-ttu-id="415de-109">Identificateur de chaîne unique utilisé pour gérer un protecteur de clé de volume chiffré.</span><span class="sxs-lookup"><span data-stu-id="415de-109">A unique string identifier used to manage an encrypted volume key protector.</span></span>

</dd> <dt>

<span data-ttu-id="415de-110">*KeyProtectorType* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="415de-110">*KeyProtectorType* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="415de-111">Type : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="415de-111">Type: **uint32**</span></span>

<span data-ttu-id="415de-112">Entier non signé qui spécifie le type du protecteur de clé.</span><span class="sxs-lookup"><span data-stu-id="415de-112">An unsigned integer that specifies the type of the key protector.</span></span>



| <span data-ttu-id="415de-113">Valeur</span><span class="sxs-lookup"><span data-stu-id="415de-113">Value</span></span>                                                                         | <span data-ttu-id="415de-114">Signification</span><span class="sxs-lookup"><span data-stu-id="415de-114">Meaning</span></span>                                              |
|-------------------------------------------------------------------------------|------------------------------------------------------|
| <dl> <span data-ttu-id="415de-115"><dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="415de-115"><dt>0</dt></span></span> </dl>  | <span data-ttu-id="415de-116">Inconnu ou autre type de protecteur</span><span class="sxs-lookup"><span data-stu-id="415de-116">Unknown or other protector type</span></span><br/>           |
| <dl> <span data-ttu-id="415de-117"><dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="415de-117"><dt>1</dt></span></span> </dl>  | <span data-ttu-id="415de-118">Module de plateforme sécurisée</span><span class="sxs-lookup"><span data-stu-id="415de-118">Trusted Platform Module (TPM)</span></span><br/>             |
| <dl> <span data-ttu-id="415de-119"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="415de-119"><dt>2</dt></span></span> </dl>  | <span data-ttu-id="415de-120">Clé externe</span><span class="sxs-lookup"><span data-stu-id="415de-120">External key</span></span><br/>                              |
| <dl> <span data-ttu-id="415de-121"><dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="415de-121"><dt>3</dt></span></span> </dl>  | <span data-ttu-id="415de-122">Mot de passe numérique</span><span class="sxs-lookup"><span data-stu-id="415de-122">Numerical password</span></span><br/>                        |
| <dl> <span data-ttu-id="415de-123"><dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="415de-123"><dt>4</dt></span></span> </dl>  | <span data-ttu-id="415de-124">TPM et code confidentiel</span><span class="sxs-lookup"><span data-stu-id="415de-124">TPM And PIN</span></span><br/>                               |
| <dl> <span data-ttu-id="415de-125"><dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="415de-125"><dt>5</dt></span></span> </dl>  | <span data-ttu-id="415de-126">TPM et clé de démarrage</span><span class="sxs-lookup"><span data-stu-id="415de-126">TPM And Startup Key</span></span><br/>                       |
| <dl> <span data-ttu-id="415de-127"><dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="415de-127"><dt>6</dt></span></span> </dl>  | <span data-ttu-id="415de-128">TPM et clé de démarrage</span><span class="sxs-lookup"><span data-stu-id="415de-128">TPM And PIN And Startup Key</span></span><br/>               |
| <dl> <span data-ttu-id="415de-129"><dt>7</dt></span><span class="sxs-lookup"><span data-stu-id="415de-129"><dt>7</dt></span></span> </dl>  | <span data-ttu-id="415de-130">Clé publique</span><span class="sxs-lookup"><span data-stu-id="415de-130">Public Key</span></span><br/>                                |
| <dl> <span data-ttu-id="415de-131"><dt>8</dt></span><span class="sxs-lookup"><span data-stu-id="415de-131"><dt>8</dt></span></span> </dl>  | <span data-ttu-id="415de-132">Passphrase</span><span class="sxs-lookup"><span data-stu-id="415de-132">Passphrase</span></span><br/>                                |
| <dl> <span data-ttu-id="415de-133"><dt>9</dt></span><span class="sxs-lookup"><span data-stu-id="415de-133"><dt>9</dt></span></span> </dl>  | <span data-ttu-id="415de-134">Certificat TPM</span><span class="sxs-lookup"><span data-stu-id="415de-134">TPM Certificate</span></span><br/>                           |
| <dl> <span data-ttu-id="415de-135"><dt>10</dt></span><span class="sxs-lookup"><span data-stu-id="415de-135"><dt>10</dt></span></span> </dl> | <span data-ttu-id="415de-136">Protecteur CNG (CryptoAPI Next Generation)</span><span class="sxs-lookup"><span data-stu-id="415de-136">CryptoAPI Next Generation (CNG) Protector</span></span><br/> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="415de-137">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="415de-137">Return value</span></span>

<span data-ttu-id="415de-138">Type : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="415de-138">Type: **uint32**</span></span>

<span data-ttu-id="415de-139">Cette méthode retourne l’un des codes suivants, ou un autre code d’erreur en cas d’échec.</span><span class="sxs-lookup"><span data-stu-id="415de-139">This method returns one of the following codes or another error code if it fails.</span></span>



| <span data-ttu-id="415de-140">Code/valeur de retour</span><span class="sxs-lookup"><span data-stu-id="415de-140">Return code/value</span></span>                                                                                                                                                                  | <span data-ttu-id="415de-141">Description</span><span class="sxs-lookup"><span data-stu-id="415de-141">Description</span></span>                                                                                   |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="415de-142"><dt>**S \_ OK**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="415de-142"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl>                                  | <span data-ttu-id="415de-143">La méthode a réussi.</span><span class="sxs-lookup"><span data-stu-id="415de-143">The method was successful.</span></span><br/>                                                         |
| <dl> <span data-ttu-id="415de-144"><dt>**E \_ INVALIDARG**</dt> <dt>2147942487 (0x80070057)</dt></span><span class="sxs-lookup"><span data-stu-id="415de-144"><dt>**E\_INVALIDARG**</dt> <dt>2147942487 (0x80070057)</dt></span></span> </dl>          | <span data-ttu-id="415de-145">Le paramètre *VolumeKeyProtectorID* ne fait pas référence à un *KeyProtectorType* valide.</span><span class="sxs-lookup"><span data-stu-id="415de-145">The *VolumeKeyProtectorID* parameter does not refer to a valid *KeyProtectorType*.</span></span><br/> |
| <dl> <span data-ttu-id="415de-146"><dt>**FVE \_ E \_ non \_ activée**</dt> <dt>2150694920 (0x80310008)</dt></span><span class="sxs-lookup"><span data-stu-id="415de-146"><dt>**FVE\_E\_NOT\_ACTIVATED**</dt> <dt>2150694920 (0x80310008)</dt></span></span> </dl> | <span data-ttu-id="415de-147">BitLocker n’est pas activé sur le volume.</span><span class="sxs-lookup"><span data-stu-id="415de-147">BitLocker is not enabled on the volume.</span></span> <span data-ttu-id="415de-148">Ajoutez un protecteur de clé pour activer BitLocker.</span><span class="sxs-lookup"><span data-stu-id="415de-148">Add a key protector to enable BitLocker.</span></span> <br/>  |



 

## <a name="remarks"></a><span data-ttu-id="415de-149">Notes</span><span class="sxs-lookup"><span data-stu-id="415de-149">Remarks</span></span>

<span data-ttu-id="415de-150">Les fichiers format MOF (MOF) contiennent les définitions des classes Windows Management Instrumentation (WMI).</span><span class="sxs-lookup"><span data-stu-id="415de-150">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="415de-151">Les fichiers MOF ne sont pas installés dans le cadre de la SDK Windows.</span><span class="sxs-lookup"><span data-stu-id="415de-151">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="415de-152">Ils sont installés sur le serveur lorsque vous ajoutez le rôle associé à l’aide de l’Gestionnaire de serveur.</span><span class="sxs-lookup"><span data-stu-id="415de-152">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="415de-153">Pour plus d’informations sur les fichiers MOF, consultez [format MOF (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="415de-153">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="415de-154">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="415de-154">Requirements</span></span>



| <span data-ttu-id="415de-155">Condition requise</span><span class="sxs-lookup"><span data-stu-id="415de-155">Requirement</span></span> | <span data-ttu-id="415de-156">Valeur</span><span class="sxs-lookup"><span data-stu-id="415de-156">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="415de-157">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="415de-157">Minimum supported client</span></span><br/> | <span data-ttu-id="415de-158">Windows Vista entreprise, les applications de bureau Windows Vista Édition intégrale \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="415de-158">Windows Vista Enterprise, Windows Vista Ultimate \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="415de-159">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="415de-159">Minimum supported server</span></span><br/> | <span data-ttu-id="415de-160">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="415de-160">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="415de-161">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="415de-161">Namespace</span></span><br/>                | <span data-ttu-id="415de-162">Racine \\ de \\ sécurité cimv2 \\ MicrosoftVolumeEncryption</span><span class="sxs-lookup"><span data-stu-id="415de-162">Root\\CIMV2\\Security\\MicrosoftVolumeEncryption</span></span><br/>                                             |
| <span data-ttu-id="415de-163">MOF</span><span class="sxs-lookup"><span data-stu-id="415de-163">MOF</span></span><br/>                      | <dl> <span data-ttu-id="415de-164"><dt>Win32 \_ encryptablevolume. mof</dt></span><span class="sxs-lookup"><span data-stu-id="415de-164"><dt>Win32\_encryptablevolume.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="415de-165">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="415de-165">See also</span></span>

<dl> <dt>

[<span data-ttu-id="415de-166">**\_EncryptableVolume Win32**</span><span class="sxs-lookup"><span data-stu-id="415de-166">**Win32\_EncryptableVolume**</span></span>](win32-encryptablevolume.md)
</dt> </dl>

 

 
