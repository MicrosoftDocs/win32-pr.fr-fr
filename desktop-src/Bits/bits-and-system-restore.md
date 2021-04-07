---
title: BITS et restauration du système
description: Toutes les versions de BITS n’utilisent pas le même format pour stocker les travaux.
ms.assetid: 97c7fa69-1b35-445b-a0a1-b4d60c3ede42
ms.topic: article
ms.date: 11/29/2018
ms.openlocfilehash: e386084e7556b472c538308b8066875a4287a8d8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104028750"
---
# <a name="bits-and-system-restore"></a><span data-ttu-id="0a9f6-103">BITS et restauration du système</span><span class="sxs-lookup"><span data-stu-id="0a9f6-103">BITS and System Restore</span></span>

<span data-ttu-id="0a9f6-104">Toutes les versions de BITS n’utilisent pas le même format pour stocker les travaux.</span><span class="sxs-lookup"><span data-stu-id="0a9f6-104">Not all versions of BITS use the same format to store jobs.</span></span> <span data-ttu-id="0a9f6-105">Si vous renvoyez l’ordinateur à un point de restauration avant une mise à niveau de BITS, l’ancienne version de BITS ne pourra peut-être pas lire les informations de la tâche actuelle.</span><span class="sxs-lookup"><span data-stu-id="0a9f6-105">If you return the computer to a restore point prior to a BITS upgrade, the old version of BITS may not be able to read the current job information.</span></span> <span data-ttu-id="0a9f6-106">Dans ce cas, le service BITS supprime la liste des tâches et crée une nouvelle liste de travaux vide.</span><span class="sxs-lookup"><span data-stu-id="0a9f6-106">If this happens, BITS will delete the jobs list and create a new empty jobs list.</span></span> <span data-ttu-id="0a9f6-107">Par conséquent, les fichiers temporaires associés à la liste de travaux précédente ne sont pas nettoyés. pour récupérer l’espace disque, vous devez supprimer les fichiers manuellement.</span><span class="sxs-lookup"><span data-stu-id="0a9f6-107">As a result, the temporary files associated with the previous jobs list are not cleaned up; to reclaim the disk space, you must delete the files manually.</span></span>

<span data-ttu-id="0a9f6-108">Les utilisateurs familiarisés avec la ligne de commande Windows peuvent éviter ce problème en utilisant l' [outil Bitsadmin](bitsadmin-tool.md) pour effacer la liste des tâches bits avant d’exécuter la restauration du système.</span><span class="sxs-lookup"><span data-stu-id="0a9f6-108">Users familiar with the Windows command line can avoid this problem by using the [BITSAdmin tool](bitsadmin-tool.md) to clear the BITS jobs list before running System Restore.</span></span> <span data-ttu-id="0a9f6-109">Pour effacer la liste des tâches BITS, exécutez la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="0a9f6-109">To clear the BITS jobs list, run the following command:</span></span>

<span data-ttu-id="0a9f6-110">**Bitsadmin/Reset/ALLUSERS**</span><span class="sxs-lookup"><span data-stu-id="0a9f6-110">**bitsadmin /reset /allusers**</span></span>

<span data-ttu-id="0a9f6-111">Notez que vous devez disposer de privilèges d’administrateur pour exécuter cette commande.</span><span class="sxs-lookup"><span data-stu-id="0a9f6-111">Note that you must have administrator privileges to run this command.</span></span>

 

 




