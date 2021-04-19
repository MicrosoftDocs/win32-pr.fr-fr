---
description: Définit l’état actuel du bouton de périphérique spécifié.
ms.assetid: 312A2B8B-D518-4797-9B50-F12493598CD6
title: Méthode SetButtonState de la classe Msvm_Ps2Mouse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_Ps2Mouse.SetButtonState
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 34475edfa27d08cbe9de488502686a84e4391eb8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106518243"
---
# <a name="setbuttonstate-method-of-the-msvm_ps2mouse-class"></a><span data-ttu-id="69234-103">Méthode SetButtonState de la \_ classe Ps2Mouse MSVM</span><span class="sxs-lookup"><span data-stu-id="69234-103">SetButtonState method of the Msvm\_Ps2Mouse class</span></span>

<span data-ttu-id="69234-104">Définit l’état actuel du bouton de périphérique spécifié.</span><span class="sxs-lookup"><span data-stu-id="69234-104">Sets the current state of the specified device button.</span></span>

## <a name="syntax"></a><span data-ttu-id="69234-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="69234-105">Syntax</span></span>


```mof
uint32 SetButtonState(
  [in] uint32  buttonIndex,
  [in] boolean buttonState
);
```



## <a name="parameters"></a><span data-ttu-id="69234-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="69234-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="69234-107">*buttonIndex* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="69234-107">*buttonIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="69234-108">Type : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="69234-108">Type: **uint32**</span></span>

<span data-ttu-id="69234-109">Index de base 1 du bouton à modifier.</span><span class="sxs-lookup"><span data-stu-id="69234-109">The 1-based index of the button to modify.</span></span>

</dd> <dt>

<span data-ttu-id="69234-110">*ButtonState* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="69234-110">*buttonState* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="69234-111">Type : **booléen**</span><span class="sxs-lookup"><span data-stu-id="69234-111">Type: **boolean**</span></span>

<span data-ttu-id="69234-112">Nouvel état inactif du bouton.</span><span class="sxs-lookup"><span data-stu-id="69234-112">The new down state of the button.</span></span> <span data-ttu-id="69234-113">Une valeur **true** signifie que le bouton est enfoncé.</span><span class="sxs-lookup"><span data-stu-id="69234-113">A **True** value means the button is down.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="69234-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="69234-114">Return value</span></span>

<span data-ttu-id="69234-115">Type : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="69234-115">Type: **uint32**</span></span>

<span data-ttu-id="69234-116">Une valeur de retour de zéro indique une réussite.</span><span class="sxs-lookup"><span data-stu-id="69234-116">A return value of zero indicates success.</span></span> <span data-ttu-id="69234-117">Une valeur différente de zéro indique un échec de modification de l’état du bouton.</span><span class="sxs-lookup"><span data-stu-id="69234-117">A nonzero value indicates a failure to modify the button state.</span></span>

<dl> <dt>

<span data-ttu-id="69234-118">**Terminé sans erreur** (0)</span><span class="sxs-lookup"><span data-stu-id="69234-118">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="69234-119">**Paramètres de méthode activés-tâche démarrée** (4096)</span><span class="sxs-lookup"><span data-stu-id="69234-119">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="69234-120">**Échec** (32768)</span><span class="sxs-lookup"><span data-stu-id="69234-120">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="69234-121">**Accès refusé** (32769)</span><span class="sxs-lookup"><span data-stu-id="69234-121">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="69234-122">**Non pris en charge** (32770)</span><span class="sxs-lookup"><span data-stu-id="69234-122">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="69234-123">**État inconnu** (32771)</span><span class="sxs-lookup"><span data-stu-id="69234-123">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="69234-124">**Délai d’expiration** (32772)</span><span class="sxs-lookup"><span data-stu-id="69234-124">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="69234-125">**Paramètre non valide** (32773)</span><span class="sxs-lookup"><span data-stu-id="69234-125">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="69234-126">Le **système est en cours d’utilisation** (32774)</span><span class="sxs-lookup"><span data-stu-id="69234-126">**System is in used** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="69234-127">**État non valide pour cette opération** (32775)</span><span class="sxs-lookup"><span data-stu-id="69234-127">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="69234-128">**Type de données incorrect** (32776)</span><span class="sxs-lookup"><span data-stu-id="69234-128">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="69234-129">Le **système n’est pas disponible** (32777)</span><span class="sxs-lookup"><span data-stu-id="69234-129">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="69234-130">**Mémoire insuffisante** (32778)</span><span class="sxs-lookup"><span data-stu-id="69234-130">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="69234-131">Notes</span><span class="sxs-lookup"><span data-stu-id="69234-131">Remarks</span></span>

<span data-ttu-id="69234-132">L’accès à la classe [**MSVM \_ Ps2Mouse**](msvm-ps2mouse.md) peut être limité par le filtrage UAC.</span><span class="sxs-lookup"><span data-stu-id="69234-132">Access to the [**Msvm\_Ps2Mouse**](msvm-ps2mouse.md) class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="69234-133">Pour plus d’informations, consultez [contrôle de compte d’utilisateur et WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="69234-133">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="69234-134">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="69234-134">Requirements</span></span>



| <span data-ttu-id="69234-135">Condition requise</span><span class="sxs-lookup"><span data-stu-id="69234-135">Requirement</span></span> | <span data-ttu-id="69234-136">Valeur</span><span class="sxs-lookup"><span data-stu-id="69234-136">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="69234-137">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="69234-137">Minimum supported client</span></span><br/> | <span data-ttu-id="69234-138">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="69234-138">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="69234-139">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="69234-139">Minimum supported server</span></span><br/> | <span data-ttu-id="69234-140">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="69234-140">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="69234-141">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="69234-141">Namespace</span></span><br/>                | <span data-ttu-id="69234-142">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="69234-142">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="69234-143">MOF</span><span class="sxs-lookup"><span data-stu-id="69234-143">MOF</span></span><br/>                      | <dl> <span data-ttu-id="69234-144"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="69234-144"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="69234-145">DLL</span><span class="sxs-lookup"><span data-stu-id="69234-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="69234-146"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="69234-146"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="69234-147">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="69234-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="69234-148">**MSVM \_ Ps2Mouse**</span><span class="sxs-lookup"><span data-stu-id="69234-148">**Msvm\_Ps2Mouse**</span></span>](msvm-ps2mouse.md)
</dt> </dl>

 

