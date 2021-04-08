---
title: Utilisation des listes de liaisons de variables
description: Une liaison de variable correspond à l’Association d’un nom d’instance d’objet SNMP à une valeur associée. Une liste de liaisons de variables est une série d’entrées de liaison de variable. Dans WinSNMP, une unité de données de protocole (PDU) comprend une liste de liaisons de variables.
ms.assetid: e6353ae7-1d32-4de4-8518-49864fcbfc57
keywords:
- Utilisation des listes de liaisons de variables SNMP
- Liste de liaisons de variables SNMP, SNMP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 26719c7dc987e61542f38a0b86db78c573793f98
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/20/2020
ms.locfileid: "103723666"
---
# <a name="working-with-variable-binding-lists"></a>Utilisation des listes de liaisons de variables

Une *liaison de variable* correspond à l’Association d’un nom d’instance d’objet SNMP à une valeur associée. Une *liste de liaisons de variables* est une série d’entrées de liaison de variable. Dans WinSNMP, une unité de données de protocole (PDU) comprend une liste de liaisons de variables.

Les détails de la structure de la liste de liaisons de variables sont limités à l’implémentation de l’WinSNMP Microsoft. Une application WinSNMP peut accéder à une liste de liaisons de variables avec un handle de type **HSNMP \_ VBL**. Pour plus d’informations, consultez [objets descripteur de ressource](resource-handle-objects.md).

L’application WinSNMP peut construire et manipuler des listes de liaisons de variables, et les inclure dans des PDU. Pour effectuer ces opérations, l’application utilise les [fonctions de liaison de variable](winsnmp-functions.md)winsnmp. Pour plus d’informations sur l’utilisation des listes de liaisons de variables et WinSNMP, consultez les rubriques répertoriées dans le tableau suivant.



| Rubrique                                                                    | Description                                      |
|--------------------------------------------------------------------------|--------------------------------------------------|
| [Création d’une liste de liaisons de variables](creating-a-variable-binding-list.md) | Décrit comment créer une liste de liaisons de variables. |
| [Gestion d’une liste de liaisons de variables](managing-a-variable-binding-list.md) | Décrit comment gérer une liste de liaisons de variables. |



 

Pour plus d’informations sur les liaisons de variables et les listes de liaisons de variables, consultez [RFC1905](https://www.ietf.org/rfc/rfc1905.txt), « protocole Operations for version 2 of simple Network Management Protocol (SNMPv2) » et les [fonctions de liaison de variable](winsnmp-functions.md)winsnmp.

 

 




