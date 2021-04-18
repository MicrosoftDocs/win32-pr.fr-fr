---
title: Certificats SSL
description: SSL (Secure Sockets Layer) (SSL) est devenu une norme pour la sécurisation des connexions Internet et est utilisée pour empêcher les écoutes clandestines sur le réseau. Le protocole SSL permet à un client et un serveur de s’authentifier mutuellement et de négocier des algorithmes de chiffrement.
ms.assetid: 2b78f609-473f-467b-8bf4-709b790bca53
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e15e4e6f2b0fe9e3bb058ba506f8a36728540443
ms.sourcegitcommit: be2b23d847b9717224c5f31816594c8abda388a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/18/2020
ms.locfileid: "106533554"
---
# <a name="ssl-certificates"></a>Certificats SSL

SSL (Secure Sockets Layer) (SSL), également connu sous le nom de TLS (Transport Layer Security), est devenu une norme pour la sécurisation des connexions Internet et est utilisée pour empêcher les écoutes clandestines sur le réseau. Le protocole SSL/TLS permet à un client et un serveur de s’authentifier mutuellement et de négocier des algorithmes de chiffrement.

SSL utilise une clé de chiffrement et un algorithme de chiffrement pour sécuriser la connexion HTTP. Les clés de chiffrement sont contenues dans les certificats SSL utilisés par le client et le serveur. Le certificat est généralement un document X. 509 ([RFC 2459](https://www.ietf.org/rfc/rfc2459.txt)). Le serveur fournit le certificat SSL pour la session et envoie le certificat au client dans la phase de négociation. Le client envoie son certificat au serveur uniquement si le serveur envoie une demande au client pour un certificat. Par conséquent, le client authentifie toujours le serveur, mais le serveur a la possibilité d’authentifier le client ou non.

Les certificats de serveur doivent être stockés dans le stockage persistant local de l’API du serveur HTTP, pour être utilisés chaque fois qu’une connexion sécurisée est créée. Chaque entrée du magasin de certificats contient également l’adresse IP et le port du serveur, le hachage du certificat (utilisé pour la signature des messages) et l’ID de l’application. L’ID d’application est utilisé pour identifier l’application propriétaire du certificat.

Les administrateurs système peuvent stocker les informations de certificat de serveur SSL avec les API de configuration. Un outil d’administration appelle la fonction [**HttpSetServiceConfiguration**](/windows/desktop/api/Http/nf-http-httpsetserviceconfiguration) et spécifie la valeur HttpServiceConfigSSLCertInfo pour le paramètre de configuration de service afin de définir des informations pour un certificat SSL. Un seul certificat de serveur peut être configuré pour chaque paire adresse IP/port sur l’ordinateur. L’API du serveur HTTP fournit également des fonctions de [**requête**](/windows/desktop/api/Http/nf-http-httpqueryserviceconfiguration) et de [**suppression**](/windows/desktop/api/Http/nf-http-httpdeleteserviceconfiguration) pour accéder ou supprimer des certificats existants.

 

 




