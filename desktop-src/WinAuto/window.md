---
title: Window (référence des éléments d’interface utilisateur MSAA)
description: Microsoft Active Accessibility crée un objet Window générique en tant que conteneur pour un autre objet. Les développeurs clients ne transmettent pas les informations des objets fenêtre aux utilisateurs finaux, car ces objets ne contiennent pas d’informations utiles.
ms.assetid: cc32528f-c454-4522-91b9-06f87cff8bf5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d87c8601ecd6344dc82bbdb416055c694687e6e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103672381"
---
# <a name="window-msaa-ui-element-reference"></a>Window (référence des éléments d’interface utilisateur MSAA)

> [!Note]  
> Cette rubrique décrit les objets de **fenêtre** à des fins de référence des éléments d’interface utilisateur MSAA. La procédure de création d’objets **fenêtres** dans différentes infrastructures d’interface utilisateur n’est pas décrite ici. Consultez la documentation de référence sur les API pour l’infrastructure d’interface utilisateur que vous utilisez.

 

Microsoft Active Accessibility crée un objet Window générique en tant que conteneur pour un autre objet. Les développeurs clients ne transmettent pas les informations des objets fenêtre aux utilisateurs finaux, car ces objets ne contiennent pas d’informations utiles.

Si une application serveur crée un contrôle personnalisé, Microsoft Active Accessibility crée un objet de fenêtre qui contient le contrôle personnalisé, mais le serveur crée un objet accessible pour fournir des informations sur le contenu du contrôle. Le système génère des événements de niveau objet pour l’objet Window, mais le serveur doit envoyer des événements pour l’objet accessible qui fournit des informations sur le contrôle.

## <a name="iaccessible-methods"></a>Méthodes IAccessible

L’objet Window prend en charge les méthodes [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) suivantes :

-   [**accHitTest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)
-   [**accLocation**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation)
-   [**accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)
-   [**accSelect**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect)

## <a name="iaccessible-properties"></a>Propriétés IAccessible

L’objet Window prend en charge les propriétés [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) suivantes :



| Propriété                                                                             | Commentaires                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
|--------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Obtient \_ accChild**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchild)                       | Récupère l’interface [IDispatch](idispatch-interface.md) de l’enfant spécifié.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| [**Obtient \_ accChildCount**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchildcount)             | La propriété **ChildCount** est 7.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| [**Obtient \_ accDescription**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accdescription)           | L’objet Window lui-même n’a pas de propriété **Description** . La propriété **Description** de l’objet enfant peut être récupérée par le biais de l’objet Window.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| [**Obtient \_ accFocus**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accfocus)                       |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| [**Obtient \_ accKeyboardShortcut**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acckeyboardshortcut) | L’objet Window lui-même n’a pas de propriété **KeyboardShortcut** . La propriété **KeyboardShortcut** de l’objet enfant est récupérée par le biais de l’objet Window.                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| [**Obtient \_ accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)                         | La propriété **Name** de l’objet Window est la même que l’objet enfant.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| [**Obtient \_ accParent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent)                     |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| [**Obtient \_ accRole**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole)                         | La propriété de **rôle** est [**\_ \_ fenêtre système de rôle**](object-roles.md). Le **rôle** de l’objet enfant est récupéré via l’objet Window.                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| [**Obtient \_ accState**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate)                       | La propriété **State** est une combinaison d’une ou plusieurs des [valeurs](object-state-constants.md)suivantes : état [**\_ système \_**](object-state-constants.md) indisponible système d’état \| [**\_ \_ indisponible**](object-state-constants.md) système \| [**\_ \_ d'**](object-state-constants.md) état de grande \| [**\_ \_**](object-state-constants.md) \| [**\_ \_ importance**](object-state-constants.md) \| [**\_ \_**](object-state-constants.md) système d’État mobile focalisable système ciblé<br/> |



 

## <a name="notes"></a>Notes

Les événements [**Event \_ System \_ DRAGDROPSTART**](event-constants.md), [**Event \_ System \_ DRAGDROPEND**](event-constants.md), [**Event \_ Object \_ Hide**](event-constants.md)et [**Event Object \_ \_ PARENTCHANGE**](event-constants.md) ne sont pas envoyés par l’objet Window. Il s’agit d’un problème connu qui est traité.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[IAccessible, interface](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)
</dt> </dl>

 

 





