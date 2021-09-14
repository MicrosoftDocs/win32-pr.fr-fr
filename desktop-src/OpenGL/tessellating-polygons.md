---
title: Polygones le pavage
description: Polygones le pavage
ms.assetid: 3b219af0-96c3-4a83-8a40-bd7966d58398
keywords:
- Utilitaire OpenGL (GLU), pavage
- GLU (utilitaire OpenGL), pavage
- Utilitaire OpenGL (GLU), polygones simples
- GLU (utilitaire OpenGL), polygones simples
- polygones simples OpenGL
- Utilitaire OpenGL (GLU), polygones complexes
- GLU (utilitaire OpenGL), polygones complexes
- polygones complexes OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 475076f6372042d61c1662b445b7573709134c65
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127311654"
---
# <a name="tessellating-polygons"></a>Polygones le pavage

OpenGL peut afficher directement uniquement les polygones convexes simples. Un polygone est simple dans les cas suivants :

-   Les bords se croisent uniquement aux sommets.
-   Il n’y a aucun vertex dupliqué.
-   Exactement deux bords se rencontrent à n’importe quel vertex.

Pour afficher des polygones simples ou des polygones simples contenant des trous, vous devez d’abord facettiser les polygones (subdivisions en polygones convexes). Une telle sous-division est appelée *pavage*. GLU fournit une collection de fonctions qui effectuent le pavage. Notez que les fonctions de pavage GLU ne peuvent pas gérer les polygones non simples. Il n’existe pas de méthode OpenGL standard pour gérer ces polygones.

Étant donné que la facettisation est souvent requise et peut être plutôt délicate, cette section décrit en détail les fonctions de pavage GLU. Ces fonctions prennent comme des polygones simples en entrée qui peuvent inclure des trous, et elles retournent une combinaison de triangles, de maillages de triangle et de fans de triangle. Si vous ne souhaitez pas gérer les maillages ou les ventilateurs, vous pouvez spécifier que les fonctions de pavage retournent uniquement des triangles. Toutefois, les informations de maillage et de ventilateur améliorent les performances. Les fonctions de pavage de polygone triangulent un polygone concave avec un ou plusieurs contourages.

**Pour utiliser le pavage de polygones**

1.  Créez un objet polygonalisation avec [**gluNewTess**](glunewtess.md).
2.  Utilisez [*gluTessCallBack*](glutess.md) pour définir les fonctions de rappel que vous allez utiliser pour traiter les triangles générés par du paveur.
3.  Avec [**gluBeginPolygon**](glubeginpolygon.md), [**gluTessVertex**](glutessvertex.md), [**gluNextContour**](glunextcontour.md)et [**gluEndPolygon**](gluendpolygon.md), spécifiez le polygone avec des trous ou le polygone concave à défaire.

    Lorsque la description du polygone est terminée, la fonction de pavage appelle vos fonctions de rappel si nécessaire.

    Vous pouvez détruire des objets pavage inutiles avec [**gluDeleteTess**](gludeletetess.md).

Pour plus d’informations sur l’enregistrement des données de pavage, consultez [utilisation des fonctions de rappel](using-callback-functions.md).

 

 




