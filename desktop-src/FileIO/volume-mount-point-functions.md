---
description: Fonctions utilisées pour gérer les dossiers montés.
ms.assetid: 2624500b-11d6-4892-97d7-22efa450f681
title: Fonctions du dossier monté
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f3e984b9bee902f11af9d7b2b956ea0681cd6e7a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104319409"
---
# <a name="mounted-folder-functions"></a><span data-ttu-id="d697c-103">Fonctions du dossier monté</span><span class="sxs-lookup"><span data-stu-id="d697c-103">Mounted Folder Functions</span></span>

<span data-ttu-id="d697c-104">Les fonctions de dossiers montées peuvent être divisées en trois groupes : fonctions à usage général, fonctions utilisées pour rechercher des volumes et fonctions utilisées pour analyser un volume à la recherche de dossiers montés.</span><span class="sxs-lookup"><span data-stu-id="d697c-104">The mounted folder functions can be divided into three groups: general-purpose functions, functions used to scan for volumes, and functions used to scan a volume for mounted folders.</span></span>

## <a name="general-purpose-mounted-folder-functions"></a><span data-ttu-id="d697c-105">Fonctions du dossier monté General-Purpose</span><span class="sxs-lookup"><span data-stu-id="d697c-105">General-Purpose Mounted Folder Functions</span></span>



| <span data-ttu-id="d697c-106">Fonction</span><span class="sxs-lookup"><span data-stu-id="d697c-106">Function</span></span>                                                                     | <span data-ttu-id="d697c-107">Description</span><span class="sxs-lookup"><span data-stu-id="d697c-107">Description</span></span>                                                                                                                                                 |
|------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d697c-108">**DeleteVolumeMountPoint**</span><span class="sxs-lookup"><span data-stu-id="d697c-108">**DeleteVolumeMountPoint**</span></span>](/windows/desktop/api/FileAPI/nf-fileapi-deletevolumemountpointw)                     | <span data-ttu-id="d697c-109">Supprime une lettre de lecteur ou un dossier monté.</span><span class="sxs-lookup"><span data-stu-id="d697c-109">Deletes a drive letter or mounted folder.</span></span>                                                                                                                   |
| [<span data-ttu-id="d697c-110">**GetVolumeNameForVolumeMountPoint**</span><span class="sxs-lookup"><span data-stu-id="d697c-110">**GetVolumeNameForVolumeMountPoint**</span></span>](/windows/desktop/api/FileAPI/nf-fileapi-getvolumenameforvolumemountpointw) | <span data-ttu-id="d697c-111">Récupère le chemin d’accès du GUID du volume associé au point de montage de volume spécifié (lettre de lecteur, chemin d’accès du GUID du volume ou dossier monté).</span><span class="sxs-lookup"><span data-stu-id="d697c-111">Retrieves the volume GUID path for the volume that is associated with the specified volume mount point (drive letter, volume GUID path, or mounted folder).</span></span> |
| [<span data-ttu-id="d697c-112">**GetVolumePathName**</span><span class="sxs-lookup"><span data-stu-id="d697c-112">**GetVolumePathName**</span></span>](/windows/desktop/api/FileAPI/nf-fileapi-getvolumepathnamew)                               | <span data-ttu-id="d697c-113">Récupère le dossier monté associé au volume spécifié.</span><span class="sxs-lookup"><span data-stu-id="d697c-113">Retrieves the mounted folder that is associated with the specified volume.</span></span>                                                                                  |
| [<span data-ttu-id="d697c-114">**SetVolumeMountPoint**</span><span class="sxs-lookup"><span data-stu-id="d697c-114">**SetVolumeMountPoint**</span></span>](/windows/desktop/api/WinBase/nf-winbase-setvolumemountpointa)                           | <span data-ttu-id="d697c-115">Associe un volume à une lettre de lecteur ou à un répertoire sur un autre volume.</span><span class="sxs-lookup"><span data-stu-id="d697c-115">Associates a volume with a drive letter or a directory on another volume.</span></span>                                                                                   |



 

## <a name="volume-scanning-functions"></a><span data-ttu-id="d697c-116">Fonctions Volume-Scanning</span><span class="sxs-lookup"><span data-stu-id="d697c-116">Volume-Scanning Functions</span></span>



| <span data-ttu-id="d697c-117">Fonction</span><span class="sxs-lookup"><span data-stu-id="d697c-117">Function</span></span>                                   | <span data-ttu-id="d697c-118">Description</span><span class="sxs-lookup"><span data-stu-id="d697c-118">Description</span></span>                                                                                                                                    |
|--------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d697c-119">**FindFirstVolume**</span><span class="sxs-lookup"><span data-stu-id="d697c-119">**FindFirstVolume**</span></span>](/windows/desktop/api/FileAPI/nf-fileapi-findfirstvolumew) | <span data-ttu-id="d697c-120">Retourne le nom d’un volume sur un ordinateur.</span><span class="sxs-lookup"><span data-stu-id="d697c-120">Returns the name of a volume on a computer.</span></span> <span data-ttu-id="d697c-121">[**FindFirstVolume**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstvolumew) est utilisé pour commencer à énumérer les volumes d’un ordinateur.</span><span class="sxs-lookup"><span data-stu-id="d697c-121">[**FindFirstVolume**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstvolumew) is used to begin enumerating the volumes of a computer.</span></span> |
| [<span data-ttu-id="d697c-122">**FindNextVolume**</span><span class="sxs-lookup"><span data-stu-id="d697c-122">**FindNextVolume**</span></span>](/windows/desktop/api/FileAPI/nf-fileapi-findnextvolumew)   | <span data-ttu-id="d697c-123">Continue la recherche d’un volume lancée par un appel à [**FindFirstVolume**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstvolumew).</span><span class="sxs-lookup"><span data-stu-id="d697c-123">Continues a volume search started by a call to [**FindFirstVolume**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstvolumew).</span></span>                                                     |
| [<span data-ttu-id="d697c-124">**FindVolumeClose**</span><span class="sxs-lookup"><span data-stu-id="d697c-124">**FindVolumeClose**</span></span>](/windows/desktop/api/FileAPI/nf-fileapi-findvolumeclose) | <span data-ttu-id="d697c-125">Ferme une recherche de volumes.</span><span class="sxs-lookup"><span data-stu-id="d697c-125">Closes a search for volumes.</span></span>                                                                                                                   |



 

## <a name="mounted-folder-scanning-functions"></a><span data-ttu-id="d697c-126">Fonctions d’analyse des dossiers montés</span><span class="sxs-lookup"><span data-stu-id="d697c-126">Mounted Folder Scanning Functions</span></span>



| <span data-ttu-id="d697c-127">Fonction</span><span class="sxs-lookup"><span data-stu-id="d697c-127">Function</span></span>                                                       | <span data-ttu-id="d697c-128">Description</span><span class="sxs-lookup"><span data-stu-id="d697c-128">Description</span></span>                                                                                                                                                                               |
|----------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d697c-129">**FindFirstVolumeMountPoint**</span><span class="sxs-lookup"><span data-stu-id="d697c-129">**FindFirstVolumeMountPoint**</span></span>](/windows/desktop/api/WinBase/nf-winbase-findfirstvolumemountpointa) | <span data-ttu-id="d697c-130">Récupère le nom d’un dossier monté sur le volume spécifié.</span><span class="sxs-lookup"><span data-stu-id="d697c-130">Retrieves the name of a mounted folder on the specified volume.</span></span> <span data-ttu-id="d697c-131">[**FindFirstVolumeMountPoint**](/windows/desktop/api/WinBase/nf-winbase-findfirstvolumemountpointa) est utilisé pour commencer l’analyse des dossiers montés sur un volume.</span><span class="sxs-lookup"><span data-stu-id="d697c-131">[**FindFirstVolumeMountPoint**](/windows/desktop/api/WinBase/nf-winbase-findfirstvolumemountpointa) is used to begin scanning the mounted folders on a volume.</span></span> |
| [<span data-ttu-id="d697c-132">**FindNextVolumeMountPoint**</span><span class="sxs-lookup"><span data-stu-id="d697c-132">**FindNextVolumeMountPoint**</span></span>](/windows/desktop/api/WinBase/nf-winbase-findnextvolumemountpointa)   | <span data-ttu-id="d697c-133">Poursuit une recherche de dossier montée démarrée par un appel à [**FindFirstVolumeMountPoint**](/windows/desktop/api/WinBase/nf-winbase-findfirstvolumemountpointa).</span><span class="sxs-lookup"><span data-stu-id="d697c-133">Continues a mounted folder search started by a call to [**FindFirstVolumeMountPoint**](/windows/desktop/api/WinBase/nf-winbase-findfirstvolumemountpointa).</span></span>                                                                    |
| [<span data-ttu-id="d697c-134">**FindVolumeMountPointClose**</span><span class="sxs-lookup"><span data-stu-id="d697c-134">**FindVolumeMountPointClose**</span></span>](/windows/desktop/api/WinBase/nf-winbase-findvolumemountpointclose) | <span data-ttu-id="d697c-135">Ferme une recherche de dossiers montés.</span><span class="sxs-lookup"><span data-stu-id="d697c-135">Closes a search for mounted folders.</span></span>                                                                                                                                                      |



 

 

 



