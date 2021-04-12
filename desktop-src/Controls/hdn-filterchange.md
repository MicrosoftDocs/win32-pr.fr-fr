---
title: HDN_FILTERCHANGE le code de notification (commctrl. h)
description: Notifie la fenêtre parente du contrôle d’en-tête que les attributs d’un filtre de contrôle d’en-tête sont modifiés ou modifiés. Ce code de notification est envoyé sous la forme d’un \_ message WM Notify.
ms.assetid: 0a46af14-569a-4119-881f-549a130f9b0d
keywords:
- Contrôles Windows de code de notification HDN_FILTERCHANGE
topic_type:
- apiref
api_name:
- HDN_FILTERCHANGE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a3d5d31b792e909cd79cdc6aa966bfdce450787b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464415"
---
# <a name="hdn_filterchange-notification-code"></a><span data-ttu-id="bbaf6-105">\_Code de notification HDN FILTERCHANGE</span><span class="sxs-lookup"><span data-stu-id="bbaf6-105">HDN\_FILTERCHANGE notification code</span></span>

<span data-ttu-id="bbaf6-106">Notifie la fenêtre parente du contrôle d’en-tête que les attributs d’un filtre de contrôle d’en-tête sont modifiés ou modifiés.</span><span class="sxs-lookup"><span data-stu-id="bbaf6-106">Notifies the header control's parent window that the attributes of a header control filter are being changed or edited.</span></span> <span data-ttu-id="bbaf6-107">Ce code de notification est envoyé sous la forme d’un message [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="bbaf6-107">This notification code sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
HDN_FILTERCHANGE

    pNMHeader =  (LPNMHEADER) lParam;
```



## <a name="parameters"></a><span data-ttu-id="bbaf6-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="bbaf6-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bbaf6-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="bbaf6-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="bbaf6-110">Pointeur vers une structure [**NMHEADER**](/windows/win32/api/commctrl/ns-commctrl-nmheadera) qui contient des informations sur le contrôle header et l’élément d’en-tête, y compris les attributs qui sont sur le point d’être modifiés.</span><span class="sxs-lookup"><span data-stu-id="bbaf6-110">A pointer to an [**NMHEADER**](/windows/win32/api/commctrl/ns-commctrl-nmheadera) structure that contains information about the header control and the header item, including the attributes that are about to change.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bbaf6-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="bbaf6-111">Return value</span></span>

<span data-ttu-id="bbaf6-112">Pas de valeur de retour.</span><span class="sxs-lookup"><span data-stu-id="bbaf6-112">No return value.</span></span>

## <a name="requirements"></a><span data-ttu-id="bbaf6-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="bbaf6-113">Requirements</span></span>



| <span data-ttu-id="bbaf6-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="bbaf6-114">Requirement</span></span> | <span data-ttu-id="bbaf6-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="bbaf6-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="bbaf6-116">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="bbaf6-116">Minimum supported client</span></span><br/> | <span data-ttu-id="bbaf6-117">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="bbaf6-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="bbaf6-118">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="bbaf6-118">Minimum supported server</span></span><br/> | <span data-ttu-id="bbaf6-119">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="bbaf6-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="bbaf6-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="bbaf6-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="bbaf6-121"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="bbaf6-121"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bbaf6-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="bbaf6-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bbaf6-123">**HDM \_ SETFILTERCHANGETIMEOUT**</span><span class="sxs-lookup"><span data-stu-id="bbaf6-123">**HDM\_SETFILTERCHANGETIMEOUT**</span></span>](hdm-setfilterchangetimeout.md)
</dt> </dl>

 

 





