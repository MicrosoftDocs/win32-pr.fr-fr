---
title: Message FINDMSGSTRING (COMMDLG. h)
description: Une boîte de dialogue Rechercher ou remplacer envoie le message FINDMSGSTRING Registered à la procédure de fenêtre de sa fenêtre propriétaire quand l’utilisateur clique sur le bouton Rechercher suivant, remplacer ou remplacer tout ou ferme la boîte de dialogue.
ms.assetid: ed0b256a-96df-4588-b8f3-f7d1f89ffe74
keywords:
- Boîtes de dialogue de message FINDMSGSTRING
topic_type:
- apiref
api_name:
- FINDMSGSTRING
- FINDMSGSTRINGA
- FINDMSGSTRINGW
api_location:
- Commdlg.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fe0d3a73d8734d79d5ed0862f66bf9ba5c030e46
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104509306"
---
# <a name="findmsgstring-message"></a><span data-ttu-id="996a5-104">Message FINDMSGSTRING</span><span class="sxs-lookup"><span data-stu-id="996a5-104">FINDMSGSTRING message</span></span>

<span data-ttu-id="996a5-105">Une boîte de dialogue **Rechercher** ou **remplacer** envoie le message **FINDMSGSTRING** Registered à la procédure de fenêtre de sa fenêtre propriétaire quand l’utilisateur clique sur le bouton **Rechercher suivant**, **remplacer** ou **remplacer tout** ou ferme la boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="996a5-105">A **Find** or **Replace** dialog box sends the **FINDMSGSTRING** registered message to the window procedure of its owner window when the user clicks the **Find Next**, **Replace**, or **Replace All** button, or closes the dialog box.</span></span>


```C++
#define FINDMSGSTRING TEXT("commdlg_FindReplace")
```



## <a name="parameters"></a><span data-ttu-id="996a5-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="996a5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="996a5-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="996a5-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="996a5-108">Ce paramètre n'est pas utilisé.</span><span class="sxs-lookup"><span data-stu-id="996a5-108">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="996a5-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="996a5-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="996a5-110">Pointeur vers une structure [**FINDREPLACE**](/windows/win32/api/commdlg/ns-commdlg-findreplacea) .</span><span class="sxs-lookup"><span data-stu-id="996a5-110">A pointer to a [**FINDREPLACE**](/windows/win32/api/commdlg/ns-commdlg-findreplacea) structure.</span></span> <span data-ttu-id="996a5-111">Les membres de cette structure contiennent la dernière entrée utilisateur, y compris la chaîne à rechercher, la chaîne de remplacement (le cas échéant) et les options de recherche et de remplacement.</span><span class="sxs-lookup"><span data-stu-id="996a5-111">The members of this structure contain the latest user input, including the string to search for, the replacement string (if any) and the search-and-replacement options.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="996a5-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="996a5-112">Return value</span></span>

<span data-ttu-id="996a5-113">Ce message n’a pas de valeur de retour.</span><span class="sxs-lookup"><span data-stu-id="996a5-113">This message has no return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="996a5-114">Notes</span><span class="sxs-lookup"><span data-stu-id="996a5-114">Remarks</span></span>

<span data-ttu-id="996a5-115">Vous devez spécifier la constante **FINDMSGSTRING** dans un appel à la fonction [**RegisterWindowMessage**](/windows/desktop/api/winuser/nf-winuser-registerwindowmessagea) pour obtenir l’identificateur du message envoyé par la boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="996a5-115">You must specify the **FINDMSGSTRING** constant in a call to the [**RegisterWindowMessage**](/windows/desktop/api/winuser/nf-winuser-registerwindowmessagea) function to get the identifier for the message sent by the dialog box.</span></span>

<span data-ttu-id="996a5-116">Lorsque vous créez la boîte de dialogue, utilisez le membre **hwndOwner** de la structure [**FINDREPLACE**](/windows/win32/api/commdlg/ns-commdlg-findreplacea) pour identifier la fenêtre de réception des messages **FINDMSGSTRING** .</span><span class="sxs-lookup"><span data-stu-id="996a5-116">When you create the dialog box, use the **hwndOwner** member of the [**FINDREPLACE**](/windows/win32/api/commdlg/ns-commdlg-findreplacea) structure to identify the window to receive **FINDMSGSTRING** messages.</span></span>

<span data-ttu-id="996a5-117">Le membre **Flags** de la structure [**FINDREPLACE**](/windows/win32/api/commdlg/ns-commdlg-findreplacea) comprend l’un des indicateurs suivants pour indiquer l’événement à l’origine du message.</span><span class="sxs-lookup"><span data-stu-id="996a5-117">The **Flags** member of the [**FINDREPLACE**](/windows/win32/api/commdlg/ns-commdlg-findreplacea) structure includes one of the following flags to indicate the event that caused the message.</span></span>



| <span data-ttu-id="996a5-118">Indicateur</span><span class="sxs-lookup"><span data-stu-id="996a5-118">Flag</span></span>                            | <span data-ttu-id="996a5-119">Signification</span><span class="sxs-lookup"><span data-stu-id="996a5-119">Meaning</span></span>                                                                                                                                                                                                     |
|---------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="996a5-120">**Fr \_ DIALOGTERM** (0x00000040)</span><span class="sxs-lookup"><span data-stu-id="996a5-120">**FR\_DIALOGTERM** (0x00000040)</span></span> | <span data-ttu-id="996a5-121">La boîte de dialogue se ferme.</span><span class="sxs-lookup"><span data-stu-id="996a5-121">The dialog box is closing.</span></span> <span data-ttu-id="996a5-122">Une fois que la fenêtre propriétaire a traité ce message, un descripteur de la boîte de dialogue n’est plus valide.</span><span class="sxs-lookup"><span data-stu-id="996a5-122">After the owner window processes this message, a handle to the dialog box is no longer valid.</span></span>                                                                                    |
| <span data-ttu-id="996a5-123">**Fr \_ FINDNEXT** (0x00000008)</span><span class="sxs-lookup"><span data-stu-id="996a5-123">**FR\_FINDNEXT** (0x00000008)</span></span>   | <span data-ttu-id="996a5-124">L’utilisateur a cliqué sur le bouton **suivant** de la boîte de dialogue **Rechercher** ou **remplacer** .</span><span class="sxs-lookup"><span data-stu-id="996a5-124">The user clicked the **Find Next** button in a **Find** or **Replace** dialog box.</span></span> <span data-ttu-id="996a5-125">Le membre **lpstrFindWhat** spécifie la chaîne à rechercher.</span><span class="sxs-lookup"><span data-stu-id="996a5-125">The **lpstrFindWhat** member specifies the string to search for.</span></span>                                                         |
| <span data-ttu-id="996a5-126">**Fr \_ REMPLACER** (0x00000010)</span><span class="sxs-lookup"><span data-stu-id="996a5-126">**FR\_REPLACE** (0x00000010)</span></span>    | <span data-ttu-id="996a5-127">L’utilisateur a cliqué sur le bouton **remplacer** dans une boîte de dialogue **remplacer** .</span><span class="sxs-lookup"><span data-stu-id="996a5-127">The user clicked the **Replace** button in a **Replace** dialog box.</span></span> <span data-ttu-id="996a5-128">Le membre **lpstrFindWhat** spécifie la chaîne à remplacer et le membre **lpstrReplaceWith** spécifie la chaîne de remplacement.</span><span class="sxs-lookup"><span data-stu-id="996a5-128">The **lpstrFindWhat** member specifies the string to replace and the **lpstrReplaceWith** member specifies the replacement string.</span></span>     |
| <span data-ttu-id="996a5-129">**Fr \_ REPLACEALL** (0x00000020)</span><span class="sxs-lookup"><span data-stu-id="996a5-129">**FR\_REPLACEALL** (0x00000020)</span></span> | <span data-ttu-id="996a5-130">L’utilisateur a cliqué sur le bouton **remplacer tout** dans une boîte de dialogue **remplacer** .</span><span class="sxs-lookup"><span data-stu-id="996a5-130">The user clicked the **Replace All** button in a **Replace** dialog box.</span></span> <span data-ttu-id="996a5-131">Le membre **lpstrFindWhat** spécifie la chaîne à remplacer et le membre **lpstrReplaceWith** spécifie la chaîne de remplacement.</span><span class="sxs-lookup"><span data-stu-id="996a5-131">The **lpstrFindWhat** member specifies the string to replace and the **lpstrReplaceWith** member specifies the replacement string.</span></span> |



 

<span data-ttu-id="996a5-132">Pour un message **suivant** ou **remplacer tout** , le membre **indicateurs** peut inclure un ou plusieurs des indicateurs suivants pour indiquer les options de recherche.</span><span class="sxs-lookup"><span data-stu-id="996a5-132">For a **Find Next** or **Replace All** message, the **Flags** member can include one or more of the following flags to indicate the search options.</span></span>



| <span data-ttu-id="996a5-133">Indicateur</span><span class="sxs-lookup"><span data-stu-id="996a5-133">Flag</span></span>                           | <span data-ttu-id="996a5-134">Signification</span><span class="sxs-lookup"><span data-stu-id="996a5-134">Meaning</span></span>                                                                                                                                                                                                                                                                                         |
|--------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="996a5-135">**Fr \_ En baisse** (0x00000001)</span><span class="sxs-lookup"><span data-stu-id="996a5-135">**FR\_DOWN** (0x00000001)</span></span>      | <span data-ttu-id="996a5-136">Si cette option est définie, le bouton **bas** des cases d’option de la direction est sélectionné, ce qui indique que l’utilisateur souhaite effectuer une recherche à partir de l’emplacement actuel jusqu’à la fin du document.</span><span class="sxs-lookup"><span data-stu-id="996a5-136">If set, the **Down** button of the direction radio buttons is selected indicating that user wants to search from the current location to the end of the document.</span></span> <span data-ttu-id="996a5-137">Si **fr \_** n’est pas défini, le bouton haut est sélectionné afin que l’utilisateur souhaite effectuer **une** recherche jusqu’au début du document.</span><span class="sxs-lookup"><span data-stu-id="996a5-137">If **FR\_DOWN** is not set, the **Up** button is selected so the user wants to search to the beginning of the document.</span></span>       |
| <span data-ttu-id="996a5-138">**Fr \_ MATCHCASE** (0x00000004)</span><span class="sxs-lookup"><span data-stu-id="996a5-138">**FR\_MATCHCASE** (0x00000004)</span></span> | <span data-ttu-id="996a5-139">Si cette option est définie, la case à cocher **respecter la casse** est activée, ce qui indique que l’utilisateur veut que la recherche respecte la casse.</span><span class="sxs-lookup"><span data-stu-id="996a5-139">If set, the **Match Case** check box is selected indicating that the user wants the search to be case-sensitive.</span></span> <span data-ttu-id="996a5-140">Si **fr \_ RespecterCasse** n’est pas défini, la case à cocher est désactivée afin que la recherche ne respecte pas la casse.</span><span class="sxs-lookup"><span data-stu-id="996a5-140">If **FR\_MATCHCASE** is not set, the check box is unselected so the search should be case-insensitive.</span></span>                                                                         |
| <span data-ttu-id="996a5-141">**Fr \_ WHOLEWORD** (0x00000002)</span><span class="sxs-lookup"><span data-stu-id="996a5-141">**FR\_WHOLEWORD** (0x00000002)</span></span> | <span data-ttu-id="996a5-142">Si cette option est définie, la case à cocher **mot entier uniquement** est activée, ce qui indique que l’utilisateur souhaite rechercher uniquement les mots entiers qui correspondent à la chaîne recherchée.</span><span class="sxs-lookup"><span data-stu-id="996a5-142">If set, the **Match Whole Word Only** check box is selected indicating that the user wants to search only for whole words that match the search string.</span></span> <span data-ttu-id="996a5-143">Si **fr \_ WHOLEWORD** n’est pas défini, la case à cocher est désactivée. par conséquent, vous devez également rechercher les fragments de mots qui correspondent à la chaîne recherchée.</span><span class="sxs-lookup"><span data-stu-id="996a5-143">If **FR\_WHOLEWORD** is not set, the check box is unselected so you should also search for word fragments that match the search string.</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="996a5-144">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="996a5-144">Requirements</span></span>



| <span data-ttu-id="996a5-145">Condition requise</span><span class="sxs-lookup"><span data-stu-id="996a5-145">Requirement</span></span> | <span data-ttu-id="996a5-146">Valeur</span><span class="sxs-lookup"><span data-stu-id="996a5-146">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="996a5-147">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="996a5-147">Minimum supported client</span></span><br/> | <span data-ttu-id="996a5-148">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="996a5-148">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="996a5-149">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="996a5-149">Minimum supported server</span></span><br/> | <span data-ttu-id="996a5-150">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="996a5-150">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="996a5-151">En-tête</span><span class="sxs-lookup"><span data-stu-id="996a5-151">Header</span></span><br/>                   | <dl> <span data-ttu-id="996a5-152"><dt>Commdlg. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="996a5-152"><dt>Commdlg.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="996a5-153">Noms Unicode et ANSI</span><span class="sxs-lookup"><span data-stu-id="996a5-153">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="996a5-154">**FINDMSGSTRINGW** (Unicode) et **FINDMSGSTRINGA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="996a5-154">**FINDMSGSTRINGW** (Unicode) and **FINDMSGSTRINGA** (ANSI)</span></span><br/>                                    |



## <a name="see-also"></a><span data-ttu-id="996a5-155">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="996a5-155">See also</span></span>

<dl> <dt>

<span data-ttu-id="996a5-156">**Référence**</span><span class="sxs-lookup"><span data-stu-id="996a5-156">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="996a5-157">**FINDREPLACE**</span><span class="sxs-lookup"><span data-stu-id="996a5-157">**FINDREPLACE**</span></span>](/windows/win32/api/commdlg/ns-commdlg-findreplacea)
</dt> <dt>

[<span data-ttu-id="996a5-158">**RegisterWindowMessage**</span><span class="sxs-lookup"><span data-stu-id="996a5-158">**RegisterWindowMessage**</span></span>](/windows/desktop/api/winuser/nf-winuser-registerwindowmessagea)
</dt> <dt>

<span data-ttu-id="996a5-159">**Méthodologique**</span><span class="sxs-lookup"><span data-stu-id="996a5-159">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="996a5-160">Bibliothèque de boîtes de dialogue communes</span><span class="sxs-lookup"><span data-stu-id="996a5-160">Common Dialog Box Library</span></span>](common-dialog-box-library.md)
</dt> </dl>

 

