---
title: Code de notification NM_RETURN (mode liste) (commctrl. h)
description: Avertit une fenêtre parente d’un contrôle d’affichage de liste que le contrôle a le focus d’entrée et que l’utilisateur a appuyé sur la touche entrée. Ce code de notification est envoyé sous la forme d’un \_ message WM Notify.
ms.assetid: 21a8d308-d747-4020-8925-d982234bcf81
keywords:
- Contrôles Windows de code de notification NM_RETURN (mode liste)
topic_type:
- apiref
api_name:
- NM_RETURN
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9b221189ced0e351f088493f00fa7b8849717668
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942552"
---
# <a name="nm_return-list-view-notification-code"></a><span data-ttu-id="111eb-105">NM \_ retour (mode liste) Code de notification</span><span class="sxs-lookup"><span data-stu-id="111eb-105">NM\_RETURN (list view) notification code</span></span>

<span data-ttu-id="111eb-106">Avertit une fenêtre parente d’un contrôle d’affichage de liste que le contrôle a le focus d’entrée et que l’utilisateur a appuyé sur la touche entrée.</span><span class="sxs-lookup"><span data-stu-id="111eb-106">Notifies a list-view control's parent window that the control has the input focus and that the user has pressed the ENTER key.</span></span> <span data-ttu-id="111eb-107">Ce code de notification est envoyé sous la forme d’un message [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="111eb-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
NM_RETURN 

    lpnmh = (LPNMHDR) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="111eb-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="111eb-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="111eb-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="111eb-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="111eb-110">Pointeur vers une structure [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) qui contient des informations supplémentaires sur cette notification.</span><span class="sxs-lookup"><span data-stu-id="111eb-110">Pointer to an [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure that contains additional information about this notification.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="111eb-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="111eb-111">Return value</span></span>

<span data-ttu-id="111eb-112">La valeur de retour de cette notification n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="111eb-112">The return value for this notification is not used.</span></span>

## <a name="requirements"></a><span data-ttu-id="111eb-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="111eb-113">Requirements</span></span>



| <span data-ttu-id="111eb-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="111eb-114">Requirement</span></span> | <span data-ttu-id="111eb-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="111eb-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="111eb-116">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="111eb-116">Minimum supported client</span></span><br/> | <span data-ttu-id="111eb-117">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="111eb-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="111eb-118">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="111eb-118">Minimum supported server</span></span><br/> | <span data-ttu-id="111eb-119">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="111eb-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="111eb-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="111eb-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="111eb-121"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="111eb-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





