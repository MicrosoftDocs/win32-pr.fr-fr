---
title: Vue d’ensemble de l’architecture UPnP
description: L’architecture UPnP définit la connectivité de réseau pair à pair des appareils, appareils et points de contrôle intelligents.
ms.assetid: 09aba033-6229-4a55-9421-a7b967508bf4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5866d3e701f53e95225538655ca45d159fb7c5f67d00e3c46c97357c7a9ee6a7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118126452"
---
# <a name="overview-of-upnp-architecture"></a>Vue d’ensemble de l’architecture UPnP

L’architecture UPnP définit la connectivité de réseau pair à pair des appareils, appareils et points de [*contrôle*](c-gly.md)intelligents. Il est conçu pour offrir une connectivité facile à utiliser, flexible et basée sur des normes aux réseaux ad hoc, gérés ou non gérés, que ces réseaux soient à la base, les petites entreprises ou directement connectés à Internet. L’architecture UPnP est une architecture de mise en réseau distribuée et ouverte qui utilise les technologies TCP/IP et Web existantes pour activer la mise en réseau de proximité transparente, en plus du contrôle et du transfert de données entre les appareils en réseau.

UPnP est une suite de protocoles basés sur IP basée sur des versions préliminaires de protocoles de services Web tels que XML et SOAP (Simple Object Access Protocol). Avec UPnP, un appareil peut rejoindre un réseau de manière dynamique, obtenir une adresse IP, transmettre ses fonctionnalités et découvrir la présence et les fonctionnalités d’autres appareils sur le réseau.

Un périphérique UPnP est un conteneur de services et d’appareils imbriqués. Par exemple, un magnétoscope peut se composer d’un service de transport de bande, d’un service de tuner et d’un service horloge. Différentes catégories d’appareils UPnP sont associées à différents ensembles de services et périphériques intégrés. Par exemple, les services d’un magnétoscope sont différents de ceux d’une imprimante. Les informations relatives à l’ensemble de services qu’un type d’appareil particulier peut fournir sont capturées dans un document de description de périphérique XML que l’appareil héberge. La description de l’appareil répertorie également les propriétés telles que le nom de l’appareil et les icônes associées à l’appareil. Microsoft a amélioré la prise en charge d’UPnP pour inclure l’intégration avec [PnP-X](/previous-versions/windows/desktop/fundisc/pnp-x) et la [découverte de fonction](/previous-versions/windows/desktop/fundisc/fd-portal).

L’architecture UPnP est plus qu’une simple extension du modèle de périphérique Plug-and-Play. Il prend en charge la configuration automatique, la mise en réseau invisible et la découverte automatique pour une gamme de catégories d’appareils d’un large éventail de fournisseurs. Cela permet à un appareil de joindre dynamiquement un réseau, d’obtenir une adresse IP et de transmettre ses fonctionnalités à la demande. Ensuite, les autres points de contrôle peuvent utiliser l’API de point de contrôle avec la technologie UPnP pour en savoir plus sur la présence et les fonctionnalités d’autres périphériques. Un appareil peut conserver un réseau en douceur et automatiquement lorsqu’il n’est plus utilisé.

Qu’est-ce que la technologie UPnP ?

-   Indépendance des supports et des appareils. La technologie UPnP peut s’exécuter sur n’importe quel support, notamment ligne téléphonique, alimentation, Ethernet, RF et 1394.
-   Indépendance de la plateforme. Les fournisseurs utilisent n’importe quel système d’exploitation et n’importe quel langage de programmation pour créer des produits basés sur UPnP.
-   Technologies basées sur Internet. La technologie UPnP est basée sur IP, TCP, UDP, HTTP et XML, entre autres.
-   Contrôle d’interface utilisateur. L’architecture UPnP permet au fournisseur de contrôle sur l’interface utilisateur de l’appareil et l’interaction à l’aide du navigateur.
-   Contrôle par programmation. L’architecture UPnP active également le contrôle par programmation des applications conventionnels.
-   Protocoles de base courants. Les fournisseurs s’accordent sur des ensembles de protocoles de base sur la base de chaque appareil.
-   Extensible. Chaque produit basé sur UPnP peut avoir des services à valeur ajoutée superposés sur l’architecture d’appareil de base de chaque fabricant.

La technologie UPnP est étendue en ce sens qu’elle cible les réseaux familiaux, les réseaux de proximité et les réseaux des petites entreprises et des bâtiments commerciaux. Il permet la communication de données entre deux appareils sous la commande de n’importe quel périphérique de contrôle sur le réseau. La technologie UPnP est indépendante de tout système d’exploitation, langage de programmation ou support physique particulier.

Microsoft fournit deux API pour travailler avec des appareils basés sur UPnP :

-   [API du point de contrôle](control-point-api.md) : fournit un ensemble d’interfaces COM qui permettent aux applications de rechercher et de contrôler les périphériques UPnP.
-   [API](device-host-api.md) de l’hôte de périphérique : fournit un ensemble d’interfaces COM qui permettent aux développeurs d’écrire les fonctionnalités principales des appareils et d’inscrire l’appareil auprès de l’hôte de l’appareil. L’hôte d’appareil gère la découverte, la description, le contrôle et les parties d’événements des fonctionnalités d’appareil UPnP.

 

 