---
description: Répertorie les fonctions plan fournies par DirectXMath.
ms.assetid: 6505e72e-4af5-5db3-4fc0-f83fa77692b1
title: Fonctions du plan de la bibliothèque DirectXMath
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4a91e58ddad68c31bcc5579b2727891fdddd5b6737761c89d9db70ca21c56bfc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119841199"
---
# <a name="directxmath-library-plane-functions"></a>Fonctions du plan de la bibliothèque DirectXMath

Répertorie les fonctions plan fournies par DirectXMath.

Ces fonctions utilisent un vecteur 4 XMVECTOR pour représenter les coefficients de l’équation plan, ax + par + CZ + D = 0, où le composant X est un, le composant Y est B, le Z-Component est C et le composant W est D.

## <a name="in-this-section"></a>Contenu de cette section



| Rubrique                                                               | Description                                                                                                      |
|---------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------|
| [**XMPlaneDot**](/windows/win32/api/directxmath/nf-directxmath-xmplanedot)<br/>                         | Calcule le produit scalaire entre un plan d’entrée et un vecteur 4D.<br/>                                    |
| [**XMPlaneDotCoord**](/windows/win32/api/directxmath/nf-directxmath-xmplanedotcoord)<br/>               | Calcule le produit scalaire entre un plan d’entrée et un vecteur 3D.<br/>                                    |
| [**XMPlaneDotNormal**](/windows/win32/api/directxmath/nf-directxmath-xmplanedotnormal)<br/>             | Calcule le produit scalaire entre le vecteur normal d’un plan et un vecteur 3D.<br/>                      |
| [**XMPlaneEqual**](/windows/win32/api/directxmath/nf-directxmath-xmplaneequal)<br/>                     | Détermine si deux plans sont égaux.<br/>                                                                   |
| [**XMPlaneFromPointNormal**](/windows/win32/api/directxmath/nf-directxmath-xmplanefrompointnormal)<br/> | Calcule l’équation d’un plan construit à partir d’un point dans le plan et d’un vecteur normal.<br/>           |
| [**XMPlaneFromPoints**](/windows/win32/api/directxmath/nf-directxmath-xmplanefrompoints)<br/>           | Calcule l’équation d’un plan construit à partir de trois points dans le plan.<br/>                          |
| [**XMPlaneIntersectLine**](/windows/win32/api/directxmath/nf-directxmath-xmplaneintersectline)<br/>     | Recherche l’intersection entre un plan et une ligne.<br/>                                                    |
| [**XMPlaneIntersectPlane**](/windows/win32/api/directxmath/nf-directxmath-xmplaneintersectplane)<br/>   | Recherche l’intersection de deux plans.<br/>                                                                 |
| [**XMPlaneIsInfinite**](/windows/win32/api/directxmath/nf-directxmath-xmplaneisinfinite)<br/>           | Teste si l’un des coefficients d’un plan est un infini positif ou négatif.<br/>                    |
| [**XMPlaneIsNaN**](/windows/win32/api/directxmath/nf-directxmath-xmplaneisnan)<br/>                     | Teste si l’un des coefficients d’un plan est une valeur NaN.<br/>                                            |
| [**XMPlaneNearEqual**](/windows/win32/api/directxmath/nf-directxmath-xmplanenearequal)<br/>             | Détermine si deux plans sont presque égaux.<br/>                                                       |
| [**XMPlaneNormalize**](/windows/win32/api/directxmath/nf-directxmath-xmplanenormalize)<br/>             | Normalise les coefficients d’un plan afin que les coefficients de x, y et z forment un vecteur normal d’unité.<br/> |
| [**XMPlaneNormalizeEst**](/windows/win32/api/directxmath/nf-directxmath-xmplanenormalizeest)<br/>       | Estime les coefficients d’un plan afin que les coefficients de x, y et z forment un vecteur normal d’unité.<br/>  |
| [**XMPlaneNotEqual**](/windows/win32/api/directxmath/nf-directxmath-xmplanenotequal)<br/>               | Détermine si deux plans sont inégaux.<br/>                                                                 |
| [**XMPlaneTransform**](/windows/win32/api/directxmath/nf-directxmath-xmplanetransform)<br/>             | Transforme un plan par une matrice donnée.<br/>                                                                 |
| [**XMPlaneTransformStream**](/windows/win32/api/directxmath/nf-directxmath-xmplanetransformstream)<br/> | Transforme un flux de plans par une matrice donnée.<br/>                                                      |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Fonctions de la bibliothèque DirectXMath](ovw-xnamath-reference-functions.md)
</dt> </dl>

 

 
