---
description: Journalisation et rapports d’erreurs
ms.assetid: 162ce34b-cc82-40bb-8422-a639152aee25
title: Journalisation et rapports d’erreurs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1cdc29d32ae26429f2fe23fe88762fabf82185c7
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106514548"
---
# <a name="logging-and-error-reporting"></a><span data-ttu-id="1b5d1-103">Journalisation et rapports d’erreurs</span><span class="sxs-lookup"><span data-stu-id="1b5d1-103">Logging and Error Reporting</span></span>

## <a name="log-file"></a><span data-ttu-id="1b5d1-104">Fichier journal</span><span class="sxs-lookup"><span data-stu-id="1b5d1-104">Log file</span></span>

<span data-ttu-id="1b5d1-105">COMREPL génère un fichier journal contenant les messages d’État et d’erreur.</span><span class="sxs-lookup"><span data-stu-id="1b5d1-105">COMREPL generates a log file containing status and error messages.</span></span> <span data-ttu-id="1b5d1-106">Ce fichier est stocké sur l’ordinateur où COMREPL a été lancé dans% systemdir% \\ com \\ Replication \\ comrepl. log.</span><span class="sxs-lookup"><span data-stu-id="1b5d1-106">This file is stored on the computer where COMREPL was launched in %systemdir%\\com\\replication\\ComRepl.log.</span></span>

<span data-ttu-id="1b5d1-107">Ce fichier journal est effacé au démarrage d’une phase de copie.</span><span class="sxs-lookup"><span data-stu-id="1b5d1-107">This log file is cleared when a copy phase is started.</span></span> <span data-ttu-id="1b5d1-108">L’installation suivante sur les cibles sera ajoutée au fichier.</span><span class="sxs-lookup"><span data-stu-id="1b5d1-108">Subsequent installation on targets will append to the file.</span></span>

## <a name="error-handling"></a><span data-ttu-id="1b5d1-109">Gestion des erreurs</span><span class="sxs-lookup"><span data-stu-id="1b5d1-109">Error handling</span></span>

<span data-ttu-id="1b5d1-110">Les erreurs sont signalées dans le fichier journal décrit ci-dessus.</span><span class="sxs-lookup"><span data-stu-id="1b5d1-110">Errors are noted in the log file described above.</span></span> <span data-ttu-id="1b5d1-111">Des informations détaillées sur l’erreur sont également disponibles dans le journal des événements sur les ordinateurs source ou cible.</span><span class="sxs-lookup"><span data-stu-id="1b5d1-111">Detailed error information may also be found in the event log on source or target computers.</span></span>

## <a name="related-topics"></a><span data-ttu-id="1b5d1-112">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="1b5d1-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1b5d1-113">Gestion des fichiers</span><span class="sxs-lookup"><span data-stu-id="1b5d1-113">File Management</span></span>](file-management.md)
</dt> <dt>

[<span data-ttu-id="1b5d1-114">Phases de réplication</span><span class="sxs-lookup"><span data-stu-id="1b5d1-114">Replication Phases</span></span>](replication-phases.md)
</dt> <dt>

[<span data-ttu-id="1b5d1-115">Utilisation de COMREPL</span><span class="sxs-lookup"><span data-stu-id="1b5d1-115">Using COMREPL</span></span>](using-comrepl.md)
</dt> <dt>

[<span data-ttu-id="1b5d1-116">Ce qui est répliqué</span><span class="sxs-lookup"><span data-stu-id="1b5d1-116">What Gets Replicated</span></span>](what-gets-replicated.md)
</dt> </dl>

 

 



