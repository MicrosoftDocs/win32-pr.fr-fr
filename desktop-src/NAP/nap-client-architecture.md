---
title: Architecture du client NAP
description: un client nap est un ordinateur exécutant Windows XP avec Service Pack 3 (SP3), Windows Vista ou Windows Server 2008 qui comprend la plateforme NAP.
ms.assetid: 163c33c9-b18b-49f9-a2a1-fd90a1dc0826
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 15862eaa6ae4f4c1f79c53cf9d540aedec295e8a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127110597"
---
# <a name="nap-client-architecture"></a>Architecture du client NAP

> [!Note]  
> La plate-forme de protection d’accès réseau n’est pas disponible à partir de Windows 10

 

un client nap est un ordinateur exécutant Windows XP avec Service Pack 3 (SP3), Windows Vista ou Windows Server 2008 qui comprend la plateforme NAP.

Cette illustration montre l’architecture de la plateforme NAP sur un client NAP.

![architecture de la plateforme NAP sur un client NAP](images/nap-client-side-arch.png)

L’architecture du client NAP se compose des éléments suivants :

-   Couche de composants du client de mise en œuvre (EC)

    Chaque EC NAP est défini pour un autre type d’accès réseau. Par exemple, il existe une configuration NAP pour la configuration DHCP et une protection d’accès réseau (EC) NAP pour les connexions VPN d’accès à distance. L’EC NAP peut être mis en correspondance avec un type spécifique de point de contrainte de mise en conformité NAP. Par exemple, l’EC NAP DHCP est conçu pour fonctionner avec un point de contrainte de mise en conformité NAP basé sur DHCP. Certains logiciels NAP ECs sont fournis avec la plateforme NAP et des fournisseurs de logiciels tiers, ou Microsoft peuvent en fournir d’autres.

-   Une couche de composants de l’agent d’intégrité système (SHA)

    Un composant SHA gère et signale un ou plusieurs éléments de l’intégrité du système. Par exemple, il peut y avoir un SHA pour les signatures antivirus et un SHA pour les mises à jour du système d’exploitation. Un SHA peut être mis en correspondance avec un serveur de mise à jour, qui est un ordinateur qui contient des ressources de mise à jour d’intégrité auxquelles les clients NAP peuvent accéder pour remédier à leur état non conforme. Par exemple, un SHA pour vérifier les signatures antivirus est mis en correspondance avec le serveur qui contient le dernier fichier de signature antivirus. Il n’est pas nécessaire de disposer d’un serveur de mise à jour correspondant. Par exemple, un agent SHA peut simplement vérifier les paramètres du système local pour s’assurer qu’un pare-feu basé sur l’hôte est activé. Windows Vista et Windows XP Service Pack 3 incluent l’Agent d’intégrité des Sécurité Windows (WSHA) qui surveille les paramètres du centre d’Sécurité Windows. Les fournisseurs de logiciels tiers ou Microsoft peuvent fournir des SHA supplémentaires à la plate-forme NAP.

-   Agent NAP

    Conserve les informations d’état d’intégrité actuelles du client NAP et facilite la communication entre les couches EC et SHA NAP. L’agent NAP est fourni avec la plateforme NAP.

-   API de l’agent d’intégrité système

    Fournit un ensemble de fonctions qui permettent à Sha de s’inscrire auprès de l’agent NAP, d’indiquer l’état d’intégrité du système, de répondre aux requêtes d’état d’intégrité du système à partir de l’agent NAP et à l’agent NAP de transmettre les informations de correction de l’intégrité du système à un SHA. L’API SHA permet aux fournisseurs de créer et d’installer des SHA supplémentaires. L’API SHA est fournie avec la plateforme NAP. Consultez les interfaces NAP suivantes : [**INapSystemHealthAgentBinding2**](inapsystemhealthagentbinding2.md), [**INapSystemHealthAgentCallback**](inapsystemhealthagentcallback.md)et [**INapSystemHealthAgentRequest**](inapsystemhealthagentrequest.md).

Pour indiquer l’état d’intégrité d’un SHA spécifique, un SHA crée une déclaration d’intégrité ([**SOH**](/windows/win32/api/naptypes/ns-naptypes-soh)) et le transmet à l’agent NAP. Une SoH peut contenir un ou plusieurs éléments de l’intégrité du système. Par exemple, l’algorithme SHA pour un programme antivirus peut créer une SoH contenant l’état du logiciel antivirus en cours d’exécution sur l’ordinateur, sa version et la dernière mise à jour de signature antivirus reçue. Chaque fois qu’un algorithme SHA met à jour son état, il crée une SoH et le transmet à l’agent NAP. Pour indiquer l’état d’intégrité global d’un client NAP, l’agent NAP utilise une déclaration d’intégrité du système (SSoH), qui comprend des informations de version pour le client NAP et l’ensemble de SoHs pour l’agent d’intégrité installé.

Les sections suivantes décrivent en détail les composants de l’architecture du client NAP.

## <a name="nap-enforcement-client"></a>Client de contrainte de mise en conformité NAP

Un client de contrainte de mise en conformité NAP demande un certain niveau d’accès à un réseau, passe l’état d’intégrité de l’ordinateur à un point de contrainte de mise en conformité NAP qui fournit l’accès au réseau. Les points de contrainte de mise en conformité NAP sont des ordinateurs ou des périphériques d’accès réseau qui utilisent NAP ou peuvent être utilisés avec NAP pour exiger l’évaluation de l’état d’intégrité d’un client NAP et fournir un accès réseau ou une communication limité. Si l’intégrité de l’ordinateur n’est pas conforme, la protection d’accès réseau (EC) NAP indique l’État restreint du client NAP à d’autres composants de l’architecture du client NAP.

la protection d’accès réseau ECs pour la plateforme nap fournie dans Windows XP avec SP3, Windows Vista et Windows Server 2008 sont les suivantes :

-   IPsec NAP IPsec pour les communications protégées par IPsec.
-   Une protection d’accès réseau (NAP) EAPHost pour les connexions authentifiées par 802.1 X.
-   Un VPN NAP pour les connexions VPN d’accès à distance.
-   Une configuration d’adresse IPv4 DHCP NAP pour DHCP.
-   Une passerelle TS NAP pour les connexions de passerelle TS.

pour Windows XP avec SP3, il existe des connexions NAP et sans fil authentifiées pour 802.1 x.

### <a name="ipsec-nap-ec"></a>IPsec NAP EC

la protection d’accès réseau (EC) IPsec est un composant qui obtient l’SSoH de l’Agent nap et l’envoie à une autorité HRA, un ordinateur exécutant Windows Server 2008 et Internet Information Services (IIS) qui obtient les certificats d’intégrité d’une autorité de certification (CA) pour les ordinateurs conformes. La protection d’accès réseau IPsec EC est connue sous le nom de partie de confiance IPsec dans le composant logiciel enfichable de configuration du client NAP. Le EC IPsec NAP interagit également avec les éléments suivants :

-   Magasin de certificats pour stocker le certificat d’intégrité.
-   les composants IPsec dans Windows pour s’assurer que le certificat d’intégrité est utilisé pour la communication protégée par IPsec.
-   le pare-feu basé sur l’hôte (par exemple, Windows pare-feu) afin que le trafic protégé par IPsec soit autorisé par le pare-feu.

### <a name="eaphost-nap-ec"></a>Protection d’accès réseau EAPHost

La protection d’accès réseau (NAP) EAPHost est un composant qui obtient le SSoH à partir de l’agent NAP et l’envoie en tant que message-longueur-valeur (TLV) PEAP pour les connexions authentifiées par 802.1 X. La protection d’accès réseau (NAP) EAPHost est connue sous le nom de mise en quarantaine EAP dans le composant logiciel enfichable Configuration du client NAP.

### <a name="vpn-nap-ec"></a>VPN NAP EC

La solution de protection d’accès réseau VPN EC est fonctionnelle dans le service de gestionnaire de connexions d’accès à distance qui obtient le SSoH à partir de l’agent NAP et l’envoie en tant que message PEAP-TLV pour les connexions VPN d’accès à distance. La protection d’accès réseau VPN EC est appelée mise en quarantaine de l’accès à distance dans le composant logiciel enfichable Configuration du client NAP.

### <a name="dhcp-nap-ec"></a>PROTECTION D’ACCÈS RÉSEAU DHCP EC

La protection d’accès réseau DHCP EC est une fonctionnalité du service client DHCP qui utilise des messages DHCP standard pour échanger des messages d’intégrité du système et des informations d’accès réseau limitées. La stratégie IPsec DHCP EC est appelée mise en quarantaine DHCP EC dans le composant logiciel enfichable Configuration du client NAP. L’EC NAP DHCP obtient le SSoH à partir de l’agent NAP. Le service client DHCP fragmente le SSoH, si nécessaire, et place chaque fragment dans une option DHCP spécifique au fournisseur Microsoft, qui est envoyée dans les messages DHCPDiscover, DHCPRequest ou DHCPInform. Les messages DHCPDecline et DHCPRelease ne contiennent pas le SSoH.

## <a name="system-health-agent"></a>Agent d’intégrité système

Un agent d’intégrité système (SHA) effectue des mises à jour de l’intégrité du système et publie son état sous la forme d’une SoH auprès de l’agent NAP. L’SoH contient des informations que le serveur de stratégie de contrôle d’intégrité NAP peut utiliser pour vérifier que l’ordinateur client est dans l’état d’intégrité requis. Un SHA est mis en correspondance avec un programme de validation d’intégrité système (SHV) côté serveur de l’architecture de la plateforme NAP. Le VALIDateur correspondant peut renvoyer une réponse SoH (SoHR) au client NAP, qui est transmis par le EC NAP et l’agent NAP au SHA, en l’informant de la marche à suivre si l’agent SHA n’est pas dans un état d’intégrité requis. Par exemple, le SoHR envoyé par un programme de contrôle d’intégrité de l’antivirus peut indiquer à l’SHA antivirus correspondant d’interroger un serveur de signature antivirus pour obtenir la dernière version du fichier de signature de l’antivirus. Le SoHR peut également inclure le nom ou l’adresse IP du serveur de signature antivirus à interroger.

Un agent SHA peut utiliser un client de stratégie installé localement pour faciliter les fonctions de gestion de l’intégrité du système avec un serveur de stratégie. Par exemple, une mise à jour logicielle SHA peut utiliser le logiciel client installé localement (le client de stratégie) pour effectuer la vérification de version et l’installation et la mise à jour des fonctions avec le serveur de mises à jour logicielles (le serveur de stratégie).

## <a name="nap-agent"></a>Agent NAP

L’agent NAP fournit les services suivants :

-   Collecte les SoHs à partir de chaque SHA et les met en cache. Le cache SoH est mis à jour chaque fois qu’un agent SHA fournit une SoH nouvelle ou mise à jour.
-   Stocke le SSoH et le fournit à NAP ECs à la demande.
-   Transmet des notifications à Sha lorsque l’État restreint change.
-   Conserve l’État restreint du système et collecte des informations d’État à partir de chaque SHA.
-   Passe SoHRs à l’algorithme SHA approprié.

 

 




