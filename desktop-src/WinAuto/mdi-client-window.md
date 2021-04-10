---
title: Fenêtre cliente MDI (référence des éléments d’interface utilisateur MSAA)
description: L’interface multidocument (MDI) est une spécification qui définit l’interface utilisateur standard pour les applications écrites pour Windows. Une application MDI permet à un utilisateur de travailler avec plusieurs documents à la fois.
ms.assetid: ede2dd19-e4c6-43e8-8f22-f807621dfa0d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e1557176752d29b7d429a0c434554df09b69a8e6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103939920"
---
# <a name="mdi-client-window-msaa-ui-element-reference"></a>Fenêtre cliente MDI (référence des éléments d’interface utilisateur MSAA)

L’interface multidocument (MDI) est une spécification qui définit l’interface utilisateur standard pour les applications écrites pour Windows. Une application MDI permet à un utilisateur de travailler avec plusieurs documents à la fois.

Une application MDI comporte trois types de fenêtres : une fenêtre frame, une fenêtre client et un certain nombre de fenêtres enfants. La fenêtre frame est semblable à la fenêtre principale d’une application et elle entoure la fenêtre cliente. La fenêtre cliente est un enfant de la fenêtre frame et sert d’arrière-plan pour les fenêtres enfants. La fenêtre cliente prend également en charge la création et la manipulation des fenêtres enfants dans lesquelles les documents sont affichés.

Le nom de la classe de fenêtre pour une fenêtre de client MDI est « MDIClient ».

## <a name="iaccessible-methods"></a>Méthodes IAccessible

Une fenêtre cliente MDI prend en charge les méthodes [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) suivantes :

-   [**accHitTest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)
-   [**accLocation**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation)
-   [**accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)
-   [**accSelect**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect)

## <a name="iaccessible-properties"></a>Propriétés IAccessible

Une fenêtre cliente MDI prend en charge les propriétés [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) suivantes :



| Propriété                                                                 | Commentaires                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|--------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Obtient \_ accChildCount**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchildcount) | La propriété **ChildCount** est le nombre de fenêtres enfants dans lesquelles les documents sont affichés.                                                                                                                                                                                                                                                                                                                                                                              |
| [**Obtient \_ accFocus**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accfocus)           |                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| [**Obtient \_ accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)             | La propriété **Name** est « Workspace ».                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| [**Obtient \_ accParent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent)         | La propriété **parente** est la fenêtre frame MDI.                                                                                                                                                                                                                                                                                                                                                                                                                          |
| [**Obtient \_ accRole**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole)             | La propriété de **rôle** est [**client de \_ système \_ de rôle**](object-roles.md)                                                                                                                                                                                                                                                                                                                                                                                  |
| [**Obtient \_ accSelection**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accselection)   |                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| [**Obtient \_ accState**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate)           | La propriété d' **État** est une combinaison d’une ou plusieurs des [valeurs](object-state-constants.md)suivantes : état du système d’état [**\_ \_ invisible**](object-state-constants.md) système d’état \| [**\_ \_ non disponible**](object-state-constants.md) système \| [**\_ \_**](object-state-constants.md) \| [**\_ \_**](object-state-constants.md)<br/> |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[IAccessible, interface](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)
</dt> </dl>

 

 





