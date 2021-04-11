---
title: Message EM_SETPUNCTUATION (RichEdit. h)
description: Définit les caractères de ponctuation pour un contrôle RichEdit.
ms.assetid: c0c8ad14-63e2-4be8-8fc0-6b8ef9be4522
keywords:
- EM_SETPUNCTUATION les contrôles de message Windows
topic_type:
- apiref
api_name:
- EM_SETPUNCTUATION
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 710392cee7f7a1fb04fce59d6549134255499172
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105568"
---
# <a name="em_setpunctuation-message"></a><span data-ttu-id="a0784-104">\_Message SETPUNCTUATION em</span><span class="sxs-lookup"><span data-stu-id="a0784-104">EM\_SETPUNCTUATION message</span></span>

<span data-ttu-id="a0784-105">Définit les caractères de ponctuation pour un contrôle RichEdit.</span><span class="sxs-lookup"><span data-stu-id="a0784-105">Sets the punctuation characters for a rich edit control.</span></span>

> [!Note]  
> <span data-ttu-id="a0784-106">Ce message est pris en charge uniquement dans les versions asiatiques de Microsoft Rich Edit 1,0.</span><span class="sxs-lookup"><span data-stu-id="a0784-106">This message is supported only in Asian-language versions of Microsoft Rich Edit 1.0.</span></span> <span data-ttu-id="a0784-107">Elle n’est pas prise en charge dans les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="a0784-107">It is not supported in any later versions.</span></span>

 

## <a name="parameters"></a><span data-ttu-id="a0784-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a0784-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a0784-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="a0784-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a0784-110">Spécifie le type de ponctuation, qui peut être l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="a0784-110">Specifies the punctuation type, which can be one of the following values.</span></span>



| <span data-ttu-id="a0784-111">Valeur</span><span class="sxs-lookup"><span data-stu-id="a0784-111">Value</span></span>                                                                                                                                                      | <span data-ttu-id="a0784-112">Signification</span><span class="sxs-lookup"><span data-stu-id="a0784-112">Meaning</span></span>                                      |
|------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <span id="PC_LEADING"></span><span id="pc_leading"></span><dl> <span data-ttu-id="a0784-113"><dt>**PC \_ leader**</dt></span><span class="sxs-lookup"><span data-stu-id="a0784-113"><dt>**PC\_LEADING**</dt></span></span> </dl>       | <span data-ttu-id="a0784-114">Caractères de ponctuation de début.</span><span class="sxs-lookup"><span data-stu-id="a0784-114">Leading punctuation characters.</span></span><br/>   |
| <span id="PC_FOLLOWING"></span><span id="pc_following"></span><dl> <span data-ttu-id="a0784-115"><dt>**PC \_ suivant**</dt></span><span class="sxs-lookup"><span data-stu-id="a0784-115"><dt>**PC\_FOLLOWING**</dt></span></span> </dl> | <span data-ttu-id="a0784-116">Caractères de ponctuation suivants.</span><span class="sxs-lookup"><span data-stu-id="a0784-116">Following punctuation characters.</span></span><br/> |
| <span id="PC_DELIMITER"></span><span id="pc_delimiter"></span><dl> <span data-ttu-id="a0784-117"><dt>**délimiteur de PC \_**</dt></span><span class="sxs-lookup"><span data-stu-id="a0784-117"><dt>**PC\_DELIMITER**</dt></span></span> </dl> | <span data-ttu-id="a0784-118">Limite.</span><span class="sxs-lookup"><span data-stu-id="a0784-118">Delimiter.</span></span><br/>                        |
| <span id="PC_OVERFLOW_"></span><span id="pc_overflow_"></span><dl> <span data-ttu-id="a0784-119"><dt>**Ordinateur \_ Dépassement de capacité**</dt></span><span class="sxs-lookup"><span data-stu-id="a0784-119"><dt>**PC\_OVERFLOW** </dt></span></span> </dl> | <span data-ttu-id="a0784-120">Non pris en charge.</span><span class="sxs-lookup"><span data-stu-id="a0784-120">Not supported.</span></span><br/>                    |



 

</dd> <dt>

<span data-ttu-id="a0784-121">*lParam*</span><span class="sxs-lookup"><span data-stu-id="a0784-121">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a0784-122">Pointeur vers une structure de [**ponctuation**](/windows/desktop/api/Richedit/ns-richedit-punctuation) qui contient les caractères de ponctuation.</span><span class="sxs-lookup"><span data-stu-id="a0784-122">Pointer to a [**PUNCTUATION**](/windows/desktop/api/Richedit/ns-richedit-punctuation) structure that contains the punctuation characters.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a0784-123">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="a0784-123">Return value</span></span>

<span data-ttu-id="a0784-124">Si l’opération a échoué, la valeur de retour est une valeur différente de zéro.</span><span class="sxs-lookup"><span data-stu-id="a0784-124">If the operation succeeds, the return value is a nonzero value.</span></span>

<span data-ttu-id="a0784-125">Si l’opération échoue, la valeur de retour est zéro.</span><span class="sxs-lookup"><span data-stu-id="a0784-125">If the operation fails, the return value is zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="a0784-126">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a0784-126">Requirements</span></span>



| <span data-ttu-id="a0784-127">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a0784-127">Requirement</span></span> | <span data-ttu-id="a0784-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="a0784-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a0784-129">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a0784-129">Minimum supported client</span></span><br/> | <span data-ttu-id="a0784-130">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a0784-130">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="a0784-131">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a0784-131">Minimum supported server</span></span><br/> | <span data-ttu-id="a0784-132">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a0784-132">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="a0784-133">En-tête</span><span class="sxs-lookup"><span data-stu-id="a0784-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="a0784-134"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="a0784-134"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a0784-135">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a0784-135">See also</span></span>

<dl> <dt>

<span data-ttu-id="a0784-136">**Référence**</span><span class="sxs-lookup"><span data-stu-id="a0784-136">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="a0784-137">**\_GETPUNCTUATION em**</span><span class="sxs-lookup"><span data-stu-id="a0784-137">**EM\_GETPUNCTUATION**</span></span>](em-getpunctuation.md)
</dt> <dt>

[<span data-ttu-id="a0784-138">**PONCTUATION**</span><span class="sxs-lookup"><span data-stu-id="a0784-138">**PUNCTUATION**</span></span>](/windows/desktop/api/Richedit/ns-richedit-punctuation)
</dt> </dl>

 

 





