---
title: Message TB_GETBUTTONINFO (commctrl. h)
description: Récupère des informations étendues pour un bouton dans une barre d’outils.
ms.assetid: 87430dd2-43d1-4e33-96ac-d33f89a654b6
keywords:
- TB_GETBUTTONINFO les contrôles de message Windows
topic_type:
- apiref
api_name:
- TB_GETBUTTONINFO
- TB_GETBUTTONINFOA
- TB_GETBUTTONINFOW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 74c7f6a8d1d36737d09cfb4d307129200a51180c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104106600"
---
# <a name="tb_getbuttoninfo-message"></a><span data-ttu-id="d1032-104">TO \_ GETBUTTONINFO message</span><span class="sxs-lookup"><span data-stu-id="d1032-104">TB\_GETBUTTONINFO message</span></span>

<span data-ttu-id="d1032-105">Récupère des informations étendues pour un bouton dans une barre d’outils.</span><span class="sxs-lookup"><span data-stu-id="d1032-105">Retrieves extended information for a button in a toolbar.</span></span>

## <a name="parameters"></a><span data-ttu-id="d1032-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d1032-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d1032-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="d1032-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d1032-108">Identificateur de commande du bouton.</span><span class="sxs-lookup"><span data-stu-id="d1032-108">Command identifier of the button.</span></span>

</dd> <dt>

<span data-ttu-id="d1032-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="d1032-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d1032-110">Pointeur vers une structure [**TBBUTTONINFO**](/windows/desktop/api/Commctrl/ns-commctrl-tbbuttoninfoa) qui reçoit les informations sur le bouton.</span><span class="sxs-lookup"><span data-stu-id="d1032-110">Pointer to a [**TBBUTTONINFO**](/windows/desktop/api/Commctrl/ns-commctrl-tbbuttoninfoa) structure that receives the button information.</span></span> <span data-ttu-id="d1032-111">Les membres **cbSize** et **dwMask** de cette structure doivent être renseignés avant l’envoi de ce message.</span><span class="sxs-lookup"><span data-stu-id="d1032-111">The **cbSize** and **dwMask** members of this structure must be filled in prior to sending this message.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d1032-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="d1032-112">Return value</span></span>

<span data-ttu-id="d1032-113">Retourne l’index de base zéro du bouton, ou-1 si une erreur se produit.</span><span class="sxs-lookup"><span data-stu-id="d1032-113">Returns the zero-based index of the button, or -1 if an error occurs.</span></span>

## <a name="remarks"></a><span data-ttu-id="d1032-114">Notes</span><span class="sxs-lookup"><span data-stu-id="d1032-114">Remarks</span></span>

<span data-ttu-id="d1032-115">Quand vous utilisez [**to \_ ADDBUTTONS**](tb-addbuttons.md) ou [**to \_ INSERTBUTTON**](tb-insertbutton.md) pour placer des boutons dans la barre d’outils, le texte du bouton est généralement spécifié par son index de pool de chaînes.</span><span class="sxs-lookup"><span data-stu-id="d1032-115">When you use [**TB\_ADDBUTTONS**](tb-addbuttons.md) or [**TB\_INSERTBUTTON**](tb-insertbutton.md) to place buttons on the toolbar, the button text is commonly specified by its string pool index.</span></span> <span data-ttu-id="d1032-116">**To \_ GETBUTTONINFO** ne récupère pas cette chaîne.</span><span class="sxs-lookup"><span data-stu-id="d1032-116">**TB\_GETBUTTONINFO** will not retrieve this string.</span></span> <span data-ttu-id="d1032-117">Pour utiliser **to \_ GETBUTTONINFO** pour récupérer le texte du bouton, vous devez d’abord définir la chaîne de texte avec [**to \_ SETBUTTONINFO**](tb-setbuttoninfo.md).</span><span class="sxs-lookup"><span data-stu-id="d1032-117">To use **TB\_GETBUTTONINFO** to retrieve button text, you must first set the text string with [**TB\_SETBUTTONINFO**](tb-setbuttoninfo.md).</span></span> <span data-ttu-id="d1032-118">Une fois que vous avez défini le texte du bouton avec **to \_ SETBUTTONINFO**, vous ne pouvez plus utiliser l’index du pool de chaînes.</span><span class="sxs-lookup"><span data-stu-id="d1032-118">Once you have set the button text with **TB\_SETBUTTONINFO**, you can no longer use the string pool index.</span></span>

## <a name="requirements"></a><span data-ttu-id="d1032-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d1032-119">Requirements</span></span>



| <span data-ttu-id="d1032-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d1032-120">Requirement</span></span> | <span data-ttu-id="d1032-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="d1032-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d1032-122">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d1032-122">Minimum supported client</span></span><br/> | <span data-ttu-id="d1032-123">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d1032-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="d1032-124">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d1032-124">Minimum supported server</span></span><br/> | <span data-ttu-id="d1032-125">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d1032-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="d1032-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="d1032-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="d1032-127"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="d1032-127"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="d1032-128">Noms Unicode et ANSI</span><span class="sxs-lookup"><span data-stu-id="d1032-128">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="d1032-129">**To \_ GETBUTTONINFOW** (Unicode) et **to \_ GETBUTTONINFOA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="d1032-129">**TB\_GETBUTTONINFOW** (Unicode) and **TB\_GETBUTTONINFOA** (ANSI)</span></span><br/>         |



## <a name="see-also"></a><span data-ttu-id="d1032-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d1032-130">See also</span></span>

<dl> <dt>

<span data-ttu-id="d1032-131">**Référence**</span><span class="sxs-lookup"><span data-stu-id="d1032-131">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="d1032-132">**TO \_ SETBUTTONINFO**</span><span class="sxs-lookup"><span data-stu-id="d1032-132">**TB\_SETBUTTONINFO**</span></span>](tb-setbuttoninfo.md)
</dt> <dt>

[<span data-ttu-id="d1032-133">**TO \_ GETBUTTONTEXT**</span><span class="sxs-lookup"><span data-stu-id="d1032-133">**TB\_GETBUTTONTEXT**</span></span>](tb-getbuttontext.md)
</dt> </dl>

 

 





