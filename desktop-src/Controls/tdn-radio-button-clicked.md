---
title: TDN_RADIO_BUTTON_CLICKED le code de notification (commctrl. h)
description: Envoyé par une boîte de dialogue de tâche lorsque l’utilisateur sélectionne une case d’option ou un lien de commande dans la boîte de dialogue de tâche. Ce code de notification est reçu uniquement par le biais de la fonction de rappel de la boîte de dialogue de tâche, qui peut être inscrite à l’aide de la méthode TaskDialogIndirect.
ms.assetid: d9a29874-6755-4754-bcaf-94746b218b47
keywords:
- Contrôles Windows de code de notification TDN_RADIO_BUTTON_CLICKED
topic_type:
- apiref
api_name:
- TDN_RADIO_BUTTON_CLICKED
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a0c8b16f738e4807c94a060b41b3932d0f3e07ea
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942838"
---
# <a name="tdn_radio_button_clicked-notification-code"></a><span data-ttu-id="720cd-105">\_Bouton radio \_ TDN \_ clic sur le code de notification</span><span class="sxs-lookup"><span data-stu-id="720cd-105">TDN\_RADIO\_BUTTON\_CLICKED notification code</span></span>

<span data-ttu-id="720cd-106">Envoyé par une boîte de dialogue de tâche lorsque l’utilisateur sélectionne une case d’option ou un lien de commande dans la boîte de dialogue de tâche.</span><span class="sxs-lookup"><span data-stu-id="720cd-106">Sent by a task dialog when the user selects a radio button or command link in the task dialog.</span></span> <span data-ttu-id="720cd-107">Ce code de notification est reçu uniquement par le biais de la fonction de rappel de la boîte de dialogue de tâche, qui peut être inscrite à l’aide de la méthode [**TaskDialogIndirect**](/windows/desktop/api/Commctrl/nf-commctrl-taskdialogindirect) .</span><span class="sxs-lookup"><span data-stu-id="720cd-107">This notification code is received only through the task dialog callback function, which can be registered using the [**TaskDialogIndirect**](/windows/desktop/api/Commctrl/nf-commctrl-taskdialogindirect) method.</span></span>


```C++
TDN_RADIO_BUTTON_CLICKED

   WPARAM wParam;
   LPARAM lParam;
```



## <a name="parameters"></a><span data-ttu-id="720cd-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="720cd-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="720cd-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="720cd-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="720cd-110">**Entier** qui spécifie l’ID correspondant à la case d’option sur laquelle l’utilisateur a cliqué.</span><span class="sxs-lookup"><span data-stu-id="720cd-110">An **int** that specifies the ID corresponding to the radio button that was clicked.</span></span>

</dd> <dt>

<span data-ttu-id="720cd-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="720cd-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="720cd-112">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="720cd-112">Must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="720cd-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="720cd-113">Return value</span></span>

<span data-ttu-id="720cd-114">La valeur de retour est ignorée.</span><span class="sxs-lookup"><span data-stu-id="720cd-114">The return value is ignored.</span></span>

## <a name="requirements"></a><span data-ttu-id="720cd-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="720cd-115">Requirements</span></span>



| <span data-ttu-id="720cd-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="720cd-116">Requirement</span></span> | <span data-ttu-id="720cd-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="720cd-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="720cd-118">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="720cd-118">Minimum supported client</span></span><br/> | <span data-ttu-id="720cd-119">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="720cd-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="720cd-120">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="720cd-120">Minimum supported server</span></span><br/> | <span data-ttu-id="720cd-121">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="720cd-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="720cd-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="720cd-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="720cd-123"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="720cd-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





