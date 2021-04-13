---
description: À propos de VDS
ms.assetid: b2f7628c-b567-40a9-9ad7-6c47077af5fb
title: À propos de VDS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 911145fda8f2dd63c886530af3d8507c38d8e829
ms.sourcegitcommit: 37f276b5d887a3aad04b1ba86e390dea9d87e591
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/04/2021
ms.locfileid: "104568277"
---
# <a name="about-vds"></a>À propos de VDS

\[À compter de Windows 8 et de Windows Server 2012, l’interface com du [service de disque virtuel](virtual-disk-service-portal.md) est remplacée par l' [API de gestion de stockage Windows](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]

Le service de disque virtuel est un service Microsoft Windows qui effectue des opérations de requête et de configuration à la demande des utilisateurs finaux, des scripts et des applications. Le service étend les fonctionnalités de stockage existantes des systèmes d’exploitation Windows Server des manières suivantes :

-   Fournit une API aux fonctionnalités existantes de gestion des volumes et des disques dans Windows.
-   Unifie la gestion des volumes et le matériel redondant de gestion des disques indépendants (RAID) sous une seule API.

VDS n’effectue pas les activités de gestion du stockage suivantes :

-   Gestion du sous-système matériel, telle que la surveillance de la température ou la surveillance des statistiques de performances pour les baies de disques.
-   Gestion de la structure du réseau de zone de stockage (SAN, Storage Area Network), telle que la sécurité et le zonage de l’adaptateur de Host-Based (HBA).

Les sections qui suivent décrivent l’architecture de VDS, le rôle des fournisseurs VDS et l’API.

## <a name="service-architecture"></a>Architecture de service

VDS définit trois interfaces : une interface unique entre la couche application et le service, ainsi que deux interfaces entre le service et les programmes fournisseurs de la couche données. L’illustration suivante montre les limites d’application à service et de service à fournisseur.

![Diagramme illustrant l’architecture de service divisée en sections « applications », « service de disque virtuel » et « fournisseurs VDS ».](images/vdsoverview.png)

L’architecture multiniveau permet à VDS de coordonner les fonctions du système de fichiers, de synchroniser les activités du fournisseur et d’arbitrer les applications. Étant donné qu’il s’agit d’une application et d’un fournisseur, VDS présente des fonctionnalités uniformes aux applications, même si certains des fournisseurs sous-jacents peuvent manquer d’uniformité.

Le service implémente des fonctionnalités communes : la mise en forme des volumes, l’ajout et la suppression de lettres de lecteur ou de dossiers montés, ainsi que la gestion des disques non alloués, c’est-à-dire des disques sans informations de partition. VDS retourne également les notifications d’événements aux applications inscrites. Pour plus d’informations, consultez [notifications VDS](vds-notification-model.md).

## <a name="role-of-providers"></a>Rôle des fournisseurs

VDS définit deux interfaces de fournisseur, une pour un fournisseur de logiciels et une pour un fournisseur de matériel. Chaque fournisseur implémente une partie différente de l’API définie par VDS :

-   Un *fournisseur de logiciels* est un programme basé sur l’hôte qui est pris en charge par un pilote en mode noyau dans la pile d’e/s de stockage. Le runtime du fournisseur-noyau interagit avec le gestionnaire de montage au moment du démarrage ou le gestionnaire de Plug-and-Play (PnP) au moment de la détection pour revendiquer chaque disque. Les fournisseurs de logiciels fonctionnent sur les volumes, les disques et les partitions de disque.

    VDS comprend deux types de fournisseurs. Le fournisseur de logiciels de base gère les disques de base et n’offre aucune liaison tolérante aux pannes. Le fournisseur de logiciels dynamique gère les disques dynamiques et offre une gestion des erreurs, le cas échéant. Le comportement du fournisseur de logiciels est cohérent avec le comportement des disques de base et dynamiques sur l’ordinateur hôte. Par exemple, si le système d’exploitation d’un hôte donné prend en charge les disques dynamiques à tolérance de pannes, VDS prend également en charge ce comportement sur l’ordinateur hôte.

-   Un *fournisseur de matériel* implémente les méthodes utilisées pour gérer un sous-système de stockage (une baie de disques ou une carte d’adaptateur de disque) qui permet la création de disques logiques configurés pour améliorer les performances, la disponibilité des données ou la récupération des données. De nombreux fabricants d’armoires RAID majeurs ont créé un fournisseur de matériel conçu pour être utilisé avec VDS. Les consommateurs de services doivent obtenir un fournisseur de matériel et le matériel associé auprès du fabricant.

    Les fonctionnalités d’un fournisseur de matériel dépendent des capacités du matériel sous-jacent. Par conséquent, le degré de mise en œuvre de l’API par chaque fabricant peut varier. Par exemple, les fabricants peuvent inclure des méthodes supplémentaires pour optimiser les configurations, surveiller et ajuster dynamiquement les performances, automatiser la gestion des erreurs ou fournir d’autres fonctionnalités intéressantes.

    Les fournisseurs de matériel offrent plusieurs options de configuration qui ne sont pas disponibles pour les fournisseurs de logiciels. La plupart des notables est le modèle de configuration automagic, qui présente une vue basée sur les attributs du stockage pour chaque application. Les indicateurs de liaison, tels que « en lecture seule » ou « récupération rapide après incident requise », remplacent la complexité de la liaison du stockage physique au stockage virtuel. Chaque fournisseur de matériel effectue le mappage d’étendue, l’allocation d’espace et la sélection de type de liaison en fonction des indicateurs qui sont envoyés par une application. Pour obtenir la description complète du fournisseur de matériel, y compris les options de configuration, consultez la documentation fournie par le fabricant du sous-système.

## <a name="application-programming-interface"></a>Interface de programmation d’applications

Les applications peuvent appeler des méthodes VDS pour interroger et configurer les disques basés sur l’hôte, le stockage RAID, ou les deux. Pour obtenir une vue d’ensemble de l’API, consultez le [modèle d’objet VDS](vds-object-model.md).

Les applications classiques pour VDS résolvent les problèmes de gestion et de surveillance de la configuration, et vont des systèmes de gestion de stockage dédiés aux applications Back Office qui recherchent un meilleur contrôle de la configuration ou de la gestion des erreurs. Les applications suivantes utilisent VDS aujourd’hui :

-   Le composant logiciel enfichable Gestion des disques configure et gère les disques contrôlés par un ordinateur hôte. Les administrateurs système et les utilisateurs finaux peuvent interroger et configurer des disques et des volumes locaux (ou distants) à l’aide de cet outil de l’interface utilisateur.
-   Diskpart.exe est un utilitaire de ligne de commande qui configure et gère les disques, les volumes et les partitions.
-   Diskraid.exe est un utilitaire de ligne de commande qui configure et gère les sous-systèmes matériels RAID. Cet utilitaire peut interagir avec tout matériel de stockage qui est accompagné d’un fournisseur de matériel VDS.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Service Disque virtuel](virtual-disk-service-portal.md)
</dt> <dt>

[Notifications VDS](vds-notification-model.md)
</dt> <dt>

[Modèle d’objet VDS](vds-object-model.md)
</dt> </dl>

 

 
