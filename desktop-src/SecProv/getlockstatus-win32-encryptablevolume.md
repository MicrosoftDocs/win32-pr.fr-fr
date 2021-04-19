---
description: Indique si le contenu du volume est accessible à partir de Windows.
ms.assetid: 54b2a41b-11c6-40ec-97fa-74996c15554e
title: Méthode GetLockStatus de la classe Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.GetLockStatus
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 3e81f77c37904f26e87f22b8e2b3b88763fe86cc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106514805"
---
# <a name="getlockstatus-method-of-the-win32_encryptablevolume-class"></a><span data-ttu-id="28f97-103">Méthode GetLockStatus de la \_ classe Win32 EncryptableVolume</span><span class="sxs-lookup"><span data-stu-id="28f97-103">GetLockStatus method of the Win32\_EncryptableVolume class</span></span>

<span data-ttu-id="28f97-104">La méthode **GetLockStatus** de la [**classe \_ EncryptableVolume Win32**](win32-encryptablevolume.md) indique si le contenu du volume est accessible à partir de Windows.</span><span class="sxs-lookup"><span data-stu-id="28f97-104">The **GetLockStatus** method of the [**Win32\_EncryptableVolume**](win32-encryptablevolume.md) class indicates whether the contents of the volume are accessible from Windows.</span></span>

## <a name="syntax"></a><span data-ttu-id="28f97-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="28f97-105">Syntax</span></span>


```mof
uint32 GetLockStatus(
  [out] uint32 LockStatus
);
```



## <a name="parameters"></a><span data-ttu-id="28f97-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="28f97-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="28f97-107">*LockStatus* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="28f97-107">*LockStatus* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="28f97-108">Type : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="28f97-108">Type: **uint32**</span></span>

<span data-ttu-id="28f97-109">Spécifie si le contenu du volume est accessible à partir de Windows.</span><span class="sxs-lookup"><span data-stu-id="28f97-109">Specifies whether the contents of the volume are accessible from Windows.</span></span>



| <span data-ttu-id="28f97-110">Valeur</span><span class="sxs-lookup"><span data-stu-id="28f97-110">Value</span></span>                                                                                                                                                                                                                           | <span data-ttu-id="28f97-111">Signification</span><span class="sxs-lookup"><span data-stu-id="28f97-111">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                               |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Unlocked"></span><span id="unlocked"></span><span id="UNLOCKED"></span><dl> <span data-ttu-id="28f97-112"><dt>**Déverrouillé**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="28f97-112"><dt>**Unlocked**</dt> <dt>0</dt></span></span> </dl> | <span data-ttu-id="28f97-113">Pour un disque dur standard :</span><span class="sxs-lookup"><span data-stu-id="28f97-113">For a standard HDD:</span></span><br/> <span data-ttu-id="28f97-114">Le contenu complet du volume est accessible.</span><span class="sxs-lookup"><span data-stu-id="28f97-114">The full contents of the volume are accessible.</span></span> <span data-ttu-id="28f97-115">Un volume déverrouillé est soit entièrement déchiffré, soit la clé de chiffrement est disponible en clair sur le disque.</span><span class="sxs-lookup"><span data-stu-id="28f97-115">An unlocked volume is either fully decrypted or has the encryption key available in the clear on disk.</span></span> <span data-ttu-id="28f97-116">Le volume contenant le système d’exploitation en cours d’exécution (par exemple, le volume Windows en cours d’exécution) est toujours accessible et ne peut pas être verrouillé.</span><span class="sxs-lookup"><span data-stu-id="28f97-116">The volume containing the current running operating system (for example, the running Windows volume) is always accessible and cannot be locked.</span></span><br/> <span data-ttu-id="28f97-117">Pour un EHDD :</span><span class="sxs-lookup"><span data-stu-id="28f97-117">For an EHDD:</span></span><br/> <span data-ttu-id="28f97-118">La bande est déverrouillée de façon perpétuelle.</span><span class="sxs-lookup"><span data-stu-id="28f97-118">The band is perpetually unlocked.</span></span><br/> |
| <span id="Locked"></span><span id="locked"></span><span id="LOCKED"></span><dl> <span data-ttu-id="28f97-119"><dt>**Verrouillé**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="28f97-119"><dt>**Locked**</dt> <dt>1</dt></span></span> </dl>         | <span data-ttu-id="28f97-120">Pour un disque dur standard :</span><span class="sxs-lookup"><span data-stu-id="28f97-120">For a standard HDD:</span></span><br/> <span data-ttu-id="28f97-121">La totalité ou une partie du contenu du volume n’est pas accessible.</span><span class="sxs-lookup"><span data-stu-id="28f97-121">All or a portion of the contents of the volume are not accessible.</span></span> <span data-ttu-id="28f97-122">Un volume verrouillé doit être partiellement ou entièrement chiffré et sa clé de chiffrement ne doit pas être disponible en clair sur le disque.</span><span class="sxs-lookup"><span data-stu-id="28f97-122">A locked volume must be partially or fully encrypted and must not have the encryption key available in the clear on disk.</span></span><br/> <span data-ttu-id="28f97-123">Pour un EHDD :</span><span class="sxs-lookup"><span data-stu-id="28f97-123">For an EHDD:</span></span><br/> <span data-ttu-id="28f97-124">La bande est déverrouillée ou verrouillée.</span><span class="sxs-lookup"><span data-stu-id="28f97-124">The band is unlocked or locked.</span></span><br/>                                                                                                             |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="28f97-125">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="28f97-125">Return value</span></span>

<span data-ttu-id="28f97-126">Type : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="28f97-126">Type: **uint32**</span></span>

<span data-ttu-id="28f97-127">Cette méthode retourne l’un des codes suivants, ou un autre code d’erreur en cas d’échec.</span><span class="sxs-lookup"><span data-stu-id="28f97-127">This method returns one of the following codes or another error code if it fails.</span></span>



| <span data-ttu-id="28f97-128">Code/valeur de retour</span><span class="sxs-lookup"><span data-stu-id="28f97-128">Return code/value</span></span>                                                                                                                                 | <span data-ttu-id="28f97-129">Description</span><span class="sxs-lookup"><span data-stu-id="28f97-129">Description</span></span>                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <span data-ttu-id="28f97-130"><dt>**S \_ OK**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="28f97-130"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl> | <span data-ttu-id="28f97-131">La méthode a réussi.</span><span class="sxs-lookup"><span data-stu-id="28f97-131">The method was successful.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="28f97-132">Notes</span><span class="sxs-lookup"><span data-stu-id="28f97-132">Remarks</span></span>

<span data-ttu-id="28f97-133">Utilisez [**UnlockWithExternalKey**](unlockwithexternalkey-win32-encryptablevolume.md) et [**UnlockWithNumericalPassword**](unlockwithnumericalpassword-win32-encryptablevolume.md) pour accéder au contenu du volume.</span><span class="sxs-lookup"><span data-stu-id="28f97-133">Use the [**UnlockWithExternalKey**](unlockwithexternalkey-win32-encryptablevolume.md) and [**UnlockWithNumericalPassword**](unlockwithnumericalpassword-win32-encryptablevolume.md) to get access to the volume contents.</span></span> <span data-ttu-id="28f97-134">Utilisez la méthode [**Lock**](lock-win32-encryptablevolume.md) pour abandonner l’accès au contenu du volume.</span><span class="sxs-lookup"><span data-stu-id="28f97-134">Use the [**Lock**](lock-win32-encryptablevolume.md) method to relinquish access to volume contents.</span></span>

<span data-ttu-id="28f97-135">Le volume qui contient le système d’exploitation en cours d’exécution est toujours accessible et ne peut pas être verrouillé.</span><span class="sxs-lookup"><span data-stu-id="28f97-135">The volume that contains the currently running operating system is always accessible and cannot be locked.</span></span>

<span data-ttu-id="28f97-136">Les fichiers format MOF (MOF) contiennent les définitions des classes Windows Management Instrumentation (WMI).</span><span class="sxs-lookup"><span data-stu-id="28f97-136">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="28f97-137">Les fichiers MOF ne sont pas installés dans le cadre de la SDK Windows.</span><span class="sxs-lookup"><span data-stu-id="28f97-137">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="28f97-138">Ils sont installés sur le serveur lorsque vous ajoutez le rôle associé à l’aide de l’Gestionnaire de serveur.</span><span class="sxs-lookup"><span data-stu-id="28f97-138">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="28f97-139">Pour plus d’informations sur les fichiers MOF, consultez [format MOF (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="28f97-139">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="28f97-140">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="28f97-140">Requirements</span></span>



| <span data-ttu-id="28f97-141">Condition requise</span><span class="sxs-lookup"><span data-stu-id="28f97-141">Requirement</span></span> | <span data-ttu-id="28f97-142">Valeur</span><span class="sxs-lookup"><span data-stu-id="28f97-142">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="28f97-143">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="28f97-143">Minimum supported client</span></span><br/> | <span data-ttu-id="28f97-144">Windows Vista entreprise, les applications de bureau Windows Vista Édition intégrale \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="28f97-144">Windows Vista Enterprise, Windows Vista Ultimate \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="28f97-145">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="28f97-145">Minimum supported server</span></span><br/> | <span data-ttu-id="28f97-146">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="28f97-146">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="28f97-147">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="28f97-147">Namespace</span></span><br/>                | <span data-ttu-id="28f97-148">Racine \\ de \\ sécurité cimv2 \\ MicrosoftVolumeEncryption</span><span class="sxs-lookup"><span data-stu-id="28f97-148">Root\\CIMV2\\Security\\MicrosoftVolumeEncryption</span></span><br/>                                             |
| <span data-ttu-id="28f97-149">MOF</span><span class="sxs-lookup"><span data-stu-id="28f97-149">MOF</span></span><br/>                      | <dl> <span data-ttu-id="28f97-150"><dt>Win32 \_ encryptablevolume. mof</dt></span><span class="sxs-lookup"><span data-stu-id="28f97-150"><dt>Win32\_encryptablevolume.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="28f97-151">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="28f97-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="28f97-152">**\_EncryptableVolume Win32**</span><span class="sxs-lookup"><span data-stu-id="28f97-152">**Win32\_EncryptableVolume**</span></span>](win32-encryptablevolume.md)
</dt> </dl>

 

 
