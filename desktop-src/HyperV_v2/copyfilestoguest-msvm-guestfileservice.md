---
description: Copie les fichiers de l’hôte Hyper-V vers l’ordinateur virtuel.
ms.assetid: 76667557-13B2-4286-BC6B-E32FADE62A7A
title: 'Msvm_GuestFileService :: CopyFilesToGuest, méthode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_GuestFileService.CopyFilesToGuest
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 9424dee6d28e0bd9cd6ac43c15ad27cdebdb7017
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106536490"
---
# <a name="msvm_guestfileservicecopyfilestoguest-method"></a><span data-ttu-id="5fdee-103">MSVM \_ GuestFileService :: CopyFilesToGuest, méthode</span><span class="sxs-lookup"><span data-stu-id="5fdee-103">Msvm\_GuestFileService::CopyFilesToGuest method</span></span>

<span data-ttu-id="5fdee-104">Copie les fichiers de l’hôte Hyper-V vers l’ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="5fdee-104">Copies files from the Hyper-V host to the virtual machine.</span></span>

## <a name="syntax"></a><span data-ttu-id="5fdee-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="5fdee-105">Syntax</span></span>


```C++
uint32 CopyFilesToGuest(
  [in]            string                  CopyFileToGuestSettings[],
  [out]           CIM_ConcreteJob     Job,
  [out, optional] Msvm_CopyFileToGuestJob ParentPools[]
);
```



## <a name="parameters"></a><span data-ttu-id="5fdee-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="5fdee-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5fdee-107">*CopyFileToGuestSettings* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="5fdee-107">*CopyFileToGuestSettings* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5fdee-108">Tableau d’instances de la classe [**MSVM \_ CopyFileToGuestSettingData**](msvm-copyfiletoguestsettingdata.md) qui représente un travail d’opération de service de fichiers invité.</span><span class="sxs-lookup"><span data-stu-id="5fdee-108">An array of instances of the [**Msvm\_CopyFileToGuestSettingData**](msvm-copyfiletoguestsettingdata.md) class that represents a guest file service operation job.</span></span>

</dd> <dt>

<span data-ttu-id="5fdee-109">*Travail* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="5fdee-109">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5fdee-110">Paramètre facultatif permettant de surveiller la progression de l’opération, qui est utilisé si la méthode n’a pas pu être exécutée de façon synchrone.</span><span class="sxs-lookup"><span data-stu-id="5fdee-110">An optional parameter for monitoring progress of the operation, which is used if the method could not be executed synchronously.</span></span> <span data-ttu-id="5fdee-111">Si l’opération s’exécute de façon asynchrone, la valeur de retour est 4096.</span><span class="sxs-lookup"><span data-stu-id="5fdee-111">If the operation is executing asynchronously, the return value is 4096.</span></span>

> [!Note]  
> <span data-ttu-id="5fdee-112">Ce paramètre a été ajouté dans Windows 10.</span><span class="sxs-lookup"><span data-stu-id="5fdee-112">This parameter was added in Windows 10.</span></span>

 

</dd> <dt>

<span data-ttu-id="5fdee-113">*ParentPools* \[ out, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="5fdee-113">*ParentPools* \[out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="5fdee-114">Tableau facultatif de références [**\_ CopyFileToGuestJob MSVM**](msvm-copyfiletoguestjob.md) utilisées pour surveiller la progression de l’opération.</span><span class="sxs-lookup"><span data-stu-id="5fdee-114">An optional array of [**Msvm\_CopyFileToGuestJob**](msvm-copyfiletoguestjob.md) references that are used for monitoring progress of the operation.</span></span> <span data-ttu-id="5fdee-115">**CopyFilesToGuest** utilise *ParentPools* s’il ne peut pas s’exécuter de façon synchrone.</span><span class="sxs-lookup"><span data-stu-id="5fdee-115">**CopyFilesToGuest** uses *ParentPools* if it can't execute synchronously.</span></span> <span data-ttu-id="5fdee-116">Si l’opération s’exécute de façon asynchrone, la valeur de retour est 4096.</span><span class="sxs-lookup"><span data-stu-id="5fdee-116">If the operation executes asynchronously, the return value is 4096.</span></span>

> [!Note]  
> <span data-ttu-id="5fdee-117">Ce paramètre a été supprimé dans Windows 10.</span><span class="sxs-lookup"><span data-stu-id="5fdee-117">This parameter was removed in Windows 10.</span></span>

 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5fdee-118">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="5fdee-118">Return value</span></span>

<span data-ttu-id="5fdee-119">En cas de réussite, retourne 0 ; Sinon, retourne une valeur d’erreur.</span><span class="sxs-lookup"><span data-stu-id="5fdee-119">On success, returns 0; otherwise, returns an error value.</span></span>

<dl> <dt>

<span data-ttu-id="5fdee-120">**Terminé sans erreur** (0)</span><span class="sxs-lookup"><span data-stu-id="5fdee-120">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="5fdee-121">**Paramètres de méthode activés-tâche démarrée** (4096)</span><span class="sxs-lookup"><span data-stu-id="5fdee-121">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="5fdee-122">**Échec** (32768)</span><span class="sxs-lookup"><span data-stu-id="5fdee-122">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="5fdee-123">**Accès refusé** (32769)</span><span class="sxs-lookup"><span data-stu-id="5fdee-123">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="5fdee-124">**Non pris en charge** (32770)</span><span class="sxs-lookup"><span data-stu-id="5fdee-124">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="5fdee-125">**État inconnu** (32771)</span><span class="sxs-lookup"><span data-stu-id="5fdee-125">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="5fdee-126">**Délai d’expiration** (32772)</span><span class="sxs-lookup"><span data-stu-id="5fdee-126">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="5fdee-127">**Paramètre non valide** (32773)</span><span class="sxs-lookup"><span data-stu-id="5fdee-127">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="5fdee-128">Le **système est en cours d’utilisation** (32774)</span><span class="sxs-lookup"><span data-stu-id="5fdee-128">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="5fdee-129">**État non valide pour cette opération** (32775)</span><span class="sxs-lookup"><span data-stu-id="5fdee-129">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="5fdee-130">**Type de données incorrect** (32776)</span><span class="sxs-lookup"><span data-stu-id="5fdee-130">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="5fdee-131">Le **système n’est pas disponible** (32777)</span><span class="sxs-lookup"><span data-stu-id="5fdee-131">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="5fdee-132">**Mémoire insuffisante** (32778)</span><span class="sxs-lookup"><span data-stu-id="5fdee-132">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="5fdee-133">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5fdee-133">Requirements</span></span>



| <span data-ttu-id="5fdee-134">Condition requise</span><span class="sxs-lookup"><span data-stu-id="5fdee-134">Requirement</span></span> | <span data-ttu-id="5fdee-135">Valeur</span><span class="sxs-lookup"><span data-stu-id="5fdee-135">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5fdee-136">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5fdee-136">Minimum supported client</span></span><br/> | <span data-ttu-id="5fdee-137">Windows 8.1 les \[ applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="5fdee-137">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="5fdee-138">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5fdee-138">Minimum supported server</span></span><br/> | <span data-ttu-id="5fdee-139">Applications de bureau Windows Server 2012 R2 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="5fdee-139">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="5fdee-140">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="5fdee-140">Namespace</span></span><br/>                | <span data-ttu-id="5fdee-141">\\\\\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="5fdee-141">\\\\Root\\Virtualization\\V2</span></span><br/>                                                                 |
| <span data-ttu-id="5fdee-142">MOF</span><span class="sxs-lookup"><span data-stu-id="5fdee-142">MOF</span></span><br/>                      | <dl> <span data-ttu-id="5fdee-143"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="5fdee-143"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="5fdee-144">DLL</span><span class="sxs-lookup"><span data-stu-id="5fdee-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5fdee-145"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="5fdee-145"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="5fdee-146">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5fdee-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5fdee-147">**MSVM \_ GuestFileService**</span><span class="sxs-lookup"><span data-stu-id="5fdee-147">**Msvm\_GuestFileService**</span></span>](msvm-guestfileservice.md)
</dt> </dl>

 

 




