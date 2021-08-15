---
title: Effet composite arithmétique
description: Utilisez l’effet composite arithmétique pour combiner 2 images à l’aide d’une somme pondérée de pixels à partir des images d’entrée.
ms.assetid: 6EC8CD61-5B51-4A8E-8A61-B291ABB5C5E0
keywords:
- effet composite arithmétique
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e45976d577299bda7dfcef9bf20eff4980cc67ac105cb14fa793065d7ce1857f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119641959"
---
# <a name="arithmetic-composite-effect"></a>Effet composite arithmétique

Utilisez l’effet composite arithmétique pour combiner 2 images à l’aide d’une somme pondérée de pixels à partir des images d’entrée.

Le CLSID de cet effet est CLSID \_ D2D1ArithmeticComposite.

-   [Formule](#formula)
-   [Exemple d’image](#example-image)
-   [Propriétés d’effet](#effect-properties)
-   [Bitmap de sortie](#output-bitmap)
-   [Requirements](#requirements)
-   [Rubriques connexes](#related-topics)

## <a name="formula"></a>Formule

La formule ici est utilisée pour calculer cet effet.

En sortie<sub>RVBA</sub> = C1 \* source<sub>RVBA</sub> \* destination<sub>RVBA</sub> + C2 \* source<sub>RVBA</sub> + C3 \* destination<sub>RVBA</sub> + C4

Où C1, C2, C3, C4 sont des coefficients que vous définissez.

Les coefficients correspondent aux valeurs d’un vecteur D2D1 \_ \_ 4F (x, y, z, w) :

-   x = C1
-   y = C2
-   z = C3
-   w = C4

## <a name="example-image"></a>Exemple d’image

Un exemple simple consiste à ajouter les pixels source et de destination. Dans l’exemple, 2 rectangles arrondis sont composés ensemble. Le rectangle source est bleu et la destination est rouge.

L’image ici est la sortie de l’effet composite arithmétique avec les coefficients de l’équation définie sur les valeurs ici.

-   C1 = 0
-   C2 = 1
-   C3 = 1
-   C4 = 0

![exemple d’image indiquant 2 rectangles arrondis de la même taille qui se chevauchent à l’aide de l’effet composite arithmétique.](images/arithmetic-50-percent.png)

Le résultat est que les valeurs en pixels pour la source et la destination sont ajoutées. Les zones où les rectangles ne chevauchent pas les valeurs RVBA sont toutes 0. L’emplacement des rectangles qui chevauchent la couleur est magenta, car les valeurs R et B sont toutes les deux au maximum.

Voici un autre exemple d’image avec du code.



| Avant image 1                                                             |
|----------------------------------------------------------------------------|
| ![première image source avant l’effet.](images/default-before.jpg)    |
| Avant image 2                                                             |
| ![deuxième image avant l’effet.](images/4-arthimetic-composite2.jpg) |
| Après                                                                      |
| ![image après la transformation.](images/4-arithmeticcomposite.png)        |



 


```C++
ComPtr<ID2D1Effect> arithmeticCompositeEffect;
m_d2dContext->CreateEffect(CLSID_D2D1ArithmeticComposite, &arithmeticCompositeEffect);

arithmeticCompositeEffect->SetInput(0, bitmap);
arithmeticCompositeEffect->SetInput(1, bitmapTwo);
arithmeticCompositeEffect->SetValue(D2D1_ARITHMETICCOMPOSITE_PROP_COEFFICIENTS, D2D1::Vector4F(0.0f, 0.5f, 0.5f, 0.0f));

m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(arithmeticCompositeEffect.Get());
m_d2dContext->EndDraw();
```



## <a name="effect-properties"></a>Propriétés d’effet



| Nom complet et énumération d’index                                               | Description                                                                                                                                                                                                                                                                                                                                                                                                                                       |
|----------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Coefficients<br/> \_COefficients d2d1 ARITHMETICCOMPOSITE \_ prop \_<br/> | Coefficients de l’équation utilisée pour composer les deux images d’entrée. Les coefficients sont sans unité et illimités. Le type est D2D1 \_ Vector \_ 4F.<br/> La valeur par défaut est {1.0 f, 0.0 f, 0.0 f, 0.0 f}.<br/>                                                                                                                                                                                                                                 |
| ClampOutput<br/> \_Sortie de Clamp d2d1 ARITHMETICCOMPOSITE \_ prop \_ \_<br/> | L’effet fixe les valeurs de couleur à entre 0 et 1 avant que l’effet ne passe les valeurs à l’effet suivant dans le graphique. <br/> Si vous affectez la valeur TRUE à cet effet, les valeurs sont ancrées. Si vous définissez cette valeur sur FALSe, l’effet n’attache pas les valeurs de couleur, mais d’autres effets et la surface de sortie peuvent fixer les valeurs si elles n’ont pas une précision suffisamment élevée.<br/> Le type est BOOL.<br/> La valeur par défaut est FALSe.<br/> |



 

## <a name="output-bitmap"></a>Bitmap de sortie

La bitmap de sortie dépend des valeurs de coefficient. Il s’agit des tailles de bitmap de sortie possibles.

-   Si C1 est le seul coefficient non nul, la taille de sortie est l’intersection des rectangles d’entrée.
-   Si C2 est le seul coefficient non nul, la taille de sortie est la taille du rectangle source.
-   Si C3 est le seul coefficient non nul, la taille de sortie est la taille du rectangle de destination..
-   Si tous les coefficients sont nuls, la taille de sortie est un rectangle vide.
-   Pour toutes les autres valeurs de coefficient, la taille de sortie est l’Union des rectangles d’entrée.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------------|------------------------------------------------------------------------------------|
| Client minimal pris en charge | mise à jour Windows 8 et de plateforme pour les applications de bureau Windows 7 Windows les applications du windows \[ \| Store\] |
| Serveur minimal pris en charge | mise à jour Windows 8 et de plateforme pour les applications de bureau Windows 7 Windows les applications du windows \[ \| Store\] |
| En-tête                   | d2d1effects. h                                                                      |
| Bibliothèque                  | d2d1. lib, dxguid. lib                                                               |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**ID2D1Effect**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect)
</dt> </dl>

 

