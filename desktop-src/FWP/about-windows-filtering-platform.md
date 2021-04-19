---
title: À propos de la plateforme de filtrage Windows
description: La plateforme de filtrage Windows (WFP) est une plateforme de traitement du trafic réseau conçue pour remplacer les interfaces de filtrage du trafic réseau Windows XP et Windows Server 2003.
ms.assetid: 6faad008-b2f6-4f45-89c7-ae98c2f58ce1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3ab259eca1da714bbeb8d4ea556e69513f33514c
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "106538594"
---
# <a name="about-windows-filtering-platform"></a>À propos de la plateforme de filtrage Windows

La plateforme de filtrage Windows (WFP) est une plateforme de traitement du trafic réseau conçue pour remplacer les interfaces de filtrage du trafic réseau Windows XP et Windows Server 2003. La plateforme WFP se compose d’un ensemble de raccordements dans la pile réseau et d’un moteur de filtrage qui coordonne les interactions entre les piles réseau.

## <a name="the-wfp-components"></a>Composants WFP

### <a name="filter-engine"></a>Moteur de filtre

L’infrastructure de filtrage multicouche de base, hébergée en mode noyau et en mode utilisateur, qui remplace les modules de filtrage multiples dans le sous-système de mise en réseau Windows XP et Windows Server 2003.

-   Filtre le trafic réseau sur n’importe quelle couche du système sur tous les champs de données qu’un shim peut fournir.
-   Implémente les filtres de « légende » en appelant des légendes pendant la classification.
-   Retourne des actions « autoriser » ou « bloquer » au shim qui l’a appelée pour la mise en application.
-   Fournit un arbitrage entre différentes sources de stratégie. Par exemple, détermine la priorité lorsqu’une application est configurée pour sécuriser tout le trafic réseau qui lui est associé, mais que le pare-feu local est configuré pour empêcher le trafic sécurisé des applications.<br/>

### <a name="base-filtering-engine-bfe"></a>Moteur de filtrage de base (BFE)

Service qui contrôle le fonctionnement de la plateforme de filtrage Windows. Il effectue les tâches suivantes.

-   Accepte des filtres et d’autres paramètres de configuration pour la plateforme.
-   Indique l’état actuel du système, y compris les statistiques.
-   Applique le modèle de sécurité pour accepter la configuration dans la plateforme. Par exemple, un administrateur local peut ajouter des filtres, mais les autres utilisateurs peuvent uniquement les afficher.<br/>
-   Raccorde les paramètres de configuration à d’autres modules dans le système. Par exemple, les stratégies de négociation IPsec accèdent aux modules de génération de clés IKE/AuthIP, les filtres sont dirigés vers le moteur de filtre.<br/>

### <a name="shims"></a>Shims

Composants en mode noyau qui résident entre la pile réseau et le moteur de filtre. Les shims assurent la décision de filtrage en classant par rapport au moteur de filtre. La liste suivante répertorie les shims disponibles.

-   Shim de mise en application de la couche application (ALE).
-   Shim de module de couche de transport.
-   Shim du module de couche réseau.
-   Shim d’erreur ICMP (Internet Control Message Protocol).
-   Ignorer le shim.
-   Shim de flux.

### <a name="callouts"></a>Légendes

Ensemble de fonctions exposées par un pilote et utilisées pour le filtrage spécialisé. Outre les actions de base de « autoriser » et « bloquer », les légendes peuvent modifier et sécuriser le trafic réseau entrant et sortant. Pour plus d’informations sur les légendes, consultez la rubrique [pilotes Windows de la plateforme de filtrage Windows](/windows-hardware/drivers/network/windows-filtering-platform-callout-drivers2) dans la documentation du kit de pilotes Windows (WDK). WFP fournit des légendes intégrées qui effectuent les tâches suivantes.<br/>

-   Effectuer le traitement IPsec.
-   Ajuster le comportement de filtrage avec état.
-   Effectue le filtrage en mode furtif (suppression silencieuse des paquets qui n’ont pas été demandés).
-   Contrôlez le déchargement TCP Chimney.
-   Interagissez avec le service Teredo.

<br/> Le moteur de filtre permet aux légendes tierces de s’inscrire à chacune de ses couches en mode noyau.<br/>

### <a name="application-programming-interface"></a>Interface de programmation d’applications

Ensemble de types de données et de fonctions accessibles aux développeurs pour créer et gérer des applications de filtrage réseau. Ces types de données et fonctions sont regroupés en plusieurs [ensembles d’API](api-sets.md).

## <a name="wfp-features"></a>Fonctionnalités WFP

-   Fournit une infrastructure de filtrage de paquets dans laquelle les éditeurs de logiciels indépendants (ISV) peuvent intégrer des modules de filtrage spécialisés.
-   Fonctionne avec IPv4 et IPv6.
-   Permet le filtrage, la modification et la réinjection des données.
-   Effectue le traitement des paquets et du flux.
-   Autorise l’activation du filtrage des paquets par application, par utilisateur et par connexion en plus de par interface réseau ou par port.
-   Fournit la sécurité au moment du démarrage jusqu’au démarrage du moteur de filtrage de base (BFE).
-   Active le filtrage avec état des connexions.
-   Gère à la fois les données chiffrées avant et après IPsec.
-   Permet l’intégration des stratégies IPsec et de filtrage du pare-feu.
-   Fournit une infrastructure de gestion des stratégies pour déterminer quand des filtres spécifiques doivent être activés. Cela comprend la médiation des exigences conflictuelles à partir de plusieurs filtres fournis par différents fournisseurs.
-   Gère la plupart du réassemblage de paquets et du suivi de l’État.
-   Comprend un système de notification utilisateur générique qui informe les abonnés des modifications apportées au système de filtrage.
-   Implémente des fonctions d’énumération qui signalent l’état du système.
-   Utilise les événements net pour enregistrer les erreurs IPsec et les rejets de paquets.
-   Prend en charge une [classe d’assistance NDF (](/windows/desktop/NDF/extensible-helper-classes)Network Diagnostics Framework).
-   Prend en charge les [extensions de socket sécurisées](/windows/desktop/WinSock/winsock-secure-socket-extensions) pour l’API Winsock, qui permettent aux applications réseau de sécuriser leur trafic en configurant WFP.
-   Au niveau des couches de mise en application de la couche d’application (ALE), a un impact minimal sur les performances du réseau en traitant uniquement le premier paquet dans une connexion.
-   Intègre le déchargement matériel où les modules de légende en mode noyau peuvent utiliser le matériel pour effectuer une inspection de paquets spécifique.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Architecture WFP](windows-filtering-platform-architecture-overview.md)
</dt> <dt>

[Opération WFP](basic-operation.md)
</dt> <dt>

[Application de la couche application (ALE)](application-layer-enforcement--ale-.md)
</dt> <dt>

[Configuration IPsec](ipsec-configuration.md)
</dt> <dt>

[Configuration de WFP](wfp-configuration.md)
</dt> <dt>

[Surveillance de WFP](wfp-monitoring.md)
</dt> <dt>

[API WFP](api-sets.md)
</dt> </dl>

 

