---
title: Comment interroger un élément virtualisé dans la vue éléments
description: cette rubrique explique comment utiliser l’automatisation de l’interface utilisateur de Microsoft pour récupérer des informations d’interface utilisateur sur les éléments virtualisés dans l’affichage Windows 7 éléments.
ms.assetid: a0bff8a1-47b1-4750-8086-e2e65a79099e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9196d62e7aa93b21aed15b76b8ced6a9520b27fb5bcee74a0e0d4ddc510c86f9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119759243"
---
# <a name="how-to-query-a-virtualized-item-in-items-view"></a>Comment interroger un élément virtualisé dans la vue éléments

cette rubrique explique comment utiliser l’automatisation de l’interface utilisateur de Microsoft pour récupérer des informations d’interface utilisateur sur les éléments virtualisés dans l’affichage Windows 7 éléments. Cette rubrique comprend les sections suivantes.

> [!Note]  
> cette rubrique s’applique uniquement à Windows 7. Sachez que les fonctionnalités d’accessibilité décrites dans cette rubrique peuvent changer dans les versions ultérieures de Windows.

 

-   [Vue d'ensemble](#overview)
-   [Arborescence de la vue éléments, structure](#items-view-tree-structure)
-   [Virtualisation](#virtualization)
-   [Obtention du décompte de tous les éléments](#obtaining-a-count-of-all-items)
-   [Obtention d’un index d’élément par rapport à tous les éléments](#obtaining-an-item-index-with-respect-to-all-items)
-   [Obtention d’une référence à un élément Vitualized](#obtaining-a-reference-to-a-vitualized-item)
-   [Défilement d’un élément virtualisé à l’écran](#scrolling-a-virtualized-item-on-screen)
-   [Rubriques connexes](#related-topics)

## <a name="overview"></a>Vue d’ensemble

La vue éléments est un composant d’interface utilisateur qui permet aux utilisateurs d’afficher et d’interagir avec des fichiers et d’autres éléments. dans Windows 7, la vue éléments remplace le contrôle list-view pour présenter des éléments dans la vue par défaut de Windows Explorer. la vue éléments est également utilisée dans la boîte de dialogue élément commun, menu Démarrer les résultats de recherche et d’autres Windows 7 éléments d’interface utilisateur qui utilisent le contrôle navigateur de l’explorateur. Par rapport au contrôle List-View, la vue items offre les avantages suivants aux utilisateurs :

-   La vue éléments peut présenter des éléments qui sont plus utiles, souhaitables et pertinents, ce qui permet aux utilisateurs de rechercher et d’organiser des éléments plus simplement, rapidement et facilement.
-   La vue éléments peut afficher de grands ensembles d’éléments à partir de sources de données qui ont des caractéristiques de performances différentes, ce qui permet aux utilisateurs de parcourir et de rechercher la totalité de leur collection d’éléments dans plusieurs sources.

l’illustration suivante montre la vue éléments dans Windows Explorer.

![capture d’écran montrant l’Explorateur Windows avec le composant vue éléments](images/itemsview.gif)

Du point de vue d’un développeur, la structure générale et les fonctionnalités de la vue éléments sont similaires à celles du contrôle List-View. La principale différence réside dans le fait que la vue items prend en charge la virtualisation, contrairement au contrôle List-View. En outre, la vue éléments utilise deux nouvelles interfaces UI Automation pour garantir que le contenu virtualisé fourni par la vue éléments est accessible. Ces interfaces sont décrites dans les sections suivantes de cette rubrique.

Pour obtenir des informations générales sur la virtualisation dans UI Automation, consultez [utilisation des éléments virtualisés](uiauto-workingwithvirtualizeditems.md).

## <a name="items-view-tree-structure"></a>Arborescence de la vue éléments, structure

Dans l’arborescence UI Automation, l’élément UI Automation de niveau supérieur de la vue éléments a le nom « ItemsView » et le type de contrôle « List ». Dans l’image précédente, l’élément UI Automation ItemsView est souligné en rouge. Différents éléments UI Automation se trouvent sous le niveau supérieur de ItemsView, mais seuls deux autres éléments UI Automation sont référencés dans ce document : éléments de groupe et éléments de liste.

Les éléments de groupe sont les éléments UI Automation qui contiennent tous les éléments de liste de ce groupe : leur type de contrôle est « groupe » et leurs noms varient en fonction du nom du groupe. Dans l’image précédente, le premier élément de groupe contient à la fois l’en-tête « A-H (1) » et l’élément de liste « dossier », et son nom est « A-H ».

Les éléments de liste sont les éléments UI Automation qui représentent les éléments feuille de la vue : leur type de contrôle est « ListItem » et leurs noms varient en fonction du nom de l’élément. dans l’image précédente, les éléments de liste sont les éléments feuille tels que « Folder », « Musique » et « image ». Ces trois éléments UI Automation sont référencés par les termes ItemsView ELEMENT, Group Element et ListItem dans le reste de ce document.

## <a name="virtualization"></a>Virtualisation

La vue éléments utilise la virtualisation, ce qui signifie que les éléments en dehors de la zone visible de la vue ne sont pas extraits du système et que la représentation de l’interface utilisateur n’est pas créée. Ces éléments sont appelés *éléments virtualisés*. Étant donné qu’ils ne sont pas créés, les éléments virtualisés n’ont pas d’éléments UI Automation et, par conséquent, n’apparaissent pas dans l’arborescence UI Automation lorsqu’un client UI Automation énumère l’arborescence. En outre, les modèles de contrôle UI Automation fonctionnent uniquement sur les éléments visibles. Par exemple, le modèle de contrôle [Selection](uiauto-implementingselection.md) ne retourne que les éléments sélectionnés visibles lorsqu’un client appelle la méthode [**IUIAutomationSelectionPattern :: GetCurrentSelection**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationselectionpattern-getcurrentselection) .

La vue items prend en charge la possibilité de récupérer les informations suivantes sur les éléments virtualisés :

-   Nombre total d’éléments, y compris les éléments virtualisés
-   Éléments UI Automation pour les éléments virtualisés
-   Éléments UI Automation pour les éléments virtualisés sélectionnés

## <a name="obtaining-a-count-of-all-items"></a>Obtention du décompte de tous les éléments

Un client peut utiliser l’élément ItemsView pour obtenir le nombre total d’éléments, ainsi que le nombre d’éléments sélectionnés. L’élément ItemsView fournit deux façons d’effectuer ces nombres. La première consiste à obtenir la propriété ItemStatus de l’élément ItemsView, tandis que la seconde consiste à obtenir des propriétés personnalisées à partir de l’élément ItemsView.

La propriété ItemStatus est une chaîne qui spécifie le nombre total d’éléments et le nombre d’éléments sélectionnés, séparés par une virgule. Par exemple : « 3 éléments, 1 élément sélectionné ». Cette chaîne est localisée et peut être communiquée directement à l’utilisateur.

Les propriétés personnalisées de l’élément ItemsView incluent une propriété pour le nombre d’éléments, et une autre pour le nombre de sélections. Ils comprennent :

-   ItemCount \_ Property \_ GUID (ABBF5C45-5CCC-47B7-BB4E-87CB87BBD162) : nombre de tous les éléments uniques dans la vue. S’ils sont regroupés par une propriété à valeurs multiples (MVP) afin qu’un seul élément puisse apparaître plusieurs fois, chaque élément n’est compté qu’une seule fois.

    (UIAutomationType : [**UIAutomationType \_ int**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-uiautomationtype), nom de programmation : "ItemCount")

-   \_ \_ GUID de la propriété SELECTEDITEMCOUNT (92A053DA-2969-4021-BF27-514CFC2E4A69) : nombre de tous les éléments uniques sélectionnés dans la vue. S’ils sont regroupés par une propriété à valeurs multiples (MVP) afin qu’un seul élément puisse apparaître plusieurs fois, chaque élément n’est compté qu’une seule fois.

    (UIAutomationType : [**UIAutomationType \_ int**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-uiautomationtype), nom de programmation : "SelectedItemCount")

ces propriétés personnalisées sont définies dans Shlguid. h, qui est inclus dans le kit de développement logiciel (SDK) Windows, et ces propriétés sont inscrites via la méthode [**IUIAutomationRegistrar :: RegisterProperty**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iuiautomationregistrar-registerproperty) . Les clients UI Automation utilisent **RegisterProperty** pour récupérer les identificateurs de propriété (connaître) pour les propriétés personnalisées.

## <a name="obtaining-an-item-index-with-respect-to-all-items"></a>Obtention d’un index d’élément par rapport à tous les éléments

Un client peut obtenir l’index d’un élément soit en obtenant la propriété ItemStatus d’un élément ListItem, soit en obtenant une propriété personnalisée d’un élément ListItem.

La propriété ItemStatus est une chaîne qui contient l’index d’un élément par rapport au nombre total d’éléments. Par exemple : « élément 1 sur 3 ». Cette chaîne est localisée et peut être communiquée directement à l’utilisateur.

La propriété personnalisée suivante obtient l’index d’élément d’un élément ListItem :

-   \_Propriété ItemIndex \_ GUID (92A053DA-2969-4021-BF27-514CFC2E4A69) : index absolu de base 1 d’un élément. S’ils sont regroupés par une propriété à valeurs multiples (MVP) afin qu’un seul élément puisse apparaître deux fois, chaque apparence de l’élément obtient un index séparé.

    (UIAutomationType : [**UIAutomationType \_ int**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-uiautomationtype), nom de programmation : "ItemIndex")

cette propriété personnalisée est définie dans Shlguid. h, qui est inclus dans le SDK Windows, et est inscrite via la méthode [**IUIAutomationRegistrar :: RegisterProperty**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iuiautomationregistrar-registerproperty) . Les clients UI Automation utilisent **RegisterProperty** pour récupérer un identificateur de propriété (connaître) pour la propriété personnalisée.

## <a name="obtaining-a-reference-to-a-vitualized-item"></a>Obtention d’une référence à un élément Vitualized

Un élément ItemsView implémente le modèle de contrôle [ItemContainer](uiauto-implementingitemcontainer.md) (interface [**IItemContainerProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iitemcontainerprovider) ), qui permet à un client d’obtenir un élément UI Automation pour un élément virtualisé (un élément qui se trouve en dehors de la zone visible). ItemsView permet au client de rechercher un élément ListItem en effectuant une recherche sur les propriétés Name et Selection : la tentative de recherche sur une autre propriété échoue.

Un élément virtuel implémente uniquement le modèle de contrôle [VirtualizedItem](uiauto-implementingvirtualizeditem.md) (interface [**IVirtualizedItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ivirtualizeditemprovider) ). Étant donné que l’élément représenté par un élément UI Automation virtualisé n’existe pas encore, toute tentative d’obtenir un autre modèle de contrôle ou une autre propriété de l’élément échoue.

Les éléments ListItem et Group sont virtualisés, mais seuls les éléments ListItem peuvent être retournés à partir du modèle de contrôle [ItemContainer](uiauto-implementingitemcontainer.md) . Étant donné que l’appel à la méthode [**IUIAutomationItemContainerPattern :: FindItemByProperty**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationitemcontainerpattern-finditembyproperty) s’exécute sur le thread d’interface utilisateur et qu’il bloque, la vue ne répond pas tant que **FindItemByProperty** n’est pas retourné, et tout autre appel de méthode sur le fournisseur doit attendre la fin de **FindItemByProperty** . Dans certains cas, **FindItemByProperty** doit traiter l’ensemble du jeu de données avant de retourner, ce qui peut nécessiter de nombreuses ressources. Si vous spécifiez **null** comme élément de départ, **FindItemByProperty** commence la recherche par le premier élément de la vue.

ItemsView prend en charge les propriétés suivantes pour [**FindItemByProperty**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationitemcontainerpattern-finditembyproperty):

-   Name (UIA \_ NamePropertyId) : recherche le premier élément dont le nom correspond entièrement à la chaîne spécifiée. La recherche ne respecte pas la casse. Les caractères génériques ou la correspondance partielle ne sont pas pris en charge. Si un nom **null** est spécifié, l’élément suivant après l’élément de départ est retourné. La spécification de noms **null** permet à un client UI Automation d’énumérer tous les éléments de la vue ; Toutefois, l’énumération de tous les éléments est déconseillée, car elle entraîne la réalisation de tous les éléments de la vue.
-   SelectionItem \_ IsSelected (UIA \_ SelectionItemIsSelectedPropertyId) : recherche le premier élément dont \_ la propriété IsSelected SelectionItem correspond à la valeur spécifiée. Spécifiez **true** pour rechercher le premier élément sélectionné, ou **false** pour rechercher le premier élément non sélectionné. Soyez prudent lors de l’énumération de tous les éléments sélectionnés, car le nombre d’éléments sélectionnés peut être très élevé, en particulier si l’utilisateur a sélectionné tous les éléments.

## <a name="scrolling-a-virtualized-item-on-screen"></a>Défilement d’un élément virtualisé à l’écran

Après avoir obtenu une référence à un élément UI Automation pour un élément virtualisé (hors de l’écran), le client peut faire défiler l’élément dans l’affichage à l’aide de la méthode [**IUIAutomationVirtualizeItemPattern :: réalise**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationvirtualizeditempattern-realize) du modèle de contrôle [VirtualizedItem](uiauto-implementingvirtualizeditem.md) . Une fois l’élément réalisé, il est visible et toutes les propriétés et les modèles de contrôle normalement associés à un élément ListItem sont disponibles pour le client.

Seuls les éléments ListItem obtenus par la méthode [**IUIAutomationItemContainerPattern :: FindItemByProperty**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationitemcontainerpattern-finditembyproperty) exposent le modèle de contrôle [VirtualizedItem](uiauto-implementingvirtualizeditem.md) . Lorsqu’un élément à l’écran est défilant hors de l’écran, l’élément devient non valide et le client doit appeler **FindItemByProperty** pour accéder à la référence hors écran.

Il est également possible de déplacer des éléments dans et hors de l’affichage à l’aide du modèle de contrôle [Scroll](uiauto-implementingscroll.md) (ou à l’aide des barres de défilement). Les éléments et les groupes sont réalisés au fur et à mesure qu’ils font défiler la vue et sont virtualisés à mesure qu’ils défilent hors de l’affichage.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Utilisation d’éléments virtualisés](uiauto-workingwithvirtualizeditems.md)
</dt> </dl>

 

 




