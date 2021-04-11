---
title: Message TB_INSERTBUTTON (commctrl. h)
description: Insère un bouton dans une barre d’outils.
ms.assetid: 6be27817-5d86-4649-bd63-173845197763
keywords:
- TB_INSERTBUTTON les contrôles de message Windows
topic_type:
- apiref
api_name:
- TB_INSERTBUTTON
- TB_INSERTBUTTONA
- TB_INSERTBUTTONW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4e08eed328a99d4a8927a7e09084bf122f2e4e84
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103341"
---
# <a name="tb_insertbutton-message"></a><span data-ttu-id="50f98-104">TO \_ INSERTBUTTON message</span><span class="sxs-lookup"><span data-stu-id="50f98-104">TB\_INSERTBUTTON message</span></span>

<span data-ttu-id="50f98-105">Insère un bouton dans une barre d’outils.</span><span class="sxs-lookup"><span data-stu-id="50f98-105">Inserts a button in a toolbar.</span></span>

## <a name="parameters"></a><span data-ttu-id="50f98-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="50f98-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="50f98-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="50f98-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="50f98-108">Index de base zéro d’un bouton.</span><span class="sxs-lookup"><span data-stu-id="50f98-108">Zero-based index of a button.</span></span> <span data-ttu-id="50f98-109">Le message insère le bouton nouveau à gauche de ce bouton.</span><span class="sxs-lookup"><span data-stu-id="50f98-109">The message inserts the new button to the left of this button.</span></span>

</dd> <dt>

<span data-ttu-id="50f98-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="50f98-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="50f98-111">Pointeur vers une structure [**TBBUTTON**](/windows/desktop/api/Commctrl/ns-commctrl-tbbutton) contenant des informations sur le bouton à insérer.</span><span class="sxs-lookup"><span data-stu-id="50f98-111">Pointer to a [**TBBUTTON**](/windows/desktop/api/Commctrl/ns-commctrl-tbbutton) structure containing information about the button to insert.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="50f98-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="50f98-112">Return value</span></span>

<span data-ttu-id="50f98-113">Retourne la **valeur true** en cas de réussite, ou **false** dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="50f98-113">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="50f98-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="50f98-114">Requirements</span></span>



| <span data-ttu-id="50f98-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="50f98-115">Requirement</span></span> | <span data-ttu-id="50f98-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="50f98-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="50f98-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="50f98-117">Minimum supported client</span></span><br/> | <span data-ttu-id="50f98-118">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="50f98-118">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="50f98-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="50f98-119">Minimum supported server</span></span><br/> | <span data-ttu-id="50f98-120">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="50f98-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="50f98-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="50f98-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="50f98-122"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="50f98-122"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="50f98-123">Noms Unicode et ANSI</span><span class="sxs-lookup"><span data-stu-id="50f98-123">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="50f98-124">**To \_ INSERTBUTTONW** (Unicode) et **to \_ INSERTBUTTONA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="50f98-124">**TB\_INSERTBUTTONW** (Unicode) and **TB\_INSERTBUTTONA** (ANSI)</span></span><br/>           |



 

 





