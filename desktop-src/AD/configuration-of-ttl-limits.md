---
title: Configuration des limites de durée de vie
description: Un client peut demander une valeur de durée de vie pour une entrée allant de 1 à 31557600 (c’est-à-dire de 1 seconde à 1 an).
ms.assetid: 4009702c-7992-4e20-9d37-384f8137ba8f
ms.tgt_platform: multiple
keywords:
- Configuration des limites de durée de vie AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d2786258d060ef4261dcd9fbfad359c71f2dbaeb
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122881595"
---
# <a name="configuration-of-ttl-limits"></a>Configuration des limites de durée de vie

Un client peut demander une valeur de durée de vie pour une entrée allant de 1 à 31557600 (c’est-à-dire de 1 seconde à 1 an). Cette plage de valeurs d’attribut sera appliquée par les valeurs d’attribut **rangeLower** et **rangeUpper** dans la définition de **schéma** d’attribut pour l’attribut **entryTTL** . Conformément à la norme RFC 2589, les serveurs d’annuaire n’ont pas besoin d’accepter cette valeur et peuvent renvoyer une valeur TTL différente au client. Les clients doivent être en mesure d’utiliser cette valeur dictée par le serveur, car leur période d’actualisation du client (CRP), qui régit la fréquence à laquelle le client doit effectuer l’opération d’actualisation sur l’entrée dynamique.

Active Directory Domain Services fournir aux administrateurs la possibilité de configurer les valeurs de durée de vie par défaut et minimale pour une forêt. La valeur TTL par défaut est celle qui sera affectée à une entrée dynamique nouvellement créée si une durée de vie n’est pas explicitement spécifiée. La durée de vie minimale remplace toute valeur TTL spécifiée par le client inférieure à la valeur minimale configurée. Aucune valeur de durée de vie maximale configurable ne doit être fournie, car un maximum est imposé par la valeur d’attribut **rangeUpper** dans l’objet **attributeSchema** . Permettre aux administrateurs de configurer ces valeurs leur permettra de définir des valeurs de durée de vie qui appliqueront un trafic d’actualisation faible ou, à l’autre extrême, fournira un répertoire très à jour.

Les valeurs par défaut pour les deux paramètres TTL configurables sont les suivantes :

-   Valeur TTL par défaut = 86400 secondes (1 jour)
-   Valeur TTL minimale = 900 secondes (15 minutes)

les paramètres TTL configurables sont stockés sous la forme d’entrées AVA (attribute value assertion) au format « &lt; value-name &gt; = &lt; value &gt; » dans l’attribut **ms-DS-Other-Paramètres** de l’objet NTDS-Service donné par le nom de domaine suivant dans la partition de Configuration :


```C++
CN=Directory Service,CN=Windows NT,CN=Services,CN=Configuration,DC=...
```



La syntaxe d’AVA exacte, pour les deux paramètres TTL configurables, est la suivante, où NNNN est exprimé en secondes :


```C++
DynamicObjectDefaultTTLSeconds=NNNN
```




```C++
DynamicObjectMinTTLSeconds=NNNN
```



Ces valeurs peuvent être définies par un administrateur via l’utilitaire de ligne de commande Ntdsutil.

 

 




