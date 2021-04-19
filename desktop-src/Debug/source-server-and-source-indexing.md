---
description: Le serveur source permet à un client de récupérer la version exacte des fichiers sources qui ont été utilisés pour générer une application.
ms.assetid: c7bf51ce-7fb4-49aa-ad33-e551b2c8362b
title: Serveur source
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5b3d8d76c70b67c176126d8e424bd5b55b616697
ms.sourcegitcommit: bfb5d94f754d017307b4cc9d914a2716701331d1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106539360"
---
# <a name="source-server"></a>Serveur source

Le serveur source permet à un client de récupérer la version exacte des fichiers sources qui ont été utilisés pour générer une application. Étant donné que le code source d’un module peut changer d’une version à l’autre, il est important d’examiner le code source tel qu’il existait lors de la création de la version du module en question.

Le serveur source récupère les fichiers appropriés à partir du contrôle de code source. Pour utiliser le serveur source, l’application doit avoir été indexée source.

## <a name="source-indexing"></a>Indexation source

Le système d’indexation source est une collection de fichiers exécutables et de scripts Perl. Les scripts perl requièrent Perl 5,6 ou une version ultérieure.

En règle générale, les fichiers binaires sont indexés à la source pendant le processus de génération après la génération de l’application. Les informations requises par le serveur source sont stockées dans les fichiers PDB.

Le serveur source est actuellement fourni avec des scripts qui doivent fonctionner avec les systèmes de contrôle de code source suivants.

-   Team Foundation Server
-   Perforce
-   Visual SourceSafe
-   ÉCHANTILLON
-   Subversion

Vous pouvez également créer un script personnalisé pour indexer votre code pour un autre système de contrôle de code source.

Le tableau suivant répertorie les outils du serveur source.



| Outil        | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
|-------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Srcsrv.ini  | Ce fichier est la liste principale de tous les serveurs de contrôle de code source. Chaque entrée a le format suivant :*MyServer* = *du*<br/> Lors de l’utilisation de Perforce, les informations sur le serveur se composent du chemin d’accès réseau complet au serveur, suivi d’un signe deux-points, suivi du numéro de port qu’il utilise. Par exemple :<br/> MYSERVER = machine. Corp. Company. com : 1666<br/> Ce fichier peut être installé sur l’ordinateur qui exécute le débogueur. Lorsque le serveur source démarre, il recherche des valeurs dans Srcsrv.ini ; ces valeurs remplacent les informations contenues dans le fichier PDB. Cela permet aux utilisateurs de configurer un débogueur pour qu’il utilise un autre serveur de contrôle de code source au moment du débogage.<br/> Pour plus d’informations, consultez l’exemple Srcsrv.ini installé avec les outils du serveur source.<br/> |
| SSINDEX. cmd | Ce script génère la liste des fichiers archivés dans le contrôle de code source, ainsi que les informations de version de chaque fichier. Il stocke un sous-ensemble de ces informations dans les fichiers. pdb générés au moment de la génération de l’application. Le script utilise l’un des modules perl suivants pour l’interface avec le contrôle de code source : P4.pm (Perforce) ou Vss.pm (Visual Source Safe). Pour plus d’informations, exécutez le script avec le- ? ou- ?? (aide détaillée) ou examinez le script.<br/>                                                                                                                                                                                                                                                                                                             |
| Srctool.exe | Cet utilitaire répertorie tous les fichiers indexés dans un fichier. pdb. Pour chaque fichier, il répertorie le chemin d’accès complet, le serveur de contrôle de code source et le numéro de version du fichier. Vous pouvez utiliser ces informations pour récupérer des fichiers sans utiliser le serveur source. Pour plus d’informations, exécutez l’utilitaire avec le/ ? option.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| Pdbstr.exe  | Cet utilitaire est utilisé par les scripts d’indexation pour insérer les informations de contrôle de version dans le flux alternatif « SRCSRV » du fichier. pdb cible. Il peut également lire n’importe quel flux à partir d’un fichier. pdb. Vous pouvez utiliser ces informations pour vérifier que les scripts d’indexation fonctionnent correctement. Pour plus d’informations, exécutez l’utilitaire avec le/ ? option.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                          |



 

## <a name="retrieving-the-source-file"></a>Récupération du fichier source

L’API DbgHelp fournit un accès aux fonctionnalités du serveur source via la fonction [**SymGetSourceFile**](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetsourcefile) . Pour récupérer le nom du fichier source à récupérer, appelez la fonction [**SymEnumSourceFiles**](/windows/desktop/api/DbgHelp/nf-dbghelp-symenumsourcefiles) ou [**SymGetLineFromAddr64**](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetlinefromaddr) .

## <a name="using-source-server-with-a-debugger"></a>Utilisation du serveur source avec un débogueur

Pour utiliser le serveur source avec WinDbg, KD, NTSD ou CDB, vérifiez que vous avez installé une version récente du package outils de débogage pour Windows (version 6,3 ou ultérieure). Ensuite, incluez SRV \* dans la commande. srcpath comme suit :

**\. srcpath SRV \* ;** _c : \\ MySource_

Notez que cet exemple comprend également un chemin d’accès source traditionnel. Si le débogueur ne peut pas récupérer le fichier à partir du serveur source, il recherche le chemin d’accès spécifié.

Si un fichier source est récupéré par le serveur source, il est conservé sur votre disque dur une fois la session de débogage terminée. Les fichiers sources sont stockés localement dans le sous-répertoire SRC du répertoire d’installation des outils de débogage pour Windows.

## <a name="source-server-data-blocks"></a>Blocs de données du serveur source

Le serveur source s’appuie sur deux blocs de données dans le fichier PDB.

-   Liste des fichiers sources. La génération d’un module crée automatiquement une liste de chemins d’accès complets aux fichiers sources utilisés pour générer le module.
-   Bloc de données. L’indexation de la source comme décrit précédemment ajoute un flux de remplacement au fichier PDB nommé « srcsrv ». Le script qui insère ces données dépend du processus de génération spécifique et du système de contrôle de code source en cours d’utilisation.

Dans la spécification de langage version 1, le bloc de données est divisé en trois sections : ini, variables et fichiers sources. Sa syntaxe est la suivante.

``` syntax
SRCSRV: ini ------------------------------------------------ 
VERSION=1
VERCTRL=<source_control_str>
DATETIME=<date_time_str>
SRCSRV: variables ------------------------------------------ 
SRCSRVTRG=%sdtrg% 
SRCSRVCMD=%sdcmd% 
SRCSRVENV=var1=string1\bvar2=string2 
DEPOT=//depot 
SDCMD=sd.exe -p %fnvar%(%var2%) print -o %srcsrvtrg% -q %depot%/%var3%#%var4%
SDTRG=%targ%\%var2%\%fnbksl%(%var3%)\%var4%\%fnfile%(%var1%) 
WIN_SDKTOOLS= sserver.microsoft.com:4444 
SRCSRV: source files --------------------------------------- 
<path1>*<var2>*<var3>*<var4> 
<path2>*<var2>*<var3>*<var4> 
<path3>*<var2>*<var3>*<var4> 
<path4>*<var2>*<var3>*<var4> 
SRCSRV: end ------------------------------------------------
```

Tout le texte est interprété littéralement, à l’exception du texte placé entre les signes de pourcentage (%). Le texte placé entre les signes de pourcentage est traité comme un nom de variable à résoudre de manière récursive, sauf s’il s’agit de l’une des fonctions suivantes :

<dl> <dt>

<span id="_fnvar___"></span><span id="_FNVAR___"></span>%fnvar%()
</dt> <dd>

Le texte du paramètre doit être placé entre des signes de pourcentage et traité comme une variable à développer.

</dd> <dt>

<span id="_fnbksl___"></span><span id="_FNBKSL___"></span>%fnbksl%()
</dt> <dd>

Toutes les barres obliques (/) dans le texte du paramètre doivent être remplacées par des barres obliques inverses ( \\ ).

</dd> <dt>

<span id="_fnfile___"></span><span id="_FNFILE___"></span>%fnfile%()
</dt> <dd>

Toutes les informations de chemin d’accès dans le texte du paramètre doivent être supprimées, en laissant uniquement le nom du fichier.

</dd> </dl>

La section ini contient des variables qui décrivent les exigences. Le script d’indexation peut ajouter n’importe quel nombre de variables à cette section. Voici quelques exemples :

<dl> <dt>

<span id="VERSION"></span><span id="version"></span>Version
</dt> <dd>

Version de la spécification de langage. Cette variable est requise.

</dd> <dt>

<span id="VERCTL"></span><span id="verctl"></span>VERCTL
</dt> <dd>

Chaîne qui décrit le produit de contrôle de code source. Cette variable est facultative.

</dd> <dt>

<span id="DATETIME"></span><span id="datetime"></span>Date/heure
</dt> <dd>

Chaîne qui indique la date et l’heure de traitement du fichier PDB. Cette variable est facultative.

</dd> </dl>

La section variables contient des variables qui décrivent comment extraire un fichier du contrôle de code source. Il peut également être utilisé pour définir des variables de texte couramment utilisées en tant que variables afin de réduire la taille du bloc de données.

<dl> <dt>

<span id="SRCSRVTRG"></span><span id="srcsrvtrg"></span>SRCSRVTRG
</dt> <dd>

Décrit comment générer le chemin d’accès cible pour le fichier extrait. Il s’agit d’une variable obligatoire.

</dd> <dt>

<span id="SRCSRVCMD"></span><span id="srcsrvcmd"></span>SRCSRVCMD
</dt> <dd>

Décrit comment générer la commande pour extraire le fichier du contrôle de code source. Cela comprend le nom du fichier exécutable et ses paramètres de ligne de commande. Il s’agit d’une variable obligatoire.

</dd> <dt>

<span id="SRCSRVENV"></span><span id="srcsrvenv"></span>SRCSRVENV
</dt> <dd>

Chaîne qui répertorie les variables d’environnement à créer lors de l’extraction de fichier. Séparez plusieurs entrées par un caractère de retour arrière ( \\ b). Il s’agit d’une variable facultative.

</dd> </dl>

La section fichiers sources contient une entrée pour chaque fichier source qui a été indexé. Le contenu de chaque ligne est interprété comme une variable avec les noms VAR1, VAR2, VAR3, et ainsi de suite jusqu’à VAR10. Les variables sont séparées par des astérisques. VAR1 doit spécifier le chemin d’accès complet au fichier source, comme indiqué ailleurs dans le fichier PDB. Par exemple, la ligne suivante :

``` syntax
c:\proj\src\file.cpp*TOOLS_PRJ*tools/mytool/src/file.cpp*3
```

est interprété comme suit :

``` syntax
VAR1=c:\proj\src\file.cpp
VAR2=TOOLS_PRJ
VAR3=tools/mytool/src/file.cpp
VAR4=3
```

Dans cet exemple, VAR4 est un numéro de version. Toutefois, la plupart des systèmes de contrôle de code source prennent en charge l’étiquetage des fichiers de sorte que l’état source d’une build donnée puisse être restauré. Par conséquent, vous pouvez également utiliser l’étiquette pour la Build. L’exemple de bloc de données peut être modifié pour contenir une variable telle que la suivante :

``` syntax
LABEL=BUILD47
```

Ensuite, en supposant que le système de contrôle de code source utilise l’arobase (@) pour indiquer une étiquette, vous pouvez modifier la variable SRCSRVCMD comme suit :

**sd.exe-p% fnvar%(% Var2%) imprimer-o% srcsrvtrg%-q% Depot%/%var3% @% label%**

## <a name="how-source-server-works"></a>Fonctionnement du serveur source

Le client du serveur source est implémenté dans Symsrv.dll. Le client n’extrait pas les informations directement à partir du fichier PDB ; elle utilise un gestionnaire de symboles comme celui implémenté dans Dbghelp.dll. Il s’agit essentiellement d’un moteur de substitution de variables récursives qui crée une ligne de commande qui peut être utilisée pour extraire le fichier source approprié du système de contrôle de code source. Votre code ne doit pas appeler Symsrv.dll directement. Pour intégrer ses fonctionnalités à votre application, utilisez la fonction [**SymGetSourceFile**](/windows/desktop/api/Dbghelp/nf-dbghelp-symgetsourcefile) .

La première version du serveur source fonctionne comme suit. Ce comportement peut changer dans les versions ultérieures.

-   Le client appelle la fonction **SrcSrvInit** avec le chemin d’accès cible à utiliser comme base pour toutes les extractions de fichiers sources. Elle stocke ce chemin d’accès dans la variable ENSION.
-   Le client extrait le flux SRCSRV du fichier PDB lorsque le PDB du module est chargé et appelle la fonction **SrcSrvLoadModule** pour passer le bloc de données au serveur source.
-   Lorsque dbghelp récupère un fichier source, le client appelle la fonction **SrcSrvGetFile** pour récupérer les fichiers sources à partir du contrôle de code source.
-   Le serveur source recherche dans le bloc de données les entrées de fichier source pour une entrée qui correspond au fichier demandé. Il remplit VAR1 en VAR *n* avec le contenu de l’entrée du fichier source. Ensuite, il étend la variable SRCSRVTRG en utilisant VAR1 à VAR *n*. Si le fichier se trouve déjà à cet emplacement, il retourne l’emplacement à l’appelant. Dans le cas contraire, il développe la variable SRCSRVCMD pour générer la commande nécessaire pour récupérer le fichier du contrôle de code source et le copier à l’emplacement cible. Enfin, elle exécute cette commande.

## <a name="creating-a-source-control-provider-module"></a>Création d’un module fournisseur de contrôle de code source

Le serveur source comprend des modules de fournisseur pour Perforce (p4.pm) et Visual Source Safe (vss.pm). Pour créer votre propre module de fournisseur, vous devez implémenter l’ensemble d’interfaces suivant.

<dl> <dt>

<span id="_module__SimpleUsage__"></span><span id="_module__simpleusage__"></span><span id="_MODULE__SIMPLEUSAGE__"></span>**$module :: SimpleUsage ()**
</dt> <dd>

Objectif : affiche des informations d’utilisation de module simples dans STDOUT.

Paramètres : aucun

Valeur de retour : aucune

</dd> <dt>

<span id="_module__VerboseUsage__"></span><span id="_module__verboseusage__"></span><span id="_MODULE__VERBOSEUSAGE__"></span>**$module :: VerboseUsage ()**
</dt> <dd>

Objectif : affiche des informations d’utilisation de module approfondies dans STDOUT.

Paramètres : aucun

Valeur de retour : aucune

</dd> <dt>

<span id="_objref____module__new__CommandArguments_"></span><span id="_objref____module__new__commandarguments_"></span><span id="_OBJREF____MODULE__NEW__COMMANDARGUMENTS_"></span>**$objref = $module :: New ( \@ CommandArguments)**
</dt> <dd>

Objectif : Initialise une instance du module fournisseur.

Parameters : tous les @ARGV arguments qui n’ont pas été reconnus par SSIndex. cmd comme des arguments généraux.

Valeur de retour : référence qui peut être utilisée dans les opérations ultérieures.

</dd> <dt>

<span id="_objref-_GatherFileInformation__SourcePath___ServerHashReference_"></span><span id="_objref-_gatherfileinformation__sourcepath___serverhashreference_"></span><span id="_OBJREF-_GATHERFILEINFORMATION__SOURCEPATH___SERVERHASHREFERENCE_"></span>**$objref->GatherFileInformation ($SourcePath, $ServerHashReference)**
</dt> <dd>

Objectif : permet au module de collecter les informations d’indexation source requises pour le répertoire spécifié par le paramètre $SourcePath. Le module ne doit pas supposer que cette entrée sera appelée une seule fois pour chaque instance d’objet, car SSIndex. cmd peut l’appeler plusieurs fois pour différents chemins d’accès.

Paramètres : (1) répertoire local contenant la source à indexer. (2) référence à un hachage contenant toutes les entrées du fichier de Srcsrv.ini spécifié.

Valeur de retour : aucune

</dd> <dt>

<span id="__VariableHashReference___FileEntry_____objref-_GetFileInfo__LocalFile_"></span><span id="__variablehashreference___fileentry_____objref-_getfileinfo__localfile_"></span><span id="__VARIABLEHASHREFERENCE___FILEENTRY_____OBJREF-_GETFILEINFO__LOCALFILE_"></span>**($VariableHashReference, $FileEntry) = $objref->GetFileInfo ($LocalFile)**
</dt> <dd>

Objectif : fournit les informations nécessaires pour extraire un seul fichier spécifique du système de contrôle de code source.

Paramètres : nom de fichier complet

Valeur de retour : (1) référence de hachage des variables nécessaires à l’interprétation de la $FileEntry retournée. SSIndex. cmd met en cache ces variables pour chaque fichier source utilisé par un fichier de débogage unique pour réduire la quantité d’informations écrites dans le flux d’index source. (2) entrée de fichier à écrire dans le flux d’index source pour permettre SrcSrv.dll d’extraire ce fichier du contrôle de code source. Le format exact de cette ligne est spécifique au système de contrôle de code source.

</dd> <dt>

<span id="_TextString____objref-_LongName__"></span><span id="_textstring____objref-_longname__"></span><span id="_TEXTSTRING____OBJREF-_LONGNAME__"></span>**$TextString = $objref->LongName ()**
</dt> <dd>

Objectif : fournit une chaîne descriptive permettant d’identifier le fournisseur de contrôle de code source pour l’utilisateur final.

Paramètres : aucun

Valeur de retour : nom descriptif du système de contrôle de code source.

</dd> <dt>

<span id="_StreamVariableLines____objref-_SourceStreamVariables__"></span><span id="_streamvariablelines____objref-_sourcestreamvariables__"></span><span id="_STREAMVARIABLELINES____OBJREF-_SOURCESTREAMVARIABLES__"></span>**@StreamVariableLines = $objref->SourceStreamVariables ()**
</dt> <dd>

Objectif : permet au fournisseur de contrôle de code source d’ajouter des variables spécifiques au contrôle de code source dans le flux source pour chaque fichier de débogage. Les exemples de modules utilisent cette méthode pour écrire les \_ variables cibles Extract cmd et extract \_ .

Paramètres : aucun

Valeur de retour : liste des entrées pour les variables de flux source.

</dd> </dl>

 

 




