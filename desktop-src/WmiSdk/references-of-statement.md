---
description: Les références de l’instruction récupèrent toutes les instances d’association qui font référence à une instance source particulière.
ms.assetid: 674be546-e7fd-4150-9d7c-2888d24bf1b3
ms.tgt_platform: multiple
title: RÉFÉRENCES de l’instruction
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f1c7cc624a1e91220fc6bfc89ef0a75878a9cfb1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106527812"
---
# <a name="references-of-statement"></a>RÉFÉRENCES de l’instruction

Les références de l’instruction récupèrent toutes les instances d’association qui font référence à une instance source particulière. Les références de l’instruction sont similaires aux ASSOCIATORS OF Statement dans sa syntaxe. Toutefois, au lieu de récupérer des instances de point de terminaison, il récupère les instances d’association intermédiaires.

Les références de la clause WHERE peuvent inclure un ou plusieurs des mots clés prédéfinis suivants et leurs valeurs :


```sql
REFERENCES OF {SourceObject} WHERE 
    ClassDefsOnly
    RequiredQualifier = QualifierName
    ResultClass = ClassName
    Role = PropertyName
```



Pour spécifier un objet source, utilisez un chemin d’accès d’objet valide pour ObjetSource. Comme avec l’instruction SELECT, la clause WHERE est facultative et est utilisée pour définir davantage la requête. Autrement dit, l’instruction suivante est parfaitement valide :


```sql
REFERENCES OF {Adapter="AHA-294X"}
```



Le mot clé **ClassDefsOnly** indique que l’instruction retourne un jeu de résultats d’objets de définition de classe plutôt que des instances réelles des classes d’association. Ces objets contiennent des définitions de classes auxquelles appartiennent les instances qui font référence à l’objet source. Par exemple, l’instruction suivante retourne les définitions des classes **AdapterDriver** et **AdapterProtocol** :


```sql
REFERENCES OF {Adapter="AHA-294X"} WHERE ClassDefsOnly
```



Le mot clé **RequiredQualifier** indique que les objets Association retournés doivent inclure le qualificateur spécifié. Le mot clé **RequiredQualifier** peut être utilisé pour inclure des instances particulières d’associations dans le jeu de résultats. Par exemple, l’instruction suivante retourne les instances d’association qui incluent un qualificateur appelé **AdapterTag**:


```sql
REFERENCES OF {Adapter="AHA-294X"}  WHERE RequiredQualifier = AdapterTag
```



Le mot clé **ResultClass** indique que les objets Association retournés doivent appartenir ou être dérivés de la classe spécifiée. Par exemple, l’instruction suivante retourne les associations de la classe **AdapterDriver** ou des sous-classes de **AdapterDriver**:


```sql
REFERENCES OF {Adapter="AHA-294X"} WHERE ResultClass = AdapterDriver
```



Les mots clés **ClassDefsOnly** et **ResultClass** s’excluent mutuellement. Leur utilisation conjointe entraîne une erreur de requête non valide.

Le mot clé **role** indique que les associations retournées sont uniquement celles dans lesquelles l’objet source joue un rôle particulier. Le rôle est défini par la propriété spécifiée, une propriété de référence de type [ref](references.md). Le mot clé **role** est utile dans les associations où un objet donné peut jouer un rôle dans certains cas et un autre rôle dans d’autres, par exemple dans les associations hiérarchiques. Le mot clé **role** peut être utilisé pour récupérer toutes les associations dans lesquelles l’objet source joue le rôle de parent, par exemple. L’instruction suivante illustre la syntaxe pour la récupération des associations qui ont une propriété **parent** référençant l’objet source en tant que parent :


```sql
REFERENCES OF {Adapter="AHA-294X"} WHERE Role = parent
```



> [!Note]  
> Les requêtes complexes ne peuvent pas utiliser « and » ou « or » pour séparer les mots clés pour les ASSOCIateurs de et les références d’instructions. En outre, le signe égal est le seul opérateur valide qui peut être utilisé avec les mots clés dans ces requêtes. Par exemple, la requête suivante est valide :

 


```sql
"REFERENCES OF {Win32_NetworkAdapter.DeviceID="0"} " +
    "WHERE resultclass = Win32_NetworkAdapterSetting " +
    "requiredQualifier = Dynamic"
```



> [!Note]  
> Les exemples suivants ne sont pas valides. Le premier exemple n’utilise pas le signe égal et le deuxième exemple tente d’utiliser par erreur le mot clé **et** :

 


```sql
"REFERENCES OF {Win32_NetworkAdapter.DeviceID="0"} " +
    "WHERE resultclass = Win32_NetworkAdapterSetting " +
    "requiredQualifier <> Dynamic"

"REFERENCES OF {Win32_NetworkAdapter.DeviceID="0"} " +
"WHERE resultclass = Win32_NetworkAdapterSetting " +
"AND requiredQualifier = Dynamic"
```



 

 



