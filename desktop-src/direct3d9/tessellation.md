---
description: Pavage (Direct3D 9)
ms.assetid: ae39b0e1-d2ae-449e-89db-0a2b24171531
title: Pavage (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 82378caac1218158ffc1834c9a9b56fb8cbd250e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127291762"
---
# <a name="tessellation-direct3d-9"></a>Pavage (Direct3D 9)

## <a name="tessellator-unit"></a>Unité du paveur

L’unité du paveur a été améliorée. Vous pouvez maintenant l’utiliser pour :

-   Effectue un pavage adaptatif de toutes les primitives d’ordre supérieur.
-   Recherchez des valeurs de remplacement par vertex d’un mappage de déplacement et passez-les à un nuanceur de sommets.
-   Prendre en charge le pavage rectangle-patch. Cela est spécifié par le biais d’une déclaration de vertex utilisant D3DDECLMETHOD \_ partial ou D3DDECLMETHOD \_ PARTIALV. Si une déclaration de vertex contenant ces méthodes est utilisée pour dessiner un correctif triangulaire, [**IDirect3DDevice9 ::D rawtripatch**](/windows/desktop/api) échoue. Pour plus d’informations sur les déclarations de vertex, consultez [**D3DVERTEXELEMENT9**](d3dvertexelement9.md).

Dans DirectX 8. x, ce qui était appelé ORDER était vraiment le degré. Dans Direct3D 9, le degré est maintenant spécifié par [**D3DDEGREETYPE**](./d3ddegreetype.md).


```
 // This used to be D3DORDERTYPE and D3DORDER* 
 typedef enum _D3DDEGREETYPE 
 { 
 D3DDEGREE_LINEAR = 1, 
 D3DDEGREE_QUADRATIC = 2, 
 D3DDEGREE_CUBIC = 3, 
 D3DDEGREE_QUINTIC = 5, 
 D3DDEGREE_FORCE_DWORD = 0x7fffffff, 
 } D3DDEGREETYPE; 
```



La modification du type de degré a affecté deux autres structures.


```
typedef struct _D3DRECTPATCH_INFO 
 { 
 UINT StartVertexOffsetWidth; 
 UINT StartVertexOffsetHeight; 
 UINT Width; 
 UINT Height; 
 UINT Stride; 
 D3DBASISTYPE Basis; 
 D3DDEGREETYPE Degree; 
 } D3DRECTPATCH_INFO; 
```




```
 typedef struct _D3DTRIPATCH_INFO 
 { 
 UINT StartVertexOffset; 
 UINT NumVertices; 
 D3DBASISTYPE Basis; 
 D3DDEGREETYPE Degree; 
 } D3DTRIPATCH_INFO; 
```



Les pilotes doivent corriger les erreurs de compilation qui résultent de cette modification quand elles se compilent avec les nouveaux en-têtes. Aucune fonctionnalité ne doit être modifiée.

## <a name="adaptive-tessellation"></a>Pavage adaptative

Le pavage adaptatif peut être appliqué à des primitives d’ordre élevé, y compris N-patchs, des carreaux de rectangles et des carreaux de triangle. Cette fonctionnalité est activée par le \_ ENABLEADAPTIVETESSELLATION D3DRS et Adaptive tessellates un correctif, en fonction de la valeur de profondeur du vertex de contrôle dans l’espace œil.

Les coordonnées z (ZI) des vertex de contrôle (VI), qui sont transformées en espace œil (Zieye) en effectuant un produit scalaire avec un vecteur 4, sont utilisées comme valeurs de profondeur. Le vecteur 4D (MDM) est spécifié par l’application à l’aide de quatre États de rendu (D3DRS \_ ADAPTIVETESS \_ X, D3DRS \_ ADAPTIVETESS \_ Y, D3DRS \_ ADAPTIVETESS \_ Z et D3DRS \_ ADAPTIVETESS \_ W). Ce 4-Vector peut être la troisième colonne des matrices de monde et de vue concaténées. Elle peut également être utilisée pour appliquer une mise à l’échelle à Zieye.

La fonction de calcul de l’TI de niveau de pavage à partir de Zieye est supposée être (MaxTessellationLevel/Zieye), ce qui signifie que le MaxTessellationLevel est le niveau de pavage à Z = 1 dans l’espace œil. Le MaxTessellationLevel est égal à une valeur définie par [**IDirect3DDevice9 :: SetNPatchMode**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setnpatchmode) pour N-patchs et, pour RT-patchs, il est égal à pNumSegs. Le niveau de pavage est ensuite ancré aux valeurs définies par les deux États de rendu supplémentaires D3DRS \_ MINTESSELLATIONLEVEL et D3DRS \_ MAXTESSELLATIONLEVEL, qui définissent les niveaux de pavage minimal et maximal à fixer. La moyenne de l’TI pour chaque vertex le long d’un bord d’un correctif est calculée pour obtenir un niveau de pavage pour cette arête. L’algorithme pour le calcul du TI pour les correctifs de rectangle, les correctifs de triangle et les N-patchs diffère dans les vertex de contrôle utilisés pour calculer le niveau de pavage.

Pour les correctifs de rectangle avec une base B-spline, les quatre sommets de contrôle les plus extérieurs sont utilisés. Par exemple, avec D3DORDER \_ cubique Order : vertex (1,1) et (1, la largeur-2) sont utilisées avec pNumSegs \[ 0 \] , les sommets (1, largeur-2) et (hauteur-2, hauteur-2) sont utilisés avec pNumSegs \[ 1, les \] sommets (hauteur-2, largeur-2) et (1, largeur-2) sont utilisés avec le pNumSegs \[ 2 \] , et les sommets (2, 1) et (1,1) sont utilisés avec \[ \]

Pour les correctifs triangulaires, les sommets des correctifs d’angle sont utilisés. Avec l' \_ ordre D3DORDER cubique : les sommets (0) et (9) sont utilisés avec pNumSegs \[ 0 \] , les sommets (9) et (6) sont utilisés avec pNumSegs \[ 1 \] et les sommets (6) et (0) sont utilisés avec pNumSegs \[ 3 \] .

Pour les N-patchs, les sommets triangulaires sont utilisés.

Pour les carreaux de rectangle et de triangle avec une base Bézier, les sommets de contrôle d’angle sont utilisés.

Contrôle du taux de pavage par vertex. Une application peut éventuellement fournir une valeur à virgule flottante positive unique par vertex, qui peut être utilisée pour contrôler le taux de pavage. Celui-ci est fourni à l’aide de l’D3DDECLUSAGE \_ TESSFACTOR, pour lequel l’index d’utilisation doit avoir la valeur 0 et le type d’entrée doit être D3DDECLTYPE \_ FLOAT1. Cette valeur est multipliée par le niveau de pavage par vertex.

### <a name="math"></a>Math

Le niveau de pavage (te) d’un bord e, représenté par deux vertex de contrôle (VE1, VE2), est calculé comme indiqué ci-dessous :


```
Vertex Vi: (Xi, Yi, Zi, TFactori (optional)). 
Ze1eye = Ve1 . Mdm 
Ze2eye = Ve2 . Mdm 
Te1 = MaxTessellationLevel * TFactore1 / Ze1eye 
Te2 = MaxTessellationLevel * TFactore2 / Ze2eye 
Te = ( Te1 + Te2 ) / 2; 
if Te > D3DRS_MAXTESSELLATIONLEVEL || Te < 0, then Te = D3DRS_MAXTESSELLATIONLEVEL 
if Te < D3DRS_MINTESSELLATIONLEVEL, then Te = D3DRS_MINTESSELLATIONLEVEL 
```



Quand D3DRS \_ ENABLEADAPTIVETESSELLATION a la **valeur true**, les primitives de triangle (listes de triangles, ventilateurs, bandes) sont dessinées en tant que N-patchs, [**IDirect3DDevice9 :: SetNPatchMode**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setnpatchmode) a une valeur définie inférieure à 1,0.

### <a name="api-changes"></a>Modifications de l’API

Nouveaux États de rendu :


```
 D3DRS_ENABLEADAPTIVETESSELLATION // BOOL 
 D3DRS_MAXTESSELLATIONLEVEL       // Float 
 D3DRS_MINTESSELLATIONLEVEL       // Float 
 D3DRS_ADAPTIVETESS_X             // Float 
 D3DRS_ADAPTIVETESS_Y             // Float 
 D3DRS_ADAPTIVETESS_Z             // Float 
 D3DRS_ADAPTIVETESS_W             // Float 
 
 // D3DRS_MINTESSELLATIONLEVEL and D3DRS_MAXTESSELLATIONLEVEL 
 // cannot be less than 1 
```



Et leurs valeurs par défaut :


```
D3DRS_MAXTESSELLATIONLEVEL = 1.0f 
D3DRS_MINTESSELLATIONLEVEL = 1.0f 
D3DRS_ADAPTIVETESS_X = 0.0f 
D3DRS_ADAPTIVETESS_Y = 0.0f 
D3DRS_ADAPTIVETESS_Z = 1.0f 
D3DRS_ADAPTIVETESS_W = 0.0f 
D3DRS_ENABLEADAPTIVETESSELLATION = FALSE 
```



Nouvelles extrémités matérielles :


```
D3DDEVCAPS2_ADAPTIVETESSRTPATCH // Can adaptively tessellate RT-patches 
D3DDEVCAPS2_ADAPTIVETESSNPATCH  // Can adaptively tessellate N-patches 
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Pipeline de vertex](vertex-pipeline.md)
</dt> </dl>

 

 
