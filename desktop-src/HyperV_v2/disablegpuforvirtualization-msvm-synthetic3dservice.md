---
description: Désactive un GPU physique pour la virtualisation.
ms.assetid: 280a3c25-7b8f-4113-bf35-171d15f4aea7
title: Méthode DisableGPUForVirtualization de la classe Msvm_Synthetic3DService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_Synthetic3DService.DisableGPUForVirtualization
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 2634a3196e0c59368002151426e6f1407a13db8c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104318030"
---
# <a name="disablegpuforvirtualization-method-of-the-msvm_synthetic3dservice-class"></a><span data-ttu-id="84035-103">Méthode DisableGPUForVirtualization de la \_ classe Synthetic3DService MSVM</span><span class="sxs-lookup"><span data-stu-id="84035-103">DisableGPUForVirtualization method of the Msvm\_Synthetic3DService class</span></span>

<span data-ttu-id="84035-104">Désactive un GPU physique pour la virtualisation.</span><span class="sxs-lookup"><span data-stu-id="84035-104">Disables a physical GPU for virtualization.</span></span>

## <a name="syntax"></a><span data-ttu-id="84035-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="84035-105">Syntax</span></span>


```mof
uint32 DisableGPUForVirtualization(
  [in]  Msvm_Physical3dGraphicsProcessor REF PhysicalGPU,
  [out] CIM_ConcreteJob                  REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="84035-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="84035-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="84035-107">*PhysicalGPU* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="84035-107">*PhysicalGPU* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="84035-108">Référence à une instance de la classe [**MSVM \_ Physical3dGraphicsProcessor**](msvm-physical3dgraphicsprocessor.md) qui représente le GPU physique à désactiver.</span><span class="sxs-lookup"><span data-stu-id="84035-108">A reference to an instance of the [**Msvm\_Physical3dGraphicsProcessor**](msvm-physical3dgraphicsprocessor.md) class that represents the physical GPU to be disabled.</span></span>

</dd> <dt>

<span data-ttu-id="84035-109">*Travail* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="84035-109">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="84035-110">Si l’opération est effectuée de façon asynchrone, cette méthode retourne 4096 et ce paramètre contient une référence à un objet dérivé de [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="84035-110">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="84035-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="84035-111">Return value</span></span>

<span data-ttu-id="84035-112">Cette méthode retourne l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="84035-112">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="84035-113">**Terminé sans erreur** (0)</span><span class="sxs-lookup"><span data-stu-id="84035-113">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="84035-114">**Non pris en charge** (1)</span><span class="sxs-lookup"><span data-stu-id="84035-114">**Not supported** (1)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="84035-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="84035-115">Requirements</span></span>



| <span data-ttu-id="84035-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="84035-116">Requirement</span></span> | <span data-ttu-id="84035-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="84035-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="84035-118">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="84035-118">Minimum supported client</span></span><br/> | <span data-ttu-id="84035-119">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="84035-119">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="84035-120">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="84035-120">Minimum supported server</span></span><br/> | <span data-ttu-id="84035-121">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="84035-121">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="84035-122">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="84035-122">Namespace</span></span><br/>                | <span data-ttu-id="84035-123">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="84035-123">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="84035-124">MOF</span><span class="sxs-lookup"><span data-stu-id="84035-124">MOF</span></span><br/>                      | <dl> <span data-ttu-id="84035-125"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="84035-125"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="84035-126">DLL</span><span class="sxs-lookup"><span data-stu-id="84035-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="84035-127"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="84035-127"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="84035-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="84035-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="84035-129">**MSVM \_ Synthetic3DService**</span><span class="sxs-lookup"><span data-stu-id="84035-129">**Msvm\_Synthetic3DService**</span></span>](msvm-synthetic3dservice.md)
</dt> </dl>

 

