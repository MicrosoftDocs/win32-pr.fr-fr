---
title: TDN_DESTROYED le code de notification (commctrl. h)
description: Envoyé par une boîte de dialogue de tâche lorsqu’elle est détruite et que son handle de fenêtre n’est plus valide. Ce code de notification est reçu uniquement par le biais de la fonction de rappel de la boîte de dialogue de tâche, qui peut être inscrite à l’aide de la méthode TaskDialogIndirect.
ms.assetid: bbebb77f-e078-46bf-a42d-65dab4f8a972
keywords:
- Contrôles Windows de code de notification TDN_DESTROYED
topic_type:
- apiref
api_name:
- TDN_DESTROYED
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3d3da93435371e696de3d4dce8deeea43926b73b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103844334"
---
# <a name="tdn_destroyed-notification-code"></a><span data-ttu-id="24acc-105">\_Code de notification TDN détruit</span><span class="sxs-lookup"><span data-stu-id="24acc-105">TDN\_DESTROYED notification code</span></span>

<span data-ttu-id="24acc-106">Envoyé par une boîte de dialogue de tâche lorsqu’elle est détruite et que son handle de fenêtre n’est plus valide.</span><span class="sxs-lookup"><span data-stu-id="24acc-106">Sent by a task dialog when it is destroyed and its window handle is no longer valid.</span></span> <span data-ttu-id="24acc-107">Ce code de notification est reçu uniquement par le biais de la fonction de rappel de la boîte de dialogue de tâche, qui peut être inscrite à l’aide de la méthode [**TaskDialogIndirect**](/windows/desktop/api/Commctrl/nf-commctrl-taskdialogindirect) .</span><span class="sxs-lookup"><span data-stu-id="24acc-107">This notification code is received only through the task dialog callback function, which can be registered using the [**TaskDialogIndirect**](/windows/desktop/api/Commctrl/nf-commctrl-taskdialogindirect) method.</span></span>


```C++
TDN_DESTROYED

   WPARAM wParam;
   LPARAM lParam;
```



## <a name="parameters"></a><span data-ttu-id="24acc-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="24acc-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="24acc-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="24acc-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="24acc-110">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="24acc-110">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="24acc-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="24acc-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="24acc-112">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="24acc-112">Must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="24acc-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="24acc-113">Return value</span></span>

<span data-ttu-id="24acc-114">La valeur de retour est ignorée.</span><span class="sxs-lookup"><span data-stu-id="24acc-114">The return value is ignored.</span></span>

## <a name="requirements"></a><span data-ttu-id="24acc-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="24acc-115">Requirements</span></span>



| <span data-ttu-id="24acc-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="24acc-116">Requirement</span></span> | <span data-ttu-id="24acc-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="24acc-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="24acc-118">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="24acc-118">Minimum supported client</span></span><br/> | <span data-ttu-id="24acc-119">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="24acc-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="24acc-120">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="24acc-120">Minimum supported server</span></span><br/> | <span data-ttu-id="24acc-121">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="24acc-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="24acc-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="24acc-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="24acc-123"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="24acc-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





