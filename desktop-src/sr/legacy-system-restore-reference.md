---
title: Référence de restauration du système héritée
description: Cette documentation décrit les détails d’implémentation du référentiel utilisé par une version héritée de la restauration du système. Elle ne s’applique pas à l’implémentation de la restauration du système sur Windows Vista.
ms.assetid: d221e83d-beb0-405c-b332-a3ab8aaef688
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: be8703cbf88b97458f07c616d48405708e25acec
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103839342"
---
# <a name="legacy-system-restore-reference"></a><span data-ttu-id="0cebd-104">Référence de restauration du système héritée</span><span class="sxs-lookup"><span data-stu-id="0cebd-104">Legacy System Restore Reference</span></span>

<span data-ttu-id="0cebd-105">\[Ces informations s’appliquent uniquement à Windows XP avec Service Pack 2 (SP2).\]</span><span class="sxs-lookup"><span data-stu-id="0cebd-105">\[This information applies only to Windows XP with Service Pack 2 (SP2).\]</span></span>

<span data-ttu-id="0cebd-106">Cette documentation décrit les détails d’implémentation du référentiel utilisé par une version héritée de la restauration du système.</span><span class="sxs-lookup"><span data-stu-id="0cebd-106">This documentation describes implementation details of the repository used by a legacy version of System Restore.</span></span> <span data-ttu-id="0cebd-107">Elle ne s’applique pas à l’implémentation de la restauration du système sur Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="0cebd-107">It does not apply to the implementation of System Restore on Windows Vista.</span></span>

## <a name="system-restore-repository-structure"></a><span data-ttu-id="0cebd-108">Structure du référentiel de restauration du système</span><span class="sxs-lookup"><span data-stu-id="0cebd-108">System Restore Repository Structure</span></span>

<span data-ttu-id="0cebd-109">Windows XP avec SP2 contient un référentiel pour la restauration du système dans le dossier suivant :% SYSTEMDRIVE% \\ System Volume Information.</span><span class="sxs-lookup"><span data-stu-id="0cebd-109">Windows XP with SP2 contains a repository for System Restore in the following folder: %SYSTEMDRIVE%\\System Volume Information.</span></span> <span data-ttu-id="0cebd-110">Ce référentiel contient des informations sur les points de restauration, qui sont essentiellement un instantané du système à un moment donné.</span><span class="sxs-lookup"><span data-stu-id="0cebd-110">This repository contains information for restore points, which are essentially a snapshot of the system at a moment in time.</span></span>

<span data-ttu-id="0cebd-111">Le référentiel est structuré comme suit :</span><span class="sxs-lookup"><span data-stu-id="0cebd-111">The repository is structured as follows:</span></span>

<span data-ttu-id="0cebd-112">**System Volume Information**    \*\* \_ Restore {*GUID*}\*\*       **RP1**       **RP2**       **RP *n*-1**       **RP \* n** \*     \*\* \_ Restore {*GUID*}\*\*       **RP1**       **RP2**       **RP *n*-1**       **RP \* n**\*</span><span class="sxs-lookup"><span data-stu-id="0cebd-112">**System Volume Information**    **\_restore{*GUID*}**       **RP1**       **RP2**       **RP *n*-1**       **RP\*n**\*    **\_restore{*GUID*}**       **RP1**       **RP2**       **RP *n*-1**       **RP\*n**\*</span></span>

<span data-ttu-id="0cebd-113">Pour déterminer \_ le dossier Restore {*GUID*} à utiliser, lisez le **GUID** spécifié dans le fichier suivant : SYSTEMROOT% \\ system32 \\ Restore \\MachineGUID.txt.</span><span class="sxs-lookup"><span data-stu-id="0cebd-113">To determine which \_restore{*GUID*} folder to use, read the **GUID** specified in the following file: SYSTEMROOT%\\System32\\Restore\\MachineGUID.txt.</span></span>

<span data-ttu-id="0cebd-114">Dans chaque \_ dossier Restore {*GUID*}, le \_ fichier Driver. cfg contient des informations provenant d’une structure de **\_ \_ configuration persistante SR** définie comme suit :</span><span class="sxs-lookup"><span data-stu-id="0cebd-114">Within each \_restore{*GUID*} folder, the \_driver.cfg file contains information from a **SR\_PERSISTENT\_CONFIG** structure defined as follows:</span></span>

``` syntax
typedef struct _SR_PERSISTENT_CONFIG
 {      
  ULONG Signature;            // Set to CPrs
  ULONG FileNameNumber;       // Number for next temp file 
                              // For example, A0000001 would be 1  
  INT64 FileSeqNumber;        // Next sequence number
  ULONG CurrentRestoreNumber; // For example, RP5 would be 5
 } SR_PERSISTENT_CONFIG, * PSR_PERSISTENT_CONFIG;
```

## <a name="files-contained-in-each-rpnfolder"></a><span data-ttu-id="0cebd-115">Fichiers contenus dans chaque dossier RP *n*</span><span class="sxs-lookup"><span data-stu-id="0cebd-115">Files Contained in Each RP *n* Folder</span></span>

<span data-ttu-id="0cebd-116">Chaque dossier RP *n* contient un dossier d’instantanés qui contient les éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="0cebd-116">Each RP *n* folder contains a Snapshot folder that contains the following:</span></span>

-   <span data-ttu-id="0cebd-117">Instantané des ruches du Registre</span><span class="sxs-lookup"><span data-stu-id="0cebd-117">A snapshot of the registry hives</span></span>
-   <span data-ttu-id="0cebd-118">Dossier de référentiel qui contient un instantané de l’espace de stockage WMI</span><span class="sxs-lookup"><span data-stu-id="0cebd-118">A Repository folder that contains a snapshot of the WMI repository</span></span>
-   <span data-ttu-id="0cebd-119">Instantané de la base de données COM+</span><span class="sxs-lookup"><span data-stu-id="0cebd-119">A snapshot of the COM+ database</span></span>
-   <span data-ttu-id="0cebd-120">Instantané de la base de données IIS</span><span class="sxs-lookup"><span data-stu-id="0cebd-120">A snapshot of the IIS database</span></span>

<span data-ttu-id="0cebd-121">Chaque dossier RP *n* contient un fichier RP. log qui contient des informations générales sur le point de restauration de la structure [**RESTOREPOINTINFOW**](/windows/win32/api/srrestoreptapi/ns-srrestoreptapi-restorepointinfoa) .</span><span class="sxs-lookup"><span data-stu-id="0cebd-121">Each RP *n* folder contains an RP.log file that contains general information about the restore point from the [**RESTOREPOINTINFOW**](/windows/win32/api/srrestoreptapi/ns-srrestoreptapi-restorepointinfoa) structure.</span></span>

<span data-ttu-id="0cebd-122">Chaque dossier RP *n* peut contenir des fichiers utilisés pour suivre les modifications d’un point de restauration.</span><span class="sxs-lookup"><span data-stu-id="0cebd-122">Each RP *n* folder may contain files used to track changes for a restore point.</span></span> <span data-ttu-id="0cebd-123">Le premier fichier est nommé « change. log », le fichier suivant est nommé « change. log. 1 », et ainsi de suite.</span><span class="sxs-lookup"><span data-stu-id="0cebd-123">The first file is named change.log, the next file is named change.log.1, and so on.</span></span> <span data-ttu-id="0cebd-124">Chaque fichier journal de modification contient les structures suivantes :</span><span class="sxs-lookup"><span data-stu-id="0cebd-124">Each change log file contains the following structures:</span></span>

-   [<span data-ttu-id="0cebd-125">**\_ \_ en-tête du journal des modifications**</span><span class="sxs-lookup"><span data-stu-id="0cebd-125">**CHANGE\_LOG\_HEADER**</span></span>](change-log-header.md)
-   <span data-ttu-id="0cebd-126">[**Modifier \_ \_Entrée du journal**](change-log-entry.md)1</span><span class="sxs-lookup"><span data-stu-id="0cebd-126">[**CHANGE\_LOG\_ENTRY**](change-log-entry.md)1</span></span>
-   <span data-ttu-id="0cebd-127">[**Modifier \_ \_Entrée de journal**](change-log-entry.md)2</span><span class="sxs-lookup"><span data-stu-id="0cebd-127">[**CHANGE\_LOG\_ENTRY**](change-log-entry.md)2</span></span>
-   <span data-ttu-id="0cebd-128">...</span><span class="sxs-lookup"><span data-stu-id="0cebd-128">...</span></span>
-   <span data-ttu-id="0cebd-129">[**Modifier \_ \_Entrée de journal**](change-log-entry.md)*n*</span><span class="sxs-lookup"><span data-stu-id="0cebd-129">[**CHANGE\_LOG\_ENTRY**](change-log-entry.md)*n*</span></span>

## <a name="related-topics"></a><span data-ttu-id="0cebd-130">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="0cebd-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0cebd-131">Structures de restauration du système héritées</span><span class="sxs-lookup"><span data-stu-id="0cebd-131">Legacy System Restore Structures</span></span>](legacy-system-restore-structures.md)
</dt> </dl>

 

 




