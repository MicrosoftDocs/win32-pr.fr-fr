---
title: Gestion d’une liste de liaisons de variables
description: La fonction SnmpGetVb récupère les informations de liaison de variable d’une liste de liaisons de variables. La fonction récupère le nom de la variable et la valeur associée à la variable à partir de l’entrée de liaison de variable spécifiée par l’application WinSNMP.
ms.assetid: 357aebd6-171a-4221-b12a-712702f9d9c6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7cc8c1cbfa4eb0ec3acdc13e9c9cc480b88ddae8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104028963"
---
# <a name="managing-a-variable-binding-list"></a>Gestion d’une liste de liaisons de variables

La fonction [**SnmpGetVb**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpgetvb) récupère les informations de liaison de variable d’une liste de liaisons de variables. La fonction récupère le nom de la variable et la valeur associée à la variable à partir de l’entrée de liaison de variable spécifiée par l’application WinSNMP.

Pour mettre à jour les entrées de liaison de variable dans une liste de liaisons de variables, appelez la fonction [**SnmpSetVb**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsetvb) . La fonction **SnmpSetVb** ajoute également de nouvelles entrées de liaison de variable à une liste de liaisons de variables existante.

L’application WinSNMP doit appeler la fonction [**SnmpDeleteVb**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpdeletevb) pour supprimer les entrées d’une liste de liaisons de variables.

Pour récupérer, modifier ou supprimer une entrée de liaison de variable, l’application WinSNMP doit spécifier la position de l’entrée dans la liste des liaisons de variables.

Un appel à la fonction [**SnmpSetPduData**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsetpdudata) associe une liste de liaisons de variables à un PDU. Un appel à la fonction [**SnmpGetPduData**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpgetpdudata) récupère une liste de liaisons de variables à partir d’une PDU. Une liaison de variable individuelle n’est pas directement associée à un PDU, mais elle est indirectement associée par son inclusion dans une liste de liaisons de variables.

 

 




