---
title: Message TB_GETTOOLTIPS (commctrl. h)
description: Récupère le handle du contrôle ToolTip, le cas échéant, associé à la barre d’outils.
ms.assetid: 1e0edfdc-d0cb-41f3-9178-1239d81d3034
keywords:
- TB_GETTOOLTIPS les contrôles de message Windows
topic_type:
- apiref
api_name:
- TB_GETTOOLTIPS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 488212b34f9f1816797f097a5a1f42d2ea4f68c0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104032942"
---
# <a name="tb_gettooltips-message"></a><span data-ttu-id="684d7-104">TO \_ GETTOOLTIPS message</span><span class="sxs-lookup"><span data-stu-id="684d7-104">TB\_GETTOOLTIPS message</span></span>

<span data-ttu-id="684d7-105">Récupère le handle du contrôle ToolTip, le cas échéant, associé à la barre d’outils.</span><span class="sxs-lookup"><span data-stu-id="684d7-105">Retrieves the handle to the tooltip control, if any, associated with the toolbar.</span></span>

## <a name="parameters"></a><span data-ttu-id="684d7-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="684d7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="684d7-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="684d7-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="684d7-108">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="684d7-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="684d7-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="684d7-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="684d7-110">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="684d7-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="684d7-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="684d7-111">Return value</span></span>

<span data-ttu-id="684d7-112">Retourne le handle du contrôle ToolTip, ou **null** si la barre d’outils n’est associée à aucune info-bulle.</span><span class="sxs-lookup"><span data-stu-id="684d7-112">Returns the handle to the tooltip control, or **NULL** if the toolbar has no associated tooltip.</span></span>

## <a name="requirements"></a><span data-ttu-id="684d7-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="684d7-113">Requirements</span></span>



| <span data-ttu-id="684d7-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="684d7-114">Requirement</span></span> | <span data-ttu-id="684d7-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="684d7-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="684d7-116">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="684d7-116">Minimum supported client</span></span><br/> | <span data-ttu-id="684d7-117">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="684d7-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="684d7-118">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="684d7-118">Minimum supported server</span></span><br/> | <span data-ttu-id="684d7-119">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="684d7-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="684d7-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="684d7-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="684d7-121"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="684d7-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





