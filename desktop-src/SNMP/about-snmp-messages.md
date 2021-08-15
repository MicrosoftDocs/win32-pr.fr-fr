---
title: À propos des messages SNMP
description: Le protocole de gestion de réseau simple utilise des messages pour communiquer et échanger des informations entre les entités SNMP distantes.
ms.assetid: 9ba4b854-fc02-40c1-a92f-7c102c900e95
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e90c8e6aba33384ddaf16fbe847f20488f0be4d584c70563a34d052a37e80a23
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119009947"
---
# <a name="about-snmp-messages"></a>À propos des messages SNMP

Le protocole de gestion de réseau simple utilise des messages pour communiquer et échanger des informations entre les entités SNMP distantes. Les messages SNMP contiennent des unités de données de protocole (PDU) et des éléments d’en-tête de message supplémentaires définis par la RFC appropriée. Une PDU est un paquet de données qui contient des composants de données SNMP (ou champs).

Le format d’un message SNMP est le même pour SNMPv1 et SNMPv2C. Toutefois, SNMPv2C prend en charge des types PDU supplémentaires. Par exemple, il prend en charge le type de demande [ \_ \_ GETBULK PDU](snmp-variable-types-and-request-pdu-types.md) , qui permet à une application de récupérer efficacement des blocs de données volumineux à partir d’entités cibles.

 

 




