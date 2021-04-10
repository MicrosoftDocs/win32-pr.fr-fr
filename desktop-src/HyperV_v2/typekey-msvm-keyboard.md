---
description: Simule une séquence de touches d’appui sur la touche.
ms.assetid: 4166BA71-315D-41BD-857C-48AFB702911E
title: Méthode TypeKey de la classe Msvm_Keyboard
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_Keyboard.TypeKey
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 1b978da48600cc52472ab8bdec011ddbaa5ff624
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103952820"
---
# <a name="typekey-method-of-the-msvm_keyboard-class"></a><span data-ttu-id="92121-103">Méthode TypeKey de la \_ classe de clavier MSVM</span><span class="sxs-lookup"><span data-stu-id="92121-103">TypeKey method of the Msvm\_Keyboard class</span></span>

<span data-ttu-id="92121-104">Simule une séquence de touches d’appui sur la touche.</span><span class="sxs-lookup"><span data-stu-id="92121-104">Simulates a press-release key sequence.</span></span> <span data-ttu-id="92121-105">Cela équivaut à appeler [**PressKey**](presskey-msvm-keyboard.md) suivi de [**ReleaseKey**](releasekey-msvm-keyboard.md).</span><span class="sxs-lookup"><span data-stu-id="92121-105">This is equivalent to calling [**PressKey**](presskey-msvm-keyboard.md) followed by [**ReleaseKey**](releasekey-msvm-keyboard.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="92121-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="92121-106">Syntax</span></span>


```mof
uint32 TypeKey(
  [in] uint32 keyCode
);
```



## <a name="parameters"></a><span data-ttu-id="92121-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="92121-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="92121-108">*keyCode* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="92121-108">*keyCode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="92121-109">Type : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="92121-109">Type: **uint32**</span></span>

<span data-ttu-id="92121-110">Code de la touche virtuelle de la touche sur laquelle appuyer.</span><span class="sxs-lookup"><span data-stu-id="92121-110">The virtual key code of the key to press.</span></span> <span data-ttu-id="92121-111">Pour obtenir la liste des codes de touche virtuelle, consultez la page [**codes de clé virtuelle**](../inputdev/virtual-key-codes.md).</span><span class="sxs-lookup"><span data-stu-id="92121-111">For the list for virtual-key codes, see [**Virtual-Key Codes**](../inputdev/virtual-key-codes.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="92121-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="92121-112">Return value</span></span>

<span data-ttu-id="92121-113">Type : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="92121-113">Type: **uint32**</span></span>

<span data-ttu-id="92121-114">Une valeur de retour de zéro indique une réussite.</span><span class="sxs-lookup"><span data-stu-id="92121-114">A return value of zero indicates success.</span></span> <span data-ttu-id="92121-115">Une valeur différente de zéro indique un échec de modification de l’état de la clé.</span><span class="sxs-lookup"><span data-stu-id="92121-115">A nonzero value indicates a failure to modify the key state.</span></span>

<dl> <dt>

<span data-ttu-id="92121-116">**Terminé sans erreur** (0)</span><span class="sxs-lookup"><span data-stu-id="92121-116">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="92121-117">**Paramètres de méthode activés-tâche démarrée** (4096)</span><span class="sxs-lookup"><span data-stu-id="92121-117">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="92121-118">**Échec** (32768)</span><span class="sxs-lookup"><span data-stu-id="92121-118">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="92121-119">**Accès refusé** (32769)</span><span class="sxs-lookup"><span data-stu-id="92121-119">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="92121-120">**Non pris en charge** (32770)</span><span class="sxs-lookup"><span data-stu-id="92121-120">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="92121-121">**État inconnu** (32771)</span><span class="sxs-lookup"><span data-stu-id="92121-121">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="92121-122">**Délai d’expiration** (32772)</span><span class="sxs-lookup"><span data-stu-id="92121-122">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="92121-123">**Paramètre non valide** (32773)</span><span class="sxs-lookup"><span data-stu-id="92121-123">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="92121-124">Le **système est en cours d’utilisation** (32774)</span><span class="sxs-lookup"><span data-stu-id="92121-124">**System is in used** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="92121-125">**État non valide pour cette opération** (32775)</span><span class="sxs-lookup"><span data-stu-id="92121-125">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="92121-126">**Type de données incorrect** (32776)</span><span class="sxs-lookup"><span data-stu-id="92121-126">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="92121-127">Le **système n’est pas disponible** (32777)</span><span class="sxs-lookup"><span data-stu-id="92121-127">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="92121-128">**Mémoire insuffisante** (32778)</span><span class="sxs-lookup"><span data-stu-id="92121-128">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="92121-129">Notes</span><span class="sxs-lookup"><span data-stu-id="92121-129">Remarks</span></span>

<span data-ttu-id="92121-130">L’accès à la classe de [**\_ clavier MSVM**](msvm-keyboard.md) peut être limité par le filtrage UAC.</span><span class="sxs-lookup"><span data-stu-id="92121-130">Access to the [**Msvm\_Keyboard**](msvm-keyboard.md) class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="92121-131">Pour plus d’informations, consultez [contrôle de compte d’utilisateur et WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="92121-131">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="92121-132">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="92121-132">Requirements</span></span>



| <span data-ttu-id="92121-133">Condition requise</span><span class="sxs-lookup"><span data-stu-id="92121-133">Requirement</span></span> | <span data-ttu-id="92121-134">Valeur</span><span class="sxs-lookup"><span data-stu-id="92121-134">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="92121-135">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="92121-135">Minimum supported client</span></span><br/> | <span data-ttu-id="92121-136">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="92121-136">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="92121-137">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="92121-137">Minimum supported server</span></span><br/> | <span data-ttu-id="92121-138">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="92121-138">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="92121-139">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="92121-139">Namespace</span></span><br/>                | <span data-ttu-id="92121-140">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="92121-140">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="92121-141">MOF</span><span class="sxs-lookup"><span data-stu-id="92121-141">MOF</span></span><br/>                      | <dl> <span data-ttu-id="92121-142"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="92121-142"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="92121-143">DLL</span><span class="sxs-lookup"><span data-stu-id="92121-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="92121-144"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="92121-144"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="92121-145">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="92121-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="92121-146">**\_Clavier MSVM**</span><span class="sxs-lookup"><span data-stu-id="92121-146">**Msvm\_Keyboard**</span></span>](msvm-keyboard.md)
</dt> <dt>

[<span data-ttu-id="92121-147">**Codes de clé virtuelle**</span><span class="sxs-lookup"><span data-stu-id="92121-147">**Virtual-Key Codes**</span></span>](../inputdev/virtual-key-codes.md)
</dt> </dl>

 

