---
title: Lignes de Portage
description: Le portage du code du GL IRIS qui dessine des lignes est relativement simple, mais vous devez noter les différences de la façon dont OpenGL stipples. Le tableau suivant répertorie les fonctions d’IRIS dans le GL pour dessiner des lignes et leurs fonctions OpenGL équivalentes.
ms.assetid: de5fd544-5a64-44b5-8976-b96867e4006d
keywords:
- Portage de l’IRIS dans le GL, lignes
- Portage à partir de IRIS GL, lignes
- portage vers OpenGL à partir de IRIS GL, lignes
- Portage OpenGL à partir de IRIS GL, lignes
- fonctions de dessin, lignes
- lignes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a8b0dd0e254380e65171acef1a536038532a370da85ffaa361e8555f77457424
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119776959"
---
# <a name="porting-lines"></a>Lignes de Portage

Le portage du code du GL IRIS qui dessine des lignes est relativement simple, mais vous devez noter les différences de la façon dont OpenGL stipples. Le tableau suivant répertorie les fonctions d’IRIS dans le GL pour dessiner des lignes et leurs fonctions OpenGL équivalentes.



| Fonction IRIS GL                               | Fonction OpenGL                                                                                         | Signification                                                                                                                                      |
|------------------------------------------------|---------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| **bgnclosedline**,**endclosedline**<br/> | [**glBegin**](glbegin.md) ( \_ boucle de ligne GL \_ )[**glEnd**](glend.md)<br/>                          | Dessine une ligne fermée.                                                                                                                         |
| **bgnline**                                    | [**glBegin**](glbegin.md) ( \_ bande de lignes GL \_ )                                                          | Dessine des segments de ligne.                                                                                                                         |
| **linewidth**                                  | [**glLineWidth**](gllinewidth.md)                                                                      | Définit la largeur de ligne.                                                                                                                             |
| **getlwidth**                                  | [**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) (largeur de ligne du GL \_ \_ )            | Retourne la largeur de la ligne active.                                                                                                                  |
| **deflinestyle**,**setlinestyle**<br/>   | [**glLineStipple**](gllinestipple.md)                                                                  | Spécifie un modèle de stipple de ligne.                                                                                                            |
| **lsrepeat**                                   | argument factor de **glLineStipple**                                                                    | Définit un facteur de répétition pour le style de ligne.                                                                                                     |
| **getlstyle**                                  | [**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) ( \_ modèle STIPPLE de la ligne GL \_ \_ ) | Retourne le modèle de stipple de ligne.                                                                                                                |
| **getlsrepeat**                                | [**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) (STIPPLE de la ligne GL- \_ \_ \_ répéter)  | Retourne le facteur de répétition.                                                                                                                       |
| **linesmooth**, **smoothline**                 | [**glEnable**](glenable.md) (lisse de la \_ ligne GL \_ )                                                       | Active l’anticrénelage de ligne (pour plus d’informations sur l’anticrénelage, consultez [Portage de fonctions d’anticrénelage](porting-antialiasing-functions.md).) |



 

OpenGL n’utilise pas de tables pour la ligne stipples ; il ne gère qu’un seul modèle stipple. Vous pouvez utiliser [**glPushAttrib**](glpushattrib.md) et [**glPopAttrib**](glpopattrib.md) pour basculer entre les différents modèles de stipple.

OpenGL ne prend pas en charge les fonctions anciennes de style de ligne de l’IRIS dans le GL (telles que **Draw**, **lsbackup**, **getlsbackup**, etc.).

Pour plus d’informations sur le dessin des lignes avec anticrénelage, consultez [Portage de fonctions d’anticrénelage](porting-antialiasing-functions.md).

??

 

 





