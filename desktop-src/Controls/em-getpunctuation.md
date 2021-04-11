---
title: Message EM_GETPUNCTUATION (RichEdit. h)
description: Obtient les caractères de ponctuation actuels pour le contrôle RichEdit.
ms.assetid: 1c04967b-d75e-4f54-b35b-cd50bac9cdfa
keywords:
- EM_GETPUNCTUATION les contrôles de message Windows
topic_type:
- apiref
api_name:
- EM_GETPUNCTUATION
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 158c26deca3328d9cdbed7ffe7cf885b0582d1a0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105298"
---
# <a name="em_getpunctuation-message"></a><span data-ttu-id="a833f-104">\_Message GETPUNCTUATION em</span><span class="sxs-lookup"><span data-stu-id="a833f-104">EM\_GETPUNCTUATION message</span></span>

<span data-ttu-id="a833f-105">Obtient les caractères de ponctuation actuels pour le contrôle RichEdit.</span><span class="sxs-lookup"><span data-stu-id="a833f-105">Gets the current punctuation characters for the rich edit control.</span></span>

> [!Note]  
> <span data-ttu-id="a833f-106">Ce message est pris en charge uniquement dans les versions asiatiques de Microsoft Rich Edit 1,0.</span><span class="sxs-lookup"><span data-stu-id="a833f-106">This message is supported only in Asian-language versions of Microsoft Rich Edit 1.0.</span></span> <span data-ttu-id="a833f-107">Elle n’est pas prise en charge dans les versions ultérieures de la modification enrichie.</span><span class="sxs-lookup"><span data-stu-id="a833f-107">It is not supported in any later versions of Rich Edit.</span></span>

 

## <a name="parameters"></a><span data-ttu-id="a833f-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a833f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a833f-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="a833f-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a833f-110">Le type de ponctuation peut être l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="a833f-110">The punctuation type can be one of the following values.</span></span>



| <span data-ttu-id="a833f-111">Valeur</span><span class="sxs-lookup"><span data-stu-id="a833f-111">Value</span></span>                                                                                                                                                      | <span data-ttu-id="a833f-112">Signification</span><span class="sxs-lookup"><span data-stu-id="a833f-112">Meaning</span></span>                                     |
|------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------|
| <span id="PC_LEADING"></span><span id="pc_leading"></span><dl> <span data-ttu-id="a833f-113"><dt>**PC \_ leader**</dt></span><span class="sxs-lookup"><span data-stu-id="a833f-113"><dt>**PC\_LEADING**</dt></span></span> </dl>       | <span data-ttu-id="a833f-114">Caractères de ponctuation de début</span><span class="sxs-lookup"><span data-stu-id="a833f-114">Leading punctuation characters</span></span><br/>   |
| <span id="PC_FOLLOWING"></span><span id="pc_following"></span><dl> <span data-ttu-id="a833f-115"><dt>**PC \_ suivant**</dt></span><span class="sxs-lookup"><span data-stu-id="a833f-115"><dt>**PC\_FOLLOWING**</dt></span></span> </dl> | <span data-ttu-id="a833f-116">Caractères de ponctuation suivants</span><span class="sxs-lookup"><span data-stu-id="a833f-116">Following punctuation characters</span></span><br/> |
| <span id="PC_DELIMITER"></span><span id="pc_delimiter"></span><dl> <span data-ttu-id="a833f-117"><dt>**délimiteur de PC \_**</dt></span><span class="sxs-lookup"><span data-stu-id="a833f-117"><dt>**PC\_DELIMITER**</dt></span></span> </dl> | <span data-ttu-id="a833f-118">Délimiteur</span><span class="sxs-lookup"><span data-stu-id="a833f-118">Delimiter</span></span><br/>                        |
| <span id="PC_OVERFLOW"></span><span id="pc_overflow"></span><dl> <span data-ttu-id="a833f-119"><dt>**dépassement du PC \_**</dt></span><span class="sxs-lookup"><span data-stu-id="a833f-119"><dt>**PC\_OVERFLOW**</dt></span></span> </dl>    | <span data-ttu-id="a833f-120">Non pris en charge</span><span class="sxs-lookup"><span data-stu-id="a833f-120">Not supported</span></span><br/>                    |



 

</dd> <dt>

<span data-ttu-id="a833f-121">*lParam*</span><span class="sxs-lookup"><span data-stu-id="a833f-121">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a833f-122">Pointeur vers une structure de [**ponctuation**](/windows/desktop/api/Richedit/ns-richedit-punctuation) qui reçoit les caractères de ponctuation.</span><span class="sxs-lookup"><span data-stu-id="a833f-122">Pointer to a [**PUNCTUATION**](/windows/desktop/api/Richedit/ns-richedit-punctuation) structure that receives the punctuation characters.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a833f-123">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="a833f-123">Return value</span></span>

<span data-ttu-id="a833f-124">Si l’opération a échoué, la valeur de retour est une valeur différente de zéro.</span><span class="sxs-lookup"><span data-stu-id="a833f-124">If the operation succeeds, the return value is a nonzero value.</span></span>

<span data-ttu-id="a833f-125">Si l’opération échoue, la valeur de retour est zéro.</span><span class="sxs-lookup"><span data-stu-id="a833f-125">If the operation fails, the return value is zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="a833f-126">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a833f-126">Requirements</span></span>



| <span data-ttu-id="a833f-127">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a833f-127">Requirement</span></span> | <span data-ttu-id="a833f-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="a833f-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a833f-129">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a833f-129">Minimum supported client</span></span><br/> | <span data-ttu-id="a833f-130">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a833f-130">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="a833f-131">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a833f-131">Minimum supported server</span></span><br/> | <span data-ttu-id="a833f-132">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a833f-132">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="a833f-133">En-tête</span><span class="sxs-lookup"><span data-stu-id="a833f-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="a833f-134"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="a833f-134"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a833f-135">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a833f-135">See also</span></span>

<dl> <dt>

<span data-ttu-id="a833f-136">**Référence**</span><span class="sxs-lookup"><span data-stu-id="a833f-136">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="a833f-137">**\_SETPUNCTUATION em**</span><span class="sxs-lookup"><span data-stu-id="a833f-137">**EM\_SETPUNCTUATION**</span></span>](em-setpunctuation.md)
</dt> <dt>

[<span data-ttu-id="a833f-138">**PONCTUATION**</span><span class="sxs-lookup"><span data-stu-id="a833f-138">**PUNCTUATION**</span></span>](/windows/desktop/api/Richedit/ns-richedit-punctuation)
</dt> </dl>

 

 





