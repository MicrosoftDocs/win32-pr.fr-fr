---
title: Élément de menu (référence des éléments d’interface utilisateur MSAA)
description: Un élément de menu représente un élément particulier dans une barre de menus ou un menu contextuel.
ms.assetid: 330782d6-4293-4e65-ab49-a616d133d273
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0cb6621a14927cc4dc9af9f3384157e60ce6570d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127518261"
---
# <a name="menu-item-msaa-ui-element-reference"></a>Élément de menu (référence des éléments d’interface utilisateur MSAA)

> [!Note]  
> Cette rubrique décrit les objets d' **élément de menu** à des fins de référence d’élément d’interface utilisateur MSAA. La procédure de création d’objets d' **élément de menu** dans différentes infrastructures d’interface utilisateur n’est pas décrite ici. Consultez la documentation de référence sur les API pour l’infrastructure d’interface utilisateur que vous utilisez.

 

Un élément de menu représente un élément particulier dans une barre de menus ou un menu contextuel. Par exemple, Microsoft Active Accessibility crée un objet d’élément de menu pour le menu **fichier** dans la barre de menus. De même, Microsoft Active Accessibility crée un objet d’élément de menu pour l’élément de menu **ouvrir** à partir du menu contextuel **fichier** .

Le nom de la classe de fenêtre d’un élément de menu est « \# 32768 ».

## <a name="iaccessible-methods"></a>Méthodes IAccessible

Un élément de menu prend en charge les méthodes [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) suivantes :



| Méthode                                                                    | Commentaires                                                                                                                                                                                                                                                                                       |
|---------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**accDoDefaultAction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accdodefaultaction) | Pour les éléments de menu de la barre de menus, [**accDoDefaultAction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accdodefaultaction) affiche ou ferme le menu en fonction de l’état du menu. Pour les éléments de menu d’un menu contextuel, **accDoDefaultAction** clique sur l’élément de menu pour exécuter la commande de menu. |
| [**acchittest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)                 |                                                                                                                                                                                                                                                                                                |
| [**accLocation**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation)               |                                                                                                                                                                                                                                                                                                |
| [**accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)               |                                                                                                                                                                                                                                                                                                |
| [**accSelect**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect)                   |                                                                                                                                                                                                                                                                                                |



 

## <a name="iaccessible-properties"></a>Propriétés IAccessible

Un élément de menu prend en charge les propriétés [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) suivantes :



| Propriété                                                                             | Commentaires                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|--------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Obtient \_ accChild**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchild)                       | Récupère l’interface [**IDispatch**](idispatch-interface.md) de l’objet de menu contextuel pour cet élément.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| [**Obtient \_ accChildCount**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchildcount)             | La propriété **ChildCount** est une pour les éléments de menu qui affichent un menu ou un sous-menu. Sinon, la propriété **ChildCount** est égale à zéro.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| [**Obtient \_ accDefaultAction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accdefaultaction)       | La propriété **DefaultAction** pour les éléments de menu qui affichent un menu ou un sous-menu est soit « Open », soit « close » en fonction de l’état du menu. La propriété **DefaultAction** de tous les autres éléments de menu est « Execute ».                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| [**Obtient \_ accFocus**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accfocus)                       |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| [**Obtient \_ accKeyboardShortcut**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acckeyboardshortcut) | La propriété **KeyboardShortcut** est la clé d’accès de l’élément de menu, qui est le caractère souligné dans le texte du nom de l’élément de menu. Par exemple, la propriété **KeyboardShortcut** pour l’élément de menu fichier est « f ».                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| [**Obtient \_ accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)                         | La propriété **Name** est identique au nom de l’élément de menu.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| [**Obtient \_ accParent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent)                     | La propriété **parent** est la barre de menus ou le menu contextuel qui contient l’élément de menu.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| [**Obtient \_ accRole**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole)                         | La propriété **role** est un [**système de rôle \_ \_ MenuItem**](object-roles.md).                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| [**Obtient \_ accState**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate)                       | La propriété **State** est soit un [**système d’état \_ \_ invisible**](object-state-constants.md) , soit une combinaison d’une ou plusieurs des valeurs suivantes : état [**\_ système \_ non disponible**](object-state-constants.md) état système \| [**\_ \_ activé**](object-state-constants.md) état système \| [**\_ \_ par défaut**](object-state-constants.md) état système \| [**\_ \_ HOTTRACKED**](object-state-constants.md) \| [**état \_ \_**](object-state-constants.md) système \| [**\_ \_ HASPOPUP**](object-state-constants.md)<br/> |



 

## <a name="notes"></a>Notes

-   Lorsqu’il est utilisé sur un élément de menu, [**accDoDefaultAction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accdodefaultaction) retourne S \_ OK, mais ne parvient pas à effectuer l’action si le caractère utilisé dans la clé d’accès est ?, !, @, ou tout autre caractère qui requiert la touche Maj ou une autre touche de modification. Cela se produit également sur les claviers internationaux avec un caractère de touche d’accès qui requiert l’appui sur la touche ALT GR.
-   La méthode [**accSelect**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect) avec [**SELFLAG \_ TAKEFOCUS**](selflag.md) ne provoque pas l’ouverture ou la fermeture d’un menu contextuel par un élément de menu. Les clients utilisent la méthode [**accDoDefaultAction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accdodefaultaction) pour ouvrir ou fermer un menu contextuel.
-   Un élément de barre de menus qui n’affiche pas de menu contextuel retourne « application » pour la propriété **Name** au lieu du nom de l’élément de menu.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[IAccessible, interface](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)
</dt> <dt>

[**Barre de menus**](menu-bar.md)
</dt> <dt>

[**Menu contextuel**](pop-up-menu.md)
</dt> </dl>

 

 





