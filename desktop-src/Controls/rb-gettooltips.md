---
title: Message RB_GETTOOLTIPS (commctrl. h)
description: Récupère le handle d’un contrôle ToolTip associé au contrôle rebar.
ms.assetid: 87897b00-857f-4a8a-ae16-a48abf4c411d
keywords:
- RB_GETTOOLTIPS les contrôles de message Windows
topic_type:
- apiref
api_name:
- RB_GETTOOLTIPS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 703b500e7009ca5f5cad46dc72d5deebeebca047
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104437"
---
# <a name="rb_gettooltips-message"></a><span data-ttu-id="c24b9-104">\_Message GETTOOLTIPS RB</span><span class="sxs-lookup"><span data-stu-id="c24b9-104">RB\_GETTOOLTIPS message</span></span>

<span data-ttu-id="c24b9-105">Récupère le handle d’un contrôle ToolTip associé au contrôle rebar.</span><span class="sxs-lookup"><span data-stu-id="c24b9-105">Retrieves the handle to any tooltip control associated with the rebar control.</span></span>

## <a name="parameters"></a><span data-ttu-id="c24b9-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c24b9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c24b9-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="c24b9-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="c24b9-108">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="c24b9-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="c24b9-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="c24b9-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="c24b9-110">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="c24b9-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c24b9-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="c24b9-111">Return value</span></span>

<span data-ttu-id="c24b9-112">Retourne une valeur **HWND** qui est le handle du contrôle ToolTip associé au contrôle rebar, ou zéro si aucun contrôle ToolTip n’est associé au contrôle rebar.</span><span class="sxs-lookup"><span data-stu-id="c24b9-112">Returns an **HWND** value that is the handle to the tooltip control associated with the rebar control, or zero if no tooltip control is associated with the rebar control.</span></span>

## <a name="requirements"></a><span data-ttu-id="c24b9-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c24b9-113">Requirements</span></span>



| <span data-ttu-id="c24b9-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c24b9-114">Requirement</span></span> | <span data-ttu-id="c24b9-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="c24b9-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c24b9-116">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c24b9-116">Minimum supported client</span></span><br/> | <span data-ttu-id="c24b9-117">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c24b9-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="c24b9-118">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c24b9-118">Minimum supported server</span></span><br/> | <span data-ttu-id="c24b9-119">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c24b9-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="c24b9-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="c24b9-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="c24b9-121"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="c24b9-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





