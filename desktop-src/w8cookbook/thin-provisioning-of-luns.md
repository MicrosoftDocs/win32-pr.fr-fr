---
title: Allocation dynamique d’unités logiques
description: Allocation dynamique d’unités logiques
ms.assetid: D64ECA7B-62AC-4C14-BE4B-84DA2E20C16B
keywords:
- Numéro d'unité logique
- LBA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4abb6fa3cec112737b23e3cd658a48984cb0fcd1
ms.sourcegitcommit: ea4baf9953a78d2d6bd530b680601e39f3884541
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/01/2020
ms.locfileid: "104031995"
---
# <a name="thin-provisioning-of-logical-units"></a>Allocation dynamique d’unités logiques

## <a name="platforms"></a>Plateformes

**Clients** – Windows 8  
**Serveurs** – Windows Server 2012  


## <a name="description"></a>Description

L’allocation dynamique Windows est une interface avec la solution de provisionnement de stockage de bout en bout. Pour fournir un service de provisionnement de stockage hautement disponible, évolutif et convivial, il faut des implémentations robustes de l’hôte du serveur vers l’appareil cible de stockage. La fonctionnalité de provisionnement dynamique de Windows fournit une vue synchrone des dispositifs de stockage à allocation dynamique pour l’administrateur système, le responsable informatique et l’administrateur de stockage via l’identification de l’unité logique (LUN) allouée dynamiquement, la notification de seuil, la gestion de l’épuisement des ressources, la récupération de l’espace et la récupération de l’état du bloc logique. La fonctionnalité d’allocation dynamique Windows présente un modèle robuste de service de provisionnement du stockage qui peut être appliqué aux services de stockage client-serveur, de stockage de virtualisation et de stockage cloud. Microsoft garantira la haute qualité de la fonctionnalité d’allocation dynamique en appliquant les exigences du kit de certification du matériel de provisionnement dynamique Windows pour les produits de groupe de stockage.

La solution de stockage de provisionnement dynamique Windows :

-   Permet aux administrateurs de stockage de créer un LUN plus grand avec moins de ressources de disque physique
-   Ajoute ou supprime une ressource de disque physique sans interrompre le service de provisionnement du stockage
-   Avertit les utilisateurs de l’utilisation du volume de stockage via le paramètre de seuil
-   Prend en charge l’approvisionnement du stockage via la configuration du pool de stockage partagé
-   Augmente ou diminue la taille du pool de stockage en fonction de la demande et de l’utilisation de l’espace de stockage.

Résumé des fonctionnalités de provisionnement dynamique de Windows :

-   Identification des numéros d’unités logiques d’allocation dynamique
-   Descripteurs pour la notification de seuil, l’épuisement des ressources temporaires et l’épuisement permanent des ressources
-   Récupération de l’espace de stockage
-   Mappage des requêtes d’état de blocs logiques

## <a name="manifestation"></a>Manifestation

Sans une bonne compréhension des handles Windows pour le numéro d’unité logique de provisionnement dynamique, l’application peut échouer avec un comportement inattendu ou pour une raison inconnue.

## <a name="using-thin-provisioning-luns"></a>Utilisation des numéros d’unités logiques d’allocation dynamique

Pour utiliser des numéros d’unités logiques alloués dynamiquement dans Windows 8 ou Windows Server 2012, les administrateurs système et de stockage doivent être conscients des aspects suivants :

-   L’identification des numéros d’unités logiques d’allocation dynamique ; les administrateurs système ou les utilisateurs finaux peuvent utiliser Defrag et l’utilitaire d’optimisation du stockage pour identifier le type de média du dispositif de stockage
-   Lorsqu’un seuil ou un événement de carence des ressources permanent est atteint, Windows consigne un événement système pour alerter l’administrateur système
-   La récupération de l’espace de stockage peut être effectuée manuellement ou automatiquement par la notification de suppression de fichier ou le planificateur de l’optimiseur de stockage.
-   L’administrateur du stockage doit implémenter la notification de seuil pour alerter l’administrateur système ou l’utilisateur final et éviter toute interruption inattendue du service de stockage.

## <a name="tests"></a>Tests

-   Le groupe de stockage doit recevoir le certificat de provisionnement dynamique Windows 8 pour prendre en charge les fonctionnalités de provisionnement dynamique Windows
-   Le kit de certification du matériel de provisionnement dynamique Windows pour le groupe de stockage est un outil de test utile pour vérifier la capacité du groupe de stockage à prendre en charge la fonctionnalité d’allocation dynamique Windows
-   Windows s’attend à ce que le numéro d’unité logique de provisionnement dynamique et le numéro d’unité logique de provisionnement complet fonctionnent dans le même système sans aucun problème.

## <a name="resources"></a>Ressources

-   [Spécification de la commande de bloc SCSI de T10 (SBC3r27)](https://www.t10.org/cgi-bin/ac.pl?t=f&f=sbc3r27.pdf)
-   [Services du tableau de bord matériel](/windows-hardware/drivers/dashboard/)

 

 