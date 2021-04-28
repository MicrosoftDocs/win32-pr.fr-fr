---
description: Suppression des services UDDI du système d’exploitation serveur
ms.assetid: 5ebc8c4c-acee-4658-8d36-30fbb17b1ef1
title: Suppression des services UDDI du système d’exploitation serveur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 960a4063d990a3b2cdac45cd933a1e7dfef41f88
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108116327"
---
# <a name="removal-of-uddi-services-from-server-operating-system"></a><span data-ttu-id="c2fef-103">Suppression des services UDDI du système d’exploitation serveur</span><span class="sxs-lookup"><span data-stu-id="c2fef-103">Removal of UDDI Services from Server Operating System</span></span>

## <a name="affected-platform"></a><span data-ttu-id="c2fef-104">Plateforme affectée</span><span class="sxs-lookup"><span data-stu-id="c2fef-104">Affected Platform</span></span>

<span data-ttu-id="c2fef-105">**Serveurs** -Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="c2fef-105">**Servers** - Windows Server 2008 R2</span></span>  



## <a name="feature-impact"></a><span data-ttu-id="c2fef-106">Impact sur les fonctionnalités</span><span class="sxs-lookup"><span data-stu-id="c2fef-106">Feature Impact</span></span>

<span data-ttu-id="c2fef-107">**Gravité** -moyenne</span><span class="sxs-lookup"><span data-stu-id="c2fef-107">**Severity** - Medium</span></span>  
<span data-ttu-id="c2fef-108">**Fréquence** -faible</span><span class="sxs-lookup"><span data-stu-id="c2fef-108">**Frequency** - Low</span></span>  

## <a name="description"></a><span data-ttu-id="c2fef-109">Description</span><span class="sxs-lookup"><span data-stu-id="c2fef-109">Description</span></span>

<span data-ttu-id="c2fef-110">Microsoft a supprimé le rôle serveur services UDDI (Universal Description, Discovery, and Integration) de Windows Server 2008 R2.</span><span class="sxs-lookup"><span data-stu-id="c2fef-110">Microsoft has removed the UDDI (Universal Description, Discovery, and Integration) Services server role from Windows Server 2008 R2.</span></span> <span data-ttu-id="c2fef-111">Les versions ultérieures des services UDDI feront partie du produit Microsoft BizTalk.</span><span class="sxs-lookup"><span data-stu-id="c2fef-111">Future releases of UDDI Services will be part of the Microsoft BizTalk product.</span></span> <span data-ttu-id="c2fef-112">Cette réalignement et la consolidation des produits permettent à Microsoft de mieux servir le marché de l’architecture orientée services (SOA).</span><span class="sxs-lookup"><span data-stu-id="c2fef-112">This product realignment and consolidation positions Microsoft to better serve the services-oriented architecture (SOA) market.</span></span>

<span data-ttu-id="c2fef-113">La première version postérieure à Windows Server 2008 des services UDDI sera compatible avec les normes UDDI v 3.0.</span><span class="sxs-lookup"><span data-stu-id="c2fef-113">The first post-Windows Server 2008 release of UDDI Services will be UDDI v3.0 standards compliant.</span></span> <span data-ttu-id="c2fef-114">Elle est fournie dans le cadre de la version BizTalk Server 2009.</span><span class="sxs-lookup"><span data-stu-id="c2fef-114">It will ship as part of the BizTalk Server 2009 release.</span></span> <span data-ttu-id="c2fef-115">Pour répondre à notre engagement à fournir une expérience utilisateur satisfaisante, nous proposons un package d’installation des services UDDI V3 pour Windows Server 2008 R2.</span><span class="sxs-lookup"><span data-stu-id="c2fef-115">To meet our commitment to provide a satisfactory user experience, we will offer a UDDI Services v3 installation package for Windows Server 2008 R2.</span></span>

## <a name="manifestation"></a><span data-ttu-id="c2fef-116">Manifestation</span><span class="sxs-lookup"><span data-stu-id="c2fef-116">Manifestation</span></span>

<span data-ttu-id="c2fef-117">La présence de versions précédentes des composants des services UDDI sur le système bloque une mise à niveau vers Windows Server 2008 R2.</span><span class="sxs-lookup"><span data-stu-id="c2fef-117">The presence of previous versions of UDDI Services components on the system blocks an upgrade to Windows Server 2008 R2.</span></span>

## <a name="mitigation-of-impact"></a><span data-ttu-id="c2fef-118">Atténuation de l’impact</span><span class="sxs-lookup"><span data-stu-id="c2fef-118">Mitigation of Impact</span></span>

<span data-ttu-id="c2fef-119">Les utilisateurs qui ont déployé un site de services UDDI à partir de Windows Server 2003 ou Windows Server 2008 peuvent choisir de ne pas mettre à niveau les serveurs qui exécutent les services UDDI vers Windows Server 2008 R2.</span><span class="sxs-lookup"><span data-stu-id="c2fef-119">Users who have deployed a UDDI Services site from Windows Server 2003 or Windows Server 2008 can choose not to upgrade the servers running the UDDI Services to Windows Server 2008 R2.</span></span> <span data-ttu-id="c2fef-120">Ils peuvent également déplacer les services UDDI vers des zones Windows Server 2003 ou Windows Server 2008 dédiées s’ils doivent mettre à niveau les zones des services UDDI en cours.</span><span class="sxs-lookup"><span data-stu-id="c2fef-120">They can also move the UDDI Services to dedicated Windows Server 2003 or Windows Server 2008 boxes if they have to upgrade the current UDDI Services boxes.</span></span>

## <a name="solution"></a><span data-ttu-id="c2fef-121">Solution</span><span class="sxs-lookup"><span data-stu-id="c2fef-121">Solution</span></span>

<span data-ttu-id="c2fef-122">La solution recommandée consiste à déployer les services UDDI v 3.0 à partir de BizTalk Server 2009 sur un ordinateur Windows Server 2008 R2, puis à migrer l’ancien site vers le nouveau site.</span><span class="sxs-lookup"><span data-stu-id="c2fef-122">The recommended solution is to deploy UDDI Services v3.0 from BizTalk Server 2009 onto a Windows Server 2008 R2 machine, and then to migrate the old site to the new site.</span></span> <span data-ttu-id="c2fef-123">Les services UDDI v 3.0 offrent une compatibilité descendante avec les services UDDI 2,0, si bien que toutes les applications qui utilisent des services UDDI ne seront pas affectées.</span><span class="sxs-lookup"><span data-stu-id="c2fef-123">UDDI Services v3.0 provides backward compatibility with UDDI Services 2.0, so any applications that are using UDDI Services will be unaffected.</span></span>

<span data-ttu-id="c2fef-124">Pour ce faire, procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="c2fef-124">To do this, follow these steps:</span></span>

1.  <span data-ttu-id="c2fef-125">Configurez un nouveau site UDDI services v 3.0 sur un ordinateur déjà chargé avec Windows Server 2008 R2.</span><span class="sxs-lookup"><span data-stu-id="c2fef-125">Set up a new UDDI Services v3.0 site on a machine already loaded with Windows Server 2008 R2.</span></span> <span data-ttu-id="c2fef-126">(Remarque : dans une installation distribuée, un site UDDI v 3.0 peut être constitué de plusieurs ordinateurs Windows Server 2008 R2.)</span><span class="sxs-lookup"><span data-stu-id="c2fef-126">(Note: In a distributed setup, a UDDI v3.0 site can consist of more than one Windows Server 2008 R2 machines.)</span></span>
2.  <span data-ttu-id="c2fef-127">Utilisez l’outil de migration de données UDDI pour migrer les données de l’ancienne base de données des services UDDI vers la nouvelle base de données.</span><span class="sxs-lookup"><span data-stu-id="c2fef-127">Use the UDDI data migration tool to migrate the data from the old UDDI Services database to the new database.</span></span>
3.  <span data-ttu-id="c2fef-128">Sauvegardez l’ancienne base de données des services UDDI pour garantir la restauration.</span><span class="sxs-lookup"><span data-stu-id="c2fef-128">Back up the old UDDI Services database to ensure rollback capability.</span></span>
4.  <span data-ttu-id="c2fef-129">Désinstallez les anciens logiciels des services UDDI, puis mettez-les à niveau vers Windows Server 2008 R2.</span><span class="sxs-lookup"><span data-stu-id="c2fef-129">Uninstall the old UDDI Services software and then upgrade those boxes to Windows Server 2008 R2.</span></span>

## <a name="links-to-other-resources"></a><span data-ttu-id="c2fef-130">Liens vers d’autres ressources</span><span class="sxs-lookup"><span data-stu-id="c2fef-130">Links to Other Resources</span></span>

-   [<span data-ttu-id="c2fef-131">Site Web des services Microsoft UDDI</span><span class="sxs-lookup"><span data-stu-id="c2fef-131">Microsoft UDDI Services website</span></span>](https://msdn.microsoft.com/biztalk/dd789428.aspx)
-   [<span data-ttu-id="c2fef-132">Spécifications UDDI</span><span class="sxs-lookup"><span data-stu-id="c2fef-132">UDDI specifications</span></span>](http://uddi.xml.org/specification)
-   [<span data-ttu-id="c2fef-133">Téléchargement des services UDDI v 3.0 pour Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="c2fef-133">UDDI Services v3.0 download for Windows Server 2008 R2</span></span>](https://www.microsoft.com/downloads/details.aspx?FamilyID=e4761835-70f0-4e8d-96c5-64818d54e06e)

 

 



