---
title: TDN_BUTTON_CLICKED le code de notification (commctrl. h)
description: Envoyé par une boîte de dialogue de tâche lorsque l’utilisateur sélectionne un bouton ou un lien de commande dans la boîte de dialogue de tâche. Ce code de notification est reçu uniquement par le biais de la fonction de rappel de la boîte de dialogue de tâche, qui peut être inscrite à l’aide de la méthode TaskDialogIndirect.
ms.assetid: eefe48f8-8a80-4280-8a7e-244d9b699ec7
keywords:
- Contrôles Windows de code de notification TDN_BUTTON_CLICKED
topic_type:
- apiref
api_name:
- TDN_BUTTON_CLICKED
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8a7a0b799f4163633194306edaa1703e068e93c9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942842"
---
# <a name="tdn_button_clicked-notification-code"></a><span data-ttu-id="91bee-105">\_Clic sur le bouton TDN du \_ Code de notification</span><span class="sxs-lookup"><span data-stu-id="91bee-105">TDN\_BUTTON\_CLICKED notification code</span></span>

<span data-ttu-id="91bee-106">Envoyé par une boîte de dialogue de tâche lorsque l’utilisateur sélectionne un bouton ou un lien de commande dans la boîte de dialogue de tâche.</span><span class="sxs-lookup"><span data-stu-id="91bee-106">Sent by a task dialog when the user selects a button or command link in the task dialog.</span></span> <span data-ttu-id="91bee-107">Ce code de notification est reçu uniquement par le biais de la fonction de rappel de la boîte de dialogue de tâche, qui peut être inscrite à l’aide de la méthode [**TaskDialogIndirect**](/windows/desktop/api/Commctrl/nf-commctrl-taskdialogindirect) .</span><span class="sxs-lookup"><span data-stu-id="91bee-107">This notification code is received only through the task dialog callback function, which can be registered using the [**TaskDialogIndirect**](/windows/desktop/api/Commctrl/nf-commctrl-taskdialogindirect) method.</span></span>


```C++
TDN_BUTTON_CLICKED  

   WPARAM wParam;
   LPARAM lParam;
```



## <a name="parameters"></a><span data-ttu-id="91bee-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="91bee-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="91bee-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="91bee-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="91bee-110">**Entier** qui spécifie l’ID du bouton ou du lien de la connexion qui a été sélectionné.</span><span class="sxs-lookup"><span data-stu-id="91bee-110">An **int** that specifies the ID of the button or comand link that was selected.</span></span>

</dd> <dt>

<span data-ttu-id="91bee-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="91bee-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="91bee-112">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="91bee-112">Must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="91bee-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="91bee-113">Return value</span></span>

<span data-ttu-id="91bee-114">Pour empêcher la fermeture de la boîte de dialogue de tâche, l’application doit retourner la **\_ valeur false**, sinon la boîte de dialogue de tâche est fermée et l’ID de bouton est retourné via l’appel d’application d’origine.</span><span class="sxs-lookup"><span data-stu-id="91bee-114">To prevent the task dialog from closing, the application must return **S\_FALSE**, otherwise the task dialog is closed and the button ID is returned via the original application call.</span></span>

## <a name="requirements"></a><span data-ttu-id="91bee-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="91bee-115">Requirements</span></span>



| <span data-ttu-id="91bee-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="91bee-116">Requirement</span></span> | <span data-ttu-id="91bee-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="91bee-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="91bee-118">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="91bee-118">Minimum supported client</span></span><br/> | <span data-ttu-id="91bee-119">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="91bee-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="91bee-120">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="91bee-120">Minimum supported server</span></span><br/> | <span data-ttu-id="91bee-121">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="91bee-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="91bee-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="91bee-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="91bee-123"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="91bee-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





