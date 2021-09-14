---
description: Contient une clause de syntaxe qui définit les données et le type de l’objet MIB.
ms.assetid: 24c483c8-db50-492f-9c2e-72620395331a
ms.tgt_platform: multiple
title: Clause de syntaxe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 02d0bf25156ddda4bf71a7f40a8de1fede2a82d5
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126923311"
---
# <a name="syntax-clause"></a>Clause de syntaxe

La macro [de type objet](object-type-macro.md) contient une clause de syntaxe qui définit les données et le type de l’objet MIB. Alors que le fournisseur SNMP observe des règles générales pour le mappage des clauses SYNTAXIQUEs, le fournisseur suit également des règles spécifiques à plusieurs types de données.

> [!Note]  
> Pour plus d’informations sur l’installation du fournisseur, consultez [configuration de l’environnement SNMP WMI](setting-up-the-wmi-snmp-environment.md).

 

Les règles de mappage suivantes s’appliquent à tous les types de données décrits dans le tableau ci-dessous :

-   La représentation textuelle de la clause syntaxique correspond à la **\_ Convention textuelle** de QUALIFICATEUR de propriété CIM.
-   La définition de type nommé dans la clause syntaxique correspond à la syntaxe de l' **objet \_** QUALIFICATEUR de propriété CIM. Ce mappage diffère selon le type de données. Pour plus d’informations, consultez les descriptions de mappage.
-   Le type SNMP utilisé lors de l’encodage des frames de protocole SNMPv1 et SNMPv2C est mappé à l' **encodage** de qualificateur de propriété CIM.
-   Le qualificateur de propriété CIM **CimType** contient la représentation textuelle qui met en forme la valeur de protocole CIM sous-jacente.

Le tableau suivant répertorie les types de données qui ont des règles spécifiques qui régissent le comportement du mappage du fournisseur.



| Type de données SNMP                                     | Description                                                                                                                                                                                                                                      |
|----------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Type primitif](#primitive-type)                  | L’un des types de données de base définis dans la structure des documents SMI (Management Information) RFC 1213 et RFC 1903.                                                                                                                            |
| [Convention textuelle](textual-convention-macro.md) | Définition de type générée par le biais de l’utilisation explicite de la macro de **Convention textuelle** SNMPv2C ou générée par le biais de l’utilisation d’un type nommé. Une convention textuelle attribue un nom et, dans certains cas, une plage de valeurs à un type de données existant. |
| [Type nommé](#named-type)                          | Référence nommée à un type primitif, une convention textuelle ou un type restreint.                                                                                                                                                                    |
| [Type restreint](#constrained-type)              | Type primitif, type nommé ou Convention textuelle qui a été limitée par un mécanisme de sous-typage défini dans les documents SMI RFC 1213 et RFC 1903.                                                                                      |



 

## <a name="primitive-type"></a>Type primitif

Le type primitif est l’un des types de données de base définis dans la structure des documents SMI (Management Information) RFC 1213 et RFC 1903. Les types primitifs SNMP sont mappés à des types définis par CIM. Le tableau suivant répertorie le mappage qui se produit lorsque la clause de syntaxe fait explicitement référence à un type primitif pour SNMPv1. La **\_ Convention textuelle**, **l’encodage** et les qualificateurs de la **\_ syntaxe d’objet** sont toujours identiques au type MIB et la valeur par défaut est toujours **null**.



| Type MIB         | Type de variante CIM | valeur CimType |
|------------------|------------------|---------------|
| INTEGER          | VT \_           | **sint32**    |
| OCTETSTRING      | VT \_ BSTR         | **string**    |
| OBJECTIDENTIFIER | VT \_ BSTR         | **string**    |
| NULL             | VT \_ null         | Non pris en charge |
| IpAddress        | VT \_ BSTR         | **string**    |
| Compteur          | VT \_           | **uint32**    |
| Jauge            | VT \_           | **uint32**    |
| Graduations        | VT \_           | **uint32**    |
| Opaque           | VT \_ BSTR         | **string**    |
| NetworkAddress   | VT \_ BSTR         | **string**    |



 

Le fournisseur ignore la macro de TYPE objet lorsque la clause de syntaxe fait référence à la **valeur null**, soit explicitement, soit par le biais d’une assignation de type nommée. Le tableau suivant répertorie le mappage qui se produit lorsque la clause de syntaxe fait explicitement référence à un type primitif pour SNMPv2. La **\_ Convention textuelle**, **l’encodage** et les qualificateurs de la **\_ syntaxe d’objet** sont toujours identiques au type MIB et la valeur par défaut est toujours **null**.



| Type MIB          | Type de variante CIM | valeur CimType |
|-------------------|------------------|---------------|
| INTEGER           | VT \_           | **sint32**    |
| CHAÎNE D’OCTETS      | VT \_ BSTR         | **string**    |
| IDENTIFICATEUR D’OBJET | VT \_ BSTR         | **string**    |
| IpAddress         | VT \_ BSTR         | **string**    |
| Counter32         | VT \_           | **uint32**    |
| Gauge32           | VT \_           | **uint32**    |
| Unsigned32        | VT \_           | **uint32**    |
| Integer32         | VT \_           | **sint32**    |
| Counter64         | VT \_ BSTR         | **uint64**    |
| Graduations         | VT \_           | **uint32**    |
| Opaque            | VT \_ BSTR         | **string**    |



 

## <a name="named-type"></a>Type nommé

Les types nommés SNMP sont mappés à des types définis par CIM. Quand la clause de syntaxe fait référence à un [type primitif](#primitive-type), une [Convention textuelle](textual-convention-macro.md)ou un [type restreint](#constrained-type) via une dérivation d’assignation de type, utilisez ces types pour déterminer quelles procédures de mappage s’appliquent.

-   Si, par dérivation des règles d’assignation de type, vous rencontrez une définition de type avec restriction :

    -   Et si, par une dérivation plus poussée, vous rencontrez l’une des conventions textuelles listées dans la [macro de Convention textuelle](textual-convention-macro.md), appliquez les règles de mappage pour les types restreints et les conventions textuelles.
    -   Sinon, si vous rencontrez l’un des types primitifs listés dans l’un des tableaux de types primitifs, appliquez les règles de mappage pour les types primitifs et les types confrontés.

-   Si vous rencontrez l’une des conventions textuelles listées dans la [ \_ macro de Convention textuelle](textual-convention-macro.md), appliquez les règles de mappage pour les conventions textuelles.
-   Si vous rencontrez l’un des types primitifs listés dans une table de types primitifs, appliquez les règles de mappage pour les types primitifs.

> [!Note]  
> Les classes qui contiennent des types de propriété qui ne sont pas conformes au mappage décrit ci-dessus ne sont pas valides. Dans ce cas, le fournisseur retourne une erreur si et quand le fournisseur demande la récupération d’une définition de classe lors de l’exécution d’une fonction de récupération d’instance.

 

## <a name="constrained-type"></a>Type restreint

Un type restreint est un type primitif, un type nommé ou une convention textuelle qui a été limitée par un mécanisme de sous-typage défini dans les documents SMI RFC 1213 et RFC 1903. Quand un sous-typage se produit, des qualificateurs CIM supplémentaires sont requis pour spécifier les valeurs de sous-type. La définition de type nommé dans la clause de syntaxe mappe textuellement à la syntaxe d' **objet \_** QUALIFICATEUR de propriété CIM jusqu’à, mais n’inclut pas les contraintes du sous-type.

Les sous-types peuvent respecter l’un des formats suivants :

-   ENTIER énuméré

    L' **énumération** du qualificateur de propriété CIM spécifie les valeurs énumérées. Ce qualificateur est représenté sous la forme d’une chaîne contenant une liste séparée par des virgules de valeurs entières 32 bits signées. Le tableau suivant répertorie les types de mappages. La valeur par défaut est toujours **null**.



| Type MIB avec restriction | Type de variante CIM | Qualificateurs CIM                                                                                                        |
|----------------------|------------------|-----------------------------------------------------------------------------------------------------------------------|
| ENTIER énuméré   | VT \_ BSTR         | **\_ Convention textuelle**: enumeratedinteger<br/> **encodage**: entier<br/> **CimType**: chaîne<br/> |



 

-   BITS

    Les **bits** de qualificateur de propriété CIM spécifient les valeurs énumérées. Ce qualificateur est représenté sous la forme d’une chaîne contenant une liste séparée par des virgules de valeurs entières 32 bits signées. Le tableau suivant répertorie les types de mappages. La valeur par défaut est toujours **null**.



| Type MIB avec restriction | Type de variante CIM      | Qualificateurs CIM                                                                                               |
|----------------------|-----------------------|--------------------------------------------------------------------------------------------------------------|
| BITS                 | matrice VT de \_ matrice VT \| \_ | **\_ Convention textuelle**: bits<br/> **encodage**: OCTETSTRING<br/> **CimType**: chaîne<br/> |



 

-   Longueur variable

    Quand la clause de syntaxe fait référence à un type primitif, à un type nommé ou à une convention textuelle qui est sous-typée sous la forme d’une chaîne d’OCTET de longueur variable ou opaque, la **\_ longueur variable** de QUALIFICATEUR de propriété CIM spécifie les valeurs minimales, maximales et de longueur fixe associées à la définition de type. Ce qualificateur est implémenté sous forme de chaîne au format suivant, où les valeurs de longueur variable sont représentées par des entiers non signés 32 bits.

    ``` syntax
    (((0.9) .. (0.9)) | (0.9))(, (((0.9) .. (0.9)) | (0.9)))*
    ```

-   Longueur fixe

    Quand la clause de syntaxe fait référence à un type primitif, à un type nommé ou à une convention textuelle qui est sous-typée sous la forme d’une chaîne d’OCTET de longueur fixe ou opaque, la **\_ longueur fixe** du QUALIFICATEUR de propriété CIM spécifie la valeur de longueur fixe. Ce qualificateur est représenté sous la forme d’une valeur entière non signée 32 bits.

-   Plage

    Quand la clause de syntaxe fait référence à un type primitif, à un type nommé ou à une convention textuelle qui est sous-typée comme un entier ou une jauge de valeur fixe ou de plage, la **\_ valeur de variable** de QUALIFICATEUR de propriété CIM spécifie les valeurs comprises dans la plage et fixes associées à la définition de type. Ce qualificateur est implémenté sous forme de chaîne au format suivant, où les valeurs de longueur fixe et de plage sont représentées sous la forme d’entiers non signés 32 bits.

    ``` syntax
    (((0.9)..(0.9))|(0.9))(,(((0.9)..(0.9))|(0.9)))*
    ```

## <a name="example-code"></a>Exemple de code

L’exemple suivant décrit un sous-type d’entier énuméré.

``` syntax
Status := INTEGER {
up(1),
down(2),
testing(3)
}
```

Cet exemple est mappé à :

``` syntax
enumeration("up(1),down(2),testing(3)")
```

L’exemple de code suivant décrit un sous-type BITS.

``` syntax
Status := BITS {
up(1),
down(2), 
testing(3)
}
```

L’exemple de code suivant est mappé à :

``` syntax
bits("up(1),down(2),testing(3)")
```

L’exemple de code suivant décrit un sous-type de longueur variable.

``` syntax
MySnmpOSIAddress ::=  TEXTUAL-CONVENTION

    DISPLAY-HINT    "*1x:/1x:"
    STATUS        current
    DESCRIPTION
            "Represents an OSI transport-address:

            octets    contents         encoding
              1        length of NSAP   'n' as an unsigned-integer
                                        (either 0 or from 3 to 20)
              2..(n+1)  NSAP          concrete binary representation
              (n+2)..m  TSEL             string of (up to 64) octets
            "
    SYNTAX         OCTET STRING (SIZE (1|4..85))
```

Cet exemple est mappé à :

``` syntax
display_hint("*1x:/1x:"),
encoding("OCTETSTRING"),
textual_convention("OCTETSTRING"),
variable_length ("1,4..85")
```

L’exemple suivant décrit un sous-type de longueur fixe.

``` syntax
IPXADDRESS := OCTET STRING (SIZE (6))
```

Cet exemple est mappé à :

``` syntax
fixed_length(6)
```

L’exemple suivant décrit un sous-type de plage.

``` syntax
Status := INTEGER (10..20|8)
```

Cet exemple est mappé à :

``` syntax
variable_value("10..20,8")
```

 

 




