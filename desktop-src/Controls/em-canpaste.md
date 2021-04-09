---
title: Message EM_CANPASTE (RichEdit. h)
description: Détermine si un contrôle RichEdit peut coller un format de presse-papiers spécifié.
ms.assetid: 1b858ad8-1312-407b-b12a-c63668ba9f72
keywords:
- EM_CANPASTE les contrôles de message Windows
topic_type:
- apiref
api_name:
- EM_CANPASTE
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aad400b610a033b6f67177da99876a892d294ec8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104033021"
---
# <a name="em_canpaste-message"></a><span data-ttu-id="17590-104">\_Message de CANPASTE em</span><span class="sxs-lookup"><span data-stu-id="17590-104">EM\_CANPASTE message</span></span>

<span data-ttu-id="17590-105">Détermine si un contrôle RichEdit peut coller un format de presse-papiers spécifié.</span><span class="sxs-lookup"><span data-stu-id="17590-105">Determines whether a rich edit control can paste a specified clipboard format.</span></span>

## <a name="parameters"></a><span data-ttu-id="17590-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="17590-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="17590-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="17590-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="17590-108">Spécifie les [formats du presse-papiers](/windows/desktop/dataxchg/clipboard-formats) à essayer.</span><span class="sxs-lookup"><span data-stu-id="17590-108">Specifies the [Clipboard Formats](/windows/desktop/dataxchg/clipboard-formats) to try.</span></span> <span data-ttu-id="17590-109">Pour essayer un format qui se trouve actuellement dans le presse-papiers, définissez ce paramètre sur zéro.</span><span class="sxs-lookup"><span data-stu-id="17590-109">To try any format currently on the clipboard, set this parameter to zero.</span></span>

</dd> <dt>

<span data-ttu-id="17590-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="17590-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="17590-111">Ce paramètre n’est pas utilisé ; elle doit être égale à zéro.</span><span class="sxs-lookup"><span data-stu-id="17590-111">This parameter is not used; it must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="17590-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="17590-112">Return value</span></span>

<span data-ttu-id="17590-113">Si le format du presse-papiers peut être collé, la valeur de retour est une valeur différente de zéro.</span><span class="sxs-lookup"><span data-stu-id="17590-113">If the clipboard format can be pasted, the return value is a nonzero value.</span></span>

<span data-ttu-id="17590-114">Si le format du presse-papiers ne peut pas être collé, la valeur de retour est zéro.</span><span class="sxs-lookup"><span data-stu-id="17590-114">If the clipboard format cannot be pasted, the return value is zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="17590-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="17590-115">Requirements</span></span>



| <span data-ttu-id="17590-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="17590-116">Requirement</span></span> | <span data-ttu-id="17590-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="17590-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="17590-118">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="17590-118">Minimum supported client</span></span><br/> | <span data-ttu-id="17590-119">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="17590-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="17590-120">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="17590-120">Minimum supported server</span></span><br/> | <span data-ttu-id="17590-121">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="17590-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="17590-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="17590-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="17590-123"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="17590-123"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="17590-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="17590-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="17590-125">**SendMessage**</span><span class="sxs-lookup"><span data-stu-id="17590-125">**SendMessage**</span></span>](/windows/desktop/api/winuser/nf-winuser-sendmessage)
</dt> </dl>

 

