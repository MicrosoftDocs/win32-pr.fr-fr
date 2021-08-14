---
description: Spécifie une clé pour sélectionner une ligne unique dans une collection scalaire ou une collection de tables.
ms.assetid: 3c4edae0-55be-4804-b5fe-07458b918365
ms.tgt_platform: multiple
title: INDEX (clause)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aca4478164839412238f59d9771aa9c96417c4055390cb4599edbb40b0e6b4a8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118318741"
---
# <a name="index-clause"></a>INDEX (clause)

La clause INDEX spécifie une clé pour sélectionner une ligne unique dans une collection scalaire ou une collection de tables. Le fournisseur SNMP est mappé à un type de classe CIM différent selon le type de table utilisé par l’appareil SNMP. Étant donné qu’une clé peut être de plusieurs types d’objets, le fournisseur utilise des règles de mappage différentes selon le type d’objet dans la clé. Pour plus d’informations, consultez types de données de la [clause d’index](#index-clause-data-types).

> [!Note]  
> Pour plus d’informations sur l’installation du fournisseur, consultez [configuration de l’environnement SNMP WMI](setting-up-the-wmi-snmp-environment.md).

 

Une collection scalaire correspond à une classe singleton CIM : autrement dit, une classe qui ne peut avoir qu’une seule instance. Étant donné qu’il n’est pas nécessaire d’identifier de façon unique une instance à partir d’une autre, une classe singleton ne désigne pas une ou plusieurs propriétés comme clé. Classes générées à partir de collections scalaires :

-   Ne contiennent pas de qualificateurs de propriété de **clé** .
-   Contiennent le **Singleton** de qualificateur de classe CIM standard, qui est de type **bool**.

Une collection de tables est mappée à une classe CIM qui peut avoir plusieurs instances. Par conséquent, la définition de la classe CIM doit contenir au moins une propriété qui définit la clé de l’objet. autrement dit, une propriété qui identifie de façon unique une instance de la classe. La clause INDEX d’une macro de [type objet](object-type-macro.md) d’une collection de tables spécifie l’ensemble de propriétés de clé de la collection. Les règles de mappage suivantes s’appliquent :

-   La **clé** de qualificateur CIM, de type **bool**, définit une propriété de clé.
-   L’ordre des informations d’INDEX dans la collection de tables définit l’ordre des clés dans la définition de la classe CIM.

    L' **\_ ordre des clés** de qualificateur CIM définit le classement des clés. Ce qualificateur est une valeur entière de 32 bits non signée qui, dans le cadre de la syntaxe de qualificateur MOF, doit être convertie en valeur entière 32 bits signée à l’aide de l’opération à complément à virgule.

Actuellement, le mappage de la clause d’INDEX SNMPv2C ne gère pas l’utilisation du qualificateur **implicite** . Une définition de classe CIM n’est pas générée dans ce cas.

## <a name="index-clause-data-types"></a>Types de données de la clause INDEX

En raison de la flexibilité de la clause INDEX dans la macro de [type objet](object-type-macro.md) , la spécification des propriétés de clé n’est pas simple. Au lieu de cela, vous devez prendre en compte les possibilités pour lesquelles la clause INDEX peut contenir un ou plusieurs des types de données suivants :

-   Valeur **indexobject** accessible en interne

    La valeur **indexobject** est une valeur nommée qui fait référence à une définition d’objet MIB figurant dans la ligne conceptuelle de la même table qui contient la clause index. La définition d’objet MIB référencée dans la clause d’INDEX est mappée à une propriété de clé de la définition de la classe CIM.

-   Valeur **indexobject** accessible en externe

    Dans ce cas, **indexobject** est une valeur nommée qui fait référence à une définition d’objet MIB figurant dans la ligne conceptuelle d’une autre table.

-   Valeur **indexType** accessible

    La valeur **indexType** est un type nommé qui fait référence à l’un des types de données suivants : **entier**, **chaîne d’octet**, identificateur d' **objet**, **networkAddress** ou **IPAddress**. Si la clause INDEX contient une référence MIB-type, les règles de mappage suivantes s’appliquent :

    -   L’objet MIB référencé est mappé à une propriété de clé de la définition de classe CIM. Sa syntaxe de type est basée sur la valeur **indexType** spécifiée, qui est mappée aux qualificateurs de propriété CIM à l’aide des procédures de mappage de [clauses de syntaxe](syntax-clause.md) standard.
    -   Le processus de mappage génère un nom de propriété unique en concaténant le descripteur d’objet de table MIB, un trait de soulignement ( \_ ) et l’ordre de classement de la valeur **indexType** de la clause d’index. Par exemple, le nom de la propriété pour le troisième composant **indexType** de la table MIB **enterpriseIfTable** est **enterpriseIfTable \_ 3**.
    -   La propriété CIM est annotée avec le qualificateur de **\_ clé virtuelle** . Ce qualificateur spécifie que le fournisseur SNMP doit calculer la valeur de la propriété en fonction du sur-ensemble d’informations d’instance associées à toutes les définitions d’objets MIB accessibles dans la définition de classe.
    -   La définition de la classe CIM doit contenir au moins une propriété qui n’a pas de qualificateur de **\_ clé virtuelle** . Si vous ne spécifiez pas cette propriété, la définition de la classe n’est pas valide.

-   Sous-type de longueur fixe

    Lorsque la clause INDEX d’une collection de tables SNMP contient un type pris en charge par SNMP qui est sous-typé comme une chaîne d’OCTET de longueur fixe, la **\_ longueur fixe** du QUALIFICATEUR de propriété CIM doit être utilisée pour spécifier cette valeur.

 

 



