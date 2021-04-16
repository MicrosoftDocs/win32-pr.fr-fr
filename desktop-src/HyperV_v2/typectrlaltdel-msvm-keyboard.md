---
description: Simule une séquence de touches Ctrl + Alt + Suppr.
ms.assetid: C24C9C42-844F-4560-B8C1-0054F5E913D6
title: Méthode TypeCtrlAltDel de la classe Msvm_Keyboard
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_Keyboard.TypeCtrlAltDel
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 64ebc4bddf8adccd7098cafed1df43d1cf1cb4eb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104320245"
---
# <a name="typectrlaltdel-method-of-the-msvm_keyboard-class"></a><span data-ttu-id="675d5-103">Méthode TypeCtrlAltDel de la \_ classe de clavier MSVM</span><span class="sxs-lookup"><span data-stu-id="675d5-103">TypeCtrlAltDel method of the Msvm\_Keyboard class</span></span>

<span data-ttu-id="675d5-104">Simule une séquence de touches Ctrl + Alt + Suppr.</span><span class="sxs-lookup"><span data-stu-id="675d5-104">Simulates a Ctrl+Alt+Del key sequence.</span></span>

## <a name="syntax"></a><span data-ttu-id="675d5-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="675d5-105">Syntax</span></span>


```mof
uint32 TypeCtrlAltDel();
```



## <a name="parameters"></a><span data-ttu-id="675d5-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="675d5-106">Parameters</span></span>

<span data-ttu-id="675d5-107">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="675d5-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="675d5-108">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="675d5-108">Return value</span></span>

<span data-ttu-id="675d5-109">Type : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="675d5-109">Type: **uint32**</span></span>

<span data-ttu-id="675d5-110">Une valeur de retour de zéro indique une réussite.</span><span class="sxs-lookup"><span data-stu-id="675d5-110">A return value of zero indicates success.</span></span> <span data-ttu-id="675d5-111">Une valeur différente de zéro indique un échec d’envoi.</span><span class="sxs-lookup"><span data-stu-id="675d5-111">A nonzero value indicates a failure to send.</span></span>

<dl> <dt>

<span data-ttu-id="675d5-112">**Terminé sans erreur** (0)</span><span class="sxs-lookup"><span data-stu-id="675d5-112">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="675d5-113">**Paramètres de méthode activés-tâche démarrée** (4096)</span><span class="sxs-lookup"><span data-stu-id="675d5-113">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="675d5-114">**Échec** (32768)</span><span class="sxs-lookup"><span data-stu-id="675d5-114">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="675d5-115">**Accès refusé** (32769)</span><span class="sxs-lookup"><span data-stu-id="675d5-115">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="675d5-116">**Non pris en charge** (32770)</span><span class="sxs-lookup"><span data-stu-id="675d5-116">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="675d5-117">**État inconnu** (32771)</span><span class="sxs-lookup"><span data-stu-id="675d5-117">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="675d5-118">**Délai d’expiration** (32772)</span><span class="sxs-lookup"><span data-stu-id="675d5-118">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="675d5-119">**Paramètre non valide** (32773)</span><span class="sxs-lookup"><span data-stu-id="675d5-119">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="675d5-120">Le **système est en cours d’utilisation** (32774)</span><span class="sxs-lookup"><span data-stu-id="675d5-120">**System is in used** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="675d5-121">**État non valide pour cette opération** (32775)</span><span class="sxs-lookup"><span data-stu-id="675d5-121">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="675d5-122">**Type de données incorrect** (32776)</span><span class="sxs-lookup"><span data-stu-id="675d5-122">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="675d5-123">Le **système n’est pas disponible** (32777)</span><span class="sxs-lookup"><span data-stu-id="675d5-123">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="675d5-124">**Mémoire insuffisante** (32778)</span><span class="sxs-lookup"><span data-stu-id="675d5-124">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="675d5-125">Notes</span><span class="sxs-lookup"><span data-stu-id="675d5-125">Remarks</span></span>

<span data-ttu-id="675d5-126">L’accès à la classe de [**\_ clavier MSVM**](msvm-keyboard.md) peut être limité par le filtrage UAC.</span><span class="sxs-lookup"><span data-stu-id="675d5-126">Access to the [**Msvm\_Keyboard**](msvm-keyboard.md) class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="675d5-127">Pour plus d’informations, consultez [contrôle de compte d’utilisateur et WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="675d5-127">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="675d5-128">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="675d5-128">Requirements</span></span>



| <span data-ttu-id="675d5-129">Condition requise</span><span class="sxs-lookup"><span data-stu-id="675d5-129">Requirement</span></span> | <span data-ttu-id="675d5-130">Valeur</span><span class="sxs-lookup"><span data-stu-id="675d5-130">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="675d5-131">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="675d5-131">Minimum supported client</span></span><br/> | <span data-ttu-id="675d5-132">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="675d5-132">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="675d5-133">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="675d5-133">Minimum supported server</span></span><br/> | <span data-ttu-id="675d5-134">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="675d5-134">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="675d5-135">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="675d5-135">Namespace</span></span><br/>                | <span data-ttu-id="675d5-136">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="675d5-136">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="675d5-137">MOF</span><span class="sxs-lookup"><span data-stu-id="675d5-137">MOF</span></span><br/>                      | <dl> <span data-ttu-id="675d5-138"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="675d5-138"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="675d5-139">DLL</span><span class="sxs-lookup"><span data-stu-id="675d5-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="675d5-140"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="675d5-140"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="675d5-141">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="675d5-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="675d5-142">**\_Clavier MSVM**</span><span class="sxs-lookup"><span data-stu-id="675d5-142">**Msvm\_Keyboard**</span></span>](msvm-keyboard.md)
</dt> </dl>

 

