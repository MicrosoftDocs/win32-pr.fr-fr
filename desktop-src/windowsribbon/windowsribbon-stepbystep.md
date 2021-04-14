---
title: Création d’une application de ruban
description: L’infrastructure du ruban Windows est composée de deux plateformes de développement distinctes, mais dépendantes, d’un langage de balisage basé sur Extensible Application Markup Language (XAML) pour déclarer des contrôles et leur disposition visuelle, et d’un jeu d’interfaces COM (Component Object Model) C++ pour définir les fonctionnalités de commande et les hooks d’application. Cette division de main-d’œuvre au sein de l’architecture de l’infrastructure du ruban requiert qu’un développeur qui souhaite tirer parti des fonctionnalités d’interface utilisateur enrichies offertes par l’infrastructure doive concevoir et décrire l’interface utilisateur dans le balisage, puis utiliser les interfaces COM de l’infrastructure du ruban pour connecter l’infrastructure à l’application hôte.
ms.assetid: 1bd3dbb5-822b-4551-8330-8b202a4cecdf
keywords:
- Ruban Windows, création d’applications
- Ruban, création d’applications
- Ruban Windows, feuille de route
- Ruban, feuille de route
- Ruban Windows, balisage
- Ruban, balisage
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0a10f683c7fbb07b9992e418a4c09dc9aecba280
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104382379"
---
# <a name="creating-a-ribbon-application"></a>Création d’une application de ruban

L’infrastructure du ruban Windows est composée de deux plates-formes de développement distinctes et dépendantes. il s’agit d’un langage de balisage basé sur Extensible Application Markup Language (XAML) pour déclarer des contrôles et leur disposition visuelle, ainsi qu’un ensemble d’interfaces COM (Component Object Model) C++ pour définir les fonctionnalités de commande et les hooks d’application. Cette division de main-d’œuvre au sein de l’architecture de l’infrastructure du ruban requiert qu’un développeur qui souhaite tirer parti des fonctionnalités d’interface utilisateur enrichies offertes par l’infrastructure doive concevoir et décrire l’interface utilisateur dans le balisage, puis utiliser les interfaces COM de l’infrastructure du ruban pour connecter l’infrastructure à l’application hôte.

-   [Feuille de route du ruban](#ribbon-roadmap)
-   [Écrire le balisage](#write-the-markup)
    -   [Compiler le balisage](#compile-the-markup)
-   [Générer l’application](#build-the-application)
    -   [Initialiser le ruban](#initialize-the-ribbon)
    -   [Lier le balisage à l’application](#link-the-markup-to-the-application)
    -   [Compiler l’application](#link-the-markup-to-the-application)
-   [Exécutions et mises à jour de l’heure d’exécution](#run-time-updates-and-executions)
-   [Prise en charge OLE](#ole-support)
-   [Rubriques connexes](#related-topics)

## <a name="ribbon-roadmap"></a>Feuille de route du ruban

Les aspects visuels d’une application de ruban, tels que les contrôles affichés et leur emplacement, sont déclarés dans le balisage (consultez [déclaration des commandes et des contrôles avec le balisage du ruban](windowsribbon-schema.md)). La logique de commande d’application, par exemple ce qui se produit quand un bouton est enfoncé, est implémentée dans le code.

Le processus d’implémentation d’un ruban et de son incorporation dans une application Windows requiert quatre tâches de base : écrire le balisage, compiler le balisage, écrire le code, compiler et lier l’application entière.

Le diagramme suivant illustre le flux de travail pour une implémentation de ruban typique.

![Diagramme montrant le flux de travail pour une implémentation de ruban typique.](images/overviews/ribbonroadmap.png)

Les sections suivantes décrivent ce processus plus en détail.

## <a name="write-the-markup"></a>Écrire le balisage

Une fois l’interface utilisateur du ruban conçue, la première tâche d’un développeur d’applications est de décrire l’interface utilisateur avec le balisage du ruban.

> [!IMPORTANT]
> Le fichier de schéma de balisage de Framework du ruban, UICC. xsd, est installé avec le kit de développement logiciel (SDK) Microsoft Windows pour Windows 7 et .NET Framework 4,0. À l’aide du chemin d’installation standard, le fichier se trouve dans le dossier% ProgramFiles% \\ Microsoft SDK numéro de la \\ \\ \[ version Windows \] \\ où il peut être référencé par de nombreux éditeurs XML pour fournir des indications et une saisie semi-automatique.

 

Les contrôles de ruban, les commandes de ruban (les éléments indépendants du contrôle qui fournissent les fonctionnalités de base pour les contrôles de ruban) et l’ensemble de la disposition de contrôle et des relations visuelles sont déclarés dans le balisage. La structure du balisage du ruban met l’accent sur la distinction entre les contrôles du ruban et les commandes via deux hiérarchies de nœuds principales : une arborescence [commandes et ressources](windowsribbon-reference-elements-command.md) et une arborescence des [vues](windowsribbon-reference-elements-view.md) .

Tous les conteneurs et actions qui sont exposés par le ruban sont déclarés dans l’arborescence [commandes et ressources](windowsribbon-reference-elements-command.md) . Chaque élément Command est associé à un ensemble de ressources, comme requis par la conception de l’interface utilisateur.

Une fois que vous avez créé les commandes pour une application, vous déclarez des contrôles dans l’arborescence des [vues](windowsribbon-reference-elements-view.md) et liez chaque contrôle à une commande pour exposer les fonctionnalités de commande. L’infrastructure du ruban détermine le positionnement réel des contrôles en fonction de la hiérarchie des contrôles déclarée ici.

L’exemple de code suivant montre comment déclarer un contrôle Button, étiqueté Exit application, et l’associer à une commande exit.


```
<Application xmlns="http://schemas.microsoft.com/windows/2009/Ribbon">
  <Application.Commands>
    <Command Name="cmdExit" LabelTitle="Exit application" />
  </Application.Commands>

  <Application.Views>
    <Ribbon>
      <Ribbon.Tabs>
        <Tab>
          <Group>
            <Button CommandName="cmdExit" />
          </Group>
        </Tab>
      </Ribbon.Tabs>
    </Ribbon>
  </Application.Views>
</Application>
        
```



> [!TIP]
> Bien qu’il soit possible d’utiliser n’importe quelle extension de nom de fichier pour le fichier de balisage du ruban,. xml est l’extension recommandée qui est utilisée dans la documentation.

 

### <a name="compile-the-markup"></a>Compiler le balisage

Une fois le fichier de balisage du ruban créé, il doit être compilé dans un format binaire par le compilateur de balisage du ruban, le compilateur de commandes d’interface utilisateur (UICC), qui est inclus dans le kit de développement logiciel (SDK) Windows. Une référence à ce fichier binaire est transmise à la méthode [**IUIFramework :: LoadUI**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-loadui) pendant l’initialisation de l’infrastructure du ruban par l’application hôte.

UICC peut être exécuté directement à partir d’une fenêtre de ligne de commande ou ajouté en tant qu’étape de génération personnalisée dans Visual Studio.

L’illustration suivante montre le compilateur de balisage UICC dans la fenêtre de l’interface de commande du kit de développement logiciel (SDK) Windows 7.

![capture d’écran montrant uicc.exe dans une fenêtre de ligne de commande.](images/overviews/screenshot-intentcl-commandline.png)

L’illustration suivante montre la UICC ajoutée en tant qu’étape de génération personnalisée dans Visual Studio.

![capture d’écran montrant uicc.exe ajouté comme étape de génération personnalisée dans Visual Studio.](images/overviews/screenshot-vs-intentcl-custombuildstep.png)

Le UICC génère trois fichiers : une version binaire du balisage (. BML), un en-tête de définition d’ID (fichier. h) pour exposer des éléments de balisage à l’application hôte du ruban, et un [script de définition de ressource](../menurc/about-resource-files.md) (fichier. RC) pour lier l’image de ruban et les ressources de type chaîne à l’application hôte au moment de la compilation.

Pour plus d’informations sur la compilation du balisage de l’infrastructure du ruban, consultez [compilation du balisage du ruban](windowsribbon-intentcl.md).

## <a name="build-the-application"></a>Générer l'application

Une fois que l’interface utilisateur préliminaire d’une application de ruban a été conçue et implémentée dans le balisage, le code d’application doit être écrit pour initialiser le Framework, consomme le balisage et lie les commandes déclarées dans le balisage aux gestionnaires de commandes appropriés dans l’application.

> [!IMPORTANT]
>
> Étant donné que l’infrastructure de ruban est basée sur COM, il est recommandé que les projets de ruban utilisent l' \_ \_ opérateur uuidof () pour référencer les GUID pour les interfaces d’infrastructure de ruban (IID). Dans les cas où il n’est pas possible d’utiliser l' \_ \_ opérateur uuidof (), par exemple lorsqu’un compilateur non-Microsoft est utilisé ou que l’application hôte est basée sur le langage C, les IID doivent être définis par l’application, car ils ne sont pas contenus dans UUID. lib.
>
> Si les IID sont définis par l’application, les GUID spécifiés dans UIRibbon. idl doivent être utilisés.
>
> UIRibbon. idl est fourni dans le cadre du [Kit de développement logiciel (SDK) Windows](https://msdn.microsoft.com/windows/bb980924.aspx) et se trouve dans le chemin d’installation standard de% ProgramFiles% \\ Microsoft SDK \\ Windows \\ v 7.0 \\ include.

 

### <a name="initialize-the-ribbon"></a>Initialiser le ruban

Le diagramme suivant illustre les étapes requises pour implémenter une application de ruban simple.

![Diagramme montrant les étapes requises pour implémenter une implémentation de ruban simple.](images/overviews/initializationsteps.png)

Les étapes suivantes décrivent en détail comment implémenter une application de ruban simple.

1.  CoCreateInstance

    L’application appelle la fonction COM CoCreateInstance standard avec l’ID de classe du Framework du ruban pour obtenir un pointeur vers le Framework.

    ```
    IUIFramework* pFramework = NULL;
    HRESULT hr = ::CoCreateInstance(
                CLSID_UIRibbonFramework, 
                NULL,
                CLSCTX_INPROC_SERVER, 
                IID_PPV_ARGS(&pFramework));
    if (FAILED(hr))
    {
      return hr;
    }
    ```

    

2.  Initialize (HWND, IUIApplication \* )

    L’application appelle [**IUIFramework :: Initialize**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-initialize), en passant deux paramètres : le handle vers la fenêtre de niveau supérieur qui contiendra le ruban et un pointeur vers l’implémentation de [**IUIApplication**](/windows/desktop/api/uiribbon/nn-uiribbon-iuiapplication) qui permet à l’infrastructure d’effectuer des rappels à l’application.

    > \[! Précieuse\]  
    > L’infrastructure du ruban est initialisée en tant que thread unique cloisonné (STA).

     

    ```
    hr = pFramework->Initialize(hWndHost, pApplication);
    if (FAILED(hr))
    {
      return hr;
    }
    ```

    

3.  LoadUI (instance, resourceName)

    L’application appelle [**IUIFramework :: LoadUI**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-loadui) pour lier la ressource de balisage. Le premier paramètre de cette fonction est un handle vers l’instance d’application du ruban. Le deuxième paramètre est le nom de la ressource de balisage binaire qui a été compilée précédemment. En passant le balisage binaire à l’infrastructure du ruban, l’application signale la structure du ruban et la façon dont les contrôles doivent être disposés. Il fournit également à l’infrastructure un manifeste de commandes à exposer (par exemple, coller, couper, Rechercher), qui sont utilisées par le Framework lorsqu’il effectue des rappels liés aux commandes au moment de l’exécution.

    ```
    hr = pFramework->LoadUI(GetModuleHandle(NULL), L"APPLICATION_RIBBON");
    if (FAILED(hr))
    {
      return hr;
    }
    ```

    

4.  Rappels [**IUIApplication :: OnCreateUICommand**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiapplication-oncreateuicommand)

    Une fois les étapes 1 à 3 terminées, l’infrastructure du ruban connaît les commandes à exposer dans le ruban. Toutefois, l’infrastructure a encore besoin de deux choses avant que le ruban soit entièrement fonctionnel : un moyen d’indiquer à l’application quand les commandes sont exécutées et un moyen d’obtenir des ressources de commande, ou des propriétés, au moment de l’exécution. Par exemple, si une zone de liste déroulante doit apparaître dans l’interface utilisateur, le Framework doit demander les éléments avec lesquels remplir la zone de liste déroulante.

    Ces deux fonctionnalités sont gérées par le biais de l’interface [**IUICommandHandler**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicommandhandler) . Plus précisément, pour chaque commande déclarée dans le balisage binaire (Voir l’étape 3 ci-dessus), l’infrastructure appelle [**IUIApplication :: OnCreateUICommand**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiapplication-oncreateuicommand) pour demander à l’application un objet **IUICommandHandler** pour cette commande.

    > [!Note]  
    > L’interface [**IUICommandHandler**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicommandhandler) permet de lier un gestionnaire de commandes à une ou plusieurs commandes.

     

Au minimum, l’application doit implémenter les stubs des méthodes [**IUIApplication**](/windows/desktop/api/uiribbon/nn-uiribbon-iuiapplication) qui retournent E \_ NOTIMPL, comme indiqué dans l’exemple suivant.


```
STDMETHOD(OnViewChanged)(UINT32 viewId,
                         UI_VIEWTYPE typeID,
                         IUnknown *view,
                         UI_VIEWVERB verb,
                         INT32 uReasonCode)
{ 
  return E_NOTIMPL; 
}

STDMETHOD(OnCreateUICommand)(UINT32 commandId,
                             UI_COMMANDTYPE typeID,
                             IUICommandHandler **commandHandler)
{ 
  return E_NOTIMPL; 
}

STDMETHOD(OnDestroyUICommand)(UINT32 commandId,
                              UI_COMMANDTYPE typeID,
                              IUICommandHandler *commandHandler) 
{ 
  return E_NOTIMPL; 
}
```



### <a name="link-the-markup-to-the-application"></a>Lier le balisage à l’application

À ce stade, les fichiers de ressources de balisage doivent être liés à l’application hôte en incluant une référence au fichier de définition de ressource de balisage (qui contient une référence au fichier d’en-tête de balisage) dans le fichier de ressources de l’application. Par exemple, une application appelée RibbonApp avec un fichier de ressources appelé ribbonUI. RC requiert la ligne suivante dans le fichier RibbonApp. rc.


```C++
#include "ribbonUI.rc"
```



En fonction du compilateur et de l’éditeur de liens utilisés, le script de définition de ressource peut également nécessiter une compilation avant que l’application du ruban puisse être compilée. L’outil en ligne de commande [du compilateur de ressources (RC)](../menurc/using-rc-the-rc-command-line-.md) fourni avec Microsoft Visual Studio et le SDK Windows peuvent être utilisés pour cette tâche.

### <a name="compile-the-application"></a>Compiler l’application

Une fois l’application de ruban compilée, elle peut être exécutée et l’interface utilisateur testée. Si l’interface utilisateur requiert une modification et qu’aucune modification n’est apportée aux gestionnaires de commandes associés dans le code d’application principal, modifiez le fichier source du balisage, recompilez le balisage avec UICC.exe et liez les nouveaux fichiers de ressources de balisage. Lorsque l’application est redémarrée, l’interface utilisateur modifiée est affichée.

Tout ceci est possible sans toucher au code d’application de base, ce qui est une amélioration significative par rapport au développement et à la distribution d’applications standard.

## <a name="run-time-updates-and-executions"></a>Exécutions et mises à jour de l’heure d’exécution

La structure de communication au moment de l’exécution de l’infrastructure du ruban est basée sur un push et un pull, ou un appelant bidirectionnel.

Ce modèle permet à l’infrastructure d’informer l’application lorsqu’une commande est exécutée et permet à l’infrastructure et à l’application d’interroger, de mettre à jour et d’invalider les valeurs de propriété et les ressources du ruban. Cette fonctionnalité est fournie par le biais d’un certain nombre d’interfaces et de méthodes.

L’infrastructure extrait les informations de propriété mises à jour à partir de l’application ruban par le biais de la méthode de rappel [**IUICommandHandler :: UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) . Un ID de commande et une clé de propriété, qui identifie la propriété de commande à mettre à jour, sont passés à la méthode qui retourne, ou envoie, une valeur pour cette clé de propriété au Framework.

L’infrastructure appelle [**IUICommandHandler :: Execute**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-execute) quand une commande est exécutée, en identifiant à la fois l’ID de commande et le type d’exécution qui se sont produits ([**UI \_ EXECUTIONVERB**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_executionverb)). C’est là que l’application spécifie la logique d’exécution d’une commande.

Le diagramme suivant illustre la communication au moment de l’exécution pour l’exécution des commandes entre l’infrastructure et l’application.

![Diagramme montrant un exemple de la communication au moment de l’exécution entre l’infrastructure du ruban et une application hôte.](images/overviews/updatesandexecutions.png)

> [!Note]  
> L’implémentation des fonctions [**IUICommandHandler :: UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) et [**IUICommandHandler :: Execute**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-execute) n’est pas nécessaire pour afficher initialement un ruban dans une application. Toutefois, ces méthodes sont nécessaires pour s’assurer que l’application fonctionne correctement lorsque les commandes sont exécutées par l’utilisateur.

 

## <a name="ole-support"></a>Prise en charge OLE

Une application de ruban peut être configurée en tant que serveur OLE pour prendre en charge l’activation OLE hors place.

Les objets créés dans une application serveur OLE conservent leur association avec l’application serveur lorsqu’ils sont insérés (collés ou placés) dans une application cliente OLE (ou un conteneur). Dans le cas d’une activation OLE hors place, le double-clic sur l’objet dans l’application cliente ouvre une instance dédiée de l’application serveur et charge l’objet pour modification. Lorsque l’application serveur est fermée, toutes les modifications apportées à l’objet sont reflétées dans l’application cliente.

> [!Note]  
> L’infrastructure du ruban ne prend pas en charge l’activation OLE sur place. Les objets créés dans un serveur OLE basé sur le ruban ne peuvent pas être modifiés à partir de l’application cliente OLE. Une instance dédiée externe de l’application serveur est requise.


## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Déclaration des commandes et des contrôles avec le balisage du ruban](./windowsribbon-schema.md)
</dt> <dt>

[Instructions relatives à l’expérience utilisateur du ruban](https://msdn.microsoft.com/library/cc872782.aspx)
</dt> <dt>

[Processus de conception du ruban](https://msdn.microsoft.com/library/cc872781.aspx)
</dt> </dl>

 

 




