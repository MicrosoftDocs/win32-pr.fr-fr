---
description: l’API WSDAPI (web Service on devices) est une implémentation du profil de périphériques pour les Services web (DPWS) pour Windows Vista et Windows Server 2008.
ms.assetid: 8eaeacb3-43db-4a57-8548-e5b81213269c
title: À propos des services Web sur les appareils
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dca7f7dc97dabd3dde7af12f3cece992b4f0ef6d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127216660"
---
# <a name="about-web-services-on-devices"></a>À propos des services Web sur les appareils

l’API WSDAPI (web Service on devices) est une implémentation du [profil de périphériques pour les Services web](https://specs.xmlsoap.org/ws/2006/02/devprof/) (DPWS) pour Windows Vista et Windows Server 2008. Le DPWS limite les spécifications de services Web afin que les clients puissent facilement découvrir des appareils. Une fois qu’un appareil est découvert, un client peut récupérer une description des services hébergés sur cet appareil et utiliser ces services.

## <a name="devices-and-services"></a>Appareils et services

Les *appareils* sont des composants, généralement des matériels, qui sont connectés au réseau. Les exemples incluent les imprimantes, les caméras Web et les systèmes vidéo.

Les appareils peuvent inclure zéro ou plusieurs *services*. Par exemple, un périphérique vidéo peut inclure des services qui prennent en charge l’alimentation et la désactivation, le contrôle de lecture, l’éjection de support et la diffusion vidéo. Le contrôle Play peut prendre en charge des actions telles que la lecture, l’interruption, le rembobinage et l’avance rapide.

## <a name="discovering-and-manipulating-a-device"></a>Découverte et manipulation d’un appareil

WSDAPI étend le modèle de Plug-and-Play local en permettant à un client de découvrir et d’accéder à un appareil distant et à ses services associés sur un réseau. Il prend en charge la découverte, la messagerie de contrôle unidirectionnelle et bidirectionnelle et l’événement.

![Diagramme montrant comment WSDAPI permet à un client de découvrir et d’accéder à un appareil distant.](images/overview01.png)

Les appareils DPWS annoncent leur présence et exposent les services (le cas échéant) à l’aide d’une adresse unique et d’un ensemble standardisé de messages XML. Les clients DPWS peuvent utiliser le processus de découverte pour Rechercher l’appareil, énumérer ses services et se connecter à ces services pour effectuer des actions spécifiques.

Un client WSDAPI interroge d’abord l’appareil pour obtenir une description complète de ses services, y compris les types de service (par exemple, un type de service d’imprimante ou un type de service de scanneur). Le client contrôle ensuite l’appareil en appelant des commandes définies par un type de service (par exemple, en appelant **CreatePrintJob** sur un appareil avec un type de service d’imprimante). Le cas échéant, le client peut également surveiller les modifications d’État dans chaque service en s’abonnant aux événements qui se produisent pendant l’exécution de la commande.

![Diagramme montrant comment un client WSDAPI interroge et interagit avec un appareil.](images/netdevice01.png)

pour plus d’informations sur les modèles de messagerie des appareils, consultez [découverte et métadonnées Exchange modèles de Message](discovery-and-metadata-exchange-message-patterns.md).

## <a name="logical-and-physical-addressing"></a>Adressage logique et physique

L’adressage logique est utilisé pour identifier de manière unique les périphériques indépendamment de leurs adresses physiques. WS-Discovery fournit un mécanisme permettant de résoudre les adresses logiques en adresses physiques, ce qui permet à la messagerie client-appareil d’avoir lieu. Par exemple, le stockage NAS (Network Attached Storage) que vous suivez. Si vous avez un ordinateur portable et un NAS, votre ordinateur portable doit être en mesure de reconnaître qu’il s’agit du même appareil, quelle que soit l’adresse physique (adresse IP) obtenue par le NAS au fur et à mesure que vous passez d’un sous-réseau à un autre. Pour ce faire, l’appareil doit avoir une identité indépendante de l’adresse IP qu’il obtient ; étant donné que les mécanismes traditionnels tels que DNS ne sont pas disponibles dans un scénario d’itinérance normal, WS-Addressing et WS-Discovery fournir l’adressage logique et la résolution comme une alternative ad hoc.

Lorsqu’un appareil est fabriqué, il reçoit un identificateur global unique, représenté sous la forme d’un URI UUID. Cet identificateur ne changera jamais pour l’appareil. Lorsque l’appareil est sous tension, il annonce toujours son adresse logique par le biais d’un message WS-Discovery [Hello](hello-message.md) , et accepte les demandes de conversion en adresse physique (en général http) via WS-Discovery de [résoudre](resolve-message.md) ou de [sonder](probe-message.md) les messages. Une fois qu’une adresse physique valide (adresse IP) est obtenue, toute la messagerie se produit au-dessus de cette adresse, et WS-Discovery est utilisé uniquement si l’adresse change, lorsque l’appareil change d’État et que les clients doivent être avertis ou lorsque l’appareil est mis hors connexion.

## <a name="building-applications"></a>Création d’applications

WSDAPI fournit une pile SOAP DPWS générique pour une utilisation par les applications clientes et de service. Le [Générateur de code des services Web sur les appareils](web-services-for-devices-code-generator.md) (WsdCodeGen.exe) peut être utilisé pour convertir une description de service (WSDL) en code proxy et stub que les applications peuvent appeler directement. Ce code généré transforme automatiquement les appels et les paramètres de fonction en messages SOAP et en champs XML, puis appelle WSDAPI pour émettre des requêtes vers le périphérique ou le client distant.

La découverte des fonctions peut être utilisée lors de la génération d’applications WSDAPI pour créer et activer des instances de fonction retournées par PnP. Ces instances de fonction contiennent des données qui peuvent être utilisées pour obtenir plus d’informations par le biais des API PnP quand une simple découverte est nécessaire. Pour plus d’informations, consultez [découverte de fonctions](/previous-versions/windows/desktop/fundisc/fd-portal) et [PnP-X](/previous-versions/windows/desktop/fundisc/pnp-x).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[détection et schémas de Message Exchange de métadonnées](discovery-and-metadata-exchange-message-patterns.md)
</dt> <dt>

[Conformité de la spécification WSDAPI](wsdapi-specification-compliance.md)
</dt> <dt>

[Vue d’ensemble des interfaces WSDAPI](overview-of-the-wsdapi-interfaces.md)
</dt> </dl>

 

 
