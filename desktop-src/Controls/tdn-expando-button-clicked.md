---
title: TDN_EXPANDO_BUTTON_CLICKED le code de notification (commctrl. h)
description: Envoyé par la boîte de dialogue de tâche lorsque l’utilisateur clique sur le bouton développé de la boîte de dialogue. Cette notification est reçue uniquement par le biais de la fonction de rappel de la boîte de dialogue de tâche, qui peut être inscrite à l’aide de la méthode TaskDialogIndirect.
ms.assetid: 15e2a9d0-9986-4fb1-a15e-dd4839e45146
keywords:
- Contrôles Windows de code de notification TDN_EXPANDO_BUTTON_CLICKED
topic_type:
- apiref
api_name:
- TDN_EXPANDO_BUTTON_CLICKED
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4f3c36379a8efc40c7873d817b832705b3c1e084
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106511184"
---
# <a name="tdn_expando_button_clicked-notification-code"></a><span data-ttu-id="6131e-105">\_Bouton TDN expando- \_ \_ clic sur le code de notification</span><span class="sxs-lookup"><span data-stu-id="6131e-105">TDN\_EXPANDO\_BUTTON\_CLICKED notification code</span></span>

<span data-ttu-id="6131e-106">Envoyé par la boîte de dialogue de tâche lorsque l’utilisateur clique sur le bouton développé de la boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="6131e-106">Sent by the task dialog when the user clicks on the dialog's expando button.</span></span> <span data-ttu-id="6131e-107">Cette notification est reçue uniquement par le biais de la fonction de rappel de la boîte de dialogue de tâche, qui peut être inscrite à l’aide de la méthode [**TaskDialogIndirect**](/windows/desktop/api/Commctrl/nf-commctrl-taskdialogindirect) .</span><span class="sxs-lookup"><span data-stu-id="6131e-107">This notification is received only through the task dialog callback function, which can be registered using the [**TaskDialogIndirect**](/windows/desktop/api/Commctrl/nf-commctrl-taskdialogindirect) method.</span></span>


```C++
TDN_EXPANDO_BUTTON_CLICKED
        
   WPARAM wParam;
   LPARAM lParam;
```



## <a name="parameters"></a><span data-ttu-id="6131e-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="6131e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6131e-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="6131e-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="6131e-110">Valeur **booléenne** qui est **true** si la boîte de dialogue est développée, ou **false** dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="6131e-110">A **BOOL** that is **TRUE** if the dialog is expanded, or **FALSE** if not.</span></span>

</dd> <dt>

<span data-ttu-id="6131e-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="6131e-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="6131e-112">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="6131e-112">Must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6131e-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="6131e-113">Return value</span></span>

<span data-ttu-id="6131e-114">La valeur de retour est ignorée.</span><span class="sxs-lookup"><span data-stu-id="6131e-114">The return value is ignored.</span></span>

## <a name="remarks"></a><span data-ttu-id="6131e-115">Notes</span><span class="sxs-lookup"><span data-stu-id="6131e-115">Remarks</span></span>

<span data-ttu-id="6131e-116">L’exemple de la section syntaxe montre le cast en wParam avant l’envoi de la notification.</span><span class="sxs-lookup"><span data-stu-id="6131e-116">The example in the Syntax section shows the cast to wParam before sending the notification.</span></span> <span data-ttu-id="6131e-117">**LParam** n’est pas utilisé et doit être égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="6131e-117">**LPARAM** is not used and must be zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="6131e-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="6131e-118">Requirements</span></span>



| <span data-ttu-id="6131e-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="6131e-119">Requirement</span></span> | <span data-ttu-id="6131e-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="6131e-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="6131e-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6131e-121">Minimum supported client</span></span><br/> | <span data-ttu-id="6131e-122">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="6131e-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="6131e-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6131e-123">Minimum supported server</span></span><br/> | <span data-ttu-id="6131e-124">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="6131e-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="6131e-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="6131e-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="6131e-126"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="6131e-126"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





