---
title: Message TVM_SETLINECOLOR (commctrl. h)
description: Le \_ message TVM SETLINECOLOR définit la couleur de la ligne active.
ms.assetid: c5fc28af-5603-489f-aa6b-73e153f9aebc
keywords:
- TVM_SETLINECOLOR les contrôles de message Windows
topic_type:
- apiref
api_name:
- TVM_SETLINECOLOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7d70340ea0d2339055faa3fb473269f3b244f335
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104032971"
---
# <a name="tvm_setlinecolor-message"></a><span data-ttu-id="836fd-104">TVM \_ SETLINECOLOR message</span><span class="sxs-lookup"><span data-stu-id="836fd-104">TVM\_SETLINECOLOR message</span></span>

<span data-ttu-id="836fd-105">Le message **TVM \_ SETLINECOLOR** définit la couleur de la ligne active.</span><span class="sxs-lookup"><span data-stu-id="836fd-105">The **TVM\_SETLINECOLOR** message sets the current line color.</span></span>

## <a name="parameters"></a><span data-ttu-id="836fd-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="836fd-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="836fd-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="836fd-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="836fd-108">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="836fd-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="836fd-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="836fd-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="836fd-110">Nouvelle couleur de ligne.</span><span class="sxs-lookup"><span data-stu-id="836fd-110">New line color.</span></span> <span data-ttu-id="836fd-111">Utilisez la \_ valeur CLR par défaut pour restaurer les couleurs par défaut du système.</span><span class="sxs-lookup"><span data-stu-id="836fd-111">Use the CLR\_DEFAULT value to restore the system default colors.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="836fd-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="836fd-112">Return value</span></span>

<span data-ttu-id="836fd-113">Retourne la couleur de ligne précédente.</span><span class="sxs-lookup"><span data-stu-id="836fd-113">Returns the previous line color.</span></span>

## <a name="remarks"></a><span data-ttu-id="836fd-114">Notes</span><span class="sxs-lookup"><span data-stu-id="836fd-114">Remarks</span></span>

<span data-ttu-id="836fd-115">Ce message modifie uniquement les couleurs des lignes.</span><span class="sxs-lookup"><span data-stu-id="836fd-115">This message only changes line colors.</span></span> <span data-ttu-id="836fd-116">Pour modifier les couleurs de' + 'et'-'à l’intérieur des boutons, utilisez le message [**TVM \_ SETTEXTCOLOR**](tvm-settextcolor.md) .</span><span class="sxs-lookup"><span data-stu-id="836fd-116">To change the colors of the '+' and '-' inside the buttons, use the [**TVM\_SETTEXTCOLOR**](tvm-settextcolor.md) message.</span></span>

## <a name="requirements"></a><span data-ttu-id="836fd-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="836fd-117">Requirements</span></span>



| <span data-ttu-id="836fd-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="836fd-118">Requirement</span></span> | <span data-ttu-id="836fd-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="836fd-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="836fd-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="836fd-120">Minimum supported client</span></span><br/> | <span data-ttu-id="836fd-121">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="836fd-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="836fd-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="836fd-122">Minimum supported server</span></span><br/> | <span data-ttu-id="836fd-123">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="836fd-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="836fd-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="836fd-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="836fd-125"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="836fd-125"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="836fd-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="836fd-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="836fd-127">**TVM \_ GETLINECOLOR**</span><span class="sxs-lookup"><span data-stu-id="836fd-127">**TVM\_GETLINECOLOR**</span></span>](tvm-getlinecolor.md)
</dt> </dl>

 

 





