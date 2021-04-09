---
description: Récupère l’état de clé d’une clé.
ms.assetid: 4AEB732D-274E-42BB-AA97-9E4D30B81338
title: Méthode IsKeyPressed de la classe Msvm_Keyboard
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_Keyboard.IsKeyPressed
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 44af7a3dc82c0d4d20a2e4c6aff21f7a47837490
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104201969"
---
# <a name="iskeypressed-method-of-the-msvm_keyboard-class"></a><span data-ttu-id="c1cfc-103">Méthode IsKeyPressed de la \_ classe de clavier MSVM</span><span class="sxs-lookup"><span data-stu-id="c1cfc-103">IsKeyPressed method of the Msvm\_Keyboard class</span></span>

<span data-ttu-id="c1cfc-104">Récupère l’état de clé d’une clé.</span><span class="sxs-lookup"><span data-stu-id="c1cfc-104">Retrieves the key state of a key.</span></span>

## <a name="syntax"></a><span data-ttu-id="c1cfc-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c1cfc-105">Syntax</span></span>


```mof
uint32 IsKeyPressed(
  [in]  uint32  keyCode,
  [out] boolean keyState
);
```



## <a name="parameters"></a><span data-ttu-id="c1cfc-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c1cfc-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c1cfc-107">*keyCode* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="c1cfc-107">*keyCode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c1cfc-108">Type : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c1cfc-108">Type: **uint32**</span></span>

<span data-ttu-id="c1cfc-109">Code de la clé virtuelle de la clé à interroger.</span><span class="sxs-lookup"><span data-stu-id="c1cfc-109">The virtual key code of the key to query.</span></span> <span data-ttu-id="c1cfc-110">Pour obtenir la liste des codes de touche virtuelle, consultez la page [**codes de clé virtuelle**](../inputdev/virtual-key-codes.md).</span><span class="sxs-lookup"><span data-stu-id="c1cfc-110">For the list for virtual-key codes, see [**Virtual-Key Codes**](../inputdev/virtual-key-codes.md).</span></span>

</dd> <dt>

<span data-ttu-id="c1cfc-111">*KeyState* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="c1cfc-111">*keyState* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c1cfc-112">Type : **booléen**</span><span class="sxs-lookup"><span data-stu-id="c1cfc-112">Type: **boolean**</span></span>

<span data-ttu-id="c1cfc-113">État actuel de la partie inférieure de la clé.</span><span class="sxs-lookup"><span data-stu-id="c1cfc-113">The current down state of the key.</span></span> <span data-ttu-id="c1cfc-114">Une valeur **true** signifie que la touche est enfoncée.</span><span class="sxs-lookup"><span data-stu-id="c1cfc-114">A **True** value means the key is down.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c1cfc-115">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="c1cfc-115">Return value</span></span>

<span data-ttu-id="c1cfc-116">Type : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c1cfc-116">Type: **uint32**</span></span>

<span data-ttu-id="c1cfc-117">Une valeur de retour de zéro indique une réussite.</span><span class="sxs-lookup"><span data-stu-id="c1cfc-117">A return value of zero indicates success.</span></span> <span data-ttu-id="c1cfc-118">Une valeur différente de zéro indique un échec d’interrogation de l’état de la clé.</span><span class="sxs-lookup"><span data-stu-id="c1cfc-118">A nonzero value indicates a failure to query the key state.</span></span>

<dl> <dt>

<span data-ttu-id="c1cfc-119">**Terminé sans erreur** (0)</span><span class="sxs-lookup"><span data-stu-id="c1cfc-119">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="c1cfc-120">**Paramètres de méthode activés-tâche démarrée** (4096)</span><span class="sxs-lookup"><span data-stu-id="c1cfc-120">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="c1cfc-121">**Échec** (32768)</span><span class="sxs-lookup"><span data-stu-id="c1cfc-121">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="c1cfc-122">**Accès refusé** (32769)</span><span class="sxs-lookup"><span data-stu-id="c1cfc-122">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="c1cfc-123">**Non pris en charge** (32770)</span><span class="sxs-lookup"><span data-stu-id="c1cfc-123">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="c1cfc-124">**État inconnu** (32771)</span><span class="sxs-lookup"><span data-stu-id="c1cfc-124">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="c1cfc-125">**Délai d’expiration** (32772)</span><span class="sxs-lookup"><span data-stu-id="c1cfc-125">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="c1cfc-126">**Paramètre non valide** (32773)</span><span class="sxs-lookup"><span data-stu-id="c1cfc-126">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="c1cfc-127">Le **système est en cours d’utilisation** (32774)</span><span class="sxs-lookup"><span data-stu-id="c1cfc-127">**System is in used** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="c1cfc-128">**État non valide pour cette opération** (32775)</span><span class="sxs-lookup"><span data-stu-id="c1cfc-128">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="c1cfc-129">**Type de données incorrect** (32776)</span><span class="sxs-lookup"><span data-stu-id="c1cfc-129">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="c1cfc-130">Le **système n’est pas disponible** (32777)</span><span class="sxs-lookup"><span data-stu-id="c1cfc-130">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="c1cfc-131">**Mémoire insuffisante** (32778)</span><span class="sxs-lookup"><span data-stu-id="c1cfc-131">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="c1cfc-132">Notes</span><span class="sxs-lookup"><span data-stu-id="c1cfc-132">Remarks</span></span>

<span data-ttu-id="c1cfc-133">La méthode **IsKeyPressed** retourne toujours la **valeur false** pour le **\_ menu VK** (18), le **\_ contrôle VK** (17) et **VK \_ Shift** (16), car il ne s’agit pas de clés réelles sur un clavier.</span><span class="sxs-lookup"><span data-stu-id="c1cfc-133">The **IsKeyPressed** method will always return **False** for the **VK\_MENU** (18), **VK\_CONTROL** (17), and **VK\_SHIFT** (16) because these are not real keys on a keyboard.</span></span> <span data-ttu-id="c1cfc-134">Ces codes de touches virtuelles sont toujours mappés à **VK \_ LMENU** (164), **VK \_ LCONTROL** (162) et **VK \_ LSHIFT** (160), respectivement, par les méthodes [**PressKey**](presskey-msvm-keyboard.md) et [**ReleaseKey**](releasekey-msvm-keyboard.md) .</span><span class="sxs-lookup"><span data-stu-id="c1cfc-134">These virtual key codes are always mapped to **VK\_LMENU** (164), **VK\_LCONTROL** (162), and **VK\_LSHIFT** (160), respectively, by the [**PressKey**](presskey-msvm-keyboard.md) and [**ReleaseKey**](releasekey-msvm-keyboard.md) methods.</span></span>

<span data-ttu-id="c1cfc-135">L’accès à la classe de [**\_ clavier MSVM**](msvm-keyboard.md) peut être limité par le filtrage UAC.</span><span class="sxs-lookup"><span data-stu-id="c1cfc-135">Access to the [**Msvm\_Keyboard**](msvm-keyboard.md) class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="c1cfc-136">Pour plus d’informations, consultez [contrôle de compte d’utilisateur et WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="c1cfc-136">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="c1cfc-137">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c1cfc-137">Requirements</span></span>



| <span data-ttu-id="c1cfc-138">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c1cfc-138">Requirement</span></span> | <span data-ttu-id="c1cfc-139">Valeur</span><span class="sxs-lookup"><span data-stu-id="c1cfc-139">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c1cfc-140">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c1cfc-140">Minimum supported client</span></span><br/> | <span data-ttu-id="c1cfc-141">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c1cfc-141">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="c1cfc-142">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c1cfc-142">Minimum supported server</span></span><br/> | <span data-ttu-id="c1cfc-143">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c1cfc-143">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="c1cfc-144">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="c1cfc-144">Namespace</span></span><br/>                | <span data-ttu-id="c1cfc-145">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="c1cfc-145">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="c1cfc-146">MOF</span><span class="sxs-lookup"><span data-stu-id="c1cfc-146">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c1cfc-147"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="c1cfc-147"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="c1cfc-148">DLL</span><span class="sxs-lookup"><span data-stu-id="c1cfc-148">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c1cfc-149"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="c1cfc-149"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="c1cfc-150">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c1cfc-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c1cfc-151">**\_Clavier MSVM**</span><span class="sxs-lookup"><span data-stu-id="c1cfc-151">**Msvm\_Keyboard**</span></span>](msvm-keyboard.md)
</dt> <dt>

[<span data-ttu-id="c1cfc-152">**Codes de clé virtuelle**</span><span class="sxs-lookup"><span data-stu-id="c1cfc-152">**Virtual-Key Codes**</span></span>](../inputdev/virtual-key-codes.md)
</dt> </dl>

 

