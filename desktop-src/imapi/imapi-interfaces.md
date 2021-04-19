---
title: Interfaces IMAPi
description: Les tableaux suivants identifient et décrivent brièvement les interfaces utilisées par les développeurs C/C++ et l’objet de script associé. Préfixez le nom de l’objet dans la table avec \ 0034 ; IMAPI2. \ 0034 ; pour qualifier complètement le nom de l’objet lors de la création de l’objet dans le script.
ms.assetid: dba81a45-34a8-4b49-9ccb-d61a7e7ee1f6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bac989a9871b761a1f1700ec599cc51affd30b2e
ms.sourcegitcommit: 927b9c371f75f52b8011483edf3a4ba37d11ebe4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/11/2020
ms.locfileid: "106538589"
---
# <a name="imapi-interfaces"></a><span data-ttu-id="57a9c-105">Interfaces IMAPi</span><span class="sxs-lookup"><span data-stu-id="57a9c-105">IMAPI Interfaces</span></span>

<span data-ttu-id="57a9c-106">Les tableaux suivants identifient et décrivent brièvement les interfaces utilisées par les développeurs C/C++ et l’objet de script associé.</span><span class="sxs-lookup"><span data-stu-id="57a9c-106">The following tables identify and briefly describe the interfaces used C/C++ developers and the associated scripting object.</span></span> <span data-ttu-id="57a9c-107">Préfixez le nom de l’objet dans la table avec « IMAPI2 ».</span><span class="sxs-lookup"><span data-stu-id="57a9c-107">Prefix the object name in the table with "IMAPI2."</span></span> <span data-ttu-id="57a9c-108">pour qualifier complètement le nom de l’objet lors de la création de l’objet dans le script.</span><span class="sxs-lookup"><span data-stu-id="57a9c-108">to fully qualify the object name when creating the object in script.</span></span>

<span data-ttu-id="57a9c-109">Le tableau suivant répertorie les interfaces associées aux appareils, au moteur de gravure et aux Writers de format et gomme.</span><span class="sxs-lookup"><span data-stu-id="57a9c-109">The following table lists the interfaces associated with devices, the burn engine, and the format writers and eraser.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="57a9c-110">Interface</span><span class="sxs-lookup"><span data-stu-id="57a9c-110">Interface</span></span></td>
<td><span data-ttu-id="57a9c-111">Object</span><span class="sxs-lookup"><span data-stu-id="57a9c-111">Object</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="57a9c-112">Moteur de gravure de bas niveau.</span><span class="sxs-lookup"><span data-stu-id="57a9c-112">Low-level burn engine.</span></span>
<ul>
<li><span data-ttu-id="57a9c-113"><a href="/windows/desktop/api/imapi2/nn-imapi2-dwriteengine2events"><strong>DWriteEngine2Events</strong></a></span><span class="sxs-lookup"><span data-stu-id="57a9c-113"><a href="/windows/desktop/api/imapi2/nn-imapi2-dwriteengine2events"><strong>DWriteEngine2Events</strong></a></span></span></li>
<li><span data-ttu-id="57a9c-114"><a href="/windows/desktop/api/imapi2/nn-imapi2-iwriteengine2"><strong>IWriteEngine2</strong></a></span><span class="sxs-lookup"><span data-stu-id="57a9c-114"><a href="/windows/desktop/api/imapi2/nn-imapi2-iwriteengine2"><strong>IWriteEngine2</strong></a></span></span></li>
<li><span data-ttu-id="57a9c-115"><a href="/windows/desktop/api/imapi2/nn-imapi2-iwriteengine2eventargs"><strong>IWriteEngine2EventArgs</strong></a></span><span class="sxs-lookup"><span data-stu-id="57a9c-115"><a href="/windows/desktop/api/imapi2/nn-imapi2-iwriteengine2eventargs"><strong>IWriteEngine2EventArgs</strong></a></span></span></li>
</ul></td>
<td><span data-ttu-id="57a9c-116">MsftWriteEngine2</span><span class="sxs-lookup"><span data-stu-id="57a9c-116">MsftWriteEngine2</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="57a9c-117">Enregistreur d’images principal.</span><span class="sxs-lookup"><span data-stu-id="57a9c-117">Main image writer.</span></span>
<ul>
<li><span data-ttu-id="57a9c-118"><a href="/windows/desktop/api/imapi2/nn-imapi2-ddiscformat2dataevents"><strong>DDiscFormat2DataEvents</strong></a></span><span class="sxs-lookup"><span data-stu-id="57a9c-118"><a href="/windows/desktop/api/imapi2/nn-imapi2-ddiscformat2dataevents"><strong>DDiscFormat2DataEvents</strong></a></span></span></li>
<li><span data-ttu-id="57a9c-119"><a href="/windows/desktop/api/imapi2/nn-imapi2-idiscformat2data"><strong>IDiscFormat2Data</strong></a></span><span class="sxs-lookup"><span data-stu-id="57a9c-119"><a href="/windows/desktop/api/imapi2/nn-imapi2-idiscformat2data"><strong>IDiscFormat2Data</strong></a></span></span></li>
<li><span data-ttu-id="57a9c-120"><a href="/windows/desktop/api/imapi2/nn-imapi2-idiscformat2dataeventargs"><strong>IDiscFormat2DataEventArgs</strong></a></span><span class="sxs-lookup"><span data-stu-id="57a9c-120"><a href="/windows/desktop/api/imapi2/nn-imapi2-idiscformat2dataeventargs"><strong>IDiscFormat2DataEventArgs</strong></a></span></span></li>
</ul></td>
<td><span data-ttu-id="57a9c-121">MsftDiscFormat2Data</span><span class="sxs-lookup"><span data-stu-id="57a9c-121">MsftDiscFormat2Data</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="57a9c-122">Effaceur de disque.</span><span class="sxs-lookup"><span data-stu-id="57a9c-122">Disc eraser.</span></span>
<ul>
<li><span data-ttu-id="57a9c-123"><a href="/windows/desktop/api/imapi2/nn-imapi2-ddiscformat2eraseevents"><strong>DDiscFormat2EraseEvents</strong></a></span><span class="sxs-lookup"><span data-stu-id="57a9c-123"><a href="/windows/desktop/api/imapi2/nn-imapi2-ddiscformat2eraseevents"><strong>DDiscFormat2EraseEvents</strong></a></span></span></li>
<li><span data-ttu-id="57a9c-124"><a href="/windows/desktop/api/imapi2/nn-imapi2-idiscformat2erase"><strong>IDiscFormat2Erase</strong></a></span><span class="sxs-lookup"><span data-stu-id="57a9c-124"><a href="/windows/desktop/api/imapi2/nn-imapi2-idiscformat2erase"><strong>IDiscFormat2Erase</strong></a></span></span></li>
</ul></td>
<td><span data-ttu-id="57a9c-125">MsftDiscFormat2Erase</span><span class="sxs-lookup"><span data-stu-id="57a9c-125">MsftDiscFormat2Erase</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="57a9c-126">Enregistreur d’images brutes.</span><span class="sxs-lookup"><span data-stu-id="57a9c-126">Raw image writer.</span></span>
<ul>
<li><span data-ttu-id="57a9c-127"><a href="/windows/desktop/api/imapi2/nn-imapi2-ddiscformat2rawcdevents"><strong>DDiscFormat2RawCDEvents</strong></a></span><span class="sxs-lookup"><span data-stu-id="57a9c-127"><a href="/windows/desktop/api/imapi2/nn-imapi2-ddiscformat2rawcdevents"><strong>DDiscFormat2RawCDEvents</strong></a></span></span></li>
<li><span data-ttu-id="57a9c-128"><a href="/windows/desktop/api/imapi2/nn-imapi2-idiscformat2rawcd"><strong>IDiscFormat2RawCD</strong></a></span><span class="sxs-lookup"><span data-stu-id="57a9c-128"><a href="/windows/desktop/api/imapi2/nn-imapi2-idiscformat2rawcd"><strong>IDiscFormat2RawCD</strong></a></span></span></li>
<li><span data-ttu-id="57a9c-129"><a href="/windows/desktop/api/imapi2/nn-imapi2-idiscformat2rawcdeventargs"><strong>IDiscFormat2RawCDEventArgs</strong></a></span><span class="sxs-lookup"><span data-stu-id="57a9c-129"><a href="/windows/desktop/api/imapi2/nn-imapi2-idiscformat2rawcdeventargs"><strong>IDiscFormat2RawCDEventArgs</strong></a></span></span></li>
</ul></td>
<td><span data-ttu-id="57a9c-130">MsftDiscFormat2RawCD</span><span class="sxs-lookup"><span data-stu-id="57a9c-130">MsftDiscFormat2RawCD</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="57a9c-131">Enregistreur d’images Track-on-once.</span><span class="sxs-lookup"><span data-stu-id="57a9c-131">Track-At-Once image writer.</span></span>
<ul>
<li><span data-ttu-id="57a9c-132"><a href="/windows/desktop/api/imapi2/nn-imapi2-ddiscformat2trackatonceevents"><strong>DDiscFormat2TrackAtOnceEvents</strong></a></span><span class="sxs-lookup"><span data-stu-id="57a9c-132"><a href="/windows/desktop/api/imapi2/nn-imapi2-ddiscformat2trackatonceevents"><strong>DDiscFormat2TrackAtOnceEvents</strong></a></span></span></li>
<li><span data-ttu-id="57a9c-133"><a href="/windows/desktop/api/imapi2/nn-imapi2-idiscformat2trackatonce"><strong>IDiscFormat2TrackAtOnce</strong></a></span><span class="sxs-lookup"><span data-stu-id="57a9c-133"><a href="/windows/desktop/api/imapi2/nn-imapi2-idiscformat2trackatonce"><strong>IDiscFormat2TrackAtOnce</strong></a></span></span></li>
<li><span data-ttu-id="57a9c-134"><a href="/windows/desktop/api/imapi2/nn-imapi2-idiscformat2trackatonceeventargs"><strong>IDiscFormat2TrackAtOnceEventArgs</strong></a></span><span class="sxs-lookup"><span data-stu-id="57a9c-134"><a href="/windows/desktop/api/imapi2/nn-imapi2-idiscformat2trackatonceeventargs"><strong>IDiscFormat2TrackAtOnceEventArgs</strong></a></span></span></li>
</ul></td>
<td><span data-ttu-id="57a9c-135">MsftDiscFormat2TrackAtOnce</span><span class="sxs-lookup"><span data-stu-id="57a9c-135">MsftDiscFormat2TrackAtOnce</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="57a9c-136">Énumération des périphériques de disque dans la liste des matériels du système.</span><span class="sxs-lookup"><span data-stu-id="57a9c-136">Enumeration of disc devices in the system hardware list.</span></span>
<ul>
<li><span data-ttu-id="57a9c-137"><a href="/windows/desktop/api/imapi2/nn-imapi2-idiscmaster2"><strong>IDiscMaster2</strong></a></span><span class="sxs-lookup"><span data-stu-id="57a9c-137"><a href="/windows/desktop/api/imapi2/nn-imapi2-idiscmaster2"><strong>IDiscMaster2</strong></a></span></span></li>
</ul></td>
<td><span data-ttu-id="57a9c-138">MsftDiscMaster2</span><span class="sxs-lookup"><span data-stu-id="57a9c-138">MsftDiscMaster2</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="57a9c-139">Délégué de notification pour l’objet MsftDiscMaster2.</span><span class="sxs-lookup"><span data-stu-id="57a9c-139">Notification delegate for the MsftDiscMaster2 object.</span></span>
<ul>
<li><span data-ttu-id="57a9c-140"><a href="/windows/desktop/api/imapi2/nn-imapi2-ddiscmaster2events"><strong>DDiscMaster2Events</strong></a></span><span class="sxs-lookup"><span data-stu-id="57a9c-140"><a href="/windows/desktop/api/imapi2/nn-imapi2-ddiscmaster2events"><strong>DDiscMaster2Events</strong></a></span></span></li>
</ul></td>
<td><span data-ttu-id="57a9c-141">DDiscMaster2Events</span><span class="sxs-lookup"><span data-stu-id="57a9c-141">DDiscMaster2Events</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="57a9c-142">Appareil d’enregistrement individuel.</span><span class="sxs-lookup"><span data-stu-id="57a9c-142">Individual recording device.</span></span>
<ul>
<li><span data-ttu-id="57a9c-143"><a href="/windows/desktop/api/imapi2/nn-imapi2-idiscrecorder2"><strong>IDiscRecorder2</strong></a></span><span class="sxs-lookup"><span data-stu-id="57a9c-143"><a href="/windows/desktop/api/imapi2/nn-imapi2-idiscrecorder2"><strong>IDiscRecorder2</strong></a></span></span></li>
<li><span data-ttu-id="57a9c-144"><a href="/windows/desktop/api/imapi2/nn-imapi2-idiscrecorder2ex"><strong>IDiscRecorder2Ex</strong></a></span><span class="sxs-lookup"><span data-stu-id="57a9c-144"><a href="/windows/desktop/api/imapi2/nn-imapi2-idiscrecorder2ex"><strong>IDiscRecorder2Ex</strong></a></span></span></li>
</ul></td>
<td><span data-ttu-id="57a9c-145">MsftDiscRecorder2</span><span class="sxs-lookup"><span data-stu-id="57a9c-145">MsftDiscRecorder2</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="57a9c-146">Attributs d’écriture de périphérique, y compris le type de média, la vitesse d’écriture et le type de contrôle de vélocité angulaire.</span><span class="sxs-lookup"><span data-stu-id="57a9c-146">Device writing attributes, including the media type, writing speed, and type of angular velocity control.</span></span>
<ul>
<li><span data-ttu-id="57a9c-147"><a href="/windows/desktop/api/imapi2/nn-imapi2-iwritespeeddescriptor"><strong>IWriteSpeedDescriptor</strong></a></span><span class="sxs-lookup"><span data-stu-id="57a9c-147"><a href="/windows/desktop/api/imapi2/nn-imapi2-iwritespeeddescriptor"><strong>IWriteSpeedDescriptor</strong></a></span></span></li>
</ul></td>
<td><span data-ttu-id="57a9c-148">MsftWriteSpeedDescriptor</span><span class="sxs-lookup"><span data-stu-id="57a9c-148">MsftWriteSpeedDescriptor</span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="57a9c-149">Le tableau suivant répertorie les interfaces du système de fichiers.</span><span class="sxs-lookup"><span data-stu-id="57a9c-149">The following table lists the file system interfaces.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="57a9c-150">Interface</span><span class="sxs-lookup"><span data-stu-id="57a9c-150">Interface</span></span></td>
<td><span data-ttu-id="57a9c-151">Object</span><span class="sxs-lookup"><span data-stu-id="57a9c-151">Object</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="57a9c-152">Flux et propriétés de l’image de démarrage pour l’intégration de l’image de démarrage dans l’image de disque.</span><span class="sxs-lookup"><span data-stu-id="57a9c-152">Boot image stream and properties for integrating the bootable image in the disc image.</span></span>
<ul>
<li><span data-ttu-id="57a9c-153"><a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ibootoptions"><strong>IBootOptions</strong></a></span><span class="sxs-lookup"><span data-stu-id="57a9c-153"><a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ibootoptions"><strong>IBootOptions</strong></a></span></span></li>
</ul></td>
<td><span data-ttu-id="57a9c-154">BootOptions</span><span class="sxs-lookup"><span data-stu-id="57a9c-154">BootOptions</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="57a9c-155">Image et propriétés du système de fichiers.</span><span class="sxs-lookup"><span data-stu-id="57a9c-155">File system image and properties.</span></span> <span data-ttu-id="57a9c-156">Cet objet comprend toutes les pistes et les références à l’image de démarrage et à l’image de résultat.</span><span class="sxs-lookup"><span data-stu-id="57a9c-156">This object includes all tracks, and references to the boot image and result image.</span></span>
<ul>
<li><span data-ttu-id="57a9c-157"><a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-dfilesystemimageevents"><strong>DFileSystemImageEvents</strong></a></span><span class="sxs-lookup"><span data-stu-id="57a9c-157"><a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-dfilesystemimageevents"><strong>DFileSystemImageEvents</strong></a></span></span></li>
<li><span data-ttu-id="57a9c-158"><a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-dfilesystemimageimportevents"><strong>DFileSystemImageImportEvents</strong></a></span><span class="sxs-lookup"><span data-stu-id="57a9c-158"><a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-dfilesystemimageimportevents"><strong>DFileSystemImageImportEvents</strong></a></span></span></li>
<li><span data-ttu-id="57a9c-159"><a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ifilesystemimage"><strong>IFileSystemImage</strong></a></span><span class="sxs-lookup"><span data-stu-id="57a9c-159"><a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ifilesystemimage"><strong>IFileSystemImage</strong></a></span></span></li>
<li><span data-ttu-id="57a9c-160"><a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ifilesystemimage2"><strong>IFileSystemImage2</strong></a></span><span class="sxs-lookup"><span data-stu-id="57a9c-160"><a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ifilesystemimage2"><strong>IFileSystemImage2</strong></a></span></span></li>
<li><span data-ttu-id="57a9c-161"><a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ifilesystemimage3"><strong>IFileSystemImage3</strong></a></span><span class="sxs-lookup"><span data-stu-id="57a9c-161"><a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ifilesystemimage3"><strong>IFileSystemImage3</strong></a></span></span></li>
</ul></td>
<td><span data-ttu-id="57a9c-162">CFileSystemImage</span><span class="sxs-lookup"><span data-stu-id="57a9c-162">CFileSystemImage</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="57a9c-163">Conteneur du flux de données fourni par l’objet de système de fichiers.</span><span class="sxs-lookup"><span data-stu-id="57a9c-163">Container of the data stream provided by the file system object.</span></span>
<ul>
<li><span data-ttu-id="57a9c-164"><a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ifilesystemimageresult"><strong>IFileSystemImageResult</strong></a></span><span class="sxs-lookup"><span data-stu-id="57a9c-164"><a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ifilesystemimageresult"><strong>IFileSystemImageResult</strong></a></span></span></li>
</ul></td>
<td><span data-ttu-id="57a9c-165">FileSystemImageResult</span><span class="sxs-lookup"><span data-stu-id="57a9c-165">FileSystemImageResult</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="57a9c-166">Élément d’annuaire dans l’image du système de fichiers.</span><span class="sxs-lookup"><span data-stu-id="57a9c-166">Directory item in the file system image.</span></span>
<ul>
<li><span data-ttu-id="57a9c-167"><a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ifsidirectoryitem"><strong>IFsiDirectoryItem</strong></a></span><span class="sxs-lookup"><span data-stu-id="57a9c-167"><a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ifsidirectoryitem"><strong>IFsiDirectoryItem</strong></a></span></span></li>
<li><span data-ttu-id="57a9c-168"><a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ifsidirectoryitem2"><strong>IFsiDirectoryItem2</strong></a></span><span class="sxs-lookup"><span data-stu-id="57a9c-168"><a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ifsidirectoryitem2"><strong>IFsiDirectoryItem2</strong></a></span></span></li>
</ul></td>
<td><span data-ttu-id="57a9c-169">FsiDirectoryItem</span><span class="sxs-lookup"><span data-stu-id="57a9c-169">FsiDirectoryItem</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="57a9c-170">Élément de fichier dans l’image du système de fichiers.</span><span class="sxs-lookup"><span data-stu-id="57a9c-170">File item in the file system image.</span></span>
<ul>
<li><span data-ttu-id="57a9c-171"><a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ifsifileitem"><strong>IFsiFileItem</strong></a></span><span class="sxs-lookup"><span data-stu-id="57a9c-171"><a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ifsifileitem"><strong>IFsiFileItem</strong></a></span></span></li>
<li><span data-ttu-id="57a9c-172"><a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ifsifileitem2"><strong>IFsiFileItem2</strong></a></span><span class="sxs-lookup"><span data-stu-id="57a9c-172"><a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ifsifileitem2"><strong>IFsiFileItem2</strong></a></span></span></li>
</ul></td>
<td><span data-ttu-id="57a9c-173">FsiFileItem</span><span class="sxs-lookup"><span data-stu-id="57a9c-173">FsiFileItem</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="57a9c-174">Interface contenant des propriétés communes aux éléments de fichier et de répertoire.</span><span class="sxs-lookup"><span data-stu-id="57a9c-174">Interface containing properties common to both file and directory items.</span></span>
<ul>
<li><span data-ttu-id="57a9c-175"><a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ifsiitem"><strong>IFsiItem</strong></a></span><span class="sxs-lookup"><span data-stu-id="57a9c-175"><a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ifsiitem"><strong>IFsiItem</strong></a></span></span></li>
</ul></td>
<td><span data-ttu-id="57a9c-176">FsiItem</span><span class="sxs-lookup"><span data-stu-id="57a9c-176">FsiItem</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="57a9c-177">Création d’images CD BRUTes.</span><span class="sxs-lookup"><span data-stu-id="57a9c-177">RAW CD image creation.</span></span>
<ul>
<li><span data-ttu-id="57a9c-178"><a href="/windows/desktop/api/imapi2/nn-imapi2-irawcdimagecreator"><strong>IRawCDImageCreator</strong></a></span><span class="sxs-lookup"><span data-stu-id="57a9c-178"><a href="/windows/desktop/api/imapi2/nn-imapi2-irawcdimagecreator"><strong>IRawCDImageCreator</strong></a></span></span></li>
<li><span data-ttu-id="57a9c-179"><a href="/windows/desktop/api/imapi2/nn-imapi2-irawcdimagetrackinfo"><strong>IRawCDImageTrackInfo</strong></a></span><span class="sxs-lookup"><span data-stu-id="57a9c-179"><a href="/windows/desktop/api/imapi2/nn-imapi2-irawcdimagetrackinfo"><strong>IRawCDImageTrackInfo</strong></a></span></span></li>
</ul></td>
<td><span data-ttu-id="57a9c-180">MsftRawCDImageCreator</span><span class="sxs-lookup"><span data-stu-id="57a9c-180">MsftRawCDImageCreator</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="57a9c-181">Objet d’assistance de l’objet de flux pour concaténer plusieurs flux.</span><span class="sxs-lookup"><span data-stu-id="57a9c-181">Stream object helper object to concatenate multiple streams.</span></span>
<ul>
<li><span data-ttu-id="57a9c-182"><a href="/windows/desktop/api/imapi2/nn-imapi2-istreamconcatenate"><strong>IStreamConcatenate</strong></a></span><span class="sxs-lookup"><span data-stu-id="57a9c-182"><a href="/windows/desktop/api/imapi2/nn-imapi2-istreamconcatenate"><strong>IStreamConcatenate</strong></a></span></span></li>
</ul></td>
<td><span data-ttu-id="57a9c-183">MsftStreamConcatenate</span><span class="sxs-lookup"><span data-stu-id="57a9c-183">MsftStreamConcatenate</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="57a9c-184">Flux entrelacé à ajouter à l’image disque.</span><span class="sxs-lookup"><span data-stu-id="57a9c-184">Interleaved stream to add to the disc image.</span></span>
<ul>
<li><span data-ttu-id="57a9c-185"><a href="/windows/desktop/api/imapi2/nn-imapi2-istreaminterleave"><strong>IStreamInterleave</strong></a></span><span class="sxs-lookup"><span data-stu-id="57a9c-185"><a href="/windows/desktop/api/imapi2/nn-imapi2-istreaminterleave"><strong>IStreamInterleave</strong></a></span></span></li>
</ul></td>
<td><span data-ttu-id="57a9c-186">MsftStreamInterleave</span><span class="sxs-lookup"><span data-stu-id="57a9c-186">MsftStreamInterleave</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="57a9c-187">Flux généré Pseudo-aléatoire.</span><span class="sxs-lookup"><span data-stu-id="57a9c-187">Pseudo-random generated stream.</span></span>
<ul>
<li><span data-ttu-id="57a9c-188"><a href="/windows/desktop/api/imapi2/nn-imapi2-istreampseudorandombased"><strong>IStreamPseudoRandomBased</strong></a></span><span class="sxs-lookup"><span data-stu-id="57a9c-188"><a href="/windows/desktop/api/imapi2/nn-imapi2-istreampseudorandombased"><strong>IStreamPseudoRandomBased</strong></a></span></span></li>
</ul></td>
<td><span data-ttu-id="57a9c-189">MsftStreamPrgn001</span><span class="sxs-lookup"><span data-stu-id="57a9c-189">MsftStreamPrgn001</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="57a9c-190">L’objet de script <strong>MsftStreamZero</strong> n’est pas implémenté en tant qu’interface.</span><span class="sxs-lookup"><span data-stu-id="57a9c-190">The <strong>MsftStreamZero</strong> scripting object is not implemented as an interface.</span></span></td>
<td><span data-ttu-id="57a9c-191"><a href="msftstreamzero.md"><strong>MsftStreamZero</strong></a></span><span class="sxs-lookup"><span data-stu-id="57a9c-191"><a href="msftstreamzero.md"><strong>MsftStreamZero</strong></a></span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="57a9c-192">Le tableau suivant répertorie les interfaces d’assistance.</span><span class="sxs-lookup"><span data-stu-id="57a9c-192">The following table lists helper interfaces.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="57a9c-193">Interface</span><span class="sxs-lookup"><span data-stu-id="57a9c-193">Interface</span></span></td>
<td><span data-ttu-id="57a9c-194">Object</span><span class="sxs-lookup"><span data-stu-id="57a9c-194">Object</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="57a9c-195">Collection de plages de secteurs dans une image de système de fichiers.</span><span class="sxs-lookup"><span data-stu-id="57a9c-195">Collection of sector ranges within a file system image.</span></span>
<ul>
<li><span data-ttu-id="57a9c-196"><a href="/windows/desktop/api/imapi2/nn-imapi2-iblockrange"><strong>IBlockRange</strong></a></span><span class="sxs-lookup"><span data-stu-id="57a9c-196"><a href="/windows/desktop/api/imapi2/nn-imapi2-iblockrange"><strong>IBlockRange</strong></a></span></span></li>
<li><span data-ttu-id="57a9c-197"><a href="/windows/desktop/api/imapi2/nn-imapi2-iblockrangelist"><strong>IBlockRangeList</strong></a></span><span class="sxs-lookup"><span data-stu-id="57a9c-197"><a href="/windows/desktop/api/imapi2/nn-imapi2-iblockrangelist"><strong>IBlockRangeList</strong></a></span></span></li>
</ul></td>
<td><span data-ttu-id="57a9c-198">Aucun objet correspondant</span><span class="sxs-lookup"><span data-stu-id="57a9c-198">No corresponding object</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="57a9c-199">Prise en charge de la vérification de la gravure.</span><span class="sxs-lookup"><span data-stu-id="57a9c-199">Burn verification support.</span></span>
<ul>
<li><span data-ttu-id="57a9c-200"><a href="/windows/desktop/api/imapi2/nn-imapi2-iburnverification"><strong>IBurnVerification</strong></a></span><span class="sxs-lookup"><span data-stu-id="57a9c-200"><a href="/windows/desktop/api/imapi2/nn-imapi2-iburnverification"><strong>IBurnVerification</strong></a></span></span></li>
</ul></td>
<td><span data-ttu-id="57a9c-201">Aucun objet correspondant</span><span class="sxs-lookup"><span data-stu-id="57a9c-201">No corresponding object</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="57a9c-202">Énumérateur de FsiItems pour les applications C/C++.</span><span class="sxs-lookup"><span data-stu-id="57a9c-202">Enumerator of FsiItems for C/C++ applications.</span></span>
<ul>
<li><span data-ttu-id="57a9c-203"><a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ienumfsiitems"><strong>IEnumFsiItems</strong></a></span><span class="sxs-lookup"><span data-stu-id="57a9c-203"><a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ienumfsiitems"><strong>IEnumFsiItems</strong></a></span></span></li>
</ul></td>
<td><span data-ttu-id="57a9c-204">EnumFsiItems</span><span class="sxs-lookup"><span data-stu-id="57a9c-204">EnumFsiItems</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="57a9c-205">Énumérateur de ProgressItems pour les applications C/C++.</span><span class="sxs-lookup"><span data-stu-id="57a9c-205">Enumerator of ProgressItems for C/C++ applications.</span></span>
<ul>
<li><span data-ttu-id="57a9c-206"><a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ienumprogressitems"><strong>IEnumProgressItems</strong></a></span><span class="sxs-lookup"><span data-stu-id="57a9c-206"><a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ienumprogressitems"><strong>IEnumProgressItems</strong></a></span></span></li>
</ul></td>
<td><span data-ttu-id="57a9c-207">EnumProgressItems</span><span class="sxs-lookup"><span data-stu-id="57a9c-207">EnumProgressItems</span></span></td>
</tr>
<tr class="even">
<td><ul>
<li><span data-ttu-id="57a9c-208"><a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ifsinamedstreams"><strong>IFsiNamedStreams</strong></a></span><span class="sxs-lookup"><span data-stu-id="57a9c-208"><a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ifsinamedstreams"><strong>IFsiNamedStreams</strong></a></span></span></li>
</ul></td>
<td><span data-ttu-id="57a9c-209">FsiFileItem2</span><span class="sxs-lookup"><span data-stu-id="57a9c-209">FsiFileItem2</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="57a9c-210">prise en charge de la vérification d’image. ISO.</span><span class="sxs-lookup"><span data-stu-id="57a9c-210">.iso image verification support.</span></span>
<ul>
<li><span data-ttu-id="57a9c-211"><a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-iisoimagemanager"><strong>IIsoImageManager</strong></a></span><span class="sxs-lookup"><span data-stu-id="57a9c-211"><a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-iisoimagemanager"><strong>IIsoImageManager</strong></a></span></span></li>
</ul></td>
<td><span data-ttu-id="57a9c-212">Aucun objet correspondant</span><span class="sxs-lookup"><span data-stu-id="57a9c-212">No corresponding object</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="57a9c-213">Prise en charge de plusieurs sessions.</span><span class="sxs-lookup"><span data-stu-id="57a9c-213">Multiple session support.</span></span>
<ul>
<li><span data-ttu-id="57a9c-214"><a href="/windows/desktop/api/imapi2/nn-imapi2-imultisession"><strong>IMultisession</strong></a></span><span class="sxs-lookup"><span data-stu-id="57a9c-214"><a href="/windows/desktop/api/imapi2/nn-imapi2-imultisession"><strong>IMultisession</strong></a></span></span></li>
</ul></td>
<td><span data-ttu-id="57a9c-215">Aucun objet correspondant</span><span class="sxs-lookup"><span data-stu-id="57a9c-215">No corresponding object</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="57a9c-216">Prise en charge de plusieurs sessions séquentielles.</span><span class="sxs-lookup"><span data-stu-id="57a9c-216">Sequential multiple session support.</span></span>
<ul>
<li><span data-ttu-id="57a9c-217"><a href="/windows/desktop/api/imapi2/nn-imapi2-imultisessionsequential"><strong>IMultisessionSequential</strong></a></span><span class="sxs-lookup"><span data-stu-id="57a9c-217"><a href="/windows/desktop/api/imapi2/nn-imapi2-imultisessionsequential"><strong>IMultisessionSequential</strong></a></span></span></li>
<li><span data-ttu-id="57a9c-218"><a href="/windows/desktop/api/imapi2/nn-imapi2-imultisessionsequential2"><strong>IMultisessionSequential2</strong></a></span><span class="sxs-lookup"><span data-stu-id="57a9c-218"><a href="/windows/desktop/api/imapi2/nn-imapi2-imultisessionsequential2"><strong>IMultisessionSequential2</strong></a></span></span></li>
</ul></td>
<td><span data-ttu-id="57a9c-219">MsftMultisessionSequential</span><span class="sxs-lookup"><span data-stu-id="57a9c-219">MsftMultisessionSequential</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="57a9c-220">Nom de fichier et blocs associés dans l’image de résultat.</span><span class="sxs-lookup"><span data-stu-id="57a9c-220">File name and associated blocks in the result image.</span></span>
<ul>
<li><span data-ttu-id="57a9c-221"><a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-iprogressitem"><strong>IProgressItem</strong></a></span><span class="sxs-lookup"><span data-stu-id="57a9c-221"><a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-iprogressitem"><strong>IProgressItem</strong></a></span></span></li>
</ul></td>
<td><span data-ttu-id="57a9c-222">ProgressItem</span><span class="sxs-lookup"><span data-stu-id="57a9c-222">ProgressItem</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="57a9c-223">Liste des images de résultat, ventilées par nom de fichier et blocs associés.</span><span class="sxs-lookup"><span data-stu-id="57a9c-223">Result image listing, broken down by file name and associated blocks.</span></span>
<ul>
<li><span data-ttu-id="57a9c-224"><a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-iprogressitems"><strong>IProgressItems</strong></a></span><span class="sxs-lookup"><span data-stu-id="57a9c-224"><a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-iprogressitems"><strong>IProgressItems</strong></a></span></span></li>
</ul></td>
<td><span data-ttu-id="57a9c-225">ProgressItems</span><span class="sxs-lookup"><span data-stu-id="57a9c-225">ProgressItems</span></span></td>
</tr>
</tbody>
</table>



 

 

 




