---
title: présentation de l’infrastructure du ruban Windows
description: affichez la page d’accueil de l’infrastructure de ruban Windows, qui est une alternative aux menus superposés, aux barres d’outils et aux volets de tâches des applications Windows traditionnelles.
ms.assetid: bc19d5eb-e3a4-4022-8051-512cb3a3e065
keywords:
- Windows Ruban, infrastructure
- Ruban, infrastructure
- Windows Ruban, à propos de
- Ruban, à propos de
- Windows Ruban, composants
- Ruban, composants
- Windows Ruban, vues
- Ruban, vues
- Windows Ruban, architecture
- Ruban, architecture
- Windows Ruban, API
- Ruban, API
- Windows Ruban, sécurité
- Ruban, sécurité
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 65576d90abb68b0efddf850f4855633f4b362d8cb21ce6f6f85f7924085e8810
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117850640"
---
# <a name="introducing-the-windows-ribbon-framework"></a>présentation de l’infrastructure du ruban Windows

l’infrastructure du ruban Windows est un système de présentation de commande riche qui offre une alternative moderne aux menus en couches, aux barres d’outils et aux volets de tâches des applications Windows traditionnelles.

-   [Nouveau paradigme de commande](#a-new-command-paradigm)
-   [Views](#views)
    -   [Affichage du ruban](#the-ribbon-view)
    -   [Vue ContextPopup](#the-contextpopup-view)
-   [Architecture du ruban](#ribbon-architecture)
    -   [API du ruban](#the-ribbon-apis)
    -   [Sécurité et confidentialité](#security-and-privacy)
    -   [Accessibilité et localisation](#accessibility-and-localization)
-   [Conclusion](#conclusion)
-   [Rubriques connexes](#related-topics)

## <a name="a-new-command-paradigm"></a>Nouveau paradigme de commande

l’infrastructure du ruban est une collection d’api Microsoft Win32 qui prennent en charge un hôte de nouvelles fonctionnalités d’interface utilisateur pour les développeurs Windows.

Cette infrastructure de commande d’interface utilisateur riche et moderne offre les fonctionnalités suivantes :

-   Implémentation facile pour les nouvelles applications de Framework de ruban et la migration simple des applications Win32 existantes.
-   Apparence et comportement cohérents dans les applications du ruban.
-   respect des directives de l’interface utilisateur Windows pour une expérience Windows de première classe grâce aux normes d’accessibilité, à la prise en charge de style visuel (à thème), aux réglages à contraste élevé automatique et à la reconnaissance des points par pouce (dpi).

L’infrastructure du ruban se compose de deux composants d’interface utilisateur principaux :

-   Barre de commandes du ruban, qui est composée de la barre d’outils accès rapide (QAT) qui expose et met en surbrillance diverses commandes de ruban comme spécifié par l’utilisateur ou l’application, et une ligne d’onglet qui contient le menu d’application, des onglets standard ou contextuels et un bouton aide.
-   Système de menu contextuel enrichi.

Une combinaison d’interfaces COM natives et XML déclaratives est utilisée pour découpler la présentation et les fonctionnalités de ces composants.

## <a name="views"></a>Les vues

Les composants de l’interface utilisateur principale de l’infrastructure du ruban, la barre de commandes du ruban et le système de menu contextuel, sont différenciés de façon structurelle par le biais des *vues*. Le Framework prend en charge deux vues : la vue du [**ruban**](windowsribbon-element-ribbon.md) et la vue [**ContextPopup**](windowsribbon-element-contextpopup.md) .

### <a name="the-ribbon-view"></a>Affichage du ruban

l’interface utilisateur de la vue du [**ruban**](windowsribbon-element-ribbon.md) est la principale fonctionnalité de l’infrastructure du ruban et fournit l’expérience utilisateur de nouvelle génération pour la présentation des commandes dans Windows applications.

Le ruban est une barre de commandes qui expose les principales fonctionnalités d’une application via une série d’onglets en haut d’une fenêtre d’application. elle est similaire à la fonctionnalité et à l’apparence de l’interface utilisateur Microsoft Office 2007 Fluent. le ruban fournit un correspondants intuitif au processus d’évaluation et d’erreur de la découverte de commande, typique des systèmes de menus de Windows standard. Optimisé pour l’efficacité et la détectabilité, le ruban facilite la recherche, la compréhension et l’utilisation des commandes avec des clics de souris et des séquences de touches minimaux par le biais d’un système de contrôles standard, de galeries et d’un aperçu instantané.

l’image suivante illustre l’implémentation de l’infrastructure du ruban dans Paint pour Windows 7.

![capture d’écran montrant l’implémentation du ruban dans Paint pour Windows 7.](images/overviews/screenshot-paint-win7transparency-mirror.png)

### <a name="the-contextpopup-view"></a>Vue ContextPopup

la vue [**ContextPopup**](windowsribbon-element-contextpopup.md) , via le [contrôle contextuel](windowsribbon-controls-contextpopup.md) contextuel, fournit un système de menu contextuel plus riche que celui disponible avec les applications Windows antérieures. Une fenêtre contextuelle de contexte ne peut être déployée que pour la prise en charge d’un ruban. un popup de contexte autonome n’est pas pris en charge par l’infrastructure du ruban.

## <a name="ribbon-architecture"></a>Architecture du ruban

contrairement au modèle de développement d’interface utilisateur Windows basé sur les contrôles traditionnel, Windows le développement de l’interface utilisateur de l’infrastructure du ruban est basé sur le concept plus abstrait des commandes. En vous concentrant sur les commandes associées aux contrôles, plutôt que sur les contrôles eux-mêmes, le Framework est en mesure d’ajuster automatiquement l’interface utilisateur en fonction des besoins en réponse à l’état d’exécution de la commande récupéré à partir de l’application hôte du ruban.

Une application qui utilise l’infrastructure de ruban expose des commandes sans être engagées avec les détails de la façon dont cette commande est représentée dans l’interface utilisateur. C’est ce qu’on appelle parfois un modèle d’interface utilisateur basé sur des intentions. Le [**type de commande**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_commandtype), ses propriétés et ses ressources définissent l’objectif de la commande pour l’application. Par exemple, l’entrée de la souris, l’entrée au clavier ou l’agitation d’un appareil gyroscopique peuvent entraîner l’exécution de la même commande. l’application est uniquement concernée par l’exécution de la commande, et non par la manière dont elle a été appelée.

L’infrastructure du ruban offre cette flexibilité en séparant les fonctionnalités de la présentation avec deux structures de développement distinctes : un langage de balisage basé sur le Extensible Application Markup Language (XAML) pour déclarer des contrôles et la disposition visuelle d’une implémentation de ruban, ainsi que des interfaces basées sur COM C++ pour initialiser l’infrastructure et gérer les événements au moment de l’exécution. Cette distinction permet aux développeurs d’interface utilisateur et aux concepteurs de être uniquement responsables de l’apparence d’une application de ruban, tandis que les fonctionnalités principales restent le domaine des ingénieurs logiciels.

Pour plus d’informations, consultez [fonctionnement des commandes et des contrôles](windowsribbon-commandscontrols.md).

### <a name="the-ribbon-apis"></a>API du ruban

Les API de ruban fournissent les connexions nécessaires entre une vue et l’application hôte du ruban. Ces API se composent des interfaces et des clés de propriétés suivantes :

-   Ensemble d’interfaces COM implémentées par l’infrastructure du ruban pour exécuter les services d’interface utilisateur.

    

    | Interface                                                                        | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
    |----------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | [IUIContextualUI****](/windows/desktop/api/uiribbon/nn-uiribbon-iuicontextualui)           | Définit les méthodes pour les fonctionnalités principales de la vue [**ContextPopup**](windowsribbon-element-contextpopup.md) .                                                                                                                                                                                                                                                                                                                                                                                                                  |
    | [IUIFramework****](/windows/desktop/api/uiribbon/nn-uiribbon-iuiframework)                 | Définit les méthodes qui prennent en charge les fonctionnalités principales des vues [**Ribbon**](windowsribbon-element-ribbon.md) et [**ContextPopup**](windowsribbon-element-contextpopup.md) .                                                                                                                                                                                                                                                                                                                                                     |
    | [IUIRibbon****](/windows/desktop/api/uiribbon/nn-uiribbon-iuiribbon)                       | Définit les méthodes pour spécifier les paramètres et les propriétés d’une vue de [**ruban**](windowsribbon-element-ribbon.md) .                                                                                                                                                                                                                                                                                                                                                                                                                   |
    | [IUISimplePropertySet****](/windows/desktop/api/uiribbon/nn-uiribbon-iuisimplepropertyset) | Définit une méthode pour récupérer la valeur identifiée par une clé de propriété. Cette interface est implémentée par l’infrastructure du ruban et est également implémentée par l’application hôte pour chaque élément de l’objet [**IUICollection**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection) d’une galerie d’éléments.<br/> Lorsqu’elle est implémentée par l’application hôte, la méthode définie par cette interface est utilisée pour récupérer une valeur de clé de propriété pour l’élément sélectionné dans [**IUICollection**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection).<br/> |
    | [IUICollection****](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection)               | Définit les méthodes de manipulation dynamique des contrôles basés sur une collection, tels que les [galeries](ribbon-controls-galleries.md)de ruban et de collection, au moment de l’exécution.                                                                                                                                                                                                                                                                                                                                                        |
    | [IUIImage****](/windows/desktop/api/uiribbon/nn-uiribbon-iuiimage)                         | Définit la méthode pour récupérer une image à afficher dans l’interface utilisateur du ruban.                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
    | [IUIImageFromBitmap****](/windows/desktop/api/uiribbon/nn-uiribbon-iuiimagefrombitmap)     | Définit la méthode de fabrique pour la création d’un objet [**IUIImage**](/windows/desktop/api/uiribbon/nn-uiribbon-iuiimage) .                                                                                                                                                                                                                                                                                                                                                                                                                                 |

    

     

-   Ensemble d’interfaces COM implémentées par l’application hôte du ruban que l’infrastructure appelle en réponse aux modifications de l’interface utilisateur.

    

    | Interface                                                                                  | Description                                                                                                  |
    |--------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------|
    | [IUIApplication****](/windows/desktop/api/uiribbon/nn-uiribbon-iuiapplication)                       | Définit les méthodes de point d’entrée de rappel d’application pour l’infrastructure du ruban.                               |
    | [IUICommandHandler****](/windows/desktop/api/uiribbon/nn-uiribbon-iuicommandhandler)                 | Définit les méthodes de collecte des informations de commande et de gestion des événements de commande à partir de l’infrastructure du ruban. |
    | [IUICollectionChangedEvent****](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollectionchangedevent) | Définit la méthode requise pour gérer les modifications apportées à une collection au moment de l’exécution.                                   |

    

     

-   Ensemble de clés de propriété qui définissent les propriétés d’interface utilisateur sur lesquelles l’application a le contrôle par programmation.

    

    | Type de clé de propriété                                                  | Description                                              |
    |--------------------------------------------------------------------|----------------------------------------------------------|
    | [Collection](windowsribbon-reference-properties-collection.md)    | Définit des propriétés pour les contrôles basés sur une collection de ruban. |
    | [Sélecteur de couleurs](windowsribbon-reference-properties-colorpicker.md) | Définit des propriétés pour les contrôles de sélecteur de couleurs du ruban.     |
    | [Police](windowsribbon-reference-properties-fontcontrol.md)         | Définit des propriétés pour le ruban FontControl.           |
    | [Global](windowsribbon-reference-properties-framework.md)         | Définit les propriétés globales de l’infrastructure du ruban.      |
    | [Ressource](windowsribbon-reference-properties-resource.md)        | Définit les propriétés de ressource du ruban.                      |
    | [Ruban](windowsribbon-reference-properties-ribbon.md)            | Définit les propriétés d’affichage du ruban.                          |
    | [State](windowsribbon-reference-properties-state.md)              | Définit des propriétés pour l’état du contrôle de ruban ou le contexte.  |

    

     

### <a name="security-and-privacy"></a>Sécurité et confidentialité

La DLL de l’infrastructure du ruban (uiribbon.dll) s’exécute dans le processus et a les mêmes privilèges que l’application hôte. Le ruban accepte uniquement ce que l’application hôte fournit comme entrée d’entrée ou d’utilisateur à partir de contrôles étroitement limités tels que le compteur et la zone de liste modifiable modifiable.

en outre, le framework ne stocke pas définitivement les informations, à l’exception de ce qui est fourni par l’application hôte ou collectées (comme l’autorise l’utilisateur final) par le biais du programme de l’expérience utilisateur Windows.

### <a name="accessibility-and-localization"></a>Accessibilité et localisation

Pour fournir une interface utilisateur hautement accessible, l’infrastructure du ruban implémente Microsoft Active Accessibility. En remplissant automatiquement les propriétés de Active Accessibility Microsoft pertinentes à l’aide d’informations valides et utiles, l’infrastructure réduit considérablement la charge des développeurs pour fournir une expérience inclusive pour tous les utilisateurs.

pour plus d’informations sur l’accessibilité dans l’infrastructure du ruban, consultez [utilisation de Active Accessibility dans l’Interface utilisateur 2007 Office Fluent](/previous-versions/office/developer/office-2007/bb404170(v=office.12)).

en outre, l’infrastructure du ruban est une fonctionnalité Windows et, par conséquent, est localisée pour tous les langages que Windows prend en charge. Toutefois, les développeurs sont responsables de la localisation de leurs propres ressources d’application spécifiques.

## <a name="conclusion"></a>Conclusion

Le ruban est une nouvelle forme de présentation de commande que les développeurs d’applications, les architectes et les concepteurs doivent prendre en compte lors de la conception et de la création de nouvelles applications ou de la mise à jour d’applications existantes.

le [Forum de développement Windows ruban](https://social.msdn.microsoft.com/Forums/windowsdesktop/home?forum=windowsribbondevelopment) est disponible pour discuter des sujets et poser des questions relatives au développement d’applications qui implémentent l’infrastructure de ruban Windows.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Déclaration des commandes et des contrôles avec le balisage du ruban](windowsribbon-schema.md)
</dt> <dt>

[Instructions relatives à l’expérience utilisateur du ruban](https://msdn.microsoft.com/library/cc872782.aspx)
</dt> <dt>

[Processus de conception du ruban](https://msdn.microsoft.com/library/cc872781.aspx)
</dt> </dl>

 

