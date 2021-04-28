---
description: 'Méthode RemoveAssociatedData de la classe Msvm_VirtualSystemReferencePointService : supprime le journal de données associé au point de référence.'
ms.assetid: b6206bda-c195-4c6f-9b80-508c20b53ce5
title: Méthode RemoveAssociatedData de la classe Msvm_VirtualSystemReferencePointService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemReferencePointService.RemoveAssociatedData
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: b5291e4e018edc89909ccde36ce0e420698af8e6
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108118617"
---
# <a name="removeassociateddata-method-of-the-msvm_virtualsystemreferencepointservice-class"></a><span data-ttu-id="9a2c1-103">Méthode RemoveAssociatedData de la \_ classe VirtualSystemReferencePointService MSVM</span><span class="sxs-lookup"><span data-stu-id="9a2c1-103">RemoveAssociatedData method of the Msvm\_VirtualSystemReferencePointService class</span></span>

<span data-ttu-id="9a2c1-104">Supprime le journal de données associé au point de référence.</span><span class="sxs-lookup"><span data-stu-id="9a2c1-104">Removes the data log associated with the reference point.</span></span>

## <a name="syntax"></a><span data-ttu-id="9a2c1-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9a2c1-105">Syntax</span></span>


```mof
uint32 RemoveAssociatedData(
  [in]  Msvm_VirtualSystemReferencePoint REF AffectedReferencePoint,
  [out] CIM_ConcreteJob                  REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="9a2c1-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="9a2c1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9a2c1-107">*AffectedReferencePoint* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="9a2c1-107">*AffectedReferencePoint* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9a2c1-108">Référence à l’instance [**MSVM \_ VirtualSystemReferencePoint**](msvm-virtualsystemreferencepoint.md) qui représente le point de référence à supprimer.</span><span class="sxs-lookup"><span data-stu-id="9a2c1-108">A reference to the [**Msvm\_VirtualSystemReferencePoint**](msvm-virtualsystemreferencepoint.md) instance which represents the reference point to be removed.</span></span>

</dd> <dt>

<span data-ttu-id="9a2c1-109">*Travail* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="9a2c1-109">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9a2c1-110">Paramètre facultatif permettant de surveiller la progression de l’opération, qui est utilisé si la méthode n’a pas pu être exécutée de façon synchrone.</span><span class="sxs-lookup"><span data-stu-id="9a2c1-110">An optional parameter for monitoring progress of the operation, which is used if the method could not be executed synchronously.</span></span> <span data-ttu-id="9a2c1-111">Si l’opération s’exécute de façon asynchrone, la valeur de retour est 4096.</span><span class="sxs-lookup"><span data-stu-id="9a2c1-111">If the operation is executing asynchronously, the return value is 4096.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9a2c1-112">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="9a2c1-112">Return value</span></span>

<span data-ttu-id="9a2c1-113">En cas de réussite, retourne 0 (terminé sans erreur) ou 4096 (travail démarré); Sinon, retourne une erreur.</span><span class="sxs-lookup"><span data-stu-id="9a2c1-113">On success, returns a 0 (Complete with No Error), or 4096 (Job Started); otherwise, return an error.</span></span>

<dl> <dt>

<span data-ttu-id="9a2c1-114">**Terminé sans erreur** (0)</span><span class="sxs-lookup"><span data-stu-id="9a2c1-114">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="9a2c1-115">**Paramètres de méthode activés-tâche démarrée** (4096)</span><span class="sxs-lookup"><span data-stu-id="9a2c1-115">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="9a2c1-116">**Échec** (32768)</span><span class="sxs-lookup"><span data-stu-id="9a2c1-116">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="9a2c1-117">**Accès refusé** (32769)</span><span class="sxs-lookup"><span data-stu-id="9a2c1-117">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="9a2c1-118">**Non pris en charge** (32770)</span><span class="sxs-lookup"><span data-stu-id="9a2c1-118">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="9a2c1-119">**État inconnu** (32771)</span><span class="sxs-lookup"><span data-stu-id="9a2c1-119">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="9a2c1-120">**Délai d’expiration** (32772)</span><span class="sxs-lookup"><span data-stu-id="9a2c1-120">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="9a2c1-121">**Paramètre non valide** (32773)</span><span class="sxs-lookup"><span data-stu-id="9a2c1-121">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="9a2c1-122">Le **système est en cours d’utilisation** (32774)</span><span class="sxs-lookup"><span data-stu-id="9a2c1-122">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="9a2c1-123">**État non valide pour cette opération** (32775)</span><span class="sxs-lookup"><span data-stu-id="9a2c1-123">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="9a2c1-124">**Type de données incorrect** (32776)</span><span class="sxs-lookup"><span data-stu-id="9a2c1-124">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="9a2c1-125">Le **système n’est pas disponible** (32777)</span><span class="sxs-lookup"><span data-stu-id="9a2c1-125">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="9a2c1-126">**Mémoire insuffisante** (32778)</span><span class="sxs-lookup"><span data-stu-id="9a2c1-126">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="9a2c1-127">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="9a2c1-127">Requirements</span></span>



| <span data-ttu-id="9a2c1-128">Condition requise</span><span class="sxs-lookup"><span data-stu-id="9a2c1-128">Requirement</span></span> | <span data-ttu-id="9a2c1-129">Valeur</span><span class="sxs-lookup"><span data-stu-id="9a2c1-129">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9a2c1-130">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9a2c1-130">Minimum supported client</span></span><br/> | <span data-ttu-id="9a2c1-131">Applications de \[ Bureau Windows 10 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="9a2c1-131">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="9a2c1-132">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9a2c1-132">Minimum supported server</span></span><br/> | <span data-ttu-id="9a2c1-133">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="9a2c1-133">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="9a2c1-134">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="9a2c1-134">Namespace</span></span><br/>                | <span data-ttu-id="9a2c1-135">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="9a2c1-135">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="9a2c1-136">MOF</span><span class="sxs-lookup"><span data-stu-id="9a2c1-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9a2c1-137"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="9a2c1-137"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="9a2c1-138">DLL</span><span class="sxs-lookup"><span data-stu-id="9a2c1-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9a2c1-139"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="9a2c1-139"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="9a2c1-140">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9a2c1-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9a2c1-141">**MSVM \_ VirtualSystemReferencePointService**</span><span class="sxs-lookup"><span data-stu-id="9a2c1-141">**Msvm\_VirtualSystemReferencePointService**</span></span>](msvm-virtualsystemreferencepointservice.md)
</dt> </dl>

 

 




