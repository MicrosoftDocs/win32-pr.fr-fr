---
title: Code de notification EN_CORRECTTEXT (RichEdit. h)
description: Avertit une fenêtre parente du contrôle RichEdit qu’un \_ geste SyV correct s’est produit, donnant à la fenêtre parente la possibilité d’annuler la correction du texte. Un contrôle RichEdit envoie ce code de notification sous la forme d’un \_ message WM Notify.
ms.assetid: d6f6278f-ff63-4f6a-a352-2b4d70df3e1a
keywords:
- Contrôles Windows de code de notification EN_CORRECTTEXT
topic_type:
- apiref
api_name:
- EN_CORRECTTEXT
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e5d1339513a94967ab60bdab2b9ee39172b19e76
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104102981"
---
# <a name="en_correcttext-notification-code"></a><span data-ttu-id="2b739-105">\_Code de notification en CORRECTTEXT</span><span class="sxs-lookup"><span data-stu-id="2b739-105">EN\_CORRECTTEXT notification code</span></span>

<span data-ttu-id="2b739-106">Avertit une fenêtre parente du contrôle RichEdit qu’un \_ geste SyV correct s’est produit, donnant à la fenêtre parente la possibilité d’annuler la correction du texte.</span><span class="sxs-lookup"><span data-stu-id="2b739-106">Notifies a rich edit control parent window that a SYV\_CORRECT gesture occurred, giving the parent window a chance to cancel correcting the text.</span></span> <span data-ttu-id="2b739-107">Un contrôle RichEdit envoie ce code de notification sous la forme d’un message [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="2b739-107">A rich edit control sends this notification code in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
EN_CORRECTTEXT

    penCorrectText = (ENCORRECTTEXT *) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="2b739-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="2b739-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2b739-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="2b739-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="2b739-110">Structure [**ENCORRECTTEXT**](/windows/desktop/api/Richedit/ns-richedit-encorrecttext) spécifiant la sélection à corriger.</span><span class="sxs-lookup"><span data-stu-id="2b739-110">An [**ENCORRECTTEXT**](/windows/desktop/api/Richedit/ns-richedit-encorrecttext) structure specifying the selection to be corrected.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2b739-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="2b739-111">Return value</span></span>

<span data-ttu-id="2b739-112">Retournez zéro pour ignorer l’action.</span><span class="sxs-lookup"><span data-stu-id="2b739-112">Return zero to ignore the action.</span></span>

<span data-ttu-id="2b739-113">Retourne une valeur différente de zéro pour traiter l’action.</span><span class="sxs-lookup"><span data-stu-id="2b739-113">Returns a nonzero value to process the action.</span></span>

## <a name="remarks"></a><span data-ttu-id="2b739-114">Notes</span><span class="sxs-lookup"><span data-stu-id="2b739-114">Remarks</span></span>

<span data-ttu-id="2b739-115">Ce code de notification est envoyé uniquement si les fonctionnalités du stylet sont disponibles.</span><span class="sxs-lookup"><span data-stu-id="2b739-115">This notification code is sent only if pen capabilities are available.</span></span>

<span data-ttu-id="2b739-116">Pour recevoir les \_ codes de notification en CORRECTTEXT, spécifiez [**ENM \_ CORRECTTEXT**](rich-edit-control-event-mask-flags.md) dans le masque envoyé avec le message de [**em \_ SETEVENTMASK**](em-seteventmask.md) .</span><span class="sxs-lookup"><span data-stu-id="2b739-116">To receive EN\_CORRECTTEXT notification codes, specify [**ENM\_CORRECTTEXT**](rich-edit-control-event-mask-flags.md) in the mask sent with the [**EM\_SETEVENTMASK**](em-seteventmask.md) message.</span></span>

> [!Note]  
> <span data-ttu-id="2b739-117">Le \_ Code de notification en CORRECTTEXT est uniquement pris en charge dans la version Rich edit 1,0.</span><span class="sxs-lookup"><span data-stu-id="2b739-117">The EN\_CORRECTTEXT notification code is only supported in rich edit version 1.0.</span></span> <span data-ttu-id="2b739-118">Elle n’est pas prise en charge dans les versions ultérieures de la modification enrichie.</span><span class="sxs-lookup"><span data-stu-id="2b739-118">It is not supported in later versions of rich edit.</span></span> <span data-ttu-id="2b739-119">Pour plus d’informations sur la compatibilité des versions RichEdit avec les différentes versions du système, consultez [à propos des contrôles](about-rich-edit-controls.md)RichEdit.</span><span class="sxs-lookup"><span data-stu-id="2b739-119">For information about the compatibility of rich edit versions with the various system versions, see [About Rich Edit Controls](about-rich-edit-controls.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="2b739-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="2b739-120">Requirements</span></span>



| <span data-ttu-id="2b739-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="2b739-121">Requirement</span></span> | <span data-ttu-id="2b739-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="2b739-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="2b739-123">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2b739-123">Minimum supported client</span></span><br/> | <span data-ttu-id="2b739-124">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="2b739-124">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="2b739-125">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2b739-125">Minimum supported server</span></span><br/> | <span data-ttu-id="2b739-126">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="2b739-126">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="2b739-127">En-tête</span><span class="sxs-lookup"><span data-stu-id="2b739-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="2b739-128"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="2b739-128"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2b739-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2b739-129">See also</span></span>

<dl> <dt>

<span data-ttu-id="2b739-130">**Référence**</span><span class="sxs-lookup"><span data-stu-id="2b739-130">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="2b739-131">**ENCORRECTTEXT**</span><span class="sxs-lookup"><span data-stu-id="2b739-131">**ENCORRECTTEXT**</span></span>](/windows/desktop/api/Richedit/ns-richedit-encorrecttext)
</dt> </dl>

 

 





