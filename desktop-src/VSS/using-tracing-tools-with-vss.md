---
description: Pour collecter des informations de suivi pour l’infrastructure VSS, vous pouvez utiliser l’outil VssTrace, logman ou l’outil tracelog.
ms.assetid: afe2a0ed-1a8e-4f8b-be9e-241d55cd9ef6
title: Utilisation des outils de suivi avec VSS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 073a2ae9ba2ba2771abdc37ff0291764ed5e9efd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104201458"
---
# <a name="using-tracing-tools-with-vss"></a>Utilisation des outils de suivi avec VSS

Pour collecter des informations de suivi pour l’infrastructure VSS, vous pouvez utiliser l’outil VssTrace, logman ou l’outil tracelog. VssTrace est disponible dans le kit de développement logiciel (SDK) Microsoft Windows et peut être utilisé pour suivre des applications VSS sur Windows 7 et les versions ultérieures du système d’exploitation Windows. Logman est un contrôleur de trace pour les événements de trace et les compteurs de performance. Il peut également être utilisé pour effectuer le suivi des applications VSS sur Windows 7 et les versions ultérieures du système d’exploitation Windows. Tracelog est inclus dans le kit WDK (Windows Driver Kit).

Pour utiliser les outils de suivi avec la [récupération automatique du système (ASR)](using-vss-automated-system-recovery-for-disaster-recovery.md), consultez [utilisation des outils de suivi avec les applications ASR](using-tracing-tools-with-vss-asr-applications.md).

> [!Note]  
> VssTrace, logman et tracelog requièrent tous des privilèges d’administrateur.

 

Pour plus d’informations sur chaque outil, consultez les sections suivantes :

-   [Utilisation de VssTrace](#using-vsstrace)
    -   [Options de Command-Line VssTrace](#vsstrace-command-line-options)
-   [Utilisation de logman](#using-logman)
-   [Utilisation de tracelog](#using-tracelog)

## <a name="using-vsstrace"></a>Utilisation de VssTrace

Pour exécuter l’outil VssTrace à partir de la ligne de commande, utilisez la syntaxe suivante :

 *options de ligne de commande* vsstrace

Pour afficher une aide concise sur la ligne de commande pour l’outil VssTrace, utilisez la syntaxe suivante :

**vsstrace-aide**

Pour afficher une aide détaillée sur la ligne de commande de l’outil VssTrace, utilisez la syntaxe suivante :

**vsstrace-help all**

### <a name="vsstrace-command-line-options"></a>Options de Command-Line VssTrace

L’outil VssTrace utilise les options de ligne de commande suivantes :

<dl> <dt>

<span id="-f_Flags"></span><span id="-f_flags"></span><span id="-F_FLAGS"></span>**-f (** *indicateurs* )
</dt> <dd>

Activez les modules dont les indicateurs sont spécifiés par le masque de masque des *indicateurs* . Chaque indicateur correspond à un module VSS. Si *Flags* est égal à zéro, aucun module n’est activé. Notez que la plupart des modules sont activés par défaut. Cette option peut être combinée avec l' **+** option _module_ . Par exemple, **vsstrace-f 0 + Writer + Coord** désactive le suivi de tous les modules qui sont activés par défaut et active le suivi des enregistreurs VSS et du service VSS. Sinon, **vsstrace + f 0xFFFF-Coord** active le suivi de tous les modules à l’exception du service VSS.

> [!Note]  
> Si vous utilisez l’option **-f** avec l’option **+** _module_ , le **-f** doit apparaître avant l’option **+** _module_ .

 

Le tableau suivant répertorie le nom et l’indicateur du module pour chaque module disponible.

| Module | Indicateur       | Activée par défaut | Éléments suivis                                                                                                                                  |
|--------|------------|--------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| EXCEPT | 0x00000001 | Oui                | Gestion des exceptions C++.                                                                                                                       |
| COORDONNÉES  | 0x00000002 | Oui                | Le service VSS, également appelé coordinateur VSS.                                                                                    |
| SWPRV  | 0x00000004 | Oui                | Service du fournisseur de clichés instantanés du système VSS.                                                                                                  |
| BUCOMP | 0x00000008 | Oui                | Le demandeur VSS et le traitement des métadonnées de sauvegarde.                                                                                             |
| WRITER | 0x00000010 | Oui                | Les opérations de l’enregistreur VSS et les implémentations du writer hébergé VSS, telles que l’enregistreur du Registre Windows.                                             |
| VSSAPI | 0x00000020 | Oui                | Fonctions diverses de l’API VSS exportées par VSSAPI.DLL.                                                                                |
| HWDIAG | 0x00000040 | Oui                | L’infrastructure et les opérations du fournisseur de matériel VSS.                                                                                          |
| ADMIN  | 0x00000080 | Oui                | Les utilitaires de ligne de commande VSS tels que VSSADMIN.EXE et DISKSHADOW.EXE.                                                                           |
| VSSUI  | 0x00000100 | Oui                | Interface utilisateur de configuration de clichés instantanés pour dossiers partagés. L’interface utilisateur est disponible uniquement sur les systèmes d’exploitation Windows Server.         |
| TEST   | 0x00000200 | Oui                | Non applicable. (Ce module de traçage est réservé.)                                                                                            |
| IOCTL  | 0x00000400 | Oui                | Détails des opérations FSCTL et IOCTL que le service VSS a lancées en appelant la fonction [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) . |
| GÉNÉRAL    | 0x00000800 | Oui                | Fonctions générales de l’utilitaire VSS, telles que les allocateurs, les classes de chaîne et les opérations de Registre et de volume.                                        |
| WRXML  | 0x00001000 | Non                 | Traitement XML pour les métadonnées de l’enregistreur. Ce module présente un niveau de bruit très élevé.                                                               |
| VSSXML | 0x00002000 | Non                 | Classes de base de traitement XML. Ce module présente un niveau de bruit très élevé.                                                                      |



 

</dd> <dt>

<span id="_Module"></span><span id="_module"></span><span id="_MODULE"></span>**+**_Modules_
</dt> <dd>

Active le module spécifié par le *module*. Plusieurs modules peuvent être activés à la fois. Pour répertorier les modules disponibles, tapez **vsstrace – Help modules** à l’invite de ligne de commande.

</dd> <dt>

<span id="-Module"></span><span id="-module"></span><span id="-MODULE"></span>**-**_Modules_
</dt> <dd>

Désactive le module spécifié par le *module*. Pour répertorier les modules disponibles, tapez **vsstrace – Help modules** à l’invite de ligne de commande.

</dd> <dt>

<span id="_pid_ProcessId"></span><span id="_pid_processid"></span><span id="_PID_PROCESSID"></span>**+ PID** *ProcessID*
</dt> <dd>

Activez le processus spécifié par *ProcessID*. Pour activer tous les processus, utilisez « \* » pour la valeur de *ProcessID*. Plusieurs options **PID** peuvent être spécifiées à la fois. L’ordre des options détermine les processus qui sont activés ou désactivés. Par exemple, pour activer uniquement le processus dont l’identificateur de processus est 0xe8c, utilisez **vsstrace-PID \* + PID 0xe8c**.

</dd> <dt>

<span id="-pid_ProcessId"></span><span id="-pid_processid"></span><span id="-PID_PROCESSID"></span>**-PID** *ProcessID*
</dt> <dd>

Désactivez le processus spécifié par *ProcessID*. Pour désactiver tous les processus, utilisez « \* » pour la valeur de *ProcessID*. Plusieurs options **PID** peuvent être spécifiées à la fois. L’ordre des options détermine les processus qui sont activés ou désactivés. Par exemple, pour désactiver tous les processus à l’exception du processus dont l’identificateur de processus est 0xe8c, utilisez **vsstrace-PID \* + PID 0xe8c**.

</dd> <dt>

<span id="_tid_ThreadId"></span><span id="_tid_threadid"></span><span id="_TID_THREADID"></span>*ThreadID* **+ TID**
</dt> <dd>

Active le thread spécifié par *ThreadID*. Pour activer tous les threads, utilisez « \* » pour la valeur de *ThreadID*. Plusieurs options **TID** peuvent être spécifiées à la fois. L’ordre des options détermine les threads qui sont activés ou désactivés. Par exemple, pour activer uniquement le thread dont l’identificateur de processus est 0x31a, utilisez **vsstrace-TID \* + TID 0x31a**.

</dd> <dt>

<span id="-tid_ThreadId"></span><span id="-tid_threadid"></span><span id="-TID_THREADID"></span>**-TID** *ThreadID*
</dt> <dd>

Désactive le thread spécifié par *ThreadID*. Pour désactiver tous les threads, utilisez « \* » pour la valeur de *ThreadID*. Plusieurs options **TID** peuvent être spécifiées à la fois. L’ordre des options détermine les threads qui sont activés ou désactivés. Par exemple, pour désactiver tous les threads à l’exception du thread dont l’identificateur de processus est 0x31a, utilisez **vsstrace-TID \* + TID 0x31a**.

</dd> <dt>

<span id="-l_Level"></span><span id="-l_level"></span><span id="-L_LEVEL"></span>**-l** *niveau*
</dt> <dd>

Utilisez le niveau de suivi spécifié par *niveau*. Plus le niveau est élevé, plus la sortie de trace est détaillée. Chaque niveau comprend tous les niveaux inférieurs. Le niveau par défaut est 170. Les niveaux suivants sont disponibles.



| Level | Informations incluses dans la sortie de trace |
|-------|------------------------------------------|
| 000   | Aucun                                     |
| 020   | Erreurs irrécupérables                             |
| 030   | Exceptions non prises en charge                     |
| 040   | Erreurs                                   |
| 050   | Assertions                               |
| 060   | Avertissements                                 |
| 080   | Gestion des exceptions                       |
| 100   | Activité du journal des événements                       |
| 120   | Informations générales                      |
| 140   | Flux de code                                |
| 160   | Entrée et sortie de la fonction                  |
| 170   | Valeurs de retour de fonction                   |
| 180   | Paramètres de fonction (laconique)              |
| 190   | Paramètres de fonction (verbose)            |
| 200   | Niveau d’information détaillé 1              |
| 210   | Informations détaillées niveau 2              |
| 220   | Niveau d’information détaillé 3              |
| 230   | Niveau de code rapide 1                        |
| 240   | Niveau de code rapide 2                        |
| 250   | Niveau de code rapide 3                        |
| 255   | Tous                                      |



 

</dd> <dt>

<span id="_indent"></span><span id="_INDENT"></span>**+ retrait**
</dt> <dd>

Mettez en retrait la sortie de trace mise en forme à chaque limite de fonction et de sous-fonction.

</dd> <dt>

<span id="-indent"></span><span id="-INDENT"></span>**-Indent**
</dt> <dd>

Ne mettez pas en retrait la sortie de trace mise en forme.

</dd> <dt>

<span id="-etl_EtlFile"></span><span id="-etl_etlfile"></span><span id="-ETL_ETLFILE"></span>**-ETL** *EtlFile*
</dt> <dd>

Convertit le fichier de sortie logman spécifié par *EtlFile* dans un format de texte lisible.

</dd> <dt>

<span id="-o_OutputFile"></span><span id="-o_outputfile"></span><span id="-O_OUTPUTFILE"></span>**-o** *fichier_sortie*
</dt> <dd>

Enregistrez les informations de traçage dans le fichier de sortie spécifié par *outputfile*. Pour des performances optimales, le fichier de sortie doit se trouver sur un volume qui ne fait pas partie du cliché instantané.

</dd> <dt>

<span id="-help_HelpOption"></span><span id="-help_helpoption"></span><span id="-HELP_HELPOPTION"></span>**-Help** *HelpOption*
</dt> <dd>

Affichez l’aide de la ligne de commande spécifiée par *HelpOption*. Les valeurs *HelpOption* valides sont **modules**, **levels** et **All**. La spécification des **modules** entraîne la liste des modules. La spécification de **niveaux** entraîne la liste des niveaux disponibles. Si vous spécifiez **All** , l’aide détaillée est affichée. Si aucune option n’est utilisée, une aide concise est affichée.

</dd> </dl>

## <a name="using-logman"></a>Utilisation de logman

La procédure suivante décrit comment utiliser logman avec votre application VSS.

**Pour utiliser logman avec votre application VSS**

1.  Utilisez la commande suivante pour démarrer le suivi :

    **logman start VSS-o** *x : \\ * * * VSS. etl-ETS-p {9138500e-3648-4EDB-aa4c-859e9f7b7c38} 0xFFF 170**

    > [!Note]  
    > Remplacez « x : \\ » par le chemin d’accès au répertoire où vous souhaitez que le fichier journal des traces soit stocké.

     

2.  Utilisez la commande suivante pour arrêter le suivi :

    **logman arrêter VSS-ETS**

Le fichier journal des traces est *x \\ :* VSS. etl.

Pour plus d’informations sur l’outil Logman, consultez [Logman](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/cc753820(v=ws.11)).

## <a name="using-tracelog"></a>Utilisation de tracelog

La procédure suivante décrit comment utiliser tracelog.

**Pour utiliser tracelog**

1.  Créez un fichier texte nommé VSS. CTL qui contient uniquement le texte suivant :

    **9138500e-3648-4EDB-aa4c-859e9f7b7c38 VSS**

2.  Utilisez la commande suivante pour démarrer le suivi :

    **tracelog-Start VSS-f** *x : \\ * * * VSS. etl-GUID VSS. CTL-indicateur 0xFF-Level 0xAA**

    > [!Note]  
    > Remplacez « x : \\ » par le chemin d’accès au répertoire où vous souhaitez que le fichier journal des traces soit stocké.

     

3.  Utilisez la commande suivante pour arrêter le suivi :

    **tracelog-arrêter VSS**

Le fichier journal des traces est *x \\ :* VSS. etl.

Pour plus d’informations sur l’outil tracelog, consultez [tracelog](https://msdn.microsoft.com/library/ms797927.aspx).

 

 
