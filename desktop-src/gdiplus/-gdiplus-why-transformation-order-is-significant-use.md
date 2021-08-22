---
description: Un objet matrice unique peut stocker une seule transformation ou une séquence de transformations.
ms.assetid: 1dc68ff8-6b17-4934-82da-ab2fc612aafa
title: Importance de l'ordre des transformations
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b8a7c0c840fa5c2debaccef4450c525bab8cf7f6e4373653eadaf53a6538891
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119359579"
---
# <a name="why-transformation-order-is-significant"></a>Importance de l'ordre des transformations

Un objet [**matrice**](/windows/desktop/api/gdiplusmatrix/nl-gdiplusmatrix-matrix) unique peut stocker une seule transformation ou une séquence de transformations. Ce dernier est appelé transformation *composite*.   La matrice d’une transformation composite est obtenue en multipliant les matrices des différentes transformations.

Dans une transformation composite, l’ordre des transformations individuelles est important. Par exemple, si vous faites pivoter, puis mettez à l’échelle, puis Traduisez, vous obtenez un résultat différent de celui que vous convertissiez, puis faites pivoter, puis mettez à l’échelle. dans Windows GDI+, les transformations composites sont construites de gauche à droite. Si S, R et T sont respectivement des matrices de mise à l’échelle, de rotation et de translation, le produit SRT (dans cet ordre) est la matrice de la transformation composite qui met à l’échelle, puis pivote, puis effectue une translation. La matrice produite par le logiciel SRT est différente de la matrice produite par le produit TRS.

Un ordre de raison important est que les transformations telles que la rotation et la mise à l’échelle sont effectuées par rapport à l’origine du système de coordonnées. La mise à l’échelle d’un objet centré à l’origine produit un résultat différent de la mise à l’échelle d’un objet qui a été déplacé hors de l’origine. De même, la rotation d’un objet centré à l’origine produit un résultat différent de la rotation d’un objet qui a été déplacé à l’extérieur de l’origine.

L’exemple suivant combine la mise à l’échelle, la rotation et la translation (dans cet ordre) pour former une transformation composite. L’argument [* * * * MatrixOrderAppend * * * *](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-matrixorder) passé à la méthode [**Graphics :: RotateTransform**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-rotatetransform) spécifie que la rotation suivra la mise à l’échelle. De même, l’argument [* * * * MatrixOrderAppend * * * *](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-matrixorder) transmis à la méthode [**Graphics :: TranslateTransform**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-translatetransform) spécifie que la translation suivra la rotation.


```
Rect rect(0, 0, 50, 50);
Pen pen(Color(255, 255, 0, 0), 0);
graphics.ScaleTransform(1.75f, 0.5f);
graphics.RotateTransform(28.0f, MatrixOrderAppend);
graphics.TranslateTransform(150.0f, 150.0f, MatrixOrderAppend);
graphics.DrawRectangle(&pen, rect);
```



L’exemple suivant effectue les mêmes appels de méthode que l’exemple précédent, mais l’ordre des appels est inversé. L’ordre des opérations obtenu est tout d’abord converti, puis pivote, puis mis à l’échelle, ce qui produit un résultat très différent de la première échelle, puis pivote, puis translate :


```
Rect rect(0, 0, 50, 50);
Pen pen(Color(255, 255, 0, 0), 0);
graphics.TranslateTransform(150.0f, 150.0f);
graphics.RotateTransform(28.0f, MatrixOrderAppend);
graphics.ScaleTransform(1.75f, 0.5f, MatrixOrderAppend);
graphics.DrawRectangle(&pen, rect);
```



Pour inverser l’ordre des transformations individuelles dans une transformation composite, il est possible d’inverser l’ordre d’une séquence d’appels de méthode. Une deuxième méthode pour contrôler l’ordre des opérations consiste à modifier l’argument de l’ordre de la matrice. L’exemple suivant est identique à l’exemple précédent, sauf que [* * * * MatrixOrderAppend * *](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-matrixorder) * * a été remplacé par * * * * [MatrixOrderPrepend *](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-matrixorder)* * *. La multiplication de matrice est effectuée dans l’ordre SRT, où S, R et T sont les matrices pour la mise à l’échelle, la rotation et la translation, respectivement. L’ordre de la transformation composite est la première mise à l’échelle, puis la rotation, puis la translation.


```
Rect rect(0, 0, 50, 50);
Pen pen(Color(255, 255, 0, 0), 0);
graphics.TranslateTransform(150.0f, 150.0f,MatrixOrderPrepend);
graphics.RotateTransform(28.0f, MatrixOrderPrepend);
graphics.ScaleTransform(1.75f, 0.5f, MatrixOrderPrepend);
graphics.DrawRectangle(&pen, rect);
```



Le résultat de l’exemple précédent est le même résultat que celui obtenu dans le premier exemple de cette section. Cela est dû au fait que nous avons inversé à la fois l’ordre des appels de méthode et l’ordre de la multiplication de la matrice.

 

 



