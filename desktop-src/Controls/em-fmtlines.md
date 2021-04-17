---
title: Message EM_FMTLINES (winuser. h)
description: Définit un indicateur qui détermine si un contrôle d’édition multiligne contient des caractères de saut de ligne conditionnels. Un saut de ligne conditionnel se compose de deux retours chariot et d’un saut de ligne et est inséré à la fin d’une ligne qui est cassée en raison de wordwrapping.
ms.assetid: bfc08062-b0a7-4ba7-8858-00cb20895c77
keywords:
- EM_FMTLINES les contrôles de message Windows
topic_type:
- apiref
api_name:
- EM_FMTLINES
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7c12a22ee8c30ffa74705f670a16caa3651e9b44
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465575"
---
# <a name="em_fmtlines-message"></a><span data-ttu-id="0e9b7-105">\_Message FMTLINES em</span><span class="sxs-lookup"><span data-stu-id="0e9b7-105">EM\_FMTLINES message</span></span>

<span data-ttu-id="0e9b7-106">Définit un indicateur qui détermine si un contrôle d’édition multiligne contient des caractères de saut de ligne conditionnels.</span><span class="sxs-lookup"><span data-stu-id="0e9b7-106">Sets a flag that determines whether a multiline edit control includes soft line-break characters.</span></span> <span data-ttu-id="0e9b7-107">Un saut de ligne conditionnel se compose de deux retours chariot et d’un saut de ligne et est inséré à la fin d’une ligne qui est cassée en raison de wordwrapping.</span><span class="sxs-lookup"><span data-stu-id="0e9b7-107">A soft line break consists of two carriage returns and a line feed and is inserted at the end of a line that is broken because of wordwrapping.</span></span>

## <a name="parameters"></a><span data-ttu-id="0e9b7-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="0e9b7-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0e9b7-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="0e9b7-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="0e9b7-110">Spécifie si les caractères de saut de ligne conditionnel doivent être insérés.</span><span class="sxs-lookup"><span data-stu-id="0e9b7-110">Specifies whether soft line-break characters are to be inserted.</span></span> <span data-ttu-id="0e9b7-111">La valeur **true** insère les caractères ; la valeur **false** les supprime.</span><span class="sxs-lookup"><span data-stu-id="0e9b7-111">A value of **TRUE** inserts the characters; a value of **FALSE** removes them.</span></span>

</dd> <dt>

<span data-ttu-id="0e9b7-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="0e9b7-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="0e9b7-113">Ce paramètre n'est pas utilisé.</span><span class="sxs-lookup"><span data-stu-id="0e9b7-113">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0e9b7-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="0e9b7-114">Return value</span></span>

<span data-ttu-id="0e9b7-115">La valeur de retour est identique au paramètre *wParam* .</span><span class="sxs-lookup"><span data-stu-id="0e9b7-115">The return value is identical to the *wParam* parameter.</span></span>

## <a name="remarks"></a><span data-ttu-id="0e9b7-116">Notes</span><span class="sxs-lookup"><span data-stu-id="0e9b7-116">Remarks</span></span>

<span data-ttu-id="0e9b7-117">Ce message affecte uniquement la mémoire tampon retournée par le message [**em \_ GETHANDLE**](em-gethandle.md) et le texte retourné par le message [**WM \_ GETTEXT**](/windows/desktop/winmsg/wm-gettext) .</span><span class="sxs-lookup"><span data-stu-id="0e9b7-117">This message affects only the buffer returned by the [**EM\_GETHANDLE**](em-gethandle.md) message and the text returned by the [**WM\_GETTEXT**](/windows/desktop/winmsg/wm-gettext) message.</span></span> <span data-ttu-id="0e9b7-118">Elle n’a aucun effet sur l’affichage du texte dans le contrôle d’édition.</span><span class="sxs-lookup"><span data-stu-id="0e9b7-118">It has no effect on the display of the text within the edit control.</span></span>

<span data-ttu-id="0e9b7-119">Le **message \_ FMTLINES em** n’affecte pas une ligne qui se termine par un saut de ligne matériel.</span><span class="sxs-lookup"><span data-stu-id="0e9b7-119">The **EM\_FMTLINES** message does not affect a line that ends with a hard line break.</span></span> <span data-ttu-id="0e9b7-120">Un saut de ligne matériel consiste en un retour chariot et un saut de ligne.</span><span class="sxs-lookup"><span data-stu-id="0e9b7-120">A hard line break consists of one carriage return and a line feed.</span></span>

> [!Note]  
> <span data-ttu-id="0e9b7-121">Taille du texte modifié lors du traitement de ce message.</span><span class="sxs-lookup"><span data-stu-id="0e9b7-121">The size of the text changes when this message is processed.</span></span>

 

<span data-ttu-id="0e9b7-122">**Modification riche :** Le **message \_ FMTLINES em** n’est pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="0e9b7-122">**Rich Edit:** The **EM\_FMTLINES** message is not supported.</span></span>

## <a name="requirements"></a><span data-ttu-id="0e9b7-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0e9b7-123">Requirements</span></span>



| <span data-ttu-id="0e9b7-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0e9b7-124">Requirement</span></span> | <span data-ttu-id="0e9b7-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="0e9b7-125">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0e9b7-126">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0e9b7-126">Minimum supported client</span></span><br/> | <span data-ttu-id="0e9b7-127">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="0e9b7-127">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="0e9b7-128">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0e9b7-128">Minimum supported server</span></span><br/> | <span data-ttu-id="0e9b7-129">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="0e9b7-129">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="0e9b7-130">En-tête</span><span class="sxs-lookup"><span data-stu-id="0e9b7-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="0e9b7-131"><dt>Winuser. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="0e9b7-131"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0e9b7-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0e9b7-132">See also</span></span>

<dl> <dt>

<span data-ttu-id="0e9b7-133">**Référence**</span><span class="sxs-lookup"><span data-stu-id="0e9b7-133">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="0e9b7-134">**EM \_ GETHANDLE**</span><span class="sxs-lookup"><span data-stu-id="0e9b7-134">**EM\_GETHANDLE**</span></span>](em-gethandle.md)
</dt> <dt>

<span data-ttu-id="0e9b7-135">**Autres ressources**</span><span class="sxs-lookup"><span data-stu-id="0e9b7-135">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="0e9b7-136">**WM \_ GETTEXT**</span><span class="sxs-lookup"><span data-stu-id="0e9b7-136">**WM\_GETTEXT**</span></span>](/windows/desktop/winmsg/wm-gettext)
</dt> </dl>

 

