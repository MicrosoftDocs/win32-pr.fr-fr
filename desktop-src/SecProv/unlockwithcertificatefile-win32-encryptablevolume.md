---
description: Utilise le fichier de certificat fourni pour obtenir la clé dérivée et déverrouiller le volume chiffré.
ms.assetid: 41811d38-5c89-4372-9dbc-3de45b05011f
title: Méthode UnlockWithCertificateFile de la classe Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.UnlockWithCertificateFile
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: d7ce1705c0ec457f64eb825e49334e76a14c184c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106532154"
---
# <a name="unlockwithcertificatefile-method-of-the-win32_encryptablevolume-class"></a><span data-ttu-id="c7651-103">Méthode UnlockWithCertificateFile de la \_ classe Win32 EncryptableVolume</span><span class="sxs-lookup"><span data-stu-id="c7651-103">UnlockWithCertificateFile method of the Win32\_EncryptableVolume class</span></span>

<span data-ttu-id="c7651-104">La méthode **UnlockWithCertificateFile** de la [**classe \_ EncryptableVolume Win32**](win32-encryptablevolume.md) utilise le fichier de [*certificat*](../secgloss/c-gly.md) fourni pour obtenir la clé dérivée et déverrouiller le volume chiffré.</span><span class="sxs-lookup"><span data-stu-id="c7651-104">The **UnlockWithCertificateFile** method of the [**Win32\_EncryptableVolume**](win32-encryptablevolume.md) class uses the provided [*certificate*](../secgloss/c-gly.md) file to obtain the derived key and unlock the encrypted volume.</span></span>

> [!Note]  
> <span data-ttu-id="c7651-105">Si le disque prend en charge le chiffrement matériel, cette fonction définit l’état de la bande sur « déverrouillé ».</span><span class="sxs-lookup"><span data-stu-id="c7651-105">If the disc supports hardware encryption this function sets the band status to "unlocked""</span></span>

 

## <a name="syntax"></a><span data-ttu-id="c7651-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c7651-106">Syntax</span></span>


```mof
uint32 UnlockWithCertificateFile(
  [in] string FileName,
  [in] string PIN
);
```



## <a name="parameters"></a><span data-ttu-id="c7651-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c7651-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c7651-108">*Nom du fichier* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="c7651-108">*FileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c7651-109">Type : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="c7651-109">Type: **string**</span></span>

<span data-ttu-id="c7651-110">Chaîne qui spécifie l’emplacement et le nom du fichier. cer utilisé pour récupérer l’empreinte numérique du certificat.</span><span class="sxs-lookup"><span data-stu-id="c7651-110">A string that specifies the location and name of the .cer file used to retrieve the certificate thumbprint.</span></span> <span data-ttu-id="c7651-111">Un certificat de [*chiffrement*](../secgloss/e-gly.md) doit être exporté au format. cer [*Distinguished Encoding Rules*](../secgloss/d-gly.md) (der) binaire encodé [*x. 509*](../secgloss/x-gly.md) ou base-64 encodé x. 509.</span><span class="sxs-lookup"><span data-stu-id="c7651-111">An [*encryption*](../secgloss/e-gly.md) certificate must be exported in .cer format ([*Distinguished Encoding Rules*](../secgloss/d-gly.md) (DER)-encoded binary [*X.509*](../secgloss/x-gly.md) or Base-64 encoded X.509).</span></span> <span data-ttu-id="c7651-112">Le certificat de chiffrement peut être généré à partir de l’infrastructure PKI de Microsoft, d’une infrastructure à clé publique tierce ou auto-signé.</span><span class="sxs-lookup"><span data-stu-id="c7651-112">The encryption certificate may be generated from Microsoft PKI, third-party PKI, or self-signed.</span></span>

</dd> <dt>

<span data-ttu-id="c7651-113">*Code confidentiel* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="c7651-113">*PIN* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c7651-114">Type : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="c7651-114">Type: **string**</span></span>

<span data-ttu-id="c7651-115">Chaîne d’identification personnelle spécifiée par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="c7651-115">A user-specified personal identification string.</span></span> <span data-ttu-id="c7651-116">Cette chaîne doit être composée d’une séquence de 4 à 20 chiffres.</span><span class="sxs-lookup"><span data-stu-id="c7651-116">This string must consist of a sequence of 4 to 20 digits.</span></span> <span data-ttu-id="c7651-117">Cette chaîne est utilisée pour authentifier silencieusement le [*fournisseur de stockage de clés*](../secgloss/k-gly.md) (KSP) lorsqu’il est utilisé avec une [*carte à puce*](../secgloss/s-gly.md).</span><span class="sxs-lookup"><span data-stu-id="c7651-117">This string is used to silently authenticate the [*key storage provider*](../secgloss/k-gly.md) (KSP) when used with a [*smart card*](../secgloss/s-gly.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c7651-118">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="c7651-118">Return value</span></span>

<span data-ttu-id="c7651-119">Type : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c7651-119">Type: **uint32**</span></span>

<span data-ttu-id="c7651-120">Cette méthode retourne l’un des codes suivants, ou un autre code d’erreur en cas d’échec.</span><span class="sxs-lookup"><span data-stu-id="c7651-120">This method returns one of the following codes or another error code if it fails.</span></span>



| <span data-ttu-id="c7651-121">Code/valeur de retour</span><span class="sxs-lookup"><span data-stu-id="c7651-121">Return code/value</span></span>                                                                                                                                                                            | <span data-ttu-id="c7651-122">Description</span><span class="sxs-lookup"><span data-stu-id="c7651-122">Description</span></span>                                                                                                                                                                                                                                                              |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="c7651-123"><dt>**S \_ OK**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="c7651-123"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl>                                            | <span data-ttu-id="c7651-124">La méthode a réussi.</span><span class="sxs-lookup"><span data-stu-id="c7651-124">The method was successful.</span></span><br/>                                                                                                                                                                                                                                    |
| <dl> <span data-ttu-id="c7651-125"><dt>**Erreur \_ FICHIER \_ \_ introuvable**</dt> <dt>0000000002 (0X2)</dt></span><span class="sxs-lookup"><span data-stu-id="c7651-125"><dt>**ERROR\_FILE\_NOT\_FOUND**</dt> <dt>0000000002 (0x2)</dt></span></span> </dl>                 | <span data-ttu-id="c7651-126">Le système ne peut pas fichier le fichier spécifié.</span><span class="sxs-lookup"><span data-stu-id="c7651-126">The system cannot file the specified file.</span></span><br/>                                                                                                                                                                                                                    |
| <dl> <span data-ttu-id="c7651-127"><dt>**FVE \_ E \_ non \_ activée**</dt> <dt>2150694920 (0x80310008)</dt></span><span class="sxs-lookup"><span data-stu-id="c7651-127"><dt>**FVE\_E\_NOT\_ACTIVATED**</dt> <dt>2150694920 (0x80310008)</dt></span></span> </dl>           | <span data-ttu-id="c7651-128">BitLocker n’est pas activé sur le volume.</span><span class="sxs-lookup"><span data-stu-id="c7651-128">BitLocker is not enabled on the volume.</span></span> <span data-ttu-id="c7651-129">Ajoutez un protecteur de clé pour activer BitLocker.</span><span class="sxs-lookup"><span data-stu-id="c7651-129">Add a key protector to enable BitLocker.</span></span> <br/>                                                                                                                                                                             |
| <dl> <span data-ttu-id="c7651-130"><dt>**FVE \_ E \_ échec de \_ l’authentification**</dt> <dt>2150694951 (0x80310027)</dt></span><span class="sxs-lookup"><span data-stu-id="c7651-130"><dt>**FVE\_E\_FAILED\_AUTHENTICATION**</dt> <dt>2150694951 (0x80310027)</dt></span></span> </dl>   | <span data-ttu-id="c7651-131">Le volume ne peut pas être déverrouillé avec les informations fournies.</span><span class="sxs-lookup"><span data-stu-id="c7651-131">The volume cannot be unlocked with the provided information.</span></span> <br/>                                                                                                                                                                                                 |
| <dl> <span data-ttu-id="c7651-132"><dt>**FVE \_ \_Protecteur E \_ \_ introuvable**</dt> <dt>2150694963 (0x80310033)</dt></span><span class="sxs-lookup"><span data-stu-id="c7651-132"><dt>**FVE\_E\_PROTECTOR\_NOT\_FOUND**</dt> <dt>2150694963 (0x80310033)</dt></span></span> </dl>    | <span data-ttu-id="c7651-133">Le protecteur de clé fourni n’existe pas sur le volume.</span><span class="sxs-lookup"><span data-stu-id="c7651-133">The provided key protector does not exist on the volume.</span></span> <span data-ttu-id="c7651-134">Vous devez entrer un autre protecteur de clé.</span><span class="sxs-lookup"><span data-stu-id="c7651-134">You must enter another key protector.</span></span><br/>                                                                                                                                                                |
| <dl> <span data-ttu-id="c7651-135"><dt>**FVE \_ Échec de l' \_ \_ authentification \_ PRIVATEKEY**</dt> <dt>2150695060 (0x80310094)</dt></span><span class="sxs-lookup"><span data-stu-id="c7651-135"><dt>**FVE\_E\_PRIVATEKEY\_AUTH\_FAILED**</dt> <dt>2150695060 (0x80310094)</dt></span></span> </dl> | <span data-ttu-id="c7651-136">La [*clé privée*](../secgloss/p-gly.md), associée au certificat spécifié, n’a pas pu être autorisée.</span><span class="sxs-lookup"><span data-stu-id="c7651-136">The [*private key*](../secgloss/p-gly.md), associated with the specified certificate, could not be authorized.</span></span> <span data-ttu-id="c7651-137">L’autorisation de clé privée n’a pas été fournie ou l’autorisation fournie n’était pas valide.</span><span class="sxs-lookup"><span data-stu-id="c7651-137">The private key authorization was either not provided or the provided authorization was invalid.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="c7651-138">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c7651-138">Requirements</span></span>



| <span data-ttu-id="c7651-139">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c7651-139">Requirement</span></span> | <span data-ttu-id="c7651-140">Valeur</span><span class="sxs-lookup"><span data-stu-id="c7651-140">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c7651-141">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c7651-141">Minimum supported client</span></span><br/> | <span data-ttu-id="c7651-142">Windows 7 entreprise, les applications de bureau Windows 7 édition intégrale \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c7651-142">Windows 7 Enterprise, Windows 7 Ultimate \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="c7651-143">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c7651-143">Minimum supported server</span></span><br/> | <span data-ttu-id="c7651-144">Applications de bureau Windows Server 2008 R2 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c7651-144">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="c7651-145">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="c7651-145">Namespace</span></span><br/>                | <span data-ttu-id="c7651-146">Racine \\ de \\ sécurité cimv2 \\ MicrosoftVolumeEncryption</span><span class="sxs-lookup"><span data-stu-id="c7651-146">Root\\CIMV2\\Security\\MicrosoftVolumeEncryption</span></span><br/>                                             |
| <span data-ttu-id="c7651-147">MOF</span><span class="sxs-lookup"><span data-stu-id="c7651-147">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c7651-148"><dt>Win32 \_ encryptablevolume. mof</dt></span><span class="sxs-lookup"><span data-stu-id="c7651-148"><dt>Win32\_encryptablevolume.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c7651-149">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c7651-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c7651-150">**\_EncryptableVolume Win32**</span><span class="sxs-lookup"><span data-stu-id="c7651-150">**Win32\_EncryptableVolume**</span></span>](win32-encryptablevolume.md)
</dt> </dl>

 

 
