---
title: Implémenter un fournisseur UI Automation Server-Side
description: Cette rubrique explique comment implémenter un fournisseur UI Automation côté serveur pour un contrôle personnalisé écrit en C++.
ms.assetid: c3a919b2-8b8c-4dde-ad71-587f3845a9f5
keywords:
- UI Automation, implémentation du fournisseur côté serveur
- UI Automation, implémentation du fournisseur
- UI Automation, implémenter des fournisseurs côté serveur
- UI Automation, implémenter des fournisseurs
- fournisseurs côté serveur, implémentation
- fournisseurs côté serveur, interfaces
- fournisseurs côté serveur, valeurs de propriété
- fournisseurs côté serveur, événements
- fournisseurs côté serveur, affectation d’un nouveau parent
- événements, fournisseurs côté serveur
- interfaces, fournisseurs côté serveur
- fournisseurs, implémenter
- implémentation de fournisseurs côté serveur
- implémenter des fournisseurs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e7fafbb9d03a25eb2e4713330c0622c25d17f9ff
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "106510697"
---
# <a name="implement-a-server-side-ui-automation-provider"></a>Implémenter un fournisseur UI Automation Server-Side

Cette rubrique explique comment implémenter un fournisseur UI Automation côté serveur pour un contrôle personnalisé écrit en C++. Il contient les sections suivantes :

-   [Interfaces de fournisseur](#provider-interfaces)
-   [Fonctionnalités requises pour les fournisseurs UI Automation](#required-functionality-for-ui-automation-providers)
-   [Valeurs de propriété](#property-values)
-   [Événements des fournisseurs](#events-from-providers)
-   [Navigation du fournisseur](#provider-navigation)
-   [Affectation d’un nouveau parent](#assigning-a-new-parent)
-   [Repositionnement du fournisseur](#provider-repositioning)
-   [Déconnexion des fournisseurs](#disconnecting-providers)
-   [Rubriques connexes](#related-topics)

Pour obtenir des exemples de code qui montrent comment implémenter des fournisseurs côté serveur, consultez [les rubriques de procédures pour les fournisseurs UI Automation](uiauto-howto-topics-for-uiautomation-providers.md).

## <a name="provider-interfaces"></a>Interfaces de fournisseur

Les interfaces COM (Component Object Model) suivantes fournissent des fonctionnalités pour les contrôles personnalisés. Pour fournir des fonctionnalités de base, chaque fournisseur UI Automation doit implémenter au moins l’interface [**IRawElementProviderSimple**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementprovidersimple) . Les interfaces [**IRawElementProviderFragment**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementproviderfragment) et [**IRawElementProviderFragmentRoot**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementproviderfragmentroot) sont facultatives, mais doivent être implémentées pour les éléments d’un contrôle complexe afin de fournir des fonctionnalités supplémentaires.



| Interface                                                                         | Description                                                                                                                                                                   |
|-----------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IRawElementProviderSimple**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementprovidersimple)             | Fournit des fonctionnalités de base pour un contrôle hébergé dans une fenêtre, notamment la prise en charge des modèles de contrôle et des propriétés.                                                         |
| [**IRawElementProviderFragment**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementproviderfragment)         | Ajoute des fonctionnalités pour un élément dans un contrôle complexe, notamment la navigation dans le fragment, la définition du focus et le retour du rectangle englobant de l’élément.             |
| [**IRawElementProviderFragmentRoot**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementproviderfragmentroot) | Ajoute des fonctionnalités pour l'élément racine d'un contrôle complexe, y compris la localisation d'un élément enfant à des coordonnées spécifiées et la définition de l'état du focus pour l'ensemble du contrôle. |



 

> [!Note]  
> Dans l’API UI Automation pour le code managé, ces interfaces forment une hiérarchie d’héritage. Ce n’est pas le cas en C++, où les interfaces sont complètement séparées.

 

Les interfaces suivantes fournissent des fonctionnalités supplémentaires, mais l’implémentation est facultative.



| Interface                                                                         | Description                                                                             |
|-----------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------|
| [**IRawElementProviderAdviseEvents**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementprovideradviseevents) | Permet au fournisseur de suivre des demandes pour des événements.                                      |
| [**IRawElementProviderHwndOverride**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementproviderhwndoverride) | Active le repositionnement d’éléments basés sur une fenêtre dans l’arborescence UI Automation d’un fragment. |



 

## <a name="required-functionality-for-ui-automation-providers"></a>Fonctionnalités requises pour les fournisseurs UI Automation

Pour communiquer avec UI Automation, votre contrôle doit implémenter les principaux domaines de fonctionnalités décrits dans le tableau suivant.



| Fonctionnalités                                              | Implémentation                                                                                                                                                                                                                                                                                                |
|------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Exposer le fournisseur à UI Automation.                      | En réponse à un message [**WM \_ GETOBJECT**](wm-getobject.md) envoyé à la fenêtre de contrôle, retournez l’objet qui implémente [**IRawElementProviderSimple**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementprovidersimple). Pour les fragments, il doit s’agir du fournisseur pour la racine du fragment.                                           |
| Fournissez des valeurs de propriété.                                   | Implémentez [**IRawElementProviderSimple :: GetPropertyValue**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementprovidersimple-getpropertyvalue) pour fournir ou substituer des valeurs.                                                                                                                                                             |
| Permet au client d’interagir avec le contrôle.            | Implémentez des interfaces qui prennent en charge chaque modèle de contrôle approprié, tel que [**IInvokeProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iinvokeprovider). Retournez ces fournisseurs de modèles de contrôle dans votre implémentation de [**IRawElementProviderSimple :: GetPatternProvider**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementprovidersimple-getpatternprovider). |
| Déclencher des événements.                                              | [**UiaRaiseAutomationEvent**](/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiaraiseautomationevent), méthodes de [**IProxyProviderWinEventSink**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iproxyproviderwineventsink).                                                                                                                                                |
| Activer la navigation et le focus dans un fragment.              | Implémentez [**IRawElementProviderFragment**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementproviderfragment) pour chaque élément du fragment. Non nécessaire pour les éléments qui ne font pas partie d’un fragment.                                                                                                                         |
| Activer le focus et la localisation des éléments enfants dans un fragment. | Implémentez [**IRawElementProviderFragmentRoot**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementproviderfragmentroot). Non nécessaire pour les éléments qui ne sont pas des racines de fragment.                                                                                                                                                          |



 

## <a name="property-values"></a>Valeurs de la propriété

Les fournisseurs UI Automation pour les contrôles personnalisés doivent prendre en charge certaines propriétés qui peuvent être utilisées par UI Automation et par les applications clientes. Pour les éléments hébergés dans Windows, UI Automation peut récupérer certaines propriétés du fournisseur de fenêtre par défaut, mais doit en obtenir d’autres à partir du fournisseur personnalisé.

En règle générale, les fournisseurs pour les contrôles basés sur des fenêtres n’ont pas besoin de fournir les propriétés suivantes qui sont identifiées par **PROPERTYID**:

-   [**UIA \_ BoundingRectanglePropertyId**](uiauto-automation-element-propids.md)
-   [**UIA \_ ClickablePointPropertyId**](uiauto-automation-element-propids.md)
-   [**UIA \_ ProcessIdPropertyId**](uiauto-automation-element-propids.md)
-   [**UIA \_ ClassNamePropertyId**](uiauto-automation-element-propids.md)
-   [**UIA \_ HasKeyboardFocusPropertyId**](uiauto-automation-element-propids.md)
-   [**UIA \_ IsEnabledPropertyId**](uiauto-automation-element-propids.md)
-   [**UIA \_ IsKeyboardFocusablePropertyId**](uiauto-automation-element-propids.md)
-   [**UIA \_ IsPasswordPropertyId**](uiauto-automation-element-propids.md)
-   [**UIA \_ NamePropertyId**](uiauto-automation-element-propids.md)
-   [**UIA \_ RuntimeIdPropertyId**](uiauto-automation-element-propids.md)

La propriété RuntimeId d’un élément simple ou d’une racine de fragment hébergée dans une fenêtre est obtenue à partir de la fenêtre. Toutefois, les éléments fragments situés sous la racine, tels que les éléments de liste dans une zone de liste, doivent fournir leurs propres identificateurs. Pour plus d’informations, consultez [**IRawElementProviderFragment :: GetRuntimeId**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementproviderfragment-getruntimeid).

La propriété IsKeyboardFocusable doit être retournée pour les fournisseurs hébergés dans un contrôle Windows Forms. Dans ce cas, le fournisseur de fenêtre par défaut ne pourra peut-être pas récupérer la bonne valeur.

La propriété Name est généralement fournie par le fournisseur hôte.

## <a name="events-from-providers"></a>Événements des fournisseurs

Les fournisseurs UI Automation doivent déclencher des événements pour informer les applications clientes des modifications de l’état de l’interface utilisateur. Les fonctions suivantes sont utilisées pour déclencher des événements.



| Fonction                                                                                   | Description                                                                                                              |
|--------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------|
| [**UiaRaiseAutomationEvent**](/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiaraiseautomationevent)                  | Déclenche différents événements, y compris les événements déclenchés par les modèles de contrôle.                                                   |
| [**UiaRaiseAutomationPropertyChangedEvent**](/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiaraiseautomationpropertychangedevent) | Déclenche un événement lorsqu’une propriété UI Automation a changé.                                                               |
| [**UiaRaiseStructureChangedEvent**](/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiaraisestructurechangedevent)      | Déclenche un événement lorsque la structure de l’arborescence UI Automation a changé, par exemple en supprimant ou en ajoutant un élément. |



 

L’objectif d’un événement est d’informer le client d’un événement qui se produit dans l’interface utilisateur. Les fournisseurs doivent déclencher un événement que la modification ait été déclenchée par l’utilisateur ou par une application cliente à l’aide d’UI Automation. Par exemple, l’événement identifié par [**UIA \_ Invoke \_ InvokedEventId**](uiauto-event-ids.md) doit être déclenché chaque fois que le contrôle est appelé, via une entrée d’utilisateur directe ou par l’application cliente appelant [**IUIAutomationInvokePattern :: Invoke**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationinvokepattern-invoke).

Pour optimiser les performances, un fournisseur peut déclencher des événements de manière sélective ou ne pas en déclencher du tout si aucune application cliente n'est enregistrée pour les recevoir. Les éléments d’API suivants sont utilisés pour l’optimisation.



| Élément API                                                                       | Description                                                                                                                                                       |
|-----------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**UiaClientsAreListening**](/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiaclientsarelistening)           | Cette fonction vérifie si des applications clientes sont abonnées à des événements UI Automation.                                                                 |
| [**IRawElementProviderAdviseEvents**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementprovideradviseevents) | L’implémentation de cette interface sur une racine de fragment permet au fournisseur d’être informé lorsque les clients enregistrent et annulent l’inscription des gestionnaires d’événements pour les événements sur le fragment. |



 

> [!Note]  
> À l’instar de l’implémentation du décompte de références dans la programmation COM, il est important que les fournisseurs UI Automation traitent les méthodes [**IRawElementProviderAdviseEvents :: AdviseEventAdded**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementprovideradviseevents-adviseeventadded) et [**AdviseEventRemoved**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementprovideradviseevents-adviseeventremoved) comme les méthodes [**IUnknown :: AddRef**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-addref) et [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) de l’interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . Tant que **AdviseEventAdded** a été appelé plus de fois que **AdviseEventRemoved** pour un événement ou une propriété spécifique, le fournisseur doit continuer à déclencher des événements correspondants, car certains clients continuent d’écouter. Les fournisseurs UI Automation peuvent également utiliser la fonction [**UiaClientsAreListening**](/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiaclientsarelistening) pour déterminer si au moins un client écoute et, le cas échéant, déclencher tous les événements appropriés.

 

## <a name="provider-navigation"></a>Navigation du fournisseur

Les fournisseurs pour les contrôles simples, tels qu’un bouton personnalisé hébergé dans une fenêtre, n’ont pas besoin de prendre en charge la navigation dans l’arborescence UI Automation. La navigation vers et depuis l’élément est gérée par le fournisseur par défaut de la fenêtre hôte, qui est spécifié dans l’implémentation de [**IRawElementProviderSimple :: HostRawElementProvider**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementprovidersimple-get_hostrawelementprovider). Quand vous implémentez un fournisseur pour un contrôle personnalisé complexe, vous devez toutefois prendre en charge la navigation entre le nœud racine du fragment et ses descendants, et entre nœuds frères.

> [!Note]  
> Les éléments d’un fragment autre que la racine doivent retourner la **valeur null** à partir de [**HostRawElementProvider**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementprovidersimple-get_hostrawelementprovider), car ils ne sont pas hébergés directement dans une fenêtre et aucun fournisseur par défaut ne peut prendre en charge la navigation vers et à partir de ceux-ci.

 

La structure du fragment est déterminée par votre implémentation de [**IRawElementProviderFragment :: Navigate**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementproviderfragment-navigate). Pour chaque direction possible à partir de chaque fragment, cette méthode retourne l'objet fournisseur de l'élément dans cette direction. S’il n’y a aucun élément dans cette direction, la méthode retourne la **valeur null**.

La racine du fragment ne prend en charge la navigation que vers les éléments enfants. Par exemple, une zone de liste retourne le premier élément de la liste lorsque la direction est **NavigateDirection \_ firstChild**, et retourne le dernier élément lorsque la direction est **NavigateDirection \_ LastChild**. La racine du fragment ne prend pas en charge la navigation vers un parent ou des frères. Cela est géré par le fournisseur de fenêtre hôte.

Les éléments d'un fragment qui ne sont pas la racine doivent prendre en charge la navigation vers le parent et tous leurs frères et enfants.

## <a name="assigning-a-new-parent"></a>Affectation d’un nouveau parent

Les fenêtres indépendantes sont en fait des fenêtres de niveau supérieur et, par défaut, s’affichent dans l’arborescence UI Automation en tant qu’enfants du bureau. Dans de nombreux cas, toutefois, les fenêtres indépendantes sont logiquement des enfants d'autres contrôles. Par exemple, la liste déroulante d'une zone de liste modifiable est logiquement un enfant de la zone de liste modifiable. De la même façon, une fenêtre indépendante de menu est logiquement un enfant du menu. UI Automation fournit la prise en charge pour assigner un nouveau parent à une fenêtre indépendante afin qu’il semble être un enfant du contrôle associé.

Pour assigner un nouveau parent à une fenêtre indépendante :

1.  Créez un fournisseur pour la fenêtre indépendante. Cela requiert que la classe de la fenêtre indépendante soit connue à l’avance.
2.  Implémentez toutes les propriétés et tous les modèles de contrôle comme d’habitude pour cette fenêtre contextuelle, comme s’il s’agissait d’un contrôle dans son propre droit.
3.  Implémentez la propriété [**IRawElementProviderSimple :: HostRawElementProvider**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementprovidersimple-get_hostrawelementprovider) pour qu’elle retourne la valeur obtenue à partir de [**UiaHostProviderFromHwnd**](/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiahostproviderfromhwnd), où le paramètre est le handle de fenêtre de la fenêtre indépendante.
4.  Implémentez [**IRawElementProviderFragment :: Navigate**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementproviderfragment-navigate) pour la fenêtre indépendante et son parent afin que la navigation soit gérée correctement du parent logique aux enfants logiques, et entre les enfants frères.

Quand UI Automation rencontre la fenêtre indépendante, il reconnaît que la navigation est remplacée par rapport à la valeur par défaut et ignore la fenêtre indépendante lorsqu’elle est rencontrée en tant qu’enfant du bureau. Au lieu de cela, le nœud est accessible uniquement via le fragment.

L’attribution d’un nouveau parent n’est pas appropriée dans les cas où un contrôle peut héberger une fenêtre de n’importe quelle classe. Par exemple, un contrôle rebar peut héberger n’importe quel type de fenêtre dans ses bandes. Pour gérer ces cas, UI Automation prend en charge une autre forme de réadressage de fenêtre, comme décrit dans la section suivante.

## <a name="provider-repositioning"></a>Repositionnement du fournisseur

Les fragments UI Automation peuvent contenir deux éléments ou plus qui sont tous contenus dans une fenêtre. Étant donné que chaque fenêtre possède son propre fournisseur par défaut qui considère que la fenêtre est un enfant d’une fenêtre conteneur, l’arborescence UI Automation par défaut affiche les fenêtres dans le fragment en tant qu’enfants de la fenêtre parente. Dans la plupart des cas, ce comportement est souhaitable, mais il peut parfois entraîner une confusion, car il ne correspond pas à la structure logique de l’interface utilisateur.

Le contrôle rebar en est un bon exemple. Un contrôle rebar contient des bandes, qui peuvent à leur tour contenir un contrôle basé sur une fenêtre, tel qu’une barre d’outils, une zone d’édition ou une zone de liste déroulante. Le fournisseur de fenêtre par défaut pour la fenêtre Rebar voit les fenêtres de contrôle de bande comme enfants et le fournisseur Rebar voit les bandes comme des enfants. Étant donné que le fournisseur de fenêtre et le fournisseur Rebar travaillent en tandem et qu’ils combinent leurs enfants, les bandes et les contrôles basés sur des fenêtres apparaissent en tant qu’enfants du contrôle rebar. Toutefois, seules les bandes doivent apparaître en tant qu’enfants du contrôle rebar, et chaque fournisseur de bandes doit être associé au fournisseur de fenêtre par défaut pour le contrôle qu’il contient.

Pour ce faire, le fournisseur de la racine du fragment pour le contrôle rebar expose un jeu d’enfants représentant les bandes. Chaque bande possède un seul fournisseur qui peut exposer des propriétés et des modèles de contrôle. Dans son implémentation de [**IRawElementProviderSimple :: HostRawElementProvider**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementprovidersimple-get_hostrawelementprovider), le fournisseur de bandes retourne le fournisseur de fenêtre par défaut pour la fenêtre de contrôle, qu’il obtient en appelant [**UiaHostProviderFromHwnd**](/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiahostproviderfromhwnd), en passant le handle de fenêtre (**HWND**) du contrôle. Enfin, le fournisseur de la racine du fragment pour le rebar implémente l’interface [**IRawElementProviderHwndOverride**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementproviderhwndoverride) et, dans son implémentation de [**IRawElementProviderHwndOverride :: GetOverrideProviderForHwnd**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementproviderhwndoverride-getoverrideproviderforhwnd), il retourne le fournisseur de bandes approprié pour le contrôle contenu dans la fenêtre spécifiée.

## <a name="disconnecting-providers"></a>Déconnexion des fournisseurs

Les applications créent généralement des contrôles tels qu’ils sont nécessaires et les détruisent par la suite. Après la destruction d’un contrôle, les ressources du fournisseur UI Automation associées au contrôle doivent être libérées en appelant [**UiaDisconnectProvider**](/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiadisconnectprovider).

De même, une application doit utiliser la fonction [**UiaDisconnectAllProviders**](/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiadisconnectallproviders) pour libérer toutes les ressources UI Automation détenues par tous les fournisseurs dans l’application avant l’arrêt.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Guide du programmeur du fournisseur UI Automation](uiauto-providerportal.md)
</dt> </dl>

 

 