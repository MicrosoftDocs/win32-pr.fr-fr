---
description: Active ou reprend tous les protecteurs de clés désactivés ou suspendus.
ms.assetid: 6f5a17a3-84f2-43a0-a85f-1037cd52439a
title: Méthode EnableKeyProtectors de la classe Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.EnableKeyProtectors
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 78f8502ae141458f1ae46a48d21c110b9434acd7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106515627"
---
# <a name="enablekeyprotectors-method-of-the-win32_encryptablevolume-class"></a><span data-ttu-id="7d228-103">Méthode EnableKeyProtectors de la \_ classe Win32 EncryptableVolume</span><span class="sxs-lookup"><span data-stu-id="7d228-103">EnableKeyProtectors method of the Win32\_EncryptableVolume class</span></span>

<span data-ttu-id="7d228-104">La méthode **EnableKeyProtectors** de la classe [**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md) active ou reprend tous les protecteurs de clés désactivés ou suspendus.</span><span class="sxs-lookup"><span data-stu-id="7d228-104">The **EnableKeyProtectors** method of the [**Win32\_EncryptableVolume**](win32-encryptablevolume.md) class enables or resumes all disabled or suspended key protectors.</span></span> <span data-ttu-id="7d228-105">Vous pouvez utiliser cette méthode pour réactiver ou reprendre la protection BitLocker sur un volume chiffré.</span><span class="sxs-lookup"><span data-stu-id="7d228-105">You can use this method to reenable or resume BitLocker protection on an encrypted volume.</span></span> <span data-ttu-id="7d228-106">Cette méthode garantit que la clé de chiffrement du volume n’est pas exposée en clair sur le disque dur.</span><span class="sxs-lookup"><span data-stu-id="7d228-106">This method ensures that the volume's encryption key is not exposed in the clear on the hard disk.</span></span>

> [!Note]  
> <span data-ttu-id="7d228-107">Si le disque prend en charge le chiffrement matériel, l’état de la bande passe à « déverrouillé » de « toujours déverrouillé ».</span><span class="sxs-lookup"><span data-stu-id="7d228-107">If the disc supports hardware encryption, the band state transitions to "unlocked" from "always unlocked".</span></span>

 

## <a name="syntax"></a><span data-ttu-id="7d228-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7d228-108">Syntax</span></span>


```mof
uint32 EnableKeyProtectors();
```



## <a name="parameters"></a><span data-ttu-id="7d228-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="7d228-109">Parameters</span></span>

<span data-ttu-id="7d228-110">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="7d228-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="7d228-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="7d228-111">Return value</span></span>

<span data-ttu-id="7d228-112">Type : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="7d228-112">Type: **uint32**</span></span>

<span data-ttu-id="7d228-113">Cette méthode retourne l’un des codes suivants, ou un autre code d’erreur en cas d’échec.</span><span class="sxs-lookup"><span data-stu-id="7d228-113">This method returns one of the following codes or another error code if it fails.</span></span>

<span data-ttu-id="7d228-114">Si les protecteurs de clé sont déjà activés et qu’aucune autre erreur ne se produit, cette méthode retourne zéro.</span><span class="sxs-lookup"><span data-stu-id="7d228-114">If key protectors are already enabled and no other errors occur, this method returns zero.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="7d228-115">Code/valeur de retour</span><span class="sxs-lookup"><span data-stu-id="7d228-115">Return code/value</span></span></th>
<th><span data-ttu-id="7d228-116">Description</span><span class="sxs-lookup"><span data-stu-id="7d228-116">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><dl> <span data-ttu-id="7d228-117"><dt><strong>S_OK</strong></dt> <dt>0 (0x0)</dt> </span><span class="sxs-lookup"><span data-stu-id="7d228-117"><dt><strong>S_OK</strong></dt> <dt>0 (0x0)</dt> </span></span></dl></td>
<td><span data-ttu-id="7d228-118">La méthode a réussi.</span><span class="sxs-lookup"><span data-stu-id="7d228-118">The method was successful.</span></span><br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="7d228-119"><dt><strong>FVE_E_SECURE_KEY_REQUIRED</strong></dt> <dt>2150694919 (0x80310007)</dt> </span><span class="sxs-lookup"><span data-stu-id="7d228-119"><dt><strong>FVE_E_SECURE_KEY_REQUIRED</strong></dt> <dt>2150694919 (0x80310007)</dt> </span></span></dl></td>
<td><span data-ttu-id="7d228-120">Aucun protecteur de clé n’existe sur le volume.</span><span class="sxs-lookup"><span data-stu-id="7d228-120">No key protectors exist on the volume.</span></span> <span data-ttu-id="7d228-121">Utilisez l’une des méthodes suivantes pour spécifier les protecteurs de clé pour le volume :</span><span class="sxs-lookup"><span data-stu-id="7d228-121">Use one of the following methods to specify key protectors for the volume:</span></span><br/>
<ul>
<li><span data-ttu-id="7d228-122"><a href="protectkeywithcertificatefile-win32-encryptablevolume.md"><strong>ProtectKeyWithCertificateFile</strong></a></span><span class="sxs-lookup"><span data-stu-id="7d228-122"><a href="protectkeywithcertificatefile-win32-encryptablevolume.md"><strong>ProtectKeyWithCertificateFile</strong></a></span></span></li>
<li><span data-ttu-id="7d228-123"><a href="protectkeywithcertificatethumbprint-win32-encryptablevolume.md"><strong>ProtectKeyWithCertificateThumbprint</strong></a></span><span class="sxs-lookup"><span data-stu-id="7d228-123"><a href="protectkeywithcertificatethumbprint-win32-encryptablevolume.md"><strong>ProtectKeyWithCertificateThumbprint</strong></a></span></span></li>
<li><span data-ttu-id="7d228-124"><a href="protectkeywithexternalkey-win32-encryptablevolume.md"><strong>ProtectKeyWithExternalKey</strong></a></span><span class="sxs-lookup"><span data-stu-id="7d228-124"><a href="protectkeywithexternalkey-win32-encryptablevolume.md"><strong>ProtectKeyWithExternalKey</strong></a></span></span></li>
<li><span data-ttu-id="7d228-125"><a href="protectkeywithnumericalpassword-win32-encryptablevolume.md"><strong>ProtectKeyWithNumericalPassword</strong></a></span><span class="sxs-lookup"><span data-stu-id="7d228-125"><a href="protectkeywithnumericalpassword-win32-encryptablevolume.md"><strong>ProtectKeyWithNumericalPassword</strong></a></span></span></li>
<li><span data-ttu-id="7d228-126"><a href="protectkeywithpassphrase-win32-encryptablevolume.md"><strong>ProtectKeyWithPassphrase</strong></a></span><span class="sxs-lookup"><span data-stu-id="7d228-126"><a href="protectkeywithpassphrase-win32-encryptablevolume.md"><strong>ProtectKeyWithPassphrase</strong></a></span></span></li>
<li><span data-ttu-id="7d228-127"><a href="protectkeywithtpm-win32-encryptablevolume.md"><strong>ProtectKeyWithTPM</strong></a></span><span class="sxs-lookup"><span data-stu-id="7d228-127"><a href="protectkeywithtpm-win32-encryptablevolume.md"><strong>ProtectKeyWithTPM</strong></a></span></span></li>
<li><span data-ttu-id="7d228-128"><a href="protectkeywithtpmandpin-win32-encryptablevolume.md"><strong>ProtectKeyWithTPMAndPIN</strong></a></span><span class="sxs-lookup"><span data-stu-id="7d228-128"><a href="protectkeywithtpmandpin-win32-encryptablevolume.md"><strong>ProtectKeyWithTPMAndPIN</strong></a></span></span></li>
<li><span data-ttu-id="7d228-129"><a href="protectkeywithtpmandpinandstartupkey-win32-encryptablevolume.md"><strong>ProtectKeyWithTPMAndPINAndStartupKey</strong></a></span><span class="sxs-lookup"><span data-stu-id="7d228-129"><a href="protectkeywithtpmandpinandstartupkey-win32-encryptablevolume.md"><strong>ProtectKeyWithTPMAndPINAndStartupKey</strong></a></span></span></li>
<li><span data-ttu-id="7d228-130"><a href="protectkeywithtpmandstartupkey-win32-encryptablevolume.md"><strong>ProtectKeyWithTPMAndStartupKey</strong></a></span><span class="sxs-lookup"><span data-stu-id="7d228-130"><a href="protectkeywithtpmandstartupkey-win32-encryptablevolume.md"><strong>ProtectKeyWithTPMAndStartupKey</strong></a></span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><dl> <span data-ttu-id="7d228-131"><dt><strong>FVE_E_NOT_ACTIVATED</strong></dt> <dt>2150694920 (0x80310008)</dt> </span><span class="sxs-lookup"><span data-stu-id="7d228-131"><dt><strong>FVE_E_NOT_ACTIVATED</strong></dt> <dt>2150694920 (0x80310008)</dt> </span></span></dl></td>
<td><span data-ttu-id="7d228-132">BitLocker n’est pas activé sur le volume.</span><span class="sxs-lookup"><span data-stu-id="7d228-132">BitLocker is not enabled on the volume.</span></span> <span data-ttu-id="7d228-133">Ajoutez un protecteur de clé pour activer BitLocker.</span><span class="sxs-lookup"><span data-stu-id="7d228-133">Add a key protector to enable BitLocker.</span></span> <br/></td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a><span data-ttu-id="7d228-134">Notes</span><span class="sxs-lookup"><span data-stu-id="7d228-134">Remarks</span></span>

<span data-ttu-id="7d228-135">Si le volume est entièrement chiffré, l’exécution de cette méthode permet de s’assurer que le volume est protégé.</span><span class="sxs-lookup"><span data-stu-id="7d228-135">If the volume is fully encrypted, successfully running this method ensures that the volume is protected.</span></span> <span data-ttu-id="7d228-136">Si le volume est partiellement chiffré, l’exécution de cette méthode implique que le volume sera protégé lorsqu’il deviendra entièrement chiffré.</span><span class="sxs-lookup"><span data-stu-id="7d228-136">If the volume is partially encrypted, successfully running this method implies that the volume will be protected when it becomes fully encrypted.</span></span> <span data-ttu-id="7d228-137">Pour plus d’informations, consultez la méthode [**GetProtectionStatus**](getprotectionstatus-win32-encryptablevolume.md) .</span><span class="sxs-lookup"><span data-stu-id="7d228-137">For more information, see the [**GetProtectionStatus**](getprotectionstatus-win32-encryptablevolume.md) method.</span></span>

<span data-ttu-id="7d228-138">Si des protecteurs de clés basés sur le module de plateforme sécurisée existent pour le volume, l’exécution correcte de cette méthode actualise également ces protecteurs afin que le module de plateforme sécurisée valide les services de démarrage actuels sur la plateforme.</span><span class="sxs-lookup"><span data-stu-id="7d228-138">If TPM-based key protectors exist for the volume, successfully running this method also refreshes these protectors so that the TPM validates against the current startup services on the platform.</span></span> <span data-ttu-id="7d228-139">En d’autres termes, vous déclarez que l’état actuel de l’ordinateur est l’état correct que le module de plateforme sécurisée doit vérifier par rapport aux redémarrages futurs de l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="7d228-139">In other words, you are asserting that the current computer state is the correct state that the TPM will check against on future computer restarts.</span></span>

<span data-ttu-id="7d228-140">Les fichiers format MOF (MOF) contiennent les définitions des classes Windows Management Instrumentation (WMI).</span><span class="sxs-lookup"><span data-stu-id="7d228-140">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="7d228-141">Les fichiers MOF ne sont pas installés dans le cadre de la SDK Windows.</span><span class="sxs-lookup"><span data-stu-id="7d228-141">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="7d228-142">Ils sont installés sur le serveur lorsque vous ajoutez le rôle associé à l’aide de l’Gestionnaire de serveur.</span><span class="sxs-lookup"><span data-stu-id="7d228-142">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="7d228-143">Pour plus d’informations sur les fichiers MOF, consultez [format MOF (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="7d228-143">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="7d228-144">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7d228-144">Requirements</span></span>



| <span data-ttu-id="7d228-145">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7d228-145">Requirement</span></span> | <span data-ttu-id="7d228-146">Valeur</span><span class="sxs-lookup"><span data-stu-id="7d228-146">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7d228-147">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7d228-147">Minimum supported client</span></span><br/> | <span data-ttu-id="7d228-148">Windows Vista entreprise, les applications de bureau Windows Vista Édition intégrale \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="7d228-148">Windows Vista Enterprise, Windows Vista Ultimate \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="7d228-149">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7d228-149">Minimum supported server</span></span><br/> | <span data-ttu-id="7d228-150">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="7d228-150">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="7d228-151">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="7d228-151">Namespace</span></span><br/>                | <span data-ttu-id="7d228-152">Racine \\ de \\ sécurité cimv2 \\ MicrosoftVolumeEncryption</span><span class="sxs-lookup"><span data-stu-id="7d228-152">Root\\CIMV2\\Security\\MicrosoftVolumeEncryption</span></span><br/>                                             |
| <span data-ttu-id="7d228-153">MOF</span><span class="sxs-lookup"><span data-stu-id="7d228-153">MOF</span></span><br/>                      | <dl> <span data-ttu-id="7d228-154"><dt>Win32 \_ encryptablevolume. mof</dt></span><span class="sxs-lookup"><span data-stu-id="7d228-154"><dt>Win32\_encryptablevolume.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7d228-155">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7d228-155">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7d228-156">**\_EncryptableVolume Win32**</span><span class="sxs-lookup"><span data-stu-id="7d228-156">**Win32\_EncryptableVolume**</span></span>](win32-encryptablevolume.md)
</dt> <dt>

[<span data-ttu-id="7d228-157">**DisableKeyProtectors**</span><span class="sxs-lookup"><span data-stu-id="7d228-157">**DisableKeyProtectors**</span></span>](disablekeyprotectors-win32-encryptablevolume.md)
</dt> <dt>

[<span data-ttu-id="7d228-158">**ProtectKeyWithCertificateFile**</span><span class="sxs-lookup"><span data-stu-id="7d228-158">**ProtectKeyWithCertificateFile**</span></span>](protectkeywithcertificatefile-win32-encryptablevolume.md)
</dt> <dt>

[<span data-ttu-id="7d228-159">**ProtectKeyWithCertificateThumbprint**</span><span class="sxs-lookup"><span data-stu-id="7d228-159">**ProtectKeyWithCertificateThumbprint**</span></span>](protectkeywithcertificatethumbprint-win32-encryptablevolume.md)
</dt> <dt>

[<span data-ttu-id="7d228-160">**ProtectKeyWithExternalKey**</span><span class="sxs-lookup"><span data-stu-id="7d228-160">**ProtectKeyWithExternalKey**</span></span>](protectkeywithexternalkey-win32-encryptablevolume.md)
</dt> <dt>

[<span data-ttu-id="7d228-161">**ProtectKeyWithNumericalPassword**</span><span class="sxs-lookup"><span data-stu-id="7d228-161">**ProtectKeyWithNumericalPassword**</span></span>](protectkeywithnumericalpassword-win32-encryptablevolume.md)
</dt> <dt>

[<span data-ttu-id="7d228-162">**ProtectKeyWithPassphrase**</span><span class="sxs-lookup"><span data-stu-id="7d228-162">**ProtectKeyWithPassphrase**</span></span>](protectkeywithpassphrase-win32-encryptablevolume.md)
</dt> <dt>

[<span data-ttu-id="7d228-163">**ProtectKeyWithTPM**</span><span class="sxs-lookup"><span data-stu-id="7d228-163">**ProtectKeyWithTPM**</span></span>](protectkeywithtpm-win32-encryptablevolume.md)
</dt> <dt>

[<span data-ttu-id="7d228-164">**ProtectKeyWithTPMAndPIN**</span><span class="sxs-lookup"><span data-stu-id="7d228-164">**ProtectKeyWithTPMAndPIN**</span></span>](protectkeywithtpmandpin-win32-encryptablevolume.md)
</dt> <dt>

[<span data-ttu-id="7d228-165">**ProtectKeyWithTPMAndPINAndStartupKey**</span><span class="sxs-lookup"><span data-stu-id="7d228-165">**ProtectKeyWithTPMAndPINAndStartupKey**</span></span>](protectkeywithtpmandpinandstartupkey-win32-encryptablevolume.md)
</dt> <dt>

[<span data-ttu-id="7d228-166">**ProtectKeyWithTPMAndStartupKey**</span><span class="sxs-lookup"><span data-stu-id="7d228-166">**ProtectKeyWithTPMAndStartupKey**</span></span>](protectkeywithtpmandstartupkey-win32-encryptablevolume.md)
</dt> </dl>

 

 
