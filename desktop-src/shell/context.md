---
description: Le fait de cliquer avec le bouton droit sur un objet entraîne normalement l’affichage d’un menu contextuel. Ce menu contient une liste de commandes que l’utilisateur peut sélectionner pour effectuer diverses actions sur l’objet. Cette section est une présentation des menus contextuels pour les objets de système de fichiers.
ms.assetid: d951d1e8-0f88-49c4-8373-e6db0e18cd72
title: Extension des menus contextuels
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d046805ebc787f5cad2bfaa40538c51b826c3f0541f3ec1afad508202a4a25fc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118460646"
---
# <a name="extending-shortcut-menus"></a>Extension des menus contextuels

Le fait de cliquer avec le bouton droit sur un objet entraîne normalement l’affichage d’un *menu contextuel*. Ce menu contient une liste de commandes que l’utilisateur peut sélectionner pour effectuer diverses actions sur l’objet. Cette section est une présentation des menus contextuels pour les objets de système de fichiers.

-   [Menus contextuels pour les objets de système de fichiers](#shortcut-menus-for-file-system-objects)
-   [Verbes de menu contextuel](#shortcut-menu-verbs)
    -   [Verbes canoniques](#canonical-verbs)
    -   [Verbes étendus](#extended-verbs)
-   [Extension du menu contextuel d’un type de fichier](#extending-the-shortcut-menu-for-a-file-type)
-   [Extension du menu contextuel pour les objets Shell prédéfinis](#extending-the-shortcut-menu-for-predefined-shell-objects)
-   [Inscription d’une application pour gérer des types de fichiers arbitraires](#registering-an-application-to-handle-arbitrary-file-types)
-   [Extension du nouveau sous-menu](#extending-the-new-submenu)

Des informations supplémentaires sont disponibles ici :

-   [Comment définir des verbes étendus](how-to-define-extended-verbs.md)
-   [Comment associer des verbes à des commandes DDE](how-to-associate-verbs-with-dde-commands.md)

## <a name="shortcut-menus-for-file-system-objects"></a>Menus contextuels pour les objets de système de fichiers

quand un utilisateur clique avec le bouton droit sur un objet, tel qu’un fichier, qui est affiché dans Windows Explorer ou sur le bureau, un menu contextuel s’affiche avec une liste de commandes. L’utilisateur peut ensuite exécuter une action sur le fichier, par exemple l’ouvrir ou le supprimer, en sélectionnant la commande appropriée.

Comme les menus contextuels sont souvent utilisés pour la gestion des fichiers, l’interpréteur de commandes fournit un ensemble de commandes par défaut, telles que couper et copier, qui apparaissent dans le menu contextuel de n’importe quel fichier. Notez que même si Open with est une commande par défaut, il n’est pas affiché pour certains types de fichiers standard, tels que. wav. L’illustration suivante de l’exemple de répertoire My documents, également utilisé comme exemple dans personnalisation des [icônes](icon.md), affiche un menu contextuel par défaut qui s’affichait en cliquant avec le bouton droit sur MyDocs4.xyz.

![capture d’écran du menu contextuel par défaut pour les objets du système de fichiers](images/context1.jpg)

La raison pour laquelle MyDocs4.xyz affiche un menu contextuel par défaut est qu’il n’est pas membre d’un [type de fichier](fa-file-types.md)inscrit. En revanche, .txt est un type de fichier inscrit. Si vous cliquez avec le bouton droit sur l’un des fichiers de .txt, vous verrez à la place un menu contextuel avec deux commandes supplémentaires dans sa section supérieure : **ouvrir** et **Imprimer**.

![capture d’écran du menu contextuel personnalisé pour les objets du système de fichiers](images/context2.jpg)

Une fois qu’un type de fichier est inscrit, vous pouvez étendre son menu contextuel avec des commandes supplémentaires. Ils s’affichent au-dessus des commandes par défaut lorsqu’un utilisateur clique avec le bouton droit sur un fichier de ce type. Bien que la plupart des commandes ajoutées de cette manière soient courantes, telles que **Print** ou **Open**, vous êtes libre d’ajouter les commandes qu’un utilisateur peut trouver utiles.

Tout ce qui est nécessaire pour étendre le menu contextuel d’un type de fichier consiste à créer une entrée de Registre pour chaque commande. Une approche plus sophistiquée consiste à implémenter un *Gestionnaire de menu contextuel*, qui vous permet d’étendre le menu contextuel pour un type de fichier fichier par fichier. Pour plus d’informations, consultez [création de gestionnaires de menus contextuels](context-menu-handlers.md).

## <a name="shortcut-menu-verbs"></a>Verbes de menu contextuel

Chaque commande du menu contextuel est identifiée dans le registre par son *verbe*. Ces verbes sont les mêmes que ceux utilisés par [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa) lors du lancement d’applications par programme. Pour plus d’informations sur l’utilisation de **ShellExecuteEx**, consultez la discussion dans [lancement d’applications](launch.md).

Un verbe est une chaîne de texte simple qui est utilisée par l’interpréteur de commandes pour identifier la commande associée. Chaque verbe correspond à la *chaîne de commande* utilisée pour lancer la commande dans une fenêtre de console ou un fichier de commandes (.bat). Par exemple, le verbe **Open** lance normalement un programme pour ouvrir un fichier. Sa chaîne de commande se présente généralement comme suit :

``` syntax
"My Program.exe" "%1"
```

« %1 » est l’espace réservé standard pour un paramètre de ligne de commande fourni avec le nom de fichier. Par exemple, il peut spécifier une page particulière à afficher dans une vue à onglets.

> [!Note]  
> Si un élément de la chaîne de commande contient ou peut contenir des espaces, il doit être placé entre guillemets. Sinon, si l’élément contient un espace, il ne sera pas analysé correctement. Par exemple, « My Program.exe » lance l’application correctement. Si vous utilisez mon Program.exe, le système tente de lancer « My » avec « Program.exe » comme premier argument de ligne de commande. Vous devez toujours utiliser des guillemets avec des arguments tels que « %1 » développés pour les chaînes par l’interpréteur de commandes, car vous ne pouvez pas être certain que la chaîne ne contiendra pas d’espace.

 

Les verbes peuvent également être associés à une *chaîne d’affichage* , qui est affichée dans le menu contextuel au lieu de la chaîne de verbe elle-même. Par exemple, la chaîne d’affichage pour **openas** est ouverte avec. Comme les chaînes de menu normales, y compris une esperluette (&) dans la chaîne d’affichage, permet de sélectionner le clavier de la commande.

### <a name="canonical-verbs"></a>Verbes canoniques

En général, les applications sont chargées de fournir des chaînes d’affichage localisées pour les verbes qu’elles définissent. Toutefois, pour fournir un degré d’indépendance du langage, le système définit un ensemble standard de verbes couramment utilisés appelés *verbes canoniques*. Un verbe canonique peut être utilisé avec n’importe quel langage et le système génère automatiquement une chaîne d’affichage correctement localisée. Par exemple, la chaîne d’affichage du verbe **Open** sera définie sur Open sur un système en anglais et öffnen sur un système allemand.

Les verbes canoniques sont les suivants :



| Valeur      | Description                                                                                 |
|------------|---------------------------------------------------------------------------------------------|
| ouvert       | Ouvre le fichier ou le dossier.                                                                   |
| opennew    | Ouvre le fichier ou le dossier dans une nouvelle fenêtre.                                                   |
| print      | Imprime le fichier.                                                                            |
| explorer    | ouvre Windows Explorer avec le dossier sélectionné.                                            |
| trouver       | ouvre la boîte de dialogue **recherche de Windows** avec le dossier défini comme emplacement de recherche par défaut. |
| ouvertes     | Ouvre la boîte **de dialogue Ouvrir avec** .                                                         |
| properties | Ouvre la feuille de propriétés de l’objet.                                                          |



 

Le verbe Printto est également canonique, mais n’est jamais affiché. Elle permet à l’utilisateur d’imprimer un fichier en le faisant glisser vers un objet Printer.

### <a name="extended-verbs"></a>Verbes étendus

Quand l’utilisateur clique avec le bouton droit sur un objet, le menu contextuel contient tous les verbes normaux. Toutefois, il peut y avoir des commandes que vous souhaitez prendre en charge mais qui n’ont pas été affichées dans chaque menu contextuel. Par exemple, vous pouvez avoir des commandes qui ne sont pas couramment utilisées ou qui sont destinées à des utilisateurs expérimentés. Pour cette raison, vous pouvez également définir un ou plusieurs *verbes étendus*. Ces verbes sont également des chaînes de caractères et sont similaires aux verbes normaux. Ils se distinguent des verbes normaux par leur mode d’enregistrement. Pour accéder aux commandes associées à des verbes étendus, l’utilisateur doit cliquer avec le bouton droit sur un objet tout en appuyant sur la touche Maj. Les verbes étendus s’affichent alors en même temps que les verbes normaux.

## <a name="extending-the-shortcut-menu-for-a-file-type"></a>Extension du menu contextuel d’un type de fichier

Le moyen le plus simple d’étendre le menu contextuel pour un type de fichier est d’utiliser le registre. Pour ce faire, ajoutez une sous-clé **Shell** sous la clé pour le ProgID de l’application associée au [type de fichier](fa-file-types.md). Si vous le souhaitez, vous pouvez définir un *verbe par défaut* pour le type de fichier en en faisant la valeur par défaut de la sous-clé **Shell** .

Le verbe par défaut s’affiche en premier dans le menu contextuel. Son objectif est de fournir à l’interpréteur de commandes un verbe qu’il peut utiliser lorsque [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa) est appelé, mais qu’aucun verbe n’est spécifié. L’interpréteur de commandes ne sélectionne pas nécessairement le verbe par défaut lorsque **ShellExecuteEx** est utilisé de cette manière. pour les [versions](versions.md) de Shell 5,0 et ultérieures, détectées sur les systèmes Windows 2000 et versions ultérieures, l’interpréteur de commandes utilise le premier verbe disponible de la liste suivante. Si aucun n’est disponible, l’opération échoue.

-   Verbe Open
-   Le verbe par défaut
-   Premier verbe dans le registre
-   Le verbe openWith

Pour les versions de Shell antérieures à la [version 5,0](versions.md), omettez le troisième élément.

Sous la sous-clé **Shell** , créez une sous-clé pour chaque verbe que vous souhaitez ajouter. Chacune de ces sous-clés aura une valeur **reg \_ SZ** définie sur la chaîne d’affichage du verbe. Vous pouvez omettre la chaîne d’affichage pour les verbes canoniques, car le système affichera automatiquement une chaîne correctement localisée. Si vous omettez la chaîne d’affichage pour les verbes qui ne sont pas Canon, la chaîne de verbes s’affiche. Pour chaque sous-clé de verbe, créez une sous-clé de **commande** avec la valeur par défaut définie sur la chaîne de commande.

L’illustration suivante montre un menu contextuel pour le type de fichier. MYP utilisé dans [types de fichiers](fa-file-types.md) et [Personnalisation des icônes](icon.md). Il a maintenant des verbes ouvrir, doit, imprimer et Printto dans son menu contextuel, avec doit comme verbe par défaut. Le menu contextuel ressemble à ce qui suit.

![capture d’écran du menu contextuel personnalisé](images/context3.jpg)

Les entrées de Registre utilisées pour étendre le menu contextuel présenté dans l’illustration précédente sont les suivantes :

```
HKEY_CLASSES_ROOT
   .myp
      (Default) = MyProgram.1
   MyProgram.1
      (Default) = MyProgram Application
      Shell
         (Default) = doit
         open
            command
               (Default) = C:\MyDir\MyProgram.exe "%1"
         doit
            (Default) = &Do It
            command
               (Default) = C:\MyDir\MyProgram.exe /d "%1"
         print
            command
               (Default) = C:\MyDir\MyProgram.exe /p "%1"
         printto
            command
               (Default) = C:\MyDir\MyProgram.exe /p "%1" "%2" %3 %4
```

Bien que la commande **Ouvrir avec** se trouve au-dessus du premier séparateur, elle est automatiquement créée par le système et ne nécessite pas d’entrée de registre. Le système crée automatiquement des noms complets pour les verbes canoniques ouverts et imprimés. Étant donné que doit n’est pas un verbe canonique, il se voit attribuer un nom d’affichage, « &le faire », que vous pouvez sélectionner en appuyant sur la touche D. Le verbe Printto n’apparaît pas dans le menu contextuel, mais il permet à l’utilisateur d’imprimer des fichiers en les déposant sur une icône d’imprimante. Dans cet exemple, %1 représente le nom de fichier et %2 le nom de l’imprimante.

Les verbes peuvent être supprimés par le biais des paramètres de stratégie en ajoutant une valeur SuppressionPolicy à la clé du verbe. Définissez la valeur de SuppressionPolicy sur l’ID de stratégie. Si la stratégie est activée, le verbe et son entrée de menu contextuel associée sont supprimés. Pour connaître les valeurs possibles de l’ID de stratégie, consultez l’énumération [**restrictions**](/windows/desktop/api/shlobj_core/ne-shlobj_core-restrictions) .

## <a name="extending-the-shortcut-menu-for-predefined-shell-objects"></a>Extension du menu contextuel pour les objets Shell prédéfinis

De nombreux objets Shell prédéfinis ont des menus contextuels qui peuvent être étendus. Inscrivez la commande à peu près de la même façon que vous enregistrez des types de fichiers standard, mais utilisez le nom de l’objet prédéfini comme nom de type de fichier.

Vous trouverez une liste d’objets prédéfinis dans la section *objets Shell prédéfinis* de la rubrique [création de gestionnaires d’extension de Shell](handlers.md). Les objets Shell prédéfinis dont les menus contextuels peuvent être étendus en ajoutant des verbes dans le Registre sont marqués dans la table avec le mot « Verb ».

## <a name="registering-an-application-to-handle-arbitrary-file-types"></a>Inscription d’une application pour gérer des types de fichiers arbitraires

Les sections précédentes de ce document décrivent comment définir des éléments de menu contextuel pour un type de fichier particulier. Entre autres choses, la définition du menu contextuel vous permet de spécifier la manière dont l’application associée ouvre un membre du type de fichier. Toutefois, comme indiqué dans [types de fichiers](fa-file-types.md), les applications peuvent également inscrire une procédure par défaut distincte à utiliser lorsqu’un utilisateur tente d’utiliser votre application pour ouvrir un type de fichier que vous n’avez pas associé à l’application. Cette rubrique est présentée ici, car vous inscrivez la procédure par défaut à peu près de la même façon que vous enregistrez les éléments de menu contextuel.

La procédure par défaut remplit deux fonctions de base. La première consiste à spécifier la manière dont votre application doit être appelée pour ouvrir un type de fichier arbitraire. Vous pouvez, par exemple, utiliser un indicateur de ligne de commande pour indiquer qu’un type de fichier inconnu est en cours d’ouverture. L’autre objectif est de définir les différentes caractéristiques d’un type de fichier, telles que les éléments de menu contextuel et l’icône. Si un utilisateur associe votre application à un type de fichier supplémentaire, ce type aura ces caractéristiques. Si le type de fichier supplémentaire a été précédemment associé à une autre application, ces caractéristiques remplacent les originaux.

Pour inscrire la procédure par défaut, placez les mêmes clés de registre que celles que vous avez créées pour le ProgID de votre application sous la sous-clé de l’application des applications **\_ \_ racines de la classe HKEY** \\ . Vous pouvez également inclure une valeur FriendlyAppName pour fournir au système un nom convivial pour votre application. Le nom convivial de l’application peut également être extrait de son fichier exécutable, mais uniquement si la valeur FriendlyAppName est absente. Le fragment de Registre suivant montre un exemple de procédure par défaut pour MyProgram.exe qui définit un nom convivial et plusieurs éléments de menu contextuel. Les chaînes de commande incluent l’indicateur/a pour notifier l’application qu’il ouvre un type de fichier arbitraire. Si vous incluez une sous-clé **DefaultIcon** , vous devez utiliser une icône générique.

```
HKEY_CLASSES_ROOT
   Applications
      MyProgram.exe
         FriendlyAppName = Friendly Name
         shell
            open
               command
                  (Default) = C:\MyDir\MyProgram.exe /a "%1"
            print
               command
                  (Default) = C:\MyDir\MyProgram.exe /a /p "%1"
            printto
               command
                  (Default) = C:\MyDir\MyProgram.exe /a /p "%1" "%2" %3 %4
```

## <a name="extending-the-new-submenu"></a>Extension du nouveau sous-menu

quand un utilisateur ouvre le menu **fichier** dans l’explorateur de Windows, la première commande est **nouvelle**. La sélection de cette commande affiche un sous-menu. Par défaut, il contient deux commandes, **dossier** et **raccourci**, qui permettent aux utilisateurs de créer des sous-dossiers et des raccourcis. Ce sous-menu peut être étendu pour inclure des commandes de création de fichier pour n’importe quel type de fichier.

Pour ajouter une commande de création de fichier au sous-menu **nouveau** , les fichiers de votre application doivent être associés à un [type de fichier](fa-file-types.md) . Incluez une sous-clé **ShellNew** sous la clé pour l’extension de nom de fichier. Lorsque la **nouvelle** commande du menu **fichier** est sélectionnée, l’interpréteur de commandes l’ajoute au **nouveau** sous-menu. La chaîne d’affichage de la commande sera la chaîne descriptive qui est assignée au ProgID du programme.

Affectez une ou plusieurs valeurs de données à la sous-clé **ShellNew** pour spécifier la méthode de création de fichier. Les valeurs disponibles suivent.



| Valeur    | Description                                                                                                                                                   |
|----------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Commande  | Exécute une application. Il s’agit d’une valeur de **reg \_ SZ** spécifiant le chemin d’accès de l’application à exécuter. Par exemple, vous pouvez le configurer pour lancer un Assistant. |
| Données     | Crée un fichier contenant les données spécifiées. Data est une **valeur \_ binaire de Reg** avec les données du fichier. Les données sont ignorées si NullFile ou FileName est spécifié.  |
| FileName | Crée un fichier qui est une copie d’un fichier spécifié. FileName est une valeur de **reg \_ SZ** , définie sur le chemin d’accès complet du fichier à copier.                 |
| NullFile | Crée un fichier vide. Aucune valeur n’est assignée à NullFile. Si NullFile est spécifié, les valeurs de nom de fichier et de données sont ignorées.                                  |



 

L’illustration suivante montre le **nouveau** sous-menu du type de fichier. MYP utilisé à titre d’exemple dans [types de fichiers](fa-file-types.md) et [Personnalisation des icônes](icon.md). Elle dispose maintenant d’une commande, **MyProgram application**. Lorsqu’un utilisateur sélectionne **application MyProgram** dans le sous-menu **nouveau** , l’interpréteur de commandes crée un fichier nommé « New MyProgram application. MYP » et le transmet à MyProgram.exe.

![capture d’écran du menu nouveau personnalisé](images/context5.png)

L’entrée de Registre est maintenant la suivante :

```
HKEY_CLASSES_ROOT
   .myp
      (Default) = MyProgram.1
      MyProgram.1
         ShellNew
            NullFile
   MyProgram.1
      (Default) = MyProgram Application
      DefaultIcon
         (Default) = C:\MyDir\MyProgram.exe,2
      Shell
         (Default) = doit
         open
            command
               (Default) = C:\MyDir\MyProgram.exe "%1"
         doit
            (Default) = &Do It
            command
               (Default) = C:\MyDir\MyProgram.exe /d "%1"
         print
            command
               (Default) = C:\MyDir\MyProgram.exe /p "%1"
         printto
            command
               (Default) = C:\MyDir\MyProgram.exe /p "%1" "%2" %3 %4
```

 

 



