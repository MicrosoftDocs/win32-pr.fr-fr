---
title: Fonctions de sélection du Portage
description: Toutes les fonctions d’IRIS GL de prélèvement ont des équivalents OpenGL, à l’exception de clearhitcode. Le tableau suivant répertorie les fonctions d’IRIS du GL de prélèvement et leurs fonctions OpenGL équivalentes.
ms.assetid: f8fbd0c2-14bf-47bc-be7f-eeef346dbac1
keywords:
- Portage du GL d’IRIS, prélèvement
- Portage à partir de IRIS GL, prélèvement
- portage vers OpenGL à partir de IRIS GL, prélèvement
- Portage OpenGL depuis IRIS GL, prélèvement
- mat
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db4c0ea6011860f7d5010dd0bb7d5d23b671d99a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127014003"
---
# <a name="porting-picking-functions"></a>Fonctions de sélection du Portage

Toutes les fonctions d’IRIS GL de prélèvement ont des équivalents OpenGL, à l’exception de **clearhitcode**. Le tableau suivant répertorie les fonctions d’IRIS du GL de prélèvement et leurs fonctions OpenGL équivalentes.



| Fonction IRIS GL                | Fonction OpenGL                                                                           | Signification                                |
|---------------------------------|-------------------------------------------------------------------------------------------|----------------------------------------|
| **clearhitcode**                | Non pris en charge.                                                                            | Efface les variables globales et Hitcode.    |
| **pickselect**<br/>       | [**glRenderMode**](glrendermode.md) ( \_ sélection GL)                                       | Bascule en mode sélection ou choix. |
| **endpickendselect**<br/> | [**glRenderMode**](glrendermode.md) ( \_ rendu GL)                                       | Bascule en mode de rendu.            |
| **picksize**                    | [**gluPickMatrix**](glupickmatrix.md)[**glSelectBuffer**](glselectbuffer.md)<br/> | Définit le tableau de retour.                 |
| **initnames**                   | [**glInitNames**](glinitnames.md)                                                        |                                        |
| **pushnamepopname**<br/>  | [**glPushName**](glpushname.md)[**glPopName**](glpopname.md)<br/>                 |                                        |
| **loadname**                    | [**glLoadName**](glloadname.md)                                                          |                                        |



 

Pour plus d’informations sur le prélèvement, consultez [**gluPickMatrix**](glupickmatrix.md).

 

 





