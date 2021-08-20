---
description: une application de sauvegarde et de récupération VSS qui effectue une récupération d’urgence (également appelée récupération complète) peut utiliser le générateur de récupération automatique du système (ASR) avec environnement de préinstallation Windows (WinPE) (Windows PE) pour sauvegarder et restaurer les volumes critiques et d’autres composants de l’état du système de démarrage. L’application de sauvegarde est implémentée en tant que demandeur VSS.
ms.assetid: 13adfd79-f26a-4385-9b59-129d06fa72eb
title: Utilisation de la récupération automatique du système VSS pour la récupération d’urgence
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6813f0f746600fa665ed20bb208f3241cb1a88a12de721d53a8afa77be4a4c35
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118998059"
---
# <a name="using-vss-automated-system-recovery-for-disaster-recovery"></a>Utilisation de la récupération automatique du système VSS pour la récupération d’urgence

une application de sauvegarde et de récupération VSS qui effectue une récupération d’urgence (également appelée récupération complète) peut utiliser le générateur de récupération automatique du système (ASR) avec environnement de préinstallation Windows (WinPE) (Windows PE) pour sauvegarder et restaurer les volumes critiques et d’autres composants de l’état du système de démarrage. L’application de sauvegarde est implémentée en tant que demandeur VSS.

**Remarque**  les Applications qui utilisent ASR doivent disposer d’une licence Windows PE.

**Windows Server 2003 et Windows XP :** La récupération automatique du système n’est pas implémentée en tant qu’enregistreur VSS.

Pour plus d’informations sur les outils de suivi que vous pouvez utiliser avec la récupération automatique du système, consultez [utilisation des outils de suivi avec les applications ASR VSS](using-tracing-tools-with-vss-asr-applications.md).

**Dans cet article :**

-   [Vue d’ensemble des tâches de phase de sauvegarde](#overview-of-backup-phase-tasks)
-   [Choix des composants critiques à sauvegarder](#choosing-which-critical-components-to-back-up)
-   [Vue d’ensemble des tâches de la phase de restauration](#overview-of-restore-phase-tasks)
-   [Exclusion de tous les disques d’un volume](#excluding-all-disks-for-a-volume)

## <a name="overview-of-backup-phase-tasks"></a>Vue d’ensemble des tâches de phase de sauvegarde

Au moment de la sauvegarde, le demandeur effectue les étapes suivantes.

> [!Note]  
> Toutes les étapes sont requises sauf indication contraire.

 

1.  Appelez la fonction [**CreateVssBackupComponents**](/windows/desktop/api/VsBackup/nf-vsbackup-createvssbackupcomponents) pour créer une instance de l’interface [**IVssBackupComponents**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents) et appelez la méthode [**IVssBackupComponents :: InitializeForBackup**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-initializeforbackup) pour initialiser l’instance afin de gérer une sauvegarde.
2.  Appelez [**IVssBackupComponents :: SetContext**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setcontext) pour définir le contexte de l’opération de cliché instantané.
3.  Appelez [**IVssBackupComponents :: SetBackupState**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setbackupstate) pour configurer la sauvegarde. Affectez la **valeur true** au paramètre *bBackupBootableSystemState* pour indiquer que la sauvegarde inclura un État du système de démarrage.
4.  Choisissez les composants critiques dans le document de métadonnées de l’enregistreur de l’Enregistreur ASR à sauvegarder et appelez [**IVssBackupComponents :: AddComponent**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addcomponent) pour chacun d’eux.
5.  Appelez [**IVssBackupComponents :: StartSnapshotSet**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-startsnapshotset) pour créer un jeu de clichés instantanés vide.
6.  Appelez [**IVssBackupComponents :: GatherWriterMetadata**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwritermetadata) pour initier un contact asynchrone avec des enregistreurs.
7.  Appelez [**IVssBackupComponents :: GetWriterMetadata**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwritermetadata) pour récupérer le document des métadonnées de l’enregistreur de l’Enregistreur ASR. L’ID d’enregistreur pour l’Enregistreur ASR est BE000CBE-11FE-4426-9C58-531AA6355FC4 et la chaîne du nom de l’enregistreur est « Enregistreur ASR ».
8.  Appelez [**IVssExamineWriterMetadata :: SaveAsXML**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssexaminewritermetadata-saveasxml) pour enregistrer une copie du document de métadonnées de l’enregistreur de l’Enregistreur ASR.
9.  Appelez [**IVssBackupComponents :: AddToSnapshotSet**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addtosnapshotset) pour chaque volume qui peut participer aux clichés instantanés pour ajouter le volume au jeu de clichés instantanés.
10. Appelez [**IVssBackupComponents ::P repareforbackup**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prepareforbackup) pour notifier aux rédacteurs de se préparer pour une opération de sauvegarde.
11. Appelez [**IVssBackupComponents :: GatherWriterStatus**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwriterstatus) et [**IVssBackupComponents :: GetWriterStatus**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwriterstatus) (ou [**IVssBackupComponentsEx3 :: GetWriterStatus**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponentsex3-getwriterstatusex)) pour vérifier l’état de l’Enregistreur ASR.
12. À ce stade, vous pouvez interroger les messages d’échec qui ont été définis par le writer dans sa méthode [**CVssWriter :: OnPrepareBackup**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onpreparebackup) . Pour obtenir un exemple de code qui montre comment afficher ces messages, consultez [**IVssComponentEx :: GetPrepareForBackupFailureMsg**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponentex-getprepareforbackupfailuremsg).
13. Appelez [**IVssBackupComponents ::D osnapshotset**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-dosnapshotset) pour créer un cliché instantané du volume.
14. Appelez [**IVssBackupComponents :: GatherWriterStatus**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwriterstatus) et [**IVssBackupComponents :: GetWriterStatus**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwriterstatus) pour vérifier l’état de l’Enregistreur ASR.
15. Sauvegardez les données.
16. Indiquez si l’opération de sauvegarde a réussi en appelant [**IVssBackupComponents :: SetBackupSucceeded**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setbackupsucceeded).
17. Appelez [**IVssBackupComponents :: BackupComplete**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-backupcomplete) pour indiquer que l’opération de sauvegarde est terminée.
18. Appelez [**IVssBackupComponents :: GatherWriterStatus**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwriterstatus) et [**IVssBackupComponents :: GetWriterStatus**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwriterstatus). La mémoire de l’état de session du writer est une ressource limitée, et les enregistreurs doivent finalement réutiliser les États de session. Cette étape marque l’état de la session de sauvegarde du writer comme étant terminé et notifie à VSS que cet emplacement de session de sauvegarde peut être réutilisé par une opération de sauvegarde ultérieure.
    > [!Note]  
    > cela est nécessaire uniquement sur Windows Server 2008 avec Service Pack 2 (SP2) et versions antérieures.

     

19. Appelez [**IVssBackupComponents :: SaveAsXML**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-saveasxml) pour enregistrer une copie du document des composants de sauvegarde du demandeur. Les informations contenues dans le document composants de sauvegarde sont utilisées au moment de la restauration lorsque le demandeur appelle la méthode [**IVssBackupComponents :: InitializeForRestore**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-initializeforrestore) .

## <a name="choosing-which-critical-components-to-back-up"></a>Choix des composants critiques à sauvegarder

Dans la phase d’initialisation de la sauvegarde, le rédacteur ASR signale les types de composants suivants dans son document de métadonnées d’écriture :

-   volumes critiques, tels que les volumes de démarrage, système et d’environnement de récupération Windows (Windows RE), ainsi que la partition de Windows RE associée à l’instance de Windows Vista ou Windows Server 2008 qui est en cours d’exécution. Un volume est un *volume critique* s’il contient des informations sur l’état du système. Les volumes de démarrage et système sont inclus automatiquement. Le demandeur doit inclure tous les volumes qui contiennent les composants critiques du système signalés par les writers, tels que les volumes qui contiennent le Active Directory. Les composants critiques du système sont marqués comme étant « non sélectionnables pour la sauvegarde ». Dans VSS, « non sélectionnable » signifie « non facultatif ». Ainsi, le demandeur doit les sauvegarder dans le cadre de l’état du système. Pour plus d’informations, consultez [sauvegarde et restauration](locating-additional-system-files.md)de l’état du système. Les composants pour lesquels l’indicateur de l’état du système du service de configuration n' \_ \_ est pas défini ne \_ \_ sont pas critiques du système.
    > [!Note]  
    > Le composant ASR est un composant critique du système qui est signalé par l’Enregistreur ASR.

     

-   Disques. Chaque disque fixe de l’ordinateur est exposé en tant que composant dans ASR. Si un disque n’a pas été exclu lors de la sauvegarde, il sera affecté lors de la restauration et peut être recréé et reformaté. Notez que pendant la restauration, le demandeur peut toujours recréer un disque qui a été exclu pendant la sauvegarde en appelant la méthode [**IVssBackupComponents :: SetRestoreOptions**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setrestoreoptions) . Si un disque d’un pack de disques dynamique est sélectionné, tous les autres disques de ce Pack doivent également être sélectionnés. Si un volume est sélectionné parce qu’il s’agit d’un volume critique (autrement dit, un volume qui contient des informations sur l’état du système), chaque disque contenant une étendue pour ce volume doit également être sélectionné. Pour rechercher les étendues d’un volume, utilisez le code de contrôle d' [**\_ \_ \_ \_ \_ étendues du disque**](/windows/win32/api/winioctl/ni-winioctl-ioctl_volume_get_volume_disk_extents) du volume de la récupération du volume ioctl.

    > [!Note]  
    > Pendant la sauvegarde, le demandeur doit inclure tous les disques fixes. Si le disque qui contient le jeu de sauvegarde du demandeur est un disque local, ce disque doit être inclus. Pendant la restauration, le demandeur doit exclure le disque qui contient le jeu de sauvegarde du demandeur pour empêcher son remplacement.

     

    Dans un environnement de clustering, la récupération automatique du système ne recrée pas la disposition des disques partagés du cluster. Ces disques doivent être restaurés en ligne après la restauration du système d’exploitation dans le Windows RE.

-   Magasin Données de configuration de démarrage (BCD) (BCD). Ce composant spécifie le chemin d’accès du répertoire qui contient le magasin BCD. Le demandeur doit spécifier ce composant et sauvegarder tous les fichiers du répertoire du magasin BCD. Pour plus d’informations sur le magasin BCD, consultez [à propos de BCD](/previous-versions/windows/desktop/bcd/about-bcd).
    > [!Note]  
    > Sur les ordinateurs qui utilisent l’interface EFI (Extended firmware interface), la partition système EFI (ESP) est toujours masquée et ne peut pas être incluse dans un cliché instantané de volume. Le demandeur doit sauvegarder le contenu de cette partition. Étant donné que cette partition ne peut pas être incluse dans un cliché instantané de volume, la sauvegarde ne peut être effectuée qu’à partir du volume actif, et non à partir du cliché instantané. Pour plus d’informations sur EFI et ESP, consultez la rubrique afficher le [Guide](/windows-hardware/drivers/bringup/).

Les noms des composants utilisent les formats suivants :

-   Pour les composants de disque, le format est

    <COMPONENT logicalPath="Disks" componentName="harddisk*n*" componentType="filegroup" />

    où *n* est le numéro du disque. Seul le numéro de disque est enregistré. Pour récupérer le numéro du disque, utilisez le code de contrôle de l' [**\_ \_ \_ \_ appareil de stockage IOCTL**](/windows/win32/api/winioctl/ni-winioctl-ioctl_storage_get_device_number) .

-   Pour les composants de volume, le format est

    <COMPONENT logicalPath="Volumes" componentName="Volume{*GUID*}" componentType="filegroup" />

    où *GUID* est le GUID du volume.

-   Pour le composant magasin BCD, le format est

    <COMPONENT logicalPath="BCD" componentName="BCD" componentType="filegroup" componentCaption = "This is the path to the boot BCD store and the boot managers...All the files in this directory need to be backed up...">

    Si la partition système a un nom de GUID de volume, ce composant peut être sélectionné. Dans le cas contraire, il ne peut pas être sélectionné.

    > [!Note]  
    > La récupération automatique du système ajoute les fichiers au groupe de fichiers du composant de stockage BCD comme suit :
    >
    > -   Pour les disques EFI, l’ASR ajoute
    >
    >     *SystemPartitionPath* \\ \\Démarrage de Microsoft EFI \\ \\ \* .\*
    >
    >     où *SystemPartitionPath* est le chemin d’accès à la partition système.
    >
    > -   Pour les disques GPT, l’ASR ajoute
    >
    >     *SystemPartitionPath* \\ Démarrez \\ \* .\*
    >
    >     où *SystemPartitionPath* est le chemin d’accès à la partition système.
    >
    > -   Le chemin d’accès de la partition système se trouve sous la clé de Registre suivante : **HKEY \_ local \_ machine** \\ **System** \\ **Setup** \\ **SystemPartition**

     

Lors de la restauration, tous les composants marqués comme volumes critiques doivent être restaurés. Si un ou plusieurs volumes critiques ne peuvent pas être restaurés, l’opération de restauration échoue.

Dans la phase de [**prérestauration**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prerestore) de la séquence de restauration, les disques qui n’ont pas été exclus lors de la sauvegarde sont recréés et reformatés par défaut. Toutefois, ils ne sont pas recréés ou reformatés s’ils remplissent les conditions suivantes :

-   Un disque de base n’est pas recréé si sa disposition du disque est intacte ou si seules des modifications supplémentaires ont été apportées à celui-ci. La disposition du disque est intacte si les conditions suivantes sont remplies :
    -   La signature de disque, le style de disque (GPT ou MBR), la taille de secteur logique et le décalage de début de volume ne sont pas modifiés.
    -   La taille du volume n’est pas réduite.
    -   Pour les disques GPT, l’identificateur de partition n’est pas modifié.
-   Un disque dynamique n’est pas recréé si sa disposition du disque est intacte ou si seules des modifications supplémentaires ont été apportées à celui-ci. Pour qu’un disque dynamique soit intact, toutes les conditions d’un disque de base doivent être remplies. En outre, la structure du volume de l’ensemble du disque dur doit être intacte. La structure du volume du Pack de disque est intacte si elle remplit les conditions suivantes, qui s’appliquent aux disques MBR et GPT :
    -   Le nombre de volumes disponibles dans le Pack physique durant la restauration doit être supérieur ou égal au nombre de volumes spécifiés dans les métadonnées de l’Enregistreur ASR lors de la sauvegarde.
    -   Le nombre de [*Plex*](../vds/virtual-disk-service-glossary-all.md) par volume doit être inchangé.
    -   Le nombre de [*membres*](../vds/virtual-disk-service-glossary-all.md) doit être inchangé.
    -   Le nombre d’étendues de disque physique doit être supérieur au nombre d’étendues de disque spécifiées dans les métadonnées de l’Enregistreur ASR.
    -   Un pack intact reste intact lors de l’ajout de volumes supplémentaires, ou si un volume du Pack est étendu (par exemple, d’un volume simple à un volume fractionné).
        > [!Note]  
        > Si un volume simple est mis en miroir, le Pack n’est pas intact et sera recréé pour garantir que l’état du volume BCD et du volume de démarrage reste cohérent après la restauration. Si des volumes sont supprimés, le Pack est recréé.

         
-   Si la structure du volume du Pack de disque dynamique est intacte et que seules des modifications supplémentaires ont été apportées à celui-ci, les disques du Pack ne sont pas recréés.

    **Windows Vista :** Les disques dynamiques sont toujours recréés. notez que ce comportement a changé avec Windows Server 2008 et Windows Vista avec Service Pack 1 (SP1).

à tout moment avant le début de la phase de restauration, le demandeur peut spécifier que les disques doivent être au format rapide en définissant la clé de registre **HKEY \_ LOCAL \_ MACHINE** \\ **SOFTWARE** \\ **Microsoft** \\ **Windows NT** \\ **CurrentVersion** \\ **ASR** \\ **RestoreSession** . Sous cette clé, il existe une valeur nommée **QuickFormat** avec le type de données « reg \_ DWORD ». Si cette valeur n’existe pas, vous devez la créer. Définissez les données de la valeur **QuickFormat** sur 1 pour la mise en forme rapide ou sur 0 pour une mise en forme lente.

Si la valeur **QuickFormat** n’existe pas, les disques seront au format lent.

La mise en forme rapide est beaucoup plus rapide que la mise en forme lente (également appelée mise en forme complète). Toutefois, le formatage rapide ne vérifie pas chaque secteur sur le volume.

## <a name="overview-of-restore-phase-tasks"></a>Vue d’ensemble des tâches de la phase de restauration

Au moment de la restauration, le demandeur effectue les étapes suivantes :

> [!Note]  
> Toutes les étapes sont requises sauf indication contraire.

 

1.  Appelez la fonction [**CreateVssBackupComponents**](/windows/desktop/api/VsBackup/nf-vsbackup-createvssbackupcomponents) pour créer une instance de l’interface [**IVssBackupComponents**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents) et appelez la méthode [**IVssBackupComponents :: InitializeForRestore**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-initializeforrestore) pour initialiser l’instance pour la restauration en chargeant le document des composants de sauvegarde du demandeur dans l’instance.
2.  \[Cette étape est requise uniquement si le demandeur doit changer si « IncludeDisk » ou « ExcludeDisk » est spécifié pour un ou plusieurs disques. \] Appelez [**IVssBackupComponents :: SetRestoreOptions**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setrestoreoptions) pour définir les options de restauration des composants de l’Enregistreur ASR. Le rédacteur ASR prend en charge les options suivantes : « IncludeDisk » permet au demandeur d’inclure un disque sur le système cible à prendre en compte pour la restauration, même s’il n’a pas été sélectionné pendant la phase de sauvegarde. « ExcludeDisk » permet au demandeur d’empêcher la recréation d’un disque sur le système cible. Notez que si « ExcludeDisk » est spécifié pour un disque contenant un volume critique, l’appel suivant à [**IVssBackupComponents ::P Restore**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prerestore) échoue.

    L’exemple suivant montre comment utiliser [**SetRestoreOptions**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setrestoreoptions) pour empêcher la recréation du disque 0 et du disque 1 et injecter des pilotes tiers dans le volume de démarrage restauré.

    **Windows server 2008, Windows Vista, Windows server 2003 et Windows XP :** L’injection de pilotes tiers n’est pas prise en charge.

    L’exemple suppose que le pointeur [**IVssBackupComponents**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents) , m \_ pBackupComponents, est valide.

    ```C++
        m_pBackupComponents->SetRestoreOptions(
            AsrWriterId,
            VSS_CT_FILEGROUP,
            NULL,
            TEXT("ASR"),
            TEXT("\"ExcludeDisk\"=\"0\", \"ExcludeDisk\"=\"1\" "),
            TEXT("\"InjectDrivers\"=\"1\" ")
            );
    ```

    

    Pour exclure tous les disques d’un volume spécifié, reportez-vous à la section « exclusion de tous les disques d’un volume ».

3.  Appelez [**IVssBackupComponents ::P Restore**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prerestore) pour indiquer à l’Enregistreur ASR de se préparer à une opération de restauration. Appelez [**IVssAsync :: QueryStatus**](/windows/desktop/api/Vss/nf-vss-ivssasync-querystatus) autant de fois que nécessaire jusqu’à ce que la valeur d’État retournée dans le paramètre *pHrResult* ne soit pas VSS \_ S \_ Async \_ en attente.
4.  Restaurer les données. Au cours de la phase de restauration, ASR reconfigure le chemin d’accès au GUID du volume ( \\ \\ ? \\ Volume {GUID}) pour chaque volume afin qu’il corresponde au chemin d’accès du GUID de volume utilisé pendant la phase de sauvegarde. Toutefois, les lettres de lecteur ne sont pas conservées, car cela entraînerait des collisions avec les lettres de lecteur qui sont automatiquement affectées dans l’environnement de récupération. Ainsi, lors de la restauration de données, le demandeur doit utiliser des chemins d’accès de GUID de volume, et non des lettres de lecteur, pour accéder aux volumes.
5.  définissez la  \\  \\ clé de registre HKLM SOFTWARE **Microsoft** \\ **Windows NT** \\ **CurrentVersion** \\ **ASR** \\ **RestoreSession** pour indiquer l’ensemble des volumes qui ont été restaurés ou reformatés.

    Sous cette clé, il existe une valeur nommée **RestoredVolumes** avec le type de données reg \_ multi \_ sz. Si cette valeur n’existe pas, vous devez la créer. Sous cette valeur, votre demandeur doit créer une entrée de GUID de volume pour chaque volume qui a été restauré. Cette entrée doit être au format suivant : \\ \\ ? \\ Volume {78618c8f-aefd-11da-A898-806e6f6e6963}. À chaque fois qu’une récupération complète est effectuée, la récupération automatique du système définit la valeur **RestoredVolumes** sur l’ensemble des volumes restaurés par ASR. Si le demandeur a restauré des volumes supplémentaires, il doit définir cette valeur sur l’Union de l’ensemble des volumes restaurés par le demandeur et l’ensemble des volumes restaurés par ASR. Si le demandeur n’utilise pas ASR, il doit remplacer la liste des volumes.

    Vous devez également créer une valeur nommée **LastInstance** avec le type de données « reg \_ sz ». Cette clé doit contenir un cookie aléatoire qui identifie de façon unique l’opération de restauration en cours. Un cookie de ce type peut être créé à l’aide des fonctions [**UuidCreate**](/windows/win32/api/rpcdce/nf-rpcdce-uuidcreate) et [**UuidToString**](/windows/win32/api/rpcdce/nf-rpcdce-uuidtostring) . À chaque fois qu’une récupération complète est effectuée, ASR réinitialise cette valeur de Registre pour notifier les demandeurs et les applications de sauvegarde non-VSS que la récupération s’est produite.

6.  Appelez [**IVssBackupComponents ::P ostrestore**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-postrestore) pour indiquer la fin de l’opération de restauration. Appelez [**IVssAsync :: QueryStatus**](/windows/desktop/api/Vss/nf-vss-ivssasync-querystatus) autant de fois que nécessaire jusqu’à ce que la valeur d’État retournée dans le paramètre *pHrResult* ne soit pas VSS \_ S \_ Async \_ en attente.

Au cours de la phase de restauration, la récupération automatique du système peut créer ou supprimer des partitions pour restaurer l’ordinateur à son état précédent. Les demandeurs ne doivent pas essayer de mapper les numéros de disque de la phase de sauvegarde à la phase de restauration.

Lors de la restauration, le demandeur doit exclure le disque qui contient le jeu de sauvegarde du demandeur. Dans le cas contraire, le jeu de sauvegarde peut être remplacé par l’opération de restauration.

Lors de la restauration, un disque est exclu s’il n’a pas été sélectionné en tant que composant lors de la sauvegarde, ou s’il est explicitement exclu en appelant [**IVssBackupComponents :: SetRestoreOptions**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setrestoreoptions) avec l’option « ExcludeDisk » lors de la restauration.

Il est important de noter que lors de la récupération d’urgence de WinPE, la fonctionnalité d’enregistreur ASR est présente, mais aucun autre Writer n’est disponible et le service VSS n’est pas en cours d’exécution. une fois la récupération d’urgence de WinPE terminée, l’ordinateur a redémarré et le système d’exploitation Windows s’exécute normalement, le service VSS peut être démarré et le demandeur peut effectuer des opérations de restauration supplémentaires qui requièrent la participation d’enregistreurs autres que le rédacteur ASR.

Si, au cours de la session de restauration, l’application de sauvegarde détecte que les ID uniques du volume ne sont pas modifiés, et que tous les volumes de l’heure de la sauvegarde sont présents et intacts dans WinPE, l’application de sauvegarde peut continuer à restaurer uniquement le contenu des volumes, sans impliquer la récupération automatique du système. dans ce cas, l’application de sauvegarde doit indiquer que l’ordinateur a été restauré en définissant la clé de registre suivante dans le système d’exploitation restauré : **HKEY \_ LOCAL \_ MACHINE** \\ **SOFTWARE** \\ **Microsoft** \\ **Windows NT** \\ **CurrentVersion** \\ **ASR** \\ **RestoreSession**

Sous cette clé, spécifiez **LastInstance** pour le nom de la valeur, reg \_ SZ pour le type de valeur et un cookie aléatoire (tel qu’un GUID créé par la fonction [**UuidCreate**](/windows/win32/api/rpcdce/nf-rpcdce-uuidcreate) ) pour les données de la valeur.

Si, au cours de la session de restauration, l’application de sauvegarde détecte qu’un ou plusieurs volumes sont modifiés ou manquants, l’application de sauvegarde doit utiliser ASR pour effectuer la restauration. ASR recrée les volumes exactement comme ils l’étaient au moment de la sauvegarde et définit la clé de Registre **RestoreSession** .

## <a name="excluding-all-disks-for-a-volume"></a>Exclusion de tous les disques d’un volume

L’exemple suivant montre comment exclure tous les disques d’un volume spécifié.


```C++
HRESULT BuildRestoreOptionString
(
    const WCHAR             *pwszVolumeNamePath,
    CMyString               *pstrExclusionList
)
{
    HANDLE                  hVolume           = INVALID_HANDLE_VALUE;
    DWORD                   cbSize            = 0;
    VOLUME_DISK_EXTENTS     * pExtents        = NULL;
    DISK_EXTENT             * pExtent         = NULL;
    ULONG                   i                 = 0;
    BOOL                    fIoRet            = FALSE;
    WCHAR                   wszDest[MAX_PATH] = L"";
    CMyString               strVolumeName;
    CMyString               strRestoreOption;

    // Open a handle to the volume device.
    strVolumeName.Set( pwszVolumeNamePath );
    // If the volume name contains a trailing backslash, remove it.
    strVolumeName.UnTrailing( L'\\' );
    hVolume = ::CreateFile(strVolumeName, 0, FILE_SHARE_READ | FILE_SHARE_WRITE, NULL, OPEN_EXISTING, NULL, 0);
    // Check whether the call to CreateFile succeeded.

    // Get the list of disks used by this volume.
    cbSize = sizeof(VOLUME_DISK_EXTENTS);
    pExtents = (VOLUME_DISK_EXTENTS *)::CoTaskMemAlloc(cbSize);

    ::ZeroMemory(pExtents, cbSize);

    fIoRet = ::DeviceIoControl(hVolume, IOCTL_VOLUME_GET_VOLUME_DISK_EXTENTS, NULL, 0, pExtents, cbSize, &cbSize, 0);
    if ( !fIoRet && GetLastError() == ERROR_MORE_DATA )
    {
        // Allocate more memory.
        cbSize = FIELD_OFFSET(VOLUME_DISK_EXTENTS, Extents) + pExtents->NumberOfDiskExtents * sizeof(DISK_EXTENT);
        ::CoTaskMemFree(pExtents);
        pExtents = NULL;

        pExtents = (VOLUME_DISK_EXTENTS *) ::CoTaskMemAlloc(cbSize);
        // Check whether CoTaskMemAlloc returned an out-of-memory error.
        ::ZeroMemory(pExtents, cbSize);

        // Now the buffer should be big enough.
        ::DeviceIoControl(hVolume, IOCTL_VOLUME_GET_VOLUME_DISK_EXTENTS, NULL, 0, pExtents, cbSize, &cbSize, 0);
        // Check whether the IOCTL succeeded.
    }
    // Check for errors; note that the IOCTL can fail for a reason other than insufficient memory.

    // For each disk, mark it to be excluded in the Restore Option string.
    for (i = 0; i < pExtents->NumberOfDiskExtents; i++)
    {
        pExtent = &pExtents->Extents[i];

        *wszDest = L'\0';
        StringCchPrintf(wszDest, MAX_PATH, L"\"ExcludeDisk\"=\"%d\", ", pExtent->DiskNumber); // check errors

        strRestoreOption.Append(wszDest);
        // Check for an out-of-memory error.
    }

    // Remove the trailing comma.
    strRestoreOption.TrimRight();
    strRestoreOption.UnTrailing(',');

    // Set the output parameter.
    strRestoreOption.Transfer( pstrExclusionList );

Exit:
    if( pExtents )
    {
        ::CoTaskMemFree(pExtents);
        pExtents = NULL;
    }

    if( hVolume != INVALID_HANDLE_VALUE )
    {
        ::CloseHandle(hVolume);
        hVolume = INVALID_HANDLE_VALUE;
    }

    return ( hr );
}

```



 

 
