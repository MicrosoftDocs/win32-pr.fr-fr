---
title: Message TDM_CLICK_BUTTON (commctrl. h)
description: Simule l’action d’un clic sur un bouton dans une boîte de dialogue de tâche.
ms.assetid: cc8a8252-3418-4a28-bfb7-11d6e3fee903
keywords:
- TDM_CLICK_BUTTON les contrôles de message Windows
topic_type:
- apiref
api_name:
- TDM_CLICK_BUTTON
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5e5933668eca907f36414113091b8901bfb9c110
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106510965"
---
# <a name="tdm_click_button-message"></a><span data-ttu-id="a00a2-104">Message de bouton de \_ clic TDM \_</span><span class="sxs-lookup"><span data-stu-id="a00a2-104">TDM\_CLICK\_BUTTON message</span></span>

<span data-ttu-id="a00a2-105">Simule l’action d’un clic sur un bouton dans une boîte de dialogue de tâche.</span><span class="sxs-lookup"><span data-stu-id="a00a2-105">Simulates the action of a button click in a task dialog.</span></span>

## <a name="parameters"></a><span data-ttu-id="a00a2-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a00a2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a00a2-107">*wParam* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="a00a2-107">*wParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a00a2-108">**Entier** qui spécifie l’ID du bouton sur lequel un clic a été effectué.</span><span class="sxs-lookup"><span data-stu-id="a00a2-108">An **int** that specifies the ID of the button to be clicked.</span></span>

</dd> <dt>

<span data-ttu-id="a00a2-109">*lParam* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="a00a2-109">*lParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a00a2-110">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="a00a2-110">Must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a00a2-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="a00a2-111">Return value</span></span>

<span data-ttu-id="a00a2-112">La valeur de retour est ignorée.</span><span class="sxs-lookup"><span data-stu-id="a00a2-112">The return value is ignored.</span></span>

## <a name="remarks"></a><span data-ttu-id="a00a2-113">Notes</span><span class="sxs-lookup"><span data-stu-id="a00a2-113">Remarks</span></span>

<span data-ttu-id="a00a2-114">L’ID de bouton spécifié par *wParam* est envoyé à la fonction de rappel [**TaskDialogCallbackProc**](/windows/win32/api/commctrl/nc-commctrl-pftaskdialogcallback) dans le cadre d’un [ \_ \_ clic sur](tdn-button-clicked.md) le code de notification du bouton TDN.</span><span class="sxs-lookup"><span data-stu-id="a00a2-114">The button ID specified by *wParam* is sent to the [**TaskDialogCallbackProc**](/windows/win32/api/commctrl/nc-commctrl-pftaskdialogcallback) callback function as part of a [TDN\_BUTTON\_CLICKED](tdn-button-clicked.md) notification code.</span></span> <span data-ttu-id="a00a2-115">Une fois que la fonction de rappel a été retournée, la boîte de dialogue de tâche est fermée si l’opération \_ a été retournée à partir de la fonction de rappel.</span><span class="sxs-lookup"><span data-stu-id="a00a2-115">After the callback function returns, the task dialog is closed if S\_OK was returned from the callback function.</span></span> <span data-ttu-id="a00a2-116">Si S \_ false a été retourné à partir de la fonction de rappel, la boîte de dialogue de tâche reste active.</span><span class="sxs-lookup"><span data-stu-id="a00a2-116">If S\_FALSE was returned from the callback function, the task dialog remains active.</span></span>

## <a name="requirements"></a><span data-ttu-id="a00a2-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a00a2-117">Requirements</span></span>



| <span data-ttu-id="a00a2-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a00a2-118">Requirement</span></span> | <span data-ttu-id="a00a2-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="a00a2-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a00a2-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a00a2-120">Minimum supported client</span></span><br/> | <span data-ttu-id="a00a2-121">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a00a2-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="a00a2-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a00a2-122">Minimum supported server</span></span><br/> | <span data-ttu-id="a00a2-123">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a00a2-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="a00a2-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="a00a2-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="a00a2-125"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="a00a2-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

