---
description: Les gestionnaires de menus contextuels, également appelés gestionnaires de menus contextuels ou gestionnaires de verbes, sont un type de gestionnaire de type de fichier. Comme tous les gestionnaires de ce type, il s’agit d’objets COM (Component Object Model) en cours d’implémentation en tant que dll.
ms.assetid: cff79cdc-8a01-4575-9af7-2a485c6a8e46
title: Création de gestionnaires de menu contextuel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e8e102833453566f42d058ff82061f34ebc65691
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127226996"
---
# <a name="creating-shortcut-menu-handlers"></a>Création de gestionnaires de menu contextuel

Les gestionnaires de menus contextuels, également appelés gestionnaires de menus contextuels ou gestionnaires de verbes, sont un type de gestionnaire de type de fichier. Ces gestionnaires peuvent être impelmented de manière à ce qu’ils se chargent dans leur propre processus ou dans l’Explorateur, ou dans d’autres processus tiers. Soyez vigilant lors de la création de gestionnaires in-process, car ils peuvent nuire au processus qui les charge.

> [!Note]  
> il existe des considérations spéciales pour les versions 64 bits de Windows lors de l’enregistrement de gestionnaires qui fonctionnent dans le contexte d’applications 32 bits : lorsqu’ils sont appelés dans le contexte d’une application de bits différents, le sous-système WOW64 redirige l’accès au système de fichiers vers certains chemins d’accès. Si votre gestionnaire de .exe est stocké dans l’un de ces chemins d’accès, il n’est pas accessible dans ce contexte. Par conséquent, pour une solution de contournement, stockez votre .exe dans un chemin d’accès qui n’est pas redirigé, ou stockez une version stub de votre .exe qui lance la version réelle.

Cette rubrique est organisée comme suit :

-   [Verbes canoniques](#canonical-verbs)
-   [Verbes étendus](#extended-verbs)
-   [Verbes d’accès par programme uniquement](#programmaticaccessonly-verbs)
-   [Personnalisation d’un menu contextuel à l’aide de verbes statiques](#customizing-a-shortcut-menu-using-static-verbs)
    -   [Activation de votre gestionnaire à l’aide de l’interface IDropTarget](#activating-your-handler-using-the-idroptarget-interface)
    -   [Spécification de la position et de l’ordre des verbes statiques](#specifying-the-position-and-order-of-static-verbs)
    -   [Positionnement des verbes en haut ou en bas du menu](#positioning-verbs-at-the-top-or-bottom-of-the-menu)
    -   [Création de menus en cascade statiques](#creating-static-cascading-menus)
    -   [Obtention du comportement dynamique pour les verbes statiques à l’aide de la syntaxe de requête avancée](#getting-dynamic-behavior-for-static-verbs-by-using-advanced-query-syntax)
    -   [déconseillé : association de verbes à des commandes échange dynamique de données](#deprecated-associating-verbs-with-dynamic-data-exchange-commands)
-   [Exécution des tâches d’implémentation de verbe](#completing-verb-implementation-tasks)
    -   [Personnalisation du menu contextuel pour les objets Shell prédéfinis](#customizing-the-shortcut-menu-for-predefined-shell-objects)
    -   [Extension d’un nouveau sous-menu](#extending-a-new-submenu)
    -   [Suppression de verbes et contrôle de la visibilité](#suppressing-verbs-and-controlling-visibility)
    -   [Utilisation du modèle de sélection de verbe](#employing-the-verb-selection-model)
    -   [Utilisation des attributs d’élément](#using-item-attributes)
    -   [Implémentation de verbes personnalisés pour les dossiers via Desktop.ini](#implementing-custom-verbs-for-folders-through-desktopini)
-   [Rubriques connexes](#related-topics)

## <a name="canonical-verbs"></a>Verbes canoniques

Les applications sont généralement chargées de fournir des chaînes d’affichage localisées pour les verbes qu’elles définissent. Toutefois, pour fournir un degré d’indépendance du langage, le système définit un ensemble standard de verbes couramment utilisés appelés verbes canoniques. Un verbe canonique n’est jamais affiché à l’utilisateur et peut être utilisé avec n’importe quelle langue d’interface utilisateur. Le système utilise le nom canonique pour générer automatiquement une chaîne d’affichage correctement localisée. Par exemple, la chaîne d’affichage du verbe Open est définie sur **Open** sur un système en anglais et sur l’équivalent allemand sur un système allemand.


| Verbe canonique | Description                                                          |
|----------------|----------------------------------------------------------------------|
| Ouvrir           | Ouvre le fichier ou le dossier.                                            |
| Opennew        | Ouvre le fichier ou le dossier dans une nouvelle fenêtre.                            |
| Imprimer          | Imprime le fichier.                                                     |
| Printto        | Permet à l’utilisateur d’imprimer un fichier en le faisant glisser vers un objet Printer. |
| Explorer        | ouvre Windows Explorer avec le dossier sélectionné.                     |
| Propriétés     | Ouvre la feuille de propriétés de l’objet.                                   |

> [!Note]  
> Le verbe **Printto** est également canonique, mais il n’est jamais affiché. Son inclusion permet à l’utilisateur d’imprimer un fichier en le faisant glisser vers un objet Printer.

Les gestionnaires de menu contextuel peuvent fournir leurs propres verbes canoniques via [**IContextMenu :: GetCommandString**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-getcommandstring) avec **GC \_ VERBW** ou **GC \_ Verba**. Le système utilise les verbes canoniques comme second paramètre (*lpOperation*) passé à [**ShellExecute**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecutea), et est [**CMINVOKECOMMANDINFO**](/windows/desktop/api/Shobjidl_core/ns-shobjidl_core-cminvokecommandinfo). membre **lpVerb** passé à la méthode [**IContextMenu :: commande InvokeCommand**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-invokecommand) .

## <a name="extended-verbs"></a>Verbes étendus

Quand l’utilisateur clique avec le bouton droit sur un objet, le menu contextuel affiche les verbes par défaut. Vous souhaiterez peut-être ajouter et prendre en charge des commandes dans certains menus contextuels qui ne s’affichent pas dans chaque menu contextuel. Par exemple, vous pouvez avoir des commandes qui ne sont pas couramment utilisées ou qui sont destinées à des utilisateurs expérimentés. Pour cette raison, vous pouvez également définir un ou plusieurs verbes étendus. Ces verbes sont semblables aux verbes normaux, mais se distinguent des verbes normaux par leur mode d’enregistrement. Pour avoir accès à des verbes étendus, l’utilisateur doit cliquer avec le bouton droit sur un objet tout en appuyant sur la touche Maj. Lorsque l’utilisateur effectue cette action, les verbes étendus sont affichés en plus des verbes par défaut.

Vous pouvez utiliser le registre pour définir un ou plusieurs verbes étendus. Les commandes associées s’affichent uniquement quand l’utilisateur clique avec le bouton droit sur un objet tout en appuyant sur la touche Maj. Pour définir un verbe comme étendu, ajoutez une valeur **\_ SZ** « étendue » à la sous-clé du verbe. Aucune donnée ne doit être associée à la valeur.

## <a name="programmatic-access-only"></a>Accès par programme uniquement

Ces verbes ne sont jamais affichés dans un menu contextuel. Ils sont accessibles à l’aide de [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa) et en spécifiant le champ **LpVerb** du paramètre *pExecInfo* (un objet [SHELLEXECUTEINFO](/windows/win32/api/shellapi/ns-shellapi-shellexecuteinfoa) ). Pour définir un verbe comme accès par programme uniquement, ajoutez une valeur de **reg \_ SZ** « ProgrammaticAccessOnly » à la sous-clé du verbe. Aucune donnée ne doit être associée à la valeur.

Vous pouvez utiliser le registre pour définir un ou plusieurs verbes étendus. Les commandes associées s’affichent uniquement quand l’utilisateur clique avec le bouton droit sur un objet tout en appuyant sur la touche Maj. Pour définir un verbe comme étendu, ajoutez une valeur **\_ SZ** « étendue » à la sous-clé du verbe. Aucune donnée ne doit être associée à la valeur.

## <a name="customizing-a-shortcut-menu-using-static-verbs"></a>Personnalisation d’un menu contextuel à l’aide de verbes statiques

Après avoir [choisi un verbe statique ou dynamique pour votre menu contextuel](shortcut-choose-method.md) , vous pouvez étendre le menu contextuel d’un type de fichier en inscrivant un verbe statique pour le type de fichier. Pour ce faire, ajoutez une sous-clé **Shell** sous la sous-clé pour le ProgID de l’application associée au type de fichier. Si vous le souhaitez, vous pouvez définir un verbe par défaut pour le type de fichier en en faisant la valeur par défaut de la sous-clé **Shell** .

Le verbe par défaut s’affiche en premier dans le menu contextuel. Son objectif est de fournir à l’interpréteur de commandes un verbe qu’il peut utiliser lorsque la fonction [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa) est appelée, mais qu’aucun verbe n’est spécifié. L’interpréteur de commandes ne sélectionne pas nécessairement le verbe par défaut lorsque **ShellExecuteEx** est utilisé de cette manière.

L’interpréteur de commandes utilise le premier verbe disponible dans l’ordre suivant :

1.  Le verbe par défaut
2.  Premier verbe du Registre, si l’ordre du verbe est spécifié
3.  Verbe **Open**
4.  Le verbe **Open with**

Si aucun des verbes listés n’est disponible, l’opération échoue.

Créez une sous-clé pour chaque verbe que vous souhaitez ajouter sous la sous-clé Shell. Chacune de ces sous-clés doit avoir une valeur **reg \_ SZ** définie sur la chaîne d’affichage du verbe (chaîne localisée). Pour chaque sous-clé de verbe, créez une sous-clé de commande avec la valeur par défaut définie sur la ligne de commande pour activer les éléments. Pour les verbes canoniques, tels que **ouvrir** et **Imprimer**, vous pouvez omettre la chaîne d’affichage, car le système affiche automatiquement une chaîne correctement localisée. Pour les verbes non canoniques, si vous omettez la chaîne d’affichage, la chaîne de verbes est affichée.

Dans l’exemple de Registre suivant, notez les points suivants :

-   Étant donné que **doit** n’est pas un verbe canonique, il est assigné à un nom complet, qui peut être sélectionné en appuyant sur la touche D.
-   Le verbe **Printto** n’apparaît pas dans le menu contextuel. Toutefois, son inclusion dans le registre permet à l’utilisateur d’imprimer des fichiers en les supprimant sur une icône d’imprimante.
-   Une sous-clé est affichée pour chaque verbe. **%1** représente le nom de fichier et **%2** le nom de l’imprimante.

```
HKEY_CLASSES_ROOT
   .myp-ms
      (Default) = MyProgram.1
      MyProgram.1
         (Default) = My Program Application
         Shell
            (Default) = doit
            doit
               (Default) = &Do It
               command
                  (Default) = c:\MyDir\MyProgram.exe /d "%1"
            open
               command
                  (Default) = c:\MyDir\MyProgram.exe /d "%1"
            print
               command
                  (Default) = c:\MyDir\MyProgram.exe /p "%1"
            printto
               command
                  (Default) = c:\MyDir\MyProgram.exe /p "%1" "%2"
```

Le diagramme suivant illustre l’extension du menu contextuel conformément aux entrées de Registre ci-dessus. Ce menu contextuel contient des verbes **ouvrir**, **exécuter** et **Imprimer** dans son menu **, avec le** verbe par défaut.

![capture d’écran du menu contextuel verbe par défaut do it](images/context-menu/context-doitdefaultverb.png)

### <a name="activating-your-handler-using-the-idroptarget-interface"></a>Activation de votre gestionnaire à l’aide de l’interface IDropTarget

échange dynamique de données (DDE) est déconseillé ; Utilisez plutôt [**IDropTarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget) . **IDropTarget** est plus robuste et offre une meilleure prise en charge de l’activation, car il utilise l’activation com du gestionnaire. Dans le cas d’une sélection de plusieurs éléments, **IDropTarget** n’est pas soumis aux restrictions de taille de mémoire tampon trouvées dans DDE et dans [**CreateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa). En outre, les éléments sont passés à l’application sous la forme d’un objet de données qui peut être converti en tableau d’éléments à l’aide de la fonction [**SHCreateShellItemArrayFromDataObject**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shcreateshellitemarrayfromdataobject) . Cela est plus simple et ne perd pas les informations d’espace de noms lorsque l’élément est converti en chemin d’accès pour les protocoles de ligne de commande ou DDE.

Pour plus d’informations sur les requêtes [**IDropTarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget) et Shell pour les attributs d’association de fichiers, consultez [types perçus et inscription d’application](fa-perceivedtypes.md).

### <a name="specifying-the-position-and-order-of-static-verbs"></a>Spécification de la position et de l’ordre des verbes statiques

Normalement, les verbes sont triés sur un menu contextuel en fonction de la façon dont ils sont énumérés. l’énumération est basée en premier sur l’ordre du tableau d’associations, puis sur l’ordre des éléments dans le tableau d’association, tel que défini par l’ordre de tri du Registre.

Les verbes peuvent être classés en spécifiant la valeur par défaut de la sous-clé Shell pour l’entrée Association. Cette valeur par défaut peut inclure un seul élément, qui sera affiché à la position supérieure du menu contextuel, ou une liste d’éléments séparés par des espaces ou des virgules. Dans ce dernier cas, le premier élément de la liste est l’élément par défaut et les autres verbes s’affichent immédiatement en dessous de celui-ci dans l’ordre spécifié.

Par exemple, l’entrée de Registre suivante produit des verbes de menu contextuel dans l’ordre suivant :

1.  Affichage
2.  Gadgets
3.  Personnalisation

```
HKEY_CLASSES_ROOT
   DesktopBackground
      Shell
         Display
         Gadgets
         Personalization
```

De même, l’entrée de Registre suivante produit des verbes de menu contextuel dans l’ordre suivant :

1.  Personnalisation
2.  Gadgets
3.  Affichage

```
HKEY_CLASSES_ROOT
   DesktopBackground
      Shell = "Personalization,Gadgets"
      Display
```

### <a name="positioning-verbs-at-the-top-or-bottom-of-the-menu"></a>Positionnement des verbes en haut ou en bas du menu

L’attribut de Registre suivant peut être utilisé pour placer un verbe en haut ou en bas du menu. S’il existe plusieurs verbes qui spécifient cet attribut, la dernière à le faire est prioritaire :

``` syntax
Position=Top | Bottom 
```

### <a name="creating-static-cascading-menus"></a>Création de menus en cascade statiques

dans Windows 7 et versions ultérieures, l’implémentation des menus en cascade est prise en charge via les paramètres du registre. avant le Windows 7, la création de menus en cascade était possible uniquement via l’implémentation de l’interface [**IContextMenu**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu) . dans Windows 7 et versions ultérieures, vous devez recourir à des solutions basées sur du code COM uniquement lorsque les méthodes statiques sont insuffisantes.

La capture d’écran suivante fournit un exemple de menu en cascade.

![capture d’écran montrant un exemple de menu en cascade](images/file-assoc/filecascademenu2ndex.png)

dans Windows 7 et versions ultérieures, il existe trois façons de créer des menus en cascade :

-   [Création de menus en cascade avec l’entrée de Registre subcommandes](#creating-cascading-menus-with-the-subcommands-registry-entry)
-   [Création de menus en cascade avec l’entrée de Registre ExtendedSubCommandsKey](#creating-cascading-menus-with-the-extendedsubcommandskey-registry-entry)
-   [Création de menus en cascade avec l’interface IExplorerCommand](#creating-cascading-menus-with-the-iexplorercommand-interface)

### <a name="creating-cascading-menus-with-the-subcommands-registry-entry"></a>Création de menus en cascade avec l’entrée de Registre subcommandes

dans Windows 7 et versions ultérieures, vous pouvez utiliser l’entrée de sous-commandes pour créer des menus en cascade à l’aide de la procédure suivante.

**Pour créer un menu en cascade à l’aide de l’entrée de sous-commandes**

1.  Créez une sous-clé sous **HKEY \_ classes \_ racine** \\ *ProgID* \\ **Shell** pour représenter votre menu en cascade. Dans cet exemple, nous attribuons à cette sous-clé le nom *CascadeTest*. Assurez-vous que la valeur par défaut de la sous-clé *CascadeTest* est vide et affichée sous la forme **(valeur non définie)**.

    ```
    HKEY_CLASSES_ROOT
       *
          shell
             CascadeTest
                (Default)
    ```

2.  Dans votre sous-clé *CascadeTest* , ajoutez une entrée MUIVerb de type **reg \_ SZ** et affectez-lui le texte qui s’affichera comme nom dans le menu contextuel. Dans cet exemple, nous lui attribuons le « menu Test cascade ».

    ```
    HKEY_CLASSES_ROOT
       *
          shell
             CascadeTest
                (Default)
                MUIVerb = Test Cascade Menu
    ```

3.  Dans votre sous-clé *CascadeTest* , ajoutez une entrée de sous-commandes de type **reg \_ SZ** qui est affectée à la liste, demlimited par des points-virgules, des verbes qui doivent apparaître dans le menu, dans l’ordre d’apparition. Par exemple, nous attribuons ici un certain nombre de verbes fournis par le système :

    ```
    HKEY_CLASSES_ROOT
       *
          Shell
             CascadeTest
                SubCommands
                Windows.delete;Windows.properties;Windows.rename;Windows.cut;Windows.copy;Windows.paste
    ```

4.  Dans le cas de verbes personnalisés, implémentez-les à l’aide de l’une des méthodes d’implémentation de verbe statique et répertoriez-les sous la sous-clé **CommandStore** comme indiqué dans cet exemple pour un verbe fictif *VerbName*:

    ```
    HKEY_LOCAL_MACHINE
       Software
          Microsoft
             Windows
                CurrentVersion
                   Explorer
                      CommandStore
                         Shell
                            VerbName
                            command
                               (Default) = notepad.exe %1
    ```

> [!Note]  
> Cette méthode présente l’avantage que les verbes personnalisés peuvent être inscrits une seule fois et réutilisés en répertoriant le nom du verbe sous l’entrée sous-commandes. Toutefois, l’application doit avoir l’autorisation de modifier le Registre sous **HKEY \_ local \_ machine**.

 

### <a name="creating-cascading-menus-with-the-extendedsubcommandskey-registry-entry"></a>Création de menus en cascade avec l’entrée de Registre ExtendedSubCommandsKey

dans Windows 7 et versions ultérieures, vous pouvez utiliser l’entrée ExtendedSubCommandKey pour créer des menus en cascade étendus : des menus en cascade dans des menus en cascade.

La capture d’écran suivante est un exemple de menu en cascade étendu.

![capture d’écran montrant le menu en cascade étendu pour les appareils](images/file-assoc/extendedsubcommandskey.png)

Étant donné que **HKEY \_ classes \_ root** est une combinaison de **HKEY \_ Current \_ User** et de **HKEY \_ local \_ machine**, vous pouvez enregistrer tous les verbes personnalisés sous la sous-clé de la sous-clé de la classe de logiciel de l' **\_ \_ utilisateur actuel** \\  \\  . Le principal avantage de cette approche est que les autorisations élevées ne sont pas requises. En outre, d’autres associations de fichiers peuvent réutiliser cet ensemble complet de verbes en spécifiant la même sous-clé ExtendedSubCommandsKey. Si vous n’avez pas besoin de réutiliser cet ensemble de verbes, vous pouvez répertorier les verbes sous le parent, mais vérifiez que la valeur par défaut du parent est vide.

**Pour créer un menu en cascade à l’aide d’une entrée ExtendedSubCommandsKey**

1.  Créez une sous-clé sous **HKEY \_ classes \_ racine** \\ *ProgID* \\ **Shell** pour représenter votre menu en cascade. Dans cet exemple, nous attribuons à cette sous-clé le nom *CascadeTest2*. Assurez-vous que la valeur par défaut de la sous-clé *CascadeTest* est vide et affichée sous la forme **(valeur non définie)**.

    ```
    HKEY_CLASSES_ROOT
       *
          shell
             CascadeTest2
                (Default)
    ```

2.  Dans votre sous-clé *CascadeTest* , ajoutez une entrée MUIVerb de type **reg \_ SZ** et affectez-lui le texte qui s’affichera comme nom dans le menu contextuel. Dans cet exemple, nous lui attribuons le « menu Test cascade ».

    ```
    HKEY_CLASSES_ROOT
       *
          shell
             CascadeTest
                (Default)
                MUIVerb = Test Cascade Menu 2
    ```

3.  Sous la sous-clé *CascadeTest* que vous avez créée, ajoutez une sous-clé **ExtendedSubCommandsKey** , puis ajoutez les sous-commandes du document (de type de **Registre \_ SZ** ), par exemple :

    ```
    HKEY_CLASSES_ROOT
       txtfile
          Shell
             Test Cascade Menu 2
                (Default)
                ExtendedSubCommandsKey
                   Layout
                   Properties
                   Select all
    ```

    Assurez-vous que la valeur par défaut de la sous-clé *menu de test cascade 2* est vide et affichée comme **(valeur non définie)**.

4.  Remplissez les sous-verbes à l’aide de l’une des implémentations de verbe statique suivantes. Notez que la sous-clé CommandFlags représente les valeurs EXPCMDFLAGS. Si vous souhaitez ajouter un séparateur avant ou après l’élément de menu cascade, utilisez ECF \_ SEPARATORBEFORE (0x20) ou ECF \_ SEPARATORAFTER (0x40). pour obtenir une description des indicateurs Windows 7 et versions ultérieures, consultez [**IExplorerCommand :: GetFlags**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iexplorercommand-getflags). ECF \_ SEPARATORBEFORE fonctionne uniquement pour les éléments de menu de niveau supérieur. MUIVerb est de type **reg \_ SZ** et CommandFlags est de type **reg \_ DWORD**.

    ```
    HKEY_CLASSES_ROOT
       txtile
          Shell
             Test Cascade Menu 2
                (Default)
                ExtendedSubCommandsKey
                   Shell
                      cmd1
                         MUIVerb = Notepad
                         command
                            (Default) = %SystemRoot%\system32\notepad.exe %1
                      cmd2
                         MUIVerb = Wordpad
                         CommandFlags = 0x20
                         command
                            (Default) = "C:\Program Files\Windows NT\Accessories\wordpad.exe" %1
    ```

La capture d’écran suivante illustre les exemples d’entrée de clé de Registre précédents.

![capture d’écran montrant un exemple de menu en cascade montrant les choix du bloc-notes et de WordPad](images/file-assoc/testcascademenu2.png)

### <a name="creating-cascading-menus-with-the-iexplorercommand-interface"></a>Création de menus en cascade avec l’interface IExplorerCommand

Vous pouvez également ajouter des verbes à un menu en cascade à l’aide de [**IExplorerCommand :: EnumSubCommands**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iexplorercommand-enumsubcommands). Cette méthode permet aux sources de données qui fournissent leurs commandes de module de commande via [**IExplorerCommandProvider**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommandprovider) d’utiliser ces commandes comme verbes dans un menu contextuel. dans Windows 7 et versions ultérieures, vous pouvez fournir la même implémentation de verbe à l’aide de [**IExplorerCommand**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommand) , comme vous pouvez le faire avec [**IContextMenu**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu).

Les deux captures d’écran suivantes illustrent l’utilisation des menus en cascade dans le dossier **appareils** .

![Capture d’écran montrant un exemple de menu en cascade dans le dossier appareils.](images/file-assoc/filecascademenu.png)

La capture d’écran suivante illustre une autre implémentation d’un menu en cascade dans le dossier **appareils** .

![capture d’écran montrant un exemple de menu en cascade dans le dossier appareils](images/file-assoc/cascadedevices2.png)

> [!Note]  
> Étant donné que [**IExplorerCommand**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommand) prend uniquement en charge l’activation in-process, il est recommandé d’utiliser des sources de données Shell qui doivent partager l’implémentation entre des commandes et des menus contextuels.

 

### <a name="getting-dynamic-behavior-for-static-verbs-by-using-advanced-query-syntax"></a>Obtention du comportement dynamique pour les verbes statiques à l’aide de la syntaxe de requête avancée

La syntaxe de requête avancée (AQS) peut exprimer une condition qui sera évaluée à l’aide des propriétés de l’élément pour lequel le verbe est instancié. Ce système fonctionne uniquement avec les propriétés rapides. Il s’agit de propriétés que la source de données Shell signale comme rapide en ne retournant pas [* * * * SHCOLSTATE \_ Slow * *](/windows/win32/api/shtypes/ne-shtypes-shcolstate) * * à partir de [**IShellFolder2 :: GetDefaultColumnState**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder2-getdefaultcolumnstate).

Windows 7 et les versions ultérieures prennent en charge les valeurs canoniques qui évitent les problèmes sur les builds localisées. la syntaxe canonique suivante est requise sur les builds localisées pour tirer parti de cette Windows 7 améliorations.

``` syntax
System.StructuredQueryType.Boolean#True
```

Dans l’exemple d’entrée de Registre suivant :

-   La valeur **appliesTo** contrôle si le verbe est affiché ou masqué.
-   La valeur DefaultAppliesTo détermine le verbe par défaut.
-   La valeur HasLUAShield détermine si un bouclier de contrôle de compte d’utilisateur (UAC) est affiché.

Dans cet exemple, la valeur **DefaultAppliesTo** convertit ce verbe en valeur par défaut pour tous les fichiers avec le mot « exampleText1 » dans son nom de fichier. La valeur **appliesTo** active le verbe pour tout fichier avec « exampleText1 » dans le nom. La valeur **HasLUAShield** affiche la protection des fichiers dont le nom contient « exampleText2 ».

```
HKEY_CLASSES_ROOT
   txtile
      shell
         test.verb
            DefaultAppliesTo = System.ItemName:"exampleText1"
            HasLUAShield = System.ItemName:"exampleText2"
            AppliesTo = System.ItemName:"exampleText1"
```

Ajoutez la sous-clé de **commande** et une valeur :

```
HKEY_CLASSES_ROOT
   txtile
      shell
         test.verb
            Command
               (Default) = %SystemRoot%\system32\notepad.exe %1
```

dans le registre Windows 7, consultez la section **HKEY \_ CLASSES \_ ROOT** \\ **drive** comme exemple de verbes bitlocker qui utilisent l’approche suivante :

-   AppliesTo = System. volume. BitlockerProtection : = 2
-   System. volume. BitlockerRequiresAdmin : = System. StructuredQueryType. Boolean \# true

Pour plus d’informations sur AQS, consultez [syntaxe de requête avancée](../search/-search-3x-advancedquerysyntax.md).

### <a name="deprecated-associating-verbs-with-dynamic-data-exchange-commands"></a>déconseillé : association de verbes à des commandes échange dynamique de données

DDE est déconseillé. Utilisez plutôt [**IDropTarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget) . DDE est déconseillé, car il s’appuie sur un message de fenêtre de diffusion pour découvrir le serveur DDE. Un serveur DDE bloque le message de fenêtre de diffusion et bloque donc les conversations DDE pour d’autres applications. Il est courant qu’une application bloquée unique provoque des blocages ultérieurs tout au bout de l’expérience de l’utilisateur.

La méthode [**IDropTarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget) est plus robuste et offre une meilleure prise en charge de l’activation, car elle utilise l’activation com du gestionnaire. Dans le cas d’une sélection de plusieurs éléments, **IDropTarget** n’est pas soumis aux restrictions de taille de mémoire tampon trouvées dans DDE et dans [**CreateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa). En outre, les éléments sont passés à l’application sous la forme d’un objet de données qui peut être converti en tableau d’éléments à l’aide de la fonction [**SHCreateShellItemArrayFromDataObject**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shcreateshellitemarrayfromdataobject) . Cela est plus simple et ne perd pas les informations d’espace de noms lorsque l’élément est converti en chemin d’accès pour les protocoles de ligne de commande ou DDE.

Pour plus d’informations sur les requêtes [**IDropTarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget) et Shell pour les attributs d’association de fichiers, consultez [types perçus et inscription d’application](fa-perceivedtypes.md).

## <a name="completing-verb-implementation-tasks"></a>Exécution des tâches d’implémentation de verbe

Les tâches suivantes pour implémenter des verbes sont pertinentes pour les implémentations de verbes statiques et dynamiques. Pour plus d’informations sur les verbes dynamiques, consultez [Personnalisation d’un menu contextuel à l’aide de verbes dynamiques](shortcut-menu-using-dynamic-verbs.md).

### <a name="customizing-the-shortcut-menu-for-predefined-shell-objects"></a>Personnalisation du menu contextuel pour les objets Shell prédéfinis

De nombreux objets Shell prédéfinis ont des menus contextuels qui peuvent être personnalisés. Inscrivez la commande à peu près de la même façon que vous enregistrez des types de fichiers standard, mais utilisez le nom de l’objet prédéfini comme nom de type de fichier.

Une liste d’objets prédéfinis se trouve dans la section *objets Shell prédéfinis* de la [création de gestionnaires d’extension de Shell](handlers.md). Les objets Shell prédéfinis dont les menus contextuels peuvent être personnalisés en ajoutant des verbes dans le Registre sont marqués dans la table avec le mot verbe.

### <a name="extending-a-new-submenu"></a>Extension d’un nouveau sous-menu

quand un utilisateur ouvre le menu **fichier** dans l’explorateur de Windows, l’une des commandes affichées est **nouveau**. La sélection de cette commande affiche un sous-menu. Par défaut, le sous-menu contient deux commandes, **dossier** et **raccourci**, qui permettent aux utilisateurs de créer des sous-dossiers et des raccourcis. Ce sous-menu peut être étendu pour inclure des commandes de création de fichier pour n’importe quel type de fichier.

Pour ajouter une commande de création de fichier au sous-menu **nouveau** , les fichiers de votre application doivent avoir un type de fichier associé. Incluez une sous-clé **ShellNew** sous le nom de fichier. Lorsque la **nouvelle** commande du menu **fichier** est sélectionnée, l’interpréteur de commandes ajoute le type de fichier au **nouveau** sous-menu. La chaîne d’affichage de la commande est la chaîne descriptive qui est assignée au ProgID du programme.

Pour spécifier la méthode de création de fichier, affectez une ou plusieurs valeurs de données à la sous-clé **ShellNew** . Les valeurs disponibles sont répertoriées dans le tableau suivant.



| Valeur de la sous-clé ShellNew | Description                                                                                                                                                              |
|-----------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Commande               | Exécute une application. Cette valeur **reg \_ SZ** spécifie le chemin d’accès de l’application à exécuter. Par exemple, vous pouvez le configurer pour lancer un Assistant.                  |
| Données                  | Crée un fichier contenant les données spécifiées. Cette valeur **reg \_ Binary** spécifie les données du fichier. Les **données** sont ignorées si **Nullfile** ou **filename** est spécifié. |
| FileName              | Crée un fichier qui est une copie d’un fichier spécifié. Cette valeur **reg \_ SZ** spécifie le chemin d’accès complet du fichier à copier.                                   |
| NullFile              | Crée un fichier vide. **Nullfile** n’a pas de valeur assignée. Si **Nullfile** est spécifié, les valeurs de registre des **données** et des **noms** de fichiers sont ignorées.                    |



 

L’exemple de clé de Registre et la capture d’écran ci-dessous illustrent le **nouveau** sous-menu pour le type de fichier. MYP-ms. Elle possède une commande, **MyProgram application**.

```
HKEY_CLASSES_ROOT
   .myp
      (Default) = MyProgram.1
      MyProgram.1
         ShellNew
         NullFile
```

La capture d’écran illustre le **nouveau** sous-menu. Lorsqu’un utilisateur sélectionne **application MyProgram** dans le sous-menu **nouveau** , l’interpréteur de commandes crée un fichier nommé **New MyProgram application. MYP-ms** et le transmet à **MyProgram.exe**.

![capture d’écran de l’Explorateur Windows montrant une nouvelle commande « application MyProgram » dans le sous-menu « nouveau »](images/context-menu/context-myprogramexe.png)

### <a name="creating-drag-and-drop-handlers"></a>Création de gestionnaires de glisser-déplacer

La procédure de base pour l’implémentation d’un gestionnaire de glisser-déplacer est identique à celle des gestionnaires de menus contextuels conventionnels. Toutefois, les gestionnaires de menus contextuels utilisent normalement uniquement le pointeur [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) transmis à la méthode [**IShellExtInit :: Initialize**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellextinit-initialize) du gestionnaire pour extraire le nom de l’objet. Un gestionnaire de glisser-déplacer peut implémenter un gestionnaire de données plus sophistiqué pour modifier le comportement de l’objet déplacé.

Quand un utilisateur clique avec le bouton droit sur un objet Shell pour faire glisser un objet, un menu contextuel s’affiche lorsque l’utilisateur tente de supprimer l’objet. La capture d’écran suivante illustre un menu contextuel de glisser-déplacer classique.

![capture d’écran du menu contextuel glisser-déplacer](images/context-menu/context-dragdrop.png)

Un gestionnaire de glisser-déplacer est un gestionnaire de menu contextuel qui peut ajouter des éléments à ce menu contextuel. Les gestionnaires de glisser-déplacer sont généralement enregistrés sous la sous-clé suivante.

```
HKEY_CLASSES_ROOT
   Directory
      shellex
         DragDropHandlers
```

Ajoutez une sous-clé sous la sous-clé **DragDropHandlers** nommée pour le gestionnaire de glisser-déplacer, puis définissez la valeur par défaut de la sous-clé sur la forme de chaîne du GUID de l’identificateur de classe (CLSID) du gestionnaire. L’exemple suivant active le gestionnaire de glisser-déplacer **MyDD** .

```
HKEY_CLASSES_ROOT
   Directory
      shellex
         DragDropHandlers
            MyDD
               (Default) = {MyDD CLSID GUID}
```

### <a name="suppressing-verbs-and-controlling-visibility"></a>Suppression de verbes et contrôle de la visibilité

vous pouvez utiliser Windows paramètres de stratégie pour contrôler la visibilité des verbes. Les verbes peuvent être supprimés par le biais des paramètres de stratégie en ajoutant une valeur **SuppressionPolicy** ou une valeur Guid **SuppressionPolicyEx** à la sous-clé de Registre du verbe. Définissez la valeur de la sous-clé **SuppressionPolicy** sur l’ID de stratégie. Si la stratégie est activée, le verbe et son entrée de menu contextuel associée sont supprimés. Pour connaître les valeurs possibles de l’ID de stratégie, consultez l’énumération [**restrictions**](/windows/desktop/api/shlobj_core/ne-shlobj_core-restrictions) .

### <a name="employing-the-verb-selection-model"></a>Utilisation du modèle de sélection de verbe

Les valeurs de Registre doivent être définies pour que les verbes gèrent les situations où un utilisateur peut sélectionner un seul élément, plusieurs éléments ou une sélection d’un élément. Un verbe requiert des valeurs de Registre distinctes pour chacune des trois situations prises en charge par le verbe. Les valeurs possibles pour le modèle de sélection de verbe sont les suivantes :

-   Spécifiez la valeur MultiSelectModel pour tous les verbes. Si la valeur MultiSelectModel n’est pas spécifiée, elle est déduite du type d’implémentation de verbe que vous avez choisi. Pour les méthodes basées sur COM (par exemple, DropTarget et ExecuteCommand), le **lecteur** est supposé, et pour les autres méthodes, le **document** est supposé.
-   Spécifiez **Single** pour les verbes qui prennent en charge une seule sélection.
-   Spécifiez **Player** pour les verbes qui prennent en charge un nombre quelconque d’éléments.
-   Spécifiez **document** pour les verbes qui créent une fenêtre de niveau supérieur pour chaque élément. Cela permet de limiter le nombre d’éléments activés et de ne pas manquer de ressources système si l’utilisateur ouvre un trop grand nombre de fenêtres.

Lorsque le nombre d’éléments sélectionnés ne correspond pas au modèle de sélection de verbe ou est supérieur aux limites par défaut indiquées dans le tableau suivant, le verbe ne s’affiche pas.



| Type d’implémentation de verbe | Document | Lecteur    |
|-----------------------------|----------|-----------|
| Hérité                      | 15 éléments | 100 éléments |
| COM                         | 15 éléments | Aucune limite  |



 

Voici des exemples d’entrées de Registre utilisant la valeur MultiSelectModel.

```
HKEY_CLASSES_ROOT
   Folder
      shell
         open
             = MultiSelectModel = Document
```

```
HKEY_CLASSES_ROOT
   ProgID
      shell
         verb
             = MultiSelectModel = Single | Document | Player
```

### <a name="using-item-attributes"></a>Utilisation des attributs d’élément

Les valeurs d’indicateur [**SFGAO**](sfgao.md) des attributs d’environnement d’un élément peuvent être testées pour déterminer si le verbe doit être activé ou désactivé.

Pour utiliser cette fonctionnalité d’attribut, ajoutez les valeurs **reg \_ DWORD** suivantes sous le verbe :

-   La valeur AttributeMask spécifie la valeur [**SFGAO**](sfgao.md) des valeurs de bit du masque avec lequel effectuer le test.
-   La valeur AttributeValue spécifie la valeur [**SFGAO**](sfgao.md) des bits qui sont testés.
-   Le ImpliedSelectionModel spécifie zéro pour les verbes d’élément, ou une valeur différente de zéro pour les verbes dans le menu contextuel d’arrière-plan.

Dans l’exemple d’entrée de Registre suivant, AttributeMask est défini sur [**SFGAO \_ ReadOnly**](sfgao.md) (0x40000).

```
HKEY_CLASSES_ROOT
   txtfile
      Shell
         test.verb2
            AttributeMask = 0x40000
            AttributeValue = 0x0
            ImpliedSelectionModel = 0x0
            command
               (Default) = %SystemRoot%\system32\notepad.exe %1
```

### <a name="implementing-custom-verbs-for-folders-through-desktopini"></a>Implémentation de verbes personnalisés pour les dossiers via Desktop.ini

dans Windows 7 et versions ultérieures, vous pouvez ajouter des verbes à un dossier par le biais de Desktop.ini. Pour plus d’informations sur les fichiers de Desktop.ini, consultez [Comment personnaliser des dossiers avec des Desktop.ini](how-to-customize-folders-with-desktop-ini.md).

> [!Note]  
> Desktop.ini fichiers doivent toujours être marqués comme étant  +  **masqués** par le système afin qu’ils ne soient pas affichés aux utilisateurs.

 

**Pour ajouter des verbes personnalisés pour les dossiers à l’aide d’un fichier Desktop.ini, procédez comme suit :**

1.  Créez un dossier marqué **en lecture seule** ou **système**.
2.  Créez un fichier de Desktop.ini qui comprend un \[ . ShellClassInfo \] DirectoryClass = ProgID du dossier.
3.  Dans le registre, créez le dossier **\_ \_ racine** de l’identificateur de classe HKEY, \\  avec la valeur CanUseForDirectory. La valeur CanUseForDirectory évite l’utilisation abusive des ProgID qui sont définis pour ne pas participer à l’implémentation de verbes personnalisés pour les dossiers par le biais de Desktop.ini.
4.  Ajoutez des verbes dans la sous-clé du **dossier** ProgID, par exemple :

    ```
    HKEY_CLASSES_ROOT
       CustomFolderType
          Shell
             MyVerb
                command
                   (Default) = %SystemRoot%\system32\notepad.exe %1\desktop.ini
    ```

> [!Note]  
> Ces verbes peuvent être le verbe par défaut. dans ce cas, le double-clic sur le dossier active le verbe.

 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Meilleures pratiques pour les gestionnaires de menus contextuels et les verbes de sélection multiple](verbs-best-practices.md)
</dt> <dt>

[Choix d’un verbe statique ou dynamique pour votre menu contextuel](shortcut-choose-method.md)
</dt> <dt>

[Personnalisation d’un menu contextuel à l’aide de verbes dynamiques](shortcut-menu-using-dynamic-verbs.md)
</dt> <dt>

[Menus contextuels (menu contextuel) et gestionnaires de menus contextuels](context-menu.md)
</dt> <dt>

[Verbes et associations de fichiers](fa-verbs.md)
</dt> <dt>

[Référence du menu contextuel](context-menu-reference.md)
</dt> </dl>

 

 
