---
description: Windows GDI+ expose une API plate qui se compose d’environ 600 fonctions, qui sont implémentées dans Gdiplus.dll et déclarées dans Gdiplusflat. h.
ms.assetid: def64d31-9a4b-4365-a618-b87735ce38f1
title: Fonctions Brush (GDI+)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7490cc641312014987b2fb847979de640c28c47e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104319018"
---
# <a name="brush-functions-gdi"></a><span data-ttu-id="1b86b-103">Fonctions Brush (GDI+)</span><span class="sxs-lookup"><span data-stu-id="1b86b-103">Brush Functions (GDI+)</span></span>

<span data-ttu-id="1b86b-104">Windows GDI+ expose une API plate qui se compose d’environ 600 fonctions, qui sont implémentées dans Gdiplus.dll et déclarées dans Gdiplusflat. h.</span><span class="sxs-lookup"><span data-stu-id="1b86b-104">Windows GDI+ exposes a flat API that consists of about 600 functions, which are implemented in Gdiplus.dll and declared in Gdiplusflat.h.</span></span> <span data-ttu-id="1b86b-105">Les fonctions de l’API plate GDI+ sont encapsulées par une collection d’environ 40 classes C++.</span><span class="sxs-lookup"><span data-stu-id="1b86b-105">The functions in the GDI+ flat API are wrapped by a collection of about 40 C++ classes.</span></span> <span data-ttu-id="1b86b-106">Il est recommandé de ne pas appeler directement les fonctions dans l’API plate.</span><span class="sxs-lookup"><span data-stu-id="1b86b-106">It is recommended that you do not directly call the functions in the flat API.</span></span> <span data-ttu-id="1b86b-107">Chaque fois que vous effectuez des appels à GDI+, vous devez le faire en appelant les méthodes et les fonctions fournies par les wrappers C++.</span><span class="sxs-lookup"><span data-stu-id="1b86b-107">Whenever you make calls to GDI+, you should do so by calling the methods and functions provided by the C++ wrappers.</span></span> <span data-ttu-id="1b86b-108">Les services de support technique Microsoft ne fournissent pas de prise en charge du code qui appelle l’API plate directement.</span><span class="sxs-lookup"><span data-stu-id="1b86b-108">Microsoft Product Support Services will not provide support for code that calls the flat API directly.</span></span> <span data-ttu-id="1b86b-109">Pour plus d’informations sur l’utilisation de ces méthodes Wrapper, consultez l' [API plate GDI+](-gdiplus-flatapi-flat.md).</span><span class="sxs-lookup"><span data-stu-id="1b86b-109">For more information on using these wrapper methods, see [GDI+ Flat API](-gdiplus-flatapi-flat.md).</span></span>

<span data-ttu-id="1b86b-110">Les fonctions d’API plates suivantes sont encapsulées par la classe C++ [**Brush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-brush) .</span><span class="sxs-lookup"><span data-stu-id="1b86b-110">The following flat API functions are wrapped by the [**Brush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-brush) C++ class.</span></span>

## <a name="brush-functions-and-corresponding-wrapper-methods"></a><span data-ttu-id="1b86b-111">Fonctions de pinceau et méthodes Wrapper correspondantes</span><span class="sxs-lookup"><span data-stu-id="1b86b-111">Brush Functions and Corresponding Wrapper Methods</span></span>



| <span data-ttu-id="1b86b-112">Fonction plate</span><span class="sxs-lookup"><span data-stu-id="1b86b-112">Flat function</span></span>                                                                        | <span data-ttu-id="1b86b-113">Méthode Wrapper</span><span class="sxs-lookup"><span data-stu-id="1b86b-113">Wrapper method</span></span>                                          | <span data-ttu-id="1b86b-114">Description</span><span class="sxs-lookup"><span data-stu-id="1b86b-114">Description</span></span>                                                                                                                                          |
|--------------------------------------------------------------------------------------|---------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1b86b-115">GpStatus WINGDIPAPI GdipCloneBrush (GpBrush \* Brush, GpBrush \* \* cloneBrush)</span><span class="sxs-lookup"><span data-stu-id="1b86b-115">GpStatus WINGDIPAPI GdipCloneBrush(GpBrush \*brush, GpBrush \*\*cloneBrush)</span></span>          | [<span data-ttu-id="1b86b-116">**Brush :: Clone**</span><span class="sxs-lookup"><span data-stu-id="1b86b-116">**Brush::Clone**</span></span>](/windows/desktop/api/Gdiplusbrush/nf-gdiplusbrush-brush-clone)     | <span data-ttu-id="1b86b-117">La méthode [**Brush :: Clone**](/windows/desktop/api/Gdiplusbrush/nf-gdiplusbrush-brush-clone) crée un nouvel objet [**Brush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-brush) basé sur ce pinceau.</span><span class="sxs-lookup"><span data-stu-id="1b86b-117">The [**Brush::Clone**](/windows/desktop/api/Gdiplusbrush/nf-gdiplusbrush-brush-clone) method creates a new [**Brush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-brush) object based on this brush.</span></span> |
| <span data-ttu-id="1b86b-118">GpStatus WINGDIPAPI GdipDeleteBrush (GpBrush \* Brush)</span><span class="sxs-lookup"><span data-stu-id="1b86b-118">GpStatus WINGDIPAPI GdipDeleteBrush(GpBrush \*brush)</span></span>                                 | <span data-ttu-id="1b86b-119">virtuel ~ Brush ()</span><span class="sxs-lookup"><span data-stu-id="1b86b-119">virtual ~Brush()</span></span>                                        | <span data-ttu-id="1b86b-120">Nettoie les ressources utilisées par un objet [**Brush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-brush) .</span><span class="sxs-lookup"><span data-stu-id="1b86b-120">Cleans up resources used by a [**Brush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-brush) object.</span></span>                                                                    |
| <span data-ttu-id="1b86b-121">GpStatus WINGDIPAPI GdipGetBrushType (GpBrush \* Brush, GpBrushType \* type)</span><span class="sxs-lookup"><span data-stu-id="1b86b-121">GpStatus WINGDIPAPI GdipGetBrushType(GpBrush \*brush, GpBrushType \*type)</span></span><br/> | [<span data-ttu-id="1b86b-122">**Brush :: GetType**</span><span class="sxs-lookup"><span data-stu-id="1b86b-122">**Brush::GetType**</span></span>](/windows/desktop/api/Gdiplusbrush/nf-gdiplusbrush-brush-gettype) | <span data-ttu-id="1b86b-123">La méthode [**Brush :: GetType**](/windows/desktop/api/Gdiplusbrush/nf-gdiplusbrush-brush-gettype) obtient le type de ce pinceau.</span><span class="sxs-lookup"><span data-stu-id="1b86b-123">The [**Brush::GetType**](/windows/desktop/api/Gdiplusbrush/nf-gdiplusbrush-brush-gettype) method gets the type of this brush.</span></span>                                                      |



 

 

 




