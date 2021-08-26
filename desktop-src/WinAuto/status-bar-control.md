---
title: Contrôle de barre d’État (référence des éléments d’interface utilisateur MSAA)
description: Les barres d’état affichent des informations d’État dans une fenêtre horizontale au bas d’une fenêtre d’application.
ms.assetid: e910a5c6-84d5-4ade-abf5-792ff1915021
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ad6c4955bfe10bc7eb224213a8e2e262179d2b122ca4eae210d0d1e72e4635b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119998059"
---
# <a name="status-bar-control-msaa-ui-element-reference"></a>Contrôle de barre d’État (référence des éléments d’interface utilisateur MSAA)

> [!Note]  
> Cette rubrique décrit les objets de **contrôle de barre d’État** à des fins de référence d’élément d’interface utilisateur MSAA. La procédure de création d’objets de **contrôle de barre d’État** dans différentes infrastructures d’interface utilisateur n’est pas décrite ici. Consultez la documentation de référence sur les API pour l’infrastructure d’interface utilisateur que vous utilisez.

 

Les barres d’état affichent des informations d’État dans une fenêtre horizontale au bas d’une fenêtre d’application. Les barres d’État sont souvent divisées en parties, appelées volets, et chaque volet affiche des informations d’État différentes. En outre, les barres d’État peuvent contenir des objets de types différents, notamment des boutons et des barres de progression. Le nom de la classe de fenêtre pour un contrôle de barre d’État est STATUSCLASSNAME, qui est défini comme « msctls \_ statusbar32 » dans commctrl. h.

## <a name="iaccessible-methods"></a>Méthodes IAccessible

Les barres d’État prennent en charge les méthodes [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) suivantes :

-   [**accHitTest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)
-   [**accLocation**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation)
-   [**accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)
-   [**accSelect**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect)

## <a name="iaccessible-properties"></a>Propriétés IAccessible

Les barres d’État prennent en charge les propriétés [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) suivantes :



| Propriété                                                                 | Commentaires                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|--------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Obtient \_ accChildCount**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchildcount) | La propriété **ChildCount** est le nombre de volets dans la barre d’État.                                                                                                                                                                                                                                                                                                                                                                                                     |
| [**Obtient \_ accFocus**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accfocus)           |                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| [**Obtient \_ accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)             | L’objet de barre d’État lui-même n’a pas de propriété **Name** . La propriété **Name** de chaque volet de la barre d’État est la même que le texte affiché.                                                                                                                                                                                                                                                                                                                   |
| [**Obtient \_ accParent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent)         | La propriété **parent** de l’objet de barre d’État est une fenêtre ( [**\_ \_ fenêtre système de rôle**](object-roles.md) ) qui entoure le contrôle et possède le même nom de classe de fenêtre que le contrôle. La propriété **parent** des volets dans la barre d’État est l’objet de barre d’État.                                                                                                                                                                           |
| [**Obtient \_ accRole**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole)             | La propriété de **rôle** pour l’objet de barre d’État proprement dit est le [**\_ \_ STATUSBAR système Role**](object-roles.md). Le texte affiché dans une barre d’État présente le [**rôle \_ système \_ STATICTEXT**](object-roles.md) en tant que propriété de **rôle** .                                                                                                                                                                                                 |
| [**Obtient \_ accState**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate)           | La propriété d' **État** est une combinaison d’une ou plusieurs des [valeurs](object-state-constants.md)suivantes : état du système d’état [**\_ \_ invisible**](object-state-constants.md) système d’état \| [**\_ \_ non disponible**](object-state-constants.md) système \| [**\_ \_**](object-state-constants.md) \| [**\_ \_**](object-state-constants.md)<br/> |



 

## <a name="notes"></a>Remarques

Comme les raccourcis clavier ne sont pas pris en charge pour les contrôles de barre d’État ou les zones de texte sur les barres d’État, l' [**\_ accKeyboardShortcut**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acckeyboardshortcut) n’est pas pris en charge.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[IAccessible, interface](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)
</dt> </dl>

 

 





