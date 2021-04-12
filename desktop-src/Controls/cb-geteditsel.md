---
title: Message CB_GETEDITSEL (winuser. h)
description: Obtient les positions des caractères de début et de fin de la sélection actuelle dans le contrôle d’édition d’une zone de liste déroulante.
ms.assetid: 72b64135-e35a-4f72-9fc7-e6bedf495f23
keywords:
- CB_GETEDITSEL les contrôles de message Windows
topic_type:
- apiref
api_name:
- CB_GETEDITSEL
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 319ce4a3c7a5a61903d4fc3bf04eed223e749787
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104032857"
---
# <a name="cb_geteditsel-message"></a><span data-ttu-id="fe9b4-104">\_Message GETEDITSEL CB</span><span class="sxs-lookup"><span data-stu-id="fe9b4-104">CB\_GETEDITSEL message</span></span>

<span data-ttu-id="fe9b4-105">Obtient les positions des caractères de début et de fin de la sélection actuelle dans le contrôle d’édition d’une zone de liste déroulante.</span><span class="sxs-lookup"><span data-stu-id="fe9b4-105">Gets the starting and ending character positions of the current selection in the edit control of a combo box.</span></span>

## <a name="parameters"></a><span data-ttu-id="fe9b4-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="fe9b4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fe9b4-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="fe9b4-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="fe9b4-108">Pointeur vers une valeur **DWORD** qui reçoit la position de départ de la sélection.</span><span class="sxs-lookup"><span data-stu-id="fe9b4-108">A pointer to a **DWORD** value that receives the starting position of the selection.</span></span> <span data-ttu-id="fe9b4-109">Ce paramètre peut être **NULL**.</span><span class="sxs-lookup"><span data-stu-id="fe9b4-109">This parameter can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="fe9b4-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="fe9b4-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="fe9b4-111">Pointeur vers une valeur **DWORD** qui reçoit la position de fin de la sélection.</span><span class="sxs-lookup"><span data-stu-id="fe9b4-111">A pointer to a **DWORD** value that receives the ending position of the selection.</span></span> <span data-ttu-id="fe9b4-112">Ce paramètre peut être **NULL**.</span><span class="sxs-lookup"><span data-stu-id="fe9b4-112">This parameter can be **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fe9b4-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="fe9b4-113">Return value</span></span>

<span data-ttu-id="fe9b4-114">La valeur de retour est une valeur **DWORD** de base zéro avec la position de départ de la sélection dans le [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) et avec la position de fin du premier caractère après le dernier caractère sélectionné dans le [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="fe9b4-114">The return value is a zero-based **DWORD** value with the starting position of the selection in the [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) and with the ending position of the first character after the last selected character in the [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)).</span></span>

## <a name="examples"></a><span data-ttu-id="fe9b4-115">Exemples</span><span class="sxs-lookup"><span data-stu-id="fe9b4-115">Examples</span></span>

<span data-ttu-id="fe9b4-116">L’exemple de code suivant montre deux façons de récupérer la plage de sélection actuelle.</span><span class="sxs-lookup"><span data-stu-id="fe9b4-116">The following code example shows two ways of retrieving the current selection range.</span></span>


```C++
DWORD start, end;

// Get the range from [out] parameters.
// hwnd is the handle of the combo box control.
SendMessage(hwnd, CB_GETEDITSEL, (WPARAM)&start, (LPARAM)&end;

// Get the range from the return value.
DWORD range = SendMessage(hwnd, CB_GETEDITSEL, NULL, NULL);
start = LOWORD(range);
end = HIWORD(range);
```



## <a name="requirements"></a><span data-ttu-id="fe9b4-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="fe9b4-117">Requirements</span></span>



| <span data-ttu-id="fe9b4-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="fe9b4-118">Requirement</span></span> | <span data-ttu-id="fe9b4-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="fe9b4-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fe9b4-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="fe9b4-120">Minimum supported client</span></span><br/> | <span data-ttu-id="fe9b4-121">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="fe9b4-121">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="fe9b4-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="fe9b4-122">Minimum supported server</span></span><br/> | <span data-ttu-id="fe9b4-123">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="fe9b4-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="fe9b4-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="fe9b4-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="fe9b4-125"><dt>Winuser. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="fe9b4-125"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fe9b4-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fe9b4-126">See also</span></span>

<dl> <dt>

<span data-ttu-id="fe9b4-127">**Référence**</span><span class="sxs-lookup"><span data-stu-id="fe9b4-127">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="fe9b4-128">**\_SETEDITSEL CB**</span><span class="sxs-lookup"><span data-stu-id="fe9b4-128">**CB\_SETEDITSEL**</span></span>](cb-seteditsel.md)
</dt> <dt>

<span data-ttu-id="fe9b4-129">**Autres ressources**</span><span class="sxs-lookup"><span data-stu-id="fe9b4-129">**Other Resources**</span></span>
</dt> <dt>

<span data-ttu-id="fe9b4-130">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="fe9b4-130">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span></span>
</dt> <dt>

<span data-ttu-id="fe9b4-131">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="fe9b4-131">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span></span>
</dt> </dl>

 

