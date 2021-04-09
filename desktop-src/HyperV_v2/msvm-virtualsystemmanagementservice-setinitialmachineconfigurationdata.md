---
description: Définit les données de configuration initiales de l’ordinateur des machines virtuelles.
ms.assetid: 0f174d29-ddb2-4a8c-b664-926245573778
title: Méthode SetInitialMachineConfigurationData de la classe Msvm_VirtualSystemManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemManagementService.SetInitialMachineConfigurationData
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 08028358d6bb53406abe15c88e0acd02e748d387
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103750180"
---
# <a name="setinitialmachineconfigurationdata-method-of-the-msvm_virtualsystemmanagementservice-class"></a><span data-ttu-id="d5385-103">Méthode SetInitialMachineConfigurationData de la \_ classe VirtualSystemManagementService MSVM</span><span class="sxs-lookup"><span data-stu-id="d5385-103">SetInitialMachineConfigurationData method of the Msvm\_VirtualSystemManagementService class</span></span>

<span data-ttu-id="d5385-104">Définit les données de configuration initiales de l’ordinateur d’une machine virtuelle.</span><span class="sxs-lookup"><span data-stu-id="d5385-104">Sets a VM's initial machine configuration data.</span></span>

## <a name="syntax"></a><span data-ttu-id="d5385-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d5385-105">Syntax</span></span>


```mof
uint32 SetInitialMachineConfigurationData(
  [in]  CIM_ComputerSystem REF TargetSystem,
  [in]  uint8                  ImcData[],
  [out] CIM_ConcreteJob    REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="d5385-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d5385-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d5385-107">*TargetSystem* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="d5385-107">*TargetSystem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d5385-108">Référence au système d’ordinateur virtuel sur lequel les données IMC seront définies.</span><span class="sxs-lookup"><span data-stu-id="d5385-108">A reference to the virtual computer system on which the IMC data will be set.</span></span>

</dd> <dt>

<span data-ttu-id="d5385-109">*ImcData* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="d5385-109">*ImcData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d5385-110">Données IMC à définir.</span><span class="sxs-lookup"><span data-stu-id="d5385-110">The IMC data to set.</span></span> <span data-ttu-id="d5385-111">Les quatre premiers octets doivent être la longueur du tableau par ordre de primauté des octets de poids fort (Big endian)</span><span class="sxs-lookup"><span data-stu-id="d5385-111">The first four bytes must be the length of the array in big-endian order</span></span>

</dd> <dt>

<span data-ttu-id="d5385-112">*Travail* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="d5385-112">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d5385-113">Paramètre facultatif permettant de surveiller la progression de l’opération, qui est utilisé si la méthode n’a pas pu être exécutée de façon synchrone.</span><span class="sxs-lookup"><span data-stu-id="d5385-113">An optional parameter for monitoring progress of the operation, which is used if the method could not be executed synchronously.</span></span> <span data-ttu-id="d5385-114">Si l’opération s’exécute de façon asynchrone, la valeur de retour est 4096.</span><span class="sxs-lookup"><span data-stu-id="d5385-114">If the operation is executing asynchronously, the return value is 4096.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d5385-115">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="d5385-115">Return value</span></span>

<span data-ttu-id="d5385-116">En cas de réussite, retourne 0 ou 4096 ; Sinon, retourne une erreur.</span><span class="sxs-lookup"><span data-stu-id="d5385-116">On success, returns 0 or 4096; otherwise, returns an error.</span></span>

<dl> <dt>

<span data-ttu-id="d5385-117">**Terminé sans erreur** (0)</span><span class="sxs-lookup"><span data-stu-id="d5385-117">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="d5385-118">**Paramètres de méthode activés-tâche démarrée** (4096)</span><span class="sxs-lookup"><span data-stu-id="d5385-118">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="d5385-119">**Échec** (32768)</span><span class="sxs-lookup"><span data-stu-id="d5385-119">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="d5385-120">**Accès refusé** (32769)</span><span class="sxs-lookup"><span data-stu-id="d5385-120">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="d5385-121">**Non pris en charge** (32770)</span><span class="sxs-lookup"><span data-stu-id="d5385-121">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="d5385-122">**État inconnu** (32771)</span><span class="sxs-lookup"><span data-stu-id="d5385-122">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="d5385-123">**Délai d’expiration** (32772)</span><span class="sxs-lookup"><span data-stu-id="d5385-123">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="d5385-124">**Paramètre non valide** (32773)</span><span class="sxs-lookup"><span data-stu-id="d5385-124">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="d5385-125">Le **système est en cours d’utilisation** (32774)</span><span class="sxs-lookup"><span data-stu-id="d5385-125">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="d5385-126">**État non valide pour cette opération** (32775)</span><span class="sxs-lookup"><span data-stu-id="d5385-126">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="d5385-127">**Type de données incorrect** (32776)</span><span class="sxs-lookup"><span data-stu-id="d5385-127">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="d5385-128">Le **système n’est pas disponible** (32777)</span><span class="sxs-lookup"><span data-stu-id="d5385-128">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="d5385-129">**Mémoire insuffisante** (32778)</span><span class="sxs-lookup"><span data-stu-id="d5385-129">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="d5385-130">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d5385-130">Requirements</span></span>



| <span data-ttu-id="d5385-131">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d5385-131">Requirement</span></span> | <span data-ttu-id="d5385-132">Valeur</span><span class="sxs-lookup"><span data-stu-id="d5385-132">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d5385-133">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d5385-133">Minimum supported client</span></span><br/> | <span data-ttu-id="d5385-134">Applications de \[ Bureau Windows 10 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d5385-134">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="d5385-135">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d5385-135">Minimum supported server</span></span><br/> | <span data-ttu-id="d5385-136">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="d5385-136">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="d5385-137">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="d5385-137">Namespace</span></span><br/>                | <span data-ttu-id="d5385-138">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="d5385-138">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="d5385-139">MOF</span><span class="sxs-lookup"><span data-stu-id="d5385-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d5385-140"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="d5385-140"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="d5385-141">DLL</span><span class="sxs-lookup"><span data-stu-id="d5385-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d5385-142"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="d5385-142"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="d5385-143">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d5385-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d5385-144">**MSVM \_ VirtualSystemManagementService**</span><span class="sxs-lookup"><span data-stu-id="d5385-144">**Msvm\_VirtualSystemManagementService**</span></span>](msvm-virtualsystemmanagementservice.md)
</dt> </dl>

 

 




