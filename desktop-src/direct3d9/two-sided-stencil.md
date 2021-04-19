---
description: Les volumes de clichés instantanés permettent de dessiner des ombres avec la mémoire tampon de stencil.
ms.assetid: 8b71d871-ee66-47c4-8190-5c75419b28b2
title: Two-Sided gabarit (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b238c4b778b9894029764032e76b60c476a891a9
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "106514101"
---
# <a name="two-sided-stencil-direct3d-9"></a>Two-Sided gabarit (Direct3D 9)

Les volumes de clichés instantanés permettent de dessiner des ombres avec la mémoire tampon de stencil. L’application calcule les volumes de clichés instantanés convertis par la géométrie de la Boucher, en calculant les bords silhouettes et en les séparant de la lumière dans un ensemble de volumes 3D. Ces volumes sont ensuite restitués deux fois dans la mémoire tampon du stencil.

Le premier rendu dessine des polygones vers l’avant et incrémente les valeurs de mémoire tampon de stencil. Le deuxième rendu dessine les polygones de l’arrière-plan du volume de cliché instantané et décrémente les valeurs de la mémoire tampon du stencil. Normalement, toutes les valeurs incrémentées et décrémentées s’annulent les unes des autres. Toutefois, la scène était déjà rendue avec une géométrie normale provoquant l’échec du test de la mémoire tampon z pour certains pixels, car le volume de cliché instantané est rendu. Les valeurs laissées dans la mémoire tampon du stencil correspondent aux pixels qui se trouvent dans l’ombre. Ces contenus de tampons de stencil restants sont utilisés comme masque, afin de mélanger en 3D un grand nombre de cœurs noirs englobant tous dans la scène. Avec la mémoire tampon de stencil jouant le rôle de masque, le résultat est d’assombrir les pixels qui se trouvent dans les ombres.

Cela signifie que la géométrie de l’ombre est dessinée deux fois par source de lumière, ce qui entraîne une pression sur le débit du vertex du GPU. La fonctionnalité de stencil à deux côtés a été conçue pour atténuer cette situation. Dans cette approche, il existe deux ensembles de l’état du gabarit (nommés ci-dessous), un jeu pour les triangles frontaux et l’autre pour les triangles de face arrière. De cette façon, une seule passe est dessinée par volume de cliché instantané, par lumière.

Les modifications de l’API sont limitées à un nouvel ensemble d’États de rendu. Le nouvel état de rendu D3DRS \_ deux \_ côtés \_ StencilMODE peut avoir la valeur **true** ou **false**. Il a la **valeur false** par défaut, ce qui correspond au comportement actuel (DirectX 8). Lorsque cette propriété a la valeur **true** (elle ne fonctionne que si D3DSTENCILCAPS \_ TWOSIDED est défini), les États de rendu suivants s’appliquent uniquement aux triangles avant (sens horaire).



| État du rendu        | Description                                                                              |
|---------------------|------------------------------------------------------------------------------------------|
| D3DRS \_ STENCILFAIL  | D3DSTENCILOP à effectuer si le test du stencil échoue.                                                |
| D3DRS \_ STENCILZFAIL | D3DSTENCILOP à effectuer si le test stencil réussit et que le test z échoue.                              |
| D3DRS \_ STENCILPASS  | D3DSTENCILOP à effectuer si les deux stencils et z-tests réussissent.                                     |
| D3DRS \_ STENCILFUNC  | D3DCMPFUNC FN. Le test stencil réussit si ((Ref & Mask) stencilfn (gabarit & Mask)) a la valeur true. |



 

Un nouvel ensemble d’États de rendu s’applique aux triangles de face arrière (à gauche).



| État du rendu             | Description                                                                                    |
|--------------------------|------------------------------------------------------------------------------------------------|
| D3DRS \_ CCW \_ STENCILFAIL  | D3DSTENCILOP à effectuer si le test du stencil échoue.                                                      |
| D3DRS \_ CCW \_ STENCILZFAIL | D3DSTENCILOP à effectuer si le test stencil réussit et que le test z échoue.                                    |
| D3DRS \_ CCW \_ STENCILPASS  | D3DSTENCILOP à effectuer si les deux stencils et z-tests réussissent.                                           |
| D3DRS \_ CCW \_ STENCILFUNC  | Fonction D3DCMPFUNC. Le test stencil réussit si ((Ref & Mask) stencilfn (gabarit & Mask)) a la valeur true. |



 

Les États de rendu des stencils restants s’appliquent toujours à la fois à l’angle et dans le sens inverse.

D3DRS \_ deux \_ côtés \_ StencilMODE est ignoré pour les lignes et les sprites point, ce qui signifie que le comportement est identique à celui de DirectX 8. Les \_ États de rendu du stencil D3DRS CCW \_ \* sont ignorés.

Un nouveau bit d’extrémité indique si l’appareil prend en charge cette fonctionnalité. Les pilotes qui ne prennent pas en charge cette fonctionnalité sont censés ignorer ces nouveaux États de rendu. Tous les autres bits d’extrémité du stencil s’appliquent aux deux modes de mise en mémoire tampon des stencils. Étant donné que \_ \_ le stencil à deux côtés implique la possibilité de dessiner avec D3DCULLMODE \_ None Set, le Cap correspondant doit être défini par le pilote s’il prend en charge ce nouveau mode de stencil. Les laboratoires WHQL (Microsoft Windows Hardware Quality Labs) doivent respecter ce point.

Nouveaux États de rendu :


```
D3DRS_Two_Sided_StencilMODE // BOOL (default is FALSE)
D3DRS_CCW_STENCILFAIL     // Same default as D3DRS_STENCILFAIL
D3DRS_CCW_STENCILZFAIL    // Same default as D3DRS_STENCILZFAIL
D3DRS_CCW_STENCILPASS     // Same default as D3DRS_STENCILPASS
D3DRS_CCW_STENCILFUNC     // Same default as D3DRS_STENCILFUNC
```



Nouvelle limite :


```
D3DSTENCILCAPS_TWOSIDED // a flag on D3DCAPS9.StencilCaps
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Techniques de tampon de stencil](stencil-buffer-techniques.md)
</dt> <dt>

[**D3DRENDERSTATETYPE**](./d3drenderstatetype.md)
</dt> </dl>

 

 
