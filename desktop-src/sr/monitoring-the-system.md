---
title: Surveillance du système
description: Surveillance du système
ms.assetid: e0318aca-4e3e-4272-ba31-c770d6b05272
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: da7d18f42ac091b9c73c4d9a9ac3929bed235310
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104379561"
---
# <a name="monitoring-the-system"></a><span data-ttu-id="a10e7-103">Surveillance du système</span><span class="sxs-lookup"><span data-stu-id="a10e7-103">Monitoring the System</span></span>

<span data-ttu-id="a10e7-104">La restauration du système dans Windows Vista et les versions ultérieures permet d’enregistrer une copie du volume lors de la génération d’un point de restauration.</span><span class="sxs-lookup"><span data-stu-id="a10e7-104">System Restore in Windows Vista and later saves a copy of the volume when generating a restore point.</span></span> <span data-ttu-id="a10e7-105">La restauration du système nécessite un minimum de 300 Mo d’espace disque libre sur le lecteur système lors de l’installation.</span><span class="sxs-lookup"><span data-stu-id="a10e7-105">System Restore requires a minimum of 300 MB of free disk space on the system drive at installation.</span></span>

<span data-ttu-id="a10e7-106">La restauration du système dans Windows XP surveille un ensemble de base de fichiers système et d’application, en archivant les États de ces fichiers avant que les modifications du système ne soient apportées.</span><span class="sxs-lookup"><span data-stu-id="a10e7-106">System Restore in Windows XP monitors a core set of system and application files, archiving the states of these files before system changes are made.</span></span> <span data-ttu-id="a10e7-107">La restauration du système enregistre également un instantané complet du Registre et certains fichiers système dynamiques.</span><span class="sxs-lookup"><span data-stu-id="a10e7-107">System Restore also saves a full snapshot of the registry and some dynamic system files.</span></span> <span data-ttu-id="a10e7-108">La restauration du système nécessite un minimum de 200 Mo d’espace disque libre sur le lecteur système lors de l’installation.</span><span class="sxs-lookup"><span data-stu-id="a10e7-108">System Restore requires a minimum of 200 MB of free disk space on the system drive at installation.</span></span> <span data-ttu-id="a10e7-109">Lorsque la quantité d’espace disque disponible passe sous 50 Mo sur un lecteur quelconque, la restauration du système passe en mode veille et arrête la création de points de restauration.</span><span class="sxs-lookup"><span data-stu-id="a10e7-109">When the amount of free disk space falls below 50 MB on any drive, System Restore switches to standby mode and stops creating restore points.</span></span> <span data-ttu-id="a10e7-110">Tous les points de restauration sont supprimés à ce moment-là.</span><span class="sxs-lookup"><span data-stu-id="a10e7-110">All restore points are deleted at that time.</span></span> <span data-ttu-id="a10e7-111">La restauration du système réactive et reprend la création de points de restauration dès que 200 Mo d’espace disque sont libres sur le lecteur système.</span><span class="sxs-lookup"><span data-stu-id="a10e7-111">System Restore reactivates and resumes creating restore points as soon as 200 MB of disk space is free on the system drive.</span></span> <span data-ttu-id="a10e7-112">Les fichiers qui sont surveillés ou exclus de l’analyse sont spécifiés dans le fichier% windir% \\ system32 \\ restore \\Filelist.xml.</span><span class="sxs-lookup"><span data-stu-id="a10e7-112">The files that are monitored or excluded from monitoring are specified in the file %windir%\\system32\\restore\\Filelist.xml.</span></span> <span data-ttu-id="a10e7-113">Pour plus d’informations, consultez [extensions de nom de fichier surveillées](monitored-file-extensions.md).</span><span class="sxs-lookup"><span data-stu-id="a10e7-113">For more information, see [Monitored File Name Extensions](monitored-file-extensions.md).</span></span>

 

 




