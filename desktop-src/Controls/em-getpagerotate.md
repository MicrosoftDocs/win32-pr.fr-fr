---
title: Message EM_GETPAGEROTATE (RichEdit. h)
description: Obtient la disposition du texte pour un contrôle RichEdit Microsoft.
ms.assetid: 0efb112e-ad51-4ebb-9037-3aee3ab9ad1d
keywords:
- EM_GETPAGEROTATE les contrôles de message Windows
topic_type:
- apiref
api_name:
- EM_GETPAGEROTATE
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ad7bc7cd3c77ae88cd4c8710e14b4472e57407ca
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466559"
---
# <a name="em_getpagerotate-message"></a><span data-ttu-id="f3c5d-104">\_Message GETPAGEROTATE em</span><span class="sxs-lookup"><span data-stu-id="f3c5d-104">EM\_GETPAGEROTATE message</span></span>

<span data-ttu-id="f3c5d-105">\[**Em \_ GETPAGEROTATE** peut être utilisé dans les systèmes d’exploitation spécifiés dans la section Configuration requise.</span><span class="sxs-lookup"><span data-stu-id="f3c5d-105">\[**EM\_GETPAGEROTATE** is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="f3c5d-106">Il sera peut-être modifié ou indisponible dans les versions ultérieures.\]</span><span class="sxs-lookup"><span data-stu-id="f3c5d-106">It may be altered or unavailable in subsequent versions.\]</span></span>

<span data-ttu-id="f3c5d-107">Obtient la disposition du texte pour un contrôle RichEdit Microsoft.</span><span class="sxs-lookup"><span data-stu-id="f3c5d-107">Gets the text layout for a Microsoft Rich Edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="f3c5d-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f3c5d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f3c5d-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="f3c5d-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f3c5d-110">Non utilisé ; doit être égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="f3c5d-110">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="f3c5d-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="f3c5d-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f3c5d-112">Non utilisé ; doit être égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="f3c5d-112">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f3c5d-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="f3c5d-113">Return value</span></span>

<span data-ttu-id="f3c5d-114">Obtient la disposition du texte actuel.</span><span class="sxs-lookup"><span data-stu-id="f3c5d-114">Gets the current text layout.</span></span> <span data-ttu-id="f3c5d-115">Pour obtenir la liste des valeurs de disposition du texte possibles, consultez [**em \_ SETPAGEROTATE**](em-setpagerotate.md).</span><span class="sxs-lookup"><span data-stu-id="f3c5d-115">For a list of possible text layout values, see [**EM\_SETPAGEROTATE**](em-setpagerotate.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="f3c5d-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f3c5d-116">Requirements</span></span>



| <span data-ttu-id="f3c5d-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f3c5d-117">Requirement</span></span> | <span data-ttu-id="f3c5d-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="f3c5d-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f3c5d-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f3c5d-119">Minimum supported client</span></span><br/> | <span data-ttu-id="f3c5d-120">Windows XP avec les \[ applications de bureau SP1 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f3c5d-120">Windows XP with SP1 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="f3c5d-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f3c5d-121">Minimum supported server</span></span><br/> | <span data-ttu-id="f3c5d-122">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f3c5d-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="f3c5d-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="f3c5d-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="f3c5d-124"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="f3c5d-124"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f3c5d-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f3c5d-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f3c5d-126">**\_SETPAGEROTATE em**</span><span class="sxs-lookup"><span data-stu-id="f3c5d-126">**EM\_SETPAGEROTATE**</span></span>](em-setpagerotate.md)
</dt> </dl>

 

 





