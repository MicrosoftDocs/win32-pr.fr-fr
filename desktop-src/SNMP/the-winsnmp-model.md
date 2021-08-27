---
title: Le modèle WinSNMP
description: Le modèle compatible WinSNMP comprend les composants de base suivants.
ms.assetid: 491df017-0b91-4fcf-97c3-4e296c3324bc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8814786b6ae44527460930daf5a9e8164645ca0ecfce52824831b2dbc7e61e80
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120127579"
---
# <a name="the-winsnmp-model"></a>Le modèle WinSNMP

Le modèle compatible WinSNMP comprend les composants de base suivants :

-   Une application de gestion de réseau SNMP compatible WinSNMP, c’est-à-dire une *application* compatible WinSNMP
-   Couche de fonction WinSNMP
-   Un fournisseur de services SNMP compatible avec WinSNMP, c’est-à-dire une *implémentation* conforme à WinSNMP

Les applications de gestion de réseau qui doivent transmettre des messages SNMP fonctionnent efficacement dans un environnement piloté par les événements. Cela est dû au fait que le protocole SNMP est un protocole basé sur des datagrammes ou sans connexion entre les entités distantes qui n’établissent pas de circuits virtuels.

étant donné que les applications Microsoft Windows sont également pilotées par les événements, WinSNMP utilise un modèle de programmation dans lequel la réception et le traitement des applications de gestion des *événements de message* asynchrones. Un événement de message asynchrone peut être une demande d’opération SNMP par une application de gestionnaire, ou la réponse à une demande d’une application agent.

SNMP envoie les demandes et les réponses en tant que messages SNMP. Un message SNMP est une unité de données de protocole (PDU) SNMP et des éléments d’en-tête de message supplémentaires définis par la RFC appropriée. Pour plus d’informations, consultez [à propos des messages SNMP](about-snmp-messages.md), [utilisation des listes de liaisons de variables](working-with-variable-binding-lists.md) et [utilisation des unités de données de protocole](working-with-protocol-data-units.md).

 

 




