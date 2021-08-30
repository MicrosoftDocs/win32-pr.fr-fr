---
description: 'Les requêtes d’association de schéma utilisent les mêmes instructions que celles utilisées dans les requêtes d’association de données : les ASSOCIateurs et les références de.'
ms.assetid: b5fc2d86-702a-42cd-82e6-f15c905ba6aa
ms.tgt_platform: multiple
title: Associations de schéma
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 461dc7c64267376baf1515ed7784da59bc789f6f1cc1171587823adb27799830
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119995689"
---
# <a name="schema-associations"></a>Associations de schéma

Les requêtes d’association de schéma utilisent les mêmes instructions que celles utilisées dans les requêtes d’association de données : les ASSOCIateurs et les références de. Toutefois, avec les requêtes d’association de données, les instances de classe sont retournées et, avec les requêtes d’association de schéma, les noms des classes qui peuvent participer aux relations d’association sont retournés. Par exemple, utilisez une requête de schéma pour rechercher toutes les classes d’association définies dans le schéma qui font référence à une classe source.

La syntaxe des ASSOCIateurs et des références d’instructions est la même pour les requêtes d’association de schéma que pour les requêtes d’association de données avec les exceptions suivantes :

-   L’objet source est une classe plutôt qu’une instance.
-   Il existe un mot clé supplémentaire, **SchemaOnly**, qui identifie la requête comme s’appliquant à un schéma plutôt qu’aux données.
-   Le mot clé **ClassDefsOnly** n’est pas valide.

L’exemple suivant illustre la syntaxe complète des ASSOCIateurs d’instruction pour une requête de schéma. Pour plus d’informations sur la syntaxe, consultez [ASSOCIATORS OF Statement](associators-of-statement.md).


```sql
ASSOCIATORS OF {SourceClass} WHERE 
    AssocClass = AssocClassName
    RequiredAssocQualifier = QualifierName
    RequiredQualifier = QualifierName
    ResultClass = ClassName
    ResultRole = PropertyName
    Role = PropertyName
    SchemaOnly
```



L’exemple suivant montre une requête qui retourne les classes de **protocole** et de **pilote** , les deux classes qui font référence à la classe source.


```sql
ASSOCIATORS OF {Adapter} WHERE SchemaOnly
```



La requête suivante retourne uniquement la classe **Driver** en raison de la restriction placée par le mot clé **AssocClass** .


```sql
ASSOCIATORS OF {Adapter} WHERE AssocClass = AdapterDriver SchemaOnly
```



La syntaxe complète des références de l’instruction pour une requête de schéma est la suivante. Pour plus d’informations sur la syntaxe, consultez [références de l’instruction](references-of-statement.md).


```sql
REFERENCES OF {SourceClass} WHERE
    ResultClass = ClassName
    Role = PropertyName
    RequiredQualifier = QualifierName
    SchemaOnly
```



> [!Note]  
> Les requêtes d’association de schéma peuvent retourner des objets en double.

 

Par exemple, la requête suivante retourne la classe [**CIM CIM \_**](/windows/desktop/CIMWin32Prov/cim-computersystem) plusieurs fois lors de l’énumération des classes dans l’espace de noms **\\ cimv2 racine** .


```sql
ASSOCIATORS OF {Win32_ComputerSystem} WHERE SchemaOnly
```



 

 
