---
description: Méthode ProtectKeyWithCertificateFile de la classe Win32_EncryptableVolume-valide l’identificateur d’objet (OID) d’utilisation améliorée de la clé du certificat fourni.
ms.assetid: cc716524-f976-4d75-84f3-693e277030e6
title: Méthode ProtectKeyWithCertificateFile de la classe Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.ProtectKeyWithCertificateFile
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: d61a0bd0d31c14f13edd9ef610e8f6d3ed20f037
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108110561"
---
# <a name="protectkeywithcertificatefile-method-of-the-win32_encryptablevolume-class"></a><span data-ttu-id="5e44b-103">Méthode ProtectKeyWithCertificateFile de la \_ classe Win32 EncryptableVolume</span><span class="sxs-lookup"><span data-stu-id="5e44b-103">ProtectKeyWithCertificateFile method of the Win32\_EncryptableVolume class</span></span>

<span data-ttu-id="5e44b-104">La méthode **ProtectKeyWithCertificateFile** de la [**classe \_ EncryptableVolume Win32**](win32-encryptablevolume.md) valide l' [*identificateur d’objet*](../secgloss/o-gly.md) (EKU) d’utilisation améliorée de la clé du certificat fourni.</span><span class="sxs-lookup"><span data-stu-id="5e44b-104">The **ProtectKeyWithCertificateFile** method of the [**Win32\_EncryptableVolume**](win32-encryptablevolume.md) class validates the Enhanced Key Usage (EKU) [*object identifier*](../secgloss/o-gly.md) (OID) of the provided certificate.</span></span>

## <a name="syntax"></a><span data-ttu-id="5e44b-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="5e44b-105">Syntax</span></span>


```mof
uint32 ProtectKeyWithCertificateFile(
  [in, optional] string FriendlyName,
  [in]           string FileName,
  [out]          string VolumeKeyProtectorID
);
```



## <a name="parameters"></a><span data-ttu-id="5e44b-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="5e44b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5e44b-107">*FriendlyName* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="5e44b-107">*FriendlyName* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="5e44b-108">Type : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="5e44b-108">Type: **string**</span></span>

<span data-ttu-id="5e44b-109">Chaîne qui spécifie un identificateur de chaîne assigné par l’utilisateur pour ce protecteur de clé.</span><span class="sxs-lookup"><span data-stu-id="5e44b-109">A string that specifies a user-assigned string identifier for this key protector.</span></span> <span data-ttu-id="5e44b-110">Si ce paramètre n’est pas spécifié, le paramètre *FriendlyName* est créé en utilisant le nom d’objet dans le certificat.</span><span class="sxs-lookup"><span data-stu-id="5e44b-110">If this parameter is not specified, the *FriendlyName* parameter is created by using the Subject Name in the certificate.</span></span>

</dd> <dt>

<span data-ttu-id="5e44b-111">*Nom du fichier* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="5e44b-111">*FileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5e44b-112">Type : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="5e44b-112">Type: **string**</span></span>

<span data-ttu-id="5e44b-113">Chaîne qui spécifie l’emplacement et le nom du fichier. cer utilisé pour activer BitLocker.</span><span class="sxs-lookup"><span data-stu-id="5e44b-113">A string that specifies the location and name of the .cer file used to enable BitLocker.</span></span> <span data-ttu-id="5e44b-114">Un certificat de chiffrement doit être exporté au format. cer [*Distinguished Encoding Rules*](../secgloss/d-gly.md) (der) binaire encodé [*x. 509*](../secgloss/x-gly.md) ou base-64 encodé x. 509.</span><span class="sxs-lookup"><span data-stu-id="5e44b-114">An encryption certificate must be exported in .cer format ([*Distinguished Encoding Rules*](../secgloss/d-gly.md) (DER)-encoded binary [*X.509*](../secgloss/x-gly.md) or Base-64 encoded X.509).</span></span> <span data-ttu-id="5e44b-115">Le certificat de chiffrement peut être généré à partir de l’infrastructure PKI de Microsoft, d’une infrastructure à clé publique tierce ou auto-signé.</span><span class="sxs-lookup"><span data-stu-id="5e44b-115">The encryption certificate may be generated from Microsoft PKI, third-party PKI, or self-signed.</span></span>

</dd> <dt>

<span data-ttu-id="5e44b-116">*VolumeKeyProtectorID* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="5e44b-116">*VolumeKeyProtectorID* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5e44b-117">Type : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="5e44b-117">Type: **string**</span></span>

<span data-ttu-id="5e44b-118">Chaîne qui identifie de façon unique le protecteur de clé créé qui peut être utilisé pour gérer ce protecteur de clé.</span><span class="sxs-lookup"><span data-stu-id="5e44b-118">A string that uniquely identifies the created key protector that can be used to manage this key protector.</span></span>

<span data-ttu-id="5e44b-119">Si le lecteur prend en charge le chiffrement matériel et que BitLocker n’a pas pris possession de la bande, la chaîne d’ID est définie sur « BitLocker » et le protecteur de clé est écrit dans les métadonnées par bande.</span><span class="sxs-lookup"><span data-stu-id="5e44b-119">If the drive supports hardware encryption and BitLocker has not taken band ownership, the ID string is set to "BitLocker" and the key protector is written to per band metadata.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5e44b-120">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="5e44b-120">Return value</span></span>

<span data-ttu-id="5e44b-121">Type : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="5e44b-121">Type: **uint32**</span></span>

<span data-ttu-id="5e44b-122">Cette méthode retourne l’un des codes suivants, ou un autre code d’erreur en cas d’échec.</span><span class="sxs-lookup"><span data-stu-id="5e44b-122">This method returns one of the following codes or another error code if it fails.</span></span>



| <span data-ttu-id="5e44b-123">Code/valeur de retour</span><span class="sxs-lookup"><span data-stu-id="5e44b-123">Return code/value</span></span>                                                                                                                                                                                           | <span data-ttu-id="5e44b-124">Description</span><span class="sxs-lookup"><span data-stu-id="5e44b-124">Description</span></span>                                                                                                                                                                                                                                                                                    |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="5e44b-125"><dt>**S \_ OK**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="5e44b-125"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl>                                                           | <span data-ttu-id="5e44b-126">La méthode a réussi.</span><span class="sxs-lookup"><span data-stu-id="5e44b-126">The method was successful.</span></span><br/>                                                                                                                                                                                                                                                          |
| <dl> <span data-ttu-id="5e44b-127"><dt>**FVE \_ E \_ \_ \_ OID NON-BitLocker**</dt> <dt>2150695022 (0x8031006E)</dt></span><span class="sxs-lookup"><span data-stu-id="5e44b-127"><dt>**FVE\_E\_NON\_BITLOCKER\_OID**</dt> <dt>2150695022 (0x8031006E)</dt></span></span> </dl>                     | <span data-ttu-id="5e44b-128">L’attribut EKU du certificat spécifié ne permet pas de l’utiliser pour Chiffrement de lecteur BitLocker.</span><span class="sxs-lookup"><span data-stu-id="5e44b-128">The EKU attribute of the specified certificate does not permit it to be used for BitLocker Drive Encryption.</span></span> <span data-ttu-id="5e44b-129">BitLocker ne requiert pas qu’un certificat ait un attribut EKU, mais s’il est configuré, il doit être défini sur un OID qui correspond à l’OID configuré pour BitLocker.</span><span class="sxs-lookup"><span data-stu-id="5e44b-129">BitLocker does not require that a certificate have an EKU attribute, but if one is configured, it must be set to an OID that matches the OID configured for BitLocker.</span></span><br/> |
| <dl> <span data-ttu-id="5e44b-130"><dt>**FVE \_ \_Certificat d’utilisateur de stratégie E \_ \_ \_ non \_ autorisé**</dt> <dt>2150695026 (0x80310072)</dt></span><span class="sxs-lookup"><span data-stu-id="5e44b-130"><dt>**FVE\_E\_POLICY\_USER\_CERTIFICATE\_NOT\_ALLOWED**</dt> <dt>2150695026 (0x80310072)</dt></span></span> </dl> | <span data-ttu-id="5e44b-131">Stratégie de groupe n’autorise pas l’utilisation de certificats d’utilisateur, tels que des cartes à puce, avec BitLocker.</span><span class="sxs-lookup"><span data-stu-id="5e44b-131">Group Policy does not permit user certificates, such as smart cards, to be used with BitLocker.</span></span><br/>                                                                                                                                                                                     |
| <dl> <span data-ttu-id="5e44b-132"><dt>**FVE \_ Le certificat de l’utilisateur de la \_ stratégie E \_ \_ \_ doit \_ être \_ HW**</dt> <dt>2150695028 (0x80310074)</dt></span><span class="sxs-lookup"><span data-stu-id="5e44b-132"><dt>**FVE\_E\_POLICY\_USER\_CERT\_MUST\_BE\_HW**</dt> <dt>2150695028 (0x80310074)</dt></span></span> </dl>        | <span data-ttu-id="5e44b-133">Stratégie de groupe nécessite que vous fournissiez une carte à puce pour utiliser BitLocker.</span><span class="sxs-lookup"><span data-stu-id="5e44b-133">Group Policy requires that you supply a smart card to use BitLocker.</span></span><br/>                                                                                                                                                                                                                |
| <dl> <span data-ttu-id="5e44b-134"><dt>**FVE \_ La \_ stratégie E \_ interdit \_ SELFSIGNED**</dt> <dt>2150695046 (0x80310086)</dt></span><span class="sxs-lookup"><span data-stu-id="5e44b-134"><dt>**FVE\_E\_POLICY\_PROHIBITS\_SELFSIGNED**</dt> <dt>2150695046 (0x80310086)</dt></span></span> </dl>           | <span data-ttu-id="5e44b-135">Stratégie de groupe n’autorise pas l’utilisation de certificats auto-signés.</span><span class="sxs-lookup"><span data-stu-id="5e44b-135">Group Policy does not permit the use of self-signed certificates.</span></span><br/>                                                                                                                                                                                                                   |
| <dl> <span data-ttu-id="5e44b-136"><dt>**Erreur \_ FICHIER \_ \_ introuvable**</dt> <dt>0000000002 (0X2)</dt></span><span class="sxs-lookup"><span data-stu-id="5e44b-136"><dt>**ERROR\_FILE\_NOT\_FOUND**</dt> <dt>0000000002 (0x2)</dt></span></span> </dl>                                | <span data-ttu-id="5e44b-137">Le système ne peut pas trouver le fichier spécifié.</span><span class="sxs-lookup"><span data-stu-id="5e44b-137">The system cannot find the specified file.</span></span><br/>                                                                                                                                                                                                                                          |



 

## <a name="remarks"></a><span data-ttu-id="5e44b-138">Notes </span><span class="sxs-lookup"><span data-stu-id="5e44b-138">Remarks</span></span>

<span data-ttu-id="5e44b-139">Si l’OID ne correspond pas à celui associé au contrôleur de service dans le registre, cette méthode échoue.</span><span class="sxs-lookup"><span data-stu-id="5e44b-139">If the OID does not match the one associated with the service controller in the registry, this method fails.</span></span> <span data-ttu-id="5e44b-140">Cela empêche l’utilisateur de définir les protecteurs de l’agent de récupération de données (DRA) manuellement sur le volume.</span><span class="sxs-lookup"><span data-stu-id="5e44b-140">This prevents the user from setting data recovery agent (DRA) protectors manually on the volume.</span></span> <span data-ttu-id="5e44b-141">Les DRA ne sont définies que par le service.</span><span class="sxs-lookup"><span data-stu-id="5e44b-141">DRAs are only to be set by the service.</span></span>

## <a name="requirements"></a><span data-ttu-id="5e44b-142">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5e44b-142">Requirements</span></span>



| <span data-ttu-id="5e44b-143">Condition requise</span><span class="sxs-lookup"><span data-stu-id="5e44b-143">Requirement</span></span> | <span data-ttu-id="5e44b-144">Valeur</span><span class="sxs-lookup"><span data-stu-id="5e44b-144">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5e44b-145">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5e44b-145">Minimum supported client</span></span><br/> | <span data-ttu-id="5e44b-146">Windows 7 entreprise, les applications de bureau Windows 7 édition intégrale \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="5e44b-146">Windows 7 Enterprise, Windows 7 Ultimate \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="5e44b-147">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5e44b-147">Minimum supported server</span></span><br/> | <span data-ttu-id="5e44b-148">Applications de bureau Windows Server 2008 R2 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="5e44b-148">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="5e44b-149">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="5e44b-149">Namespace</span></span><br/>                | <span data-ttu-id="5e44b-150">Racine \\ de \\ sécurité cimv2 \\ MicrosoftVolumeEncryption</span><span class="sxs-lookup"><span data-stu-id="5e44b-150">Root\\CIMV2\\Security\\MicrosoftVolumeEncryption</span></span><br/>                                             |
| <span data-ttu-id="5e44b-151">MOF</span><span class="sxs-lookup"><span data-stu-id="5e44b-151">MOF</span></span><br/>                      | <dl> <span data-ttu-id="5e44b-152"><dt>Win32 \_ encryptablevolume. mof</dt></span><span class="sxs-lookup"><span data-stu-id="5e44b-152"><dt>Win32\_encryptablevolume.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5e44b-153">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5e44b-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5e44b-154">**\_EncryptableVolume Win32**</span><span class="sxs-lookup"><span data-stu-id="5e44b-154">**Win32\_EncryptableVolume**</span></span>](win32-encryptablevolume.md)
</dt> </dl>

 

 
