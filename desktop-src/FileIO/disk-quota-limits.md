---
description: Décrit deux types de limites de quota de disque et la mesure des limites de quota de disque.
ms.assetid: 6595d5e0-eb97-437e-abd2-3a04faefde7d
title: Limites de quota de disque
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3f51fff88bcb29d12c52387267c5e910ba36fa15
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106517918"
---
# <a name="disk-quota-limits"></a>Limites de quota de disque

L’espace disque utilisé par chaque fichier est facturé directement à l’utilisateur propriétaire du fichier. Le propriétaire d’un fichier est identifié par l’identificateur de sécurité (SID) dans les informations de sécurité du fichier. L’espace disque total facturé pour un utilisateur est la somme de la longueur de tous les flux de données. En d’autres termes, les flux de jeu de propriétés et les flux de données utilisateur résidents affectent le quota de l’utilisateur.

Le quota n’est pas facturé pour les points de réanalyse, les descripteurs de sécurité ou d’autres métadonnées associées aux fichiers. La compression ou la décompression des fichiers n’affecte pas l’espace disque indiqué pour les fichiers. Par conséquent, les paramètres de quota sur un volume peuvent être comparés aux paramètres d’un autre volume.

Il existe deux types de limites de quota de disque, comme indiqué dans le tableau suivant.



| Limite                        | Description                                                                                                                                                                                                                                                                    |
|------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Seuil d'avertissement<br/> | Vous pouvez configurer le système pour générer une entrée de fichier journal système lorsque l’espace disque facturé à l’utilisateur dépasse cette valeur.<br/>                                                                                                                                         |
| Quota de disque dur<br/>        | Vous pouvez configurer le système pour générer une entrée de fichier journal système lorsque l’espace disque facturé à l’utilisateur dépasse cette valeur. Vous pouvez également configurer le système pour refuser de l’espace disque supplémentaire à l’utilisateur lorsque l’espace disque facturé à l’utilisateur dépasse cette valeur.<br/> |



 

Le système de fichiers NTFS crée automatiquement une entrée de quota utilisateur lorsqu’un utilisateur écrit pour la première fois sur le volume. Les entrées créées automatiquement se voient attribuer le seuil d’avertissement par défaut et les valeurs de limite de quota matériel pour le volume.

 

 




