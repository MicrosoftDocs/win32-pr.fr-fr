---
description: Chaque définition d’objet MIB contient une clause ACCESS (SNMPv1) ou MAX-ACCESS (SNMPv2C) qui définit les droits d’accès à l’objet.
ms.assetid: c3b8d65b-c1ca-4131-baf4-1aab54451180
ms.tgt_platform: multiple
title: Clauses Access et MAX-ACCESS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 37084a25a48c874866774b990a70e1332e730103
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106523312"
---
# <a name="access-and-max-access-clauses"></a>Clauses Access et MAX-ACCESS

Chaque définition d’objet MIB contient une clause ACCESS (SNMPv1) ou MAX-ACCESS (SNMPv2C) qui définit les droits d’accès à l’objet.

> [!Note]  
> Pour plus d’informations sur l’installation du fournisseur, consultez [configuration de l’environnement SNMP WMI](setting-up-the-wmi-snmp-environment.md).

 

Le tableau suivant répertorie le mappage de la clause d’accès SNMPv1.



| Clause d’accès MIB | Qualificateur CIM       |
|-------------------|---------------------|
| en lecture seule         | **Lire**            |
| lecture-écriture        | **Lire**, **écrire** |
| en écriture seule        | **Écrire**           |
| non accessible    | **Non \_ accessible** |



 

Le tableau suivant répertorie le mappage de la clause MAX-ACCESS SNMPv2C.



| MIB-clause d’accès     | Qualificateur CIM       |
|-----------------------|---------------------|
| en lecture seule             | **Lire**            |
| lecture-écriture            | **Lire**, **écrire** |
| lecture-créer           | **Lire**            |
| accessible-pour notification | **Non \_ accessible** |
| non accessible        | **Non \_ accessible** |



 

Lorsqu’un objet MIB est mappé à not-accessible et n’est pas une propriété indexée de la classe, il n’existe aucun mappage de l’objet MIB lui-même.

 

 



