---
title: LVN_GETINFOTIP le code de notification (commctrl. h)
description: Envoyé par une grande icône Afficher le contrôle List-View avec le \_ \_ style étendu LVS ex info-bulle.
ms.assetid: 62be5087-7e49-4722-a63a-1768e030af48
keywords:
- Contrôles Windows de code de notification LVN_GETINFOTIP
topic_type:
- apiref
api_name:
- LVN_GETINFOTIP
- LVN_GETINFOTIPA
- LVN_GETINFOTIPW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c2b4552456a575e2f03e02b2bfb78f7fcc1d8ca1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104519329"
---
# <a name="lvn_getinfotip-notification-code"></a><span data-ttu-id="77a3c-104">\_Code de notification LVN GETINFOTIP</span><span class="sxs-lookup"><span data-stu-id="77a3c-104">LVN\_GETINFOTIP notification code</span></span>

<span data-ttu-id="77a3c-105">Envoyé par une grande icône Afficher le contrôle List-View avec le style étendu [**LVS \_ ex \_ info-bulle**](extended-list-view-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="77a3c-105">Sent by a large icon view list-view control that has the [**LVS\_EX\_INFOTIP**](extended-list-view-styles.md) extended style.</span></span> <span data-ttu-id="77a3c-106">Ce code de notification est envoyé lorsque le contrôle List-View demande des informations de texte supplémentaires à afficher dans une info-bulle.</span><span class="sxs-lookup"><span data-stu-id="77a3c-106">This notification code is sent when the list-view control is requesting additional text information to be displayed in a tooltip.</span></span> <span data-ttu-id="77a3c-107">Il est envoyé sous la forme d’un message [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="77a3c-107">It is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
LVN_GETINFOTIP

    pGetInfoTip = (LPNMLVGETINFOTIP) lParam;
```



## <a name="parameters"></a><span data-ttu-id="77a3c-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="77a3c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="77a3c-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="77a3c-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="77a3c-110">Pointeur vers une structure [**NMLVGETINFOTIP**](/windows/win32/api/commctrl/ns-commctrl-nmlvgetinfotipa) qui contient des informations sur ce code de notification.</span><span class="sxs-lookup"><span data-stu-id="77a3c-110">Pointer to an [**NMLVGETINFOTIP**](/windows/win32/api/commctrl/ns-commctrl-nmlvgetinfotipa) structure that contains information about this notification code.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="77a3c-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="77a3c-111">Return value</span></span>

<span data-ttu-id="77a3c-112">La valeur de retour de cette notification n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="77a3c-112">The return value for this notification is not used.</span></span>

## <a name="remarks"></a><span data-ttu-id="77a3c-113">Notes</span><span class="sxs-lookup"><span data-stu-id="77a3c-113">Remarks</span></span>

<span data-ttu-id="77a3c-114">Ce code de notification est uniquement envoyé par les contrôles List-View qui ont le style étendu [**LVS \_ ex \_ info-bulle**](extended-list-view-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="77a3c-114">This notification code is only sent by list-view controls that have the [**LVS\_EX\_INFOTIP**](extended-list-view-styles.md) extended style.</span></span> <span data-ttu-id="77a3c-115">Le \_ Code de notification LVN GETINFOTIP est envoyé uniquement pour le sous-élément 0.</span><span class="sxs-lookup"><span data-stu-id="77a3c-115">The LVN\_GETINFOTIP notification code is sent only for subitem 0.</span></span>

## <a name="requirements"></a><span data-ttu-id="77a3c-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="77a3c-116">Requirements</span></span>



| <span data-ttu-id="77a3c-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="77a3c-117">Requirement</span></span> | <span data-ttu-id="77a3c-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="77a3c-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="77a3c-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="77a3c-119">Minimum supported client</span></span><br/> | <span data-ttu-id="77a3c-120">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="77a3c-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="77a3c-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="77a3c-121">Minimum supported server</span></span><br/> | <span data-ttu-id="77a3c-122">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="77a3c-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="77a3c-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="77a3c-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="77a3c-124"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="77a3c-124"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="77a3c-125">Noms Unicode et ANSI</span><span class="sxs-lookup"><span data-stu-id="77a3c-125">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="77a3c-126">**LVN \_ GETINFOTIPW** (Unicode) et **LVN \_ GETINFOTIPA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="77a3c-126">**LVN\_GETINFOTIPW** (Unicode) and **LVN\_GETINFOTIPA** (ANSI)</span></span><br/>             |



 

 





