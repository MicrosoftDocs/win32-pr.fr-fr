---
description: Envoyé à toutes les fenêtres de niveau supérieur lorsque le système détecte plus de 12,5% de l’heure système pendant un intervalle de 30 à 60 secondes est consacré au compactage de la mémoire. Cela indique que la mémoire système est insuffisante.
ms.assetid: e8adc655-0252-4a43-8a62-b08e96f5744e
title: Message WM_COMPACTING (winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8fb94e77a1c6b27701b26ed4b7e6e01f326aaa40
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106542959"
---
# <a name="wm_compacting-message"></a><span data-ttu-id="800f6-104">\_Message de compactage WM</span><span class="sxs-lookup"><span data-stu-id="800f6-104">WM\_COMPACTING message</span></span>

<span data-ttu-id="800f6-105">Envoyé à toutes les fenêtres de niveau supérieur lorsque le système détecte plus de 12,5% de l’heure système pendant un intervalle de 30 à 60 secondes est consacré au compactage de la mémoire.</span><span class="sxs-lookup"><span data-stu-id="800f6-105">Sent to all top-level windows when the system detects more than 12.5 percent of system time over a 30- to 60-second interval is being spent compacting memory.</span></span> <span data-ttu-id="800f6-106">Cela indique que la mémoire système est insuffisante.</span><span class="sxs-lookup"><span data-stu-id="800f6-106">This indicates that system memory is low.</span></span>

<span data-ttu-id="800f6-107">Une fenêtre reçoit ce message par le biais de sa fonction [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="800f6-107">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>

> [!Note]  
> <span data-ttu-id="800f6-108">Ce message est fourni uniquement pour la compatibilité avec les applications Windows 16 bits.</span><span class="sxs-lookup"><span data-stu-id="800f6-108">This message is provided only for compatibility with 16-bit Windows-based applications.</span></span>

 


```C++
#define WM_COMPACTING                   0x0041
```



## <a name="parameters"></a><span data-ttu-id="800f6-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="800f6-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="800f6-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="800f6-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="800f6-111">Taux de temps processeur actuellement passé par le système à compacter la mémoire sur le temps processeur actuellement passé par le système effectuant d’autres opérations.</span><span class="sxs-lookup"><span data-stu-id="800f6-111">The ratio of central processing unit (CPU) time currently spent by the system compacting memory to CPU time currently spent by the system performing other operations.</span></span> <span data-ttu-id="800f6-112">Par exemple, 0x8000 représente 50% du temps processeur passé à compacter la mémoire.</span><span class="sxs-lookup"><span data-stu-id="800f6-112">For example, 0x8000 represents 50 percent of CPU time spent compacting memory.</span></span>

</dd> <dt>

<span data-ttu-id="800f6-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="800f6-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="800f6-114">Ce paramètre n'est pas utilisé.</span><span class="sxs-lookup"><span data-stu-id="800f6-114">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="800f6-115">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="800f6-115">Return value</span></span>

<span data-ttu-id="800f6-116">Type : **LRESULT**</span><span class="sxs-lookup"><span data-stu-id="800f6-116">Type: **LRESULT**</span></span>

<span data-ttu-id="800f6-117">Si une application traite ce message, elle doit retourner la valeur zéro.</span><span class="sxs-lookup"><span data-stu-id="800f6-117">If an application processes this message, it should return zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="800f6-118">Notes</span><span class="sxs-lookup"><span data-stu-id="800f6-118">Remarks</span></span>

<span data-ttu-id="800f6-119">Lorsqu’une application reçoit ce message, elle doit libérer autant de mémoire que possible, en tenant compte du niveau actuel d’activité de l’application et du nombre total d’applications en cours d’exécution sur le système.</span><span class="sxs-lookup"><span data-stu-id="800f6-119">When an application receives this message, it should free as much memory as possible, taking into account the current level of activity of the application and the total number of applications running on the system.</span></span>

## <a name="requirements"></a><span data-ttu-id="800f6-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="800f6-120">Requirements</span></span>



| <span data-ttu-id="800f6-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="800f6-121">Requirement</span></span> | <span data-ttu-id="800f6-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="800f6-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="800f6-123">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="800f6-123">Minimum supported client</span></span><br/> | <span data-ttu-id="800f6-124">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="800f6-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="800f6-125">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="800f6-125">Minimum supported server</span></span><br/> | <span data-ttu-id="800f6-126">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="800f6-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="800f6-127">En-tête</span><span class="sxs-lookup"><span data-stu-id="800f6-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="800f6-128"><dt>Winuser. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="800f6-128"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="800f6-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="800f6-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="800f6-130">Vue d’ensemble de Windows</span><span class="sxs-lookup"><span data-stu-id="800f6-130">Windows Overview</span></span>](windows.md)
</dt> </dl>

 

 
