---
description: 'En savoir plus sur : clé d’index'
title: Clé d’index
TOCTitle: Index Key
ms:assetid: 104bdb1c-71ac-44f4-bbda-c553131aaad4
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269188(v=EXCHG.10)
ms:contentKeyID: 32765491
ms.date: 04/11/2016
ms.topic: article
ms.openlocfilehash: eff0812f363fa83d133ab087140d415d8e2dbad3
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126917456"
---
# <a name="index-key"></a>Clé d’index


_**S’applique à :** Windows | Windows Serveurs_

## <a name="index-key"></a>Clé d’index

Un index est créé sur les données de la table avec [JetCreateIndex](./jetcreateindex-function.md) ou il est possible de créer plusieurs index simultanément avec [JetCreateIndex2](./jetcreateindex2-function.md) à l’aide de la structure [JET_INDEXCREATE](./jet-indexcreate-structure.md) . L’index est défini en termes de tableau de colonnes, dans l’ordre de priorité. Ce tableau de colonnes est également appelé clé d’index. La clé d’index peut être définie comme index primaire lorsque l’option JET_bitIndexPrimary est définie dans le paramètre *Grbit* de [JetCreateIndex](./jetcreateindex-function.md) ou [JET_INDEXCREATE](./jet-indexcreate-structure.md). La clé d’index est une chaîne terminée par le caractère null de jetons se terminant par null, comme indiqué dans l’exemple suivant :

\+Col1 \\ 0-col2 \\ 0 + COL3 \\ 0 \\ 0

La clé de l’exemple peut être utilisée pour créer un index sur trois colonnes de la table. Chaque colonne spécifiée dans l’index est appelée « segment d’index » ou « colonne clé ». Le segment d’index peut être croissant ou décroissant en termes de contribution à la commande. Dans l’exemple ci-dessus, le nom de la première colonne de l’index est col1. Le signe + indique que col1 est indexé dans l’ordre croissant. La clause – Before col2 indique qu’elle est indexée dans l’ordre décroissant.

Lorsque des colonnes conditionnelles sont présentes dans l’index, la structure [JET_CONDITIONALCOLUMN](./jet-conditionalcolumn-structure.md) est utilisée pour indiquer la façon dont elles sont indexées. Une colonne conditionnelle peut être utilisée pour contrôler la présence ou l’absence d’une entrée d’index dans un index en fonction de la valeur dans la colonne conditionnelle correspondante sans affecter l’ordre de tri de l’index. Une colonne conditionnelle peut inclure ou exclure une entrée d’index de l’index si la valeur de cette colonne conditionnelle est NULL pour l’enregistrement correspondant.

Par défaut, la taille maximale de la clé d’index est donnée par la constante JET_cbKeyMost qui a toujours été 255 octets de données normalisées (octets de données, y compris la charge de l’indexation). à partir de Windows Vista, la taille maximale de la clé d’index peut être définie avec la structure [JET_INDEXCREATE](./jet-indexcreate-structure.md) . La taille maximale de la clé d’index correspond à la taille de la page de la base de données. Pour activer une taille de clé maximale personnalisée, spécifiez l’option Jet_bitIndexKeyMost dans le membre grbits de [JET_INDEXCREATE](./jet-indexcreate-structure.md)et définissez le membre **cbKeyMost** sur l’une des valeurs suivantes :

  - JET_cbKeyMost2KBytePage : lorsque la taille de la page de la base de données est de 2048 octets, la taille maximale de la clé d’index peut être comprise entre 255 octets minimum et 500 octets au maximum.

  - JET_cbKeyMost4KBytePage : lorsque la taille de la page de la base de données est de 4096 octets, la taille maximale de la clé d’index peut être comprise entre 255 octets minimum et 1000 octets au maximum.

  - JET_cbKeyMost8KBytePage : lorsque la taille de la page de la base de données est de 8196 octets, la taille maximale de la clé d’index peut être comprise entre 255 octets minimum et 2000 octets au maximum.

L’exemple indiqué dans le diagramme ci-dessous montre une table contenant des informations sur les employés. La table comporte 6 colonnes, chacune définissant un attribut d’employé spécifique. Un enregistrement de la table contient des valeurs pour un employé, telles que le nom de l’employé dans la colonne 1 et l’ID de l’employé dans la colonne 2. Un index primaire créé pour cette table organise les données en fonction du nom d’employé en premier, et l’ID d’employé en second. Le nom et l’ID sont indexés dans l’ordre croissant. Par exemple, un enregistrement contenant le nom Johnson et l’ID d’employé 12345 est listé avant un enregistrement avec le nom d’employé Jones et l’ID 10000. Tous les enregistrements pour Jones sont stockés ensemble dans la table, avec leurs ID d’employé dans l’ordre croissant, comme indiqué dans le tableau.

![ESE_Documentation_IndexTable](images/Gg269188.ESE_Documentation_IndexTable(EXCHG.10).gif "ESE_Documentation_IndexTable")

La clé de l’index primaire doit être unique, mais les clés de l’index secondaire peuvent être des doublons. Par exemple, si un index est créé sur le nom de famille et qu’il y a deux personnes avec Stevens dans la base de données, ESE renvoie une erreur Jet_errKeyDuplicate à partir de [JetUpdate](./jetupdate-function.md) ou [JetUpdate2](./jetupdate2-function.md), lorsque l’application tente d’insérer le deuxième « Stevens ». Lorsque la clé réelle est supérieure à la taille de clé maximale, la clé est tronquée. Les effets de troncation clés de recherche et d’unicité et doivent être gérés par l’application. Par exemple, si « Stevens » et « Stevenson » ont été stockés dans un index sur le nom de famille et que la taille maximale de la clé était trop petite pour stocker la partie « on » de « Stevenson », alors le moteur de base de données déclare que « Stevens » et « Stevenson » sont des doublons, même si ce n’est pas le cas. L’application doit être préparée à gérer les cas de ce type lors de la recherche et de la mise à jour si la définition d’index et les valeurs de colonne qu’elle indexe sont telles que la troncation de clé est une possibilité. à partir de Windows Vista, les applications peuvent spécifier l’option Jet_bitIndexDisallowTruncation dans [JET_INDEXCREATE](./jet-indexcreate-structure.md) ou [JetMakeKey](./jetmakekey-function.md). Si vous spécifiez cet indicateur, toute mise à jour de l’index entraînant l’échec d’une clé tronquée avec JET_errKeyTruncated. Dans le cas contraire, les clés sont tronquées en mode silencieux. Cela permettra à l’application de fonctionner sans problème pour les artefacts provoqués par la troncation de clé précédemment décrite.
