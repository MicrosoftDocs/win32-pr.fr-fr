---
description: WMI utilise les chemins d’accès des objets dans les propriétés de référence des classes d’association pour identifier les objets connexes, ainsi que l’utilisation de chemins d’accès aux objets dans les paramètres d’entrée ou de sortie pour plusieurs méthodes.
ms.assetid: 07fee6f8-810e-4dec-8f0f-787756ee3beb
ms.tgt_platform: multiple
title: Exigences relatives au chemin d’accès de l’objet WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e2b46195eae3e8351c9c611a34c28cc9d5dd58d6
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127122489"
---
# <a name="wmi-object-path-requirements"></a>Exigences relatives au chemin d’accès de l’objet WMI

WMI utilise les chemins d’accès des objets dans les propriétés de référence des classes d’association pour identifier les objets connexes, ainsi que l’utilisation de chemins d’accès aux objets dans les paramètres d’entrée ou de sortie pour plusieurs méthodes. Étant donné que les chemins d’accès aux objets sont traités comme des chaînes à des fins de recherche et de comparaison, la valeur d’un chemin d’accès d’objet lorsqu’il est utilisé comme propriété de référence est toujours la chaîne elle-même et non l’objet déréférencé. Les comparaisons de chaînes qui traitent les chemins d’accès aux objets sont toujours sensibles à la casse.

Un chemin d’accès d’objet peut utiliser la syntaxe suivante :

-   Chaînes contenues entre guillemets simples.
-   Barres obliques comme séparateurs.
-   Barres obliques inverses en tant que séparateurs.
-   Constantes hexadécimales pour les entiers.
-   Constantes booléennes pour les classes avec des clés qui acceptent des valeurs booléennes.
-   Notation d’URL pour représenter des caractères non imprimables, tels que %20 pour un espace blanc.

En outre, une chaîne de chemin d’accès d’objet doit respecter les restrictions suivantes :

-   Un serveur local supposé avec un chemin d’accès d’espace de noms partiel. Par conséquent, la spécification de l’espace de noms root et default implique l’espace de noms racine et l’espace de noms par défaut sur le serveur local.
-   Aucun espace blanc dans un élément ou entre des éléments.
-   Les guillemets incorporés dans les chemins d’accès aux objets sont autorisés, mais doivent délimiter le guillemet avec les caractères d’échappement, comme dans une application C ou C++.
-   Seules les valeurs décimales sont reconnues comme des parties numériques de clés.

 

 



