---
title: HDN_ITEMCHANGING le code de notification (commctrl. h)
description: Avertit la fenêtre parente d’un contrôle header que les attributs d’un élément d’en-tête sont sur le point d’être modifiés. Ce code de notification est envoyé sous la forme d’un \_ message WM Notify.
ms.assetid: c3361f88-69d4-425f-b548-0ad3b2a00af4
keywords:
- Contrôles Windows de code de notification HDN_ITEMCHANGING
topic_type:
- apiref
api_name:
- HDN_ITEMCHANGING
- HDN_ITEMCHANGINGA
- HDN_ITEMCHANGINGW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c803f9bde466b524b2ca1cb89062f5fc89d6865f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843149"
---
# <a name="hdn_itemchanging-notification-code"></a><span data-ttu-id="57549-105">\_Code de notification HDN ITEMCHANGING</span><span class="sxs-lookup"><span data-stu-id="57549-105">HDN\_ITEMCHANGING notification code</span></span>

<span data-ttu-id="57549-106">Avertit la fenêtre parente d’un contrôle header que les attributs d’un élément d’en-tête sont sur le point d’être modifiés.</span><span class="sxs-lookup"><span data-stu-id="57549-106">Notifies a header control's parent window that the attributes of a header item are about to change.</span></span> <span data-ttu-id="57549-107">Ce code de notification est envoyé sous la forme d’un message [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="57549-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
HDN_ITEMCHANGING

    pNMHeader = (LPNMHEADER) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="57549-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="57549-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="57549-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="57549-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="57549-110">Pointeur vers une structure [**NMHEADER**](/windows/win32/api/commctrl/ns-commctrl-nmheadera) qui contient des informations sur le contrôle header et l’élément d’en-tête, y compris les attributs qui sont sur le point d’être modifiés.</span><span class="sxs-lookup"><span data-stu-id="57549-110">A pointer to an [**NMHEADER**](/windows/win32/api/commctrl/ns-commctrl-nmheadera) structure that contains information about the header control and the header item, including the attributes that are about to change.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="57549-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="57549-111">Return value</span></span>

<span data-ttu-id="57549-112">Retourne **false** pour autoriser les modifications, ou **true** pour les empêcher.</span><span class="sxs-lookup"><span data-stu-id="57549-112">Returns **FALSE** to allow the changes, or **TRUE** to prevent them.</span></span>

## <a name="requirements"></a><span data-ttu-id="57549-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="57549-113">Requirements</span></span>



| <span data-ttu-id="57549-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="57549-114">Requirement</span></span> | <span data-ttu-id="57549-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="57549-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="57549-116">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="57549-116">Minimum supported client</span></span><br/> | <span data-ttu-id="57549-117">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="57549-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="57549-118">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="57549-118">Minimum supported server</span></span><br/> | <span data-ttu-id="57549-119">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="57549-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="57549-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="57549-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="57549-121"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="57549-121"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="57549-122">Noms Unicode et ANSI</span><span class="sxs-lookup"><span data-stu-id="57549-122">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="57549-123">**HDN \_ ITEMCHANGINGW** (Unicode) et **HDN \_ ITEMCHANGINGA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="57549-123">**HDN\_ITEMCHANGINGW** (Unicode) and **HDN\_ITEMCHANGINGA** (ANSI)</span></span><br/>         |



 

 





