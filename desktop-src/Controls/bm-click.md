---
title: Message BM_CLICK (winuser. h)
description: Simule l’utilisateur qui clique sur un bouton. Ce message force le bouton à recevoir les \_ messages WM LBUTTONDOWN et WM \_ LBUTTONUP, ainsi que la fenêtre parente du bouton pour recevoir un code de notification sur lequel un clic a été \_ effectué.
ms.assetid: f76ca5eb-170c-43fc-a239-67af15497f08
keywords:
- BM_CLICK les contrôles de message Windows
topic_type:
- apiref
api_name:
- BM_CLICK
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7b86c4809ac1ded3a9b7c57d1b73b70ab1cebc3b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104032566"
---
# <a name="bm_click-message"></a><span data-ttu-id="64f8d-105">\_Message de clic sur BM</span><span class="sxs-lookup"><span data-stu-id="64f8d-105">BM\_CLICK message</span></span>

<span data-ttu-id="64f8d-106">Simule l’utilisateur qui clique sur un bouton.</span><span class="sxs-lookup"><span data-stu-id="64f8d-106">Simulates the user clicking a button.</span></span> <span data-ttu-id="64f8d-107">Ce message force le bouton à recevoir les messages [**WM \_ LBUTTONDOWN**](/windows/desktop/inputdev/wm-lbuttondown) et [**WM \_ LBUTTONUP**](/windows/desktop/inputdev/wm-lbuttonup) , ainsi que la fenêtre parente du bouton pour recevoir un code de notification sur lequel un clic a été [ \_ effectué](bn-clicked.md) .</span><span class="sxs-lookup"><span data-stu-id="64f8d-107">This message causes the button to receive the [**WM\_LBUTTONDOWN**](/windows/desktop/inputdev/wm-lbuttondown) and [**WM\_LBUTTONUP**](/windows/desktop/inputdev/wm-lbuttonup) messages, and the button's parent window to receive a [BN\_CLICKED](bn-clicked.md) notification code.</span></span>

## <a name="parameters"></a><span data-ttu-id="64f8d-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="64f8d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="64f8d-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="64f8d-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="64f8d-110">Non utilisé ; doit être égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="64f8d-110">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="64f8d-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="64f8d-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="64f8d-112">Non utilisé ; doit être égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="64f8d-112">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="64f8d-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="64f8d-113">Return value</span></span>

<span data-ttu-id="64f8d-114">Ce message ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="64f8d-114">This message does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="64f8d-115">Notes</span><span class="sxs-lookup"><span data-stu-id="64f8d-115">Remarks</span></span>

<span data-ttu-id="64f8d-116">Si le bouton se trouve dans une boîte de dialogue et que la boîte de dialogue n’est pas active, le message de **\_ clic** peut échouer.</span><span class="sxs-lookup"><span data-stu-id="64f8d-116">If the button is in a dialog box and the dialog box is not active, the **BM\_CLICK** message might fail.</span></span> <span data-ttu-id="64f8d-117">Pour garantir la réussite de cette situation, appelez la fonction [**SetActiveWindow**](/windows/desktop/api/winuser/nf-winuser-setactivewindow) pour activer la boîte de dialogue avant d’envoyer le message de **\_ clic de BM** au bouton.</span><span class="sxs-lookup"><span data-stu-id="64f8d-117">To ensure success in this situation, call the [**SetActiveWindow**](/windows/desktop/api/winuser/nf-winuser-setactivewindow) function to activate the dialog box before sending the **BM\_CLICK** message to the button.</span></span>

## <a name="requirements"></a><span data-ttu-id="64f8d-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="64f8d-118">Requirements</span></span>



| <span data-ttu-id="64f8d-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="64f8d-119">Requirement</span></span> | <span data-ttu-id="64f8d-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="64f8d-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="64f8d-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="64f8d-121">Minimum supported client</span></span><br/> | <span data-ttu-id="64f8d-122">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="64f8d-122">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="64f8d-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="64f8d-123">Minimum supported server</span></span><br/> | <span data-ttu-id="64f8d-124">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="64f8d-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="64f8d-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="64f8d-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="64f8d-126"><dt>Winuser. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="64f8d-126"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



 

