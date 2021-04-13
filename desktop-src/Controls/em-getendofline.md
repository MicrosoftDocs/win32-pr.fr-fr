---
title: Message EM_GETENDOFLINE (commctrl. h)
description: Récupère le caractère de fin de ligne utilisé lors de l’insertion d’un LineBreak. Envoyez ce message explicitement ou à l’aide de la \_ macro Edit GetEndOfLine.
ms.assetid: 557f796e-c9d1-4ea1-b8a6-44ae0bed5ffc
keywords:
- EM_GETENDOFLINE les contrôles de message Windows
topic_type:
- apiref
api_name:
- EM_GETENDOFLINE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 10/19/2018
ms.openlocfilehash: 98d537d2ea4239ab3f511666aeba46be93a2b881
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464546"
---
# <a name="em_getendofline-message"></a><span data-ttu-id="eee92-105">\_Message GETENDOFLINE em</span><span class="sxs-lookup"><span data-stu-id="eee92-105">EM\_GETENDOFLINE message</span></span>

<span data-ttu-id="eee92-106">Récupère le caractère de fin de ligne d’un contrôle d’édition.</span><span class="sxs-lookup"><span data-stu-id="eee92-106">Retrieves the end-of-line character for an edit control.</span></span> <span data-ttu-id="eee92-107">Envoyez ce message explicitement ou à l’aide de la macro [**Edit \_ GetEndOfLine**](/windows/desktop/api/Commctrl/nf-commctrl-edit_getendofline) .</span><span class="sxs-lookup"><span data-stu-id="eee92-107">Send this message explicitly or by using the [**Edit\_GetEndOfLine**](/windows/desktop/api/Commctrl/nf-commctrl-edit_getendofline) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="eee92-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="eee92-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="eee92-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="eee92-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="eee92-110">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="eee92-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="eee92-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="eee92-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="eee92-112">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="eee92-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="eee92-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="eee92-113">Return value</span></span>

<span data-ttu-id="eee92-114">Retourne le caractère de fin de ligne utilisé par le contrôle d’édition.</span><span class="sxs-lookup"><span data-stu-id="eee92-114">Returns the end-of-line character used by the edit control.</span></span> <span data-ttu-id="eee92-115">Il peut s’agir de l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="eee92-115">This can be one of the following values.</span></span>

| <span data-ttu-id="eee92-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="eee92-116">Value</span></span>                                                                                                                                                   | <span data-ttu-id="eee92-117">Signification</span><span class="sxs-lookup"><span data-stu-id="eee92-117">Meaning</span></span>                                                                                        |
|---------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| <span id="EC_ENDOFLINE_CRLF"></span><span id="ec_endofline_crlf"></span><dl> <span data-ttu-id="eee92-118"><dt>**\_ENDOFLINE ce \_ CRLF**</dt></span><span class="sxs-lookup"><span data-stu-id="eee92-118"><dt>**EC\_ENDOFLINE\_CRLF**</dt></span></span> </dl> | <span data-ttu-id="eee92-119">Le caractère de fin de ligne utilisé pour le nouveau sauts est le retour chariot suivi du saut de ligne (CRLF).</span><span class="sxs-lookup"><span data-stu-id="eee92-119">The end-of-line character used for new linebreaks is carriage return followed by linefeed (CRLF).</span></span><br/> |
| <span id="EC_ENDOFLINE_CR"></span><span id="ec_endofline_cr"></span><dl> <span data-ttu-id="eee92-120"><dt>**\_ENDOFLINE ce \_ CR**</dt></span><span class="sxs-lookup"><span data-stu-id="eee92-120"><dt>**EC\_ENDOFLINE\_CR**</dt></span></span> </dl>       | <span data-ttu-id="eee92-121">Le caractère de fin de ligne utilisé pour le nouveau sauts est le retour chariot (CR).</span><span class="sxs-lookup"><span data-stu-id="eee92-121">The end-of-line character used for new linebreaks is carriage return (CR).</span></span><br/>                        |
| <span id="EC_ENDOFLINE_LF"></span><span id="ec_endofline_lf"></span><dl> <span data-ttu-id="eee92-122"><dt>**EC \_ ENDOFLINE \_ LF**</dt></span><span class="sxs-lookup"><span data-stu-id="eee92-122"><dt>**EC\_ENDOFLINE\_LF**</dt></span></span> </dl>       | <span data-ttu-id="eee92-123">Le caractère de fin de ligne utilisé pour le nouveau sauts est un saut de ligne (LF).</span><span class="sxs-lookup"><span data-stu-id="eee92-123">The end-of-line character used for new linebreaks is linefeed (LF).</span></span><br/>                               |

## <a name="remarks"></a><span data-ttu-id="eee92-124">Notes</span><span class="sxs-lookup"><span data-stu-id="eee92-124">Remarks</span></span>

<span data-ttu-id="eee92-125">Lorsque le caractère de fin de ligne utilisé est défini sur **EC \_ ENDOFLINE \_ DETECTFROMCONTENT** à l’aide de [**Edit \_ SetEndOfLine**](/windows/desktop/api/Commctrl/nf-commctrl-edit_setendofline), ce message retourne le caractère de fin de ligne détecté.</span><span class="sxs-lookup"><span data-stu-id="eee92-125">When the end-of-line character used is set to **EC\_ENDOFLINE\_DETECTFROMCONTENT** using [**Edit\_SetEndOfLine**](/windows/desktop/api/Commctrl/nf-commctrl-edit_setendofline), this message will return the detected end-of-line character.</span></span>

## <a name="requirements"></a><span data-ttu-id="eee92-126">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="eee92-126">Requirements</span></span>



| <span data-ttu-id="eee92-127">Condition requise</span><span class="sxs-lookup"><span data-stu-id="eee92-127">Requirement</span></span> | <span data-ttu-id="eee92-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="eee92-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="eee92-129">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="eee92-129">Minimum supported client</span></span><br/> | <span data-ttu-id="eee92-130">Applications de bureau Windows 10, version 1809 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="eee92-130">Windows 10, version 1809 \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="eee92-131">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="eee92-131">Minimum supported server</span></span><br/> | <span data-ttu-id="eee92-132">Applications de bureau Windows Server 2019 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="eee92-132">Windows Server 2019 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="eee92-133">En-tête</span><span class="sxs-lookup"><span data-stu-id="eee92-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="eee92-134"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="eee92-134"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="eee92-135">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="eee92-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eee92-136">\**\_SETENDOFLINE em*</span><span class="sxs-lookup"><span data-stu-id="eee92-136">\**EM\_SETENDOFLINE*</span></span>](em-setendofline.md)
</dt> </dl>
 

 





