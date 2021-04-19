---
description: Désactive ou interrompt tous les protecteurs de clé associés à ce volume.
ms.assetid: 19eed858-a116-4ec8-937a-2eea7aadbdc6
title: Méthode DisableKeyProtectors de la classe Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.DisableKeyProtectors
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 1de392c50f6665d793883582e2679cd502efbe37
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106534532"
---
# <a name="disablekeyprotectors-method-of-the-win32_encryptablevolume-class"></a><span data-ttu-id="6d0fe-103">Méthode DisableKeyProtectors de la \_ classe Win32 EncryptableVolume</span><span class="sxs-lookup"><span data-stu-id="6d0fe-103">DisableKeyProtectors method of the Win32\_EncryptableVolume class</span></span>

<span data-ttu-id="6d0fe-104">La méthode **DisableKeyProtectors** de la [**classe \_ EncryptableVolume Win32**](win32-encryptablevolume.md) désactive ou interrompt tous les protecteurs de clé associés à ce volume.</span><span class="sxs-lookup"><span data-stu-id="6d0fe-104">The **DisableKeyProtectors** method of the [**Win32\_EncryptableVolume**](win32-encryptablevolume.md) class disables or suspends all key protectors associated with this volume.</span></span>

## <a name="syntax"></a><span data-ttu-id="6d0fe-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="6d0fe-105">Syntax</span></span>


```mof
uint32 DisableKeyProtectors(
  [in, optional] uint32 DisableCount
);
```



## <a name="parameters"></a><span data-ttu-id="6d0fe-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="6d0fe-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6d0fe-107">*DisableCount* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="6d0fe-107">*DisableCount* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="6d0fe-108">Type : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="6d0fe-108">Type: **uint32**</span></span>

<span data-ttu-id="6d0fe-109">Entier qui spécifie le nombre de redémarrages pour lesquels les protecteurs de clé seront désactivés.</span><span class="sxs-lookup"><span data-stu-id="6d0fe-109">Integer that specifies the number of reboots for which the key protectors will be disabled.</span></span> <span data-ttu-id="6d0fe-110">Ce paramètre est uniquement disponible sur les volumes du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="6d0fe-110">This parameter is only available on OS volumes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6d0fe-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="6d0fe-111">Return value</span></span>

<span data-ttu-id="6d0fe-112">Type : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="6d0fe-112">Type: **uint32**</span></span>

<span data-ttu-id="6d0fe-113">Cette méthode retourne l’un des codes suivants, ou un autre code d’erreur en cas d’échec.</span><span class="sxs-lookup"><span data-stu-id="6d0fe-113">This method returns one of the following codes or another error code if it fails.</span></span>



| <span data-ttu-id="6d0fe-114">Code/valeur de retour</span><span class="sxs-lookup"><span data-stu-id="6d0fe-114">Return code/value</span></span>                                                                                                                                                                  | <span data-ttu-id="6d0fe-115">Description</span><span class="sxs-lookup"><span data-stu-id="6d0fe-115">Description</span></span>                           |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <span data-ttu-id="6d0fe-116"><dt>**S \_ OK**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="6d0fe-116"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl>                                  | <span data-ttu-id="6d0fe-117">La méthode a réussi.</span><span class="sxs-lookup"><span data-stu-id="6d0fe-117">The method was successful.</span></span><br/> |
| <dl> <span data-ttu-id="6d0fe-118"><dt>**FVE \_ E \_ Locked \_ volume**</dt> <dt>2150694912 (0x80310000)</dt></span><span class="sxs-lookup"><span data-stu-id="6d0fe-118"><dt>**FVE\_E\_LOCKED\_VOLUME**</dt> <dt>2150694912 (0x80310000)</dt></span></span> </dl> | <span data-ttu-id="6d0fe-119">Le volume est verrouillé.</span><span class="sxs-lookup"><span data-stu-id="6d0fe-119">The volume is locked.</span></span><br/>      |



 

## <a name="security-considerations"></a><span data-ttu-id="6d0fe-120">Considérations relatives à la sécurité</span><span class="sxs-lookup"><span data-stu-id="6d0fe-120">Security Considerations</span></span>

<span data-ttu-id="6d0fe-121">Cette méthode expose la clé de chiffrement du volume en clair sur le disque dur, ce qui désactive toute protection du volume.</span><span class="sxs-lookup"><span data-stu-id="6d0fe-121">This method exposes the volume's encryption key in the clear on the hard disk, turning off any volume protection.</span></span> <span data-ttu-id="6d0fe-122">Nous vous recommandons de ne pas avoir de mot de passe ou de clé de chiffrement en texte clair.</span><span class="sxs-lookup"><span data-stu-id="6d0fe-122">We recommend against having any password or encryption key in plaintext.</span></span>

## <a name="remarks"></a><span data-ttu-id="6d0fe-123">Notes</span><span class="sxs-lookup"><span data-stu-id="6d0fe-123">Remarks</span></span>

<span data-ttu-id="6d0fe-124">De nouveaux protecteurs de clé peuvent être ajoutés même lorsque les protecteurs de clé sont désactivés ou suspendus.</span><span class="sxs-lookup"><span data-stu-id="6d0fe-124">New key protectors can be added even when key protectors are disabled or suspended.</span></span> <span data-ttu-id="6d0fe-125">Ces protecteurs de clé restent désactivés, sauf si [**EnableKeyProtectors**](enablekeyprotectors-win32-encryptablevolume.md) est appelé.</span><span class="sxs-lookup"><span data-stu-id="6d0fe-125">These key protectors will remain disabled unless [**EnableKeyProtectors**](enablekeyprotectors-win32-encryptablevolume.md) is called.</span></span>

<span data-ttu-id="6d0fe-126">Les fichiers format MOF (MOF) contiennent les définitions des classes Windows Management Instrumentation (WMI).</span><span class="sxs-lookup"><span data-stu-id="6d0fe-126">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="6d0fe-127">Les fichiers MOF ne sont pas installés dans le cadre de la SDK Windows.</span><span class="sxs-lookup"><span data-stu-id="6d0fe-127">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="6d0fe-128">Ils sont installés sur le serveur lorsque vous ajoutez le rôle associé à l’aide de l’Gestionnaire de serveur.</span><span class="sxs-lookup"><span data-stu-id="6d0fe-128">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="6d0fe-129">Pour plus d’informations sur les fichiers MOF, consultez [format MOF (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="6d0fe-129">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="6d0fe-130">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="6d0fe-130">Requirements</span></span>



| <span data-ttu-id="6d0fe-131">Condition requise</span><span class="sxs-lookup"><span data-stu-id="6d0fe-131">Requirement</span></span> | <span data-ttu-id="6d0fe-132">Valeur</span><span class="sxs-lookup"><span data-stu-id="6d0fe-132">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6d0fe-133">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6d0fe-133">Minimum supported client</span></span><br/> | <span data-ttu-id="6d0fe-134">Windows 8.1 les \[ applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="6d0fe-134">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="6d0fe-135">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6d0fe-135">Minimum supported server</span></span><br/> | <span data-ttu-id="6d0fe-136">Applications de bureau Windows Server 2012 R2 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="6d0fe-136">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="6d0fe-137">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="6d0fe-137">Namespace</span></span><br/>                | <span data-ttu-id="6d0fe-138">Racine \\ de \\ sécurité cimv2 \\ MicrosoftVolumeEncryption</span><span class="sxs-lookup"><span data-stu-id="6d0fe-138">Root\\CIMV2\\Security\\MicrosoftVolumeEncryption</span></span><br/>                                             |
| <span data-ttu-id="6d0fe-139">MOF</span><span class="sxs-lookup"><span data-stu-id="6d0fe-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6d0fe-140"><dt>Win32 \_ encryptablevolume. mof</dt></span><span class="sxs-lookup"><span data-stu-id="6d0fe-140"><dt>Win32\_encryptablevolume.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6d0fe-141">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6d0fe-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6d0fe-142">**\_EncryptableVolume Win32**</span><span class="sxs-lookup"><span data-stu-id="6d0fe-142">**Win32\_EncryptableVolume**</span></span>](win32-encryptablevolume.md)
</dt> <dt>

[<span data-ttu-id="6d0fe-143">**EnableKeyProtectors**</span><span class="sxs-lookup"><span data-stu-id="6d0fe-143">**EnableKeyProtectors**</span></span>](enablekeyprotectors-win32-encryptablevolume.md)
</dt> </dl>

 

 
