---
title: Message TTM_HITTEST (commctrl. h)
description: Teste un point pour déterminer s’il se trouve dans le rectangle englobant de l’outil spécifié et, si c’est le cas, récupère des informations sur l’outil.
ms.assetid: d4dcc29b-c64c-41b8-a153-300df68ecdf5
keywords:
- TTM_HITTEST les contrôles de message Windows
topic_type:
- apiref
api_name:
- TTM_HITTEST
- TTM_HITTESTA
- TTM_HITTESTW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f7b515ccb5c283b66760f24c02749368e424e6fe
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465351"
---
# <a name="ttm_hittest-message"></a><span data-ttu-id="aa65a-104">\_Message atténuation HITTEST</span><span class="sxs-lookup"><span data-stu-id="aa65a-104">TTM\_HITTEST message</span></span>

<span data-ttu-id="aa65a-105">Teste un point pour déterminer s’il se trouve dans le rectangle englobant de l’outil spécifié et, si c’est le cas, récupère des informations sur l’outil.</span><span class="sxs-lookup"><span data-stu-id="aa65a-105">Tests a point to determine whether it is within the bounding rectangle of the specified tool and, if it is, retrieves information about the tool.</span></span>

## <a name="parameters"></a><span data-ttu-id="aa65a-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="aa65a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="aa65a-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="aa65a-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="aa65a-108">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="aa65a-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="aa65a-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="aa65a-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="aa65a-110">Pointeur vers une structure [**TTHITTESTINFO**](/windows/win32/api/commctrl/ns-commctrl-tthittestinfoa) .</span><span class="sxs-lookup"><span data-stu-id="aa65a-110">Pointer to a [**TTHITTESTINFO**](/windows/win32/api/commctrl/ns-commctrl-tthittestinfoa) structure.</span></span> <span data-ttu-id="aa65a-111">Lors de l’envoi du message, le membre **HWND** doit spécifier le descripteur d’un outil et le membre **PT** doit spécifier les coordonnées d’un point.</span><span class="sxs-lookup"><span data-stu-id="aa65a-111">When sending the message, the **hwnd** member must specify the handle to a tool and the **pt** member must specify the coordinates of a point.</span></span> <span data-ttu-id="aa65a-112">Si la valeur de retour est **true**, le membre **TI** (une structure [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) ) reçoit des informations sur l’outil qui occupe le point.</span><span class="sxs-lookup"><span data-stu-id="aa65a-112">If the return value is **TRUE**, the **ti** member (a [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) structure) receives information about the tool that occupies the point.</span></span> <span data-ttu-id="aa65a-113">Le membre **cbSize** de la structure **TI** doit être rempli avant l’envoi de ce message.</span><span class="sxs-lookup"><span data-stu-id="aa65a-113">The **cbSize** member of the **ti** structure must be filled in before sending this message.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="aa65a-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="aa65a-114">Return value</span></span>

<span data-ttu-id="aa65a-115">Retourne la **valeur true** si l’outil occupe le point spécifié, ou **false** dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="aa65a-115">Returns **TRUE** if the tool occupies the specified point, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="aa65a-116">Notes</span><span class="sxs-lookup"><span data-stu-id="aa65a-116">Remarks</span></span>

<span data-ttu-id="aa65a-117">Ce message doit être envoyé lorsque l’indicateur de piste TTF est défini pour l’outil \_ .</span><span class="sxs-lookup"><span data-stu-id="aa65a-117">This message must be sent when the tool has the TTF\_TRACK flag set.</span></span> <span data-ttu-id="aa65a-118">Pour plus d’informations sur cet indicateur, consultez [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa).</span><span class="sxs-lookup"><span data-stu-id="aa65a-118">For more information on this flag, see [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa).</span></span> <span data-ttu-id="aa65a-119">ATTÉNUATION \_ HITTEST échoue si \_ la piste ttf n’est pas définie, même si le point d’accès se trouve dans le rectangle d’outils.</span><span class="sxs-lookup"><span data-stu-id="aa65a-119">TTM\_HITTEST will fail if TTF\_TRACK is not set, regardless if the hit point is in the tools rectangle or not.</span></span>

## <a name="requirements"></a><span data-ttu-id="aa65a-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="aa65a-120">Requirements</span></span>



| <span data-ttu-id="aa65a-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="aa65a-121">Requirement</span></span> | <span data-ttu-id="aa65a-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="aa65a-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="aa65a-123">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="aa65a-123">Minimum supported client</span></span><br/> | <span data-ttu-id="aa65a-124">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="aa65a-124">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="aa65a-125">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="aa65a-125">Minimum supported server</span></span><br/> | <span data-ttu-id="aa65a-126">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="aa65a-126">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="aa65a-127">En-tête</span><span class="sxs-lookup"><span data-stu-id="aa65a-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="aa65a-128"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="aa65a-128"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="aa65a-129">Noms Unicode et ANSI</span><span class="sxs-lookup"><span data-stu-id="aa65a-129">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="aa65a-130">**Atténuation \_ HITTESTW** (Unicode) et **atténuation \_ HITTESTA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="aa65a-130">**TTM\_HITTESTW** (Unicode) and **TTM\_HITTESTA** (ANSI)</span></span><br/>                   |



 

 





