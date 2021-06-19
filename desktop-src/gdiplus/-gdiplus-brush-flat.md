---
description: Windows GDI+ expose une API plate qui se compose d’environ 600 fonctions. Ces fonctions d’API plate sont encapsulées par la classe C++ Brush.
ms.assetid: def64d31-9a4b-4365-a618-b87735ce38f1
title: Fonctions Brush (GDI+)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ffe23588c44d8a3a6412cd0c2bc1327b98bbbd95
ms.sourcegitcommit: 91530c19d26ba4c57a6af1f37b57f211f580464e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112395084"
---
# <a name="brush-functions-gdi"></a><span data-ttu-id="823a7-104">Fonctions Brush (GDI+)</span><span class="sxs-lookup"><span data-stu-id="823a7-104">Brush Functions (GDI+)</span></span>

<span data-ttu-id="823a7-105">Windows GDI+ expose une API plate qui se compose d’environ 600 fonctions, qui sont implémentées dans Gdiplus.dll et déclarées dans Gdiplusflat. h.</span><span class="sxs-lookup"><span data-stu-id="823a7-105">Windows GDI+ exposes a flat API that consists of about 600 functions, which are implemented in Gdiplus.dll and declared in Gdiplusflat.h.</span></span> <span data-ttu-id="823a7-106">Les fonctions de l’API plate GDI+ sont encapsulées par une collection d’environ 40 classes C++.</span><span class="sxs-lookup"><span data-stu-id="823a7-106">The functions in the GDI+ flat API are wrapped by a collection of about 40 C++ classes.</span></span> <span data-ttu-id="823a7-107">Il est recommandé de ne pas appeler directement les fonctions dans l’API plate.</span><span class="sxs-lookup"><span data-stu-id="823a7-107">It is recommended that you do not directly call the functions in the flat API.</span></span> <span data-ttu-id="823a7-108">Chaque fois que vous effectuez des appels à GDI+, vous devez le faire en appelant les méthodes et les fonctions fournies par les wrappers C++.</span><span class="sxs-lookup"><span data-stu-id="823a7-108">Whenever you make calls to GDI+, you should do so by calling the methods and functions provided by the C++ wrappers.</span></span> <span data-ttu-id="823a7-109">Les services de support technique Microsoft ne fournissent pas de prise en charge du code qui appelle l’API plate directement.</span><span class="sxs-lookup"><span data-stu-id="823a7-109">Microsoft Product Support Services will not provide support for code that calls the flat API directly.</span></span> <span data-ttu-id="823a7-110">Pour plus d’informations sur l’utilisation de ces méthodes Wrapper, consultez l' [API plate GDI+](-gdiplus-flatapi-flat.md).</span><span class="sxs-lookup"><span data-stu-id="823a7-110">For more information on using these wrapper methods, see [GDI+ Flat API](-gdiplus-flatapi-flat.md).</span></span>

<span data-ttu-id="823a7-111">Les fonctions d’API plates suivantes sont encapsulées par la classe C++ [**Brush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-brush) .</span><span class="sxs-lookup"><span data-stu-id="823a7-111">The following flat API functions are wrapped by the [**Brush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-brush) C++ class.</span></span>

## <a name="brush-functions-and-corresponding-wrapper-methods"></a><span data-ttu-id="823a7-112">Fonctions de pinceau et méthodes Wrapper correspondantes</span><span class="sxs-lookup"><span data-stu-id="823a7-112">Brush Functions and Corresponding Wrapper Methods</span></span>



| <span data-ttu-id="823a7-113">Fonction plate</span><span class="sxs-lookup"><span data-stu-id="823a7-113">Flat function</span></span>                                                                        | <span data-ttu-id="823a7-114">Méthode Wrapper</span><span class="sxs-lookup"><span data-stu-id="823a7-114">Wrapper method</span></span>                                          | <span data-ttu-id="823a7-115">Description</span><span class="sxs-lookup"><span data-stu-id="823a7-115">Description</span></span>                                                                                                                                          |
|--------------------------------------------------------------------------------------|---------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="823a7-116">GpStatus WINGDIPAPI GdipCloneBrush (GpBrush \* Brush, GpBrush \* \* cloneBrush)</span><span class="sxs-lookup"><span data-stu-id="823a7-116">GpStatus WINGDIPAPI GdipCloneBrush(GpBrush \*brush, GpBrush \*\*cloneBrush)</span></span>          | [<span data-ttu-id="823a7-117">**Brush :: Clone**</span><span class="sxs-lookup"><span data-stu-id="823a7-117">**Brush::Clone**</span></span>](/windows/desktop/api/Gdiplusbrush/nf-gdiplusbrush-brush-clone)     | <span data-ttu-id="823a7-118">La méthode [**Brush :: Clone**](/windows/desktop/api/Gdiplusbrush/nf-gdiplusbrush-brush-clone) crée un nouvel objet [**Brush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-brush) basé sur ce pinceau.</span><span class="sxs-lookup"><span data-stu-id="823a7-118">The [**Brush::Clone**](/windows/desktop/api/Gdiplusbrush/nf-gdiplusbrush-brush-clone) method creates a new [**Brush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-brush) object based on this brush.</span></span> |
| <span data-ttu-id="823a7-119">GpStatus WINGDIPAPI GdipDeleteBrush (GpBrush \* Brush)</span><span class="sxs-lookup"><span data-stu-id="823a7-119">GpStatus WINGDIPAPI GdipDeleteBrush(GpBrush \*brush)</span></span>                                 | <span data-ttu-id="823a7-120">virtuel ~ Brush ()</span><span class="sxs-lookup"><span data-stu-id="823a7-120">virtual ~Brush()</span></span>                                        | <span data-ttu-id="823a7-121">Nettoie les ressources utilisées par un objet [**Brush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-brush) .</span><span class="sxs-lookup"><span data-stu-id="823a7-121">Cleans up resources used by a [**Brush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-brush) object.</span></span>                                                                    |
| <span data-ttu-id="823a7-122">GpStatus WINGDIPAPI GdipGetBrushType (GpBrush \* Brush, GpBrushType \* type)</span><span class="sxs-lookup"><span data-stu-id="823a7-122">GpStatus WINGDIPAPI GdipGetBrushType(GpBrush \*brush, GpBrushType \*type)</span></span><br/> | [<span data-ttu-id="823a7-123">**Brush :: GetType**</span><span class="sxs-lookup"><span data-stu-id="823a7-123">**Brush::GetType**</span></span>](/windows/desktop/api/Gdiplusbrush/nf-gdiplusbrush-brush-gettype) | <span data-ttu-id="823a7-124">La méthode [**Brush :: GetType**](/windows/desktop/api/Gdiplusbrush/nf-gdiplusbrush-brush-gettype) obtient le type de ce pinceau.</span><span class="sxs-lookup"><span data-stu-id="823a7-124">The [**Brush::GetType**](/windows/desktop/api/Gdiplusbrush/nf-gdiplusbrush-brush-gettype) method gets the type of this brush.</span></span>                                                      |



 

 

 




