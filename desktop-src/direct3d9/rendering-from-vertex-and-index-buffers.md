---
description: Direct3D prend en charge les méthodes de dessin indexées et non indexées.
ms.assetid: 9b94ab86-2a6a-4abd-ab56-95315f473226
title: Rendu à partir de mémoires tampons de vertex et d’index (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0e4290dc2ff40e1ec0448e3948342aa3b02ac62bf9866a44958ea53bee9658d8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118092630"
---
# <a name="rendering-from-vertex-and-index-buffers-direct3d-9"></a>Rendu à partir de mémoires tampons de vertex et d’index (Direct3D 9)

Direct3D prend en charge les méthodes de dessin indexées et non indexées. Les méthodes indexées utilisent un ensemble unique d’index pour tous les composants de vertex. Les données de vertex sont stockées dans des mémoires tampons de vertex, et les données d’index sont stockées dans des mémoires tampons d’index. Voici quelques scénarios courants de dessin de primitives utilisant des tampons de vertex et d’index.

Ces exemples comparent l’utilisation de [**IDirect3DDevice9 ::D rawprimitive**](/windows/desktop/api) et [**IDirect3DDevice9 ::D rawindexedprimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawindexedprimitive)

## <a name="scenario-1-drawing-two-triangles-without-indexing"></a>Scénario 1 : dessin de deux triangles sans indexation

Supposons que vous souhaitiez dessiner le quadruple qui est représenté dans l’illustration suivante.

![illustration d’un carré constitué de deux triangles](images/dip-fig1.png)

Si vous utilisez le type de primitive List de triangle pour restituer les deux triangles, chaque triangle est stocké sous la forme de 3 Vertex individuels, ce qui donne une mémoire tampon de vertex similaire à l’illustration suivante.

![diagramme d’une mémoire tampon de vertex qui définit trois vertex pour deux triangles](images/dip-fig2.png)

L’appel de dessin est très simple ; à partir de l’emplacement 0 dans la mémoire tampon de vertex, dessinez deux triangles. Si l’élimination est activée, l’ordre des vertex sera important. Cet exemple est basé sur l’État par défaut de l’élimination dans le sens inverse des aiguilles d’une montre. les triangles visibles doivent donc être dessinés dans le sens des aiguilles d’une montre. Le type primitif de liste de triangles lit simplement trois vertex dans l’ordre linéaire à partir de la mémoire tampon pour chaque triangle. cet appel dessinera donc des triangles (0, 1, 2) et (3, 4, 5) :


```
DrawPrimitive( D3DPT_TRIANGLELIST, // PrimitiveType
               0,                  // StartVertex
               2 );                // PrimitiveCount
```



## <a name="scenario-2-drawing-two-triangles-with-indexing"></a>Scénario 2 : dessin de deux triangles avec indexation

Comme vous pouvez le constater, la mémoire tampon de vertex contient des données en double dans les emplacements 0 et 4, 2 et 5. Cela est logique, car les deux triangles partagent deux vertex communs. Ces données dupliquées sont inutiles et la mémoire tampon de vertex peut être compressée à l’aide d’une mémoire tampon d’index. Une mémoire tampon de vertex plus petite réduit la quantité de données de vertex qui doit être envoyée à la carte graphique. Plus important encore, l’utilisation d’un tampon d’index permet à l’adaptateur de stocker des vertex dans un cache de vertex ; Si la primitive qui est dessinée contient un vertex récemment utilisé, ce vertex peut être extrait du cache au lieu de le lire à partir de la mémoire tampon de vertex, ce qui entraîne une augmentation importante des performances.

Une mémoire tampon d’index « indexe » dans la mémoire tampon de vertex afin que chaque vertex unique doive être stocké une seule fois dans la mémoire tampon de vertex. Le diagramme suivant illustre une approche indexée du scénario de dessin précédent.

![diagramme d’une mémoire tampon d’index pour la mémoire tampon de vertex précédente](images/dip-fig3.png)

la mémoire tampon d’index stocke VB valeurs d’index, qui font référence à un vertex particulier dans la mémoire tampon de vertex. une mémoire tampon de vertex peut être considérée comme un tableau de vertex, de sorte que l’index VB est simplement l’index dans la mémoire tampon de vertex pour le vertex cible. De même, un index IB est un index dans le tampon d’index. cela peut s’avérer très confus très rapidement si vous n’êtes pas vigilant. assurez-vous que vous êtes bien clair sur le vocabulaire utilisé : VB index de valeurs d’index dans la mémoire tampon de vertex, index de valeurs d’index IB dans le tampon d’index, et le tampon d’index lui-même stocke VB valeurs d’index.

L’appel de dessin est illustré ci-dessous. Les significations de tous les arguments sont discutées à la longueur du scénario de dessin suivant. pour le moment, il vous suffit de noter que cet appel demande à Direct3D de restituer une liste de triangles contenant deux triangles, en commençant à l’emplacement 0 dans la mémoire tampon d’index. Cet appel dessinera les deux mêmes triangles dans le même ordre que précédemment, garantissant ainsi une orientation appropriée dans le sens des aiguilles d’une montre :


```
   
DrawIndexedPrimitive( D3DPT_TRIANGLELIST, // PrimitiveType
                    0,                  // BaseVertexIndex
                    0,                  // MinIndex
                    4,                  // NumVertices
                    0,                  // StartIndex
                    2 );                // PrimitiveCount
```



## <a name="scenario-3-drawing-one-triangle-with-indexing"></a>Scénario 3 : dessin d’un triangle avec indexation

Supposons maintenant que vous souhaitez dessiner uniquement le deuxième triangle, mais que vous souhaitez utiliser la même mémoire tampon de vertex et la même mémoire tampon d’index que ceux utilisés lors du dessin de la totalité du quadruple, comme indiqué dans le diagramme suivant.

![diagramme du tampon d’index et de la mémoire tampon de vertex pour le deuxième triangle](images/dip-fig4.png)

Pour cet appel de dessin, le premier index IB utilisé est 3 ; Cette valeur est appelée StartIndex. l’Index VB le plus bas utilisé est 0 ; Cette valeur est appelée MinIndex. Même si seuls trois vertex sont requis pour dessiner le triangle, ces trois vertex sont répartis sur quatre emplacements adjacents dans la mémoire tampon de vertex ; le nombre d’emplacements dans le bloc contigu de mémoire tampon de vertex requis pour l’appel de dessin est appelé NumVertices et sera défini sur 4 dans cet appel. Les valeurs MinIndex et NumVertices sont en fait simplement des indications pour aider Direct3D à optimiser l’accès à la mémoire lors du traitement des vertex logiciels et peuvent simplement être définies pour inclure l’intégralité de la mémoire tampon du vertex au prix des performances.

Voici l’appel de dessin pour le cas à triangle unique ; la signification de l’argument BaseVertexIndex sera expliquée ci-dessous :


```
   
DrawIndexedPrimitive( D3DPT_TRIANGLELIST, // PrimitiveType
                    0,                  // BaseVertexIndex
                    0,                  // MinIndex
                    4,                  // NumVertices
                    3,                  // StartIndex
                    1 );                // PrimitiveCount
```



## <a name="scenario-4-drawing-one-triangle-with-offset-indexing"></a>Scénario 4 : dessin d’un triangle avec l’indexation de décalage

BaseVertexIndex est une valeur ajoutée à chaque index VB stocké dans la mémoire tampon d’Index. Par exemple, si nous avions passé la valeur 50 pour BaseVertexIndex lors de l’appel précédent, cela équivaut à utiliser le tampon d’index dans le diagramme suivant pour la durée de l’appel DrawIndexedPrimitive :

![diagramme d’une mémoire tampon d’index avec une valeur de 50 pour basevertexindex](images/dip-fig5.png)

Cette valeur est rarement définie sur une valeur différente de 0, mais peut être utile si vous souhaitez découpler le tampon d’index de la mémoire tampon de vertex : si, lors du remplissage du tampon d’index pour un maillage particulier, l’emplacement du maillage dans la mémoire tampon de vertex n’est pas encore connu, vous pouvez simplement faire en sorte que les sommets du maillage soient situés au début lorsqu’il est temps d’effectuer l’appel de dessin, transmettez simplement l’emplacement de départ réel en tant que BaseVertexIndex.

Cette technique peut également être utilisée lors du dessin de plusieurs instances d’une maille à l’aide d’une seule mémoire tampon d’index ; par exemple, si la mémoire tampon de vertex contenait deux mailles avec un ordre de dessin identique mais des vertex légèrement différents (peut-être des couleurs diffuses ou des coordonnées de texture différentes), les deux mailles peuvent être dessinées à l’aide de différentes valeurs pour BaseVertexIndex. Grâce à ce concept, vous pouvez utiliser une seule mémoire tampon d’index pour dessiner plusieurs instances d’une maille, chacune contenue dans une mémoire tampon de vertex différente, en recourant simplement à la mémoire tampon de vertex active et en ajustant les BaseVertexIndex en fonction des besoins. Notez que la valeur BaseVertexIndex est également ajoutée automatiquement à l’argument MinIndex, ce qui est utile lorsque vous voyez comment il est utilisé :

Supposons maintenant que nous voulons à nouveau dessiner uniquement le deuxième triangle du Quad en utilisant le même tampon d’index qu’auparavant ; toutefois, une autre mémoire tampon de vertex est utilisée dans laquelle le quad se trouve à VB Index 50. L’ordre relatif des vertex Quad reste inchangé, seul l’emplacement de départ dans la mémoire tampon de vertex est différent. Le tampon d’index et la mémoire tampon de vertex ressemblent au diagramme suivant.

![diagramme du tampon d’index et de la mémoire tampon de vertex avec un index VB de 50](images/dip-fig6.png)

Voici l’appel de dessin approprié ; Notez que BaseVertexIndex est la seule valeur qui a changé par rapport au scénario précédent :


```
   
DrawIndexedPrimitive( D3DPT_TRIANGLELIST, // PrimitiveType
                    50,                 // BaseVertexIndex
                    0,                  // MinIndex
                    4,                  // NumVertices
                    3,                  // StartIndex
                    1 );                // PrimitiveCount
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Rendu des primitives](rendering-primitives.md)
</dt> </dl>

 

 
