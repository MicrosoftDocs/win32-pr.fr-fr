---
description: Cette rubrique est une référence pour les entrées qui peuvent être utilisées dans un fichier autorun. inf. Une entrée se compose d’une clé et d’une valeur.
ms.assetid: 5b8fd559-b1be-4552-a7be-19ad107855af
title: Entrées autorun. inf
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 221e0a99e6352b5cfe50f3c3c0c2939933ff6c6f862e1a03b54127968b9c1838
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119937159"
---
# <a name="autoruninf-entries"></a>Entrées autorun. inf

Cette rubrique est une référence pour les entrées qui peuvent être utilisées dans un fichier autorun. inf. Une entrée se compose d’une clé et d’une valeur.

-   [\[Clés d’exécution automatique \]](#autorun-keys)
    -   [action](#parameters)
    -   [CustomEvent](#customevent)
    -   [Icône](#parameters)
    -   [label](#parameters)
    -   [open](#parameters)
    -   [UseAutoPlay](#parameters)
    -   [ShellExecute](#shellexecute)
    -   [Shell](#autoruninf-entries)
    -   [verbe de Shell \\](#shellverb)
-   [\[Clés de contenu \]](#content-keys)
-   [\[\]Clés ExclusiveContentPaths](#exclusivecontentpaths-keys)
-   [\[\]Clés IgnoreContentPaths](#ignorecontentpaths-keys)
-   [\[\]Clés DeviceInstall](#deviceinstall-keys)
    -   [DriverPath](#driverpath)

## <a name="autorun-keys"></a>\[Clés d’exécution automatique \]

-   [action](#parameters)
-   [CustomEvent](#customevent)
-   [Icône](#parameters)
-   [label](#parameters)
-   [open](#parameters)
-   [UseAutoPlay](#parameters)
-   [ShellExecute](#shellexecute)
-   [Shell](#autoruninf-entries)
-   [verbe de Shell \\](#shellverb)

### <a name="action"></a>action

L’entrée **action** spécifie le texte utilisé dans la boîte de dialogue d’exécution automatique pour le gestionnaire représentant le programme spécifié dans l’entrée [Open](#parameters) ou [ShellExecute](#shellexecute) du fichier autorun. inf du média. La valeur peut être exprimée sous forme de texte ou de ressource stockée dans un fichier binaire.


```
action=ActionText
```




```
action=@[filepath\]filename,-resourceID
```



### <a name="parameters"></a>Paramètres

-   *ActionText*

    Texte utilisé dans la boîte de dialogue d’exécution automatique pour le gestionnaire représentant le programme spécifié dans l’entrée [Open](#parameters) ou [ShellExecute](#shellexecute) du fichier autorun. inf du média.

-   *cheminfichier*

    Chaîne qui contient le chemin d’accès complet du répertoire qui contient le fichier binaire contenant la chaîne. Si aucun chemin d’accès n’est spécifié, le fichier doit se trouver dans le répertoire racine du lecteur.

-   *extension*

    Chaîne qui contient le nom du fichier binaire.

-   *IDRessource*

    ID de la chaîne dans le fichier binaire.

### <a name="remarks"></a>Remarques

la clé d' **action** est utilisée uniquement dans Windows XP Service Pack 2 (SP2) ou version ultérieure. Il est uniquement pris en charge pour les lecteurs de type lecteur \_ amovible et lecteur \_ fixe. Dans le cas d’un disque \_ amovible, la clé d' **action** est requise. une commande d' **action** dans le fichier Autorun. inf d’un CD audio ou d’un DVD de film est ignorée, et ces médias continuent de se comporter comme dans Windows XP Service Pack 1 (SP1) et versions antérieures.

La chaîne affichée dans la boîte de dialogue d’exécution automatique est construite en combinant le texte spécifié dans l’entrée d' **action** avec le texte codé en dur du fournisseur, fourni par l’interpréteur de commandes. L' [icône](#parameters) s’affiche en regard de celle-ci. Cette entrée apparaît toujours comme première option dans la boîte de dialogue d’exécution automatique et est sélectionnée par défaut. Si l’utilisateur accepte l’option, l’application spécifiée par l’entrée [Open](#parameters) ou [ShellExecute](#shellexecute) dans le fichier autorun. inf du média est lancée. L’option **toujours effectuer l’action sélectionnée** n’est pas disponible dans cette situation.

Les touches [action](#parameters) et [icône](#parameters) définissent ensemble la représentation de l’application qui est visible par l’utilisateur final dans la boîte de dialogue d’exécution automatique. Ils doivent être composés de manière à ce que les utilisateurs puissent facilement les identifier. Ils doivent indiquer l’application à exécuter, la société qui l’a créée et toute marque associée.

Pour la compatibilité descendante, l’entrée d' **action** est facultative pour les appareils de type Drive \_ fixed. Pour ce type, une entrée par défaut est utilisée dans la boîte de dialogue d’exécution automatique si aucune entrée d' **action** n’est présente dans le fichier autorun. inf.

L’entrée d' **action** est obligatoire pour les appareils de type lecteur \_ amovible, qui jusqu’à présent ne disposent pas de la prise en charge de autorun. inf. Si aucune entrée d' **action** n’est présente, la boîte de dialogue d’exécution automatique s’affiche, mais sans option pour lancer le contenu supplémentaire.

### <a name="customevent"></a>CustomEvent

L’entrée **CustomEvent** spécifie un événement de contenu de lecture automatique personnalisé.


```
CustomEvent=CustomEventName
```



### <a name="parameters"></a>Paramètres

-   *CustomEventName*

    Chaîne de texte contenant le nom de l’événement de contenu de lecture automatique. Le nom ne doit pas comporter plus de 100 caractères alphanumériques.

### <a name="remarks"></a>Remarques

Vous pouvez inclure un nom d’événement personnalisé dans le fichier autorun. inf d’un volume. Lorsque l’exécution automatique invite l’utilisateur à utiliser une application avec le volume, il affiche uniquement les applications qui ont été inscrites pour le nom d’événement personnalisé spécifié. Pour plus d’informations sur la façon dont vous pouvez inscrire une application en tant que gestionnaire pour votre événement de contenu de lecture automatique personnalisé, consultez [lancement automatique avec exécution](/previous-versions/windows/apps/hh452731(v=win.10)) automatique ou [inscription d’un gestionnaire d’événements](how-to-register-an-event-handler.md).

L’exemple suivant spécifie la valeur « MyContentOnArrival » comme nouvel événement de contenu de lecture automatique.


```
CustomEvent=MyContentOnArrival
```



### <a name="icon"></a>icon

l’entrée d' **icône** spécifie une icône qui représente le lecteur avec activation automatique dans l’interface utilisateur Windows.


```
icon=iconfilename[,index]
```



### <a name="parameters"></a>Paramètres

-   *argument*

    Nom d’un fichier. ico, .bmp, .exe ou .dll contenant les informations sur l’icône. Si un fichier contient plusieurs icônes, vous devez également spécifier un index de base zéro de l’icône.

### <a name="remarks"></a>Remarques

l’icône, ainsi que l’étiquette, représente le lecteur compatible avec la fonction AutoRun dans l’interface utilisateur Windows. par exemple, dans l’explorateur de Windows, le lecteur est représenté par cette icône au lieu de l’icône de lecteur standard. Le fichier de l’icône doit se trouver dans le même répertoire que le fichier spécifié par la commande [ouvrir](#parameters) .

L’exemple suivant spécifie la deuxième icône dans le fichier MyProg.exe.


```
icon=MyProg.exe,1
```



### <a name="label"></a>label

l’entrée d' **étiquette** spécifie une étiquette de texte qui représente le lecteur avec activation automatique dans l’interface utilisateur Windows.


```
label=LabelText
```



### <a name="parameters"></a>Paramètres

-   *LabelText*

    Chaîne de texte contenant l’étiquette. Il peut contenir des espaces et ne doit pas dépasser 32 caractères.

> [!Note]  
> Il est possible de placer une valeur dans le paramètre **LabelText** qui dépasse 32 caractères et de ne pas recevoir de message d’erreur. Toutefois, le système affiche uniquement les 32 premiers caractères. Les caractères qui suivent le 32e sont tronqués et ne s’affichent pas. Par exemple, si le **LabelText** est le suivant : label = « ce CD est conçu pour être le CD de musique ultime ». les éléments suivants s’affichent : « ce CD est conçu pour être le UL ».

 

### <a name="remarks"></a>Remarques

l’étiquette, ainsi qu’une icône, représente le lecteur prenant en charge l’exécution automatique dans l’interface utilisateur Windows.

L’exemple suivant spécifie la valeur « mon étiquette de lecteur » comme étiquette du lecteur.


```
label=My Drive Label
```



### <a name="open"></a>ouvert

L’entrée **ouverte** spécifie le chemin d’accès et le nom de fichier de l’application que l’exécution automatique lance lorsqu’un utilisateur insère un disque dans le lecteur.


```
open=[exepath\]exefile [param1 [param2] ...] 
```



### <a name="parameters"></a>Paramètres

-   *exefile*

    Chemin complet d’un fichier exécutable qui s’exécute lors de l’insertion du CD. Si seul un nom de fichier est spécifié, il doit se trouver dans le répertoire racine du lecteur. Pour rechercher le fichier dans un sous-répertoire, vous devez spécifier un chemin d’accès. Vous pouvez également inclure un ou plusieurs paramètres de ligne de commande à passer à l’application de démarrage.

### <a name="useautoplay"></a>UseAutoPlay

sur Windows XP, l’entrée **UseAutoPlay** spécifie que l’exécution automatique doit être utilisée à la place de l’exécution automatique.

sur Windows Vista et versions ultérieures, cette entrée entraîne la suppression des actions spécifiées pour l’exécution automatique (à l’aide des entrées **open** ou **shellexecute** ) à partir de la boîte de dialogue d’exécution automatique. cette entrée n’a aucun effet sur les versions de Windows antérieures à Windows XP.

sur Windows 8 et versions ultérieures, la spécification de la valeur 0 désactive l’exécution automatique pour cet appareil.

### <a name="parameters"></a>Paramètres

Pour utiliser cette option, ajoutez une entrée pour **UseAutoPlay** au fichier autorun. inf et affectez à l’entrée la valeur 1. aucune autre valeur n’est prise en charge sur les versions de Windows antérieures à Windows 8.

sur Windows 8 et versions ultérieures, spécifiez la valeur 0 pour désactiver l’exécution automatique pour cet appareil.


```
UseAutoPlay=1
```



### <a name="remarks"></a>Remarques

actuellement, **UseAutoPlay** est applicable uniquement sur Windows XP ou version ultérieure et uniquement sur un lecteur que [**GetDriveType**](/windows/win32/api/fileapi/nf-fileapi-getdrivetypea) détermine comme étant du type **lecteur \_ CDROM**.

lorsque **UseAutoPlay** est utilisé, toute action spécifiée par les entrées **open** ou **shellexecute** dans Autorun. inf est ignorée sur Windows XP et omise de la boîte de dialogue d’exécution automatique sur Windows Vista.

AutoRun est généralement utilisé pour exécuter ou charger automatiquement un contenu sur le média inséré, tandis que la lecture automatique présente une boîte de dialogue qui comprend une liste des actions pertinentes qui peuvent être exécutées et permet à l’utilisateur de choisir l’action à entreprendre. Pour plus d’informations sur la différence entre l’exécution automatique et l’exécution automatique, consultez [création d’une application de CD-ROM compatible avec l’exécution automatique](autoplay.md) et [utilisation et configuration de l’exécution automatique](autoplay2k-using.md), respectivement.

### <a name="usage-example"></a>Exemple d'utilisation

un CD contient trois fichiers : Autorun. inf, Readme.txt et Musique. wma. selon la version de Windows en cours d’utilisation et les options spécifiées dans Autorun. inf, le cd peut être géré par l’exécution automatique ou l’exécution automatique lorsqu’il est inséré (en supposant que l’exécution automatique/exécution automatique est activée pour le lecteur dans lequel le CD est inséré).

Tout d’abord, envisagez d’utiliser un fichier autorun. inf avec le contenu suivant, en notant que **UseAutoPlay = 1** n’est pas spécifié :


```
[AutoRun]
shellexecute="Readme.txt"
```



l’action effectuée par l’interpréteur de commandes lorsque ce CD est inséré dépend de la version de Windows en cours d’utilisation :

-   sur Windows XP ou version antérieure, ce CD est géré par l’exécution automatique lorsqu’il est inséré. Dans ce cas, l’entrée **ShellExecute** est lue et l’interpréteur de commandes appelle le gestionnaire de fichiers associé à .txt fichiers ; en général, cela ouvre Readme.txt dans Bloc-notes.
-   sur Windows Vista, la présence d’un fichier Autorun. inf avec une entrée **shellexecute** entraîne l’identification du support en tant que type d’exécution automatique « logiciels et jeux ». Dans ce cas, l’utilisateur reçoit une boîte de dialogue d’exécution automatique qui comprend l’action spécifiée par l’entrée **ShellExecute** (présentée sous la forme « charger Readme.txt » dans la boîte de dialogue), ainsi que les actions par défaut associées aux médias de type « logiciels et jeux ».

pour indiquer que l’exécution automatique doit être utilisée au lieu de l’exécution automatique sur Windows XP, et que l’action spécifiée par l’entrée shellexecute d’autorun doit être supprimée de la boîte de dialogue d’exécution automatique sur Windows Vista, insérez **UseAutoPlay** dans le fichier autorun. inf comme suit :


```
[AutoRun]
shellexecute="Readme.txt"
UseAutoPlay=1
```



là encore, l’action effectuée par l’interpréteur de commandes lorsque ce CD est inséré dépend de la version de Windows en cours d’utilisation.

-   dans les versions de Windows antérieures à Windows XP, l’exécution automatique est toujours utilisée et l’action spécifiée par **shellexecute** est effectuée, comme décrit précédemment. (notez que seule l’exécution automatique est disponible sur les versions de Windows antérieures à Windows XP.)
-   sur Windows XP, l’entrée **UseAutoPlay** provoque l’utilisation de la lecture automatique à la place de l’exécution automatique. dans ce cas, l’exécution automatique détermine que le média contient un fichier Windows Media Audio (. wma) et classe le contenu comme « fichiers Musique ». l’utilisateur reçoit une boîte de dialogue d’exécution automatique contenant des gestionnaires inscrits pour le type de média lecture automatique « fichiers Musiques ». l’entrée ShellExecute d’AutoRun est ignorée.

### <a name="shellexecute"></a>ShellExecute

[Version 5,0.](versions.md) L’entrée **ShellExecute** spécifie un fichier d’application ou de données que l’exécution automatique utilisera pour appeler [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa).


```
shellexecute=[filepath\]filename[param1, [param2]...] 
```



### <a name="parameters"></a>Paramètres

-   *cheminfichier*

    Chaîne qui contient le chemin d’accès complet du répertoire qui contient les données ou le fichier exécutable. Si aucun chemin d’accès n’est spécifié, le fichier doit se trouver dans le répertoire racine du lecteur.

-   *extension*

    Chaîne qui contient le nom du fichier. S’il s’agit d’un fichier exécutable, il est lancé. S’il s’agit d’un fichier de données, il doit être membre d’un [type de fichier](fa-file-types.md). [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa) lance la commande par défaut associée au type de fichier.

-   *paramx*

    Contient tous les paramètres supplémentaires qui doivent être passés à [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa).

### <a name="remarks"></a>Remarques

Cette entrée est semblable à [Open](#parameters), mais elle vous permet d’utiliser les informations d' [Association de fichiers](fa-intro.md) pour exécuter l’application.

### <a name="shell"></a>shell

L’entrée **Shell** spécifie une commande par défaut pour le menu contextuel du lecteur.


```
shell=verb
```



### <a name="parameters"></a>Paramètres

-   *verbe*

    Verbe qui correspond à la commande de menu. Le verbe et sa commande de menu associée doivent être définis dans le fichier autorun. inf avec une entrée de [ \\ verbe de Shell](#shellverb) .

### <a name="remarks"></a>Remarques

Quand un utilisateur clique avec le bouton droit sur l’icône du lecteur, un menu contextuel s’affiche. Si un fichier autorun. inf est présent, la commande de menu contextuel par défaut est extraite de celui-ci. Cette commande s’exécute également lorsque l’utilisateur double-clique sur l’icône du lecteur.

Pour spécifier la commande de menu contextuel par défaut, commencez par définir son verbe, sa chaîne de commande et son texte de menu avec le [ \\ verbe de Shell](#shellverb). Utilisez ensuite l’interpréteur de commandes pour en faire la commande de menu contextuel par défaut. Dans le cas contraire, le texte de l’élément de menu par défaut sera « AutoPlay », ce qui lance l’application spécifiée par l’entrée [ouverte](#parameters) .

### <a name="shellverb"></a>verbe de Shell \\

L’entrée de **\\ verbe de l’interpréteur** de commandes ajoute une commande personnalisée au menu contextuel du lecteur.


```
shell\verb\command=Filename.exe 
shell\verb=MenuText
```



### <a name="parameters"></a>Paramètres

-   *verbe*

    Verbe de la commande de menu. L’entrée de *_\\ commande_* de _verbe_ de **Shell \\** associe le verbe à un fichier exécutable. Les verbes ne doivent pas contenir d’espaces incorporés. Par défaut, le *verbe* est le texte affiché dans le menu contextuel.

-   *Filename.exe*

    Chemin d’accès et nom de fichier de l’application qui exécute l’action.

-   *MenuText*

    Ce paramètre spécifie le texte affiché dans le menu contextuel. Si elle est omise, le *verbe* est affiché. *MenuText* peut être à casse mixte et peut contenir des espaces. Vous pouvez définir une touche de raccourci pour l’élément de menu en plaçant une esperluette (&) devant la lettre.

### <a name="remarks"></a>Remarques

Quand un utilisateur clique avec le bouton droit sur l’icône du lecteur, un menu contextuel s’affiche. L’ajout d’entrées de **\\ verbe de Shell** au fichier autorun. inf du lecteur vous permet d’ajouter des commandes à ce menu contextuel.

Cette entrée comporte deux parties, qui doivent se trouver sur des lignes distinctes. La première partie est la commande de _verbe_ de l' **\\ interpréteur** de *_\\ commandes_*. Elle est obligatoire. Elle associe une chaîne, appelée *verbe*, à l’application à lancer lors de l’exécution de la commande. La deuxième partie est l’entrée de _verbe_ de l' **interpréteur \\** de commandes. Ce nom est facultatif. Vous pouvez l’inclure pour spécifier le texte qui s’affiche dans le menu contextuel.

Pour spécifier une commande de menu contextuel par défaut, définissez le verbe avec le **\\ verbe de Shell** et définissez-le comme commande par défaut avec l’entrée de [Shell](#autoruninf-entries) .

l’exemple de fragment Autorun. inf suivant associe le verbe *readinesst* à la chaîne de commande « Bloc-notes abc \\readme.txt ». Le texte de menu est « read me », et « m » est défini comme touche de raccourci de l’élément. lorsque l’utilisateur sélectionne cette commande, le fichier abcreadme.txt du lecteur \\ s’ouvre avec Microsoft Bloc-notes.


```
shell\readit\command=notepad abc\readme.txt 
shell\readit=Read &Me
```



## <a name="content-keys"></a>\[Clés de contenu \]

Il existe trois clés de type de fichier : **MusicFiles**, **PictureFiles** et **VideoFiles**.

Si l’un de ces contenus a la valeur true par le biais des valeurs non sensibles à la casse 1, y, Yes, t ou true, l’interface utilisateur de la lecture automatique affiche les gestionnaires associés à ce type de contenu, que le contenu de ce type existe ou non sur le média.

Si l’un de ces contenus est défini sur false par le biais des valeurs non sensibles à la casse 0, n, no, f ou false, l’interface utilisateur de l’exécution automatique n’affiche pas les gestionnaires associés à ce type de contenu, même si le contenu de ce type est détecté sur le média.

L’utilisation de cette section a pour but d’autoriser les créateurs de contenu à communiquer l’intention du contenu à la lecture automatique. Par exemple, un CD peut être classé comme contenant uniquement du contenu musical, même s’il contient également des images et des vidéos et qu’il aurait été considéré comme ayant un contenu mixte.

la section **\[ contenu \]** est uniquement prise en charge sous Windows Vista et versions ultérieures.


```
[Content]
MusicFiles=Y
PictureFiles=0
VideoFiles=false
```



## <a name="exclusivecontentpaths-keys"></a>\[\]Clés ExclusiveContentPaths

Les dossiers listés dans cette section limitent la lecture automatique à la recherche de contenu dans uniquement les dossiers et les sous-dossiers. Ils peuvent être fournis avec ou sans barre oblique inverse de début ( \\ ). Dans les deux cas, ils sont considérés comme des chemins absolus à partir du répertoire racine du média. Dans le cas de dossiers dont le nom comporte des espaces, ne les placez pas entre guillemets, car les guillemets sont pris littéralement dans le chemin d’accès.

L’utilisation de cette section a pour but de permettre aux auteurs de contenu de communiquer l’intention du contenu à la lecture automatique et de raccourcir le temps d’analyse en limitant l’analyse à certaines zones significatives du média.

Les chemins d’accès valides sont les suivants :


```
[ExclusiveContentPaths]
\music
\music\more music
music2
```



la section **\[ ExclusiveContentPaths \]** est uniquement prise en charge sous Windows Vista et versions ultérieures.

## <a name="ignorecontentpaths-keys"></a>\[\]Clés IgnoreContentPaths

Les dossiers répertoriés dans cette section et leurs sous-dossiers sont ignorés par l’exécution automatique lors de la recherche de contenu dans un média. Ils peuvent être fournis avec ou sans barre oblique inverse de début ( \\ ). Dans les deux cas, ils sont considérés comme des chemins absolus à partir du répertoire racine du média. Dans le cas de dossiers dont le nom comporte des espaces, ne les placez pas entre guillemets, car les guillemets sont pris littéralement dans le chemin d’accès.

Les chemins d’accès de cette section sont prioritaires sur les chemins d’accès dans la section **\[ ExclusiveContentPaths \]** . Si un chemin d’accès donné dans **\[ IgnoreContentPaths \]** est un sous-dossier d’un chemin d’accès donné dans **\[ ExclusiveContentPaths \]**, il est toujours ignoré.

L’utilisation de cette section a pour but de permettre aux auteurs de contenu de communiquer l’intention du contenu à la lecture automatique et de raccourcir le temps d’analyse en limitant l’analyse à certaines zones significatives du média.

Les chemins d’accès valides sont les suivants :


```
[IgnoreContentPaths]
\music
\music\more music
music2
```



la section **\[ IgnoreContentPaths \]** est uniquement prise en charge sous Windows Vista et versions ultérieures.

## <a name="deviceinstall-keys"></a>\[\]Clés DeviceInstall

### <a name="driverpath"></a>DriverPath

L’entrée **DriverPath** spécifie un répertoire à rechercher de manière récursive pour les fichiers de pilote. Cette commande est utilisée lors de l’installation d’un pilote et ne fait pas partie d’une opération d’exécution automatique. la section **\[ DeviceInstall \]** est uniquement prise en charge sous Windows XP.


```
[DeviceInstall]
DriverPath=directorypath
```



### <a name="parameters"></a>Paramètres

-   *DirectoryPath*

    chemin d’accès à un répertoire qui Windows recherche des fichiers de pilote, ainsi que tous ses sous-répertoires.

### <a name="remarks"></a>Remarques

N’utilisez pas de lettres de lecteur dans *DirectoryPath* , car elles sont modifiées d’un ordinateur à l’autre.

Pour effectuer une recherche dans plusieurs répertoires, ajoutez une entrée **DriverPath** pour chaque répertoire, comme dans cet exemple.


```
[DeviceInstall]
DriverPath=drivers\video 
DriverPath=drivers\audio
```



Si aucune entrée **DriverPath** n’est fournie dans la section **\[ \] DeviceInstall** ou si l’entrée **DriverPath** n’a pas de valeur, ce lecteur est ignoré lors d’une recherche de fichiers de pilote.

 

 
