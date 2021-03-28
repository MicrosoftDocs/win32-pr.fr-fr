---
description: Windows GDI+ expose une API plate qui se compose d’environ 600 fonctions, qui sont implémentées dans Gdiplus.dll et déclarées dans Gdiplusflat. h.
ms.assetid: b4fcc02c-1b0f-4731-8312-29894b1f722f
title: Fonctions de mémoire
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 86e748f8a68cc6f04deba3c9676638ee48ee2e86
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104972866"
---
# <a name="memory-functions"></a><span data-ttu-id="78a11-103">Fonctions de mémoire</span><span class="sxs-lookup"><span data-stu-id="78a11-103">Memory Functions</span></span>

<span data-ttu-id="78a11-104">Windows GDI+ expose une API plate qui se compose d’environ 600 fonctions, qui sont implémentées dans Gdiplus.dll et déclarées dans Gdiplusflat. h.</span><span class="sxs-lookup"><span data-stu-id="78a11-104">Windows GDI+ exposes a flat API that consists of about 600 functions, which are implemented in Gdiplus.dll and declared in Gdiplusflat.h.</span></span> <span data-ttu-id="78a11-105">Les fonctions de l’API plate GDI+ sont encapsulées par une collection d’environ 40 classes C++.</span><span class="sxs-lookup"><span data-stu-id="78a11-105">The functions in the GDI+ flat API are wrapped by a collection of about 40 C++ classes.</span></span> <span data-ttu-id="78a11-106">Il est recommandé de ne pas appeler directement les fonctions dans l’API plate.</span><span class="sxs-lookup"><span data-stu-id="78a11-106">It is recommended that you do not directly call the functions in the flat API.</span></span> <span data-ttu-id="78a11-107">Chaque fois que vous effectuez des appels à GDI+, vous devez le faire en appelant les méthodes et les fonctions fournies par les wrappers C++.</span><span class="sxs-lookup"><span data-stu-id="78a11-107">Whenever you make calls to GDI+, you should do so by calling the methods and functions provided by the C++ wrappers.</span></span> <span data-ttu-id="78a11-108">Les services de support technique Microsoft ne fournissent pas de prise en charge du code qui appelle l’API plate directement.</span><span class="sxs-lookup"><span data-stu-id="78a11-108">Microsoft Product Support Services will not provide support for code that calls the flat API directly.</span></span> <span data-ttu-id="78a11-109">Pour plus d’informations sur l’utilisation de ces méthodes Wrapper, consultez l' [API plate GDI+](-gdiplus-flatapi-flat.md).</span><span class="sxs-lookup"><span data-stu-id="78a11-109">For more information on using these wrapper methods, see [GDI+ Flat API](-gdiplus-flatapi-flat.md).</span></span>

<span data-ttu-id="78a11-110">Les fonctions d’API plates suivantes sont encapsulées par la classe C++ [**GdiplusBase**](/windows/desktop/api/gdiplusbase/nl-gdiplusbase-gdiplusbase) .</span><span class="sxs-lookup"><span data-stu-id="78a11-110">The following flat API functions are wrapped by the [**GdiplusBase**](/windows/desktop/api/gdiplusbase/nl-gdiplusbase-gdiplusbase) C++ class.</span></span>

## <a name="memory-functions-and-corresponding-wrapper-methods"></a><span data-ttu-id="78a11-111">Fonctions de mémoire et méthodes Wrapper correspondantes</span><span class="sxs-lookup"><span data-stu-id="78a11-111">Memory Functions and Corresponding Wrapper Methods</span></span>



| <span data-ttu-id="78a11-112">Fonction plate</span><span class="sxs-lookup"><span data-stu-id="78a11-112">Flat function</span></span>                                          | <span data-ttu-id="78a11-113">Méthode Wrapper</span><span class="sxs-lookup"><span data-stu-id="78a11-113">Wrapper method</span></span>                                                                                                                                      | <span data-ttu-id="78a11-114">Notes</span><span class="sxs-lookup"><span data-stu-id="78a11-114">Remarks</span></span>                                                                                                      |
|--------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="78a11-115">GpStatus WINGDIPAPI GdipAlloc (taille \_ t taille)</span><span class="sxs-lookup"><span data-stu-id="78a11-115">GpStatus WINGDIPAPI GdipAlloc(size\_t size)</span></span><br/> | [<span data-ttu-id="78a11-116">**GpStatus WINGDIPAPI GdiplusBase void \* (operator new) (taille \_ t en \_ taille)**</span><span class="sxs-lookup"><span data-stu-id="78a11-116">**GpStatus WINGDIPAPI GdiplusBase void\* (operator new)(size\_t in\_size)**</span></span>](/windows/win32/api/gdiplusbase/nf-gdiplusbase-gdiplusbase-operatornew)<br/>      | <span data-ttu-id="78a11-117">Alloue de la mémoire pour un objet GDI+ Windows.</span><span class="sxs-lookup"><span data-stu-id="78a11-117">Allocates memory for one Windows GDI+ object.</span></span> <br/> <span data-ttu-id="78a11-118">GdipAlloc est déclaré dans GdiplusMem. h.</span><span class="sxs-lookup"><span data-stu-id="78a11-118">GdipAlloc is declared in GdiplusMem.h.</span></span><br/>  |
| <span data-ttu-id="78a11-119">GpStatus WINGDIPAPI GdipFree (void \* PTR);</span><span class="sxs-lookup"><span data-stu-id="78a11-119">GpStatus WINGDIPAPI GdipFree(void\* ptr);</span></span><br/>   | [<span data-ttu-id="78a11-120">**GpStatus WINGDIPAPI GdiplusBase void (opérateur delete) (void \* dans \_ pVoid)**</span><span class="sxs-lookup"><span data-stu-id="78a11-120">**GpStatus WINGDIPAPI GdiplusBase void (operator delete)(void\* in\_pVoid)**</span></span>](/windows/win32/api/gdiplusbase/nf-gdiplusbase-gdiplusbase-operatordelete)<br/> | <span data-ttu-id="78a11-121">Libère de la mémoire pour un objet GDI+ Windows.</span><span class="sxs-lookup"><span data-stu-id="78a11-121">Deallocates memory for one Windows GDI+ object.</span></span> <br/> <span data-ttu-id="78a11-122">GdipFree est déclaré dans GdiplusMem. h.</span><span class="sxs-lookup"><span data-stu-id="78a11-122">GdipFree is declared in GdiplusMem.h.</span></span><br/> |



 

 

 
