---
title: Message EM_SETIMECOLOR (RichEdit. h)
description: Définit la couleur de la composition de l’éditeur de méthode d’entrée (IME) pour un contrôle RichEdit.
ms.assetid: ea5449c9-7d0f-4340-8e3e-1e0b77d443f6
keywords:
- EM_SETIMECOLOR les contrôles de message Windows
topic_type:
- apiref
api_name:
- EM_SETIMECOLOR
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3c020bb3af2b1197afc005bd0b6efec82b609b88
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465711"
---
# <a name="em_setimecolor-message"></a><span data-ttu-id="f1222-104">\_Message SETIMECOLOR em</span><span class="sxs-lookup"><span data-stu-id="f1222-104">EM\_SETIMECOLOR message</span></span>

<span data-ttu-id="f1222-105">Définit la couleur de la composition de l’éditeur de méthode d’entrée (IME) pour un contrôle RichEdit.</span><span class="sxs-lookup"><span data-stu-id="f1222-105">Sets the Input Method Editor (IME) composition color for a rich edit control.</span></span>

> [!Note]  
> <span data-ttu-id="f1222-106">Ce message est pris en charge uniquement dans les versions asiatiques de Microsoft Rich Edit 1,0.</span><span class="sxs-lookup"><span data-stu-id="f1222-106">This message is supported only in Asian-language versions of Microsoft Rich Edit 1.0.</span></span> <span data-ttu-id="f1222-107">Elle n’est pas prise en charge dans les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="f1222-107">It is not supported in any later versions.</span></span>

 

## <a name="parameters"></a><span data-ttu-id="f1222-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f1222-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f1222-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="f1222-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f1222-110">Ce paramètre n’est pas utilisé ; elle doit être égale à zéro.</span><span class="sxs-lookup"><span data-stu-id="f1222-110">This parameter is not used; it must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="f1222-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="f1222-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f1222-112">Pointeur vers une structure [**COMPCOLOR**](/windows/desktop/api/Richedit/ns-richedit-compcolor) qui contient la couleur de composition à définir.</span><span class="sxs-lookup"><span data-stu-id="f1222-112">Pointer to a [**COMPCOLOR**](/windows/desktop/api/Richedit/ns-richedit-compcolor) structure that contains the composition color to be set.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f1222-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="f1222-113">Return value</span></span>

<span data-ttu-id="f1222-114">Si l’opération a échoué, la valeur de retour est une valeur différente de zéro.</span><span class="sxs-lookup"><span data-stu-id="f1222-114">If the operation succeeds, the return value is a nonzero value.</span></span>

<span data-ttu-id="f1222-115">Si l’opération échoue, la valeur de retour est zéro.</span><span class="sxs-lookup"><span data-stu-id="f1222-115">If the operation fails, the return value is zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="f1222-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f1222-116">Requirements</span></span>



| <span data-ttu-id="f1222-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f1222-117">Requirement</span></span> | <span data-ttu-id="f1222-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="f1222-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f1222-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f1222-119">Minimum supported client</span></span><br/> | <span data-ttu-id="f1222-120">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f1222-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="f1222-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f1222-121">Minimum supported server</span></span><br/> | <span data-ttu-id="f1222-122">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f1222-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="f1222-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="f1222-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="f1222-124"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="f1222-124"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f1222-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f1222-125">See also</span></span>

<dl> <dt>

<span data-ttu-id="f1222-126">**Référence**</span><span class="sxs-lookup"><span data-stu-id="f1222-126">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="f1222-127">**\_GETIMECOLOR em**</span><span class="sxs-lookup"><span data-stu-id="f1222-127">**EM\_GETIMECOLOR**</span></span>](em-getimecolor.md)
</dt> <dt>

[<span data-ttu-id="f1222-128">**COMPCOLOR**</span><span class="sxs-lookup"><span data-stu-id="f1222-128">**COMPCOLOR**</span></span>](/windows/desktop/api/Richedit/ns-richedit-compcolor)
</dt> </dl>

 

 





