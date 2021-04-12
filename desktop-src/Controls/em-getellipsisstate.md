---
title: Message EM_GETELLIPSISSTATE (RichEdit. h)
description: Récupère l’état actuel des points de suspension.
ms.assetid: D02AE225-F5BF-401A-9877-55C68946CDBE
keywords:
- EM_GETELLIPSISSTATE les contrôles de message Windows
topic_type:
- apiref
api_name:
- EM_GETELLIPSISSTATE
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 905bc8ecc180189f46e896aa0d9aaa3ba88b3f0b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465386"
---
# <a name="em_getellipsisstate-message"></a><span data-ttu-id="f5279-104">\_Message GETELLIPSISSTATE em</span><span class="sxs-lookup"><span data-stu-id="f5279-104">EM\_GETELLIPSISSTATE message</span></span>

<span data-ttu-id="f5279-105">Récupère l’état actuel des points de suspension.</span><span class="sxs-lookup"><span data-stu-id="f5279-105">Retrieves the current ellipsis state.</span></span>


```C++
#define EM_GETELLIPSISSTATE       (WM_USER + 322)
```



## <a name="parameters"></a><span data-ttu-id="f5279-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f5279-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f5279-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="f5279-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f5279-108">Non utilisé ; doit être égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="f5279-108">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="f5279-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="f5279-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f5279-110">Non utilisé ; doit être égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="f5279-110">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f5279-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="f5279-111">Return value</span></span>

<span data-ttu-id="f5279-112">La valeur de retour est TRUE si des points de suspension sont affichés et FALSe dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="f5279-112">The return value is TRUE if an ellipsis is being displayed and FALSE otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="f5279-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f5279-113">Requirements</span></span>



| <span data-ttu-id="f5279-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f5279-114">Requirement</span></span> | <span data-ttu-id="f5279-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="f5279-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f5279-116">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f5279-116">Minimum supported client</span></span><br/> | <span data-ttu-id="f5279-117">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f5279-117">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="f5279-118">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f5279-118">Minimum supported server</span></span><br/> | <span data-ttu-id="f5279-119">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f5279-119">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="f5279-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="f5279-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="f5279-121"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="f5279-121"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f5279-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f5279-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f5279-123">**\_GETELLIPSISMODE em**</span><span class="sxs-lookup"><span data-stu-id="f5279-123">**EM\_GETELLIPSISMODE**</span></span>](em-getellipsismode.md)
</dt> <dt>

[<span data-ttu-id="f5279-124">**\_SETELLIPSISMODE em**</span><span class="sxs-lookup"><span data-stu-id="f5279-124">**EM\_SETELLIPSISMODE**</span></span>](em-setellipsismode.md)
</dt> </dl>

 

 





