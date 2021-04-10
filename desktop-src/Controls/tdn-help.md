---
title: TDN_HELP le code de notification (commctrl. h)
description: Envoyé par une boîte de dialogue de tâche lorsque l’utilisateur appuie sur la touche F1 du clavier pendant que la boîte de dialogue a le focus. Ce code de notification est reçu uniquement par le biais de la fonction de rappel de la boîte de dialogue de tâche, qui peut être inscrite à l’aide de la méthode TaskDialogIndirect.
ms.assetid: 207ba231-639d-4906-b5dc-1592f2717f1c
keywords:
- Contrôles Windows de code de notification TDN_HELP
topic_type:
- apiref
api_name:
- TDN_HELP
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 64d5e08342094aec5adc3da42621307d1577cd68
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104106237"
---
# <a name="tdn_help-notification-code"></a><span data-ttu-id="c8f5c-105">\_Code de notification d’aide TDN</span><span class="sxs-lookup"><span data-stu-id="c8f5c-105">TDN\_HELP notification code</span></span>

<span data-ttu-id="c8f5c-106">Envoyé par une boîte de dialogue de tâche lorsque l’utilisateur appuie sur la touche F1 du clavier pendant que la boîte de dialogue a le focus.</span><span class="sxs-lookup"><span data-stu-id="c8f5c-106">Sent by a task dialog when the user presses F1 on the keyboard while the dialog has focus.</span></span> <span data-ttu-id="c8f5c-107">Ce code de notification est reçu uniquement par le biais de la fonction de rappel de la boîte de dialogue de tâche, qui peut être inscrite à l’aide de la méthode [**TaskDialogIndirect**](/windows/desktop/api/Commctrl/nf-commctrl-taskdialogindirect) .</span><span class="sxs-lookup"><span data-stu-id="c8f5c-107">This notification code is received only through the task dialog callback function, which can be registered using the [**TaskDialogIndirect**](/windows/desktop/api/Commctrl/nf-commctrl-taskdialogindirect) method.</span></span>


```C++
TDN_HELP
        
   WPARAM wParam;
   LPARAM lParam;
```



## <a name="parameters"></a><span data-ttu-id="c8f5c-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c8f5c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c8f5c-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="c8f5c-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c8f5c-110">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="c8f5c-110">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="c8f5c-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="c8f5c-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c8f5c-112">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="c8f5c-112">Must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c8f5c-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="c8f5c-113">Return value</span></span>

<span data-ttu-id="c8f5c-114">La valeur de retour est ignorée.</span><span class="sxs-lookup"><span data-stu-id="c8f5c-114">The return value is ignored.</span></span>

## <a name="requirements"></a><span data-ttu-id="c8f5c-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c8f5c-115">Requirements</span></span>



| <span data-ttu-id="c8f5c-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c8f5c-116">Requirement</span></span> | <span data-ttu-id="c8f5c-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="c8f5c-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c8f5c-118">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c8f5c-118">Minimum supported client</span></span><br/> | <span data-ttu-id="c8f5c-119">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c8f5c-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="c8f5c-120">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c8f5c-120">Minimum supported server</span></span><br/> | <span data-ttu-id="c8f5c-121">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c8f5c-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="c8f5c-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="c8f5c-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="c8f5c-123"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="c8f5c-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





