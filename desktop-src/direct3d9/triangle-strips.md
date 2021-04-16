---
description: Une bande triangulaire est une série de triangles connectés.
ms.assetid: 3923c570-47a4-4b53-a097-731981380ae0
title: Bandes triangulaires
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b2766529a37b994e5fe30815ca6300476f06c7d4
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104557769"
---
# <a name="triangle-strips"></a>Bandes triangulaires

Une bande triangulaire est une série de triangles connectés. Étant donné que les triangles sont connectés, l’application n’a pas besoin de spécifier à plusieurs reprises les trois vertex pour chaque triangle. Par exemple, vous n’avez besoin que de sept sommets pour définir la bande triangulaire suivante.

![illustration d’une bande triangulaire avec sept sommets](images/tristrip.png)

Le système utilise les vertex v1, v2 et v3 pour dessiner le premier triangle. v2, V4 et v3 pour dessiner le deuxième triangle ; v3, V4 et V5 pour dessiner le troisième ; v4, V6 et V5 pour dessiner le quatrième ; et ainsi de suite. Notez que les sommets du deuxième et du quatrième triangles sont dans le désordre. Cela est nécessaire pour s’assurer que tous les triangles sont dessinés dans l’orientation dans le sens des aiguilles d’une montre.

La plupart des objets dans les scènes 3D sont composés de bandes triangulaires. Cela est dû au fait que les bandes de triangle peuvent être utilisées pour spécifier des objets complexes d’une manière qui utilise efficacement la mémoire et le temps de traitement.

L’illustration suivante représente une bande triangulaire rendue.

![illustration d’une bande triangulaire rendue](images/tstrip2.png)

Le code suivant montre comment créer des vertex pour cette bande triangulaire.


```
struct CUSTOMVERTEX
{
float x,y,z;
};

CUSTOMVERTEX Vertices[] = 
{
    {-5.0, -5.0, 0.0},
    { 0.0,  5.0, 0.0},
    { 5.0, -5.0, 0.0},
    {10.0,  5.0, 0.0},
    {15.0, -5.0, 0.0},
    {20.0,  5.0, 0.0}
};
```



L’exemple de code ci-dessous montre comment restituer cette bande triangulaire dans Direct3D 9 à l’aide de [**IDirect3DDevice9 ::D rawprimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive).


```
//
// It is assumed that d3dDevice is a valid
// pointer to a IDirect3DDevice9 interface.
//
d3dDevice->DrawPrimitive( D3DPT_TRIANGLESTRIP, 0, 4);
```



Utilisez une bande triangulaire pour restituer des triangles qui ne sont pas connectés les uns aux autres. Pour ce faire, spécifiez un triangle dégenerate (autrement dit, un triangle dont la zone est égale à zéro) dans la liste de triangles. Cela crée une ligne entre les deux triangles qui ne s’affiche pas. Pour afficher uniquement le premier et le dernier triangles de l’exemple précédent, modifiez la mémoire tampon du vertex comme indiqué ici :


```
CUSTOMVERTEX Vertices[] =
{
    {-5.0, -5.0, 0.0},
    { 0.0,  5.0, 0.0},
    { 5.0, -5.0, 0.0},
    { 5.0, -5.0, 0.0}, // degenerate triangle
    {10.0,  5.0, 0.0}, // degenerate triangle
    {10.0,  5.0, 0.0},
    {15.0, -5.0, 0.0},
    {20.0,  5.0, 0.0}
};
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Primitives](primitives.md)
</dt> </dl>

 

 
