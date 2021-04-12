---
description: Décrit la syntaxe de base d’une instruction SELECT pour les requêtes d’événement.
ms.assetid: 8882fdcb-3768-41e3-82ab-3006d903f3a0
ms.tgt_platform: multiple
title: Instruction SELECT pour les requêtes d’événements
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ab840072269d04987bf42939f1f566ee6b99afab
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104210204"
---
# <a name="select-statement-for-event-queries"></a>Instruction SELECT pour les requêtes d’événements

Vous pouvez utiliser diverses instructions SELECT pour rechercher des informations sur les événements. Les instructions peuvent être des instructions de base ou elles peuvent être plus restrictives pour limiter le jeu de résultats retourné par la requête.

L’exemple suivant est une instruction SELECT de base qui est utilisée pour rechercher des informations sur les événements.


```sql
SELECT * FROM EventClass
```



Lorsqu’un consommateur envoie une requête, il s’agit d’une demande de notification de toutes les occurrences de l’événement représenté par **EventClass**. Cette requête comprend une demande de notification concernant toutes les propriétés du système d’événements et non-système. Lorsqu’un fournisseur d’événements soumet une requête, il enregistre la prise en charge de la génération de notifications lorsqu’un événement représenté par **EventClass** se produit.

Les consommateurs peuvent spécifier des propriétés individuelles au lieu de l’astérisque ( \* ) dans l’instruction SELECT.

L’exemple suivant montre comment interroger des propriétés spécifiques.


```sql
SELECT property_1, property_2, property_3 FROM MyEventClass
```



Toutefois, toutes les propriétés d’un objet incorporé sont retournées, même si la requête spécifie des propriétés d’objet incorporées.

L’exemple suivant montre deux requêtes qui retournent les mêmes données.


```sql
SELECT targetInstance FROM __InstanceCreationEvent within 2
    WHERE targetinstance isa "Win32_Process"
```




```sql
SELECT targetInstance.Name FROM __InstanceCreationEvent within 2
    WHERE targetinstance isa "Win32_Process"
```



Si une propriété système n’est pas pertinente pour une requête spécifique, elle contient la **valeur null**. Par exemple, la valeur de la propriété système **\_ \_ RelPath** est **null** pour toutes les requêtes d’événement.

Les propriétés système suivantes contiennent la **valeur null** pour les requêtes d’événements :

<dl> \_\_Joint  
\_\_D  
\_\_Constitue  
\_\_Serveurs  
</dl>

Pour plus d’informations, consultez [référence des propriétés système WMI](wmi-system-properties.md).

Toutes les requêtes d’événements peuvent inclure une [clause WHERE](where-clause.md)facultative, mais les clauses WHERE sont principalement utilisées par les consommateurs pour spécifier un filtrage supplémentaire. Il est fortement recommandé que les consommateurs spécifient toujours une clause WHERE. Le coût d’une requête complexe est minime par rapport au coût de la diffusion et du traitement des notifications inutiles.

L’exemple suivant montre une requête qui demande des notifications de tous les événements de modification d’instance qui affectent la classe hypothétique **EmailEvent**.


```sql
SELECT * FROM EmailEvent
```



Si les événements associés à **EmailEvent** se produisent fréquemment, le consommateur est submergé d’événements. Une meilleure requête demande des événements uniquement lorsque des conditions spécifiques utilisent des propriétés de la classe spécifiée, par exemple lorsque le niveau d’importance est élevé.

L’exemple suivant illustre la requête que vous pouvez utiliser si **EmailImportance** est une propriété de la classe **EmailEvent**.


```sql
SELECT * FROM EmailEvent WHERE EmailImportance > 3
```



Notez que WMI peut rejeter une requête pour plusieurs raisons. Par exemple, la requête peut être trop complexe ou gourmande en ressources pour l’évaluation. Dans ce cas, WMI retourne des codes d’erreur spécifiques, tels que la **\_ requête WBEM E \_ non valide \_**.

Les propriétés des objets incorporés peuvent être utilisées dans la clause WHERE.

L’exemple suivant montre comment interroger des objets où la propriété **TargetInstance** de la classe système [**\_ \_ InstanceModificationEvent**](--instancemodificationevent.md) est un objet [**\_ disque logique Win32**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) incorporé et **FreeSpace** est une propriété du **\_ disque logique Win32**.


```sql
SELECT * FROM __InstanceModificationEvent WITHIN 600
    WHERE TargetInstance ISA "Win32_LogicalDisk" 
    AND   TargetInstance.FreeSpace < 1000000
```



## <a name="examples"></a>Exemples

L’exemple d' [événement de création d’analyse pour un nom de processus spécifique](https://Gallery.TechNet.Microsoft.Com/52716121-f386-49de-86cd-46ca54d1714f) VBScript sur TechNet utilise l’instruction SELECT pour surveiller les événements de création d’instance WMI pour \_ le processus Win32, en filtrant un nom de processus spécifique.

 

 
