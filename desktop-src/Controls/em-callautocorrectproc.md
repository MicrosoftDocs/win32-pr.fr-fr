---
title: Message EM_CALLAUTOCORRECTPROC (RichEdit. h)
description: Appelle la fonction de rappel de correction automatique stockée par le \_ message em SETAUTOCORRECTPROC, à condition que le texte qui précède le point d’insertion soit candidat à la correction automatique.
ms.assetid: 93116467-B345-4FD9-9162-3E01CF3C6F20
keywords:
- EM_CALLAUTOCORRECTPROC les contrôles de message Windows
topic_type:
- apiref
api_name:
- EM_CALLAUTOCORRECTPROC
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 73109d2499fc01a1d811066dc6059593c7ed5e0b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465914"
---
# <a name="em_callautocorrectproc-message"></a><span data-ttu-id="e81cc-104">\_Message CALLAUTOCORRECTPROC em</span><span class="sxs-lookup"><span data-stu-id="e81cc-104">EM\_CALLAUTOCORRECTPROC message</span></span>

<span data-ttu-id="e81cc-105">Appelle la fonction de rappel de correction automatique stockée par le message [**em \_ SETAUTOCORRECTPROC**](em-setautocorrectproc.md) , à condition que le texte qui précède le point d’insertion soit candidat à la correction automatique.</span><span class="sxs-lookup"><span data-stu-id="e81cc-105">Calls the autocorrect callback function that is stored by the [**EM\_SETAUTOCORRECTPROC**](em-setautocorrectproc.md) message, provided that the text preceding the insertion point is a candidate for autocorrection.</span></span>


```C++
#define EM_CALLAUTOCORRECTPROC       (WM_USER + 255)
```



## <a name="parameters"></a><span data-ttu-id="e81cc-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e81cc-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e81cc-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="e81cc-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e81cc-108">Caractère de type **WCHAR**.</span><span class="sxs-lookup"><span data-stu-id="e81cc-108">A character of type **WCHAR**.</span></span> <span data-ttu-id="e81cc-109">Si ce caractère est une tabulation (U + 0009) et que le caractère qui précède le point d’insertion n’est pas un onglet, alors le caractère qui précède le point d’insertion est traité dans le cadre de la chaîne du candidat à la correction automatique et non sous la forme d’un délimiteur de chaîne. Sinon, *wParam* n’a aucun effet.</span><span class="sxs-lookup"><span data-stu-id="e81cc-109">If this character is a tab (U+0009), and the character preceding the insertion point isn t a tab, then the character preceding the insertion point is treated as part of the autocorrect candidate string instead of as a string delimiter; otherwise, *wParam* has no effect.</span></span>

</dd> <dt>

<span data-ttu-id="e81cc-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="e81cc-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e81cc-111">Non utilisé ; doit être égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="e81cc-111">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e81cc-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="e81cc-112">Return value</span></span>

<span data-ttu-id="e81cc-113">La valeur de retour est égale à zéro si le message a été correctement effectué, ou différent de zéro si une erreur se produit.</span><span class="sxs-lookup"><span data-stu-id="e81cc-113">The return value is zero if the message succeeds, or nonzero if an error occurs.</span></span>

## <a name="requirements"></a><span data-ttu-id="e81cc-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e81cc-114">Requirements</span></span>



| <span data-ttu-id="e81cc-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e81cc-115">Requirement</span></span> | <span data-ttu-id="e81cc-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="e81cc-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e81cc-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e81cc-117">Minimum supported client</span></span><br/> | <span data-ttu-id="e81cc-118">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e81cc-118">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="e81cc-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e81cc-119">Minimum supported server</span></span><br/> | <span data-ttu-id="e81cc-120">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e81cc-120">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="e81cc-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="e81cc-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="e81cc-122"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="e81cc-122"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e81cc-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e81cc-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e81cc-124">*AutoCorrectProc*</span><span class="sxs-lookup"><span data-stu-id="e81cc-124">*AutoCorrectProc*</span></span>](/windows/desktop/api/Richedit/nc-richedit-autocorrectproc)
</dt> <dt>

[<span data-ttu-id="e81cc-125">**\_GETAUTOCORRECTPROC em**</span><span class="sxs-lookup"><span data-stu-id="e81cc-125">**EM\_GETAUTOCORRECTPROC**</span></span>](em-getautocorrectproc.md)
</dt> <dt>

[<span data-ttu-id="e81cc-126">**\_SETAUTOCORRECTPROC em**</span><span class="sxs-lookup"><span data-stu-id="e81cc-126">**EM\_SETAUTOCORRECTPROC**</span></span>](em-setautocorrectproc.md)
</dt> </dl>

 

 





