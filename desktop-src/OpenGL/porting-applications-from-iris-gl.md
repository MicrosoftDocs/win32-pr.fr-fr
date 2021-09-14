---
title: Portage d’applications à partir de IRIS GL
description: Portage d’applications à partir de IRIS GL
ms.assetid: d410b516-76a1-4cab-a843-801aa6215db5
keywords:
- OpenGL sur Windows, le portage du GL IRIS
- portage vers OpenGL, IRIS GL
- Portage OpenGL, IRIS GL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7c9e739b40f63bb2fd00bb62b4e5ec5566df3c82
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127009301"
---
# <a name="porting-applications-from-iris-gl"></a>Portage d’applications à partir de IRIS GL

Cette section répertorie les principales différences entre IRIS GL et OpenGL et décrit les étapes de base pour le portage du code de IRIS GL vers OpenGL. Pour obtenir la liste complète des différences entre IRIS GL et Open GL, voir [Iris GL et OpenGL différences](iris-gl-and-opengl-differences.md).

le portage de programmes de comptabilité en IRIS vers OpenGL pour Windows nécessite beaucoup plus de travail que la conversion de programmes OpenGL à partir du système de fenêtre X. Tandis que les programmes IRIS GL sont conçus pour s’exécuter avec un matériel et des logiciels spécifiques, OpenGL a été conçu pour la portabilité entre les différents systèmes.

Le tableau suivant répertorie quelques-unes des principales différences entre les programmes OpenGL et IRIS GL.



| Code OpenGL                                                                                                                                              | Code du GL IRIS                                                                                                                          |
|----------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| Indépendant du système d’exploitation ; ne contient aucune fonction pour la fenêtrage, la gestion des événements, l’allocation et la gestion des tampons, etc.                              | Dépend du système d’exploitation ; fenêtrage-les fonctions système sont mélangées avec des fonctions de rendu. Il n’existe aucun gestionnaire Windows dans IRIS GL. |
| Utilise une convention d’affectation de noms commune standard. Les fonctions OpenGL et les types définis commencent par un préfixe « GL » pour éviter les conflits avec d’autres bibliothèques.        | N’utilise pas une convention d’affectation de noms commune pour les fonctions et les types définis.                                                              |
| Gère les variables d’État (telles que la couleur, le brouillard, la texture, l’éclairage, etc.) directement et de manière cohérente. N’utilise pas de tables pour charger des valeurs de variables d’État. | Utilise des tables pour gérer les variables d’État et doit lier des variables aux valeurs de table.                                                        |
| Les listes d’affichage ne peuvent pas être modifiées.                                                                                                                          | Les listes d’affichage peuvent être modifiées.                                                                                                          |
| Ne fournit pas de format de fichier pour les polices.                                                                                                                | Fournit des fonctions pour gérer des polices et des chaînes de texte, ainsi qu’un format de fichier pour les polices.                                                      |
| Inclut une bibliothèque de l’utilitaire de comptabilité (GLU) qui contient des fonctions et des routines supplémentaires (telles que les routines de rendu NURBS et quadratiques).                    | Ne prend pas en charge la bibliothèque GLU.                                                                                                     |



 

**Utilisez la procédure générale suivante pour porter vos programmes IRIS GL vers OpenGL**

1.  réécrivez le code qui effectue des appels à un gestionnaire de fenêtres, à une configuration de fenêtre, à un périphérique ou à un événement, ou lorsque vous chargez une carte de couleurs à un code équivalent Windows. La réécriture d’une application d’un système d’exploitation à un autre peut être complexe et difficile. Ce sujet dépasse le cadre de cette section.
2.  Localisez tout code qui utilise des fonctions et routines IRIS GL. Traduisez ces fonctions en leurs fonctions OpenGL équivalentes. Pour obtenir la liste complète des fonctions et routines de l’IRIS et des équivalents OpenGL équivalents, consultez [fonctions OpenGL et leurs équivalents de la comptabilité Iris](opengl-functions-and-their-iris-gl-equivalents.md).
3.  Modifiez le code de l’IRIS dans le code de la comptabilité, comme décrit dans [Special Iris GL issues Problems](special-iris-gl-porting-issues.md).

<!-- -->

1.  réécrivez le code qui effectue des appels à un gestionnaire de fenêtres, à une configuration de fenêtre, à un périphérique ou à un événement, ou lorsque vous chargez une carte de couleurs à un code équivalent Windows. La réécriture d’une application d’un système d’exploitation à un autre peut être complexe et difficile. Ce sujet dépasse le cadre de cette section.
2.  Localisez tout code qui utilise des fonctions et routines IRIS GL. Traduisez ces fonctions en leurs fonctions OpenGL équivalentes. Pour obtenir la liste complète des fonctions et routines de l’IRIS et des équivalents OpenGL équivalents, consultez [fonctions OpenGL et leurs équivalents de la comptabilité Iris](opengl-functions-and-their-iris-gl-equivalents.md).
3.  Modifiez le code de l’IRIS dans le code de la comptabilité, comme décrit dans [Special Iris GL issues Problems](special-iris-gl-porting-issues.md).

 

 




