---
title: Message EM_GETIMECOMPTEXT (RichEdit. h)
description: Récupère le texte de la composition de l’éditeur de méthode d’entrée (IME).
ms.assetid: 1516305c-5f87-4ae0-97db-8709c71abacc
keywords:
- EM_GETIMECOMPTEXT les contrôles de message Windows
topic_type:
- apiref
api_name:
- EM_GETIMECOMPTEXT
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 834c55d6b5e40de7dcacfeb3e2d0c2e0878a0f3a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942485"
---
# <a name="em_getimecomptext-message"></a><span data-ttu-id="cd627-104">\_Message GETIMECOMPTEXT em</span><span class="sxs-lookup"><span data-stu-id="cd627-104">EM\_GETIMECOMPTEXT message</span></span>

<span data-ttu-id="cd627-105">Récupère le texte de la composition de l’éditeur de méthode d’entrée (IME).</span><span class="sxs-lookup"><span data-stu-id="cd627-105">Retrieves the Input Method Editor (IME) composition text.</span></span>

## <a name="parameters"></a><span data-ttu-id="cd627-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="cd627-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cd627-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="cd627-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="cd627-108">Structure [**IMECOMPTEXT**](/windows/desktop/api/Richedit/ns-richedit-imecomptext) .</span><span class="sxs-lookup"><span data-stu-id="cd627-108">The [**IMECOMPTEXT**](/windows/desktop/api/Richedit/ns-richedit-imecomptext) structure.</span></span>

</dd> <dt>

<span data-ttu-id="cd627-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="cd627-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="cd627-110">Mémoire tampon qui reçoit le texte de composition.</span><span class="sxs-lookup"><span data-stu-id="cd627-110">The buffer that receives the composition text.</span></span> <span data-ttu-id="cd627-111">La taille de cette mémoire tampon est contenue dans le membre **CB** de la structure *wParam* .</span><span class="sxs-lookup"><span data-stu-id="cd627-111">The size of this buffer is contained in the **cb** member of the *wParam* structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cd627-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="cd627-112">Return value</span></span>

<span data-ttu-id="cd627-113">En cas de réussite, la valeur de retour est le nombre de caractères Unicode copiés dans la mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="cd627-113">If successful, the return value is the number of Unicode characters copied to the buffer.</span></span> <span data-ttu-id="cd627-114">Dans le cas contraire, il est égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="cd627-114">Otherwise, it is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="cd627-115">Notes</span><span class="sxs-lookup"><span data-stu-id="cd627-115">Remarks</span></span>

<span data-ttu-id="cd627-116">Ce message accepte uniquement les chaînes Unicode.</span><span class="sxs-lookup"><span data-stu-id="cd627-116">This message only takes Unicode strings.</span></span>

<span data-ttu-id="cd627-117">**Avertissement de sécurité :** Veillez à disposer d’une mémoire tampon suffisante pour la taille de l’entrée.</span><span class="sxs-lookup"><span data-stu-id="cd627-117">**Security Warning:** Be sure to have a buffer sufficient for the size of the input.</span></span> <span data-ttu-id="cd627-118">Dans le cas contraire, vous risquez de rencontrer des problèmes pour votre application.</span><span class="sxs-lookup"><span data-stu-id="cd627-118">Failure to do so could cause problems for your application.</span></span>

## <a name="requirements"></a><span data-ttu-id="cd627-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="cd627-119">Requirements</span></span>



| <span data-ttu-id="cd627-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="cd627-120">Requirement</span></span> | <span data-ttu-id="cd627-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="cd627-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="cd627-122">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="cd627-122">Minimum supported client</span></span><br/> | <span data-ttu-id="cd627-123">Windows XP avec les \[ applications de bureau SP1 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="cd627-123">Windows XP with SP1 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="cd627-124">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="cd627-124">Minimum supported server</span></span><br/> | <span data-ttu-id="cd627-125">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="cd627-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="cd627-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="cd627-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="cd627-127"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="cd627-127"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cd627-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="cd627-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cd627-129">**IMECOMPTEXT**</span><span class="sxs-lookup"><span data-stu-id="cd627-129">**IMECOMPTEXT**</span></span>](/windows/desktop/api/Richedit/ns-richedit-imecomptext)
</dt> </dl>

 

 





