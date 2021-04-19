---
description: Supprime toutes les clés externes et les informations associées enregistrées sur le volume du système d’exploitation en cours d’exécution et utilisées pour déverrouiller automatiquement les volumes de données.
ms.assetid: a5fef793-0634-493d-b62d-cb842844b1e8
title: Méthode ClearAllAutoUnlockKeys de la classe Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.ClearAllAutoUnlockKeys
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: b7f7e68891865893c1444a2c5de2370799b74426
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106544642"
---
# <a name="clearallautounlockkeys-method-of-the-win32_encryptablevolume-class"></a><span data-ttu-id="8b988-103">Méthode ClearAllAutoUnlockKeys de la \_ classe Win32 EncryptableVolume</span><span class="sxs-lookup"><span data-stu-id="8b988-103">ClearAllAutoUnlockKeys method of the Win32\_EncryptableVolume class</span></span>

<span data-ttu-id="8b988-104">La méthode **ClearAllAutoUnlockKeys** de la classe [**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md) supprime toutes les clés externes et les informations associées enregistrées sur le volume du système d’exploitation en cours d’exécution et utilisées pour déverrouiller automatiquement les volumes de données.</span><span class="sxs-lookup"><span data-stu-id="8b988-104">The **ClearAllAutoUnlockKeys** method of the [**Win32\_EncryptableVolume**](win32-encryptablevolume.md) class removes all external keys and related information saved onto the currently running operating system volume that are used to automatically unlock data volumes.</span></span>

## <a name="syntax"></a><span data-ttu-id="8b988-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="8b988-105">Syntax</span></span>


```mof
uint32 ClearAllAutoUnlockKeys();
```



## <a name="parameters"></a><span data-ttu-id="8b988-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="8b988-106">Parameters</span></span>

<span data-ttu-id="8b988-107">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="8b988-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="8b988-108">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="8b988-108">Return value</span></span>

<span data-ttu-id="8b988-109">Type : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="8b988-109">Type: **uint32**</span></span>

<span data-ttu-id="8b988-110">Cette méthode retourne l’un des codes suivants, ou un autre code d’erreur en cas d’échec.</span><span class="sxs-lookup"><span data-stu-id="8b988-110">This method returns one of the following codes or another error code if it fails.</span></span>



| <span data-ttu-id="8b988-111">Code/valeur de retour</span><span class="sxs-lookup"><span data-stu-id="8b988-111">Return code/value</span></span>                                                                                                                                                                   | <span data-ttu-id="8b988-112">Description</span><span class="sxs-lookup"><span data-stu-id="8b988-112">Description</span></span>                                                                                  |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="8b988-113"><dt>**S \_ OK**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="8b988-113"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl>                                   | <span data-ttu-id="8b988-114">La méthode a réussi.</span><span class="sxs-lookup"><span data-stu-id="8b988-114">The method was successful.</span></span><br/>                                                        |
| <dl> <span data-ttu-id="8b988-115"><dt>**FVE \_ E \_ non \_ activée**</dt> <dt>2150694920 (0x80310008)</dt></span><span class="sxs-lookup"><span data-stu-id="8b988-115"><dt>**FVE\_E\_NOT\_ACTIVATED**</dt> <dt>2150694920 (0x80310008)</dt></span></span> </dl>  | <span data-ttu-id="8b988-116">BitLocker n’est pas activé sur le volume.</span><span class="sxs-lookup"><span data-stu-id="8b988-116">BitLocker is not enabled on the volume.</span></span> <span data-ttu-id="8b988-117">Ajoutez un protecteur de clé pour activer BitLocker.</span><span class="sxs-lookup"><span data-stu-id="8b988-117">Add a key protector to enable BitLocker.</span></span> <br/> |
| <dl> <span data-ttu-id="8b988-118"><dt>**FVE \_ E \_ non \_ OS \_ volume**</dt> <dt>2150694952 (0x80310028)</dt></span><span class="sxs-lookup"><span data-stu-id="8b988-118"><dt>**FVE\_E\_NOT\_OS\_VOLUME**</dt> <dt>2150694952 (0x80310028)</dt></span></span> </dl> | <span data-ttu-id="8b988-119">La méthode ne peut être exécutée que pour le volume du système d’exploitation en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="8b988-119">The method can only be run for the currently running operating system volume.</span></span><br/>     |



 

## <a name="remarks"></a><span data-ttu-id="8b988-120">Notes</span><span class="sxs-lookup"><span data-stu-id="8b988-120">Remarks</span></span>

<span data-ttu-id="8b988-121">**ClearAllAutoUnlockKeys** atteint la même fonctionnalité que l’exécution de [**DisableAutoUnlock**](disableautounlock-win32-encryptablevolume.md) pour chaque volume de données qui a été associé au système d’exploitation en cours d’exécution, même les volumes de données qui ne sont pas actuellement connectés à l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="8b988-121">**ClearAllAutoUnlockKeys** achieves the same functionality as running [**DisableAutoUnlock**](disableautounlock-win32-encryptablevolume.md) for every data volume that has ever been associated with the currently running operating system, even data volumes that are not currently connected to the computer.</span></span> <span data-ttu-id="8b988-122">Elle supprime également toutes les informations de déverrouillage obsolètes associées aux volumes de données qui n’existent plus.</span><span class="sxs-lookup"><span data-stu-id="8b988-122">It also removes any stale unlocking information associated with data volumes that no longer exist.</span></span>

<span data-ttu-id="8b988-123">Avant d’appeler le [**déchiffrement**](decrypt-win32-encryptablevolume.md) sur le volume du système d’exploitation en cours d’exécution, utilisez **ClearAllAutoUnlockKeys** pour vous assurer que les informations placées dans le Registre du système d’exploitation pour déverrouiller automatiquement les volumes de données ne sont pas accessibles en clair sur le disque.</span><span class="sxs-lookup"><span data-stu-id="8b988-123">Before calling [**Decrypt**](decrypt-win32-encryptablevolume.md) on the currently running operating system volume, use **ClearAllAutoUnlockKeys** to ensure that information placed in the operating system registry to automatically unlock data volumes is not accessible in the clear on disk.</span></span>

<span data-ttu-id="8b988-124">Une fois l’exécution de **ClearAllAutoUnlockKeys** réussie, les méthodes [**UnlockWithExternalKey**](unlockwithexternalkey-win32-encryptablevolume.md) ou [**UnlockWithNumericalPassword**](unlockwithnumericalpassword-win32-encryptablevolume.md) peuvent être utilisées pour déverrouiller tous les volumes de données de cet ordinateur.</span><span class="sxs-lookup"><span data-stu-id="8b988-124">After **ClearAllAutoUnlockKeys** runs successfully, the methods [**UnlockWithExternalKey**](unlockwithexternalkey-win32-encryptablevolume.md) or [**UnlockWithNumericalPassword**](unlockwithnumericalpassword-win32-encryptablevolume.md) can be used to unlock all data volumes on this computer.</span></span> <span data-ttu-id="8b988-125">Utilisez [**EnableAutoUnlock**](enableautounlock-win32-encryptablevolume.md) pour réactiver le déverrouillage automatique d’un volume de données.</span><span class="sxs-lookup"><span data-stu-id="8b988-125">Use [**EnableAutoUnlock**](enableautounlock-win32-encryptablevolume.md) to re-enable automatic unlocking of a data volume.</span></span>

<span data-ttu-id="8b988-126">Si aucune autre erreur n’est retournée, **ClearAllAutoUnlockKeys** supprime du Registre tous les ID de protecteur de volume et les clés externes utilisés pour déverrouiller automatiquement tout volume de données qui a déjà été associé au volume du système d’exploitation en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="8b988-126">If no other errors are returned, **ClearAllAutoUnlockKeys** removes from the registry any volume protector IDs and external keys used to automatically unlock any data volume that has ever been associated with the currently running operating system volume.</span></span>

<span data-ttu-id="8b988-127">Les fichiers format MOF (MOF) contiennent les définitions des classes Windows Management Instrumentation (WMI).</span><span class="sxs-lookup"><span data-stu-id="8b988-127">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="8b988-128">Les fichiers MOF ne sont pas installés dans le cadre de la SDK Windows.</span><span class="sxs-lookup"><span data-stu-id="8b988-128">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="8b988-129">Ils sont installés sur le serveur lorsque vous ajoutez le rôle associé à l’aide de l’Gestionnaire de serveur.</span><span class="sxs-lookup"><span data-stu-id="8b988-129">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="8b988-130">Pour plus d’informations sur les fichiers MOF, consultez [format MOF (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="8b988-130">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="8b988-131">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8b988-131">Requirements</span></span>



| <span data-ttu-id="8b988-132">Condition requise</span><span class="sxs-lookup"><span data-stu-id="8b988-132">Requirement</span></span> | <span data-ttu-id="8b988-133">Valeur</span><span class="sxs-lookup"><span data-stu-id="8b988-133">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8b988-134">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8b988-134">Minimum supported client</span></span><br/> | <span data-ttu-id="8b988-135">Windows Vista entreprise, les applications de bureau Windows Vista Édition intégrale \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="8b988-135">Windows Vista Enterprise, Windows Vista Ultimate \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="8b988-136">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8b988-136">Minimum supported server</span></span><br/> | <span data-ttu-id="8b988-137">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="8b988-137">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="8b988-138">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="8b988-138">Namespace</span></span><br/>                | <span data-ttu-id="8b988-139">Racine \\ de \\ sécurité cimv2 \\ MicrosoftVolumeEncryption</span><span class="sxs-lookup"><span data-stu-id="8b988-139">Root\\CIMV2\\Security\\MicrosoftVolumeEncryption</span></span><br/>                                             |
| <span data-ttu-id="8b988-140">MOF</span><span class="sxs-lookup"><span data-stu-id="8b988-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="8b988-141"><dt>Win32 \_ encryptablevolume. mof</dt></span><span class="sxs-lookup"><span data-stu-id="8b988-141"><dt>Win32\_encryptablevolume.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8b988-142">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8b988-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8b988-143">**\_EncryptableVolume Win32**</span><span class="sxs-lookup"><span data-stu-id="8b988-143">**Win32\_EncryptableVolume**</span></span>](win32-encryptablevolume.md)
</dt> </dl>

 

 
