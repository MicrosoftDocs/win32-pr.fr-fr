---
title: Message EM_SETAUTOCORRECTPROC (RichEdit. h)
description: Définit la procédure de rappel de correction automatique actuelle.
ms.assetid: 2FA48CFC-0D7C-41EF-8207-5EDC644FF3BC
keywords:
- EM_SETAUTOCORRECTPROC les contrôles de message Windows
topic_type:
- apiref
api_name:
- EM_SETAUTOCORRECTPROC
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a7359c86c3fdabe4c410f600d0af3100dde4c4ed
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466558"
---
# <a name="em_setautocorrectproc-message"></a><span data-ttu-id="a5824-104">\_Message SETAUTOCORRECTPROC em</span><span class="sxs-lookup"><span data-stu-id="a5824-104">EM\_SETAUTOCORRECTPROC message</span></span>

<span data-ttu-id="a5824-105">Définit la procédure de rappel de correction automatique actuelle.</span><span class="sxs-lookup"><span data-stu-id="a5824-105">Defines the current autocorrect callback procedure.</span></span>


```C++
#define EM_SETAUTOCORRECTPROC       (WM_USER + 234)
```



## <a name="parameters"></a><span data-ttu-id="a5824-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a5824-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a5824-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="a5824-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a5824-108">Fonction de rappel [*AutoCorrectProc*](/windows/desktop/api/Richedit/nc-richedit-autocorrectproc) .</span><span class="sxs-lookup"><span data-stu-id="a5824-108">The [*AutoCorrectProc*](/windows/desktop/api/Richedit/nc-richedit-autocorrectproc) callback function.</span></span>

</dd> <dt>

<span data-ttu-id="a5824-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="a5824-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a5824-110">Non utilisé ; doit être égal à zéro</span><span class="sxs-lookup"><span data-stu-id="a5824-110">Not used; must be zero</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a5824-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="a5824-111">Return value</span></span>

<span data-ttu-id="a5824-112">Si l’opération a échoué, la valeur de retour est zéro.</span><span class="sxs-lookup"><span data-stu-id="a5824-112">If the operation succeeds, the return value is zero.</span></span> <span data-ttu-id="a5824-113">Si l’opération échoue, la valeur de retour est une valeur différente de zéro.</span><span class="sxs-lookup"><span data-stu-id="a5824-113">If the operation fails, the return value is a nonzero value.</span></span>

## <a name="requirements"></a><span data-ttu-id="a5824-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a5824-114">Requirements</span></span>



| <span data-ttu-id="a5824-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a5824-115">Requirement</span></span> | <span data-ttu-id="a5824-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="a5824-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a5824-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a5824-117">Minimum supported client</span></span><br/> | <span data-ttu-id="a5824-118">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a5824-118">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="a5824-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a5824-119">Minimum supported server</span></span><br/> | <span data-ttu-id="a5824-120">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a5824-120">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="a5824-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="a5824-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="a5824-122"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="a5824-122"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a5824-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a5824-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a5824-124">*AutoCorrectProc*</span><span class="sxs-lookup"><span data-stu-id="a5824-124">*AutoCorrectProc*</span></span>](/windows/desktop/api/Richedit/nc-richedit-autocorrectproc)
</dt> <dt>

[<span data-ttu-id="a5824-125">**\_CALLAUTOCORRECTPROC em**</span><span class="sxs-lookup"><span data-stu-id="a5824-125">**EM\_CALLAUTOCORRECTPROC**</span></span>](em-callautocorrectproc.md)
</dt> <dt>

[<span data-ttu-id="a5824-126">**\_GETAUTOCORRECTPROC em**</span><span class="sxs-lookup"><span data-stu-id="a5824-126">**EM\_GETAUTOCORRECTPROC**</span></span>](em-getautocorrectproc.md)
</dt> </dl>

 

 





