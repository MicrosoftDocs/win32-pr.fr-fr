---
title: MCN_VIEWCHANGE le code de notification (commctrl. h)
description: Envoyé par un contrôle Month Calendar lorsque l’affichage actuel change. Ce code de notification est envoyé sous la forme d’un \_ message WM Notify.
ms.assetid: ee35ac1d-9aeb-4d75-9cef-016487f23602
keywords:
- Contrôles Windows de code de notification MCN_VIEWCHANGE
topic_type:
- apiref
api_name:
- MCN_VIEWCHANGE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: abbcad3fdda355ac2795dbe49a89fa4e7c2c5cad
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464530"
---
# <a name="mcn_viewchange-notification-code"></a><span data-ttu-id="61218-105">\_Code de notification MCN VIEWCHANGE</span><span class="sxs-lookup"><span data-stu-id="61218-105">MCN\_VIEWCHANGE notification code</span></span>

<span data-ttu-id="61218-106">Envoyé par un contrôle Month Calendar lorsque l’affichage actuel change.</span><span class="sxs-lookup"><span data-stu-id="61218-106">Sent by a month calendar control when the current view changes.</span></span> <span data-ttu-id="61218-107">Ce code de notification est envoyé sous la forme d’un message [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="61218-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
MCN_VIEWCHANGE

    lpNMViewChange = (LPNMVIEWCHANGE) lParam;
```



## <a name="parameters"></a><span data-ttu-id="61218-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="61218-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="61218-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="61218-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="61218-110">Pointeur vers une structure [**NMVIEWCHANGE**](/windows/win32/api/commctrl/ns-commctrl-nmviewchange) qui contient des informations sur la vue actuelle.</span><span class="sxs-lookup"><span data-stu-id="61218-110">Pointer to an [**NMVIEWCHANGE**](/windows/win32/api/commctrl/ns-commctrl-nmviewchange) structure that contains information about the current view.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="61218-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="61218-111">Return value</span></span>

<span data-ttu-id="61218-112">Pas de valeur de retour.</span><span class="sxs-lookup"><span data-stu-id="61218-112">No return value.</span></span>

## <a name="requirements"></a><span data-ttu-id="61218-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="61218-113">Requirements</span></span>



| <span data-ttu-id="61218-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="61218-114">Requirement</span></span> | <span data-ttu-id="61218-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="61218-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="61218-116">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="61218-116">Minimum supported client</span></span><br/> | <span data-ttu-id="61218-117">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="61218-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="61218-118">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="61218-118">Minimum supported server</span></span><br/> | <span data-ttu-id="61218-119">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="61218-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="61218-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="61218-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="61218-121"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="61218-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





