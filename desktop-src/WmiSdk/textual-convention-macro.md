---
description: Les conventions textuelles SNMP sont mappées à des types définis par CIM.
ms.assetid: 73bb6c22-0a68-4a4b-8de2-8326ec67a059
ms.tgt_platform: multiple
title: Macro de CONVENTION textuelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 329508ce3d124c0b3954675b3142aeb33c402923
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106524121"
---
# <a name="textual-convention-macro"></a>Macro de CONVENTION textuelle

Les conventions textuelles SNMP sont mappées à des types définis par CIM.

> [!Note]  
> Pour plus d’informations sur l’installation du fournisseur, consultez [configuration de l’environnement SNMP WMI](setting-up-the-wmi-snmp-environment.md).

 

Les règles de mappage suivantes s’appliquent aux conventions de texte SNMP :

-   La définition de type nommé dans la clause de syntaxe mappe textuellement à la **\_ syntaxe d’objet** QUALIFICATEUR de propriété CIM.
-   Utilisez le tableau suivant pour mapper des conventions textuelles lorsque la clause de syntaxe fait explicitement référence à une convention textuelle d’une macro de CONVENTION textuelle SNMPv2C ou fait référence à une convention textuelle implicite. La valeur par défaut est toujours **null**.



| Convention textuelle | Type de variante CIM | Qualificateur CIM                                                                                                                                                        |
|--------------------|------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| DateAndTime        | **VT \_ BSTR**     | **\_ Convention textuelle**: DateAndTime<br/> **encodage**: OCTETSTRING<br/> **\_ syntaxe** de l’objet : DateAndTime<br/> **CimType**: chaîne<br/>       |
| DisplayString      | **VT \_ BSTR**     | **\_ Convention textuelle**: DisplayString<br/> **encodage**: OCTETSTRING<br/> **\_ syntaxe** de l’objet : DisplayString<br/> **CimType**: chaîne<br/>   |
| MacAddress         | **VT \_ BSTR**     | **\_ Convention textuelle**: MacAddress<br/> **encodage**: OCTETSTRING<br/> **\_ syntaxe** de l’objet : MacAddress<br/> **CimType**: chaîne<br/>         |
| PhysAddress        | **VT \_ BSTR**     | **\_ Convention textuelle**: PhysAddress<br/> **encodage**: OCTETSTRING<br/> **\_ syntaxe** de l’objet : PhysAddress<br/> **CimType**: chaîne<br/>       |
| SnmpUDPAddress     | **VT \_ BSTR**     | **\_ Convention textuelle**: SnmpUDPAddress<br/> **encodage**: OCTETSTRING<br/> **\_ syntaxe** de l’objet : SnmpUDPAddress<br/> **CimType**: chaîne<br/> |
| SnmpOSIAddress     | **VT \_ BSTR**     | **\_ Convention textuelle**: SnmpOSIAddress<br/> **encodage**: OCTETSTRING<br/> **\_ syntaxe** de l’objet : SnmpOSIAddress<br/> **CimType**: chaîne<br/> |
| SnmpIPXAddress     | **VT \_ BSTR**     | **\_ Convention textuelle**: SnmpIPXAddress<br/> **encodage**: OCTETSTRING<br/> **\_ syntaxe** de l’objet : SnmpIPXAddress<br/> **CimType**: chaîne<br/> |



 

-   Le type Variant défini par CIM et la **\_ Convention textuelle** de QUALIFICATEUR de propriété CIM, l' **encodage**, la **\_ syntaxe d’objet** et la carte **CimType** à l’aide du type primitif sous-jacent.
-   La clause d’indicateur d’affichage de la macro de CONVENTION textuelle SNMPv2C mappe textuellement à l’indicateur d' **affichage \_** du QUALIFICATEUR de propriété CIM. Ce qualificateur n’est pas généré s’il n’y a aucune macro de CONVENTION textuelle, ou la macro ne contient pas de clause d’indication d’affichage.

## <a name="example-code"></a>Exemple de code

L’exemple suivant décrit une convention textuelle SNMPv1.

``` syntax
myNamedType ::= DISPLAYSTRING (SIZE (0..127))

myNamedProperty OBJECT-TYPE
SYNTAX  myNamedType
ACCESS read-only
STATUS MANDATORY
DESCRIPTION ""
```

Cet exemple génère les qualificateurs CIM suivants.

``` syntax
object_syntax("myNamedType"),
textual_convention("DISPLAYSTRING"),
encoding("OCTETSTRING"),
variable_length("0..127")
```

L’exemple suivant décrit une convention textuelle SNMPv2.

``` syntax
myDisplaystring ::= TEXTUAL-CONVENTION
DISPLAY-HINT "255a"
STATUS current
DESCRIPTION "" 
SYNTAX OCTET STRING (SIZE (0..127))

myNamedProperty OBJECT-TYPE
SYNTAX  myDisplaystring
MAX-ACCESS read-only
STATUS current
DESCRIPTION ""
```

Cet exemple génère les qualificateurs CIM suivants.

``` syntax
object_syntax("myDisplaystring"),
textual_convention("OCTETSTRING"),
encoding("OCTETSTRING"),
display_hint("255a"),
variable_length("0..127")
```

 

 




