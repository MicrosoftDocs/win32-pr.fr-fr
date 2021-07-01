---
title: API de mastérisation d’image
description: API de mastérisation d’image
ms.assetid: 4902d3fb-3195-4909-ab64-28f8a77ba14c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c7fabf41d1c82420709b39bb5db03c2ac3e851d2
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/30/2021
ms.locfileid: "113119675"
---
# <a name="image-mastering-api"></a><span data-ttu-id="f4bce-103">API de mastérisation d’image</span><span class="sxs-lookup"><span data-stu-id="f4bce-103">Image Mastering API</span></span>

## <a name="purpose"></a><span data-ttu-id="f4bce-104">Objectif</span><span class="sxs-lookup"><span data-stu-id="f4bce-104">Purpose</span></span>

<span data-ttu-id="f4bce-105">L’API de mastérisation des images Microsoft Windows permet aux applications de préparer et de graver des images sur des supports de stockage sur CD, DVD et disques Blu-Ray.</span><span class="sxs-lookup"><span data-stu-id="f4bce-105">The Microsoft Windows image mastering API enables applications to stage and burn images to CD, DVD, and Blu-ray optical storage media.</span></span> <span data-ttu-id="f4bce-106">D’autres supports de type disque qui définissent les images de la même manière peuvent également utiliser cette API.</span><span class="sxs-lookup"><span data-stu-id="f4bce-106">Other disc-like media that lay images in the same manner can also use this API.</span></span>

## <a name="developer-audience"></a><span data-ttu-id="f4bce-107">Développeurs concernés</span><span class="sxs-lookup"><span data-stu-id="f4bce-107">Developer audience</span></span>

<span data-ttu-id="f4bce-108">IMAPi est conçu pour les développeurs C/C++ et Visual Basic, ainsi que pour ceux qui écrivent des scripts à l’aide de VBScript.</span><span class="sxs-lookup"><span data-stu-id="f4bce-108">IMAPI is designed for C/C++ and Visual Basic developers and those writing scripts using VBScript.</span></span>

<span data-ttu-id="f4bce-109">Il est recommandé d’avoir connaissance des technologies de CD, DVD et Blu-Ray et des systèmes de fichiers.</span><span class="sxs-lookup"><span data-stu-id="f4bce-109">Knowledge of CD, DVD, and Blu-ray technologies and file systems is recommended.</span></span> <span data-ttu-id="f4bce-110">Les développeurs peuvent bénéficier d’une bonne connaissance de la dernière révision de la commande multimédia (MMC) sur [ftp://ftp.T10.org/T10/drafts/MMC6](https://www.microsoft.com/?ref=go).</span><span class="sxs-lookup"><span data-stu-id="f4bce-110">Developers may benefit from a familiarity with the latest revision of Multimedia Command (MMC) at [ftp://ftp.t10.org/t10/drafts/mmc6](https://www.microsoft.com/?ref=go).</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="f4bce-111">Conditions d’exécution</span><span class="sxs-lookup"><span data-stu-id="f4bce-111">Run-time requirements</span></span>

<span data-ttu-id="f4bce-112">IMAPi 2,0 est pris en charge en mode natif à partir de Windows Vista et de Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="f4bce-112">IMAPI 2.0 is supported natively starting with Windows Vista and Windows Server 2008.</span></span> <span data-ttu-id="f4bce-113">L’activation de la fonctionnalité IMAPi 2,0 pour Windows XP et Windows Server 2003 requiert l’installation du package de mise à jour [KB932716](https://support.microsoft.com/kb/932716) .</span><span class="sxs-lookup"><span data-stu-id="f4bce-113">Enabling IMAPI 2.0 functionality for Windows XP and Windows Server 2003 requires the installation of the [KB932716](https://support.microsoft.com/kb/932716) update package.</span></span> <span data-ttu-id="f4bce-114">Si ce package n’est pas installé, Windows XP prend en charge [imapi 1,0](imapiv1.md)en mode natif.</span><span class="sxs-lookup"><span data-stu-id="f4bce-114">If this package is not installed, Windows XP still natively supports [IMAPI 1.0](imapiv1.md).</span></span>

> [!Note]  
> <span data-ttu-id="f4bce-115">Le Pack de fonctionnalités Windows pour le stockage est accessible au public par le biais du [Centre de téléchargement Microsoft](https://www.microsoft.com/downloads/details.aspx?FamilyID=63ab51ea-99c9-45c0-980a-c556746fcf05).</span><span class="sxs-lookup"><span data-stu-id="f4bce-115">The Windows Feature Pack for Storage is available to the public via the [Microsoft Download Center](https://www.microsoft.com/downloads/details.aspx?FamilyID=63ab51ea-99c9-45c0-980a-c556746fcf05).</span></span> <span data-ttu-id="f4bce-116">Vous trouverez des informations supplémentaires sur les modifications spécifiques de l’API dans la section [Nouveautés](what-s-new.md) .</span><span class="sxs-lookup"><span data-stu-id="f4bce-116">Additional information regarding specific API changes can be found in the [What's New](what-s-new.md) section.</span></span>

 

## <a name="in-this-section"></a><span data-ttu-id="f4bce-117">Contenu de cette section</span><span class="sxs-lookup"><span data-stu-id="f4bce-117">In this section</span></span>



| <span data-ttu-id="f4bce-118">Rubrique</span><span class="sxs-lookup"><span data-stu-id="f4bce-118">Topic</span></span>                                             | <span data-ttu-id="f4bce-119">Description</span><span class="sxs-lookup"><span data-stu-id="f4bce-119">Description</span></span>                                                                           |
|---------------------------------------------------|---------------------------------------------------------------------------------------|
| [<span data-ttu-id="f4bce-120">Nouveautés</span><span class="sxs-lookup"><span data-stu-id="f4bce-120">What's New</span></span>](what-s-new.md)<br/>           | <span data-ttu-id="f4bce-121">Informations détaillant chaque version importante de l’API de mastérisation d’image.</span><span class="sxs-lookup"><span data-stu-id="f4bce-121">Information detailing each significant release of the Image Mastering API.</span></span><br/> |
| [<span data-ttu-id="f4bce-122">À propos d’IMAPi</span><span class="sxs-lookup"><span data-stu-id="f4bce-122">About IMAPI</span></span>](about-imapi.md)<br/>         | <span data-ttu-id="f4bce-123">Informations générales sur l’API de mastérisation d’image.</span><span class="sxs-lookup"><span data-stu-id="f4bce-123">General information about the Image Mastering API.</span></span><br/>                         |
| [<span data-ttu-id="f4bce-124">Utilisation d’IMAPi</span><span class="sxs-lookup"><span data-stu-id="f4bce-124">Using IMAPI</span></span>](using-imapi.md)<br/>         | <span data-ttu-id="f4bce-125">Rubriques relatives aux tâches qui montrent comment utiliser l’API de mastérisation d’image.</span><span class="sxs-lookup"><span data-stu-id="f4bce-125">Task-related topics that demonstrate how to use the Image Mastering API.</span></span><br/>   |
| [<span data-ttu-id="f4bce-126">Référence IMAPi</span><span class="sxs-lookup"><span data-stu-id="f4bce-126">IMAPI Reference</span></span>](imapi-reference.md)<br/> | <span data-ttu-id="f4bce-127">Description détaillée des interfaces IMAPi et d’autres éléments de programmation.</span><span class="sxs-lookup"><span data-stu-id="f4bce-127">Detailed descriptions of IMAPI interfaces and other programming elements.</span></span><br/>  |



 

## <a name="additional-resources"></a><span data-ttu-id="f4bce-128">Ressources supplémentaires</span><span class="sxs-lookup"><span data-stu-id="f4bce-128">Additional resources</span></span>

<span data-ttu-id="f4bce-129">Vous trouverez des informations supplémentaires sur IMAPi et d’autres sujets connexes aux emplacements suivants :</span><span class="sxs-lookup"><span data-stu-id="f4bce-129">Further information regarding IMAPI and other related subjects can be found at the following locations:</span></span>



| <span data-ttu-id="f4bce-130">Rubrique</span><span class="sxs-lookup"><span data-stu-id="f4bce-130">Topic</span></span>                                                                                                 | <span data-ttu-id="f4bce-131">Description</span><span class="sxs-lookup"><span data-stu-id="f4bce-131">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                   |
|--------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f4bce-132">Blog Microsoft Optical Storage</span><span class="sxs-lookup"><span data-stu-id="f4bce-132">Microsoft Optical Storage Blog</span></span>](/archive/blogs/opticalstorage/)                | <span data-ttu-id="f4bce-133">Met en évidence les rubriques qui se concentrent sur l’implémentation de l’API de mastérisation d’image dans les scénarios de développement réel.</span><span class="sxs-lookup"><span data-stu-id="f4bce-133">Highlights topics that focus on the implementation of the Image Mastering API in real world development scenarios.</span></span>                                                                                                                                                                                                                                                 |
| [<span data-ttu-id="f4bce-134">Forum de discussion sur les plateformes optiques</span><span class="sxs-lookup"><span data-stu-id="f4bce-134">Optical Platform Discussion Forum</span></span>](https://social.msdn.microsoft.com/forums/windowsopticalplatform/threads/)              | <span data-ttu-id="f4bce-135">Discutez des problèmes de CDROM.SYS, IMAPIv2 et de système de fichiers en direct.</span><span class="sxs-lookup"><span data-stu-id="f4bce-135">Discuss CDROM.SYS, IMAPIv2 and Live File System issues.</span></span> <span data-ttu-id="f4bce-136">Ce forum se concentre sur les rubriques au niveau du système et est destiné aux développeurs d’applications plutôt qu’à utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="f4bce-136">This forum focuses on system-level topics and is intended for application developers rather than endusers.</span></span>                                                                                                                                                                                                 |
| [<span data-ttu-id="f4bce-137">Comité technique de T10</span><span class="sxs-lookup"><span data-stu-id="f4bce-137">T10 Technical Committee</span></span>](https://www.t10.org/)                       | <span data-ttu-id="f4bce-138">Un Comité technique du Comité InterNational des normes des technologies de l’information (INCITS, prononcé « Insights »).</span><span class="sxs-lookup"><span data-stu-id="f4bce-138">A Technical Committee of the InterNational Committee on Information Technology Standards (INCITS, pronounced "insights").</span></span> <span data-ttu-id="f4bce-139">L’INCITS est homologué par et fonctionne selon les règles approuvées par le American National Standards Institute (ANSI).</span><span class="sxs-lookup"><span data-stu-id="f4bce-139">INCITS is accredited by, and operates under rules that are approved by, the American National Standards Institute (ANSI).</span></span> <span data-ttu-id="f4bce-140">Ces règles sont conçues pour garantir que les normes volontaires sont développées par le consensus des groupes de l’industrie.</span><span class="sxs-lookup"><span data-stu-id="f4bce-140">These rules are designed to ensure that voluntary standards are developed by the consensus of industry groups.</span></span> |
| [<span data-ttu-id="f4bce-141">Association de technologie de stockage optique (OSTA)</span><span class="sxs-lookup"><span data-stu-id="f4bce-141">Optical Storage Technology Association (OSTA)</span></span>](http://www.osta.org/) | <span data-ttu-id="f4bce-142">Travaille à la mise en forme du futur du secteur grâce à des réunions régulières d’applications de stockage optique commercial (COSA), de compatibilité DVD, de marketing, MPV (MusicPhotoVideo), de comités UDF et d’un nouveau Comité Blue laser ad hoc.</span><span class="sxs-lookup"><span data-stu-id="f4bce-142">Works to shape the future of the industry through regular meetings of Commercial Optical Storage Applications (COSA), DVD Compatibility, Marketing, MPV (MusicPhotoVideo), UDF committees, and a new adhoc Blue Laser committee.</span></span> <span data-ttu-id="f4bce-143">Les sociétés intéressées du monde entier sont invitées à rejoindre l’organisation et à participer à ses comités et à ses programmes.</span><span class="sxs-lookup"><span data-stu-id="f4bce-143">Interested companies worldwide are invited to join the organization and participate in its committees and programs.</span></span>               |



 

 

