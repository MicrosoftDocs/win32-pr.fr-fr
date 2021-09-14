---
description: Les extensions de socket sécurisé de Winsock permettent à une application de socket de contrôler la sécurité de leur trafic sur un réseau.
ms.assetid: 023a9f96-814f-40c3-a186-ae0a0c9baef2
title: Extensions Winsock Secure Socket
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b62ee593b3abbb3bb0f8dbf27b79d6868f04fc0
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126918875"
---
# <a name="winsock-secure-socket-extensions"></a>Extensions Winsock Secure Socket

Les extensions de socket sécurisé de Winsock permettent à une application de socket de contrôler la sécurité de leur trafic sur un réseau. Ces extensions permettent à une application de fournir la stratégie de sécurité et les exigences de son trafic réseau, et d’interroger les paramètres de sécurité appliqués. Par exemple, une application peut utiliser ces extensions pour interroger le jeton de sécurité d’homologue qui peut être utilisé pour effectuer des vérifications d’accès au niveau de l’application.

Les extensions de socket sécurisé sont conçues pour intégrer les services fournis par IPsec et d’autres protocoles de sécurité à l’aide de Winsock Framework. avant Windows Vista, sur Windows Server 2003 et Windows XP, IPsec a été configuré par un administrateur via des stratégies locales et de domaine. sur Windows Vista, secure socket extensions permet à la place des applications de configurer et de contrôler entièrement ou partiellement la sécurité de leur trafic réseau au niveau du socket.

les Applications peuvent déjà sécuriser le trafic réseau à l’aide d’api publiques, telles que la gestion IPsec, la plateforme de filtrage Windows et l’Interface SSPI (Security Support Provider Interface). Toutefois, l’utilisation de ces API peut rendre l’application plus difficile à développer et peut compliquer la configuration et le déploiement de. Les extensions Winsock Secure Socket ont été conçues pour simplifier le développement d’applications réseau qui nécessitent un trafic réseau sécurisé en laissant Winsock gérer la plus grande partie de la complexité.

ces extensions de socket sécurisé sont disponibles sur Windows Vista et versions ultérieures.

## <a name="secure-socket-functions"></a>Fonctions de socket sécurisé

Les fonctions d’extension de socket sécurisé sont les suivantes :

-   [**WSADeleteSocketPeerTargetName**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-wsadeletesocketpeertargetname)
-   [**WSAImpersonateSocketPeer**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-wsaimpersonatesocketpeer)
-   [**WSAQuerySocketSecurity**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-wsaquerysocketsecurity)
-   [**WSARevertImpersonation**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-wsarevertimpersonation)
-   [**WSASetSocketPeerTargetName**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-wsasetsocketpeertargetname)
-   [**WSASetSocketSecurity**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-wsasetsocketsecurity)

> [!Note]  
> les fonctions de socket sécurisé ne prennent actuellement en charge que le protocole IPsec et sont disponibles sur Windows Vista et versions ultérieures.

 

Les structures et les énumérations utilisées par les fonctions de socket sécurisé sont les suivantes :

-   [**nom de la cible de l' \_ homologue du socket \_ \_**](/windows/desktop/api/Mstcpip/ns-mstcpip-socket_peer_target_name)
-   [**\_protocole de sécurité de socket \_**](/windows/desktop/api/Mstcpip/ne-mstcpip-socket_security_protocol)
-   [**\_ \_ informations sur la requête de sécurité de socket \_**](/windows/desktop/api/Mstcpip/ns-mstcpip-socket_security_query_info)
-   [**\_modèle de \_ requête de sécurité de socket \_**](/windows/desktop/api/Mstcpip/ns-mstcpip-socket_security_query_template)
-   [**\_paramètres de sécurité du socket \_**](/windows/desktop/api/Mstcpip/ns-mstcpip-socket_security_settings)
-   [**paramètres de sécurité du SOCKET \_ \_ \_ IPSec**](/windows/desktop/api/Mstcpip/ns-mstcpip-socket_security_settings_ipsec)

Les fonctions de socket sécurisé sont simples à utiliser pour les applications normales et sont suffisamment flexibles pour les applications qui ont besoin d’un niveau de contrôle élevé sur leur sécurité. Ces fonctions permettent de garder le mécanisme de sécurité sous-jacent masqué de l’application. Une application peut spécifier des exigences de sécurité génériques et permettre à l’administrateur de contrôler le protocole de sécurité utilisé pour prendre en charge les exigences. Bien qu’il soit possible d’étendre ces fonctions pour ajouter d’autres protocoles de sécurité, actuellement, seul IPsec s’intègre aux fonctions de socket sécurisé.

La fonction [**WSASetSocketSecurity**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-wsasetsocketsecurity) permet à une application d’activer la sécurité et d’appliquer des paramètres de sécurité avant qu’une connexion soit établie.

La fonction [**WSASetSocketPeerTargetName**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-wsasetsocketpeertargetname) permet à une application de spécifier le nom cible correspondant à une entité homologue. Le protocole de sécurité sélectionné utilisera ces informations lors de l’authentification de l’homologue. Cette fonctionnalité résout les problèmes liés aux attaques de l’intercepteur approuvé.

La fonction [**WSADeleteSocketPeerTargetName**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-wsadeletesocketpeertargetname) est utilisée pour supprimer un nom d’homologue précédemment spécifié pour un Socket.

Une fois qu’une connexion est établie, la fonction [**WSAQuerySocketSecurity**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-wsaquerysocketsecurity) permet à une application d’interroger les propriétés de sécurité de la connexion, ce qui peut inclure le jeton d’accès d’ordinateur ou d’accès à l’ordinateur.

Après l’établissement d’une connexion, la fonction [**WSAImpersonateSocketPeer**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-wsaimpersonatesocketpeer) permet à une application d’emprunter l’identité de l’entité de sécurité correspondant à un homologue de socket afin d’effectuer une autorisation au niveau de l’application.

Le [**WSARevertImpersonation**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-wsarevertimpersonation) permet à une application de mettre fin à l’emprunt d’identité d’un homologue de Socket.

## <a name="secure-socket-architecture"></a>Architecture du socket sécurisé

![architecture de base des extensions Winsock Secure Socket](images/ss-arch.png)

-   Une application appelle les fonctions de socket sécurisé pour définir ou interroger les paramètres de sécurité d’un Socket.
-   les fonctions de socket sécurisé sont un ensemble de fonctions d’extension de type sécurisé qui encapsulent les appels à la fonction [**WSAIoctl**](/windows/desktop/api/Winsock2/nf-winsock2-wsaioctl) à l’aide de valeurs nouvellement définies pour le paramètre *dwIoControlCode* disponible sur Windows Vista et versions ultérieures. Ces IOCTL sont gérées par la pile réseau.
-   La pile réseau dirigera l’appel vers l’application de la [couche application (ALE)](../fwp/application-layer-enforcement--ale-.md) avec le descripteur du point de terminaison. Pour les fonctions [**WSADeleteSocketPeerTargetName**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-wsadeletesocketpeertargetname), [**WSASetSocketPeerTargetName**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-wsasetsocketpeertargetname)et [**WSASetSocketSecurity**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-wsasetsocketsecurity) , ALE configure les paramètres de l’application sur le point de terminaison local. Pour la fonction [**WSAQuerySocketSecurity**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-wsaquerysocketsecurity) , ALE lira les informations demandées à partir des points de terminaison locaux et distants applicables.
-   en fonction des événements de socket, l’application de la couche application (ALE) applique des stratégies pour l’architecture du socket sécurisé à l’aide de la plateforme de filtrage Windows. pour plus d’informations, consultez [à propos](../fwp/about-windows-filtering-platform.md) de la Windows de filtrage de la plateforme et de l' [application de la couche application (ALE)](../fwp/application-layer-enforcement--ale-.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[à propos de la plateforme de filtrage Windows](../fwp/about-windows-filtering-platform.md)
</dt> <dt>

[Exemples de Winsock avancés utilisant Secure Socket extensions](advanced-winsock-samples-using-secure-socket-extensions.md)
</dt> <dt>

[Application de la couche application (ALE)](../fwp/application-layer-enforcement--ale-.md)
</dt> <dt>

[Configuration IPsec](../fwp/ipsec-configuration.md)
</dt> <dt>

[Fonctions IPsec](../fwp/fwp-ipsec-functions.md)
</dt> <dt>

[Programmation Winsock sécurisée](secure-winsock-programming.md)
</dt> <dt>

[interface du fournisseur de la prise en charge de la sécurité (Security Support Provider Interface ou SSPI)](../rpc/security-support-provider-interface-sspi-.md)
</dt> <dt>

[Utilisation des extensions de socket sécurisé](using-secure-socket-extensions.md)
</dt> <dt>

[Plateforme de filtrage Windows](../fwp/windows-filtering-platform-start-page.md)
</dt> <dt>

[Windows Filtrage des fonctions API de la plateforme](../fwp/fwp-functions.md)
</dt> </dl>

 

 
