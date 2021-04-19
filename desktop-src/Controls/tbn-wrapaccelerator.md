---
title: TBN_WRAPACCELERATOR le code de notification (commctrl. h)
description: Demande l’index du bouton dans une ou plusieurs barres d’outils correspondant au caractère d’accélérateur spécifié. Ce code de notification est envoyé sous la forme d’un \_ message WM Notify.
ms.assetid: fc2443fd-e1b3-4085-b65d-96c08f544944
keywords:
- Contrôles Windows de code de notification TBN_WRAPACCELERATOR
topic_type:
- apiref
api_name:
- TBN_WRAPACCELERATOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4ed5e6063f8ac32b317b8f7ce37682b151c56a4a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106509088"
---
# <a name="tbn_wrapaccelerator-notification-code"></a><span data-ttu-id="32b6a-105">\_Code de notification TBN WRAPACCELERATOR</span><span class="sxs-lookup"><span data-stu-id="32b6a-105">TBN\_WRAPACCELERATOR notification code</span></span>

<span data-ttu-id="32b6a-106">Demande l’index du bouton dans une ou plusieurs barres d’outils correspondant au caractère d’accélérateur spécifié.</span><span class="sxs-lookup"><span data-stu-id="32b6a-106">Requests the index of the button in one or more toolbars corresponding to the specified accelerator character.</span></span> <span data-ttu-id="32b6a-107">Ce code de notification est envoyé sous la forme d’un message [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="32b6a-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
TBN_WRAPACCELERATOR

    lpnmtb = (NMTBWRAPACCELERATOR) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="32b6a-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="32b6a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="32b6a-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="32b6a-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="32b6a-110">Pointeur vers une structure qui contient le caractère de touche accélérateur et qui reçoit l’index du bouton correspondant.</span><span class="sxs-lookup"><span data-stu-id="32b6a-110">A pointer to a structure that contains the accelerator key character, and that receives the index of the corresponding button.</span></span> <span data-ttu-id="32b6a-111">L’index est-1 si l’accélérateur ne correspond pas à une commande.</span><span class="sxs-lookup"><span data-stu-id="32b6a-111">The index is -1 if the accelerator does not correspond to a command.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="32b6a-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="32b6a-112">Return value</span></span>

<span data-ttu-id="32b6a-113">**True** si un index est retourné ; sinon, **false**.</span><span class="sxs-lookup"><span data-stu-id="32b6a-113">**TRUE** if an index is returned, otherwise **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="32b6a-114">Notes</span><span class="sxs-lookup"><span data-stu-id="32b6a-114">Remarks</span></span>

<span data-ttu-id="32b6a-115">Les applications avec une ou plusieurs barres d’outils peuvent recevoir ce code de notification.</span><span class="sxs-lookup"><span data-stu-id="32b6a-115">Applications with one or more toolbars may receive this notification code.</span></span>

<span data-ttu-id="32b6a-116">La structure **NMTBWRAPACCELERATOR** doit être définie par l’application comme suit :</span><span class="sxs-lookup"><span data-stu-id="32b6a-116">The **NMTBWRAPACCELERATOR** structure must be defined by the application as follows:</span></span>

``` syntax
typedef struct tagNMTBWRAPACCELERATOR {
    NMHDR hdr;
    UINT ch;
    int iButton;
} NMTBWRAPACCELERATOR, *LPNMTBWRAPACCELERATOR;
```

## <a name="requirements"></a><span data-ttu-id="32b6a-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="32b6a-117">Requirements</span></span>



| <span data-ttu-id="32b6a-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="32b6a-118">Requirement</span></span> | <span data-ttu-id="32b6a-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="32b6a-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="32b6a-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="32b6a-120">Minimum supported client</span></span><br/> | <span data-ttu-id="32b6a-121">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="32b6a-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="32b6a-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="32b6a-122">Minimum supported server</span></span><br/> | <span data-ttu-id="32b6a-123">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="32b6a-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="32b6a-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="32b6a-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="32b6a-125"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="32b6a-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





