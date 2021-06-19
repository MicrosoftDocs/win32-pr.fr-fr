---
description: Windows GDI+ expose une API plate qui se compose d’environ 600 fonctions. Ces fonctions d’API plates sont encapsulées par la classe C++ GdiplusBase.
ms.assetid: b4fcc02c-1b0f-4731-8312-29894b1f722f
title: Fonctions de mémoire
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6ed10574f9cc88c5b7ca8a2b0ed09924fe8c5192
ms.sourcegitcommit: 91530c19d26ba4c57a6af1f37b57f211f580464e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112395824"
---
# <a name="memory-functions"></a><span data-ttu-id="8bec4-104">Fonctions de mémoire</span><span class="sxs-lookup"><span data-stu-id="8bec4-104">Memory Functions</span></span>

<span data-ttu-id="8bec4-105">Windows GDI+ expose une API plate qui se compose d’environ 600 fonctions, qui sont implémentées dans Gdiplus.dll et déclarées dans Gdiplusflat. h.</span><span class="sxs-lookup"><span data-stu-id="8bec4-105">Windows GDI+ exposes a flat API that consists of about 600 functions, which are implemented in Gdiplus.dll and declared in Gdiplusflat.h.</span></span> <span data-ttu-id="8bec4-106">Les fonctions de l’API plate GDI+ sont encapsulées par une collection d’environ 40 classes C++.</span><span class="sxs-lookup"><span data-stu-id="8bec4-106">The functions in the GDI+ flat API are wrapped by a collection of about 40 C++ classes.</span></span> <span data-ttu-id="8bec4-107">Il est recommandé de ne pas appeler directement les fonctions dans l’API plate.</span><span class="sxs-lookup"><span data-stu-id="8bec4-107">It is recommended that you do not directly call the functions in the flat API.</span></span> <span data-ttu-id="8bec4-108">Chaque fois que vous effectuez des appels à GDI+, vous devez le faire en appelant les méthodes et les fonctions fournies par les wrappers C++.</span><span class="sxs-lookup"><span data-stu-id="8bec4-108">Whenever you make calls to GDI+, you should do so by calling the methods and functions provided by the C++ wrappers.</span></span> <span data-ttu-id="8bec4-109">Les services de support technique Microsoft ne fournissent pas de prise en charge du code qui appelle l’API plate directement.</span><span class="sxs-lookup"><span data-stu-id="8bec4-109">Microsoft Product Support Services will not provide support for code that calls the flat API directly.</span></span> <span data-ttu-id="8bec4-110">Pour plus d’informations sur l’utilisation de ces méthodes Wrapper, consultez l' [API plate GDI+](-gdiplus-flatapi-flat.md).</span><span class="sxs-lookup"><span data-stu-id="8bec4-110">For more information on using these wrapper methods, see [GDI+ Flat API](-gdiplus-flatapi-flat.md).</span></span>

<span data-ttu-id="8bec4-111">Les fonctions d’API plates suivantes sont encapsulées par la classe C++ [**GdiplusBase**](/windows/desktop/api/gdiplusbase/nl-gdiplusbase-gdiplusbase) .</span><span class="sxs-lookup"><span data-stu-id="8bec4-111">The following flat API functions are wrapped by the [**GdiplusBase**](/windows/desktop/api/gdiplusbase/nl-gdiplusbase-gdiplusbase) C++ class.</span></span>

## <a name="memory-functions-and-corresponding-wrapper-methods"></a><span data-ttu-id="8bec4-112">Fonctions de mémoire et méthodes Wrapper correspondantes</span><span class="sxs-lookup"><span data-stu-id="8bec4-112">Memory Functions and Corresponding Wrapper Methods</span></span>



| <span data-ttu-id="8bec4-113">Fonction plate</span><span class="sxs-lookup"><span data-stu-id="8bec4-113">Flat function</span></span>                                          | <span data-ttu-id="8bec4-114">Méthode Wrapper</span><span class="sxs-lookup"><span data-stu-id="8bec4-114">Wrapper method</span></span>                                                                                                                                      | <span data-ttu-id="8bec4-115">Remarques</span><span class="sxs-lookup"><span data-stu-id="8bec4-115">Remarks</span></span>                                                                                                      |
|--------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8bec4-116">GpStatus WINGDIPAPI GdipAlloc (taille \_ t taille)</span><span class="sxs-lookup"><span data-stu-id="8bec4-116">GpStatus WINGDIPAPI GdipAlloc(size\_t size)</span></span><br/> | [<span data-ttu-id="8bec4-117">**GpStatus WINGDIPAPI GdiplusBase void \* (operator new) (taille \_ t en \_ taille)**</span><span class="sxs-lookup"><span data-stu-id="8bec4-117">**GpStatus WINGDIPAPI GdiplusBase void\* (operator new)(size\_t in\_size)**</span></span>](/windows/win32/api/gdiplusbase/nf-gdiplusbase-gdiplusbase-operatornew)<br/>      | <span data-ttu-id="8bec4-118">Alloue de la mémoire pour un objet GDI+ Windows.</span><span class="sxs-lookup"><span data-stu-id="8bec4-118">Allocates memory for one Windows GDI+ object.</span></span> <br/> <span data-ttu-id="8bec4-119">GdipAlloc est déclaré dans GdiplusMem. h.</span><span class="sxs-lookup"><span data-stu-id="8bec4-119">GdipAlloc is declared in GdiplusMem.h.</span></span><br/>  |
| <span data-ttu-id="8bec4-120">GpStatus WINGDIPAPI GdipFree (void \* PTR);</span><span class="sxs-lookup"><span data-stu-id="8bec4-120">GpStatus WINGDIPAPI GdipFree(void\* ptr);</span></span><br/>   | [<span data-ttu-id="8bec4-121">**GpStatus WINGDIPAPI GdiplusBase void (opérateur delete) (void \* dans \_ pVoid)**</span><span class="sxs-lookup"><span data-stu-id="8bec4-121">**GpStatus WINGDIPAPI GdiplusBase void (operator delete)(void\* in\_pVoid)**</span></span>](/windows/win32/api/gdiplusbase/nf-gdiplusbase-gdiplusbase-operatordelete)<br/> | <span data-ttu-id="8bec4-122">Libère de la mémoire pour un objet GDI+ Windows.</span><span class="sxs-lookup"><span data-stu-id="8bec4-122">Deallocates memory for one Windows GDI+ object.</span></span> <br/> <span data-ttu-id="8bec4-123">GdipFree est déclaré dans GdiplusMem. h.</span><span class="sxs-lookup"><span data-stu-id="8bec4-123">GdipFree is declared in GdiplusMem.h.</span></span><br/> |



 

 

 
