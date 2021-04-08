---
title: TBN_HOTITEMCHANGE le code de notification (commctrl. h)
description: Envoyé par un contrôle de barre d’outils lorsque l’élément réactif (en surbrillance) change. Ce code de notification est envoyé sous la forme d’un \_ message WM Notify.
ms.assetid: 49e68e2a-d9c0-463d-954d-34c9adfad62b
keywords:
- Contrôles Windows de code de notification TBN_HOTITEMCHANGE
topic_type:
- apiref
api_name:
- TBN_HOTITEMCHANGE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d314a7250128a0f3e6b3fed54e5765487619d8e2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103739892"
---
# <a name="tbn_hotitemchange-notification-code"></a><span data-ttu-id="0c312-105">\_Code de notification TBN HOTITEMCHANGE</span><span class="sxs-lookup"><span data-stu-id="0c312-105">TBN\_HOTITEMCHANGE notification code</span></span>

<span data-ttu-id="0c312-106">Envoyé par un contrôle de barre d’outils lorsque l’élément réactif (en surbrillance) change.</span><span class="sxs-lookup"><span data-stu-id="0c312-106">Sent by a toolbar control when the hot (highlighted) item changes.</span></span> <span data-ttu-id="0c312-107">Ce code de notification est envoyé sous la forme d’un message [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="0c312-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
TBN_HOTITEMCHANGE

    lpnmhi = (LPNMTBHOTITEM) lParam;
```



## <a name="parameters"></a><span data-ttu-id="0c312-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="0c312-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0c312-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="0c312-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="0c312-110">Pointeur vers une structure [**NMTBHOTITEM**](/windows/win32/api/commctrl/ns-commctrl-nmtbhotitem) qui contient des informations sur ce code de notification.</span><span class="sxs-lookup"><span data-stu-id="0c312-110">Pointer to an [**NMTBHOTITEM**](/windows/win32/api/commctrl/ns-commctrl-nmtbhotitem) structure that contains information about this notification code.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0c312-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="0c312-111">Return value</span></span>

<span data-ttu-id="0c312-112">Retourne zéro pour permettre à l’élément d’être mis en surbrillance, ou différent de zéro pour empêcher la mise en surbrillance de l’élément.</span><span class="sxs-lookup"><span data-stu-id="0c312-112">Return zero to allow the item to be highlighted, or nonzero to prevent the item from being highlighted.</span></span>

## <a name="requirements"></a><span data-ttu-id="0c312-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0c312-113">Requirements</span></span>



| <span data-ttu-id="0c312-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0c312-114">Requirement</span></span> | <span data-ttu-id="0c312-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="0c312-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="0c312-116">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0c312-116">Minimum supported client</span></span><br/> | <span data-ttu-id="0c312-117">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="0c312-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="0c312-118">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0c312-118">Minimum supported server</span></span><br/> | <span data-ttu-id="0c312-119">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="0c312-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="0c312-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="0c312-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="0c312-121"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="0c312-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





