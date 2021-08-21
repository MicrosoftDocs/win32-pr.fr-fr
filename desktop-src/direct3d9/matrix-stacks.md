---
description: La bibliothèque de l’utilitaire D3DX fournit l’interface ID3DXMATRIXStack.
ms.assetid: e3cfb29e-4ef6-4b48-ad6b-f0371f526507
title: Piles de matrices (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a480236bc42142b725e232a9fb92807be73fb03097104a0cc4fc08643f4361af
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119044325"
---
# <a name="matrix-stacks-direct3d-9"></a>Piles de matrices (Direct3D 9)

La bibliothèque de l’utilitaire D3DX fournit l’interface [**ID3DXMATRIXStack**](id3dxmatrixstack.md) . Il fournit un mécanisme pour permettre aux matrices d’être envoyées et dépilées d’une pile de matrices. L’implémentation d’une pile de matrices est un moyen efficace de suivre les matrices tout en parcourant une hiérarchie de transformation.

La bibliothèque de l’utilitaire D3DX utilise une pile de matrices pour stocker les transformations sous forme de matrices. Les différentes méthodes de l’interface [**ID3DXMATRIXStack**](id3dxmatrixstack.md) traitent de la matrice actuelle ou de la matrice située en haut de la pile. Vous pouvez effacer la matrice actuelle avec la méthode [**ID3DXMATRIXStack :: LoadIdentity**](id3dxmatrixstack--loadidentity.md) . Pour spécifier explicitement une certaine matrice à charger comme matrice de transformation actuelle, utilisez la méthode [**ID3DXMATRIXStack :: LoadMatrix**](id3dxmatrixstack--loadmatrix.md) . Ensuite, vous pouvez appeler la méthode [**ID3DXMATRIXStack :: MultMatrix**](id3dxmatrixstack--multmatrix.md) ou la méthode [**ID3DXMATRIXStack :: MultMatrixLocal**](id3dxmatrixstack--multmatrixlocal.md) pour multiplier la matrice actuelle par la matrice spécifiée.

La méthode [**ID3DXMATRIXStack ::P op**](id3dxmatrixstack--pop.md) vous permet de revenir à la matrice de transformation précédente et la méthode [**ID3DXMATRIXStack ::P par émission**](id3dxmatrixstack--push.md) ajoute une matrice de transformation à la pile.

Les matrices individuelles sur la pile de matrices sont représentées sous forme de matrices homogènes 4x4, définies par la structure [**D3DXMATRIX**](d3dxmatrix.md) de la bibliothèque de l’utilitaire D3DX.

La bibliothèque de l’utilitaire D3DX fournit une pile de matrice via un objet COM (Component Object Model).

## <a name="implementing-a-scene-hierarchy"></a>Implémentation d’une hiérarchie de scène

Une pile de matrices simplifie la construction de modèles hiérarchiques, dans lesquels des objets compliqués sont construits à partir d’une série d’objets plus simples.

Une scène, ou transformation, est généralement représentée par une structure de données d’arborescence. Chaque nœud de la structure de données de l’arborescence contient une matrice. Une matrice particulière représente la modification des systèmes de coordonnées du parent du nœud au nœud. Par exemple, si vous modélisez un ARM humain, vous pouvez implémenter la hiérarchie présentée dans le diagramme suivant.

![diagramme de la hiérarchie d’un bras humain](images/stack1.png)

Dans cette hiérarchie, la matrice du corps place le corps dans le monde. La matrice UpperArm contient la rotation de l’épaule, la matrice LowerArm contient la rotation du coude et la matrice de la main contient la rotation du poignet. Pour déterminer où se trouve la main par rapport au monde, vous multipliez toutes les matrices du corps à la main.

La hiérarchie précédente est trop simple, car chaque nœud n’a qu’un seul enfant. Si vous commencez à modéliser la main plus en détail, vous ajouterez probablement des doigts et un curseur de défilement. Chaque chiffre peut être ajouté à la hiérarchie en tant qu’enfant de main, comme indiqué dans le diagramme suivant.

![diagramme de la hiérarchie d’une main humaine](images/stack2.png)

Si vous parcourez le graphique complet du bras dans l’ordre à profondeur prioritaire, en passant d’un seul chemin d’accès à l’autre, avant de passer au chemin suivant : pour dessiner la scène, vous effectuez une séquence de rendu segmenté. Par exemple, pour afficher la main et les doigts, vous devez implémenter le modèle suivant.

1.  Poussez la matrice main sur la pile de matrice.
2.  Dessinez la main.
3.  Exécute un push de la matrice Thumb sur la pile de matrice.
4.  Dessinez le curseur.
5.  Affiche la matrice de curseur de défilement en dehors de la pile.
6.  Poussez la matrice Finger 1 sur la pile de matrice.
7.  Dessinez le premier doigt.
8.  Dépilez la matrice Finger 1 de la pile.
9.  Poussez la matrice Finger 2 sur la pile de matrice. Vous poursuivez cette procédure jusqu’à ce que tous les doigts et le curseur soient rendus.

Une fois que vous avez terminé le rendu des doigts, vous pouvez dépiler la matrice de la main.

Vous pouvez suivre ce processus de base dans le code avec les exemples suivants. Lorsque vous rencontrez un nœud lors de la recherche à profondeur prioritaire de la structure des données de l’arborescence, poussez la matrice en haut de la pile de matrice.


```
MatrixStack->Push();

MatrixStack->MultMatrix(pNode->matrix);
```



Lorsque vous avez terminé avec un nœud, affichez la matrice en haut de la pile de matrice.


```
MatrixStack->Pop();
```



De cette façon, la matrice située en haut de la pile représente toujours la transformation universelle du nœud actuel. Par conséquent, avant de dessiner chaque nœud, vous devez définir la matrice Direct3D.


```
pD3DDevice->SetTransform(D3DTS_WORLDMATRIX(0), *MatrixStack->GetTop());
```



Pour plus d’informations sur les méthodes spécifiques que vous pouvez effectuer sur une pile de matrices D3DX, consultez la rubrique de référence [**ID3DXMATRIXStack**](id3dxmatrixstack.md) .

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Pipeline de vertex](vertex-pipeline.md)
</dt> </dl>

 

 



