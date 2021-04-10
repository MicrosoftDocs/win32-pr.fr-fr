---
description: Définit la coordonnée z du contrôle de roulette du dispositif de pointage.
ms.assetid: 02349957-6BAA-42E7-B3D4-F39E748615E6
title: Méthode SetScrollPosition de la classe Msvm_SyntheticMouse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SyntheticMouse.SetScrollPosition
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 6d82ad2cd75b41ca914d0db49d5de4709790ea6a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104115762"
---
# <a name="setscrollposition-method-of-the-msvm_syntheticmouse-class"></a><span data-ttu-id="a8895-103">Méthode SetScrollPosition de la \_ classe SyntheticMouse MSVM</span><span class="sxs-lookup"><span data-stu-id="a8895-103">SetScrollPosition method of the Msvm\_SyntheticMouse class</span></span>

<span data-ttu-id="a8895-104">Définit la coordonnée z du contrôle de roulette du dispositif de pointage.</span><span class="sxs-lookup"><span data-stu-id="a8895-104">Sets the z-coordinate of the wheel control of the pointing device.</span></span> <span data-ttu-id="a8895-105">Les valeurs écrites dans cette propriété sont toujours des décalages de coordonnées relatives.</span><span class="sxs-lookup"><span data-stu-id="a8895-105">Values written to this property are always relative coordinate offsets.</span></span>

## <a name="syntax"></a><span data-ttu-id="a8895-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a8895-106">Syntax</span></span>


```mof
uint32 SetScrollPosition(
  [in] sint32 scrollPositionDelta
);
```



## <a name="parameters"></a><span data-ttu-id="a8895-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a8895-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a8895-108">*scrollPositionDelta* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="a8895-108">*scrollPositionDelta* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a8895-109">Type : **sint32**</span><span class="sxs-lookup"><span data-stu-id="a8895-109">Type: **sint32**</span></span>

<span data-ttu-id="a8895-110">Delta de la position de défilement.</span><span class="sxs-lookup"><span data-stu-id="a8895-110">The delta of the scroll position.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a8895-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="a8895-111">Return value</span></span>

<span data-ttu-id="a8895-112">Type : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="a8895-112">Type: **uint32**</span></span>

<span data-ttu-id="a8895-113">Une valeur de retour de zéro indique une réussite.</span><span class="sxs-lookup"><span data-stu-id="a8895-113">A return value of zero indicates success.</span></span> <span data-ttu-id="a8895-114">Une valeur différente de zéro indique un échec de modification de la position de défilement.</span><span class="sxs-lookup"><span data-stu-id="a8895-114">A nonzero value indicates a failure to alter the scroll position.</span></span>

<dl> <dt>

<span data-ttu-id="a8895-115">**Terminé sans erreur** (0)</span><span class="sxs-lookup"><span data-stu-id="a8895-115">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="a8895-116">**Paramètres de méthode activés-tâche démarrée** (4096)</span><span class="sxs-lookup"><span data-stu-id="a8895-116">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="a8895-117">**Échec** (32768)</span><span class="sxs-lookup"><span data-stu-id="a8895-117">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="a8895-118">**Accès refusé** (32769)</span><span class="sxs-lookup"><span data-stu-id="a8895-118">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="a8895-119">**Non pris en charge** (32770)</span><span class="sxs-lookup"><span data-stu-id="a8895-119">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="a8895-120">**État inconnu** (32771)</span><span class="sxs-lookup"><span data-stu-id="a8895-120">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="a8895-121">**Délai d’expiration** (32772)</span><span class="sxs-lookup"><span data-stu-id="a8895-121">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="a8895-122">**Paramètre non valide** (32773)</span><span class="sxs-lookup"><span data-stu-id="a8895-122">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="a8895-123">Le **système est en cours d’utilisation** (32774)</span><span class="sxs-lookup"><span data-stu-id="a8895-123">**System is in used** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="a8895-124">**État non valide pour cette opération** (32775)</span><span class="sxs-lookup"><span data-stu-id="a8895-124">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="a8895-125">**Type de données incorrect** (32776)</span><span class="sxs-lookup"><span data-stu-id="a8895-125">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="a8895-126">Le **système n’est pas disponible** (32777)</span><span class="sxs-lookup"><span data-stu-id="a8895-126">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="a8895-127">**Mémoire insuffisante** (32778)</span><span class="sxs-lookup"><span data-stu-id="a8895-127">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="a8895-128">Notes</span><span class="sxs-lookup"><span data-stu-id="a8895-128">Remarks</span></span>

<span data-ttu-id="a8895-129">L’accès à la classe [**MSVM \_ SyntheticMouse**](msvm-syntheticmouse.md) peut être limité par le filtrage UAC.</span><span class="sxs-lookup"><span data-stu-id="a8895-129">Access to the [**Msvm\_SyntheticMouse**](msvm-syntheticmouse.md) class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="a8895-130">Pour plus d’informations, consultez [contrôle de compte d’utilisateur et WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="a8895-130">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="a8895-131">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a8895-131">Requirements</span></span>



| <span data-ttu-id="a8895-132">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a8895-132">Requirement</span></span> | <span data-ttu-id="a8895-133">Valeur</span><span class="sxs-lookup"><span data-stu-id="a8895-133">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a8895-134">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a8895-134">Minimum supported client</span></span><br/> | <span data-ttu-id="a8895-135">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a8895-135">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="a8895-136">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a8895-136">Minimum supported server</span></span><br/> | <span data-ttu-id="a8895-137">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a8895-137">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="a8895-138">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="a8895-138">Namespace</span></span><br/>                | <span data-ttu-id="a8895-139">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="a8895-139">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="a8895-140">MOF</span><span class="sxs-lookup"><span data-stu-id="a8895-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a8895-141"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="a8895-141"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="a8895-142">DLL</span><span class="sxs-lookup"><span data-stu-id="a8895-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a8895-143"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="a8895-143"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="a8895-144">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a8895-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a8895-145">**MSVM \_ SyntheticMouse**</span><span class="sxs-lookup"><span data-stu-id="a8895-145">**Msvm\_SyntheticMouse**</span></span>](msvm-syntheticmouse.md)
</dt> </dl>

 

