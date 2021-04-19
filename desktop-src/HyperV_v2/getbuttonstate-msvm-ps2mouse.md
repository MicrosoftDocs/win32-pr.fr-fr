---
description: Récupère l’état actuel du bouton de périphérique spécifié.
ms.assetid: 7772A3AC-1677-44A7-9E5E-D31E90988705
title: Méthode GetButtonState de la classe Msvm_Ps2Mouse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_Ps2Mouse.GetButtonState
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 8bb0df6ad49f0d260d95c6f65e0f0f481b393dc3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106515271"
---
# <a name="getbuttonstate-method-of-the-msvm_ps2mouse-class"></a><span data-ttu-id="8d2d0-103">Méthode GetButtonState de la \_ classe Ps2Mouse MSVM</span><span class="sxs-lookup"><span data-stu-id="8d2d0-103">GetButtonState method of the Msvm\_Ps2Mouse class</span></span>

<span data-ttu-id="8d2d0-104">Récupère l’état actuel du bouton de périphérique spécifié.</span><span class="sxs-lookup"><span data-stu-id="8d2d0-104">Retrieves the current state of the specified device button.</span></span>

## <a name="syntax"></a><span data-ttu-id="8d2d0-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="8d2d0-105">Syntax</span></span>


```mof
uint32 GetButtonState(
  [in]  uint32  buttonIndex,
  [out] boolean buttonState
);
```



## <a name="parameters"></a><span data-ttu-id="8d2d0-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="8d2d0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8d2d0-107">*buttonIndex* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="8d2d0-107">*buttonIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8d2d0-108">Type : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="8d2d0-108">Type: **uint32**</span></span>

<span data-ttu-id="8d2d0-109">Index de base 1 du bouton à interroger.</span><span class="sxs-lookup"><span data-stu-id="8d2d0-109">The 1-based index of the button to query.</span></span>

</dd> <dt>

<span data-ttu-id="8d2d0-110">*ButtonState* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="8d2d0-110">*buttonState* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8d2d0-111">Type : **booléen**</span><span class="sxs-lookup"><span data-stu-id="8d2d0-111">Type: **boolean**</span></span>

<span data-ttu-id="8d2d0-112">État actuel du bouton enfoncé.</span><span class="sxs-lookup"><span data-stu-id="8d2d0-112">The current down state of the button.</span></span> <span data-ttu-id="8d2d0-113">Une valeur **true** signifie que le bouton est enfoncé.</span><span class="sxs-lookup"><span data-stu-id="8d2d0-113">A **True** value means the button is down.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8d2d0-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="8d2d0-114">Return value</span></span>

<span data-ttu-id="8d2d0-115">Type : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="8d2d0-115">Type: **uint32**</span></span>

<span data-ttu-id="8d2d0-116">Une valeur de retour de zéro indique une réussite.</span><span class="sxs-lookup"><span data-stu-id="8d2d0-116">A return value of zero indicates success.</span></span> <span data-ttu-id="8d2d0-117">Une valeur différente de zéro indique un échec de requête.</span><span class="sxs-lookup"><span data-stu-id="8d2d0-117">A nonzero value indicates a query failure.</span></span>

<dl> <dt>

<span data-ttu-id="8d2d0-118">**Terminé sans erreur** (0)</span><span class="sxs-lookup"><span data-stu-id="8d2d0-118">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="8d2d0-119">**Paramètres de méthode activés-tâche démarrée** (4096)</span><span class="sxs-lookup"><span data-stu-id="8d2d0-119">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="8d2d0-120">**Échec** (32768)</span><span class="sxs-lookup"><span data-stu-id="8d2d0-120">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="8d2d0-121">**Accès refusé** (32769)</span><span class="sxs-lookup"><span data-stu-id="8d2d0-121">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="8d2d0-122">**Non pris en charge** (32770)</span><span class="sxs-lookup"><span data-stu-id="8d2d0-122">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="8d2d0-123">**État inconnu** (32771)</span><span class="sxs-lookup"><span data-stu-id="8d2d0-123">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="8d2d0-124">**Délai d’expiration** (32772)</span><span class="sxs-lookup"><span data-stu-id="8d2d0-124">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="8d2d0-125">**Paramètre non valide** (32773)</span><span class="sxs-lookup"><span data-stu-id="8d2d0-125">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="8d2d0-126">Le **système est en cours d’utilisation** (32774)</span><span class="sxs-lookup"><span data-stu-id="8d2d0-126">**System is in used** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="8d2d0-127">**État non valide pour cette opération** (32775)</span><span class="sxs-lookup"><span data-stu-id="8d2d0-127">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="8d2d0-128">**Type de données incorrect** (32776)</span><span class="sxs-lookup"><span data-stu-id="8d2d0-128">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="8d2d0-129">Le **système n’est pas disponible** (32777)</span><span class="sxs-lookup"><span data-stu-id="8d2d0-129">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="8d2d0-130">**Mémoire insuffisante** (32778)</span><span class="sxs-lookup"><span data-stu-id="8d2d0-130">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="8d2d0-131">Notes</span><span class="sxs-lookup"><span data-stu-id="8d2d0-131">Remarks</span></span>

<span data-ttu-id="8d2d0-132">L’accès à la classe [**MSVM \_ Ps2Mouse**](msvm-ps2mouse.md) peut être limité par le filtrage UAC.</span><span class="sxs-lookup"><span data-stu-id="8d2d0-132">Access to the [**Msvm\_Ps2Mouse**](msvm-ps2mouse.md) class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="8d2d0-133">Pour plus d’informations, consultez [contrôle de compte d’utilisateur et WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="8d2d0-133">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="8d2d0-134">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8d2d0-134">Requirements</span></span>



| <span data-ttu-id="8d2d0-135">Condition requise</span><span class="sxs-lookup"><span data-stu-id="8d2d0-135">Requirement</span></span> | <span data-ttu-id="8d2d0-136">Valeur</span><span class="sxs-lookup"><span data-stu-id="8d2d0-136">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8d2d0-137">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8d2d0-137">Minimum supported client</span></span><br/> | <span data-ttu-id="8d2d0-138">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="8d2d0-138">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="8d2d0-139">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8d2d0-139">Minimum supported server</span></span><br/> | <span data-ttu-id="8d2d0-140">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="8d2d0-140">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="8d2d0-141">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="8d2d0-141">Namespace</span></span><br/>                | <span data-ttu-id="8d2d0-142">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="8d2d0-142">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="8d2d0-143">MOF</span><span class="sxs-lookup"><span data-stu-id="8d2d0-143">MOF</span></span><br/>                      | <dl> <span data-ttu-id="8d2d0-144"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="8d2d0-144"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="8d2d0-145">DLL</span><span class="sxs-lookup"><span data-stu-id="8d2d0-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8d2d0-146"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="8d2d0-146"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="8d2d0-147">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8d2d0-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8d2d0-148">**MSVM \_ Ps2Mouse**</span><span class="sxs-lookup"><span data-stu-id="8d2d0-148">**Msvm\_Ps2Mouse**</span></span>](msvm-ps2mouse.md)
</dt> </dl>

 

