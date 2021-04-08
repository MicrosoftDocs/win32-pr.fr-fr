---
title: HDN_BEGINFILTEREDIT le code de notification (commctrl. h)
description: Avertit la fenêtre parente d’un contrôle header qu’une modification de filtre a commencé. Ce code de notification est envoyé sous la forme d’un \_ message WM Notify.
ms.assetid: 93964453-bb94-4127-8ed4-41acb226b8e2
keywords:
- Contrôles Windows de code de notification HDN_BEGINFILTEREDIT
topic_type:
- apiref
api_name:
- HDN_BEGINFILTEREDIT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0527427752b5621e626add17d61e60a675958f42
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942930"
---
# <a name="hdn_beginfilteredit-notification-code"></a><span data-ttu-id="a13ed-105">\_Code de notification HDN BEGINFILTEREDIT</span><span class="sxs-lookup"><span data-stu-id="a13ed-105">HDN\_BEGINFILTEREDIT notification code</span></span>

<span data-ttu-id="a13ed-106">Avertit la fenêtre parente d’un contrôle header qu’une modification de filtre a commencé.</span><span class="sxs-lookup"><span data-stu-id="a13ed-106">Notifies a header control's parent window that a filter edit has begun.</span></span> <span data-ttu-id="a13ed-107">Ce code de notification est envoyé sous la forme d’un message [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="a13ed-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
HDN_BEGINFILTEREDIT

   pNMHeader = (LPNMHEADER) lParam;
```



## <a name="parameters"></a><span data-ttu-id="a13ed-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a13ed-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a13ed-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="a13ed-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a13ed-110">Pointeur vers une structure [**NMHEADER**](/windows/win32/api/commctrl/ns-commctrl-nmheadera) qui contient des informations supplémentaires sur le filtre en cours de modification.</span><span class="sxs-lookup"><span data-stu-id="a13ed-110">A pointer to an [**NMHEADER**](/windows/win32/api/commctrl/ns-commctrl-nmheadera) structure that contains additional information about the filter that is being edited.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a13ed-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="a13ed-111">Return value</span></span>

<span data-ttu-id="a13ed-112">Pas de valeur de retour.</span><span class="sxs-lookup"><span data-stu-id="a13ed-112">No return value.</span></span>

## <a name="requirements"></a><span data-ttu-id="a13ed-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a13ed-113">Requirements</span></span>



| <span data-ttu-id="a13ed-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a13ed-114">Requirement</span></span> | <span data-ttu-id="a13ed-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="a13ed-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a13ed-116">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a13ed-116">Minimum supported client</span></span><br/> | <span data-ttu-id="a13ed-117">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a13ed-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="a13ed-118">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a13ed-118">Minimum supported server</span></span><br/> | <span data-ttu-id="a13ed-119">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a13ed-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="a13ed-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="a13ed-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="a13ed-121"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="a13ed-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





