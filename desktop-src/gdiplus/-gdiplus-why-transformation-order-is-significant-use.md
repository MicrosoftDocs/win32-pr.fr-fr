---
description: Un objet matrice unique peut stocker une seule transformation ou une séquence de transformations.
ms.assetid: 1dc68ff8-6b17-4934-82da-ab2fc612aafa
title: Importance de l'ordre des transformations
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a7350d63456902ff47183faa08170b3b2fef481
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104972135"
---
# <a name="why-transformation-order-is-significant"></a><span data-ttu-id="e81ad-103">Importance de l'ordre des transformations</span><span class="sxs-lookup"><span data-stu-id="e81ad-103">Why Transformation Order Is Significant</span></span>

<span data-ttu-id="e81ad-104">Un objet [**matrice**](/windows/desktop/api/gdiplusmatrix/nl-gdiplusmatrix-matrix) unique peut stocker une seule transformation ou une séquence de transformations.</span><span class="sxs-lookup"><span data-stu-id="e81ad-104">A single [**Matrix**](/windows/desktop/api/gdiplusmatrix/nl-gdiplusmatrix-matrix) object can store a single transformation or a sequence of transformations.</span></span> <span data-ttu-id="e81ad-105">Ce dernier est appelé transformation *composite*.  </span><span class="sxs-lookup"><span data-stu-id="e81ad-105">The latter is called a *composite*  *transformation*.</span></span> <span data-ttu-id="e81ad-106">La matrice d’une transformation composite est obtenue en multipliant les matrices des différentes transformations.</span><span class="sxs-lookup"><span data-stu-id="e81ad-106">The matrix of a composite transformation is obtained by multiplying the matrices of the individual transformations.</span></span>

<span data-ttu-id="e81ad-107">Dans une transformation composite, l’ordre des transformations individuelles est important.</span><span class="sxs-lookup"><span data-stu-id="e81ad-107">In a composite transformation, the order of the individual transformations is important.</span></span> <span data-ttu-id="e81ad-108">Par exemple, si vous faites pivoter, puis mettez à l’échelle, puis Traduisez, vous obtenez un résultat différent de celui que vous convertissiez, puis faites pivoter, puis mettez à l’échelle.</span><span class="sxs-lookup"><span data-stu-id="e81ad-108">For example, if you first rotate, then scale, then translate, you get a different result than if you first translate, then rotate, then scale.</span></span> <span data-ttu-id="e81ad-109">Dans Windows GDI+, les transformations composites sont construites de gauche à droite.</span><span class="sxs-lookup"><span data-stu-id="e81ad-109">In Windows GDI+, composite transformations are built from left to right.</span></span> <span data-ttu-id="e81ad-110">Si S, R et T sont respectivement des matrices de mise à l’échelle, de rotation et de translation, le produit SRT (dans cet ordre) est la matrice de la transformation composite qui met à l’échelle, puis pivote, puis effectue une translation.</span><span class="sxs-lookup"><span data-stu-id="e81ad-110">If S, R, and T are scale, rotation, and translation matrices respectively, then the product SRT (in that order) is the matrix of the composite transformation that first scales, then rotates, then translates.</span></span> <span data-ttu-id="e81ad-111">La matrice produite par le logiciel SRT est différente de la matrice produite par le produit TRS.</span><span class="sxs-lookup"><span data-stu-id="e81ad-111">The matrix produced by the product SRT is different from the matrix produced by the product TRS.</span></span>

<span data-ttu-id="e81ad-112">Un ordre de raison important est que les transformations telles que la rotation et la mise à l’échelle sont effectuées par rapport à l’origine du système de coordonnées.</span><span class="sxs-lookup"><span data-stu-id="e81ad-112">One reason order is significant is that transformations like rotation and scaling are done with respect to the origin of the coordinate system.</span></span> <span data-ttu-id="e81ad-113">La mise à l’échelle d’un objet centré à l’origine produit un résultat différent de la mise à l’échelle d’un objet qui a été déplacé hors de l’origine.</span><span class="sxs-lookup"><span data-stu-id="e81ad-113">Scaling an object that is centered at the origin produces a different result than scaling an object that has been moved away from the origin.</span></span> <span data-ttu-id="e81ad-114">De même, la rotation d’un objet centré à l’origine produit un résultat différent de la rotation d’un objet qui a été déplacé à l’extérieur de l’origine.</span><span class="sxs-lookup"><span data-stu-id="e81ad-114">Similarly, rotating an object that is centered at the origin produces a different result than rotating an object that has been moved away from the origin.</span></span>

<span data-ttu-id="e81ad-115">L’exemple suivant combine la mise à l’échelle, la rotation et la translation (dans cet ordre) pour former une transformation composite.</span><span class="sxs-lookup"><span data-stu-id="e81ad-115">The following example combines scaling, rotation and translation (in that order) to form a composite transformation.</span></span> <span data-ttu-id="e81ad-116">L’argument [\* \* \* \* MatrixOrderAppend \* \* \* \*](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-matrixorder) passé à la méthode [**Graphics :: RotateTransform**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-rotatetransform) spécifie que la rotation suivra la mise à l’échelle.</span><span class="sxs-lookup"><span data-stu-id="e81ad-116">The argument [\*\*\*\*MatrixOrderAppend\*\*\*\*](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-matrixorder) passed to the [**Graphics::RotateTransform**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-rotatetransform) method specifies that the rotation will follow the scaling.</span></span> <span data-ttu-id="e81ad-117">De même, l’argument [\* \* \* \* MatrixOrderAppend \* \* \* \*](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-matrixorder) transmis à la méthode [**Graphics :: TranslateTransform**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-translatetransform) spécifie que la translation suivra la rotation.</span><span class="sxs-lookup"><span data-stu-id="e81ad-117">Likewise, the argument [\*\*\*\*MatrixOrderAppend\*\*\*\*](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-matrixorder) passed to the [**Graphics::TranslateTransform**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-translatetransform) method specifies that the translation will follow the rotation.</span></span>


```
Rect rect(0, 0, 50, 50);
Pen pen(Color(255, 255, 0, 0), 0);
graphics.ScaleTransform(1.75f, 0.5f);
graphics.RotateTransform(28.0f, MatrixOrderAppend);
graphics.TranslateTransform(150.0f, 150.0f, MatrixOrderAppend);
graphics.DrawRectangle(&pen, rect);
```



<span data-ttu-id="e81ad-118">L’exemple suivant effectue les mêmes appels de méthode que l’exemple précédent, mais l’ordre des appels est inversé.</span><span class="sxs-lookup"><span data-stu-id="e81ad-118">The following example makes the same method calls as the previous example, but the order of the calls is reversed.</span></span> <span data-ttu-id="e81ad-119">L’ordre des opérations obtenu est tout d’abord converti, puis pivote, puis mis à l’échelle, ce qui produit un résultat très différent de la première échelle, puis pivote, puis translate :</span><span class="sxs-lookup"><span data-stu-id="e81ad-119">The resulting order of operations is first translate, then rotate, then scale, which produces a very different result than first scale, then rotate, then translate:</span></span>


```
Rect rect(0, 0, 50, 50);
Pen pen(Color(255, 255, 0, 0), 0);
graphics.TranslateTransform(150.0f, 150.0f);
graphics.RotateTransform(28.0f, MatrixOrderAppend);
graphics.ScaleTransform(1.75f, 0.5f, MatrixOrderAppend);
graphics.DrawRectangle(&pen, rect);
```



<span data-ttu-id="e81ad-120">Pour inverser l’ordre des transformations individuelles dans une transformation composite, il est possible d’inverser l’ordre d’une séquence d’appels de méthode.</span><span class="sxs-lookup"><span data-stu-id="e81ad-120">One way to reverse the order of the individual transformations in a composite transformation is to reverse the order of a sequence of method calls.</span></span> <span data-ttu-id="e81ad-121">Une deuxième méthode pour contrôler l’ordre des opérations consiste à modifier l’argument de l’ordre de la matrice.</span><span class="sxs-lookup"><span data-stu-id="e81ad-121">A second way to control the order of operations is to change the matrix order argument.</span></span> <span data-ttu-id="e81ad-122">L’exemple suivant est identique à l’exemple précédent, sauf que [\* \* \* \* MatrixOrderAppend \* \*](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-matrixorder) \* \* a été remplacé par \* \* \* \* [MatrixOrderPrepend \*](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-matrixorder)\* \* \*.</span><span class="sxs-lookup"><span data-stu-id="e81ad-122">The following example is the same as the previous example, except that [\*\*\*\*MatrixOrderAppend\*\*\*\*](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-matrixorder) has been changed to [\*\*\*\*MatrixOrderPrepend\*\*\*\*](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-matrixorder).</span></span> <span data-ttu-id="e81ad-123">La multiplication de matrice est effectuée dans l’ordre SRT, où S, R et T sont les matrices pour la mise à l’échelle, la rotation et la translation, respectivement.</span><span class="sxs-lookup"><span data-stu-id="e81ad-123">The matrix multiplication is done in the order SRT, where S, R, and T are the matrices for scale, rotate, and translate, respectively.</span></span> <span data-ttu-id="e81ad-124">L’ordre de la transformation composite est la première mise à l’échelle, puis la rotation, puis la translation.</span><span class="sxs-lookup"><span data-stu-id="e81ad-124">The order of the composite transformation is first scale, then rotate, then translate.</span></span>


```
Rect rect(0, 0, 50, 50);
Pen pen(Color(255, 255, 0, 0), 0);
graphics.TranslateTransform(150.0f, 150.0f,MatrixOrderPrepend);
graphics.RotateTransform(28.0f, MatrixOrderPrepend);
graphics.ScaleTransform(1.75f, 0.5f, MatrixOrderPrepend);
graphics.DrawRectangle(&pen, rect);
```



<span data-ttu-id="e81ad-125">Le résultat de l’exemple précédent est le même résultat que celui obtenu dans le premier exemple de cette section.</span><span class="sxs-lookup"><span data-stu-id="e81ad-125">The result of the preceding example is the same result that we achieved in the first example of this section.</span></span> <span data-ttu-id="e81ad-126">Cela est dû au fait que nous avons inversé à la fois l’ordre des appels de méthode et l’ordre de la multiplication de la matrice.</span><span class="sxs-lookup"><span data-stu-id="e81ad-126">This is because we reversed both the order of the method calls and the order of the matrix multiplication.</span></span>

 

 



