---
description: Simule une version de clé.
ms.assetid: EAE84BD5-ECEA-44E7-A7AB-CD18299DF2FE
title: Méthode ReleaseKey de la classe Msvm_Keyboard
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_Keyboard.ReleaseKey
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 2193a4b78128ff3f65e98b4425528a51f6cf5916
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104530100"
---
# <a name="releasekey-method-of-the-msvm_keyboard-class"></a><span data-ttu-id="af766-103">Méthode ReleaseKey de la \_ classe de clavier MSVM</span><span class="sxs-lookup"><span data-stu-id="af766-103">ReleaseKey method of the Msvm\_Keyboard class</span></span>

<span data-ttu-id="af766-104">Simule une version de clé.</span><span class="sxs-lookup"><span data-stu-id="af766-104">Simulates a key release.</span></span> <span data-ttu-id="af766-105">En cas de réussite, la clé sera à l’État up.</span><span class="sxs-lookup"><span data-stu-id="af766-105">When successful, the key will be in the up state.</span></span>

## <a name="syntax"></a><span data-ttu-id="af766-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="af766-106">Syntax</span></span>


```mof
uint32 ReleaseKey(
  [in] uint32 keyCode
);
```



## <a name="parameters"></a><span data-ttu-id="af766-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="af766-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="af766-108">*keyCode* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="af766-108">*keyCode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="af766-109">Type : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="af766-109">Type: **uint32**</span></span>

<span data-ttu-id="af766-110">Code de la clé virtuelle à libérer.</span><span class="sxs-lookup"><span data-stu-id="af766-110">The virtual key code of the key to release.</span></span> <span data-ttu-id="af766-111">Pour obtenir la liste des codes de touche virtuelle, consultez la page [**codes de clé virtuelle**](../inputdev/virtual-key-codes.md).</span><span class="sxs-lookup"><span data-stu-id="af766-111">For the list for virtual-key codes, see [**Virtual-Key Codes**](../inputdev/virtual-key-codes.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="af766-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="af766-112">Return value</span></span>

<span data-ttu-id="af766-113">Type : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="af766-113">Type: **uint32**</span></span>

<span data-ttu-id="af766-114">Une valeur de retour de zéro indique une réussite.</span><span class="sxs-lookup"><span data-stu-id="af766-114">A return value of zero indicates success.</span></span> <span data-ttu-id="af766-115">Une valeur différente de zéro indique un échec de modification de l’état de la clé.</span><span class="sxs-lookup"><span data-stu-id="af766-115">A nonzero value indicates a failure to modify the key state.</span></span>

<dl> <dt>

<span data-ttu-id="af766-116">**Terminé sans erreur** (0)</span><span class="sxs-lookup"><span data-stu-id="af766-116">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="af766-117">**Paramètres de méthode activés-tâche démarrée** (4096)</span><span class="sxs-lookup"><span data-stu-id="af766-117">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="af766-118">**Échec** (32768)</span><span class="sxs-lookup"><span data-stu-id="af766-118">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="af766-119">**Accès refusé** (32769)</span><span class="sxs-lookup"><span data-stu-id="af766-119">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="af766-120">**Non pris en charge** (32770)</span><span class="sxs-lookup"><span data-stu-id="af766-120">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="af766-121">**État inconnu** (32771)</span><span class="sxs-lookup"><span data-stu-id="af766-121">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="af766-122">**Délai d’expiration** (32772)</span><span class="sxs-lookup"><span data-stu-id="af766-122">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="af766-123">**Paramètre non valide** (32773)</span><span class="sxs-lookup"><span data-stu-id="af766-123">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="af766-124">Le **système est en cours d’utilisation** (32774)</span><span class="sxs-lookup"><span data-stu-id="af766-124">**System is in used** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="af766-125">**État non valide pour cette opération** (32775)</span><span class="sxs-lookup"><span data-stu-id="af766-125">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="af766-126">**Type de données incorrect** (32776)</span><span class="sxs-lookup"><span data-stu-id="af766-126">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="af766-127">Le **système n’est pas disponible** (32777)</span><span class="sxs-lookup"><span data-stu-id="af766-127">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="af766-128">**Mémoire insuffisante** (32778)</span><span class="sxs-lookup"><span data-stu-id="af766-128">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="af766-129">Notes</span><span class="sxs-lookup"><span data-stu-id="af766-129">Remarks</span></span>

<span data-ttu-id="af766-130">La méthode **ReleaseKey** mappe les références au **\_ menu VK** (18), **au \_ contrôle VK** (17) et à **VK \_ Shift** (16) **à VK \_ LMENU** (164), **VK \_ LCONTROL** (162) et **VK \_ LSHIFT** (160), respectivement, car le **\_ menu VK**, le **\_ contrôle VK** et les codes de touches virtuelles **VK \_ Shift** ne représentent pas des clés réelles sur un clavier.</span><span class="sxs-lookup"><span data-stu-id="af766-130">The **ReleaseKey** method maps references to the **VK\_MENU** (18), **VK\_CONTROL** (17), and **VK\_SHIFT** (16) to **VK\_LMENU** (164), **VK\_LCONTROL** (162), and **VK\_LSHIFT** (160), respectively, because the **VK\_MENU**, **VK\_CONTROL**, and **VK\_SHIFT** virtual key codes do not represent real keys on a keyboard.</span></span>

<span data-ttu-id="af766-131">L’accès à la classe de [**\_ clavier MSVM**](msvm-keyboard.md) peut être limité par le filtrage UAC.</span><span class="sxs-lookup"><span data-stu-id="af766-131">Access to the [**Msvm\_Keyboard**](msvm-keyboard.md) class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="af766-132">Pour plus d’informations, consultez [contrôle de compte d’utilisateur et WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="af766-132">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="af766-133">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="af766-133">Requirements</span></span>



| <span data-ttu-id="af766-134">Condition requise</span><span class="sxs-lookup"><span data-stu-id="af766-134">Requirement</span></span> | <span data-ttu-id="af766-135">Valeur</span><span class="sxs-lookup"><span data-stu-id="af766-135">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="af766-136">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="af766-136">Minimum supported client</span></span><br/> | <span data-ttu-id="af766-137">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="af766-137">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="af766-138">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="af766-138">Minimum supported server</span></span><br/> | <span data-ttu-id="af766-139">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="af766-139">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="af766-140">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="af766-140">Namespace</span></span><br/>                | <span data-ttu-id="af766-141">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="af766-141">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="af766-142">MOF</span><span class="sxs-lookup"><span data-stu-id="af766-142">MOF</span></span><br/>                      | <dl> <span data-ttu-id="af766-143"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="af766-143"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="af766-144">DLL</span><span class="sxs-lookup"><span data-stu-id="af766-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="af766-145"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="af766-145"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="af766-146">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="af766-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="af766-147">**\_Clavier MSVM**</span><span class="sxs-lookup"><span data-stu-id="af766-147">**Msvm\_Keyboard**</span></span>](msvm-keyboard.md)
</dt> <dt>

[<span data-ttu-id="af766-148">**Codes de clé virtuelle**</span><span class="sxs-lookup"><span data-stu-id="af766-148">**Virtual-Key Codes**</span></span>](../inputdev/virtual-key-codes.md)
</dt> </dl>

 

