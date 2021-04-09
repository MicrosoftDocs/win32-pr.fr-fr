---
description: Commence le chiffrement d’un volume entièrement déchiffré, ou reprend le chiffrement d’un volume partiellement chiffré.
ms.assetid: bba8b800-309b-4268-8278-db69827bbdf6
title: Méthode Encrypt de la classe Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.Encrypt
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 463f13c250404e9a66095144166e74dbfae933ac
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104035204"
---
# <a name="encrypt-method-of-the-win32_encryptablevolume-class"></a><span data-ttu-id="ed5e1-103">Méthode Encrypt de la \_ classe EncryptableVolume Win32</span><span class="sxs-lookup"><span data-stu-id="ed5e1-103">Encrypt method of the Win32\_EncryptableVolume class</span></span>

<span data-ttu-id="ed5e1-104">La méthode **Encrypt** de la [**classe \_ EncryptableVolume Win32**](win32-encryptablevolume.md) commence le chiffrement d’un volume entièrement déchiffré, ou reprend le chiffrement d’un volume partiellement chiffré.</span><span class="sxs-lookup"><span data-stu-id="ed5e1-104">The **Encrypt** method of the [**Win32\_EncryptableVolume**](win32-encryptablevolume.md) class begins encryption of a fully decrypted volume, or resumes encryption of a partially encrypted volume.</span></span> <span data-ttu-id="ed5e1-105">Lorsque le chiffrement est suspendu ou en cours, cette méthode se comporte comme [**ResumeConversion**](resumeconversion-win32-encryptablevolume.md).</span><span class="sxs-lookup"><span data-stu-id="ed5e1-105">When encryption is paused or in-progress, this method behaves the same as [**ResumeConversion**](resumeconversion-win32-encryptablevolume.md).</span></span> <span data-ttu-id="ed5e1-106">Lorsque le déchiffrement est suspendu ou en cours, cette méthode arrête le déchiffrement et commence le chiffrement.</span><span class="sxs-lookup"><span data-stu-id="ed5e1-106">When decryption is paused or in-progress, this method stops the decryption and begins encryption.</span></span>

> [!Note]  
> <span data-ttu-id="ed5e1-107">Si le lecteur est chiffré sur le matériel, cette méthode ne chiffre pas les données.</span><span class="sxs-lookup"><span data-stu-id="ed5e1-107">If the drive is hardware encrypted, this method does not encrypt data.</span></span> <span data-ttu-id="ed5e1-108">Au lieu de cela, il définit l’état de la bande sur « déverrouillé » à « toujours déverrouillé ».</span><span class="sxs-lookup"><span data-stu-id="ed5e1-108">Instead, it sets the band status to "unlocked" from "always unlocked".</span></span> <span data-ttu-id="ed5e1-109">Si la bande est verrouillée, déverrouillée ou est en lecture seule, le lecteur est considéré comme étant chiffré.</span><span class="sxs-lookup"><span data-stu-id="ed5e1-109">If the band is locked, unlocked or is read-only, the drive is considered to be encrypted.</span></span>

 

<span data-ttu-id="ed5e1-110">**Windows Vista :** Le chiffrement d’un volume autre que le volume du système d’exploitation en cours d’exécution n’est pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="ed5e1-110">**Windows Vista:** Encryption of a volume other than the currently running operating system volume is not supported.</span></span>

## <a name="syntax"></a><span data-ttu-id="ed5e1-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ed5e1-111">Syntax</span></span>


```mof
uint32 Encrypt(
  [in, optional] uint32 EncryptionMethod,
  [in, optional] uint32 EncryptionFlags
);
```



## <a name="parameters"></a><span data-ttu-id="ed5e1-112">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ed5e1-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ed5e1-113">*EncryptionMethod* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="ed5e1-113">*EncryptionMethod* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="ed5e1-114">Type : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ed5e1-114">Type: **uint32**</span></span>

<span data-ttu-id="ed5e1-115">Entier non signé qui spécifie l’algorithme de chiffrement et la taille de clé utilisés pour chiffrer le volume.</span><span class="sxs-lookup"><span data-stu-id="ed5e1-115">An unsigned integer that specifies the encryption algorithm and key size used to encrypt the volume.</span></span> <span data-ttu-id="ed5e1-116">Si ce paramètre est supérieur à zéro et que le volume est partiellement ou entièrement chiffré, *EncryptionMethod* doit correspondre à la méthode de chiffrement existante du volume.</span><span class="sxs-lookup"><span data-stu-id="ed5e1-116">If this parameter is greater than zero and the volume is partially or fully encrypted, *EncryptionMethod* must match the volume's existing encryption method.</span></span> <span data-ttu-id="ed5e1-117">Si ce paramètre est supérieur à zéro et que le paramètre de stratégie de groupe correspondant est activé avec une valeur valide, *EncryptionMethod* doit correspondre au paramètre stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="ed5e1-117">If this parameter is greater than zero and the corresponding Group Policy setting is enabled with a valid value, *EncryptionMethod* must match the Group Policy setting.</span></span>

<span data-ttu-id="ed5e1-118">Pour obtenir la liste des valeurs de EncryptionMethod possibles, consultez la méthode [**GetEncryptionMethod**](getencryptionmethod-win32-encryptablevolume.md) .</span><span class="sxs-lookup"><span data-stu-id="ed5e1-118">For a list of possible EncryptionMethod values, see the [**GetEncryptionMethod**](getencryptionmethod-win32-encryptablevolume.md) method.</span></span>

<span data-ttu-id="ed5e1-119">La valeur par défaut pour Windows 7 ou une valeur inférieure est : 1 (AES \_ 128 \_ avec \_ diffuseur).</span><span class="sxs-lookup"><span data-stu-id="ed5e1-119">Default value for Windows 7 or below is: 1 (AES\_128\_WITH\_DIFFUSER).</span></span>

<span data-ttu-id="ed5e1-120">La valeur par défaut pour Windows 8, Windows 8.1 ou Windows 10, version 1507 est : 3 (AES \_ 128).</span><span class="sxs-lookup"><span data-stu-id="ed5e1-120">Default value for Windows 8, Windows 8.1 or Windows 10, version 1507 is: 3 (AES\_128).</span></span>

<span data-ttu-id="ed5e1-121">La valeur par défaut pour Windows 10, version 1511 ou ultérieure est : 6 (XTS \_ AES \_ 128).</span><span class="sxs-lookup"><span data-stu-id="ed5e1-121">Default value for Windows 10, version 1511 or above is: 6 (XTS\_AES\_128).</span></span>

</dd> <dt>

<span data-ttu-id="ed5e1-122">*EncryptionFlags* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="ed5e1-122">*EncryptionFlags* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="ed5e1-123">Type : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ed5e1-123">Type: **uint32**</span></span>

<span data-ttu-id="ed5e1-124">Indicateurs qui décrivent le comportement de chiffrement.</span><span class="sxs-lookup"><span data-stu-id="ed5e1-124">Flags that describe the encryption behavior.</span></span>

<span data-ttu-id="ed5e1-125">**Windows 7, Windows server 2008 R2, Windows Vista entreprise et Windows server 2008 :** Ce paramètre n’est pas disponible.</span><span class="sxs-lookup"><span data-stu-id="ed5e1-125">**Windows 7, Windows Server 2008 R2, Windows Vista Enterprise and Windows Server 2008:** This parameter is not available.</span></span>

<span data-ttu-id="ed5e1-126">Combinaison de 32 bits avec les bits suivants actuellement définis.</span><span class="sxs-lookup"><span data-stu-id="ed5e1-126">A combination of 32 bits with following bits currently defined.</span></span>



| <span data-ttu-id="ed5e1-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="ed5e1-127">Value</span></span>                                                                                  | <span data-ttu-id="ed5e1-128">Signification</span><span class="sxs-lookup"><span data-stu-id="ed5e1-128">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
|----------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="ed5e1-129"><dt>0x00000001</dt></span><span class="sxs-lookup"><span data-stu-id="ed5e1-129"><dt>0x00000001</dt></span></span> </dl>  | <span data-ttu-id="ed5e1-130">Effectuez le chiffrement du volume en mode de chiffrement de données uniquement lors du démarrage du nouveau processus de chiffrement.</span><span class="sxs-lookup"><span data-stu-id="ed5e1-130">Perform volume encryption in data-only encryption mode when starting new encryption process.</span></span> <span data-ttu-id="ed5e1-131">Si le chiffrement a été suspendu ou arrêté, l’appel de la méthode **Encrypt** reprend efficacement la conversion et la valeur de ce bit est ignorée.</span><span class="sxs-lookup"><span data-stu-id="ed5e1-131">If encryption has been paused or stopped, calling the **Encrypt** method effectively resumes conversion and the value of this bit is ignored.</span></span> <span data-ttu-id="ed5e1-132">Ce bit n’a d’effet que lorsque les méthodes **Encrypt** ou [**EncryptAfterHardwareTest**](encryptafterhardwaretest-win32-encryptablevolume.md) démarrent le chiffrement à partir de l’état de déchiffrement intégral, du déchiffrement en cours ou de l’état de déchiffrement suspendu.</span><span class="sxs-lookup"><span data-stu-id="ed5e1-132">This bit only has effect when either the **Encrypt** or [**EncryptAfterHardwareTest**](encryptafterhardwaretest-win32-encryptablevolume.md) methods start encryption from the fully decrypted state, decryption in progress state, or decryption paused state.</span></span> <span data-ttu-id="ed5e1-133">Si ce bit est égal à zéro, ce qui signifie qu’il n’est pas défini lors du démarrage du nouveau processus de chiffrement, la conversion en mode complet est effectuée.</span><span class="sxs-lookup"><span data-stu-id="ed5e1-133">If this bit is zero, meaning that it is not set, when starting new encryption process, then full mode conversion will be performed.</span></span><br/> |
| <dl> <span data-ttu-id="ed5e1-134"><dt>0x00000002</dt></span><span class="sxs-lookup"><span data-stu-id="ed5e1-134"><dt>0x00000002</dt></span></span> </dl>  | <span data-ttu-id="ed5e1-135">Effectuez une réinitialisation à la demande de l’espace libre du volume.</span><span class="sxs-lookup"><span data-stu-id="ed5e1-135">Perform on-demand wipe of the volume free space.</span></span> <span data-ttu-id="ed5e1-136">L’appel de la méthode **Encrypt** avec cet ensemble de bits est autorisé uniquement lorsque le volume n’est pas en cours de conversion ou d’effacement et est dans un État « chiffré ».</span><span class="sxs-lookup"><span data-stu-id="ed5e1-136">Calling the **Encrypt** method with this bit set is only allowed when volume is not currently converting or wiping and is in an "encrypted" state.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| <dl> <span data-ttu-id="ed5e1-137"><dt>0x00010000 </dt></span><span class="sxs-lookup"><span data-stu-id="ed5e1-137"><dt>0x00010000 </dt></span></span> </dl> | <span data-ttu-id="ed5e1-138">Effectuez l’opération demandée de façon synchrone.</span><span class="sxs-lookup"><span data-stu-id="ed5e1-138">Perform the requested operation synchronously.</span></span> <span data-ttu-id="ed5e1-139">L’appel sera bloqué jusqu’à ce que l’opération demandée soit terminée ou ait été interrompue.</span><span class="sxs-lookup"><span data-stu-id="ed5e1-139">The call will block until requested operation has completed or was interrupted.</span></span> <span data-ttu-id="ed5e1-140">Cet indicateur est pris en charge uniquement avec la méthode **Encrypt** .</span><span class="sxs-lookup"><span data-stu-id="ed5e1-140">This flag is only supported with the **Encrypt** method.</span></span> <span data-ttu-id="ed5e1-141">Cet indicateur peut être spécifié lorsque l’option **Encrypt** est appelée pour reprendre le chiffrement ou l’effacement arrêté ou interrompu ou lorsque le chiffrement ou l’effacement est en cours.</span><span class="sxs-lookup"><span data-stu-id="ed5e1-141">This flag can be specified when **Encrypt** is called to resume stopped or interrupted encryption or wiping or when either encryption or wiping is in progress.</span></span> <span data-ttu-id="ed5e1-142">Cela permet à l’appelant de reprendre en mode synchrone l’attente jusqu’à ce que le processus soit terminé ou interrompu.</span><span class="sxs-lookup"><span data-stu-id="ed5e1-142">This allows the caller to resume synchronously waiting until the process is completed or interrupted.</span></span><br/>                                                                                                                                                                                  |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ed5e1-143">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="ed5e1-143">Return value</span></span>

<span data-ttu-id="ed5e1-144">Type : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ed5e1-144">Type: **uint32**</span></span>

<span data-ttu-id="ed5e1-145">Cette méthode retourne l’un des codes suivants, ou un autre code d’erreur en cas d’échec.</span><span class="sxs-lookup"><span data-stu-id="ed5e1-145">This method returns one of the following codes or another error code if it fails.</span></span>

<span data-ttu-id="ed5e1-146">Cette méthode est retournée immédiatement.</span><span class="sxs-lookup"><span data-stu-id="ed5e1-146">This method returns immediately.</span></span> <span data-ttu-id="ed5e1-147">Si le volume est déjà entièrement chiffré et qu’aucune autre erreur n’est renvoyée, cette méthode retourne 0.</span><span class="sxs-lookup"><span data-stu-id="ed5e1-147">If the volume is already fully encrypted and no other errors are returned, this method returns 0.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="ed5e1-148">Code/valeur de retour</span><span class="sxs-lookup"><span data-stu-id="ed5e1-148">Return code/value</span></span></th>
<th><span data-ttu-id="ed5e1-149">Description</span><span class="sxs-lookup"><span data-stu-id="ed5e1-149">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><dl> <span data-ttu-id="ed5e1-150"><dt><strong>S_OK</strong></dt> <dt>0 (0x0)</dt> </span><span class="sxs-lookup"><span data-stu-id="ed5e1-150"><dt><strong>S_OK</strong></dt> <dt>0 (0x0)</dt> </span></span></dl></td>
<td><span data-ttu-id="ed5e1-151">La méthode a réussi.</span><span class="sxs-lookup"><span data-stu-id="ed5e1-151">The method was successful.</span></span><br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="ed5e1-152"><dt><strong>E_INVALIDARG</strong></dt> <dt>2147942487 (0x80070057)</dt> </span><span class="sxs-lookup"><span data-stu-id="ed5e1-152"><dt><strong>E_INVALIDARG</strong></dt> <dt>2147942487 (0x80070057)</dt> </span></span></dl></td>
<td><span data-ttu-id="ed5e1-153">Le paramètre <em>EncryptionMethod</em> est fourni, mais il n’est pas dans la plage connue ou ne correspond pas au paramètre de stratégie de groupe actuel.</span><span class="sxs-lookup"><span data-stu-id="ed5e1-153">The <em>EncryptionMethod</em> parameter is provided but is not within the known range or does not match the current Group Policy setting.</span></span><br/></td>
</tr>
<tr class="odd">
<td><dl> <span data-ttu-id="ed5e1-154"><dt><strong>FVE_E_CANNOT_ENCRYPT_NO_KEY</strong></dt> <dt>2150694958 (0x8031002E)</dt> </span><span class="sxs-lookup"><span data-stu-id="ed5e1-154"><dt><strong>FVE_E_CANNOT_ENCRYPT_NO_KEY</strong></dt> <dt>2150694958 (0x8031002E)</dt> </span></span></dl></td>
<td><span data-ttu-id="ed5e1-155">Il n’existe aucune clé de chiffrement pour le volume.</span><span class="sxs-lookup"><span data-stu-id="ed5e1-155">No encryption key exists for the volume.</span></span> <span data-ttu-id="ed5e1-156">Désactivez les protecteurs de clé à l’aide de la méthode <a href="disablekeyprotectors-win32-encryptablevolume.md"><strong>DisableKeyProtectors</strong></a> ou utilisez l’une des méthodes suivantes pour spécifier les protecteurs de clé pour le volume :</span><span class="sxs-lookup"><span data-stu-id="ed5e1-156">Either disable key protectors by using the <a href="disablekeyprotectors-win32-encryptablevolume.md"><strong>DisableKeyProtectors</strong></a> method or use one of the following methods to specify key protectors for the volume:</span></span><br/>
<ul>
<li><span data-ttu-id="ed5e1-157"><a href="protectkeywithexternalkey-win32-encryptablevolume.md"><strong>ProtectKeyWithExternalKey</strong></a></span><span class="sxs-lookup"><span data-stu-id="ed5e1-157"><a href="protectkeywithexternalkey-win32-encryptablevolume.md"><strong>ProtectKeyWithExternalKey</strong></a></span></span></li>
<li><span data-ttu-id="ed5e1-158"><a href="protectkeywithnumericalpassword-win32-encryptablevolume.md"><strong>ProtectKeyWithNumericalPassword</strong></a></span><span class="sxs-lookup"><span data-stu-id="ed5e1-158"><a href="protectkeywithnumericalpassword-win32-encryptablevolume.md"><strong>ProtectKeyWithNumericalPassword</strong></a></span></span></li>
<li><span data-ttu-id="ed5e1-159"><a href="protectkeywithtpm-win32-encryptablevolume.md"><strong>ProtectKeyWithTPM</strong></a></span><span class="sxs-lookup"><span data-stu-id="ed5e1-159"><a href="protectkeywithtpm-win32-encryptablevolume.md"><strong>ProtectKeyWithTPM</strong></a></span></span></li>
<li><span data-ttu-id="ed5e1-160"><a href="protectkeywithtpmandpin-win32-encryptablevolume.md"><strong>ProtectKeyWithTPMAndPIN</strong></a></span><span class="sxs-lookup"><span data-stu-id="ed5e1-160"><a href="protectkeywithtpmandpin-win32-encryptablevolume.md"><strong>ProtectKeyWithTPMAndPIN</strong></a></span></span></li>
<li><span data-ttu-id="ed5e1-161"><a href="protectkeywithtpmandpinandstartupkey-win32-encryptablevolume.md"><strong>ProtectKeyWithTPMAndPINAndStartupKey</strong></a></span><span class="sxs-lookup"><span data-stu-id="ed5e1-161"><a href="protectkeywithtpmandpinandstartupkey-win32-encryptablevolume.md"><strong>ProtectKeyWithTPMAndPINAndStartupKey</strong></a></span></span></li>
<li><span data-ttu-id="ed5e1-162"><a href="protectkeywithtpmandstartupkey-win32-encryptablevolume.md"><strong>ProtectKeyWithTPMAndStartupKey</strong></a></span><span class="sxs-lookup"><span data-stu-id="ed5e1-162"><a href="protectkeywithtpmandstartupkey-win32-encryptablevolume.md"><strong>ProtectKeyWithTPMAndStartupKey</strong></a></span></span></li>
</ul><span data-ttu-id="ed5e1-163">
<strong>Windows Vista :</strong> Lorsqu’il n’existe aucune clé de chiffrement pour le volume, ERROR_INVALID_OPERATION est retourné à la place.</span><span class="sxs-lookup"><span data-stu-id="ed5e1-163">
<strong>Windows Vista:</strong> When no encryption key exists for the volume, ERROR_INVALID_OPERATION is returned instead.</span></span> <span data-ttu-id="ed5e1-164">La valeur décimale est 4317 et la valeur hexadécimale est 0x10DD.</span><span class="sxs-lookup"><span data-stu-id="ed5e1-164">The decimal value is 4317 and the hexadecimal value is 0x10DD.</span></span><br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="ed5e1-165"><dt><strong>FVE_E_CANNOT_SET_FVEK_ENCRYPTED</strong></dt> <dt>2150694957 (0x8031002D)</dt> </span><span class="sxs-lookup"><span data-stu-id="ed5e1-165"><dt><strong>FVE_E_CANNOT_SET_FVEK_ENCRYPTED</strong></dt> <dt>2150694957 (0x8031002D)</dt> </span></span></dl></td>
<td><span data-ttu-id="ed5e1-166">La méthode de chiffrement fournie ne correspond pas à celle du volume partiellement ou entièrement chiffré.</span><span class="sxs-lookup"><span data-stu-id="ed5e1-166">The provided encryption method does not match that of the partially or fully encrypted volume.</span></span> <span data-ttu-id="ed5e1-167">Pour continuer le chiffrement, laissez le paramètre <em>EncryptionMethod</em> vide ou utilisez une valeur égale à zéro.</span><span class="sxs-lookup"><span data-stu-id="ed5e1-167">To continue encryption, leave the <em>EncryptionMethod</em> parameter blank or use a value of zero.</span></span><br/></td>
</tr>
<tr class="odd">
<td><dl> <span data-ttu-id="ed5e1-168"><dt><strong>FVE_E_CLUSTERING_NOT_SUPPORTED</strong></dt> <dt>2150694942 (0x8031001E)</dt> </span><span class="sxs-lookup"><span data-stu-id="ed5e1-168"><dt><strong>FVE_E_CLUSTERING_NOT_SUPPORTED</strong></dt> <dt>2150694942 (0x8031001E)</dt> </span></span></dl></td>
<td><span data-ttu-id="ed5e1-169">Le volume ne peut pas être chiffré car cet ordinateur est configuré pour faire partie d’un cluster de serveurs.</span><span class="sxs-lookup"><span data-stu-id="ed5e1-169">The volume cannot be encrypted because this computer is configured to be part of a server cluster.</span></span><br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="ed5e1-170"><dt><strong>FVE_E_LOCKED_VOLUME</strong></dt> <dt>2150694912 (0x80310000)</dt> </span><span class="sxs-lookup"><span data-stu-id="ed5e1-170"><dt><strong>FVE_E_LOCKED_VOLUME</strong></dt> <dt>2150694912 (0x80310000)</dt> </span></span></dl></td>
<td><span data-ttu-id="ed5e1-171">Le volume est verrouillé.</span><span class="sxs-lookup"><span data-stu-id="ed5e1-171">The volume is locked.</span></span><br/></td>
</tr>
<tr class="odd">
<td><dl> <span data-ttu-id="ed5e1-172"><dt><strong>FVE_E_POLICY_PASSWORD_REQUIRED</strong></dt> <dt>2150694956 (0x8031002C)</dt> </span><span class="sxs-lookup"><span data-stu-id="ed5e1-172"><dt><strong>FVE_E_POLICY_PASSWORD_REQUIRED</strong></dt> <dt>2150694956 (0x8031002C)</dt> </span></span></dl></td>
<td><span data-ttu-id="ed5e1-173">Aucun protecteur de clé du type de &quot; mot de passe numérique &quot; n’est spécifié.</span><span class="sxs-lookup"><span data-stu-id="ed5e1-173">No key protectors of the type &quot;Numerical Password&quot; are specified.</span></span> <span data-ttu-id="ed5e1-174">Le stratégie de groupe nécessite une sauvegarde des informations de récupération pour Active Directory Domain Services.</span><span class="sxs-lookup"><span data-stu-id="ed5e1-174">The Group Policy requires a backup of recovery information to Active Directory Domain Services.</span></span> <span data-ttu-id="ed5e1-175">Pour ajouter au moins un protecteur de clé de ce type, utilisez la méthode <a href="protectkeywithnumericalpassword-win32-encryptablevolume.md"><strong>ProtectKeyWithNumericalPassword</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="ed5e1-175">To add at least one key protector of that type, use the <a href="protectkeywithnumericalpassword-win32-encryptablevolume.md"><strong>ProtectKeyWithNumericalPassword</strong></a> method.</span></span><br/></td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a><span data-ttu-id="ed5e1-176">Notes</span><span class="sxs-lookup"><span data-stu-id="ed5e1-176">Remarks</span></span>

<span data-ttu-id="ed5e1-177">Lorsque vous utilisez cette méthode sans le second paramètre facultatif (selon la définition de Windows 7 et de Windows Vista Enterprise), la méthode lance toujours la conversion en mode complet afin de conserver un comportement à compatibilité descendante.</span><span class="sxs-lookup"><span data-stu-id="ed5e1-177">When you use this method without the second optional parameter (according to the Windows 7 and Windows Vista Enterprise definition), the method will always initiate full mode conversion in order to keep backward compatible behavior.</span></span> <span data-ttu-id="ed5e1-178">De cette façon, l’attente de sécurité des applications et des scripts existants ne sera pas interrompue par l’ajout du deuxième paramètre facultatif dans Windows 8 et Windows Server 2012.</span><span class="sxs-lookup"><span data-stu-id="ed5e1-178">This way the security expectation of existing applications and scripts will not be broken with the addition of the second optional parameter in Windows 8 and Windows Server 2012.</span></span>

<span data-ttu-id="ed5e1-179">Vous pouvez appeler [**GetConversionStatus**](getconversionstatus-win32-encryptablevolume.md) pour déterminer si le chiffrement est en cours et le pourcentage du volume qui a été chiffré.</span><span class="sxs-lookup"><span data-stu-id="ed5e1-179">You can call [**GetConversionStatus**](getconversionstatus-win32-encryptablevolume.md) to determine whether encryption is in progress and the percentage of the volume that has been encrypted.</span></span>

<span data-ttu-id="ed5e1-180">Une fois que le volume est entièrement chiffré et que des protecteurs de clés ont été ajoutés et activés, l’état de protection du volume passe à « activé ».</span><span class="sxs-lookup"><span data-stu-id="ed5e1-180">After the volume is fully encrypted and if key protectors have been added and enabled, the protection status for the volume changes to "on".</span></span>

<span data-ttu-id="ed5e1-181">Les fichiers format MOF (MOF) contiennent les définitions des classes Windows Management Instrumentation (WMI).</span><span class="sxs-lookup"><span data-stu-id="ed5e1-181">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="ed5e1-182">Les fichiers MOF ne sont pas installés dans le cadre de la SDK Windows.</span><span class="sxs-lookup"><span data-stu-id="ed5e1-182">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="ed5e1-183">Ils sont installés sur le serveur lorsque vous ajoutez le rôle associé à l’aide de l’Gestionnaire de serveur.</span><span class="sxs-lookup"><span data-stu-id="ed5e1-183">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="ed5e1-184">Pour plus d’informations sur les fichiers MOF, consultez [format MOF (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="ed5e1-184">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="ed5e1-185">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ed5e1-185">Requirements</span></span>



| <span data-ttu-id="ed5e1-186">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ed5e1-186">Requirement</span></span> | <span data-ttu-id="ed5e1-187">Valeur</span><span class="sxs-lookup"><span data-stu-id="ed5e1-187">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ed5e1-188">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ed5e1-188">Minimum supported client</span></span><br/> | <span data-ttu-id="ed5e1-189">Windows Vista entreprise, les applications de bureau Windows Vista Édition intégrale \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ed5e1-189">Windows Vista Enterprise, Windows Vista Ultimate \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="ed5e1-190">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ed5e1-190">Minimum supported server</span></span><br/> | <span data-ttu-id="ed5e1-191">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ed5e1-191">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="ed5e1-192">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="ed5e1-192">Namespace</span></span><br/>                | <span data-ttu-id="ed5e1-193">Racine \\ de \\ sécurité cimv2 \\ MicrosoftVolumeEncryption</span><span class="sxs-lookup"><span data-stu-id="ed5e1-193">Root\\CIMV2\\Security\\MicrosoftVolumeEncryption</span></span><br/>                                             |
| <span data-ttu-id="ed5e1-194">MOF</span><span class="sxs-lookup"><span data-stu-id="ed5e1-194">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ed5e1-195"><dt>Win32 \_ encryptablevolume. mof</dt></span><span class="sxs-lookup"><span data-stu-id="ed5e1-195"><dt>Win32\_encryptablevolume.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ed5e1-196">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ed5e1-196">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ed5e1-197">**\_EncryptableVolume Win32**</span><span class="sxs-lookup"><span data-stu-id="ed5e1-197">**Win32\_EncryptableVolume**</span></span>](win32-encryptablevolume.md)
</dt> </dl>

 

 
