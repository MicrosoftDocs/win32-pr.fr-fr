---
description: Dans certains cas, les fichiers à sauvegarder ne sont pas l’emplacement par défaut de ces fichiers.
ms.assetid: b9e96827-a678-45ca-8ede-4508a406f071
title: Utilisation de chemins alternatifs pendant la sauvegarde
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a98e93af4d12b804032a64841542e731ff77e048
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106515858"
---
# <a name="working-with-alternate-paths-during-backup"></a>Utilisation de chemins alternatifs pendant la sauvegarde

Dans certains cas, les fichiers à sauvegarder ne sont pas l’emplacement par défaut de ces fichiers.

Par exemple, certains enregistreurs ne peuvent pas garantir que leurs données ont été vidées dans la fenêtre de temps entre les événements [*figer*](vssgloss-f.md) et [*libérer*](vssgloss-t.md) . Ces enregistreurs peuvent choisir de générer des fichiers dupliqués contenant une dernière configuration correcte connue dans un répertoire source autre que celui par défaut, ou un [*autre chemin d’accès*](vssgloss-a.md).

Le terme autre chemin, utilisé avec VSS, ne doit pas être confondu avec le terme [*autre mappage d’emplacement*](vssgloss-a.md). Les chemins d’accès alternatifs sont utilisés uniquement pendant les opérations de sauvegarde et font référence à une autre source à partir de laquelle effectuer la sauvegarde. Les mappages d’emplacements alternatifs sont utilisés uniquement pendant les opérations de restauration et font référence à une autre destination pour les opérations de restauration.

**Pour utiliser un autre chemin pendant la sauvegarde**

1.  Pendant la phase de découverte d’une opération de sauvegarde (voir [vue d’ensemble de la phase de découverte de sauvegarde](overview-of-the-backup-discovery-phase.md)), un demandeur examine les données du composant de ce writer à l’aide de [**IVssExamineWriterMetadata :: GetComponent**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssexaminewritermetadata-getcomponent) et obtient les instances de l’interface [**IVssWMComponent**](/windows/desktop/api/VsBackup/nl-vsbackup-ivsswmcomponent) .
2.  Un demandeur obtient ensuite le jeu de [*fichiers*](vssgloss-f.md) géré par chaque composant, représenté par les instances de l’interface [**IVssWMFiledesc**](/windows/desktop/api/VsWriter/nl-vswriter-ivsswmfiledesc) , en appelant la méthode [**IVssWMComponent :: GetFile**](/windows/desktop/api/VsBackup/nf-vsbackup-ivsswmcomponent-getfile) .
3.  En plus d’un chemin d’accès ([**IVssWMFiledesc :: GetPath**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswmfiledesc-getpath)), d’une spécification de fichier ([**IVssWMFiledesc :: GetFilespec**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswmfiledesc-getfilespec)) et d’un indicateur de récurrence ([**IVssWMFiledesc :: GetRecursive**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswmfiledesc-getrecursive)), un objet [**IVssWMFiledesc**](/windows/desktop/api/VsWriter/nl-vswriter-ivsswmfiledesc) peut contenir un autre emplacement (utilisé comme autre chemin pour les opérations de sauvegarde et un autre mappage d’emplacement pour les opérations de restauration) à l’aide de la méthode [**IVssWMFiledesc :: GetAlternateLocation**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswmfiledesc-getalternatelocation) .
4.  Si la valeur retournée par [**IVssWMFiledesc :: GetAlternateLocation**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswmfiledesc-getalternatelocation) n’est pas null, les applications de sauvegarde utilisent cette valeur au lieu de la valeur obtenue à partir de [**IVssWMFiledesc :: GetPath**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswmfiledesc-getpath) pour sélectionner et localiser les fichiers à sauvegarder.
5.  Malgré l’utilisation d’un chemin alternatif, les demandeurs doivent respecter la spécification de fichier et les paramètres récursifs retournés par [**IVssWMFiledesc :: GetFilespec**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswmfiledesc-getfilespec) et [**IVssWMFiledesc :: GetRecursive**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswmfiledesc-getrecursive).

Notez que lors de la restauration, tout autre chemin d’accès, autrement dit, un autre emplacement retourné par une instance de [**IVssWMFiledesc :: GetAlternateLocation**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswmfiledesc-getalternatelocation) obtenu à partir d’une instance de [**IVssWMComponent**](/windows/desktop/api/VsBackup/nl-vsbackup-ivsswmcomponent), qui a été obtenue à partir d’une instance de [**IVssExamineWriterMetadata**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssexaminewritermetadata) obtenue en récupérant un document de métadonnées d’écriture stocké, n’est pas utilisé lors de la restauration.

Le chemin d’accès par défaut (retourné par la méthode [**GetPath**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswmfiledesc-getpath) de la même instance de [**IVssWMFiledesc**](/windows/desktop/api/VsWriter/nl-vswriter-ivsswmfiledesc)) est utilisé pour définir un emplacement de restauration, ou un autre mappage d’emplacement (trouvé à l’aide de la méthode [**IVssWMFiledesc :: GetAlternateLocation**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswmfiledesc-getalternatelocation) ) indique l’emplacement de restauration d’un fichier (voir [utilisation d’autres emplacements pendant la restauration](working-with-alternate-locations-during-restore.md)).

 

 



