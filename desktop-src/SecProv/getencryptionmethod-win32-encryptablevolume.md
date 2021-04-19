---
description: Indique l’algorithme de chiffrement et la taille de clé utilisés sur le volume.
ms.assetid: 89df3dfc-4789-4d3c-b267-d8e26758e754
title: Méthode GetEncryptionMethod de la classe Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.GetEncryptionMethod
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 16fb9b00976b652bcc9643ab5ec4912029898424
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106521318"
---
# <a name="getencryptionmethod-method-of-the-win32_encryptablevolume-class"></a><span data-ttu-id="4f34c-103">Méthode GetEncryptionMethod de la \_ classe Win32 EncryptableVolume</span><span class="sxs-lookup"><span data-stu-id="4f34c-103">GetEncryptionMethod method of the Win32\_EncryptableVolume class</span></span>

<span data-ttu-id="4f34c-104">La méthode **GetEncryptionMethod** de la classe [**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md) indique l’algorithme de chiffrement et la taille de clé utilisés sur le volume.</span><span class="sxs-lookup"><span data-stu-id="4f34c-104">The **GetEncryptionMethod** method of the [**Win32\_EncryptableVolume**](win32-encryptablevolume.md) class indicates the encryption algorithm and key size used on the volume.</span></span>

## <a name="syntax"></a><span data-ttu-id="4f34c-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="4f34c-105">Syntax</span></span>


```mof
uint32 GetEncryptionMethod(
  [out] uint32 EncryptionMethod,
  [out] string SelfEncryptionDriveEncryptionMethod
);
```



## <a name="parameters"></a><span data-ttu-id="4f34c-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="4f34c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4f34c-107">*EncryptionMethod* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="4f34c-107">*EncryptionMethod* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4f34c-108">Type : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="4f34c-108">Type: **uint32**</span></span>

<span data-ttu-id="4f34c-109">Entier non signé qui spécifie l’algorithme de chiffrement et la taille de clé utilisés sur le volume.</span><span class="sxs-lookup"><span data-stu-id="4f34c-109">An unsigned integer that specifies the encryption algorithm and key size used on the volume.</span></span>



| <span data-ttu-id="4f34c-110">Valeur</span><span class="sxs-lookup"><span data-stu-id="4f34c-110">Value</span></span>                                                                                                                                                                                                                                          | <span data-ttu-id="4f34c-111">Signification</span><span class="sxs-lookup"><span data-stu-id="4f34c-111">Meaning</span></span>                                                                                                                                                                                                                                                           |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="None"></span><span id="none"></span><span id="NONE"></span><dl> <span data-ttu-id="4f34c-112"><dt>**Aucun**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="4f34c-112"><dt>**None**</dt> <dt>0</dt></span></span> </dl>                                | <span data-ttu-id="4f34c-113">Le volume n’est pas chiffré.</span><span class="sxs-lookup"><span data-stu-id="4f34c-113">The volume is not encrypted.</span></span><br/>                                                                                                                                                                                                                           |
| <span id="AES_128_WITH_DIFFUSER"></span><span id="aes_128_with_diffuser"></span><dl> <span data-ttu-id="4f34c-114"><dt>**AES \_ 128 \_ avec \_ diffuseur**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="4f34c-114"><dt>**AES\_128\_WITH\_DIFFUSER**</dt> <dt>1</dt></span></span> </dl> | <span data-ttu-id="4f34c-115">Le volume a été entièrement ou partiellement chiffré avec l’algorithme Advanced Encryption Standard (AES) amélioré avec une couche de diffuseurs, avec une taille de clé AES de 128 bits.</span><span class="sxs-lookup"><span data-stu-id="4f34c-115">The volume has been fully or partially encrypted with the Advanced Encryption Standard (AES) algorithm enhanced with a diffuser layer, using an AES key size of 128 bits.</span></span> <span data-ttu-id="4f34c-116">Cette méthode n’est plus disponible sur les appareils exécutant Windows 8.1 ou une version ultérieure.</span><span class="sxs-lookup"><span data-stu-id="4f34c-116">This method is no longer available on devices running Windows 8.1 or higher.</span></span><br/> |
| <span id="AES_256_WITH_DIFFUSER"></span><span id="aes_256_with_diffuser"></span><dl> <span data-ttu-id="4f34c-117"><dt>**AES \_ 256 \_ avec \_ diffuseur**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="4f34c-117"><dt>**AES\_256\_WITH\_DIFFUSER**</dt> <dt>2</dt></span></span> </dl> | <span data-ttu-id="4f34c-118">Le volume a été entièrement ou partiellement chiffré avec l’algorithme Advanced Encryption Standard (AES) amélioré avec une couche de diffuseurs, avec une taille de clé AES de 256 bits.</span><span class="sxs-lookup"><span data-stu-id="4f34c-118">The volume has been fully or partially encrypted with the Advanced Encryption Standard (AES) algorithm enhanced with a diffuser layer, using an AES key size of 256 bits.</span></span> <span data-ttu-id="4f34c-119">Cette méthode n’est plus disponible sur les appareils exécutant Windows 8.1 ou une version ultérieure.</span><span class="sxs-lookup"><span data-stu-id="4f34c-119">This method is no longer available on devices running Windows 8.1 or higher.</span></span><br/> |
| <span id="AES_128"></span><span id="aes_128"></span><dl> <span data-ttu-id="4f34c-120"><dt>**AES \_ 128**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="4f34c-120"><dt>**AES\_128**</dt> <dt>3</dt></span></span> </dl>                                             | <span data-ttu-id="4f34c-121">Le volume a été entièrement ou partiellement chiffré avec l’algorithme Advanced Encryption Standard (AES), avec une taille de clé AES de 128 bits.</span><span class="sxs-lookup"><span data-stu-id="4f34c-121">The volume has been fully or partially encrypted with the Advanced Encryption Standard (AES) algorithm, using an AES key size of 128 bits.</span></span><br/>                                                                                                             |
| <span id="AES_256"></span><span id="aes_256"></span><dl> <span data-ttu-id="4f34c-122"><dt>**AES \_ 256**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="4f34c-122"><dt>**AES\_256**</dt> <dt>4</dt></span></span> </dl>                                             | <span data-ttu-id="4f34c-123">Le volume a été entièrement ou partiellement chiffré avec l’algorithme Advanced Encryption Standard (AES), avec une taille de clé AES de 256 bits.</span><span class="sxs-lookup"><span data-stu-id="4f34c-123">The volume has been fully or partially encrypted with the Advanced Encryption Standard (AES) algorithm, using an AES key size of 256 bits.</span></span><br/>                                                                                                             |
| <span id="HARDWARE_ENCRYPTION"></span><span id="hardware_encryption"></span><dl> <span data-ttu-id="4f34c-124"><dt>**Matériel \_ CHIFFREment**</dt> <dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="4f34c-124"><dt>**HARDWARE\_ENCRYPTION**</dt> <dt>5</dt></span></span> </dl>         | <span data-ttu-id="4f34c-125">Le volume a été entièrement ou partiellement chiffré à l’aide des fonctionnalités matérielles du lecteur.</span><span class="sxs-lookup"><span data-stu-id="4f34c-125">The volume has been fully or partially encrypted by using the hardware capabilities of the drive.</span></span><br/>                                                                                                                                                      |
| <span id="XTS_AES_128"></span><span id="xts_aes_128"></span><dl> <span data-ttu-id="4f34c-126"><dt>**XTS \_ AES \_ 128**</dt> <dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="4f34c-126"><dt>**XTS\_AES\_128**</dt> <dt>6</dt></span></span> </dl>                                | <span data-ttu-id="4f34c-127">Le volume a été entièrement ou partiellement chiffré avec XTS à l’aide de l’Advanced Encryption Standard (AES) et une taille de clé AES de 128 bits.</span><span class="sxs-lookup"><span data-stu-id="4f34c-127">The volume has been fully or partially encrypted with XTS using the Advanced Encryption Standard (AES), and an AES key size of 128 bits.</span></span> <span data-ttu-id="4f34c-128">Cette méthode est disponible uniquement sur les appareils exécutant Windows 10, version 1511 ou ultérieure.</span><span class="sxs-lookup"><span data-stu-id="4f34c-128">This method is only available on devices running Windows 10, version 1511 or higher.</span></span><br/>                          |
| <span id="XTS_AES_256"></span><span id="xts_aes_256"></span><dl> <span data-ttu-id="4f34c-129"><dt>**XTS \_ AES \_ 256**</dt> <dt>7</dt></span><span class="sxs-lookup"><span data-stu-id="4f34c-129"><dt>**XTS\_AES\_256**</dt> <dt>7</dt></span></span> </dl>                                | <span data-ttu-id="4f34c-130">Le volume a été entièrement ou partiellement chiffré avec XTS à l’aide de l’Advanced Encryption Standard (AES) et une taille de clé AES de 256 bits.</span><span class="sxs-lookup"><span data-stu-id="4f34c-130">The volume has been fully or partially encrypted with XTS using the Advanced Encryption Standard (AES), and an AES key size of 256 bits.</span></span> <span data-ttu-id="4f34c-131">Cette méthode est disponible uniquement sur les appareils exécutant Windows 10, version 1511 ou ultérieure.</span><span class="sxs-lookup"><span data-stu-id="4f34c-131">This method is only available on devices running Windows 10, version 1511 or higher.</span></span><br/>                          |
| <dl> <span data-ttu-id="4f34c-132"><dt>(UInt32)-1</dt></span><span class="sxs-lookup"><span data-stu-id="4f34c-132"><dt>(uint32)–1</dt></span></span> </dl>                                                                                                                                                          | <span data-ttu-id="4f34c-133">UNKNOWN</span><span class="sxs-lookup"><span data-stu-id="4f34c-133">UNKNOWN</span></span><br/> <span data-ttu-id="4f34c-134">Le volume a été entièrement ou partiellement chiffré avec un algorithme et une taille de clé inconnus.</span><span class="sxs-lookup"><span data-stu-id="4f34c-134">The volume has been fully or partially encrypted with an unknown algorithm and key size.</span></span><br/>                                                                                                                                            |



 

</dd> <dt>

<span data-ttu-id="4f34c-135">*SelfEncryptionDriveEncryptionMethod* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="4f34c-135">*SelfEncryptionDriveEncryptionMethod* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4f34c-136">Type : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="4f34c-136">Type: **string**</span></span>

<span data-ttu-id="4f34c-137">L’algorithme de chiffrement est configuré sur le lecteur à chiffrement automatique.</span><span class="sxs-lookup"><span data-stu-id="4f34c-137">The encryption algorithm is configured on the self-encrypting drive.</span></span> <span data-ttu-id="4f34c-138">Une chaîne NULL signifie que BitLocker utilise le chiffrement logiciel ou qu’aucune méthode de chiffrement n’est signalée.</span><span class="sxs-lookup"><span data-stu-id="4f34c-138">A null string means that either BitLocker is using software encryption or no encryption method is reported.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4f34c-139">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="4f34c-139">Return value</span></span>

<span data-ttu-id="4f34c-140">Type : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="4f34c-140">Type: **uint32**</span></span>

<span data-ttu-id="4f34c-141">Cette méthode retourne l’un des codes suivants, ou un autre code d’erreur en cas d’échec.</span><span class="sxs-lookup"><span data-stu-id="4f34c-141">This method returns one of the following codes or another error code if it fails.</span></span>



| <span data-ttu-id="4f34c-142">Code/valeur de retour</span><span class="sxs-lookup"><span data-stu-id="4f34c-142">Return code/value</span></span>                                                                                                                                 | <span data-ttu-id="4f34c-143">Description</span><span class="sxs-lookup"><span data-stu-id="4f34c-143">Description</span></span>                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <span data-ttu-id="4f34c-144"><dt>**S \_ OK**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="4f34c-144"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl> | <span data-ttu-id="4f34c-145">La méthode a réussi.</span><span class="sxs-lookup"><span data-stu-id="4f34c-145">The method was successful.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="4f34c-146">Notes</span><span class="sxs-lookup"><span data-stu-id="4f34c-146">Remarks</span></span>

<span data-ttu-id="4f34c-147">Les fichiers format MOF (MOF) contiennent les définitions des classes Windows Management Instrumentation (WMI).</span><span class="sxs-lookup"><span data-stu-id="4f34c-147">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="4f34c-148">Les fichiers MOF ne sont pas installés dans le cadre de la SDK Windows.</span><span class="sxs-lookup"><span data-stu-id="4f34c-148">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="4f34c-149">Ils sont installés sur le serveur lorsque vous ajoutez le rôle associé à l’aide de l’Gestionnaire de serveur.</span><span class="sxs-lookup"><span data-stu-id="4f34c-149">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="4f34c-150">Pour plus d’informations sur les fichiers MOF, consultez [format MOF (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="4f34c-150">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="4f34c-151">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="4f34c-151">Requirements</span></span>



| <span data-ttu-id="4f34c-152">Condition requise</span><span class="sxs-lookup"><span data-stu-id="4f34c-152">Requirement</span></span> | <span data-ttu-id="4f34c-153">Valeur</span><span class="sxs-lookup"><span data-stu-id="4f34c-153">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4f34c-154">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4f34c-154">Minimum supported client</span></span><br/> | <span data-ttu-id="4f34c-155">Windows Vista entreprise, les applications de bureau Windows Vista Édition intégrale \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="4f34c-155">Windows Vista Enterprise, Windows Vista Ultimate \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="4f34c-156">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4f34c-156">Minimum supported server</span></span><br/> | <span data-ttu-id="4f34c-157">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="4f34c-157">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="4f34c-158">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="4f34c-158">Namespace</span></span><br/>                | <span data-ttu-id="4f34c-159">Racine \\ de \\ sécurité cimv2 \\ MicrosoftVolumeEncryption</span><span class="sxs-lookup"><span data-stu-id="4f34c-159">Root\\CIMV2\\Security\\MicrosoftVolumeEncryption</span></span><br/>                                             |
| <span data-ttu-id="4f34c-160">MOF</span><span class="sxs-lookup"><span data-stu-id="4f34c-160">MOF</span></span><br/>                      | <dl> <span data-ttu-id="4f34c-161"><dt>Win32 \_ encryptablevolume. mof</dt></span><span class="sxs-lookup"><span data-stu-id="4f34c-161"><dt>Win32\_encryptablevolume.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4f34c-162">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4f34c-162">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4f34c-163">**\_EncryptableVolume Win32**</span><span class="sxs-lookup"><span data-stu-id="4f34c-163">**Win32\_EncryptableVolume**</span></span>](win32-encryptablevolume.md)
</dt> </dl>

 

 
