---
description: Le fournisseur SNMP utilise les qualificateurs de propriété CIM suivants lors du mappage des définitions d’objets MIB aux définitions de classe CIM.
ms.assetid: 6e858e7e-5c46-4350-9696-c5efa1252c00
ms.tgt_platform: multiple
title: Qualificateurs de propriété CIM pour les objets MIB
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 34f2a25edf9c15930202d3c8cf79d3d62b0d1dd9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104209991"
---
# <a name="cim-property-qualifiers-for-mib-objects"></a>Qualificateurs de propriété CIM pour les objets MIB

Le fournisseur SNMP utilise les qualificateurs de propriété CIM suivants lors du mappage des définitions d’objets MIB aux définitions de classe CIM. Un qualificateur obligatoire doit être présent pour permettre au fournisseur SNMP de résoudre entièrement un objet MIB. L’impossibilité de définir un qualificateur obligatoire renvoie une erreur. La spécification d’une valeur de qualificateur non conforme retourne également une erreur.

> [!Note]  
> Pour plus d’informations sur l’installation du fournisseur, consultez [configuration de l’environnement SNMP WMI](setting-up-the-wmi-snmp-environment.md).

 



| Qualificateur                          | Description                                                                                                                                                                                            |
|------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Bits**                           | **chaîne** Obligatoire, si le qualificateur de la **\_ Convention textuelle** n’est pas égal au bit.<br/> Valeurs énumérées pour la définition de sous-type d’un bit.<br/>                                        |
| **Cimtype**                        | **chaîne** Requise<br/> Représentation textuelle CIM qui met en forme une valeur de protocole CIM sous-jacente.<br/>                                                                                    |
| **Defval**                         | **chaîne** Facultatif<br/> Valeur par défaut de l’objet.<br/>                                                                                                                                       |
| **Description**                    | **chaîne** Facultatif<br/> Description de l’objet.<br/>                                                                                                                                    |
| **Indicateur d’affichage \_**                  | **chaîne** Facultatif<br/> Manière dont les données de l’objet doivent apparaître à un utilisateur.<br/>                                                                                                    |
| **Encodage**                       | **chaîne** Facultatif<br/> Type SNMP utilisé lors de l’encodage des frames de protocole SNMPv1 et SNMPv2C.<br/>                                                                                              |
| **Enumeration**                    | **chaîne** Obligatoire, si le qualificateur de la **\_ Convention textuelle** n’est pas égal à ENUMERATEDINTEGER.<br/> Valeurs énumérées pour une définition de sous-type d’entier énuméré.<br/>                  |
| **\_Longueur fixe**                  | **UInt32** Facultatif<br/> Valeur de longueur fixe.<br/>                                                                                                                                           |
| [**Essentiel**](standard-qualifiers.md) | Valeur **booléenne** Facultatif<br/> Propriété de clé d’une définition de classe.<br/>                                                                                                                             |
| **Ordre des clés \_**                     | **UInt32** Facultatif, sauf si [**Key**](standard-qualifiers.md) est spécifié.<br/> Ordre de la propriété de clé dans la définition de classe.<br/>                                                   |
| **Nom**                           | **chaîne** Requise<br/> Nom implicite de la propriété. Notez que ce qualificateur n’est pas défini explicitement.<br/>                                                                           |
| **Identificateur d’objet \_**             | **chaîne** Requise<br/> Identificateur d’objet MIB de l’objet.<br/>                                                                                                                              |
| **Syntaxe de l’objet \_**                 | **chaîne** Facultatif<br/> Définition de type nommé de l’objet.<br/>                                                                                                                               |
| **Lire**                           | Valeur **booléenne** Facultatif (au moins l’une des options **Read** ou **Write** doit être spécifiée)<br/> Octroie l’accès en lecture à l’objet.<br/>                                                                     |
| **Référence**                      | **chaîne** Facultatif<br/> Fait référence à un autre document qui contient plus d’informations sur l’objet.<br/>                                                                                   |
| **État**                         | **chaîne** Facultatif<br/> Indique si l’objet doit être pris en charge.<br/>                                                                                                               |
| **\_Convention textuelle**            | **chaîne** Requise<br/> Représentation textuelle de la clause syntaxique de la macro de [type objet](object-type-macro.md) MIB.<br/>                                                           |
| **Unités**                          | **chaîne** Facultatif<br/> Définition précise de ce que l’objet représente.<br/>                                                                                                             |
| **Longueur de variable \_**               | **chaîne** Facultatif<br/> Valeurs minimales, maximales et de longueur fixe associées à la définition de type de l’objet.<br/>                                                                       |
| **Valeur de la variable \_**                | **chaîne** Facultatif<br/> Valeurs étendues et fixes associées à la définition de type de l’objet.<br/>                                                                                         |
| **\_Clé virtuelle**                   | Valeur **booléenne** Facultatif<br/> Indique que la valeur de la propriété doit être basée sur le sur-ensemble d’informations d’instance associées à tous les objets MIB accessibles dans la définition de classe.<br/> |
| **Écrire**                          | Valeur **booléenne** Facultatif (au moins l’une des options **Read** ou **Write** doit être spécifiée)<br/> Accorde l’accès en écriture à l’objet.<br/>                                                                    |



 

 

 




