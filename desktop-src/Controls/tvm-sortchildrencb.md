---
title: Message TVM_SORTCHILDRENCB (commctrl. h)
description: Trie les éléments d’arborescence à l’aide d’une fonction de rappel définie par l’application qui compare les éléments. Vous pouvez envoyer ce message explicitement ou à l’aide de la \_ macro SortChildrenCB TreeView.
ms.assetid: 1669e576-5e57-49f6-8097-7d6547306014
keywords:
- TVM_SORTCHILDRENCB les contrôles de message Windows
topic_type:
- apiref
api_name:
- TVM_SORTCHILDRENCB
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4b1dab4abbbc019a81d7a066c81dbb3537a0d80d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466794"
---
# <a name="tvm_sortchildrencb-message"></a><span data-ttu-id="21ba3-105">TVM \_ SORTCHILDRENCB message</span><span class="sxs-lookup"><span data-stu-id="21ba3-105">TVM\_SORTCHILDRENCB message</span></span>

<span data-ttu-id="21ba3-106">Trie les éléments d’arborescence à l’aide d’une fonction de rappel définie par l’application qui compare les éléments.</span><span class="sxs-lookup"><span data-stu-id="21ba3-106">Sorts tree-view items using an application-defined callback function that compares the items.</span></span> <span data-ttu-id="21ba3-107">Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**\_ SortChildrenCB TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_sortchildrencb) .</span><span class="sxs-lookup"><span data-stu-id="21ba3-107">You can send this message explicitly or by using the [**TreeView\_SortChildrenCB**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_sortchildrencb) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="21ba3-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="21ba3-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="21ba3-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="21ba3-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="21ba3-110">Réservé.</span><span class="sxs-lookup"><span data-stu-id="21ba3-110">Reserved.</span></span> <span data-ttu-id="21ba3-111">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="21ba3-111">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="21ba3-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="21ba3-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="21ba3-113">Pointeur vers une structure [**TVSORTCB**](/windows/win32/api/commctrl/ns-commctrl-tvsortcb) .</span><span class="sxs-lookup"><span data-stu-id="21ba3-113">Pointer to a [**TVSORTCB**](/windows/win32/api/commctrl/ns-commctrl-tvsortcb) structure.</span></span> <span data-ttu-id="21ba3-114">Le membre **lpfnCompare** est l’adresse de la fonction de rappel définie par l’application, qui est appelée au cours de l’opération de tri chaque fois que l’ordre relatif de deux éléments de liste doit être comparé.</span><span class="sxs-lookup"><span data-stu-id="21ba3-114">The **lpfnCompare** member is the address of the application-defined callback function, which is called during the sort operation each time the relative order of two list items needs to be compared.</span></span> <span data-ttu-id="21ba3-115">Pour plus d’informations sur la fonction de rappel, consultez la description de **TVSORTCB**.</span><span class="sxs-lookup"><span data-stu-id="21ba3-115">For more information about the callback function, see the description of **TVSORTCB**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="21ba3-116">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="21ba3-116">Return value</span></span>

<span data-ttu-id="21ba3-117">Retourne la **valeur true** en cas de réussite, ou **false** dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="21ba3-117">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="21ba3-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="21ba3-118">Requirements</span></span>



| <span data-ttu-id="21ba3-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="21ba3-119">Requirement</span></span> | <span data-ttu-id="21ba3-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="21ba3-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="21ba3-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="21ba3-121">Minimum supported client</span></span><br/> | <span data-ttu-id="21ba3-122">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="21ba3-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="21ba3-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="21ba3-123">Minimum supported server</span></span><br/> | <span data-ttu-id="21ba3-124">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="21ba3-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="21ba3-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="21ba3-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="21ba3-126"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="21ba3-126"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





