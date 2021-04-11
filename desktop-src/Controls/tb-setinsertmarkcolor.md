---
title: Message TB_SETINSERTMARKCOLOR (commctrl. h)
description: Définit la couleur utilisée pour dessiner la marque d’insertion pour la barre d’outils.
ms.assetid: 09a04449-9a1f-4f9a-b09f-9f22f930d735
keywords:
- TB_SETINSERTMARKCOLOR les contrôles de message Windows
topic_type:
- apiref
api_name:
- TB_SETINSERTMARKCOLOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 954654d71a3e3b7bba9af287d3e92fb2362e8711
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104102865"
---
# <a name="tb_setinsertmarkcolor-message"></a><span data-ttu-id="0f02e-104">TO \_ SETINSERTMARKCOLOR message</span><span class="sxs-lookup"><span data-stu-id="0f02e-104">TB\_SETINSERTMARKCOLOR message</span></span>

<span data-ttu-id="0f02e-105">Définit la couleur utilisée pour dessiner la marque d’insertion pour la barre d’outils.</span><span class="sxs-lookup"><span data-stu-id="0f02e-105">Sets the color used to draw the insertion mark for the toolbar.</span></span>

## <a name="parameters"></a><span data-ttu-id="0f02e-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="0f02e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0f02e-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="0f02e-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="0f02e-108">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="0f02e-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="0f02e-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="0f02e-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="0f02e-110">Valeur **COLORREF** qui contient la nouvelle couleur de la marque d’insertion.</span><span class="sxs-lookup"><span data-stu-id="0f02e-110">**COLORREF** value that contains the new insertion mark color.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0f02e-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="0f02e-111">Return value</span></span>

<span data-ttu-id="0f02e-112">Retourne une valeur **COLORREF** qui contient la couleur de la marque d’insertion précédente.</span><span class="sxs-lookup"><span data-stu-id="0f02e-112">Returns a **COLORREF** value that contains the previous insertion mark color.</span></span>

## <a name="requirements"></a><span data-ttu-id="0f02e-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0f02e-113">Requirements</span></span>



| <span data-ttu-id="0f02e-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0f02e-114">Requirement</span></span> | <span data-ttu-id="0f02e-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="0f02e-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="0f02e-116">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0f02e-116">Minimum supported client</span></span><br/> | <span data-ttu-id="0f02e-117">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="0f02e-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="0f02e-118">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0f02e-118">Minimum supported server</span></span><br/> | <span data-ttu-id="0f02e-119">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="0f02e-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="0f02e-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="0f02e-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="0f02e-121"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="0f02e-121"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0f02e-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0f02e-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0f02e-123">**TO \_ GETINSERTMARKCOLOR**</span><span class="sxs-lookup"><span data-stu-id="0f02e-123">**TB\_GETINSERTMARKCOLOR**</span></span>](tb-getinsertmarkcolor.md)
</dt> </dl>

 

 





