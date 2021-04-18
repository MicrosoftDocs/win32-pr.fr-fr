---
description: Indique si le volume est automatiquement déverrouillé lorsqu’il est monté.
ms.assetid: cba04d77-1e7c-4191-8eb7-b8c43694193f
title: Méthode IsAutoUnlockEnabled de la classe Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.IsAutoUnlockEnabled
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 2a144d54ff4564fa322efadd521e44c2fa9a8173
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106512947"
---
# <a name="isautounlockenabled-method-of-the-win32_encryptablevolume-class"></a><span data-ttu-id="fffe7-103">Méthode IsAutoUnlockEnabled de la \_ classe Win32 EncryptableVolume</span><span class="sxs-lookup"><span data-stu-id="fffe7-103">IsAutoUnlockEnabled method of the Win32\_EncryptableVolume class</span></span>

<span data-ttu-id="fffe7-104">La méthode **IsAutoUnlockEnabled** de la [**classe \_ EncryptableVolume Win32**](win32-encryptablevolume.md) indique si le volume est automatiquement déverrouillé lorsqu’il est monté (par exemple, lorsque des périphériques mémoire amovibles sont connectés à l’ordinateur).</span><span class="sxs-lookup"><span data-stu-id="fffe7-104">The **IsAutoUnlockEnabled** method of the [**Win32\_EncryptableVolume**](win32-encryptablevolume.md) class indicates whether the volume is automatically unlocked when it is mounted (for example, when removable memory devices are connected to the computer).</span></span>

## <a name="syntax"></a><span data-ttu-id="fffe7-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="fffe7-105">Syntax</span></span>


```mof
uint32 IsAutoUnlockEnabled(
  [out] boolean IsAutoUnlockEnabled,
  [out] string  VolumeKeyProtectorID
);
```



## <a name="parameters"></a><span data-ttu-id="fffe7-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="fffe7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fffe7-107">*IsAutoUnlockEnabled* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="fffe7-107">*IsAutoUnlockEnabled* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="fffe7-108">Type : **booléen**</span><span class="sxs-lookup"><span data-stu-id="fffe7-108">Type: **boolean**</span></span>

<span data-ttu-id="fffe7-109">Valeur booléenne qui est true si la clé externe utilisée pour déverrouiller automatiquement le volume existe et a été stockée dans le volume du système d’exploitation en cours d’exécution, sinon elle est false.</span><span class="sxs-lookup"><span data-stu-id="fffe7-109">A Boolean value that is true if the external key used to automatically unlock the volume exists and has been stored in the currently running operating system volume, otherwise it is false.</span></span>

</dd> <dt>

<span data-ttu-id="fffe7-110">*VolumeKeyProtectorID* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="fffe7-110">*VolumeKeyProtectorID* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="fffe7-111">Type : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="fffe7-111">Type: **string**</span></span>

<span data-ttu-id="fffe7-112">Identificateur de chaîne unique qui contient l’ID de protecteur de clé de volume chiffré associé si *IsAutoUnlockEnabled* a la valeur true.</span><span class="sxs-lookup"><span data-stu-id="fffe7-112">A unique string identifier that contains the associated encrypted volume key protector ID if *IsAutoUnlockEnabled* is true.</span></span>

<span data-ttu-id="fffe7-113">Si *IsAutoUnlockEnabled* a la valeur false, *VolumeKeyProtectorID* est une chaîne vide.</span><span class="sxs-lookup"><span data-stu-id="fffe7-113">If *IsAutoUnlockEnabled* is false, *VolumeKeyProtectorID* is an empty string.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fffe7-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="fffe7-114">Return value</span></span>

<span data-ttu-id="fffe7-115">Type : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="fffe7-115">Type: **uint32**</span></span>

<span data-ttu-id="fffe7-116">Cette méthode retourne l’un des codes suivants, ou un autre code d’erreur en cas d’échec.</span><span class="sxs-lookup"><span data-stu-id="fffe7-116">This method returns one of the following codes or another error code if it fails.</span></span>



| <span data-ttu-id="fffe7-117">Code/valeur de retour</span><span class="sxs-lookup"><span data-stu-id="fffe7-117">Return code/value</span></span>                                                                                                                                                                     | <span data-ttu-id="fffe7-118">Description</span><span class="sxs-lookup"><span data-stu-id="fffe7-118">Description</span></span>                                                                                 |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="fffe7-119"><dt>**S \_ OK**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="fffe7-119"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl>                                     | <span data-ttu-id="fffe7-120">La méthode a réussi.</span><span class="sxs-lookup"><span data-stu-id="fffe7-120">The method was successful.</span></span><br/>                                                       |
| <dl> <span data-ttu-id="fffe7-121"><dt>**FVE \_ E \_ non \_ activée**</dt> <dt>2150694920 (0x80310008)</dt></span><span class="sxs-lookup"><span data-stu-id="fffe7-121"><dt>**FVE\_E\_NOT\_ACTIVATED**</dt> <dt>2150694920 (0x80310008)</dt></span></span> </dl>    | <span data-ttu-id="fffe7-122">BitLocker n’est pas activé sur le volume.</span><span class="sxs-lookup"><span data-stu-id="fffe7-122">BitLocker is not enabled on the volume.</span></span> <span data-ttu-id="fffe7-123">Ajoutez un protecteur de clé pour activer BitLocker.</span><span class="sxs-lookup"><span data-stu-id="fffe7-123">Add a key protector to enable BitLocker.</span></span><br/> |
| <dl> <span data-ttu-id="fffe7-124"><dt>**FVE \_ E \_ non \_ \_ VOLUME de données**</dt> <dt>2150694937 (0x80310019)</dt></span><span class="sxs-lookup"><span data-stu-id="fffe7-124"><dt>**FVE\_E\_NOT\_DATA\_VOLUME**</dt> <dt>2150694937 (0x80310019)</dt></span></span> </dl> | <span data-ttu-id="fffe7-125">La méthode ne peut pas être exécutée pour le volume du système d’exploitation en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="fffe7-125">The method cannot be run for the currently running operating system volume.</span></span><br/>      |



 

## <a name="remarks"></a><span data-ttu-id="fffe7-126">Notes</span><span class="sxs-lookup"><span data-stu-id="fffe7-126">Remarks</span></span>

<span data-ttu-id="fffe7-127">Les fichiers format MOF (MOF) contiennent les définitions des classes Windows Management Instrumentation (WMI).</span><span class="sxs-lookup"><span data-stu-id="fffe7-127">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="fffe7-128">Les fichiers MOF ne sont pas installés dans le cadre de la SDK Windows.</span><span class="sxs-lookup"><span data-stu-id="fffe7-128">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="fffe7-129">Ils sont installés sur le serveur lorsque vous ajoutez le rôle associé à l’aide de l’Gestionnaire de serveur.</span><span class="sxs-lookup"><span data-stu-id="fffe7-129">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="fffe7-130">Pour plus d’informations sur les fichiers MOF, consultez [format MOF (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="fffe7-130">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="fffe7-131">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="fffe7-131">Requirements</span></span>



| <span data-ttu-id="fffe7-132">Condition requise</span><span class="sxs-lookup"><span data-stu-id="fffe7-132">Requirement</span></span> | <span data-ttu-id="fffe7-133">Valeur</span><span class="sxs-lookup"><span data-stu-id="fffe7-133">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fffe7-134">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="fffe7-134">Minimum supported client</span></span><br/> | <span data-ttu-id="fffe7-135">Windows Vista entreprise, les applications de bureau Windows Vista Édition intégrale \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="fffe7-135">Windows Vista Enterprise, Windows Vista Ultimate \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="fffe7-136">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="fffe7-136">Minimum supported server</span></span><br/> | <span data-ttu-id="fffe7-137">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="fffe7-137">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="fffe7-138">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="fffe7-138">Namespace</span></span><br/>                | <span data-ttu-id="fffe7-139">Racine \\ de \\ sécurité cimv2 \\ MicrosoftVolumeEncryption</span><span class="sxs-lookup"><span data-stu-id="fffe7-139">Root\\CIMV2\\Security\\MicrosoftVolumeEncryption</span></span><br/>                                             |
| <span data-ttu-id="fffe7-140">MOF</span><span class="sxs-lookup"><span data-stu-id="fffe7-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="fffe7-141"><dt>Win32 \_ encryptablevolume. mof</dt></span><span class="sxs-lookup"><span data-stu-id="fffe7-141"><dt>Win32\_encryptablevolume.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fffe7-142">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fffe7-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fffe7-143">**\_EncryptableVolume Win32**</span><span class="sxs-lookup"><span data-stu-id="fffe7-143">**Win32\_EncryptableVolume**</span></span>](win32-encryptablevolume.md)
</dt> </dl>

 

 
