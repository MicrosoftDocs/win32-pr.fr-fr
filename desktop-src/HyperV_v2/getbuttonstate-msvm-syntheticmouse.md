---
description: Récupère l’état actuel du bouton de périphérique spécifié.
ms.assetid: 66363AF1-E360-478D-8E62-513DE66EF130
title: Méthode GetButtonState de la classe Msvm_SyntheticMouse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SyntheticMouse.GetButtonState
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 3812d3e019a303656305471fc097fb1479fa1ada
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106531667"
---
# <a name="getbuttonstate-method-of-the-msvm_syntheticmouse-class"></a><span data-ttu-id="77136-103">Méthode GetButtonState de la \_ classe SyntheticMouse MSVM</span><span class="sxs-lookup"><span data-stu-id="77136-103">GetButtonState method of the Msvm\_SyntheticMouse class</span></span>

<span data-ttu-id="77136-104">Récupère l’état actuel du bouton de périphérique spécifié.</span><span class="sxs-lookup"><span data-stu-id="77136-104">Retrieves the current state of the specified device button.</span></span>

## <a name="syntax"></a><span data-ttu-id="77136-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="77136-105">Syntax</span></span>


```mof
uint32 GetButtonState(
  [in]  uint32  buttonIndex,
  [out] boolean isDown
);
```



## <a name="parameters"></a><span data-ttu-id="77136-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="77136-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="77136-107">*buttonIndex* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="77136-107">*buttonIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="77136-108">Type : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="77136-108">Type: **uint32**</span></span>

<span data-ttu-id="77136-109">Index de base 1 du bouton à interroger.</span><span class="sxs-lookup"><span data-stu-id="77136-109">The 1-based index of the button to query.</span></span>

</dd> <dt>

<span data-ttu-id="77136-110">*isDown* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="77136-110">*isDown* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="77136-111">Type : **booléen**</span><span class="sxs-lookup"><span data-stu-id="77136-111">Type: **boolean**</span></span>

<span data-ttu-id="77136-112">État actuel du bouton enfoncé.</span><span class="sxs-lookup"><span data-stu-id="77136-112">The current down state of the button.</span></span> <span data-ttu-id="77136-113">Une valeur **true** signifie que le bouton est enfoncé.</span><span class="sxs-lookup"><span data-stu-id="77136-113">A **True** value means the button is down.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="77136-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="77136-114">Return value</span></span>

<span data-ttu-id="77136-115">Type : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="77136-115">Type: **uint32**</span></span>

<span data-ttu-id="77136-116">Une valeur de retour de zéro indique une réussite.</span><span class="sxs-lookup"><span data-stu-id="77136-116">A return value of zero indicates success.</span></span> <span data-ttu-id="77136-117">Une valeur différente de zéro indique un échec de requête.</span><span class="sxs-lookup"><span data-stu-id="77136-117">A nonzero value indicates a query failure.</span></span>

<dl> <dt>

<span data-ttu-id="77136-118">**Terminé sans erreur** (0)</span><span class="sxs-lookup"><span data-stu-id="77136-118">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="77136-119">**Paramètres de méthode activés-tâche démarrée** (4096)</span><span class="sxs-lookup"><span data-stu-id="77136-119">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="77136-120">**Échec** (32768)</span><span class="sxs-lookup"><span data-stu-id="77136-120">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="77136-121">**Accès refusé** (32769)</span><span class="sxs-lookup"><span data-stu-id="77136-121">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="77136-122">**Non pris en charge** (32770)</span><span class="sxs-lookup"><span data-stu-id="77136-122">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="77136-123">**État inconnu** (32771)</span><span class="sxs-lookup"><span data-stu-id="77136-123">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="77136-124">**Délai d’expiration** (32772)</span><span class="sxs-lookup"><span data-stu-id="77136-124">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="77136-125">**Paramètre non valide** (32773)</span><span class="sxs-lookup"><span data-stu-id="77136-125">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="77136-126">Le **système est en cours d’utilisation** (32774)</span><span class="sxs-lookup"><span data-stu-id="77136-126">**System is in used** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="77136-127">**État non valide pour cette opération** (32775)</span><span class="sxs-lookup"><span data-stu-id="77136-127">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="77136-128">**Type de données incorrect** (32776)</span><span class="sxs-lookup"><span data-stu-id="77136-128">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="77136-129">Le **système n’est pas disponible** (32777)</span><span class="sxs-lookup"><span data-stu-id="77136-129">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="77136-130">**Mémoire insuffisante** (32778)</span><span class="sxs-lookup"><span data-stu-id="77136-130">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="77136-131">Notes</span><span class="sxs-lookup"><span data-stu-id="77136-131">Remarks</span></span>

<span data-ttu-id="77136-132">L’accès à la classe [**MSVM \_ SyntheticMouse**](msvm-syntheticmouse.md) peut être limité par le filtrage UAC.</span><span class="sxs-lookup"><span data-stu-id="77136-132">Access to the [**Msvm\_SyntheticMouse**](msvm-syntheticmouse.md) class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="77136-133">Pour plus d’informations, consultez [contrôle de compte d’utilisateur et WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="77136-133">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="77136-134">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="77136-134">Requirements</span></span>



| <span data-ttu-id="77136-135">Condition requise</span><span class="sxs-lookup"><span data-stu-id="77136-135">Requirement</span></span> | <span data-ttu-id="77136-136">Valeur</span><span class="sxs-lookup"><span data-stu-id="77136-136">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="77136-137">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="77136-137">Minimum supported client</span></span><br/> | <span data-ttu-id="77136-138">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="77136-138">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="77136-139">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="77136-139">Minimum supported server</span></span><br/> | <span data-ttu-id="77136-140">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="77136-140">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="77136-141">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="77136-141">Namespace</span></span><br/>                | <span data-ttu-id="77136-142">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="77136-142">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="77136-143">MOF</span><span class="sxs-lookup"><span data-stu-id="77136-143">MOF</span></span><br/>                      | <dl> <span data-ttu-id="77136-144"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="77136-144"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="77136-145">DLL</span><span class="sxs-lookup"><span data-stu-id="77136-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="77136-146"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="77136-146"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="77136-147">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="77136-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="77136-148">**MSVM \_ SyntheticMouse**</span><span class="sxs-lookup"><span data-stu-id="77136-148">**Msvm\_SyntheticMouse**</span></span>](msvm-syntheticmouse.md)
</dt> </dl>

 

