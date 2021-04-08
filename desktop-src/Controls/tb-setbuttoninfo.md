---
title: Message TB_SETBUTTONINFO (commctrl. h)
description: Définit les informations d’un bouton existant dans une barre d’outils.
ms.assetid: ac9b88b9-d0d0-4669-a342-708924d97c8b
keywords:
- TB_SETBUTTONINFO les contrôles de message Windows
topic_type:
- apiref
api_name:
- TB_SETBUTTONINFO
- TB_SETBUTTONINFOA
- TB_SETBUTTONINFOW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 70612a90f245a25dde5a487917d7c3b669424ea8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103844262"
---
# <a name="tb_setbuttoninfo-message"></a><span data-ttu-id="5c75a-104">TO \_ SETBUTTONINFO message</span><span class="sxs-lookup"><span data-stu-id="5c75a-104">TB\_SETBUTTONINFO message</span></span>

<span data-ttu-id="5c75a-105">Définit les informations d’un bouton existant dans une barre d’outils.</span><span class="sxs-lookup"><span data-stu-id="5c75a-105">Sets the information for an existing button in a toolbar.</span></span>

## <a name="parameters"></a><span data-ttu-id="5c75a-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="5c75a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5c75a-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="5c75a-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="5c75a-108">Identificateur du bouton.</span><span class="sxs-lookup"><span data-stu-id="5c75a-108">Button identifier.</span></span>

</dd> <dt>

<span data-ttu-id="5c75a-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="5c75a-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="5c75a-110">Pointeur vers une structure [**TBBUTTONINFO**](/windows/desktop/api/Commctrl/ns-commctrl-tbbuttoninfoa) qui contient les informations sur le nouveau bouton.</span><span class="sxs-lookup"><span data-stu-id="5c75a-110">Pointer to a [**TBBUTTONINFO**](/windows/desktop/api/Commctrl/ns-commctrl-tbbuttoninfoa) structure that contains the new button information.</span></span> <span data-ttu-id="5c75a-111">Les membres **cbSize** et **dwMask** de cette structure doivent être renseignés avant l’envoi de ce message.</span><span class="sxs-lookup"><span data-stu-id="5c75a-111">The **cbSize** and **dwMask** members of this structure must be filled in prior to sending this message.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5c75a-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="5c75a-112">Return value</span></span>

<span data-ttu-id="5c75a-113">Retourne une valeur différente de zéro en cas de réussite, ou zéro dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="5c75a-113">Returns nonzero if successful, or zero otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="5c75a-114">Notes</span><span class="sxs-lookup"><span data-stu-id="5c75a-114">Remarks</span></span>

<span data-ttu-id="5c75a-115">Le texte est généralement affecté à des boutons lorsqu’ils sont ajoutés à une barre d’outils en spécifiant l’index d’une chaîne dans le pool de chaînes de la barre d’outils.</span><span class="sxs-lookup"><span data-stu-id="5c75a-115">Text is commonly assigned to buttons when they are added to a toolbar by specifying the index of a string in the toolbar's string pool.</span></span> <span data-ttu-id="5c75a-116">Si vous utilisez un **\_ SETBUTTONINFO to** pour assigner un nouveau texte à un bouton, il remplace définitivement le texte du pool de chaînes.</span><span class="sxs-lookup"><span data-stu-id="5c75a-116">If you use a **TB\_SETBUTTONINFO** to assign new text to a button, it will permanently override the text from the string pool.</span></span> <span data-ttu-id="5c75a-117">Vous pouvez modifier le texte en appelant à nouveau **to \_ SETBUTTONINFO** , mais vous ne pouvez pas réassigner la chaîne à partir du pool de chaînes.</span><span class="sxs-lookup"><span data-stu-id="5c75a-117">You can change the text by calling **TB\_SETBUTTONINFO** again, but you cannot reassign the string from the string pool.</span></span>

## <a name="requirements"></a><span data-ttu-id="5c75a-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5c75a-118">Requirements</span></span>



| <span data-ttu-id="5c75a-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="5c75a-119">Requirement</span></span> | <span data-ttu-id="5c75a-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="5c75a-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="5c75a-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5c75a-121">Minimum supported client</span></span><br/> | <span data-ttu-id="5c75a-122">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="5c75a-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="5c75a-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5c75a-123">Minimum supported server</span></span><br/> | <span data-ttu-id="5c75a-124">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="5c75a-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="5c75a-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="5c75a-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="5c75a-126"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="5c75a-126"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="5c75a-127">Noms Unicode et ANSI</span><span class="sxs-lookup"><span data-stu-id="5c75a-127">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="5c75a-128">**To \_ SETBUTTONINFOW** (Unicode) et **to \_ SETBUTTONINFOA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="5c75a-128">**TB\_SETBUTTONINFOW** (Unicode) and **TB\_SETBUTTONINFOA** (ANSI)</span></span><br/>         |



## <a name="see-also"></a><span data-ttu-id="5c75a-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5c75a-129">See also</span></span>

<dl> <dt>

<span data-ttu-id="5c75a-130">**Référence**</span><span class="sxs-lookup"><span data-stu-id="5c75a-130">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="5c75a-131">**TO \_ ADDBUTTONS**</span><span class="sxs-lookup"><span data-stu-id="5c75a-131">**TB\_ADDBUTTONS**</span></span>](tb-addbuttons.md)
</dt> <dt>

[<span data-ttu-id="5c75a-132">**TO \_ GETBUTTONINFO**</span><span class="sxs-lookup"><span data-stu-id="5c75a-132">**TB\_GETBUTTONINFO**</span></span>](tb-getbuttoninfo.md)
</dt> <dt>

[<span data-ttu-id="5c75a-133">**TO \_ GETBUTTONTEXT**</span><span class="sxs-lookup"><span data-stu-id="5c75a-133">**TB\_GETBUTTONTEXT**</span></span>](tb-getbuttontext.md)
</dt> <dt>

[<span data-ttu-id="5c75a-134">**TO \_ GETSTRING**</span><span class="sxs-lookup"><span data-stu-id="5c75a-134">**TB\_GETSTRING**</span></span>](tb-getstring.md)
</dt> <dt>

[<span data-ttu-id="5c75a-135">**TO \_ INSERTBUTTON**</span><span class="sxs-lookup"><span data-stu-id="5c75a-135">**TB\_INSERTBUTTON**</span></span>](tb-insertbutton.md)
</dt> </dl>

 

 





