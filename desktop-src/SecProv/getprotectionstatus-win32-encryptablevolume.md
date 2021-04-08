---
description: Indique si le volume et sa clé de chiffrement sont sécurisés.
ms.assetid: bcd8fce5-da39-4aa8-93ff-0768deb900ec
title: Méthode GetProtectionStatus de la classe Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.GetProtectionStatus
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 5f3fa2aaa019097a01a6e6d1628d7c4fe9b82710
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103750844"
---
# <a name="getprotectionstatus-method-of-the-win32_encryptablevolume-class"></a><span data-ttu-id="5bb8c-103">Méthode GetProtectionStatus de la \_ classe Win32 EncryptableVolume</span><span class="sxs-lookup"><span data-stu-id="5bb8c-103">GetProtectionStatus method of the Win32\_EncryptableVolume class</span></span>

<span data-ttu-id="5bb8c-104">La méthode **GetProtectionStatus** de la [**classe \_ EncryptableVolume Win32**](win32-encryptablevolume.md) indique si le volume et sa clé de chiffrement (le cas échéant) sont sécurisés.</span><span class="sxs-lookup"><span data-stu-id="5bb8c-104">The **GetProtectionStatus** method of the [**Win32\_EncryptableVolume**](win32-encryptablevolume.md) class indicates whether the volume and its encryption key (if any) are secured.</span></span>

<span data-ttu-id="5bb8c-105">La protection est désactivée si un volume n’est pas chiffré ou partiellement chiffré, ou si la clé de chiffrement du volume est disponible en clair sur le disque dur.</span><span class="sxs-lookup"><span data-stu-id="5bb8c-105">Protection is off if a volume is unencrypted or partially encrypted, or if the volume's encryption key is available in the clear on the hard disk.</span></span>

## <a name="syntax"></a><span data-ttu-id="5bb8c-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="5bb8c-106">Syntax</span></span>


```mof
uint32 GetProtectionStatus(
  [out] uint32 ProtectionStatus
);
```



## <a name="parameters"></a><span data-ttu-id="5bb8c-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="5bb8c-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5bb8c-108">*ProtectionStatus* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="5bb8c-108">*ProtectionStatus* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5bb8c-109">Type : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="5bb8c-109">Type: **uint32**</span></span>

<span data-ttu-id="5bb8c-110">Spécifie si le volume et la clé de chiffrement (le cas échéant) sont sécurisés.</span><span class="sxs-lookup"><span data-stu-id="5bb8c-110">Specifies whether the volume and the encryption key (if any) are secured.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="5bb8c-111">Valeur</span><span class="sxs-lookup"><span data-stu-id="5bb8c-111">Value</span></span></th>
<th><span data-ttu-id="5bb8c-112">Signification</span><span class="sxs-lookup"><span data-stu-id="5bb8c-112">Meaning</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span id="Unprotected"></span><span id="unprotected"></span><span id="UNPROTECTED"></span><dl> <span data-ttu-id="5bb8c-113"><dt><strong>Non protégé</strong></dt> <dt>0</dt> </span><span class="sxs-lookup"><span data-stu-id="5bb8c-113"><dt><strong>Unprotected</strong></dt> <dt>0</dt> </span></span></dl></td>
<td><span data-ttu-id="5bb8c-114">PROTECTION DÉSACTIVÉE</span><span class="sxs-lookup"><span data-stu-id="5bb8c-114">PROTECTION OFF</span></span><br/> <span data-ttu-id="5bb8c-115">Pour un disque dur standard :</span><span class="sxs-lookup"><span data-stu-id="5bb8c-115">For a standard HDD:</span></span><br/> <span data-ttu-id="5bb8c-116">Le volume n’est pas chiffré, partiellement chiffré ou la clé de chiffrement du volume est disponible en clair sur le disque dur.</span><span class="sxs-lookup"><span data-stu-id="5bb8c-116">The volume is unencrypted, partially encrypted, or the volume's encryption key is available in the clear on the hard disk.</span></span> <span data-ttu-id="5bb8c-117">La clé de chiffrement est disponible en clair sur le disque dur si les protecteurs de clé ont été désactivés à l’aide de la méthode <a href="disablekeyprotectors-win32-encryptablevolume.md"><strong>DisableKeyProtectors</strong></a> ou si aucun protecteur de clé n’a été spécifié à l’aide des méthodes suivantes :</span><span class="sxs-lookup"><span data-stu-id="5bb8c-117">The encryption key is available in the clear on the hard disk if key protectors have been disabled by using the <a href="disablekeyprotectors-win32-encryptablevolume.md"><strong>DisableKeyProtectors</strong></a> method or if no key protectors have been specified by using the following methods:</span></span>
<ul>
<li><span data-ttu-id="5bb8c-118"><a href="protectkeywithcertificatefile-win32-encryptablevolume.md"><strong>ProtectKeyWithCertificateFile</strong></a></span><span class="sxs-lookup"><span data-stu-id="5bb8c-118"><a href="protectkeywithcertificatefile-win32-encryptablevolume.md"><strong>ProtectKeyWithCertificateFile</strong></a></span></span></li>
<li><span data-ttu-id="5bb8c-119"><a href="protectkeywithcertificatethumbprint-win32-encryptablevolume.md"><strong>ProtectKeyWithCertificateThumbprint</strong></a></span><span class="sxs-lookup"><span data-stu-id="5bb8c-119"><a href="protectkeywithcertificatethumbprint-win32-encryptablevolume.md"><strong>ProtectKeyWithCertificateThumbprint</strong></a></span></span></li>
<li><span data-ttu-id="5bb8c-120"><a href="protectkeywithexternalkey-win32-encryptablevolume.md"><strong>ProtectKeyWithExternalKey</strong></a></span><span class="sxs-lookup"><span data-stu-id="5bb8c-120"><a href="protectkeywithexternalkey-win32-encryptablevolume.md"><strong>ProtectKeyWithExternalKey</strong></a></span></span></li>
<li><span data-ttu-id="5bb8c-121"><a href="protectkeywithnumericalpassword-win32-encryptablevolume.md"><strong>ProtectKeyWithNumericalPassword</strong></a></span><span class="sxs-lookup"><span data-stu-id="5bb8c-121"><a href="protectkeywithnumericalpassword-win32-encryptablevolume.md"><strong>ProtectKeyWithNumericalPassword</strong></a></span></span></li>
<li><span data-ttu-id="5bb8c-122"><a href="protectkeywithpassphrase-win32-encryptablevolume.md"><strong>ProtectKeyWithPassphrase</strong></a></span><span class="sxs-lookup"><span data-stu-id="5bb8c-122"><a href="protectkeywithpassphrase-win32-encryptablevolume.md"><strong>ProtectKeyWithPassphrase</strong></a></span></span></li>
<li><span data-ttu-id="5bb8c-123"><a href="protectkeywithtpm-win32-encryptablevolume.md"><strong>ProtectKeyWithTPM</strong></a></span><span class="sxs-lookup"><span data-stu-id="5bb8c-123"><a href="protectkeywithtpm-win32-encryptablevolume.md"><strong>ProtectKeyWithTPM</strong></a></span></span></li>
<li><span data-ttu-id="5bb8c-124"><a href="protectkeywithtpmandpin-win32-encryptablevolume.md"><strong>ProtectKeyWithTPMAndPIN</strong></a></span><span class="sxs-lookup"><span data-stu-id="5bb8c-124"><a href="protectkeywithtpmandpin-win32-encryptablevolume.md"><strong>ProtectKeyWithTPMAndPIN</strong></a></span></span></li>
<li><span data-ttu-id="5bb8c-125"><a href="protectkeywithtpmandpinandstartupkey-win32-encryptablevolume.md"><strong>ProtectKeyWithTPMAndPINAndStartupKey</strong></a></span><span class="sxs-lookup"><span data-stu-id="5bb8c-125"><a href="protectkeywithtpmandpinandstartupkey-win32-encryptablevolume.md"><strong>ProtectKeyWithTPMAndPINAndStartupKey</strong></a></span></span></li>
<li><span data-ttu-id="5bb8c-126"><a href="protectkeywithtpmandstartupkey-win32-encryptablevolume.md"><strong>ProtectKeyWithTPMAndStartupKey</strong></a></span><span class="sxs-lookup"><span data-stu-id="5bb8c-126"><a href="protectkeywithtpmandstartupkey-win32-encryptablevolume.md"><strong>ProtectKeyWithTPMAndStartupKey</strong></a></span></span></li>
</ul>
<br/> <span data-ttu-id="5bb8c-127">Pour un EHDD :</span><span class="sxs-lookup"><span data-stu-id="5bb8c-127">For an EHDD:</span></span><br/> <span data-ttu-id="5bb8c-128">La bande du volume est déverrouillée de façon permanente, n’a pas de gestionnaire de clés ou est gérée par un gestionnaire de clés tiers.</span><span class="sxs-lookup"><span data-stu-id="5bb8c-128">The band for the volume is perpetually unlocked, has no key manager, or is managed by a third party key manager.</span></span><br/> <span data-ttu-id="5bb8c-129">Cela peut également signifier que la bande est gérée par BitLocker mais que la méthode <a href="disablekeyprotectors-win32-encryptablevolume.md"><strong>DisableKeyProtectors</strong></a> a été appelée et que le lecteur est suspendu.</span><span class="sxs-lookup"><span data-stu-id="5bb8c-129">This can also mean that the band is managed by BitLocker but the <a href="disablekeyprotectors-win32-encryptablevolume.md"><strong>DisableKeyProtectors</strong></a> method has been called and the drive is suspended.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="Protected"></span><span id="protected"></span><span id="PROTECTED"></span><dl> <span data-ttu-id="5bb8c-130"><dt><strong>Protégé</strong></dt> <dt>1</dt> </span><span class="sxs-lookup"><span data-stu-id="5bb8c-130"><dt><strong>Protected</strong></dt> <dt>1</dt> </span></span></dl></td>
<td><span data-ttu-id="5bb8c-131">PROTECTION ACTIVÉE</span><span class="sxs-lookup"><span data-stu-id="5bb8c-131">PROTECTION ON</span></span><br/> <span data-ttu-id="5bb8c-132">Pour un disque dur standard :</span><span class="sxs-lookup"><span data-stu-id="5bb8c-132">For a standard HDD:</span></span><br/> <span data-ttu-id="5bb8c-133">Le volume est entièrement chiffré et la clé de chiffrement du volume n’est pas disponible en clair sur le disque dur.</span><span class="sxs-lookup"><span data-stu-id="5bb8c-133">The volume is fully encrypted and the encryption key for the volume is not available in the clear on the hard disk.</span></span><br/> <span data-ttu-id="5bb8c-134">Pour un EHDD :</span><span class="sxs-lookup"><span data-stu-id="5bb8c-134">For an EHDD:</span></span><br/> <span data-ttu-id="5bb8c-135">BitLocker est le gestionnaire de clés de la bande.</span><span class="sxs-lookup"><span data-stu-id="5bb8c-135">BitLocker is the key manager for the band.</span></span> <span data-ttu-id="5bb8c-136">Le lecteur peut être verrouillé ou déverrouillé, mais ne peut pas être déverrouillé de façon permanente.</span><span class="sxs-lookup"><span data-stu-id="5bb8c-136">The drive can be locked or unlocked but cannot be perpetually unlocked.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span><dl> <span data-ttu-id="5bb8c-137"><dt><strong>Inconnu</strong></dt> <dt>2</dt> </span><span class="sxs-lookup"><span data-stu-id="5bb8c-137"><dt><strong>Unknown</strong></dt> <dt>2</dt> </span></span></dl></td>
<td><span data-ttu-id="5bb8c-138">Impossible de déterminer l’état de la protection du volume.</span><span class="sxs-lookup"><span data-stu-id="5bb8c-138">The volume protection status cannot be determined.</span></span> <span data-ttu-id="5bb8c-139">Cela peut être dû au fait que le volume est dans un état verrouillé.</span><span class="sxs-lookup"><span data-stu-id="5bb8c-139">This can be caused by the volume being in a locked state.</span></span><br/> <span data-ttu-id="5bb8c-140"><strong>Windows Vista Édition intégrale, Windows Vista entreprise et Windows Server 2008 :</strong> Cette valeur n’est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="5bb8c-140"><strong>Windows Vista Ultimate, Windows Vista Enterprise and Windows Server 2008:</strong> This value is not supported.</span></span> <span data-ttu-id="5bb8c-141">Cette valeur est prise en charge à compter de Windows 7 et de Windows Server 2008 R2.</span><span class="sxs-lookup"><span data-stu-id="5bb8c-141">This value is supported beginning with Windows 7 and Windows Server 2008 R2.</span></span><br/></td>
</tr>
</tbody>
</table>



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5bb8c-142">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="5bb8c-142">Return value</span></span>

<span data-ttu-id="5bb8c-143">Type : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="5bb8c-143">Type: **uint32**</span></span>

<span data-ttu-id="5bb8c-144">Cette méthode retourne l’un des codes suivants, ou un autre code d’erreur en cas d’échec.</span><span class="sxs-lookup"><span data-stu-id="5bb8c-144">This method returns one of the following codes or another error code if it fails.</span></span>



| <span data-ttu-id="5bb8c-145">Code/valeur de retour</span><span class="sxs-lookup"><span data-stu-id="5bb8c-145">Return code/value</span></span>                                                                                                                                 | <span data-ttu-id="5bb8c-146">Description</span><span class="sxs-lookup"><span data-stu-id="5bb8c-146">Description</span></span>                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <span data-ttu-id="5bb8c-147"><dt>**S \_ OK**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="5bb8c-147"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl> | <span data-ttu-id="5bb8c-148">La méthode a réussi.</span><span class="sxs-lookup"><span data-stu-id="5bb8c-148">The method was successful.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="5bb8c-149">Notes</span><span class="sxs-lookup"><span data-stu-id="5bb8c-149">Remarks</span></span>

<span data-ttu-id="5bb8c-150">Vous pouvez chiffrer un volume uniquement si vous appelez [**DisableKeyProtectors**](disablekeyprotectors-win32-encryptablevolume.md) en premier ou utilisez l’une des méthodes suivantes :</span><span class="sxs-lookup"><span data-stu-id="5bb8c-150">You can encrypt a volume only if you either call [**DisableKeyProtectors**](disablekeyprotectors-win32-encryptablevolume.md) first or use one of the following methods:</span></span>

-   [<span data-ttu-id="5bb8c-151">**ProtectKeyWithCertificateFile**</span><span class="sxs-lookup"><span data-stu-id="5bb8c-151">**ProtectKeyWithCertificateFile**</span></span>](protectkeywithcertificatefile-win32-encryptablevolume.md)
-   [<span data-ttu-id="5bb8c-152">**ProtectKeyWithCertificateThumbprint**</span><span class="sxs-lookup"><span data-stu-id="5bb8c-152">**ProtectKeyWithCertificateThumbprint**</span></span>](protectkeywithcertificatethumbprint-win32-encryptablevolume.md)
-   [<span data-ttu-id="5bb8c-153">**ProtectKeyWithExternalKey**</span><span class="sxs-lookup"><span data-stu-id="5bb8c-153">**ProtectKeyWithExternalKey**</span></span>](protectkeywithexternalkey-win32-encryptablevolume.md)
-   [<span data-ttu-id="5bb8c-154">**ProtectKeyWithNumericalPassword**</span><span class="sxs-lookup"><span data-stu-id="5bb8c-154">**ProtectKeyWithNumericalPassword**</span></span>](protectkeywithnumericalpassword-win32-encryptablevolume.md)
-   [<span data-ttu-id="5bb8c-155">**ProtectKeyWithPassphrase**</span><span class="sxs-lookup"><span data-stu-id="5bb8c-155">**ProtectKeyWithPassphrase**</span></span>](protectkeywithpassphrase-win32-encryptablevolume.md)
-   [<span data-ttu-id="5bb8c-156">**ProtectKeyWithTPM**</span><span class="sxs-lookup"><span data-stu-id="5bb8c-156">**ProtectKeyWithTPM**</span></span>](protectkeywithtpm-win32-encryptablevolume.md)
-   [<span data-ttu-id="5bb8c-157">**ProtectKeyWithTPMAndPIN**</span><span class="sxs-lookup"><span data-stu-id="5bb8c-157">**ProtectKeyWithTPMAndPIN**</span></span>](protectkeywithtpmandpin-win32-encryptablevolume.md)
-   [<span data-ttu-id="5bb8c-158">**ProtectKeyWithTPMAndPINAndStartupKey**</span><span class="sxs-lookup"><span data-stu-id="5bb8c-158">**ProtectKeyWithTPMAndPINAndStartupKey**</span></span>](protectkeywithtpmandpinandstartupkey-win32-encryptablevolume.md)
-   [<span data-ttu-id="5bb8c-159">**ProtectKeyWithTPMAndStartupKey**</span><span class="sxs-lookup"><span data-stu-id="5bb8c-159">**ProtectKeyWithTPMAndStartupKey**</span></span>](protectkeywithtpmandstartupkey-win32-encryptablevolume.md)

<span data-ttu-id="5bb8c-160">Par conséquent, si le disque est chiffré et que *ProtectionStatus* retourne la valeur zéro (protection désactivée), les clés sont désactivées.</span><span class="sxs-lookup"><span data-stu-id="5bb8c-160">Therefore, if the disk is encrypted and *ProtectionStatus* returns zero (PROTECTION OFF), keys are disabled.</span></span>

<span data-ttu-id="5bb8c-161">Utilisez [**GetKeyProtectors**](getkeyprotectors-win32-encryptablevolume.md) pour répertorier les protecteurs de clé qui ont été spécifiés pour sécuriser la clé de chiffrement du volume.</span><span class="sxs-lookup"><span data-stu-id="5bb8c-161">Use [**GetKeyProtectors**](getkeyprotectors-win32-encryptablevolume.md) to list the key protectors that have been specified to secure the volume's encryption key.</span></span> <span data-ttu-id="5bb8c-162">Si les protecteurs de clé existent mais que la protection est égale à zéro (PROTECTION désactivée), utilisez [**EnableKeyProtectors**](enablekeyprotectors-win32-encryptablevolume.md) pour activer la protection du volume.</span><span class="sxs-lookup"><span data-stu-id="5bb8c-162">If key protectors exist but protection is zero (PROTECTION OFF), use [**EnableKeyProtectors**](enablekeyprotectors-win32-encryptablevolume.md) to turn on volume protection.</span></span>

<span data-ttu-id="5bb8c-163">Les fichiers format MOF (MOF) contiennent les définitions des classes Windows Management Instrumentation (WMI).</span><span class="sxs-lookup"><span data-stu-id="5bb8c-163">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="5bb8c-164">Les fichiers MOF ne sont pas installés dans le cadre de la SDK Windows.</span><span class="sxs-lookup"><span data-stu-id="5bb8c-164">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="5bb8c-165">Ils sont installés sur le serveur lorsque vous ajoutez le rôle associé à l’aide de l’Gestionnaire de serveur.</span><span class="sxs-lookup"><span data-stu-id="5bb8c-165">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="5bb8c-166">Pour plus d’informations sur les fichiers MOF, consultez [format MOF (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="5bb8c-166">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="5bb8c-167">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5bb8c-167">Requirements</span></span>



| <span data-ttu-id="5bb8c-168">Condition requise</span><span class="sxs-lookup"><span data-stu-id="5bb8c-168">Requirement</span></span> | <span data-ttu-id="5bb8c-169">Valeur</span><span class="sxs-lookup"><span data-stu-id="5bb8c-169">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5bb8c-170">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5bb8c-170">Minimum supported client</span></span><br/> | <span data-ttu-id="5bb8c-171">Windows Vista entreprise, les applications de bureau Windows Vista Édition intégrale \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="5bb8c-171">Windows Vista Enterprise, Windows Vista Ultimate \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="5bb8c-172">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5bb8c-172">Minimum supported server</span></span><br/> | <span data-ttu-id="5bb8c-173">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="5bb8c-173">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="5bb8c-174">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="5bb8c-174">Namespace</span></span><br/>                | <span data-ttu-id="5bb8c-175">Racine \\ de \\ sécurité cimv2 \\ MicrosoftVolumeEncryption</span><span class="sxs-lookup"><span data-stu-id="5bb8c-175">Root\\CIMV2\\Security\\MicrosoftVolumeEncryption</span></span><br/>                                             |
| <span data-ttu-id="5bb8c-176">MOF</span><span class="sxs-lookup"><span data-stu-id="5bb8c-176">MOF</span></span><br/>                      | <dl> <span data-ttu-id="5bb8c-177"><dt>Win32 \_ encryptablevolume. mof</dt></span><span class="sxs-lookup"><span data-stu-id="5bb8c-177"><dt>Win32\_encryptablevolume.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5bb8c-178">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5bb8c-178">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5bb8c-179">**\_EncryptableVolume Win32**</span><span class="sxs-lookup"><span data-stu-id="5bb8c-179">**Win32\_EncryptableVolume**</span></span>](win32-encryptablevolume.md)
</dt> </dl>

 

 
