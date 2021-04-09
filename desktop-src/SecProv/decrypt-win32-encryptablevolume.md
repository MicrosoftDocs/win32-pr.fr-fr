---
description: Commence le déchiffrement d’un volume entièrement chiffré ou reprend le déchiffrement d’un volume partiellement chiffré.
ms.assetid: 3cdbb1c1-1084-4ddb-ba8d-fc2e3ec75224
title: Méthode Decrypt de la classe Win32_EncryptableVolume (InfoCard. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.Decrypt
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 96f7ab1c237879d83be25ddb54425ac31fcb855d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103865437"
---
# <a name="decrypt-method-of-the-win32_encryptablevolume-class"></a><span data-ttu-id="d6f5c-103">Méthode Decrypt de la \_ classe EncryptableVolume Win32</span><span class="sxs-lookup"><span data-stu-id="d6f5c-103">Decrypt method of the Win32\_EncryptableVolume class</span></span>

<span data-ttu-id="d6f5c-104">La méthode **Decrypt** de la classe [**\_ EncryptableVolume Win32**](win32-encryptablevolume.md) commence le déchiffrement d’un volume entièrement chiffré, ou reprend le déchiffrement d’un volume partiellement chiffré.</span><span class="sxs-lookup"><span data-stu-id="d6f5c-104">The **Decrypt** method of the [**Win32\_EncryptableVolume**](win32-encryptablevolume.md) class begins decryption of a fully encrypted volume, or resumes decryption of a partially encrypted volume.</span></span>

<span data-ttu-id="d6f5c-105">Quand le déchiffrement est suspendu ou en cours, cette méthode se comporte comme [**ResumeConversion**](resumeconversion-win32-encryptablevolume.md).</span><span class="sxs-lookup"><span data-stu-id="d6f5c-105">When decryption is paused or in-progress, this method behaves the same as [**ResumeConversion**](resumeconversion-win32-encryptablevolume.md).</span></span> <span data-ttu-id="d6f5c-106">Lorsque le chiffrement est suspendu ou en cours, cette méthode annule le chiffrement et commence le déchiffrement.</span><span class="sxs-lookup"><span data-stu-id="d6f5c-106">When encryption is paused or in-progress, this method reverts the encryption and begins decryption.</span></span> <span data-ttu-id="d6f5c-107">Une fois le déchiffrement terminé, tous les protecteurs de clé sur ce volume sont supprimés du système et le volume est converti en système de fichiers NTFS standard.</span><span class="sxs-lookup"><span data-stu-id="d6f5c-107">After decryption completes, all key protectors on this volume are removed from the system and the volume converts to a standard NTFS file system.</span></span>

> [!Note]  
> <span data-ttu-id="d6f5c-108">Si le disque est chiffré sur le matériel, la méthode de **déchiffrement** définit l’état de la bande sur « toujours déverrouillé », supprime toutes les métadonnées associées et met à zéro l’ID de sécurité du lecteur.</span><span class="sxs-lookup"><span data-stu-id="d6f5c-108">If the disc is hardware encrypted, the **Decrypt** method sets band status to "always unlocked", removes all associated metadata, and zeroes the security ID for the drive.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="d6f5c-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d6f5c-109">Syntax</span></span>


```mof
uint32 Decrypt();
```



## <a name="parameters"></a><span data-ttu-id="d6f5c-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d6f5c-110">Parameters</span></span>

<span data-ttu-id="d6f5c-111">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="d6f5c-111">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="d6f5c-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="d6f5c-112">Return value</span></span>

<span data-ttu-id="d6f5c-113">Type : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="d6f5c-113">Type: **uint32**</span></span>

<span data-ttu-id="d6f5c-114">Cette méthode retourne l’un des codes suivants, ou un autre code d’erreur en cas d’échec.</span><span class="sxs-lookup"><span data-stu-id="d6f5c-114">This method returns one of the following codes or another error code if it fails.</span></span>

<span data-ttu-id="d6f5c-115">Cette méthode est retournée immédiatement.</span><span class="sxs-lookup"><span data-stu-id="d6f5c-115">This method returns immediately.</span></span> <span data-ttu-id="d6f5c-116">Si le volume est déjà entièrement déchiffré et qu’aucune autre erreur n’existe, cette méthode retourne 0.</span><span class="sxs-lookup"><span data-stu-id="d6f5c-116">If the volume is already fully decrypted and no other errors exist, this method returns 0.</span></span>



| <span data-ttu-id="d6f5c-117">Code/valeur de retour</span><span class="sxs-lookup"><span data-stu-id="d6f5c-117">Return code/value</span></span>                                                                                                                                                                       | <span data-ttu-id="d6f5c-118">Description</span><span class="sxs-lookup"><span data-stu-id="d6f5c-118">Description</span></span>                                                                                                                                                                                                                             |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="d6f5c-119"><dt>**S \_ OK**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="d6f5c-119"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl>                                       | <span data-ttu-id="d6f5c-120">La méthode a réussi.</span><span class="sxs-lookup"><span data-stu-id="d6f5c-120">The method was successful.</span></span><br/>                                                                                                                                                                                                   |
| <dl> <span data-ttu-id="d6f5c-121"><dt>**FVE \_ E \_ Locked \_ volume**</dt> <dt>2150694912 (0x80310000)</dt></span><span class="sxs-lookup"><span data-stu-id="d6f5c-121"><dt>**FVE\_E\_LOCKED\_VOLUME**</dt> <dt>2150694912 (0x80310000)</dt></span></span> </dl>      | <span data-ttu-id="d6f5c-122">Le volume est verrouillé.</span><span class="sxs-lookup"><span data-stu-id="d6f5c-122">The volume is locked.</span></span><br/>                                                                                                                                                                                                        |
| <dl> <span data-ttu-id="d6f5c-123"><dt>**FVE \_ \_Désactivation du \_ déverrouillage d’E**</dt> /t <dt>2150694953 (0x80310029)</dt></span><span class="sxs-lookup"><span data-stu-id="d6f5c-123"><dt>**FVE\_E\_AUTOUNLOCK\_ENABLED**</dt> <dt>2150694953 (0x80310029)</dt></span></span> </dl> | <span data-ttu-id="d6f5c-124">Impossible de déchiffrer ce volume, car les clés utilisées pour déverrouiller automatiquement les volumes de données sont disponibles.</span><span class="sxs-lookup"><span data-stu-id="d6f5c-124">This volume cannot be decrypted because keys used to automatically unlock data volumes are available.</span></span> <br/> <span data-ttu-id="d6f5c-125">Utilisez [**ClearAllAutoUnlockKeys**](clearallautounlockkeys-win32-encryptablevolume.md) pour supprimer ces clés.</span><span class="sxs-lookup"><span data-stu-id="d6f5c-125">Use [**ClearAllAutoUnlockKeys**](clearallautounlockkeys-win32-encryptablevolume.md) to remove these keys.</span></span><br/> |



 

## <a name="security-considerations"></a><span data-ttu-id="d6f5c-126">Considérations relatives à la sécurité</span><span class="sxs-lookup"><span data-stu-id="d6f5c-126">Security Considerations</span></span>

<span data-ttu-id="d6f5c-127">L’appel de la méthode de **déchiffrement** laisse les données non protégées.</span><span class="sxs-lookup"><span data-stu-id="d6f5c-127">Calling the **Decrypt** method leaves data unprotected.</span></span>

<span data-ttu-id="d6f5c-128">Si l’état de protection du volume est égal à 1 (PROTECTION activée) avant l’utilisation de cette méthode, l’exécution correcte de cette méthode modifie l’état de la protection en 0 (PROTECTION désactivée), car par définition un volume partiellement chiffré n’est pas protégé.</span><span class="sxs-lookup"><span data-stu-id="d6f5c-128">If the protection status of the volume is 1 (PROTECTION ON) before this method is used, successful completion of this method changes the protection status to 0 (PROTECTION OFF), since by definition a partially encrypted volume is not protected.</span></span>

## <a name="remarks"></a><span data-ttu-id="d6f5c-129">Notes</span><span class="sxs-lookup"><span data-stu-id="d6f5c-129">Remarks</span></span>

<span data-ttu-id="d6f5c-130">Si le volume n’est pas déjà entièrement déchiffré, l’exécution de **Decrypte** fait en sorte que [**GetConversionStatus**](getconversionstatus-win32-encryptablevolume.md) indique que le déchiffrement est en cours et affiche le pourcentage du volume qui reste chiffré.</span><span class="sxs-lookup"><span data-stu-id="d6f5c-130">If the volume is not already fully decrypted, running **Decrypt** causes [**GetConversionStatus**](getconversionstatus-win32-encryptablevolume.md) to indicate that decryption is progress and shows the percentage of the volume that remains encrypted.</span></span>

<span data-ttu-id="d6f5c-131">Si l’état de protection du volume est « activé » avant l’exécution de cette méthode, l’exécution de cette méthode remplace l’état de protection par « désactivé », car par définition, un volume partiellement chiffré n’est pas protégé.</span><span class="sxs-lookup"><span data-stu-id="d6f5c-131">If the protection status of the volume is "on" before this method is run, running this method changes the protection status to "off", since by definition a partially encrypted volume is not protected.</span></span>

<span data-ttu-id="d6f5c-132">Si cette méthode est exécutée sur le volume du système d’exploitation en cours d’exécution et que ce volume du système d’exploitation est utilisé pour déverrouiller automatiquement les volumes de données (consultez la méthode [**EnableAutoUnlock**](enableautounlock-win32-encryptablevolume.md)), vous devez d’abord appeler la méthode [**ClearAllAutoUnlockKeys**](clearallautounlockkeys-win32-encryptablevolume.md).</span><span class="sxs-lookup"><span data-stu-id="d6f5c-132">If this method is run on the currently running operating system volume and this operating system volume is being used to automatically unlock data volumes (see method [**EnableAutoUnlock**](enableautounlock-win32-encryptablevolume.md)) you must first call the method [**ClearAllAutoUnlockKeys**](clearallautounlockkeys-win32-encryptablevolume.md).</span></span>

<span data-ttu-id="d6f5c-133">Les fichiers format MOF (MOF) contiennent les définitions des classes Windows Management Instrumentation (WMI).</span><span class="sxs-lookup"><span data-stu-id="d6f5c-133">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="d6f5c-134">Les fichiers MOF ne sont pas installés dans le cadre de la SDK Windows.</span><span class="sxs-lookup"><span data-stu-id="d6f5c-134">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="d6f5c-135">Ils sont installés sur le serveur lorsque vous ajoutez le rôle associé à l’aide de l’Gestionnaire de serveur.</span><span class="sxs-lookup"><span data-stu-id="d6f5c-135">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="d6f5c-136">Pour plus d’informations sur les fichiers MOF, consultez [format MOF (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="d6f5c-136">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="d6f5c-137">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d6f5c-137">Requirements</span></span>



| <span data-ttu-id="d6f5c-138">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d6f5c-138">Requirement</span></span> | <span data-ttu-id="d6f5c-139">Valeur</span><span class="sxs-lookup"><span data-stu-id="d6f5c-139">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d6f5c-140">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d6f5c-140">Minimum supported client</span></span><br/> | <span data-ttu-id="d6f5c-141">Windows Vista entreprise, les applications de bureau Windows Vista Édition intégrale \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d6f5c-141">Windows Vista Enterprise, Windows Vista Ultimate \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="d6f5c-142">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d6f5c-142">Minimum supported server</span></span><br/> | <span data-ttu-id="d6f5c-143">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d6f5c-143">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="d6f5c-144">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="d6f5c-144">Namespace</span></span><br/>                | <span data-ttu-id="d6f5c-145">Racine \\ de \\ sécurité cimv2 \\ MicrosoftVolumeEncryption</span><span class="sxs-lookup"><span data-stu-id="d6f5c-145">Root\\CIMV2\\Security\\MicrosoftVolumeEncryption</span></span><br/>                                             |
| <span data-ttu-id="d6f5c-146">En-tête</span><span class="sxs-lookup"><span data-stu-id="d6f5c-146">Header</span></span><br/>                   | <dl> <span data-ttu-id="d6f5c-147"><dt>InfoCard. h</dt></span><span class="sxs-lookup"><span data-stu-id="d6f5c-147"><dt>Infocard.h</dt></span></span> </dl>                   |
| <span data-ttu-id="d6f5c-148">MOF</span><span class="sxs-lookup"><span data-stu-id="d6f5c-148">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d6f5c-149"><dt>Win32 \_ encryptablevolume. mof</dt></span><span class="sxs-lookup"><span data-stu-id="d6f5c-149"><dt>Win32\_encryptablevolume.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d6f5c-150">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d6f5c-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d6f5c-151">**\_EncryptableVolume Win32**</span><span class="sxs-lookup"><span data-stu-id="d6f5c-151">**Win32\_EncryptableVolume**</span></span>](win32-encryptablevolume.md)
</dt> </dl>

 

 
