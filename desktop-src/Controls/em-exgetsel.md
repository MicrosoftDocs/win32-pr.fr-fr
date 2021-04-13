---
title: Message EM_EXGETSEL (RichEdit. h)
description: Récupère les positions des caractères de début et de fin de la sélection dans un contrôle RichEdit.
ms.assetid: 60fcf13e-6c45-4f4e-9b54-70f0985122fb
keywords:
- EM_EXGETSEL les contrôles de message Windows
topic_type:
- apiref
api_name:
- EM_EXGETSEL
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4b97fb43a76f0f8ac91dd16c0cfa5700c5431eb2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465894"
---
# <a name="em_exgetsel-message"></a><span data-ttu-id="2a01f-104">\_Message EXGETSEL em</span><span class="sxs-lookup"><span data-stu-id="2a01f-104">EM\_EXGETSEL message</span></span>

<span data-ttu-id="2a01f-105">Récupère les positions des caractères de début et de fin de la sélection dans un contrôle RichEdit.</span><span class="sxs-lookup"><span data-stu-id="2a01f-105">Retrieves the starting and ending character positions of the selection in a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="2a01f-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="2a01f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2a01f-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="2a01f-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="2a01f-108">Ce paramètre n’est pas utilisé ; elle doit être égale à zéro.</span><span class="sxs-lookup"><span data-stu-id="2a01f-108">This parameter is not used; it must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="2a01f-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="2a01f-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="2a01f-110">Structure [**CHARRANGE**](/windows/desktop/api/Richedit/ns-richedit-charrange) qui reçoit la plage de sélection.</span><span class="sxs-lookup"><span data-stu-id="2a01f-110">A [**CHARRANGE**](/windows/desktop/api/Richedit/ns-richedit-charrange) structure that receives the selection range.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2a01f-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="2a01f-111">Return value</span></span>

<span data-ttu-id="2a01f-112">Ce message ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="2a01f-112">This message does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="2a01f-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="2a01f-113">Requirements</span></span>



| <span data-ttu-id="2a01f-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="2a01f-114">Requirement</span></span> | <span data-ttu-id="2a01f-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="2a01f-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="2a01f-116">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2a01f-116">Minimum supported client</span></span><br/> | <span data-ttu-id="2a01f-117">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="2a01f-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="2a01f-118">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2a01f-118">Minimum supported server</span></span><br/> | <span data-ttu-id="2a01f-119">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="2a01f-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="2a01f-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="2a01f-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="2a01f-121"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="2a01f-121"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2a01f-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2a01f-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2a01f-123">**CHARRANGE**</span><span class="sxs-lookup"><span data-stu-id="2a01f-123">**CHARRANGE**</span></span>](/windows/desktop/api/Richedit/ns-richedit-charrange)
</dt> </dl>

 

 





