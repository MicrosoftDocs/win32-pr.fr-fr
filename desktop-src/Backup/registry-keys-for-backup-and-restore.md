---
title: Clés et valeurs de Registre pour la sauvegarde et la restauration
ms.assetid: 83449f78-cca1-449b-8c5f-3c8a91c8b3e7
description: 'En savoir plus sur : clés et valeurs de Registre pour la sauvegarde et la restauration'
keywords:
- sauvegarde de sauvegarde, clés de Registre
- Sauvegarde des clés de Registre
- Sauvegarde CustomPerformanceSettings
- Sauvegarde DisableMonitoring
- Sauvegarde FilesNotToBackup
- Sauvegarde FilesNotToSnapshot
- Sauvegarde KeysNotToRestore
- Sauvegarde LastInstance
- Sauvegarde LastRestoreId
- Sauvegarde MaxShadowCopies
- Sauvegarde MinDiffAreaFileSize
- Sauvegarde OverallPerformanceSetting
- Sauvegarde SYSVOL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ef9796ff96efbc20ac90de6d26a0c1bac7b17633
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104111543"
---
# <a name="registry-keys-and-values-for-backup-and-restore"></a>Clés et valeurs de Registre pour la sauvegarde et la restauration

Les applications qui demandent ou effectuent des opérations de sauvegarde et de restauration doivent utiliser les clés et valeurs de Registre suivantes pour communiquer entre elles ou avec des fonctionnalités telles que le [service VSS (VSS)](/windows/desktop/VSS/volume-shadow-copy-service-portal) et la sauvegarde Windows :

-   [CustomPerformanceSettings](#customperformancesettings)
-   [DisableMonitoring](#disablemonitoring)
-   [FilesNotToBackup](#filesnottobackup)
-   [FilesNotToSnapshot](#filesnottosnapshot)
-   [IdleTimeout](#idletimeout)
-   [KeysNotToRestore](#keysnottorestore)
-   [LastInstance](#lastinstance)
-   [LastRestoreId](#lastrestoreid)
-   [MaxShadowCopies](#maxshadowcopies)
-   [MinDiffAreaFileSize](#mindiffareafilesize)
-   [OverallPerformanceSetting et CustomPerformanceSettings](#overallperformancesetting-and-customperformancesettings)
-   [SYSVOL](#sysvol)

## <a name="customperformancesettings"></a>CustomPerformanceSettings

Consultez [OverallPerformanceSetting et CustomPerformanceSettings](#overallperformancesetting-and-customperformancesettings).

## <a name="disablemonitoring"></a>DisableMonitoring

Sur les plateformes clientes Windows à compter de Windows 7, les utilisateurs sont automatiquement invités à configurer la fonctionnalité sauvegarde Windows, si ce n’est déjà fait. Ces notifications s’affichent au démarrage de l’ordinateur, à partir de sept jours après l’installation du système d’exploitation. Elles s’affichent également lorsque l’utilisateur se connecte à un disque dur ; dans ce cas, les notifications s’affichent immédiatement.

Les OEM et les développeurs d’applications de sauvegarde tierces peuvent utiliser la valeur de Registre **DisableMonitoring** pour désactiver ces notifications automatiques.

Cette valeur n’existe pas par défaut. elle doit donc être créée sous la clé de Registre suivante :

**HKEY \_ Logiciel de l' \_ ordinateur local** \\  \\ **Microsoft** \\ **Windows** \\ **CurrentVersion** \\ **WindowsBackup**

La valeur de Registre **DisableMonitoring** a le type de données reg \_ DWORD et est interprétée comme suit :

-   Si les données de la valeur sont définies sur 1 et que les utilisateurs n’ont pas déjà configuré la fonctionnalité sauvegarde Windows, les notifications automatiques sont désactivées. Si une notification automatique est déjà présente dans le centre de maintenance, la définition de cette valeur de Registre entraîne la suppression de la notification à 10:00 le matin suivant.
-   Si la valeur n’existe pas, si ses données ne sont pas définies, ou si ses données sont définies à zéro, les notifications automatiques ne sont pas désactivées.

**Windows Vista et Windows XP :** Cette valeur de Registre n’est pas prise en charge.

## <a name="filesnottobackup"></a>FilesNotToBackup

La clé de Registre **FilesNotToBackup** spécifie les noms des fichiers et répertoires que les applications de sauvegarde ne doivent pas sauvegarder ou restaurer. Chacune des entrées de cette clé est une chaîne REG \_ \_ multisz au format suivant :

\[ \] Lecteur \[ *Chemin d’accès* \] \\ *Nom du fichier* \[ commutateur\]

-   Le *lecteur* spécifie le lecteur et est facultatif. Par exemple, c :. Pour spécifier tous les lecteurs, utilisez une barre oblique inverse ( \) ; aucune lettre de lecteur n’est nécessaire.
-   *Path* spécifie le chemin d’accès et est facultatif. Il ne peut pas contenir de caractères génériques.
-   *Filename* spécifie le fichier ou le répertoire et est obligatoire. Il peut contenir des caractères génériques.
-   /s spécifie que tous les sous-répertoires du chemin d’accès spécifié doivent être inclus.
-   Les variables d’environnement telles que% SystemRoot% peuvent être substituées à la totalité ou à une partie de la chaîne entière.

Le tableau suivant présente quelques entrées typiques.

| Nom de l’entrée                             | Valeur par défaut                                                                             |
|----------------------------------------|-------------------------------------------------------------------------------------------|
| Internet Explorer                      | Fichiers temporaires                                                                           |
| Fichier d’échange de mémoire                       | \\Pagefile.sys                                                                            |
| MS Distributed Transaction Coordinator | C : \\ Windows \\ system32 \\ MSDTC MSDTC \\ . LOG C : \\ \\ \\ suivi MSDtc Windows \\ system32 \\ dtctrace. log |
| Cache Fichiers hors connexion                    | % Systemroot% \\ CSC \\ \* /s                                                                  |
| Gestion de l'alimentation                       | \\hiberfil.sys                                                                            |
| Stockage d’instance simple                | \\SIS Common Store \\ \* . \* /s                                                              |
| Fichiers temporaires                        | % TEMP% \\ \* /s                                                                             |



 

> [!Note]  
> En règle générale, les applications qui effectuent des sauvegardes au niveau du volume en copiant l’ensemble du volume au niveau du bloc, de sorte qu’il ne peut pas honorer la clé de Registre **FilesNotToBackup** au moment de la sauvegarde. Au lieu de cela, ils attendent jusqu’à l’heure de la restauration de supprimer les fichiers qui n’étaient pas sauvegardés. Dans la plupart des cas, il s’agit d’une stratégie raisonnable. Toutefois, dans le cas de fichiers de stockage d’instance unique, les fichiers de stockage Common SIS ne doivent pas être supprimés au moment de la restauration.

 

Pour les sauvegardes de volumes au niveau du bloc, Sauvegarde Windows Server et l’utilitaire Windows Wbadmin honorent la clé de Registre **FilesNotToBackup** en supprimant les fichiers appropriés au moment de la restauration. La restauration du système et la sauvegarde de l’état du système n’honorent pas la clé de Registre **FilesNotToBackup** .

**Windows XP :** La restauration du système honore la clé de Registre **FilesNotToBackup** .

## <a name="filesnottosnapshot"></a>FilesNotToSnapshot

VSS prend en charge la clé de Registre **FilesNotToSnapshot** . Les applications et les services peuvent utiliser cette clé pour spécifier les fichiers à supprimer des clichés instantanés nouvellement créés. Pour plus d’informations, consultez [exclusion de fichiers des clichés instantanés](/windows/desktop/VSS/excluding-files-from-shadow-copies).

**Windows Server 2003 et Windows XP :** Cette clé de Registre n’est pas prise en charge.

Pour les sauvegardes de volumes au niveau du bloc, Sauvegarde Windows Server honore la clé de Registre **FilesNotToSnapshot** en supprimant les fichiers appropriés au moment de la restauration.

## <a name="idletimeout"></a>IdleTimeout

La valeur de Registre **IdleTimeout** spécifie la durée, en secondes, pendant laquelle le service VSS attendra lorsqu’il est inactif. Si cette valeur de délai d’attente est atteinte et qu’il n’y a aucune tâche à effectuer, le service VSS s’arrête.

Cette valeur de Registre se trouve sous la clé de Registre suivante :

**HKEY \_ \_** \\  \\  \\  \\  \\ **Paramètres** VSS des services de CurrentControlSet de système d’ordinateur local

Si cette valeur de Registre n’existe pas :

-   La valeur de délai d’expiration réelle utilisée est de 180 secondes (3 minutes) par défaut.
-   Vous pouvez créer une valeur avec le nom **IdleTimeout** et le type DWORD et lui attribuer la valeur souhaitée.

Si cette valeur de Registre est définie sur 0 seconde :

-   La valeur de délai d’expiration réelle utilisée est de 180 secondes (3 minutes).

Si vous définissez cette valeur de Registre :

-   VSS utilise la valeur de délai d’attente que vous définissez.
-   Vous pouvez spécifier n’importe quelle valeur comprise entre 1 et FFFFFFFF secondes. Toutefois, il est recommandé de choisir une valeur comprise entre 1 et 180 secondes.

**Windows Server 2003 et Windows XP :** Cette clé de Registre n’est pas prise en charge.

## <a name="keysnottorestore"></a>KeysNotToRestore

La clé de Registre **KeysNotToRestore** spécifie les noms des sous-clés et des valeurs de registre que les applications de sauvegarde ne doivent pas restaurer. Pour plus d’informations, consultez [KeysNotToRestore](/previous-versions/windows/it-pro/windows-server-2003/cc737538(v=ws.10)). Il n’est pas nécessaire d’honorer la clé de Registre **KeysNotToRestore** .

**Windows Server 2003 et Windows XP :** Vous devez respecter la clé de Registre **KeysNotToRestore** .

Pour les sauvegardes de volumes au niveau du bloc, Sauvegarde Windows Server honore la clé de Registre **KeysNotToRestore** en supprimant les fichiers appropriés au moment de la restauration.

La sauvegarde de l’état du système honore la clé de Registre **KeysNotToRestore** .

## <a name="lastinstance"></a>LastInstance

La valeur de Registre **LastInstance** indique qu’une opération de restauration complète a été effectuée et que les volumes ont été remplacés mais pas mis en forme. Pour plus d’informations, consultez [utilisation de la récupération automatique du système VSS pour la récupération d’urgence](/windows/desktop/VSS/using-vss-automated-system-recovery-for-disaster-recovery).

**Windows Server 2003 et Windows XP :** Cette valeur de Registre n’est pas prise en charge.

## <a name="lastrestoreid"></a>LastRestoreId

Quand une application de sauvegarde effectue une restauration de l’état du système, elle doit indiquer qu’elle a fait cela en définissant la valeur de Registre **LastRestoreId** . Dans ce cas, « restauration de l’état du système » fait référence à toute restauration qui restaure de manière sélective les fichiers binaires et les pilotes du système d’exploitation.

Si l’ensemble du volume de démarrage et du système est restauré au niveau du volume, cette valeur ne doit pas être définie.

Si la valeur de Registre **LastRestoreId** n’existe pas, l’application de sauvegarde doit la créer sous la clé de Registre suivante :

**HKEY \_ \_** Contrôle CurrentControlSet du système de l’ordinateur local \\  \\  \\  \\ **backuprestore** \\ **SystemStateRestore**

Créez une valeur avec le nom **LastRestoreId** et tapez reg \_ sz. La valeur doit être une valeur opaque unique, telle qu’un GUID.

À chaque fois qu’une nouvelle restauration de l’état du système est effectuée, l’application de sauvegarde doit modifier les données de la valeur **LastRestoreId** .

Les autres applications qui doivent surveiller les restaurations de l’état du système doivent stocker les données de cette valeur de registre. Ces données peuvent être comparées aux données actuelles de la valeur de Registre **LastRestoreId** pour déterminer si une nouvelle restauration de l’état du système a été effectuée.

**Windows Vista, Windows Server 2003 et Windows XP :** Cette valeur de Registre n’est pas prise en charge tant que Windows Vista avec Service Pack 1 (SP1) et Windows Server 2008 ne sont pas pris en charge.

## <a name="maxshadowcopies"></a>MaxShadowCopies

La valeur de Registre **MaxShadowCopies** spécifie le nombre maximal de [*clichés instantanés accessibles*](/windows/desktop/VSS/vssgloss-c) par le client qui peuvent être stockés sur chaque volume de l’ordinateur. Un cliché instantané accessible par le client est un cliché instantané créé à l’aide de la valeur accessible par le **\_ \_ client \_ CTX VSS** de l’énumération du [**\_ \_ \_ contexte de capture instantanée VSS**](/windows/desktop/api/vss/ne-vss-vss_snapshot_context) . Les clichés instantanés accessibles par les clients sont utilisés par les clichés instantanés pour dossiers partagés. Pour plus d’informations sur les clichés instantanés, consultez la documentation [VSS](/windows/desktop/VSS/volume-shadow-copy-service-portal) .

Si la valeur de Registre **MaxShadowCopies** n’existe pas, l’application de sauvegarde peut la créer sous la clé de Registre suivante :

**HKEY \_ \_** \\  \\  \\  \\  \\ **Paramètres** VSS des services de CurrentControlSet de système d’ordinateur local

Créez une valeur avec le nom **MaxShadowCopies** et tapez DWORD. Les données par défaut de cette valeur sont 64. La valeur minimale est 1. La valeur maximale est 512.

> [!Note]  
> Pour les autres types de clichés instantanés, aucune valeur de registre ne correspond à **MaxShadowCopies**. Le nombre maximal de clichés instantanés est de 512 par volume.

 

**Remarque**  Le paramètre **MaxShadowCopies** est pris en charge sur Windows Server 2003 ou version ultérieure.

**Windows Server 2003 :** Sur les serveurs de cluster, les données de la valeur de Registre **MaxShadowCopies** devront peut-être être définies sur un nombre inférieur. Pour plus d’informations, consultez « lorsque vous utilisez la Service VSS sur des ordinateurs Windows Server 2003 qui exécutent de nombreuses opérations d’e/s, les volumes de disque sont plus longs à mettre en ligne » dans la base de connaissances de l’aide et du support à l’adresse [https://support.microsoft.com/kb/945058](https://support.microsoft.com/kb/945058) .

**Windows XP :** Cette valeur de Registre n’est pas prise en charge.

## <a name="mindiffareafilesize"></a>MinDiffAreaFileSize

[VSS](/windows/desktop/VSS/volume-shadow-copy-service-portal) alloue une zone de stockage de clichés instantanés (ou « zone diff ») pour stocker les données des clichés instantanés. La taille minimale de la zone de stockage des clichés instantanés est un paramètre par ordinateur qui peut être spécifié à l’aide de la valeur de Registre **MinDiffAreaFileSize** .

Si la valeur de Registre **MinDiffAreaFileSize** n’est pas définie, la taille minimale de la zone de stockage des clichés instantanés est de 32 Mo pour les volumes inférieurs à 500 mo et 320 Mo pour les volumes supérieurs à 500 Mo.

**Windows server 2008, Windows server 2003 avec SP1 et Windows Vista :** Si la valeur de Registre **MinDiffAreaFileSize** n’est pas définie, la zone de stockage des clichés instantanés a une taille minimale de 300 Mo. Si la valeur de Registre **MinDiffAreaFileSize** est définie, ses données doivent être comprises entre 300 mo et 3000 Mo (3 Go), et il doit s’agir d’un multiple de 300 Mo.

**Windows Server 2003 :** Si la valeur de Registre **MinDiffAreaFileSize** n’est pas définie, la taille minimale de la zone de stockage des clichés instantanés est de 100 Mo.

**Windows XP :** Cette valeur de Registre n’est pas prise en charge.

Si la valeur de Registre **MinDiffAreaFileSize** n’existe pas, l’application de sauvegarde peut la créer sous la clé de Registre suivante :

**HKEY \_ \_** Services de \\  \\ **CurrentControlSet** \\  \\  de système d’ordinateur local

Créez une valeur avec le nom **MinDiffAreaFileSize** et tapez reg \_ DWORD. Les données de cette clé sont spécifiées en mégaoctets. 320 est égal à 320 Mo et 3200 est égal à 3,2 Go. Vous devez spécifier un nombre qui est un multiple de 32. Si vous spécifiez une valeur qui n’est pas un multiple de 32, le multiple de 32 suivant sera utilisé.

Les clichés instantanés peuvent ne pas fonctionner correctement si la valeur de Registre **MinDiffAreaFileSize** spécifie une taille minimale supérieure à la taille maximale de la zone de stockage des clichés instantanés. Pour spécifier la taille maximale de la zone de stockage des clichés instantanés, utilisez la commande [vssadmin](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/cc754968(v=ws.11)) Add ShadowStorage ou la commande vssadmin Resize ShadowStorage. Pour afficher la taille maximale actuelle, utilisez la commande [vssadmin list ShadowStorage](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/cc754968(v=ws.11)) . Si vous n’avez pas défini de taille maximale, il n’y a aucune limite à la quantité d’espace qui peut être utilisée.

## <a name="overallperformancesetting-and-customperformancesettings"></a>OverallPerformanceSetting et CustomPerformanceSettings

Les valeurs de Registre **OverallPerformanceSetting** et **CustomPerformanceSettings** sont utilisées pour spécifier les paramètres de performances de sauvegarde Windows Server. Ces valeurs de Registre sont prises en charge uniquement sur les systèmes d’exploitation Windows Server.

**Windows Server 2003 :** Ces valeurs de registre ne sont pas prises en charge.

Si ces valeurs de Registre n’existent pas, l’application de sauvegarde peut les créer sous la clé de Registre suivante :

**HKEY \_ Logiciel de l' \_ ordinateur local** \\  \\ **Microsoft** \\ **Windows**- \\  \\ **sauvegarde au niveau du bloc Windows** CurrentVersion

Pour spécifier les paramètres de performances de tous les volumes, créez une valeur avec le nom **OverallPerformanceSetting** et tapez reg \_ DWORD. Les données de la valeur doivent être définies sur l’une des valeurs suivantes.

| Valeur | Signification                                                                                                                                                                                                                                   |
|-------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 1     | Performances de sauvegarde normales (à l’aide de sauvegardes complètes). Ce paramètre correspond au paramètre de performances de sauvegarde normal décrit dans [optimisation des performances de sauvegarde et de serveur](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/dd759145(v=ws.11)).            |
| 2     | Performances de sauvegarde plus rapides (à l’aide de sauvegardes incrémentielles). Ce paramètre correspond au paramètre de performances de sauvegarde plus rapide décrit dans [optimisation des performances de sauvegarde et de serveur](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/dd759145(v=ws.11)).     |
| 3     | Performances de sauvegarde personnalisées (en spécifiant un paramètre de performances pour chaque volume). Ce paramètre correspond au paramètre personnalisé décrit dans [optimisation des performances de sauvegarde et de serveur](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/dd759145(v=ws.11)). |



 

Si vous affectez à **OverallPerformanceSetting** la valeur 3, vous devez également spécifier des paramètres de performances pour chaque volume individuellement. Pour ce faire, créez une valeur avec le nom **CustomPerformanceSettings** et tapez reg \_ multi \_ sz. Les données de cette valeur doivent être définies comme suit :

-   Chaque chaîne dans la \_ \_ séquence de chaînes multiszs reg contient le paramètre pour un volume.
-   Chaque chaîne se compose d’un GUID de volume, suivi d’une virgule, puis d’une valeur DWORD.
-   Chacune des valeurs DWORD est 1 (sauvegarde complète) ou 2 (sauvegarde incrémentielle).

Supposons, par exemple, que l’ordinateur dispose de deux volumes, comme suit :

-   Les deux volumes sont C : \\ et D : \\ .
-   Le GUID pour le volume C : \\ est 07c473ca4-2df8-11de-9d80-806e6f6e6963 et le GUID pour le volume D : \\ est 0ac22ea6c-712f-11de-adb0-00215a67606e.
-   Vous souhaitez spécifier une sauvegarde normale perfornance pour le volume C : \\ et des performances de sauvegarde plus rapides pour le volume D : \\ .

Pour ce faire, vous devez définir **OverallPerformanceSetting** sur 3 et **CustomPerformanceSettings** sur « 07c473ca4-2df8-11de-9d80-806e6f6e6963, 1 \\ 00ac22ea6c-712f-11de-adb0-00215a67606e, 2 ».

Si vous affectez à **OverallPerformanceSetting** la valeur 1 ou 2, les données de la valeur **CustomPerformanceSettings** sont ignorées.

## <a name="sysvol"></a>SYSVOL

La valeur de Registre **SYSVOL** est un moyen d’informer le service de réplication système de fichiers DFS (DFSR) qu’une opération de restauration de l’état du système a été lancée. Toute application de sauvegarde qui effectue une restauration de l’état du système de SYSVOL doit utiliser cette valeur pour indiquer si l’opération de restauration fait autorité ou ne fait pas autorité. Cette valeur est lue par le service DFSR. Si cette valeur n’est pas définie, la restauration SYSVOL est effectuée de manière non forcée par défaut.

Si la valeur de Registre **SYSVOL** n’existe pas, l’application de sauvegarde doit la créer sous la clé de Registre suivante :

**HKEY \_ \_** \\  \\  \\  \\  \\ **Restauration** DFSR des services de système d’ordinateur local

Créez une valeur avec le nom **SYSVOL** et tapez reg \_ sz. Les données de la valeur doivent être définies sur « faisant autorité » ou « ne faisant pas autorité » en fonction de la demande de l’administrateur système.

**Windows Vista, Windows Server 2003 et Windows XP :** Cette valeur de Registre n’est pas prise en charge.

 

 
