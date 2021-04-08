---
description: Cette méthode est utilisée pour rechercher la réserve réelle avec le paramètre d’entrée correspondant au nombre de processeurs d’ordinateurs virtuels pour lesquels la réserve est calculée.
ms.assetid: C0497900-00F3-4975-9D12-C82C13C03D8E
title: Méthode CalculatePossibleReserve de la classe Msvm_ProcessorPool
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ProcessorPool.CalculatePossibleReserve
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: c7f88bcf3295b1792fca6be88ae0c9282b72646e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103756622"
---
# <a name="calculatepossiblereserve-method-of-the-msvm_processorpool-class"></a><span data-ttu-id="05658-103">Méthode CalculatePossibleReserve de la \_ classe ProcessorPool MSVM</span><span class="sxs-lookup"><span data-stu-id="05658-103">CalculatePossibleReserve method of the Msvm\_ProcessorPool class</span></span>

<span data-ttu-id="05658-104">Cette méthode est utilisée pour rechercher la réserve réelle avec le paramètre d’entrée correspondant au nombre de processeurs d’ordinateurs virtuels pour lesquels la réserve est calculée.</span><span class="sxs-lookup"><span data-stu-id="05658-104">This method is used to find the actual reserve with the input parameter being the number of virtual machine processors for which the reserve is calculated.</span></span> <span data-ttu-id="05658-105">Cette méthode est nécessaire car la réservation des ressources du processeur dépend fortement du nombre de processeurs qui doivent être planifiés en parallèle.</span><span class="sxs-lookup"><span data-stu-id="05658-105">This method is necessary because the reservation of processor resources is highly dependent on the number of processors which must be scheduled in parallel.</span></span>

## <a name="syntax"></a><span data-ttu-id="05658-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="05658-106">Syntax</span></span>


```mof
uint32 CalculatePossibleReserve(
  [in] uint16 ProcessorCount
);
```



## <a name="parameters"></a><span data-ttu-id="05658-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="05658-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="05658-108">*ProcessorCount* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="05658-108">*ProcessorCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="05658-109">Type : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="05658-109">Type: **uint16**</span></span>

<span data-ttu-id="05658-110">Nombre de processeurs d’ordinateurs virtuels pour lesquels la réserve est calculée.</span><span class="sxs-lookup"><span data-stu-id="05658-110">The number of virtual machine processors for which the reserve is calculated.</span></span> <span data-ttu-id="05658-111">La valeur maximale de cette propriété est le nombre de processeurs logiques pour l’ordinateur hôte.</span><span class="sxs-lookup"><span data-stu-id="05658-111">The maximum value for this property is the logical processor count for the host computer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="05658-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="05658-112">Return value</span></span>

<span data-ttu-id="05658-113">Type : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="05658-113">Type: **uint32**</span></span>

<span data-ttu-id="05658-114">Quantité de ressources de processeur qui peuvent être réservées pour un ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="05658-114">The amount of CPU resources that may be reserved for a virtual machine.</span></span>

## <a name="remarks"></a><span data-ttu-id="05658-115">Notes</span><span class="sxs-lookup"><span data-stu-id="05658-115">Remarks</span></span>

<span data-ttu-id="05658-116">L’accès à la classe [**MSVM \_ ProcessorPool**](msvm-processorpool.md) peut être limité par le filtrage UAC.</span><span class="sxs-lookup"><span data-stu-id="05658-116">Access to the [**Msvm\_ProcessorPool**](msvm-processorpool.md) class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="05658-117">Pour plus d’informations, consultez [contrôle de compte d’utilisateur et WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="05658-117">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="05658-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="05658-118">Requirements</span></span>



| <span data-ttu-id="05658-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="05658-119">Requirement</span></span> | <span data-ttu-id="05658-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="05658-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="05658-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="05658-121">Minimum supported client</span></span><br/> | <span data-ttu-id="05658-122">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="05658-122">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="05658-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="05658-123">Minimum supported server</span></span><br/> | <span data-ttu-id="05658-124">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="05658-124">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="05658-125">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="05658-125">Namespace</span></span><br/>                | <span data-ttu-id="05658-126">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="05658-126">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="05658-127">MOF</span><span class="sxs-lookup"><span data-stu-id="05658-127">MOF</span></span><br/>                      | <dl> <span data-ttu-id="05658-128"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="05658-128"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="05658-129">DLL</span><span class="sxs-lookup"><span data-stu-id="05658-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="05658-130"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="05658-130"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="05658-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="05658-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="05658-132">**MSVM \_ ProcessorPool**</span><span class="sxs-lookup"><span data-stu-id="05658-132">**Msvm\_ProcessorPool**</span></span>](msvm-processorpool.md)
</dt> </dl>

 

