---
description: Le tableau suivant décrit les quatre types de composants qui peuvent être impliqués dans une opération de sauvegarde.
ms.assetid: d94e015b-6735-4a88-9d24-b73f0b5f6542
title: Utilisation de la sélectivité pour la sauvegarde
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e4bd20bd0c9139f8ed1c9f56cc8f499f1b6aaf14
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104485009"
---
# <a name="working-with-selectability-for-backup"></a>Utilisation de la sélectivité pour la sauvegarde

Le tableau suivant décrit les quatre types de composants qui peuvent être impliqués dans une opération de sauvegarde.



| Type de composant                                                                                                                                                                                                               | Description                                                                                        |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------|
| <span id="Nonselectable-for-backup_components"></span><span id="nonselectable-for-backup_components"></span><span id="NONSELECTABLE-FOR-BACKUP_COMPONENTS"></span>Composants non sélectionnables-pour la sauvegarde<br/>             | Pas d’ancêtres sélectionnables pour la sauvegarde dans leurs chemins logiques.<br/>                              |
| <span id="Selectable-for-backup_components"></span><span id="selectable-for-backup_components"></span><span id="SELECTABLE-FOR-BACKUP_COMPONENTS"></span>Éléments sélectionnables pour la sauvegarde<br/>                         | Pas d’ancêtres sélectionnables pour la sauvegarde dans leurs chemins logiques.<br/>                              |
| <span id="Nonselectable-for-backup_subcomponents"></span><span id="nonselectable-for-backup_subcomponents"></span><span id="NONSELECTABLE-FOR-BACKUP_SUBCOMPONENTS"></span>Éléments non sélectionnables-pour-sauvegarder<br/> | Éléments non sélectionnables-pour la sauvegarde avec des ancêtres sélectionnables pour la sauvegarde dans leur chemin d’accès.<br/> |
| <span id="Selectable-for-backup_subcomponents"></span><span id="selectable-for-backup_subcomponents"></span><span id="SELECTABLE-FOR-BACKUP_SUBCOMPONENTS"></span>Les sous-composants sélectionnables pour la sauvegarde<br/>             | Sélectionnable-pour les composants de sauvegarde avec des ancêtres sélectionnables pour la sauvegarde dans leur chemin d’accès.<br/>    |



 

En outre, n’importe quel composant sélectionnable pour la sauvegarde, qu’il ait ou non un élément sélectionnable pour la sauvegarde, définit un [*jeu de composants*](vssgloss-c.md) si d’autres composants en ont un ancêtre dans leurs chemins logiques.

Les règles régissant la sélection des composants à sauvegarder peuvent être résumées comme suit :

-   Quand un composant sans ancêtre sélectionnable pour la sauvegarde dans son chemin logique (que le composant soit sélectionnable-pour la sauvegarde ou non sélectionnable-for-Backup) est inclus dans une sauvegarde, il doit être [*inclus de manière explicite*](vssgloss-e.md). Cela signifie que les métadonnées de ces composants sont ajoutées au document des composants de sauvegarde.

    Les demandeurs ajoutent explicitement ces composants à l’aide de la méthode [**IVssBackupComponents :: AddComponent**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addcomponent) .

-   Les sous-composants non sélectionnables pour la sauvegarde sont toujours [*inclus implicitement*](vssgloss-i.md) dans la sauvegarde. Cela signifie que les métadonnées de ces composants ne font pas partie du document sur les composants de sauvegarde.
-   Les sous-composants sélectionnables-for-Backup sont implicitement inclus si cet ancêtre est explicitement inclus dans la sauvegarde. Dans ce cas, les métadonnées de ces composants ne sont pas ajoutées au document des composants de sauvegarde. Si un sous-composant implicitement sélectionnable pour la sauvegarde définit un jeu de composants, les membres de ce jeu de composants sont également implicitement sélectionnés.
-   Les sous-composants sélectionnables-for-Backup dont l’ancêtre sélectionnable pour la sauvegarde n’est pas explicitement inclus dans la sauvegarde peuvent toujours être inclus explicitement par le demandeur à l’aide de la méthode [**IVssBackupComponents :: AddComponent**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addcomponent) . Les métadonnées du composant seront ensuite ajoutées au document composants de sauvegarde. En outre, si un sous-composant sélectionnable pour la sauvegarde définit un jeu de composants, les membres de ce jeu de composants sont implicitement inclus dans la sauvegarde.

Le cas « MyWriter » présenté dans [chemin logique des composants](logical-pathing-of-components.md) peut être utilisé comme exemple pour illustrer la sélectivité de la sauvegarde.



| Nom du composant | Chemin logique            | Sélectionnable pour la sauvegarde |
|----------------|-------------------------|-----------------------|
| Exécut  | ""                      | N                     |
| "ConfigFiles"  | Exécut           | N                     |
| "LicenseInfo"  | ""                      | O                     |
| « Security »     | ""                      | O                     |
| UserInfo     | « Security »              | N                     |
| EUR.1 | « Security »              | N                     |
| "writerData"   | ""                      | O                     |
| Jeu1         | "writerData"            | N                     |
| Janvier          | « writerData \\ Set1 »      | N                     |
| Decembre          | « writerData \\ Set1 »      | N                     |
| Set2         | "writerData"            | N                     |
| Janvier          | « writerData \\ Set2 »      | N                     |
| Decembre          | « writerData \\ Set2 »      | N                     |
| Demande        | « writerData \\ QueryLogs » | N                     |
| Syntaxe        | "writerData"            | O                     |
| Janvier          | « utilisation de writerData \\ »     | N                     |
| Decembre          | « utilisation de writerData \\ »     | N                     |



 

Chaque fois que « MyWriter » est sauvegardé, l’inclusion explicite du composant « exécutables » à l’aide de la méthode [**IVssBackupComponents :: AddComponent**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addcomponent) inclut implicitement le composant « ConfigFiles ».

Le composant « LicenseInfo » est un composant autonome sélectionnable pour la sauvegarde. Il peut être sélectionné à l’aide de la méthode [**IVssBackupComponents :: AddComponent**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addcomponent) à la discrétion du demandeur, mais sa sélection ne sélectionne aucun autre composant.

Le composant sélectionnable-for-Backup « Security » définit un ensemble de composants simple contenant deux sous-composants non sélectionnables pour la sauvegarde, « UserInfo » et « Certificates ». Si la « sécurité » est explicitement incluse pour la sauvegarde, les « UserInfo » et les « certificats » sont toujours également inclus implicitement. Il n’existe aucun moyen d’inclure les sous-composants « UserInfo » ou « Certificates » dans une opération de sauvegarde, sauf si la « sécurité » est incluse.

Si le composant « writerData » est sélectionné, les composants non sélectionnables pour la sauvegarde « Set1 », « Set2 » et « requête », ainsi que le composant sélectionnable-for-Backup « utilisation », sont implicitement sélectionnés. Chacun de ces composants a des sous-composants qui sont implicitement sélectionnés pour la sauvegarde. Aucune de leurs métadonnées ne sera ajoutée au document des composants de sauvegarde.

Si le composant « writerData » n’est pas sélectionné, les composants non sélectionnables-for-Backup « Set1 », « Set2 » et « Query » ne sont pas inclus pour la sauvegarde.

Toutefois, les demandeurs peuvent choisir d’inclure explicitement le sélectionnable pour le composant de sauvegarde « utilisation ». Les métadonnées de ce composant seront ajoutées au document des composants de sauvegarde. Les sous-composants « utilisation » « Jan » et « DEC » seront implicitement ajoutés à la sauvegarde, mais leurs informations ne seront pas ajoutées au document des composants de sauvegarde.

L’inclusion explicite d’un composant pour la sauvegarde crée une instance [**IVssComponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) correspondante dans le document composants de sauvegarde.

Un demandeur récupère des informations sur les composants inclus explicitement dans son document de composants de sauvegarde en examinant ces Writers (à l’aide de [**IVssBackupComponents :: GetWriterComponents**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwritercomponents)) inclus dans son document et en extrayant les objets [**IVssComponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) stockés.

Comme les informations sur le jeu de fichiers (spécification de fichier, chemin d’accès et indicateur de récurrence) des composants présents dans le document sur les composants de sauvegarde ne sont pas présentes, les demandeurs doivent interroger les documents de métadonnées de l’enregistreur pour obtenir des informations complètes sur tous les composants inclus dans le document des composants de sauvegarde.

 

 




