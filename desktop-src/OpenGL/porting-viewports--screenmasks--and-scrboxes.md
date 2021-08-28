---
title: Portage des Viewports, Screenmasks et Scrboxes
description: Les fonctions de fenêtre d’affichage du code IRIS suivantes n’ont pas d’équivalent OpenGL
ms.assetid: 223e9b5b-1ddd-45a6-8489-b262d0207a5a
keywords:
- Portage de l’IRIS dans le GL, fonctions de fenêtre d’affichage
- Portage à partir de IRIS GL, fonctions Viewport
- portage vers OpenGL à partir de l’IRIS GL, fonctions Viewport
- Portage OpenGL à partir de IRIS GL, fonctions Viewport
- fonctions de fenêtre d’affichage
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fb1a01cfb038faf87e48381856fe281bf2c935d13fedb78b79266e2af4fe15e4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119776909"
---
# <a name="porting-viewports-screenmasks-and-scrboxes"></a>Portage des Viewports, Screenmasks et Scrboxes

Les fonctions de fenêtre d’affichage du code IRIS suivantes n’ont pas d’équivalent OpenGL :

-   **reshapeviewport**
-   **scrbox**
-   **getscrbox**

Avec la fonction IRIS GL **Viewport** , vous spécifiez les coordonnées x (en pixels) de gauche et de droite d’un rectangle de fenêtre d’affichage et les coordonnées y pour le haut et le bas. Toutefois, avec la fonction OpenGL [**glViewport**](glviewport.md) , vous spécifiez les coordonnées x et y (en pixels) du coin inférieur gauche du rectangle de la fenêtre d’affichage, ainsi que sa largeur et sa hauteur.

Le tableau suivant répertorie les fonctions de fenêtre d’affichage du GL d’IRIS et leurs fonctions OpenGL équivalentes.



| Fonction IRIS GL                          | Fonction OpenGL                                                                                         | Signification                      |
|-------------------------------------------|---------------------------------------------------------------------------------------------------------|------------------------------|
| **fenêtre d’affichage** (gauche, droite, bas, haut) | [**glViewport**](glviewport.md) (x, y, largeur, hauteur)                                                | Définit la fenêtre d’affichage.           |
| **popviewportpushviewport**<br/>    | [**glPopAttrib**](glpopattrib.md)[**glPushAttrib**](glpushattrib.md) ( \_ bit de fenêtre d’affichage GL \_ )<br/> | Exécute un push sur la pile et le dépile.   |
| **getviewport**                           | [**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) ( \_ fenêtre d’affichage GL)               | Retourne les dimensions de la fenêtre d’affichage. |



 

??

 

 





