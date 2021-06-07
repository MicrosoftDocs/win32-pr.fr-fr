---
title: Autres rôles d’objet et méthodes prises en charge (référence des éléments d’interface utilisateur MSAA)
description: Cette rubrique fournit des informations sur les rôles d’objet qui ne sont pas inclus dans les rubriques précédentes relatives aux éléments d’interface utilisateur.
ms.assetid: 0c3a3ccf-f02a-4aca-9380-a13774598a19
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f17e8573142a57e0acf08980895fdae3ea6d1841
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/04/2021
ms.locfileid: "111444000"
---
# <a name="other-object-roles-and-supported-methods-msaa-ui-element-reference"></a>Autres rôles d’objet et méthodes prises en charge (référence des éléments d’interface utilisateur MSAA)

Cette rubrique fournit des informations sur les rôles d’objet qui ne sont pas inclus dans les rubriques précédentes relatives aux éléments d’interface utilisateur. Chaque rôle d’objet comprend une liste des méthodes et des propriétés [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) prises en charge pour le rôle d’objet. Tandis que d’autres rubriques documentées ont pris en charge les méthodes et propriétés **IAccessible** pour les éléments d’interface utilisateur, cette rubrique répertorie les méthodes et les propriétés que vous pouvez vous attendre à prendre en charge pour un rôle d’objet particulier. La plupart des éléments d’interface utilisateur qui peuvent avoir l’un des rôles répertoriés ici sont généralement affichés dans les navigateurs.

> [!Note]  
> Utilisez cette rubrique comme indication. Nous vous suggérons vivement d’utiliser les outils de Active Accessibility Microsoft pour vérifier le comportement attendu pour un rôle d’objet individuel.

 

Le tableau suivant répertorie les rôles d’objet supplémentaires que Oleacc.dll prend en charge.



| &nbsp; |  &nbsp; |
|-------------------------------------------------------------------------|-----------------------------------------------------------|
| [**\_alerte du système de rôle \_**](/windows)                           | [**déroulant système de rôle \_ \_**](/windows)       |
| [**\_application de système de rôle \_**](/windows)               | [**\_équation du système de rôle \_**](/windows)       |
| [**\_bordure du système de rôle \_**](/windows)                         | [**\_graphique du système de rôle \_**](/windows)         |
| [**système de rôle \_ \_ BUTTONDROPDOWN**](/windows)         | [**système de rôle \_ \_ HELPBALLOON**](/windows) |
| [**système de rôle \_ \_ BUTTONDROPDOWNGRID**](/windows) | [**\_adresse IP du système de rôle \_**](/windows)     |
| [**système de rôle \_ \_ BUTTONMENU**](/windows)                 | [**\_lien système de rôle \_**](/windows)               |
| [**\_cellule système de rôle \_**](/windows)                             | [**\_volet système de rôle \_**](/windows)               |
| [**\_caractère système du rôle \_**](/windows)                   | [**\_ligne du système de rôle \_**](/windows)                 |
| [**\_graphique de système de rôle \_**](/windows)                           | [**système de rôle \_ \_ ROWHEADER**](/windows)     |
| [**\_horloge système du rôle \_**](/windows)                           | [**\_séparateur système de rôle \_**](/windows)     |
| [**\_colonne système de rôle \_**](/windows)                         | [**\_son du système de rôle \_**](/windows)             |
| [**\_diagramme du système de rôle \_**](/windows)                       | [**système de rôle \_ \_ SPLITBUTTON**](/windows) |
| [**\_numérotation du système de rôle \_**](/windows)                             | [**\_table système des rôles \_**](/windows)             |
| [**\_document système de rôle \_**](/windows)                     | [**\_espace blanc du système de rôle \_**](/windows)   |



 

## <a name="role_system_alert"></a>\_alerte du système de rôle \_

Pour plus d’informations sur ce rôle, [**consultez \_ \_ alerte du système de rôle**](object-roles.md).

**Propriétés et méthodes prises en charge**

-   Obtient \_ accName
-   Obtient \_ accRole
-   Obtient \_ accState

## <a name="role_system_application"></a>\_application de système de rôle \_

Pour plus d’informations sur ce rôle, consultez rôle de l' [**\_ \_ application système**](object-roles.md).

**Propriétés et méthodes prises en charge**

-   accHitTest
-   accLocation
-   accNavigate
-   Obtient \_ accChild
-   Obtient \_ accChildCount
-   Obtient \_ accFocus
-   Obtient \_ accHelp
-   Obtient \_ accHelpTopic
-   Obtient \_ accKeyboardShortcut
-   Obtient \_ accName
-   Obtient \_ accParent
-   Obtient \_ accRole
-   Obtient \_ accState

## <a name="role_system_border"></a>\_bordure du système de rôle \_

Pour plus d’informations sur ce rôle, consultez la rubrique [**\_ \_ bordure du système de rôle**](object-roles.md).

**Propriétés et méthodes prises en charge**

-   accHitTest
-   accLocation
-   accNavigate
-   Obtient \_ accRole
-   Obtient \_ accState

## <a name="role_system_buttondropdown"></a>système de rôle \_ \_ BUTTONDROPDOWN

Pour plus d’informations sur ce rôle, consultez [**rôle \_ système \_ BUTTONDROPDOWN**](object-roles.md).

**Propriétés et méthodes prises en charge**

-   accDoDefaultAction
-   accHitTest
-   accLocation
-   accNavigate
-   Obtient \_ accChild
-   Obtient \_ accChildCount
-   Obtient \_ accDefaultAction
-   Obtient \_ accFocus
-   Obtient \_ accHelp
-   Obtient \_ accHelpTopic
-   Obtient \_ accKeyboardShortcut
-   Obtient \_ accName
-   Obtient \_ accParent
-   Obtient \_ accRole
-   Obtient \_ accState

## <a name="role_system_buttondropdowngrid"></a>système de rôle \_ \_ BUTTONDROPDOWNGRID

Pour plus d’informations sur ce rôle, consultez [**rôle \_ système \_ BUTTONDROPDOWNGRID**](object-roles.md).

**Propriétés et méthodes prises en charge**

-   accDoDefaultAction
-   accHitTest
-   accLocation
-   accNavigate
-   Obtient \_ accChild
-   Obtient \_ accChildCount
-   Obtient \_ accDefaultAction
-   Obtient \_ accFocus
-   Obtient \_ accHelp
-   Obtient \_ accHelpTopic
-   Obtient \_ accKeyboardShortcut
-   Obtient \_ accName
-   Obtient \_ accParent
-   Obtient \_ accRole
-   Obtient \_ accState

## <a name="role_system_buttonmenu"></a>système de rôle \_ \_ BUTTONMENU

Pour plus d’informations sur ce rôle, consultez [**rôle \_ système \_ BUTTONMENU**](object-roles.md).

**Propriétés et méthodes prises en charge**

-   accDoDefaultAction
-   accHitTest
-   accLocation
-   accNavigate
-   Obtient \_ accDefaultAction
-   Obtient \_ accFocus
-   Obtient \_ accHelp
-   Obtient \_ accHelpTopic
-   Obtient \_ accKeyboardShortcut
-   Obtient \_ accName
-   Obtient \_ accParent
-   Obtient \_ accRole
-   Obtient \_ accState

## <a name="role_system_cell"></a>\_cellule système de rôle \_

Pour plus d’informations sur ce rôle, consultez la rubrique [**\_ \_ cellule système Role**](object-roles.md).

**Propriétés et méthodes prises en charge**

-   accHitTest
-   accLocation
-   accNavigate
-   accSelect
-   Obtient \_ accChild
-   Obtient \_ accChildCount
-   Obtient \_ accFocus
-   Obtient \_ accHelp
-   Obtient \_ accHelpTopic
-   Obtient \_ accKeyboardShortcut
-   Obtient \_ accName
-   Obtient \_ accParent
-   Obtient \_ accRole
-   Obtient \_ accState
-   Obtient \_ accValue

## <a name="role_system_character"></a>\_caractère système du rôle \_

Pour plus d’informations sur ce rôle, [**consultez \_ \_ caractère système du rôle**](object-roles.md).

**Propriétés et méthodes prises en charge**

-   accHitTest
-   accLocation
-   accNavigate
-   Obtient \_ accDescription
-   Obtient \_ accFocus
-   Obtient \_ accKeyboardShortcut
-   Obtient \_ accName
-   Obtient \_ accParent
-   Obtient \_ accRole
-   Obtient \_ accState
-   Obtient \_ accValue

## <a name="role_system_chart"></a>\_graphique de système de rôle \_

Pour plus d’informations sur ce rôle, consultez la rubrique [**\_ \_ graphique de système de rôle**](object-roles.md).

**Propriétés et méthodes prises en charge**

-   accHitTest
-   accLocation
-   accNavigate
-   Obtient \_ accChild
-   Obtient \_ accChildCount
-   Obtient \_ accFocus
-   Obtient \_ accHelp
-   Obtient \_ accHelpTopic
-   Obtient \_ accKeyboardShortcut
-   Obtient \_ accName
-   Obtient \_ accParent
-   Obtient \_ accRole
-   Obtient \_ accState

## <a name="role_system_clock"></a>\_horloge système du rôle \_

Pour plus d’informations sur ce rôle, [**consultez \_ \_ horloge du système de rôle**](object-roles.md).

**Propriétés et méthodes prises en charge**

-   accHitTest
-   accLocation
-   accNavigate
-   Obtient \_ accFocus
-   Obtient \_ accHelp
-   Obtient \_ accHelpTopic
-   Obtient \_ accKeyboardShortcut
-   Obtient \_ accName
-   Obtient \_ accParent
-   Obtient \_ accRole
-   Obtient \_ accState
-   Obtient \_ accValue

## <a name="role_system_column"></a>\_colonne système de rôle \_

Pour plus d’informations sur ce rôle, [**consultez \_ \_ colonne système Role**](object-roles.md).

**Propriétés et méthodes prises en charge**

-   accHitTest
-   accLocation
-   accNavigate
-   accSelect
-   Obtient \_ accChild
-   Obtient \_ accChildCount
-   Obtient \_ accFocus
-   Obtient \_ accName
-   Obtient \_ accParent
-   Obtient \_ accRole
-   Obtient \_ accState
-   Obtient \_ accValue

## <a name="role_system_diagram"></a>\_diagramme du système de rôle \_

Pour plus d’informations sur ce rôle, [**consultez \_ \_ diagramme du système de rôle**](object-roles.md).

**Propriétés et méthodes prises en charge**

-   accHitTest
-   accLocation
-   accNavigate
-   Obtient \_ accChild
-   Obtient \_ accChildCount
-   Obtient \_ accFocus
-   Obtient \_ accHelp
-   Obtient \_ accHelpTopic
-   Obtient \_ accKeyboardShortcut
-   Obtient \_ accName
-   Obtient \_ accParent
-   Obtient \_ accRole
-   Obtient \_ accState

## <a name="role_system_dial"></a>\_numérotation du système de rôle \_

Pour plus d’informations sur ce rôle, consultez la page [**\_ \_ accès au système de rôle**](object-roles.md).

**Propriétés et méthodes prises en charge**

-   accDoDefaultAction
-   accHitTest
-   accLocation
-   accNavigate
-   Obtient \_ accDefaultAction
-   Obtient \_ accFocus
-   Obtient \_ accHelp
-   Obtient \_ accHelpTopic
-   Obtient \_ accKeyboardShortcut
-   Obtient \_ accName
-   Obtient \_ accParent
-   Obtient \_ accRole
-   Obtient \_ accState
-   Obtient \_ accValue

## <a name="role_system_document"></a>\_document système de rôle \_

Pour plus d’informations sur ce rôle, [**consultez \_ \_ document de système de rôle**](object-roles.md).

**Propriétés et méthodes prises en charge**

-   accHitTest
-   accLocation
-   accNavigate
-   accSelect
-   Obtient \_ accChild
-   Obtient \_ accChildCount
-   Obtient \_ accFocus
-   Obtient \_ accName
-   Obtient \_ accParent
-   Obtient \_ accRole
-   Obtient \_ accState

## <a name="role_system_droplist"></a>déroulant système de rôle \_ \_

Pour plus d’informations sur ce rôle, consultez la page [**\_ \_ déroulante système de rôles**](object-roles.md).

**Propriétés et méthodes prises en charge**

-   accDoDefaultAction
-   accHitTest
-   accLocation
-   accNavigate
-   Obtient \_ accChild
-   Obtient \_ accChildCount
-   Obtient \_ accDefaultAction
-   Obtient \_ accFocus
-   Obtient \_ accHelp
-   Obtient \_ accHelpTopic
-   Obtient \_ accKeyboardShortcut
-   Obtient \_ accName
-   Obtient \_ accParent
-   Obtient \_ accRole
-   Obtient \_ accState

## <a name="role_system_equation"></a>\_équation du système de rôle \_

Pour plus d’informations sur ce rôle, [**consultez \_ \_ équation du système de rôle**](object-roles.md).

**Propriétés et méthodes prises en charge**

-   accHitTest
-   accLocation
-   accNavigate
-   Obtient \_ accFocus
-   Obtient \_ accName
-   Obtient \_ accParent
-   Obtient \_ accRole
-   Obtient \_ accState
-   Obtient \_ accValue

## <a name="role_system_graphic"></a>\_graphique du système de rôle \_

Pour plus d’informations sur ce rôle, [**consultez \_ \_ graphique du système de rôles**](object-roles.md).

**Propriétés et méthodes prises en charge**

-   accHitTest
-   accLocation
-   accNavigate
-   Obtient \_ accFocus
-   Obtient \_ accHelp
-   Obtient \_ accHelpTopic
-   Obtient \_ accKeyboardShortcut
-   Obtient \_ accName
-   Obtient \_ accParent
-   Obtient \_ accRole
-   Obtient \_ accState

## <a name="role_system_helpballoon"></a>système de rôle \_ \_ HELPBALLOON

Pour plus d’informations sur ce rôle, consultez [**rôle \_ système \_ HELPBALLOON**](object-roles.md).

**Propriétés et méthodes prises en charge**

-   accHitTest
-   accLocation
-   accNavigate
-   Obtient \_ accChild
-   Obtient \_ accChildCount
-   Obtient \_ accDefaultAction
-   Obtient \_ accName
-   Obtient \_ accParent
-   Obtient \_ accRole
-   Obtient \_ accState
-   Obtient \_ accValue

## <a name="role_system_ipaddress"></a>\_adresse IP du système de rôle \_

Pour plus d’informations sur ce rôle, [**consultez \_ \_ adresse IP du système de rôle**](object-roles.md).

**Propriétés et méthodes prises en charge**

-   accHitTest
-   accLocation
-   accNavigate
-   Obtient \_ accChild
-   Obtient \_ accChildCount
-   Obtient \_ accFocus
-   Obtient \_ accHelp
-   Obtient \_ accHelpTopic
-   Obtient \_ accKeyboardShortcut
-   Obtient \_ accName
-   Obtient \_ accParent
-   Obtient \_ accRole
-   Obtient \_ accState
-   Obtient \_ accValue

## <a name="role_system_link"></a>\_lien système de rôle \_

Pour plus d’informations sur ce rôle, [**consultez \_ \_ lien système de rôle**](object-roles.md).

**Propriétés et méthodes prises en charge**

-   accDoDefaultAction
-   accHitTest
-   accLocation
-   accNavigate
-   Obtient \_ accChild
-   Obtient \_ accChildCount
-   Obtient \_ accDefaultAction
-   Obtient \_ accDescription
-   Obtient \_ accFocus
-   Obtient \_ accKeyboardShortcut
-   Obtient \_ accName
-   Obtient \_ accParent
-   Obtient \_ accRole
-   Obtient \_ accState
-   Obtient \_ accValue

## <a name="role_system_pane"></a>\_volet système de rôle \_

Pour plus d’informations sur ce rôle, [**consultez \_ \_ volet système de rôles**](object-roles.md).

**Propriétés et méthodes prises en charge**

-   accHitTest
-   accLocation
-   accNavigate
-   Obtient \_ accChild
-   Obtient \_ accChildCount
-   Obtient \_ accFocus
-   Obtient \_ accHelp
-   Obtient \_ accHelpTopic
-   Obtient \_ accKeyboardShortcut
-   Obtient \_ accName
-   Obtient \_ accParent
-   Obtient \_ accRole
-   Obtient \_ accState

## <a name="role_system_row"></a>\_ligne du système de rôle \_

Pour plus d’informations sur ce rôle, consultez rôle de la [**\_ \_ ligne système**](object-roles.md).

**Propriétés et méthodes prises en charge**

-   accHitTest
-   accLocation
-   accNavigate
-   accSelect
-   Obtient \_ accChild
-   Obtient \_ accChildCount
-   Obtient \_ accDescription
-   Obtient \_ accFocus
-   Obtient \_ accName
-   Obtient \_ accParent
-   Obtient \_ accRole
-   Obtient \_ accState
-   Obtient \_ accValue

## <a name="role_system_rowheader"></a>système de rôle \_ \_ ROWHEADER

Pour plus d’informations sur ce rôle, consultez [**rôle \_ système \_ ROWHEADER**](object-roles.md).

**Propriétés et méthodes prises en charge**

-   accHitTest
-   accLocation
-   accNavigate
-   accSelect
-   Obtient \_ accChild
-   Obtient \_ accChildCount
-   Obtient \_ accDefaultAction
-   Obtient \_ accDescription
-   Obtient \_ accFocus
-   Obtient \_ accName
-   Obtient \_ accParent
-   Obtient \_ accRole
-   Obtient \_ accState
-   Obtient \_ accValue

## <a name="role_system_separator"></a>\_séparateur système de rôle \_

Pour plus d’informations sur ce rôle, [**consultez \_ \_ séparateur de système de rôles**](object-roles.md).

**Propriétés et méthodes prises en charge**

-   accHitTest
-   accLocation
-   Obtient \_ accChild
-   Obtient \_ accChildCount
-   Obtient \_ accParent
-   Obtient \_ accRole
-   Obtient \_ accState

## <a name="role_system_sound"></a>\_son du système de rôle \_

Pour plus d’informations sur ce rôle, consultez [**rôle \_ système \_ audio**](object-roles.md).

**Propriétés et méthodes prises en charge**

-   Obtient \_ accDescription
-   Obtient \_ accName
-   Obtient \_ accRole
-   Obtient \_ accState

## <a name="role_system_splitbutton"></a>système de rôle \_ \_ SPLITBUTTON

Pour plus d’informations sur ce rôle, consultez [**rôle \_ système \_ SPLITBUTTON**](object-roles.md).

**Propriétés et méthodes prises en charge**

-   accDoDefaultAction
-   accHitTest
-   accLocation
-   accNavigate
-   Obtient \_ accDefaultAction
-   Obtient \_ accHelp
-   Obtient \_ accHelpTopic
-   Obtient \_ accKeyboardShortcut
-   Obtient \_ accName
-   Obtient \_ accParent
-   Obtient \_ accRole
-   Obtient \_ accState

## <a name="role_system_table"></a>\_table système des rôles \_

Pour plus d’informations sur ce rôle, [**consultez \_ \_ table système Role**](object-roles.md).

**Propriétés et méthodes prises en charge**

-   accHitTest
-   accLocation
-   accNavigate
-   accSelect
-   Obtient \_ accChild
-   Obtient \_ accChildCount
-   Obtient \_ accDescription
-   Obtient \_ accFocus
-   Obtient \_ accHelp
-   Obtient \_ accHelpTopic
-   Obtient \_ accKeyboardShortcut
-   Obtient \_ accName
-   Obtient \_ accParent
-   Obtient \_ accRole
-   Obtient \_ accState

## <a name="role_system_whitespace"></a>\_espace blanc du système de rôle \_

Pour plus d’informations sur ce rôle, [**consultez \_ \_ espace système du rôle**](object-roles.md).

**Propriétés et méthodes prises en charge**

-   accLocation
-   accSelect
-   Obtient \_ accParent
-   Obtient \_ accRole
-   Obtient \_ accState

 

 