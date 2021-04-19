---
description: .
ms.assetid: 6a31cca3-f47c-4663-b2e8-aad6b4a6f28f
title: Serveur Hyper-V
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d6997074e000b17a119a838df5b6fab961b8ee0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106539352"
---
# <a name="server-hyper-v"></a>Serveur Hyper-V

## <a name="platforms"></a>Plateformes

 **Clients** -Windows XP Windows \| Vista Windows \| 7  
**Serveurs** -windows Server 2008 \| Windows Server 2008 R2  

## <a name="feature-impact"></a>Impact sur les fonctionnalités

 **Gravité** -faible  
**Fréquence** -faible  





## <a name="description"></a>Description

La virtualisation de serveur permet à plusieurs systèmes d’exploitation de s’exécuter sur un seul ordinateur physique en tant qu’ordinateurs virtuels, ce qui vous permet de consolider les charges de travail des ordinateurs serveurs sous-exploités sur un plus petit nombre de machines entièrement utilisées. Windows 7 comprend plusieurs améliorations apportées à la version 2008 de Windows Server :

-   **Migration dynamique :** Dans Windows Server 2008, nous avions une migration rapide. Avec Migration dynamique, nous avons amélioré la vitesse de migration et la flexibilité de stockage.
-   **Prise en charge du processeur logique :** Nous avons augmenté les processeurs hôtes logiques de 16LP à 64LP.
-   **Ajout à chaud du stockage :** Vous pouvez maintenant ajouter des disques durs virtuels ou des disques directs à un ordinateur virtuel en cours d’exécution sans éteindre la machine virtuelle.
-   **Nouvelle prise en charge du matériel :** Nous avons ajouté la prise en charge des technologies incluses dans les nouveaux processeurs et les cartes réseau commercialisés, y compris la traduction de second niveau (SLAT), le déchargement TCP (Chimney) et VMdQ.
-   **Virtualisation des services Terminal Server (TSV) :** Nous avons centralisé la solution de bureau pour Hyper-V.

## <a name="manifestation-of-impact"></a>Manifeste de l’impact

-   **Migration dynamique :** Vous devrez peut-être modifier la façon dont vous avez conçu vos systèmes de stockage afin de tirer pleinement parti de cette technologie. Bien que ces modifications ne soient pas nécessaires, vous pouvez choisir de les implémenter pour tirer pleinement parti des avantages. Vous aurez peut-être besoin d’une application de gestion pour orchestrer Migration dynamique.
-   **Prise en charge du processeur logique :** Cette fonctionnalité n’aura aucun impact sur les clients ou les éditeurs de logiciels indépendants lors de la migration de Windows Server 2008 vers Windows Server 2008 R2.
-   **Ajout à chaud du stockage :** Cette fonctionnalité n’aura aucun impact sur les clients ou les éditeurs de logiciels indépendants lors de la migration de Windows Server 2008 vers Windows Server 2008 R2. Les applications de gestion qui configurent les paramètres d’un ordinateur virtuel peuvent nécessiter une mise à jour pour pouvoir gérer cette nouvelle fonctionnalité.
-   **Nouvelle prise en charge du matériel :** Ces fonctionnalités s’appliquent uniquement au nouveau matériel qui est introduit sur le marché. Dans la mesure où la prise en charge de ces fonctionnalités n’est pas prise en charge par la version, il est peu probable qu’un serveur physique migré depuis Windows Server 2008 vers Windows Server 2008 R2 sera affecté. Si ces fonctionnalités sont disponibles sur le serveur en cours de migration, aucune modification directe n’est prévue.
-   **Virtualisation des services Terminal Server :** Cette fonctionnalité n’aura aucun impact sur les clients ou les éditeurs de logiciels indépendants lors de la migration de Windows Server 2008 vers Windows Server 2008 R2. Les applications qui tirent parti des services Terminal Server (TS) peuvent être affectées. Cette fonctionnalité s’intègre directement avec les services Terminal Server et, par conséquent, les applications qui configurent les services Terminal Server peuvent nécessiter une mise à jour afin de gérer cette nouvelle fonctionnalité.

## <a name="mitigation"></a>Limitation des risques

-   **Migration dynamique :** Fournir des recommandations aux utilisateurs finaux avec les meilleures pratiques et les recommandations relatives à la conception du système de stockage. Vous devez informer l’utilisateur final sur les options et les recommandations.

## <a name="leveraging-capabilitities"></a>Exploitation de capabilitities

-   **Migration dynamique :** Cette fonctionnalité active l’environnement informatique dynamique. Les développeurs d’applications de gestion de la virtualisation doivent modifier leur application pour tirer parti de cette nouvelle fonctionnalité. Microsoft met les interfaces WMI à la disposition du public pour permettre aux développeurs d’intégrer des applications avec cette fonctionnalité.
-   **Virtualisation des services Terminal Server :** Cette fonctionnalité permet un nouveau scénario de virtualisation. Les applications qui tirent parti des services Terminal Server (TS) peuvent être affectées. Cette fonctionnalité s’intègre directement avec les services Terminal Server et, par conséquent, les applications qui configurent les services Terminal Server peuvent nécessiter une mise à jour afin de gérer cette nouvelle fonctionnalité.

## <a name="links-to-other-resources"></a>Liens vers d’autres ressources

[Interfaces de gestion WMI pour Hyper-V V1](/previous-versions/windows/desktop/virtual/windows-virtualization-portal). Bien que la majeure partie de ce contenu s’applique à v2 d’Hyper-V, une version mise à jour avec des informations spécifiques à V2 devrait être disponible plus près du lancement de Windows 7.

 

 
