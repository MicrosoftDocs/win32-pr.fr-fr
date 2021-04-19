---
title: Styles de contrôle de barre de progression (CommCtrl. h)
description: Les styles de contrôle suivants sont pris en charge par les contrôles de barre de progression
ms.assetid: bd89aa74-c15e-4745-8b2b-7cbd8b28c1c8
topic_type:
- apiref
api_name:
- PBS_MARQUEE
- PBS_SMOOTH
- PBS_SMOOTHREVERSE
- PBS_VERTICAL
api_location:
- CommCtrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d55ec928fb1ee2715576f3131dde0f661a91fcf8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106523603"
---
# <a name="progress-bar-control-styles"></a><span data-ttu-id="3465d-103">Styles de contrôle de barre de progression</span><span class="sxs-lookup"><span data-stu-id="3465d-103">Progress Bar Control Styles</span></span>

<span data-ttu-id="3465d-104">Les styles de contrôle suivants sont pris en charge par les contrôles de [barre de progression](progress-bar-control.md) :</span><span class="sxs-lookup"><span data-stu-id="3465d-104">The following control styles are supported by [Progress Bar](progress-bar-control.md) controls:</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;"><span data-ttu-id="3465d-105">Constante</span><span class="sxs-lookup"><span data-stu-id="3465d-105">Constant</span></span></th>
<th style="text-align: left;"><span data-ttu-id="3465d-106">Description</span><span class="sxs-lookup"><span data-stu-id="3465d-106">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span id="PBS_MARQUEE"></span><span id="pbs_marquee"></span><dl> <span data-ttu-id="3465d-107"><dt><strong>PBS_MARQUEE</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="3465d-107"><dt><strong>PBS_MARQUEE</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="3465d-108"><a href="common-control-versions.md">Version 6,0</a> ou ultérieure.</span><span class="sxs-lookup"><span data-stu-id="3465d-108"><a href="common-control-versions.md">Version 6.0</a> or later.</span></span> <span data-ttu-id="3465d-109">La taille de l’indicateur de progression n’augmente pas, mais se déplace à plusieurs reprises le long de la longueur de la barre, ce qui indique l’activité sans spécifier quelle proportion de la progression est terminée.</span><span class="sxs-lookup"><span data-stu-id="3465d-109">The progress indicator does not grow in size but instead moves repeatedly along the length of the bar, indicating activity without specifying what proportion of the progress is complete.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="3465d-110">Comctl32.dll version 6 n’est pas redistribuable, mais elle est incluse dans Windows ou version ultérieure.</span><span class="sxs-lookup"><span data-stu-id="3465d-110">Comctl32.dll version 6 is not redistributable but it is included in Windows or later.</span></span> <span data-ttu-id="3465d-111">Pour utiliser Comctl32.dll version 6, spécifiez-la dans un manifeste.</span><span class="sxs-lookup"><span data-stu-id="3465d-111">To use Comctl32.dll version 6, specify it in a manifest.</span></span> <span data-ttu-id="3465d-112">Pour plus d’informations sur les manifestes, consultez <a href="cookbook-overview.md">activation des styles visuels</a>.</span><span class="sxs-lookup"><span data-stu-id="3465d-112">For more information on manifests, see <a href="cookbook-overview.md">Enabling Visual Styles</a>.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="PBS_SMOOTH"></span><span id="pbs_smooth"></span><dl> <span data-ttu-id="3465d-113"><dt><strong>PBS_SMOOTH</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="3465d-113"><dt><strong>PBS_SMOOTH</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="3465d-114"><a href="common-control-versions.md">Version 4,70</a> ou ultérieure.</span><span class="sxs-lookup"><span data-stu-id="3465d-114"><a href="common-control-versions.md">Version 4.70</a> or later.</span></span> <span data-ttu-id="3465d-115">La barre de progression affiche l’état de progression dans une barre de défilement lisse au lieu de la barre segmentée par défaut.</span><span class="sxs-lookup"><span data-stu-id="3465d-115">The progress bar displays progress status in a smooth scrolling bar instead of the default segmented bar.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="3465d-116">Ce style est pris en charge uniquement dans le thème Windows classique.</span><span class="sxs-lookup"><span data-stu-id="3465d-116">This style is supported only in the Windows Classic theme.</span></span> <span data-ttu-id="3465d-117">Tous les autres thèmes remplacent ce style.</span><span class="sxs-lookup"><span data-stu-id="3465d-117">All other themes override this style.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="PBS_SMOOTHREVERSE"></span><span id="pbs_smoothreverse"></span><dl> <span data-ttu-id="3465d-118"><dt><strong>PBS_SMOOTHREVERSE</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="3465d-118"><dt><strong>PBS_SMOOTHREVERSE</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="3465d-119"><a href="common-control-versions.md">Version 6,0</a> ou ultérieure et <strong>Windows Vista.</strong></span><span class="sxs-lookup"><span data-stu-id="3465d-119"><a href="common-control-versions.md">Version 6.0</a> or later and <strong>Windows Vista.</strong></span></span> <span data-ttu-id="3465d-120">Détermine le comportement d’animation que la barre de progression doit utiliser lors du déplacement vers l’arrière (d’une valeur supérieure à une valeur inférieure).</span><span class="sxs-lookup"><span data-stu-id="3465d-120">Determines the animation behavior that the progress bar should use when moving backward (from a higher value to a lower value).</span></span> <span data-ttu-id="3465d-121">Si cette valeur est définie, une &quot; &quot; transition en douceur aura lieu, sinon le contrôle &quot; passera &quot; à la valeur inférieure.</span><span class="sxs-lookup"><span data-stu-id="3465d-121">If this is set, then a &quot;smooth&quot; transition will occur, otherwise the control will &quot;jump&quot; to the lower value.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="PBS_VERTICAL"></span><span id="pbs_vertical"></span><dl> <span data-ttu-id="3465d-122"><dt><strong>PBS_VERTICAL</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="3465d-122"><dt><strong>PBS_VERTICAL</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="3465d-123"><a href="common-control-versions.md">Version 4,70</a> ou ultérieure.</span><span class="sxs-lookup"><span data-stu-id="3465d-123"><a href="common-control-versions.md">Version 4.70</a> or later.</span></span> <span data-ttu-id="3465d-124">La barre de progression affiche l’état de progression verticalement, de bas en haut.</span><span class="sxs-lookup"><span data-stu-id="3465d-124">The progress bar displays progress status vertically, from bottom to top.</span></span><br/></td>
</tr>
</tbody>
</table>



## <a name="remarks"></a><span data-ttu-id="3465d-125">Notes</span><span class="sxs-lookup"><span data-stu-id="3465d-125">Remarks</span></span>

<span data-ttu-id="3465d-126">Vous pouvez définir des styles de barre de progression, de la même façon que d’autres contrôles communs, avec [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa), [**GetWindowLong**](/windows/desktop/api/winuser/nf-winuser-getwindowlonga)ou [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga).</span><span class="sxs-lookup"><span data-stu-id="3465d-126">You can set progress bar styles, in the same way as other common controls, with [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa), [**GetWindowLong**](/windows/desktop/api/winuser/nf-winuser-getwindowlonga), or [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga).</span></span>

## <a name="requirements"></a><span data-ttu-id="3465d-127">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3465d-127">Requirements</span></span>



| <span data-ttu-id="3465d-128">Condition requise</span><span class="sxs-lookup"><span data-stu-id="3465d-128">Requirement</span></span> | <span data-ttu-id="3465d-129">Valeur</span><span class="sxs-lookup"><span data-stu-id="3465d-129">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="3465d-130">En-tête</span><span class="sxs-lookup"><span data-stu-id="3465d-130">Header</span></span><br/> | <dl> <span data-ttu-id="3465d-131"><dt>CommCtrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="3465d-131"><dt>CommCtrl.h</dt></span></span> </dl> |



 

