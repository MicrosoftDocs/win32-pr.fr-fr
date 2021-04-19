---
description: Lors du développement d’une application qui utilise les services HTTP Microsoft Windows (WinHTTP), il est important de comprendre les concepts et la terminologie suivants relatifs à la mise en réseau en général et au protocole HTTP en particulier.
ms.assetid: 6ea0c16f-1233-4580-97bb-14e224646857
title: Terminologie réseau (WinHTTP)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8173b921957a95ebde7f00034c31b2f016b78ab5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106521807"
---
# <a name="network-terminology-winhttp"></a>Terminologie réseau (WinHTTP)

Lors du développement d’une application qui utilise les services HTTP Microsoft Windows (WinHTTP), il est important de comprendre les concepts et la terminologie suivants relatifs à la mise en réseau en général et au protocole HTTP en particulier.

-   [Transactions HTTP](#http-transactions)
-   [Serveurs proxy](#proxy-servers)
-   [Modes synchrone et asynchrone](#synchronous-and-asynchronous-modes)
-   [Authentification](#authentication)

## <a name="http-transactions"></a>Transactions HTTP

Lorsque vous utilisez des transactions HTTP, vous échangez des informations avec un autre ordinateur ailleurs sur un réseau. Les informations échangées peuvent être un fichier contenant du texte ou du contenu multimédia, ou bien les résultats d’une requête de base de données. Une information échangée sur un réseau est appelée une *ressource*. Normalement, l’ordinateur qui envoie une ressource est le serveur et l’ordinateur qui reçoit cette ressource est un client. Toutefois, il est également possible pour un client de poster des données sur un serveur. Parfois, une transaction HTTP implique un serveur de couche intermédiaire. Un serveur de couche intermédiaire rassemble plusieurs ressources à partir d’autres serveurs, compile les informations en une seule ressource et envoie cette ressource au client.

Le processus d’obtention d’une ressource à l’aide du protocole HTTP nécessite l’échange d’une série de messages entre le client et le serveur. Le client commence la transaction en envoyant un message qui demande une ressource. Ce message est appelé requête HTTP, ou parfois simplement une demande. Une requête HTTP est constituée des composants suivants.

-   Méthode, Uniform Resource Identifier (URI), numéro de version du protocole
-   headers
-   Corps d’entité

Lorsqu’un serveur reçoit une demande, il répond en renvoyant un message au client. Le message envoyé par le serveur est appelé réponse HTTP. Une réponse HTTP est constituée des composants suivants.

-   Numéro de version du protocole, code d’État, texte d’État
-   headers
-   Corps d’entité

La réponse indique que la demande ne peut pas être traitée ou fournit des informations demandées. Selon le type de requête, il peut s’agir d’informations sur une ressource, telles que sa taille et son type, ou peut être une partie ou la totalité de la ressource elle-même. La partie d’une réponse qui comprend une partie ou la totalité de la ressource demandée est appelée « données de réponse » ou « corps d’entité » et la réponse n’est pas terminée tant que toutes les données de réponse n’ont pas été reçues.

Pour plus d’informations sur les transactions HTTP et le protocole HTTP, consultez [RFC 2616](https://www.ietf.org/rfc/rfc2616.txt), Hypertext Transfer Protocol (http/1.1).

## <a name="proxy-servers"></a>Serveurs proxy

Bien qu’une demande envoyée par un client soit finalement reçue par le serveur cible, il arrive que la transaction passe d’abord par un serveur proxy. Un proxy intercepte la demande et peut même modifier la demande avant de l’envoyer au serveur. Lorsque le serveur répond, la réponse passe également par le proxy avant d’être transférée au client. Le proxy peut modifier les en-têtes de cette réponse.

En interceptant et en traduisant les transactions réseau, un proxy peut :

-   Protégez le client en surveillant les transactions potentiellement dangereuses.
-   Permet au client de communiquer à l’aide de protocoles qui peuvent ne pas être implémentés par le logiciel client.
-   Agir en tant que passerelle entre un réseau privé et un réseau public.

L’API WinHTTP comprend un outil de configuration de proxy qui vous permet de fournir à WinHTTP des informations sur les serveurs proxy qui interceptent vos transactions HTTP. Pour plus d’informations sur l’utilisation de l’outil de configuration de proxy, consultez [ProxyCfg.exe, un outil de configuration de proxy](proxycfg-exe--a-proxy-configuration-tool.md).

## <a name="synchronous-and-asynchronous-modes"></a>Modes synchrone et asynchrone

Il existe deux modèles de programmation pour obtenir des ressources sur un réseau à l’aide de WinHTTP : les modèles synchrones et asynchrones. Dans un modèle synchrone, un appel à une fonction ou à une méthode ne se termine pas tant que l’opération demandée n’est pas terminée ou qu’une erreur ne se produit. Par exemple, lorsque votre application demande une ressource à l’aide de WinHTTP de manière synchrone, elle ne passe pas à l’étape suivante tant que les données demandées n’ont pas été reçues.

Un modèle asynchrone, en revanche, permet à une application d’effectuer d’autres tâches pendant qu’elle attend la récupération de la ressource. Si une autre fonction ou méthode WinHTTP est appelée et qu’une opération précédente n’est pas terminée, la fonction retourne une erreur. Lorsque vous utilisez WinHTTP de manière asynchrone, les événements COM (Component Object Model) et le rappel sont disponibles pour notifier une application de la progression dans une opération HTTP.

## <a name="authentication"></a>Authentification

L’authentification est le processus par lequel un proxy HTTP ou un serveur HTTP valide les informations de connexion d’un utilisateur avant d’autoriser l’accès aux ressources. Divers schémas d’authentification sont utilisés sur Internet. En général, le nom et le mot de passe d’un utilisateur sont comparés à une liste autorisée, et si le système détecte une correspondance, l’accès est accordé à l’étendue spécifiée dans la liste d’autorisations de l’utilisateur.

Les fonctions WinHTTP prennent en charge l’authentification serveur et proxy pour les sessions HTTP. WinHTTP prend en charge les schémas d’authentification suivants : de base, Digest (voir [RFC 2617](https://www.ietf.org/rfc/rfc2617.txt)), [authentification NTLM](../com/ntlmssp.md), Negotiate/ [Kerberos](../com/kerberos-v5-protocol.md)et Microsoft Passport 1,4. Pour plus d’informations sur l’authentification, ainsi qu’un exemple d’utilisation de l’authentification dans une application Microsoft Visual C++, consultez [authentification dans WinHTTP](authentication-in-winhttp.md).

Pour plus d’informations sur les considérations de sécurité relatives à l’authentification de base et Passport, consultez Considérations sur la [sécurité WinHTTP](winhttp-security-considerations.md).

 

 
