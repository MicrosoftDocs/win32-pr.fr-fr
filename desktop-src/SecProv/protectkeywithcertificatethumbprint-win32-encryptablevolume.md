---
description: Méthode ProtectKeyWithCertificateThumbprint de la classe Win32_EncryptableVolume-valide l’identificateur d’objet (OID) d’utilisation améliorée de la clé du certificat fourni.
ms.assetid: 7096cead-c44a-404c-b1e1-3e0ab27070f8
title: Méthode ProtectKeyWithCertificateThumbprint de la classe Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.ProtectKeyWithCertificateThumbprint
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 8c71684bf66d8d14df60c9ff09083f507b114024
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108110577"
---
# <a name="protectkeywithcertificatethumbprint-method-of-the-win32_encryptablevolume-class"></a><span data-ttu-id="f28b8-103">Méthode ProtectKeyWithCertificateThumbprint de la \_ classe Win32 EncryptableVolume</span><span class="sxs-lookup"><span data-stu-id="f28b8-103">ProtectKeyWithCertificateThumbprint method of the Win32\_EncryptableVolume class</span></span>

<span data-ttu-id="f28b8-104">La méthode **ProtectKeyWithCertificateThumbprint** de la [**classe \_ EncryptableVolume Win32**](win32-encryptablevolume.md) valide l' [*identificateur d’objet*](../secgloss/o-gly.md) (EKU) d’utilisation améliorée de la clé du certificat fourni.</span><span class="sxs-lookup"><span data-stu-id="f28b8-104">The **ProtectKeyWithCertificateThumbprint** method of the [**Win32\_EncryptableVolume**](win32-encryptablevolume.md) class validates the Enhanced Key Usage (EKU) [*object identifier*](../secgloss/o-gly.md) (OID) of the provided certificate.</span></span>

## <a name="syntax"></a><span data-ttu-id="f28b8-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f28b8-105">Syntax</span></span>


```mof
uint32 ProtectKeyWithCertificateThumbprint(
  [in, optional] string FriendlyName,
  [in]           string CertThumbprint,
  [out]          string VolumeKeyProtectorID
);
```



## <a name="parameters"></a><span data-ttu-id="f28b8-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f28b8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f28b8-107">*FriendlyName* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="f28b8-107">*FriendlyName* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="f28b8-108">Type : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="f28b8-108">Type: **string**</span></span>

<span data-ttu-id="f28b8-109">Chaîne qui spécifie un identificateur de chaîne assigné par l’utilisateur pour ce protecteur de clé.</span><span class="sxs-lookup"><span data-stu-id="f28b8-109">A string that specifies a user-assigned string identifier for this key protector.</span></span> <span data-ttu-id="f28b8-110">Si ce paramètre n’est pas spécifié, le paramètre *FriendlyName* est créé en utilisant le nom d’objet dans le certificat.</span><span class="sxs-lookup"><span data-stu-id="f28b8-110">If this parameter is not specified, the *FriendlyName* parameter is created by using the Subject Name in the certificate.</span></span>

</dd> <dt>

<span data-ttu-id="f28b8-111">*CertThumbprint* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="f28b8-111">*CertThumbprint* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f28b8-112">Type : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="f28b8-112">Type: **string**</span></span>

<span data-ttu-id="f28b8-113">Chaîne qui spécifie l’empreinte numérique du certificat.</span><span class="sxs-lookup"><span data-stu-id="f28b8-113">A string that specifies the certificate thumbprint.</span></span>

</dd> <dt>

<span data-ttu-id="f28b8-114">*VolumeKeyProtectorID* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="f28b8-114">*VolumeKeyProtectorID* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f28b8-115">Type : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="f28b8-115">Type: **string**</span></span>

<span data-ttu-id="f28b8-116">Chaîne qui identifie de façon unique le protecteur de clé créé qui peut être utilisé pour gérer ce protecteur de clé.</span><span class="sxs-lookup"><span data-stu-id="f28b8-116">A string that uniquely identifies the created key protector that can be used to manage this key protector.</span></span>

<span data-ttu-id="f28b8-117">Si le lecteur prend en charge le chiffrement matériel et que BitLocker n’a pas pris possession de la bande, la chaîne d’ID est définie sur « BitLocker » et le protecteur de clé est écrit dans les métadonnées par bande.</span><span class="sxs-lookup"><span data-stu-id="f28b8-117">If the drive supports hardware encryption and BitLocker has not taken band ownership, the ID string is set to "BitLocker" and the key protector is written to per band metadata.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f28b8-118">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="f28b8-118">Return value</span></span>

<span data-ttu-id="f28b8-119">Type : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f28b8-119">Type: **uint32**</span></span>

<span data-ttu-id="f28b8-120">Cette méthode retourne l’un des codes suivants, ou un autre code d’erreur en cas d’échec.</span><span class="sxs-lookup"><span data-stu-id="f28b8-120">This method returns one of the following codes or another error code if it fails.</span></span>



| <span data-ttu-id="f28b8-121">Code/valeur de retour</span><span class="sxs-lookup"><span data-stu-id="f28b8-121">Return code/value</span></span>                                                                                                                                                                                           | <span data-ttu-id="f28b8-122">Description</span><span class="sxs-lookup"><span data-stu-id="f28b8-122">Description</span></span>                                                                                                                                                                                                                                                                                    |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="f28b8-123"><dt>**S \_ OK**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="f28b8-123"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl>                                                           | <span data-ttu-id="f28b8-124">La méthode a réussi.</span><span class="sxs-lookup"><span data-stu-id="f28b8-124">The method was successful.</span></span><br/>                                                                                                                                                                                                                                                          |
| <dl> <span data-ttu-id="f28b8-125"><dt>**Erreur \_ \_Données non valides**</dt> <dt>13 (0xD)</dt></span><span class="sxs-lookup"><span data-stu-id="f28b8-125"><dt>**ERROR\_INVALID\_DATA**</dt> <dt>13 (0xD)</dt></span></span> </dl>                                           | <span data-ttu-id="f28b8-126">Les données ne sont pas correctes.</span><span class="sxs-lookup"><span data-stu-id="f28b8-126">The data is not valid.</span></span><br/>                                                                                                                                                                                                                                                              |
| <dl> <span data-ttu-id="f28b8-127"><dt>**FVE \_ E \_ \_ \_ OID NON-BitLocker**</dt> <dt>2150695022 (0x8031006E)</dt></span><span class="sxs-lookup"><span data-stu-id="f28b8-127"><dt>**FVE\_E\_NON\_BITLOCKER\_OID**</dt> <dt>2150695022 (0x8031006E)</dt></span></span> </dl>                     | <span data-ttu-id="f28b8-128">L’attribut EKU du certificat spécifié ne permet pas de l’utiliser pour Chiffrement de lecteur BitLocker.</span><span class="sxs-lookup"><span data-stu-id="f28b8-128">The EKU attribute of the specified certificate does not permit it to be used for BitLocker Drive Encryption.</span></span> <span data-ttu-id="f28b8-129">BitLocker ne requiert pas qu’un certificat ait un attribut EKU, mais s’il est configuré, il doit être défini sur un OID qui correspond à l’OID configuré pour BitLocker.</span><span class="sxs-lookup"><span data-stu-id="f28b8-129">BitLocker does not require that a certificate have an EKU attribute, but if one is configured, it must be set to an OID that matches the OID configured for BitLocker.</span></span><br/> |
| <dl> <span data-ttu-id="f28b8-130"><dt>**FVE \_ \_Certificat d’utilisateur de stratégie E \_ \_ \_ non \_ autorisé**</dt> <dt>2150695026 (0x80310072)</dt></span><span class="sxs-lookup"><span data-stu-id="f28b8-130"><dt>**FVE\_E\_POLICY\_USER\_CERTIFICATE\_NOT\_ALLOWED**</dt> <dt>2150695026 (0x80310072)</dt></span></span> </dl> | <span data-ttu-id="f28b8-131">Stratégie de groupe n’autorise pas l’utilisation de certificats d’utilisateur, tels que des cartes à puce, avec BitLocker.</span><span class="sxs-lookup"><span data-stu-id="f28b8-131">Group Policy does not permit user certificates, such as smart cards, to be used with BitLocker.</span></span><br/>                                                                                                                                                                                     |
| <dl> <span data-ttu-id="f28b8-132"><dt>**FVE \_ Le certificat de l’utilisateur de la \_ stratégie E \_ \_ \_ doit \_ être \_ HW**</dt> <dt>2150695028 (0x80310074)</dt></span><span class="sxs-lookup"><span data-stu-id="f28b8-132"><dt>**FVE\_E\_POLICY\_USER\_CERT\_MUST\_BE\_HW**</dt> <dt>2150695028 (0x80310074)</dt></span></span> </dl>        | <span data-ttu-id="f28b8-133">Stratégie de groupe nécessite que vous fournissiez une carte à puce pour utiliser BitLocker.</span><span class="sxs-lookup"><span data-stu-id="f28b8-133">Group Policy requires that you supply a smart card to use BitLocker.</span></span><br/>                                                                                                                                                                                                                |
| <dl> <span data-ttu-id="f28b8-134"><dt>**FVE \_ La \_ stratégie E \_ interdit \_ SELFSIGNED**</dt> <dt>2150695046 (0x80310086)</dt></span><span class="sxs-lookup"><span data-stu-id="f28b8-134"><dt>**FVE\_E\_POLICY\_PROHIBITS\_SELFSIGNED**</dt> <dt>2150695046 (0x80310086)</dt></span></span> </dl>           | <span data-ttu-id="f28b8-135">Stratégie de groupe n’autorise pas l’utilisation de certificats auto-signés.</span><span class="sxs-lookup"><span data-stu-id="f28b8-135">Group Policy does not permit the use of self-signed certificates.</span></span><br/>                                                                                                                                                                                                                   |



 

## <a name="remarks"></a><span data-ttu-id="f28b8-136">Notes </span><span class="sxs-lookup"><span data-stu-id="f28b8-136">Remarks</span></span>

<span data-ttu-id="f28b8-137">Si l’OID ne correspond pas à celui associé au contrôleur de service dans le registre, cette méthode échoue.</span><span class="sxs-lookup"><span data-stu-id="f28b8-137">If the OID does not match the one associated with the service controller in the registry, this method fails.</span></span> <span data-ttu-id="f28b8-138">Cela empêche l’utilisateur de définir les protecteurs de l’agent de récupération de données (DRA) manuellement sur le volume.</span><span class="sxs-lookup"><span data-stu-id="f28b8-138">This prevents the user from setting data recovery agent (DRA) protectors manually on the volume.</span></span> <span data-ttu-id="f28b8-139">Les DRA ne sont définies que par le service.</span><span class="sxs-lookup"><span data-stu-id="f28b8-139">DRAs are only to be set by the service.</span></span>

## <a name="requirements"></a><span data-ttu-id="f28b8-140">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f28b8-140">Requirements</span></span>



| <span data-ttu-id="f28b8-141">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f28b8-141">Requirement</span></span> | <span data-ttu-id="f28b8-142">Valeur</span><span class="sxs-lookup"><span data-stu-id="f28b8-142">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f28b8-143">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f28b8-143">Minimum supported client</span></span><br/> | <span data-ttu-id="f28b8-144">Windows 7 entreprise, les applications de bureau Windows 7 édition intégrale \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f28b8-144">Windows 7 Enterprise, Windows 7 Ultimate \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="f28b8-145">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f28b8-145">Minimum supported server</span></span><br/> | <span data-ttu-id="f28b8-146">Applications de bureau Windows Server 2008 R2 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f28b8-146">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="f28b8-147">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="f28b8-147">Namespace</span></span><br/>                | <span data-ttu-id="f28b8-148">Racine \\ de \\ sécurité cimv2 \\ MicrosoftVolumeEncryption</span><span class="sxs-lookup"><span data-stu-id="f28b8-148">Root\\CIMV2\\Security\\MicrosoftVolumeEncryption</span></span><br/>                                             |
| <span data-ttu-id="f28b8-149">MOF</span><span class="sxs-lookup"><span data-stu-id="f28b8-149">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f28b8-150"><dt>Win32 \_ encryptablevolume. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f28b8-150"><dt>Win32\_encryptablevolume.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f28b8-151">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f28b8-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f28b8-152">**\_EncryptableVolume Win32**</span><span class="sxs-lookup"><span data-stu-id="f28b8-152">**Win32\_EncryptableVolume**</span></span>](win32-encryptablevolume.md)
</dt> </dl>

 

 
