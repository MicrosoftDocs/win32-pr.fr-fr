---
description: Le protocole de négociation TLS (Transport Layer Security) est responsable de l’authentification et de l’échange de clés nécessaires à l’établissement ou à la reprise des sessions sécurisées.
ms.assetid: 65fb4db3-e505-457a-9159-dba0b506ea0b
title: Protocole de négociation TLS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e0c7cfa9e9db54a6035abe147ce00bbde59bcc86
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127096265"
---
# <a name="tls-handshake-protocol"></a>Protocole de négociation TLS

Le protocole de négociation TLS ( [*Transport Layer Security*](../secgloss/t-gly.md) ) est responsable de l’authentification et de l’échange de clés nécessaires à l’établissement ou à la reprise des sessions sécurisées. Lors de l’établissement d’une [*session*](../secgloss/s-gly.md)sécurisée, le protocole de négociation gère les éléments suivants :

-   Négociation de la suite de chiffrement
-   L’authentification du serveur et, éventuellement, le client
-   Échange d’informations sur la clé de session.

## <a name="cipher-suite-negotiation"></a>Négociation de la suite de chiffrement

Le client et le serveur effectuent un contact et choisissent la suite de chiffrement qui sera utilisée dans l’échange de messages.

## <a name="authentication"></a>Authentication

Dans TLS, un serveur prouve son identité au client. Le client peut également avoir besoin de prouver son identité au serveur. L’infrastructure à clé publique, l’utilisation de [*paires de clés publiques/privées*](../secgloss/p-gly.md), est la base de cette authentification. La méthode exacte utilisée pour l’authentification est déterminée par la suite de chiffrement négociée.

## <a name="key-exchange"></a>Exchange de clé

Le client et le serveur échangent des nombres aléatoires et un numéro spécial appelé secret pré-maître. Ces nombres sont combinés à des données supplémentaires permettant au client et au serveur de créer leur secret partagé, appelé secret principal. Le secret principal est utilisé par le client et le serveur pour générer le secret d’écriture MAC, qui est la clé de session utilisée pour le [*hachage*](../secgloss/h-gly.md), et la clé d’écriture, qui est la [*clé de session*](../secgloss/s-gly.md) utilisée pour le chiffrement.

## <a name="establishing-a-secure-session-by-using-tls"></a>Établissement d’une session sécurisée à l’aide de TLS

Le protocole de négociation TLS implique les étapes suivantes :

1.  Le client envoie un message « client Hello » au serveur, ainsi que la valeur aléatoire du client et les suites de chiffrement prises en charge.
2.  Le serveur répond en envoyant un message « Server Hello » au client, ainsi que la valeur aléatoire du serveur.
3.  Le serveur envoie son certificat au client à des fins d’authentification et peut demander un certificat au client. Le serveur envoie le message « serveur Hello Done ».
4.  Si le serveur a demandé un certificat à partir du client, le client l’envoie.
5.  Le client crée un secret de prémaster aléatoire et le chiffre à l’aide de la [*clé publique*](../secgloss/p-gly.md) du certificat du serveur, en envoyant le secret pré-maître chiffré au serveur.
6.  Le serveur reçoit le secret pré-maître. Le serveur et le client génèrent chacun le secret principal et les [*clés de session*](../secgloss/s-gly.md) en fonction du secret de prémaître.
7.  Le client envoie une notification « modifier les spécifications de chiffrement » au serveur pour indiquer que le client va commencer à utiliser les nouvelles [*clés de session*](../secgloss/s-gly.md) pour le [*hachage*](../secgloss/h-gly.md) et le chiffrement des messages. Le client envoie également le message « client terminé ».
8.  Le serveur reçoit « modifier la spécification de chiffrement » et bascule son état de sécurité de la couche d’enregistrement sur [*chiffrement symétrique*](../secgloss/s-gly.md) à l’aide des [*clés de session*](../secgloss/s-gly.md). Le serveur envoie le message « serveur terminé » au client.
9.  Le client et le serveur peuvent maintenant échanger des données d’application sur le canal sécurisé qu’ils ont établi. Tous les messages envoyés du client au serveur et du serveur au client sont chiffrés à l’aide de la clé de session.

## <a name="resuming-a-secure-session-by-using-tls"></a>Reprise d’une session sécurisée à l’aide de TLS

1.  Le client envoie un message « client Hello » à l’aide de l’ID de session de la session à reprendre.
2.  Le serveur examine son cache de session pour rechercher un ID de session correspondant. Si une correspondance est trouvée et que le serveur est en mesure de reprendre la session, il envoie un message « Server Hello » avec l’ID de session.
    > [!Note]  
    > Si une correspondance d’ID de session est introuvable, le serveur génère un nouvel ID de session et le client TLS et le serveur effectuent une négociation complète.

     

3.  Le client et le serveur doivent échanger des messages « modifier les spécifications de chiffrement » et envoyer des messages « client terminé » et « serveur terminé ».
4.  Le client et le serveur peuvent maintenant reprendre l’échange de données d’application sur le canal sécurisé.

 

 
