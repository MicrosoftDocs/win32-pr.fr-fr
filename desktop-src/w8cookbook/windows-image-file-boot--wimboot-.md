---
title: Démarrage du fichier image Windows (WimBoot)
description: Démarrage du fichier image Windows (WimBoot)
ms.assetid: 1C4EFC42-6698-4981-8C55-D1DFC6309F31
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d9f14ea506226e2c16d771ecec52fa31a8c871b4
ms.sourcegitcommit: 46376be61d3fa308f9b1a06d7e2fa122a39755af
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/10/2020
ms.locfileid: "103734644"
---
# <a name="windows-image-file-boot-wimboot"></a><span data-ttu-id="acd49-103">Démarrage du fichier image Windows (WimBoot)</span><span class="sxs-lookup"><span data-stu-id="acd49-103">Windows Image File Boot (WimBoot)</span></span>

## <a name="platform"></a><span data-ttu-id="acd49-104">Plateforme</span><span class="sxs-lookup"><span data-stu-id="acd49-104">Platform</span></span>

<span data-ttu-id="acd49-105">**Clients :** Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="acd49-105">**Clients:** Windows 8.1</span></span>  

## <a name="description"></a><span data-ttu-id="acd49-106">Description</span><span class="sxs-lookup"><span data-stu-id="acd49-106">Description</span></span>

<span data-ttu-id="acd49-107">WimBoot est une autre façon pour les fabricants OEM de déployer Windows.</span><span class="sxs-lookup"><span data-stu-id="acd49-107">WimBoot is an alternative way for OEMs to deploy Windows.</span></span> <span data-ttu-id="acd49-108">Un déploiement WimBoot démarre et exécute Windows directement à partir d’un fichier image Windows (WIM) compressé.</span><span class="sxs-lookup"><span data-stu-id="acd49-108">A WimBoot deployment boots and runs Windows directly out of a compressed Windows Image File (WIM).</span></span> <span data-ttu-id="acd49-109">Ce fichier WIM est immuable et son accès est géré par un nouveau pilote de filtre de système de fichiers (WoF.sys).</span><span class="sxs-lookup"><span data-stu-id="acd49-109">This WIM file is immutable, and access to it is managed by a new file system filter driver (WoF.sys).</span></span>

<span data-ttu-id="acd49-110">Le résultat est une réduction significative de l’espace disque nécessaire à l’installation de Windows.</span><span class="sxs-lookup"><span data-stu-id="acd49-110">The result is a significant reduction in the disk space required to install Windows.</span></span>

## <a name="manifestations"></a><span data-ttu-id="acd49-111">Manifestations</span><span class="sxs-lookup"><span data-stu-id="acd49-111">Manifestations</span></span>

<span data-ttu-id="acd49-112">La plupart des applications doivent être complètement désaffectées par WimBoot.</span><span class="sxs-lookup"><span data-stu-id="acd49-112">Most applications should be completely unaffected by WimBoot.</span></span> <span data-ttu-id="acd49-113">Seules les applications qui accèdent à des fichiers système ou déverrouillent des fichiers système ou des fichiers préchargés pour l’accès en écriture peuvent être affectées.</span><span class="sxs-lookup"><span data-stu-id="acd49-113">Only applications that access and unlock system files or pre-loaded files for write access may be affected.</span></span> <span data-ttu-id="acd49-114">Étant donné que le fichier WIM est immuable, les mises à jour de celui-ci (c’est-à-dire les fichiers système ou préchargés) sont simplement stockées sur la partition C : \\ .</span><span class="sxs-lookup"><span data-stu-id="acd49-114">Since the WIM is immutable, updates to it (that is, system or pre-loaded files) are simply stored on the C:\\ partition.</span></span>

<span data-ttu-id="acd49-115">Si une application a déverrouillé l’accès en écriture pour tous les fichiers système et les fichiers préchargés par le fichier WIM, les économies que WimBoot fournit seraient complètement perdues, car tous ces fichiers seraient décompressés et placés sur le volume C : \\ .</span><span class="sxs-lookup"><span data-stu-id="acd49-115">If an application unlocked write access for all WIM-backed system and pre-loaded files, the savings that WimBoot delivers would be completely lost, as all of these files would be decompressed and placed on the C:\\ volume.</span></span>

<span data-ttu-id="acd49-116">En outre, les applications de sauvegarde et de restauration doivent être conscientes des déploiements de WimBoot, car le fichier WIM est présent dans une partition distincte. autrement dit, lors de la sauvegarde, les partitions C : \\ et Wim doivent être enregistrées et les deux doivent être restaurées ensemble.</span><span class="sxs-lookup"><span data-stu-id="acd49-116">Furthermore, back-up and restore applications need to be aware of WimBoot deployments, as the WIM is present in a separate partition; that is, on back-up, both the C:\\ and WIM partitions must be saved and both must be restored together.</span></span>

## <a name="solution"></a><span data-ttu-id="acd49-117">Solution</span><span class="sxs-lookup"><span data-stu-id="acd49-117">Solution</span></span>

<span data-ttu-id="acd49-118">De nouvelles API ont été introduites pour permettre aux applications de demander directement si un volume ou un fichier donné est associé à un fichier WIM.</span><span class="sxs-lookup"><span data-stu-id="acd49-118">New APIs were introduced that allow applications to directly query if a given volume or file is backed by a WIM.</span></span> <span data-ttu-id="acd49-119">Ces informations permettent aux applications de prendre des décisions appropriées, telles que l’ouverture de ces fichiers uniquement pour l’accès en lecture ou pour identifier les volumes/partitions qui doivent être sauvegardées et restaurées ensemble.</span><span class="sxs-lookup"><span data-stu-id="acd49-119">This information allows applications to make appropriate decisions, such as opening these files only for read access or to identify volumes/partitions that have to be backed up and restored together.</span></span>

## <a name="compatibility-performance-reliability-or-usability-tests"></a><span data-ttu-id="acd49-120">Compatibilité, performances, fiabilité ou tests d’utilisation</span><span class="sxs-lookup"><span data-stu-id="acd49-120">Compatibility, performance, reliability, or usability tests</span></span>

<span data-ttu-id="acd49-121">Les développeurs d’applications doivent tester leurs logiciels et leurs scénarios correspondants sur un système WimBoot, en particulier si ces applications accèdent à des fichiers système ou préchargés.</span><span class="sxs-lookup"><span data-stu-id="acd49-121">Application developers should test their software and its corresponding scenarios on a WimBoot system, especially if these applications access system or pre-loaded files.</span></span> <span data-ttu-id="acd49-122">Une attention particulière doit être accordée à une réduction significative de l’espace disque disponible après la fin d’un scénario.</span><span class="sxs-lookup"><span data-stu-id="acd49-122">Special attention should be paid to a significant reduction in available disk space after a scenario has been completed.</span></span>

 

 




