---
description: Windows GDI+ expose une API plate qui se compose d’environ 600 fonctions. Ces fonctions d’API plates sont encapsulées par la classe C++ SolidBrush.
ms.assetid: b427b8ab-66fd-4f57-b08e-5f337a9ac9af
title: Fonctions SolidBrush
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc9feb2676c60b3f504315f75303aadb16a1cd1f
ms.sourcegitcommit: 91530c19d26ba4c57a6af1f37b57f211f580464e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112395554"
---
# <a name="solidbrush-functions"></a><span data-ttu-id="16599-104">Fonctions SolidBrush</span><span class="sxs-lookup"><span data-stu-id="16599-104">SolidBrush Functions</span></span>

<span data-ttu-id="16599-105">Windows GDI+ expose une API plate qui se compose d’environ 600 fonctions, qui sont implémentées dans Gdiplus.dll et déclarées dans Gdiplusflat. h.</span><span class="sxs-lookup"><span data-stu-id="16599-105">Windows GDI+ exposes a flat API that consists of about 600 functions, which are implemented in Gdiplus.dll and declared in Gdiplusflat.h.</span></span> <span data-ttu-id="16599-106">Les fonctions de l’API plate GDI+ sont encapsulées par une collection d’environ 40 classes C++.</span><span class="sxs-lookup"><span data-stu-id="16599-106">The functions in the GDI+ flat API are wrapped by a collection of about 40 C++ classes.</span></span> <span data-ttu-id="16599-107">Nous vous recommandons de ne pas appeler directement les fonctions dans l’API plate.</span><span class="sxs-lookup"><span data-stu-id="16599-107">We recommend not to call the functions in the flat API directly.</span></span> <span data-ttu-id="16599-108">Chaque fois que vous effectuez des appels à GDI+, nous vous recommandons de le faire en appelant les méthodes et les fonctions fournies par les wrappers C++.</span><span class="sxs-lookup"><span data-stu-id="16599-108">Whenever you make calls to GDI+, we recommend that you do so by calling the methods and functions provided by the C++ wrappers.</span></span> <span data-ttu-id="16599-109">Les services de support technique Microsoft ne fournissent pas de prise en charge du code qui appelle l’API plate directement.</span><span class="sxs-lookup"><span data-stu-id="16599-109">Microsoft Product Support Services will not provide support for code that calls the flat API directly.</span></span> <span data-ttu-id="16599-110">Pour plus d’informations sur l’utilisation de ces méthodes Wrapper, consultez l' [API plate GDI+](-gdiplus-flatapi-flat.md).</span><span class="sxs-lookup"><span data-stu-id="16599-110">For more info on using these wrapper methods, see [GDI+ Flat API](-gdiplus-flatapi-flat.md).</span></span>

<span data-ttu-id="16599-111">Les fonctions d’API plates suivantes sont encapsulées par la classe C++ [**SolidBrush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-solidbrush) .</span><span class="sxs-lookup"><span data-stu-id="16599-111">The following flat API functions are wrapped by the [**SolidBrush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-solidbrush) C++ class.</span></span>

## <a name="brush-functions-and-corresponding-wrapper-methods"></a><span data-ttu-id="16599-112">Fonctions de pinceau et méthodes Wrapper correspondantes</span><span class="sxs-lookup"><span data-stu-id="16599-112">Brush Functions and Corresponding Wrapper Methods</span></span>



| <span data-ttu-id="16599-113">Fonction plate</span><span class="sxs-lookup"><span data-stu-id="16599-113">Flat function</span></span>                                                                               | <span data-ttu-id="16599-114">Méthode Wrapper</span><span class="sxs-lookup"><span data-stu-id="16599-114">Wrapper method</span></span>                                                                                       | <span data-ttu-id="16599-115">Remarques</span><span class="sxs-lookup"><span data-stu-id="16599-115">Remarks</span></span>                                                                                 |
|---------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="16599-116">**GpStatus WINGDIPAPI GdipCreateSolidFill (ARGB Color, GpSolidFill \* \* Brush)**</span><span class="sxs-lookup"><span data-stu-id="16599-116">**GpStatus WINGDIPAPI GdipCreateSolidFill(ARGB color, GpSolidFill \*\*brush)**</span></span><br/>   | <span data-ttu-id="16599-117">[**SolidBrush :: SolidBrush (dans la couleur const Color& Color)**](/windows/win32/api/gdiplusbrush/nf-gdiplusbrush-solidbrush-solidbrush(constsolidbrush_))</span><span class="sxs-lookup"><span data-stu-id="16599-117">[**SolidBrush::SolidBrush(IN const Color& color)**](/windows/win32/api/gdiplusbrush/nf-gdiplusbrush-solidbrush-solidbrush(constsolidbrush_))</span></span> | <span data-ttu-id="16599-118">Crée un objet [**SolidBrush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-solidbrush) basé sur une couleur</span><span class="sxs-lookup"><span data-stu-id="16599-118">Creates a [**SolidBrush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-solidbrush) object based on a color</span></span> |
| <span data-ttu-id="16599-119">**GpStatus WINGDIPAPI GdipSetSolidFillColor (GpSolidFill \* Brush, ARGB Color)**</span><span class="sxs-lookup"><span data-stu-id="16599-119">**GpStatus WINGDIPAPI GdipSetSolidFillColor(GpSolidFill \*brush, ARGB color)**</span></span><br/>   | [<span data-ttu-id="16599-120">**SolidBrush :: SetColor (dans la couleur const Color& Color)**</span><span class="sxs-lookup"><span data-stu-id="16599-120">**SolidBrush::SetColor(IN const Color& color)**</span></span>](/windows/desktop/api/Gdiplusbrush/nf-gdiplusbrush-solidbrush-setcolor)     | <span data-ttu-id="16599-121">Définit la couleur de ce pinceau Uni</span><span class="sxs-lookup"><span data-stu-id="16599-121">Sets the color of this solid brush</span></span>                                                      |
| <span data-ttu-id="16599-122">**GpStatus WINGDIPAPI GdipGetSolidFillColor (GpSolidFill \* Brush, ARGB \* Color)**</span><span class="sxs-lookup"><span data-stu-id="16599-122">**GpStatus WINGDIPAPI GdipGetSolidFillColor(GpSolidFill \*brush, ARGB \*color)**</span></span><br/> | [<span data-ttu-id="16599-123">**SolidBrush :: GetColor (couleur de sortie de sortie \* ) const**</span><span class="sxs-lookup"><span data-stu-id="16599-123">**SolidBrush::GetColor(OUT Color\* color) const**</span></span>](/windows/desktop/api/Gdiplusbrush/nf-gdiplusbrush-solidbrush-getcolor)   | <span data-ttu-id="16599-124">Obtient la couleur de ce pinceau Uni</span><span class="sxs-lookup"><span data-stu-id="16599-124">Gets the color of this solid brush</span></span>                                                      |



 

 

 
