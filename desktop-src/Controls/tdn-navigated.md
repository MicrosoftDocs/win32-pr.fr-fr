---
title: TDN_NAVIGATED le code de notification (commctrl. h)
description: Envoyé par une boîte de dialogue de tâche lorsque la navigation s’est produite. Ce code de notification est reçu uniquement par le biais de la fonction de rappel de la boîte de dialogue de tâche, qui peut être inscrite à l’aide de la méthode TaskDialogIndirect.
ms.assetid: e7668ab3-3a11-4bf4-8cb4-067d3204fb3f
keywords:
- Contrôles Windows de code de notification TDN_NAVIGATED
topic_type:
- apiref
api_name:
- TDN_NAVIGATED
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6c9d8e9244889d7e55aad2b89f8ca4bb1c0bb1a1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104509422"
---
# <a name="tdn_navigated-notification-code"></a><span data-ttu-id="335a6-105">\_Code de notification TDN parcouru</span><span class="sxs-lookup"><span data-stu-id="335a6-105">TDN\_NAVIGATED notification code</span></span>

<span data-ttu-id="335a6-106">Envoyé par une boîte de dialogue de tâche lorsque la navigation s’est produite.</span><span class="sxs-lookup"><span data-stu-id="335a6-106">Sent by a task dialog when navigation has occurred.</span></span> <span data-ttu-id="335a6-107">Ce code de notification est reçu uniquement par le biais de la fonction de rappel de la boîte de dialogue de tâche, qui peut être inscrite à l’aide de la méthode [**TaskDialogIndirect**](/windows/desktop/api/Commctrl/nf-commctrl-taskdialogindirect) .</span><span class="sxs-lookup"><span data-stu-id="335a6-107">This notification code is received only through the task dialog callback function, which can be registered using the [**TaskDialogIndirect**](/windows/desktop/api/Commctrl/nf-commctrl-taskdialogindirect) method.</span></span>


```C++
TDN_NAVIGATED
     
   WPARAM wParam;
   LPARAM lParam;
```



## <a name="parameters"></a><span data-ttu-id="335a6-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="335a6-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="335a6-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="335a6-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="335a6-110">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="335a6-110">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="335a6-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="335a6-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="335a6-112">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="335a6-112">Must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="335a6-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="335a6-113">Return value</span></span>

<span data-ttu-id="335a6-114">La valeur de retour est ignorée.</span><span class="sxs-lookup"><span data-stu-id="335a6-114">The return value is ignored.</span></span>

## <a name="requirements"></a><span data-ttu-id="335a6-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="335a6-115">Requirements</span></span>



| <span data-ttu-id="335a6-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="335a6-116">Requirement</span></span> | <span data-ttu-id="335a6-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="335a6-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="335a6-118">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="335a6-118">Minimum supported client</span></span><br/> | <span data-ttu-id="335a6-119">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="335a6-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="335a6-120">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="335a6-120">Minimum supported server</span></span><br/> | <span data-ttu-id="335a6-121">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="335a6-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="335a6-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="335a6-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="335a6-123"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="335a6-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





