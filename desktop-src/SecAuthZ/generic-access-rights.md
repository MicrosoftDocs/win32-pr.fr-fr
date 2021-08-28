---
description: Les objets sécurisables utilisent un format de masque d’accès dans lequel les quatre bits de poids fort spécifient des droits d’accès génériques.
ms.assetid: e18cede9-9bf7-4866-850b-5d7fa43a5b0f
title: Droits d’accès génériques
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ee90a6866afc294cfef1c8fdad96e239f76ce8f9c251aeabc2d2a907e3e0bbe5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119672089"
---
# <a name="generic-access-rights"></a>Droits d’accès génériques

Les objets sécurisables utilisent un [format de masque d’accès](access-mask-format.md) dans lequel les quatre bits de poids fort spécifient des droits d’accès génériques. Chaque type d’objet sécurisable mappe ces bits à un ensemble de ses droits d’accès standard et spécifiques aux objets. par exemple, un objet de fichier Windows mappe le \_ bit de lecture générique au \_ contrôle de lecture et synchronise les droits d’accès standard et les droits d’accès de lecture de fichier \_ , de lecture de \_ fichier \_ \_ EA et de lecture de fichier spécifiques à l' \_ \_ objet. D’autres types d’objets mappent le \_ bit de lecture générique à n’importe quel jeu de droits d’accès adapté à ce type d’objet.

Vous pouvez utiliser des droits d’accès génériques pour spécifier le type d’accès dont vous avez besoin lorsque vous ouvrez un handle vers un objet. C’est généralement plus simple que de spécifier tous les droits standard et spécifiques correspondants.

Le tableau suivant montre les constantes définies pour les droits d’accès génériques.



| Constante         | Signification générique            |
|------------------|----------------------------|
| GÉNÉRIQUE \_ tout     | Tous les droits d’accès possibles |
| \_Exécution générique | Exécuter l’accès             |
| \_lecture générique    | Accès en lecture                |
| \_écriture générique   | Accès en écriture               |



 

Les applications qui définissent des objets sécurisables privés peuvent également utiliser les droits d’accès génériques.

 

 



