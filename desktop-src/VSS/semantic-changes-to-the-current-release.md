---
description: 'La combinaison du chemin d’accès, de la spécification de fichier et de l’indicateur de récurrence (wszPath, wszFileSpec et bRecursive, respectivement) doit correspondre à celle de l’un des jeux de fichiers ajoutés à l’un des composants du générateur à l’aide de IVssCreateWriterMetadata :: AddFilesToFileGroup, IVssCreateWriterMetadata :: AddDatabaseFiles ou IVssCreateWriterMetadata :: AddDatabaseLogFiles lorsque :'
ms.assetid: debf181a-1579-46f2-86ef-a1d2a850e99e
title: Modifications sémantiques apportées à Windows Server 2003
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 53b9d2edc56f215f554b497eebff9f76a1da53dd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104202380"
---
# <a name="semantic-changes-to-windows-server-2003"></a>Modifications sémantiques apportées à Windows Server 2003

La combinaison du chemin d’accès, de la spécification de fichier et de l’indicateur de récurrence (*wszPath*, *wszFileSpec* et *bRecursive*, respectivement) doit correspondre à celle de l’un des jeux de fichiers ajoutés à l’un des composants du générateur à l’aide de [**IVssCreateWriterMetadata :: AddFilesToFileGroup**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-addfilestofilegroup), [**IVssCreateWriterMetadata :: AddDatabaseFiles**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-adddatabasefiles)ou [**IVssCreateWriterMetadata :: AddDatabaseLogFiles**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-adddatabaselogfiles) lorsque :

-   Un demandeur ajoute une nouvelle cible à l’aide de [**IVssBackupComponents :: AddNewTarget**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addnewtarget).
-   Un writer ajoute un autre mappage d’emplacement à l’aide de [**IVssCreateWriterMetadata :: AddAlternateLocationMapping**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-addalternatelocationmapping).
-   Les fichiers existants sont ajoutés en tant que fichiers différenciés à l’aide de [**IVssComponent :: AddDifferencedFilesByLastModifyTime**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-adddifferencedfilesbylastmodifytime).
-   Un demandeur indique qu’un autre mappage d’emplacement a été utilisé pour restaurer un jeu de fichiers à l’aide de [**IVssBackupComponents :: AddAlternativeLocationMapping**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addalternativelocationmapping).

 

 



