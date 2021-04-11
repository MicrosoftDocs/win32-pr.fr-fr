---
description: Une vérification de redondance cyclique (CRC) de fichiers est disponible avec Windows Installer.
ms.assetid: c895488b-6e60-4175-8865-4ba4b0cb2d9a
title: Vérification des CRC au cours d’une installation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 56e03bb6754b0259aa8b27333c8137408e7dc956
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104204016"
---
# <a name="crc-checking-during-an-installation"></a><span data-ttu-id="56662-103">Vérification des CRC au cours d’une installation</span><span class="sxs-lookup"><span data-stu-id="56662-103">CRC Checking During an Installation</span></span>

<span data-ttu-id="56662-104">Une vérification de redondance cyclique (CRC) de fichiers est disponible avec Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="56662-104">A Cyclic Redundancy Check (CRC) of files is available with Windows Installer.</span></span> <span data-ttu-id="56662-105">La vérification du CRC est un mécanisme de vérification des erreurs, similaire à une somme de contrôle, qui permet à une application de déterminer si les informations d’un fichier ont été modifiées.</span><span class="sxs-lookup"><span data-stu-id="56662-105">CRC checking is an error-checking mechanism, similar to a checksum, that enables an application to determine whether the information in a file has been modified.</span></span> <span data-ttu-id="56662-106">Une fois que le Windows Installer terminé de copier un fichier, il obtient une valeur CRC des fichiers source et de destination.</span><span class="sxs-lookup"><span data-stu-id="56662-106">After the Windows Installer finishes copying a file, it gets a CRC value from both the source and destination files.</span></span> <span data-ttu-id="56662-107">Le programme d’installation vérifie le CRC d’origine marqué dans le fichier et le compare au CRC calculé à partir de la copie.</span><span class="sxs-lookup"><span data-stu-id="56662-107">The installer checks the original CRC stamped into the file and compares this to the CRC calculated from the copy.</span></span> <span data-ttu-id="56662-108">La vérification du CRC échoue si la valeur CRC d’origine n’est pas null et est différente du CRC calculé sur la copie.</span><span class="sxs-lookup"><span data-stu-id="56662-108">The CRC check fails if the original CRC value is non-null and is different from the CRC calculated on the copy.</span></span> <span data-ttu-id="56662-109">Si le CRC d’origine est null, aucune vérification n’est effectuée.</span><span class="sxs-lookup"><span data-stu-id="56662-109">If the original CRC is null, no check occurs.</span></span>

<span data-ttu-id="56662-110">La Windows Installer effectue une vérification de CRC sur un fichier dans les cas suivants :</span><span class="sxs-lookup"><span data-stu-id="56662-110">The Windows Installer does a CRC check on a file in the following cases:</span></span>

-   <span data-ttu-id="56662-111">Si la [propriété MSICHECKCRCS](msicheckcrcs.md) est définie et **msidbFileAttributesChecksum** est inclus dans le champ Attributes de l’enregistrement du fichier dans la [table file](file-table.md).</span><span class="sxs-lookup"><span data-stu-id="56662-111">If the [MSICHECKCRCS property](msicheckcrcs.md) is set and **msidbFileAttributesChecksum** is included in the Attributes field of the file's record in the [File table](file-table.md).</span></span> <span data-ttu-id="56662-112">Le programme d’installation effectue la vérification de CRC après l’installation, la duplication ou le déplacement du fichier.</span><span class="sxs-lookup"><span data-stu-id="56662-112">The installer does the CRC check once after installing, duplicating, or moving the file.</span></span>
-   <span data-ttu-id="56662-113">Si la [propriété MSICHECKCRCS](msicheckcrcs.md) est définie et que **msidbFileAttributesChecksum** est inclus dans le champ Attributes de l’enregistrement du fichier dans la [table file](file-table.md), le programme d’installation effectue une vérification des CRC après avoir appliqué un correctif au fichier.</span><span class="sxs-lookup"><span data-stu-id="56662-113">If the [MSICHECKCRCS property](msicheckcrcs.md) is set and **msidbFileAttributesChecksum** is included in the Attributes field of the file's record in the [File table](file-table.md), the installer does a CRC check after patching the file.</span></span>
-   <span data-ttu-id="56662-114">Si le **msidbFileAttributesChecksum** est inclus dans le champ attributs de l’enregistrement du fichier dans la [table file](file-table.md), le programme d’installation effectue une vérification de CRC avant de lier les images.</span><span class="sxs-lookup"><span data-stu-id="56662-114">If the **msidbFileAttributesChecksum** is included in the Attributes field of the file's record in the [File table](file-table.md), the installer does a CRC check before binding images.</span></span>

<span data-ttu-id="56662-115">Si la vérification échoue avant la liaison d’une image, le programme d’installation signale les deux erreurs suivantes dans le fichier journal et poursuit l’installation sans lier le fichier.</span><span class="sxs-lookup"><span data-stu-id="56662-115">If the check fails before binding an image, the installer reports the following two errors in the log file and continues the installation without binding the file.</span></span>



| <span data-ttu-id="56662-116">Code</span><span class="sxs-lookup"><span data-stu-id="56662-116">Code</span></span> | <span data-ttu-id="56662-117">Message</span><span class="sxs-lookup"><span data-stu-id="56662-117">Message</span></span>                                               |
|------|-------------------------------------------------------|
| <span data-ttu-id="56662-118">2941</span><span class="sxs-lookup"><span data-stu-id="56662-118">2941</span></span> | <span data-ttu-id="56662-119">Impossible de calculer le CRC pour le fichier \[ 2 \] .</span><span class="sxs-lookup"><span data-stu-id="56662-119">Unable to compute the CRC for file \[2\].</span></span>             |
| <span data-ttu-id="56662-120">2942</span><span class="sxs-lookup"><span data-stu-id="56662-120">2942</span></span> | <span data-ttu-id="56662-121">L’action BindImage n’a pas été exécutée sur \[ 2 \] fichiers.</span><span class="sxs-lookup"><span data-stu-id="56662-121">BindImage action has not been executed on \[2\] file.</span></span> |



 

<span data-ttu-id="56662-122">Si la vérification échoue après qu’un fichier non compressé a été copié, dupliqué ou corrigé, le programme d’installation signale l’erreur suivante.</span><span class="sxs-lookup"><span data-stu-id="56662-122">If the check fails after an uncompressed file had been copied, duplicated, or patched, the installer reports the following error.</span></span> <span data-ttu-id="56662-123">Cette erreur est également signalée si la vérification échoue après la copie d’un fichier compressé.</span><span class="sxs-lookup"><span data-stu-id="56662-123">This error is also reported if the check fails after a compressed file is copied.</span></span> <span data-ttu-id="56662-124">Si le fichier a l’attribut **msidbFileAttributesVital** , le fichier est considéré comme vital pour l’installation et l’utilisateur a la possibilité de réessayer ou d’annuler l’installation.</span><span class="sxs-lookup"><span data-stu-id="56662-124">If the file has the **msidbFileAttributesVital** attribute, the file is considered vital to the installation and the user gets the option to retry or cancel the installation.</span></span> <span data-ttu-id="56662-125">Si le fichier est marqué comme non critique dans la colonne attributs de la [table file](file-table.md), l’utilisateur peut ignorer l’erreur et continuer, réessayer ou annuler l’installation.</span><span class="sxs-lookup"><span data-stu-id="56662-125">If the file is marked as nonvital in the Attributes column of the [File table](file-table.md), the user may ignore the error and continue, retry, or cancel the installation.</span></span>



| <span data-ttu-id="56662-126">Code</span><span class="sxs-lookup"><span data-stu-id="56662-126">Code</span></span> | <span data-ttu-id="56662-127">Message</span><span class="sxs-lookup"><span data-stu-id="56662-127">Message</span></span>                                         |
|------|-------------------------------------------------|
| <span data-ttu-id="56662-128">1331</span><span class="sxs-lookup"><span data-stu-id="56662-128">1331</span></span> | <span data-ttu-id="56662-129">Échec de la copie correcte du \[ \] fichier 2 : erreur CRC.</span><span class="sxs-lookup"><span data-stu-id="56662-129">Failed to correctly copy \[2\] file: CRC error.</span></span> |



 

<span data-ttu-id="56662-130">Notez que seuls les fichiers non compressés sont déplacés.</span><span class="sxs-lookup"><span data-stu-id="56662-130">Note that only uncompressed files are moved.</span></span> <span data-ttu-id="56662-131">Si la vérification échoue après le déplacement d’un fichier non compressé, le programme d’installation affiche l’erreur suivante.</span><span class="sxs-lookup"><span data-stu-id="56662-131">If the check fails after an uncompressed file is moved, the installer displays the following error.</span></span> <span data-ttu-id="56662-132">Si le fichier a l’attribut **msidbFileAttributesVital** , le fichier est considéré comme vital pour l’installation et l’installation échoue.</span><span class="sxs-lookup"><span data-stu-id="56662-132">If the file has the **msidbFileAttributesVital** attribute, the file is considered vital to the installation and the installation fails.</span></span> <span data-ttu-id="56662-133">Si le fichier est marqué comme non vital dans la colonne attributs de la [table file](file-table.md), l’utilisateur a la possibilité d’annuler ou d’ignorer l’erreur et de poursuivre l’installation.</span><span class="sxs-lookup"><span data-stu-id="56662-133">If the file is marked as nonvital in the Attributes column of the [File table](file-table.md), the user gets the option to cancel or to ignore the error and continue the installation.</span></span>



| <span data-ttu-id="56662-134">Code</span><span class="sxs-lookup"><span data-stu-id="56662-134">Code</span></span> | <span data-ttu-id="56662-135">Message</span><span class="sxs-lookup"><span data-stu-id="56662-135">Message</span></span>                                         |
|------|-------------------------------------------------|
| <span data-ttu-id="56662-136">1332</span><span class="sxs-lookup"><span data-stu-id="56662-136">1332</span></span> | <span data-ttu-id="56662-137">Échec du déplacement du \[ \] fichier 2 : erreur CRC.</span><span class="sxs-lookup"><span data-stu-id="56662-137">Failed to correctly move \[2\] file: CRC error.</span></span> |



 

<span data-ttu-id="56662-138">Si la vérification échoue après l’application d’un correctif à un fichier non compressé, le programme d’installation affiche l’erreur suivante.</span><span class="sxs-lookup"><span data-stu-id="56662-138">If the check fails after an uncompressed file is patched, the installer displays the following error.</span></span> <span data-ttu-id="56662-139">Si le fichier a l’attribut **msidbFileAttributesVital** , le fichier est considéré comme vital pour l’installation et l’installation échoue.</span><span class="sxs-lookup"><span data-stu-id="56662-139">If the file has the **msidbFileAttributesVital** attribute, the file is considered vital to the installation and the installation fails.</span></span> <span data-ttu-id="56662-140">Si le fichier est marqué comme non vital dans la colonne attributs de la [table file](file-table.md), l’utilisateur a la possibilité d’annuler ou d’ignorer l’erreur et de poursuivre l’installation.</span><span class="sxs-lookup"><span data-stu-id="56662-140">If the file is marked as nonvital in the Attributes column of the [File table](file-table.md), the user gets the option to cancel or to ignore the error and continue the installation.</span></span>



| <span data-ttu-id="56662-141">Code</span><span class="sxs-lookup"><span data-stu-id="56662-141">Code</span></span> | <span data-ttu-id="56662-142">Message</span><span class="sxs-lookup"><span data-stu-id="56662-142">Message</span></span>                                          |
|------|--------------------------------------------------|
| <span data-ttu-id="56662-143">1333</span><span class="sxs-lookup"><span data-stu-id="56662-143">1333</span></span> | <span data-ttu-id="56662-144">Échec de la correction \[ du \] fichier 2 : erreur CRC.</span><span class="sxs-lookup"><span data-stu-id="56662-144">Failed to correctly patch \[2\] file: CRC error.</span></span> |



 

 

 



