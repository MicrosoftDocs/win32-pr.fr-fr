---
description: Le service de Registre Windows prend en charge un enregistreur VSS, appelé Registry Writer, qui permet aux demandeurs de sauvegarder un registre système à l’aide des données stockées sur un volume de clichés instantanés.
ms.assetid: 94a45b04-0bdc-4211-bed0-caeabba774af
title: Opérations de sauvegarde et de restauration du Registre sous VSS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db1a3022ec2fb08b07bcff8b28455ae7154e4c40
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106543109"
---
# <a name="registry-backup-and-restore-operations-under-vss"></a>Opérations de sauvegarde et de restauration du Registre sous VSS

Le service de Registre Windows prend en charge un enregistreur VSS, appelé Registry Writer, qui permet aux demandeurs de sauvegarder un registre système à l’aide des données stockées sur un volume de clichés instantanés. Pour plus d’informations sur l’enregistreur du Registre, consultez la page [enregistreurs VSS](in-box-vss-writers.md).

L’enregistreur du registre effectue des sauvegardes et des restaurations sur place du Registre. En outre, l’enregistreur du Registre signale uniquement les ruches système. il ne signale pas les ruches utilisateur.

**Windows Server 2003 :** Le rédacteur du Registre utilise un fichier de référentiel intermédiaire (également appelé fichier de fractionnement) pour stocker les données de registre. En outre, l’enregistreur du Registre signale les ruches système et les ruches utilisateur.

L’ID du writer du Registre est AFBAB4A2-367D-4D15-A586-71DBB18F8485.

**Windows XP :** Il n’y a pas d’enregistreur de registre. Les données du Registre sont signalées par l’enregistreur d’état de démarrage, dont l’ID d’enregistreur est F2436E37-09F5-41AF-9B2A-4CA2435DBFD5.

> [!Note]  
> Microsoft ne fournit pas de support technique pour les développeurs ou les professionnels de l’informatique pour l’implémentation de restaurations en ligne sur l’état du système sur Windows (toutes les versions). Pour plus d’informations sur l’utilisation des API et des procédures fournies par Microsoft pour implémenter des restaurations en ligne de l’état du système, consultez les ressources de la communauté disponibles dans le [Centre de communauté MSDN](https://msdn.microsoft.com/community/default.aspx).

 

> [!Note]  
> Les informations suivantes s’appliquent uniquement à Windows Server 2003 et Windows XP.

 

## <a name="registry-backup-using-vss"></a>Sauvegarde du Registre à l’aide de VSS

Le rédacteur du Registre exporte et enregistre les fichiers de Registre actifs dans les emplacements définis par la clé **HKEY \_ local \_ machine** \\ **System** \\ **CurrentControlSet** \\ **Control** \\ **hivelist**.

Les noms des valeurs sous cette entrée de Registre identifient la ruche de Registre à enregistrer, et les données de la valeur fournissent le fichier contenant le fichier (le fichier Hive). Les fichiers Hive sont spécifiés au format suivant : \\ Device \\ *HarddiskVolumeX* \\ *path* \\ *filename*.

Par exemple, sous **HKEY \_ local \_ machine** \\ **System** \\ **CurrentControlSet** \\ **Control** \\ **hivelist**, vous pouvez voir le logiciel **\\ Registry \\ machine \\ Software**  =  \\ Device \\ HarddiskVolume1 \\ Windows \\ system32 \\ config \\ Software.

L’enregistreur du registre s’assure que les fichiers Hive sont enregistrés sur le disque avant le cliché instantané.

Lors de la sauvegarde des ruches du Registre, un demandeur remplace le \\ \\ *HarddiskVolumeX* d’appareil par la chaîne de l' [*objet périphérique*](vssgloss-d.md) du cliché instantané du volume.

> [!Note]  
> Vous pouvez convertir le \\ chemin d’accès du \\ *HarddiskVolumeX* d’appareil en un chemin Win32 équivalent à l’aide de la fonction [**QueryDosDevice**](/windows/win32/api/fileapi/nf-fileapi-querydosdevicew) . Pour plus d’informations, consultez [obtention d’un nom de fichier à partir d’un handle de fichier](../memory/obtaining-a-file-name-from-a-file-handle.md) ou [affichage de noms de chemin d’accès de volume](../fileio/displaying-volume-paths.md).

 

## <a name="registry-restore-using-non-vss-win32-apis"></a>Restauration du Registre à l’aide des API Win32 non-VSS

Pour une restauration en ligne (mode sans échec ou système d’exploitation complet), les sous-clés de la clé de Registre au sein de la clé de registre de la commande de système d’exploitation de l' **\_ \_ ordinateur local HKEY** du \\  \\  \\  \\ **Gestionnaire de sessions** \\  .

Les fonctions [**MoveFileEx**](/windows/win32/api/winbase/nf-winbase-movefileexa) et [**MoveFileTransacted**](/windows/win32/api/winbase/nf-winbase-movefiletransacteda) utilisent cette clé de Registre pour stocker des informations sur les fichiers qui ont été renommés à l’aide du \_ délai MOVEFILE \_ jusqu’à la \_ valeur de redémarrage dans le paramètre *dwFlags* .

Pour conserver le contenu de la clé de Registre **PendingFileRenameOperations** , votre application de sauvegarde doit appeler la fonction [**RegLoadKey**](/windows/win32/api/winreg/nf-winreg-regloadkeya) pour connecter le fichier de Registre à restaurer dans le Registre actif. Votre application de sauvegarde peut ensuite utiliser les différentes fonctions de Registre pour copier les clés et valeurs souhaitées dans la ruche chargée. Une fois la copie terminée, les fonctions [**regflushkey a**](/windows/win32/api/winreg/nf-winreg-regflushkey) et [**RegUnloadKey**](/windows/win32/api/winreg/nf-winreg-regunloadkeya) doivent être appelées.

Pour une restauration hors connexion (environnement de récupération Windows ou Windows PE), il n’est pas nécessaire d’honorer la clé de Registre **PendingFileRenameOperations** .

## <a name="registry-restore-using-non-vss-win32-apis-in-windows-server-2003"></a>Restauration du Registre à l’aide des API Win32 non-VSS dans Windows Server 2003

> [!Note]  
> Les informations suivantes s’appliquent uniquement aux opérations de restauration liées à la récupération d’urgence (également appelée récupération complète) effectuées dans Windows Server 2003.

 

Lors de la restauration du Registre, une application de sauvegarde doit déplacer certaines des sous-clés du registre actuel vers le registre à restaurer.

Pour ce faire, une application de sauvegarde peut appeler **RegLoadKey** pour connecter le fichier de Registre à restaurer dans le registre actuellement actif. Il peut ensuite utiliser les différentes fonctions de Registre pour copier les clés et les valeurs souhaitées dans la ruche chargée. Une fois la copie terminée, **regflushkey a** et **RegUnloadKey** sont appelés.

Une clé de registre indique à une application de restauration (demandeur) les clés de Registre sous **HKEY \_ local \_ machine \\ System** qui ne doivent pas être remplacées au moment de la restauration :

**HKEY \_ local \_ machine \\ System \\ CurrentControlSet \\ Control \\ backuprestore \\ KeysNotToRestore**

Une partie du processus de restauration de l’état du système implique la restauration d’un registre sauvegardé précédemment.

Les applications de sauvegarde doivent faire particulièrement attention lors de la restauration de la ruche du **\_ \_ \\ système HKEY local machine** , car le processus d’installation d’une version temporaire du système d’exploitation Windows aura des clés établies dans la ruche système nouvellement installée dont les valeurs doivent survivre à l’opération de restauration.

Par exemple, lorsque le système de remplacement a une carte d’interface réseau différente du système d’origine, la restauration des clés d’origine pour la carte précédente entraîne des résultats imprévisibles. Cela est dû au fait que le service de Plug-and-Play a détecté et placé les entrées de Registre appropriées du service et du pilote dans le registre. Ces valeurs doivent être conservées pour démarrer correctement après la restauration du système.

Cette section décrit comment les applications de sauvegarde peuvent découvrir les clés et les fichiers qui doivent être conservés lors de l’exécution d’une restauration de la ruche **\_ \_ \\ système HKEY local machine** . Dans certains cas, cela implique la copie par programmation des clés de la ruche d’installation récemment installée dans la ruche à restaurer. Dans d’autres cas, le fait de s’assurer que les clés de registre d’un produit ne sont pas remplacées est aussi simple que de spécifier de telles clés dans le fichier de configuration INF du produit.

Les clés (et les données de clé) qui doivent être préservées sont énumérées dans la ruche du **\_ \_ \\ système HKEY local machine** sous le

**HKEY \_ local \_ machine \\ System \\ CurrentControlSet \\ Control \\ backuprestore \\ KeysNotToRestore**

clé sous forme d’ensembles \_ de \_ chaînes reg multisz (appelées *chaînes de clé* dans ce document).

Une application de sauvegarde (demandeur) doit examiner les valeurs de ces clés dans le Registre actif et le Registre qui vient d’être restauré, car une application ou un service peut ajouter des valeurs à tout moment.

La manière dont les chaînes de clé doivent être interprétées par les applications de sauvegarde est déterminée par leur caractère terminal :

1.  Les chaînes de clé se terminant par une barre oblique inverse (« \\ ») sont interprétées comme des sous-clés. Lorsqu’une telle sous-chaîne est rencontrée, l’application de sauvegarde doit conserver toutes les données et toutes les clés subordonnées.

    Par exemple, le code suivant spécifie que toutes les clés et données subordonnées doivent être conservées dans une opération de restauration :

    **HKEY \_ local \_ machine \\ System \\ CurrentControlSet \\ services \\ dmio \\ informations de démarrage\\**

    À cette fin, cette clé et toutes les clés et données subordonnées doivent être copiées à partir du Registre existant (c’est-à-dire celui créé par l’installation de Windows) dans le Registre qui vient d’être restauré. C’est ce que l’on appelle une opération de *remplacement de clé* . Cette opération remplace la clé correspondante dans le registre restauré.

2.  Les chaînes de clé dont le caractère de fin est un astérisque (« \* ») spécifient que toutes les sous-clés doivent être fusionnées. Par exemple, la chaîne de clé :

    **HKEY \_ Services de CurrentControlSet de système d’ordinateur LOCAL _ \_ \\ \\ \\ \\ \**

    Spécifie que la clé services dans le Registre existant (par exemple, celles créées par l’installation de Windows) doit être fusionnée dans le registre restauré. C’est ce que l’on appelle une opération _key Merge * et si une sous-clé existe à la fois dans la ruche existante et dans la ruche restaurée, la clé du répertoire restauré est conservée avec les exceptions suivantes :

    -   Si la sous-clé de la ruche existante contient une valeur nommée « Start », et que la sous-clé dans la restaurée ne le fait pas.
    -   Si la sous-clé de la ruche existante et restaurée contient une valeur nommée « Start » et que sa valeur numérique dans la ruche existante est inférieure.

    La valeur « START » dans le registre spécifie quand un service ou un pilote démarre et peut avoir une valeur numérique comprise entre 0-4. Plus la valeur est faible, plus tôt dans le processus de démarrage, le service démarre.

    Si cette clé existe dans le répertoire existant et dans le répertoire restauré, vous devez examiner la valeur de la clé de démarrage dans chaque Hive. Si la valeur de la ruche existante est inférieure à la valeur du répertoire restauré, la valeur inférieure doit être conservée.

    Une fois encore, cette clé est utilisée pour déterminer si un service ou un pilote doit être démarré au moment du démarrage, à l’heure système, manuellement, automatiquement ou désactivée. La valeur inférieure représente une heure de début antérieure. L’heure de début précédente doit être appliquée au nouveau registre pour s’assurer que le service ou les pilotes sont démarrés correctement au démarrage suivant.

3.  Les chaînes de clé dont le caractère de fin n’est ni une barre oblique inverse, ni un astérisque sont interprétées comme des valeurs de Registre à conserver.

    Par exemple, la chaîne de clé :

    **HKEY \_ local \_ machine \\ System \\ CurrentControlSet \\ contrôler le \\ Gestionnaire de sessions \\ PendingFileRenameOperations**

    Le mécanisme par lequel les clés peuvent être conservées par programme implique l’API du Registre Win32. Par exemple, un algorithme est énuméré ci-dessous :

    1.  Restaurez le fichier ruche du système sauvegardé dans un fichier. Pour cet exemple, laissez le nom System. reg.
    2.  Utilisez **RegLoadKey** pour charger System. reg dans **HKEY \_ local \_ machine** sous un nom temporaire. Par exemple, un tel nom peut être

        **HKEY \_ local \_ machine \\ tmp \_ système**

    3.  Énumérez les valeurs dans la sous-clé **KeysNotToRestore** à partir des deux copies du Registre et créez un sur-ensemble des listes. Copier chaque clé de ce type à partir du

        **HKEY \_ local \_ machine \\ System**

        clé dans

        **HKEY \_ local \_ machine \\ tmp \_ système**

        clé selon la sémantique décrite ci-dessus.

    4.  Lorsque vous avez terminé , utilisez les  &  points d’entrée regflushkey a **RegUnloadKey** pour enregistrer le

        **HKEY \_ local \_ machine \\ tmp \_ système**

        clé dans System. reg.

    5.  Enfin, utilisez **RegReplaceKey** pour spécifier que System. reg doit remplacer

        **HKEY \_ local \_ machine \\ System**

        fichier Hive, système.

 

 
