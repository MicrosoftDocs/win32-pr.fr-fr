---
title: Valeurs de dessin personnalisées (CommCtrl. h)
description: Cette section répertorie les valeurs utilisées pour identifier les parties d’un contrôle TrackBar.
ms.assetid: 154321c7-99f8-4ed5-a5ff-fb96126b43c7
topic_type:
- apiref
api_name:
- TBCD_CHANNEL
- TBCD_THUMB
- TBCD_TICS
api_location:
- CommCtrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ccf05ab951fdc83ec5be414688be56d710ba0d98
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106537471"
---
# <a name="custom-draw-values"></a><span data-ttu-id="320ce-103">Valeurs de dessin personnalisées</span><span class="sxs-lookup"><span data-stu-id="320ce-103">Custom Draw Values</span></span>

<span data-ttu-id="320ce-104">Cette section répertorie les valeurs utilisées pour identifier les parties d’un contrôle TrackBar.</span><span class="sxs-lookup"><span data-stu-id="320ce-104">This section lists the values used to identify a Trackbar control's parts.</span></span>



| <span data-ttu-id="320ce-105">Constante</span><span class="sxs-lookup"><span data-stu-id="320ce-105">Constant</span></span>                                                                                                                                                   | <span data-ttu-id="320ce-106">Description</span><span class="sxs-lookup"><span data-stu-id="320ce-106">Description</span></span>                                                                                                     |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------|
| <span id="TBCD_CHANNEL"></span><span id="tbcd_channel"></span><dl> <span data-ttu-id="320ce-107"><dt>**\_canal TBCD**</dt></span><span class="sxs-lookup"><span data-stu-id="320ce-107"><dt>**TBCD\_CHANNEL**</dt></span></span> </dl> | <span data-ttu-id="320ce-108">Identifie le canal que le marqueur de curseur de défilement du contrôle TrackBar délimite.</span><span class="sxs-lookup"><span data-stu-id="320ce-108">Identifies the channel that the trackbar control's thumb marker slides along.</span></span><br/>                        |
| <span id="TBCD_THUMB"></span><span id="tbcd_thumb"></span><dl> <span data-ttu-id="320ce-109"><dt>**\_Thumb TBCD**</dt></span><span class="sxs-lookup"><span data-stu-id="320ce-109"><dt>**TBCD\_THUMB**</dt></span></span> </dl>       | <span data-ttu-id="320ce-110">Identifie le marqueur de curseur de défilement du contrôle TrackBar.</span><span class="sxs-lookup"><span data-stu-id="320ce-110">Identifies the trackbar control's thumb marker.</span></span> <span data-ttu-id="320ce-111">Il s’agit de la partie du contrôle que l’utilisateur déplace.</span><span class="sxs-lookup"><span data-stu-id="320ce-111">This is the part of the control that the user moves.</span></span><br/> |
| <span id="TBCD_TICS"></span><span id="tbcd_tics"></span><dl> <span data-ttu-id="320ce-112"><dt>**TBCD \_ tics**</dt></span><span class="sxs-lookup"><span data-stu-id="320ce-112"><dt>**TBCD\_TICS**</dt></span></span> </dl>          | <span data-ttu-id="320ce-113">Identifie les graduations affichées le long du bord du contrôle TrackBar.</span><span class="sxs-lookup"><span data-stu-id="320ce-113">Identifies the tick marks that are displayed along the trackbar control's edge.</span></span><br/>                      |



## <a name="remarks"></a><span data-ttu-id="320ce-114">Notes</span><span class="sxs-lookup"><span data-stu-id="320ce-114">Remarks</span></span>

<span data-ttu-id="320ce-115">Les valeurs de dessin personnalisées, par exemple, sont spécifiées dans le membre **dwItemSpec** de la structure [**NMCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw) .</span><span class="sxs-lookup"><span data-stu-id="320ce-115">Custom Draw values, for example, are specified in the **dwItemSpec** member of the [**NMCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw) structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="320ce-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="320ce-116">Requirements</span></span>



| <span data-ttu-id="320ce-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="320ce-117">Requirement</span></span> | <span data-ttu-id="320ce-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="320ce-118">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="320ce-119">En-tête</span><span class="sxs-lookup"><span data-stu-id="320ce-119">Header</span></span><br/> | <dl> <span data-ttu-id="320ce-120"><dt>CommCtrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="320ce-120"><dt>CommCtrl.h</dt></span></span> </dl> |



 

 





