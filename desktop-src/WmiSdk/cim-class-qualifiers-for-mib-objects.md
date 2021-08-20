---
description: Le fournisseur SNMP utilise les qualificateurs de classe CIM suivants lors du mappage des définitions d’objets MIB aux définitions de classe CIM.
ms.assetid: 458167dc-562e-47b8-8760-797ae13f9459
ms.tgt_platform: multiple
title: Qualificateurs de classe CIM pour les objets MIB
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e3f7e84473a85ef78cd81f6d0a3f4fc7cc1e488d2dec955c31a917677a9631c8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117925846"
---
# <a name="cim-class-qualifiers-for-mib-objects"></a>Qualificateurs de classe CIM pour les objets MIB

Le fournisseur SNMP utilise les qualificateurs de classe CIM suivants lors du mappage des définitions d’objets MIB aux définitions de classe CIM. Un qualificateur obligatoire doit être présent pour permettre au fournisseur SNMP de résoudre entièrement un objet de groupe. L’impossibilité de définir un qualificateur obligatoire renvoie une erreur. La spécification d’une valeur de qualificateur non conforme retourne également une erreur.

> [!Note]  
> Pour plus d’informations sur l’installation du fournisseur, consultez [configuration de l’environnement SNMP WMI](setting-up-the-wmi-snmp-environment.md).

 



| Qualificateur           | Description                                                                                                                             |
|---------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| **Description**     | **chaîne** Facultatif<br/> Description de la classe.<br/>                                                                      |
| **ObjectID de groupe \_** | **chaîne** Obligatoire, si la classe est pour le fournisseur de classes SNMP.<br/> Identificateur d’objet de la collection fabriquée.<br/> |
| **Importations de modules \_** | **chaîne** Facultatif<br/> Liste séparée par des virgules des noms de module MIB utilisés pour résoudre les importations.<br/>                              |
| **Nom du module \_**    | **chaîne** Facultatif<br/> Nom d’identité d’un module MIB.<br/>                                                                 |
| **Référence**       | **chaîne** Facultatif<br/> Fait référence à un autre document qui contient plus d’informations sur la classe.<br/>                     |
| **Singleton**       | Valeur **booléenne** Obligatoire pour les classes mappées à partir de collections scalaires.<br/> Indique une classe qui ne peut avoir qu’une seule instance.<br/>  |



 

 

 




