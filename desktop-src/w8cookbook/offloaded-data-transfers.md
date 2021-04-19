---
title: Transferts de données déchargées
description: Transferts de données déchargées
ms.assetid: 91EBE6D6-2DA7-48DA-AEB7-3FAFCA8341F5
keywords:
- ODX
- déchargement de copie
- déchargement
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1057ed27347fefc7ebc6a171eb7273da4341b024
ms.sourcegitcommit: ea4baf9953a78d2d6bd530b680601e39f3884541
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/01/2020
ms.locfileid: "106509884"
---
# <a name="offloaded-data-transfers"></a>Transferts de données déchargées

## <a name="platforms"></a>Plateformes

**Clients** – Windows 8  
**Serveurs** – Windows Server 2012  


## <a name="description"></a>Description

Pour accélérer le déplacement des données de stockage, Microsoft a développé une nouvelle technologie de transfert de données : le transfert de données déchargées (ODX). Au lieu d’utiliser des opérations d’écriture de lecture et de mise en mémoire tampon, Windows ODX démarre l’opération de copie avec une lecture de déchargement et récupère un jeton représentant les données du dispositif de stockage, puis utilise une commande d’écriture de déchargement avec le jeton pour demander le déplacement des données du disque source vers le disque de destination. Le gestionnaire de copie des périphériques de stockage effectue le déplacement des données en fonction du jeton. Dans Windows 8, le responsable informatique et l’administrateur du stockage sont en mesure d’utiliser la fonctionnalité ODX de Windows pour interagir avec le périphérique de stockage afin de déplacer des fichiers ou des données volumineux via le réseau de stockage à grande vitesse. Windows ODX réduit considérablement le trafic réseau client-serveur et l’utilisation du temps processeur pendant les transferts de données volumineux, car tous les déplacements de données se trouvent sur le réseau de stockage principal. ODX peut être utilisé dans le cadre du déploiement d’ordinateurs virtuels, de la migration massive des données et de la prise en charge des périphériques de stockage hiérarchisé, et peut réduire le coût du déploiement du matériel physique via les fonctionnalités de stockage ODX et de l’allocation dynamique.

> [!Note]  
> Cette fonctionnalité fonctionne uniquement sur les périphériques de stockage avec l’implémentation de la spécification SPC4 et SBC3.

 

## <a name="functional-details"></a>Détails fonctionnels

-   La fonctionnalité ODX de Windows est incorporée dans le moteur de copie du système d’exploitation Windows. pendant l’énumération du stockage, Windows interroge la fonctionnalité ODX du dispositif de stockage
-   La copie du dispositif de stockage source et du périphérique de stockage de destination de copie doit être gérée sous le même gestionnaire de copie pour la prise en charge du déchargement
-   Si une opération de déchargement de copie échoue, le gestionnaire de copie du dispositif de stockage doit retourner les données de sens supplémentaires appropriées pour la gestion des erreurs des applications
-   Le moteur de copie Windows revient à l’opération de copie traditionnelle en cas d’échec de l’opération de déchargement de copie

## <a name="using-odx"></a>Utilisation de ODX

-   L’application de transfert de données doit s’assurer que le LUN source de copie et le numéro d’unité logique de destination de copie sont bien basés sur ODX avant d’appeler les routines d’API ODX
-   Dans l’Explorateur Windows, les utilisateurs peuvent utiliser « faire glisser » ou « copier et coller » pour effectuer un déchargement de copie
-   Lorsque le numéro d’unité logique source et le numéro d’unité logique de destination sont montés avec le système de fichiers, l’application ne doit appeler que le \_ déchargement FSCTL \_ et l' \_ écriture de déchargement FSCTL \_ pour effectuer le transfert de données du LUN source vers le LUN de destination.
-   Si une opération de déchargement de copie échoue, le gestionnaire de copie du dispositif de stockage doit retourner les données de sens supplémentaires appropriées pour la gestion des erreurs des applications
-   Lorsque le numéro d’unité logique source ou le numéro d’unité logique de destination n’est pas monté avec le système de fichiers et verrouillé, l’application doit appeler le \_ stockage IOCTL \_ gérer les \_ \_ \_ attributs du jeu de données avec DeviceDsmAction \_ OffloadRead ou DeviceDsmAction \_ OffloadWrite action pour effectuer le déchargement de copie
-   Les applications de gestion du stockage peuvent utiliser \_ \_ l’API Pass via SCSI pour effectuer des transferts de données déchargées lorsque les numéros d’unité logique source et de destination ne sont pas montés avec un système de fichiers et verrouillés

## <a name="tests"></a>Tests

-   Pour garantir une expérience utilisateur robuste, vérifiez la certification ODX Windows du groupe de stockage.
-   Le dispositif de stockage doit respecter les exigences de certification des transferts de données déchargées Windows (utilisées pour être logo) pour prendre en charge la fonctionnalité ODX
-   Utiliser le kit de certification du matériel des transferts de données déchargées Windows pour vérifier la prise en charge des fonctionnalités ODX des dispositifs de stockage

## <a name="resources"></a>Ressources

-   Spécification de la spécification XCOPY pour XCOPY Lite (11-059r8)
    -   [https://www.t10.org/cgi-bin/ac.pl?t=f&f=spc4r35b.pdf](https://www.t10.org/cgi-bin/ac.pl?t=f&f=spc4r35b.pdf)
    -   [https://www.t10.org/cgi-bin/ac.pl?t=f&f=sbc3r30.pdf](https://www.t10.org/cgi-bin/ac.pl?t=f&f=sbc3r30.pdf)
-   [Services du tableau de bord matériel](/windows-hardware/drivers/dashboard/)
-   [\_Structure de transfert SCSI \_](/windows-hardware/drivers/ddi/ntddscsi/ns-ntddscsi-_scsi_pass_through)

 

 