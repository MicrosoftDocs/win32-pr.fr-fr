---
title: TDN_DIALOG_CONSTRUCTED le code de notification (commctrl. h)
description: Envoyé par une boîte de dialogue de tâche après la création de la boîte de dialogue et avant son affichage. Ce code de notification est reçu uniquement par le biais de la fonction de rappel de la boîte de dialogue de tâche, qui peut être inscrite à l’aide de la méthode TaskDialogIndirect.
ms.assetid: e8556039-a74d-4e33-931d-a63ad5b2d4b0
keywords:
- Contrôles Windows de code de notification TDN_DIALOG_CONSTRUCTED
topic_type:
- apiref
api_name:
- TDN_DIALOG_CONSTRUCTED
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c8d3360a8cee3542037ea927363de8cab69977e5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942841"
---
# <a name="tdn_dialog_constructed-notification-code"></a><span data-ttu-id="29ecc-105">Code de notification de la \_ boîte de dialogue TDN \_</span><span class="sxs-lookup"><span data-stu-id="29ecc-105">TDN\_DIALOG\_CONSTRUCTED notification code</span></span>

<span data-ttu-id="29ecc-106">Envoyé par une boîte de dialogue de tâche après la création de la boîte de dialogue et avant son affichage.</span><span class="sxs-lookup"><span data-stu-id="29ecc-106">Sent by a task dialog after the dialog has been created and before it is displayed.</span></span> <span data-ttu-id="29ecc-107">Ce code de notification est reçu uniquement par le biais de la fonction de rappel de la boîte de dialogue de tâche, qui peut être inscrite à l’aide de la méthode [**TaskDialogIndirect**](/windows/desktop/api/Commctrl/nf-commctrl-taskdialogindirect) .</span><span class="sxs-lookup"><span data-stu-id="29ecc-107">This notification code is received only through the task dialog callback function, which can be registered using the [**TaskDialogIndirect**](/windows/desktop/api/Commctrl/nf-commctrl-taskdialogindirect) method.</span></span>


```C++
TDN_DIALOG_CONSTRUCTED
     
   WPARAM wParam;
   LPARAM lParam;
```



## <a name="parameters"></a><span data-ttu-id="29ecc-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="29ecc-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="29ecc-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="29ecc-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="29ecc-110">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="29ecc-110">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="29ecc-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="29ecc-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="29ecc-112">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="29ecc-112">Must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="29ecc-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="29ecc-113">Return value</span></span>

<span data-ttu-id="29ecc-114">La valeur de retour est ignorée.</span><span class="sxs-lookup"><span data-stu-id="29ecc-114">The return value is ignored.</span></span>

## <a name="requirements"></a><span data-ttu-id="29ecc-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="29ecc-115">Requirements</span></span>



| <span data-ttu-id="29ecc-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="29ecc-116">Requirement</span></span> | <span data-ttu-id="29ecc-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="29ecc-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="29ecc-118">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="29ecc-118">Minimum supported client</span></span><br/> | <span data-ttu-id="29ecc-119">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="29ecc-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="29ecc-120">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="29ecc-120">Minimum supported server</span></span><br/> | <span data-ttu-id="29ecc-121">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="29ecc-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="29ecc-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="29ecc-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="29ecc-123"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="29ecc-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





