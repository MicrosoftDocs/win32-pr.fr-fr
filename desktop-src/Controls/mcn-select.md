---
title: MCN_SELECT le code de notification (commctrl. h)
description: Envoyé par un contrôle Month Calendar lorsque l’utilisateur effectue une sélection de date explicite dans un contrôle Month Calendar. Ce code de notification est envoyé sous la forme d’un \_ message WM Notify.
ms.assetid: 3cabb4b2-9422-4190-85d3-ab6593891e3d
keywords:
- Contrôles Windows de code de notification MCN_SELECT
topic_type:
- apiref
api_name:
- MCN_SELECT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9252133267b9c552542df17ed73caa8c34a69641
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104032491"
---
# <a name="mcn_select-notification-code"></a><span data-ttu-id="7dc03-105">MCN \_ Sélectionner un code de notification</span><span class="sxs-lookup"><span data-stu-id="7dc03-105">MCN\_SELECT notification code</span></span>

<span data-ttu-id="7dc03-106">Envoyé par un contrôle Month Calendar lorsque l’utilisateur effectue une sélection de date explicite dans un contrôle Month Calendar.</span><span class="sxs-lookup"><span data-stu-id="7dc03-106">Sent by a month calendar control when the user makes an explicit date selection within a month calendar control.</span></span> <span data-ttu-id="7dc03-107">Ce code de notification est envoyé sous la forme d’un message [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="7dc03-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
MCN_SELECT

    lpNMSelChange = (LPNMSELCHANGE) lParam;
```



## <a name="parameters"></a><span data-ttu-id="7dc03-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="7dc03-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7dc03-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="7dc03-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="7dc03-110">Pointeur vers une structure [**NMSELCHANGE**](/windows/win32/api/commctrl/ns-commctrl-nmselchange) qui contient des informations sur la plage de dates actuellement sélectionnée.</span><span class="sxs-lookup"><span data-stu-id="7dc03-110">Pointer to an [**NMSELCHANGE**](/windows/win32/api/commctrl/ns-commctrl-nmselchange) structure that contains information about the currently selected date range.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7dc03-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="7dc03-111">Return value</span></span>

<span data-ttu-id="7dc03-112">Pas de valeur de retour.</span><span class="sxs-lookup"><span data-stu-id="7dc03-112">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="7dc03-113">Notes</span><span class="sxs-lookup"><span data-stu-id="7dc03-113">Remarks</span></span>

<span data-ttu-id="7dc03-114">Le code de notification **\_ Select MCN** est similaire à [**MCN \_ selChange**](mcn-selchange.md), mais **MCN \_ Select** est envoyée uniquement en réponse aux sélections de dates explicites de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="7dc03-114">The **MCN\_SELECT** notification code is similar to [**MCN\_SELCHANGE**](mcn-selchange.md), but **MCN\_SELECT** is sent only in response to a user's explicit date selections.</span></span> <span data-ttu-id="7dc03-115">**MCN \_ SELCHANGE** s’applique à toute modification de sélection.</span><span class="sxs-lookup"><span data-stu-id="7dc03-115">**MCN\_SELCHANGE** applies to any selection change.</span></span>

## <a name="requirements"></a><span data-ttu-id="7dc03-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7dc03-116">Requirements</span></span>



| <span data-ttu-id="7dc03-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7dc03-117">Requirement</span></span> | <span data-ttu-id="7dc03-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="7dc03-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="7dc03-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7dc03-119">Minimum supported client</span></span><br/> | <span data-ttu-id="7dc03-120">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="7dc03-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="7dc03-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7dc03-121">Minimum supported server</span></span><br/> | <span data-ttu-id="7dc03-122">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="7dc03-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="7dc03-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="7dc03-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="7dc03-124"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="7dc03-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





