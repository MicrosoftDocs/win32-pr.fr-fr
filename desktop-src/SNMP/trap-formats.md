---
title: Formats d’interruption
description: Le format des PDU d’interruption est différent de celui des autres PDU. Le format des interruptions SNMPv1 et SNMPv2C est également différent.
ms.assetid: 2d2b4520-28b7-4a2e-8dee-456e17d9d6f6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b73e9cd2a5396bbe258fcb67c88cc207ea0243a9e8aff9f31e4866b9ee8adcc1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119885679"
---
# <a name="trap-formats"></a>Formats d’interruption

Le format des PDU d’interruption est différent de celui des autres PDU. Le format des interruptions SNMPv1 et SNMPv2C est également différent.

Dans l’infrastructure SNMPv2C, le format de l’interruption de la PDU est une liste de liaison variable de *n* entrées de liaison de variable organisées de la manière suivante :

-   La première entrée de liaison de variable contient un horodatage.
-   La deuxième entrée de liaison de variable est un identificateur d’objet qui identifie l’interruption.
-   Les troisième et *n* entrées de liaison de variable, le cas échéant, contiennent des informations supplémentaires associées à l’interruption.

Dans le cadre de l’infrastructure SNMPv1, le format d’interruption de la PDU est le suivant.

| Champ                      | Description                                                      |
|----------------------------|------------------------------------------------------------------|
| enterprise                 | Identifie le type d’appareil qui a généré l’interruption.           |
| ADR de l’agent                 | Identifie l’adresse IP de l’appareil qui a généré l’interruption. |
| interruption générique/d’interruption spécifique | Identifie un type d’interruption prédéfini.                               |
| horodatage                 | Identifie le moment où l’interruption a été générée.                          |
| liaisons de variables          | Contient des informations supplémentaires associées à l’interruption.        |



 

La fonction [**SnmpRecvMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmprecvmsg) retourne toujours un message au format SNMPv2c. Si le message contient le type d' **opération \_ \_ interruption PDU SNMP**, l’application peut lire les entrées de liaison de variable du message et récupérer les informations associées à l’interruption.

 

 




