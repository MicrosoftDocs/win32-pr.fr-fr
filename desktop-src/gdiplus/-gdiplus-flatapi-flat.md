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
# <a name="gdi-flat-api"></a>API plate GDI+

Windows GDI+ expose une API plate qui se compose d’environ 600 fonctions, qui sont implémentées dans Gdiplus.dll et déclarées dans Gdiplusflat. h. Les fonctions de l’API plate GDI+ sont encapsulées par une collection d’environ 40 classes C++. Il est recommandé de ne pas appeler directement les fonctions dans l’API plate. Chaque fois que vous effectuez des appels à GDI+, vous devez le faire en appelant les méthodes et les fonctions fournies par les wrappers C++. Les services de support technique Microsoft ne fournissent pas de prise en charge du code qui appelle l’API plate directement.

Comme alternative aux wrappers C++, l’infrastructure Microsoft .NET fournit un ensemble de classes wrapper de code managé pour GDI+. Les wrappers de code managé pour GDI+ appartiennent aux espaces de noms suivants.

-   [System.Drawing](/dotnet/api/system.drawing?view=dotnet-plat-ext-3.1&preserve-view=true)
-   [System. Drawing. Drawing2D](/dotnet/api/system.drawing.drawing2d?view=dotnet-plat-ext-3.1&preserve-view=true)
-   [System. Drawing. Imaging](/dotnet/api/system.drawing.imaging?view=dotnet-plat-ext-3.1&preserve-view=true)
-   [System. Drawing. Text](/dotnet/api/system.drawing.text?view=dotnet-plat-ext-3.1&preserve-view=true)

Les deux jeux de wrappers (C++ et code managé) utilisent une approche orientée objet. il existe donc des différences entre la façon dont les paramètres sont passés aux méthodes Wrapper et la façon dont les paramètres sont passés aux fonctions dans l’API plate. Par exemple, l’un des wrappers C++ est la classe [**Matrix**](/windows/win32/api/gdiplusmatrix/nl-gdiplusmatrix-matrix) . Chaque objet **Matrix** a un champ, **nativeMatrix**, qui pointe vers une variable interne de type **GpMatrix**. Lorsque vous transmettez des paramètres à une méthode d’un objet **Matrix** , cette méthode passe ces paramètres (ou un ensemble de paramètres connexes) à l’une des fonctions de l’API plate GDI+. Toutefois, cette méthode transmet également le champ **nativeMatrix** (en tant que paramètre d’entrée) à la fonction d’API plate. Le code suivant montre comment la méthode [**Matrix :: Shear**](/windows/win32/api/Gdiplusmatrix/nf-gdiplusmatrix-matrix-shear) appelle la fonction **GdipShearMatrix (GPMATRIX \* Matrix, Real shearX, Real cisaillement, GpMatrixOrder Order)** .


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



Les constructeurs de [**matrice**](/windows/win32/api/gdiplusmatrix/nl-gdiplusmatrix-matrix) passent l’adresse d’une variable de pointeur **GpMatrix** (en tant que paramètre de sortie) à la fonction **GdipCreateMatrix (GpMatrix \* \* Matrix)** . **GdipCreateMatrix** crée et Initialise une variable **GpMatrix** interne, puis assigne l’adresse du **GpMatrix** à la variable pointeur. Le constructeur copie ensuite la valeur du pointeur dans le champ **nativeMatrix** .


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



Les méthodes de clonage dans les classes wrapper ne reçoivent pas de paramètres, mais transmettent souvent deux paramètres à la fonction sous-jacente dans l’API plate GDI+. Par exemple, la méthode [**Matrix :: Clone**](/windows/win32/api/Gdiplusmatrix/nf-gdiplusmatrix-matrix-clone) passe **nativeMatrix** (comme paramètre d’entrée) et l’adresse d’une variable de pointeur **GpMatrix** (en tant que paramètre de sortie) à la fonction **GdipCloneMatrix** . Le code suivant montre comment la méthode **Matrix :: Clone** appelle la fonction **GdipCloneMatrix (GpMatrix \* Matrix, GpMatrix \* \* cloneMatrix)** .


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



Les fonctions de l’API plate retournent une valeur de type GpStatus. L’énumération GpStatus est identique à l’énumération d' [**État**](/windows/win32/api/Gdiplustypes/ne-gdiplustypes-status) utilisée par les méthodes wrapper. Dans GdiplusGpStubs. h, GpStatus est défini comme suit :

`typedef Status GpStatus;`

La plupart des méthodes des classes wrapper retournent une valeur d’État qui indique si la méthode a réussi. Toutefois, certaines des méthodes de wrapper retournent des valeurs d’État. Quand vous appelez une méthode wrapper qui retourne une valeur d’État, la méthode wrapper passe les paramètres appropriés à la fonction sous-jacente dans l’API plate GDI+. Par exemple, la [**classe Matrix**](/windows/win32/api/gdiplusmatrix/nl-gdiplusmatrix-matrix) a une [**méthode Matrix :: IsInvertible**](/windows/win32/api/Gdiplusmatrix/nf-gdiplusmatrix-matrix-isinvertible) qui transmet le champ **nativeMatrix** et l’adresse d’une variable **bool** (en tant que paramètre de sortie) à la fonction **GdipIsMatrixInvertible** . Le code suivant montre comment la méthode **Matrix :: IsInvertible** appelle la fonction **GdipIsMatrixInvertible (GDIPCONST GPMATRIX \* Matrix, bool \* result)** .


```
BOOL IsInvertible() const
{
   BOOL result = FALSE;
   ...
   GdipIsMatrixInvertible(nativeMatrix, &result);
   return result;
}
```



Un autre des wrappers est la classe [**Color**](/windows/win32/api/gdipluscolor/nl-gdipluscolor-color) . Un objet **Color** contient un champ unique de type **ARGB**, qui est défini en tant que **valeur DWORD**. Quand vous transmettez un objet **Color** à l’une des méthodes Wrapper, cette méthode passe le champ **ARGB** à la fonction sous-jacente dans l’API plate GDI+. Le code suivant montre comment la méthode [**Pen :: setColor**](/windows/win32/api/Gdipluspen/nf-gdipluspen-pen-setcolor) appelle la fonction **GdipSetPenColor (GPPEN \* Pen, ARGB ARVB)** . La méthode [**Color :: GetValue**](/windows/win32/api/Gdipluscolor/nf-gdipluscolor-color-getvalue) retourne la valeur du champ **ARGB** .


```
Status SetColor(IN const Color& color)
{
   ...
   GdipSetPenColor(nativePen, color.GetValue());
}
```



Les rubriques suivantes montrent la relation entre l’API plate GDI+ et les méthodes Wrapper C++.

-   [AdjustableArrowCap, fonctions](-gdiplus-adjustablearrowcap-flat.md)
-   [Fonctions bitmap](-gdiplus-bitmap-flat.md)
-   [Fonctions de pinceau](-gdiplus-brush-flat.md)
-   [CachedBitmap, fonctions](-gdiplus-cachedbitmap-flat.md)
-   [CustomLineCap, fonctions](-gdiplus-customlinecap-flat.md)
-   [Fonctions de police](-gdiplus-font-flat.md)
-   [FontFamilyFunctions](-gdiplus-fontfamily-flat.md)
-   [Fonctions Graphics](-gdiplus-graphics-flat.md)
-   [GraphicsPath, fonctions](-gdiplus-graphicspath-flat.md)
-   [Fonctions HatchBrush](-gdiplus-hatchbrush-flat.md)
-   [Fonctions image](-gdiplus-image-flat.md)
-   [ImageAttributes, fonctions](-gdiplus-imageattributes-flat.md)
-   [LinearGradientBrush, fonctions](-gdiplus-lineargradientbrush-flat.md)
-   [Fonctions de matrice](-gdiplus-matrix-flat.md)
-   [Fonctions de mémoire](-gdiplus-memory-flat.md)
-   [Fonctions de notification](-gdiplus-notification-flat.md)
-   [PathGradientBrush, fonctions](-gdiplus-pathgradientbrush-flat.md)
-   [PathIterator, fonctions](-gdiplus-pathiterator-flat.md)
-   [Fonctions de stylet](-gdiplus-pen-flat.md)
-   [Fonctions de région](-gdiplus-region-flat.md)
-   [Fonctions SolidBrush](-gdiplus-solidbrush-flat.md)
-   [Fonctions de format de chaîne](-gdiplus-stringformat-flat.md)
-   [Fonctions de texte](-gdiplus-text-flat.md)
-   [Fonctions de pinceau de texture](-gdiplus-texturebrush-flat.md)

 

 
