---
title: HDN_DIVIDERDBLCLICK le code de notification (commctrl. h)
description: Avertit la fenêtre parente d’un contrôle header que l’utilisateur a double-cliqué sur la zone de séparation du contrôle. Ce code de notification est envoyé sous la forme d’un \_ message WM Notify.
ms.assetid: b722196a-23ae-49c3-b0a2-8fe0d1e33b26
keywords:
- Contrôles Windows de code de notification HDN_DIVIDERDBLCLICK
topic_type:
- apiref
api_name:
- HDN_DIVIDERDBLCLICK
- HDN_DIVIDERDBLCLICKA
- HDN_DIVIDERDBLCLICKW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0129096139a4d698f25de543a2628b473bfd66e2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104033272"
---
# <a name="hdn_dividerdblclick-notification-code"></a><span data-ttu-id="ebdb6-105">\_Code de notification HDN DIVIDERDBLCLICK</span><span class="sxs-lookup"><span data-stu-id="ebdb6-105">HDN\_DIVIDERDBLCLICK notification code</span></span>

<span data-ttu-id="ebdb6-106">Avertit la fenêtre parente d’un contrôle header que l’utilisateur a double-cliqué sur la zone de séparation du contrôle.</span><span class="sxs-lookup"><span data-stu-id="ebdb6-106">Notifies a header control's parent window that the user double-clicked the divider area of the control.</span></span> <span data-ttu-id="ebdb6-107">Ce code de notification est envoyé sous la forme d’un message [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="ebdb6-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
HDN_DIVIDERDBLCLICK

    pNMHeader = (LPNMHEADER) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="ebdb6-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ebdb6-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ebdb6-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="ebdb6-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ebdb6-110">Pointeur vers une structure [**NMHEADER**](/windows/win32/api/commctrl/ns-commctrl-nmheadera) qui contient des informations sur le contrôle header et l’élément sur lequel l’utilisateur a double-cliqué sur le séparateur.</span><span class="sxs-lookup"><span data-stu-id="ebdb6-110">A pointer to an [**NMHEADER**](/windows/win32/api/commctrl/ns-commctrl-nmheadera) structure that contains information about the header control and the item whose divider was double-clicked.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ebdb6-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="ebdb6-111">Return value</span></span>

<span data-ttu-id="ebdb6-112">Pas de valeur de retour.</span><span class="sxs-lookup"><span data-stu-id="ebdb6-112">No return value.</span></span>

## <a name="requirements"></a><span data-ttu-id="ebdb6-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ebdb6-113">Requirements</span></span>



| <span data-ttu-id="ebdb6-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ebdb6-114">Requirement</span></span> | <span data-ttu-id="ebdb6-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="ebdb6-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ebdb6-116">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ebdb6-116">Minimum supported client</span></span><br/> | <span data-ttu-id="ebdb6-117">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ebdb6-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="ebdb6-118">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ebdb6-118">Minimum supported server</span></span><br/> | <span data-ttu-id="ebdb6-119">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ebdb6-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="ebdb6-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="ebdb6-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="ebdb6-121"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="ebdb6-121"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="ebdb6-122">Noms Unicode et ANSI</span><span class="sxs-lookup"><span data-stu-id="ebdb6-122">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="ebdb6-123">**HDN \_ DIVIDERDBLCLICKW** (Unicode) et **HDN \_ DIVIDERDBLCLICKA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="ebdb6-123">**HDN\_DIVIDERDBLCLICKW** (Unicode) and **HDN\_DIVIDERDBLCLICKA** (ANSI)</span></span><br/>   |



 

 





