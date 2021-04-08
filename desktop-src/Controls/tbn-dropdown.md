---
title: TBN_DROPDOWN le code de notification (commctrl. h)
description: Envoyé par un contrôle de barre d’outils lorsque l’utilisateur clique sur un bouton déroulant. Ce code de notification est envoyé sous la forme d’un \_ message WM Notify.
ms.assetid: 85360f74-4b43-4d0a-8c89-22b0741fe96a
keywords:
- Contrôles Windows de code de notification TBN_DROPDOWN
topic_type:
- apiref
api_name:
- TBN_DROPDOWN
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ad7adbb9e0e2ed3d77f8ca8bfb6b09dedd2265be
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103941943"
---
# <a name="tbn_dropdown-notification-code"></a><span data-ttu-id="27928-105">\_Code de notification de liste déroulante TBN</span><span class="sxs-lookup"><span data-stu-id="27928-105">TBN\_DROPDOWN notification code</span></span>

<span data-ttu-id="27928-106">Envoyé par un contrôle de barre d’outils lorsque l’utilisateur clique sur un bouton déroulant.</span><span class="sxs-lookup"><span data-stu-id="27928-106">Sent by a toolbar control when the user clicks a dropdown button.</span></span> <span data-ttu-id="27928-107">Ce code de notification est envoyé sous la forme d’un message [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="27928-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
TBN_DROPDOWN

    lpnmtb = (LPNMTOOLBAR) lParam;
```



## <a name="parameters"></a><span data-ttu-id="27928-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="27928-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="27928-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="27928-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="27928-110">Pointeur vers une structure [**NMTOOLBAR**](/windows/win32/api/commctrl/ns-commctrl-nmtoolbara) qui contient des informations sur ce code de notification.</span><span class="sxs-lookup"><span data-stu-id="27928-110">Pointer to an [**NMTOOLBAR**](/windows/win32/api/commctrl/ns-commctrl-nmtoolbara) structure that contains information about this notification code.</span></span> <span data-ttu-id="27928-111">Pour ce code de notification, seuls les membres **HDR** et **iItem** de cette structure sont valides.</span><span class="sxs-lookup"><span data-stu-id="27928-111">For this notification code, only the **hdr** and **iItem** members of this structure are valid.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="27928-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="27928-112">Return value</span></span>

<span data-ttu-id="27928-113">Renvoie l'une des valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="27928-113">Returns one of the following values:</span></span>



| <span data-ttu-id="27928-114">Code de retour</span><span class="sxs-lookup"><span data-stu-id="27928-114">Return code</span></span>                                                                                          | <span data-ttu-id="27928-115">Description</span><span class="sxs-lookup"><span data-stu-id="27928-115">Description</span></span>                                                                       |
|------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="27928-116"><dt>**TBDDRET \_ par défaut**</dt></span><span class="sxs-lookup"><span data-stu-id="27928-116"><dt>**TBDDRET\_DEFAULT**</dt></span></span> </dl>      | <span data-ttu-id="27928-117">La liste déroulante a été gérée.</span><span class="sxs-lookup"><span data-stu-id="27928-117">The drop-down was handled.</span></span><br/>                                             |
| <dl> <span data-ttu-id="27928-118"><dt>**TBDDRET \_ NOdéfaut**</dt></span><span class="sxs-lookup"><span data-stu-id="27928-118"><dt>**TBDDRET\_NODEFAULT**</dt></span></span> </dl>    | <span data-ttu-id="27928-119">La liste déroulante n’a pas été gérée.</span><span class="sxs-lookup"><span data-stu-id="27928-119">The drop-down was not handled.</span></span><br/>                                         |
| <dl> <span data-ttu-id="27928-120"><dt>**TBDDRET \_ TREATPRESSED**</dt></span><span class="sxs-lookup"><span data-stu-id="27928-120"><dt>**TBDDRET\_TREATPRESSED**</dt></span></span> </dl> | <span data-ttu-id="27928-121">La liste déroulante a été gérée, mais traite le bouton comme un bouton normal.</span><span class="sxs-lookup"><span data-stu-id="27928-121">The drop-down was handled, but treat the button like a regular button.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="27928-122">Notes</span><span class="sxs-lookup"><span data-stu-id="27928-122">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="27928-123">Les boutons déroulants peuvent être bruts (style de [**\_ liste déroulante BTNS**](toolbar-control-and-button-styles.md) ), afficher une flèche en regard de l’image du bouton (style de [**\_ WHOLEDROPDOWN BTNS**](toolbar-control-and-button-styles.md) ) ou afficher une flèche séparée de l’image ([**TBSTYLE \_ ex \_ DRAWDDARROWS**](toolbar-extended-styles.md) style).</span><span class="sxs-lookup"><span data-stu-id="27928-123">Dropdown buttons can be plain ([**BTNS\_DROPDOWN**](toolbar-control-and-button-styles.md) style), display an arrow next to the button image ([**BTNS\_WHOLEDROPDOWN**](toolbar-control-and-button-styles.md) style), or display an arrow that is separated from the image ([**TBSTYLE\_EX\_DRAWDDARROWS**](toolbar-extended-styles.md) style).</span></span> <span data-ttu-id="27928-124">Si une flèche séparée est utilisée, \_ la liste déroulante TBN est envoyée uniquement si l’utilisateur clique sur la partie de flèche du bouton.</span><span class="sxs-lookup"><span data-stu-id="27928-124">If a separated arrow is used, TBN\_DROPDOWN is sent only if the user clicks the arrow portion of the button.</span></span> <span data-ttu-id="27928-125">Si l’utilisateur clique sur la partie principale du bouton, un message de [**\_ commande WM**](/windows/desktop/menurc/wm-command) avec l’ID du bouton est envoyé, comme avec un bouton standard.</span><span class="sxs-lookup"><span data-stu-id="27928-125">If the user clicks the main part of the button, a [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) message with button's ID is sent, just as with a standard button.</span></span> <span data-ttu-id="27928-126">Pour les deux autres styles du bouton déroulant, \_ la liste déroulante TBN est envoyée lorsque l’utilisateur clique sur une partie du bouton.</span><span class="sxs-lookup"><span data-stu-id="27928-126">For the other two styles of dropdown button, TBN\_DROPDOWN is sent when the user clicks any part of the button.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="27928-127">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="27928-127">Requirements</span></span>



| <span data-ttu-id="27928-128">Condition requise</span><span class="sxs-lookup"><span data-stu-id="27928-128">Requirement</span></span> | <span data-ttu-id="27928-129">Valeur</span><span class="sxs-lookup"><span data-stu-id="27928-129">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="27928-130">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="27928-130">Minimum supported client</span></span><br/> | <span data-ttu-id="27928-131">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="27928-131">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="27928-132">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="27928-132">Minimum supported server</span></span><br/> | <span data-ttu-id="27928-133">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="27928-133">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="27928-134">En-tête</span><span class="sxs-lookup"><span data-stu-id="27928-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="27928-135"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="27928-135"><dt>Commctrl.h</dt></span></span> </dl> |



 

