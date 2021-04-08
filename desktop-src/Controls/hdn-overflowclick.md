---
title: HDN_OVERFLOWCLICK le code de notification (commctrl. h)
description: Envoyé par un contrôle d’en-tête à son parent lorsque l’utilisateur clique sur le bouton de dépassement de capacité de l’en-tête. Ce code de notification est envoyé sous la forme d’un \_ message WM Notify.
ms.assetid: 770ae00a-b87f-4de2-b869-2a233f2c493e
keywords:
- Contrôles Windows de code de notification HDN_OVERFLOWCLICK
topic_type:
- apiref
api_name:
- HDN_OVERFLOWCLICK
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 911953fcbea785cb7024bc9d0670c8ed33239524
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843670"
---
# <a name="hdn_overflowclick-notification-code"></a><span data-ttu-id="42394-105">\_Code de notification HDN OVERFLOWCLICK</span><span class="sxs-lookup"><span data-stu-id="42394-105">HDN\_OVERFLOWCLICK notification code</span></span>

<span data-ttu-id="42394-106">Envoyé par un contrôle d’en-tête à son parent lorsque l’utilisateur clique sur le bouton de dépassement de capacité de l’en-tête.</span><span class="sxs-lookup"><span data-stu-id="42394-106">Sent by a header control to its parent when the header's overflow button is clicked.</span></span> <span data-ttu-id="42394-107">Ce code de notification est envoyé sous la forme d’un message [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="42394-107">This notification code is sent in the form of an [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
HDN_OVERFLOWCLICK

    pNMHeader = (LPNMHEADER) lParam;
```



## <a name="parameters"></a><span data-ttu-id="42394-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="42394-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="42394-109">*lParam* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="42394-109">*lParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="42394-110">Pointeur vers une structure [**NMHEADER**](/windows/win32/api/commctrl/ns-commctrl-nmheadera) qui décrit le code de notification.</span><span class="sxs-lookup"><span data-stu-id="42394-110">A pointer to a [**NMHEADER**](/windows/win32/api/commctrl/ns-commctrl-nmheadera) structure that describes the notification code.</span></span> <span data-ttu-id="42394-111">Le processus appelant est chargé d’allouer cette structure, y compris la structure [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) contenue.</span><span class="sxs-lookup"><span data-stu-id="42394-111">The calling process is responsible for allocating this structure, including the contained [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure.</span></span> <span data-ttu-id="42394-112">Définissez les membres de la structure **NMHDR** , y compris le membre de *code* qui doit être défini sur HDN \_ OVERFLOWCLICK.</span><span class="sxs-lookup"><span data-stu-id="42394-112">Set the members of the **NMHDR** structure, including the *code* member that must be set to HDN\_OVERFLOWCLICK.</span></span>

<span data-ttu-id="42394-113">Définissez le membre **iItem** de la structure [**NMHEADER**](/windows/win32/api/commctrl/ns-commctrl-nmheadera) sur l’index du premier élément d’en-tête qui n’est pas visible et doit donc être affiché sur un dépassement de capacité.</span><span class="sxs-lookup"><span data-stu-id="42394-113">Set the **iItem** member of the [**NMHEADER**](/windows/win32/api/commctrl/ns-commctrl-nmheadera) structure to the index of the first header item that is not visible and thus should be displayed on an overflow.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="42394-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="42394-114">Return value</span></span>

<span data-ttu-id="42394-115">Pas de valeur de retour.</span><span class="sxs-lookup"><span data-stu-id="42394-115">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="42394-116">Notes</span><span class="sxs-lookup"><span data-stu-id="42394-116">Remarks</span></span>

<span data-ttu-id="42394-117">Le récepteur de notification convertit **lParam** pour récupérer la structure [**NMHEADER**](/windows/win32/api/commctrl/ns-commctrl-nmheadera) .</span><span class="sxs-lookup"><span data-stu-id="42394-117">The notification receiver casts **LPARAM** to retrieve the [**NMHEADER**](/windows/win32/api/commctrl/ns-commctrl-nmheadera) structure.</span></span> <span data-ttu-id="42394-118">**WParam** contient l’ID du contrôle qui envoie la notification.</span><span class="sxs-lookup"><span data-stu-id="42394-118">**WPARAM** contains the ID of the control that sends the notification.</span></span>

<span data-ttu-id="42394-119">Ce message est envoyé uniquement lorsque le style de [**\_ dépassement de capacité HDS**](header-control-styles.md) est défini sur le contrôle header.</span><span class="sxs-lookup"><span data-stu-id="42394-119">This message is sent only when style [**HDS\_OVERFLOW**](header-control-styles.md) is set on the header control.</span></span>

## <a name="requirements"></a><span data-ttu-id="42394-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="42394-120">Requirements</span></span>



| <span data-ttu-id="42394-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="42394-121">Requirement</span></span> | <span data-ttu-id="42394-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="42394-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="42394-123">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="42394-123">Minimum supported client</span></span><br/> | <span data-ttu-id="42394-124">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="42394-124">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="42394-125">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="42394-125">Minimum supported server</span></span><br/> | <span data-ttu-id="42394-126">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="42394-126">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="42394-127">En-tête</span><span class="sxs-lookup"><span data-stu-id="42394-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="42394-128"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="42394-128"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





