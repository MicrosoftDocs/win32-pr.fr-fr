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
# <a name="isa-operator-for-schema-queries"></a><span data-ttu-id="e2ef8-103">Opérateur ISA pour les requêtes de schéma</span><span class="sxs-lookup"><span data-stu-id="e2ef8-103">ISA Operator for Schema Queries</span></span>

<span data-ttu-id="e2ef8-104">L’opérateur ISA est un opérateur spécifique à WQL qui peut être utilisé dans les requêtes de données, d’événements et de schémas.</span><span class="sxs-lookup"><span data-stu-id="e2ef8-104">The ISA operator is a WQL-specific operator that can be used in data, event, and schema queries.</span></span>

<span data-ttu-id="e2ef8-105">Quand ISA est inclus dans la [clause WHERE](where-clause.md) d’une requête de schéma, il demande que la requête soit appliquée à toutes les sous-classes de la classe que vous spécifiez.</span><span class="sxs-lookup"><span data-stu-id="e2ef8-105">When ISA is included in the [WHERE clause](where-clause.md) of an schema query, it requests that the query be applied to all subclasses of the class you specify.</span></span>

<span data-ttu-id="e2ef8-106">Par exemple, l’instruction suivante demande une notification toutes les 10 minutes des événements de modification d’instance pour toutes les instances qui sont membres d’une classe dérivant de la classe [**\_ disque logique Win32**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) .</span><span class="sxs-lookup"><span data-stu-id="e2ef8-106">For example, the following statement requests notification every 10 minutes of instance modification events for all instances that are members of any class deriving from the [**Win32\_LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) class.</span></span>


```sql
SELECT * FROM __InstanceModificationEvent WITHIN 600
WHERE TargetInstance ISA "Win32_LogicalDisk"
```



<span data-ttu-id="e2ef8-107">La requête suivante retourne la définition de la classe du [**\_ processeur CIM**](/windows/desktop/CIMWin32Prov/cim-processor) et les définitions de toutes ses sous-classes.</span><span class="sxs-lookup"><span data-stu-id="e2ef8-107">The following query returns the definition for the [**CIM\_Processor**](/windows/desktop/CIMWin32Prov/cim-processor) class and definitions for all of its subclasses.</span></span>


```sql
SELECT * FROM meta_class WHERE __this ISA "CIM_Processor"
```



<span data-ttu-id="e2ef8-108">La classe **meta \_ Class** identifie cela comme une requête de schéma, la propriété **\_ \_ appelée identifie** la classe cible de la requête et l’opérateur ISA demande des définitions pour les sous-classes de la classe cible.</span><span class="sxs-lookup"><span data-stu-id="e2ef8-108">The class **meta\_class** identifies this as a schema query, the property called **\_\_this** identifies the target class of the query, and the ISA operator requests definitions for the subclasses of the target class.</span></span>

 

 
