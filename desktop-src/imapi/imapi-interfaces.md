---
title: Interfaces IMAPi
description: Les tableaux suivants identifient et décrivent brièvement les interfaces utilisées par les développeurs C/C++ et l’objet de script associé. Préfixez le nom de l’objet dans la table avec \ 0034 ; IMAPI2. \ 0034 ; pour qualifier complètement le nom de l’objet lors de la création de l’objet dans le script.
ms.assetid: dba81a45-34a8-4b49-9ccb-d61a7e7ee1f6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 58768520f9617da2ba5cf76348a6d30f4a38974b
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122987222"
---
# <a name="imapi-interfaces"></a>Interfaces IMAPi

Les tableaux suivants identifient et décrivent brièvement les interfaces utilisées par les développeurs C/C++ et l’objet de script associé. Préfixez le nom de l’objet dans la table avec « IMAPI2 ». pour qualifier complètement le nom de l’objet lors de la création de l’objet dans le script.

Le tableau suivant répertorie les interfaces associées aux appareils, au moteur de gravure et aux Writers de format et gomme.





|--------|-------| | Interface | Objet | | Moteur de gravure de bas niveau.<ul><li><a href="/windows/desktop/api/imapi2/nn-imapi2-dwriteengine2events"><strong>DWriteEngine2Events</strong></a></li><li><a href="/windows/desktop/api/imapi2/nn-imapi2-iwriteengine2"><strong>IWriteEngine2</strong></a></li><li><a href="/windows/desktop/api/imapi2/nn-imapi2-iwriteengine2eventargs"><strong>IWriteEngine2EventArgs</strong></a></li></ul> | MsftWriteEngine2 | | Enregistreur d’images principal.<ul><li><a href="/windows/desktop/api/imapi2/nn-imapi2-ddiscformat2dataevents"><strong>DDiscFormat2DataEvents</strong></a></li><li><a href="/windows/desktop/api/imapi2/nn-imapi2-idiscformat2data"><strong>IDiscFormat2Data</strong></a></li><li><a href="/windows/desktop/api/imapi2/nn-imapi2-idiscformat2dataeventargs"><strong>IDiscFormat2DataEventArgs</strong></a></li></ul> | MsftDiscFormat2Data | | Effaceur de disque.<ul><li><a href="/windows/desktop/api/imapi2/nn-imapi2-ddiscformat2eraseevents"><strong>DDiscFormat2EraseEvents</strong></a></li><li><a href="/windows/desktop/api/imapi2/nn-imapi2-idiscformat2erase"><strong>IDiscFormat2Erase</strong></a></li></ul> | MsftDiscFormat2Erase | | Enregistreur d’images brutes.<ul><li><a href="/windows/desktop/api/imapi2/nn-imapi2-ddiscformat2rawcdevents"><strong>DDiscFormat2RawCDEvents</strong></a></li><li><a href="/windows/desktop/api/imapi2/nn-imapi2-idiscformat2rawcd"><strong>IDiscFormat2RawCD</strong></a></li><li><a href="/windows/desktop/api/imapi2/nn-imapi2-idiscformat2rawcdeventargs"><strong>IDiscFormat2RawCDEventArgs</strong></a></li></ul> | MsftDiscFormat2RawCD | | Enregistreur d’images Track-on-once.<ul><li><a href="/windows/desktop/api/imapi2/nn-imapi2-ddiscformat2trackatonceevents"><strong>DDiscFormat2TrackAtOnceEvents</strong></a></li><li><a href="/windows/desktop/api/imapi2/nn-imapi2-idiscformat2trackatonce"><strong>IDiscFormat2TrackAtOnce</strong></a></li><li><a href="/windows/desktop/api/imapi2/nn-imapi2-idiscformat2trackatonceeventargs"><strong>IDiscFormat2TrackAtOnceEventArgs</strong></a></li></ul> | MsftDiscFormat2TrackAtOnce | | Énumération des périphériques de disque dans la liste des matériels du système.<ul><li><a href="/windows/desktop/api/imapi2/nn-imapi2-idiscmaster2"><strong>IDiscMaster2</strong></a></li></ul> | MsftDiscMaster2 | | Délégué de notification pour l’objet MsftDiscMaster2.<ul><li><a href="/windows/desktop/api/imapi2/nn-imapi2-ddiscmaster2events"><strong>DDiscMaster2Events</strong></a></li></ul> | DDiscMaster2Events | | Appareil d’enregistrement individuel.<ul><li><a href="/windows/desktop/api/imapi2/nn-imapi2-idiscrecorder2"><strong>IDiscRecorder2</strong></a></li><li><a href="/windows/desktop/api/imapi2/nn-imapi2-idiscrecorder2ex"><strong>IDiscRecorder2Ex</strong></a></li></ul> | MsftDiscRecorder2 | | Attributs d’écriture de périphérique, y compris le type de média, la vitesse d’écriture et le type de contrôle de vélocité angulaire.<ul><li><a href="/windows/desktop/api/imapi2/nn-imapi2-iwritespeeddescriptor"><strong>IWriteSpeedDescriptor</strong></a></li></ul> | MsftWriteSpeedDescriptor | 




 

Le tableau suivant répertorie les interfaces du système de fichiers.





|--------|-------| | Interface | Objet | | Flux et propriétés de l’image de démarrage pour l’intégration de l’image de démarrage dans l’image de disque.<ul><li><a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ibootoptions"><strong>IBootOptions</strong></a></li></ul> | BootOptions | | Image et propriétés du système de fichiers. Cet objet comprend toutes les pistes et les références à l’image de démarrage et à l’image de résultat.<ul><li><a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-dfilesystemimageevents"><strong>DFileSystemImageEvents</strong></a></li><li><a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-dfilesystemimageimportevents"><strong>DFileSystemImageImportEvents</strong></a></li><li><a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ifilesystemimage"><strong>IFileSystemImage</strong></a></li><li><a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ifilesystemimage2"><strong>IFileSystemImage2</strong></a></li><li><a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ifilesystemimage3"><strong>IFileSystemImage3</strong></a></li></ul> | CFileSystemImage | | Conteneur du flux de données fourni par l’objet de système de fichiers.<ul><li><a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ifilesystemimageresult"><strong>IFileSystemImageResult</strong></a></li></ul> | FileSystemImageResult | | Élément d’annuaire dans l’image du système de fichiers.<ul><li><a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ifsidirectoryitem"><strong>IFsiDirectoryItem</strong></a></li><li><a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ifsidirectoryitem2"><strong>IFsiDirectoryItem2</strong></a></li></ul> | FsiDirectoryItem | | Élément de fichier dans l’image du système de fichiers.<ul><li><a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ifsifileitem"><strong>IFsiFileItem</strong></a></li><li><a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ifsifileitem2"><strong>IFsiFileItem2</strong></a></li></ul> | FsiFileItem | | Interface contenant des propriétés communes aux éléments de fichier et de répertoire.<ul><li><a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ifsiitem"><strong>IFsiItem</strong></a></li></ul> | FsiItem | | Création d’images CD BRUTes.<ul><li><a href="/windows/desktop/api/imapi2/nn-imapi2-irawcdimagecreator"><strong>IRawCDImageCreator</strong></a></li><li><a href="/windows/desktop/api/imapi2/nn-imapi2-irawcdimagetrackinfo"><strong>IRawCDImageTrackInfo</strong></a></li></ul> | MsftRawCDImageCreator | | Objet d’assistance de l’objet de flux pour concaténer plusieurs flux.<ul><li><a href="/windows/desktop/api/imapi2/nn-imapi2-istreamconcatenate"><strong>IStreamConcatenate</strong></a></li></ul> | MsftStreamConcatenate | | Flux entrelacé à ajouter à l’image disque.<ul><li><a href="/windows/desktop/api/imapi2/nn-imapi2-istreaminterleave"><strong>IStreamInterleave</strong></a></li></ul> | MsftStreamInterleave | | Flux généré Pseudo-aléatoire.<ul><li><a href="/windows/desktop/api/imapi2/nn-imapi2-istreampseudorandombased"><strong>IStreamPseudoRandomBased</strong></a></li></ul> | MsftStreamPrgn001 | | L’objet de script <strong>MsftStreamZero</strong> n’est pas implémenté en tant qu’interface. | <a href="msftstreamzero.md"><strong>MsftStreamZero</strong></a> | 




 

Le tableau suivant répertorie les interfaces d’assistance.





|--------|-------| | Interface | Objet | | Collection de plages de secteurs dans une image de système de fichiers.<ul><li><a href="/windows/desktop/api/imapi2/nn-imapi2-iblockrange"><strong>IBlockRange</strong></a></li><li><a href="/windows/desktop/api/imapi2/nn-imapi2-iblockrangelist"><strong>IBlockRangeList</strong></a></li></ul> | Aucun objet correspondant | | Prise en charge de la vérification de la gravure.<ul><li><a href="/windows/desktop/api/imapi2/nn-imapi2-iburnverification"><strong>IBurnVerification</strong></a></li></ul> | Aucun objet correspondant | | Énumérateur de FsiItems pour les applications C/C++.<ul><li><a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ienumfsiitems"><strong>IEnumFsiItems</strong></a></li></ul> | EnumFsiItems | | Énumérateur de ProgressItems pour les applications C/C++.<ul><li><a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ienumprogressitems"><strong>IEnumProgressItems</strong></a></li></ul> | EnumProgressItems | | <ul><li><a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ifsinamedstreams"><strong>IFsiNamedStreams</strong></a></li></ul> | Prise en charge de la vérification d’image FsiFileItem2 | |. ISO.<ul><li><a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-iisoimagemanager"><strong>IIsoImageManager</strong></a></li></ul> | Aucun objet correspondant | | Prise en charge de plusieurs sessions.<ul><li><a href="/windows/desktop/api/imapi2/nn-imapi2-imultisession"><strong>IMultisession</strong></a></li></ul> | Aucun objet correspondant | | Prise en charge de plusieurs sessions séquentielles.<ul><li><a href="/windows/desktop/api/imapi2/nn-imapi2-imultisessionsequential"><strong>IMultisessionSequential</strong></a></li><li><a href="/windows/desktop/api/imapi2/nn-imapi2-imultisessionsequential2"><strong>IMultisessionSequential2</strong></a></li></ul> | MsftMultisessionSequential | | Nom de fichier et blocs associés dans l’image de résultat.<ul><li><a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-iprogressitem"><strong>IProgressItem</strong></a></li></ul> | ProgressItem | | Liste des images de résultat, ventilées par nom de fichier et blocs associés.<ul><li><a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-iprogressitems"><strong>IProgressItems</strong></a></li></ul> | ProgressItems | 




 

 

 




