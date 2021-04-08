---
description: Met à niveau un volume du format Windows Vista vers le format Windows 7.
ms.assetid: d6654e92-8176-471b-b8e5-815dd9512240
title: Méthode UpgradeVolume de la classe Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.UpgradeVolume
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 6769e8a4a480becc5a5584826f60cdb85f8b90e5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103951078"
---
# <a name="upgradevolume-method-of-the-win32_encryptablevolume-class"></a><span data-ttu-id="5f953-103">Méthode UpgradeVolume de la \_ classe Win32 EncryptableVolume</span><span class="sxs-lookup"><span data-stu-id="5f953-103">UpgradeVolume method of the Win32\_EncryptableVolume class</span></span>

<span data-ttu-id="5f953-104">La méthode **UpgradeVolume** de la classe [**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md) met à niveau un volume du format Windows Vista vers le format Windows 7.</span><span class="sxs-lookup"><span data-stu-id="5f953-104">The **UpgradeVolume** method of the [**Win32\_EncryptableVolume**](win32-encryptablevolume.md) class upgrades a volume from the Windows Vista format to the Windows 7 format.</span></span> <span data-ttu-id="5f953-105">Il s’agit d’une opération non réversible.</span><span class="sxs-lookup"><span data-stu-id="5f953-105">This is a nonreversible operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="5f953-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="5f953-106">Syntax</span></span>


```mof
uint32 UpgradeVolume();
```



## <a name="parameters"></a><span data-ttu-id="5f953-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="5f953-107">Parameters</span></span>

<span data-ttu-id="5f953-108">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="5f953-108">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="5f953-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="5f953-109">Return value</span></span>

<span data-ttu-id="5f953-110">Type : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="5f953-110">Type: **uint32**</span></span>

<span data-ttu-id="5f953-111">Cette méthode retourne l’un des codes suivants, ou un autre code d’erreur en cas d’échec.</span><span class="sxs-lookup"><span data-stu-id="5f953-111">This method returns one of the following codes or another error code if it fails.</span></span>

<span data-ttu-id="5f953-112">Si le volume est déjà déverrouillé et qu’aucune autre erreur ne se produit, cette méthode retourne zéro.</span><span class="sxs-lookup"><span data-stu-id="5f953-112">If the volume is already unlocked and no other errors occur, this method returns zero.</span></span>



| <span data-ttu-id="5f953-113">Code/valeur de retour</span><span class="sxs-lookup"><span data-stu-id="5f953-113">Return code/value</span></span>                                                                                                                                                                  | <span data-ttu-id="5f953-114">Description</span><span class="sxs-lookup"><span data-stu-id="5f953-114">Description</span></span>                                                                                  |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="5f953-115"><dt>**S \_ OK**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="5f953-115"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl>                                  | <span data-ttu-id="5f953-116">La méthode a réussi.</span><span class="sxs-lookup"><span data-stu-id="5f953-116">The method was successful.</span></span><br/>                                                        |
| <dl> <span data-ttu-id="5f953-117"><dt>**E \_ INVALIDARG**</dt> <dt>214794287 (0xCCD802F)</dt></span><span class="sxs-lookup"><span data-stu-id="5f953-117"><dt>**E\_INVALIDARG**</dt> <dt>214794287 (0xCCD802F)</dt></span></span> </dl>            | <span data-ttu-id="5f953-118">Un ou plusieurs arguments ne sont pas valides.</span><span class="sxs-lookup"><span data-stu-id="5f953-118">One or more of the arguments are not valid.</span></span><br/>                                       |
| <dl> <span data-ttu-id="5f953-119"><dt>**FVE \_ E \_ Locked \_ volume**</dt> <dt>2150694912 (0x80310000)</dt></span><span class="sxs-lookup"><span data-stu-id="5f953-119"><dt>**FVE\_E\_LOCKED\_VOLUME**</dt> <dt>2150694912 (0x80310000)</dt></span></span> </dl> | <span data-ttu-id="5f953-120">Le volume est verrouillé.</span><span class="sxs-lookup"><span data-stu-id="5f953-120">The volume is locked.</span></span><br/>                                                             |
| <dl> <span data-ttu-id="5f953-121"><dt>**FVE \_ E \_ non \_ activée**</dt> <dt>2150694920 (0x80310008)</dt></span><span class="sxs-lookup"><span data-stu-id="5f953-121"><dt>**FVE\_E\_NOT\_ACTIVATED**</dt> <dt>2150694920 (0x80310008)</dt></span></span> </dl> | <span data-ttu-id="5f953-122">BitLocker n’est pas activé sur le volume.</span><span class="sxs-lookup"><span data-stu-id="5f953-122">BitLocker is not enabled on the volume.</span></span> <span data-ttu-id="5f953-123">Ajoutez un protecteur de clé pour activer BitLocker.</span><span class="sxs-lookup"><span data-stu-id="5f953-123">Add a key protector to enable BitLocker.</span></span> <br/> |



 

## <a name="remarks"></a><span data-ttu-id="5f953-124">Notes</span><span class="sxs-lookup"><span data-stu-id="5f953-124">Remarks</span></span>

<span data-ttu-id="5f953-125">Les fichiers format MOF (MOF) contiennent les définitions des classes Windows Management Instrumentation (WMI).</span><span class="sxs-lookup"><span data-stu-id="5f953-125">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="5f953-126">Les fichiers MOF ne sont pas installés dans le cadre de la SDK Windows.</span><span class="sxs-lookup"><span data-stu-id="5f953-126">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="5f953-127">Ils sont installés sur le serveur lorsque vous ajoutez le rôle associé à l’aide de l’Gestionnaire de serveur.</span><span class="sxs-lookup"><span data-stu-id="5f953-127">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="5f953-128">Pour plus d’informations sur les fichiers MOF, consultez [format MOF (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="5f953-128">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="5f953-129">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5f953-129">Requirements</span></span>



| <span data-ttu-id="5f953-130">Condition requise</span><span class="sxs-lookup"><span data-stu-id="5f953-130">Requirement</span></span> | <span data-ttu-id="5f953-131">Valeur</span><span class="sxs-lookup"><span data-stu-id="5f953-131">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5f953-132">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5f953-132">Minimum supported client</span></span><br/> | <span data-ttu-id="5f953-133">Windows 7 entreprise, les applications de bureau Windows 7 édition intégrale \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="5f953-133">Windows 7 Enterprise, Windows 7 Ultimate \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="5f953-134">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5f953-134">Minimum supported server</span></span><br/> | <span data-ttu-id="5f953-135">Applications de bureau Windows Server 2008 R2 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="5f953-135">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="5f953-136">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="5f953-136">Namespace</span></span><br/>                | <span data-ttu-id="5f953-137">Racine \\ de \\ sécurité cimv2 \\ MicrosoftVolumeEncryption</span><span class="sxs-lookup"><span data-stu-id="5f953-137">Root\\CIMV2\\Security\\MicrosoftVolumeEncryption</span></span><br/>                                             |
| <span data-ttu-id="5f953-138">MOF</span><span class="sxs-lookup"><span data-stu-id="5f953-138">MOF</span></span><br/>                      | <dl> <span data-ttu-id="5f953-139"><dt>Win32 \_ encryptablevolume. mof</dt></span><span class="sxs-lookup"><span data-stu-id="5f953-139"><dt>Win32\_encryptablevolume.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5f953-140">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5f953-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5f953-141">**\_EncryptableVolume Win32**</span><span class="sxs-lookup"><span data-stu-id="5f953-141">**Win32\_EncryptableVolume**</span></span>](win32-encryptablevolume.md)
</dt> </dl>

 

 
