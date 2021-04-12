---
title: Message TB_PRESSBUTTON (commctrl. h)
description: Appuie sur le bouton spécifié ou le relâche dans une barre d’outils.
ms.assetid: 03f6c3c2-d679-4e3a-a07b-c7e46c97972a
keywords:
- TB_PRESSBUTTON les contrôles de message Windows
topic_type:
- apiref
api_name:
- TB_PRESSBUTTON
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5b0e86092951b242cee7388fc0d5d1bbdbca835e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105043"
---
# <a name="tb_pressbutton-message"></a><span data-ttu-id="ae199-104">TO \_ PRESSBUTTON message</span><span class="sxs-lookup"><span data-stu-id="ae199-104">TB\_PRESSBUTTON message</span></span>

<span data-ttu-id="ae199-105">Appuie sur le bouton spécifié ou le relâche dans une barre d’outils.</span><span class="sxs-lookup"><span data-stu-id="ae199-105">Presses or releases the specified button in a toolbar.</span></span>

## <a name="parameters"></a><span data-ttu-id="ae199-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ae199-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ae199-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="ae199-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ae199-108">Identificateur de commande du bouton à appuyer ou à libérer.</span><span class="sxs-lookup"><span data-stu-id="ae199-108">Command identifier of the button to press or release.</span></span>

</dd> <dt>

<span data-ttu-id="ae199-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="ae199-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ae199-110">Le [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) est un **booléen** qui indique s’il faut appuyer ou relâcher le bouton spécifié.</span><span class="sxs-lookup"><span data-stu-id="ae199-110">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) is a **BOOL** that indicates whether to press or release the specified button.</span></span> <span data-ttu-id="ae199-111">Si la **valeur est true**, le bouton est enfoncé.</span><span class="sxs-lookup"><span data-stu-id="ae199-111">If **TRUE**, the button is pressed.</span></span> <span data-ttu-id="ae199-112">Si la **valeur est false**, le bouton est relâché.</span><span class="sxs-lookup"><span data-stu-id="ae199-112">If **FALSE**, the button is released.</span></span>

<span data-ttu-id="ae199-113">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) doit être égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="ae199-113">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ae199-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="ae199-114">Return value</span></span>

<span data-ttu-id="ae199-115">Retourne la **valeur true** en cas de réussite, ou **false** dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="ae199-115">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="ae199-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ae199-116">Requirements</span></span>



| <span data-ttu-id="ae199-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ae199-117">Requirement</span></span> | <span data-ttu-id="ae199-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="ae199-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ae199-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ae199-119">Minimum supported client</span></span><br/> | <span data-ttu-id="ae199-120">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ae199-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="ae199-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ae199-121">Minimum supported server</span></span><br/> | <span data-ttu-id="ae199-122">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ae199-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="ae199-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="ae199-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="ae199-124"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="ae199-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

