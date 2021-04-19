---
description: Indique si des clés externes ou des informations associées qui peuvent être utilisées pour déverrouiller automatiquement des volumes de données existent dans le volume du système d’exploitation en cours d’exécution.
ms.assetid: 37e7fe85-312d-49ff-aa6b-8c76c4fc4bba
title: Méthode IsAutoUnlockKeyStored de la classe Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.IsAutoUnlockKeyStored
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: aedb834bdfd26ce4b348a41b4046c0c4e2c7e260
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106536549"
---
# <a name="isautounlockkeystored-method-of-the-win32_encryptablevolume-class"></a><span data-ttu-id="324e5-103">Méthode IsAutoUnlockKeyStored de la \_ classe Win32 EncryptableVolume</span><span class="sxs-lookup"><span data-stu-id="324e5-103">IsAutoUnlockKeyStored method of the Win32\_EncryptableVolume class</span></span>

<span data-ttu-id="324e5-104">La méthode **IsAutoUnlockKeyStored** de la [**classe \_ EncryptableVolume Win32**](win32-encryptablevolume.md) indique si des clés externes ou des informations associées qui peuvent être utilisées pour déverrouiller automatiquement des volumes de données existent dans le volume du système d’exploitation en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="324e5-104">The **IsAutoUnlockKeyStored** method of the [**Win32\_EncryptableVolume**](win32-encryptablevolume.md) class indicates whether any external keys or related information that may be used to automatically unlock data volumes exist in the currently running operating system volume.</span></span>

## <a name="syntax"></a><span data-ttu-id="324e5-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="324e5-105">Syntax</span></span>


```mof
uint32 IsAutoUnlockKeyStored(
  [out] boolean IsAutoUnlockKeyStored
);
```



## <a name="parameters"></a><span data-ttu-id="324e5-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="324e5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="324e5-107">*IsAutoUnlockKeyStored* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="324e5-107">*IsAutoUnlockKeyStored* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="324e5-108">Type : **booléen**</span><span class="sxs-lookup"><span data-stu-id="324e5-108">Type: **boolean**</span></span>

<span data-ttu-id="324e5-109">La **valeur est true** si des informations pouvant être utilisées pour déverrouiller automatiquement des volumes de données sont stockées dans le Registre du volume du système d’exploitation en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="324e5-109">Is **true** if any information that can be used to automatically unlock data volumes is stored in the registry of the currently running operating system volume.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="324e5-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="324e5-110">Return value</span></span>

<span data-ttu-id="324e5-111">Type : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="324e5-111">Type: **uint32**</span></span>

<span data-ttu-id="324e5-112">Cette méthode retourne l’un des codes suivants, ou un autre code d’erreur en cas d’échec.</span><span class="sxs-lookup"><span data-stu-id="324e5-112">This method returns one of the following codes or another error code if it fails.</span></span>



| <span data-ttu-id="324e5-113">Code/valeur de retour</span><span class="sxs-lookup"><span data-stu-id="324e5-113">Return code/value</span></span>                                                                                                                                                                   | <span data-ttu-id="324e5-114">Description</span><span class="sxs-lookup"><span data-stu-id="324e5-114">Description</span></span>                                                                                  |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="324e5-115"><dt>**S \_ OK**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="324e5-115"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl>                                   | <span data-ttu-id="324e5-116">La méthode a réussi.</span><span class="sxs-lookup"><span data-stu-id="324e5-116">The method was successful.</span></span><br/>                                                        |
| <dl> <span data-ttu-id="324e5-117"><dt>**FVE \_ E \_ non \_ activée**</dt> <dt>2150694920 (0x80310008)</dt></span><span class="sxs-lookup"><span data-stu-id="324e5-117"><dt>**FVE\_E\_NOT\_ACTIVATED**</dt> <dt>2150694920 (0x80310008)</dt></span></span> </dl>  | <span data-ttu-id="324e5-118">BitLocker n’est pas activé sur le volume.</span><span class="sxs-lookup"><span data-stu-id="324e5-118">BitLocker is not enabled on the volume.</span></span> <span data-ttu-id="324e5-119">Ajoutez un protecteur de clé pour activer BitLocker.</span><span class="sxs-lookup"><span data-stu-id="324e5-119">Add a key protector to enable BitLocker.</span></span> <br/> |
| <dl> <span data-ttu-id="324e5-120"><dt>**FVE \_ E \_ non \_ OS \_ volume**</dt> <dt>2150694952 (0x80310028)</dt></span><span class="sxs-lookup"><span data-stu-id="324e5-120"><dt>**FVE\_E\_NOT\_OS\_VOLUME**</dt> <dt>2150694952 (0x80310028)</dt></span></span> </dl> | <span data-ttu-id="324e5-121">La méthode ne peut être exécutée que pour le volume du système d’exploitation en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="324e5-121">The method can only be run for the currently running operating system volume.</span></span><br/>     |



 

## <a name="remarks"></a><span data-ttu-id="324e5-122">Notes</span><span class="sxs-lookup"><span data-stu-id="324e5-122">Remarks</span></span>

<span data-ttu-id="324e5-123">Utilisez [**ClearAllAutoUnlockKeys**](clearallautounlockkeys-win32-encryptablevolume.md) pour supprimer toutes les informations de déverrouillage du volume du système d’exploitation en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="324e5-123">Use [**ClearAllAutoUnlockKeys**](clearallautounlockkeys-win32-encryptablevolume.md) to remove all unlocking information from the currently running operating system volume.</span></span>

<span data-ttu-id="324e5-124">Les informations utilisées pour déverrouiller un volume sont stockées lors de l’exécution de [**EnableAutoUnlock**](enableautounlock-win32-encryptablevolume.md) pour un volume de données pendant l’exécution du volume du système d’exploitation en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="324e5-124">Information used to unlock a volume is stored when [**EnableAutoUnlock**](enableautounlock-win32-encryptablevolume.md) is run for a data volume while the currently running operating system volume is running.</span></span>

<span data-ttu-id="324e5-125">**IsAutoUnlockKeyStored** diffère de [**IsAutoUnlockEnabled**](isautounlockenabled-win32-encryptablevolume.md) dans le cas où, même si le déverrouillage automatique est désactivé pour tous les volumes de données actuellement connectés à l’ordinateur, il se peut qu’il y ait toujours des informations de déverrouillage associées aux volumes de données déconnectés ou aux volumes de données qui n’existent plus.</span><span class="sxs-lookup"><span data-stu-id="324e5-125">**IsAutoUnlockKeyStored** differs from [**IsAutoUnlockEnabled**](isautounlockenabled-win32-encryptablevolume.md) in that even if automatic unlocking is disabled for all data volumes currently connected to the computer, there may still be unlocking information associated with disconnected data volumes or data volumes that no longer exist.</span></span>

<span data-ttu-id="324e5-126">Les fichiers format MOF (MOF) contiennent les définitions des classes Windows Management Instrumentation (WMI).</span><span class="sxs-lookup"><span data-stu-id="324e5-126">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="324e5-127">Les fichiers MOF ne sont pas installés dans le cadre de la SDK Windows.</span><span class="sxs-lookup"><span data-stu-id="324e5-127">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="324e5-128">Ils sont installés sur le serveur lorsque vous ajoutez le rôle associé à l’aide de l’Gestionnaire de serveur.</span><span class="sxs-lookup"><span data-stu-id="324e5-128">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="324e5-129">Pour plus d’informations sur les fichiers MOF, consultez [format MOF (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="324e5-129">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="324e5-130">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="324e5-130">Requirements</span></span>



| <span data-ttu-id="324e5-131">Condition requise</span><span class="sxs-lookup"><span data-stu-id="324e5-131">Requirement</span></span> | <span data-ttu-id="324e5-132">Valeur</span><span class="sxs-lookup"><span data-stu-id="324e5-132">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="324e5-133">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="324e5-133">Minimum supported client</span></span><br/> | <span data-ttu-id="324e5-134">Windows Vista entreprise, les applications de bureau Windows Vista Édition intégrale \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="324e5-134">Windows Vista Enterprise, Windows Vista Ultimate \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="324e5-135">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="324e5-135">Minimum supported server</span></span><br/> | <span data-ttu-id="324e5-136">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="324e5-136">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="324e5-137">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="324e5-137">Namespace</span></span><br/>                | <span data-ttu-id="324e5-138">Racine \\ de \\ sécurité cimv2 \\ MicrosoftVolumeEncryption</span><span class="sxs-lookup"><span data-stu-id="324e5-138">Root\\CIMV2\\Security\\MicrosoftVolumeEncryption</span></span><br/>                                             |
| <span data-ttu-id="324e5-139">MOF</span><span class="sxs-lookup"><span data-stu-id="324e5-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="324e5-140"><dt>Win32 \_ encryptablevolume. mof</dt></span><span class="sxs-lookup"><span data-stu-id="324e5-140"><dt>Win32\_encryptablevolume.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="324e5-141">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="324e5-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="324e5-142">**\_EncryptableVolume Win32**</span><span class="sxs-lookup"><span data-stu-id="324e5-142">**Win32\_EncryptableVolume**</span></span>](win32-encryptablevolume.md)
</dt> </dl>

 

 
