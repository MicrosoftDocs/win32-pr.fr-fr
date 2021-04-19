---
description: Une collection SNMP mappe à une classe CIM et les éléments d’une collection sont mappés aux propriétés d’une classe CIM. Toutes les définitions de classe CIM générées doivent être dérivées de la classe SnmpObjectType.
ms.assetid: e6f82fd6-e3d8-48c5-8c7b-a30a2d502f41
ms.tgt_platform: multiple
title: Regroupements SNMP
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: a85473a394ce715ff9759e974a47824e5621509f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106543483"
---
# <a name="snmp-collections"></a>Regroupements SNMP

Une collection SNMP mappe à une classe CIM et les éléments d’une collection sont mappés aux propriétés d’une classe CIM. Toutes les définitions de classe CIM générées doivent être dérivées de la classe **SnmpObjectType** .

> [!Note]  
> Pour plus d’informations sur l’installation du fournisseur, consultez [configuration de l’environnement SNMP WMI](setting-up-the-wmi-snmp-environment.md).

 

Les définitions de classe suivantes parent toutes les définitions de classe générées :

``` syntax
[abstract]
class SnmpMacro
{
};

[abstract]
class SnmpObjectType:SnmpMacro
{
};
```

## <a name="remarks"></a>Notes

Les règles suivantes s’appliquent lors du mappage de regroupements SNMP à des classes CIM. Sauf indication contraire, ces règles s’appliquent à la fois aux collections scalaires et aux collections de tables :

-   Le processus de mappage génère des noms de classe CIM en concaténant « SNMP \_ », le nom d’identité du module MIB, « \_ » et le descripteur d’objet de la collection.

    Par exemple : le **système** se convertit en **\_ \_ \_ système SNMP RFC1213 MIB**, tandis que **ifTable** se traduit en **SNMP \_ RFC1213 \_ MIB \_ ifTable**.

-   Dans tous les cas, les traits d’Union (-) dans les identificateurs MIB SNMP sont mappés aux traits de soulignement ( \_ ) dans les noms de classe CIM.
-   Des conflits de noms peuvent se produire en raison du non-respect de la casse du nom CIM. Si un conflit de noms se produit, le fournisseur choisit l’une des définitions de groupe conflictuelles et ignore les définitions restantes.
-   Le nom d’identité du module MIB qui contient la collection est mappé au **\_ nom du module** qualificateur de la classe CIM.
-   L’identificateur d’objet de la collection fabriquée est mappé à l' **\_ ObjectID du groupe** de qualificateurs de classe CIM.
-   La liste d’importations du module MIB (obtenue à partir de la définition de macro **module-Identity** ) est mappée aux **\_ importations du module** qualificateur de la classe CIM. Ce qualificateur contient une liste de noms de module séparés par des virgules.

 

 



