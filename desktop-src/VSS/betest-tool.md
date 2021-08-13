---
description: Le test est un demandeur VSS qui teste les opérations de sauvegarde et de restauration avancées.
ms.assetid: a6cc7308-a9fa-4a84-9e7c-4d0adda28db5
title: Outil de test
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fd5f37e8bfc224061a8205bf0759cbba4798b0d53227e4f12d89b1e9ddf629d5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119471149"
---
# <a name="betest-tool"></a>Outil de test

Le test est un demandeur VSS qui teste les opérations de sauvegarde et de restauration avancées. Cet outil peut être utilisé pour tester l’utilisation par une application de fonctionnalités VSS complexes, telles que les suivantes :

-   Sauvegarde incrémentielle et différentielle
-   Options de restauration complexes, telles que la restauration faisant autorité
-   Options de restauration par progression

> [!Note]  
> le test est inclus dans le kit de développement logiciel (SDK) de Microsoft Windows pour Windows Vista et versions ultérieures. le kit de développement logiciel (SDK) VSS 7,2 comprend une version de test qui s’exécute uniquement sur Windows Server 2003. cette rubrique décrit la version SDK Windows de test, et non la version Windows Server 2003 incluse dans le kit de développement logiciel (SDK) VSS 7,2. pour plus d’informations sur le téléchargement de la SDK Windows et du kit de développement logiciel (SDK) VSS 7,2, consultez [Service VSS](volume-shadow-copy-service-portal.md).

 

dans l’installation SDK Windows, l’outil de test est disponible dans `%Program Files(x86)%\Windows Kits\8.1\bin\x64` (pour les Windows 64 bits) et `%Program Files(x86)%\Windows Kits\8.1\bin\x86` (pour le Windows 32 bits).

## <a name="running-the-betest-tool"></a>Exécution de l’outil de test

Pour exécuter l’outil de test à partir de la ligne de commande, utilisez la syntaxe suivante :

 *Options de ligne de commande* de test

L’exemple d’utilisation suivant montre comment utiliser l’outil posant un test avec l' [outil writer de test VSS](vss-test-writer-tool.md), qui est un enregistreur VSS.

**Exemple d’utilisation de l’outil de test**

1.  Créez un répertoire de test nommé C : \\ distest. Copiez les fichiers suivants dans ce répertoire :
    -   betest.exe
    -   vswriter.exe
    -   [BetestSample.xml](#sample-xml-configuration-file-betestsamplexml)
    -   [VswriterSample.xml](#sample-xml-configuration-file-vswritersamplexml)
2.  Créez un répertoire nommé C : \\ TestPath. Placez certains fichiers de données de test dans ce répertoire.
3.  Créez un répertoire nommé C : \\ BackupDestination. Laissez ce répertoire vide.
4.  Ouvrez deux fenêtres de commandes avec élévation de privilèges et définissez le répertoire de travail de chacun sur C : disposant d’un \\ test.
5.  Dans la première fenêtre de commande, démarrez l' [outil enregistreur de test VSS](vss-test-writer-tool.md) comme suit :

    **vswriter.exe VswriterSample.xml**

    Le fichier vswriterSample.xml configure l’outil VSS test Writer Tool (vswriter) pour qu’il signale le contenu du \\ répertoire c : TestPath en vue d’une opération de sauvegarde. Notez que l’outil VSS test Writer ne produira pas de sortie tant qu’il ne détectera pas l’activité d’un demandeur comme un test. Pour arrêter l’outil enregistreur de test VSS, appuyez sur CTRL + C.

6.  Dans la deuxième fenêtre de commande, utilisez l’outil de test pour effectuer une opération de sauvegarde comme suit :

    **betest.exe/B/S backup.xml/D C : \\ BackupDestination/x BetestSample.xml**

    Le test va sauvegarder les fichiers du répertoire C : \\ TestPath dans le répertoire c : \\ BackupDestination. Le document du composant de sauvegarde est enregistré dans le fichier C : \\ test \\backup.xml.

7.  Si l’opération de sauvegarde réussit, supprimez le contenu du répertoire C : \\ TestPath et utilisez l’outil de test pour effectuer une opération de restauration comme suit :

    **betest.exe/R/S backup.xml/D C : \\ BackupDestination/x BetestSample.xml**

## <a name="betest-tool-command-line-options"></a>Outils de test Command-Line options

L’outil Test Tool utilise les options de ligne de commande suivantes pour identifier le travail à effectuer.

<dl> <dt>

<span id="_Auth"></span><span id="_auth"></span><span id="_AUTH"></span>**/Auth**
</dt> <dd>

Effectue une opération de restauration faisant autorité pour Active Directory ou Active Directory mode d’application.

**Windows Server 2003 :** Cette option de ligne de commande n’est pas prise en charge.

</dd> <dt>

<span id="_B"></span><span id="_b"></span>**/B**
</dt> <dd>

Effectue une opération de sauvegarde, mais n’effectue pas de restauration.

</dd> <dt>

<span id="_BC"></span><span id="_bc"></span>**/BC**
</dt> <dd>

Exécute uniquement l’opération de sauvegarde terminée.

**Windows Server 2003 :** Cette option de ligne de commande n’est pas prise en charge.

</dd> <dt>

<span id="_C_Filename"></span><span id="_c_filename"></span><span id="_C_FILENAME"></span> *Nom de fichier* /c
</dt> <dd>

> [!Note]  
> Cette option de ligne de commande est fournie uniquement pour la compatibilité descendante. L’option de ligne de commande **/x** doit être utilisée à la place.

 

Sélectionne les composants à sauvegarder ou à restaurer en fonction du contenu du fichier de configuration spécifié par *filename*. Ce fichier doit contenir uniquement des caractères ANSI dans la plage comprise entre 0 et 127, et il ne doit pas être supérieur à 1 Mo. Chaque ligne du fichier doit utiliser le format suivant :

*WriterId* : *ComponentName*;

Où *WriterId* est l’ID de l’enregistreur et *ComponentName* est le nom de l’un des composants du writer. L’ID de l’enregistreur et les noms des composants doivent être placés entre guillemets, et il doit y avoir des espaces avant et après les deux-points ( :). Si deux ou plusieurs composants sont spécifiés, ils doivent être séparés par des virgules. Par exemple :

"5affb034-969f-4919-8875-88f830d0ef89" : "TestFiles1", "TestFiles2", "TestFiles3";

</dd> <dt>

<span id="_D_Path"></span><span id="_d_path"></span><span id="_D_PATH"></span>**/D** *chemin d’accès*
</dt> <dd>

Enregistrez les fichiers sauvegardés dans ou restaurez-les à partir du répertoire de sauvegarde spécifié par *chemin d’accès*.

</dd> <dt>

<span id="_NBC"></span><span id="_nbc"></span>**/NBC**
</dt> <dd>

Omet l’opération de sauvegarde terminée.

**Windows Server 2003 :** Cette option de ligne de commande n’est pas prise en charge.

</dd> <dt>

<span id="_O"></span><span id="_o"></span>**/O**
</dt> <dd>

Spécifie que la sauvegarde comprend un État du système de démarrage.

</dd> <dt>

<span id="_P"></span><span id="_p"></span>**/P**
</dt> <dd>

Crée un cliché instantané persistant.

**Windows Server 2003 :** Cette option de ligne de commande n’est pas prise en charge.

</dd> <dt>

<span id="_Pre_Filename"></span><span id="_pre_filename"></span><span id="_PRE_FILENAME"></span> *Nom de fichier* /pre
</dt> <dd>

Si le type de sauvegarde spécifié dans l’option de ligne de commande **/t** est INCRÉMENTIEL ou différentiel, définissez le document de sauvegarde sur le fichier spécifié par *nom* de fichier pour la sauvegarde complète ou incrémentielle précédente.

**Windows Server 2003 et Windows XP :** Cette option de ligne de commande n’est pas prise en charge.

</dd> <dt>

<span id="_R"></span><span id="_r"></span>**/R**
</dt> <dd>

Effectue la restauration, mais n’effectue pas de sauvegarde. Doit être utilisé avec l’option de ligne de commande **/s** .

</dd> <dt>

<span id="_Rollback"></span><span id="_rollback"></span><span id="_ROLLBACK"></span>**/Rollback**
</dt> <dd>

Crée un cliché instantané qui peut être utilisé pour la restauration de l’application.

**Windows Server 2003 :** Cette option de ligne de commande n’est pas prise en charge.

</dd> <dt>

<span id="_S_Filename"></span><span id="_s_filename"></span><span id="_S_FILENAME"></span>**/S** *nom de fichier*
</dt> <dd>

En cas de sauvegarde, enregistre le document de sauvegarde dans le fichier spécifié par *filename*. En cas de restauration uniquement, charge le document de sauvegarde à partir de ce fichier.

</dd> <dt>

<span id="_Snapshot"></span><span id="_snapshot"></span><span id="_SNAPSHOT"></span>**/Snapshot**
</dt> <dd>

Crée un cliché instantané du volume, mais n’effectue pas de sauvegarde ou de restauration.

**Windows Server 2003 :** Cette option de ligne de commande n’est pas prise en charge.

</dd> <dt>

<span id="_StopError"></span><span id="_stoperror"></span><span id="_STOPERROR"></span>**/StopError**
</dt> <dd>

Arrête le test lorsque la première erreur d’écriture est rencontrée.

**Windows Server 2003 :** Cette option de ligne de commande n’est pas prise en charge.

</dd> <dt>

<span id="_T_BackupType"></span><span id="_t_backuptype"></span><span id="_T_BACKUPTYPE"></span>**/T** *BackupType*
</dt> <dd>

Spécifie le type de sauvegarde. *BackupType* peut être complet, Journal, Copy, Incremental ou Differential. Pour plus d’informations sur les types de sauvegardes, consultez la rubrique [**\_ \_ type de sauvegarde VSS**](/windows/desktop/api/Vss/ne-vss-vss_backup_type).

</dd> <dt>

<span id="_V"></span><span id="_v"></span>**/F**
</dt> <dd>

Génère une sortie détaillée qui peut être utilisée pour la résolution des problèmes.

**Windows Server 2003 :** Cette option de ligne de commande n’est pas prise en charge.

</dd> <dt>

<span id="_X_Filename"></span><span id="_x_filename"></span><span id="_X_FILENAME"></span>**/X** *nom du fichier*
</dt> <dd>

Sélectionne les composants à sauvegarder ou à restaurer en fonction du contenu du fichier de configuration XML spécifié par *filename*. Ce fichier doit contenir uniquement des caractères ANSI dans la plage comprise entre 0 et 127. Le format du fichier XML est défini par le schéma dans le fichier BETest.xml. Pour obtenir un exemple de fichier de configuration, consultez BetestSample.xml. Ces deux fichiers se trouvent dans le répertoire vsstools

> [!Note]  
> Vous pouvez afficher le fichier BETest.xml dans Internet Explorer. Avant d’ouvrir ce fichier, assurez-vous que le fichier XDR-Schema. xsl se trouve dans le même répertoire que BETest.xml. Le fichier XDR-Schema. xsl contient des instructions de rendu qui rendent le fichier BETest.xml plus lisible.

 

**Windows Server 2003 :** Cette option de ligne de commande n’est pas prise en charge.

</dd> </dl>

## <a name="sample-xml-configuration-file-betestsamplexml"></a>Exemple de fichier de configuration XML : BetestSample.xml

L’exemple de fichier de configuration suivant, BetestSample.xml, se trouve dans le répertoire Vsstools

``` syntax
<BETest>
    <Writer writerid="5affb034-969f-4919-8875-88f830d0ef89">
        <Component componentName="TestFiles">
        </Component>
    </Writer>
</BETest>
```

Cet exemple de fichier de configuration simple sélectionne un composant à sauvegarder ou à restaurer.

## <a name="sample-xml-configuration-file-vswritersamplexml"></a>Exemple de fichier de configuration XML : VswriterSample.xml

L’exemple de fichier de configuration suivant, VswriterSample.xml, se trouve dans le répertoire Vsstools

``` syntax
<TestWriter   usage="USER_DATA"
                    deleteFiles="no">

    <RestoreMethod method="RESTORE_IF_CAN_BE_REPLACED" 
                   writerRestore="always"
                   rebootRequired="no" />
    
    <Component componentType="filegroup" 
               componentName="TestFiles">
               <ComponentFile path="c:\TestPath" filespec="*" recursive="no" />
    </Component>

</TestWriter>
```

L’élément racine dans ce fichier de configuration est nommé TestWriter. Tous les autres éléments sont organisés sous l’élément TestWriter.

Le premier attribut associé à TestWriter est l’attribut d’utilisation. Cet attribut spécifie le type d’utilisation signalé par le biais de la méthode [**IVssExamineWriterMetadata :: GetIdentity**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssexaminewritermetadata-getidentity) . L’une des valeurs possibles pour cet attribut est \_ données utilisateur.

Le deuxième attribut est l’attribut deleteFiles. Cet attribut est décrit dans [Configuring Writer Attributes](vss-test-writer-tool.md).

Le premier élément enfant de l’élément racine est un élément RestoreMethod. Cet élément spécifie les éléments suivants :

-   La méthode Restore (dans ce cas, Restore \_ si \_ peut \_ être \_ remplacé)
-   Si l’enregistreur requiert des événements de restauration (dans ce cas, toujours)
-   Si un redémarrage est nécessaire après la restauration de l’enregistreur (dans ce cas, non)

Cet élément peut éventuellement spécifier un autre mappage d’emplacement. (Dans ce cas, aucun autre emplacement n’est spécifié.) Pour plus d’informations, consultez [spécification de mappages d’emplacements de substitution](vss-test-writer-tool.md).

Le deuxième élément enfant est un élément de composant. Cet élément amène le writer à ajouter un composant à ses métadonnées. Un élément composant contient des attributs permettant de décrire le composant et les éléments enfants pour décrire le contenu du composant, comme suit :

-   componentType pour indiquer s’il s’agit d’un groupe de fichiers ou d’une base de données (dans ce cas, un groupe de fichiers)
-   logicalPath pour le chemin d’accès logique du composant (dans ce cas, aucun n’est spécifié)
-   componentName pour le nom du composant (dans ce cas, « TestFiles »)
-   sélectionnable pour indiquer l’État sélectionnable pour la sauvegarde

L’élément Component a également un élément enfant nommé ComponentFile pour ajouter une spécification de fichier à ce composant. (Un élément de composant peut avoir un nombre arbitraire d’éléments ComponentFile qui peuvent être spécifiés pour chaque composant.) Cet élément ComponentFile a les attributs suivants :

-   path = "c : \\ TestPath"
-   spécification de spécification = " \* "
-   récursif = « non »

 

 



