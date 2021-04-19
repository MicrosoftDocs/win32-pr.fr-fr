---
title: Identificateurs d’objets (AD DS)
description: Les identificateurs d’objets (OID) sont des valeurs numériques uniques émises par différentes autorités émettrices afin d’identifier de manière unique les éléments de données, les syntaxes et d’autres parties des applications distribuées.
ms.assetid: a8f5a1c7-eda3-4430-b959-daef13c00a1b
ms.tgt_platform: multiple
keywords:
- identificateurs d’objets AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2253a6173e06f5d7b0c136a520db3e1e5a5e798e
ms.sourcegitcommit: 8ea1a82717bd3dbb3457be0697329aa37fb13f08
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/11/2019
ms.locfileid: "106510661"
---
# <a name="object-identifiers-ad-ds"></a>Identificateurs d’objets (AD DS)

Les identificateurs d’objets (OID) sont des valeurs numériques uniques émises par différentes autorités émettrices afin d’identifier de manière unique les éléments de données, les syntaxes et d’autres parties des applications distribuées. Les OID sont disponibles dans les applications OSI, les répertoires X. 500, SNMP et d’autres applications où l’unicité est importante. Les OID sont basés sur une structure arborescente, dans laquelle une autorité de délivrance supérieure, telle que l’ISO, alloue une branche de l’arbre à une sous-autorité qui peut à son tour allouer des sous-branches.

Le protocole LDAP (RFC 2251) requiert un service d’annuaire pour identifier les classes d’objet, les attributs et les syntaxes avec les OID. Cela fait partie de l’héritage LDAP X. 500.

Dans Active Directory Domain Services, les OID incluent certains émis par le fichier ISO pour les classes et les attributs X. 500, et certains émis par Microsoft et d’autres autorités émettrices. La notation OID est une chaîne de nombres en pointillés, par exemple « 1.2.840.113556.1.5.9 », qui est décrite dans le tableau suivant.



| Valeur  | Signification          | Description                                              |
|--------|------------------|----------------------------------------------------------|
| 1      | ISO              | Identifie l’autorité racine.                           |
| 2      | ANSI             | Désignation de groupe affectée par ISO.                       |
| 840    | États-Unis              | Désignation de pays/région affectée par le groupe.        |
| 113556 | Microsoft        | Désignation de l’organisation attribuée par le pays ou la région. |
| 1      | Active Directory | Attribué par l’organisation.                            |
| 5      | Classes          | Attribué par l’organisation.                            |
| 9      | classe d' **utilisateur**   | Attribué par l’organisation.                            |



 

Pour plus d’informations et pour connaître les deux procédures utilisées pour obtenir des OID valides à utiliser pour étendre le schéma Active Directory, consultez [obtention d’un identificateur d’objet](obtaining-an-object-identifier.md).

 

 




