---
title: Boîte de dialogue (référence des éléments d’interface utilisateur MSAA)
description: Une boîte de dialogue est une fenêtre temporaire créée par une application pour récupérer les entrées d’utilisateur.
ms.assetid: 7d132c2c-eab1-4132-b2b6-fa1f8b142f58
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 52abc4f08dabb8bfc96c83b5323951135bc4042d87b4e443e29fb1ecd5592852
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120122229"
---
# <a name="dialog-box-msaa-ui-element-reference"></a>Boîte de dialogue (référence des éléments d’interface utilisateur MSAA)

> [!Note]  
> Cette rubrique décrit les objets **boîte de dialogue** à des fins de référence des éléments d’interface utilisateur MSAA. La procédure de création d’objets de **boîte de dialogue** dans différentes infrastructures d’interface utilisateur n’est pas décrite ici. Consultez la documentation de référence sur les API pour l’infrastructure d’interface utilisateur que vous utilisez.

 

Une boîte de dialogue est une fenêtre temporaire créée par une application pour récupérer les entrées d’utilisateur. Une application utilise des boîtes de dialogue pour inviter l’utilisateur à fournir des informations supplémentaires sur les commandes que l’utilisateur a choisies à partir d’un menu. Une boîte de dialogue contient un ou plusieurs contrôles (fenêtres enfants) avec lesquels l’utilisateur entre du texte, choisit des options ou dirige l’action de la commande.

Le nom de la classe de fenêtre pour les boîtes de dialogue est « \# 32770 ».

## <a name="iaccessible-methods"></a>Méthodes IAccessible

Une boîte de dialogue prend en charge les méthodes [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) suivantes :



| Méthode                                                                    | Commentaires                                                                                                                                                                                                                                                                               |
|---------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**accDoDefaultAction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accdodefaultaction) | Si la boîte de dialogue contient un bouton de commande par défaut, la méthode [**accDoDefaultAction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accdodefaultaction) appelle [**PostMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea) avec le message de bouton de [**\_ clic BM**](/windows/desktop/Controls/bm-click) pour cliquer sur le bouton de commande par défaut. |
| [**accHitTest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)                 |                                                                                                                                                                                                                                                                                        |
| [**accLocation**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation)               |                                                                                                                                                                                                                                                                                        |
| [**accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)               |                                                                                                                                                                                                                                                                                        |
| [**accSelect**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect)                   |                                                                                                                                                                                                                                                                                        |



 

## <a name="iaccessible-properties"></a>Propriétés IAccessible

Une boîte de dialogue prend en charge les propriétés [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) suivantes :



| Propriété                                                                                 | Commentaires                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Obtient \_ accChildCount**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchildcount)                 | La propriété **ChildCount** est égale au nombre de contrôles de fenêtre enfants sur la boîte de dialogue.                                                                                                                                                                                                                                                                                                                                                                           |
| [**Obtient \_ accDefaultAction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accdefaultaction)           | Si la boîte de dialogue contient un bouton de commande par défaut, la propriété **DefaultAction** est « Press ».                                                                                                                                                                                                                                                                                                                                                                             |
| [**Obtient \_ accFocus**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accfocus)                           |                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| [**Obtient \_ accKeyboardShortcut**](/windows/desktop/api/oleacc/nf-oleacc-iaccessible-get_acckeyboardshortcut) | En règle générale, les boîtes de dialogue n’ont pas de raccourcis clavier. Si le texte de la fenêtre de la boîte de dialogue contient un caractère perluète (&), Microsoft Active Accessibility retourne une chaîne non null en tant que propriété **KeyboardShortcut** .                                                                                                                                                                                                                                        |
| [**Obtient \_ accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)                             | La propriété **Name** est le texte de la fenêtre, ou Caption, qui est affiché dans la barre de titre de la boîte de dialogue.                                                                                                                                                                                                                                                                                                                                                              |
| [**Obtient \_ accParent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent)                         | La propriété **parent** est une fenêtre ( [**\_ \_ fenêtre système de rôle**](object-roles.md) ) qui entoure la boîte de dialogue et qui possède les mêmes propriétés de **nom** et nom de classe de fenêtre que la boîte de dialogue.                                                                                                                                                                                                                                                        |
| [**Obtient \_ accRole**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole)                             | La propriété de **rôle** est la [**boîte de \_ \_ dialogue système de rôle**](object-roles.md) ou le système de [**rôle \_ \_ PROPERTYPAGE**](object-roles.md).                                                                                                                                                                                                                                                                                                 |
| [**Obtient \_ accState**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate)                           | La propriété d' **État** est une combinaison d’une ou plusieurs des [valeurs](object-state-constants.md)suivantes : état du système d’état [**\_ \_ invisible**](object-state-constants.md) système d’état \| [**\_ \_ non disponible**](object-state-constants.md) système \| [**\_ \_**](object-state-constants.md) \| [**\_ \_**](object-state-constants.md)<br/> |



 

## <a name="remarks"></a>Remarques

L’objet Dialog ne prend pas en charge la méthode [**\_ accChild**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchild) . Pour obtenir un pointeur d’interface [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) vers un contrôle sur une boîte de dialogue, les clients doivent obtenir le handle de fenêtre du contrôle, puis appeler [**AccessibleObjectFromWindow**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromwindow).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[IAccessible, interface](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)
</dt> </dl>

 

