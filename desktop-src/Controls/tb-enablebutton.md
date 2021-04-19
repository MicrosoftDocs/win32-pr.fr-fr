---
title: Message TB_ENABLEBUTTON (commctrl. h)
description: Active ou désactive le bouton spécifié dans une barre d’outils.
ms.assetid: d73851ee-f909-4b70-9514-c45cd3a7e999
keywords:
- TB_ENABLEBUTTON les contrôles de message Windows
topic_type:
- apiref
api_name:
- TB_ENABLEBUTTON
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: caf2fe865d49f9c89e31b1701abfcbf7991ae72e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106515685"
---
# <a name="tb_enablebutton-message"></a><span data-ttu-id="66cbc-104">TO \_ ENABLEBUTTON message</span><span class="sxs-lookup"><span data-stu-id="66cbc-104">TB\_ENABLEBUTTON message</span></span>

<span data-ttu-id="66cbc-105">Active ou désactive le bouton spécifié dans une barre d’outils.</span><span class="sxs-lookup"><span data-stu-id="66cbc-105">Enables or disables the specified button in a toolbar.</span></span>

## <a name="parameters"></a><span data-ttu-id="66cbc-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="66cbc-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="66cbc-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="66cbc-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="66cbc-108">Identificateur de commande du bouton à activer ou à désactiver.</span><span class="sxs-lookup"><span data-stu-id="66cbc-108">Command identifier of the button to enable or disable.</span></span>

</dd> <dt>

<span data-ttu-id="66cbc-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="66cbc-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="66cbc-110">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) est un **booléen** qui indique s’il faut activer ou désactiver le bouton spécifié.</span><span class="sxs-lookup"><span data-stu-id="66cbc-110">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) is a **BOOL** that indicates whether to enable or disable the specified button.</span></span> <span data-ttu-id="66cbc-111">Si la **valeur est true**, le bouton est activé.</span><span class="sxs-lookup"><span data-stu-id="66cbc-111">If **TRUE**, the button is enabled.</span></span> <span data-ttu-id="66cbc-112">Si la **valeur est false**, le bouton est désactivé.</span><span class="sxs-lookup"><span data-stu-id="66cbc-112">If **FALSE**, the button is disabled.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="66cbc-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="66cbc-113">Return value</span></span>

<span data-ttu-id="66cbc-114">Retourne la **valeur true** en cas de réussite, ou **false** dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="66cbc-114">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="66cbc-115">Notes</span><span class="sxs-lookup"><span data-stu-id="66cbc-115">Remarks</span></span>

<span data-ttu-id="66cbc-116">Lorsqu’un bouton a été activé, il peut être appuyé et activé.</span><span class="sxs-lookup"><span data-stu-id="66cbc-116">When a button has been enabled, it can be pressed and checked.</span></span>

## <a name="requirements"></a><span data-ttu-id="66cbc-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="66cbc-117">Requirements</span></span>



| <span data-ttu-id="66cbc-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="66cbc-118">Requirement</span></span> | <span data-ttu-id="66cbc-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="66cbc-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="66cbc-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="66cbc-120">Minimum supported client</span></span><br/> | <span data-ttu-id="66cbc-121">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="66cbc-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="66cbc-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="66cbc-122">Minimum supported server</span></span><br/> | <span data-ttu-id="66cbc-123">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="66cbc-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="66cbc-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="66cbc-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="66cbc-125"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="66cbc-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

