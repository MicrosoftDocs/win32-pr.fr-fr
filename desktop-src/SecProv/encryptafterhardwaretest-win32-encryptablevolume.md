---
description: Commence le chiffrement d’un volume de système d’exploitation entièrement déchiffré après un test matériel.
ms.assetid: 216c96bb-7737-4421-8b16-1ce295342266
title: Méthode EncryptAfterHardwareTest de la classe Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.EncryptAfterHardwareTest
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: f356b9adda5e1b25fdd3d9fc39ace5cf8028da32
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525689"
---
# <a name="encryptafterhardwaretest-method-of-the-win32_encryptablevolume-class"></a><span data-ttu-id="482bf-103">Méthode EncryptAfterHardwareTest de la \_ classe Win32 EncryptableVolume</span><span class="sxs-lookup"><span data-stu-id="482bf-103">EncryptAfterHardwareTest method of the Win32\_EncryptableVolume class</span></span>

<span data-ttu-id="482bf-104">La méthode **EncryptAfterHardwareTest** de la classe [**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md) commence le chiffrement d’un volume de système d’exploitation entièrement déchiffré après un test matériel.</span><span class="sxs-lookup"><span data-stu-id="482bf-104">The **EncryptAfterHardwareTest** method of the [**Win32\_EncryptableVolume**](win32-encryptablevolume.md) class begins encryption of a fully decrypted operating system volume after a hardware test.</span></span> <span data-ttu-id="482bf-105">Un redémarrage est nécessaire pour effectuer ce test matériel.</span><span class="sxs-lookup"><span data-stu-id="482bf-105">A reboot is required to perform this hardware test.</span></span> <span data-ttu-id="482bf-106">Utilisez cette méthode à la place de la méthode [**Encrypt**](encrypt-win32-encryptablevolume.md) pour vérifier que BitLocker fonctionnera comme prévu.</span><span class="sxs-lookup"><span data-stu-id="482bf-106">Use this method instead of the [**Encrypt**](encrypt-win32-encryptablevolume.md) method to check that BitLocker will work as expected.</span></span>

> [!Note]  
> <span data-ttu-id="482bf-107">Si le disque dur est chiffré sur le matériel, cette méthode ne chiffre pas les données.</span><span class="sxs-lookup"><span data-stu-id="482bf-107">If the hard drive is hardware encrypted, this method does not encrypt data.</span></span> <span data-ttu-id="482bf-108">Au lieu de cela, il définit l’état de la bande sur déverrouillé de « perpétuellement déverrouillé ».</span><span class="sxs-lookup"><span data-stu-id="482bf-108">Instead, it sets the band status to unlocked from "perpetually unlocked".</span></span> <span data-ttu-id="482bf-109">Si la bande est verrouillée, déverrouillée ou est en lecture seule, le lecteur est considéré comme étant chiffré.</span><span class="sxs-lookup"><span data-stu-id="482bf-109">If the band is locked, unlocked or is read-only, the drive is considered to be encrypted.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="482bf-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="482bf-110">Syntax</span></span>


```mof
uint32 EncryptAfterHardwareTest(
  [in, optional] uint32 EncryptionMethod,
  [in, optional] uint32 EncryptionFlags
);
```



## <a name="parameters"></a><span data-ttu-id="482bf-111">Paramètres</span><span class="sxs-lookup"><span data-stu-id="482bf-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="482bf-112">*EncryptionMethod* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="482bf-112">*EncryptionMethod* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="482bf-113">Type : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="482bf-113">Type: **uint32**</span></span>

<span data-ttu-id="482bf-114">Spécifie l’algorithme de chiffrement et la taille de clé utilisés pour chiffrer le volume.</span><span class="sxs-lookup"><span data-stu-id="482bf-114">Specifies the encryption algorithm and key size used to encrypt the volume.</span></span> <span data-ttu-id="482bf-115">Laissez ce paramètre vide pour utiliser la valeur par défaut de zéro.</span><span class="sxs-lookup"><span data-stu-id="482bf-115">Leave this parameter blank to use the default value of zero.</span></span> <span data-ttu-id="482bf-116">Si le volume est partiellement ou entièrement chiffré, la valeur de ce paramètre doit être égale à 0 ou correspondre à la méthode de chiffrement existante du volume.</span><span class="sxs-lookup"><span data-stu-id="482bf-116">If the volume is partially or fully encrypted, the value of this parameter must be 0 or match the volume's existing encryption method.</span></span> <span data-ttu-id="482bf-117">Si le paramètre de stratégie de groupe correspondant a été activé avec une valeur valide, la valeur de ce paramètre doit être 0 ou correspondre au paramètre stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="482bf-117">If the corresponding Group Policy setting has been enabled with a valid value, the value of this parameter must be 0 or match the Group Policy setting.</span></span>

<span data-ttu-id="482bf-118">Si le paramètre de stratégie de groupe correspondant n’est pas valide, la valeur par défaut AES 128 avec diffuseur est utilisée.</span><span class="sxs-lookup"><span data-stu-id="482bf-118">If the corresponding Group Policy setting is invalid, the default of AES 128 with diffuser is used.</span></span>



| <span data-ttu-id="482bf-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="482bf-119">Value</span></span>                                                                                                                                                                                                                                       | <span data-ttu-id="482bf-120">Signification</span><span class="sxs-lookup"><span data-stu-id="482bf-120">Meaning</span></span>                                                                                                                                                                                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Unspecified"></span><span id="unspecified"></span><span id="UNSPECIFIED"></span><dl> <span data-ttu-id="482bf-121"><dt>0</dt> <dt>**non spécifié**</dt></span><span class="sxs-lookup"><span data-stu-id="482bf-121"><dt>**Unspecified**</dt> <dt>0</dt></span></span> </dl> | <span data-ttu-id="482bf-122">Utilisez le paramètre de stratégie de groupe actuel, s’il est disponible et valide, ou la méthode de chiffrement par défaut dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="482bf-122">Use the current Group Policy setting, if available and valid, or the default encryption method otherwise.</span></span><br/>                                                                              |
| <dl> <span data-ttu-id="482bf-123"><dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="482bf-123"><dt>1</dt></span></span> </dl>                                                                                                                                                                | <span data-ttu-id="482bf-124">AES 128 AVEC DIFFUSEUR</span><span class="sxs-lookup"><span data-stu-id="482bf-124">AES 128 WITH DIFFUSER</span></span><br/> <span data-ttu-id="482bf-125">Chiffrez le volume à l’aide de l’algorithme Advanced Encryption Standard (AES) amélioré avec une couche diffuseur et en utilisant une taille de clé AES de 128 bits.</span><span class="sxs-lookup"><span data-stu-id="482bf-125">Encrypt the volume by using the Advanced Encryption Standard (AES) algorithm enhanced with a diffuser layer and by using an AES key size of 128 bits.</span></span><br/> |
| <dl> <span data-ttu-id="482bf-126"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="482bf-126"><dt>2</dt></span></span> </dl>                                                                                                                                                                | <span data-ttu-id="482bf-127">AES 256 AVEC DIFFUSEUR</span><span class="sxs-lookup"><span data-stu-id="482bf-127">AES 256 WITH DIFFUSER</span></span><br/> <span data-ttu-id="482bf-128">Chiffrez le volume à l’aide de l’algorithme Advanced Encryption Standard (AES) amélioré avec une couche diffuseur et en utilisant une taille de clé AES de 256 bits.</span><span class="sxs-lookup"><span data-stu-id="482bf-128">Encrypt the volume by using the Advanced Encryption Standard (AES) algorithm enhanced with a diffuser layer and by using an AES key size of 256 bits.</span></span><br/> |
| <span id="AES_128"></span><span id="aes_128"></span><dl> <span data-ttu-id="482bf-129"><dt>**AES \_ 128**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="482bf-129"><dt>**AES\_128**</dt> <dt>3</dt></span></span> </dl>                                          | <span data-ttu-id="482bf-130">Chiffrez le volume à l’aide de l’algorithme Advanced Encryption Standard (AES) et à l’aide d’une taille de clé AES de 128 bits.</span><span class="sxs-lookup"><span data-stu-id="482bf-130">Encrypt the volume by using the Advanced Encryption Standard (AES) algorithm and by using an AES key size of 128 bits.</span></span><br/>                                                                 |
| <span id="AES_256"></span><span id="aes_256"></span><dl> <span data-ttu-id="482bf-131"><dt>**AES \_ 256**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="482bf-131"><dt>**AES\_256**</dt> <dt>4</dt></span></span> </dl>                                          | <span data-ttu-id="482bf-132">Chiffrez le volume à l’aide de l’algorithme Advanced Encryption Standard (AES) et à l’aide d’une taille de clé AES de 256 bits.</span><span class="sxs-lookup"><span data-stu-id="482bf-132">Encrypt the volume by using the Advanced Encryption Standard (AES) algorithm and by using an AES key size of 256 bits.</span></span><br/>                                                                 |



 

</dd> <dt>

<span data-ttu-id="482bf-133">*EncryptionFlags* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="482bf-133">*EncryptionFlags* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="482bf-134">Type : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="482bf-134">Type: **uint32**</span></span>

<span data-ttu-id="482bf-135">Indicateurs qui décrivent le comportement de chiffrement.</span><span class="sxs-lookup"><span data-stu-id="482bf-135">Flags that describe the encryption behavior.</span></span>

<span data-ttu-id="482bf-136">**Windows 7, Windows server 2008 R2, Windows Vista entreprise et Windows server 2008 :** Ce paramètre n’est pas disponible.</span><span class="sxs-lookup"><span data-stu-id="482bf-136">**Windows 7, Windows Server 2008 R2, Windows Vista Enterprise and Windows Server 2008:** This parameter is not available.</span></span>

<span data-ttu-id="482bf-137">Combinaison de 32 bits avec les bits suivants actuellement définis.</span><span class="sxs-lookup"><span data-stu-id="482bf-137">A combination of 32 bits with the following bits currently defined.</span></span>



| <span data-ttu-id="482bf-138">Valeur</span><span class="sxs-lookup"><span data-stu-id="482bf-138">Value</span></span>                                                                                  | <span data-ttu-id="482bf-139">Signification</span><span class="sxs-lookup"><span data-stu-id="482bf-139">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|----------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="482bf-140"><dt>0x00000001</dt></span><span class="sxs-lookup"><span data-stu-id="482bf-140"><dt>0x00000001</dt></span></span> </dl>  | <span data-ttu-id="482bf-141">Effectuez le chiffrement du volume en mode de chiffrement de données uniquement lors du démarrage du nouveau processus de chiffrement.</span><span class="sxs-lookup"><span data-stu-id="482bf-141">Perform volume encryption in data-only encryption mode when starting new encryption process.</span></span> <span data-ttu-id="482bf-142">Si le chiffrement a été suspendu ou arrêté, l’appel de la méthode [**Encrypt**](encrypt-win32-encryptablevolume.md) reprend efficacement la conversion et la valeur de ce bit est ignorée.</span><span class="sxs-lookup"><span data-stu-id="482bf-142">If encryption has been paused or stopped, calling the [**Encrypt**](encrypt-win32-encryptablevolume.md) method effectively resumes conversion and the value of this bit is ignored.</span></span> <span data-ttu-id="482bf-143">Ce bit n’a d’effet que lorsque les méthodes **Encrypt** ou **EncryptAfterHardwareTest** démarrent le chiffrement à partir de l’état de déchiffrement intégral, du déchiffrement en cours ou de l’état de déchiffrement suspendu.</span><span class="sxs-lookup"><span data-stu-id="482bf-143">This bit only has effect when either the **Encrypt** or **EncryptAfterHardwareTest** methods start encryption from the fully decrypted state, decryption in progress state, or decryption paused state.</span></span> <span data-ttu-id="482bf-144">Si ce bit est égal à zéro, ce qui signifie qu’il n’est pas défini lors du démarrage du nouveau processus de chiffrement, la conversion en mode complet est effectuée.</span><span class="sxs-lookup"><span data-stu-id="482bf-144">If this bit is zero, meaning that it is not set, when starting new encryption process, then full mode conversion will be performed.</span></span><br/> |
| <dl> <span data-ttu-id="482bf-145"><dt>0x00000002</dt></span><span class="sxs-lookup"><span data-stu-id="482bf-145"><dt>0x00000002</dt></span></span> </dl>  | <span data-ttu-id="482bf-146">Effectuez une réinitialisation à la demande de l’espace libre du volume.</span><span class="sxs-lookup"><span data-stu-id="482bf-146">Perform on-demand wipe of the volume free space.</span></span> <span data-ttu-id="482bf-147">L’appel de la méthode [**Encrypt**](encrypt-win32-encryptablevolume.md) avec cet ensemble de bits est autorisé uniquement lorsque le volume n’est pas en cours de conversion ou d’effacement et est dans un État « chiffré ».</span><span class="sxs-lookup"><span data-stu-id="482bf-147">Calling the [**Encrypt**](encrypt-win32-encryptablevolume.md) method with this bit set is only allowed when volume is not currently converting or wiping and is in an "encrypted" state.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                    |
| <dl> <span data-ttu-id="482bf-148"><dt>0x00010000 </dt></span><span class="sxs-lookup"><span data-stu-id="482bf-148"><dt>0x00010000 </dt></span></span> </dl> | <span data-ttu-id="482bf-149">Effectuez l’opération demandée de façon synchrone.</span><span class="sxs-lookup"><span data-stu-id="482bf-149">Perform the requested operation synchronously.</span></span> <span data-ttu-id="482bf-150">L’appel sera bloqué jusqu’à ce que l’opération demandée soit terminée ou ait été interrompue.</span><span class="sxs-lookup"><span data-stu-id="482bf-150">The call will block until requested operation has completed or was interrupted.</span></span> <span data-ttu-id="482bf-151">Cet indicateur est pris en charge uniquement avec la méthode [**Encrypt**](encrypt-win32-encryptablevolume.md) .</span><span class="sxs-lookup"><span data-stu-id="482bf-151">This flag is only supported with the [**Encrypt**](encrypt-win32-encryptablevolume.md) method.</span></span> <span data-ttu-id="482bf-152">Cet indicateur peut être spécifié lorsque l’option **Encrypt** est appelée pour reprendre le chiffrement ou l’effacement arrêté ou interrompu ou lorsque le chiffrement ou l’effacement est en cours.</span><span class="sxs-lookup"><span data-stu-id="482bf-152">This flag can be specified when **Encrypt** is called to resume stopped or interrupted encryption or wiping or when either encryption or wiping is in progress.</span></span> <span data-ttu-id="482bf-153">Cela permet à l’appelant de reprendre en mode synchrone l’attente jusqu’à ce que le processus soit terminé ou interrompu.</span><span class="sxs-lookup"><span data-stu-id="482bf-153">This allows the caller to resume synchronously waiting until the process is completed or interrupted.</span></span><br/>                                                                                                                          |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="482bf-154">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="482bf-154">Return value</span></span>

<span data-ttu-id="482bf-155">Type : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="482bf-155">Type: **uint32**</span></span>

<span data-ttu-id="482bf-156">Cette méthode retourne l’un des codes suivants, ou un autre code d’erreur en cas d’échec.</span><span class="sxs-lookup"><span data-stu-id="482bf-156">This method returns one of the following codes or another error code if it fails.</span></span>

<span data-ttu-id="482bf-157">Cette méthode est retournée immédiatement.</span><span class="sxs-lookup"><span data-stu-id="482bf-157">This method returns immediately.</span></span> <span data-ttu-id="482bf-158">Si le volume est déjà entièrement chiffré et qu’aucune autre erreur n’est retournée, cette méthode retourne zéro.</span><span class="sxs-lookup"><span data-stu-id="482bf-158">If the volume is already fully encrypted and no other errors are returned, this method returns zero.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="482bf-159">Code/valeur de retour</span><span class="sxs-lookup"><span data-stu-id="482bf-159">Return code/value</span></span></th>
<th><span data-ttu-id="482bf-160">Description</span><span class="sxs-lookup"><span data-stu-id="482bf-160">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><dl> <span data-ttu-id="482bf-161"><dt><strong>S_OK</strong></dt> <dt>0 (0x0)</dt> </span><span class="sxs-lookup"><span data-stu-id="482bf-161"><dt><strong>S_OK</strong></dt> <dt>0 (0x0)</dt> </span></span></dl></td>
<td><span data-ttu-id="482bf-162">La méthode a réussi.</span><span class="sxs-lookup"><span data-stu-id="482bf-162">The method was successful.</span></span><br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="482bf-163"><dt><strong>E_INVALIDARG</strong></dt> <dt>2147942487 (0x80070057)</dt> </span><span class="sxs-lookup"><span data-stu-id="482bf-163"><dt><strong>E_INVALIDARG</strong></dt> <dt>2147942487 (0x80070057)</dt> </span></span></dl></td>
<td><span data-ttu-id="482bf-164">Le paramètre <em>EncryptionMethod</em> est fourni, mais il n’est pas dans la plage connue ou ne correspond pas au paramètre de stratégie de groupe actuel.</span><span class="sxs-lookup"><span data-stu-id="482bf-164">The <em>EncryptionMethod</em> parameter is provided but is not within the known range or does not match the current Group Policy setting.</span></span><br/></td>
</tr>
<tr class="odd">
<td><dl> <span data-ttu-id="482bf-165"><dt><strong>FVE_E_CANNOT_ENCRYPT_NO_KEY</strong></dt> <dt>2150694958 (0x8031002E)</dt> </span><span class="sxs-lookup"><span data-stu-id="482bf-165"><dt><strong>FVE_E_CANNOT_ENCRYPT_NO_KEY</strong></dt> <dt>2150694958 (0x8031002E)</dt> </span></span></dl></td>
<td><span data-ttu-id="482bf-166">Il n’existe aucune clé de chiffrement pour le volume.</span><span class="sxs-lookup"><span data-stu-id="482bf-166">No encryption key exists for the volume.</span></span><br/> <span data-ttu-id="482bf-167">Désactivez les protecteurs de clé à l’aide de la méthode <a href="disablekeyprotectors-win32-encryptablevolume.md"><strong>DisableKeyProtectors</strong></a> , ou utilisez l’une des méthodes suivantes pour spécifier les protecteurs de clé pour le volume :</span><span class="sxs-lookup"><span data-stu-id="482bf-167">Either disable key protectors by using the <a href="disablekeyprotectors-win32-encryptablevolume.md"><strong>DisableKeyProtectors</strong></a> method, or use one of the following methods to specify key protectors for the volume:</span></span>
<ul>
<li><span data-ttu-id="482bf-168"><a href="protectkeywithexternalkey-win32-encryptablevolume.md"><strong>ProtectKeyWithExternalKey</strong></a></span><span class="sxs-lookup"><span data-stu-id="482bf-168"><a href="protectkeywithexternalkey-win32-encryptablevolume.md"><strong>ProtectKeyWithExternalKey</strong></a></span></span></li>
<li><span data-ttu-id="482bf-169"><a href="protectkeywithnumericalpassword-win32-encryptablevolume.md"><strong>ProtectKeyWithNumericalPassword</strong></a></span><span class="sxs-lookup"><span data-stu-id="482bf-169"><a href="protectkeywithnumericalpassword-win32-encryptablevolume.md"><strong>ProtectKeyWithNumericalPassword</strong></a></span></span></li>
<li><span data-ttu-id="482bf-170"><a href="protectkeywithtpm-win32-encryptablevolume.md"><strong>ProtectKeyWithTPM</strong></a></span><span class="sxs-lookup"><span data-stu-id="482bf-170"><a href="protectkeywithtpm-win32-encryptablevolume.md"><strong>ProtectKeyWithTPM</strong></a></span></span></li>
<li><span data-ttu-id="482bf-171"><a href="protectkeywithtpmandpin-win32-encryptablevolume.md"><strong>ProtectKeyWithTPMAndPIN</strong></a></span><span class="sxs-lookup"><span data-stu-id="482bf-171"><a href="protectkeywithtpmandpin-win32-encryptablevolume.md"><strong>ProtectKeyWithTPMAndPIN</strong></a></span></span></li>
<li><span data-ttu-id="482bf-172"><a href="protectkeywithtpmandpinandstartupkey-win32-encryptablevolume.md"><strong>ProtectKeyWithTPMAndPINAndStartupKey</strong></a></span><span class="sxs-lookup"><span data-stu-id="482bf-172"><a href="protectkeywithtpmandpinandstartupkey-win32-encryptablevolume.md"><strong>ProtectKeyWithTPMAndPINAndStartupKey</strong></a></span></span></li>
<li><span data-ttu-id="482bf-173"><a href="protectkeywithtpmandstartupkey-win32-encryptablevolume.md"><strong>ProtectKeyWithTPMAndStartupKey</strong></a></span><span class="sxs-lookup"><span data-stu-id="482bf-173"><a href="protectkeywithtpmandstartupkey-win32-encryptablevolume.md"><strong>ProtectKeyWithTPMAndStartupKey</strong></a></span></span></li>
</ul>
<br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="482bf-174"><dt><strong>FVE_E_CLUSTERING_NOT_SUPPORTED</strong></dt> <dt>2150694942 (0x8031001E)</dt> </span><span class="sxs-lookup"><span data-stu-id="482bf-174"><dt><strong>FVE_E_CLUSTERING_NOT_SUPPORTED</strong></dt> <dt>2150694942 (0x8031001E)</dt> </span></span></dl></td>
<td><span data-ttu-id="482bf-175">Le volume ne peut pas être chiffré car cet ordinateur est configuré pour faire partie d’un cluster de serveurs.</span><span class="sxs-lookup"><span data-stu-id="482bf-175">The volume cannot be encrypted because this computer is configured to be part of a server cluster.</span></span><br/></td>
</tr>
<tr class="odd">
<td><dl> <span data-ttu-id="482bf-176"><dt><strong>FVE_E_NO_PROTECTORS_TO_TEST</strong></dt> <dt>2150694971 (0x8031003B)</dt> </span><span class="sxs-lookup"><span data-stu-id="482bf-176"><dt><strong>FVE_E_NO_PROTECTORS_TO_TEST</strong></dt> <dt>2150694971 (0x8031003B)</dt> </span></span></dl></td>
<td><span data-ttu-id="482bf-177">Aucun protecteur de clé de type &quot; TPM &quot; , &quot; TPM et pin &quot; , TPM, &quot; code confidentiel et clé de démarrage &quot; , TPM et clé de &quot; démarrage &quot; ou &quot; clé externe ne &quot; peut être trouvé.</span><span class="sxs-lookup"><span data-stu-id="482bf-177">No key protectors of the type &quot;TPM&quot;, &quot;TPM And PIN&quot;, &quot;TPM And PIN And Startup Key&quot;, &quot;TPM And Startup Key&quot;, or &quot;External Key&quot; can be found.</span></span> <span data-ttu-id="482bf-178">Le test matériel concerne uniquement les protecteurs de clé précédents.</span><span class="sxs-lookup"><span data-stu-id="482bf-178">The hardware test only involves the previous key protectors.</span></span><br/> <span data-ttu-id="482bf-179">Si vous souhaitez toujours exécuter un test matériel, vous devez utiliser l’une des méthodes suivantes pour spécifier les protecteurs de clé pour le volume :</span><span class="sxs-lookup"><span data-stu-id="482bf-179">If you still want to run a hardware test, you must use one of the following methods to specify key protectors for the volume:</span></span>
<ul>
<li><span data-ttu-id="482bf-180"><a href="protectkeywithexternalkey-win32-encryptablevolume.md"><strong>ProtectKeyWithExternalKey</strong></a></span><span class="sxs-lookup"><span data-stu-id="482bf-180"><a href="protectkeywithexternalkey-win32-encryptablevolume.md"><strong>ProtectKeyWithExternalKey</strong></a></span></span></li>
<li><span data-ttu-id="482bf-181"><a href="protectkeywithnumericalpassword-win32-encryptablevolume.md"><strong>ProtectKeyWithNumericalPassword</strong></a></span><span class="sxs-lookup"><span data-stu-id="482bf-181"><a href="protectkeywithnumericalpassword-win32-encryptablevolume.md"><strong>ProtectKeyWithNumericalPassword</strong></a></span></span></li>
<li><span data-ttu-id="482bf-182"><a href="protectkeywithtpm-win32-encryptablevolume.md"><strong>ProtectKeyWithTPM</strong></a></span><span class="sxs-lookup"><span data-stu-id="482bf-182"><a href="protectkeywithtpm-win32-encryptablevolume.md"><strong>ProtectKeyWithTPM</strong></a></span></span></li>
<li><span data-ttu-id="482bf-183"><a href="protectkeywithtpmandpin-win32-encryptablevolume.md"><strong>ProtectKeyWithTPMAndPIN</strong></a></span><span class="sxs-lookup"><span data-stu-id="482bf-183"><a href="protectkeywithtpmandpin-win32-encryptablevolume.md"><strong>ProtectKeyWithTPMAndPIN</strong></a></span></span></li>
<li><span data-ttu-id="482bf-184"><a href="protectkeywithtpmandpinandstartupkey-win32-encryptablevolume.md"><strong>ProtectKeyWithTPMAndPINAndStartupKey</strong></a></span><span class="sxs-lookup"><span data-stu-id="482bf-184"><a href="protectkeywithtpmandpinandstartupkey-win32-encryptablevolume.md"><strong>ProtectKeyWithTPMAndPINAndStartupKey</strong></a></span></span></li>
<li><span data-ttu-id="482bf-185"><a href="protectkeywithtpmandstartupkey-win32-encryptablevolume.md"><strong>ProtectKeyWithTPMAndStartupKey</strong></a></span><span class="sxs-lookup"><span data-stu-id="482bf-185"><a href="protectkeywithtpmandstartupkey-win32-encryptablevolume.md"><strong>ProtectKeyWithTPMAndStartupKey</strong></a></span></span></li>
</ul>
<br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="482bf-186"><dt><strong>FVE_E_NOT_DECRYPTED</strong></dt> <dt>2150694969 (0x80310039)</dt> </span><span class="sxs-lookup"><span data-stu-id="482bf-186"><dt><strong>FVE_E_NOT_DECRYPTED</strong></dt> <dt>2150694969 (0x80310039)</dt> </span></span></dl></td>
<td><span data-ttu-id="482bf-187">Le volume est partiellement ou entièrement chiffré.</span><span class="sxs-lookup"><span data-stu-id="482bf-187">The volume is partially or fully encrypted.</span></span><br/> <span data-ttu-id="482bf-188">Le test matériel s’applique avant le chiffrement.</span><span class="sxs-lookup"><span data-stu-id="482bf-188">The hardware test applies before encryption occurs.</span></span> <span data-ttu-id="482bf-189">Si vous souhaitez toujours exécuter le test, utilisez d’abord la méthode <a href="decrypt-win32-encryptablevolume.md"><strong>Decrypt</strong></a> , puis utilisez l’une des méthodes suivantes pour ajouter des protecteurs de clé :</span><span class="sxs-lookup"><span data-stu-id="482bf-189">If you still want to run the test, first use the <a href="decrypt-win32-encryptablevolume.md"><strong>Decrypt</strong></a> method and then use one of the following methods to add key protectors:</span></span>
<ul>
<li><span data-ttu-id="482bf-190"><a href="protectkeywithexternalkey-win32-encryptablevolume.md"><strong>ProtectKeyWithExternalKey</strong></a></span><span class="sxs-lookup"><span data-stu-id="482bf-190"><a href="protectkeywithexternalkey-win32-encryptablevolume.md"><strong>ProtectKeyWithExternalKey</strong></a></span></span></li>
<li><span data-ttu-id="482bf-191"><a href="protectkeywithnumericalpassword-win32-encryptablevolume.md"><strong>ProtectKeyWithNumericalPassword</strong></a></span><span class="sxs-lookup"><span data-stu-id="482bf-191"><a href="protectkeywithnumericalpassword-win32-encryptablevolume.md"><strong>ProtectKeyWithNumericalPassword</strong></a></span></span></li>
<li><span data-ttu-id="482bf-192"><a href="protectkeywithtpm-win32-encryptablevolume.md"><strong>ProtectKeyWithTPM</strong></a></span><span class="sxs-lookup"><span data-stu-id="482bf-192"><a href="protectkeywithtpm-win32-encryptablevolume.md"><strong>ProtectKeyWithTPM</strong></a></span></span></li>
<li><span data-ttu-id="482bf-193"><a href="protectkeywithtpmandpin-win32-encryptablevolume.md"><strong>ProtectKeyWithTPMAndPIN</strong></a></span><span class="sxs-lookup"><span data-stu-id="482bf-193"><a href="protectkeywithtpmandpin-win32-encryptablevolume.md"><strong>ProtectKeyWithTPMAndPIN</strong></a></span></span></li>
<li><span data-ttu-id="482bf-194"><a href="protectkeywithtpmandstartupkey-win32-encryptablevolume.md"><strong>ProtectKeyWithTPMAndStartupKey</strong></a></span><span class="sxs-lookup"><span data-stu-id="482bf-194"><a href="protectkeywithtpmandstartupkey-win32-encryptablevolume.md"><strong>ProtectKeyWithTPMAndStartupKey</strong></a></span></span></li>
</ul>
<br/></td>
</tr>
<tr class="odd">
<td><dl> <span data-ttu-id="482bf-195"><dt><strong>FVE_E_NOT_OS_VOLUME</strong></dt> <dt>2150694952 (0x80310028)</dt> </span><span class="sxs-lookup"><span data-stu-id="482bf-195"><dt><strong>FVE_E_NOT_OS_VOLUME</strong></dt> <dt>2150694952 (0x80310028)</dt> </span></span></dl></td>
<td><span data-ttu-id="482bf-196">Le volume est un volume de données.</span><span class="sxs-lookup"><span data-stu-id="482bf-196">The volume is a data volume.</span></span><br/> <span data-ttu-id="482bf-197">Le test matériel s’applique uniquement aux volumes qui peuvent démarrer le système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="482bf-197">The hardware test applies only to volumes that can start the operating system.</span></span> <span data-ttu-id="482bf-198">Exécutez cette méthode sur le volume du système d’exploitation actuellement démarré.</span><span class="sxs-lookup"><span data-stu-id="482bf-198">Run this method on the currently started operating system volume.</span></span><br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="482bf-199"><dt><strong>FVE_E_POLICY_PASSWORD_REQUIRED</strong></dt> <dt>2150694956 (0x8031002C)</dt> </span><span class="sxs-lookup"><span data-stu-id="482bf-199"><dt><strong>FVE_E_POLICY_PASSWORD_REQUIRED</strong></dt> <dt>2150694956 (0x8031002C)</dt> </span></span></dl></td>
<td><span data-ttu-id="482bf-200">Aucun protecteur de clé du type de &quot; mot de passe numérique &quot; n’est spécifié.</span><span class="sxs-lookup"><span data-stu-id="482bf-200">No key protectors of the type &quot;Numerical Password&quot; are specified.</span></span> <span data-ttu-id="482bf-201">Le stratégie de groupe nécessite une sauvegarde des informations de récupération pour Active Directory Domain Services.</span><span class="sxs-lookup"><span data-stu-id="482bf-201">The Group Policy requires a backup of recovery information to Active Directory Domain Services.</span></span> <span data-ttu-id="482bf-202">Pour ajouter au moins un protecteur de clé de ce type, utilisez la méthode <a href="protectkeywithnumericalpassword-win32-encryptablevolume.md"><strong>ProtectKeyWithNumericalPassword</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="482bf-202">To add at least one key protector of that type, use the <a href="protectkeywithnumericalpassword-win32-encryptablevolume.md"><strong>ProtectKeyWithNumericalPassword</strong></a> method.</span></span><br/></td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a><span data-ttu-id="482bf-203">Notes</span><span class="sxs-lookup"><span data-stu-id="482bf-203">Remarks</span></span>

<span data-ttu-id="482bf-204">Lorsque vous utilisez cette méthode sans le second paramètre facultatif (selon la définition de Windows 7 et de Windows Vista Enterprise), la méthode lance toujours la conversion en mode complet afin de conserver un comportement à compatibilité descendante.</span><span class="sxs-lookup"><span data-stu-id="482bf-204">When you use this method without the second optional parameter (according to the Windows 7 and Windows Vista Enterprise definition), the method will always initiate full mode conversion in order to keep backward compatible behavior.</span></span> <span data-ttu-id="482bf-205">De cette façon, l’attente de sécurité des applications et des scripts existants ne sera pas interrompue par l’ajout du deuxième paramètre facultatif dans Windows 8 et Windows Server 2012.</span><span class="sxs-lookup"><span data-stu-id="482bf-205">This way the security expectation of existing applications and scripts will not be broken with the addition of the second optional parameter in Windows 8 and Windows Server 2012.</span></span>

<span data-ttu-id="482bf-206">Contrairement à la méthode [**Encrypt**](encrypt-win32-encryptablevolume.md) , cette méthode effectue les opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="482bf-206">Unlike the [**Encrypt**](encrypt-win32-encryptablevolume.md) method, this method does the following:</span></span>

-   <span data-ttu-id="482bf-207">Teste si le module de plateforme sécurisée peut déverrouiller le volume, si un protecteur de clé lié au module de plateforme sécurisée existe.</span><span class="sxs-lookup"><span data-stu-id="482bf-207">Tests whether the TPM will be able to unlock the volume, if a TPM-related key protector exists.</span></span>
-   <span data-ttu-id="482bf-208">Teste si l’ordinateur peut lire un lecteur flash USB qui contient un fichier de clé externe au démarrage, si le volume est déverrouillé par une clé externe (y compris une clé de démarrage).</span><span class="sxs-lookup"><span data-stu-id="482bf-208">Tests whether the computer can read a USB flash drive that contains an external key file during start, if the volume will be unlocked by an external key (including a startup key).</span></span>
-   <span data-ttu-id="482bf-209">Nécessite un redémarrage de l’ordinateur pour exécuter le test matériel.</span><span class="sxs-lookup"><span data-stu-id="482bf-209">Requires a computer restart to run the hardware test.</span></span>
-   <span data-ttu-id="482bf-210">Commence le chiffrement uniquement si le test matériel est correctement effectué.</span><span class="sxs-lookup"><span data-stu-id="482bf-210">Begins encryption only if the hardware test succeeds.</span></span>
-   <span data-ttu-id="482bf-211">Ne peut pas être utilisé sur un volume de données, sur un volume partiellement ou entièrement chiffré, ou pour reprendre le chiffrement.</span><span class="sxs-lookup"><span data-stu-id="482bf-211">Cannot be used on a data volume, on a partially or fully encrypted volume, or to resume encryption.</span></span>

<span data-ttu-id="482bf-212">Avant d’exécuter cette méthode, utilisez les méthodes suivantes pour créer les protecteurs de clé associés :</span><span class="sxs-lookup"><span data-stu-id="482bf-212">Before running this method, use the following methods to create the related key protectors:</span></span>

-   [<span data-ttu-id="482bf-213">**ProtectKeyWithExternalKey**</span><span class="sxs-lookup"><span data-stu-id="482bf-213">**ProtectKeyWithExternalKey**</span></span>](protectkeywithexternalkey-win32-encryptablevolume.md)
-   [<span data-ttu-id="482bf-214">**ProtectKeyWithTPM**</span><span class="sxs-lookup"><span data-stu-id="482bf-214">**ProtectKeyWithTPM**</span></span>](protectkeywithtpm-win32-encryptablevolume.md)
-   [<span data-ttu-id="482bf-215">**ProtectKeyWithTPMAndPIN**</span><span class="sxs-lookup"><span data-stu-id="482bf-215">**ProtectKeyWithTPMAndPIN**</span></span>](protectkeywithtpmandpin-win32-encryptablevolume.md)
-   [<span data-ttu-id="482bf-216">**ProtectKeyWithTPMAndPINAndStartupKey**</span><span class="sxs-lookup"><span data-stu-id="482bf-216">**ProtectKeyWithTPMAndPINAndStartupKey**</span></span>](protectkeywithtpmandpinandstartupkey-win32-encryptablevolume.md)
-   [<span data-ttu-id="482bf-217">**ProtectKeyWithTPMAndStartupKey**</span><span class="sxs-lookup"><span data-stu-id="482bf-217">**ProtectKeyWithTPMAndStartupKey**</span></span>](protectkeywithtpmandstartupkey-win32-encryptablevolume.md)

<span data-ttu-id="482bf-218">Après avoir exécuté cette méthode, effectuez les étapes supplémentaires suivantes :</span><span class="sxs-lookup"><span data-stu-id="482bf-218">After running this method, take these additional steps:</span></span>

1.  <span data-ttu-id="482bf-219">Insérez dans l’ordinateur un lecteur flash USB qui contient un fichier de clé externe.</span><span class="sxs-lookup"><span data-stu-id="482bf-219">Insert into the computer a USB flash drive that contains an external key file.</span></span> <span data-ttu-id="482bf-220">Cette étape s’applique uniquement si le volume a un protecteur de clé de type « clé externe » ou « TPM et clé de démarrage ».</span><span class="sxs-lookup"><span data-stu-id="482bf-220">This step applies only if the volume has a key protector of type "External Key" or "TPM And Startup Key".</span></span>
2.  <span data-ttu-id="482bf-221">Redémarrez l'ordinateur.</span><span class="sxs-lookup"><span data-stu-id="482bf-221">Restart the computer.</span></span>

<span data-ttu-id="482bf-222">Lors du redémarrage de l’ordinateur, le test matériel s’exécute automatiquement.</span><span class="sxs-lookup"><span data-stu-id="482bf-222">On computer restart, the hardware test runs automatically.</span></span>

<span data-ttu-id="482bf-223">Le chiffrement commence si le test matériel est correctement effectué.</span><span class="sxs-lookup"><span data-stu-id="482bf-223">Encryption begins if the hardware test succeeds.</span></span> <span data-ttu-id="482bf-224">Sinon, essayez de résoudre les défaillances matérielles.</span><span class="sxs-lookup"><span data-stu-id="482bf-224">Otherwise, attempt to resolve any hardware failures.</span></span> <span data-ttu-id="482bf-225">Exécutez [**GetHardwareTestStatus**](gethardwareteststatus-win32-encryptablevolume.md) après avoir redémarré l’ordinateur pour obtenir les résultats des tests.</span><span class="sxs-lookup"><span data-stu-id="482bf-225">Run [**GetHardwareTestStatus**](gethardwareteststatus-win32-encryptablevolume.md) after restarting the computer to get test results.</span></span>

<span data-ttu-id="482bf-226">Les fichiers format MOF (MOF) contiennent les définitions des classes Windows Management Instrumentation (WMI).</span><span class="sxs-lookup"><span data-stu-id="482bf-226">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="482bf-227">Les fichiers MOF ne sont pas installés dans le cadre de la SDK Windows.</span><span class="sxs-lookup"><span data-stu-id="482bf-227">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="482bf-228">Ils sont installés sur le serveur lorsque vous ajoutez le rôle associé à l’aide de l’Gestionnaire de serveur.</span><span class="sxs-lookup"><span data-stu-id="482bf-228">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="482bf-229">Pour plus d’informations sur les fichiers MOF, consultez [format MOF (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="482bf-229">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="482bf-230">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="482bf-230">Requirements</span></span>



| <span data-ttu-id="482bf-231">Condition requise</span><span class="sxs-lookup"><span data-stu-id="482bf-231">Requirement</span></span> | <span data-ttu-id="482bf-232">Valeur</span><span class="sxs-lookup"><span data-stu-id="482bf-232">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="482bf-233">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="482bf-233">Minimum supported client</span></span><br/> | <span data-ttu-id="482bf-234">Windows Vista entreprise, les applications de bureau Windows Vista Édition intégrale \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="482bf-234">Windows Vista Enterprise, Windows Vista Ultimate \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="482bf-235">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="482bf-235">Minimum supported server</span></span><br/> | <span data-ttu-id="482bf-236">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="482bf-236">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="482bf-237">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="482bf-237">Namespace</span></span><br/>                | <span data-ttu-id="482bf-238">Racine \\ de \\ sécurité cimv2 \\ MicrosoftVolumeEncryption</span><span class="sxs-lookup"><span data-stu-id="482bf-238">Root\\CIMV2\\Security\\MicrosoftVolumeEncryption</span></span><br/>                                             |
| <span data-ttu-id="482bf-239">MOF</span><span class="sxs-lookup"><span data-stu-id="482bf-239">MOF</span></span><br/>                      | <dl> <span data-ttu-id="482bf-240"><dt>Win32 \_ encryptablevolume. mof</dt></span><span class="sxs-lookup"><span data-stu-id="482bf-240"><dt>Win32\_encryptablevolume.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="482bf-241">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="482bf-241">See also</span></span>

<dl> <dt>

[<span data-ttu-id="482bf-242">**\_EncryptableVolume Win32**</span><span class="sxs-lookup"><span data-stu-id="482bf-242">**Win32\_EncryptableVolume**</span></span>](win32-encryptablevolume.md)
</dt> </dl>

 

 
