---
title: Message TB_GETSTRING (commctrl. h)
description: Récupère une chaîne à partir du pool de chaînes d’une barre d’outils.
ms.assetid: a5f80c16-bc6d-466d-8ec6-77451432148e
keywords:
- TB_GETSTRING les contrôles de message Windows
topic_type:
- apiref
api_name:
- TB_GETSTRING
- TB_GETSTRINGA
- TB_GETSTRINGW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 465ad2546397fa31c33d6a52b4989902c979d91d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104032617"
---
# <a name="tb_getstring-message"></a><span data-ttu-id="673b2-104">TO \_ GETSTRING (message)</span><span class="sxs-lookup"><span data-stu-id="673b2-104">TB\_GETSTRING message</span></span>

<span data-ttu-id="673b2-105">Récupère une chaîne à partir du pool de chaînes d’une barre d’outils.</span><span class="sxs-lookup"><span data-stu-id="673b2-105">Retrieves a string from a toolbar's string pool.</span></span>

## <a name="parameters"></a><span data-ttu-id="673b2-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="673b2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="673b2-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="673b2-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="673b2-108">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) spécifie la longueur de la mémoire tampon *lParam* , en octets.</span><span class="sxs-lookup"><span data-stu-id="673b2-108">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) specifies the length of the *lParam* buffer, in bytes.</span></span> <span data-ttu-id="673b2-109">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) spécifie l’index de la chaîne.</span><span class="sxs-lookup"><span data-stu-id="673b2-109">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifies the index of the string.</span></span>

</dd> <dt>

<span data-ttu-id="673b2-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="673b2-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="673b2-111">Pointeur vers une mémoire tampon utilisée pour retourner la chaîne.</span><span class="sxs-lookup"><span data-stu-id="673b2-111">Pointer to a buffer used to return the string.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="673b2-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="673b2-112">Return value</span></span>

<span data-ttu-id="673b2-113">Retourne la longueur de chaîne en cas de réussite, ou-1 dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="673b2-113">Returns the string length if successful, or -1 otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="673b2-114">Notes</span><span class="sxs-lookup"><span data-stu-id="673b2-114">Remarks</span></span>

<span data-ttu-id="673b2-115">Ce message retourne la chaîne spécifiée à partir du pool de chaînes de la barre d’outils.</span><span class="sxs-lookup"><span data-stu-id="673b2-115">This message returns the specified string from the toolbar's string pool.</span></span> <span data-ttu-id="673b2-116">Elle ne correspond pas nécessairement à la chaîne de texte actuellement affichée par un bouton.</span><span class="sxs-lookup"><span data-stu-id="673b2-116">It does not necessarily correspond to the text string currently being displayed by a button.</span></span> <span data-ttu-id="673b2-117">Pour récupérer la chaîne de texte actuelle d’un bouton, envoyez la barre d’outils à un message [**\_ GETBUTTONTEXT to**](tb-getbuttontext.md) .</span><span class="sxs-lookup"><span data-stu-id="673b2-117">To retrieve a button's current text string, send the toolbar a [**TB\_GETBUTTONTEXT**](tb-getbuttontext.md) message.</span></span>

## <a name="requirements"></a><span data-ttu-id="673b2-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="673b2-118">Requirements</span></span>



| <span data-ttu-id="673b2-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="673b2-119">Requirement</span></span> | <span data-ttu-id="673b2-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="673b2-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="673b2-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="673b2-121">Minimum supported client</span></span><br/> | <span data-ttu-id="673b2-122">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="673b2-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="673b2-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="673b2-123">Minimum supported server</span></span><br/> | <span data-ttu-id="673b2-124">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="673b2-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="673b2-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="673b2-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="673b2-126"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="673b2-126"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="673b2-127">Noms Unicode et ANSI</span><span class="sxs-lookup"><span data-stu-id="673b2-127">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="673b2-128">**To \_ GETSTRINGW** (Unicode) et **to \_ GETSTRINGA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="673b2-128">**TB\_GETSTRINGW** (Unicode) and **TB\_GETSTRINGA** (ANSI)</span></span><br/>                 |



## <a name="see-also"></a><span data-ttu-id="673b2-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="673b2-129">See also</span></span>

<dl> <dt>

<span data-ttu-id="673b2-130">**Référence**</span><span class="sxs-lookup"><span data-stu-id="673b2-130">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="673b2-131">**TO \_ ADDSTRING**</span><span class="sxs-lookup"><span data-stu-id="673b2-131">**TB\_ADDSTRING**</span></span>](tb-addstring.md)
</dt> <dt>

[<span data-ttu-id="673b2-132">**TO \_ ADDBUTTONS**</span><span class="sxs-lookup"><span data-stu-id="673b2-132">**TB\_ADDBUTTONS**</span></span>](tb-addbuttons.md)
</dt> <dt>

[<span data-ttu-id="673b2-133">**TO \_ INSERTBUTTON**</span><span class="sxs-lookup"><span data-stu-id="673b2-133">**TB\_INSERTBUTTON**</span></span>](tb-insertbutton.md)
</dt> </dl>

 

