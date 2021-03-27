---
description: Les enregistrements splines représentent les courbes quadratiques (c’est-à-dire, les b-splines quadratiques) utilisées par TrueType.
ms.assetid: 39b81ffc-382b-467c-83d7-d0754847759a
title: Enregistrements spline
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a1e10f36e4a0481f9950f63c4cbbb59d48d24df0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103755837"
---
# <a name="spline-records"></a><span data-ttu-id="f028e-103">Enregistrements spline</span><span class="sxs-lookup"><span data-stu-id="f028e-103">Spline Records</span></span>

<span data-ttu-id="f028e-104">Les enregistrements splines représentent les courbes quadratiques (c’est-à-dire, les b-splines quadratiques) utilisées par TrueType.</span><span class="sxs-lookup"><span data-stu-id="f028e-104">Spline records represent the quadratic curves (that is, quadratic b-splines) used by TrueType.</span></span> <span data-ttu-id="f028e-105">Un enregistrement de spline commence par le dernier point de l’enregistrement précédent (ou pour le premier enregistrement du contour, avec le point de départ).</span><span class="sxs-lookup"><span data-stu-id="f028e-105">A spline record begins with the last point in the previous record (or for the first record in the contour, with the starting point).</span></span> <span data-ttu-id="f028e-106">Pour le premier enregistrement de spline, le point de départ et le dernier point de l’enregistrement se trouvent sur le contour du glyphe.</span><span class="sxs-lookup"><span data-stu-id="f028e-106">For the first spline record, the starting point and the last point in the record are on the glyph outline.</span></span> <span data-ttu-id="f028e-107">Pour tous les autres enregistrements de spline, seul le dernier point se trouve sur le contour du glyphe.</span><span class="sxs-lookup"><span data-stu-id="f028e-107">For all other spline records, only the last point is on the glyph outline.</span></span> <span data-ttu-id="f028e-108">Tous les autres points des enregistrements spline sont en dehors du contour du glyphe et doivent être rendus comme des points de contrôle des b-splines.</span><span class="sxs-lookup"><span data-stu-id="f028e-108">All other points in the spline records are off the glyph outline and must be rendered as the control points of b-splines.</span></span>

<span data-ttu-id="f028e-109">Le dernier enregistrement de spline ou de polyligne d’un contour se termine toujours par le point de départ du contour.</span><span class="sxs-lookup"><span data-stu-id="f028e-109">The last spline or polyline record in a contour always ends with the contour's starting point.</span></span> <span data-ttu-id="f028e-110">Cette organisation garantit que chaque contour est fermé.</span><span class="sxs-lookup"><span data-stu-id="f028e-110">This arrangement ensures that every contour is closed.</span></span>

<span data-ttu-id="f028e-111">Comme les b-splines nécessitent trois points (un point dépassant le contour du glyphe entre deux points du contour), vous devez effectuer des calculs quand un enregistrement de spline contient plusieurs points hors courbe.</span><span class="sxs-lookup"><span data-stu-id="f028e-111">Because b-splines require three points (one point off the glyph outline between two points that are on the outline), you must perform some calculations when a spline record contains more than one off-curve point.</span></span>

<span data-ttu-id="f028e-112">Par exemple, si un enregistrement spline contient trois points (A, B et C) et qu’il ne s’agit pas du premier enregistrement, les points A et B sont déduits du contour du glyphe.</span><span class="sxs-lookup"><span data-stu-id="f028e-112">For example, if a spline record contains three points (A, B, and C) and it is not the first record, points A and B are off the glyph outline.</span></span> <span data-ttu-id="f028e-113">Pour interpréter le point A, utilisez la position actuelle (qui est toujours sur le contour du glyphe) et le point sur le contour du glyphe entre les points A et B. Pour rechercher le point médian (M) entre A et B, vous pouvez effectuer le calcul suivant.</span><span class="sxs-lookup"><span data-stu-id="f028e-113">To interpret point A, use the current position (which is always on the glyph outline) and the point on the glyph outline between points A and B. To find the midpoint (M) between A and B, you can perform the following calculation.</span></span>

<span data-ttu-id="f028e-114">M = A + (B A)/2</span><span class="sxs-lookup"><span data-stu-id="f028e-114">M = A + (B A)/2</span></span>

<span data-ttu-id="f028e-115">Le point médian entre des points consécutifs hors plan dans un enregistrement de spline est un point sur le contour du glyphe, en fonction de la définition du format de spline utilisé dans les polices TrueType.</span><span class="sxs-lookup"><span data-stu-id="f028e-115">The midpoint between consecutive off-outline points in a spline record is a point on the glyph outline, according to the definition of the spline format used in TrueType fonts.</span></span>

<span data-ttu-id="f028e-116">Si la position actuelle est désignée par P, les deux splines quadratiques définies par cet enregistrement spline sont (P, A, M) et (M, B, C).</span><span class="sxs-lookup"><span data-stu-id="f028e-116">If the current position is designated by P, the two quadratic splines defined by this spline record are (P, A, M) and (M, B, C).</span></span>

 

 



