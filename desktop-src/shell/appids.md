---
description: les id de modèle utilisateur de l’Application (AppUserModelIDs) sont largement utilisés par la barre des tâches des systèmes Windows 7 et versions ultérieures pour associer les processus, les fichiers et les fenêtres à une application particulière.
ms.assetid: ebce2d99-6f20-4545-9f12-d79cd8d0828f
title: ID de modèle d’utilisateur d’application (AppUserModelIDs)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: acd0835af241a36e4d9c95237890cb63790f7fe9031476dfa8ec21254266ffd7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119351469"
---
# <a name="application-user-model-ids-appusermodelids"></a>ID de modèle d’utilisateur d’application (AppUserModelIDs)

les id de modèle utilisateur de l’Application (AppUserModelIDs) sont largement utilisés par la barre des tâches des systèmes Windows 7 et versions ultérieures pour associer les processus, les fichiers et les fenêtres à une application particulière. Dans certains cas, il suffit de s’appuyer sur la AppUserModelID interne assignée à un processus par le système. Toutefois, une application qui possède plusieurs processus ou une application qui s’exécute dans un processus hôte peut avoir besoin de s’identifier de manière explicite pour pouvoir regrouper ses différentes fenêtres dans un même bouton de la barre des tâches et contrôler le contenu de la liste de raccourcis de cette application.

-   [AppUserModelIDs définie par l’application et System-Defined](#application-defined-and-system-defined-appusermodelids)
-   [Comment former un Application-Defined AppUserModelID](#how-to-form-an-application-defined-appusermodelid)
-   [Où assigner un AppUserModelID](#where-to-assign-an-appusermodelid)
-   [Inscription d’une application en tant que processus hôte](#registering-an-application-as-a-host-process)
-   [Listes d’exclusion pour l’épinglage de la barre des tâches et listes récentes/fréquentes](#exclusion-lists-for-taskbar-pinning-and-recentfrequent-lists)
-   [Rubriques connexes](#related-topics)

## <a name="application-defined-and-system-defined-appusermodelids"></a>Application-Defined et System-Defined AppUserModelIDs

Certaines applications ne déclarent pas de AppUserModelID explicite. Ils sont facultatifs. Dans ce cas, le système utilise une série d’heuristiques pour assigner une AppUserModelID interne. Toutefois, il existe un avantage en termes de performances pour éviter ces calculs et un AppUserModelID explicite est le seul moyen de garantir une expérience utilisateur exacte. Par conséquent, il est fortement recommandé de définir un ID explicite. Les applications ne peuvent pas récupérer une AppUserModelID affectée par le système.

Si une application utilise un AppUserModelID explicite, elle doit également affecter la même valeur AppUserModelID à l’ensemble des fenêtres, des processus, des raccourcis et des associations de fichiers en cours d’exécution. Elle doit également utiliser la valeur AppUserModelID lors de la personnalisation de sa liste de raccourcis par le biais de [**ICustomDestinationList**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icustomdestinationlist), et dans tous les appels à [**SHAddToRecentDocs**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shaddtorecentdocs).

> [!Note]  
> Si les applications n’ont pas de AppUserModelID explicite, elles doivent appeler les méthodes [**IApplicationDestinations**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iapplicationdestinations), [**IApplicationDocumentLists**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iapplicationdocumentlists)et [**ICustomDestinationList**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icustomdestinationlist) ainsi que [**SHAddToRecentDocs**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shaddtorecentdocs) à partir de l’application. Si ces méthodes sont appelées à partir d’un autre processus, comme un programme d’installation ou un programme de désinstallation, le système ne peut pas générer la AppUserModelID correcte et ces appels n’auront aucun effet.

 

Les éléments suivants décrivent des scénarios courants qui requièrent une AppUserModelID explicite. Elles signalent également les cas où plusieurs AppUserModelIDs explicites doivent être utilisés.

-   Un seul fichier exécutable avec une interface utilisateur avec plusieurs modes qui s’affichent à l’utilisateur en tant qu’applications distinctes doivent assigner différents AppUserModelIDs à chaque mode. Par exemple, une partie d’une application que les utilisateurs voient comme une expérience indépendante qu’ils peuvent épingler et lancer à partir de la barre des tâches séparément du reste de l’application doit avoir son propre AppUserModelID, distinct de l’expérience principale.
-   Plusieurs raccourcis avec des arguments différents qui mènent à ce que l’utilisateur voit comme la même application doivent utiliser un AppUserModelID pour tous les raccourcis. par exemple, Windows Internet explorer propose différents raccourcis pour différents modes (tels que le lancement sans modules complémentaires), mais ils doivent tous apparaître pour l’utilisateur sous la forme d’une seule instance d’Internet Explorer.
-   Un fichier exécutable qui agit comme un processus hôte et exécute le contenu cible comme une application doit [s’inscrire en tant qu’application hôte](#registering-an-application-as-a-host-process), après quoi il peut affecter différents AppUserModelIDs à chaque expérience perçue qu’il héberge. Le processus hôte peut également permettre au programme hébergé de définir son AppUserModelIDs. Dans les deux cas, le processus hôte doit conserver un enregistrement de la source du AppUserModelIDs, soit lui-même, soit l’application hébergée. Dans ce cas, il n’y a pas d’expérience utilisateur principale du processus hôte sans le contenu cible. les exemples sont Windows applications distantes intégrées localement (RAIL), le Runtime Java, RunDLL32.exe ou DLLHost.exe.

    Dans le cas d’applications hébergées existantes, le système tente d’identifier les expériences individuelles, mais les nouvelles applications doivent utiliser des AppUserModelIDs explicites pour garantir l’expérience utilisateur prévue.

-   Les processus coopératifs ou chaînés qui font partie de la même application doivent avoir la même valeur AppUserModelID appliquée à chaque processus. il s’agit par exemple de jeux avec un processus de lancement (chaîné) et de Microsoft Lecteur Windows Media, qui a une expérience de première exécution/configuration exécutée dans un processus et l’application principale s’exécutant dans un autre processus (coopératif).
-   une extension d’espace de noms de Shell qui agit comme une application distincte pour plus que la consultation et la gestion de contenu dans Windows Explorer doit affecter une AppUserModelID dans ses propriétés de dossier. Le panneau de configuration en est un exemple.
-   Dans un environnement de virtualisation comme une infrastructure de déploiement, l’environnement de virtualisation doit assigner différents AppUserModelIDs à chaque application qu’il gère. Dans ce cas, un lanceur d’applications utilise un processus intermédiaire pour configurer l’environnement, puis transmet l’opération à un processus différent pour exécuter l’application. Notez que cela entraîne l’impossibilité pour le système d’associer le processus cible en cours d’exécution au raccourci, car le raccourci pointe vers le processus intermédiaire.

    Si une application possède plusieurs fenêtres, raccourcis ou processus, la valeur AppUserModelID affectée à cette application doit également être appliquée à chacun de ces éléments par l’environnement de virtualisation.

    un exemple de cette situation est le ClickOnce framework, qui affecte correctement les AppUserModelIDs pour le compte des applications qu’il gère. comme dans tous ces environnements, les applications déployées et gérées par des ClickOnce ne doivent pas assigner des AppUserModelIDs explicites, car cela entraînera un conflit avec le AppUserModelIDs attribué par ClickOnce et entraînera des résultats inattendus.

## <a name="how-to-form-an-application-defined-appusermodelid"></a>Comment former un Application-Defined AppUserModelID

Une application doit fournir son AppUserModelID au format suivant. Il ne peut pas comporter plus de 128 caractères et ne peut pas contenir d’espaces. Chaque section doit respecter la casse Pascal.

`CompanyName.ProductName.SubProduct.VersionInformation`

`CompanyName` et `ProductName` doivent toujours être utilisés, tandis que les `SubProduct` `VersionInformation` parties et sont facultatives et dépendent des exigences de l’application. `SubProduct` permet à une application principale composée de plusieurs sous-applications de fournir un bouton de barre des tâches distinct pour chaque sous-application et ses fenêtres associées. `VersionInformation` permet à deux versions d’une application de coexister pendant qu’elles sont considérées comme des entités discrètes. Si une application n’est pas destinée à être utilisée de cette manière, `VersionInformation` doit être omis afin qu’une version mise à niveau puisse utiliser la même valeur AppUserModelID que la version qu’elle a remplacée.

## <a name="where-to-assign-an-appusermodelid"></a>Où assigner un AppUserModelID

Quand une application utilise un ou plusieurs AppUserModelIDs explicites, elle doit appliquer ces AppUserModelIDs aux emplacements et situations suivants :

-   Dans la propriété [System.AppUserModel.ID](../properties/props-system-appusermodel-id.md) du fichier de raccourci de l’application. Un raccourci (sous la forme d’un fichier [**IShellLink**](/windows/desktop/api/Shobjidl_core/nn-shobjidl_core-ishelllinka), CLSID \_ ShellLink ou. lnk) prend en charge les propriétés par le biais de [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) et d’autres mécanismes de définition de propriétés utilisés dans l’ensemble du shell. Cela permet à la barre des tâches d’identifier le raccourci approprié pour épingler et de s’assurer que les fenêtres appartenant au processus sont associées de manière appropriée à ce bouton de la barre des tâches.
    > [!Note]  
    > La propriété [System.AppUserModel.ID](../properties/props-system-appusermodel-id.md) doit être appliquée à un raccourci lorsque ce raccourci est créé. lors de l’utilisation du Microsoft Windows Installer (MSI) pour installer l’application, la table [MsiShortcutProperty](../msi/msishortcutproperty-table.md) permet d’appliquer la valeur AppUserModelID au raccourci lorsqu’il est créé pendant l’installation.

     

-   En tant que propriété de l’une des fenêtres de l’application en cours d’exécution. Cela peut être défini de deux manières :

    1.  Si différentes fenêtres détenues par un processus nécessitent différents AppUserModelIDs pour contrôler le regroupement de la barre des tâches, utilisez [**SHGetPropertyStoreForWindow**](/windows/win32/api/shellapi/nf-shellapi-shgetpropertystoreforwindow)) pour récupérer la Banque de propriétés de la fenêtre et définir la valeur AppUserModelID comme propriété de fenêtre.
    2.  Si toutes les fenêtres du processus utilisent le même AppUserModelID, définissez la valeur AppUserModelID sur le processus à l’aide de [**SetCurrentProcessExplicitAppUserModelID**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-setcurrentprocessexplicitappusermodelid). Une application doit appeler **SetCurrentProcessExplicitAppUserModelID** pour définir son AppUserModelID pendant la routine de démarrage initiale d’une application avant que l’application ne présente une interface utilisateur, effectue toute manipulation de ses listes de raccourcis, ou fait (ou force le système à effectuer) tout appel à [**SHAddToRecentDocs**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shaddtorecentdocs).

    Une AppUserModelID au niveau de la fenêtre substitue un AppUserModelID au niveau du processus.

    Quand une application définit un AppUserModelID explicite au niveau de la fenêtre, l’application peut fournir les détails de sa commande de redémarrage pour le bouton de la barre des tâches. Pour fournir ces informations, les propriétés suivantes sont utilisées :

    -   [System. AppUserModel. RelaunchCommand](../properties/props-system-appusermodel-relaunchcommand.md)
    -   [System. AppUserModel. RelaunchDisplayNameResource](../properties/props-system-appusermodel-relaunchdisplaynameresource.md)
    -   [System. AppUserModel. RelaunchIconResource](../properties/props-system-appusermodel-relaunchiconresource.md)

    > [!Note]  
    > S’il existe un raccourci pour lancer l’application, une application doit appliquer la valeur AppUserModelID en tant que propriété du raccourci au lieu d’utiliser les propriétés de relancement. Dans ce cas, la ligne de commande, l’icône et le texte du raccourci sont utilisés pour fournir les mêmes informations que les propriétés de relancement.

     

    Une AppUserModelID explicite au niveau de la fenêtre peut également utiliser la propriété [System. AppUserModel. PreventPinning](../properties/props-system-appusermodel-preventpinning.md) pour indiquer qu’elle ne doit pas être disponible pour l’épinglage ou le relancement.

-   Dans un appel à Customize ou Update ([**ICustomDestinationList**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icustomdestinationlist)), récupérez ([**IApplicationDocumentLists**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iapplicationdocumentlists)) ou Clear ([**IApplicationDestinations**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iapplicationdestinations)) la liste de raccourcis de l’application.
-   Dans l’enregistrement d’association de fichiers (via son [ProgID](fa-progids.md)) si l’application utilise les listes de destinations **récentes** ou **fréquentes** générées automatiquement par le système. Ces informations d’association sont référencées par [**SHAddToRecentDocs**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shaddtorecentdocs). Ces informations sont également utilisées lors de l’ajout de destinations [**IShellItem**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem) à des listes de raccourcis personnalisées via [**ICustomDestinationList :: AppendCategory**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icustomdestinationlist-appendcategory).
-   Dans n’importe quel appel, l’application effectue directement [**SHAddToRecentDocs**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shaddtorecentdocs). Si l’application dépend de la boîte de dialogue de fichier commune pour effectuer des appels à **SHAddToRecentDocs** en son nom, ces appels peuvent déduire l’AppUserModelID explicite uniquement si la valeur AppUserModelID est définie pour l’ensemble du processus. Si l’application définit AppUserModelIDs sur son Windows au lieu du processus, l’application doit effectuer tous les appels à **SHAddToRecentDocs** elle-même, avec son AppUserModelID explicite, et empêcher la boîte de dialogue de fichier commune d’effectuer ses propres appels. Cela doit être fait à chaque fois qu’un élément est ouvert, pour garantir que les sections **récentes** ou **fréquentes** de la liste de raccourcis de l’application sont exactes.

Les éléments suivants décrivent des scénarios courants et permettent d’appliquer des AppUserModelIDs explicites dans ces scénarios.

-   Lorsqu’un seul processus contient plusieurs applications, utilisez [**SHGetPropertyStoreForWindow**](/windows/win32/api/shellapi/nf-shellapi-shgetpropertystoreforwindow) pour récupérer la Banque de propriétés de la fenêtre et définir la valeur AppUserModelID en tant que propriété de fenêtre.
-   Quand une application utilise plusieurs processus, appliquez la valeur AppUserModelID à chaque processus. Le fait que vous utilisiez le même AppUserModelID sur chaque processus varie selon que vous souhaitez que chaque processus apparaisse dans le cadre de l’application principale ou en tant qu’entités individuelles.
-   Pour séparer certaines fenêtres d’un jeu dans le même processus, utilisez le magasin de propriétés de la fenêtre pour appliquer une seule AppUserModelID aux fenêtres que vous souhaitez séparer, puis appliquez une valeur AppUserModelID différente au processus. Toute fenêtre de ce processus qui n’a pas été explicitement étiquetée avec la AppUserModelID au niveau de la fenêtre hérite de la AppUserModelID du processus.
-   Si un type de fichier est associé à une application, assignez la AppUserModelID à l’inscription du [ProgID](fa-progids.md) du type de fichier. Si un seul fichier exécutable est lancé dans différents modes qui apparaissent à l’utilisateur en tant qu’applications distinctes, un AppUserModelID distinct est requis pour chaque mode. Dans ce cas, il doit y avoir plusieurs inscriptions ProgID pour le type de fichier, chacune avec une AppUserModelID différente.
-   Quand il existe plusieurs emplacements de raccourci à partir desquels un utilisateur peut lancer une application (dans le menu **Démarrer** , sur le bureau ou ailleurs), récupérez la Banque de propriétés du raccourci pour appliquer un seul AppUserModelID à tous les raccourcis en tant que propriétés de raccourci.
-   Lorsqu’un appel explicite est adressé à [**SHAddToRecentDocs**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shaddtorecentdocs) par une application, utilisez la valeur AppUserModelID dans l’appel. Quand la boîte de dialogue de fichier commune est utilisée pour ouvrir ou enregistrer des fichiers, **SHAddToRecentDocs** est appelé par la boîte de dialogue pour le compte de l’application. Cet appel peut déduire la AppUserModelID explicite à partir du processus. Toutefois, si une AppUserModelID explicite est appliquée en tant que propriété de fenêtre, la boîte de dialogue de fichier commune ne peut pas déterminer la AppUserModelID correcte. Dans ce cas, l’application elle-même doit appeler explicitement **SHAddToRecentDocs** et lui fournir la AppUserModelID correcte. En outre, l’application doit empêcher la boîte de dialogue de fichier commune d’appeler **SHAddToRecentDocs** en son nom en définissant l' \_ indicateur Fos DONTADDTORECENT dans la méthode **GetOptions** de [**IFileOpenDialog**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ifileopendialog) ou [**IFileSaveDialog**](/windows/desktop/api/Shobjidl_core/nn-shobjidl_core-ifilesavedialog).

## <a name="registering-an-application-as-a-host-process"></a>Inscription d’une application en tant que processus hôte

Une application peut définir l’entrée de Registre IsHostApp pour faire en sorte que le processus de ce fichier exécutable soit considéré comme un processus hôte par la barre des tâches. Cela affecte ses entrées de regroupement et de liste de raccourcis par défaut.

L’exemple suivant illustre l’entrée de registre requise. Notez qu’une valeur n’est pas affectée à l’entrée ; sa présence est tout ce qui est nécessaire. Il s’agit d’une \_ valeur reg null.

```
HKEY_CLASSES_ROOT
   Applications
      example.exe
         IsHostApp
```

Si le processus lui-même ou le fichier de raccourci utilisé pour lancer le processus a une valeur AppUserModelID explicite, la liste des processus hôtes est ignorée et l’application est traitée comme une application normale par la barre des tâches. Les fenêtres d’application en cours d’exécution sont regroupées sous un seul bouton de la barre des tâches et l’application peut être épinglée à la barre des tâches.

Si seul le nom de l’exécutable du processus en cours d’exécution est connu, sans un AppUserModelID explicite, et que l’exécutable se trouve dans la liste des processus hôtes, chaque instance du processus est traitée comme une entité distincte pour le regroupement de la barre des tâches. Le bouton de la barre des tâches associé à une instance spécifique du processus n’affiche pas une option code confidentiel/désépingler ou une icône de lancement pour une nouvelle instance du processus. Le processus n’est pas non plus éligible pour l’inclusion dans la liste la plus fréquemment utilisée (MFU) du menu **Démarrer** . Toutefois, si le processus a été lancé à l’aide d’un raccourci contenant des arguments de lancement (généralement le contenu cible à héberger comme « application »), le système peut déterminer l’identité et l’application peut être épinglée et redémarrée.

## <a name="exclusion-lists-for-taskbar-pinning-and-recentfrequent-lists"></a>Listes d’exclusion pour l’épinglage de la barre des tâches et listes récentes/fréquentes

Les applications, les processus et les fenêtres peuvent choisir de ne pas être disponibles pour épingler à la barre des tâches ou d’être incluses dans la liste des programmes fréquemment utilisés du menu **Démarrer** . Pour ce faire, il existe trois mécanismes :

1.  Ajoutez l’entrée NoStartPage à l’inscription de l’application, comme indiqué ici :

    ```
    HKEY_CLASSES_ROOT
       Applications
          Example.exe
             NoStartPage
    ```

    Les données associées à l’entrée NoStartPage sont ignorées. Seule la présence de l’entrée est requise. Par conséquent, le type idéal pour NoStartPage est REG \_ None.

    Notez que toute utilisation d’une valeur AppUserModelID explicite remplace l’entrée NoStartPage. Si un AppUserModelID explicite est appliqué à un raccourci, à un processus ou à une fenêtre, il devient regroupement et éligible pour la liste MFU du menu **Démarrer** .

2.  Définissez la propriété [System. AppUserModel. PreventPinning](../properties/props-system-appusermodel-preventpinning.md) sur les fenêtres et les raccourcis. Cette propriété doit être définie sur une fenêtre avant la propriété de l’ID de groupe de [ \_ \_ sécurité AppUserModel](../properties/props-system-appusermodel-id.md) .
3.  Ajoutez un AppUserModelID explicite en tant que valeur sous la sous-clé de Registre suivante comme indiqué ici :

    ```
    HKEY_LOCAL_MACHINE
       Software
          Microsoft
             Windows
                CurrentVersion
                   Explorer
                      FileAssociation
                         NoStartPageAppUserModelIDs
                            AppUserModelID1
                            AppUserModelID2
                            AppUserModelID3
    ```

    Chaque entrée est une \_ valeur reg null avec le nom de AppUserModelID. Une AppUserModelID trouvée dans cette liste n’est pas regroupement et n’est pas éligible pour l’inclusion dans la liste des listes de **réutiliser** du menu Démarrer.

Sachez que certains fichiers exécutables ainsi que les raccourcis qui contiennent certaines chaînes dans leur nom sont automatiquement exclus de l’épinglage et de l’inclusion dans la liste des MFU.

> [!Note]  
> Cette exclusion automatique peut être remplacée en appliquant une AppUserModelID explicite.

 

Si l’une des chaînes suivantes, quelle que soit la casse, est incluse dans le nom du raccourci, le programme n’est pas regroupement et n’est pas affiché dans la liste des plus fréquemment utilisés (non applicable à Windows 10) :

-   Documentation
-   Aide
-   Installer
-   En savoir plus
-   Lisez-moi
-   Lire en premier
-   Fichier Lisezmoi
-   Supprimer
-   Installation
-   Assistance
-   Nouveautés

La liste de programmes suivante n’est pas regroupement et est exclue de la liste des plus fréquemment utilisés.

-   Applaunch.exe
-   Control.exe
-   Dfsvc.exe
-   Dllhost.exe
-   Guestmodemsg.exe
-   Hh.exe
-   Install.exe
-   Isuninst.exe
-   Lnkstub.exe
-   Mmc.exe
-   Mshta.exe
-   Msiexec.exe
-   Msoobe.exe
-   Rundll32.exe
-   Setup.exe
-   St5unst.exe
-   Unwise.exe
-   Unwise32.exe
-   Werfault.exe
-   Winhlp32.exe
-   Wlrmdr.exe
-   Wuapp.exe

Les listes précédentes sont stockées dans les valeurs de Registre suivantes.

> [!Note]  
> Ces listes ne doivent pas être modifiées par les applications. Utilisez l’une des méthodes de liste d’exclusion répertoriées précédemment pour la même expérience.

 

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows
            CurrentVersion
               Explorer
                  FileAssociation
                     AddRemoveApps
                     HostApps
```

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**SetCurrentProcessExplicitAppUserModelID**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-setcurrentprocessexplicitappusermodelid)
</dt> <dt>

[**GetCurrentProcessExplicitAppUserModelID**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-getcurrentprocessexplicitappusermodelid)
</dt> <dt>

[Extensions de la barre des tâches](taskbar-extensions.md)
</dt> <dt>

[**ICustomDestinationList::SetAppID**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icustomdestinationlist-setappid)
</dt> <dt>

[**IApplicationDocumentLists::SetAppID**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iapplicationdocumentlists-setappid)
</dt> <dt>

[**IApplicationDestinations::SetAppID**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iapplicationdestinations-setappid)
</dt> <dt>

[**SHGetPropertyStoreForWindow**](/windows/win32/api/shellapi/nf-shellapi-shgetpropertystoreforwindow)
</dt> </dl>

 

 
