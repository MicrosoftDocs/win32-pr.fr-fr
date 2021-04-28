---
description: Méthode SetButtonState de la classe Msvm_SyntheticMouse-définit l’état actuel du bouton de périphérique spécifié.
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
ms.openlocfilehash: 161520ac1b7e9dba1a084a8fb3c623155aa135fe
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108109207"
---
# <a name="setbuttonstate-method-of-the-msvm_syntheticmouse-class"></a><span data-ttu-id="0a4f7-103">Méthode SetButtonState de la \_ classe SyntheticMouse MSVM</span><span class="sxs-lookup"><span data-stu-id="0a4f7-103">SetButtonState method of the Msvm\_SyntheticMouse class</span></span>

<span data-ttu-id="0a4f7-104">Définit l’état actuel du bouton de périphérique spécifié.</span><span class="sxs-lookup"><span data-stu-id="0a4f7-104">Sets the current state of the specified device button.</span></span>

## <a name="syntax"></a><span data-ttu-id="0a4f7-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0a4f7-105">Syntax</span></span>


```mof
uint32 SetButtonState(
  [in] uint32  buttonIndex,
  [in] boolean isDown
);
```



## <a name="parameters"></a><span data-ttu-id="0a4f7-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="0a4f7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0a4f7-107">*buttonIndex* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="0a4f7-107">*buttonIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0a4f7-108">Type : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="0a4f7-108">Type: **uint32**</span></span>

<span data-ttu-id="0a4f7-109">Index de base 1 du bouton à modifier.</span><span class="sxs-lookup"><span data-stu-id="0a4f7-109">The 1-based index of the button to modify.</span></span>

</dd> <dt>

<span data-ttu-id="0a4f7-110">*isDown* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="0a4f7-110">*isDown* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0a4f7-111">Type : **booléen**</span><span class="sxs-lookup"><span data-stu-id="0a4f7-111">Type: **boolean**</span></span>

<span data-ttu-id="0a4f7-112">Nouvel état inactif du bouton.</span><span class="sxs-lookup"><span data-stu-id="0a4f7-112">The new down state of the button.</span></span> <span data-ttu-id="0a4f7-113">Une valeur **true** signifie que le bouton est enfoncé.</span><span class="sxs-lookup"><span data-stu-id="0a4f7-113">A **True** value means the button is down.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0a4f7-114">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="0a4f7-114">Return value</span></span>

<span data-ttu-id="0a4f7-115">Type : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="0a4f7-115">Type: **uint32**</span></span>

<span data-ttu-id="0a4f7-116">Une valeur différente de zéro indique un échec de modification de l’état du bouton.</span><span class="sxs-lookup"><span data-stu-id="0a4f7-116">Non zero values indicate a failure to modify the button state.</span></span>

<dl> <dt>

<span data-ttu-id="0a4f7-117">**Terminé sans erreur** (0)</span><span class="sxs-lookup"><span data-stu-id="0a4f7-117">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="0a4f7-118">**Paramètres de méthode activés-tâche démarrée** (4096)</span><span class="sxs-lookup"><span data-stu-id="0a4f7-118">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="0a4f7-119">**Échec** (32768)</span><span class="sxs-lookup"><span data-stu-id="0a4f7-119">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="0a4f7-120">**Accès refusé** (32769)</span><span class="sxs-lookup"><span data-stu-id="0a4f7-120">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="0a4f7-121">**Non pris en charge** (32770)</span><span class="sxs-lookup"><span data-stu-id="0a4f7-121">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="0a4f7-122">**État inconnu** (32771)</span><span class="sxs-lookup"><span data-stu-id="0a4f7-122">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="0a4f7-123">**Délai d’expiration** (32772)</span><span class="sxs-lookup"><span data-stu-id="0a4f7-123">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="0a4f7-124">**Paramètre non valide** (32773)</span><span class="sxs-lookup"><span data-stu-id="0a4f7-124">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="0a4f7-125">Le **système est en cours d’utilisation** (32774)</span><span class="sxs-lookup"><span data-stu-id="0a4f7-125">**System is in used** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="0a4f7-126">**État non valide pour cette opération** (32775)</span><span class="sxs-lookup"><span data-stu-id="0a4f7-126">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="0a4f7-127">**Type de données incorrect** (32776)</span><span class="sxs-lookup"><span data-stu-id="0a4f7-127">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="0a4f7-128">Le **système n’est pas disponible** (32777)</span><span class="sxs-lookup"><span data-stu-id="0a4f7-128">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="0a4f7-129">**Mémoire insuffisante** (32778)</span><span class="sxs-lookup"><span data-stu-id="0a4f7-129">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="0a4f7-130">Notes </span><span class="sxs-lookup"><span data-stu-id="0a4f7-130">Remarks</span></span>

<span data-ttu-id="0a4f7-131">L’accès à la classe [**MSVM \_ SyntheticMouse**](msvm-syntheticmouse.md) peut être limité par le filtrage UAC.</span><span class="sxs-lookup"><span data-stu-id="0a4f7-131">Access to the [**Msvm\_SyntheticMouse**](msvm-syntheticmouse.md) class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="0a4f7-132">Pour plus d’informations, consultez [contrôle de compte d’utilisateur et WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="0a4f7-132">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="0a4f7-133">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0a4f7-133">Requirements</span></span>



| <span data-ttu-id="0a4f7-134">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0a4f7-134">Requirement</span></span> | <span data-ttu-id="0a4f7-135">Valeur</span><span class="sxs-lookup"><span data-stu-id="0a4f7-135">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0a4f7-136">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0a4f7-136">Minimum supported client</span></span><br/> | <span data-ttu-id="0a4f7-137">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="0a4f7-137">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="0a4f7-138">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0a4f7-138">Minimum supported server</span></span><br/> | <span data-ttu-id="0a4f7-139">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="0a4f7-139">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="0a4f7-140">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="0a4f7-140">Namespace</span></span><br/>                | <span data-ttu-id="0a4f7-141">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="0a4f7-141">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="0a4f7-142">MOF</span><span class="sxs-lookup"><span data-stu-id="0a4f7-142">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0a4f7-143"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="0a4f7-143"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="0a4f7-144">DLL</span><span class="sxs-lookup"><span data-stu-id="0a4f7-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0a4f7-145"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="0a4f7-145"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="0a4f7-146">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0a4f7-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0a4f7-147">**MSVM \_ SyntheticMouse**</span><span class="sxs-lookup"><span data-stu-id="0a4f7-147">**Msvm\_SyntheticMouse**</span></span>](msvm-syntheticmouse.md)
</dt> </dl>

 

