---
description: Windows GDI+ expose une API plate qui se compose d’environ 600 fonctions, qui sont implémentées dans Gdiplus.dll et déclarées dans Gdiplusflat. h.
ms.assetid: b427b8ab-66fd-4f57-b08e-5f337a9ac9af
title: Fonctions SolidBrush
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc7d75e99f46877ce990a985e47bc4b9021faaa2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104972146"
---
# <a name="solidbrush-functions"></a><span data-ttu-id="4497a-103">Fonctions SolidBrush</span><span class="sxs-lookup"><span data-stu-id="4497a-103">SolidBrush Functions</span></span>

<span data-ttu-id="4497a-104">Windows GDI+ expose une API plate qui se compose d’environ 600 fonctions, qui sont implémentées dans Gdiplus.dll et déclarées dans Gdiplusflat. h.</span><span class="sxs-lookup"><span data-stu-id="4497a-104">Windows GDI+ exposes a flat API that consists of about 600 functions, which are implemented in Gdiplus.dll and declared in Gdiplusflat.h.</span></span> <span data-ttu-id="4497a-105">Les fonctions de l’API plate GDI+ sont encapsulées par une collection d’environ 40 classes C++.</span><span class="sxs-lookup"><span data-stu-id="4497a-105">The functions in the GDI+ flat API are wrapped by a collection of about 40 C++ classes.</span></span> <span data-ttu-id="4497a-106">Nous vous recommandons de ne pas appeler directement les fonctions dans l’API plate.</span><span class="sxs-lookup"><span data-stu-id="4497a-106">We recommend not to call the functions in the flat API directly.</span></span> <span data-ttu-id="4497a-107">Chaque fois que vous effectuez des appels à GDI+, nous vous recommandons de le faire en appelant les méthodes et les fonctions fournies par les wrappers C++.</span><span class="sxs-lookup"><span data-stu-id="4497a-107">Whenever you make calls to GDI+, we recommend that you do so by calling the methods and functions provided by the C++ wrappers.</span></span> <span data-ttu-id="4497a-108">Les services de support technique Microsoft ne fournissent pas de prise en charge du code qui appelle l’API plate directement.</span><span class="sxs-lookup"><span data-stu-id="4497a-108">Microsoft Product Support Services will not provide support for code that calls the flat API directly.</span></span> <span data-ttu-id="4497a-109">Pour plus d’informations sur l’utilisation de ces méthodes Wrapper, consultez l' [API plate GDI+](-gdiplus-flatapi-flat.md).</span><span class="sxs-lookup"><span data-stu-id="4497a-109">For more info on using these wrapper methods, see [GDI+ Flat API](-gdiplus-flatapi-flat.md).</span></span>

<span data-ttu-id="4497a-110">Les fonctions d’API plates suivantes sont encapsulées par la classe C++ [**SolidBrush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-solidbrush) .</span><span class="sxs-lookup"><span data-stu-id="4497a-110">The following flat API functions are wrapped by the [**SolidBrush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-solidbrush) C++ class.</span></span>

## <a name="brush-functions-and-corresponding-wrapper-methods"></a><span data-ttu-id="4497a-111">Fonctions de pinceau et méthodes Wrapper correspondantes</span><span class="sxs-lookup"><span data-stu-id="4497a-111">Brush Functions and Corresponding Wrapper Methods</span></span>



| <span data-ttu-id="4497a-112">Fonction plate</span><span class="sxs-lookup"><span data-stu-id="4497a-112">Flat function</span></span>                                                                               | <span data-ttu-id="4497a-113">Méthode Wrapper</span><span class="sxs-lookup"><span data-stu-id="4497a-113">Wrapper method</span></span>                                                                                       | <span data-ttu-id="4497a-114">Notes</span><span class="sxs-lookup"><span data-stu-id="4497a-114">Remarks</span></span>                                                                                 |
|---------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4497a-115">**GpStatus WINGDIPAPI GdipCreateSolidFill (ARGB Color, GpSolidFill \* \* Brush)**</span><span class="sxs-lookup"><span data-stu-id="4497a-115">**GpStatus WINGDIPAPI GdipCreateSolidFill(ARGB color, GpSolidFill \*\*brush)**</span></span><br/>   | <span data-ttu-id="4497a-116">[**SolidBrush :: SolidBrush (dans la couleur const Color& Color)**](/windows/win32/api/gdiplusbrush/nf-gdiplusbrush-solidbrush-solidbrush(constsolidbrush_))</span><span class="sxs-lookup"><span data-stu-id="4497a-116">[**SolidBrush::SolidBrush(IN const Color& color)**](/windows/win32/api/gdiplusbrush/nf-gdiplusbrush-solidbrush-solidbrush(constsolidbrush_))</span></span> | <span data-ttu-id="4497a-117">Crée un objet [**SolidBrush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-solidbrush) basé sur une couleur</span><span class="sxs-lookup"><span data-stu-id="4497a-117">Creates a [**SolidBrush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-solidbrush) object based on a color</span></span> |
| <span data-ttu-id="4497a-118">**GpStatus WINGDIPAPI GdipSetSolidFillColor (GpSolidFill \* Brush, ARGB Color)**</span><span class="sxs-lookup"><span data-stu-id="4497a-118">**GpStatus WINGDIPAPI GdipSetSolidFillColor(GpSolidFill \*brush, ARGB color)**</span></span><br/>   | [<span data-ttu-id="4497a-119">**SolidBrush :: SetColor (dans la couleur const Color& Color)**</span><span class="sxs-lookup"><span data-stu-id="4497a-119">**SolidBrush::SetColor(IN const Color& color)**</span></span>](/windows/desktop/api/Gdiplusbrush/nf-gdiplusbrush-solidbrush-setcolor)     | <span data-ttu-id="4497a-120">Définit la couleur de ce pinceau Uni</span><span class="sxs-lookup"><span data-stu-id="4497a-120">Sets the color of this solid brush</span></span>                                                      |
| <span data-ttu-id="4497a-121">**GpStatus WINGDIPAPI GdipGetSolidFillColor (GpSolidFill \* Brush, ARGB \* Color)**</span><span class="sxs-lookup"><span data-stu-id="4497a-121">**GpStatus WINGDIPAPI GdipGetSolidFillColor(GpSolidFill \*brush, ARGB \*color)**</span></span><br/> | [<span data-ttu-id="4497a-122">**SolidBrush :: GetColor (couleur de sortie de sortie \* ) const**</span><span class="sxs-lookup"><span data-stu-id="4497a-122">**SolidBrush::GetColor(OUT Color\* color) const**</span></span>](/windows/desktop/api/Gdiplusbrush/nf-gdiplusbrush-solidbrush-getcolor)   | <span data-ttu-id="4497a-123">Obtient la couleur de ce pinceau Uni</span><span class="sxs-lookup"><span data-stu-id="4497a-123">Gets the color of this solid brush</span></span>                                                      |



 

 

 
