---
description: Une action personnalisée peut appeler des fonctions écrites en VBScript ou JScript.
ms.assetid: d859713f-b8b8-4eb0-b678-52b5d880bd20
title: scripts ;
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 114a11c12e94dd2f3285757bd01167f14b412ac6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106533643"
---
# <a name="scripts"></a>scripts ;

Une action personnalisée peut appeler des fonctions écrites en VBScript ou JScript. Windows Installer ne fournit pas le moteur de script. Les auteurs souhaitant utiliser un langage de script pendant l’installation doivent donc s’assurer que le moteur de script approprié est disponible.

Le programme d’installation ne prend pas en charge la version 1,0 de JScript.

Une action personnalisée 64 bits basée sur des scripts doit être marquée explicitement comme une action personnalisée 64 bits en ajoutant le bit **msidbCustomActionType64BitScript** au type numérique actions personnalisées dans la colonne type de la table [CustomAction](customaction-table.md) . Pour plus d’informations [, consultez actions personnalisées 64 bits](64-bit-custom-actions.md).

Les types d’actions personnalisées de base suivants appellent des fonctions écrites en script.



| Type d’action personnalisé                                 | Description                                                                                    |
|----------------------------------------------------|------------------------------------------------------------------------------------------------|
| [Type d’action personnalisé 5](custom-action-type-5.md)   | Fichier JScript stocké dans un flux de table binaire.                                                  |
| [Type d’action personnalisée 21](custom-action-type-21.md) | Fichier JScript installé avec un produit.                                                 |
| [Type d’action personnalisé 53](custom-action-type-53.md) | Texte JScript spécifié par une valeur de propriété.                                                    |
| [Type d’action personnalisé 37](custom-action-type-37.md) | Texte JScript stocké dans la colonne cible de la table [CustomAction](customaction-table.md) .  |
| [Type d’action personnalisé 6](custom-action-type-6.md)   | Fichier VBScript stocké dans un flux de table [binaire](binary-table.md) .                             |
| [Type d’action personnalisée 22](custom-action-type-22.md) | Fichier VBScript installé avec un produit.                                                |
| [Type d’action personnalisé 54](custom-action-type-54.md) | Texte VBScript spécifié par une valeur de propriété.                                                   |
| [Type d’action personnalisé 38](custom-action-type-38.md) | Texte VBScript stocké dans la colonne cible de la table [CustomAction](customaction-table.md) . |



 

> [!Note]  
> Le programme d’installation exécute des actions personnalisées de script directement et n’utilise pas Windows Script Host. L’objet **wscript** ne peut pas être utilisé à l’intérieur d’une action personnalisée de script, car cet objet est fourni par Windows Script Host. Les objets dans le modèle d’objet Windows Script Host peuvent uniquement être utilisés dans des actions personnalisées si Windows Script Host est installé sur l’ordinateur en créant de nouvelles instances de l’objet, avec un appel à CreateObject et en fournissant le ProgId de l’objet (par exemple « WScript. Shell »). Selon le type d’action personnalisée de script, l’accès à certains objets et méthodes du modèle objet Windows Script Host peut être refusé pour des raisons de sécurité.

 

Pour plus d’informations, consultez la [liste récapitulative de tous les types d’actions personnalisées](summary-list-of-all-custom-action-types.md) pour obtenir un résumé de tous les types d’actions personnalisées et la façon dont elles sont encodées dans la table [CustomAction](customaction-table.md) .

 

 



