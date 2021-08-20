---
description: Il existe de nombreuses raisons pour lesquelles un demandeur n’est pas autorisé à restaurer les fichiers du support de sauvegarde à leur emplacement d’origine.
ms.assetid: 2a9cfd99-5a2c-4c0c-98ff-11c745298cda
title: Utilisation d’autres emplacements pendant la restauration
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 907732c7b4b97668f1a317f9e03c3ea35bdec9618ff0e3e3c1a2f1e319eb19fa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119056147"
---
# <a name="working-with-alternate-locations-during-restore"></a>Utilisation d’autres emplacements pendant la restauration

Il existe de nombreuses raisons pour lesquelles un demandeur n’est pas autorisé à restaurer les fichiers du support de sauvegarde à leur emplacement d’origine. Par exemple, une méthode ou une cible de restauration peut nécessiter une telle restauration, ou l’emplacement de restauration actuel peut être occupé et non inscriptible.

Pour gérer ces cas-là, un enregistreur peut avoir défini un [*mappage d’emplacement secondaire*](vssgloss-a.md), une destination de restauration non standard à utiliser pour des circonstances particulières.

Le terme autre mappage d’emplacement, tel qu’il est utilisé avec VSS, ne doit pas être confondu avec le terme [*autre chemin*](vssgloss-a.md). Les mappages d’emplacements alternatifs sont utilisés uniquement pendant les opérations de restauration et font référence à une autre destination pour les opérations de restauration. Les chemins d’accès alternatifs sont utilisés uniquement pendant les opérations de sauvegarde et font référence à une autre source à partir de laquelle effectuer la sauvegarde.

Pour utiliser d’autres mappages d’emplacements pendant la restauration, un demandeur effectue les opérations suivantes (généralement après la génération d’un événement de [**prérestauration**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prerestore) ) :

1.  À l’aide d’une instance de l’interface [**IVssExamineWriterMetadata**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssexaminewritermetadata) obtenue en extrayant un writer stocké, un demandeur utilise la méthode [**IVssExamineWriterMetadata :: GetAlternateLocationMapping**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssexaminewritermetadata-getalternatelocationmapping) pour obtenir les mappages d’emplacement de remplacement d’un writer en tant qu’instances de l’interface [**IVssWMFiledesc**](/windows/desktop/api/VsWriter/nl-vswriter-ivsswmfiledesc) .

    > [!Note]  
    > Le demandeur utilise [**IVssExamineWriterMetadata :: GetAlternateLocationMapping**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssexaminewritermetadata-getalternatelocationmapping), et non [**IVssComponent :: GetAlternateLocationMapping**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getalternatelocationmapping). La première retourne les mappages d’emplacements secondaires pouvant être utilisés par un demandeur. Ce dernier est utilisé pour indiquer les autres mappages d’emplacements réellement utilisés par un demandeur.

     

2.  L’appel à [**IVssExamineWriterMetadata :: GetAlternateLocationMapping**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssexaminewritermetadata-getalternatelocationmapping) retourne une instance de l’interface [**IVssWMFiledesc**](/windows/desktop/api/VsWriter/nl-vswriter-ivsswmfiledesc) . Cette instance contient des informations sur le jeu de fichiers (un chemin d’accès spécifié par [**IVssWMFiledesc :: GetPath**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswmfiledesc-getpath)), une spécification de fichier retournée via [**IVssWMFiledesc :: GetFilespec**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswmfiledesc-getfilespec)et un indicateur de récurrence obtenu de [**IVssWMFiledesc :: GetRecursive**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswmfiledesc-getrecursive), correspondant à l’un des jeux de fichiers ajoutés (à l’aide [](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-addfilestofilegroup)de [**IVssCreateWriterMetadata :: AddDatabaseFiles**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-adddatabasefiles), [**IVssCreateWriterMetadata :**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-adddatabaselogfiles)

    La valeur retournée par [**IVssWMFiledesc :: GetAlternateLocation**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswmfiledesc-getalternatelocation) est le mappage d’emplacement de remplacement pour ce jeu de fichiers.

3.  Les mappages d’emplacements secondaires ne contiennent pas d’informations sur les composants. il est donc nécessaire de comparer les informations sur le jeu de fichiers (chemin d’accès, spécification de fichier et indicateur de récurrence) obtenues en appelant [**IVssExamineWriterMetadata :: GetAlternateLocationMapping**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssexaminewritermetadata-getalternatelocationmapping) à celles contenues dans les composants du writer.

    Vous pouvez trouver ces informations en effectuant une itération sur les composants du writer et en appelant [**IVssExamineWriterMetadata :: GetComponent**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssexaminewritermetadata-getcomponent) pour obtenir une instance de l’interface [**IVssWMComponent**](/windows/desktop/api/VsBackup/nl-vsbackup-ivsswmcomponent) et utiliser [**IVssWMComponent :: GetFile**](/windows/desktop/api/VsBackup/nf-vsbackup-ivsswmcomponent-getfile) pour obtenir une instance [**IVssWMFiledesc**](/windows/desktop/api/VsWriter/nl-vswriter-ivsswmfiledesc) contenant les informations sur le jeu de fichiers du composant.

    Lorsque les informations sur le jeu de fichiers retournées par l’instance de [**IVssWMFiledesc**](/windows/desktop/api/VsWriter/nl-vswriter-ivsswmfiledesc) obtenue à partir de [**IVssExamineWriterMetadata :: GetComponent**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssexaminewritermetadata-getcomponent) et [**IVssWMComponent :: GetFile**](/windows/desktop/api/VsBackup/nf-vsbackup-ivsswmcomponent-getfile) correspondent à celles obtenues à partir de l’instance **IVssWMFiledesc** dérivée de [**IVssWMFiledesc :: GetAlternateLocation**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswmfiledesc-getalternatelocation), le composant qui gère les fichiers avec le mappage d’emplacement de substitution spécifique a été trouvé.

4.  Une fois le composant localisé, le demandeur peut déterminer les conditions dans lesquelles un autre mappage d’emplacement doit être utilisé en procédant comme suit :

    -   Examen de la méthode de restauration du composant, obtenue en appelant [**IVssExamineWriterMetadata :: GetRestoreMethod**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssexaminewritermetadata-getrestoremethod).
    -   Vérification pour déterminer si une cible de restauration remplace la méthode Restore, en appelant [**IVssComponent :: GetRestoreTarget**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getrestoretarget).

        Si le composant trouvé dans le document de métadonnées du writer avait été [*explicitement inclus*](vssgloss-e.md) dans la sauvegarde, l’instance de l’interface [**IVssComponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) correspondra à ce composant. Si le composant avait été [*implicitement inclus*](vssgloss-i.md) dans la sauvegarde, l’instance de **IVssComponent** correspond au composant définissant le jeu de composants dont le composant dans le document de métadonnées de writer est un sous-composant.

5.  Avec ces informations, le demandeur peut déterminer le composant par composant s’il doit restaurer un jeu de fichiers donné d’un composant donné vers une destination définie par le mappage de l’emplacement secondaire.

6.  Lors de l’utilisation d’un mappage d’emplacement secondaire, le demandeur respecte le descripteur de fichier et l’indicateur récursif du jeu de fichiers et utilise le chemin d’accès fourni par le mappage de l’emplacement secondaire.

    Le demandeur indique qu’il a utilisé un autre mappage d’emplacement au cours d’une opération de restauration en appelant [**IVssBackupComponents :: AddAlternativeLocationMapping**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addalternativelocationmapping) avec les informations d’emplacement par défaut du jeu de fichiers, l’autre destination de restauration utilisée et un nom de composant.

    Si le jeu de fichiers a été géré par un composant qui a été explicitement inclus dans la sauvegarde, le nom de ce composant sera utilisé. Si le jeu de fichiers a été géré par un composant qui a été implicitement inclus dans la sauvegarde, le nom utilisé correspond à celui du composant qui définit le jeu de composants dont le composant qui gère le jeu de fichiers est un sous-composant.

Les enregistreurs vérifient si les jeux de fichiers de l’un de leurs composants ont été restaurés dans un autre mappage d’emplacement en appelant [**IVssComponent :: GetAlternateLocationMapping**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getalternatelocationmapping).

 

 



