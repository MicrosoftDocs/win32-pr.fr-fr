---
description: Fournit des informations d’État sur un test matériel d’un volume de système d’exploitation entièrement déchiffré.
ms.assetid: d76bc266-3718-443e-94f9-dcaa0ec53151
title: Méthode GetHardwareTestStatus de la classe Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.GetHardwareTestStatus
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 26d1984a79edef5f00f7687260fda7b211153863
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106521317"
---
# <a name="gethardwareteststatus-method-of-the-win32_encryptablevolume-class"></a><span data-ttu-id="faae7-103">Méthode GetHardwareTestStatus de la \_ classe Win32 EncryptableVolume</span><span class="sxs-lookup"><span data-stu-id="faae7-103">GetHardwareTestStatus method of the Win32\_EncryptableVolume class</span></span>

<span data-ttu-id="faae7-104">La méthode **GetHardwareTestStatus** de la classe [**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md) fournit des informations d’État sur un test matériel d’un volume de système d’exploitation entièrement déchiffré.</span><span class="sxs-lookup"><span data-stu-id="faae7-104">The **GetHardwareTestStatus** method of the [**Win32\_EncryptableVolume**](win32-encryptablevolume.md) class provides status information about a hardware test of a fully decrypted operating system volume.</span></span>

<span data-ttu-id="faae7-105">Utilisez cette méthode pour indiquer si un test matériel est en attente, ainsi que la réussite ou l’échec d’un test matériel qui s’est terminé lors du dernier redémarrage de l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="faae7-105">Use this method to show whether a hardware test is pending, as well as the success or failure of a hardware test that completed on the last computer restart.</span></span> <span data-ttu-id="faae7-106">Pour demander un test matériel, utilisez la méthode [**EncryptAfterHardwareTest**](encryptafterhardwaretest-win32-encryptablevolume.md) .</span><span class="sxs-lookup"><span data-stu-id="faae7-106">To request a hardware test, use the [**EncryptAfterHardwareTest**](encryptafterhardwaretest-win32-encryptablevolume.md) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="faae7-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="faae7-107">Syntax</span></span>


```mof
uint32 GetHardwareTestStatus(
  [out] uint32 TestStatus,
  [out] uint32 TestError
);
```



## <a name="parameters"></a><span data-ttu-id="faae7-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="faae7-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="faae7-109">*TestStatus* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="faae7-109">*TestStatus* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="faae7-110">Type : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="faae7-110">Type: **uint32**</span></span>

<span data-ttu-id="faae7-111">Spécifie si un test matériel est en attente, ainsi que la réussite de l’échec d’un test matériel qui s’est terminé lors du dernier redémarrage de l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="faae7-111">Specifies whether a hardware test is pending, as well as the success of failure of a hardware test that completed on the last computer restart.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="faae7-112">Valeur</span><span class="sxs-lookup"><span data-stu-id="faae7-112">Value</span></span></th>
<th><span data-ttu-id="faae7-113">Signification</span><span class="sxs-lookup"><span data-stu-id="faae7-113">Meaning</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span id="NotFailed_and_NonePending"></span><span id="notfailed_and_nonepending"></span><span id="NOTFAILED_AND_NONEPENDING"></span><dl> <span data-ttu-id="faae7-114"><dt><strong>NotFailed_and_NonePending</strong></dt> <dt>0</dt> </span><span class="sxs-lookup"><span data-stu-id="faae7-114"><dt><strong>NotFailed_and_NonePending</strong></dt> <dt>0</dt> </span></span></dl></td>
<td><span data-ttu-id="faae7-115">Si un test a été demandé, le test a réussi au dernier redémarrage de l’ordinateur et le chiffrement du volume est maintenant en cours.</span><span class="sxs-lookup"><span data-stu-id="faae7-115">If a test was requested, the test has succeeded on the last computer restart and volume encryption is now in progress.</span></span> <span data-ttu-id="faae7-116">Pour connaître l’état du chiffrement, consultez la méthode <a href="getconversionstatus-win32-encryptablevolume.md"><strong>GetConversionStatus</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="faae7-116">For the encryption status, see the <a href="getconversionstatus-win32-encryptablevolume.md"><strong>GetConversionStatus</strong></a> method.</span></span> <span data-ttu-id="faae7-117">Dans le cas contraire, aucun test n’a été exécuté au dernier redémarrage de l’ordinateur et aucun n’est en attente.</span><span class="sxs-lookup"><span data-stu-id="faae7-117">Otherwise, no test ran on the last computer restart and none is pending.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span id="Failed"></span><span id="failed"></span><span id="FAILED"></span><dl> <span data-ttu-id="faae7-118"><dt><strong>Échec</strong></dt> <dt>1</dt> </span><span class="sxs-lookup"><span data-stu-id="faae7-118"><dt><strong>Failed</strong></dt> <dt>1</dt> </span></span></dl></td>
<td><span data-ttu-id="faae7-119">Le chiffrement de volume n’a pas démarré.</span><span class="sxs-lookup"><span data-stu-id="faae7-119">Volume encryption did not start.</span></span> <span data-ttu-id="faae7-120">Tous les protecteurs de clé ont été supprimés.</span><span class="sxs-lookup"><span data-stu-id="faae7-120">All key protectors were removed.</span></span><br/> <span data-ttu-id="faae7-121">Pour résoudre un échec de test :</span><span class="sxs-lookup"><span data-stu-id="faae7-121">To resolve a failed test:</span></span><br/>
<ul>
<li><span data-ttu-id="faae7-122">Consultez les informations contenues dans le paramètre <em>TestError</em> .</span><span class="sxs-lookup"><span data-stu-id="faae7-122">Consult the information in the <em>TestError</em> parameter.</span></span></li>
<li><span data-ttu-id="faae7-123">Ajoutez des protecteurs de clé et réutilisez la méthode <a href="encryptafterhardwaretest-win32-encryptablevolume.md"><strong>EncryptAfterHardwareTest</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="faae7-123">Add key protectors and use the <a href="encryptafterhardwaretest-win32-encryptablevolume.md"><strong>EncryptAfterHardwareTest</strong></a> method again.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span id="Pending"></span><span id="pending"></span><span id="PENDING"></span><dl> <span data-ttu-id="faae7-124"><dt><strong>En attente</strong></dt> <dt>2</dt> </span><span class="sxs-lookup"><span data-stu-id="faae7-124"><dt><strong>Pending</strong></dt> <dt>2</dt> </span></span></dl></td>
<td><span data-ttu-id="faae7-125">Un test a été demandé et s’exécutera au prochain redémarrage de l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="faae7-125">A test has been requested and will run on the next computer restart.</span></span><br/></td>
</tr>
</tbody>
</table>



 

</dd> <dt>

<span data-ttu-id="faae7-126">*TestError* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="faae7-126">*TestError* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="faae7-127">Type : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="faae7-127">Type: **uint32**</span></span>

<span data-ttu-id="faae7-128">Spécifie l’erreur du dernier test matériel effectué.</span><span class="sxs-lookup"><span data-stu-id="faae7-128">Specifies the error from the last completed hardware test.</span></span>



| <span data-ttu-id="faae7-129">Valeur</span><span class="sxs-lookup"><span data-stu-id="faae7-129">Value</span></span>                                                                                               | <span data-ttu-id="faae7-130">Signification</span><span class="sxs-lookup"><span data-stu-id="faae7-130">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                  |
|-----------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="faae7-131"><dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="faae7-131"><dt>0</dt></span></span> </dl>                        | <span data-ttu-id="faae7-132">Aucune erreur ne s’est produite ou aucun test matériel n’a été exécuté lors du dernier redémarrage de l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="faae7-132">No errors occurred or no hardware test ran on the last computer restart.</span></span><br/>                                                                                                                                                                                                                                                                      |
| <dl> <span data-ttu-id="faae7-133"><dt> 2150694972 (0x8031003C)</dt></span><span class="sxs-lookup"><span data-stu-id="faae7-133"><dt> 2150694972 (0x8031003C)</dt></span></span> </dl> | <span data-ttu-id="faae7-134">FVE \_ E \_ keyfile \_ \_ introuvable</span><span class="sxs-lookup"><span data-stu-id="faae7-134">FVE\_E\_KEYFILE\_NOT\_FOUND</span></span><br/> <span data-ttu-id="faae7-135">Un lecteur flash USB avec un fichier de clé externe est introuvable.</span><span class="sxs-lookup"><span data-stu-id="faae7-135">A USB flash drive with an external key file was not found.</span></span> <span data-ttu-id="faae7-136">Si le problème persiste, l’ordinateur ne peut pas lire les lecteurs USB lors du redémarrage.</span><span class="sxs-lookup"><span data-stu-id="faae7-136">If this failure persists, the computer cannot read USB drives during restart.</span></span> <span data-ttu-id="faae7-137">Vous ne pourrez peut-être pas utiliser de clés externes pour déverrouiller le volume du système d’exploitation lors du redémarrage.</span><span class="sxs-lookup"><span data-stu-id="faae7-137">You may not be able to use external keys to unlock the operating system volume during restart.</span></span><br/>                                                                |
| <dl> <span data-ttu-id="faae7-138"><dt> 2150694973 (0x8031003D)</dt></span><span class="sxs-lookup"><span data-stu-id="faae7-138"><dt> 2150694973 (0x8031003D)</dt></span></span> </dl> | <span data-ttu-id="faae7-139">FVE \_ E \_ keyfile \_ non valide</span><span class="sxs-lookup"><span data-stu-id="faae7-139">FVE\_E\_KEYFILE\_INVALID</span></span><br/> <span data-ttu-id="faae7-140">Le fichier de clé externe sur le disque mémoire flash USB est endommagé.</span><span class="sxs-lookup"><span data-stu-id="faae7-140">The external key file on the USB flash drive was corrupt.</span></span> <span data-ttu-id="faae7-141">Essayez d’utiliser un autre lecteur flash USB pour stocker le fichier de clé externe.</span><span class="sxs-lookup"><span data-stu-id="faae7-141">Try a different USB flash drive to store the external key file.</span></span><br/>                                                                                                                                                                                 |
| <dl> <span data-ttu-id="faae7-142"><dt> 2150694975 (0x8031003F)</dt></span><span class="sxs-lookup"><span data-stu-id="faae7-142"><dt> 2150694975 (0x8031003F)</dt></span></span> </dl> | <span data-ttu-id="faae7-143">FVE \_ E \_ TPM \_ désactivé</span><span class="sxs-lookup"><span data-stu-id="faae7-143">FVE\_E\_TPM\_DISABLED</span></span><br/> <span data-ttu-id="faae7-144">Le module de plateforme sécurisée est désactivé ou désactivé, ou désactivé et désactivé.</span><span class="sxs-lookup"><span data-stu-id="faae7-144">The TPM is either disabled or deactivated or both disabled and deactivated.</span></span> <span data-ttu-id="faae7-145">Pour activer le module de plateforme sécurisée, utilisez le fournisseur WMI [**\_ TPM Win32**](win32-tpm.md) ou exécutez le composant logiciel enfichable de gestion du module de plateforme sécurisée (TPM. msc).</span><span class="sxs-lookup"><span data-stu-id="faae7-145">To turn on the TPM, use the [**Win32\_Tpm**](win32-tpm.md) WMI provider or run the TPM management snap-in (Tpm.msc).</span></span><br/>                                                                                                            |
| <dl> <span data-ttu-id="faae7-146"><dt> 2150694977 (0x80310041)</dt></span><span class="sxs-lookup"><span data-stu-id="faae7-146"><dt> 2150694977 (0x80310041)</dt></span></span> </dl> | <span data-ttu-id="faae7-147">\_PCR FVE E \_ TPM \_ non valide \_</span><span class="sxs-lookup"><span data-stu-id="faae7-147">FVE\_E\_TPM\_INVALID\_PCR</span></span><br/> <span data-ttu-id="faae7-148">Le module de plateforme sécurisée a détecté une modification des services de redémarrage du système d’exploitation dans le profil de validation de plateforme actuel.</span><span class="sxs-lookup"><span data-stu-id="faae7-148">The TPM detected a change in operating system restart services within the current platform validation profile.</span></span> <span data-ttu-id="faae7-149">Retirez un CD ou un DVD de démarrage de l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="faae7-149">Remove any startup CD or DVD from the computer.</span></span> <span data-ttu-id="faae7-150">Si le problème persiste, vérifiez que les mises à niveau du microprogramme et du BIOS les plus récentes sont installées, et que le module de plateforme sécurisée fonctionne normalement.</span><span class="sxs-lookup"><span data-stu-id="faae7-150">If this failure persists, check that the latest firmware and BIOS upgrades are installed, and that the TPM is otherwise working properly.</span></span><br/> |
| <dl> <span data-ttu-id="faae7-151"><dt>2150694979 (0x80310043)</dt></span><span class="sxs-lookup"><span data-stu-id="faae7-151"><dt>2150694979 (0x80310043)</dt></span></span> </dl>  | <span data-ttu-id="faae7-152">\_ \_ code PIN E FVE \_ non valide</span><span class="sxs-lookup"><span data-stu-id="faae7-152">FVE\_E\_PIN\_INVALID</span></span><br/> <span data-ttu-id="faae7-153">Le code PIN fourni est incorrect.</span><span class="sxs-lookup"><span data-stu-id="faae7-153">The provided PIN was incorrect.</span></span><br/>                                                                                                                                                                                                                                                                               |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="faae7-154">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="faae7-154">Return value</span></span>

<span data-ttu-id="faae7-155">Type : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="faae7-155">Type: **uint32**</span></span>

<span data-ttu-id="faae7-156">Le tableau suivant répertorie certains des codes de retour courants.</span><span class="sxs-lookup"><span data-stu-id="faae7-156">The following table lists some of the common return codes.</span></span>



| <span data-ttu-id="faae7-157">Code/valeur de retour</span><span class="sxs-lookup"><span data-stu-id="faae7-157">Return code/value</span></span>                                                                                                                                                                  | <span data-ttu-id="faae7-158">Description</span><span class="sxs-lookup"><span data-stu-id="faae7-158">Description</span></span>                      |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="faae7-159"><dt>**S \_ OK**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="faae7-159"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl>                                  | <span data-ttu-id="faae7-160">S_OK</span><span class="sxs-lookup"><span data-stu-id="faae7-160">The method succeeded.</span></span><br/> |
| <dl> <span data-ttu-id="faae7-161"><dt>**FVE \_ E \_ Locked \_ volume**</dt> <dt>2150694912 (0x80310000)</dt></span><span class="sxs-lookup"><span data-stu-id="faae7-161"><dt>**FVE\_E\_LOCKED\_VOLUME**</dt> <dt>2150694912 (0x80310000)</dt></span></span> </dl> | <span data-ttu-id="faae7-162">Le volume est verrouillé.</span><span class="sxs-lookup"><span data-stu-id="faae7-162">The volume is locked.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="faae7-163">Notes</span><span class="sxs-lookup"><span data-stu-id="faae7-163">Remarks</span></span>

<span data-ttu-id="faae7-164">Pour demander un test matériel, utilisez la méthode [**EncryptAfterHardwareTest**](encryptafterhardwaretest-win32-encryptablevolume.md) .</span><span class="sxs-lookup"><span data-stu-id="faae7-164">To request a hardware test, use the [**EncryptAfterHardwareTest**](encryptafterhardwaretest-win32-encryptablevolume.md) method.</span></span>

<span data-ttu-id="faae7-165">Pour exécuter un test matériel lorsque son état est en attente, procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="faae7-165">To run a hardware test when its status is pending, follow these steps:</span></span>

1.  <span data-ttu-id="faae7-166">Insérez dans l’ordinateur un lecteur flash USB qui contient un fichier de clé externe.</span><span class="sxs-lookup"><span data-stu-id="faae7-166">Insert into the computer a USB flash drive that contains an external key file.</span></span> <span data-ttu-id="faae7-167">Cette étape s’applique uniquement si le volume a un protecteur de clé de type « clé externe » ou « TPM et clé de démarrage ».</span><span class="sxs-lookup"><span data-stu-id="faae7-167">This step applies only if the volume has a key protector of type "External Key" or "TPM And Startup Key".</span></span>
2.  <span data-ttu-id="faae7-168">Redémarrez l'ordinateur.</span><span class="sxs-lookup"><span data-stu-id="faae7-168">Restart the computer.</span></span> <span data-ttu-id="faae7-169">Lors du redémarrage de l’ordinateur, le test matériel s’exécute automatiquement.</span><span class="sxs-lookup"><span data-stu-id="faae7-169">On computer restart, the hardware test runs automatically.</span></span>

<span data-ttu-id="faae7-170">Pour annuler le test matériel, utilisez la méthode [**Encrypt**](encrypt-win32-encryptablevolume.md) .</span><span class="sxs-lookup"><span data-stu-id="faae7-170">To cancel the hardware test, use the [**Encrypt**](encrypt-win32-encryptablevolume.md) method.</span></span>

<span data-ttu-id="faae7-171">Un test réussi détermine que :</span><span class="sxs-lookup"><span data-stu-id="faae7-171">A successful test determines that:</span></span>

-   <span data-ttu-id="faae7-172">Le module de plateforme sécurisée peut déverrouiller le volume s’il en existe un.</span><span class="sxs-lookup"><span data-stu-id="faae7-172">The TPM can unlock the volume if a TPM-related key protector exists.</span></span>
-   <span data-ttu-id="faae7-173">L’ordinateur peut lire un lecteur flash USB qui contient un fichier de clé externe au démarrage si le volume peut être déverrouillé par une clé externe (y compris une clé de démarrage).</span><span class="sxs-lookup"><span data-stu-id="faae7-173">The computer can read a USB flash drive that contains an external key file during startup if the volume can be unlocked by an external key (including a startup key).</span></span>

<span data-ttu-id="faae7-174">Les résultats des tests matériels ne seront pas disponibles après toute modification apportée à la conversion ou après le prochain redémarrage de l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="faae7-174">Hardware test results will not be available after any changes in conversion or after the next computer restart.</span></span> <span data-ttu-id="faae7-175">Consultez le journal des événements système pour obtenir des informations sur les tests matériels précédemment exécutés sur l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="faae7-175">Check the System event log for the information about any hardware tests that previously ran on the computer.</span></span>

<span data-ttu-id="faae7-176">Les fichiers format MOF (MOF) contiennent les définitions des classes Windows Management Instrumentation (WMI).</span><span class="sxs-lookup"><span data-stu-id="faae7-176">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="faae7-177">Les fichiers MOF ne sont pas installés dans le cadre de la SDK Windows.</span><span class="sxs-lookup"><span data-stu-id="faae7-177">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="faae7-178">Ils sont installés sur le serveur lorsque vous ajoutez le rôle associé à l’aide de l’Gestionnaire de serveur.</span><span class="sxs-lookup"><span data-stu-id="faae7-178">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="faae7-179">Pour plus d’informations sur les fichiers MOF, consultez [format MOF (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="faae7-179">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="faae7-180">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="faae7-180">Requirements</span></span>



| <span data-ttu-id="faae7-181">Condition requise</span><span class="sxs-lookup"><span data-stu-id="faae7-181">Requirement</span></span> | <span data-ttu-id="faae7-182">Valeur</span><span class="sxs-lookup"><span data-stu-id="faae7-182">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="faae7-183">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="faae7-183">Minimum supported client</span></span><br/> | <span data-ttu-id="faae7-184">Windows Vista entreprise, les applications de bureau Windows Vista Édition intégrale \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="faae7-184">Windows Vista Enterprise, Windows Vista Ultimate \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="faae7-185">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="faae7-185">Minimum supported server</span></span><br/> | <span data-ttu-id="faae7-186">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="faae7-186">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="faae7-187">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="faae7-187">Namespace</span></span><br/>                | <span data-ttu-id="faae7-188">Racine \\ de \\ sécurité cimv2 \\ MicrosoftVolumeEncryption</span><span class="sxs-lookup"><span data-stu-id="faae7-188">Root\\CIMV2\\Security\\MicrosoftVolumeEncryption</span></span><br/>                                             |
| <span data-ttu-id="faae7-189">MOF</span><span class="sxs-lookup"><span data-stu-id="faae7-189">MOF</span></span><br/>                      | <dl> <span data-ttu-id="faae7-190"><dt>Win32 \_ encryptablevolume. mof</dt></span><span class="sxs-lookup"><span data-stu-id="faae7-190"><dt>Win32\_encryptablevolume.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="faae7-191">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="faae7-191">See also</span></span>

<dl> <dt>

[<span data-ttu-id="faae7-192">**\_EncryptableVolume Win32**</span><span class="sxs-lookup"><span data-stu-id="faae7-192">**Win32\_EncryptableVolume**</span></span>](win32-encryptablevolume.md)
</dt> </dl>

 

 
