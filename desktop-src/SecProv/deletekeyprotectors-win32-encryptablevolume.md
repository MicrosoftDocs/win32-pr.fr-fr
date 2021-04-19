---
description: Supprime tous les protecteurs de clé du volume.
ms.assetid: 46f61899-87ff-4e86-8409-635117cff4de
title: Méthode DeleteKeyProtectors de la classe Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.DeleteKeyProtectors
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 0195a89884dcd9f9288cab020d9804dcc81b7977
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106524678"
---
# <a name="deletekeyprotectors-method-of-the-win32_encryptablevolume-class"></a><span data-ttu-id="7b398-103">Méthode DeleteKeyProtectors de la \_ classe Win32 EncryptableVolume</span><span class="sxs-lookup"><span data-stu-id="7b398-103">DeleteKeyProtectors method of the Win32\_EncryptableVolume class</span></span>

<span data-ttu-id="7b398-104">La méthode **DeleteKeyProtectors** de la classe [**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md) supprime tous les protecteurs de clé du volume.</span><span class="sxs-lookup"><span data-stu-id="7b398-104">The **DeleteKeyProtectors** method of the [**Win32\_EncryptableVolume**](win32-encryptablevolume.md) class deletes all key protectors for the volume.</span></span>

<span data-ttu-id="7b398-105">Si un volume non chiffré possède des protecteurs de clés, lorsque **DeleteKeyProtectors** est exécuté correctement, le volume revient à un système de fichiers NTFS standard.</span><span class="sxs-lookup"><span data-stu-id="7b398-105">If an unencrypted volume has key protectors, when **DeleteKeyProtectors** is run successfully the volume reverts to a standard NTFS file system.</span></span>

<span data-ttu-id="7b398-106">Si le volume n’est pas encore complètement déchiffré, utilisez [**DisableKeyProtectors**](disablekeyprotectors-win32-encryptablevolume.md) avant d’exécuter **DeleteKeyProtectors** pour vous assurer que les parties chiffrées du volume restent accessibles.</span><span class="sxs-lookup"><span data-stu-id="7b398-106">If the volume is not yet fully decrypted, use [**DisableKeyProtectors**](disablekeyprotectors-win32-encryptablevolume.md) before running **DeleteKeyProtectors** to ensure that encrypted portions of the volume remain accessible.</span></span>

## <a name="syntax"></a><span data-ttu-id="7b398-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7b398-107">Syntax</span></span>


```mof
uint32 DeleteKeyProtectors();
```



## <a name="parameters"></a><span data-ttu-id="7b398-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="7b398-108">Parameters</span></span>

<span data-ttu-id="7b398-109">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="7b398-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="7b398-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="7b398-110">Return value</span></span>

<span data-ttu-id="7b398-111">Type : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="7b398-111">Type: **uint32**</span></span>

<span data-ttu-id="7b398-112">Cette méthode retourne l’un des codes suivants, ou un autre code d’erreur en cas d’échec.</span><span class="sxs-lookup"><span data-stu-id="7b398-112">This method returns one of the following codes or another error code if it fails.</span></span>



| <span data-ttu-id="7b398-113">Code/valeur de retour</span><span class="sxs-lookup"><span data-stu-id="7b398-113">Return code/value</span></span>                                                                                                                                                                          | <span data-ttu-id="7b398-114">Description</span><span class="sxs-lookup"><span data-stu-id="7b398-114">Description</span></span>                                                                                                                                                                                                                                                                                                               |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="7b398-115"><dt>**S \_ OK**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="7b398-115"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl>                                          | <span data-ttu-id="7b398-116">La méthode a réussi.</span><span class="sxs-lookup"><span data-stu-id="7b398-116">The method was successful.</span></span><br/>                                                                                                                                                                                                                                                                                     |
| <dl> <span data-ttu-id="7b398-117"><dt>**FVE \_ E \_ Locked \_ volume**</dt> <dt>2150694912 (0x80310000)</dt></span><span class="sxs-lookup"><span data-stu-id="7b398-117"><dt>**FVE\_E\_LOCKED\_VOLUME**</dt> <dt>2150694912 (0x80310000)</dt></span></span> </dl>         | <span data-ttu-id="7b398-118">Le volume est verrouillé.</span><span class="sxs-lookup"><span data-stu-id="7b398-118">The volume is locked.</span></span><br/>                                                                                                                                                                                                                                                                                          |
| <dl> <span data-ttu-id="7b398-119"><dt>**FVE \_ \_Clé E \_ requise**</dt> <dt>2150694941 (0x8031001D)</dt></span><span class="sxs-lookup"><span data-stu-id="7b398-119"><dt>**FVE\_E\_KEY\_REQUIRED**</dt> <dt>2150694941 (0x8031001D)</dt></span></span> </dl>          | <span data-ttu-id="7b398-120">Le dernier protecteur de clé pour un volume partiellement ou entièrement chiffré ne peut pas être supprimé si les protecteurs de clé sont activés.</span><span class="sxs-lookup"><span data-stu-id="7b398-120">The last key protector for a partially or fully encrypted volume cannot be removed if key protectors are enabled.</span></span> <span data-ttu-id="7b398-121">Utilisez [**DisableKeyProtectors**](disablekeyprotectors-win32-encryptablevolume.md) avant de supprimer ce dernier protecteur de clé pour vous assurer que les parties chiffrées du volume restent accessibles.</span><span class="sxs-lookup"><span data-stu-id="7b398-121">Use [**DisableKeyProtectors**](disablekeyprotectors-win32-encryptablevolume.md) before removing this last key protector to ensure that encrypted portions of the volume remain accessible.</span></span> <br/> |
| <dl> <span data-ttu-id="7b398-122"><dt>**FVE \_ \_Limite de volume E \_ \_ déjà**</dt> <dt>2150694943 (0x8031001F)</dt></span><span class="sxs-lookup"><span data-stu-id="7b398-122"><dt>**FVE\_E\_VOLUME\_BOUND\_ALREADY**</dt> <dt>2150694943 (0x8031001F)</dt></span></span> </dl> | <span data-ttu-id="7b398-123">Les protecteurs de clé ne peuvent pas être supprimés, car l’un d’eux est utilisé pour déverrouiller automatiquement le volume.</span><span class="sxs-lookup"><span data-stu-id="7b398-123">Key protectors cannot be deleted because one of them is being used to automatically unlock the volume.</span></span> <br/> <span data-ttu-id="7b398-124">Utilisez [**DisableAutoUnlock**](disableautounlock-win32-encryptablevolume.md) pour désactiver le déverrouillage automatique avant d’exécuter cette méthode.</span><span class="sxs-lookup"><span data-stu-id="7b398-124">Use [**DisableAutoUnlock**](disableautounlock-win32-encryptablevolume.md) to disable automatic unlocking before running this method.</span></span><br/>                                                       |



 

## <a name="remarks"></a><span data-ttu-id="7b398-125">Notes</span><span class="sxs-lookup"><span data-stu-id="7b398-125">Remarks</span></span>

<span data-ttu-id="7b398-126">Les fichiers format MOF (MOF) contiennent les définitions des classes Windows Management Instrumentation (WMI).</span><span class="sxs-lookup"><span data-stu-id="7b398-126">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="7b398-127">Les fichiers MOF ne sont pas installés dans le cadre de la SDK Windows.</span><span class="sxs-lookup"><span data-stu-id="7b398-127">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="7b398-128">Ils sont installés sur le serveur lorsque vous ajoutez le rôle associé à l’aide de l’Gestionnaire de serveur.</span><span class="sxs-lookup"><span data-stu-id="7b398-128">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="7b398-129">Pour plus d’informations sur les fichiers MOF, consultez [format MOF (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="7b398-129">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="7b398-130">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7b398-130">Requirements</span></span>



| <span data-ttu-id="7b398-131">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7b398-131">Requirement</span></span> | <span data-ttu-id="7b398-132">Valeur</span><span class="sxs-lookup"><span data-stu-id="7b398-132">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7b398-133">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7b398-133">Minimum supported client</span></span><br/> | <span data-ttu-id="7b398-134">Windows Vista entreprise, les applications de bureau Windows Vista Édition intégrale \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="7b398-134">Windows Vista Enterprise, Windows Vista Ultimate \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="7b398-135">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7b398-135">Minimum supported server</span></span><br/> | <span data-ttu-id="7b398-136">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="7b398-136">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="7b398-137">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="7b398-137">Namespace</span></span><br/>                | <span data-ttu-id="7b398-138">Racine \\ de \\ sécurité cimv2 \\ MicrosoftVolumeEncryption</span><span class="sxs-lookup"><span data-stu-id="7b398-138">Root\\CIMV2\\Security\\MicrosoftVolumeEncryption</span></span><br/>                                             |
| <span data-ttu-id="7b398-139">MOF</span><span class="sxs-lookup"><span data-stu-id="7b398-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="7b398-140"><dt>Win32 \_ encryptablevolume. mof</dt></span><span class="sxs-lookup"><span data-stu-id="7b398-140"><dt>Win32\_encryptablevolume.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7b398-141">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7b398-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7b398-142">**\_EncryptableVolume Win32**</span><span class="sxs-lookup"><span data-stu-id="7b398-142">**Win32\_EncryptableVolume**</span></span>](win32-encryptablevolume.md)
</dt> </dl>

 

 
