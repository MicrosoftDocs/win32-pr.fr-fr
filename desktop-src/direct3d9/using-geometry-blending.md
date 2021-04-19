---
description: La structure définie par l’utilisateur suivante peut être utilisée pour les vertex qui seront mélangés entre deux matrices.
ms.assetid: 6bcabcf9-d14e-446a-8dd2-e741211cc704
title: Utilisation de la fusion géométrique (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fc12c4d7d83ce4c01c76bd338a07f8e0aac7c003
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "106544540"
---
# <a name="using-geometry-blending-direct3d-9"></a>Utilisation de la fusion géométrique (Direct3D 9)

La structure définie par l’utilisateur suivante peut être utilisée pour les vertex qui seront mélangés entre deux matrices.


```
// The flexible vertex format (FVF) descriptor for this vertex would be:
//   FVF = D3DFVF_XYZB1 | D3DFVF_NORMAL | D3DFVF_TEX1; 

struct D3DBLENDVERTEX {
    D3DVECTOR v;
    FLOAT     blend; 
    D3DVECTOR n;
    FLOAT     tu, tv;
};
```



Le poids de fusion doit apparaître après les données position et RHW dans le prix de la Commission et avant la normale du vertex.

Notez que le format de vertex précédent contient une seule valeur de poids de fusion. Cela est dû au fait qu’il y aura deux matrices universelles définies dans les États [**D3DTS \_ WORLDMATRIX**](d3dts-worldmatrix.md)(0) et **D3DTS \_ WORLDMATRIX**(1) Transform. Le système fusionne chaque vertex entre ces deux matrices à l’aide de la valeur de poids unique. Pour trois matrices, seuls deux poids sont requis, et ainsi de suite.

> [!Note]
>
> La définition des poids de la peau est simple. L’utilisation d’une fonction linéaire de la distance entre les jointures est un bon début, mais une fonction sigmoïde plus lisse semble mieux. Le choix d’une fonction de distribution de poids d’épiderme peut entraîner des froissures nets au niveau des jointures, si nécessaire, en utilisant une variation importante du poids de la peau sur une distance.

 

## <a name="setting-blending-matrices"></a>Définition des matrices de fusion

Vous définissez les matrices de transformation entre lesquelles le système fusionne en appelant la méthode [**IDirect3DDevice9 :: setTransform**](/windows/desktop/api) . Définissez le premier paramètre sur une valeur définie par la macro [**D3DTS \_ WORLDMATRIX**](d3dts-worldmatrix.md) , puis définissez le deuxième paramètre sur l’adresse de la matrice à définir.

L’exemple de code C++ suivant définit deux matrices universelles, entre lesquelles la géométrie est mélangée pour créer l’illusion d’un bras joint.


```
// For this example, the d3dDevice variable is assumed to be a valid pointer
//   to an IDirect3DDevice9 interface for an initialized 3D scene.

float     BendAngle = 3.1415926f / 4.0f; // 45 degrees
D3DMATRIX matUpperArm, matLowerArm;

// The upper arm is immobile. Use the identity matrix.
D3DXMatrixIdentity( matUpperArm );
d3dDevice->SetTransform( D3DTS_WORLDMATRIX(0), &matUpperArm );

// The lower arm rotates about the x-axis, attached to the upper arm.
D3DXMatrixRotationX( matLowerArm, -BendAngle ); 
d3dDevice->SetTransform( D3DTS_WORLDMATRIX(1), &matLowerArm );
```



La définition d’une matrice de fusion fait simplement en sorte que le système met en cache la matrice pour une utilisation ultérieure ; elle n’indique pas au système de commencer à fusionner les vertex.

## <a name="enabling-geometry-blending"></a>Activation de la fusion de géométrie

La fusion géométrique est désactivée par défaut. Pour activer la fusion de géométrie, appelez la méthode [**IDirect3DDevice9 :: SetRenderState**](/windows/desktop/api) pour définir l' \_ État de rendu D3DRS VERTEXBLEND sur une valeur du type énuméré [**D3DVERTEXBLENDFLAGS**](./d3dvertexblendflags.md) . L’exemple de code suivant montre ce à quoi peut ressembler cet appel lors de la définition de l’état de rendu d’une fusion entre deux matrices universelles.


```
d3dDevice->SetRenderState( D3DRS_VERTEXBLEND, D3DVBF_1WEIGHTS );
```



Lorsque D3DRS \_ VERTEXBLEND est défini sur une valeur autre que D3DVBF \_ Disable, le système suppose que le nombre approprié de poids de fusion est inclus dans le format de vertex. Il vous incombe de fournir un format de vertex conforme et de fournir une description appropriée de ce format aux méthodes de rendu Direct3D.

Lorsqu’il est activé, le système effectue une fusion géométrique pour tous les objets rendus par les méthodes de rendu DrawPrimitive.

## <a name="see-also"></a>Voir aussi

[Correction des codes de fonction de la Commission (Direct3D 9)](fixed-function-fvf-codes.md)


## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Fusion géométrique](geometry-blending.md)
</dt> </dl>

 

 
