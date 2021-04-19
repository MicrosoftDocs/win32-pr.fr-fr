---
description: L’opérateur ISA est un opérateur spécifique à WQL qui peut être utilisé dans les requêtes de données, d’événements et de schémas.
ms.assetid: 0520470c-ebfc-4c45-8a1f-47fd66bf8414
ms.tgt_platform: multiple
title: Opérateur ISA pour les requêtes de schéma
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7fb50146e4bd1219712c84bc1acec7fc7d50146b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106530642"
---
# <a name="isa-operator-for-schema-queries"></a>Opérateur ISA pour les requêtes de schéma

L’opérateur ISA est un opérateur spécifique à WQL qui peut être utilisé dans les requêtes de données, d’événements et de schémas.

Quand ISA est inclus dans la [clause WHERE](where-clause.md) d’une requête de schéma, il demande que la requête soit appliquée à toutes les sous-classes de la classe que vous spécifiez.

Par exemple, l’instruction suivante demande une notification toutes les 10 minutes des événements de modification d’instance pour toutes les instances qui sont membres d’une classe dérivant de la classe [**\_ disque logique Win32**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) .


```sql
SELECT * FROM __InstanceModificationEvent WITHIN 600
WHERE TargetInstance ISA "Win32_LogicalDisk"
```



La requête suivante retourne la définition de la classe du [**\_ processeur CIM**](/windows/desktop/CIMWin32Prov/cim-processor) et les définitions de toutes ses sous-classes.


```sql
SELECT * FROM meta_class WHERE __this ISA "CIM_Processor"
```



La classe **meta \_ Class** identifie cela comme une requête de schéma, la propriété **\_ \_ appelée identifie** la classe cible de la requête et l’opérateur ISA demande des définitions pour les sous-classes de la classe cible.

 

 
