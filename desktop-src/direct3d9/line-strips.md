---
description: Une bande est une primitive composée de segments de ligne connectés.
ms.assetid: 73905718-a4c6-4f73-beef-4cccac7eea8c
title: Bandes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6dd8ba98518cac542a9b8272e4f96494889ef24f269744626aa24e882c7af509
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118799629"
---
# <a name="line-strips"></a>Bandes

Une bande est une primitive composée de segments de ligne connectés. Votre application peut utiliser des bandes de lignes pour créer des polygones qui ne sont pas fermés. Un polygone fermé est un polygone dont le dernier vertex est connecté à son premier vertex par un segment de ligne. Si votre application crée des polygones basés sur des bandes, il n’est pas garanti que les vertex soient coplanés.

L’illustration suivante montre une bande de lignes rendue.

![illustration d’une bande](images/linstrip.gif)

Le code suivant montre comment créer des sommets pour cette bande.


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



L’exemple de code ci-dessous montre comment afficher une bande de courbes dans Direct3D 9 à l’aide de [**IDirect3DDevice9 ::D rawprimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) .


```
//
// It is assumed that d3dDevice is a valid
// pointer to a IDirect3DDevice9 interface.
//
d3dDevice->DrawPrimitive( D3DPT_LINESTRIP, 0, 5 );
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Primitives](primitives.md)
</dt> </dl>

 

 
