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
# <a name="thin-provisioning-of-logical-units"></a><span data-ttu-id="ec6df-105">Allocation dynamique d’unités logiques</span><span class="sxs-lookup"><span data-stu-id="ec6df-105">Thin provisioning of logical units</span></span>

## <a name="platforms"></a><span data-ttu-id="ec6df-106">Plateformes</span><span class="sxs-lookup"><span data-stu-id="ec6df-106">Platforms</span></span>

<span data-ttu-id="ec6df-107">**Clients** – Windows 8</span><span class="sxs-lookup"><span data-stu-id="ec6df-107">**Clients** – Windows 8</span></span>  
<span data-ttu-id="ec6df-108">**Serveurs** – Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="ec6df-108">**Servers** – Windows Server 2012</span></span>  


## <a name="description"></a><span data-ttu-id="ec6df-109">Description</span><span class="sxs-lookup"><span data-stu-id="ec6df-109">Description</span></span>

<span data-ttu-id="ec6df-110">L’allocation dynamique Windows est une interface avec la solution de provisionnement de stockage de bout en bout.</span><span class="sxs-lookup"><span data-stu-id="ec6df-110">Windows Thin Provisioning is an interface to the end-to-end storage provisioning solution.</span></span> <span data-ttu-id="ec6df-111">Pour fournir un service de provisionnement de stockage hautement disponible, évolutif et convivial, il faut des implémentations robustes de l’hôte du serveur vers l’appareil cible de stockage.</span><span class="sxs-lookup"><span data-stu-id="ec6df-111">To deliver a highly available, scalable and user-friendly storage provisioning service requires robust implementations from the server host to the storage target device.</span></span> <span data-ttu-id="ec6df-112">La fonctionnalité de provisionnement dynamique de Windows fournit une vue synchrone des dispositifs de stockage à allocation dynamique pour l’administrateur système, le responsable informatique et l’administrateur de stockage via l’identification de l’unité logique (LUN) allouée dynamiquement, la notification de seuil, la gestion de l’épuisement des ressources, la récupération de l’espace et la récupération de l’état du bloc logique.</span><span class="sxs-lookup"><span data-stu-id="ec6df-112">The Windows thin provisioning feature provides a synchronous view of the thin provisioning storage devices to the system administrator, IT manager, and storage administrator through the thinly provisioned logical unit’s (LUN’s) identification, threshold notification, resource exhaustion handling, space reclamation, and logical block addressing (LBA) state retrieval.</span></span> <span data-ttu-id="ec6df-113">La fonctionnalité d’allocation dynamique Windows présente un modèle robuste de service de provisionnement du stockage qui peut être appliqué aux services de stockage client-serveur, de stockage de virtualisation et de stockage cloud.</span><span class="sxs-lookup"><span data-stu-id="ec6df-113">The Windows thin provisioning feature presents a robust storage provisioning service model that can be applied to client-server storage systems, virtualization storage, and cloud storage services.</span></span> <span data-ttu-id="ec6df-114">Microsoft garantira la haute qualité de la fonctionnalité d’allocation dynamique en appliquant les exigences du kit de certification du matériel de provisionnement dynamique Windows pour les produits de groupe de stockage.</span><span class="sxs-lookup"><span data-stu-id="ec6df-114">Microsoft will ensure the high quality of the thin provisioning feature by enforcing the Windows Thin Provisioning Hardware Certification Kit requirements for storage array products.</span></span>

<span data-ttu-id="ec6df-115">La solution de stockage de provisionnement dynamique Windows :</span><span class="sxs-lookup"><span data-stu-id="ec6df-115">The Windows Thin Provisioning storage solution:</span></span>

-   <span data-ttu-id="ec6df-116">Permet aux administrateurs de stockage de créer un LUN plus grand avec moins de ressources de disque physique</span><span class="sxs-lookup"><span data-stu-id="ec6df-116">Allows storage administrators to create a larger LUN with fewer physical disk resources</span></span>
-   <span data-ttu-id="ec6df-117">Ajoute ou supprime une ressource de disque physique sans interrompre le service de provisionnement du stockage</span><span class="sxs-lookup"><span data-stu-id="ec6df-117">Adds or removes physical disk resource without interrupting the storage provisioning service</span></span>
-   <span data-ttu-id="ec6df-118">Avertit les utilisateurs de l’utilisation du volume de stockage via le paramètre de seuil</span><span class="sxs-lookup"><span data-stu-id="ec6df-118">Alerts users to the storage volume usage through the threshold setting</span></span>
-   <span data-ttu-id="ec6df-119">Prend en charge l’approvisionnement du stockage via la configuration du pool de stockage partagé</span><span class="sxs-lookup"><span data-stu-id="ec6df-119">Supports storage provisioning through the shared storage pool configuration</span></span>
-   <span data-ttu-id="ec6df-120">Augmente ou diminue la taille du pool de stockage en fonction de la demande et de l’utilisation de l’espace de stockage.</span><span class="sxs-lookup"><span data-stu-id="ec6df-120">Increases or decreases the size of the storage pool according to the demand and usage of storage space</span></span>

<span data-ttu-id="ec6df-121">Résumé des fonctionnalités de provisionnement dynamique de Windows :</span><span class="sxs-lookup"><span data-stu-id="ec6df-121">Summary of the Windows Thin Provisioning features:</span></span>

-   <span data-ttu-id="ec6df-122">Identification des numéros d’unités logiques d’allocation dynamique</span><span class="sxs-lookup"><span data-stu-id="ec6df-122">Thin Provisioning LUN identification</span></span>
-   <span data-ttu-id="ec6df-123">Descripteurs pour la notification de seuil, l’épuisement des ressources temporaires et l’épuisement permanent des ressources</span><span class="sxs-lookup"><span data-stu-id="ec6df-123">Handles for threshold notification, temporary resource exhaustion, and permanent resource exhaustion</span></span>
-   <span data-ttu-id="ec6df-124">Récupération de l’espace de stockage</span><span class="sxs-lookup"><span data-stu-id="ec6df-124">Storage space reclamation</span></span>
-   <span data-ttu-id="ec6df-125">Mappage des requêtes d’état de blocs logiques</span><span class="sxs-lookup"><span data-stu-id="ec6df-125">Mapping state queries of logical blocks</span></span>

## <a name="manifestation"></a><span data-ttu-id="ec6df-126">Manifestation</span><span class="sxs-lookup"><span data-stu-id="ec6df-126">Manifestation</span></span>

<span data-ttu-id="ec6df-127">Sans une bonne compréhension des handles Windows pour le numéro d’unité logique de provisionnement dynamique, l’application peut échouer avec un comportement inattendu ou pour une raison inconnue.</span><span class="sxs-lookup"><span data-stu-id="ec6df-127">Without the proper understanding of the Windows handles for thin provisioning LUN, the app could fail with unexpected behavior or for an unknown cause.</span></span>

## <a name="using-thin-provisioning-luns"></a><span data-ttu-id="ec6df-128">Utilisation des numéros d’unités logiques d’allocation dynamique</span><span class="sxs-lookup"><span data-stu-id="ec6df-128">Using thin provisioning LUNs</span></span>

<span data-ttu-id="ec6df-129">Pour utiliser des numéros d’unités logiques alloués dynamiquement dans Windows 8 ou Windows Server 2012, les administrateurs système et de stockage doivent être conscients des aspects suivants :</span><span class="sxs-lookup"><span data-stu-id="ec6df-129">To use thinly provisioned LUNs in Windows 8 or Windows Server 2012, system and storage administrators should be aware of these matters:</span></span>

-   <span data-ttu-id="ec6df-130">L’identification des numéros d’unités logiques d’allocation dynamique ; les administrateurs système ou les utilisateurs finaux peuvent utiliser Defrag et l’utilitaire d’optimisation du stockage pour identifier le type de média du dispositif de stockage</span><span class="sxs-lookup"><span data-stu-id="ec6df-130">Thin provisioning LUN identification; system administrators or end users can use Defrag and the Storage Optimizer utility to identify the media type of the storage device</span></span>
-   <span data-ttu-id="ec6df-131">Lorsqu’un seuil ou un événement de carence des ressources permanent est atteint, Windows consigne un événement système pour alerter l’administrateur système</span><span class="sxs-lookup"><span data-stu-id="ec6df-131">When a threshold or a permanent resource exhaustion event is hit, Windows will log a system event to alert the system administrator</span></span>
-   <span data-ttu-id="ec6df-132">La récupération de l’espace de stockage peut être effectuée manuellement ou automatiquement par la notification de suppression de fichier ou le planificateur de l’optimiseur de stockage.</span><span class="sxs-lookup"><span data-stu-id="ec6df-132">Storage space reclamation can be performed manually or automatically by file delete notification or the scheduler of the storage optimizer</span></span>
-   <span data-ttu-id="ec6df-133">L’administrateur du stockage doit implémenter la notification de seuil pour alerter l’administrateur système ou l’utilisateur final et éviter toute interruption inattendue du service de stockage.</span><span class="sxs-lookup"><span data-stu-id="ec6df-133">Storage administrator should implement the threshold notification to alert system administrator or end user and avoid any unexpected storage service interruption</span></span>

## <a name="tests"></a><span data-ttu-id="ec6df-134">Tests</span><span class="sxs-lookup"><span data-stu-id="ec6df-134">Tests</span></span>

-   <span data-ttu-id="ec6df-135">Le groupe de stockage doit recevoir le certificat de provisionnement dynamique Windows 8 pour prendre en charge les fonctionnalités de provisionnement dynamique Windows</span><span class="sxs-lookup"><span data-stu-id="ec6df-135">Storage array must receive Windows 8 Thin Provisioning certificate to support Windows Thin Provisioning features</span></span>
-   <span data-ttu-id="ec6df-136">Le kit de certification du matériel de provisionnement dynamique Windows pour le groupe de stockage est un outil de test utile pour vérifier la capacité du groupe de stockage à prendre en charge la fonctionnalité d’allocation dynamique Windows</span><span class="sxs-lookup"><span data-stu-id="ec6df-136">Windows Thin Provisioning Hardware Certification Kit for storage array will be a useful test tool to verify storage array’s capability for Windows Thin Provisioning feature support</span></span>
-   <span data-ttu-id="ec6df-137">Windows s’attend à ce que le numéro d’unité logique de provisionnement dynamique et le numéro d’unité logique de provisionnement complet fonctionnent dans le même système sans aucun problème.</span><span class="sxs-lookup"><span data-stu-id="ec6df-137">Windows expects the Thin Provisioning LUN and Full Provisioning LUN to work in the same system without any issue</span></span>

## <a name="resources"></a><span data-ttu-id="ec6df-138">Ressources</span><span class="sxs-lookup"><span data-stu-id="ec6df-138">Resources</span></span>

-   [<span data-ttu-id="ec6df-139">Spécification de la commande de bloc SCSI de T10 (SBC3r27)</span><span class="sxs-lookup"><span data-stu-id="ec6df-139">T10 SCSI Block Command Spec (SBC3r27)</span></span>](https://www.t10.org/cgi-bin/ac.pl?t=f&f=sbc3r27.pdf)
-   [<span data-ttu-id="ec6df-140">Services du tableau de bord matériel</span><span class="sxs-lookup"><span data-stu-id="ec6df-140">Hardware Dashboard Services</span></span>](/windows-hardware/drivers/dashboard/)

 

 