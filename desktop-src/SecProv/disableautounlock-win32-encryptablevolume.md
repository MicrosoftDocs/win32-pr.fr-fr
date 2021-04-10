---
description: Supprime la clé externe enregistrée sur le volume du système d’exploitation en cours d’exécution.
ms.assetid: a8c4bb3b-6566-4173-b550-e89740f1cba6
title: Méthode DisableAutoUnlock de la classe Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.DisableAutoUnlock
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 6dd4e11e2ff4906627c2d790987500062136d56d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103865434"
---
# <a name="disableautounlock-method-of-the-win32_encryptablevolume-class"></a><span data-ttu-id="f7398-103">Méthode DisableAutoUnlock de la \_ classe Win32 EncryptableVolume</span><span class="sxs-lookup"><span data-stu-id="f7398-103">DisableAutoUnlock method of the Win32\_EncryptableVolume class</span></span>

<span data-ttu-id="f7398-104">La méthode **DisableAutoUnlock** de la classe [**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md) supprime la clé externe enregistrée sur le volume du système d’exploitation en cours d’exécution afin qu’un volume de données ne soit pas automatiquement déverrouillé lorsqu’il est monté, par exemple lorsque des périphériques mémoire amovibles sont connectés à l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="f7398-104">The **DisableAutoUnlock** method of the [**Win32\_EncryptableVolume**](win32-encryptablevolume.md) class removes the external key saved onto the currently running operating system volume so that a data volume is not automatically unlocked when it is mounted, such as when removable memory devices are connected to the computer.</span></span>

<span data-ttu-id="f7398-105">Si le déverrouillage automatique est désactivé ou suspendu, les méthodes [**UnlockWithExternalKey**](unlockwithexternalkey-win32-encryptablevolume.md) ou [**UnlockWithNumericalPassword**](unlockwithnumericalpassword-win32-encryptablevolume.md) doivent être utilisées pour déverrouiller le volume.</span><span class="sxs-lookup"><span data-stu-id="f7398-105">If automatic unlocking is disabled or suspended, the methods [**UnlockWithExternalKey**](unlockwithexternalkey-win32-encryptablevolume.md) or [**UnlockWithNumericalPassword**](unlockwithnumericalpassword-win32-encryptablevolume.md) must be used to unlock the volume.</span></span>

## <a name="syntax"></a><span data-ttu-id="f7398-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f7398-106">Syntax</span></span>


```mof
uint32 DisableAutoUnlock();
```



## <a name="parameters"></a><span data-ttu-id="f7398-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f7398-107">Parameters</span></span>

<span data-ttu-id="f7398-108">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="f7398-108">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="f7398-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="f7398-109">Return value</span></span>

<span data-ttu-id="f7398-110">Type : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f7398-110">Type: **uint32**</span></span>

<span data-ttu-id="f7398-111">Cette méthode retourne l’un des codes suivants, ou un autre code d’erreur en cas d’échec.</span><span class="sxs-lookup"><span data-stu-id="f7398-111">This method returns one of the following codes or another error code if it fails.</span></span>



| <span data-ttu-id="f7398-112">Code/valeur de retour</span><span class="sxs-lookup"><span data-stu-id="f7398-112">Return code/value</span></span>                                                                                                                                                                       | <span data-ttu-id="f7398-113">Description</span><span class="sxs-lookup"><span data-stu-id="f7398-113">Description</span></span>                                                                                 |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="f7398-114"><dt>**S \_ OK**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="f7398-114"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl>                                       | <span data-ttu-id="f7398-115">La méthode a réussi.</span><span class="sxs-lookup"><span data-stu-id="f7398-115">The method was successful.</span></span><br/>                                                       |
| <dl> <span data-ttu-id="f7398-116"><dt> **\_ Volume FVE \_ E \_ non \_ lié**</dt> <dt>2150694935 (0x80310017)</dt></span><span class="sxs-lookup"><span data-stu-id="f7398-116"><dt>**FVE\_E\_VOLUME\_NOT\_BOUND** </dt> <dt>2150694935 (0x80310017)</dt></span></span> </dl> | <span data-ttu-id="f7398-117">Le déverrouillage automatique sur le volume est désactivé.</span><span class="sxs-lookup"><span data-stu-id="f7398-117">Automatic unlocking on the volume is disabled.</span></span><br/>                                   |
| <dl> <span data-ttu-id="f7398-118"><dt>**FVE \_ E \_ non \_ activée**</dt> <dt>2150694920 (0x80310008)</dt></span><span class="sxs-lookup"><span data-stu-id="f7398-118"><dt>**FVE\_E\_NOT\_ACTIVATED**</dt> <dt>2150694920 (0x80310008)</dt></span></span> </dl>      | <span data-ttu-id="f7398-119">BitLocker n’est pas activé sur le volume.</span><span class="sxs-lookup"><span data-stu-id="f7398-119">BitLocker is not enabled on the volume.</span></span> <span data-ttu-id="f7398-120">Ajoutez un protecteur de clé pour activer BitLocker.</span><span class="sxs-lookup"><span data-stu-id="f7398-120">Add a key protector to enable BitLocker.</span></span><br/> |
| <dl> <span data-ttu-id="f7398-121"><dt>**FVE \_ E \_ non \_ \_ VOLUME de données**</dt> <dt>2150694937 (0x80310019)</dt></span><span class="sxs-lookup"><span data-stu-id="f7398-121"><dt>**FVE\_E\_NOT\_DATA\_VOLUME**</dt> <dt>2150694937 (0x80310019)</dt></span></span> </dl>   | <span data-ttu-id="f7398-122">La méthode ne peut pas être exécutée pour le volume du système d’exploitation en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="f7398-122">The method cannot be run for the currently running operating system volume.</span></span><br/>      |



 

## <a name="remarks"></a><span data-ttu-id="f7398-123">Notes</span><span class="sxs-lookup"><span data-stu-id="f7398-123">Remarks</span></span>

<span data-ttu-id="f7398-124">Si aucune erreur n’est retournée, cette méthode supprime du Registre tous les ID de protecteur de volume et les clés externes utilisés pour déverrouiller automatiquement le volume.</span><span class="sxs-lookup"><span data-stu-id="f7398-124">If no errors are returned, this method removes from the registry any volume protector IDs and external keys used to automatically unlock the volume.</span></span>

<span data-ttu-id="f7398-125">Les fichiers format MOF (MOF) contiennent les définitions des classes Windows Management Instrumentation (WMI).</span><span class="sxs-lookup"><span data-stu-id="f7398-125">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="f7398-126">Les fichiers MOF ne sont pas installés dans le cadre de la SDK Windows.</span><span class="sxs-lookup"><span data-stu-id="f7398-126">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="f7398-127">Ils sont installés sur le serveur lorsque vous ajoutez le rôle associé à l’aide de l’Gestionnaire de serveur.</span><span class="sxs-lookup"><span data-stu-id="f7398-127">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="f7398-128">Pour plus d’informations sur les fichiers MOF, consultez [format MOF (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="f7398-128">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="f7398-129">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f7398-129">Requirements</span></span>



| <span data-ttu-id="f7398-130">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f7398-130">Requirement</span></span> | <span data-ttu-id="f7398-131">Valeur</span><span class="sxs-lookup"><span data-stu-id="f7398-131">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f7398-132">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f7398-132">Minimum supported client</span></span><br/> | <span data-ttu-id="f7398-133">Windows Vista entreprise, les applications de bureau Windows Vista Édition intégrale \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f7398-133">Windows Vista Enterprise, Windows Vista Ultimate \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="f7398-134">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f7398-134">Minimum supported server</span></span><br/> | <span data-ttu-id="f7398-135">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f7398-135">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="f7398-136">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="f7398-136">Namespace</span></span><br/>                | <span data-ttu-id="f7398-137">Racine \\ de \\ sécurité cimv2 \\ MicrosoftVolumeEncryption</span><span class="sxs-lookup"><span data-stu-id="f7398-137">Root\\CIMV2\\Security\\MicrosoftVolumeEncryption</span></span><br/>                                             |
| <span data-ttu-id="f7398-138">MOF</span><span class="sxs-lookup"><span data-stu-id="f7398-138">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f7398-139"><dt>Win32 \_ encryptablevolume. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f7398-139"><dt>Win32\_encryptablevolume.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f7398-140">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f7398-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f7398-141">**\_EncryptableVolume Win32**</span><span class="sxs-lookup"><span data-stu-id="f7398-141">**Win32\_EncryptableVolume**</span></span>](win32-encryptablevolume.md)
</dt> </dl>

 

 
