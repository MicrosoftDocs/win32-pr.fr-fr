---
description: Les périphériques Direct3D peuvent transformer les coordonnées de texture pour les vertex en appliquant une matrice 4x4.
ms.assetid: f36439de-e37a-457c-9485-a435847eb01e
title: Transformations de coordonnées de texture (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 755af38c6c58fc2f19297b056e3e9f35ce2559a6a7a2d52e8a23c94f93f4fbaa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119984789"
---
# <a name="texture-coordinate-transformations-direct3d-9"></a>Transformations de coordonnées de texture (Direct3D 9)

Les périphériques Direct3D peuvent transformer les coordonnées de texture pour les vertex en appliquant une matrice 4x4. Le système applique les transformations aux coordonnées de texture de la même manière que la géométrie. Toutes les transformations (mise à l’échelle, rotation, translation, projection, cisaillement ou toute combinaison de ces opérations) peuvent être effectuées à l’aide d’une matrice 4x4.

> [!Note]  
> Direct3D ne modifie pas les sommets transformés et allumés. Par conséquent, une application utilisant des vertex transformés et allumés ne peut pas utiliser Direct3D pour transformer les coordonnées de texture des vertex.

 

Les appareils qui prennent en charge les opérations de transformation et d’éclairage à accélération matérielle (T&L Device HAL) accélèrent également la transformation des coordonnées de texture. Lorsque l’accélération matérielle des transformations n’est pas disponible, les optimisations spécifiques à la plateforme dans le pipeline de géométrie Direct3D s’appliquent aux transformations de coordonnées de texture.

Les transformations de coordonnée de texture sont utiles pour produire des effets spéciaux tout en évitant la nécessité de modifier directement les coordonnées de texture de votre géométrie. Vous pouvez utiliser des matrices de translation ou de rotation simples pour animer des textures sur un objet, ou vous pouvez transformer des coordonnées de texture générées automatiquement par Direct3D pour simplifier et éventuellement accélérer les effets avancés tels que les textures projetées et le mappage de lumière dynamique. En outre, vous pouvez utiliser des transformations de coordonnée de texture pour réutiliser un ensemble unique de coordonnées de texture à plusieurs fins, dans plusieurs étapes de texture.

## <a name="setting-and-retrieving-texture-coordinate-transformations"></a>Définition et récupération des transformations de coordonnées de texture

Comme les matrices que votre application utilise pour la géométrie, vous définissez et récupérez les transformations de coordonnée de texture en appelant les méthodes [**IDirect3DDevice9 :: setTransform**](/windows/desktop/api) et [**IDirect3DDevice9 :: GetTransform**](/windows/desktop/api) . Ces méthodes acceptent les D3DTS \_ TEXTURE0 par le biais \_ des membres D3DTS TEXTURE7 du type énuméré [**D3DTRANSFORMSTATETYPE**](./d3dtransformstatetype.md) pour identifier les matrices de transformation pour les étapes de texture 0 à 7, respectivement.

Le code suivant définit une matrice à appliquer aux coordonnées de texture pour l’étape de texture 0.


```
// For this example, assume the d3dDevice variable contains a 
//   valid pointer to an IDirect3DDevice9 interface.

D3DMATRIX matTrans = D3DXMatrixIdentity( NULL );

// Set up the matrix for the desired transformation.
d3dDevice->SetTransform( D3DTS_TEXTURE0, &matTrans );
```



## <a name="enabling-texture-coordinate-transformations"></a>Activation des transformations de coordonnée de texture

L' \_ État de l’étape de texture D3DTSS TEXTURETRANSFORMFLAGS contrôle l’application des transformations de coordonnées de texture. Les valeurs de cet état d’étape de texture sont définies par le type énuméré [**D3DTEXTURETRANSFORMFLAGS**](./d3dtexturetransformflags.md) .

Les transformations de coordonnées de texture sont désactivées lorsque D3DTSS \_ TEXTURETRANSFORMFLAGS est défini sur D3DTTFF \_ Disable (valeur par défaut). En supposant que les transformations de coordonnées de texture ont été activées pour l’étape 0, le code suivant les désactive.


```
// For this example, assume the d3dDevice variable contains a 
// valid pointer to an IDirect3DDevice9 interface.

d3dDevice->SetTextureStageState( 0, D3DTSS_TEXTURETRANSFORMFLAGS, 
                                 D3DTTFF_DISABLE );
```



Les autres valeurs définies dans [**D3DTEXTURETRANSFORMFLAGS**](./d3dtexturetransformflags.md) sont utilisées pour activer les transformations de coordonnée de texture et pour contrôler le nombre d’éléments de coordonnées de texture qui en résultent passés au rastériseur. Par exemple, prenez le code suivant.


```
// For this example, assume the d3dDevice variable contains a 
//   valid pointer to an IDirect3DDevice9 interface.

d3dDevice->SetTextureStageState( 0, D3DTSS_TEXTURETRANSFORMFLAGS, 
                                 D3DTTFF_COUNT2 );
```



La \_ valeur COUNT2 D3DTTFF indique au système d’appliquer le jeu de matrices de transformation pour l’étape de texture 0, puis de passer les deux premiers éléments des coordonnées de texture modifiées au rastériseur.

L' \_ indicateur de transformation de texture projeté D3DTTFF indique les coordonnées d’une texture projetée. Lorsque cet indicateur est spécifié, le rastériseur divise les éléments transmis par le dernier élément. Prenons le code suivant, par exemple.


```
// For this example, assume the d3dDevice variable contains a 
//   valid pointer to an IDirect3DDevice9 interface.

d3dDevice->SetTextureStageState( 0, D3DTSS_TEXTURETRANSFORMFLAGS, 
                                 D3DTTFF_COUNT3 | D3DTTFF_PROJECTED );
```



Cet exemple indique au système de passer trois éléments de coordonnée de texture au rastériseur. Le rastériseur divise les deux premiers éléments par le troisième, en produisant les coordonnées de texture 2D nécessaires pour traiter la texture.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Traitement des coordonnées de texture](texture-coordinate-processing.md)
</dt> </dl>

 

 
