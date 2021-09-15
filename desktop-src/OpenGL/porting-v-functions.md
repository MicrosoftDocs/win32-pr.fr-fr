---
title: Portage des fonctions v
description: Dans IRIS GL, vous utilisez des variations sur la fonction v pour spécifier des vertex. La fonction OpenGL équivalente est glVertex ci-dessous sont des exemples de glVertex.
ms.assetid: b4ac0c41-983a-4387-a69f-530c9094dc33
keywords:
- Portage de l’IRIS dans le GL, sommets
- Portage à partir de IRIS GL, vertex
- portage vers OpenGL à partir de IRIS GL, vertex
- Portage OpenGL à partir de IRIS GL, vertex
- fonctions de dessin, sommets
- vertex, Portage à partir de IRIS GL
- Portage de l’IRIS dans le GL, fonctions v
- Portage à partir de l’IRIS GL, fonctions v
- portage vers OpenGL à partir de l’IRIS GL, fonctions v
- Portage OpenGL depuis IRIS GL, fonctions v
- fonctions de dessin, fonctions v
- fonctions v
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bfd5e40915f891817606ac8517c0b3b980b436be
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127311702"
---
# <a name="porting-v-functions"></a>Portage des fonctions v

Dans IRIS GL, vous utilisez des variations sur la fonction **v** pour spécifier des vertex. La fonction OpenGL équivalente est [glVertex](glvertex-functions.md): vous trouverez ci-dessous des exemples de **glVertex**.

``` syntax
glVertex2[d|f|i|s][v]( x, y ); 
glVertex3[d|f|i|s][v]( x, y, z); 
glVertex4[d|f|i|s][v]( x, y, z, w);
```

La fonction **glVertex** prend des suffixes de la même façon que les autres appels OpenGL. Les versions vectorielles de l’appel prennent des tableaux de la taille appropriée comme arguments. Dans la version 2D, z = 0 et w = 1. Dans la version 3D, w = 1.

 

 




