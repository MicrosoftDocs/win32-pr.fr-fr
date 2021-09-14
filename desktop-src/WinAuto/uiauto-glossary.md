---
title: glossaire (Windows fonctionnalités d’accessibilité)
description: Page de glossaire
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: c45583f2-a6e8-4a01-9577-9b604b5bbc62
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 16679c63f0716058e53c7c9d164a24593c481dff
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127010522"
---
# <a name="glossary-windows-accessibility-features"></a>glossaire (Windows fonctionnalités d’accessibilité)

## <a name="a"></a>Un

<dl> <dt>

**clé d’accès**
</dt> <dd>

Caractère souligné dans le texte de l’étiquette d’un contrôle.

</dd> <dt>

**aide sur l’accessibilité**
</dt> <dd>

Également appelé technologie d’assistance ; programmes spécialisés qui fonctionnent avec le système d’exploitation d’un ordinateur pour répondre à des handicaps spécifiques, tels qu’une plage limitée de mouvement ou de cécité. Les produits incluent des claviers plus larges, des claviers orientés regards, des utilitaires d’entrée vocale, des claviers à l’écran et des produits capables de convertir du texte en paroles ou en affichage braille dynamique. Pour plus d’informations, consultez [produits de technologie d’assistance](https://www.microsoft.com/enable/at/default.aspx).

</dd> <dt>

**objet accessible**
</dt> <dd>

Tout élément d’interface utilisateur qui implémente l’interface [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) et possède des propriétés qui décrivent le nom de l’objet, les emplacements d’écran et d’autres informations nécessaires aux aides à l’accessibilité. Pour plus d’informations, consultez [objets accessibles](accessible-objects.md).

</dd> </dl>

## <a name="c"></a>C

<dl> <dt>

**élément enfant**
</dt> <dd>

Consultez [*élément simple*](uiauto-glossary.md).

</dd> <dt>

**client**
</dt> <dd>

Tout programme qui utilise UI Automation ou Microsoft Active Accessibility pour accéder, identifier ou manipuler les éléments d’interface utilisateur d’une application ; les clients incluent des aides à l’accessibilité, des outils de test automatisés et certaines applications de formation basées sur l’ordinateur. Pour plus d’informations, consultez fonctionnement de [Active Accessibility](how-active-accessibility-works.md).

</dd> <dt>

**fournisseur côté client**
</dt> <dd>

Composant logiciel implémenté par un client UI Automation pour récupérer des informations sur l’interface utilisateur d’une application qui ne prend pas en charge ou ne prend pas entièrement en charge l’Automation d’interface utilisateur. en règle générale, les fournisseurs côté client (proxys) communiquent avec l’application à travers la limite de processus en envoyant et en recevant des messages Windows.

</dd> <dt>

**container**
</dt> <dd>

Également appelé parent ; objet accessible qui correspond à un ou plusieurs éléments simples ; par exemple, un objet [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) pour une zone de liste est le parent des éléments de la liste.

</dd> <dt>

**modèle de contrôle**
</dt> <dd>

Dans UI Automation, implémentation de conception qui décrit une partie discrète des fonctionnalités d’un contrôle. Cette fonctionnalité peut inclure l’apparence visuelle d’un contrôle et les actions qu’il peut effectuer.

</dd> <dt>

**objet de modèle de contrôle**
</dt> <dd>

Instance d’exécution d’un objet COM qui expose une ou plusieurs interfaces de modèle de contrôle.

</dd> <dt>

**fournisseur de modèle de contrôle**
</dt> <dd>

Composant logiciel qui implémente une ou plusieurs interfaces de modèle de contrôle.

</dd> <dt>

**contrôle personnalisé**
</dt> <dd>

Contrôle créé par un utilisateur ou un éditeur de logiciels tiers, ou un contrôle défini par le système qui a été modifié par un utilisateur ou un éditeur de logiciels tiers.

</dd> </dl>

## <a name="d"></a>D

<dl> <dt>

**dégénérer la plage de texte (plage vide)**
</dt> <dd>

Objet qui représente une plage de texte vide (zéro caractère). Une plage de texte dégénérée a des points de terminaison adjacents et spécifie un point entre deux caractères.

</dd> <dt>

**plage de texte disjointe**
</dt> <dd>

Objet qui représente plusieurs étendues de texte qui ne sont pas physiquement adjacentes les unes aux autres.

</dd> <dt>

**conteneur d’ancrage**
</dt> <dd>

Contrôle qui permet la disposition des éléments enfants, à la fois horizontalement et verticalement, par rapport aux limites du conteneur d’ancrage et des autres éléments du conteneur.

</dd> </dl>

## <a name="e"></a>E

<dl> <dt>

**écouteur d’événements**
</dt> <dd>

Application cliente qui s’est inscrite pour recevoir des notifications d’UI Automation ou de Microsoft Active Accessibility chaque fois que des modifications spécifiques de l’interface utilisateur se produisent.

</dd> <dt>

**notification d'événement**
</dt> <dd>

Appel d’un fournisseur UI Automation à un client, dans lequel le fournisseur avertit le client d’un événement qui peut affecter l’État ou l’apparence d’un élément d’interface utilisateur.

</dd> </dl>

## <a name="f"></a>F

<dl> <dt>

**filtrer \[\]**
</dt> <dd>

Pour définir les types d’éléments UI Automation à inclure dans une vue de l’arborescence UI Automation. Voir aussi : vue brute, vue de contrôle et affichage du contenu.

</dd> <dt>

**racine du fragment**
</dt> <dd>

Élément UI Automation au niveau du nœud racine d’une sous-arborescence de l’arborescence UI Automation. Une racine de fragment n’a pas de parent, mais elle est hébergée dans une autre infrastructure, généralement un handle de fenêtre Win32 (**HWND**).

</dd> </dl>

## <a name="h"></a>H

<dl> <dt>

**host**
</dt> <dd>

Élément d’interface utilisateur, tel qu’une fenêtre ou un contrôle, qui contient d’autres éléments d’interface utilisateur. Un hôte exécute des services UI Automation pour le compte des éléments hébergés.

</dd> </dl>

## <a name="i"></a>I

<dl> <dt>

**IAccessible**
</dt> <dd>

Interface COM qui contient toutes les méthodes et propriétés de Microsoft Active Accessibility.

</dd> <dt>

**Proxy IAccessible**
</dt> <dd>

Type de prise en charge de [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) qui fournit des informations d’accessibilité par défaut pour les éléments d’interface utilisateur standard : les contrôles utilisateur, les menus utilisateur et les contrôles communs de COMCTL et Comctl32. Pour plus d’informations, consultez [proxys IAccessible](iaccessible-proxies.md).

</dd> </dl>

## <a name="l"></a>L

<dl> <dt>

**navigation logique**
</dt> <dd>

L’un des deux modes de navigation [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) dans lequel un client explore la hiérarchie d’objets Microsoft Active Accessibility (Next, Previous, parent, premier enfant, dernier enfant).

</dd> </dl>

## <a name="m"></a>M

<dl> <dt>

**marshaling**
</dt> <dd>

Empaquetage et envoi de paramètres d’interface à travers les limites du processus.

</dd> </dl>

## <a name="n"></a>N

<dl> <dt>

**implémentation native**
</dt> <dd>

Type de prise en charge fourni par les éléments d’interface utilisateur qui implémentent l’interface [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) .

</dd> </dl>

## <a name="o"></a>O

<dl> <dt>

**modèle hors écran**
</dt> <dd>

Ce modèle est une base de données d’objets à l’écran et comprend leurs propriétés et leurs relations spatiales.

</dd> <dt>

**OLEACC**
</dt> <dd>

Bibliothèque de liens dynamiques qui fournit le temps d’exécution de Microsoft Active Accessibility et gère les demandes des clients Microsoft Active Accessibility.

</dd> </dl>

## <a name="p"></a>P

<dl> <dt>

**parent**
</dt> <dd>

Également appelé conteneur ; objet accessible qui correspond à un ou plusieurs éléments simples ; par exemple, un objet [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) pour une zone de liste est le parent des éléments de liste

</dd> <dt>

**élément Automation d’espace réservé**
</dt> <dd>

Élément UI Automation qui représente un élément virtualisé dans l’arborescence UI Automation. En règle générale, un espace réservé n’a pas de données chargées pour toutes les propriétés UI Automation et il est requis pour implémenter uniquement le modèle de contrôle [VirtualizedItem](uiauto-implementingvirtualizeditem.md) .

</dd> <dt>

**événement de modification de propriété**
</dt> <dd>

Événement déclenché lorsque la valeur d’une propriété a été modifiée. Les clients s’inscrivent pour recevoir des événements de modification de propriété spécifiques, et UI Automation notifie les clients inscrits lorsque ces événements se produisent.

</dd> <dt>

**interface du fournisseur**
</dt> <dd>

Collection de méthodes publiques implémentée par un fournisseur UI Automation.

</dd> <dt>

**procur**
</dt> <dd>

Consultez le [*proxy IAccessible*](uiauto-glossary.md).

</dd> </dl>

## <a name="r"></a>R

<dl> <dt>

**affichage brut**
</dt> <dd>

Arborescence complète des objets [**IUIAutomationElement**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) dans l’arborescence UI Automation pour laquelle le bureau est la racine. L’affichage brut suit étroitement la structure de programmation native d’une application et, par conséquent, est l’affichage le plus précis de la structure de l’interface utilisateur. C’est aussi la base sur laquelle reposent les autres affichages de l’arborescence.

</dd> <dt>

**élément réalisé**
</dt> <dd>

Élément d’interface utilisateur pour lequel des informations complètes ont été chargées en mémoire, ce qui permet à UI Automation de créer un élément Automation pour l’élément.

</dd> <dt>

**identificateur au moment de l’exécution**
</dt> <dd>

Tableau d’entiers qui identifie l’instance en cours d’exécution d’un élément UI Automation. L’identificateur est unique dans l’interface utilisateur du Bureau sur lequel il a été généré.

</dd> </dl>

## <a name="s"></a>S

<dl> <dt>

**Tableau sécurisé**
</dt> <dd>

Type de données autodescriptives pour déclarer des tableaux utilisés pour la création de composants COM. Avec les données, un tableau sécurisé contient des informations sur le nombre et les limites de ses dimensions.

</dd> <dt>

**portée**
</dt> <dd>

Définition de l’étendue de la vue, à partir d’un élément de base.

</dd> <dt>

**server**
</dt> <dd>

Tout contrôle, module ou application qui utilise Microsoft Active Accessibility pour exposer des informations sur son interface utilisateur

</dd> <dt>

**fournisseur côté serveur**
</dt> <dd>

Composant logiciel qui expose des informations sur un élément d’interface utilisateur basé sur une infrastructure d’interface utilisateur qui ne prend pas en charge l’Automation d’interface utilisateur en mode natif. Les fournisseurs côté serveur (fournisseurs natifs) communiquent avec les applications clientes à travers la limite de processus en exposant des interfaces COM au système de base UI Automation, qui traite les demandes des clients.

</dd> <dt>

**élément simple**
</dt> <dd>

Également connu sous le nom d’élément enfant ; tout élément d’interface utilisateur qui partage un objet [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) avec d’autres éléments et s’appuie sur cet objet **IAccessible** pour exposer ses propriétés. Pour plus d’informations, consultez [éléments simples](simple-elements.md).

</dd> <dt>

**navigation spatiale**
</dt> <dd>

L’un des deux modes de navigation [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) dans lequel un client passe d’un élément d’interface utilisateur à un autre en fonction de ses positions à l’écran (vers le haut, vers le haut, à gauche, à droite).

</dd> </dl>

## <a name="t"></a>T

<dl> <dt>

**Text Services Framework**
</dt> <dd>

Une infrastructure système évolutive qui permet les services de langage naturel et l’entrée de texte avancée sur le bureau et dans les applications.

</dd> <dt>

**unité de texte**
</dt> <dd>

Unité de texte prédéfinie (caractère, mot, ligne ou paragraphe) utilisée pour naviguer dans les segments logiques d’une plage de texte.

</dd> </dl>

## <a name="u"></a>U

<dl> <dt>

**Client UI Automation**
</dt> <dd>

Application de technologie d’assistance, telle qu’un lecteur d’écran, qui utilise UI Automation pour obtenir un accès par programmation aux éléments d’interface utilisateur dans une interface utilisateur d’application. Le client présente des informations sur les éléments de l’interface utilisateur à l’utilisateur final. Les scripts de tests automatisés sont également considérés comme des clients UI Automation.

</dd> <dt>

**Noyau UI Automation**
</dt> <dd>

Composant Runtime qui implémente l’infrastructure UI Automation.

</dd> <dt>

**UI Automation (élément)**
</dt> <dd>

Élément d’interface utilisateur représenté par un objet COM qui implémente une interface de fournisseur UI Automation et qui expose l’interface [**IUIAutomationElement**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) aux clients UI Automation.

</dd> <dt>

**Infrastructure UI Automation**
</dt> <dd>

composant Windows intégral qui prend en charge l’accès par programme à la plupart des éléments d’interface utilisateur sur le bureau. Il permet aux produits de technologie d’assistance tels que les lecteurs d’écran de fournir des informations sur l’interface utilisateur aux utilisateurs finaux et de manipuler l’interface utilisateur par d’autres moyens que l’entrée standard. UI Automation permet également aux scripts de test automatisés d’interagir avec l’interface utilisateur.

</dd> <dt>

**Nœud UI Automation**
</dt> <dd>

Action déconseillée. Consultez UI Automation, élément.

</dd> <dt>

**Fournisseur UI Automation**
</dt> <dd>

Implémentation d’interfaces UI Automation qui expose des informations de programmation sur un élément d’interface utilisateur. Le fournisseur fournit ces informations à l’infrastructure UI Automation en réponse aux demandes des clients UI Automation.

</dd> <dt>

**Arborescence UI Automation**
</dt> <dd>

représentation hiérarchique de tous les éléments UI Automation sur le bureau de Windows. L’arborescence se compose d’un élément racine qui représente le Bureau actuel et dont les éléments enfants représentent des Windows d’application. Chacun de ces éléments enfants peut contenir des éléments qui représentent des éléments de l’interface utilisateur, tels que des menus, des boutons, des barres d’outils et des zones de liste. Ces éléments peuvent contenir des éléments tels que des éléments de liste.

</dd> <dt>

**Infrastructure d’interface utilisateur**
</dt> <dd>

Composant qui gère les contrôles enfants, les tests de positionnement et le rendu dans une zone de l’écran.

</dd> </dl>

## <a name="v"></a>V

<dl> <dt>

**identificateur d’affichage**
</dt> <dd>

Valeur qui identifie une vue disponible pour un élément UI Automation qui implémente un modèle de contrôle. Ce type d’élément fournit et peut basculer entre plusieurs représentations du même ensemble d’informations ou de contrôles enfants.

</dd> <dt>

**élément virtualisé**
</dt> <dd>

Élément d’interface utilisateur qui est chargé en mémoire uniquement lorsqu’il est nécessaire, en général lorsque l’élément devient visible à l’écran. Un élément virtualisé est représenté par un élément Automation d’espace réservé dans l’arborescence UI Automation.

</dd> </dl>

## <a name="w"></a>W

<dl> <dt>

**Événements de fenêtre (WinEvents)**
</dt> <dd>

Type d’événement utilisé pour notifier les clients qu’un objet accessible a changé d’une certaine manière.

</dd> <dt>

**élément basé sur une fenêtre**
</dt> <dd>

Élément UI Automation qui représente un élément d’interface utilisateur qui a son propre handle de fenêtre Win32 (**HWND**).

</dd> </dl>

 

 




