---
description: Définit la position horizontale et verticale du curseur de la souris.
ms.assetid: 7845E10A-7F61-4134-BF81-AED5483F36AD
title: Méthode SetAbsolutePosition de la classe Msvm_SyntheticMouse (Dbdao. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SyntheticMouse.SetAbsolutePosition
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 4b8ffb3a4d415f76dedf30acba5869b4cc585eb5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103864889"
---
# <a name="setabsoluteposition-method-of-the-msvm_syntheticmouse-class"></a><span data-ttu-id="74947-103">Méthode SetAbsolutePosition de la \_ classe SyntheticMouse MSVM</span><span class="sxs-lookup"><span data-stu-id="74947-103">SetAbsolutePosition method of the Msvm\_SyntheticMouse class</span></span>

<span data-ttu-id="74947-104">Définit la position horizontale et verticale du curseur de la souris.</span><span class="sxs-lookup"><span data-stu-id="74947-104">Sets the horizontal and vertical position of the mouse cursor.</span></span>

## <a name="syntax"></a><span data-ttu-id="74947-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="74947-105">Syntax</span></span>


```mof
uint32 SetAbsolutePosition(
  [in] sint32 horizontalPosition,
  [in] sint32 verticalPosition
);
```



## <a name="parameters"></a><span data-ttu-id="74947-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="74947-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="74947-107">*horizontalPosition* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="74947-107">*horizontalPosition* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="74947-108">Type : **sint32**</span><span class="sxs-lookup"><span data-stu-id="74947-108">Type: **sint32**</span></span>

<span data-ttu-id="74947-109">Nouvelle position horizontale du curseur de la souris, en pixels.</span><span class="sxs-lookup"><span data-stu-id="74947-109">The new horizontal position of the mouse cursor, in pixels.</span></span>

</dd> <dt>

<span data-ttu-id="74947-110">*verticalPosition* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="74947-110">*verticalPosition* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="74947-111">Type : **sint32**</span><span class="sxs-lookup"><span data-stu-id="74947-111">Type: **sint32**</span></span>

<span data-ttu-id="74947-112">Nouvelle position verticale du curseur de la souris, en pixels.</span><span class="sxs-lookup"><span data-stu-id="74947-112">The new vertical position of the mouse cursor, in pixels.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="74947-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="74947-113">Return value</span></span>

<span data-ttu-id="74947-114">Type : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="74947-114">Type: **uint32**</span></span>

<span data-ttu-id="74947-115">Une valeur de retour de zéro indique une réussite.</span><span class="sxs-lookup"><span data-stu-id="74947-115">A return value of zero indicates success.</span></span> <span data-ttu-id="74947-116">Une valeur différente de zéro indique un échec de modification de la position de défilement.</span><span class="sxs-lookup"><span data-stu-id="74947-116">A nonzero value indicates a failure to alter the scroll position.</span></span>

<dl> <dt>

<span data-ttu-id="74947-117">**Terminé sans erreur** (0)</span><span class="sxs-lookup"><span data-stu-id="74947-117">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="74947-118">**Paramètres de méthode activés-tâche démarrée** (4096)</span><span class="sxs-lookup"><span data-stu-id="74947-118">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="74947-119">**Échec** (32768)</span><span class="sxs-lookup"><span data-stu-id="74947-119">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="74947-120">**Accès refusé** (32769)</span><span class="sxs-lookup"><span data-stu-id="74947-120">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="74947-121">**Non pris en charge** (32770)</span><span class="sxs-lookup"><span data-stu-id="74947-121">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="74947-122">**État inconnu** (32771)</span><span class="sxs-lookup"><span data-stu-id="74947-122">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="74947-123">**Délai d’expiration** (32772)</span><span class="sxs-lookup"><span data-stu-id="74947-123">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="74947-124">**Paramètre non valide** (32773)</span><span class="sxs-lookup"><span data-stu-id="74947-124">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="74947-125">Le **système est en cours d’utilisation** (32774)</span><span class="sxs-lookup"><span data-stu-id="74947-125">**System is in used** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="74947-126">**État non valide pour cette opération** (32775)</span><span class="sxs-lookup"><span data-stu-id="74947-126">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="74947-127">**Type de données incorrect** (32776)</span><span class="sxs-lookup"><span data-stu-id="74947-127">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="74947-128">Le **système n’est pas disponible** (32777)</span><span class="sxs-lookup"><span data-stu-id="74947-128">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="74947-129">**Mémoire insuffisante** (32778)</span><span class="sxs-lookup"><span data-stu-id="74947-129">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="74947-130">Notes</span><span class="sxs-lookup"><span data-stu-id="74947-130">Remarks</span></span>

<span data-ttu-id="74947-131">L’accès à la classe [**MSVM \_ SyntheticMouse**](msvm-syntheticmouse.md) peut être limité par le filtrage UAC.</span><span class="sxs-lookup"><span data-stu-id="74947-131">Access to the [**Msvm\_SyntheticMouse**](msvm-syntheticmouse.md) class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="74947-132">Pour plus d’informations, consultez [contrôle de compte d’utilisateur et WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="74947-132">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="74947-133">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="74947-133">Requirements</span></span>



| <span data-ttu-id="74947-134">Condition requise</span><span class="sxs-lookup"><span data-stu-id="74947-134">Requirement</span></span> | <span data-ttu-id="74947-135">Valeur</span><span class="sxs-lookup"><span data-stu-id="74947-135">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="74947-136">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="74947-136">Minimum supported client</span></span><br/> | <span data-ttu-id="74947-137">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="74947-137">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="74947-138">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="74947-138">Minimum supported server</span></span><br/> | <span data-ttu-id="74947-139">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="74947-139">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="74947-140">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="74947-140">Namespace</span></span><br/>                | <span data-ttu-id="74947-141">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="74947-141">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="74947-142">En-tête</span><span class="sxs-lookup"><span data-stu-id="74947-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="74947-143"><dt>Dbdao. h</dt></span><span class="sxs-lookup"><span data-stu-id="74947-143"><dt>Dbdao.h</dt></span></span> </dl>                      |
| <span data-ttu-id="74947-144">MOF</span><span class="sxs-lookup"><span data-stu-id="74947-144">MOF</span></span><br/>                      | <dl> <span data-ttu-id="74947-145"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="74947-145"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="74947-146">DLL</span><span class="sxs-lookup"><span data-stu-id="74947-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="74947-147"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="74947-147"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="74947-148">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="74947-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="74947-149">**MSVM \_ SyntheticMouse**</span><span class="sxs-lookup"><span data-stu-id="74947-149">**Msvm\_SyntheticMouse**</span></span>](msvm-syntheticmouse.md)
</dt> </dl>

 

