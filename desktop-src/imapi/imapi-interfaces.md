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
# <a name="imapi-interfaces"></a>Interfaces IMAPi

Les tableaux suivants identifient et décrivent brièvement les interfaces utilisées par les développeurs C/C++ et l’objet de script associé. Préfixez le nom de l’objet dans la table avec « IMAPI2 ». pour qualifier complètement le nom de l’objet lors de la création de l’objet dans le script.

Le tableau suivant répertorie les interfaces associées aux appareils, au moteur de gravure et aux Writers de format et gomme.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Interface</td>
<td>Object</td>
</tr>
<tr class="even">
<td>Moteur de gravure de bas niveau.
<ul>
<li><a href="/windows/desktop/api/imapi2/nn-imapi2-dwriteengine2events"><strong>DWriteEngine2Events</strong></a></li>
<li><a href="/windows/desktop/api/imapi2/nn-imapi2-iwriteengine2"><strong>IWriteEngine2</strong></a></li>
<li><a href="/windows/desktop/api/imapi2/nn-imapi2-iwriteengine2eventargs"><strong>IWriteEngine2EventArgs</strong></a></li>
</ul></td>
<td>MsftWriteEngine2</td>
</tr>
<tr class="odd">
<td>Enregistreur d’images principal.
<ul>
<li><a href="/windows/desktop/api/imapi2/nn-imapi2-ddiscformat2dataevents"><strong>DDiscFormat2DataEvents</strong></a></li>
<li><a href="/windows/desktop/api/imapi2/nn-imapi2-idiscformat2data"><strong>IDiscFormat2Data</strong></a></li>
<li><a href="/windows/desktop/api/imapi2/nn-imapi2-idiscformat2dataeventargs"><strong>IDiscFormat2DataEventArgs</strong></a></li>
</ul></td>
<td>MsftDiscFormat2Data</td>
</tr>
<tr class="even">
<td>Effaceur de disque.
<ul>
<li><a href="/windows/desktop/api/imapi2/nn-imapi2-ddiscformat2eraseevents"><strong>DDiscFormat2EraseEvents</strong></a></li>
<li><a href="/windows/desktop/api/imapi2/nn-imapi2-idiscformat2erase"><strong>IDiscFormat2Erase</strong></a></li>
</ul></td>
<td>MsftDiscFormat2Erase</td>
</tr>
<tr class="odd">
<td>Enregistreur d’images brutes.
<ul>
<li><a href="/windows/desktop/api/imapi2/nn-imapi2-ddiscformat2rawcdevents"><strong>DDiscFormat2RawCDEvents</strong></a></li>
<li><a href="/windows/desktop/api/imapi2/nn-imapi2-idiscformat2rawcd"><strong>IDiscFormat2RawCD</strong></a></li>
<li><a href="/windows/desktop/api/imapi2/nn-imapi2-idiscformat2rawcdeventargs"><strong>IDiscFormat2RawCDEventArgs</strong></a></li>
</ul></td>
<td>MsftDiscFormat2RawCD</td>
</tr>
<tr class="even">
<td>Enregistreur d’images Track-on-once.
<ul>
<li><a href="/windows/desktop/api/imapi2/nn-imapi2-ddiscformat2trackatonceevents"><strong>DDiscFormat2TrackAtOnceEvents</strong></a></li>
<li><a href="/windows/desktop/api/imapi2/nn-imapi2-idiscformat2trackatonce"><strong>IDiscFormat2TrackAtOnce</strong></a></li>
<li><a href="/windows/desktop/api/imapi2/nn-imapi2-idiscformat2trackatonceeventargs"><strong>IDiscFormat2TrackAtOnceEventArgs</strong></a></li>
</ul></td>
<td>MsftDiscFormat2TrackAtOnce</td>
</tr>
<tr class="odd">
<td>Énumération des périphériques de disque dans la liste des matériels du système.
<ul>
<li><a href="/windows/desktop/api/imapi2/nn-imapi2-idiscmaster2"><strong>IDiscMaster2</strong></a></li>
</ul></td>
<td>MsftDiscMaster2</td>
</tr>
<tr class="even">
<td>Délégué de notification pour l’objet MsftDiscMaster2.
<ul>
<li><a href="/windows/desktop/api/imapi2/nn-imapi2-ddiscmaster2events"><strong>DDiscMaster2Events</strong></a></li>
</ul></td>
<td>DDiscMaster2Events</td>
</tr>
<tr class="odd">
<td>Appareil d’enregistrement individuel.
<ul>
<li><a href="/windows/desktop/api/imapi2/nn-imapi2-idiscrecorder2"><strong>IDiscRecorder2</strong></a></li>
<li><a href="/windows/desktop/api/imapi2/nn-imapi2-idiscrecorder2ex"><strong>IDiscRecorder2Ex</strong></a></li>
</ul></td>
<td>MsftDiscRecorder2</td>
</tr>
<tr class="even">
<td>Attributs d’écriture de périphérique, y compris le type de média, la vitesse d’écriture et le type de contrôle de vélocité angulaire.
<ul>
<li><a href="/windows/desktop/api/imapi2/nn-imapi2-iwritespeeddescriptor"><strong>IWriteSpeedDescriptor</strong></a></li>
</ul></td>
<td>MsftWriteSpeedDescriptor</td>
</tr>
</tbody>
</table>



 

Le tableau suivant répertorie les interfaces du système de fichiers.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Interface</td>
<td>Object</td>
</tr>
<tr class="even">
<td>Flux et propriétés de l’image de démarrage pour l’intégration de l’image de démarrage dans l’image de disque.
<ul>
<li><a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ibootoptions"><strong>IBootOptions</strong></a></li>
</ul></td>
<td>BootOptions</td>
</tr>
<tr class="odd">
<td>Image et propriétés du système de fichiers. Cet objet comprend toutes les pistes et les références à l’image de démarrage et à l’image de résultat.
<ul>
<li><a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-dfilesystemimageevents"><strong>DFileSystemImageEvents</strong></a></li>
<li><a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-dfilesystemimageimportevents"><strong>DFileSystemImageImportEvents</strong></a></li>
<li><a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ifilesystemimage"><strong>IFileSystemImage</strong></a></li>
<li><a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ifilesystemimage2"><strong>IFileSystemImage2</strong></a></li>
<li><a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ifilesystemimage3"><strong>IFileSystemImage3</strong></a></li>
</ul></td>
<td>CFileSystemImage</td>
</tr>
<tr class="even">
<td>Conteneur du flux de données fourni par l’objet de système de fichiers.
<ul>
<li><a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ifilesystemimageresult"><strong>IFileSystemImageResult</strong></a></li>
</ul></td>
<td>FileSystemImageResult</td>
</tr>
<tr class="odd">
<td>Élément d’annuaire dans l’image du système de fichiers.
<ul>
<li><a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ifsidirectoryitem"><strong>IFsiDirectoryItem</strong></a></li>
<li><a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ifsidirectoryitem2"><strong>IFsiDirectoryItem2</strong></a></li>
</ul></td>
<td>FsiDirectoryItem</td>
</tr>
<tr class="even">
<td>Élément de fichier dans l’image du système de fichiers.
<ul>
<li><a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ifsifileitem"><strong>IFsiFileItem</strong></a></li>
<li><a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ifsifileitem2"><strong>IFsiFileItem2</strong></a></li>
</ul></td>
<td>FsiFileItem</td>
</tr>
<tr class="odd">
<td>Interface contenant des propriétés communes aux éléments de fichier et de répertoire.
<ul>
<li><a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ifsiitem"><strong>IFsiItem</strong></a></li>
</ul></td>
<td>FsiItem</td>
</tr>
<tr class="even">
<td>Création d’images CD BRUTes.
<ul>
<li><a href="/windows/desktop/api/imapi2/nn-imapi2-irawcdimagecreator"><strong>IRawCDImageCreator</strong></a></li>
<li><a href="/windows/desktop/api/imapi2/nn-imapi2-irawcdimagetrackinfo"><strong>IRawCDImageTrackInfo</strong></a></li>
</ul></td>
<td>MsftRawCDImageCreator</td>
</tr>
<tr class="odd">
<td>Objet d’assistance de l’objet de flux pour concaténer plusieurs flux.
<ul>
<li><a href="/windows/desktop/api/imapi2/nn-imapi2-istreamconcatenate"><strong>IStreamConcatenate</strong></a></li>
</ul></td>
<td>MsftStreamConcatenate</td>
</tr>
<tr class="even">
<td>Flux entrelacé à ajouter à l’image disque.
<ul>
<li><a href="/windows/desktop/api/imapi2/nn-imapi2-istreaminterleave"><strong>IStreamInterleave</strong></a></li>
</ul></td>
<td>MsftStreamInterleave</td>
</tr>
<tr class="odd">
<td>Flux généré Pseudo-aléatoire.
<ul>
<li><a href="/windows/desktop/api/imapi2/nn-imapi2-istreampseudorandombased"><strong>IStreamPseudoRandomBased</strong></a></li>
</ul></td>
<td>MsftStreamPrgn001</td>
</tr>
<tr class="even">
<td>L’objet de script <strong>MsftStreamZero</strong> n’est pas implémenté en tant qu’interface.</td>
<td><a href="msftstreamzero.md"><strong>MsftStreamZero</strong></a></td>
</tr>
</tbody>
</table>



 

Le tableau suivant répertorie les interfaces d’assistance.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Interface</td>
<td>Object</td>
</tr>
<tr class="even">
<td>Collection de plages de secteurs dans une image de système de fichiers.
<ul>
<li><a href="/windows/desktop/api/imapi2/nn-imapi2-iblockrange"><strong>IBlockRange</strong></a></li>
<li><a href="/windows/desktop/api/imapi2/nn-imapi2-iblockrangelist"><strong>IBlockRangeList</strong></a></li>
</ul></td>
<td>Aucun objet correspondant</td>
</tr>
<tr class="odd">
<td>Prise en charge de la vérification de la gravure.
<ul>
<li><a href="/windows/desktop/api/imapi2/nn-imapi2-iburnverification"><strong>IBurnVerification</strong></a></li>
</ul></td>
<td>Aucun objet correspondant</td>
</tr>
<tr class="even">
<td>Énumérateur de FsiItems pour les applications C/C++.
<ul>
<li><a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ienumfsiitems"><strong>IEnumFsiItems</strong></a></li>
</ul></td>
<td>EnumFsiItems</td>
</tr>
<tr class="odd">
<td>Énumérateur de ProgressItems pour les applications C/C++.
<ul>
<li><a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ienumprogressitems"><strong>IEnumProgressItems</strong></a></li>
</ul></td>
<td>EnumProgressItems</td>
</tr>
<tr class="even">
<td><ul>
<li><a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ifsinamedstreams"><strong>IFsiNamedStreams</strong></a></li>
</ul></td>
<td>FsiFileItem2</td>
</tr>
<tr class="odd">
<td>prise en charge de la vérification d’image. ISO.
<ul>
<li><a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-iisoimagemanager"><strong>IIsoImageManager</strong></a></li>
</ul></td>
<td>Aucun objet correspondant</td>
</tr>
<tr class="even">
<td>Prise en charge de plusieurs sessions.
<ul>
<li><a href="/windows/desktop/api/imapi2/nn-imapi2-imultisession"><strong>IMultisession</strong></a></li>
</ul></td>
<td>Aucun objet correspondant</td>
</tr>
<tr class="odd">
<td>Prise en charge de plusieurs sessions séquentielles.
<ul>
<li><a href="/windows/desktop/api/imapi2/nn-imapi2-imultisessionsequential"><strong>IMultisessionSequential</strong></a></li>
<li><a href="/windows/desktop/api/imapi2/nn-imapi2-imultisessionsequential2"><strong>IMultisessionSequential2</strong></a></li>
</ul></td>
<td>MsftMultisessionSequential</td>
</tr>
<tr class="even">
<td>Nom de fichier et blocs associés dans l’image de résultat.
<ul>
<li><a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-iprogressitem"><strong>IProgressItem</strong></a></li>
</ul></td>
<td>ProgressItem</td>
</tr>
<tr class="odd">
<td>Liste des images de résultat, ventilées par nom de fichier et blocs associés.
<ul>
<li><a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-iprogressitems"><strong>IProgressItems</strong></a></li>
</ul></td>
<td>ProgressItems</td>
</tr>
</tbody>
</table>



 

 

 




