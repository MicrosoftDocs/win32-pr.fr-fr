---
description: Création de clichés instantanés pour les fournisseurs
ms.assetid: d5042945-ba81-40d0-b204-1f08d153a788
title: Création de clichés instantanés pour les fournisseurs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 91cc7306e7a13ef8e96ab032016a922411a70f95
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104034340"
---
# <a name="shadow-copy-creation-for-providers"></a>Création de clichés instantanés pour les fournisseurs

## <a name="the-shadow-copy-creation-process"></a>Processus de création de clichés instantanés

Un demandeur est l’application qui initie la demande de création d’un cliché instantané. En général, le demandeur est une application de sauvegarde. Le cas échéant, VSS appellera les fournisseurs concernés. La plupart des fournisseurs sont intéressés par trois demandes spécifiques du demandeur.

1.  Le demandeur commence l’activité de création de clichés instantanés à l’aide d’un appel à [**IVssBackupComponents :: StartSnapshotSet**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-startsnapshotset). Cela génère un **GUID** de type **\_ ID VSS** qui identifie de façon unique ce jeu de clichés instantanés spécifique-the SnapshotSetId. Le fournisseur n’est pas impliqué dans cette étape, mais SnapshotSetId est largement utilisé dans toutes les étapes suivantes.
2.  Pour chaque volume qu’il souhaite inclure dans ce jeu de clichés instantanés, le demandeur appelle [**IVssBackupComponents :: AddToSnapshotSet**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addtosnapshotset). VSS détermine le fournisseur qui sera utilisé pour copier par cliché instantané le volume.
    -   Plusieurs fournisseurs peuvent participer à un jeu de clichés instantanés. Par exemple, si le volume système et un volume de données font partie du même jeu de clichés instantanés, le fournisseur système peut faire office de fournisseur de clichés instantanés pour le volume système alors qu’un fournisseur de matériel peut servir de fournisseur de clichés instantanés pour le volume de données. Les deux fournisseurs font partie du même jeu de clichés instantanés et l’utilisateur s’attend à obtenir la même cohérence ponctuelle sur les deux volumes.
    -   Pour pouvoir sélectionner un fournisseur de matériel, le fournisseur de matériel doit être en mesure de prendre en charge tous les numéros d’unités logiques contribuant au volume spécifié.
    -   Tous les fournisseurs inscrits ont la possibilité d’indiquer la prise en charge d’un volume donné lors de la création de clichés instantanés. Si plusieurs fournisseurs indiquent la prise en charge, VSS utilise par défaut les fournisseurs de matériel, les fournisseurs de logiciels et enfin le fournisseur système (si aucun autre fournisseur n’indique la prise en charge de ce volume).
    -   Un demandeur peut remplacer cet ordre par défaut en indiquant explicitement le fournisseur requis pour créer le cliché instantané.
    -   Si plusieurs fournisseurs de matériel prennent en charge un volume donné, il n’existe aucune garantie quant à l’ordre dans lequel les fournisseurs de matériel sont appelés.
3.  Après un ou plusieurs appels à [**AddToSnapshotSet**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addtosnapshotset), le demandeur peut demander la création du cliché instantané à l’aide de la méthode [**IVssBackupComponents ::D osnapshotset**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-dosnapshotset) . VSS utilise ensuite le système pour créer le cliché instantané. La méthode **DoSnapshotSet** effectue ce travail de façon asynchrone et le demandeur peut interroger ou attendre la fin du processus de création de clichés instantanés.

Ce diagramme illustre les interactions entre le demandeur, le service VSS, la prise en charge du noyau VSS, tous les enregistreurs VSS impliqués et tous les fournisseurs de matériel VSS. Consultez [le processus de création](the-shadow-copy-creation-process.md) de clichés instantanés pour obtenir une description détaillée de ces interactions.

![interactions entre le demandeur, les composants de sauvegarde, les rédacteurs et les fournisseurs](images/vssimpl.png)

Lorsque le processus de création de clichés instantanés est terminé, le demandeur peut déterminer si la création du cliché instantané a réussi et, si ce n’est pas le cas, déterminer la source de l’échec.

L’intervalle de temps entre le gel et le dégel des applications du writer doit être réduit. Le fournisseur doit démarrer de façon asynchrone tout le travail de préparation lié au cliché instantané (par exemple, un fournisseur de matériel qui utilise des plex démarrant la synchronisation) dans la méthode [**IVssHardwareSnapshotProvider :: BeginPrepareSnapshot**](/windows/desktop/api/VsProv/nf-vsprov-ivsshardwaresnapshotprovider-beginpreparesnapshot) , puis attendre la fin de la méthode [**IVssProviderCreateSnapshotSet :: EndPrepareSnapshots**](/windows/desktop/api/VsProv/nf-vsprov-ivssprovidercreatesnapshotset-endpreparesnapshots) .

Il existe plusieurs fenêtres de limite de minutage que les fournisseurs doivent suivre. Par conséquent, les fournisseurs corrects effectuent tout traitement inutile avant [**IVssProviderCreateSnapshotSet ::P recommitsnapshots**](/windows/desktop/api/VsProv/nf-vsprov-ivssprovidercreatesnapshotset-precommitsnapshots) et après [**IVssProviderCreateSnapshotSet ::P ostcommitsnapshots**](/windows/desktop/api/VsProv/nf-vsprov-ivssprovidercreatesnapshotset-postcommitsnapshots).

Le jeu de clichés instantanés est fixe lorsque [**DoSnapshotSet**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-dosnapshotset) est appelé. Des volumes supplémentaires ne peuvent pas être ajoutés ultérieurement, car les volumes supplémentaires ne partagent pas le même point dans le temps.

Il existe une limite de 64 volumes dans le jeu de clichés instantanés. Un volume spécifique peut correspondre à un numéro d’unité logique (LUN) entier, à une partie d’un numéro d’unité logique ou à des parties de plusieurs numéros d’unités logiques. La plupart des configurations auront un volume par LUN, bien que des mappages arbitraires soient possibles.

Il n’existe aucune limite quant au nombre de jeux de clichés instantanés ou au nombre de jeux de clichés instantanés d’un volume d’origine. Un fournisseur peut définir des limites spécifiques ou limiter dynamiquement en fonction des ressources matérielles disponibles.

### <a name="point-in-time-for-writerless-applications"></a>Point dans le temps pour les applications qui n’ont pas été en écriture

VSS comprend une prise en charge spéciale qui définit le point dans le temps qui est commun pour tous les volumes d’un jeu de clichés instantanés. Les fournisseurs de matériel n’ont pas besoin d’interagir directement avec ces technologies de noyau, car ils sont appelés dans le cadre du traitement normal des validations de clichés instantanés. Toutefois, il est utile de comprendre les mécanismes utilisés, car il explique la définition du « point dans le temps » pour les applications sans écriture (les applications qui n’ont pas exposé une interface d’enregistreur VSS et ne participent donc pas au processus de création de cliché instantané de volume.)

Cette prise en charge du noyau VSS pour un point dans le temps commun est distribuée entre le pilote VolSnap.sys, les systèmes de fichiers et VSS.

1.  Pour que la prise en charge du noyau VSS soit appelée, VSS a déjà effectué les opérations suivantes :
    1.  Déterminez les volumes qui doivent être impliqués dans le cliché instantané.
    2.  Déterminez le fournisseur à utiliser sur chaque volume.
    3.  Applications figées qui acceptent des messages de blocage/libération.
    4.  Préparez les fournisseurs pour le cliché instantané en appelant les méthodes [**PreCommitSnapshots**](/windows/desktop/api/VsProv/nf-vsprov-ivssprovidercreatesnapshotset-precommitsnapshots) . Tous les fournisseurs sont en attente de la création du cliché instantané réel.
2.  Le point dans le temps est alors créé. VSS vide simultanément les systèmes de fichiers sur tous les volumes qui doivent faire l’objet de clichés instantanés.
    1.  VSS émet une \_ \_ \_ \_ \_ commande de contrôle de vidage et de conservation des écritures IOCTL VOLSNAP sur chaque volume qui vide les systèmes de fichiers. Cette IOCTL est passée dans la pile de stockage à VolSnap.sys. VolSnap.sys contient ensuite tous les paquets IRP d’écriture jusqu’à l’étape 4 ci-dessous. Tout système de fichiers (par exemple, RAW) sans prise en charge de ce nouvel IOCTL passe l’IOCTL inconnu, où il est de nouveau détenu par VolSnap.sys. Sur les volumes NTFS, le vidage valide également le journal NTFS.
    2.  Cela interrompt toutes les activités de métadonnées NTFS/FAT ; les métadonnées du système de fichiers sont correctement validées.
    3.  Le cliché instantané instantané : VolSnap.sys entraîne la mise en file d’attente de tous les paquets IRP d’écriture suivants sur tous les volumes qui doivent être des clichés instantanés.
    4.  VolSnap.sys attend la fin de toutes les écritures en attente sur les volumes de clichés instantanés. Les volumes sont à présent inutilisables en ce qui concerne les écritures et ont été reposés à exactement le même moment sur chaque volume. Il n’existe aucune garantie concernant les écritures dans les sections mappées par l’utilisateur ou les écritures émises entre (a) et (b) sur les systèmes de fichiers qui n’implémentent pas l’IOCTL de vidage (par exemple, RAW).
3.  VSS ordonne à chaque fournisseur d’effectuer le cliché instantané en appelant les méthodes [**IVssProviderCreateSnapshotSet :: CommitSnapshots**](/windows/desktop/api/VsProv/nf-vsprov-ivssprovidercreatesnapshotset-commitsnapshots) . La préparation des fournisseurs doit être terminée afin qu’il s’agit d’une opération rapide.

    Notez que le système d’e/s n’est pas utilisé pendant l’exécution de ces méthodes [**CommitSnapshots**](/windows/desktop/api/VsProv/nf-vsprov-ivssprovidercreatesnapshotset-commitsnapshots) . Si un fournisseur effectue une synchronisation des numéros d’unités logiques de la source et des clichés instantanés, cette synchronisation doit être effectuée avant le retour de la méthode **CommitSnapshots** du fournisseur. Elle ne peut pas être exécutée de façon asynchrone.

4.  Immédiatement après le retour de la méthode [**CommitSnapshots**](/windows/desktop/api/VsProv/nf-vsprov-ivssprovidercreatesnapshotset-commitsnapshots) du dernier fournisseur, VSS libère tous les paquets IRP d’écriture en attente (y compris les IRP qui bloquent les systèmes de fichiers à la fin de leurs chemins de validation) en appelant un autre IRP transmis à VolSnap.sys.
5.  Si le processus de cliché instantané a réussi, alors VSS :
    1.  Appelle [**PostCommitSnapshots**](/windows/desktop/api/VsProv/nf-vsprov-ivssprovidercreatesnapshotset-postcommitsnapshots) pour les fournisseurs impliqués.
    2.  Appelle [**CVssWriter :: OnThaw**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onthaw) pour les Writers impliqués.
    3.  Informe le demandeur que le processus de cliché instantané est terminé.

[**PreCommitSnapshots**](/windows/desktop/api/VsProv/nf-vsprov-ivssprovidercreatesnapshotset-precommitsnapshots), [**CommitSnapshots**](/windows/desktop/api/VsProv/nf-vsprov-ivssprovidercreatesnapshotset-commitsnapshots), [**PostCommitSnapshots**](/windows/desktop/api/VsProv/nf-vsprov-ivssprovidercreatesnapshotset-postcommitsnapshots) sont tout à la fois critiques. Toutes les e/s des applications avec des enregistreurs sont figées de **PreCommitSnapshots** à **PostCommitSnapshots**; tout retard affecte la disponibilité de l’application. Toutes les e/s de fichier, y compris les e/s d’application sans enregistreur, sont interrompues pendant **CommitSnapshots**.

Les fournisseurs doivent effectuer tout le travail critique avant de retourner à partir de [**EndPrepareSnapshots**](/windows/desktop/api/VsProv/nf-vsprov-ivssprovidercreatesnapshotset-endpreparesnapshots).

-   [**CommitSnapshots**](/windows/desktop/api/VsProv/nf-vsprov-ivssprovidercreatesnapshotset-commitsnapshots) doit être retourné en quelques secondes. La phase **CommitSnapshots** se trouve dans la fenêtre de vidage et de suspension. La prise en charge du noyau VSS annule le vidage et le blocage qui maintiennent les e/s si la version suivante n’est pas reçue dans les 10 secondes, et VSS ne parvient pas à créer le cliché instantané. D’autres activités se produiront sur le système, de sorte qu’un fournisseur ne doit pas s’appuyer sur la durée totale de 10 secondes. Le fournisseur ne doit pas appeler les API Win32 au cours de la validation, car le nombre d’écritures et de bloc est inattendu. Si le fournisseur prend plus de quelques secondes pour terminer l’appel, il y a une forte probabilité que cette opération échoue.
-   La séquence complète de [**PreCommitSnapshots**](/windows/desktop/api/VsProv/nf-vsprov-ivssprovidercreatesnapshotset-precommitsnapshots) au retour de [**PostCommitSnapshots**](/windows/desktop/api/VsProv/nf-vsprov-ivssprovidercreatesnapshotset-postcommitsnapshots) est mappée à la fenêtre entre les enregistreurs recevant les événements Freeze et dégeler. La valeur par défaut de l’enregistreur pour cette fenêtre est de 60 secondes, mais un enregistreur peut remplacer cette valeur par un délai d’expiration plus court. Par exemple, l’enregistreur Microsoft Exchange Server change le délai d’expiration à 20 secondes. Les fournisseurs ne doivent pas passer plus d’une seconde ou deux dans cette méthode.

Pendant la [**CommitSnapshots**](/windows/desktop/api/VsProv/nf-vsprov-ivssprovidercreatesnapshotset-commitsnapshots) , le fournisseur doit éviter toute e/s de fichier non paginée ; ces e/s ont une probabilité très élevée de blocage. En particulier, le fournisseur ne doit pas écrire de manière synchrone les journaux de débogage ou de suivi.

 

 



