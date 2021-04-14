---
description: Envoyé à une application lorsque l’IME obtient un caractère du résultat de la conversion. Une fenêtre reçoit ce message par le biais de sa fonction WindowProc.
ms.assetid: 1e1353c3-5215-4829-a00a-2fee47a430eb
title: Message WM_IME_CHAR (winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: be0e2df06d9d837b0c1fbc0f9c9d9eb852252c47
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104393776"
---
# <a name="wm_ime_char-message"></a><span data-ttu-id="49b7c-104">\_Message de \_ type de message IME WM</span><span class="sxs-lookup"><span data-stu-id="49b7c-104">WM\_IME\_CHAR message</span></span>

<span data-ttu-id="49b7c-105">Envoyé à une application lorsque l’IME obtient un caractère du résultat de la conversion.</span><span class="sxs-lookup"><span data-stu-id="49b7c-105">Sent to an application when the IME gets a character of the conversion result.</span></span> <span data-ttu-id="49b7c-106">Une fenêtre reçoit ce message par le biais de sa fonction [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="49b7c-106">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
LRESULT CALLBACK WindowProc(
 HWND  hwnd,
 WM_IME_CHAR,
 WPARAM wParam,
 LPARAM lParam   
);
```



## <a name="parameters"></a><span data-ttu-id="49b7c-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="49b7c-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="49b7c-108">*HWND*</span><span class="sxs-lookup"><span data-stu-id="49b7c-108">*hwnd*</span></span> 
</dt> <dd>

<span data-ttu-id="49b7c-109">Handle de fenêtre.</span><span class="sxs-lookup"><span data-stu-id="49b7c-109">A handle to window.</span></span>

</dd> <dt>

<span data-ttu-id="49b7c-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="49b7c-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="49b7c-111">**DBCS :** Valeur de caractère codé sur un octet ou sur deux octets.</span><span class="sxs-lookup"><span data-stu-id="49b7c-111">**DBCS:** A single-byte or double-byte character value.</span></span> <span data-ttu-id="49b7c-112">Pour un caractère codé sur deux octets, (BYTE) (wParam >> 8) contient l’octet de tête.</span><span class="sxs-lookup"><span data-stu-id="49b7c-112">For a double-byte character, (BYTE)(wParam >> 8) contains the lead byte.</span></span> <span data-ttu-id="49b7c-113">Notez que les parenthèses sont nécessaires, car l’opérateur de cast a une priorité plus élevée que l’opérateur de décalage.</span><span class="sxs-lookup"><span data-stu-id="49b7c-113">Note that the parentheses are necessary because the cast operator has higher precedence than the shift operator.</span></span>

<span data-ttu-id="49b7c-114">**Unicode :** Valeur de caractère Unicode.</span><span class="sxs-lookup"><span data-stu-id="49b7c-114">**Unicode:** A Unicode character value.</span></span>

</dd> <dt>

<span data-ttu-id="49b7c-115">*lParam*</span><span class="sxs-lookup"><span data-stu-id="49b7c-115">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="49b7c-116">L’indicateur de répétition, le code d’analyse, l’indicateur de clé étendue, le code de contexte, l’indicateur d’état de la clé précédente et l’indicateur d’état de transition, avec les valeurs définies ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="49b7c-116">The repeat count, scan code, extended key flag, context code, previous key state flag, and transition state flag, with values as defined below.</span></span>



| <span data-ttu-id="49b7c-117">bit</span><span class="sxs-lookup"><span data-stu-id="49b7c-117">Bit</span></span>   | <span data-ttu-id="49b7c-118">Signification</span><span class="sxs-lookup"><span data-stu-id="49b7c-118">Meaning</span></span>                                                                              |
|-------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="49b7c-119">0-15</span><span class="sxs-lookup"><span data-stu-id="49b7c-119">0-15</span></span>  | <span data-ttu-id="49b7c-120">Nombre de répétitions.</span><span class="sxs-lookup"><span data-stu-id="49b7c-120">Repeat count.</span></span> <span data-ttu-id="49b7c-121">Étant donné que les premier et deuxième octets sont continus, il s’agit toujours de 1.</span><span class="sxs-lookup"><span data-stu-id="49b7c-121">Since the first byte and second byte are continuous, this is always 1.</span></span> |
| <span data-ttu-id="49b7c-122">16-23</span><span class="sxs-lookup"><span data-stu-id="49b7c-122">16-23</span></span> | <span data-ttu-id="49b7c-123">Recherchez dans le code un caractère asiatique complet.</span><span class="sxs-lookup"><span data-stu-id="49b7c-123">Scan code for a complete Asian character.</span></span>                                            |
| <span data-ttu-id="49b7c-124">24</span><span class="sxs-lookup"><span data-stu-id="49b7c-124">24</span></span>    | <span data-ttu-id="49b7c-125">Clé étendue.</span><span class="sxs-lookup"><span data-stu-id="49b7c-125">Extended key.</span></span>                                                                        |
| <span data-ttu-id="49b7c-126">25-28</span><span class="sxs-lookup"><span data-stu-id="49b7c-126">25-28</span></span> | <span data-ttu-id="49b7c-127">Non utilisé.</span><span class="sxs-lookup"><span data-stu-id="49b7c-127">Not used.</span></span>                                                                            |
| <span data-ttu-id="49b7c-128">29</span><span class="sxs-lookup"><span data-stu-id="49b7c-128">29</span></span>    | <span data-ttu-id="49b7c-129">Code de contexte.</span><span class="sxs-lookup"><span data-stu-id="49b7c-129">Context code.</span></span>                                                                        |
| <span data-ttu-id="49b7c-130">30</span><span class="sxs-lookup"><span data-stu-id="49b7c-130">30</span></span>    | <span data-ttu-id="49b7c-131">État de la clé précédente.</span><span class="sxs-lookup"><span data-stu-id="49b7c-131">Previous key state.</span></span>                                                                  |
| <span data-ttu-id="49b7c-132">31</span><span class="sxs-lookup"><span data-stu-id="49b7c-132">31</span></span>    | <span data-ttu-id="49b7c-133">État de transition.</span><span class="sxs-lookup"><span data-stu-id="49b7c-133">Transition state.</span></span>                                                                    |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="49b7c-134">Notes</span><span class="sxs-lookup"><span data-stu-id="49b7c-134">Remarks</span></span>

<span data-ttu-id="49b7c-135">Contrairement au message [**WM \_ char**](../inputdev/wm-char.md) pour une fenêtre non Unicode, ce message peut inclure des valeurs de caractères codés sur deux octets et sur un octet.</span><span class="sxs-lookup"><span data-stu-id="49b7c-135">Unlike the [**WM\_CHAR**](../inputdev/wm-char.md) message for a non-Unicode window, this message can include double-byte and single-byte character values.</span></span> <span data-ttu-id="49b7c-136">Pour une fenêtre Unicode, ce message est le même que le \_ type WM.</span><span class="sxs-lookup"><span data-stu-id="49b7c-136">For a Unicode window, this message is the same as WM\_CHAR.</span></span>

<span data-ttu-id="49b7c-137">Pour une fenêtre non Unicode, si le message de \_ type IME WM \_ contient un caractère codé sur deux octets et que l’application transmet ce message à [**DEFWINDOWPROC**](/windows/desktop/api/winuser/nf-winuser-defwindowproca), l’IME convertit ce message en deux \_ messages WM char, chacun contenant un octet du caractère codé sur deux octets.</span><span class="sxs-lookup"><span data-stu-id="49b7c-137">For a non-Unicode window, if the WM\_IME\_CHAR message includes a double-byte character and the application passes this message to [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca), the IME converts this message into two WM\_CHAR messages, each containing one byte of the double-byte character.</span></span>

## <a name="requirements"></a><span data-ttu-id="49b7c-138">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="49b7c-138">Requirements</span></span>



| <span data-ttu-id="49b7c-139">Condition requise</span><span class="sxs-lookup"><span data-stu-id="49b7c-139">Requirement</span></span> | <span data-ttu-id="49b7c-140">Valeur</span><span class="sxs-lookup"><span data-stu-id="49b7c-140">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="49b7c-141">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="49b7c-141">Minimum supported client</span></span><br/> | <span data-ttu-id="49b7c-142">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="49b7c-142">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="49b7c-143">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="49b7c-143">Minimum supported server</span></span><br/> | <span data-ttu-id="49b7c-144">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="49b7c-144">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="49b7c-145">En-tête</span><span class="sxs-lookup"><span data-stu-id="49b7c-145">Header</span></span><br/>                   | <dl> <span data-ttu-id="49b7c-146"><dt>Winuser. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="49b7c-146"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="49b7c-147">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="49b7c-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="49b7c-148">Gestionnaire de méthode d’entrée</span><span class="sxs-lookup"><span data-stu-id="49b7c-148">Input Method Manager</span></span>](input-method-manager.md)
</dt> <dt>

[<span data-ttu-id="49b7c-149">Messages du gestionnaire de méthode d’entrée</span><span class="sxs-lookup"><span data-stu-id="49b7c-149">Input Method Manager Messages</span></span>](input-method-manager-messages.md)
</dt> </dl>

 

 
