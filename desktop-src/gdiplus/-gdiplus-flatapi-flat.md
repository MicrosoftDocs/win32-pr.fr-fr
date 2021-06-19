---
description: Windows GDI+ expose une API plate qui se compose d’environ 600 fonctions. Microsoft .NET Framework fournit un ensemble de classes wrapper de code managé pour GDI+.
ms.assetid: afd8cf81-8a20-4592-bd0a-46341742cc9b
title: API plate GDI+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 65f91c3c925b7de31f27e91c70cbd1bf0cbbb2a4
ms.sourcegitcommit: 91530c19d26ba4c57a6af1f37b57f211f580464e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112394984"
---
# <a name="gdi-flat-api"></a><span data-ttu-id="c5c7b-104">API plate GDI+</span><span class="sxs-lookup"><span data-stu-id="c5c7b-104">GDI+ Flat API</span></span>

<span data-ttu-id="c5c7b-105">Windows GDI+ expose une API plate qui se compose d’environ 600 fonctions, qui sont implémentées dans Gdiplus.dll et déclarées dans Gdiplusflat. h.</span><span class="sxs-lookup"><span data-stu-id="c5c7b-105">Windows GDI+ exposes a flat API that consists of about 600 functions, which are implemented in Gdiplus.dll and declared in Gdiplusflat.h.</span></span> <span data-ttu-id="c5c7b-106">Les fonctions de l’API plate GDI+ sont encapsulées par une collection d’environ 40 classes C++.</span><span class="sxs-lookup"><span data-stu-id="c5c7b-106">The functions in the GDI+ flat API are wrapped by a collection of about 40 C++ classes.</span></span> <span data-ttu-id="c5c7b-107">Il est recommandé de ne pas appeler directement les fonctions dans l’API plate.</span><span class="sxs-lookup"><span data-stu-id="c5c7b-107">It is recommended that you do not directly call the functions in the flat API.</span></span> <span data-ttu-id="c5c7b-108">Chaque fois que vous effectuez des appels à GDI+, vous devez le faire en appelant les méthodes et les fonctions fournies par les wrappers C++.</span><span class="sxs-lookup"><span data-stu-id="c5c7b-108">Whenever you make calls to GDI+, you should do so by calling the methods and functions provided by the C++ wrappers.</span></span> <span data-ttu-id="c5c7b-109">Les services de support technique Microsoft ne fournissent pas de prise en charge du code qui appelle l’API plate directement.</span><span class="sxs-lookup"><span data-stu-id="c5c7b-109">Microsoft Product Support Services will not provide support for code that calls the flat API directly.</span></span>

<span data-ttu-id="c5c7b-110">Comme alternative aux wrappers C++, l’infrastructure Microsoft .NET fournit un ensemble de classes wrapper de code managé pour GDI+.</span><span class="sxs-lookup"><span data-stu-id="c5c7b-110">As an alternative to the C++ wrappers, the Microsoft .NET Framework provides a set of managed-code wrapper classes for GDI+.</span></span> <span data-ttu-id="c5c7b-111">Les wrappers de code managé pour GDI+ appartiennent aux espaces de noms suivants.</span><span class="sxs-lookup"><span data-stu-id="c5c7b-111">The managed-code wrappers for GDI+ belong to the following namespaces.</span></span>

-   [<span data-ttu-id="c5c7b-112">System.Drawing</span><span class="sxs-lookup"><span data-stu-id="c5c7b-112">System.Drawing</span></span>](/dotnet/api/system.drawing?view=dotnet-plat-ext-3.1&preserve-view=true)
-   [<span data-ttu-id="c5c7b-113">System. Drawing. Drawing2D</span><span class="sxs-lookup"><span data-stu-id="c5c7b-113">System.Drawing.Drawing2D</span></span>](/dotnet/api/system.drawing.drawing2d?view=dotnet-plat-ext-3.1&preserve-view=true)
-   [<span data-ttu-id="c5c7b-114">System. Drawing. Imaging</span><span class="sxs-lookup"><span data-stu-id="c5c7b-114">System.Drawing.Imaging</span></span>](/dotnet/api/system.drawing.imaging?view=dotnet-plat-ext-3.1&preserve-view=true)
-   [<span data-ttu-id="c5c7b-115">System. Drawing. Text</span><span class="sxs-lookup"><span data-stu-id="c5c7b-115">System.Drawing.Text</span></span>](/dotnet/api/system.drawing.text?view=dotnet-plat-ext-3.1&preserve-view=true)

<span data-ttu-id="c5c7b-116">Les deux jeux de wrappers (C++ et code managé) utilisent une approche orientée objet. il existe donc des différences entre la façon dont les paramètres sont passés aux méthodes Wrapper et la façon dont les paramètres sont passés aux fonctions dans l’API plate.</span><span class="sxs-lookup"><span data-stu-id="c5c7b-116">Both sets of wrappers (C++ and managed code) use an object-oriented approach, so there are some differences between the way parameters are passed to the wrapper methods and the way parameters are passed to functions in the flat API.</span></span> <span data-ttu-id="c5c7b-117">Par exemple, l’un des wrappers C++ est la classe [**Matrix**](/windows/win32/api/gdiplusmatrix/nl-gdiplusmatrix-matrix) .</span><span class="sxs-lookup"><span data-stu-id="c5c7b-117">For example, one of the C++ wrappers is the [**Matrix**](/windows/win32/api/gdiplusmatrix/nl-gdiplusmatrix-matrix) class.</span></span> <span data-ttu-id="c5c7b-118">Chaque objet **Matrix** a un champ, **nativeMatrix**, qui pointe vers une variable interne de type **GpMatrix**.</span><span class="sxs-lookup"><span data-stu-id="c5c7b-118">Each **Matrix** object has a field, **nativeMatrix**, that points to an internal variable of type **GpMatrix**.</span></span> <span data-ttu-id="c5c7b-119">Lorsque vous transmettez des paramètres à une méthode d’un objet **Matrix** , cette méthode passe ces paramètres (ou un ensemble de paramètres connexes) à l’une des fonctions de l’API plate GDI+.</span><span class="sxs-lookup"><span data-stu-id="c5c7b-119">When you pass parameters to a method of a **Matrix** object, that method passes those parameters (or a set of related parameters) along to one of the functions in the GDI+ flat API.</span></span> <span data-ttu-id="c5c7b-120">Toutefois, cette méthode transmet également le champ **nativeMatrix** (en tant que paramètre d’entrée) à la fonction d’API plate.</span><span class="sxs-lookup"><span data-stu-id="c5c7b-120">But that method also passes the **nativeMatrix** field (as an input parameter) to the flat API function.</span></span> <span data-ttu-id="c5c7b-121">Le code suivant montre comment la méthode [**Matrix :: Shear**](/windows/win32/api/Gdiplusmatrix/nf-gdiplusmatrix-matrix-shear) appelle la fonction **GdipShearMatrix (GPMATRIX \* Matrix, Real shearX, Real cisaillement, GpMatrixOrder Order)** .</span><span class="sxs-lookup"><span data-stu-id="c5c7b-121">The following code shows how the [**Matrix::Shear**](/windows/win32/api/Gdiplusmatrix/nf-gdiplusmatrix-matrix-shear) method calls the **GdipShearMatrix(GpMatrix \*matrix, REAL shearX, REAL shearY, GpMatrixOrder order)** function.</span></span>


```
Status Shear(
      IN REAL shearX, 
      IN REAL shearY,
      IN MatrixOrder order = MatrixOrderPrepend)
{
   ...
   GdipShearMatrix(nativeMatrix, shearX, shearY, order);
   ...
}
```



<span data-ttu-id="c5c7b-122">Les constructeurs de [**matrice**](/windows/win32/api/gdiplusmatrix/nl-gdiplusmatrix-matrix) passent l’adresse d’une variable de pointeur **GpMatrix** (en tant que paramètre de sortie) à la fonction **GdipCreateMatrix (GpMatrix \* \* Matrix)** .</span><span class="sxs-lookup"><span data-stu-id="c5c7b-122">The [**Matrix**](/windows/win32/api/gdiplusmatrix/nl-gdiplusmatrix-matrix) constructors pass the address of a **GpMatrix** pointer variable (as an output parameter) to the **GdipCreateMatrix(GpMatrix \*\*matrix)** function.</span></span> <span data-ttu-id="c5c7b-123">**GdipCreateMatrix** crée et Initialise une variable **GpMatrix** interne, puis assigne l’adresse du **GpMatrix** à la variable pointeur.</span><span class="sxs-lookup"><span data-stu-id="c5c7b-123">**GdipCreateMatrix** creates and initializes an internal **GpMatrix** variable and then assigns the address of the **GpMatrix** to the pointer variable.</span></span> <span data-ttu-id="c5c7b-124">Le constructeur copie ensuite la valeur du pointeur dans le champ **nativeMatrix** .</span><span class="sxs-lookup"><span data-stu-id="c5c7b-124">Then the constructor copies the value of the pointer to the **nativeMatrix** field.</span></span>


```
Matrix()
{
   GpMatrix *matrix = NULL;
   lastResult = DllExports::GdipCreateMatrix(&matrix);
   SetNativeMatrix(matrix);
}

VOID SetNativeMatrix(GpMatrix *nativeMatrix)
{
   this->nativeMatrix = nativeMatrix;
}
```



<span data-ttu-id="c5c7b-125">Les méthodes de clonage dans les classes wrapper ne reçoivent pas de paramètres, mais transmettent souvent deux paramètres à la fonction sous-jacente dans l’API plate GDI+.</span><span class="sxs-lookup"><span data-stu-id="c5c7b-125">Clone methods in the wrapper classes receive no parameters but often pass two parameters to the underlying function in the GDI+ flat API.</span></span> <span data-ttu-id="c5c7b-126">Par exemple, la méthode [**Matrix :: Clone**](/windows/win32/api/Gdiplusmatrix/nf-gdiplusmatrix-matrix-clone) passe **nativeMatrix** (comme paramètre d’entrée) et l’adresse d’une variable de pointeur **GpMatrix** (en tant que paramètre de sortie) à la fonction **GdipCloneMatrix** .</span><span class="sxs-lookup"><span data-stu-id="c5c7b-126">For example, the [**Matrix::Clone**](/windows/win32/api/Gdiplusmatrix/nf-gdiplusmatrix-matrix-clone) method passes **nativeMatrix** (as an input parameter) and the address of a **GpMatrix** pointer variable (as an output parameter) to the **GdipCloneMatrix** function.</span></span> <span data-ttu-id="c5c7b-127">Le code suivant montre comment la méthode **Matrix :: Clone** appelle la fonction **GdipCloneMatrix (GpMatrix \* Matrix, GpMatrix \* \* cloneMatrix)** .</span><span class="sxs-lookup"><span data-stu-id="c5c7b-127">The following code shows how the **Matrix::Clone** method calls the **GdipCloneMatrix(GpMatrix \*matrix, GpMatrix \*\*cloneMatrix)** function.</span></span>


```
Matrix *Clone() const
{
   GpMatrix *cloneMatrix = NULL;
   ...
   GdipCloneMatrix(nativeMatrix, &cloneMatrix));
   ...
   return new Matrix(cloneMatrix);
 }
```



<span data-ttu-id="c5c7b-128">Les fonctions de l’API plate retournent une valeur de type GpStatus.</span><span class="sxs-lookup"><span data-stu-id="c5c7b-128">The functions in the flat API return a value of type GpStatus.</span></span> <span data-ttu-id="c5c7b-129">L’énumération GpStatus est identique à l’énumération d' [**État**](/windows/win32/api/Gdiplustypes/ne-gdiplustypes-status) utilisée par les méthodes wrapper.</span><span class="sxs-lookup"><span data-stu-id="c5c7b-129">The GpStatus enumeration is identical to the [**Status**](/windows/win32/api/Gdiplustypes/ne-gdiplustypes-status) enumeration used by the wrapper methods.</span></span> <span data-ttu-id="c5c7b-130">Dans GdiplusGpStubs. h, GpStatus est défini comme suit :</span><span class="sxs-lookup"><span data-stu-id="c5c7b-130">In GdiplusGpStubs.h, GpStatus is defined as follows:</span></span>

`typedef Status GpStatus;`

<span data-ttu-id="c5c7b-131">La plupart des méthodes des classes wrapper retournent une valeur d’État qui indique si la méthode a réussi.</span><span class="sxs-lookup"><span data-stu-id="c5c7b-131">Most of the methods in the wrapper classes return a status value that indicates whether the method succeeded.</span></span> <span data-ttu-id="c5c7b-132">Toutefois, certaines des méthodes de wrapper retournent des valeurs d’État.</span><span class="sxs-lookup"><span data-stu-id="c5c7b-132">However, some of the wrapper methods return state values.</span></span> <span data-ttu-id="c5c7b-133">Quand vous appelez une méthode wrapper qui retourne une valeur d’État, la méthode wrapper passe les paramètres appropriés à la fonction sous-jacente dans l’API plate GDI+.</span><span class="sxs-lookup"><span data-stu-id="c5c7b-133">When you call a wrapper method that returns a state value, the wrapper method passes the appropriate parameters to the underlying function in the GDI+ flat API.</span></span> <span data-ttu-id="c5c7b-134">Par exemple, la [**classe Matrix**](/windows/win32/api/gdiplusmatrix/nl-gdiplusmatrix-matrix) a une [**méthode Matrix :: IsInvertible**](/windows/win32/api/Gdiplusmatrix/nf-gdiplusmatrix-matrix-isinvertible) qui transmet le champ **nativeMatrix** et l’adresse d’une variable **bool** (en tant que paramètre de sortie) à la fonction **GdipIsMatrixInvertible** .</span><span class="sxs-lookup"><span data-stu-id="c5c7b-134">For example, the [**Matrix**](/windows/win32/api/gdiplusmatrix/nl-gdiplusmatrix-matrix) class has an [**Matrix::IsInvertible**](/windows/win32/api/Gdiplusmatrix/nf-gdiplusmatrix-matrix-isinvertible) method that passes the **nativeMatrix** field and and the address of a **BOOL** variable (as an output parameter) to the **GdipIsMatrixInvertible** function.</span></span> <span data-ttu-id="c5c7b-135">Le code suivant montre comment la méthode **Matrix :: IsInvertible** appelle la fonction **GdipIsMatrixInvertible (GDIPCONST GPMATRIX \* Matrix, bool \* result)** .</span><span class="sxs-lookup"><span data-stu-id="c5c7b-135">The following code shows how the **Matrix::IsInvertible** method calls the **GdipIsMatrixInvertible(GDIPCONST GpMatrix \*matrix, BOOL \*result)** function.</span></span>


```
BOOL IsInvertible() const
{
   BOOL result = FALSE;
   ...
   GdipIsMatrixInvertible(nativeMatrix, &result);
   return result;
}
```



<span data-ttu-id="c5c7b-136">Un autre des wrappers est la classe [**Color**](/windows/win32/api/gdipluscolor/nl-gdipluscolor-color) .</span><span class="sxs-lookup"><span data-stu-id="c5c7b-136">Another one of the wrappers is the [**Color**](/windows/win32/api/gdipluscolor/nl-gdipluscolor-color) class.</span></span> <span data-ttu-id="c5c7b-137">Un objet **Color** contient un champ unique de type **ARGB**, qui est défini en tant que **valeur DWORD**.</span><span class="sxs-lookup"><span data-stu-id="c5c7b-137">A **Color** object has a single field of type **ARGB**, which is defined as a **DWORD**.</span></span> <span data-ttu-id="c5c7b-138">Quand vous transmettez un objet **Color** à l’une des méthodes Wrapper, cette méthode passe le champ **ARGB** à la fonction sous-jacente dans l’API plate GDI+.</span><span class="sxs-lookup"><span data-stu-id="c5c7b-138">When you pass a **Color** object to one of the wrapper methods, that method passes the **ARGB** field along to the underlying function in the GDI+ flat API.</span></span> <span data-ttu-id="c5c7b-139">Le code suivant montre comment la méthode [**Pen :: setColor**](/windows/win32/api/Gdipluspen/nf-gdipluspen-pen-setcolor) appelle la fonction **GdipSetPenColor (GPPEN \* Pen, ARGB ARVB)** .</span><span class="sxs-lookup"><span data-stu-id="c5c7b-139">The following code shows how the [**Pen::SetColor**](/windows/win32/api/Gdipluspen/nf-gdipluspen-pen-setcolor) method calls the **GdipSetPenColor(GpPen \*pen, ARGB argb)** function.</span></span> <span data-ttu-id="c5c7b-140">La méthode [**Color :: GetValue**](/windows/win32/api/Gdipluscolor/nf-gdipluscolor-color-getvalue) retourne la valeur du champ **ARGB** .</span><span class="sxs-lookup"><span data-stu-id="c5c7b-140">The [**Color::GetValue**](/windows/win32/api/Gdipluscolor/nf-gdipluscolor-color-getvalue) method returns the value of the **ARGB** field.</span></span>


```
Status SetColor(IN const Color& color)
{
   ...
   GdipSetPenColor(nativePen, color.GetValue());
}
```



<span data-ttu-id="c5c7b-141">Les rubriques suivantes montrent la relation entre l’API plate GDI+ et les méthodes Wrapper C++.</span><span class="sxs-lookup"><span data-stu-id="c5c7b-141">The following topics show the relationship between the GDI+ flat API and the C++ wrapper methods.</span></span>

-   [<span data-ttu-id="c5c7b-142">AdjustableArrowCap, fonctions</span><span class="sxs-lookup"><span data-stu-id="c5c7b-142">AdjustableArrowCap Functions</span></span>](-gdiplus-adjustablearrowcap-flat.md)
-   [<span data-ttu-id="c5c7b-143">Fonctions bitmap</span><span class="sxs-lookup"><span data-stu-id="c5c7b-143">Bitmap Functions</span></span>](-gdiplus-bitmap-flat.md)
-   [<span data-ttu-id="c5c7b-144">Fonctions de pinceau</span><span class="sxs-lookup"><span data-stu-id="c5c7b-144">Brush Functions</span></span>](-gdiplus-brush-flat.md)
-   [<span data-ttu-id="c5c7b-145">CachedBitmap, fonctions</span><span class="sxs-lookup"><span data-stu-id="c5c7b-145">CachedBitmap Functions</span></span>](-gdiplus-cachedbitmap-flat.md)
-   [<span data-ttu-id="c5c7b-146">CustomLineCap, fonctions</span><span class="sxs-lookup"><span data-stu-id="c5c7b-146">CustomLineCap Functions</span></span>](-gdiplus-customlinecap-flat.md)
-   [<span data-ttu-id="c5c7b-147">Fonctions de police</span><span class="sxs-lookup"><span data-stu-id="c5c7b-147">Font Functions</span></span>](-gdiplus-font-flat.md)
-   [<span data-ttu-id="c5c7b-148">FontFamilyFunctions</span><span class="sxs-lookup"><span data-stu-id="c5c7b-148">FontFamilyFunctions</span></span>](-gdiplus-fontfamily-flat.md)
-   [<span data-ttu-id="c5c7b-149">Fonctions Graphics</span><span class="sxs-lookup"><span data-stu-id="c5c7b-149">Graphics Functions</span></span>](-gdiplus-graphics-flat.md)
-   [<span data-ttu-id="c5c7b-150">GraphicsPath, fonctions</span><span class="sxs-lookup"><span data-stu-id="c5c7b-150">GraphicsPath Functions</span></span>](-gdiplus-graphicspath-flat.md)
-   [<span data-ttu-id="c5c7b-151">Fonctions HatchBrush</span><span class="sxs-lookup"><span data-stu-id="c5c7b-151">HatchBrush Functions</span></span>](-gdiplus-hatchbrush-flat.md)
-   [<span data-ttu-id="c5c7b-152">Fonctions image</span><span class="sxs-lookup"><span data-stu-id="c5c7b-152">Image Functions</span></span>](-gdiplus-image-flat.md)
-   [<span data-ttu-id="c5c7b-153">ImageAttributes, fonctions</span><span class="sxs-lookup"><span data-stu-id="c5c7b-153">ImageAttributes Functions</span></span>](-gdiplus-imageattributes-flat.md)
-   [<span data-ttu-id="c5c7b-154">LinearGradientBrush, fonctions</span><span class="sxs-lookup"><span data-stu-id="c5c7b-154">LinearGradientBrush Functions</span></span>](-gdiplus-lineargradientbrush-flat.md)
-   [<span data-ttu-id="c5c7b-155">Fonctions de matrice</span><span class="sxs-lookup"><span data-stu-id="c5c7b-155">Matrix Functions</span></span>](-gdiplus-matrix-flat.md)
-   [<span data-ttu-id="c5c7b-156">Fonctions de mémoire</span><span class="sxs-lookup"><span data-stu-id="c5c7b-156">Memory Functions</span></span>](-gdiplus-memory-flat.md)
-   [<span data-ttu-id="c5c7b-157">Fonctions de notification</span><span class="sxs-lookup"><span data-stu-id="c5c7b-157">Notification Functions</span></span>](-gdiplus-notification-flat.md)
-   [<span data-ttu-id="c5c7b-158">PathGradientBrush, fonctions</span><span class="sxs-lookup"><span data-stu-id="c5c7b-158">PathGradientBrush Functions</span></span>](-gdiplus-pathgradientbrush-flat.md)
-   [<span data-ttu-id="c5c7b-159">PathIterator, fonctions</span><span class="sxs-lookup"><span data-stu-id="c5c7b-159">PathIterator Functions</span></span>](-gdiplus-pathiterator-flat.md)
-   [<span data-ttu-id="c5c7b-160">Fonctions de stylet</span><span class="sxs-lookup"><span data-stu-id="c5c7b-160">Pen Functions</span></span>](-gdiplus-pen-flat.md)
-   [<span data-ttu-id="c5c7b-161">Fonctions de région</span><span class="sxs-lookup"><span data-stu-id="c5c7b-161">Region Functions</span></span>](-gdiplus-region-flat.md)
-   [<span data-ttu-id="c5c7b-162">Fonctions SolidBrush</span><span class="sxs-lookup"><span data-stu-id="c5c7b-162">SolidBrush Functions</span></span>](-gdiplus-solidbrush-flat.md)
-   [<span data-ttu-id="c5c7b-163">Fonctions de format de chaîne</span><span class="sxs-lookup"><span data-stu-id="c5c7b-163">String Format Functions</span></span>](-gdiplus-stringformat-flat.md)
-   [<span data-ttu-id="c5c7b-164">Fonctions de texte</span><span class="sxs-lookup"><span data-stu-id="c5c7b-164">Text Functions</span></span>](-gdiplus-text-flat.md)
-   [<span data-ttu-id="c5c7b-165">Fonctions de pinceau de texture</span><span class="sxs-lookup"><span data-stu-id="c5c7b-165">Texture Brush Functions</span></span>](-gdiplus-texturebrush-flat.md)

 

 
