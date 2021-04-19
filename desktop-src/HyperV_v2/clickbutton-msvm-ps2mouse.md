---
description: Simule un clic sur le bouton de périphérique spécifié.
ms.assetid: 77CFA2E9-E422-464C-B124-6F7D3D56BA4C
title: Méthode ClickButton de la classe Msvm_Ps2Mouse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_Ps2Mouse.ClickButton
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: ffaded2a5e9a8e4e37a158e3aa91b27520dff2b7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106521514"
---
# <a name="clickbutton-method-of-the-msvm_ps2mouse-class"></a><span data-ttu-id="7cd6e-103">Méthode ClickButton de la \_ classe Ps2Mouse MSVM</span><span class="sxs-lookup"><span data-stu-id="7cd6e-103">ClickButton method of the Msvm\_Ps2Mouse class</span></span>

<span data-ttu-id="7cd6e-104">Simule un clic sur le bouton de périphérique spécifié.</span><span class="sxs-lookup"><span data-stu-id="7cd6e-104">Simulates a click of the specified device button.</span></span> <span data-ttu-id="7cd6e-105">Cela équivaut à appeler [**SetButtonState**](setbuttonstate-msvm-syntheticmouse.md) deux fois, d’abord à appuyer sur le bouton, puis à le libérer.</span><span class="sxs-lookup"><span data-stu-id="7cd6e-105">This is equivalent to calling [**SetButtonState**](setbuttonstate-msvm-syntheticmouse.md) twice, first to press the button, and again to release it.</span></span>

## <a name="syntax"></a><span data-ttu-id="7cd6e-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7cd6e-106">Syntax</span></span>


```mof
uint32 ClickButton(
  [in] uint32 buttonIndex
);
```



## <a name="parameters"></a><span data-ttu-id="7cd6e-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="7cd6e-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7cd6e-108">*buttonIndex* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="7cd6e-108">*buttonIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7cd6e-109">Type : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="7cd6e-109">Type: **uint32**</span></span>

<span data-ttu-id="7cd6e-110">Index de base 1 du bouton.</span><span class="sxs-lookup"><span data-stu-id="7cd6e-110">The 1-based index of the button.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7cd6e-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="7cd6e-111">Return value</span></span>

<span data-ttu-id="7cd6e-112">Type : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="7cd6e-112">Type: **uint32**</span></span>

<span data-ttu-id="7cd6e-113">Une valeur de retour de zéro indique une réussite.</span><span class="sxs-lookup"><span data-stu-id="7cd6e-113">A return value of zero indicates success.</span></span> <span data-ttu-id="7cd6e-114">Une valeur différente de zéro indique un échec de modification de l’état du bouton.</span><span class="sxs-lookup"><span data-stu-id="7cd6e-114">A nonzero value indicates a failure to modify the button state.</span></span>

<dl> <dt>

<span data-ttu-id="7cd6e-115">**Terminé sans erreur** (0)</span><span class="sxs-lookup"><span data-stu-id="7cd6e-115">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="7cd6e-116">**Paramètres de méthode activés-tâche démarrée** (4096)</span><span class="sxs-lookup"><span data-stu-id="7cd6e-116">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="7cd6e-117">**Échec** (32768)</span><span class="sxs-lookup"><span data-stu-id="7cd6e-117">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="7cd6e-118">**Accès refusé** (32769)</span><span class="sxs-lookup"><span data-stu-id="7cd6e-118">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="7cd6e-119">**Non pris en charge** (32770)</span><span class="sxs-lookup"><span data-stu-id="7cd6e-119">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="7cd6e-120">**État inconnu** (32771)</span><span class="sxs-lookup"><span data-stu-id="7cd6e-120">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="7cd6e-121">**Délai d’expiration** (32772)</span><span class="sxs-lookup"><span data-stu-id="7cd6e-121">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="7cd6e-122">**Paramètre non valide** (32773)</span><span class="sxs-lookup"><span data-stu-id="7cd6e-122">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="7cd6e-123">Le **système est en cours d’utilisation** (32774)</span><span class="sxs-lookup"><span data-stu-id="7cd6e-123">**System is in used** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="7cd6e-124">**État non valide pour cette opération** (32775)</span><span class="sxs-lookup"><span data-stu-id="7cd6e-124">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="7cd6e-125">**Type de données incorrect** (32776)</span><span class="sxs-lookup"><span data-stu-id="7cd6e-125">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="7cd6e-126">Le **système n’est pas disponible** (32777)</span><span class="sxs-lookup"><span data-stu-id="7cd6e-126">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="7cd6e-127">**Mémoire insuffisante** (32778)</span><span class="sxs-lookup"><span data-stu-id="7cd6e-127">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="7cd6e-128">Notes</span><span class="sxs-lookup"><span data-stu-id="7cd6e-128">Remarks</span></span>

<span data-ttu-id="7cd6e-129">L’accès à la classe [**MSVM \_ Ps2Mouse**](msvm-ps2mouse.md) peut être limité par le filtrage UAC.</span><span class="sxs-lookup"><span data-stu-id="7cd6e-129">Access to the [**Msvm\_Ps2Mouse**](msvm-ps2mouse.md) class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="7cd6e-130">Pour plus d’informations, consultez [contrôle de compte d’utilisateur et WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="7cd6e-130">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="7cd6e-131">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7cd6e-131">Requirements</span></span>



| <span data-ttu-id="7cd6e-132">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7cd6e-132">Requirement</span></span> | <span data-ttu-id="7cd6e-133">Valeur</span><span class="sxs-lookup"><span data-stu-id="7cd6e-133">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7cd6e-134">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7cd6e-134">Minimum supported client</span></span><br/> | <span data-ttu-id="7cd6e-135">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="7cd6e-135">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="7cd6e-136">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7cd6e-136">Minimum supported server</span></span><br/> | <span data-ttu-id="7cd6e-137">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="7cd6e-137">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="7cd6e-138">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="7cd6e-138">Namespace</span></span><br/>                | <span data-ttu-id="7cd6e-139">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="7cd6e-139">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="7cd6e-140">MOF</span><span class="sxs-lookup"><span data-stu-id="7cd6e-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="7cd6e-141"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="7cd6e-141"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="7cd6e-142">DLL</span><span class="sxs-lookup"><span data-stu-id="7cd6e-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7cd6e-143"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="7cd6e-143"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="7cd6e-144">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7cd6e-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7cd6e-145">**MSVM \_ Ps2Mouse**</span><span class="sxs-lookup"><span data-stu-id="7cd6e-145">**Msvm\_Ps2Mouse**</span></span>](msvm-ps2mouse.md)
</dt> </dl>

 

