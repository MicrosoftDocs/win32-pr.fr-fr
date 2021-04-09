---
description: Les enregistreurs peuvent affiner les performances de différents types de sauvegarde au niveau du jeu de fichiers en indiquant à l’aide d’un type de sauvegarde de spécification de fichier, indiqué par un masque de bits ou une opération de bits OR des membres de l' \_ \_ \_ énumération du type de sauvegarde spécification de fichier VSS \_ .
ms.assetid: a3ac69b4-894a-4536-8fab-f45ad7e5118a
title: Prise en charge des schémas au niveau du fichier
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 460d256a3eaa016933e697687d05e26838c14ae2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103952983"
---
# <a name="file-level-schema-support"></a><span data-ttu-id="0a40b-103">Prise en charge des schémas au niveau du fichier</span><span class="sxs-lookup"><span data-stu-id="0a40b-103">File Level Schema Support</span></span>

<span data-ttu-id="0a40b-104">Les enregistreurs peuvent affiner les performances de différents types de sauvegarde au niveau du [*jeu de fichiers*](vssgloss-f.md) en indiquant à l’aide d’un type de sauvegarde de spécification de fichier, indiqué par un masque de bits ou une opération de bits or des membres de l’énumération du type de sauvegarde spécification de [**\_ fichier \_ \_ \_ VSS**](/windows/desktop/api/Vss/ne-vss-vss_file_spec_backup_type) .</span><span class="sxs-lookup"><span data-stu-id="0a40b-104">Writers can fine-tune the performance of various types of backup at the [*file set*](vssgloss-f.md) level by indicating through a file specification backup type, indicated by a bit mask or bitwise OR of the members of the [**VSS\_FILE\_SPEC\_BACKUP\_TYPE**](/windows/desktop/api/Vss/ne-vss-vss_file_spec_backup_type) enumeration.</span></span>

<span data-ttu-id="0a40b-105">Pour les types de sauvegarde spécifiés, le writer indique les éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="0a40b-105">For specified types of backup, the writer indicates the following:</span></span>

-   <span data-ttu-id="0a40b-106">S’il est nécessaire de copier le cliché instantané du volume pour sauvegarder correctement un jeu de fichiers.</span><span class="sxs-lookup"><span data-stu-id="0a40b-106">Whether it will be necessary to shadow copy the volume to properly back up a file set.</span></span> <span data-ttu-id="0a40b-107">Par exemple, si les fichiers d’un jeu de fichiers ne sont pas ouverts exclusivement par le writer et qu’il peut s’assurer qu’il est stable, aucun cliché instantané n’est nécessaire.</span><span class="sxs-lookup"><span data-stu-id="0a40b-107">For instance, if the files in a file set are not exclusively opened by the writer and it can ensure that it is stable, a shadow copy is not needed.</span></span>
-   <span data-ttu-id="0a40b-108">Si le demandeur doit effectuer la sauvegarde de telle sorte que, quelle que soit l’heure de la dernière modification ou d’autres problèmes, la version des fichiers du jeu de fichiers en cours à la sauvegarde sera restaurée.</span><span class="sxs-lookup"><span data-stu-id="0a40b-108">Whether the requester has to perform the backup in such a way that, regardless of last modification time or other issues, the version of the file set's files current at backup will be restored.</span></span> <span data-ttu-id="0a40b-109">En général, cela signifie que le jeu de fichiers est copié dans le cadre de la sauvegarde.</span><span class="sxs-lookup"><span data-stu-id="0a40b-109">Typically, this means that the file set is copied as part of the backup.</span></span>

<span data-ttu-id="0a40b-110">Les valeurs du [**\_ type de \_ \_ sauvegarde spec \_ de fichier VSS**](/windows/desktop/api/Vss/ne-vss-vss_file_spec_backup_type) qui indiquent l’exigence de cliché instantané sont :</span><span class="sxs-lookup"><span data-stu-id="0a40b-110">The values of [**VSS\_FILE\_SPEC\_BACKUP\_TYPE**](/windows/desktop/api/Vss/ne-vss-vss_file_spec_backup_type) that indicate shadow copy requirement are:</span></span>

-   <span data-ttu-id="0a40b-111">\_FSBT VSS \_ tous les \_ instantanés \_ requis</span><span class="sxs-lookup"><span data-stu-id="0a40b-111">VSS\_FSBT\_ALL\_SNAPSHOT\_REQUIRED</span></span>
-   <span data-ttu-id="0a40b-112">\_ \_ instantané complet VSS \_ FSBT \_ requis</span><span class="sxs-lookup"><span data-stu-id="0a40b-112">VSS\_FSBT\_FULL\_SNAPSHOT\_REQUIRED</span></span>
-   <span data-ttu-id="0a40b-113">\_ \_ instantané différentiel FSBT \_ VSS \_ requis</span><span class="sxs-lookup"><span data-stu-id="0a40b-113">VSS\_FSBT\_DIFFERENTIAL\_SNAPSHOT\_REQUIRED</span></span>
-   <span data-ttu-id="0a40b-114">\_instantané FSBT \_ incrémentiel VSS \_ \_ requis</span><span class="sxs-lookup"><span data-stu-id="0a40b-114">VSS\_FSBT\_INCREMENTAL\_SNAPSHOT\_REQUIRED</span></span>
-   <span data-ttu-id="0a40b-115">\_instantané de \_ Journal FSBT VSS \_ \_ requis</span><span class="sxs-lookup"><span data-stu-id="0a40b-115">VSS\_FSBT\_LOG\_SNAPSHOT\_REQUIRED</span></span>

<span data-ttu-id="0a40b-116">Les valeurs du [**\_ type de \_ \_ sauvegarde spécification \_ de fichier VSS**](/windows/desktop/api/Vss/ne-vss-vss_file_spec_backup_type) qui indiquent la nécessité de sauvegarder un fichier sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="0a40b-116">The values of [**VSS\_FILE\_SPEC\_BACKUP\_TYPE**](/windows/desktop/api/Vss/ne-vss-vss_file_spec_backup_type) that indicate the requirement to back up a file are:</span></span>

-   <span data-ttu-id="0a40b-117">\_sauvegarde VSS FSBT \_ toutes les \_ sauvegardes \_ requises</span><span class="sxs-lookup"><span data-stu-id="0a40b-117">VSS\_FSBT\_ALL\_BACKUP\_REQUIRED</span></span>
-   <span data-ttu-id="0a40b-118">\_ \_ sauvegarde complète VSS \_ FSBT \_ requise</span><span class="sxs-lookup"><span data-stu-id="0a40b-118">VSS\_FSBT\_FULL\_BACKUP\_REQUIRED</span></span>
-   <span data-ttu-id="0a40b-119">\_ \_ sauvegarde différentielle FSBT \_ VSS \_ requise</span><span class="sxs-lookup"><span data-stu-id="0a40b-119">VSS\_FSBT\_DIFFERENTIAL\_BACKUP\_REQUIRED</span></span>
-   <span data-ttu-id="0a40b-120">\_sauvegarde VSS FSBT \_ \_ \_ requise</span><span class="sxs-lookup"><span data-stu-id="0a40b-120">VSS\_FSBT\_INCREMENTAL\_BACKUP\_REQUIRED</span></span>
-   <span data-ttu-id="0a40b-121">\_sauvegarde du \_ Journal FSBT VSS \_ \_ requise</span><span class="sxs-lookup"><span data-stu-id="0a40b-121">VSS\_FSBT\_LOG\_BACKUP\_REQUIRED</span></span>

<span data-ttu-id="0a40b-122">Par défaut, les jeux de fichiers sont marqués avec un type de sauvegarde de spécification de fichier VSS \_ FSBT \_ toutes les \_ sauvegardes \_ nécessaires \| VSS \_ FSBT \_ tous les \_ instantanés \_ requis, ce qui signifie qu’un cliché instantané est toujours requis pour gérer les fichiers du jeu de fichiers et que les fichiers doivent être copiés dans tous les types de sauvegardes.</span><span class="sxs-lookup"><span data-stu-id="0a40b-122">By default, file sets are tagged with a file specification backup type of VSS\_FSBT\_ALL\_BACKUP\_REQUIRED \| VSS\_FSBT\_ALL\_SNAPSHOT\_REQUIRED, meaning that a shadow copy is always required in handling the file set's files, and that the files should be copied in all types of backup.</span></span>

 

 



