---
description: Définit l’état actuel du bouton de périphérique spécifié.
ms.assetid: 942DB31C-09A2-43B6-A666-267AF6A84E0E
title: Méthode SetButtonState de la classe Msvm_SyntheticMouse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SyntheticMouse.SetButtonState
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: c99915fa8ede9cbb405f4483ac10ca9ff8efaf71
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104202762"
---
# <a name="setbuttonstate-method-of-the-msvm_syntheticmouse-class"></a><span data-ttu-id="6fe71-103">Méthode SetButtonState de la \_ classe SyntheticMouse MSVM</span><span class="sxs-lookup"><span data-stu-id="6fe71-103">SetButtonState method of the Msvm\_SyntheticMouse class</span></span>

<span data-ttu-id="6fe71-104">Définit l’état actuel du bouton de périphérique spécifié.</span><span class="sxs-lookup"><span data-stu-id="6fe71-104">Sets the current state of the specified device button.</span></span>

## <a name="syntax"></a><span data-ttu-id="6fe71-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="6fe71-105">Syntax</span></span>


```mof
uint32 SetButtonState(
  [in] uint32  buttonIndex,
  [in] boolean isDown
);
```



## <a name="parameters"></a><span data-ttu-id="6fe71-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="6fe71-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6fe71-107">*buttonIndex* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="6fe71-107">*buttonIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6fe71-108">Type : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="6fe71-108">Type: **uint32**</span></span>

<span data-ttu-id="6fe71-109">Index de base 1 du bouton à modifier.</span><span class="sxs-lookup"><span data-stu-id="6fe71-109">The 1-based index of the button to modify.</span></span>

</dd> <dt>

<span data-ttu-id="6fe71-110">*isDown* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="6fe71-110">*isDown* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6fe71-111">Type : **booléen**</span><span class="sxs-lookup"><span data-stu-id="6fe71-111">Type: **boolean**</span></span>

<span data-ttu-id="6fe71-112">Nouvel état inactif du bouton.</span><span class="sxs-lookup"><span data-stu-id="6fe71-112">The new down state of the button.</span></span> <span data-ttu-id="6fe71-113">Une valeur **true** signifie que le bouton est enfoncé.</span><span class="sxs-lookup"><span data-stu-id="6fe71-113">A **True** value means the button is down.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6fe71-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="6fe71-114">Return value</span></span>

<span data-ttu-id="6fe71-115">Type : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="6fe71-115">Type: **uint32**</span></span>

<span data-ttu-id="6fe71-116">Une valeur différente de zéro indique un échec de modification de l’état du bouton.</span><span class="sxs-lookup"><span data-stu-id="6fe71-116">Non zero values indicate a failure to modify the button state.</span></span>

<dl> <dt>

<span data-ttu-id="6fe71-117">**Terminé sans erreur** (0)</span><span class="sxs-lookup"><span data-stu-id="6fe71-117">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="6fe71-118">**Paramètres de méthode activés-tâche démarrée** (4096)</span><span class="sxs-lookup"><span data-stu-id="6fe71-118">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="6fe71-119">**Échec** (32768)</span><span class="sxs-lookup"><span data-stu-id="6fe71-119">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="6fe71-120">**Accès refusé** (32769)</span><span class="sxs-lookup"><span data-stu-id="6fe71-120">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="6fe71-121">**Non pris en charge** (32770)</span><span class="sxs-lookup"><span data-stu-id="6fe71-121">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="6fe71-122">**État inconnu** (32771)</span><span class="sxs-lookup"><span data-stu-id="6fe71-122">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="6fe71-123">**Délai d’expiration** (32772)</span><span class="sxs-lookup"><span data-stu-id="6fe71-123">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="6fe71-124">**Paramètre non valide** (32773)</span><span class="sxs-lookup"><span data-stu-id="6fe71-124">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="6fe71-125">Le **système est en cours d’utilisation** (32774)</span><span class="sxs-lookup"><span data-stu-id="6fe71-125">**System is in used** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="6fe71-126">**État non valide pour cette opération** (32775)</span><span class="sxs-lookup"><span data-stu-id="6fe71-126">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="6fe71-127">**Type de données incorrect** (32776)</span><span class="sxs-lookup"><span data-stu-id="6fe71-127">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="6fe71-128">Le **système n’est pas disponible** (32777)</span><span class="sxs-lookup"><span data-stu-id="6fe71-128">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="6fe71-129">**Mémoire insuffisante** (32778)</span><span class="sxs-lookup"><span data-stu-id="6fe71-129">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="6fe71-130">Notes</span><span class="sxs-lookup"><span data-stu-id="6fe71-130">Remarks</span></span>

<span data-ttu-id="6fe71-131">L’accès à la classe [**MSVM \_ SyntheticMouse**](msvm-syntheticmouse.md) peut être limité par le filtrage UAC.</span><span class="sxs-lookup"><span data-stu-id="6fe71-131">Access to the [**Msvm\_SyntheticMouse**](msvm-syntheticmouse.md) class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="6fe71-132">Pour plus d’informations, consultez [contrôle de compte d’utilisateur et WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="6fe71-132">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="6fe71-133">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="6fe71-133">Requirements</span></span>



| <span data-ttu-id="6fe71-134">Condition requise</span><span class="sxs-lookup"><span data-stu-id="6fe71-134">Requirement</span></span> | <span data-ttu-id="6fe71-135">Valeur</span><span class="sxs-lookup"><span data-stu-id="6fe71-135">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6fe71-136">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6fe71-136">Minimum supported client</span></span><br/> | <span data-ttu-id="6fe71-137">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="6fe71-137">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="6fe71-138">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6fe71-138">Minimum supported server</span></span><br/> | <span data-ttu-id="6fe71-139">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="6fe71-139">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="6fe71-140">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="6fe71-140">Namespace</span></span><br/>                | <span data-ttu-id="6fe71-141">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="6fe71-141">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="6fe71-142">MOF</span><span class="sxs-lookup"><span data-stu-id="6fe71-142">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6fe71-143"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="6fe71-143"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="6fe71-144">DLL</span><span class="sxs-lookup"><span data-stu-id="6fe71-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6fe71-145"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="6fe71-145"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="6fe71-146">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6fe71-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6fe71-147">**MSVM \_ SyntheticMouse**</span><span class="sxs-lookup"><span data-stu-id="6fe71-147">**Msvm\_SyntheticMouse**</span></span>](msvm-syntheticmouse.md)
</dt> </dl>

 

