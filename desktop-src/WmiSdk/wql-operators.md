---
description: Décrit les opérateurs WQL utilisés dans la clause WHERE ou l’instruction SELECT.
ms.assetid: a62de66d-d5ba-49a1-8262-bfa10ac2db75
ms.tgt_platform: multiple
title: Opérateurs WQL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2a441afb661e4f8d92e21d944462dddd6d7390fd2dbe871512342f7c9251d6ee
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118553086"
---
# <a name="wql-operators"></a>Opérateurs WQL

le langage WQL (Windows Management Instrumentation Query Language) prend en charge un ensemble d’opérateurs standard utilisés dans la [clause where](where-clause.md) d’une instruction SELECT, comme suit.



| Opérateur       | Description              |
|----------------|--------------------------|
| =              | Égal à                 |
| <           | Inférieur à                |
| >           | Supérieur à             |
| <=          | Inférieur ou égal à    |
| >=          | Supérieur ou égal à |
| ! = ou <> | Différent de             |



 

Il existe quelques opérateurs supplémentaires spécifiques à WQL : est, n’est pas, ISA et LIKE. Les opérateurs IS et IS NOT ne sont valides dans la clause WHERE que si la constante est **null**. Par exemple, les requêtes suivantes sont valides :


```sql
SELECT * FROM Win32_LogicalDisk WHERE FileSystem IS NULL
SELECT * FROM Win32_LogicalDisk WHERE FileSystem IS NOT NULL
```



Les requêtes suivantes montrent des utilisations non valides de IS et NOT :


```sql
SELECT * FROM Win32_LogicalDisk WHERE DriveType IS 5
SELECT * FROM Win32_LogicalDisk WHERE FileSystem IS NOT "NTFS"
```



L’opérateur ISA est utilisé dans la clause WHERE des requêtes de données et d’événements pour tester des objets incorporés pour une hiérarchie de classes. L’opérateur ISA élimine la nécessité d’effectuer le suivi des classes récemment dérivées lors de la demande d’une hiérarchie de classes. Lorsque vous utilisez ISA, les sous-classes nouvellement créées et existantes de la classe demandée sont automatiquement incluses dans le jeu de résultats.

Pour plus d’informations sur la syntaxe et l’utilisation de cet opérateur, consultez les rubriques suivantes :

-   [Opérateur ISA pour les requêtes de données](isa-operator-for-data-queries.md)
-   [Opérateur ISA pour les requêtes d’événements](isa-operator-for-event-queries.md)
-   [Opérateur ISA pour les requêtes de schéma](isa-operator-for-schema-queries.md)

L’opérateur LIKE est valide dans la clause WHERE et est utilisé pour déterminer si une chaîne de caractères donnée correspond à un modèle spécifié. Par exemple, la requête suivante retourne toutes les instances de \_ classes Win32.


```sql
SELECT * FROM Meta_Class WHERE __Class LIKE "%Win32%"
```



Pour plus d’informations sur la syntaxe et l’utilisation de cet opérateur, consultez [Like, opérateur](like-operator.md).

 

 



