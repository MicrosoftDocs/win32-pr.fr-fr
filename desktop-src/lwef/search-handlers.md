---
title: Création de gestionnaires de recherche
description: L’interpréteur de commandes prend en charge plusieurs utilitaires de recherche qui permettent aux utilisateurs de localiser des objets d’espace de noms tels que des fichiers ou des imprimantes. Vous pouvez créer un moteur de recherche personnalisé et le mettre à la disposition des utilisateurs en implémentant et en inscrivant un gestionnaire de recherche.
ms.assetid: ffd023bb-16ab-43ce-b00b-5e32656c8013
keywords:
- gestionnaires de recherche
- inscrire, gestionnaires de recherche
- gestionnaires de recherche statiques
- Register, gestionnaires de recherche statiques
- gestionnaires de recherche dynamique
- inscription, gestionnaires de recherche dynamique
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e6476109302a176822137747353b2762b0caea8a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127413076"
---
# <a name="creating-search-handlers"></a>Création de gestionnaires de recherche

\[cette fonctionnalité est prise en charge uniquement sous Windows XP ou version antérieure. utilisez plutôt Windows Search.\]

L’interpréteur de commandes prend en charge plusieurs utilitaires de recherche qui permettent aux utilisateurs de localiser des objets d’espace de noms tels que des fichiers ou des imprimantes. Vous pouvez créer un moteur de recherche personnalisé et le mettre à la disposition des utilisateurs en implémentant et en inscrivant un *Gestionnaire de recherche*.

Les procédures générales d’implémentation et d’inscription d’un gestionnaire d’extensions de Shell sont décrites dans [création de gestionnaires d’extensions de Shell](/windows/desktop/shell/handlers). Ce document se concentre sur les aspects de l’implémentation qui sont spécifiques aux gestionnaires de recherche.

-   [Fonctionnement des gestionnaires de recherche](#how-search-handlers-work)
-   [Inscription des gestionnaires de recherche](#registering-search-handlers)
    -   [Inscription d’un gestionnaire de recherche statique](#registering-a-static-search-handler)
    -   [Inscription d’un gestionnaire de recherche dynamique](#registering-a-dynamic-search-handler)
-   [Implémentation de gestionnaires de recherche](#implementing-search-handlers)

## <a name="how-search-handlers-work"></a>Fonctionnement des gestionnaires de recherche

Les utilisateurs ont deux moyens de sélectionner un moteur de recherche. la première consiste à partir de la menu Démarrer. avec les systèmes antérieurs à Windows 2000, la sélection de la commande **rechercher** dans le menu **démarrer** affiche un sous-menu des moteurs de recherche disponibles. avec Windows 2000 et versions ultérieures, la commande **rechercher** du menu de la **saint**-art est renommée rechercher. l’illustration suivante montre le bouton de **recherche** sur un système Windows XP.

![sous-menu Rechercher du menu Démarrer](images/searchhandler1.jpg)

les utilisateurs peuvent également lancer une recherche à partir de Windows Explorer. sur les systèmes antérieurs à Windows 2000, ils cliquent sur la commande **rechercher** du menu **outils** pour afficher essentiellement le même menu que celui associé au menu **démarrer** . toutefois, Windows Explorer pour Windows 2000 gère les moteurs de recherche d’une manière très différente. Au lieu de gérer les moteurs de recherche en tant que sous-menu du menu **Outils** , il existe désormais un bouton de **recherche** dans la barre d’outils. Cliquez sur ce bouton pour ouvrir le volet de **recherche** de la barre d’explorateur. L’illustration suivante montre le volet **de recherche Rechercher des fichiers et des dossiers** .

![volet de recherche de la barre d’Explorateur Windows](images/searchhandler2.jpg)

il existe un certain nombre de différences dans la façon dont Windows 2000 et les systèmes antérieurs gèrent les gestionnaires de recherche qui affectent à la fois l’implémentation et l’inscription.



| pré-Windows 2000                                                                                                                                                                                                       | Windows 2000 et versions ultérieures                                                                                                                                                                                                                                                                                            |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Les gestionnaires de recherche sont implémentés en tant que type de [Gestionnaire de menu contextuel](/windows/desktop/shell/context-menu-handlers).                                                                                                                     | Les gestionnaires de recherche peuvent être implémentés en tant que gestionnaires de menus contextuels ou en tant que documents HTML dynamiques (DHTML).                                                                                                                                                                                                               |
| Les gestionnaires de recherche peuvent être statiques ou dynamiques. Les gestionnaires statiques sont chargés uniquement lorsqu’ils sont sélectionnés par l’utilisateur. Les gestionnaires dynamiques sont chargés par le shell au démarrage et ne se terminent pas tant que le shell n’est pas fermé. | Les gestionnaires implémentés en tant que gestionnaires de menu contextuel peuvent être statiques ou dynamiques. Les gestionnaires implémentés en tant que documents DHTML doivent être statiques.                                                                                                                                                                           |
| les gestionnaires de recherche s’affichent dans le sous-menu **rechercher** du menu **démarrer** et dans le sous-menu **rechercher** du menu **outils** de Windows Explorer.                                                                                  | Les gestionnaires de recherche s’affichent uniquement dans le sous-menu **Rechercher** du menu **Démarrer** . pour rendre un volet de recherche personnalisé disponible par le biais de la barre de menus Windows Explorer, vous devez l’implémenter en tant qu' [objet de bande](/previous-versions/windows/desktop/legacy/cc144099(v=vs.85)). elle est ensuite listée dans le sous-menu du **volet d’exploration** du menu **affichage** de Windows explorer. |



 

## <a name="registering-search-handlers"></a>Inscription des gestionnaires de recherche

Les gestionnaires de recherche sont inscrits sous la sous-clé **FindExtensions** du type de fichier.

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows
            CurrentVersion
               Explorer
                  FindExtensions
```

À partir de ce point, la procédure d’inscription varie selon que le gestionnaire doit être statique ou dynamique. Pour obtenir une présentation générale de l’inscription des gestionnaires d’extensions de Shell, consultez [création de gestionnaires d’extensions de Shell](/windows/desktop/shell/handlers).

### <a name="registering-a-static-search-handler"></a>Inscription d’un gestionnaire de recherche statique

Les gestionnaires de recherche statiques sont chargés uniquement lorsqu’ils sont lancés par l’utilisateur. Cette approche fonctionne mieux pour les dll de petite taille qui peuvent être chargées rapidement. Si vous utilisez DHTML pour implémenter votre gestionnaire, il doit être statique. Pour inscrire un gestionnaire d’extensions statiques, créez une sous-clé nommée pour le gestionnaire sous la sous-clé **statique** de la sous-clé **FindExtensions** . Le nom n’est pas utilisé par le système, mais il ne doit pas être identique aux autres noms de gestionnaires de recherche sous la sous-clé **FindExtensions** .

### <a name="shortcut-menu-based-search-handlers"></a>Gestionnaires de recherche basés sur des menus contextuels

Si votre gestionnaire est implémenté en tant que [Gestionnaire de menu contextuel](/windows/desktop/shell/context-menu-handlers), définissez la valeur par défaut de la sous-clé de nom du gestionnaire sur le GUID de l’identificateur de classe (CLSID) de l’objet. Sous la sous-clé Name du gestionnaire, créez une sous-clé nommée **0** (zéro) et définissez sa valeur par défaut sur la chaîne qui sera affichée dans le sous-menu **Rechercher** ou **Rechercher** . Vous pouvez activer les raccourcis clavier de la manière habituelle, en faisant précéder le caractère de raccourci d’une esperluette (&). Vous pouvez afficher une petite icône facultative à droite du texte du menu en créant une sous-clé **DefaultIcon** sous la sous-clé **0** . Définissez sa valeur par défaut sur une chaîne contenant le chemin d’accès du fichier contenant l’icône, suivi d’une virgule, puis de l’index de base zéro de l’icône.

L’exemple suivant enregistre le gestionnaire de recherche **MySearchEngine** . Le texte du menu est « mon moteur de recherche », avec M spécifié comme touche de raccourci. L’icône se trouve dans C : \\ MyDir \\MySearch.dll, avec un index de 2.

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows
            CurrentVersion
               Explorer
                  FindExtensions
                     Static
                        MySearchEngine
                           (Default) = {MySearchEngine CLSID GUID}
                           0
                              (Default) = &My Search Engine
                              DefaultIcon
                                 (Default) = c:\MyDir\MySearch.dll,2
```

### <a name="dhtml-based-search-handlers"></a>Gestionnaires de recherche DHTML

avec Windows 2000, vous pouvez également implémenter un gestionnaire de recherche en tant que document DHTML. Son nom est indiqué dans le sous-menu **Rechercher** du menu **Démarrer** . lorsque l’utilisateur le sélectionne, il lance Windows explorer avec la barre d’exploration ouverte dans le document de recherche. Vous pouvez également spécifier un document DHTML à afficher à droite du volet d’exploration. Il n’existe aucun moyen de lancer un autre gestionnaire à partir du volet de recherche par défaut. les moteurs de recherche peuvent être lancés directement à partir de Windows Explorer, mais uniquement s’ils sont implémentés en tant qu' [objets de bande](/previous-versions/windows/desktop/legacy/cc144099(v=vs.85)).

Pour inscrire un gestionnaire de recherche DHTML, définissez la sous-clé de nom du gestionnaire sur la forme de chaîne du CLSID \_ ShellSearchExt (actuellement {169A0691-8DF9-11D1-A1C4-00C04FD75D13}) et créez les sous-clés suivantes.

1.  Créez une sous-clé **0**(zéro) sous la sous-clé du nom du gestionnaire et définissez sa valeur par défaut sur le texte du menu.
2.  Pour qu’une icône s’affiche en regard du texte du menu, créez une sous-clé **DefaultIcon** sous **0** et définissez sa valeur par défaut sur le chemin d’accès et l’index de l’icône.
3.  Créez une sous-clé **SearchGUID** sous **0**. Attribuez un GUID au document DHTML et définissez la valeur par défaut de **SearchGUID** sur son format de chaîne. Ce GUID n’a pas besoin d’être inscrit sous le **\_ \_ \\ CLSID racine de la classe HKEY**.
4.  Créez une sous-clé d' **URL** sous **SearchGUID**. Définissez sa valeur par défaut sur le chemin d’accès du document HTML qui s’affichera dans le volet d’exploration.
5.  Créez une sous-clé **UrlNavNew** sous **SearchGUID**. Définissez sa valeur par défaut sur le chemin d’accès du document HTML qui s’affiche à droite du volet d’exploration.

L’exemple suivant enregistre le gestionnaire de recherche **MySearchEngine** implémenté en tant que document DHTML. Le texte du menu est « mon moteur de recherche », avec M spécifié comme touche de raccourci. L’icône se trouve dans C : \\ MyDir \\MySearch.dll, avec un index de 2. Le document DHTML de la barre d’exploration est C : \\ MyDir \\MySearch.htm et le document qui s’affiche à droite de la barre d’exploration est c : \\ mydir \\MySearchPage.htm.

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows
            CurrentVersion
               Explorer
                  FindExtensions
                     Static
                        MySearchEngine
                           (Default) = {169A0691-8DF9-11d1-A1C4-00C04FD75D13}
                           0
                              (Default) = &My Search Engine
                              DefaultIcon
                                 (Default) = c:\MyDir\MySearch.dll,2
                                 SearchGUID
                                    (Default) = {My Search GUID}
                                    Url
                                       (Default) = C:\MyDir\MySearch.htm
                                    UrlNavNew
                                       (Default) = C:\MyDir\MySearchPage.htm
```

### <a name="registering-a-dynamic-search-handler"></a>Inscription d’un gestionnaire de recherche dynamique

Si votre gestionnaire est implémenté en tant que [Gestionnaire de menu contextuel](/windows/desktop/shell/context-menu-handlers), vous pouvez également l’inscrire en tant que gestionnaire dynamique. Dans ce cas, il est chargé avec l’interpréteur de commandes et se termine uniquement lorsque l’interpréteur de commandes se termine. Les gestionnaires de recherche dynamique répondent bien plus rapidement que les gestionnaires statiques lorsqu’ils sont lancés par l’utilisateur. Cette approche fonctionne mieux si le chargement de la DLL de votre gestionnaire peut prendre beaucoup de temps, ou s’il est probable qu’elle est souvent appelée.

Les gestionnaires de recherche dynamique sont inscrits sous la sous-clé **FindExtensions** .

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows
            CurrentVersion
               Explorer
                  FindExtensions
```

Créez une sous-clé de **FindExtensions** nommée pour le gestionnaire et définissez sa valeur par défaut sur le GUID CLSID du gestionnaire. Les icônes de menu ne sont pas prises en charge pour les gestionnaires de recherche dynamique. L’exemple suivant inscrit MySearchEngine en tant que gestionnaire de recherche dynamique.

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows
            CurrentVersion
               Explorer
                  FindExtensions
                     MySearchEngine
                        (Default) = {MySearchEngine CLSID GUID}
                        0
                           (Default) = &My Search Engine
```

Contrairement aux gestionnaires de recherche statique, vous ne spécifiez pas le texte de menu dans le registre. Lorsque le gestionnaire est chargé, l’interpréteur de commandes appelle la méthode [**IContextMenu :: QueryContextMenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu) du gestionnaire pour ajouter des éléments au sous-menu **Rechercher** ou **Rechercher** .

## <a name="implementing-search-handlers"></a>Implémentation de gestionnaires de recherche

Les gestionnaires de recherche peuvent être implémentés en tant que gestionnaires de menus contextuels pour toutes les versions de Windows. pour Windows 2000, elles peuvent également être implémentées en tant que documents DHTML.

Pour obtenir une présentation générale de l’implémentation des gestionnaires de menus contextuels, consultez [création de gestionnaires de menus contextuels](/windows/desktop/shell/context-menu-handlers). Les gestionnaires de recherche diffèrent des gestionnaires de menus contextuels standard de plusieurs façons.

Pour les gestionnaires de menus statiques, le sous-menu **Rechercher** ou **Rechercher** est créé à partir des informations contenues dans le registre. Il n’est pas nécessaire que le gestionnaire ajoute un élément de menu, comme le ferait un gestionnaire de menu contextuel normal. L’interpréteur de commandes gère les gestionnaires de menus statiques de la façon suivante.

-   Lorsque l’utilisateur lance l’élément de menu du gestionnaire, le shell charge la DLL du gestionnaire et appelle [**IContextMenu :: commande InvokeCommand**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-invokecommand) pour indiquer au gestionnaire de lancer le moteur de recherche. Les méthodes [**IShellExtInit :: Initialize**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellextinit-initialize) et [**IContextMenu :: QueryContextMenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu) ne sont pas appelées.
-   Quand [**IContextMenu :: commande InvokeCommand**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-invokecommand) est appelé, le membre **lpVerb** de la structure [**CMINVOKECOMMANDINFO**](/windows/desktop/api/shobjidl_core/ns-shobjidl_core-cminvokecommandinfo) qui est passé identifie la commande. Le mot de poids faible de **lpVerb** est défini sur l’équivalent numérique du nom de la sous-clé de la commande. Étant donné que cette sous-clé est normalement nommée **0**, **lpVerb** est généralement défini sur zéro. Le gestionnaire doit ensuite lancer le moteur de recherche.

Les gestionnaires de recherche dynamique sont implémentés à peu près de la même façon que les gestionnaires de menus contextuels normaux. L’exception principale est que lorsque [**IShellExtInit :: Initialize**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellextinit-initialize) est appelé, les arguments *pidlFolder* et *lpdobj* ont la valeur **null**.

Les gestionnaires de recherche DHTML sont implémentés en tant que document DHTML normal. ils peuvent inclure des technologies HTML, DHTML ou de script qui sont prises en charge par Windows Internet Explorer.

 

 