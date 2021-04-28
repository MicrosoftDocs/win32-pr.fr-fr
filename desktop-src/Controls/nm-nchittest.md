---
title: NM_NCHITTEST le code de notification (commctrl. h)
description: NM_NCHITTEST code de notification-envoyé par un contrôle rebar lorsque le contrôle reçoit un \_ message WM NCHITTEST. Ce code de notification est envoyé sous la forme d’un \_ message WM Notify.
ms.assetid: 0e088b14-b912-4f60-9d25-cd0a0ba264c3
keywords:
- Contrôles Windows de code de notification NM_NCHITTEST
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
ms.openlocfilehash: 68ede0ac017fbe5146cd68e51e2a38c7f66c7898
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108112317"
---
# <a name="nm_nchittest-notification-code"></a><span data-ttu-id="834ba-105">\_Code de notification NCHITTEST nm</span><span class="sxs-lookup"><span data-stu-id="834ba-105">NM\_NCHITTEST notification code</span></span>

<span data-ttu-id="834ba-106">Envoyé par un contrôle rebar lorsque le contrôle reçoit un message [**WM \_ NCHITTEST**](/windows/desktop/inputdev/wm-nchittest) .</span><span class="sxs-lookup"><span data-stu-id="834ba-106">Sent by a rebar control when the control receives a [**WM\_NCHITTEST**](/windows/desktop/inputdev/wm-nchittest) message.</span></span> <span data-ttu-id="834ba-107">Ce code de notification est envoyé sous la forme d’un message [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="834ba-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
NM_NCHITTEST
        
    lpnmmouse = (LPNMMOUSE) lParam;
```



## <a name="parameters"></a><span data-ttu-id="834ba-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="834ba-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="834ba-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="834ba-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="834ba-110">Pointeur vers une structure [**NMMOUSE**](/windows/win32/api/commctrl/ns-commctrl-nmmouse) qui contient des informations sur le code de notification.</span><span class="sxs-lookup"><span data-stu-id="834ba-110">A pointer to a [**NMMOUSE**](/windows/win32/api/commctrl/ns-commctrl-nmmouse) structure that contains information about the notification code.</span></span> <span data-ttu-id="834ba-111">Le membre *PT* contient les coordonnées de la souris du message de test de positionnement.</span><span class="sxs-lookup"><span data-stu-id="834ba-111">The *pt* member contains the mouse coordinates of the hit test message.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="834ba-112">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="834ba-112">Return value</span></span>

<span data-ttu-id="834ba-113">Sauf indication contraire, retourne zéro pour permettre au contrôle d’effectuer le traitement par défaut du message de test de positionnement, ou de retourner l’une des \* valeurs HT documentées sous [**WM \_ NCHITTEST**](/windows/desktop/inputdev/wm-nchittest) pour remplacer le traitement par défaut du test de positionnement.</span><span class="sxs-lookup"><span data-stu-id="834ba-113">Unless otherwise specified, return zero to allow the control to perform default processing of the hit test message, or return one of the HT\* values documented under [**WM\_NCHITTEST**](/windows/desktop/inputdev/wm-nchittest) to override the default hit test processing.</span></span>

## <a name="requirements"></a><span data-ttu-id="834ba-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="834ba-114">Requirements</span></span>



| <span data-ttu-id="834ba-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="834ba-115">Requirement</span></span> | <span data-ttu-id="834ba-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="834ba-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="834ba-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="834ba-117">Minimum supported client</span></span><br/> | <span data-ttu-id="834ba-118">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="834ba-118">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="834ba-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="834ba-119">Minimum supported server</span></span><br/> | <span data-ttu-id="834ba-120">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="834ba-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="834ba-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="834ba-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="834ba-122"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="834ba-122"><dt>Commctrl.h</dt></span></span> </dl> |



 

