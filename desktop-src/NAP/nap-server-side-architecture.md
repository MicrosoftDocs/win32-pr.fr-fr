---
title: Architecture côté serveur NAP
description: Architecture côté serveur NAP
ms.assetid: b05c52d5-1f90-41d4-a540-d20e70e54bcb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 82f5921cd6b2dc7ebbff06b357775677eaae2305475752b6ea92e33ad7afd390
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117799005"
---
# <a name="nap-server-side-architecture"></a>Architecture côté serveur NAP

> [!Note]  
> La plate-forme de protection d’accès réseau n’est pas disponible à partir de Windows 10

 

l’architecture de la plateforme côté serveur NAP utilise des ordinateurs exécutant Windows server 2008. la figure suivante illustre l’architecture de la prise en charge côté serveur de la plateforme nap, composée de points de contrainte de mise en conformité nap basés sur des Windows et d’un serveur de stratégie de contrôle d’intégrité nap.

![architecture de la prise en charge côté serveur de la plateforme NAP](images/nap-server-side-arch.png)

un point de contrainte de mise en conformité nap basé sur des Windows possède une couche de composants de serveur de contrainte de mise en conformité nap. Chaque NAP ES est défini pour un autre type d’accès réseau ou de communication. Par exemple, il existe une protection NAP ES pour les connexions VPN d’accès à distance et une NAP pour la configuration DHCP. La protection NAP ES correspond généralement à un type spécifique de client compatible NAP. Par exemple, les NAP ES DHCP sont conçus pour fonctionner avec un client de contrainte de mise en conformité NAP basé sur DHCP. Les fournisseurs de logiciels tiers ou Microsoft peuvent fournir une protection d’accès réseau supplémentaire NAP pour la plateforme NAP. Une protection d’accès réseau (NAP) obtient la déclaration d’intégrité du système (SSoH) à partir de la EC NAP correspondante et l’envoie à un serveur de stratégie de contrôle d’intégrité NAP en tant qu’attribut spécifique du fournisseur RADIUS (Remote Authentication Dial-in User Service) du [message radius Access-Request](https://www.ietf.org/rfc/rfc2865.txt?number=2865)

Comme indiqué dans l’illustration de l’architecture côté serveur, le serveur de stratégie d’intégrité NAP comporte les composants suivants :

-   Service NPS (Network Policy Server)

    Reçoit le message de Access-Request RADIUS, extrait le SSoH et le transmet au composant serveur d’administration NAP. le service NPS est fourni avec Windows Server 2008.

-   Serveur d’administration NAP

    Facilite la communication entre le service NPS et les programmes de validation d’intégrité système (SHV). Le composant serveur d’administration NAP est fourni avec la plateforme NAP.

-   Une couche de composants SHV

    Chaque SHV est défini pour un ou plusieurs types d’informations sur l’intégrité du système et peut être mis en correspondance avec un SHA. Par exemple, il peut y avoir un SHV pour un programme antivirus. Un VALIDateur peut être mis en correspondance avec un ou plusieurs serveurs d’exigence d’intégrité. Par exemple, un programme SHV de vérification des signatures antivirus est mis en correspondance avec le serveur qui contient le dernier fichier de signature. Les programmes de validation d’intégrité système n’ont pas besoin d’avoir un serveur d’exigence d’intégrité correspondant. Un SHV peut simplement indiquer aux clients compatibles NAP de vérifier les paramètres du système local pour s’assurer qu’un pare-feu basé sur l’hôte est activé. Windows le serveur 2008 comprend le programme de validation d’intégrité Sécurité Windows (WSHV). Des programmes de validation d’intégrité système supplémentaires sont fournis par des éditeurs de logiciels tiers ou par Microsoft en tant que composants additionnels à la plateforme NAP.

-   API SHV

    Fournit un ensemble d’appels de fonction qui autorisent les validateurs d’inscription auprès du composant serveur d’administration NAP, reçoivent les déclarations d’intégrité (SoHs) du composant serveur d’administration NAP et envoient des réponses de déclaration d’intégrité (SoHRs) au composant serveur d’administration NAP. L’API SHV est fournie avec la plateforme NAP. Consultez les interfaces NAP suivantes : [**INapSystemHealthValidator**](inapsystemhealthvalidator.md) et [**INapSystemHealthValidationRequest**](inapsystemhealthvalidationrequest.md).

Comme décrit précédemment, la configuration la plus courante pour l’infrastructure côté serveur NAP est constituée de points de contrainte de mise en conformité NAP qui fournissent l’accès au réseau ou la communication d’un type spécifique et des serveurs de stratégie de contrôle d’intégrité NPS distincts qui assurent la validation et la correction de l’intégrité du système. il est possible d’installer le service NPS en tant que serveur de stratégie d’intégrité nap sur des points de contrainte de mise en conformité nap basés sur des Windows individuels. Toutefois, dans cette configuration, chaque point de contrainte de mise en conformité NAP doit ensuite être configuré séparément avec l’accès réseau et les stratégies de contrôle d’intégrité. La configuration recommandée consiste à utiliser des serveurs de stratégie de contrôle d’intégrité NAP distincts.

L’architecture globale de la protection d’accès réseau se compose des ensembles de composants suivants :

-   Les trois composants clients NAP (une couche SHA, l’agent NAP et une couche EC NAP).
-   les quatre composants côté serveur nap (une couche SHV, le serveur d’Administration nap, le service NPS et une couche nap ES sur les points de contrainte de mise en conformité nap basés sur Windows).
-   Serveurs de stratégie de contrôle d’intégrité, qui sont des ordinateurs qui peuvent fournir des spécifications d’intégrité du système actuelles pour les serveurs de stratégie de contrôle d’intégrité NAP.
-   Serveurs de mise à jour, qui sont des ordinateurs qui contiennent des ressources de mise à jour d’intégrité auxquelles les clients NAP peuvent accéder pour corriger leur état non conforme.

L’illustration suivante montre les relations entre les composants de la plateforme NAP.

![relations entre les composants de la plateforme NAP](images/nap-components.png)

Notez la correspondance des jeux de composants suivants :

-   NAP et ESs NAP sont généralement mis en correspondance.

    Par exemple, la protection d’accès réseau DHCP EC sur le client NAP est mise en correspondance avec les NAP DHCP sur le serveur DHCP.

-   SHA et les serveurs de mise à jour peuvent être mis en correspondance.

    Par exemple, un SHA antivirus sur le client est mis en correspondance avec un serveur de mise à jour de signature antivirus.

-   Vous pouvez mettre en correspondance les validateurs d’intégrité et les serveurs d’exigence d’intégrité.

    Par exemple, un programme d’intégrité des logiciels antivirus sur le serveur de stratégie de contrôle d’intégrité NAP peut être mis en correspondance avec un serveur d’exigence d’intégrité antivirus.

Les éditeurs de logiciels tiers peuvent étendre la plateforme NAP des manières suivantes :

-   Créez une nouvelle méthode par laquelle l’intégrité d’un client NAP est évaluée.

    Les fournisseurs de logiciels tiers doivent créer un SHA pour le client NAP, un SHV pour le serveur de stratégie de contrôle d’intégrité NAP et, si nécessaire, des spécifications d’intégrité et des serveurs de mise à jour. Si l’exigence d’intégrité ou les serveurs de mise à jour existent déjà, par exemple un serveur de distribution de signature antivirus, seuls les composants SHA et SHV correspondants doivent être créés. Dans certains cas, les spécifications d’intégrité ou les serveurs de mise à jour ne sont pas nécessaires.

-   Créez une nouvelle méthode pour appliquer les exigences d’intégrité pour l’accès réseau ou la communication.

    Les fournisseurs de logiciels tiers doivent créer une protection d’accès réseau (EC) NAP sur le client NAP. si la méthode de mise en œuvre utilise un service Windows, les fournisseurs de logiciels tiers doivent créer des NAP correspondants qui communiquent avec un serveur de stratégie d’intégrité nap à l’aide du protocole radius ou à l’aide du service NPS installé sur le point de contrainte de mise en conformité nap en tant que proxy radius.

Les sections suivantes décrivent en détail les composants de l’architecture côté serveur NAP.

## <a name="nap-enforcement-server"></a>Serveur de contrainte de mise en conformité NAP

Un serveur de contrainte de mise en conformité NAP autorise un certain niveau d’accès réseau ou de communication, peut passer l’état d’intégrité d’un client NAP au serveur de stratégie de contrôle d’intégrité réseau pour l’évaluation et, en fonction de la réponse, peut fournir l’application d’un accès limité au réseau.

l’ESs NAP inclus avec Windows Server 2008 est le suivant :

-   Une protection d’accès réseau (NAP) IPsec pour les communications protégées par IPsec.

    pour les communications protégées par IPsec, l’autorité HRA, un ordinateur exécutant Windows Server 2008 et Internet Information Services (IIS) qui obtient les certificats d’intégrité d’une autorité de certification pour les ordinateurs conformes, transmet les informations d’état d’intégrité du client nap au serveur de stratégie de contrôle d’intégrité nap.

-   Une protection d’accès réseau (NAP) DHCP pour la configuration d’adresse IP basée sur DHCP.

    La protection d’accès réseau DHCP ES est une fonctionnalité du service serveur DHCP qui utilise des messages DHCP standard pour communiquer avec la protection d’accès réseau DHCP EC sur un client NAP. La contrainte de mise en conformité DHCP pour un accès limité au réseau est effectuée par le biais des options DHCP.

-   Une passerelle des services Terminal Server NAP ES pour les connexions basées sur un serveur de passerelle TS.

Pour les connexions VPN d’accès à distance et authentifiées par 802.1 X, la fonctionnalité du service NPS utilise des messages PEAP-TLV entre les clients NAP et le serveur de stratégie de contrôle d’intégrité NAP. La contrainte de mise en conformité VPN s’effectue via des filtres de paquets IP appliqués à la connexion VPN. l’application de 802.1 x est effectuée au niveau de l’appareil d’accès réseau 802.1 X en appliquant des filtres de paquets IP à la connexion ou en affectant à la connexion un ID de réseau local virtuel correspondant au réseau restreint.

## <a name="nap-administration-server"></a>Serveur d’administration NAP

Le composant serveur d’administration NAP fournit les services suivants :

-   Obtient le SSoHs à partir des NAP par le biais du service NPS.
-   Distribue le SoHs dans le SSoHs aux validateurs d’intégrité du système (SHV) appropriés.
-   Collecte des SoHRs à partir des validateurs d’intégrité du système et les transmet au service NPS à des fins d’évaluation.

## <a name="nps-service"></a>Service NPS

RADIUS est un protocole largement déployé qui permet l’authentification, l’autorisation et la comptabilité centralisées pour l’accès réseau qui est décrite dans les RFC 2865 et 2866. Développé à l’origine pour l’accès à distance, RADIUS est désormais pris en charge par les points d’accès sans fil, les commutateurs Ethernet d’authentification, les serveurs VPN, les serveurs d’accès DSL (Digital Subscriber Line) et d’autres serveurs d’accès réseau.

NPS est l’implémentation d’un serveur et d’un proxy RADIUS dans Windows server 2008. le serveur NPS remplace le service d’authentification Internet (IAS) dans Windows Server 2003. Pour la plateforme NAP, le service NPS comprend le composant serveur d’administration NAP, la prise en charge de l’API SHV et des validateurs d’intégrité du système, ainsi que les options de configuration des stratégies de contrôle d’intégrité.

En fonction du SoHRs des validateurs d’intégrité et des stratégies de contrôle d’intégrité configurées, le service NPS crée une réponse de déclaration d’intégrité système (SSoHR), qui indique si le client NAP est conforme ou non conforme et comprend l’ensemble des SoHRs des validateurs d’intégrité.

## <a name="system-health-validator-shv"></a>Programme de validation d’intégrité système (SHV)

Un SHV reçoit une SoH du serveur d’administration NAP et compare les informations d’état d’intégrité du système avec l’état d’intégrité du système requis. Par exemple, si la SoH provient d’un SHA antivirus et contient le numéro de version du dernier fichier de signature de virus, le programme de validation d’intégrité des virus correspondant peut vérifier le numéro de version le plus récent auprès du serveur d’impératifs d’intégrité antivirus pour valider l’SoH du client NAP.

Le SHV renvoie un SoHR au serveur d’administration NAP. Le SoHR peut contenir des informations sur la façon dont l’algorithme SHA correspondant sur le client NAP peut répondre aux exigences actuelles en matière d’intégrité du système. Par exemple, le SoHR envoyé par le programme de contrôle d’intégrité de l’antivirus peut indiquer à l’antivirus SHA sur le client NAP de demander la dernière version du fichier de signature antivirus à un serveur de signature antivirus spécifique par son nom ou son adresse IP.

 

 




