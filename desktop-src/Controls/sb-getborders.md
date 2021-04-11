---
title: Message SB_GETBORDERS (commctrl. h)
description: Récupère les largeurs actuelles des bordures horizontale et verticale d’une fenêtre d’État.
ms.assetid: 120c1e0d-6f42-424e-94e0-a080d216d39d
keywords:
- SB_GETBORDERS les contrôles de message Windows
topic_type:
- apiref
api_name:
- SB_GETBORDERS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 854df2cd367a852a2e6a0e638b470187efabe58c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105082"
---
# <a name="sb_getborders-message"></a><span data-ttu-id="56807-104">\_Message SB GETBORDERS</span><span class="sxs-lookup"><span data-stu-id="56807-104">SB\_GETBORDERS message</span></span>

<span data-ttu-id="56807-105">Récupère les largeurs actuelles des bordures horizontale et verticale d’une fenêtre d’État.</span><span class="sxs-lookup"><span data-stu-id="56807-105">Retrieves the current widths of the horizontal and vertical borders of a status window.</span></span>

## <a name="parameters"></a><span data-ttu-id="56807-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="56807-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="56807-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="56807-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="56807-108">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="56807-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="56807-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="56807-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="56807-110">Pointeur vers un tableau d’entiers qui a trois éléments.</span><span class="sxs-lookup"><span data-stu-id="56807-110">Pointer to an integer array that has three elements.</span></span> <span data-ttu-id="56807-111">Le premier élément reçoit la largeur de la bordure horizontale, le deuxième reçoit la largeur de la bordure verticale et le troisième reçoit la largeur de la bordure entre les rectangles.</span><span class="sxs-lookup"><span data-stu-id="56807-111">The first element receives the width of the horizontal border, the second receives the width of the vertical border, and the third receives the width of the border between rectangles.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="56807-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="56807-112">Return value</span></span>

<span data-ttu-id="56807-113">Retourne la **valeur true** en cas de réussite, ou **false** dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="56807-113">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="56807-114">Notes</span><span class="sxs-lookup"><span data-stu-id="56807-114">Remarks</span></span>

<span data-ttu-id="56807-115">Les bordures déterminent l’espacement entre le bord extérieur de la fenêtre et les rectangles de la fenêtre qui contiennent du texte.</span><span class="sxs-lookup"><span data-stu-id="56807-115">The borders determine the spacing between the outside edge of the window and the rectangles within the window that contain text.</span></span> <span data-ttu-id="56807-116">Les bordures déterminent également l’espacement entre les rectangles.</span><span class="sxs-lookup"><span data-stu-id="56807-116">The borders also determine the spacing between rectangles.</span></span>

## <a name="requirements"></a><span data-ttu-id="56807-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="56807-117">Requirements</span></span>



| <span data-ttu-id="56807-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="56807-118">Requirement</span></span> | <span data-ttu-id="56807-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="56807-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="56807-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="56807-120">Minimum supported client</span></span><br/> | <span data-ttu-id="56807-121">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="56807-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="56807-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="56807-122">Minimum supported server</span></span><br/> | <span data-ttu-id="56807-123">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="56807-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="56807-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="56807-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="56807-125"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="56807-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





