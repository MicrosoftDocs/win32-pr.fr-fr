---
description: 'La combinaison du chemin d’accès, de la spécification de fichier et de l’indicateur de récurrence (wszPath, wszFileSpec et bRecursive, respectivement) doit correspondre à celle de l’un des jeux de fichiers ajoutés à l’un des composants du générateur à l’aide de IVssCreateWriterMetadata :: AddFilesToFileGroup, IVssCreateWriterMetadata :: AddDatabaseFiles ou IVssCreateWriterMetadata :: AddDatabaseLogFiles lorsque :'
ms.assetid: debf181a-1579-46f2-86ef-a1d2a850e99e
title: modifications sémantiques apportées au serveur Windows 2003
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8319259dc27c981822bb242d20243264ca9025d959693aafcb3836976fd7754d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119866259"
---
# <a name="semantic-changes-to-windows-server-2003"></a>modifications sémantiques apportées au serveur Windows 2003

La combinaison du chemin d’accès, de la spécification de fichier et de l’indicateur de récurrence (*wszPath*, *wszFileSpec* et *bRecursive*, respectivement) doit correspondre à celle de l’un des jeux de fichiers ajoutés à l’un des composants du générateur à l’aide de [**IVssCreateWriterMetadata :: AddFilesToFileGroup**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-addfilestofilegroup), [**IVssCreateWriterMetadata :: AddDatabaseFiles**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-adddatabasefiles)ou [**IVssCreateWriterMetadata :: AddDatabaseLogFiles**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-adddatabaselogfiles) lorsque :

-   Un demandeur ajoute une nouvelle cible à l’aide de [**IVssBackupComponents :: AddNewTarget**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addnewtarget).
-   Un writer ajoute un autre mappage d’emplacement à l’aide de [**IVssCreateWriterMetadata :: AddAlternateLocationMapping**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-addalternatelocationmapping).
-   Les fichiers existants sont ajoutés en tant que fichiers différenciés à l’aide de [**IVssComponent :: AddDifferencedFilesByLastModifyTime**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-adddifferencedfilesbylastmodifytime).
-   Un demandeur indique qu’un autre mappage d’emplacement a été utilisé pour restaurer un jeu de fichiers à l’aide de [**IVssBackupComponents :: AddAlternativeLocationMapping**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addalternativelocationmapping).

 

 



