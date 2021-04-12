---
title: LVN_BEGINSCROLL le code de notification (commctrl. h)
description: Avertit la fenêtre parente d’un contrôle List-View quand une opération de défilement démarre. Ce code de notification est envoyé sous la forme d’un \_ message WM Notify.
ms.assetid: 67123db1-118c-43d7-8511-12a3c4413958
keywords:
- Contrôles Windows de code de notification LVN_BEGINSCROLL
topic_type:
- apiref
api_name:
- LVN_BEGINSCROLL
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ae09a05525ac6e9f08d8cc7a0b7de6ef51329baa
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464406"
---
# <a name="lvn_beginscroll-notification-code"></a><span data-ttu-id="faa7b-105">\_Code de notification LVN BEGINSCROLL</span><span class="sxs-lookup"><span data-stu-id="faa7b-105">LVN\_BEGINSCROLL notification code</span></span>

<span data-ttu-id="faa7b-106">Avertit la fenêtre parente d’un contrôle List-View quand une opération de défilement démarre.</span><span class="sxs-lookup"><span data-stu-id="faa7b-106">Notifies a list-view control's parent window when a scrolling operation starts.</span></span> <span data-ttu-id="faa7b-107">Ce code de notification est envoyé sous la forme d’un message [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="faa7b-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
LVN_BEGINSCROLL

    pnmLVScroll = (LPNMLVSCROLL) lParam;
```



## <a name="parameters"></a><span data-ttu-id="faa7b-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="faa7b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="faa7b-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="faa7b-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="faa7b-110">Pointeur vers une structure [**NMLVSCROLL**](/windows/win32/api/commctrl/ns-commctrl-nmlvscroll) qui contient la position horizontale ou verticale de l’emplacement où l’opération de défilement démarre.</span><span class="sxs-lookup"><span data-stu-id="faa7b-110">Pointer to a [**NMLVSCROLL**](/windows/win32/api/commctrl/ns-commctrl-nmlvscroll) structure that contains the horizontal or vertical position of where the scroll operation starts.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="faa7b-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="faa7b-111">Return value</span></span>

<span data-ttu-id="faa7b-112">Valeur de retour non utilisée.</span><span class="sxs-lookup"><span data-stu-id="faa7b-112">Return value not used.</span></span>

## <a name="remarks"></a><span data-ttu-id="faa7b-113">Notes</span><span class="sxs-lookup"><span data-stu-id="faa7b-113">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="faa7b-114">Pour utiliser ce code de notification, vous devez fournir un manifeste spécifiant Comclt32.dll version 6,0.</span><span class="sxs-lookup"><span data-stu-id="faa7b-114">To use this notification code, you must provide a manifest specifying Comclt32.dll version 6.0.</span></span> <span data-ttu-id="faa7b-115">Pour plus d’informations sur les manifestes, consultez [activation des styles visuels](cookbook-overview.md).</span><span class="sxs-lookup"><span data-stu-id="faa7b-115">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="faa7b-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="faa7b-116">Requirements</span></span>



| <span data-ttu-id="faa7b-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="faa7b-117">Requirement</span></span> | <span data-ttu-id="faa7b-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="faa7b-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="faa7b-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="faa7b-119">Minimum supported client</span></span><br/> | <span data-ttu-id="faa7b-120">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="faa7b-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="faa7b-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="faa7b-121">Minimum supported server</span></span><br/> | <span data-ttu-id="faa7b-122">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="faa7b-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="faa7b-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="faa7b-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="faa7b-124"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="faa7b-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





