---
description: La macro de TYPE objet contient des clauses obligatoires et facultatives qui décrivent les caractéristiques de base d’un objet MIB. Le fournisseur SNMP convertit une MIB en parties correspondantes de la macro de TYPE objet.
ms.assetid: ad76a4fc-354e-4270-862c-062aa523bf7e
ms.tgt_platform: multiple
title: Macro de TYPE objet
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c605a414c402f2cf2d18be2d966db6408f23cdc9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104111962"
---
# <a name="object-type-macro"></a>Macro de TYPE objet

La macro de TYPE objet contient des clauses obligatoires et facultatives qui décrivent les caractéristiques de base d’un objet MIB. Le fournisseur SNMP convertit une MIB en parties correspondantes de la macro de TYPE objet.

> [!Note]  
> Pour plus d’informations sur l’installation du fournisseur, consultez [configuration de l’environnement SNMP WMI](setting-up-the-wmi-snmp-environment.md).

 

## <a name="components"></a>Composants

<dl> <dt>

<span id="MIB_object"></span><span id="mib_object"></span><span id="MIB_OBJECT"></span>Objet MIB
</dt> <dd>

Objet qui contient la plupart des données en question.

</dd> <dt>

<span id="Object_descriptor"></span><span id="object_descriptor"></span><span id="OBJECT_DESCRIPTOR"></span>Descripteur d’objet
</dt> <dd>

Nom unique ou descripteur d’objet identifiant chaque objet MIB. Chaque descripteur d’objet MIB correspond exactement à un nom de propriété CIM. Par exemple, **ifIndex** se traduit par **ifIndex**.

</dd> <dt>

<span id="SYNTAX_Clause"></span><span id="syntax_clause"></span><span id="SYNTAX_CLAUSE"></span>[Clause de syntaxe](syntax-clause.md)
</dt> <dd>

Définit les données et le type d’un objet MIB.

</dd> <dt>

<span id="INDEX_clause"></span><span id="index_clause"></span><span id="INDEX_CLAUSE"></span>[INDEX (clause)](index-clause.md)
</dt> <dd>

Définit une clé pour la sélection d’une ligne de table unique.

</dd> <dt>

<span id="AUGMENTS_clause"></span><span id="augments_clause"></span><span id="AUGMENTS_CLAUSE"></span>Clauses d’augmentation
</dt> <dd>

Indique que la collection de tables qu’elle spécifie peut être considérée comme une extension d’une autre collection de tables et peut remplacer la clause INDEX dans SNMPv2. Les collections référencées par la clause d’AUGMENTATIONs peuvent être combinées avec l’autre collection de tables pour former une seule collection. La collection résultante partage les propriétés de clé primaire spécifiées dans la dernière collection de tables de la chaîne.

Dans ce cas, les règles de mappage précédentes spécifiées pour la clause INDEX sont appliquées à la dernière collection de tables de la chaîne. La collection d’objets est ensuite mappée à une définition de classe CIM.

</dd> <dt>

<span id="OBJECT-IDENTIFIER_clause"></span><span id="object-identifier_clause"></span><span id="OBJECT-IDENTIFIER_CLAUSE"></span>Clause de l’identificateur d’objet
</dt> <dd>

Contient un identificateur d’objet unique pour un objet MIB. Cet identificateur d’objet est mappé à l' **\_ identificateur d’objet** du QUALIFICATEUR de propriété CIM.

</dd> <dt>

<span id="ACCESS_and_MAX-ACCESS_Clauses"></span><span id="access_and_max-access_clauses"></span><span id="ACCESS_AND_MAX-ACCESS_CLAUSES"></span>[Clauses Access et MAX-ACCESS](access-and-max-access-clauses.md)
</dt> <dd>

Définissez les droits d’accès à l’objet MIB.

</dd> <dt>

<span id="DESCRIPTION_clause"></span><span id="description_clause"></span><span id="DESCRIPTION_CLAUSE"></span>DESCRIPTION (clause)
</dt> <dd>

Fournit une description textuelle de l’objet, qui correspond à la **Description** du qualificateur de propriété CIM. Cette clause peut être vide.

Chaque objet **table** et **entrée** d’une définition de table SNMP contient également une clause Description, qui peut également être vide. Les clauses de TABLE et de DESCRIPTION d’entrée sont concaténées et le résultat est mappé à la **Description** du qualificateur de classe CIM.

</dd> <dt>

<span id="STATUS_clause"></span><span id="status_clause"></span><span id="STATUS_CLAUSE"></span>Clause STATUs
</dt> <dd>

Indique si l’objet doit être pris en charge. Lorsque la valeur de la clause STATUs est **obsolète**, le fournisseur ignore l’objet MIB du mappage. Dans le cas contraire, la clause STATUs correspond à l' **État** de qualificateur de propriété CIM.

Pour SNMPv1, la valeur par défaut de l' **État** est **obligatoire** ou **facultative**, mais le qualificateur peut contenir une autre valeur. Pour SNMPv2C, la valeur par défaut de l' **État** est **en cours** ou **déconseillée**, mais le qualificateur peut contenir une autre valeur.

</dd> <dt>

<span id="DEFVAL_clause"></span><span id="defval_clause"></span><span id="DEFVAL_CLAUSE"></span>DEFVAL, clause
</dt> <dd>

Affecte une valeur par défaut à une variable dans une ligne de table logique et mappe à la chaîne de qualificateur de propriété CIM **defval**.

</dd> <dt>

<span id="REFERENCE_clause"></span><span id="reference_clause"></span><span id="REFERENCE_CLAUSE"></span>RÉFÉRENCE (clause)
</dt> <dd>

Fait référence à un autre document qui contient plus d’informations sur l’objet. Cette clause est mappée à la **référence** de qualificateur de propriété CIM, qui est de type chaîne.

</dd> <dt>

<span id="UNITS_clause"></span><span id="units_clause"></span><span id="UNITS_CLAUSE"></span>UNITs, clause
</dt> <dd>

Fournit une définition précise de ce que l’objet représente. Cette clause mappe aux **unités** de qualificateur de propriété CIM, qui est de type chaîne.

</dd> </dl>

## <a name="remarks"></a>Notes

La macro de TYPE objet décrit les caractéristiques de base d’un objet MIB individuel. Un ensemble de macros de TYPE objet peut être considéré comme un groupe d’objets connexes. Dans SNMPv2C, utilisez la macro de groupe d’objets pour regrouper de manière formelle des ensembles d’objets connexes dans une collection. Toutefois, il n’existe aucun mécanisme formel pour créer des collections dans SNMPv1. Dans le cadre du fournisseur SNMP, la macro de groupe d’objets est ignorée, mais vous pouvez inventer des relations et fabriquer des collections.

 

 



