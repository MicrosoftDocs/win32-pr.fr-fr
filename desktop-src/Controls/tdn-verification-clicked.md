---
title: TDN_VERIFICATION_CLICKED le code de notification (commctrl. h)
description: Envoyé par une boîte de dialogue de tâche lorsque l’utilisateur clique sur la case à cocher vérification de la boîte de dialogue des tâches. Ce code de notification est reçu uniquement par le biais de la fonction de rappel de la boîte de dialogue de tâche, qui peut être inscrite à l’aide de la méthode TaskDialogIndirect.
ms.assetid: cd7bc07a-9a70-4361-abfa-986a5a2e13e0
keywords:
- Contrôles Windows de code de notification TDN_VERIFICATION_CLICKED
topic_type:
- apiref
api_name:
- TDN_VERIFICATION_CLICKED
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7887a4d696f5294ebffc6fc6cc7183ff2c0aed8d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942837"
---
# <a name="tdn_verification_clicked-notification-code"></a><span data-ttu-id="0eeed-105">Vérification de TDN \_ \_ sur le code de notification</span><span class="sxs-lookup"><span data-stu-id="0eeed-105">TDN\_VERIFICATION\_CLICKED notification code</span></span>

<span data-ttu-id="0eeed-106">Envoyé par une boîte de dialogue de tâche lorsque l’utilisateur clique sur la case à cocher vérification de la boîte de dialogue des tâches.</span><span class="sxs-lookup"><span data-stu-id="0eeed-106">Sent by a task dialog when the user clicks the task dialog verification check box.</span></span> <span data-ttu-id="0eeed-107">Ce code de notification est reçu uniquement par le biais de la fonction de rappel de la boîte de dialogue de tâche, qui peut être inscrite à l’aide de la méthode [**TaskDialogIndirect**](/windows/desktop/api/Commctrl/nf-commctrl-taskdialogindirect) .</span><span class="sxs-lookup"><span data-stu-id="0eeed-107">This notification code is received only through the task dialog callback function, which can be registered using the [**TaskDialogIndirect**](/windows/desktop/api/Commctrl/nf-commctrl-taskdialogindirect) method.</span></span>


```C++
TDN_VERIFICATION_CLICKED

   WPARAM wParam;
   LPARAM lParam;
```



## <a name="parameters"></a><span data-ttu-id="0eeed-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="0eeed-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0eeed-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="0eeed-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="0eeed-110">Valeur **booléenne** qui spécifie l’état de la case à cocher de vérification.</span><span class="sxs-lookup"><span data-stu-id="0eeed-110">A **BOOL** that specifies the status of the verification checkbox.</span></span> <span data-ttu-id="0eeed-111">La **valeur est true** si la case vérification est cochée, ou **false** si elle est désactivée.</span><span class="sxs-lookup"><span data-stu-id="0eeed-111">It is **TRUE** if the verification checkbox is checked, or **FALSE** if it is unchecked.</span></span>

</dd> <dt>

<span data-ttu-id="0eeed-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="0eeed-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="0eeed-113">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="0eeed-113">Must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0eeed-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="0eeed-114">Return value</span></span>

<span data-ttu-id="0eeed-115">La valeur de retour est ignorée.</span><span class="sxs-lookup"><span data-stu-id="0eeed-115">The return value is ignored.</span></span>

## <a name="requirements"></a><span data-ttu-id="0eeed-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0eeed-116">Requirements</span></span>



| <span data-ttu-id="0eeed-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0eeed-117">Requirement</span></span> | <span data-ttu-id="0eeed-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="0eeed-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="0eeed-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0eeed-119">Minimum supported client</span></span><br/> | <span data-ttu-id="0eeed-120">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="0eeed-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="0eeed-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0eeed-121">Minimum supported server</span></span><br/> | <span data-ttu-id="0eeed-122">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="0eeed-122">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="0eeed-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="0eeed-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="0eeed-124"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="0eeed-124"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0eeed-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0eeed-125">See also</span></span>

<dl> <dt>

<span data-ttu-id="0eeed-126">**Référence**</span><span class="sxs-lookup"><span data-stu-id="0eeed-126">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="0eeed-127">*TaskDialogCallbackProc*</span><span class="sxs-lookup"><span data-stu-id="0eeed-127">*TaskDialogCallbackProc*</span></span>](/windows/win32/api/commctrl/nc-commctrl-pftaskdialogcallback)
</dt> </dl>

 

