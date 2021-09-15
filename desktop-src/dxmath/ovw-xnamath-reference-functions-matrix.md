---
description: Répertorie les fonctions de matrice fournies par DirectXMath.
ms.assetid: d59d0dcc-deae-3f7e-55c5-0c5ff383343b
title: Fonctions de matrice de la bibliothèque DirectXMath
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a91ecdef8389bf60594d370c2b3de01995bc1169
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127403452"
---
# <a name="directxmath-library-matrix-functions"></a>Fonctions de matrice de la bibliothèque DirectXMath

Répertorie les fonctions de matrice fournies par DirectXMath.

> [!Note]  
> DirectXMath offre des versions gauche et droite des fonctions de matrice avec « droitier », mais suppose toujours un format de ligne principale.

 

## <a name="in-this-section"></a>Contenu de cette section



| Rubrique                                                                                               | Description                                                                                                                            |
|-----------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| [**XMMatrixAffineTransformation**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixaffinetransformation)<br/>                     | Crée une matrice de transformation affine.<br/>                                                                                     |
| [**XMMatrixAffineTransformation2D**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixaffinetransformation2d)<br/>                 | Crée une matrice de transformation affine 2D dans le plan XY. <br/>                                                                  |
| [**XMMatrixDecompose**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixdecompose)<br/>                                           | Décompose une matrice de transformation 3D générale en ses composants scalaires, de rotation et de translation.<br/>                   |
| [**XMMatrixDeterminant**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixdeterminant)<br/>                                       | Calcule le déterminant d’une matrice.<br/>                                                                                       |
| [**XMMatrixIdentity**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixidentity)<br/>                                             | Génère la matrice d’identité.<br/>                                                                                                 |
| [**XMMatrixInverse**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixinverse)<br/>                                               | Calcule l’inverse d’une matrice.<br/>                                                                                           |
| [**XMMatrixIsIdentity**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixisidentity)<br/>                                         | Teste si une matrice est la matrice d’identité.<br/>                                                                              |
| [**XMMatrixIsInfinite**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixisinfinite)<br/>                                         | Teste si l’un des éléments d’une matrice est un infini positif ou négatif.<br/>                                            |
| [**XMMatrixIsNaN**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixisnan)<br/>                                                   | Teste si l’un des éléments d’une matrice est NaN.<br/>                                                                      |
| [**XMMatrixLookAtLH**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixlookatlh)<br/>                                             | Crée une matrice globale pour un système de coordonnées gaucher à l’aide d’une position de caméra, une direction vers le haut et un point focal.<br/>       |
| [**XMMatrixLookAtRH**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixlookatrh)<br/>                                             | Crée une matrice globale pour un système de coordonnées droitier à l’aide d’une position de caméra, une direction vers le haut et un point focal.<br/>      |
| [**XMMatrixLookToLH**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixlooktolh)<br/>                                             | Crée une matrice globale pour un système de coordonnées gaucher à l’aide d’une position de caméra, une direction vers le haut et une direction de caméra.<br/>  |
| [**XMMatrixLookToRH**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixlooktorh)<br/>                                             | Crée une matrice globale pour un système de coordonnées droitier à l’aide d’une position de caméra, une direction vers le haut et une direction de caméra.<br/> |
| [**XMMatrixMultiply**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixmultiply)<br/>                                             | Calcule le produit de deux matrices.<br/>                                                                                       |
| [**XMMatrixMultiplyTranspose**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixmultiplytranspose)<br/>                           | Calcule la permutation du produit de deux matrices.<br/>                                                                      |
| [**XMMatrixOrthographicLH**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixorthographiclh)<br/>                                 | Crée une matrice de projection orthogonale pour un système de coordonnées gaucher.<br/>                                                 |
| [**XMMatrixOrthographicOffCenterLH**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixorthographicoffcenterlh)<br/>               | Crée une matrice de projection orthogonale personnalisée pour un système de coordonnées gaucher.<br/>                                           |
| [**XMMatrixOrthographicOffCenterRH**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixorthographicoffcenterrh)<br/>               | Crée une matrice de projection orthogonale personnalisée pour un système de coordonnées droitier.<br/>                                          |
| [**XMMatrixOrthographicRH**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixorthographicrh)<br/>                                 | Crée une matrice de projection orthogonale pour un système de coordonnées droitier.<br/>                                                |
| [**XMMatrixPerspectiveFovLH**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixperspectivefovlh)<br/>                             | Crée une matrice de projection de perspective pour un système gaucher en fonction d’un champ de vue.<br/>                                                |
| [**XMMatrixPerspectiveFovRH**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixperspectivefovrh)<br/>                             | Crée une matrice de projection de perspective pour un système droitier en fonction d’un champ de vue.<br/>                                               |
| [**XMMatrixPerspectiveLH**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixperspectivelh)<br/>                                   | Crée une matrice de projection de perspective pour un système gaucher.<br/>                                                                         |
| [**XMMatrixPerspectiveOffCenterLH**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixperspectiveoffcenterlh)<br/>                 | Crée une version personnalisée d’une matrice de projection de perspective pour un système gaucher.<br/>                                                     |
| [**XMMatrixPerspectiveOffCenterRH**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixperspectiveoffcenterrh)<br/>                 | Crée une version personnalisée d’une matrice de projection de perspective pour un système droitier.<br/>                                                    |
| [**XMMatrixPerspectiveRH**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixperspectiverh)<br/>                                   | Crée une matrice de projection de perspective pour un système droitier.<br/>                                                                        |
| [**XMMatrixReflect**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixreflect)<br/>                                               | Crée une matrice de transformation conçue pour refléter les vecteurs dans un plan donné.<br/>                                           |
| [**XMMatrixRotationAxis**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixrotationaxis)<br/>                                     | Crée une matrice qui pivote autour d’un axe arbitraire.<br/>                                                                      |
| [**XMMatrixRotationNormal**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixrotationnormal)<br/>                                 | Crée une matrice qui pivote autour d’un vecteur normal arbitraire.<br/>                                                             |
| [**XMMatrixRotationQuaternion**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixrotationquaternion)<br/>                         | Génère une matrice de rotation à partir d’un Quaternion.<br/>                                                                                 |
| [**XMMatrixRotationRollPitchYaw**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixrotationrollpitchyaw)<br/>                     | Crée une matrice de rotation basée sur un pas donné, un lacet et un rouleau (angles Euler).<br/>                                              |
| [**XMMatrixRotationRollPitchYawFromVector**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixrotationrollpitchyawfromvector)<br/> | Crée une matrice de rotation basée sur un vecteur contenant les angles Euler (pas, lacets et rouleaux).<br/>                              |
| [**XMMatrixRotationX**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixrotationx)<br/>                                           | Crée une matrice qui pivote autour de l’axe x.<br/>                                                                             |
| [**XMMatrixRotationY**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixrotationy)<br/>                                           | Crée une matrice qui pivote autour de l’axe y.<br/>                                                                             |
| [**XMMatrixRotationZ**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixrotationz)<br/>                                           | Crée une matrice qui pivote autour de l’axe z.<br/>                                                                             |
| [**XMMatrixScaling**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixscaling)<br/>                                               | Crée une matrice qui met à l’échelle le long de l’axe x, de l’axe y et de l’axe z.<br/>                                                           |
| [**XMMatrixScalingFromVector**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixscalingfromvector)<br/>                           | Crée une matrice de mise à l’échelle à partir d’un vecteur 3D.<br/>                                                                                   |
| [**XMMatrixSet**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixset)<br/>                                                       | Crée une matrice avec des valeurs **float** .<br/>                                                                                     |
| [**XMMatrixShadow**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixshadow)<br/>                                                 | Crée une matrice de transformation qui aplatit la géométrie dans un plan.<br/>                                                         |
| [**XMMatrixTransformation**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixtransformation)<br/>                                 | Crée une matrice de transformation.<br/>                                                                                             |
| [**XMMatrixTransformation2D**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixtransformation2d)<br/>                             | Crée une matrice de transformation 2D dans le plan XY.<br/>                                                                          |
| [**XMMatrixTranslation**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixtranslation)<br/>                                       | Crée une matrice de translation à partir des offsets spécifiés.<br/>                                                                     |
| [**XMMatrixTranslationFromVector**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixtranslationfromvector)<br/>                   | Crée une matrice de traduction à partir d’un vecteur.<br/>                                                                                  |
| [**XMMatrixTranspose**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixtranspose)<br/>                                           | Calcule la permutation d’une matrice.<br/>                                                                                         |
| [**XMMatrixVectorTensorProduct**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixvectortensorproduct)<br/>                                           | Calcule le produit tenseur externe de 2 vecteurs.<br/>                                                                                         |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Fonctions de la bibliothèque DirectXMath](ovw-xnamath-reference-functions.md)
</dt> </dl>

 

 
