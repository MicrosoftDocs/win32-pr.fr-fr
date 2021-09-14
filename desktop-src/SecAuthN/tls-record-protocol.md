---
description: Le protocole d’enregistrement TLS (Transport Layer Security) sécurise les données d’application à l’aide des clés créées pendant le protocole de transfert.
ms.assetid: 3ad4cbd9-ce7c-4882-9c53-c935068c0ba7
title: Protocole d’enregistrement TLS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a53d41ad73dc9e1338f0cbff1bec5d6cd6a55e3
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127096262"
---
# <a name="tls-record-protocol"></a>Protocole d’enregistrement TLS

Le protocole d’enregistrement TLS ( [*Transport Layer Security*](../secgloss/t-gly.md) ) sécurise les données d’application à l’aide des clés créées pendant le [protocole de transfert](tls-handshake-protocol.md). Le protocole d’enregistrement est responsable de la sécurisation des données d’application et de la vérification de leur [*intégrité*](../secgloss/i-gly.md) et de leur origine. Il gère les éléments suivants :

-   Division des messages sortants en blocs gérables et réassemblage des messages entrants.
-   Compression des blocs sortants et décompression des blocs entrants (facultatif).
-   Application d’un [*code d’Authentification de message*](../secgloss/m-gly.md) (Mac) aux messages sortants et vérification des messages entrants à l’aide du Mac.
-   Chiffrement des messages sortants et déchiffrement des messages entrants.

Lorsque le protocole d’enregistrement est terminé, les données chiffrées sortantes sont transmises à la couche TCP (Transmission Control Protocol) pour le transport.

 

 
