---
title: Message EM_GETAUTOCORRECTPROC (RichEdit. h)
description: Obtient un pointeur vers la fonction AutoCorrectProc définie par l’application.
ms.assetid: 90821036-F27D-4AC3-9AB8-40A94486B938
keywords:
- EM_GETAUTOCORRECTPROC les contrôles de message Windows
topic_type:
- apiref
api_name:
- EM_GETAUTOCORRECTPROC
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dc4d730d15ca8631e6d663e3d4f971f115d5c268
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465574"
---
# <a name="em_getautocorrectproc-message"></a><span data-ttu-id="0669c-104">\_Message GETAUTOCORRECTPROC em</span><span class="sxs-lookup"><span data-stu-id="0669c-104">EM\_GETAUTOCORRECTPROC message</span></span>

<span data-ttu-id="0669c-105">Obtient un pointeur vers la fonction [*AutoCorrectProc*](/windows/desktop/api/Richedit/nc-richedit-autocorrectproc) définie par l’application.</span><span class="sxs-lookup"><span data-stu-id="0669c-105">Gets a pointer to the application-defined [*AutoCorrectProc*](/windows/desktop/api/Richedit/nc-richedit-autocorrectproc) function.</span></span>

## <a name="parameters"></a><span data-ttu-id="0669c-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="0669c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0669c-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="0669c-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="0669c-108">Non utilisé ; doit être égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="0669c-108">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="0669c-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="0669c-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="0669c-110">Non utilisé ; doit être égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="0669c-110">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0669c-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="0669c-111">Return value</span></span>

<span data-ttu-id="0669c-112">Retourne un pointeur vers la fonction [*AutoCorrectProc*](/windows/desktop/api/Richedit/nc-richedit-autocorrectproc) définie par l’application.</span><span class="sxs-lookup"><span data-stu-id="0669c-112">Returns a pointer to the application-defined [*AutoCorrectProc*](/windows/desktop/api/Richedit/nc-richedit-autocorrectproc) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="0669c-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0669c-113">Requirements</span></span>



| <span data-ttu-id="0669c-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0669c-114">Requirement</span></span> | <span data-ttu-id="0669c-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="0669c-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="0669c-116">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0669c-116">Minimum supported client</span></span><br/> | <span data-ttu-id="0669c-117">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="0669c-117">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="0669c-118">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0669c-118">Minimum supported server</span></span><br/> | <span data-ttu-id="0669c-119">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="0669c-119">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="0669c-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="0669c-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="0669c-121"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="0669c-121"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0669c-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0669c-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0669c-123">*AutoCorrectProc*</span><span class="sxs-lookup"><span data-stu-id="0669c-123">*AutoCorrectProc*</span></span>](/windows/desktop/api/Richedit/nc-richedit-autocorrectproc)
</dt> <dt>

[<span data-ttu-id="0669c-124">**\_CALLAUTOCORRECTPROC em**</span><span class="sxs-lookup"><span data-stu-id="0669c-124">**EM\_CALLAUTOCORRECTPROC**</span></span>](em-callautocorrectproc.md)
</dt> <dt>

[<span data-ttu-id="0669c-125">**\_SETAUTOCORRECTPROC em**</span><span class="sxs-lookup"><span data-stu-id="0669c-125">**EM\_SETAUTOCORRECTPROC**</span></span>](em-setautocorrectproc.md)
</dt> </dl>

 

 





