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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127404248"
---
# <a name="thin-provisioning-of-logical-units"></a>Allocation dynamique d’unités logiques

## <a name="platforms"></a>Plateformes

**Clients** – Windows 8  
**serveurs** – Windows Server 2012  


## <a name="description"></a>Description

Windows L’allocation dynamique est une interface avec la solution de provisionnement de stockage de bout en bout. Pour fournir un service de provisionnement de stockage hautement disponible, évolutif et convivial, il faut des implémentations robustes de l’hôte du serveur vers l’appareil cible de stockage. le Windows fonctionnalité d’allocation dynamique fournit une vue synchrone des périphériques de stockage à allocation dynamique à l’administrateur système, au responsable informatique et à l’administrateur de stockage par le biais de l’identification de l’unité logique (LUN) allouée dynamiquement, de la notification de seuil, de la gestion de l’épuisement des ressources, de la récupération de l’espace et de l’adressage LBA. le Windows fonctionnalité d’allocation dynamique présente un modèle robuste de service de provisionnement du stockage qui peut être appliqué aux systèmes de stockage client-serveur, au stockage de virtualisation et aux services de stockage cloud. Microsoft garantira la haute qualité de la fonctionnalité de provisionnement dynamique en appliquant les Windows exigences du Kit de Certification du matériel de provisionnement dynamique pour les produits de groupe de stockage.

la solution de stockage à allocation dynamique Windows :

-   Permet aux administrateurs de stockage de créer un LUN plus grand avec moins de ressources de disque physique
-   Ajoute ou supprime une ressource de disque physique sans interrompre le service de provisionnement du stockage
-   Avertit les utilisateurs de l’utilisation du volume de stockage via le paramètre de seuil
-   Prend en charge l’approvisionnement du stockage via la configuration du pool de stockage partagé
-   Augmente ou diminue la taille du pool de stockage en fonction de la demande et de l’utilisation de l’espace de stockage.

résumé des fonctionnalités d’allocation dynamique Windows :

-   Identification des numéros d’unités logiques d’allocation dynamique
-   Descripteurs pour la notification de seuil, l’épuisement des ressources temporaires et l’épuisement permanent des ressources
-   récupération de l’espace de Stockage
-   Mappage des requêtes d’état de blocs logiques

## <a name="manifestation"></a>Manifestation

sans une bonne compréhension des handles de Windows pour le numéro d’unité logique de provisionnement dynamique, l’application peut échouer avec un comportement inattendu ou pour une raison inconnue.

## <a name="using-thin-provisioning-luns"></a>Utilisation des numéros d’unités logiques d’allocation dynamique

pour utiliser des numéros d’unités logiques alloués dynamiquement dans Windows 8 ou Windows Server 2012, les administrateurs système et de stockage doivent être conscients des aspects suivants :

-   L’identification des numéros d’unités logiques d’allocation dynamique ; les administrateurs système ou les utilisateurs finaux peuvent utiliser la défragmentation et l’utilitaire d’optimisation Stockage pour identifier le type de média du dispositif de stockage
-   lorsqu’un seuil ou un événement de carence des ressources permanent est atteint, Windows enregistre un événement système pour alerter l’administrateur système
-   Stockage la récupération de l’espace peut être effectuée manuellement ou automatiquement par la notification de suppression de fichier ou le planificateur de l’optimiseur de stockage.
-   Stockage administrateur doit implémenter la notification de seuil pour alerter l’administrateur système ou l’utilisateur final et éviter toute interruption inattendue du service de stockage

## <a name="tests"></a>Tests

-   Stockage groupe doit recevoir Windows 8 certificat de provisionnement dynamique pour prendre en charge Windows fonctionnalités de provisionnement dynamique
-   Windows le Kit de Certification du matériel de provisionnement dynamique pour le groupe de stockage est un outil de test utile pour vérifier la capacité du groupe de stockage à Windows prise en charge de la fonctionnalité d’allocation dynamique
-   Windows s’attend à ce que le numéro d’unité logique de provisionnement dynamique et le numéro d’unité logique de provisionnement complet fonctionnent dans le même système sans aucun problème.

## <a name="resources"></a>Ressources

-   [Spécification de la commande de bloc SCSI de T10 (SBC3r27)](https://www.t10.org/cgi-bin/ac.pl?t=f&f=sbc3r27.pdf)
-   [Services du tableau de bord matériel](/windows-hardware/drivers/dashboard/)

 

 