---
title: Message EM_FORMATRANGE (RichEdit. h)
description: Met en forme une plage de texte dans un contrôle RichEdit pour un appareil spécifique.
ms.assetid: 6d1e562b-d741-4d4a-a395-554083cb0dbb
keywords:
- EM_FORMATRANGE les contrôles de message Windows
topic_type:
- apiref
api_name:
- EM_FORMATRANGE
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f8f235fb054643623510ea23e73001aaeb070be3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843713"
---
# <a name="em_formatrange-message"></a><span data-ttu-id="c75b8-104">\_Message FormatRange em</span><span class="sxs-lookup"><span data-stu-id="c75b8-104">EM\_FORMATRANGE message</span></span>

<span data-ttu-id="c75b8-105">Met en forme une plage de texte dans un contrôle RichEdit pour un appareil spécifique.</span><span class="sxs-lookup"><span data-stu-id="c75b8-105">Formats a range of text in a rich edit control for a specific device.</span></span>

## <a name="parameters"></a><span data-ttu-id="c75b8-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c75b8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c75b8-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="c75b8-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c75b8-108">Spécifie s’il faut restituer le texte.</span><span class="sxs-lookup"><span data-stu-id="c75b8-108">Specifies whether to render the text.</span></span> <span data-ttu-id="c75b8-109">Si ce paramètre n’est pas égal à zéro, le texte est rendu.</span><span class="sxs-lookup"><span data-stu-id="c75b8-109">If this parameter is not zero, the text is rendered.</span></span> <span data-ttu-id="c75b8-110">Dans le cas contraire, le texte est uniquement mesuré.</span><span class="sxs-lookup"><span data-stu-id="c75b8-110">Otherwise, the text is just measured.</span></span>

</dd> <dt>

<span data-ttu-id="c75b8-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="c75b8-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c75b8-112">Structure [**FormatRange**](/windows/desktop/api/Richedit/ns-richedit-formatrange) contenant des informations sur le périphérique de sortie, ou **null** pour libérer des informations mises en cache par le contrôle.</span><span class="sxs-lookup"><span data-stu-id="c75b8-112">A [**FORMATRANGE**](/windows/desktop/api/Richedit/ns-richedit-formatrange) structure containing information about the output device, or **NULL** to free information cached by the control.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c75b8-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="c75b8-113">Return value</span></span>

<span data-ttu-id="c75b8-114">Ce message retourne l’index du dernier caractère qui tient dans la région, plus 1.</span><span class="sxs-lookup"><span data-stu-id="c75b8-114">This message returns the index of the last character that fits in the region, plus 1.</span></span>

## <a name="remarks"></a><span data-ttu-id="c75b8-115">Notes</span><span class="sxs-lookup"><span data-stu-id="c75b8-115">Remarks</span></span>

<span data-ttu-id="c75b8-116">Ce message est généralement utilisé pour mettre en forme le contenu d’un contrôle RichEdit pour un périphérique de sortie tel qu’une imprimante.</span><span class="sxs-lookup"><span data-stu-id="c75b8-116">This message is typically used to format the content of rich edit control for an output device such as a printer.</span></span>

<span data-ttu-id="c75b8-117">Après avoir utilisé ce message pour mettre en forme une plage de texte, il est important de libérer les informations mises en cache en renvoyant **\_ FormatRange em** , mais avec *lParam* défini sur **null**; sinon, une fuite de mémoire se produit.</span><span class="sxs-lookup"><span data-stu-id="c75b8-117">After using this message to format a range of text, it is important that you free cached information by sending **EM\_FORMATRANGE** again, but with *lParam* set to **NULL**; otherwise, a memory leak will occur.</span></span> <span data-ttu-id="c75b8-118">De même, après avoir utilisé ce message pour un appareil, vous devez libérer les informations mises en cache avant de l’utiliser à nouveau pour un autre appareil.</span><span class="sxs-lookup"><span data-stu-id="c75b8-118">Also, after using this message for one device, you must free cached information before using it again for a different device.</span></span>

## <a name="requirements"></a><span data-ttu-id="c75b8-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c75b8-119">Requirements</span></span>



| <span data-ttu-id="c75b8-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c75b8-120">Requirement</span></span> | <span data-ttu-id="c75b8-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="c75b8-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c75b8-122">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c75b8-122">Minimum supported client</span></span><br/> | <span data-ttu-id="c75b8-123">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c75b8-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="c75b8-124">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c75b8-124">Minimum supported server</span></span><br/> | <span data-ttu-id="c75b8-125">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c75b8-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="c75b8-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="c75b8-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="c75b8-127"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="c75b8-127"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c75b8-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c75b8-128">See also</span></span>

<dl> <dt>

<span data-ttu-id="c75b8-129">**Référence**</span><span class="sxs-lookup"><span data-stu-id="c75b8-129">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="c75b8-130">**\_DISPLAYBAND em**</span><span class="sxs-lookup"><span data-stu-id="c75b8-130">**EM\_DISPLAYBAND**</span></span>](em-displayband.md)
</dt> <dt>

<span data-ttu-id="c75b8-131">**Méthodologique**</span><span class="sxs-lookup"><span data-stu-id="c75b8-131">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="c75b8-132">Impression de contrôles RichEdit</span><span class="sxs-lookup"><span data-stu-id="c75b8-132">Printing Rich Edit Controls</span></span>](printing-rich-edit-controls.md)
</dt> </dl>

 

 





