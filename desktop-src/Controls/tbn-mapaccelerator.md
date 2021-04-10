---
title: TBN_MAPACCELERATOR le code de notification (commctrl. h)
description: Demande l’index du bouton dans la barre d’outils correspondant au caractère d’accélérateur spécifié. Ce code de notification est envoyé sous la forme d’un \_ message WM Notify.
ms.assetid: 16d16560-62ef-4457-bf8c-bc6dddb520d7
keywords:
- Contrôles Windows de code de notification TBN_MAPACCELERATOR
topic_type:
- apiref
api_name:
- TBN_MAPACCELERATOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d4b20f1908f441c38e23aa7428f8c8edb8a192c7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103941659"
---
# <a name="tbn_mapaccelerator-notification-code"></a><span data-ttu-id="1cde1-105">\_Code de notification TBN MAPACCELERATOR</span><span class="sxs-lookup"><span data-stu-id="1cde1-105">TBN\_MAPACCELERATOR notification code</span></span>

<span data-ttu-id="1cde1-106">Demande l’index du bouton dans la barre d’outils correspondant au caractère d’accélérateur spécifié.</span><span class="sxs-lookup"><span data-stu-id="1cde1-106">Requests the index of the button in the toolbar corresponding to the specified accelerator character.</span></span> <span data-ttu-id="1cde1-107">Ce code de notification est envoyé sous la forme d’un message [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="1cde1-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
TBN_MAPACCELERATOR

    lpnmtb = (NMCHAR*) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="1cde1-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="1cde1-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1cde1-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="1cde1-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1cde1-110">Pointeur vers une structure [**NMCHAR**](/windows/win32/api/commctrl/ns-commctrl-nmchar) qui contient le caractère de touche accélérateur et qui reçoit l’index du bouton correspondant.</span><span class="sxs-lookup"><span data-stu-id="1cde1-110">A pointer to an [**NMCHAR**](/windows/win32/api/commctrl/ns-commctrl-nmchar) structure that contains the accelerator key character and that receives the index of the corresponding button.</span></span> <span data-ttu-id="1cde1-111">Le champ **dwItemNext** a la valeur-1 si l’accélérateur ne correspond pas à une commande.</span><span class="sxs-lookup"><span data-stu-id="1cde1-111">The **dwItemNext** field is -1 if the accelerator does not correspond to a command.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1cde1-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="1cde1-112">Return value</span></span>

<span data-ttu-id="1cde1-113">TRUE si **NMCHAR. dwItemNext** est défini sur une valeur.</span><span class="sxs-lookup"><span data-stu-id="1cde1-113">TRUE if **NMCHAR.dwItemNext** is set to a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="1cde1-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1cde1-114">Requirements</span></span>



| <span data-ttu-id="1cde1-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1cde1-115">Requirement</span></span> | <span data-ttu-id="1cde1-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="1cde1-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="1cde1-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1cde1-117">Minimum supported client</span></span><br/> | <span data-ttu-id="1cde1-118">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="1cde1-118">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="1cde1-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1cde1-119">Minimum supported server</span></span><br/> | <span data-ttu-id="1cde1-120">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="1cde1-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="1cde1-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="1cde1-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="1cde1-122"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="1cde1-122"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





