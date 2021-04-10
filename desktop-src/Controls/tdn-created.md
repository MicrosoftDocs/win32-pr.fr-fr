---
title: TDN_CREATED le code de notification (commctrl. h)
description: Envoyé par la boîte de dialogue de tâche après la création de la boîte de dialogue et avant son affichage. Ce code de notification est reçu uniquement par le biais de la fonction de rappel de la boîte de dialogue de tâche, qui peut être inscrite à l’aide de la méthode TaskDialogIndirect.
ms.assetid: cfe13db3-9c3c-425c-a6ef-17c5cb33eeb6
keywords:
- Contrôles Windows de code de notification TDN_CREATED
topic_type:
- apiref
api_name:
- TDN_CREATED
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a25aa40af6b2cb002f2da7aab7c71fd68702ae65
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942843"
---
# <a name="tdn_created-notification-code"></a><span data-ttu-id="4a41e-105">\_Code de notification créé par TDN</span><span class="sxs-lookup"><span data-stu-id="4a41e-105">TDN\_CREATED notification code</span></span>

<span data-ttu-id="4a41e-106">Envoyé par la boîte de dialogue de tâche après la création de la boîte de dialogue et avant son affichage.</span><span class="sxs-lookup"><span data-stu-id="4a41e-106">Sent by the task dialog after the dialog has been created and before it is displayed.</span></span> <span data-ttu-id="4a41e-107">Ce code de notification est reçu uniquement par le biais de la fonction de rappel de la boîte de dialogue de tâche, qui peut être inscrite à l’aide de la méthode [**TaskDialogIndirect**](/windows/desktop/api/Commctrl/nf-commctrl-taskdialogindirect) .</span><span class="sxs-lookup"><span data-stu-id="4a41e-107">This notification code is received only through the task dialog callback function, which can be registered using the [**TaskDialogIndirect**](/windows/desktop/api/Commctrl/nf-commctrl-taskdialogindirect) method.</span></span>


```C++
TDN_CREATED
     
   WPARAM wParam;
   LPARAM lParam;
```



## <a name="parameters"></a><span data-ttu-id="4a41e-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="4a41e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4a41e-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="4a41e-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="4a41e-110">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="4a41e-110">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="4a41e-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="4a41e-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="4a41e-112">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="4a41e-112">Must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4a41e-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="4a41e-113">Return value</span></span>

<span data-ttu-id="4a41e-114">La valeur de retour est ignorée.</span><span class="sxs-lookup"><span data-stu-id="4a41e-114">The return value is ignored.</span></span>

## <a name="requirements"></a><span data-ttu-id="4a41e-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="4a41e-115">Requirements</span></span>



| <span data-ttu-id="4a41e-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="4a41e-116">Requirement</span></span> | <span data-ttu-id="4a41e-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="4a41e-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="4a41e-118">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4a41e-118">Minimum supported client</span></span><br/> | <span data-ttu-id="4a41e-119">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="4a41e-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="4a41e-120">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4a41e-120">Minimum supported server</span></span><br/> | <span data-ttu-id="4a41e-121">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="4a41e-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="4a41e-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="4a41e-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="4a41e-123"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="4a41e-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





