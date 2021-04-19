---
description: Décale la position du pointeur de la souris selon les deltas horizontaux et verticaux spécifiés.
ms.assetid: C74E4BEA-C7E1-44C7-B4FC-8926F23DF1FE
title: Méthode SetRelativePosition de la classe Msvm_Ps2Mouse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_Ps2Mouse.SetRelativePosition
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: b7f4d10f48bce4b33cd4965f08633b85b5a738bb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106534614"
---
# <a name="setrelativeposition-method-of-the-msvm_ps2mouse-class"></a><span data-ttu-id="09cf6-103">Méthode SetRelativePosition de la \_ classe Ps2Mouse MSVM</span><span class="sxs-lookup"><span data-stu-id="09cf6-103">SetRelativePosition method of the Msvm\_Ps2Mouse class</span></span>

<span data-ttu-id="09cf6-104">Décale la position du pointeur de la souris selon les deltas horizontaux et verticaux spécifiés.</span><span class="sxs-lookup"><span data-stu-id="09cf6-104">Offsets the position of the mouse pointer by the specified horizontal and vertical deltas.</span></span>

## <a name="syntax"></a><span data-ttu-id="09cf6-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="09cf6-105">Syntax</span></span>


```mof
uint32 SetRelativePosition(
  [in] sint8 horizontalDelta,
  [in] sint8 verticalDelta
);
```



## <a name="parameters"></a><span data-ttu-id="09cf6-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="09cf6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="09cf6-107">*horizontalDelta* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="09cf6-107">*horizontalDelta* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="09cf6-108">Type : **sint8**</span><span class="sxs-lookup"><span data-stu-id="09cf6-108">Type: **sint8**</span></span>

<span data-ttu-id="09cf6-109">Modification horizontale de la position de la souris, en pixels.</span><span class="sxs-lookup"><span data-stu-id="09cf6-109">The horizontal change for the mouse position, in pixels.</span></span>

</dd> <dt>

<span data-ttu-id="09cf6-110">*verticalDelta* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="09cf6-110">*verticalDelta* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="09cf6-111">Type : **sint8**</span><span class="sxs-lookup"><span data-stu-id="09cf6-111">Type: **sint8**</span></span>

<span data-ttu-id="09cf6-112">Modification verticale de la position de la souris, en pixels.</span><span class="sxs-lookup"><span data-stu-id="09cf6-112">The vertical change for the mouse position, in pixels.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="09cf6-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="09cf6-113">Return value</span></span>

<span data-ttu-id="09cf6-114">Type : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="09cf6-114">Type: **uint32**</span></span>

<span data-ttu-id="09cf6-115">Une valeur de retour de zéro indique une réussite.</span><span class="sxs-lookup"><span data-stu-id="09cf6-115">A return value of zero indicates success.</span></span> <span data-ttu-id="09cf6-116">Une valeur différente de zéro indique un échec de modification de la position de la souris.</span><span class="sxs-lookup"><span data-stu-id="09cf6-116">A nonzero value indicates a failure to alter the mouse position.</span></span>

<dl> <dt>

<span data-ttu-id="09cf6-117">**Terminé sans erreur** (0)</span><span class="sxs-lookup"><span data-stu-id="09cf6-117">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="09cf6-118">**Paramètres de méthode activés-tâche démarrée** (4096)</span><span class="sxs-lookup"><span data-stu-id="09cf6-118">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="09cf6-119">**Échec** (32768)</span><span class="sxs-lookup"><span data-stu-id="09cf6-119">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="09cf6-120">**Accès refusé** (32769)</span><span class="sxs-lookup"><span data-stu-id="09cf6-120">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="09cf6-121">**Non pris en charge** (32770)</span><span class="sxs-lookup"><span data-stu-id="09cf6-121">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="09cf6-122">**État inconnu** (32771)</span><span class="sxs-lookup"><span data-stu-id="09cf6-122">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="09cf6-123">**Délai d’expiration** (32772)</span><span class="sxs-lookup"><span data-stu-id="09cf6-123">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="09cf6-124">**Paramètre non valide** (32773)</span><span class="sxs-lookup"><span data-stu-id="09cf6-124">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="09cf6-125">Le **système est en cours d’utilisation** (32774)</span><span class="sxs-lookup"><span data-stu-id="09cf6-125">**System is in used** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="09cf6-126">**État non valide pour cette opération** (32775)</span><span class="sxs-lookup"><span data-stu-id="09cf6-126">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="09cf6-127">**Type de données incorrect** (32776)</span><span class="sxs-lookup"><span data-stu-id="09cf6-127">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="09cf6-128">Le **système n’est pas disponible** (32777)</span><span class="sxs-lookup"><span data-stu-id="09cf6-128">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="09cf6-129">**Mémoire insuffisante** (32778)</span><span class="sxs-lookup"><span data-stu-id="09cf6-129">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="09cf6-130">Notes</span><span class="sxs-lookup"><span data-stu-id="09cf6-130">Remarks</span></span>

<span data-ttu-id="09cf6-131">L’accès à la classe [**MSVM \_ Ps2Mouse**](msvm-ps2mouse.md) peut être limité par le filtrage UAC.</span><span class="sxs-lookup"><span data-stu-id="09cf6-131">Access to the [**Msvm\_Ps2Mouse**](msvm-ps2mouse.md) class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="09cf6-132">Pour plus d’informations, consultez [contrôle de compte d’utilisateur et WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="09cf6-132">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="09cf6-133">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="09cf6-133">Requirements</span></span>



| <span data-ttu-id="09cf6-134">Condition requise</span><span class="sxs-lookup"><span data-stu-id="09cf6-134">Requirement</span></span> | <span data-ttu-id="09cf6-135">Valeur</span><span class="sxs-lookup"><span data-stu-id="09cf6-135">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="09cf6-136">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="09cf6-136">Minimum supported client</span></span><br/> | <span data-ttu-id="09cf6-137">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="09cf6-137">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="09cf6-138">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="09cf6-138">Minimum supported server</span></span><br/> | <span data-ttu-id="09cf6-139">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="09cf6-139">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="09cf6-140">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="09cf6-140">Namespace</span></span><br/>                | <span data-ttu-id="09cf6-141">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="09cf6-141">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="09cf6-142">MOF</span><span class="sxs-lookup"><span data-stu-id="09cf6-142">MOF</span></span><br/>                      | <dl> <span data-ttu-id="09cf6-143"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="09cf6-143"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="09cf6-144">DLL</span><span class="sxs-lookup"><span data-stu-id="09cf6-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="09cf6-145"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="09cf6-145"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="09cf6-146">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="09cf6-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="09cf6-147">**MSVM \_ Ps2Mouse**</span><span class="sxs-lookup"><span data-stu-id="09cf6-147">**Msvm\_Ps2Mouse**</span></span>](msvm-ps2mouse.md)
</dt> </dl>

 

