---
description: Simule une séquence de touches à l’aide de codes d’analyse.
ms.assetid: F67D2FBA-3CE0-4135-9043-FAB59381DE3C
title: Méthode TypeScancodes de la classe Msvm_Keyboard
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_Keyboard.TypeScancodes
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 97479a1a0926894f72472b7459f77cd9325ac6fa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103752357"
---
# <a name="typescancodes-method-of-the-msvm_keyboard-class"></a><span data-ttu-id="13ffe-103">Méthode TypeScancodes de la \_ classe de clavier MSVM</span><span class="sxs-lookup"><span data-stu-id="13ffe-103">TypeScancodes method of the Msvm\_Keyboard class</span></span>

<span data-ttu-id="13ffe-104">Simule une séquence de touches à l’aide de codes d’analyse.</span><span class="sxs-lookup"><span data-stu-id="13ffe-104">Simulates a key sequence using scan codes.</span></span>

## <a name="syntax"></a><span data-ttu-id="13ffe-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="13ffe-105">Syntax</span></span>


```mof
uint32 TypeScancodes(
  [in] uint8 Scancodes[]
);
```



## <a name="parameters"></a><span data-ttu-id="13ffe-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="13ffe-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="13ffe-107">*Scancodes* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="13ffe-107">*Scancodes* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="13ffe-108">Type : **UInt8 \[ \]**</span><span class="sxs-lookup"><span data-stu-id="13ffe-108">Type: **uint8\[\]**</span></span>

<span data-ttu-id="13ffe-109">Tableau qui contient les codes d’analyse à taper.</span><span class="sxs-lookup"><span data-stu-id="13ffe-109">An array that contains the scan codes to type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="13ffe-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="13ffe-110">Return value</span></span>

<span data-ttu-id="13ffe-111">Type : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="13ffe-111">Type: **uint32**</span></span>

<span data-ttu-id="13ffe-112">Cette méthode retourne 0 si elle est réussie.</span><span class="sxs-lookup"><span data-stu-id="13ffe-112">This method returns 0 if it succeeds.</span></span> <span data-ttu-id="13ffe-113">Toute autre valeur de retour indique une erreur.</span><span class="sxs-lookup"><span data-stu-id="13ffe-113">Any other return value indicates an error.</span></span> <span data-ttu-id="13ffe-114">La valeur de retour peut être l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="13ffe-114">The return value can be one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="13ffe-115">**Terminé sans erreur** (0)</span><span class="sxs-lookup"><span data-stu-id="13ffe-115">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="13ffe-116">**Paramètres de méthode activés-tâche démarrée** (4096)</span><span class="sxs-lookup"><span data-stu-id="13ffe-116">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="13ffe-117">**Échec** (32768)</span><span class="sxs-lookup"><span data-stu-id="13ffe-117">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="13ffe-118">**Accès refusé** (32769)</span><span class="sxs-lookup"><span data-stu-id="13ffe-118">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="13ffe-119">**Non pris en charge** (32770)</span><span class="sxs-lookup"><span data-stu-id="13ffe-119">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="13ffe-120">**État inconnu** (32771)</span><span class="sxs-lookup"><span data-stu-id="13ffe-120">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="13ffe-121">**Délai d’expiration** (32772)</span><span class="sxs-lookup"><span data-stu-id="13ffe-121">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="13ffe-122">**Paramètre non valide** (32773)</span><span class="sxs-lookup"><span data-stu-id="13ffe-122">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="13ffe-123">Le **système est en cours d’utilisation** (32774)</span><span class="sxs-lookup"><span data-stu-id="13ffe-123">**System is in used** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="13ffe-124">**État non valide pour cette opération** (32775)</span><span class="sxs-lookup"><span data-stu-id="13ffe-124">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="13ffe-125">**Type de données incorrect** (32776)</span><span class="sxs-lookup"><span data-stu-id="13ffe-125">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="13ffe-126">Le **système n’est pas disponible** (32777)</span><span class="sxs-lookup"><span data-stu-id="13ffe-126">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="13ffe-127">**Mémoire insuffisante** (32778)</span><span class="sxs-lookup"><span data-stu-id="13ffe-127">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="13ffe-128">Notes</span><span class="sxs-lookup"><span data-stu-id="13ffe-128">Remarks</span></span>

<span data-ttu-id="13ffe-129">L’accès à la classe de [**\_ clavier MSVM**](msvm-keyboard.md) peut être limité par le filtrage UAC.</span><span class="sxs-lookup"><span data-stu-id="13ffe-129">Access to the [**Msvm\_Keyboard**](msvm-keyboard.md) class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="13ffe-130">Pour plus d’informations, consultez [contrôle de compte d’utilisateur et WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="13ffe-130">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="13ffe-131">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="13ffe-131">Requirements</span></span>



| <span data-ttu-id="13ffe-132">Condition requise</span><span class="sxs-lookup"><span data-stu-id="13ffe-132">Requirement</span></span> | <span data-ttu-id="13ffe-133">Valeur</span><span class="sxs-lookup"><span data-stu-id="13ffe-133">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="13ffe-134">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="13ffe-134">Minimum supported client</span></span><br/> | <span data-ttu-id="13ffe-135">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="13ffe-135">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="13ffe-136">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="13ffe-136">Minimum supported server</span></span><br/> | <span data-ttu-id="13ffe-137">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="13ffe-137">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="13ffe-138">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="13ffe-138">Namespace</span></span><br/>                | <span data-ttu-id="13ffe-139">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="13ffe-139">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="13ffe-140">MOF</span><span class="sxs-lookup"><span data-stu-id="13ffe-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="13ffe-141"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="13ffe-141"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="13ffe-142">DLL</span><span class="sxs-lookup"><span data-stu-id="13ffe-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="13ffe-143"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="13ffe-143"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="13ffe-144">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="13ffe-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="13ffe-145">**\_Clavier MSVM**</span><span class="sxs-lookup"><span data-stu-id="13ffe-145">**Msvm\_Keyboard**</span></span>](msvm-keyboard.md)
</dt> </dl>

 

