---
title: Authentification, autorisation et gestion des comptes RADIUS
description: NPS prend entièrement en charge le protocole protocole RADIUS (Remote Authentication Dial-In User Service) (RADIUS). Le protocole RADIUS est la norme de facto pour l’authentification des utilisateurs distants et il est documenté dans le document RFC 2865 et RFC 2866.
ms.assetid: 3e00d555-355c-4a4c-a389-ab44e9ed9ca9
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e3b0395b6bc147da4f78bb718cda714014b9b665f5a26a8d20fa29402ee8dec1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119063489"
---
# <a name="radius-authentication-authorization-and-accounting"></a>Authentification, autorisation et gestion des comptes RADIUS

> [!Note]  
> le Service d’authentification Internet (IAS) a été renommé serveur nps (network Policy Server) à partir de Windows Server 2008. Le contenu de cette rubrique s’applique à IAS et à NPS. Dans le texte, NPS est utilisé pour faire référence à toutes les versions du service, y compris les versions initialement appelées IAS.

 

NPS prend entièrement en charge le protocole protocole RADIUS (Remote Authentication Dial-In User Service) (RADIUS). Le protocole RADIUS est la norme de facto pour l’authentification des utilisateurs distants et il est documenté dans le document [rfc 2865](https://www.ietf.org/rfc/rfc2865.txt) et [RFC 2866](https://www.ietf.org/rfc/rfc2866.txt).

## <a name="radius-authentication-and-authorization"></a>Authentification et autorisation RADIUS

Le diagramme suivant montre un client d’authentification (« utilisateur ») qui se connecte à un serveur d’accès réseau (NAS) via une connexion d’accès à distance, à l’aide de la protocole PPP (PPP). Pour authentifier l’utilisateur, le NAS contacte un serveur distant exécutant NPS. Le serveur NAS et le serveur NPS communiquent à l’aide du protocole RADIUS.

![authentification des utilisateurs distants](images/ias01.png)

Un NAS fonctionne comme un client d’un serveur ou de serveurs qui prennent en charge le protocole RADIUS. Les serveurs qui prennent en charge le protocole RADIUS sont généralement appelés serveurs RADIUS. Le client RADIUS, autrement dit, le NAS, transmet des informations sur l’utilisateur aux serveurs RADIUS désignés, puis agit sur la réponse que les serveurs renvoient. La demande envoyée par le NAS au serveur RADIUS afin d’authentifier l’utilisateur est généralement appelée « demande d’authentification ».

Si un serveur RADIUS authentifie l’utilisateur avec succès, le serveur RADIUS retourne des informations de configuration au NAS afin qu’il puisse fournir un service réseau à l’utilisateur. Ces informations de configuration sont composées de « autorisations » et elles contiennent, entre autres, le type de service que le NAS peut fournir à l’utilisateur (par exemple, PPP ou Telnet).

Pendant que le serveur RADIUS traite la demande d’authentification, il peut effectuer des fonctions d’autorisation telles que la vérification du numéro de téléphone de l’utilisateur et la vérification de la présence ou non d’une session de l’utilisateur. Le serveur RADIUS peut déterminer si l’utilisateur a déjà une session en cours en contactant un serveur d’État.

Pour plus d’informations sur l’authentification et l’autorisation RADIUS, consultez [RFC 2865](https://www.ietf.org/rfc/rfc2865.txt).

## <a name="radius-accounting"></a>Gestion des comptes RADIUS

Le serveur RADIUS collecte également une variété d’informations envoyées par le NAS qui peuvent être utilisées pour la gestion des comptes et pour la création de rapports sur l’activité réseau. Le client RADIUS envoie des informations aux serveurs RADIUS désignés quand l’utilisateur se connecte et se déconnecte. Le client RADIUS peut envoyer des informations d’utilisation supplémentaires sur une base périodique pendant que la session est en cours. Les demandes envoyées par le client au serveur pour enregistrer les informations d’ouverture/de fermeture de session et d’utilisation sont généralement appelées « demandes de gestion ».

Pour plus d’informations sur la gestion des comptes RADIUS, consultez [RFC 2866](https://www.ietf.org/rfc/rfc2866.txt).

## <a name="radius-proxy"></a>Proxy RADIUS

Un serveur RADIUS peut agir en tant que client proxy pour d’autres serveurs RADIUS. Dans ce cas, le serveur RADIUS contacté par le NAS transmet la requête d’authentification ou de gestion des comptes à un autre serveur RADIUS qui effectue réellement l’authentification ou la tâche de gestion des comptes.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Service d’authentification Internet et serveur NPS (Network Policy Server)](internet-authentication-service-vs-network-policy-server.md)
</dt> <dt>

[Paquets de gestion de comptes RADIUS](/windows/desktop/Nps/ias-radius-accounting-packets)
</dt> <dt>

[Utilisation d’un serveur d’État](/windows/desktop/Nps/ias-working-with-a-state-server)
</dt> </dl>

 

 