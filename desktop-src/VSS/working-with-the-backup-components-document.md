---
description: Un demandeur crée un document de composants de sauvegarde au début de l’exécution d’une sauvegarde.
ms.assetid: 5e40e45d-6afa-401a-a6b4-7bec460cb9ec
title: Utilisation du document sur les composants de sauvegarde
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 40d5d3c97696b85d589501f6d3af0b6c7d0e6d47
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106519304"
---
# <a name="working-with-the-backup-components-document"></a><span data-ttu-id="128f5-103">Utilisation du document sur les composants de sauvegarde</span><span class="sxs-lookup"><span data-stu-id="128f5-103">Working with the Backup Components Document</span></span>

<span data-ttu-id="128f5-104">Un demandeur crée un document de composants de sauvegarde au début de l’exécution d’une sauvegarde.</span><span class="sxs-lookup"><span data-stu-id="128f5-104">A requester creates a Backup Components Document at the start of performing a backup.</span></span> <span data-ttu-id="128f5-105">Le document ne contient initialement qu’une description de l’état de l’opération de sauvegarde.</span><span class="sxs-lookup"><span data-stu-id="128f5-105">The document initially contains only a description of the state of the backup operation.</span></span> <span data-ttu-id="128f5-106">Pendant la restauration, le document doit fournir des instructions sur la façon dont un demandeur doit effectuer la copie des fichiers sur le disque.</span><span class="sxs-lookup"><span data-stu-id="128f5-106">During restore, the document should provide instructions on how a requester should proceed in copying files back to disk.</span></span> <span data-ttu-id="128f5-107">Au cours de l’opération de restauration, le document composants de sauvegarde est modifié et contient l’état de cette opération.</span><span class="sxs-lookup"><span data-stu-id="128f5-107">In the course of the restore operation, the Backup Components Document is modified and contains the state of that operation.</span></span>

<span data-ttu-id="128f5-108">Contrairement au document de métadonnées de l’enregistreur, qui est en lecture seule, il existe une fenêtre dans laquelle le document des composants de sauvegarde peut être modifié par les demandeurs et les rédacteurs.</span><span class="sxs-lookup"><span data-stu-id="128f5-108">Unlike the Writer Metadata Document, which is read-only, there is a window in which the Backup Components Document can be modified by both requesters and writers.</span></span> <span data-ttu-id="128f5-109">Le document peut être mis à jour jusqu’à la génération d’un événement [*BackupComplete*](vssgloss-b.md) ou [*BackupShutdown*](vssgloss-b.md) pendant les opérations de sauvegarde et jusqu’à un événement [*postRestore*](vssgloss-p.md) lors de la restauration.</span><span class="sxs-lookup"><span data-stu-id="128f5-109">The document can be updated until the generation of a [*BackupComplete*](vssgloss-b.md) or [*BackupShutdown*](vssgloss-b.md) event during backup operations, and until a [*PostRestore*](vssgloss-p.md) event during restores.</span></span>

<span data-ttu-id="128f5-110">Pour utiliser le document des composants de sauvegarde d’un demandeur, vous devez comprendre les sujets suivants :</span><span class="sxs-lookup"><span data-stu-id="128f5-110">To use a requester's Backup Components Document requires an understanding of the following topics:</span></span>

-   [<span data-ttu-id="128f5-111">Cycle de vie des documents des composants de sauvegarde</span><span class="sxs-lookup"><span data-stu-id="128f5-111">Backup Components Document Life Cycle</span></span>](backup-components-document-life-cycle.md)
-   [<span data-ttu-id="128f5-112">Contenu du document des composants de sauvegarde</span><span class="sxs-lookup"><span data-stu-id="128f5-112">Backup Components Document Contents</span></span>](backup-components-document-contents.md)

 

 



