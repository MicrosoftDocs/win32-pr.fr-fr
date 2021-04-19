---
description: Récupère la clé publique et l’empreinte de certificat d’un protecteur de clé publique.
ms.assetid: 86fd0562-feb9-4b85-b27b-30270f864d8e
title: Méthode GetKeyProtectorCertificate de la classe Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.GetKeyProtectorCertificate
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 3954d3c55c4695e501d486f309598569b1facfc0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106522142"
---
# <a name="getkeyprotectorcertificate-method-of-the-win32_encryptablevolume-class"></a><span data-ttu-id="eb831-103">Méthode GetKeyProtectorCertificate de la \_ classe Win32 EncryptableVolume</span><span class="sxs-lookup"><span data-stu-id="eb831-103">GetKeyProtectorCertificate method of the Win32\_EncryptableVolume class</span></span>

<span data-ttu-id="eb831-104">La méthode **GetKeyProtectorCertificate** de la classe [**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md) récupère la [*clé publique*](../secgloss/p-gly.md) et l’empreinte de [*certificat*](../secgloss/c-gly.md) pour un protecteur de clé publique.</span><span class="sxs-lookup"><span data-stu-id="eb831-104">The **GetKeyProtectorCertificate** method of the [**Win32\_EncryptableVolume**](win32-encryptablevolume.md) class retrieves the [*public key*](../secgloss/p-gly.md) and [*certificate*](../secgloss/c-gly.md) thumbprint for a public key protector.</span></span>

## <a name="syntax"></a><span data-ttu-id="eb831-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="eb831-105">Syntax</span></span>


```mof
uint32 GetKeyProtectorCertificate(
  [in]  string VolumeKeyProtectorID,
  [out] uint8  PublicKey[],
  [out] string CertThumbprint,
  [out] uint32 CertType
);
```



## <a name="parameters"></a><span data-ttu-id="eb831-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="eb831-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="eb831-107">*VolumeKeyProtectorID* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="eb831-107">*VolumeKeyProtectorID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="eb831-108">Type : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="eb831-108">Type: **string**</span></span>

<span data-ttu-id="eb831-109">Identificateur de chaîne unique utilisé pour gérer un protecteur de clé de volume chiffré.</span><span class="sxs-lookup"><span data-stu-id="eb831-109">A unique string identifier used to manage an encrypted volume key protector.</span></span>

</dd> <dt>

<span data-ttu-id="eb831-110">*PublicKey* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="eb831-110">*PublicKey* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="eb831-111">Type : **UInt8 \[ \]**</span><span class="sxs-lookup"><span data-stu-id="eb831-111">Type: **uint8\[\]**</span></span>

<span data-ttu-id="eb831-112">Tableau d’octets qui spécifie la clé publique.</span><span class="sxs-lookup"><span data-stu-id="eb831-112">An array of bytes that specifies the public key.</span></span>

</dd> <dt>

<span data-ttu-id="eb831-113">*CertThumbprint* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="eb831-113">*CertThumbprint* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="eb831-114">Type : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="eb831-114">Type: **string**</span></span>

<span data-ttu-id="eb831-115">Chaîne qui spécifie l’empreinte numérique du certificat.</span><span class="sxs-lookup"><span data-stu-id="eb831-115">A string that specifies the certificate thumbprint.</span></span>

</dd> <dt>

<span data-ttu-id="eb831-116">*Le type* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="eb831-116">*CertType* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="eb831-117">Type : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="eb831-117">Type: **uint32**</span></span>

<span data-ttu-id="eb831-118">Entier non signé qui spécifie le type du protecteur de clé.</span><span class="sxs-lookup"><span data-stu-id="eb831-118">An unsigned integer that specifies the type of the key protector.</span></span> <span data-ttu-id="eb831-119">Cet entier permet de faire la distinction entre l’agent de récupération de données (DRA) et les certificats utilisateur.</span><span class="sxs-lookup"><span data-stu-id="eb831-119">This integer is used to differentiate between data recovery agent (DRA) and user certificates.</span></span>



| <span data-ttu-id="eb831-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="eb831-120">Value</span></span>                                                                        | <span data-ttu-id="eb831-121">Signification</span><span class="sxs-lookup"><span data-stu-id="eb831-121">Meaning</span></span>                                  |
|------------------------------------------------------------------------------|------------------------------------------|
| <dl> <span data-ttu-id="eb831-122"><dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="eb831-122"><dt>1</dt></span></span> </dl> | <span data-ttu-id="eb831-123">Le certificat est un DRA.</span><span class="sxs-lookup"><span data-stu-id="eb831-123">The certificate is a DRA.</span></span><br/>     |
| <dl> <span data-ttu-id="eb831-124"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="eb831-124"><dt>2</dt></span></span> </dl> | <span data-ttu-id="eb831-125">Le certificat n’est pas un DRA.</span><span class="sxs-lookup"><span data-stu-id="eb831-125">The certificate is not a DRA.</span></span><br/> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="eb831-126">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="eb831-126">Return value</span></span>

<span data-ttu-id="eb831-127">Type : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="eb831-127">Type: **uint32**</span></span>

<span data-ttu-id="eb831-128">Cette méthode retourne l’un des codes suivants, ou un autre code d’erreur en cas d’échec.</span><span class="sxs-lookup"><span data-stu-id="eb831-128">This method returns one of the following codes or another error code if it fails.</span></span>



| <span data-ttu-id="eb831-129">Code/valeur de retour</span><span class="sxs-lookup"><span data-stu-id="eb831-129">Return code/value</span></span>                                                                                                                                                                                       | <span data-ttu-id="eb831-130">Description</span><span class="sxs-lookup"><span data-stu-id="eb831-130">Description</span></span>                                                                                                     |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="eb831-131"><dt>**S \_ OK**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="eb831-131"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl>                                                       | <span data-ttu-id="eb831-132">La méthode a réussi.</span><span class="sxs-lookup"><span data-stu-id="eb831-132">The method was successful.</span></span><br/>                                                                           |
| <dl> <span data-ttu-id="eb831-133"><dt>**E \_ INVALIDARG**</dt> <dt>2147942487 (0x80070057)</dt></span><span class="sxs-lookup"><span data-stu-id="eb831-133"><dt>**E\_INVALIDARG**</dt> <dt>2147942487 (0x80070057)</dt></span></span> </dl>                               | <span data-ttu-id="eb831-134">Le protecteur de clé spécifié n’est pas un protecteur de clé.</span><span class="sxs-lookup"><span data-stu-id="eb831-134">The specified key protector is not a key protector.</span></span> <span data-ttu-id="eb831-135">Vous devez entrer un autre protecteur de clé.</span><span class="sxs-lookup"><span data-stu-id="eb831-135">You must enter another key protector.</span></span><br/>            |
| <dl> <span data-ttu-id="eb831-136"><dt>**FVE \_ E \_ Locked \_ volume**</dt> <dt>2150694912 (0x80310000)</dt></span><span class="sxs-lookup"><span data-stu-id="eb831-136"><dt>**FVE\_E\_LOCKED\_VOLUME**</dt> <dt>2150694912 (0x80310000)</dt></span></span> </dl>                      | <span data-ttu-id="eb831-137">Ce lecteur est verrouillé par Chiffrement de lecteur BitLocker.</span><span class="sxs-lookup"><span data-stu-id="eb831-137">This drive is locked by BitLocker Drive Encryption.</span></span> <span data-ttu-id="eb831-138">Vous devez déverrouiller ce volume à partir du panneau de configuration.</span><span class="sxs-lookup"><span data-stu-id="eb831-138">You must unlock this volume from Control Panel.</span></span> <br/> |
| <dl> <span data-ttu-id="eb831-139"><dt>**FVE \_ E \_ non \_ activée**</dt> <dt>2150694920 (0x80310008)</dt></span><span class="sxs-lookup"><span data-stu-id="eb831-139"><dt>**FVE\_E\_NOT\_ACTIVATED**</dt> <dt>2150694920 (0x80310008)</dt></span></span> </dl>                      | <span data-ttu-id="eb831-140">BitLocker n’est pas activé sur le volume.</span><span class="sxs-lookup"><span data-stu-id="eb831-140">BitLocker is not enabled on the volume.</span></span> <span data-ttu-id="eb831-141">Ajoutez un protecteur de clé pour activer BitLocker.</span><span class="sxs-lookup"><span data-stu-id="eb831-141">Add a key protector to enable BitLocker.</span></span> <br/>                    |
| <dl> <span data-ttu-id="eb831-142"><dt>**FVE \_ \_Certificat d’utilisateur de stratégie E \_ \_ \_ requis**</dt> <dt>2150695027 (0x80310073)</dt></span><span class="sxs-lookup"><span data-stu-id="eb831-142"><dt>**FVE\_E\_POLICY\_USER\_CERTIFICATE\_REQUIRED**</dt> <dt>2150695027 (0x80310073)</dt></span></span> </dl> | <span data-ttu-id="eb831-143">Stratégie de groupe nécessite l’utilisation d’un certificat d’utilisateur, tel qu’une carte à puce.</span><span class="sxs-lookup"><span data-stu-id="eb831-143">Group Policy requires the use of a user certificate, such as a smart card.</span></span><br/>                           |



 

## <a name="remarks"></a><span data-ttu-id="eb831-144">Notes</span><span class="sxs-lookup"><span data-stu-id="eb831-144">Remarks</span></span>

<span data-ttu-id="eb831-145">Les fichiers format MOF (MOF) contiennent les définitions des classes Windows Management Instrumentation (WMI).</span><span class="sxs-lookup"><span data-stu-id="eb831-145">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="eb831-146">Les fichiers MOF ne sont pas installés dans le cadre de la SDK Windows.</span><span class="sxs-lookup"><span data-stu-id="eb831-146">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="eb831-147">Ils sont installés sur le serveur lorsque vous ajoutez le rôle associé à l’aide de l’Gestionnaire de serveur.</span><span class="sxs-lookup"><span data-stu-id="eb831-147">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="eb831-148">Pour plus d’informations sur les fichiers MOF, consultez [format MOF (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="eb831-148">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="eb831-149">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="eb831-149">Requirements</span></span>



| <span data-ttu-id="eb831-150">Condition requise</span><span class="sxs-lookup"><span data-stu-id="eb831-150">Requirement</span></span> | <span data-ttu-id="eb831-151">Valeur</span><span class="sxs-lookup"><span data-stu-id="eb831-151">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="eb831-152">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="eb831-152">Minimum supported client</span></span><br/> | <span data-ttu-id="eb831-153">Windows 7 entreprise, les applications de bureau Windows 7 édition intégrale \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="eb831-153">Windows 7 Enterprise, Windows 7 Ultimate \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="eb831-154">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="eb831-154">Minimum supported server</span></span><br/> | <span data-ttu-id="eb831-155">Applications de bureau Windows Server 2008 R2 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="eb831-155">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="eb831-156">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="eb831-156">Namespace</span></span><br/>                | <span data-ttu-id="eb831-157">Racine \\ de \\ sécurité cimv2 \\ MicrosoftVolumeEncryption</span><span class="sxs-lookup"><span data-stu-id="eb831-157">Root\\CIMV2\\Security\\MicrosoftVolumeEncryption</span></span><br/>                                             |
| <span data-ttu-id="eb831-158">MOF</span><span class="sxs-lookup"><span data-stu-id="eb831-158">MOF</span></span><br/>                      | <dl> <span data-ttu-id="eb831-159"><dt>Win32 \_ encryptablevolume. mof</dt></span><span class="sxs-lookup"><span data-stu-id="eb831-159"><dt>Win32\_encryptablevolume.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="eb831-160">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="eb831-160">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eb831-161">**\_EncryptableVolume Win32**</span><span class="sxs-lookup"><span data-stu-id="eb831-161">**Win32\_EncryptableVolume**</span></span>](win32-encryptablevolume.md)
</dt> </dl>

 

 
