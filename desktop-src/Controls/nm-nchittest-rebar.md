---
title: Code de notification NM_NCHITTEST (Rebar) (commctrl. h)
description: Envoyé par un contrôle rebar lorsque le contrôle reçoit un \_ message WM NCHITTEST. Ce code de notification est envoyé sous la forme d’un \_ message WM Notify.
ms.assetid: b345d83e-682d-4067-a783-689d64f9b7bc
keywords:
- Contrôles Windows de code de notification NM_NCHITTEST (Rebar)
topic_type:
- apiref
api_name:
- NM_NCHITTEST
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4fb4568cad87017d9fff94deb60583ac0b4c1d0e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105097"
---
# <a name="nm_nchittest-rebar-notification-code"></a><span data-ttu-id="ce742-105">\_Code de notification NCHITTEST nm (Rebar)</span><span class="sxs-lookup"><span data-stu-id="ce742-105">NM\_NCHITTEST (rebar) notification code</span></span>

<span data-ttu-id="ce742-106">Envoyé par un contrôle rebar lorsque le contrôle reçoit un message [**WM \_ NCHITTEST**](/windows/desktop/inputdev/wm-nchittest) .</span><span class="sxs-lookup"><span data-stu-id="ce742-106">Sent by a rebar control when the control receives a [**WM\_NCHITTEST**](/windows/desktop/inputdev/wm-nchittest) message.</span></span> <span data-ttu-id="ce742-107">Ce code de notification est envoyé sous la forme d’un message [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="ce742-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
NM_NCHITTEST

    lpnmmouse = (LPNMMOUSE) lParam;
```



## <a name="parameters"></a><span data-ttu-id="ce742-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ce742-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ce742-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="ce742-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ce742-110">Pointeur vers une structure [**NMMOUSE**](/windows/win32/api/commctrl/ns-commctrl-nmmouse) qui contient des informations sur le code de notification.</span><span class="sxs-lookup"><span data-stu-id="ce742-110">Pointer to an [**NMMOUSE**](/windows/win32/api/commctrl/ns-commctrl-nmmouse) structure that contains information about the notification code.</span></span> <span data-ttu-id="ce742-111">Le membre **dwItemSpec** contient l’index de bande sur lequel le message de test de positionnement s’est produit et le membre **PT** contient les coordonnées de la souris du message de test de positionnement.</span><span class="sxs-lookup"><span data-stu-id="ce742-111">The **dwItemSpec** member contains the band index over which the hit test message occurred, and the **pt** member contains the mouse coordinates of the hit test message.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ce742-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="ce742-112">Return value</span></span>

<span data-ttu-id="ce742-113">Retournez zéro pour permettre au Rebar d’effectuer le traitement par défaut du message de test de positionnement, ou retournez l’une des \* valeurs HT documentées sous [**WM \_ NCHITTEST**](/windows/desktop/inputdev/wm-nchittest) pour remplacer le traitement par défaut du test de positionnement.</span><span class="sxs-lookup"><span data-stu-id="ce742-113">Return zero to allow the rebar to perform default processing of the hit test message, or return one of the HT\* values documented under [**WM\_NCHITTEST**](/windows/desktop/inputdev/wm-nchittest) to override the default hit test processing.</span></span>

## <a name="requirements"></a><span data-ttu-id="ce742-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ce742-114">Requirements</span></span>



| <span data-ttu-id="ce742-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ce742-115">Requirement</span></span> | <span data-ttu-id="ce742-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="ce742-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ce742-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ce742-117">Minimum supported client</span></span><br/> | <span data-ttu-id="ce742-118">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ce742-118">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="ce742-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ce742-119">Minimum supported server</span></span><br/> | <span data-ttu-id="ce742-120">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ce742-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="ce742-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="ce742-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="ce742-122"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="ce742-122"><dt>Commctrl.h</dt></span></span> </dl> |



 

