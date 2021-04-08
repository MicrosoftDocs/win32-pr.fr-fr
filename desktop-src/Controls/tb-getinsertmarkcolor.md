---
title: Message TB_GETINSERTMARKCOLOR (commctrl. h)
description: Récupère la couleur utilisée pour dessiner la marque d’insertion pour la barre d’outils.
ms.assetid: 52915dc6-a45c-4f3b-aa9b-99a23d423e59
keywords:
- TB_GETINSERTMARKCOLOR les contrôles de message Windows
topic_type:
- apiref
api_name:
- TB_GETINSERTMARKCOLOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 104ceebd5f3989ed870cf70ccad819300d85c05d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843609"
---
# <a name="tb_getinsertmarkcolor-message"></a><span data-ttu-id="e0e28-104">TO \_ GETINSERTMARKCOLOR message</span><span class="sxs-lookup"><span data-stu-id="e0e28-104">TB\_GETINSERTMARKCOLOR message</span></span>

<span data-ttu-id="e0e28-105">Récupère la couleur utilisée pour dessiner la marque d’insertion pour la barre d’outils.</span><span class="sxs-lookup"><span data-stu-id="e0e28-105">Retrieves the color used to draw the insertion mark for the toolbar.</span></span>

## <a name="parameters"></a><span data-ttu-id="e0e28-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e0e28-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e0e28-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="e0e28-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="e0e28-108">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="e0e28-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="e0e28-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="e0e28-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="e0e28-110">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="e0e28-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e0e28-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="e0e28-111">Return value</span></span>

<span data-ttu-id="e0e28-112">Retourne une valeur [**COLORREF**](/windows/desktop/gdi/colorref) qui contient la couleur de la marque d’insertion actuelle.</span><span class="sxs-lookup"><span data-stu-id="e0e28-112">Returns a [**COLORREF**](/windows/desktop/gdi/colorref) value that contains the current insertion mark color.</span></span>

## <a name="requirements"></a><span data-ttu-id="e0e28-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e0e28-113">Requirements</span></span>



| <span data-ttu-id="e0e28-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e0e28-114">Requirement</span></span> | <span data-ttu-id="e0e28-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="e0e28-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e0e28-116">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e0e28-116">Minimum supported client</span></span><br/> | <span data-ttu-id="e0e28-117">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e0e28-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="e0e28-118">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e0e28-118">Minimum supported server</span></span><br/> | <span data-ttu-id="e0e28-119">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e0e28-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="e0e28-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="e0e28-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="e0e28-121"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="e0e28-121"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e0e28-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e0e28-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e0e28-123">**TO \_ SETINSERTMARKCOLOR**</span><span class="sxs-lookup"><span data-stu-id="e0e28-123">**TB\_SETINSERTMARKCOLOR**</span></span>](tb-setinsertmarkcolor.md)
</dt> </dl>

 

