---
description: La clause OBJECTs de la macro de TYPE NOTIFICATION énumère le jeu d’objets associés à l’objet notification.
ms.assetid: 0cb4776f-aae2-452d-9472-caf6d28fb870
ms.tgt_platform: multiple
title: Clause OBJECTs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9a9289be0a3fa228e74a720ec385a5b13354f849710a88287a9911f470e40758
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119131041"
---
# <a name="objects-clause"></a>Clause OBJECTs

La clause OBJECTs de la macro de [type notification](notification-type-macro.md) énumère le jeu d’objets associés à l’objet notification.

> [!Note]  
> Pour plus d’informations sur l’installation du fournisseur, consultez [configuration de l’environnement SNMP WMI](setting-up-the-wmi-snmp-environment.md).

 

Les règles suivantes s’appliquent lors du mappage à des classes CIM :

-   Chaque membre de la clause OBJECTs correspond à une propriété de la définition de la classe CIM. Le descripteur d’objet du membre mappe textuellement au nom de propriété CIM. Par exemple, **ifIndex** se traduit par **ifIndex**.
-   Chaque propriété CIM générée par le processus de mappage contient le qualificateur **VarBindIndex** .

    **VarBindIndex** est un qualificateur obligatoire **UInt32** qui décrit la position de l’objet tel qu’il apparaît dans la clause Objects de la macro [Trap-type](trap-type-macro.md) ou [notification-type](notification-type-macro.md) . L’entier spécifie également la position de la propriété telle qu’elle apparaît dans la liste des liaisons de variables de l’unité de données d’interruption SNMPv1 ou SNMPv2C (unité de données de protocole), respectivement. (Étant donné que les deux premières liaisons de variables sont toujours TimeStamp et identification, toutes les variables supplémentaires sont numérotées après la valeur 2.)

    Quand la classe d’événements CIM est générée à partir d’une macro de [type d’interruption](trap-type-macro.md) SNMPv1, le qualificateur **VarBindIndex** a une valeur initiale de 1 pour la première variable dans la liste des liaisons de variables.

    Quand la classe d’événements CIM est générée à partir d’une macro de [type notification](notification-type-macro.md) SNMPv2C, le qualificateur **VarBindIndex** a une valeur initiale de 3 pour la première variable de la liste liaisons de variables.

Lors du mappage d’une classe CIM encapsulée, chaque membre de la clause OBJECTs est mappé à une propriété CIM qui reflète le nom, le type et la valeur de l’objet MIB correspondant. Les procédures de mappage utilisées sont spécifiées dans les rubriques suivantes :

-   [Clause de syntaxe](syntax-clause.md)
-   [Macro de CONVENTION textuelle](textual-convention-macro.md)
-   [Clauses Access et MAX-ACCESS](access-and-max-access-clauses.md)

Lors de l’utilisation d’une classe CIM référent, chaque membre de la clause OBJECTs est mappé comme suit :

-   Chaque membre de la clause OBJECTs est mappé à une seule propriété de la classe CIM. La propriété est fortement typée comme un objet incorporé.
-   La classe de l’objet incorporé est générée à l’aide de la procédure de mappage d’objet standard. Pour plus d’informations, consultez [macro de type objet](object-type-macro.md). Par exemple, **ifTable** est mappé à une classe incorporée nommée **SNMP \_ RFC1213 \_ MIB \_ ifTable**.
-   Les valeurs associées aux liaisons de variable d’un PDU d’interruption sont instanciées en tant qu’objets incorporés d’un objet de la classe référent. Chaque objet incorporé contient des valeurs pour chacune des propriétés de clé de l’objet et la valeur de la propriété dans la liaison de variable qui est mappée.

 

 



