---
description: remarque cette rubrique s’applique uniquement à Windows server 2003 R2 et Windows server 2003 avec Service Pack 1 (SP1).
ms.assetid: a192d9a7-1c65-4251-acb1-4df03ebfe910
title: sauvegarde et restauration de l’état du système dans Windows server 2003 R2 et Windows server 2003 SP1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c4803acc5981cc74084789064bd276baa28b35c0ffe225e49d2b65ba5485e51a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120032949"
---
# <a name="backing-up-and-restoring-system-state-in-windows-server-2003-r2-and-windows-server-2003-sp1"></a>sauvegarde et restauration de l’état du système dans Windows server 2003 R2 et Windows server 2003 SP1

> [!Note]  
> cette rubrique s’applique uniquement à Windows server 2003 R2 et Windows server 2003 avec Service Pack 1 (SP1). Pour plus d’informations sur les autres versions de système d’exploitation, consultez [sauvegarde et restauration de l’état du système](locating-additional-system-files.md).

 

> [!Note]  
> Microsoft ne fournit pas de support technique pour les développeurs ou les professionnels de l’informatique pour l’implémentation des restaurations en ligne de l’état du système sur Windows (toutes les versions). pour plus d’informations sur l’utilisation des api et des procédures fournies par Microsoft pour implémenter des restaurations en ligne de l’état du système, consultez les ressources de la communauté disponibles sur le [centre de Community MSDN](https://msdn.microsoft.com/community/default.aspx).

 

lorsque vous effectuez une sauvegarde ou une restauration VSS, l’état du système de Windows est défini comme étant une collection de plusieurs éléments clés du système d’exploitation et de leurs fichiers. Ces éléments doivent toujours être traités par les opérations de sauvegarde et de restauration en tant qu’unité.

dans Windows server 2003 R2 et Windows server 2003 avec SP1, il n’existe aucune API Windows conçue pour traiter ces objets comme un seul. il est donc recommandé que les demandeurs aient leur propre objet d’état du système afin qu’ils puissent traiter ces composants de manière cohérente.

étant donné que le service VSS s’exécute sur les versions de Windows où la protection de fichiers [*système*](vssgloss-s.md) (WFP) protège les fichiers d’état du système contre toute altération, des étapes spéciales sont nécessaires pour sauvegarder et restaurer l’état du système.

L’état du système se compose des éléments suivants :

-   Tous les fichiers protégés par WFP, fichiers de démarrage, y compris NTLDR, Ntdetect et configurations des compteurs de performances
-   Le Active Directory (ADSI) (sur les systèmes qui sont des contrôleurs de domaine)
-   Le dossier de volume système (SYSVOL) qui est répliqué par le service de réplication de fichiers (FRS) (sur les systèmes qui sont des contrôleurs de domaine)
-   Serveur de certificats (sur les systèmes qui fournissent l’autorité de certification)
-   base de données de cluster (sur les systèmes qui sont un nœud d’un cluster Windows)
-   Service de registre
-   Base de données d’inscription de classe COM+

L’état du système peut être sauvegardé dans n’importe quel ordre.

Toutefois, la restauration de l’état du système doit remplacer d’abord les fichiers de démarrage et valider la section système (Hive) du Registre comme dernière étape du processus, et peut se produire dans l’ordre suivant :

1.  Restaurez les fichiers de démarrage.
2.  Base de données d’inscription de classe COM+
3.  Restaurez les bases de données SYSVOL, du serveur de certificats et du cluster (si nécessaire).
4.  Restaurez les Active Directory (si nécessaire).
5.  Restaurez le registre.

Certains services système, tels que l’autorité de certification, comportent des enregistreurs VSS conventionnels et suivent les algorithmes de sauvegarde et de restauration VSS. D’autres, telles que le registre, nécessitent des opérations de sauvegarde ou de restauration personnalisées ; Pour plus d’informations, consultez [sauvegardes et restaurations personnalisées](custom-backups-and-restores.md).

## <a name="vss-backup-and-restores-of-boot-and-system-files"></a>Sauvegarde et restauration VSS des fichiers système et de démarrage

Les fichiers système et de démarrage doivent être sauvegardés et restaurés uniquement en tant qu’entité unique.

Un demandeur peut utiliser en toute sécurité des versions cliché instantané de ces fichiers et s’assurer que le volume système et le périphérique de démarrage sont des [*clichés instantanés*](vssgloss-s.md).

Les fichiers système et de démarrage sont les suivants :

-   Les principaux fichiers de démarrage : <dl> NtLdr.exe  
    Boot.ini  
    NtDetect.com  
    NtBootDD.sys (le cas échéant)  
    </dl>
-   The WFP service catalog file must be backed up prior to backing up the WFP files, and it is found under: <dl> % SystemRoot% \\ system32 \\ CatRoot \\ {F750E6C3-38EE-11D1-85E5-00C04FC295EE} </dl>
-   Tous les fichiers protégés par la protection des fichiers [*système*](vssgloss-s.md) et énumérés par [**SfcGetNextProtectedFile**](/windows/win32/api/sfc/nf-sfc-sfcgetnextprotectedfile) (voir opérations de restauration VSS des fichiers protégés par WFP) -   les fichiers de configuration du compteur de performances : <dl> % SystemRoot% \\ system32 \\ perf ? 00 ?. anciens  
    % SystemRoot% \\ system32 \\ perf ? 00 ?. bak </dl>
-le cas échéant, le fichier de métabase internet Information Server (IIS) doit être inclus dans les opérations de sauvegarde et de restauration, car il contient l’état utilisé par Microsoft Exchange et d’autres applications réseau. Ce fichier se trouve à l'emplacement suivant : <dl> % SystemRoot% \\ system32 \\ inetsrv \\ Metabase. bin </dl>
-   Si le fichier de la métabase IIS est sauvegardé, les clés pour permettre aux applications de lire certaines entrées chiffrées doivent être restaurées dans le cadre de l’état du système. Les fichiers se trouvent sous : <dl> % SystemRoot% \\ system32 \\ Microsoft \\ Protect\\\*  
    % AllUsersProfile% \\ Microsoft \\ crypto \\ RSA \\ MachineKeys\\\* </dl>
-Lors de la sauvegarde des fichiers système et de démarrage, il peut s’avérer nécessaire de déterminer le périphérique de démarrage DOS en procédant comme suit : 1. recherchez la partition système sous **HKEY \_ local \_ machine** \\ **System** \\ **Setup** \\ **SystemPartition**.
    2.  Transmettez la variable d’environnement racine système (% SystemRoot%) au gestionnaire de montage pour obtenir le nom de l’appareil NT.

## <a name="vss-restore-operations-of-wfp-protected-files"></a>Opérations de restauration VSS des fichiers protégés par WFP

Le service WFP est conçu pour empêcher le remplacement accidentel ou fragmentaire des fichiers système. Par conséquent, des étapes spéciales doivent être effectuées pour restaurer les données WFP.

Signifie que l’enregistreur WFP doit spécifier la méthode **VSS \_ RME \_ Restore \_ au \_ redémarrage de** la restauration lors de la définition de son document de métadonnées d’écriture. Si un demandeur détermine que le scripteur WFP n’a pas pu spécifier cette méthode de restauration, il indique une erreur de writer.

Un demandeur doit implémenter une méthode de restauration de la **\_ restauration VSS RME \_ \_ au \_ redémarrage** à l’aide de la fonction Win32 [**MoveFileEx**](/windows/win32/api/winbase/nf-winbase-movefileexa) avec le **délai MOVEFILE jusqu’au paramètre \_ \_ \_ reboot** pour remplacer les fichiers système. Les fichiers restaurés ne sont pas copiés dans les répertoires de fichiers système réels tant que le système n’a pas redémarré. Le remplacement des fichiers système protégés se produit uniquement si la valeur de l’entrée de Registre **reg \_ Word** suivante est définie sur 1 :

**HKEY \_ \_** Gestionnaire de session du contrôle CurrentControlSet du système de l’ordinateur local \\  \\  \\  \\  \\ **AllowProtectedRenames** = 1

Cette valeur doit être définie avant tout démarrage où les fichiers protégés doivent être remplacés par [**MoveFileEx**](/windows/win32/api/winbase/nf-winbase-movefileexa) et sont supprimés après le redémarrage.

Le répertoire système dllcache doit également être sauvegardé ou restauré, avec la sauvegarde et la restauration du volume de démarrage, et se trouve en examinant l’entrée de Registre **reg \_ expand \_ SZ** :

**HKEY \_ logiciel de l' \_ ordinateur LOCAL** \\  \\ **Microsoft** \\ **Windows NT** \\ **CurrentVersion** \\ **WinLogon** \\ **SfcDllCache**<dl> <dt>

                  Data type
</dt> <dd>                  REG \_ développer \_ SZ</dd> </dl>

Le contenu du répertoire System dllcache est reconstruit à l’aide de l’outil de vérification des fichiers système (SFC) à partir de l’invite de commandes :

-   L’option **/scanonce** analyse tous les fichiers protégés au prochain démarrage du système.
-   L’option **/scannow** analyse immédiatement tous les fichiers protégés.

Tous les fichiers protégés sont analysés, et toutes les versions qui ne sont pas valides seront remplacées à la fois dans le répertoire et dans l’emplacement dllcache.

Il y a quatre fichiers qui font partie de la plateforme WFP qui ne peuvent pas être restaurés avec les fichiers WFP :

<dl> Ctl3dv2.dll  
DtcSetup.exe  
NtDll.dll  
Smss.exe  
</dl>

Ces fichiers facilitent le processus de restauration des fichiers WFP et, par conséquent, une dépendance circulaire. Actuellement, il n’existe aucun moyen de restaurer ces fichiers, sauf pour réinstaller Windows.

 

 
