---
title: HDN_FILTERBTNCLICK le code de notification (commctrl. h)
description: Notifie la fenêtre parente du contrôle header lorsque l’utilisateur clique sur le bouton de filtre ou en réponse à un \_ message HDM SETITEM. Ce code de notification est envoyé sous la forme d’un \_ message WM Notify.
ms.assetid: 36b85cdc-1022-4568-8891-0c919c850fd4
keywords:
- Contrôles Windows de code de notification HDN_FILTERBTNCLICK
topic_type:
- apiref
api_name:
- HDN_FILTERBTNCLICK
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c3dbbdab8adf0bee400d591f3d8b4cec6fa1ea81
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843150"
---
# <a name="hdn_filterbtnclick-notification-code"></a><span data-ttu-id="7cae2-105">\_Code de notification HDN FILTERBTNCLICK</span><span class="sxs-lookup"><span data-stu-id="7cae2-105">HDN\_FILTERBTNCLICK notification code</span></span>

<span data-ttu-id="7cae2-106">Notifie la fenêtre parente du contrôle header lorsque l’utilisateur clique sur le bouton de filtre ou en réponse à un message [**HDM \_ SETITEM**](hdm-setitem.md) .</span><span class="sxs-lookup"><span data-stu-id="7cae2-106">Notifies the header control's parent window when the filter button is clicked or in response to an [**HDM\_SETITEM**](hdm-setitem.md) message.</span></span> <span data-ttu-id="7cae2-107">Ce code de notification est envoyé sous la forme d’un message [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="7cae2-107">This notification code sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
HDN_FILTERBTNCLICK

    pNMHDFilterBtnClk = (LPNMHDFILTERBTNCLICK) lParam;
```



## <a name="parameters"></a><span data-ttu-id="7cae2-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="7cae2-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7cae2-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="7cae2-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="7cae2-110">Pointeur vers une structure [**NMHDFILTERBTNCLICK**](/windows/win32/api/commctrl/ns-commctrl-nmhdfilterbtnclick) qui contient des informations sur le contrôle header et le bouton de filtre d’en-tête.</span><span class="sxs-lookup"><span data-stu-id="7cae2-110">A pointer to an [**NMHDFILTERBTNCLICK**](/windows/win32/api/commctrl/ns-commctrl-nmhdfilterbtnclick) structure that contains information about the header control and the header filter button.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7cae2-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="7cae2-111">Return value</span></span>

<span data-ttu-id="7cae2-112">Si vous renvoyez la **valeur true**, un code de notification [HDN \_ FILTERCHANGE](hdn-filterchange.md) sera envoyé à la fenêtre parente du contrôle d’en-tête.</span><span class="sxs-lookup"><span data-stu-id="7cae2-112">If you return **TRUE**, an [HDN\_FILTERCHANGE](hdn-filterchange.md) notification code will be sent to the header control's parent window.</span></span> <span data-ttu-id="7cae2-113">Ce code de notification donne à la fenêtre parente la possibilité de synchroniser ses éléments d’interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="7cae2-113">This notification code gives the parent window an opportunity to synchronize its user interface elements.</span></span> <span data-ttu-id="7cae2-114">Retourne la **valeur false** si vous ne souhaitez pas envoyer la notification.</span><span class="sxs-lookup"><span data-stu-id="7cae2-114">Return **FALSE** if you do not want the notification sent.</span></span>

## <a name="requirements"></a><span data-ttu-id="7cae2-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7cae2-115">Requirements</span></span>



| <span data-ttu-id="7cae2-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7cae2-116">Requirement</span></span> | <span data-ttu-id="7cae2-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="7cae2-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="7cae2-118">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7cae2-118">Minimum supported client</span></span><br/> | <span data-ttu-id="7cae2-119">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="7cae2-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="7cae2-120">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7cae2-120">Minimum supported server</span></span><br/> | <span data-ttu-id="7cae2-121">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="7cae2-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="7cae2-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="7cae2-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="7cae2-123"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="7cae2-123"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7cae2-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7cae2-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7cae2-125">**NMHDFILTERBTNCLICK**</span><span class="sxs-lookup"><span data-stu-id="7cae2-125">**NMHDFILTERBTNCLICK**</span></span>](/windows/win32/api/commctrl/ns-commctrl-nmhdfilterbtnclick)
</dt> </dl>

 

 





