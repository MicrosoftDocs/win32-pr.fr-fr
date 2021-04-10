---
title: Utilisation d’unités de données de protocole
description: Le protocole SNMP (simple Network Management Protocol) envoie des demandes et des réponses d’opération en tant que messages SNMP.
ms.assetid: 0928981c-4d60-4583-9eef-8127e05b1ba8
keywords:
- Utilisation d’unités de données de protocole SNMP
- Unités de données de protocole SNMP, utilisation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c2e40f36fa28f7ff17974d79f4f8ac29b8b6130b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104029529"
---
# <a name="working-with-protocol-data-units"></a>Utilisation d’unités de données de protocole

Le protocole SNMP (simple Network Management Protocol) envoie des demandes et des réponses d’opération en tant que messages SNMP. Un message SNMP est une unité de données de protocole (PDU) SNMP et des éléments d’en-tête de message supplémentaires définis par la RFC appropriée. Une PDU comprend une liste de liaisons de variables.

La structure d’une PDU est limitée à l’implémentation de l’WinSNMP Microsoft. Une application WinSNMP peut accéder à un PDU avec un descripteur de type **HSNMP \_ PDU**. L’application WinSNMP doit créer un PDU avant d’appeler la fonction [**SnmpSendMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsendmsg) ou la fonction [**SnmpEncodeMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpencodemsg) .

L’application peut extraire et mettre à jour les éléments de données d’une PDU, et libérer les ressources allouées aux PDU. Pour effectuer ces opérations, l’application utilise les [fonctions d’rampe d’alimentation](winsnmp-functions.md)winsnmp. Le tableau suivant répertorie les rubriques qui traitent de l’utilisation des PDU dans l’environnement de programmation WinSNMP.



| Rubrique                                                                        | Description                                                        |
|------------------------------------------------------------------------------|--------------------------------------------------------------------|
| [Création d’une PDU](creating-a-pdu.md)                                         | Décrit comment créer une PDU.                                     |
| [Mise à jour d’une PDU](updating-a-pdu.md)                                         | Décrit comment récupérer et mettre à jour les champs de la PDU.                   |
| [Duplication d’une PDU](duplicating-a-pdu.md)                                   | Décrit comment dupliquer une PDU.                                  |
| [Validation d’une PDU](validating-a-pdu.md)                                     | Décrit la validation d’une PDU.                                 |
| [Réponse correspondante et demandes d’alimentation (PDU)](matching-response-and-request-pdus.md) | Décrit le processus de correspondance d’un PDU de réponse à un PDU de demande. |



 

Pour plus d’informations, consultez [utilisation des listes de liaisons de variables](working-with-variable-binding-lists.md) et des objets de handle de [ressource](resource-handle-objects.md).

 

 




