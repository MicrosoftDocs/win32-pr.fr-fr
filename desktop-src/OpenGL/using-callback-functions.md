---
title: Utilisation des fonctions de rappel
description: Les fonctions de rappel GLU, gluBeginPolygon, gluTessVertex, gluNextContour et gluEndPolygon, sont similaires aux fonctions de polygones OpenGL.
ms.assetid: e8277ba9-e270-4d7d-a29f-143f2f0d0324
keywords:
- Utilitaire OpenGL (GLU), fonctions de rappel
- GLU (utilitaire OpenGL), fonctions de rappel
- Utilitaire OpenGL (GLU), pavage
- GLU (utilitaire OpenGL), pavage
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a826d9416f94304762be2e840a3b6fea9ba458ec
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103839702"
---
# <a name="using-callback-functions"></a>Utilisation des fonctions de rappel

Les fonctions de rappel GLU, [**gluBeginPolygon**](glubeginpolygon.md), [**gluTessVertex**](glutessvertex.md), [**gluNextContour**](glunextcontour.md)et [**gluEndPolygon**](gluendpolygon.md), sont similaires aux fonctions de polygones OpenGL.

Elles enregistrent généralement les données pour les triangles, les maillages de triangle et les ventilateurs à triangle dans les structures de données définies par l’utilisateur ou dans des listes d’affichage OpenGL. Pour afficher les polygones, un autre code parcourt les structures de données ou appelle les listes d’affichage. Bien que les fonctions de rappel puissent appeler des fonctions OpenGL pour afficher directement les polygones, cette opération n’est généralement pas effectuée, car le pavage peut être gourmand en ressources en calcul. Il est judicieux d’enregistrer les données si vous souhaitez les afficher à nouveau... Les fonctions de pavage de GLU étant garanties qu’elles ne peuvent jamais retourner de nouveaux vertex, l’interpolation des vertex, des coordonnées de texture ou des couleurs n’est jamais nécessaire.

 

 




