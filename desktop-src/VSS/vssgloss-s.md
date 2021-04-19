---
description: A B C D E F G H I J K L M N O P Q R S T U V W X Y Z
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: c4f826bc-ea80-4fd5-99da-630e7ae56dd7
title: S (Service VSS)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eb5979d30f0b88762a2d022a89063ee44bd91a3a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106514617"
---
# <a name="s-volume-shadow-copy-service"></a>S (Service VSS)

[A](vssgloss-a.md) [B](vssgloss-b.md) [C](vssgloss-c.md) [D](vssgloss-d.md) [e](vssgloss-e.md) [F](vssgloss-f.md) [G](vssgloss-g.md) [H](vssgloss-h.md) [I](vssgloss-i.md) J K [L](vssgloss-l.md) M [N](vssgloss-n.md) [O](vssgloss-o.md) [P](vssgloss-p.md) Q [R](vssgloss-r.md) S [T](vssgloss-t.md) U [V](vssgloss-v.md) [W](vssgloss-w.md) X Y Z

<dl> <dt>

<span id="base.vssgloss_selectability_for_backup"></span><span id="BASE.VSSGLOSS_SELECTABILITY_FOR_BACKUP"></span>**sélectivité pour la sauvegarde**
</dt> <dd>

Un composant est dit sélectionnable pour la sauvegarde si son inclusion explicite dans une opération de sauvegarde est facultative. La sélection de la sauvegarde est activée si la valeur du membre **bSelectable** de la structure [**VSS \_ COMPONENTINFO**](/windows/desktop/api/VsBackup/ns-vsbackup-vss_componentinfo) est **true**. Il n’existe pas de valeur par défaut pour la sélection d’un composant pour la sauvegarde ; un enregistreur doit toujours définir cette valeur explicitement.

Les enregistreurs utilisent également la sélectivité pour la restauration afin d’organiser la participation de leurs composants aux opérations de restauration.

Voir aussi *composant sélectionnable*, *sélectivité pour la restauration*, [*inclusion de composant explicite*](vssgloss-e.md), [*inclusion de composant implicite*](vssgloss-i.md).

</dd> <dt>

<span id="base.vssgloss_selectability_for_restore"></span><span id="BASE.VSSGLOSS_SELECTABILITY_FOR_RESTORE"></span>**sélectivité pour la restauration**
</dt> <dd>

Un composant est dit sélectionnable pour la restauration s’il peut être sauvegardé implicitement en tant que partie d’un jeu de composants, puis restauré séparément par la suite sans le reste du jeu de composants. La sélection de la restauration est activée si la valeur du membre **bSelectableForRestore** de la structure [**VSS \_ COMPONENTINFO**](/windows/desktop/api/VsBackup/ns-vsbackup-vss_componentinfo) est **true**. Par défaut, la sélection d’un composant pour la restauration est **false**. La sélectivité pour la restauration n’a de sens que lorsqu’un composant n’a pas été ajouté au document de sauvegarde.

Voir aussi *composant sélectionnable*, *sélectivité pour la sauvegarde*, [*inclusion de composant explicite*](vssgloss-e.md), [*inclusion de composant implicite*](vssgloss-i.md).

</dd> <dt>

<span id="base.vssgloss_selectable_component"></span><span id="BASE.VSSGLOSS_SELECTABLE_COMPONENT"></span>**composant sélectionnable**
</dt> <dd>

Un composant est dit sélectionnable si son inclusion explicite dans une opération de sauvegarde ou de restauration est facultative.

La sélection de la sauvegarde et de la sélectivité pour la restauration est indépendante les unes des autres. un composant peut être sélectionnable pour les deux opérations, pour la restauration et non pour la sauvegarde, ou pour la sauvegarde et non pour la restauration.

Les enregistreurs utilisent également la sélectivité pour organiser leurs composants en groupes :

-   Les composants non sélectionnables sans ancêtres sélectionnables dans leurs chemins logiques doivent toujours être explicitement inclus si un enregistreur doit être sauvegardé ou restauré.
-   Les composants non sélectionnables avec des ancêtres sélectionnables seront inclus dans une sauvegarde ou une restauration uniquement si au moins un ancêtre sélectionnable est inclus.
-   Les composants sélectionnables sans ancêtres sélectionnables ne peuvent être inclus que dans une opération de sauvegarde ou de restauration.
-   Les composants sélectionnables avec des ancêtres sélectionnables peuvent être explicitement inclus dans une opération de sauvegarde ou de restauration, ou peuvent être implicitement inclus si l’un de leurs ancêtres sélectionnables est inclus.

Voir aussi [*composants*](vssgloss-c.md), *sélection pour la sauvegarde*, *sélectivité pour la restauration*, [*inclusion de composant explicite*](vssgloss-e.md), [*inclusion de composant implicite*](vssgloss-i.md).

</dd> <dt>

<span id="base.vssgloss_shadow_copy"></span><span id="BASE.VSSGLOSS_SHADOW_COPY"></span>**cliché instantané**
</dt> <dd>

Réplica à un point dans le temps en lecture seule du contenu d’un volume d’origine. Chaque cliché instantané est indexé par un GUID persistant. Également appelé cliché instantané du volume. Voir aussi *jeu de clichés instantanés*.

</dd> <dt>

<span id="base.vssgloss_shadow_copies_for_shared_folders"></span><span id="BASE.VSSGLOSS_SHADOW_COPIES_FOR_SHARED_FOLDERS"></span>**clichés instantanés pour dossiers partagés**
</dt> <dd>

Fonctionnalité de Windows qui crée des copies de sauvegarde en ligne légères de volumes à l’aide de VSS. Les clients peuvent accéder à ces sauvegardes via le shell Windows pour voir les anciennes versions des fichiers et annuler des erreurs sans nécessiter une restauration complète. Voir aussi cliché [*instantané accessible*](vssgloss-c.md)par le client.

</dd> <dt>

<span id="base.vssgloss_shadow_copy_set"></span><span id="BASE.VSSGLOSS_SHADOW_COPY_SET"></span>**jeu de clichés instantanés**
</dt> <dd>

Collection de clichés instantanés de volume créés en même temps et identifiées par un ID de jeu de clichés instantanés commun (valeur GUID persistant). Il s’agit du mécanisme utilisé pour permettre la gestion d’une opération de cliché instantané sur plusieurs volumes. Voir aussi cliché *instantané*.

</dd> <dt>

<span id="base.vssgloss_software_based_provider"></span><span id="BASE.VSSGLOSS_SOFTWARE_BASED_PROVIDER"></span>**fournisseur de logiciels**
</dt> <dd>

Fournisseur qui intercepte les demandes d’e/s au niveau du logiciel entre le système de fichiers et le gestionnaire de volume. Voir aussi [*fournisseur de matériel*](vssgloss-h.md), [*fournisseur*](vssgloss-p.md).

</dd> <dt>

<span id="base.vssgloss_subcomponent"></span><span id="BASE.VSSGLOSS_SUBCOMPONENT"></span>**sous-composant**
</dt> <dd>

Tout composant qui possède un chemin d’accès logique contenant un élément sélectionnable (pour la sauvegarde ou la restauration) du composant parent. Les sous-composants doivent avoir un chemin d’accès logique au format {nom du composant \_ } {nom du sous- \\ composant \_ }. Si l’ancêtre d’un sous-composant (pour la sauvegarde ou la restauration) est explicitement inclus dans une sauvegarde ou une restauration, le sous-composant est implicitement inclus dans l’opération. Les sous-composants inclus implicitement n’ont pas leurs données incluses dans le document des composants de sauvegarde, qu’ils soient sélectionnables (pour la restauration ou la sauvegarde) ou non. Voir aussi [*composant*](vssgloss-c.md), [*chemin logique*](vssgloss-l.md).

</dd> <dt>

<span id="base.vssgloss_surfaced_shadow_copy"></span><span id="BASE.VSSGLOSS_SURFACED_SHADOW_COPY"></span>**clichés instantanés en surface**
</dt> <dd>

Volume de clichés instantanés visible pour l’espace de noms du gestionnaire de montage d’un système, ce qui signifie que **FindFirstVolume** et **FindNextVolume** peuvent le trouver et que les notifications d’arrivée et de départ du volume sont générées. Tous les clichés instantanés exposés sont également des clichés instantanés en surface. Toutefois, un cliché instantané superficiel n’a pas besoin d’être exposé. Si un cliché instantané est transportable, il ne peut pas être exposé. Voir aussi cliché [*instantané exposé*](vssgloss-e.md), cliché [*instantané transportable*](vssgloss-t.md).

</dd> <dt>

<span id="base.vssgloss_system_file_protection"></span><span id="BASE.VSSGLOSS_SYSTEM_FILE_PROTECTION"></span>**Protection des fichiers système**
</dt> <dd>

Voir [*protection des fichiers Windows*](vssgloss-w.md).

</dd> <dt>

<span id="base.vssgloss_system_level_applications"></span><span id="BASE.VSSGLOSS_SYSTEM_LEVEL_APPLICATIONS"></span>**applications au niveau système**
</dt> <dd>

Indique le point auquel le service VSS notifie un enregistreur d’un gel. Les enregistreurs qui sont initialisés en tant qu’applications au niveau du système sont avertis après que les rédacteurs ont été initialisés en tant qu’applications de niveau frontal ou en tant qu’applications de niveau principal. Consultez également [*niveau application*](vssgloss-a.md), [*applications de niveau*](vssgloss-b.md)principal, [*applications de niveau frontal*](vssgloss-f.md).

</dd> <dt>

<span id="base.vssgloss_system_provider"></span><span id="BASE.VSSGLOSS_SYSTEM_PROVIDER"></span>**fournisseur système**
</dt> <dd>

Fournisseur préinstallé par défaut fourni dans le cadre de Windows.

</dd> <dt>

<span id="base.vssgloss_system_volume_folder"></span><span id="BASE.VSSGLOSS_SYSTEM_VOLUME_FOLDER"></span>**Dossier du volume système**
</dt> <dd>

Répertoire partagé qui stocke les copies partagées des fichiers publics d’un domaine, c’est-à-dire les fichiers répliqués sur tous les contrôleurs de domaine du domaine.

</dd> </dl>

 

 



