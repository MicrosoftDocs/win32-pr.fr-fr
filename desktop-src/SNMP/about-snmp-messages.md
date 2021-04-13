---
title: À propos des messages SNMP
description: Le protocole de gestion de réseau simple utilise des messages pour communiquer et échanger des informations entre les entités SNMP distantes.
ms.assetid: 9ba4b854-fc02-40c1-a92f-7c102c900e95
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4a0426bf44d976ddf9e2eafe2093dcea94956cb4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104379748"
---
# <a name="about-snmp-messages"></a>À propos des messages SNMP

Le protocole de gestion de réseau simple utilise des messages pour communiquer et échanger des informations entre les entités SNMP distantes. Les messages SNMP contiennent des unités de données de protocole (PDU) et des éléments d’en-tête de message supplémentaires définis par la RFC appropriée. Une PDU est un paquet de données qui contient des composants de données SNMP (ou champs).

Le format d’un message SNMP est le même pour SNMPv1 et SNMPv2C. Toutefois, SNMPv2C prend en charge des types PDU supplémentaires. Par exemple, il prend en charge le type de demande [ \_ \_ GETBULK PDU](snmp-variable-types-and-request-pdu-types.md) , qui permet à une application de récupérer efficacement des blocs de données volumineux à partir d’entités cibles.

 

 




