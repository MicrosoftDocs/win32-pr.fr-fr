---
title: Vue d'ensemble technique
description: Microsoft Active Accessibility améliore la façon dont les aides à l’accessibilité (programmes spécialisés qui aident les personnes handicapées à utiliser les ordinateurs de manière plus efficace) fonctionnent avec les applications qui s’exécutent sur Microsoft Windows.
ms.assetid: d71ef40e-4c58-4ee6-8909-04ff4f8d20d3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 69f3931c6a69e9b8caed849942424039178a7884
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127518189"
---
# <a name="technical-overview"></a>Vue d'ensemble technique

Microsoft Active Accessibility améliore la façon dont les aides à l’accessibilité (programmes spécialisés qui aident les personnes handicapées à utiliser les ordinateurs de manière plus efficace) fonctionnent avec les applications qui s’exécutent sur Microsoft Windows.

Microsoft Active Accessibility est basé sur le modèle COM (Component Object Model), qui a été développé par Microsoft et est une norme de l’industrie qui définit une méthode courante pour la communication entre les applications et les systèmes d’exploitation. Microsoft Active Accessibility comprend les composants suivants :

-   L’interface COM [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible), qui expose des informations sur les éléments d’interface utilisateur. **IAccessible** possède également des propriétés et des méthodes pour obtenir des informations sur et manipuler cet élément d’interface utilisateur.
-   WinEvents, un système d’événement qui permet aux serveurs de notifier les clients lorsqu’un objet accessible change.
-   Oleacc.dll, une DLL de prise en charge ou d’exécution.

La DLL Microsoft Active Accessibility, Oleacc.dll, est constituée des composants suivants :

-   Fonctions qui permettent aux clients de demander un pointeur d’interface [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) (par exemple, [**AccessibleObjectFromWindow**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromwindow)).
-   Fonctions permettant aux serveurs de retourner un pointeur d’interface [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) à un client (par exemple, [**LresultFromObject**](/windows/desktop/api/Oleacc/nf-oleacc-lresultfromobject)).
-   Fonctions permettant d’obtenir du texte localisé pour le rôle et les codes d’État (par exemple, [**GetRoleText**](/windows/desktop/api/Oleacc/nf-oleacc-getroletexta) et [**GetStateText**](/windows/desktop/api/Oleacc/nf-oleacc-getstatetexta)).
-   Certaines fonctions d’assistance ([**AccessibleChildren**](/windows/desktop/api/Oleacc/nf-oleacc-accessiblechildren)).
-   Code qui fournit l’implémentation par défaut de [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) pour les contrôles utilisateur standard et COMCTL. Étant donné qu’elles implémentent **IAccessible** pour le compte des contrôles système, elles sont appelées *proxys*.

## <a name="in-this-section"></a>Dans cette section

-   [Fonctionnement de Active Accessibility](how-active-accessibility-works.md)
-   [Notions de base Active Accessibility](active-accessibility-basics.md)
-   [Instructions du serveur](server-guidelines.md)
-   [Instructions du client](client-guidelines.md)
-   [Directives COM et Unicode](com-and-unicode-guidelines.md)

 

 




