---
description: Cette rubrique répertorie les méthodes ExcludeClip de la classe Graphics. Pour obtenir la liste complète des méthodes de la classe Graphics, consultez Graphics.
ms.assetid: ee2b1bc7-6623-4144-b8fb-2ab9fbe28f59
title: Méthodes Graphics. ExcludeClip (Gdiplusgraphics. h)
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: 70011bfe1aba7ef8e7c14b58f61bfcbd9549c8fb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "104996469"
---
# <a name="graphicsexcludeclip-methods"></a><span data-ttu-id="def9c-104">Méthodes Graphics. ExcludeClip</span><span class="sxs-lookup"><span data-stu-id="def9c-104">Graphics.ExcludeClip methods</span></span>

<span data-ttu-id="def9c-105">Cette rubrique répertorie les méthodes ExcludeClip de la classe [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) .</span><span class="sxs-lookup"><span data-stu-id="def9c-105">This topic lists the ExcludeClip methods of the [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) class.</span></span> <span data-ttu-id="def9c-106">Pour obtenir la liste complète des méthodes de la classe **Graphics** , consultez [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics).</span><span class="sxs-lookup"><span data-stu-id="def9c-106">For a complete list of methods for the **Graphics** class, see [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics).</span></span>

### <a name="overload-list"></a><span data-ttu-id="def9c-107">Liste de surcharge</span><span class="sxs-lookup"><span data-stu-id="def9c-107">Overload list</span></span>



| <span data-ttu-id="def9c-108">Méthode</span><span class="sxs-lookup"><span data-stu-id="def9c-108">Method</span></span>                                                                         | <span data-ttu-id="def9c-109">Description</span><span class="sxs-lookup"><span data-stu-id="def9c-109">Description</span></span>                                                                                                                                                                                                  |
|:-------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="def9c-110">[**ExcludeClip (Rect&)**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-excludeclip(inconstrect_))</span><span class="sxs-lookup"><span data-stu-id="def9c-110">[**ExcludeClip(Rect&)**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-excludeclip(inconstrect_))</span></span>   | <span data-ttu-id="def9c-111">La méthode [**Graphics :: ExcludeClip**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-excludeclip(inconstrect_)) met à jour la zone de découpage avec la partie de elle-même qui ne croise pas le rectangle spécifié.</span><span class="sxs-lookup"><span data-stu-id="def9c-111">The [**Graphics::ExcludeClip**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-excludeclip(inconstrect_)) method updates the clipping region to the portion of itself that does not intersect the specified rectangle.</span></span><br/>  |
| <span data-ttu-id="def9c-112">[**ExcludeClip (RectF&)**](/previous-versions//ms535975(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="def9c-112">[**ExcludeClip(RectF&)**](/previous-versions//ms535975(v=vs.85))</span></span> | <span data-ttu-id="def9c-113">La méthode [**Graphics :: ExcludeClip**](/previous-versions//ms535975(v=vs.85)) met à jour la zone de découpage avec la partie de elle-même qui ne croise pas le rectangle spécifié.</span><span class="sxs-lookup"><span data-stu-id="def9c-113">The [**Graphics::ExcludeClip**](/previous-versions//ms535975(v=vs.85)) method updates the clipping region to the portion of itself that does not intersect the specified rectangle.</span></span><br/> |
| <span data-ttu-id="def9c-114">[**ExcludeClip (région \* )**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-excludeclip(inconstregion))</span><span class="sxs-lookup"><span data-stu-id="def9c-114">[**ExcludeClip(Region\*)**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-excludeclip(inconstregion))</span></span>   | <span data-ttu-id="def9c-115">La méthode [**Graphics :: ExcludeClip**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-excludeclip(inconstregion)) met à jour la zone de découpage avec la partie de elle-même qui ne chevauche pas la région spécifiée.</span><span class="sxs-lookup"><span data-stu-id="def9c-115">The [**Graphics::ExcludeClip**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-excludeclip(inconstregion)) method updates the clipping region with the portion of itself that does not overlap the specified region.</span></span><br/>        |



## <a name="requirements"></a><span data-ttu-id="def9c-116">Spécifications</span><span class="sxs-lookup"><span data-stu-id="def9c-116">Requirements</span></span>



| <span data-ttu-id="def9c-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="def9c-117">Requirement</span></span> | <span data-ttu-id="def9c-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="def9c-118">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="def9c-119">En-tête</span><span class="sxs-lookup"><span data-stu-id="def9c-119">Header</span></span><br/> | <dl> <span data-ttu-id="def9c-120"><dt>Gdiplusgraphics. h</dt></span><span class="sxs-lookup"><span data-stu-id="def9c-120"><dt>Gdiplusgraphics.h</dt></span></span> </dl> |



 

 
