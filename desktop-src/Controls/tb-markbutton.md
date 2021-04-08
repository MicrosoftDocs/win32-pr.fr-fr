---
title: Message TB_MARKBUTTON (commctrl. h)
description: Définit l’état de surbrillance d’un bouton donné dans un contrôle ToolBar.
ms.assetid: cba0e2d2-40a7-4e20-a1ef-d5f5444c96d9
keywords:
- TB_MARKBUTTON les contrôles de message Windows
topic_type:
- apiref
api_name:
- TB_MARKBUTTON
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9d42983f5fb0ef6e62716cefa2fa8db4fca87fa4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104033094"
---
# <a name="tb_markbutton-message"></a><span data-ttu-id="8466e-104">TO \_ MARKBUTTON message</span><span class="sxs-lookup"><span data-stu-id="8466e-104">TB\_MARKBUTTON message</span></span>

<span data-ttu-id="8466e-105">Définit l’état de surbrillance d’un bouton donné dans un contrôle ToolBar.</span><span class="sxs-lookup"><span data-stu-id="8466e-105">Sets the highlight state of a given button in a toolbar control.</span></span>

## <a name="parameters"></a><span data-ttu-id="8466e-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="8466e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8466e-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="8466e-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="8466e-108">Identificateur de commande pour un bouton de barre d’outils.</span><span class="sxs-lookup"><span data-stu-id="8466e-108">Command identifier for a toolbar button.</span></span>

</dd> <dt>

<span data-ttu-id="8466e-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="8466e-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="8466e-110">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) est un **booléen** qui indique le nouvel état de mise en surbrillance.</span><span class="sxs-lookup"><span data-stu-id="8466e-110">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) is a **BOOL** that indicates the new highlight state.</span></span> <span data-ttu-id="8466e-111">Si la **valeur est true**, le bouton est mis en surbrillance.</span><span class="sxs-lookup"><span data-stu-id="8466e-111">If **TRUE**, the button is highlighted.</span></span> <span data-ttu-id="8466e-112">Si la **valeur est false**, le bouton est défini sur son état par défaut.</span><span class="sxs-lookup"><span data-stu-id="8466e-112">If **FALSE**, the button is set to its default state.</span></span>

<span data-ttu-id="8466e-113">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) doit être égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="8466e-113">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8466e-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="8466e-114">Return value</span></span>

<span data-ttu-id="8466e-115">Retourne une valeur différente de zéro en cas de réussite, ou zéro dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="8466e-115">Returns nonzero if successful, or zero otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="8466e-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8466e-116">Requirements</span></span>



| <span data-ttu-id="8466e-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="8466e-117">Requirement</span></span> | <span data-ttu-id="8466e-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="8466e-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="8466e-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8466e-119">Minimum supported client</span></span><br/> | <span data-ttu-id="8466e-120">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="8466e-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="8466e-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8466e-121">Minimum supported server</span></span><br/> | <span data-ttu-id="8466e-122">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="8466e-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="8466e-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="8466e-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="8466e-124"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="8466e-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

