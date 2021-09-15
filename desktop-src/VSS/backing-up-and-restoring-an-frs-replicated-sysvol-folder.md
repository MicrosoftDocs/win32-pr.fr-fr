---
description: Cette rubrique explique comment déterminer si un dossier SYSVOL est répliqué par DFSR ou FSR et explique comment sauvegarder et restaurer un dossier SYSVOL répliqué par le service FRS.
ms.assetid: 32d8a5bd-eeb4-4db6-8129-b5cd3508a7e5
title: Sauvegarde et restauration d’un dossier SYSVOL FRS-Replicated
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ea83ccbc156182a4a3b84c758cb22153f4f7110f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127413409"
---
# <a name="backing-up-and-restoring-an-frs-replicated-sysvol-folder"></a>Sauvegarde et restauration d’un dossier SYSVOL FRS-Replicated

Le dossier volume système (SYSVOL) fournit un emplacement standard pour stocker les éléments importants d' [stratégie de groupe](/previous-versions/windows/it-pro/windows-server-2003/cc779838(v=ws.10)) objets et de scripts. Une copie du dossier SYSVOL existe sur chaque contrôleur de domaine dans un domaine. Le dossier SYSVOL est répliqué par [système de fichiers DFS réplication (DFSR)](/windows-server/storage/dfs-replication/migrate-sysvol-to-dfsr) ou le [service de réplication de fichiers (FRS)](/previous-versions/windows/it-pro/windows-server-2003/cc781582(v=ws.10)). Cette rubrique explique comment déterminer si un dossier SYSVOL est répliqué par DFSR ou FSR et explique comment sauvegarder et restaurer un dossier SYSVOL répliqué par le service FRS.

FRS peut copier le contenu SYSVOL vers d’autres contrôleurs de domaine au sein du domaine. FRS surveille le dossier SYSVOL et, si une modification est apportée à un fichier stocké dans le dossier SYSVOL, le service de réplication de fichiers réplique automatiquement le fichier modifié dans les dossiers SYSVOL sur les autres contrôleurs de domaine du domaine.

> [!Note]  
> Seul le modèle stratégie de groupe est répliqué en répliquant le contenu du dossier SYSVOL. Le conteneur stratégie de groupe est répliqué via la réplication Active Directory. Pour que stratégie de groupe fonctionne correctement, le modèle stratégie de groupe et le conteneur stratégie de groupe doivent être disponibles sur un contrôleur de domaine.

 

Cette rubrique aborde les sujets suivants :

-   [Déterminer si le dossier SYSVOL d’un contrôleur de domaine est répliqué par DFSR ou FRS](#determining-whether-a-domain-controllers-sysvol-folder-is-replicated-by-dfsr-or-frs)
-   [Sauvegarde d’un dossier SYSVOL DFSR-Replicated](#backing-up-a-dfsr-replicated-sysvol-folder)
-   [sauvegarde d’un dossier SYSVOL FRS-Replicated sur un domaine Windows server 2008 ou Windows server 2003](#backing-up-an-frs-replicated-sysvol-folder-on-a-windows-server-2008-or-windows-server-2003-domain)
-   [Exemple de document de métadonnées de l’enregistreur FRS](#sample-frs-writer-metadata-document)
-   [Définition des clés de Registre pour la restauration d’un dossier SYSVOL FRS-Replicated](#setting-registry-keys-for-a-restore-of-an-frs-replicated-sysvol-folder)
-   [Exécution d’une restauration ne faisant pas autorité d’un dossier SYSVOL FRS-Replicated](#performing-a-nonauthoritative-restore-of-an-frs-replicated-sysvol-folder)
-   [Exécution d’une restauration faisant autorité d’un dossier FRS-Replicated SYSVOL](#performing-an-authoritative-restore-of-an-frs-replicated-sysvol-folder)

## <a name="determining-whether-a-domain-controllers-sysvol-folder-is-replicated-by-dfsr-or-frs"></a>Déterminer si le dossier SYSVOL d’un contrôleur de domaine est répliqué par DFSR ou FRS

Le tableau suivant résume la façon de déterminer si le dossier SYSVOL d’un contrôleur de domaine est en cours de réplication par [DFSR](/windows-server/storage/dfs-replication/migrate-sysvol-to-dfsr) ou FRS.

| Si le contrôleur de domaine est en cours d’exécution                                                                                                                  | SYSVOL est répliqué par |
|------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------|
| Windows serveur 2008 + niveau fonctionnel du domaine de Windows server 2008 + [migration SYSVOL](https://blogs.technet.com/filecab/archive/2008/02/08/sysvol-migration-series-part-1-introduction-to-the-sysvol-migration-process.aspx) terminée | DFSR                    |
| Windows serveur 2008 + niveau fonctionnel de domaine sous Windows serveur 2008                                                                              | FILE                     |
| Windows Server 2003                                                                                                                                  | FILE                     |



 

si le [niveau fonctionnel](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc754918(v=ws.10)) du domaine est Windows serveur 2008 et que le domaine a subi la [migration sysvol](https://blogs.technet.com/filecab/archive/2008/02/08/sysvol-migration-series-part-1-introduction-to-the-sysvol-migration-process.aspx), [DFSR](/windows-server/storage/dfs-replication/migrate-sysvol-to-dfsr) sera utilisé pour répliquer le dossier sysvol. si le premier contrôleur de domaine dans le domaine a été promu directement au [niveau fonctionnel](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc754918(v=ws.10))du serveur Windows 2008, DFSR est automatiquement utilisé pour la réplication SYSVOL. Dans ce cas, il n’est pas nécessaire de migrer la réplication SYSVOL de FRS vers DFSR. si le domaine a été mis à niveau vers Windows [niveau fonctionnel](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc754918(v=ws.10))du serveur 2008, le service frs est utilisé pour la réplication SYSVOL jusqu’à ce que le processus de [migration](https://blogs.technet.com/filecab/archive/2008/02/08/sysvol-migration-series-part-1-introduction-to-the-sysvol-migration-process.aspx) de frs vers DFSR soit terminé.

pour déterminer si DFSR ou FRS est utilisé sur un contrôleur de domaine qui exécute Windows Server 2008, vérifiez la valeur de la sous-clé de registre **HKEY \_ LOCAL \_ MACHINE** \\ **System** \\ **CurrentControlSet** \\ **Services** \\ **DFSR** \\ **parameters** \\ **sysvol frs** \\ **Migrating sysvol frs** \\ **LocalState** . Si cette sous-clé de Registre existe et que sa valeur est définie sur 3 (éliminé), [DFSR](/windows-server/storage/dfs-replication/migrate-sysvol-to-dfsr) est utilisé. Si la sous-clé n’existe pas, ou si elle a une valeur différente, le service FRS est utilisé.

## <a name="backing-up-a-dfsr-replicated-sysvol-folder"></a>Sauvegarde d’un dossier SYSVOL DFSR-Replicated

Si le dossier SYSVOL est répliqué par [DFSR](/windows-server/storage/dfs-replication/migrate-sysvol-to-dfsr), l’enregistreur VSS DFSR peut être utilisé pour le sauvegarder. Pour plus d’informations sur l’enregistreur VSS DFSR, consultez [dossiers répliqués DFSR](/previous-versions/windows/desktop/dfsr/dfsr-replicated-folders).

## <a name="backing-up-an-frs-replicated-sysvol-folder-on-a-windows-server-2008-or-windows-server-2003-domain"></a>sauvegarde d’un dossier SYSVOL FRS-Replicated sur un domaine Windows server 2008 ou Windows server 2003

sur un contrôleur de domaine qui exécute Windows server 2008 ou Windows server 2003, l’infrastructure vss est présente. par conséquent, l’enregistreur vss FRS peut être utilisé pour sauvegarder le dossier SYSVOL et les composants FRS.

Le document des métadonnées de l’enregistreur de l’enregistreur VSS de FRS fournit des informations sur l’emplacement du dossier SYSVOL et les listes d’exclusion pour le writer. Sur la base de ces informations, une application de sauvegarde VSS (demandeur) peut sauvegarder le dossier SYSVOL à l’aide des techniques de sauvegarde VSS standard.

Le document de métadonnées de l’enregistreur contient des informations sur le writer, les données que le writer possède et la façon de restaurer ces données. Il s’agit d’un document en lecture seule qui peut être récupéré par l’application de sauvegarde avant d’effectuer une sauvegarde. L’outil [DiskShadow](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/cc772172(v=ws.11)) peut être utilisé pour afficher le document de métadonnées de l’enregistreur VSS Writer. La commande des [enregistreurs de liste DiskShadow](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/cc772172(v=ws.11)) fournit des informations sur les enregistreurs présents sur le système. Cette liste contient des informations sur l’enregistreur FRS sur les contrôleurs de domaine qui utilisent FRS pour la réplication SYSVOL ou sur des serveurs de fichiers qui utilisent le service FRS pour la réplication des [cibles de lien DFS](/previous-versions/windows/it-pro/windows-server-2003/cc782417(v=ws.10)).

l’exemple de document de métadonnées de l’enregistreur frs suivant montre un exemple de document de métadonnées de l’enregistreur frs pour un contrôleur de domaine qui contient le dossier sysvol sur D : \\ Windows \\ SYSVOL. Le chemin d’accès indiqué dans la section « fichiers exclus » est le même que celui obtenu lors de l’interrogation de la clé de Registre **SYSVOL** du service Netlogon :

**HKEY \_ LOCAL \_ machine** \\ **System système** \\ **CurrentControlSet** \\ **services** \\ **Netlogon** \\ **paramètres** \\ **SYSVOL**

La seule exception à cette règle se produit lorsque le contrôleur de domaine se trouve dans l’État Redirigé de la [migration SYSVOL](https://blogs.technet.com/filecab/archive/2008/02/08/sysvol-migration-series-part-1-introduction-to-the-sysvol-migration-process.aspx). Dans cet État, les enregistreurs correspondant à FRS et au service [DFSR](/windows-server/storage/dfs-replication/migrate-sysvol-to-dfsr) signalent leurs copies respectives du dossier Sysvol. Toutefois, la copie du dossier SYSVOL du service [DFSR](/windows-server/storage/dfs-replication/migrate-sysvol-to-dfsr) (généralement un dossier appelé SYSVOL \_ DFSR) est celle qui est partagée par le contrôleur de domaine. ce chemin d’accès est celui référencé par la clé de Registre **SYSVOL** .

L’enregistreur VSS FRS requiert une méthode de restauration personnalisée. Cela signifie que certaines étapes personnalisées doivent être effectuées lors de la restauration de fichiers en cours de réplication par FRS. Pour plus d’informations, consultez exécution d’une restauration ne faisant pas autorité d’un dossier SYSVOL FRS-Replicated.

> [!Note]  
> les sauvegardes de l’état du système pour les contrôleurs de domaine Windows n’incluent pas la base de données frs qui gère les informations d’état du service frs concernant les fichiers dans le dossier SYSVOL et d’autres jeux de contenu. La base de données FRS, les journaux de débogage, les fichiers de zone de transit et les fichiers du [dossier de données préexistant](/previous-versions/windows/it-pro/windows-server-2003/cc758169(v=ws.10)) sont exclus d’une sauvegarde de l’état du système. L’exemple de spécification d’enregistreur FRS suivant contient la liste d’exclusions dans la section « fichiers exclus ».

 

## <a name="sample-frs-writer-metadata-document"></a>Exemple de document de métadonnées de l’enregistreur FRS

voici un exemple de Document de métadonnées d’enregistreur FRS pour un contrôleur de domaine dont le chemin d’accès au dossier sysvol est D : \\ Windows \\ SYSVOL.

``` syntax
* WRITER "FRS Writer"
    - Writer ID   = {d76f5a28-3092-4589-ba48-2958fb88ce29}
    - Writer Instance ID = {07ae58e5-6977-4e34-9dfe-399bbd2cbe40}
    - Supports restore events = FALSE
    - Writer restore conditions = VSS_WRE_NEVER
    - Restore method = VSS_RME_CUSTOM
    - Requires reboot after restore = FALSE

    - Excluded files:
       - Exclude: Path = d:\windows\ntfrs\jet, Filespec = *
       - Exclude: Path = d:\Windows\debug\NtFrs, Filespec = NtFrs*
       - Exclude: Path = d:\windows\sysvol\domain\DO_NOT_REMOVE_NtFrs_PreInstall_Directory, Filespec = *
       - Exclude: Path = d:\windows\sysvol\domain\NtFrs_PreExisting___See_EventLog, Filespec = *
       - Exclude: Path = d:\windows\sysvol\staging\domain, Filespec = NTFRS_*

    - Component "FRS Writer:\SYSVOL\da45368c-b2d3-4cf0-bdc338a2cde15a7b"
       - Name: 'da45368c-b2d3-4cf0-bdc338a2cde15a7b'
       - Logical Path: 'SYSVOL'
       - Full Path: '\SYSVOL\da45368c-b2d3-4cf0-bdc338a2cde15a7b'
       - Caption: ''
       - Type: VSS_CT_FILEGROUP [2]
       - Is Selectable: 'TRUE'
       - Is top level: 'TRUE'
       - Notify on backup complete: 'TRUE'
       - Components:
       - File List: Path = d:\windows\sysvol, Filespec = *
       - Affected paths by this component:
         - d:\windows\sysvol
       - Affected volumes by this component:
         - \\?\Volume{da897ba5-5840-11db-93c1-806e6f6e6963}\ [D:\]
       - Component Dependencies:
```

## <a name="setting-registry-keys-for-a-restore-of-an-frs-replicated-sysvol-folder"></a>Définition des clés de Registre pour la restauration d’un dossier SYSVOL FRS-Replicated

La clé de Registre **BurFlags** est utilisée pour effectuer des restaurations faisant autorité ou non faisant autorité sur les membres FRS des jeux de réplicas DFS ou SYSVOL. La clé de Registre **BurFlags** globale (à l’échelle de l’ordinateur) contient des \_ valeurs REG DWORD et se trouve à l’emplacement suivant dans le registre :

**HKEY \_ \_** \\  \\  \\ Paramètres de CurrentControlSet **services** \\ **NTFRS** des paramètres NTFRS des \\ **paramètres** de système \\  \\  d’ordinateur local au démarrage

Les valeurs les plus courantes pour la clé de Registre **BurFlags** sont les suivantes :

-   D2, également appelée restauration en mode ne faisant pas autorité.
-   D4, également appelée restauration en mode faisant autorité.

Il existe des clés de Registre **BurFlags** globales et spécifiques au jeu de réplicas. La définition de la clé de Registre **BurFlags** globale réinitialise tous les jeux de réplicas que le membre contient. Cette clé globale doit être définie lorsque le serveur ne contient qu’un seul jeu de réplicas, ou lorsque les jeux de réplicas qu’il contient sont relativement peu nombreux et de petite taille. Par exemple, si le serveur est un contrôleur de domaine qui n’héberge aucun jeu de contenu qui est répliqué à l’aide de FRS autre que le dossier SYSVOL, la clé de Registre **BurFlags** globale peut être définie.

La clé de Registre **BurFlags** globale se trouve à l’emplacement suivant dans le registre :

**HKEY \_ \_** \\  \\  \\ Paramètres de CurrentControlSet **services** \\ **NTFRS** des paramètres NTFRS des \\ **paramètres** de système \\  \\  d’ordinateur local au démarrage

Contrairement à la clé **BurFlags** globale, la clé **BurFlags** spécifique au jeu de réplicas permet la réinitialisation de jeux de réplicas individuels discrets, ce qui permet de laisser les jeux de réplication sains intacts.

Les clés de Registre **BurFlags** spécifiques au jeu de réplicas peuvent être localisées en déterminant le GUID de ce jeu de réplicas particulier.

La procédure suivante décrit comment déterminer quel GUID correspond à un jeu de réplicas particulier et décrit comment configurer une restauration.

**Pour déterminer quel GUID correspond à un jeu de réplicas particulier et configurer une restauration**

1.  Arrêtez le service FRS.
2.  Pour déterminer le GUID qui représente un jeu de réplicas particulier :
    1.  Recherchez la clé suivante dans le registre.

        **HKEY \_ \_** \\  \\  \\  \\ Paramètres NTFRS des paramètres NTFRS des paramètres **NTFRS** des paramètres système d’ordinateur local \\  \\ **jeux de réplicas**

    2.  Sous la sous-clé **jeux de réplicas** , il existe une ou plusieurs sous-clés identifiées par un GUID.
    3.  La valeur **racine du jeu de réplicas** pour chaque GUID est un chemin de système de fichiers qui indique le jeu de réplicas représenté par ce GUID.
    4.  Itérez sur cette liste de GUID jusqu’à ce que le jeu de réplicas souhaité soit localisé. Notez le GUID correspondant.

3.  Recherchez la sous-clé suivante dans le registre :

    **HKEY \_ \_** \\  \\  \\ Paramètres NTFRS **services** NTFRS des paramètres NTFRS des paramètres de l’ordinateur local \\  \\  \\ **jeux de réplicas cumulatifs**

4.  Sous cette sous-clé, localisez le GUID qui a été noté à l’étape 2. Sous la sous-clé GUID, créez une entrée pour la clé **BurFlags** .
5.  Redémarrez le service FRS.

## <a name="performing-a-nonauthoritative-restore-of-an-frs-replicated-sysvol-folder"></a>Exécution d’une restauration ne faisant pas autorité d’un dossier SYSVOL FRS-Replicated

La restauration ne faisant pas autorité est la méthode la plus courante pour réinitialiser la réplication SYSVOL sur des contrôleurs de domaine individuels. Les contrôleurs de domaine dont la restauration ne fait pas autorité doivent avoir des connexions entrantes à partir d’autres contrôleurs de domaine opérationnels, qui participent à Active Directory et à la réplication FRS. Dans un environnement de déploiement à grande échelle composé de nombreux contrôleurs de domaine, les contrôleurs de domaine restants peuvent être récupérés à l’aide d’une restauration en mode ne faisant pas autorité dans les conditions suivantes :

-   Il doit y avoir au moins un membre de réplica correct connu (un contrôleur de domaine avec un dossier SYSVOL sain).
-   Les autres contrôleurs de domaine doivent être réinitialisés dans l’ordre des partenaires de réplication directe.

La procédure suivante décrit comment effectuer une restauration ne faisant pas autorité.

**Pour effectuer une restauration ne faisant pas autorité**

1.  Arrêtez le service FRS.
2.  Restaurez les données sauvegardées dans le dossier SYSVOL.
3.  Configurez la clé de Registre **BurFlags** en affectant à la valeur de la clé de Registre suivante la valeur DWORD D2.

    **HKEY \_ LOCAL \_ machine** \\ **System système** \\ **CurrentControlSet** \\ **services** \\ **NTFRS** \\ **Parameters** \\ processus de **sauvegarde/restauration** \\ **au démarrage** \\ **BurFlags**

4.  Redémarrez le service FRS.

Lors du redémarrage du service FRS, les actions suivantes se produisent :

-   La valeur de la clé de Registre **BurFlags** est réinitialisée à zéro.
-   Les fichiers figurant dans les dossiers FRS réinitialisés sont déplacés vers un dossier existant.
-   L’événement 13565 est consigné dans le journal des événements FRS pour signaler qu’une restauration ne faisant pas autorité a démarré.
    > [!Note]  
    > Les codes d’événement FRS sont documentés dans « codes d’erreur du journal des événements FRS » de la base de connaissances de l’aide et du support à l’adresse <https://go.microsoft.com/fwlink/p/?linkid=117779>

     

-   La base de données FRS est reconstruite.
-   Le membre effectue une jointure initiale du jeu de réplicas à partir d’un partenaire en amont ou de l’ordinateur spécifié dans la clé de Registre **parent du jeu de réplicas** si un parent a été spécifié pour les jeux de réplicas Sysvol.
-   L’ordinateur réinitialisé exécute une réplication complète des jeux de réplicas affectés au début de la planification de réplication appropriée.
-   Une fois le processus terminé, un événement 13516 est enregistré pour signaler que le service FRS est opérationnel. Si l’événement n’est pas consigné, il y a un problème avec la configuration de FRS.

> [!Note]  
> Le placement des fichiers dans le dossier [préexistant](/previous-versions/windows/it-pro/windows-server-2003/cc758169(v=ws.10)) sur les membres réinitialisés est un dispositif de protection de FRS conçu pour empêcher la perte accidentelle de données. Tous les fichiers destinés au réplica qui existent uniquement dans le dossier préexistant local et qui ont été répliqués après la réplication initiale peuvent ensuite être copiés dans le dossier approprié. Une fois la réplication sortante effectuée, les fichiers figurant dans le dossier préexistant peuvent être supprimés pour libérer de l’espace disque supplémentaire.

 

## <a name="performing-an-authoritative-restore-of-an-frs-replicated-sysvol-folder"></a>Exécution d’une restauration faisant autorité d’un dossier FRS-Replicated SYSVOL

Les restaurations faisant autorité sont utilisées en dernier recours dans le cas de situations critiques, telles que la divergence de données sur le jeu de contenu provoqué par des collisions de répertoire. Par exemple, une restauration faisant autorité peut être nécessaire pour restaurer un jeu de réplicas FRS où la réplication a été complètement arrêtée et une reconstruction à partir de zéro est nécessaire.

Si vous devez effectuer une restauration faisant autorité du dossier SYSVOL, sachez qu’il s’agit d’un processus très complexe. Des instructions complètes détaillant les opérations qui doivent être effectuées pour une restauration faisant autorité du contenu du dossier SYSVOL sont documentées dans la base de connaissances de l’aide et du support à l’adresse « régénération de l’arborescence SYSVOL et de son contenu dans un domaine » <https://go.microsoft.com/fwlink/p/?linkid=117780> .

Les conditions suivantes doivent être remplies pour qu’une restauration FRS faisant autorité soit effectuée :

1.  Le service FRS doit être désactivé sur tous les partenaires de réplication en aval (direct et transitif) pour le dossier SYSVOL réinitialisé avant que la restauration faisant autorité ait été configurée.
2.  Les événements 13553 et 13516 ont été enregistrés dans le journal des événements FRS. Ces événements indiquent que l’appartenance du jeu de réplicas SYSVOL a été établie sur le contrôleur de domaine configuré pour la restauration faisant autorité.
    > [!Note]  
    > Les codes d’événement FRS sont documentés dans « codes d’erreur du journal des événements FRS » de la base de connaissances de l’aide et du support à l’adresse <https://go.microsoft.com/fwlink/p/?linkid=117779>

     

3.  Le contrôleur de domaine configuré pour la restauration faisant autorité est configuré pour faire autorité pour toutes les données SYSVOL qui doivent être répliquées sur les contrôleurs de domaine restants.
4.  Tous les autres partenaires du jeu de réplicas doivent être réinitialisés avec une restauration ne faisant pas autorité.

 

 
