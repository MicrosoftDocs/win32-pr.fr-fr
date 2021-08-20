---
title: Serveurs proxy et WinRM
description: Windows La gestion à distance (WinRM) utilise HTTP et HTTPs pour envoyer des messages entre les ordinateurs client et serveur. En général, le client WinRM envoie des messages directement au serveur WinRM. Les clients WinRM peuvent également être configurés pour utiliser un serveur proxy.
ms.assetid: f8137b3a-7704-4b21-a923-6e2692e18d90
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 663493f9c3e71e44be000f436ad4573f911652a8e142b77ffab41acbff250b60
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118112937"
---
# <a name="proxy-servers-and-winrm"></a>Serveurs proxy et WinRM

Windows La gestion à distance (WinRM) utilise HTTP et HTTPs pour envoyer des messages entre les ordinateurs client et serveur. En général, le client WinRM envoie des messages directement au serveur WinRM. Les clients WinRM peuvent également être configurés pour utiliser un serveur proxy.

Pour plus d'informations, consultez les sections suivantes :

-   [Configuration d’un serveur proxy pour WinRM 2,0](#configuring-a-proxy-server-for-winrm-20)
    -   [Connexions par proxy HTTPs](#https-based-proxy-connections)
    -   [Connexions par proxy basées sur HTTP](#http-based-proxy-connections)
-   [Configuration d’un serveur proxy pour WinRM 1,1 et versions antérieures](#configuring-a-proxy-server-for-winrm-11-and-earlier)

## <a name="configuring-a-proxy-server-for-winrm-20"></a>Configuration d’un serveur proxy pour WinRM 2,0

WinRM 2,0 prend en charge un large éventail de configurations de proxy. Par exemple, WinRM prend en charge les proxies pour les transports HTTP et HTTPs, ainsi que pour les serveurs proxy authentifiés et non authentifiés.

### <a name="https-based-proxy-connections"></a>Connexions HTTPS-Based proxy

Pour une meilleure sécurité et une affinité basée sur la connexion, le protocole HTTPs doit être utilisé comme mécanisme de transport.

Si le serveur proxy requiert une authentification, les clients et les serveurs WinRM doivent utiliser le protocole HTTPs.

> [!Note]  
> L’authentification auprès du serveur proxy est indépendante de l’authentification au serveur de destination.

 

### <a name="http-based-proxy-connections"></a>Connexions HTTP-Based proxy

Si aucune authentification du serveur proxy n’est requise, le protocole HTTP ou HTTPs peut être utilisé pour le transport. Toutefois, les connexions basées sur HTTP entre un client WinRM et un serveur WinRM via un serveur proxy peuvent être problématiques.

Les problèmes suivants peuvent se produire lors de l’utilisation de connexions basées sur HTTP :

-   Le serveur proxy ne prend pas en charge l’authentification basée sur la connexion, ce qui peut entraîner l’échec de l’authentification sur le serveur de destination en raison d’une erreur d’accès refusé.
-   Plusieurs ensembles d’informations d’identification sont nécessaires pour se connecter au serveur de destination et au serveur proxy.
-   Les serveurs proxy HTTP peuvent ne pas prendre en charge la possibilité de gérer les connexions serveur et basées sur le client associées. Si le proxy ne lie pas fortement un client à un serveur et conserve la connexion TCP/IP, les clients non authentifiés peuvent accéder aux données. En outre, l’absence d’affinité de connexion peut entraîner l’échec de l’authentification sur le serveur.

Si vous devez utiliser le protocole HTTP comme transport, le serveur proxy doit prendre en charge la configuration suivante pour obtenir une meilleure réponse WinRM et empêcher les échecs d’accès refusés pour les clients WinRM :

-   Prise en charge de HTTP/1.1. HTTP/1.1 est plus strict dans le mappage de l’affinité de connexion entre le client et le serveur.
-   Authentification basée sur la connexion pour Negotiate, Kerberos et CredSSP.

    L’authentification d’une demande nécessite plusieurs allers-retours entre le client et le serveur. La plus grande négociation pour l’authentification est terminée une fois que le serveur d’authentification (WinRM) a envoyé une réponse au client qui n’est pas une réponse 401 (non autorisé). Si le serveur WinRM renvoie une réponse au client qui n’est pas une réponse 401, le proxy ne doit pas fermer la connexion.

    Plusieurs paires demande/réponse peuvent être envoyées entre le client et le serveur avant l’envoi des données de paquet réelles. WinRM 2,0 utilise les schémas d’authentification Negotiate et Kerberos avec le chiffrement, ce qui peut ajouter des allers-retours supplémentaires. Les données ne peuvent pas être envoyées au serveur tant que l’authentification n’est pas terminée.

    Le serveur WinRM renvoie une réponse de niveau 200 qui indique que l’authentification est terminée. Les serveurs proxy HTTP peuvent mettre fin à l’affinité d’authentification basée sur la connexion et fermer la connexion TCP/IP après avoir reçu la réponse de niveau 200 du serveur WinRM. Le dernier aller-retour entre le client et le serveur n’inclut pas le paquet de demande d’origine. Si le serveur proxy ferme la connexion, le serveur tente de réauthentifier le client et la demande du client n’est peut-être jamais envoyée au serveur. Si l’affinité basée sur la connexion n’est pas gérée, l’authentification par rapport au serveur de destination peut échouer avec une erreur d’accès refusé.

-   Persistance de la connexion. La connexion TCP/IP du client au proxy doit continuer à mapper à la même connexion TCP/IP entre le proxy et le serveur. La gestion de cette connexion permet d’obtenir un niveau de performance plus élevé. Si la connexion n’est pas maintenue, chaque requête doit être authentifiée de nouveau, ce qui peut affecter les performances.

### <a name="encryption-and-winrm-20"></a>Chiffrement et WinRM 2,0

WinRM 2,0 prend en charge le chiffrement sur HTTP à l’aide des schémas d’authentification Negotiate, Kerberos et CredSSP. Si un serveur WinRM prend en charge le protocole HTTP et est accessible via un proxy, le serveur WinRM doit appliquer le chiffrement et ne pas autoriser le trafic réseau non chiffré.

Dans tous les cas, les requêtes HTTP non chiffrées doivent être envoyées par les serveurs proxy. Lorsque les données doivent traverser un serveur proxy avant d’être envoyées au serveur de destination, les problèmes de sécurité suivants sont très importants :

-   Il est possible qu’un serveur proxy malveillant examine toutes les paires demande/réponse, y compris les informations d’identification.
-   Si les connexions TCP/IP ne sont pas fortement mappées entre le client WinRM et le serveur proxy, et entre le serveur proxy et le serveur de destination, un client non autorisé peut se connecter au serveur de destination à l’aide de la même connexion authentifiée entre le serveur proxy et le serveur de destination. Le serveur de destination peut autoriser l’accès du client non authentifié aux données. Si le chiffrement est appliqué, le serveur de destination envoie un message d’accès refusé au client non authentifié.

L’utilisation du chiffrement permet d’atténuer les problèmes de sécurité potentiels.

## <a name="configuring-a-proxy-server-for-winrm-11-and-earlier"></a>Configuration d’un serveur proxy pour WinRM 1,1 et versions antérieures

si un proxy est requis pour atteindre le serveur winrm, le client winrm s’appuie sur la configuration du proxy des services HTTP (WinHTTP) Windows. Par défaut, WinHTTP n’est pas configuré pour utiliser un serveur proxy. La configuration du proxy WinHTTP peut être modifiée à l’aide des utilitaires de ligne de commande [ProxyCfg.exe](/previous-versions/windows/desktop/ms761351(v=vs.85)) ou [netsh](/previous-versions/windows/it-pro/windows-server-2003/cc785383(v=ws.10)) .

**WinRM 1,1 et versions antérieures :** WinRM n’utilise pas les paramètres de proxy d’Internet Explorer.

 

 