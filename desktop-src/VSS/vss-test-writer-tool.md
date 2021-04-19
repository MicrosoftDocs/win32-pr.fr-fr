---
description: Le writer de test est un utilitaire que vous pouvez utiliser pour tester des applications VSS.
ms.assetid: 02434cb9-390c-4cf0-9941-b833ace55685
title: Outil enregistreur de test VSS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 61ffdbb513697a701866be5ceeb40168e8c28368
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106536116"
---
# <a name="vss-test-writer-tool"></a>Outil enregistreur de test VSS

Le writer de test est un utilitaire que vous pouvez utiliser pour tester des applications VSS. Ce writer peut être configuré pour effectuer presque toutes les actions qu’un enregistreur VSS peut effectuer. En outre, l’enregistreur de test effectue des vérifications importantes pour s’assurer que le demandeur a correctement traité ces actions d’écriture.

Chaque instance du writer est initialisée avec un fichier de configuration XML qui décrit exactement les composants sur lesquels le writer fera l’objet d’un rapport, ainsi que le comportement de l’enregistreur. Le writer peut être configuré pour signaler différents types de scénarios, y compris des scénarios plus complexes utilisant les interfaces incrémentielles et différentielles. Le rédacteur effectue des vérifications à différents moments pendant le processus pour s’assurer que le demandeur se comporte de manière appropriée. Une fois la restauration terminée, l’enregistreur vérifie que tous les fichiers nécessaires ont été restaurés sans endommagement. Le writer peut également être configuré pour exécuter d’autres opérations, telles que des événements spécifiques en cas d’échec.

> [!Note]  
> Cet outil est inclus dans le kit de développement logiciel (SDK) Microsoft Windows pour Windows Vista et versions ultérieures. Vous pouvez télécharger le SDK Windows à partir de [https://msdn.microsoft.com/windowsvista](https://msdn.microsoft.com/windows/default.aspx) .

 

Dans l’installation SDK Windows, l’outil VssSampleProvider se trouve dans `%Program Files(x86)%\Windows Kits\8.1\bin\x64` (pour Windows 64 bits) et `%Program Files(x86)%\Windows Kits\8.1\bin\x86` .

## <a name="running-the-test-writer-tool"></a>Exécution de l’outil test Writer

Pour démarrer le writer de test, tapez la commande suivante à l’invite de commandes :

 *Fichier config* vswriter.exe

où *config-file* est le chemin d’accès à un fichier de configuration qui spécifie le comportement de ce writer.

Pour arrêter le writer de test, appuyez sur CTRL + C.

Plusieurs instances de l’enregistreur de test peuvent être exécutées en même temps. Toutefois, chaque instance du writer signalera le même ID de classe de Writer (bien qu’un ID d’instance de writer différent), de sorte que les chemins d’accès logiques et les noms de composants doivent être uniques dans toutes les instances d’exécution simultanées du writer.

Pour vous assurer que le rédacteur peut vérifier correctement que le demandeur a respecté les spécifications d’exclusion de fichier, tous les fichiers qui ont été sauvegardés doivent être supprimés du volume d’origine avant d’essayer de les restaurer. Il est recommandé de stocker un modèle de chaque scénario de writer, afin que le scénario puisse être recréé facilement.

## <a name="using-a-configuration-file"></a>Utilisation d'un fichier de configuration

L’exemple de fichier de configuration suivant, vswriter \_config.xml, se trouve dans `%ProgramFiles%\Microsoft SDKs\Windows\v7.0\bin\vsstools` sur les plateformes x86 et `%ProgramFiles%\Microsoft SDKs\Windows\v7.0\bin\x64\vsstools` sur les plateformes x64.

``` syntax
<TestWriter usage="USER_DATA">

    <RestoreMethod method="RESTORE_IF_CAN_BE_REPLACED"
                   writerRestore="always"
                   rebootRequired="no" />

    <ExcludeFile path="c:\writerData\notTheseFiles" 
                 filespec="excludeThisFile.txt" 
                 recursive="no"/>

    <Component componentType="filegroup"
               componentName="TestFiles">
        <ComponentFile path="c:\writerData\myFilesHere" 
                       filespec="*"
                       recursive="no" />
    </Component>

</TestWriter>
```

L’élément racine dans ce fichier de configuration est nommé TestWriter. Tous les autres éléments sont organisés sous l’élément TestWriter.

L’un des attributs associés à TestWriter est l’attribut d’utilisation. Cet attribut spécifie le type d’utilisation signalé par le biais de [**IVssExamineWriterMetadata :: GetIdentity**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssexaminewritermetadata-getidentity). L’une des valeurs possibles pour cet attribut est \_ données utilisateur.

Le premier élément enfant de l’élément racine doit toujours être un élément RestoreMethod. Cet élément spécifie les éléments suivants :

-   La méthode Restore (dans ce cas, Restore \_ si \_ peut \_ être \_ remplacé)
-   Si l’enregistreur requiert des événements de restauration (dans ce cas, toujours)
-   Si un redémarrage est nécessaire après la restauration de l’enregistreur (dans ce cas, non)

Cet élément peut éventuellement spécifier un autre mappage d’emplacement. (Dans ce cas, aucun autre emplacement n’est spécifié.)

Le deuxième élément enfant est un élément ExcludeFile. Cet élément fait en sorte que le writer exclut un fichier ou un ensemble de fichiers de la sauvegarde.

Le troisième élément enfant est un élément de composant. Cet élément amène le writer à ajouter un composant à ses métadonnées. Un élément composant contient des attributs permettant de décrire le composant et les éléments enfants pour décrire le contenu du composant, comme suit :

-   componentType pour indiquer s’il s’agit d’un groupe de fichiers ou d’une base de données
-   logicalPath pour le chemin d’accès logique du composant
-   componentName pour le nom du composant
-   sélectionnable pour indiquer l’État sélectionnable pour la sauvegarde

L’élément Component a également un élément enfant nommé ComponentFile pour ajouter une spécification de fichier à ce composant. (Un élément de composant peut avoir un nombre arbitraire d’éléments ComponentFile qui peuvent être spécifiés pour chaque composant.) Cet élément ComponentFile a les attributs suivants :

-   path = "c : \\ writerData \\ myFilesHere"
-   spécification de spécification = " \* "
-   récursif = « non »

Bien que le writer de test vérifie le comportement du demandeur, il ne vérifie pas que le fichier de configuration gère toujours la sémantique documentée pour un writer. Il y a de nombreuses opérations qu’un enregistreur bien composé ne doit pas faire (par exemple, pour signaler le même fichier dans plusieurs composants) et c’est à l’auteur du fichier de configuration XML de conserver ces sémantiques.

## <a name="configuring-writer-attributes"></a>Configuration des attributs du writer

L’élément racine TestWriter contient des attributs qui déterminent différents comportements du writer. Voici quelques-uns des comportements qui peuvent être modifiés :



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Attribut</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span id="verbosity"></span><span id="VERBOSITY"></span>Commentaires<br/></td>
<td>Le rédacteur imprime l’État sur la console lorsqu’il reçoit des événements et les traite. Le niveau de détail affiché est spécifié par l’attribut de commentaires. Vous avez le choix entre trois niveaux de commentaires :<br/> <dl> <dt><span id="low"></span><span id="LOW"></span>entrée</dt> <dd> Seuls les échecs dans le writer ou un comportement incorrect du demandeur seront imprimés.<br/> </dd> <dt><span id="medium"></span><span id="MEDIUM"></span>médias</dt> <dd> Tout ce qui a un niveau de détail faible est imprimé en plus des informations d’État supplémentaires, par exemple lors de la réception des événements. C'est le niveau par défaut.<br/> </dd> <dt><span id="high"></span><span id="HIGH"></span>rapide</dt> <dd> Des informations d’État détaillées sur le fonctionnement de l’enregistreur sont signalées.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span id="deleteFiles"></span><span id="deletefiles"></span><span id="DELETEFILES"></span>deleteFiles<br/></td>
<td>Pour effectuer une vérification supplémentaire, définissez cet attribut sur &quot; Oui &quot; pour obliger l’enregistreur à supprimer tous ses fichiers immédiatement après la création du cliché instantané de volume. Le demandeur doit ensuite copier les fichiers à partir du cliché instantané, car ils n’existent plus sur le volume d’origine. <br/>
<blockquote>
[!Note]<br />
Dans le cas des enregistreurs de fractionnement, les fichiers sont supprimés de l’emplacement d’origine après le fractionnement, mais avant la création du cliché instantané. Une fois le cliché instantané créé, les fichiers sont supprimés du répertoire de fractionnement.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="deletePartialFiles"></span><span id="deletepartialfiles"></span><span id="DELETEPARTIALFILES"></span>deletePartialFiles<br/></td>
<td>Pour supprimer des fichiers partiels, affectez la valeur Oui à cet attribut &quot; &quot; .<br/></td>
</tr>
<tr class="even">
<td><span id="deleteDifferencedFiles"></span><span id="deletedifferencedfiles"></span><span id="DELETEDIFFERENCEDFILES"></span>deleteDifferencedFiles<br/></td>
<td>Pour supprimer des fichiers différenciés, définissez cet attribut sur &quot; Oui &quot; .<br/></td>
</tr>
<tr class="odd">
<td><span id="checkIncludes"></span><span id="checkincludes"></span><span id="CHECKINCLUDES"></span>checkIncludes<br/></td>
<td>Définissez cet attribut sur &quot; Oui &quot; pour obliger l’enregistreur à vérifier que tous les fichiers qui ont été sauvegardés ont été restaurés à un emplacement approprié et que le fichier n’a pas été endommagé. Les fichiers partiels et les fichiers différenciés sont également gérés correctement.<br/></td>
</tr>
<tr class="even">
<td><span id="checkExcludes"></span><span id="checkexcludes"></span><span id="CHECKEXCLUDES"></span>checkExcludes<br/></td>
<td>Définissez cet attribut sur &quot; Oui &quot; pour obliger l’enregistreur à vérifier que les fichiers correspondant à une spécification de fichier dans la liste d’exclusion ne sont pas restaurés. Pour que cela fonctionne correctement, les répertoires de restauration doivent être vidés avant la restauration.<br/></td>
</tr>
</tbody>
</table>



 

## <a name="specifying-alternate-location-mappings"></a>Spécification de mappages d’emplacements de substitution

Un autre mappage d’emplacement spécifie un emplacement vers lequel effectuer la restauration si la méthode de restauration est VSS \_ WRE \_ restaurer \_ à un \_ autre \_ emplacement ou si la restauration normale d’un composant échoue. Un enregistreur peut signaler ses mappages d’emplacements alternatifs au demandeur à l’aide de la méthode [**IVssExamineWriterMetadata :: GetAlternateLocationMapping**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssexaminewritermetadata-getalternatelocationmapping) . Vous pouvez ajouter d’autres mappages d’emplacement au fichier de configuration du writer de test en ajoutant des sous-éléments AlternateLocationMapping à l’élément RestoreMethod.

L’élément RestoreMethod suivant contient un sous-élément AlternateLocationMapping.

``` syntax
<RestoreMethod method="RESTORE_IF_CAN_REPLACE"
              writerRestore="always"
              rebootRequired="no">
    <AlternateLocationMapping path="c:\files"
                              filespec="*.txt"
                              recursive="no"
                              alternatePath="c:\altfiles"/>
</RestoreMethod>
```

Cet exemple spécifie que le demandeur doit tout d’abord tenter de restaurer tous les fichiers correspondant à c : \\ Files \\ \* . txt dans le \\ répertoire c : files. Si l’un de ces fichiers ne peut pas être remplacé, le demandeur doit restaurer tous les fichiers dans le répertoire c : altfiles à la \\ place. Le demandeur doit enregistrer ce mappage de l’autre emplacement à l’aide de la méthode [**IVssBackupComponents :: AddAlternativeLocationMapping**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addalternativelocationmapping) . Si le writer de test est configuré pour vérifier si les fichiers ont été restaurés, il vérifie également si le demandeur a appelé **AddAlternativeLocationMapping**.

## <a name="specifying-files-to-be-excluded"></a>Spécification des fichiers à exclure

Chaque enregistreur peut spécifier une liste de spécifications de fichiers qui spécifient les fichiers à exclure de la sauvegarde par le demandeur. Vous pouvez ajouter ces spécifications de fichier au fichier de configuration du writer de test en ajoutant des sous-éléments ExcludeFile à l’élément racine TestWriter.

Voici un exemple de sous-élément ExcludeFile qui exclut tous les fichiers dans le répertoire C : \\ Files qui correspondent à c : \\ temp \* . \* .

``` syntax
    <ExcludeFile path="c:\files" 
                 filespec="temp*.*" 
                 recursive="no"/>
```

## <a name="backing-up-spit-writers"></a>Sauvegarde des enregistreurs de fractionnement

De nombreux enregistreurs jouent le rôle de « rédacteurs de fractionnement ». Un enregistreur de fractionnement crée des fichiers intermédiaires, ou « fichiers de fractionnement », en fonction d’un jeu de fichiers d’origine, et place les fichiers de fractionnement dans un autre emplacement au moment de la sauvegarde. Le writer utilise la méthode [**IVssWMFiledesc :: GetAlternateLocation**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswmfiledesc-getalternatelocation) pour notifier au demandeur qu’il doit sauvegarder ces fichiers à partir de l’emplacement secondaire. Toutefois, ces fichiers doivent toujours être restaurés à l’emplacement actif des fichiers d’origine. L’enregistreur de test peut être configuré pour agir en tant qu’enregistreur de fractionnement pour une spécification de fichier particulière.

L’élément ComponentFile suivant contient un attribut alternatePath :

``` syntax
    <ComponentFile path="c:\files"
                   filespec="*.txt"
                   recursive="no"
                   alternatePath="c:\files\spit" />
```

Cet exemple configure le writer de test pour copier tous les fichiers correspondant à c : \\ Files \\ \* . txt dans le \\ répertoire c : Files de \\ fractionnement juste avant la création du cliché instantané de volume. Le demandeur doit sauvegarder les fichiers à partir du \\ Répertoire de fractionnement c : Files \\ . Si le writer de test est configuré pour supprimer des fichiers, il supprime les fichiers d’origine avant que le cliché instantané ne soit créé, de sorte qu’ils n’apparaissent pas dans le répertoire c : \\ Files du volume de clichés instantanés. Dans ce cas, les fichiers figurant dans c : \\ files de \\ fractionnement sont supprimés après la création du cliché instantané. ils doivent donc être sauvegardés à partir du répertoire c : \\ Files \\ de fractionnement sur le volume des clichés instantanés.

## <a name="reporting-component-dependencies"></a>Dépendances des composants de rapport

Les enregistreurs peuvent spécifier une dépendance entre un composant local et un composant qui existe dans un autre writer. Ces dépendances sont signalées au demandeur à l’aide de [**IVssWMComponent :: GetDependency**](/windows/desktop/api/VsBackup/nf-vsbackup-ivsswmcomponent-getdependency). Le writer de test peut être configuré pour signaler ces dépendances en ajoutant un ou plusieurs sous-éléments de dépendance à l’élément de composant.

L’élément Component suivant contient un sous-élément Dependency :

``` syntax
    <Component componentType="filegroup"
               logicalPath=""
               componentName="WriterComponent"
               selectable="yes">
         <Dependency writerId="<GUID of target writer>"
                     logicalPath="ComponentPath"
                     componentName="Writer2Component" />
    </Component>
```

La dépendance est spécifiée en tant qu’attributs de l’élément de dépendance. writerId est l’ID de classe du writer contenant la cible de la dépendance, logicalPath est le chemin logique du composant dans ce Writer et componentName est le nom du composant. Dans ce cas, si le demandeur sauvegarde « WriterComponent » dans le writer actuel, il doit également sauvegarder le composant « ComponentPath \\ Writer2Component » dans le writer cible.

> [!Note]  
> Le writer de test n’effectue aucune vérification pour vérifier que les dépendances sont respectées.

 

## <a name="failing-events"></a>Événements ayant échoué

L’enregistreur de test peut être configuré pour faire échouer les événements normaux reçus par un writer. Ces événements sont les suivants :



| Événement                                                                                                                                    | Description                                                                                                                                                                                                                                                         |
|------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Identify"></span><span id="identify"></span><span id="IDENTIFY"></span>Repérer<br/>                                     | Reçu en réponse à un appel de [**IVssBackupComponents :: GatherWriterMetadata**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwritermetadata) . En cas d’échec, l’enregistreur n’est pas signalé.<br/>                                                                 |
| <span id="PrepareForBackup"></span><span id="prepareforbackup"></span><span id="PREPAREFORBACKUP"></span>PrepareForBackup<br/>     | Reçu en réponse au demandeur appelant [**IVssBackupComponents ::P repareforbackup**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prepareforbackup).<br/>                                                                                                                 |
| <span id="PrepareForSnapsot"></span><span id="prepareforsnapsot"></span><span id="PREPAREFORSNAPSOT"></span>PrepareForSnapsot<br/> | Reçu lorsque le demandeur appelle [**IVssBackupComponents ::D osnapshotset**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-dosnapshotset), mais avant la création du cliché instantané.<br/>                                                                                              |
| <span id="Freeze"></span><span id="freeze"></span><span id="FREEZE"></span>Antigel<br/>                                             | Reçu immédiatement après [*PrepareForSnapshot*](vssgloss-p.md), mais avant la création du cliché instantané.<br/>                                                                                                      |
| <span id="Thaw"></span><span id="thaw"></span><span id="THAW"></span>Congelé<br/>                                                     | Reçue à la fin de la création du cliché instantané.<br/>                                                                                                                                                                                                     |
| <span id="PostSnapshot"></span><span id="postsnapshot"></span><span id="POSTSNAPSHOT"></span>PostSnapshot<br/>                     | Reçu après la libération du dégel, mais avant la fin de [**IVssBackupComponents ::D osnapshotset**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-dosnapshotset) .<br/>                                                                                                                   |
| <span id="Abort"></span><span id="abort"></span><span id="ABORT"></span>Arrêté<br/>                                                 | Reçu si trop de temps s’écoule entre le [*gel*](vssgloss-f.md) et le [*dégel*](vssgloss-t.md) ou si le demandeur appelle [**IVssBackupComponents :: AbortBackup**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-abortbackup).<br/> |
| <span id="BackupComplete"></span><span id="backupcomplete"></span><span id="BACKUPCOMPLETE"></span>BackupComplete<br/>             | Reçu lorsque le demandeur se termine. Les défaillances ici ne seront jamais signalées.<br/>                                                                                                                                                                                 |
| <span id="PreRestore"></span><span id="prerestore"></span><span id="PRERESTORE"></span>Prérestauration<br/>                             | Reçu lorsque le demandeur appelle [**IVssBackupComponents ::P Restore**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prerestore).<br/>                                                                                                                                           |
| <span id="PostRestore"></span><span id="postrestore"></span><span id="POSTRESTORE"></span>PostRestore<br/>                         | Reçu lorsque le demandeur appelle [**IVssBackupComponents ::P ostrestore**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-postrestore).<br/>                                                                                                                                         |



 

Ces échecs sont configurés en ajoutant un ou plusieurs sous-éléments FailEvent à l’élément racine TestWriter. Deux classes de défaillances peuvent être définies : renouvelable et non renouvelable. Les erreurs pouvant être renouvelées sont des erreurs qui peuvent disparaître si l’intégralité du processus de sauvegarde est retentée, alors que des erreurs qui ne peuvent pas être renouvelées ne peuvent pas être supprimées. Le type d’échec de l’événement est choisi en fonction de l’attribut renouvelable.

Voici un exemple d’échec non renouvelable de base :

``` syntax
    <FailEvent writerEvent="Freeze"
               retryable="no" />
```

Cet exemple entraîne l’échec de l’enregistreur pendant l’événement [*Freeze*](vssgloss-f.md) . [**IVssBackupComponents :: GatherWriterStatus**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwriterstatus) signale que l’échec de l’enregistreur VSS E WRITERERROR n’est pas \_ \_ \_ renouvelable.

Voici un exemple d’erreur de base renouvelable :

``` syntax
    <FailEvent writerEvent="Freeze"
               retryable="yes"
               numFailures="2"/>
```

Dans cet exemple, l’enregistreur échouera les deux premières fois qu’il recevra un événement [*Freeze*](vssgloss-f.md) . Après les deux premières fois, l’enregistreur fonctionnera toujours. L’échec de l’enregistreur rapporté par [**GatherWriterStatus**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwriterstatus) sera un code d’erreur aléatoire renouvelable.

## <a name="declaring-supported-backup-types"></a>Déclaration des types de sauvegarde pris en charge

Les rédacteurs communiquent les types de sauvegarde pris en charge par l’appel de [**IVssExamineWriterMetadata :: GetBackupSchema**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssexaminewritermetadata-getbackupschema)par le demandeur. L’élément racine TestWriter contient des attributs pour chaque type de sauvegarde pour indiquer la prise en charge. Ces attributs sont supportsCopy, supportsDifferential, supportsIncremental et supportsLog. Pour indiquer la prise en charge d’un type de sauvegarde particulier, définissez l’attribut correspondant sur « Oui ».

Si le demandeur définit le type de sauvegarde sur un type de sauvegarde qui n’est pas pris en charge par l’enregistreur, le rédacteur note ce fait pendant la [**PrepareForBackup**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prepareforbackup), mais fonctionne normalement.

## <a name="indicating-the-file-backup-type"></a>Indication du type de sauvegarde de fichiers

La méthode [**IVssWMFiledesc :: GetBackupTypeMask**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswmfiledesc-getbackuptypemask) renvoie un masque de réécriture au demandeur indiquant comment un fichier doit être sauvegardé. Cela indique si un fichier est obligatoire ou non requis au cours de types spécifiques de sauvegarde, et si un cliché instantané est nécessaire au cours de types spécifiques de sauvegarde. Les types de sauvegarde dans ce masque de réécriture sont expliqués plus en détail dans le [rôle demandeur de document dans sauvegarde des magasins complexes](requestor-role-in-backing-up-complex-stores.md).

Dans le writer de test, les éléments de ce masque de réinitialisation sont spécifiés en définissant des attributs dans chaque élément ComponentFile. Les attributs fullBackupRequired, diffBackupRequired, incBackupRequired et logBackupRequired spécifient quand un fichier doit être sauvegardé. Les attributs fullSnapshotRequired, diffSnapshotRequired, incSnapshotRequired et logSnapshotRequired spécifient à quel moment un fichier doit être sauvegardé à partir d’un cliché instantané d’un volume (et jamais à partir du volume d’origine). La valeur par défaut de toutes ces valeurs est « oui », indiquant qu’un fichier doit toujours être sauvegardé et doit être sauvegardé à partir d’un cliché instantané d’un volume.

## <a name="adding-partial-files"></a>Ajout de fichiers partiels

Pendant le traitement de [**DoSnapshotSet**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-dosnapshotset), un enregistreur a la possibilité d’ajouter des fichiers partiels à chaque composant. Ces fichiers partiels sont signalés à l’aide de [**IVssComponent :: GetPartialFile**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getpartialfile). Le writer de test peut être configuré pour ajouter des fichiers partiels en spécifiant des sous-éléments PartialFile dans un élément de composant.

Voici un exemple d’élément de composant qui a deux sous-éléments PartialFile :

``` syntax
    <Component componentType="filegroup"
               logicalPath=""
               componentName="WriterComponent"
               selectable="yes">
        <ComponentFile path="c:\files"
                       filespec="*.txt"
                       recursive="no"/>
        <PartialFile path="c:\files"
                     filespec="partial.txt"
                     ranges="0:5,100:20" />
        <PartialFile path="c:\files2"
                     filespec="partial.txt"
                     ranges="0:5,100:20" />
    </Component>
```

Seuls les fichiers partiels qui correspondent partiellement à un ComponentFile existant (comme dans le premier fichier partiel de l’exemple) ou les nouveaux fichiers partiels qui se trouvent sur le même volume qu’un ComponentFile existant (comme dans le deuxième fichier partiel) doivent être spécifiés de cette façon. Pour ce composant, le demandeur doit sauvegarder entièrement tous les fichiers correspondant à c : \\ Files \\ \* . txt, à l’exception de partial.txt. Le demandeur doit ensuite sauvegarder les plages spécifiées (où une plage est un décalage suivi d’une longueur) pour les fichiers c : \\ files \\partial.txt et c : \\ files2 \\partial.txt.

Si le writer est configuré pour vérifier les restaurations de fichiers, seules les plages sauvegardées du fichier partiel sont vérifiées au moment de la restauration. Les modifications apportées à d’autres parties du fichier seront invisibles. Si l’attribut deletePartialFiles de l’élément racine TestWriter est défini, les fichiers partiels sont supprimés du volume d’origine immédiatement après la création du cliché instantané.

## <a name="adding-differenced-files"></a>Ajout de fichiers différenciés

Pendant le traitement de [**DoSnapshotSet**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-dosnapshotset), un enregistreur peut ajouter des fichiers différenciés à chaque composant. Ces fichiers différenciés sont signalés à l’aide de [**IVssComponent :: GetDifferencedFile**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getdifferencedfile). Le writer de test peut être configuré pour ajouter des fichiers différenciés en spécifiant des sous-éléments DifferencedFile dans un élément de composant.

Voici un exemple d’élément de composant qui a deux sous-éléments DifferencedFile :

``` syntax
    <Component componentType="filegroup"
               logicalPath=""
               componentName="WriterComponent"
               selectable="yes">
        <ComponentFile path="c:\files"
                       filespec="*.txt"
                       recursive="no"/>
        <DifferencedFile path="c:\files"
                         filespec="*.txt"
                         year="2007"
                         month="1"
                         day="22"
                         hour="12"
                         minute="44"
                         second="17" />
        <DifferencedFile path="c:\files2"
                         filespec="*.txt"
                         year="2007"
                         month="1"
                         day="22"
                         hour="12"
                         minute="44"
                         second="17" />
    </Component>
```

Contrairement aux fichiers partiels, les fichiers différenciés ne doivent jamais partiellement correspondre à une spécification ComponentFile. La spécification de fichier dans un élément DifferencedFile doit correspondre exactement à un ComponentFile (comme dans le premier fichier différent dans l’exemple) ou elle ne doit pas être identique, mais se trouver sur un volume référencé dans un ComponentFile (comme dans le deuxième fichier différent). Les valeurs de date et d’heure doivent être relatives au fuseau horaire local, mais elles seront converties en heure GMT avant d’être signalées au demandeur. Dans l’exemple, seuls les fichiers correspondant à c : \\ Files \\ \* . txt ou c : \\ files2 \\ \* . txt qui ont été modifiés depuis 1/22/2003:12:44:17 seront sauvegardés.

Si le writer de test est configuré pour vérifier les restaurations de fichiers, seuls les fichiers modifiés sont vérifiés pour la restauration. Si l’attribut deleteDifferencedFiles de l’élément racine TestWriter est défini, les fichiers différenciés sont supprimés du volume d’origine immédiatement après la création du cliché instantané.

## <a name="new-targets"></a>Nouvelles cibles

Certains enregistreurs permettent au demandeur de l’informer qu’un nouvel emplacement a été choisi pour restaurer certains fichiers. Le writer indique qu’il prend en charge ce mode dans le cadre du masque de masque retourné par [**IVssExamineWriterMetadata :: GetBackupSchema**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssexaminewritermetadata-getbackupschema). Par défaut, l’enregistreur de test prend toujours en charge les nouvelles cibles. Cette prise en charge peut être désactivée en affectant à l’attribut supportsNewTarget de l’élément racine TestWriter la valeur « no ».

Si un writer prend en charge de nouvelles cibles, le demandeur peut informer l’enregistreur de nouvelles cibles en appelant [**IVssBackupComponents :: AddNewTarget**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addnewtarget). Le rédacteur vérifie ensuite le nouvel emplacement cible pour vérifier la restauration plutôt que l’emplacement d’origine.

## <a name="more-information"></a>Informations complémentaires

Le writer de test prend en charge d’autres options de configuration qui ne sont pas décrites ici. Le schéma complet de toutes les fonctionnalités de configuration du writer de test est spécifié dans swriter.xml dans `%ProgramFiles%\Microsoft SDKs\Windows\v7.0\bin\x64\vsstools` (pour windows 64 bits) et `%ProgramFiles%\Microsoft SDKs\Windows\v7.0\bin\vsstools` (pour Windows 32 bits). Ce fichier contient un schéma XML qui décrit complètement tous les éléments et attributs qui composent un fichier de configuration. Chaque élément et chaque attribut de ce fichier sont commentés avec une description qui documente l’utilisation de l’attribut ou de l’élément.

 

 




