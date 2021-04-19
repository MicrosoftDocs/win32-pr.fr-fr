---
description: Réinitialise le clavier virtuel.
ms.assetid: 6D4A9F02-53BD-47C2-9C09-F22C3630312F
title: Méthode Reset de la classe Msvm_Keyboard
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_Keyboard.Reset
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 4fe46657177789e49b49ec2c36f0e7a9dc95394f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106523665"
---
# <a name="reset-method-of-the-msvm_keyboard-class"></a><span data-ttu-id="3fd29-103">Méthode Reset de la \_ classe de clavier MSVM</span><span class="sxs-lookup"><span data-stu-id="3fd29-103">Reset method of the Msvm\_Keyboard class</span></span>

<span data-ttu-id="3fd29-104">Réinitialise le clavier virtuel.</span><span class="sxs-lookup"><span data-stu-id="3fd29-104">Resets the virtual keyboard.</span></span>

## <a name="syntax"></a><span data-ttu-id="3fd29-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3fd29-105">Syntax</span></span>


```mof
uint32 Reset();
```



## <a name="parameters"></a><span data-ttu-id="3fd29-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="3fd29-106">Parameters</span></span>

<span data-ttu-id="3fd29-107">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="3fd29-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="3fd29-108">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="3fd29-108">Return value</span></span>

<span data-ttu-id="3fd29-109">Une valeur de retour de zéro indique une réussite.</span><span class="sxs-lookup"><span data-stu-id="3fd29-109">A return value of zero indicates success.</span></span> <span data-ttu-id="3fd29-110">Une valeur de retour d’une indique un échec, car la méthode n’est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="3fd29-110">A return value of one indicates a failure because the method is not supported.</span></span>

<dl> <dt>

<span data-ttu-id="3fd29-111">**Terminé sans erreur** (0)</span><span class="sxs-lookup"><span data-stu-id="3fd29-111">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="3fd29-112">**Non pris en charge** (1)</span><span class="sxs-lookup"><span data-stu-id="3fd29-112">**Not supported** (1)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="3fd29-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3fd29-113">Requirements</span></span>



| <span data-ttu-id="3fd29-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="3fd29-114">Requirement</span></span> | <span data-ttu-id="3fd29-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="3fd29-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3fd29-116">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3fd29-116">Minimum supported client</span></span><br/> | <span data-ttu-id="3fd29-117">Windows 8.1 les \[ applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="3fd29-117">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="3fd29-118">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3fd29-118">Minimum supported server</span></span><br/> | <span data-ttu-id="3fd29-119">Applications de bureau Windows Server 2012 R2 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="3fd29-119">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="3fd29-120">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="3fd29-120">Namespace</span></span><br/>                | <span data-ttu-id="3fd29-121">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="3fd29-121">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="3fd29-122">MOF</span><span class="sxs-lookup"><span data-stu-id="3fd29-122">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3fd29-123"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="3fd29-123"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="3fd29-124">DLL</span><span class="sxs-lookup"><span data-stu-id="3fd29-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3fd29-125"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="3fd29-125"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="3fd29-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3fd29-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3fd29-127">**\_Clavier MSVM**</span><span class="sxs-lookup"><span data-stu-id="3fd29-127">**Msvm\_Keyboard**</span></span>](msvm-keyboard.md)
</dt> </dl>

 

 




