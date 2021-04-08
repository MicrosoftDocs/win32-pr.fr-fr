---
title: Message EM_GETHYPHENATEINFO (RichEdit. h)
description: Récupère des informations sur la césure pour un contrôle Rich Edit Microsoft.
ms.assetid: 70ccb698-e440-493b-8f38-2bf7f32e4b26
keywords:
- EM_GETHYPHENATEINFO les contrôles de message Windows
topic_type:
- apiref
api_name:
- EM_GETHYPHENATEINFO
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5d083b4bbc4b6854f767395d51dd9899c2a185d0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104033058"
---
# <a name="em_gethyphenateinfo-message"></a><span data-ttu-id="35ffe-104">\_Message GETHYPHENATEINFO em</span><span class="sxs-lookup"><span data-stu-id="35ffe-104">EM\_GETHYPHENATEINFO message</span></span>

<span data-ttu-id="35ffe-105">Récupère des informations sur la césure pour un contrôle Rich Edit Microsoft.</span><span class="sxs-lookup"><span data-stu-id="35ffe-105">Retrieves information about hyphenation for a Microsoft Rich Edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="35ffe-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="35ffe-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="35ffe-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="35ffe-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="35ffe-108">Structure [**HYPHENATEINFO**](/windows/win32/api/richedit/ns-richedit-hyphenateinfo) .</span><span class="sxs-lookup"><span data-stu-id="35ffe-108">The [**HYPHENATEINFO**](/windows/win32/api/richedit/ns-richedit-hyphenateinfo) structure.</span></span>

</dd> <dt>

<span data-ttu-id="35ffe-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="35ffe-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="35ffe-110">Non utilisé ; doit être égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="35ffe-110">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="35ffe-111">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="35ffe-111">Requirements</span></span>



| <span data-ttu-id="35ffe-112">Condition requise</span><span class="sxs-lookup"><span data-stu-id="35ffe-112">Requirement</span></span> | <span data-ttu-id="35ffe-113">Valeur</span><span class="sxs-lookup"><span data-stu-id="35ffe-113">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="35ffe-114">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="35ffe-114">Minimum supported client</span></span><br/> | <span data-ttu-id="35ffe-115">Windows XP avec les \[ applications de bureau SP1 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="35ffe-115">Windows XP with SP1 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="35ffe-116">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="35ffe-116">Minimum supported server</span></span><br/> | <span data-ttu-id="35ffe-117">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="35ffe-117">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="35ffe-118">En-tête</span><span class="sxs-lookup"><span data-stu-id="35ffe-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="35ffe-119"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="35ffe-119"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="35ffe-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="35ffe-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="35ffe-121">**\_SETHYPHENATEINFO em**</span><span class="sxs-lookup"><span data-stu-id="35ffe-121">**EM\_SETHYPHENATEINFO**</span></span>](em-sethyphenateinfo.md)
</dt> </dl>

 

 





