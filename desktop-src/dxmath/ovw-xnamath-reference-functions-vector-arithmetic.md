---
description: Répertorie les fonctions arithmétiques vectorielles.
ms.assetid: d7ed4516-74a6-81ec-79a2-2e39cf112d11
title: Fonctions arithmétiques vectorielles
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 64ad5149153b736ddf6d2f2af5b9671e32651f86
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106524101"
---
# <a name="vector-arithmetic-functions"></a>Fonctions arithmétiques vectorielles

Répertorie les fonctions arithmétiques vectorielles.

## <a name="in-this-section"></a>Contenu de cette section



| Rubrique                                                                                   | Description                                                                                                               |
|-----------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------|
| [**XMVectorAbs**](/windows/win32/api/directxmath/nf-directxmath-xmvectorabs)<br/>                                           | Calcule la valeur absolue de chaque composant d’un [**XMVECTOR**](xmvector-data-type.md).<br/>                    |
| [**XMVectorAdd**](/windows/win32/api/directxmath/nf-directxmath-xmvectoradd)<br/>                                           | Calcule la somme de deux vecteurs.<br/>                                                                               |
| [**XMVectorAddAngles**](/windows/win32/api/directxmath/nf-directxmath-xmvectoraddangles)<br/>                               | Ajoute deux vecteurs représentant des angles.<br/>                                                                          |
| [**XMVectorCeiling**](/windows/win32/api/directxmath/nf-directxmath-xmvectorceiling)<br/>                                   | Calcule le plafond de chaque composant d’un [**XMVECTOR**](xmvector-data-type.md).<br/>                           |
| [**XMVectorClamp**](/windows/win32/api/directxmath/nf-directxmath-xmvectorclamp)<br/>                                       | Fixe les composants d’un vecteur à une plage minimale et maximale spécifiée.<br/>                                    |
| [**XMVectorDivide**](/windows/win32/api/directxmath/nf-directxmath-xmvectordivide)<br/>                                     | Divise une instance de `XMVECTOR` par une deuxième instance, en retournant le résultat dans une troisième instance.<br/>             |
| [**XMVectorFloor**](/windows/win32/api/directxmath/nf-directxmath-xmvectorfloor)<br/>                                       | Calcule le plancher de chaque composant d’un [**XMVECTOR**](xmvector-data-type.md).<br/>                             |
| [**XMVectorIsInfinite**](/windows/win32/api/directxmath/nf-directxmath-xmvectorisinfinite)<br/>                             | Effectue un test par composant pour +/-Infinity sur un vecteur.<br/>                                                    |
| [**XMVectorIsNaN**](/windows/win32/api/directxmath/nf-directxmath-xmvectorisnan)<br/>                                       | Effectue un test NaN par composant sur un vecteur.<br/>                                                                 |
| [**XMVectorMax**](/windows/win32/api/directxmath/nf-directxmath-xmvectormax)<br/>                                           | Effectue une comparaison par composant entre deux vecteurs et retourne un vecteur contenant les composants les plus volumineux.<br/>  |
| [**XMVectorMin**](/windows/win32/api/directxmath/nf-directxmath-xmvectormin)<br/>                                           | Effectue une comparaison par composant entre deux vecteurs et retourne un vecteur contenant les plus petits composants.<br/> |
| [**XMVectorMod**](/windows/win32/api/directxmath/nf-directxmath-xmvectormod)<br/>                                           | Calcule le reste à virgule flottante par composant du quotient de deux vecteurs.<br/>                            |
| [**XMVectorModAngles**](/windows/win32/api/directxmath/nf-directxmath-xmvectormodangles)<br/>                               | Calcule le modulo de l’angle par composant 2PI.<br/>                                                                   |
| [**XMVectorMultiply**](/windows/win32/api/directxmath/nf-directxmath-xmvectormultiply)<br/>                                 | Calcule le produit par composant de deux vecteurs.<br/>                                                             |
| [**XMVectorMultiplyAdd**](/windows/win32/api/directxmath/nf-directxmath-xmvectormultiplyadd)<br/>                           | Calcule le produit des deux premiers vecteurs ajoutés au troisième vecteur.<br/>                                       |
| [**XMVectorNegate**](/windows/win32/api/directxmath/nf-directxmath-xmvectornegate)<br/>                                     | Calcule la négation d’un vecteur.<br/>                                                                             |
| [**XMVectorNegativeMultiplySubtract**](/windows/win32/api/directxmath/nf-directxmath-xmvectornegativemultiplysubtract)<br/> | Calcule la différence entre un troisième vecteur et le produit des deux premiers vecteurs.<br/>                            |
| [**XMVectorPow**](/windows/win32/api/directxmath/nf-directxmath-xmvectorpow)<br/>                                           | Calcule *v1* élevé à la puissance de *v2*.<br/>                                                                     |
| [**XMVectorReciprocal**](/windows/win32/api/directxmath/nf-directxmath-xmvectorreciprocal)<br/>                             | Calcule la réciproque par composant d’un vecteur.<br/>                                                             |
| [**XMVectorReciprocalEst**](/windows/win32/api/directxmath/nf-directxmath-xmvectorreciprocalest)<br/>                       | Estime l’inverse par composant d’un vecteur.<br/>                                                            |
| [**XMVectorReciprocalSqrt**](/windows/win32/api/directxmath/nf-directxmath-xmvectorreciprocalsqrt)<br/>                     | Calcule la racine carrée réciproque par composant d’un vecteur.<br/>                                                 |
| [**XMVectorReciprocalSqrtEst**](/windows/win32/api/directxmath/nf-directxmath-xmvectorreciprocalsqrtest)<br/>               | Estime la racine carrée réciproque par composant d’un vecteur.<br/>                                                |
| [**XMVectorRound**](/windows/win32/api/directxmath/nf-directxmath-xmvectorround)<br/>                                       | Arrondit chaque composant d’un vecteur à l’entier le plus proche.<br/>                                                      |
| [**XMVectorSaturate**](/windows/win32/api/directxmath/nf-directxmath-xmvectorsaturate)<br/>                                 | Sature chaque composant d’un vecteur dans la plage 0.0 f à 1.0 f.<br/>                                                |
| [**XMVectorScale**](/windows/win32/api/directxmath/nf-directxmath-xmvectorscale)<br/>                                       | Scalaire multiplie un vecteur par une valeur à virgule flottante.<br/>                                                          |
| [**XMVectorSqrt**](/windows/win32/api/directxmath/nf-directxmath-xmvectorsqrt)<br/>                                         | Calcule la racine carrée par composant d’un vecteur.<br/>                                                            |
| [**XMVectorSqrtEst**](/windows/win32/api/directxmath/nf-directxmath-xmvectorsqrtest)<br/>                                   | Estime la racine carrée par composant d’un vecteur.<br/>                                                           |
| [**XMVectorSubtract**](/windows/win32/api/directxmath/nf-directxmath-xmvectorsubtract)<br/>                                 | Calcule la différence de deux vecteurs.<br/>                                                                        |
| [**XMVectorSubtractAngles**](/windows/win32/api/directxmath/nf-directxmath-xmvectorsubtractangles)<br/>                     | Soustrait deux vecteurs représentant des angles.<br/>                                                                     |
| [**XMVectorSum**](/windows/win32/api/directxmath/nf-directxmath-xmvectorsum)<br/>                                           | Calcule la somme horizontale des composants d’un [**XMVECTOR**](xmvector-data-type.md).<br/>                    |
| [**XMVectorTruncate**](/windows/win32/api/directxmath/nf-directxmath-xmvectortruncate)<br/>                                 | Arrondit chaque composant d’un vecteur à la valeur entière la plus proche dans la direction de zéro.<br/>                       |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Fonctions vectorielles de la bibliothèque DirectXMath](ovw-xnamath-reference-functions-vector.md)
</dt> </dl>

 

 
