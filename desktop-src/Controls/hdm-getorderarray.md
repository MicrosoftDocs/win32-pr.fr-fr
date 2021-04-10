---
title: Message HDM_GETORDERARRAY (commctrl. h)
description: Obtient l’ordre de gauche à droite actuel des éléments dans un contrôle header. Vous pouvez envoyer ce message explicitement ou utiliser la macro d’en-tête \_ GetOrderArray.
ms.assetid: b287d3c1-ae61-41a4-a884-dc008eb24ad8
keywords:
- HDM_GETORDERARRAY les contrôles de message Windows
topic_type:
- apiref
api_name:
- HDM_GETORDERARRAY
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e334b0023ad3441c20048273e9bc58c1b25622b9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103771"
---
# <a name="hdm_getorderarray-message"></a><span data-ttu-id="6c40e-105">\_Message HDM GETORDERARRAY</span><span class="sxs-lookup"><span data-stu-id="6c40e-105">HDM\_GETORDERARRAY message</span></span>

<span data-ttu-id="6c40e-106">Obtient l’ordre de gauche à droite actuel des éléments dans un contrôle header.</span><span class="sxs-lookup"><span data-stu-id="6c40e-106">Gets the current left-to-right order of items in a header control.</span></span> <span data-ttu-id="6c40e-107">Vous pouvez envoyer ce message explicitement ou utiliser la macro d' [**en-tête \_ GetOrderArray**](/windows/desktop/api/Commctrl/nf-commctrl-header_getorderarray) .</span><span class="sxs-lookup"><span data-stu-id="6c40e-107">You can send this message explicitly or use the [**Header\_GetOrderArray**](/windows/desktop/api/Commctrl/nf-commctrl-header_getorderarray) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="6c40e-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="6c40e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6c40e-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="6c40e-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="6c40e-110">Nombre d’éléments entiers que *lParam* peut contenir.</span><span class="sxs-lookup"><span data-stu-id="6c40e-110">The number of integer elements that *lParam* can hold.</span></span> <span data-ttu-id="6c40e-111">Cette valeur doit être égale au nombre d’éléments dans le contrôle (consultez [**HDM \_ GETITEMCOUNT**](hdm-getitemcount.md)).</span><span class="sxs-lookup"><span data-stu-id="6c40e-111">This value must be equal to the number of items in the control (see [**HDM\_GETITEMCOUNT**](hdm-getitemcount.md)).</span></span>

</dd> <dt>

<span data-ttu-id="6c40e-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="6c40e-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="6c40e-113">Pointeur vers un tableau d’entiers qui reçoivent les valeurs d’index des éléments dans l’en-tête.</span><span class="sxs-lookup"><span data-stu-id="6c40e-113">A pointer to an array of integers that receive the index values for items in the header.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6c40e-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="6c40e-114">Return value</span></span>

<span data-ttu-id="6c40e-115">Retourne une valeur différente de zéro en cas de réussite, et la mémoire tampon au niveau de *lParam* reçoit le numéro d’élément de chaque élément du contrôle header dans l’ordre dans lequel ils apparaissent de gauche à droite.</span><span class="sxs-lookup"><span data-stu-id="6c40e-115">Returns nonzero if successful, and the buffer at *lParam* receives the item number for each item in the header control in the order in which they appear from left to right.</span></span> <span data-ttu-id="6c40e-116">Dans le cas contraire, le message retourne la valeur zéro.</span><span class="sxs-lookup"><span data-stu-id="6c40e-116">Otherwise, the message returns zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="6c40e-117">Notes</span><span class="sxs-lookup"><span data-stu-id="6c40e-117">Remarks</span></span>

<span data-ttu-id="6c40e-118">Le nombre d’éléments dans *lParam* est spécifié dans *wParam* et doit être égal au nombre d’éléments dans le contrôle.</span><span class="sxs-lookup"><span data-stu-id="6c40e-118">The number of elements in *lParam* is specified in *wParam* and must be equal to the number of items in the control.</span></span> <span data-ttu-id="6c40e-119">Par exemple, le fragment de code suivant réserve une quantité de mémoire suffisante pour contenir les valeurs d’index.</span><span class="sxs-lookup"><span data-stu-id="6c40e-119">For example, the following code fragment will reserve enough memory to hold the index values.</span></span>


```
int iItems,

    *lpiArray;



// Get memory for buffer.

(iItems = SendMessage(hwndHD, HDM_GETITEMCOUNT, 0,0))!=-1)

    if(!(lpiArray = calloc(iItems,sizeof(int))))

MessageBox(hwnd, "Out of memory.","Error", MB_OK);
```



## <a name="requirements"></a><span data-ttu-id="6c40e-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="6c40e-120">Requirements</span></span>



| <span data-ttu-id="6c40e-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="6c40e-121">Requirement</span></span> | <span data-ttu-id="6c40e-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="6c40e-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="6c40e-123">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6c40e-123">Minimum supported client</span></span><br/> | <span data-ttu-id="6c40e-124">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="6c40e-124">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="6c40e-125">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6c40e-125">Minimum supported server</span></span><br/> | <span data-ttu-id="6c40e-126">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="6c40e-126">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="6c40e-127">En-tête</span><span class="sxs-lookup"><span data-stu-id="6c40e-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="6c40e-128"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="6c40e-128"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





