---
title: Barre de menus (référence des éléments d’interface utilisateur MSAA)
description: Une barre de menus est la zone d’une fenêtre située immédiatement sous la barre de titre qui contient des éléments de menu tels que fichier, Edition, fenêtre et aide.
ms.assetid: 63b496c7-ae3b-49b5-8c22-41fc9a8f3981
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a239a0bb5f860132ba0f9b9393129c2c7a093dae
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127010690"
---
# <a name="menu-bar-msaa-ui-element-reference"></a>Barre de menus (référence des éléments d’interface utilisateur MSAA)

> [!Note]  
> Cette rubrique décrit les objets de **barre de menus** à des fins de référence des éléments d’interface utilisateur MSAA. La procédure de création d’objets de **barre de menus** dans différentes infrastructures d’interface utilisateur n’est pas décrite ici. Consultez la documentation de référence sur les API pour l’infrastructure d’interface utilisateur que vous utilisez.

 

Une barre de menus est la zone d’une fenêtre située immédiatement sous la barre de titre qui contient des éléments de menu tels que **fichier**, **Edition**, **fenêtre** et **aide**. Microsoft Active Accessibility crée également un objet de barre de menus pour un menu système, qui est le menu dans le coin supérieur gauche de la barre de titre et contient des éléments de menu tels que **restaurer**, **déplacer**, **dimensionner**, **réduire** et **agrandir**.

> [!Note]  
> Étant donné que les contrôles de barre de menus ne reçoivent pas le focus, les méthodes [**accSelect**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect) et [**\_ accFocus**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accfocus) ne sont pas prises en charge pour ce contrôle.

 

## <a name="iaccessible-methods"></a>Méthodes IAccessible

Les contrôles de barre de menus prennent en charge les méthodes [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) suivantes :

-   [**accHitTest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)
-   [**accLocation**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation)
-   [**accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)
-   [**accSelect**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect)

## <a name="iaccessible-properties"></a>Propriétés IAccessible

Les contrôles de barre de menus prennent en charge les propriétés [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) suivantes :



| Propriété                                                                             | Commentaires                                                                                                                                                                                                                                                                                                                                                                         |
|--------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Obtient \_ accChild**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchild)                       | Récupère le [**IDispatch**](idispatch-interface.md) pour l’élément de menu spécifié. Les ID enfants pour les éléments de menu sont numérotés de manière séquentielle de gauche à droite en commençant par un.                                                                                                                                                                                             |
| [**Obtient \_ accChildCount**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchildcount)             | La propriété **ChildCount** est le nombre d’éléments de menu de la barre de menus. La propriété **ChildCount** d’un menu système est une.                                                                                                                                                                                                                                                   |
| [**Obtient \_ accDescription**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accdescription)           | La propriété **Description** d’une barre de menus est « contient des commandes permettant de manipuler la vue ou le document actuel ». La propriété **Description** d’un menu système est « contient des commandes permettant de manipuler la fenêtre ».                                                                                                                                                                   |
| [**Obtient \_ accDefaultAction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accdefaultaction)       |                                                                                                                                                                                                                                                                                                                                                                                  |
| [**Obtient \_ accFocus**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accfocus)                       |                                                                                                                                                                                                                                                                                                                                                                                  |
| [**Obtient \_ accHelp**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acchelp)                         |                                                                                                                                                                                                                                                                                                                                                                                  |
| [**Obtient \_ accHelpTopic**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acchelptopic)               |                                                                                                                                                                                                                                                                                                                                                                                  |
| [**Obtient \_ accKeyboardShortcut**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acckeyboardshortcut) | La propriété **KeyboardShortcut** d’une barre de menus sous la barre de titre est « ALT ». La propriété **KeyboardShortcut** d’un menu système est « ALT + espace ».                                                                                                                                                                                                                             |
| [**Obtient \_ accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)                         | La propriété **Name** d’une barre de menus sous la barre de titre est « application ». La propriété **Name** d’un menu système est « System ».                                                                                                                                                                                                                                                |
| [**Obtient \_ accParent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent)                     |                                                                                                                                                                                                                                                                                                                                                                                  |
| [**Obtient \_ accRole**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole)                         | La propriété **role** est [**rôle de la barre de \_ \_ menus du système**](object-roles.md).                                                                                                                                                                                                                                                                                      |
| [**Obtient \_ accState**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate)                       | La propriété **State** est une combinaison d’une ou plusieurs des [valeurs](object-state-constants.md)suivantes : état du système d’État invisible système d’état [**\_ \_ invisible**](object-state-constants.md) système \| [**\_ \_**](object-state-constants.md) \| [**\_ \_**](object-state-constants.md)<br/> |



 

## <a name="notes"></a>Notes

Le système déclenche plusieurs événements [**\_ \_ MENUSTART du système d’événements**](event-constants.md) qui n’ont pas toujours un événement [**MENUEND du \_ système \_ d’événements**](event-constants.md) correspondant. En outre, le système ne déclenche pas les [**événements \_ \_ MENUPOPUPSTART**](event-constants.md) et [**\_ \_ MENUPOPUPEND**](event-constants.md) du système d’événements de manière cohérente. Il s’agit d’un problème connu qui est traité.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[IAccessible, interface](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)
</dt> <dt>

[**Élément de menu**](menu-item.md)
</dt> <dt>

[**Menu contextuel**](pop-up-menu.md)
</dt> </dl>

 

 





