---
description: Indique l’état du chiffrement ou du déchiffrement sur le volume.
ms.assetid: b292a380-1b4a-4dff-948b-6494ec3b400b
title: Méthode GetConversionStatus de la classe Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.GetConversionStatus
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 9357db3397b04639329c1afd502d9da30cbb39be
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862290"
---
# <a name="getconversionstatus-method-of-the-win32_encryptablevolume-class"></a><span data-ttu-id="2d209-103">Méthode GetConversionStatus de la \_ classe Win32 EncryptableVolume</span><span class="sxs-lookup"><span data-stu-id="2d209-103">GetConversionStatus method of the Win32\_EncryptableVolume class</span></span>

<span data-ttu-id="2d209-104">La méthode **GetConversionStatus** de la [**classe \_ EncryptableVolume Win32**](win32-encryptablevolume.md) indique l’état du chiffrement ou du déchiffrement sur le volume.</span><span class="sxs-lookup"><span data-stu-id="2d209-104">The **GetConversionStatus** method of the [**Win32\_EncryptableVolume**](win32-encryptablevolume.md) class indicates the status of the encryption or decryption on the volume.</span></span>

## <a name="syntax"></a><span data-ttu-id="2d209-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="2d209-105">Syntax</span></span>


```mof
uint32 GetConversionStatus(
  [out] uint32 ConversionStatus,
  [out] uint32 EncryptionPercentage,
  [out] uint32 EncryptionFlags,
  [out] uint32 WipingStatus,
  [out] uint32 WipingPercentage,
  [in]  uint32 PrecisionFactor
);
```



## <a name="parameters"></a><span data-ttu-id="2d209-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="2d209-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2d209-107">*ConversionStatus* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="2d209-107">*ConversionStatus* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2d209-108">Type : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="2d209-108">Type: **uint32**</span></span>

<span data-ttu-id="2d209-109">État de chiffrement ou de déchiffrement du volume.</span><span class="sxs-lookup"><span data-stu-id="2d209-109">Volume encryption or decryption status.</span></span> <span data-ttu-id="2d209-110">Il peut s’agir de l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="2d209-110">This can be one of the following values.</span></span>



| <span data-ttu-id="2d209-111">Valeur</span><span class="sxs-lookup"><span data-stu-id="2d209-111">Value</span></span>                                                                                                                                                                                                                                                                           | <span data-ttu-id="2d209-112">Signification</span><span class="sxs-lookup"><span data-stu-id="2d209-112">Meaning</span></span>                                                                                                                                                                   |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="FullyDecrypted"></span><span id="fullydecrypted"></span><span id="FULLYDECRYPTED"></span><dl> <span data-ttu-id="2d209-113"><dt>**FullyDecrypted**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="2d209-113"><dt>**FullyDecrypted**</dt> <dt>0</dt></span></span> </dl>                         | <span data-ttu-id="2d209-114">Pour un disque dur standard (HDD), le volume est entièrement déchiffré.</span><span class="sxs-lookup"><span data-stu-id="2d209-114">For a standard hard drive (HDD), the volume is fully decrypted.</span></span><br/> <span data-ttu-id="2d209-115">Pour un disque dur chiffré (EHDD) matériel, le volume est déverrouillé de façon permanente.</span><span class="sxs-lookup"><span data-stu-id="2d209-115">For a hardware encrypted hard drive (EHDD), the volume is perpetually unlocked.</span></span><br/>     |
| <span id="FullyEncrypted"></span><span id="fullyencrypted"></span><span id="FULLYENCRYPTED"></span><dl> <span data-ttu-id="2d209-116"><dt>**FullyEncrypted**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="2d209-116"><dt>**FullyEncrypted**</dt> <dt>1</dt></span></span> </dl>                         | <span data-ttu-id="2d209-117">Pour un disque dur standard (HDD), le volume est entièrement chiffré.</span><span class="sxs-lookup"><span data-stu-id="2d209-117">For a standard hard drive (HDD), the volume is fully encrypted.</span></span><br/> <span data-ttu-id="2d209-118">Pour un disque dur chiffré (EHDD) matériel, le volume n’est pas déverrouillé de façon permanente.</span><span class="sxs-lookup"><span data-stu-id="2d209-118">For a hardware encrypted hard drive (EHDD), the volume is not perpetually unlocked.</span></span><br/> |
| <span id="EncryptionInProgress"></span><span id="encryptioninprogress"></span><span id="ENCRYPTIONINPROGRESS"></span><dl> <span data-ttu-id="2d209-119"><dt>**EncryptionInProgress**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="2d209-119"><dt>**EncryptionInProgress**</dt> <dt>2</dt></span></span> </dl> | <span data-ttu-id="2d209-120">Le volume est partiellement chiffré.</span><span class="sxs-lookup"><span data-stu-id="2d209-120">The volume is partially encrypted.</span></span><br/>                                                                                                                             |
| <span id="DecryptionInProgress"></span><span id="decryptioninprogress"></span><span id="DECRYPTIONINPROGRESS"></span><dl> <span data-ttu-id="2d209-121"><dt>**DecryptionInProgress**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="2d209-121"><dt>**DecryptionInProgress**</dt> <dt>3</dt></span></span> </dl> | <span data-ttu-id="2d209-122">Le volume est partiellement chiffré.</span><span class="sxs-lookup"><span data-stu-id="2d209-122">The volume is partially encrypted.</span></span><br/>                                                                                                                             |
| <span id="EncryptionPaused"></span><span id="encryptionpaused"></span><span id="ENCRYPTIONPAUSED"></span><dl> <span data-ttu-id="2d209-123"><dt>**EncryptionPaused**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="2d209-123"><dt>**EncryptionPaused**</dt> <dt>4</dt></span></span> </dl>                 | <span data-ttu-id="2d209-124">Le volume a été suspendu pendant la progression du chiffrement.</span><span class="sxs-lookup"><span data-stu-id="2d209-124">The volume has been paused during the encryption progress.</span></span> <span data-ttu-id="2d209-125">Le volume est partiellement chiffré.</span><span class="sxs-lookup"><span data-stu-id="2d209-125">The volume is partially encrypted.</span></span><br/>                                                                  |
| <span id="DecryptionPaused"></span><span id="decryptionpaused"></span><span id="DECRYPTIONPAUSED"></span><dl> <span data-ttu-id="2d209-126"><dt>**DecryptionPaused**</dt> <dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="2d209-126"><dt>**DecryptionPaused**</dt> <dt>5</dt></span></span> </dl>                 | <span data-ttu-id="2d209-127">Le volume a été suspendu pendant la progression du déchiffrement.</span><span class="sxs-lookup"><span data-stu-id="2d209-127">The volume has been paused during the decryption progress.</span></span> <span data-ttu-id="2d209-128">Le volume est partiellement chiffré.</span><span class="sxs-lookup"><span data-stu-id="2d209-128">The volume is partially encrypted.</span></span><br/>                                                                  |



 

</dd> <dt>

<span data-ttu-id="2d209-129">*EncryptionPercentage* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="2d209-129">*EncryptionPercentage* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2d209-130">Type : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="2d209-130">Type: **uint32**</span></span>

<span data-ttu-id="2d209-131">Pourcentage du volume chiffré.</span><span class="sxs-lookup"><span data-stu-id="2d209-131">Percentage of the volume that is encrypted.</span></span> <span data-ttu-id="2d209-132">Il s’agit d’un entier compris entre 0 et 100 inclus.</span><span class="sxs-lookup"><span data-stu-id="2d209-132">This is an integer from 0 to 100 inclusive.</span></span>

<span data-ttu-id="2d209-133">En raison de l’arrondi des nombres, un pourcentage de chiffrement de 0 ou de 100 n’indique pas nécessairement que le disque est entièrement déchiffré ou entièrement chiffré.</span><span class="sxs-lookup"><span data-stu-id="2d209-133">Due to rounding of numbers, an encryption percentage of 0 or 100 does not necessarily indicate that the disk is fully decrypted or fully encrypted.</span></span> <span data-ttu-id="2d209-134">Utilisez toujours *ConversionStatus* pour déterminer si le disque est en fait entièrement déchiffré ou entièrement chiffré.</span><span class="sxs-lookup"><span data-stu-id="2d209-134">Always use *ConversionStatus* to determine whether the disk is in fact fully decrypted or fully encrypted.</span></span>

</dd> <dt>

<span data-ttu-id="2d209-135">*EncryptionFlags* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="2d209-135">*EncryptionFlags* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2d209-136">Type : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="2d209-136">Type: **uint32**</span></span>

<span data-ttu-id="2d209-137">Indicateurs qui décrivent le comportement de chiffrement.</span><span class="sxs-lookup"><span data-stu-id="2d209-137">Flags that describe the encryption behavior.</span></span>

<span data-ttu-id="2d209-138">Combinaison de 32 bits avec les bits suivants actuellement définis.</span><span class="sxs-lookup"><span data-stu-id="2d209-138">A combination of 32 bits with following bits currently defined.</span></span>



| <span data-ttu-id="2d209-139">Valeur</span><span class="sxs-lookup"><span data-stu-id="2d209-139">Value</span></span>                                                                                  | <span data-ttu-id="2d209-140">Signification</span><span class="sxs-lookup"><span data-stu-id="2d209-140">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
|----------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="2d209-141"><dt>0x00000001</dt></span><span class="sxs-lookup"><span data-stu-id="2d209-141"><dt>0x00000001</dt></span></span> </dl>  | <span data-ttu-id="2d209-142">Effectuez le chiffrement du volume en mode de chiffrement de données uniquement lors du démarrage du nouveau processus de chiffrement.</span><span class="sxs-lookup"><span data-stu-id="2d209-142">Perform volume encryption in data-only encryption mode when starting new encryption process.</span></span> <span data-ttu-id="2d209-143">Si le chiffrement a été suspendu ou arrêté, l’appel de la méthode [**Encrypt**](encrypt-win32-encryptablevolume.md) reprend efficacement la conversion et la valeur de ce bit est ignorée.</span><span class="sxs-lookup"><span data-stu-id="2d209-143">If encryption has been paused or stopped, calling the [**Encrypt**](encrypt-win32-encryptablevolume.md) method effectively resumes conversion and the value of this bit is ignored.</span></span> <span data-ttu-id="2d209-144">Ce bit n’a d’effet que lorsque les méthodes **Encrypt** ou [**EncryptAfterHardwareTest**](encryptafterhardwaretest-win32-encryptablevolume.md) démarrent le chiffrement à partir de l’état de déchiffrement intégral, du déchiffrement en cours ou de l’état de déchiffrement suspendu.</span><span class="sxs-lookup"><span data-stu-id="2d209-144">This bit only has effect when either the **Encrypt** or [**EncryptAfterHardwareTest**](encryptafterhardwaretest-win32-encryptablevolume.md) methods start encryption from the fully decrypted state, decryption in progress state, or decryption paused state.</span></span> <span data-ttu-id="2d209-145">Si ce bit est égal à zéro, ce qui signifie qu’il n’est pas défini lors du démarrage du nouveau processus de chiffrement, la conversion en mode complet est effectuée.</span><span class="sxs-lookup"><span data-stu-id="2d209-145">If this bit is zero, meaning that it is not set, when starting new encryption process, then full mode conversion will be performed.</span></span><br/> |
| <dl> <span data-ttu-id="2d209-146"><dt>0x00000002</dt></span><span class="sxs-lookup"><span data-stu-id="2d209-146"><dt>0x00000002</dt></span></span> </dl>  | <span data-ttu-id="2d209-147">Effectuez une réinitialisation à la demande de l’espace libre du volume.</span><span class="sxs-lookup"><span data-stu-id="2d209-147">Perform on-demand wipe of the volume free space.</span></span> <span data-ttu-id="2d209-148">L’appel de la méthode [**Encrypt**](encrypt-win32-encryptablevolume.md) avec cet ensemble de bits est autorisé uniquement lorsque le volume n’est pas en cours de conversion ou d’effacement et est dans un État « chiffré ».</span><span class="sxs-lookup"><span data-stu-id="2d209-148">Calling the [**Encrypt**](encrypt-win32-encryptablevolume.md) method with this bit set is only allowed when volume is not currently converting or wiping and is in an "encrypted" state.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| <dl> <span data-ttu-id="2d209-149"><dt>0x00010000 </dt></span><span class="sxs-lookup"><span data-stu-id="2d209-149"><dt>0x00010000 </dt></span></span> </dl> | <span data-ttu-id="2d209-150">Effectuez l’opération demandée de façon synchrone.</span><span class="sxs-lookup"><span data-stu-id="2d209-150">Perform the requested operation synchronously.</span></span> <span data-ttu-id="2d209-151">L’appel sera bloqué jusqu’à ce que l’opération demandée soit terminée ou ait été interrompue.</span><span class="sxs-lookup"><span data-stu-id="2d209-151">The call will block until requested operation has completed or was interrupted.</span></span> <span data-ttu-id="2d209-152">Cet indicateur est pris en charge uniquement avec la méthode [**Encrypt**](encrypt-win32-encryptablevolume.md) .</span><span class="sxs-lookup"><span data-stu-id="2d209-152">This flag is only supported with the [**Encrypt**](encrypt-win32-encryptablevolume.md) method.</span></span> <span data-ttu-id="2d209-153">Cet indicateur peut être spécifié lorsque l’option **Encrypt** est appelée pour reprendre le chiffrement ou l’effacement arrêté ou interrompu ou lorsque le chiffrement ou l’effacement est en cours.</span><span class="sxs-lookup"><span data-stu-id="2d209-153">This flag can be specified when **Encrypt** is called to resume stopped or interrupted encryption or wiping or when either encryption or wiping is in progress.</span></span> <span data-ttu-id="2d209-154">Cela permet à l’appelant de reprendre en mode synchrone l’attente jusqu’à ce que le processus soit terminé ou interrompu.</span><span class="sxs-lookup"><span data-stu-id="2d209-154">This allows the caller to resume synchronously waiting until the process is completed or interrupted.</span></span><br/>                                                                                                                                                                                  |



 

</dd> <dt>

<span data-ttu-id="2d209-155">*WipingStatus* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="2d209-155">*WipingStatus* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2d209-156">Type : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="2d209-156">Type: **uint32**</span></span>

<span data-ttu-id="2d209-157">État d’effacement de l’espace libre.</span><span class="sxs-lookup"><span data-stu-id="2d209-157">Free space wiping status.</span></span> <span data-ttu-id="2d209-158">Il peut s’agir de l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="2d209-158">This can be one of the following values.</span></span>



| <span data-ttu-id="2d209-159">Valeur</span><span class="sxs-lookup"><span data-stu-id="2d209-159">Value</span></span>                                                                                                                                                                                                                                                                                               | <span data-ttu-id="2d209-160">Signification</span><span class="sxs-lookup"><span data-stu-id="2d209-160">Meaning</span></span>                                                |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------|
| <span id="FreeSpaceNotWiped"></span><span id="freespacenotwiped"></span><span id="FREESPACENOTWIPED"></span><dl> <span data-ttu-id="2d209-161"><dt>**FreeSpaceNotWiped**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="2d209-161"><dt>**FreeSpaceNotWiped**</dt> <dt>0</dt></span></span> </dl>                                 | <span data-ttu-id="2d209-162">L’espace libre n’a pas été réinitialisé.</span><span class="sxs-lookup"><span data-stu-id="2d209-162">The free space has not been wiped.</span></span><br/>          |
| <span id="FreeSpaceWiped"></span><span id="freespacewiped"></span><span id="FREESPACEWIPED"></span><dl> <span data-ttu-id="2d209-163"><dt>**FreeSpaceWiped**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="2d209-163"><dt>**FreeSpaceWiped**</dt> <dt>1</dt></span></span> </dl>                                             | <span data-ttu-id="2d209-164">L’espace libre a été réinitialisé.</span><span class="sxs-lookup"><span data-stu-id="2d209-164">The free space has been wiped.</span></span><br/>              |
| <span id="FreeSpaceWipingInProgress"></span><span id="freespacewipinginprogress"></span><span id="FREESPACEWIPINGINPROGRESS"></span><dl> <span data-ttu-id="2d209-165"><dt>**FreeSpaceWipingInProgress**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="2d209-165"><dt>**FreeSpaceWipingInProgress**</dt> <dt>2</dt></span></span> </dl> | <span data-ttu-id="2d209-166">L’effacement de l’espace libre est actuellement en cours.</span><span class="sxs-lookup"><span data-stu-id="2d209-166">Free space wiping is currently in progress.</span></span><br/> |
| <span id="FreeSpaceWipingPaused"></span><span id="freespacewipingpaused"></span><span id="FREESPACEWIPINGPAUSED"></span><dl> <span data-ttu-id="2d209-167"><dt>**FreeSpaceWipingPaused**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="2d209-167"><dt>**FreeSpaceWipingPaused**</dt> <dt>3</dt></span></span> </dl>                 | <span data-ttu-id="2d209-168">L’effacement de l’espace libre a été suspendu.</span><span class="sxs-lookup"><span data-stu-id="2d209-168">Free space wiping has been paused.</span></span><br/>          |



 

</dd> <dt>

<span data-ttu-id="2d209-169">*WipingPercentage* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="2d209-169">*WipingPercentage* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2d209-170">Type : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="2d209-170">Type: **uint32**</span></span>

<span data-ttu-id="2d209-171">Valeur comprise entre 0 et 100 qui spécifie le pourcentage d’espace libre qui a été réinitialisé.</span><span class="sxs-lookup"><span data-stu-id="2d209-171">A value from 0 to 100 that specifies the percentage of free space that has been wiped.</span></span>

</dd> <dt>

<span data-ttu-id="2d209-172">*PrecisionFactor* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="2d209-172">*PrecisionFactor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2d209-173">Type : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="2d209-173">Type: **uint32**</span></span>

<span data-ttu-id="2d209-174">Valeur comprise entre 0 et 4 qui spécifie le niveau de précision.</span><span class="sxs-lookup"><span data-stu-id="2d209-174">A value from 0 to 4 that specifies the precision level</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2d209-175">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="2d209-175">Return value</span></span>

<span data-ttu-id="2d209-176">Type : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="2d209-176">Type: **uint32**</span></span>

<span data-ttu-id="2d209-177">Cette méthode retourne l’un des codes suivants, ou un autre code d’erreur en cas d’échec.</span><span class="sxs-lookup"><span data-stu-id="2d209-177">This method returns one of the following codes or another error code if it fails.</span></span>



| <span data-ttu-id="2d209-178">Code/valeur de retour</span><span class="sxs-lookup"><span data-stu-id="2d209-178">Return code/value</span></span>                                                                                                                                                                  | <span data-ttu-id="2d209-179">Description</span><span class="sxs-lookup"><span data-stu-id="2d209-179">Description</span></span>                           |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <span data-ttu-id="2d209-180"><dt>**S \_ OK**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="2d209-180"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl>                                  | <span data-ttu-id="2d209-181">La méthode a réussi.</span><span class="sxs-lookup"><span data-stu-id="2d209-181">The method was successful.</span></span><br/> |
| <dl> <span data-ttu-id="2d209-182"><dt>**FVE \_ E \_ Locked \_ volume**</dt> <dt>2150694912 (0x80310000)</dt></span><span class="sxs-lookup"><span data-stu-id="2d209-182"><dt>**FVE\_E\_LOCKED\_VOLUME**</dt> <dt>2150694912 (0x80310000)</dt></span></span> </dl> | <span data-ttu-id="2d209-183">Le volume est verrouillé.</span><span class="sxs-lookup"><span data-stu-id="2d209-183">The volume is locked.</span></span><br/>      |



 

## <a name="remarks"></a><span data-ttu-id="2d209-184">Notes</span><span class="sxs-lookup"><span data-stu-id="2d209-184">Remarks</span></span>

<span data-ttu-id="2d209-185">Les fichiers format MOF (MOF) contiennent les définitions des classes Windows Management Instrumentation (WMI).</span><span class="sxs-lookup"><span data-stu-id="2d209-185">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="2d209-186">Les fichiers MOF ne sont pas installés dans le cadre de la SDK Windows.</span><span class="sxs-lookup"><span data-stu-id="2d209-186">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="2d209-187">Ils sont installés sur le serveur lorsque vous ajoutez le rôle associé à l’aide de l’Gestionnaire de serveur.</span><span class="sxs-lookup"><span data-stu-id="2d209-187">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="2d209-188">Pour plus d’informations sur les fichiers MOF, consultez [format MOF (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="2d209-188">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="2d209-189">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="2d209-189">Requirements</span></span>



| <span data-ttu-id="2d209-190">Condition requise</span><span class="sxs-lookup"><span data-stu-id="2d209-190">Requirement</span></span> | <span data-ttu-id="2d209-191">Valeur</span><span class="sxs-lookup"><span data-stu-id="2d209-191">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2d209-192">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2d209-192">Minimum supported client</span></span><br/> | <span data-ttu-id="2d209-193">Windows Vista entreprise, les applications de bureau Windows Vista Édition intégrale \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="2d209-193">Windows Vista Enterprise, Windows Vista Ultimate \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="2d209-194">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2d209-194">Minimum supported server</span></span><br/> | <span data-ttu-id="2d209-195">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="2d209-195">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="2d209-196">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="2d209-196">Namespace</span></span><br/>                | <span data-ttu-id="2d209-197">Racine \\ de \\ sécurité cimv2 \\ MicrosoftVolumeEncryption</span><span class="sxs-lookup"><span data-stu-id="2d209-197">Root\\CIMV2\\Security\\MicrosoftVolumeEncryption</span></span><br/>                                             |
| <span data-ttu-id="2d209-198">MOF</span><span class="sxs-lookup"><span data-stu-id="2d209-198">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2d209-199"><dt>Win32 \_ encryptablevolume. mof</dt></span><span class="sxs-lookup"><span data-stu-id="2d209-199"><dt>Win32\_encryptablevolume.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2d209-200">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2d209-200">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2d209-201">**\_EncryptableVolume Win32**</span><span class="sxs-lookup"><span data-stu-id="2d209-201">**Win32\_EncryptableVolume**</span></span>](win32-encryptablevolume.md)
</dt> </dl>

 

 
