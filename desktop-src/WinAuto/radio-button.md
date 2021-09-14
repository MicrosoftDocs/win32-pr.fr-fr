---
title: Case d’option (référence de l’élément d’interface utilisateur MSAA)
description: Les cases d’option permettent de sélectionner l’une des différentes options, généralement dans une boîte de dialogue.
ms.assetid: cf4568ff-1bc4-4770-bc54-a5d08ac0a60c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9766e85f530281e4f843c4d39fd41fe35d4fb620
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127010660"
---
# <a name="radio-button-msaa-ui-element-reference"></a>Case d’option (référence de l’élément d’interface utilisateur MSAA)

> [!Note]  
> Cette rubrique décrit les objets case d' **option** à des fins de référence d’élément d’interface utilisateur MSAA. La création d’objets case d' **option** dans différentes infrastructures d’interface utilisateur n’est pas décrite ici. Consultez la documentation de référence sur les API pour l’infrastructure d’interface utilisateur que vous utilisez.

 

Les cases d’option permettent de sélectionner l’une des différentes options, généralement dans une boîte de dialogue. Une case d’option contient un petit cercle avec le texte en regard de celle-ci. Lorsque cette option est sélectionnée, le cercle est entouré d’un cercle plus petit et rempli. Si vous sélectionnez un bouton dans un jeu désélectionnant le bouton sélectionné précédemment, une seule des options de l’ensemble est sélectionnée à la fois.

Le nom de la classe de fenêtre pour une case d’option est « BUTTON ».

## <a name="iaccessible-methods"></a>Méthodes IAccessible

Une case d’option prend en charge les méthodes [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) suivantes :



| Méthode                                                                    | Commentaires                                                                                                      |
|---------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------|
| [**accDoDefaultAction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accdodefaultaction) | La méthode [**accDoDefaultAction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accdodefaultaction) clique sur la case d’option. |
| [**accHitTest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)                 |                                                                                                               |
| [**accLocation**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation)               |                                                                                                               |
| [**accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)               |                                                                                                               |
| [**accSelect**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect)                   |                                                                                                               |



 

## <a name="iaccessible-properties"></a>Propriétés IAccessible

Une case d’option prend en charge les propriétés [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) suivantes :



| Propriété                                                                             | Commentaires                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|--------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Obtient \_ accChild**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchild)                       |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| [**Obtient \_ accChildCount**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchildcount)             | La propriété **ChildCount** est égale à zéro.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| [**Obtient \_ accDefaultAction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accdefaultaction)       | La propriété **DefaultAction** pour une case d’option est « check ».                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| [**Obtient \_ accDescription**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accdescription)           |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| [**Obtient \_ accFocus**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accfocus)                       |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| [**Obtient \_ accHelp**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acchelp)                         |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| [**Obtient \_ accHelpTopic**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acchelptopic)               |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| [**Obtient \_ accKeyboardShortcut**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acckeyboardshortcut) | La propriété **KeyboardShortcut** est la clé d’accès de la case d’option, qui est un caractère souligné dans le texte de la fenêtre du contrôle. Cette chaîne contient le caractère clé d’accès ajouté à la chaîne « ALT + ».                                                                                                                                                                                                                                                                                                                                                                                                                           |
| [**Obtient \_ accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)                         | La propriété **Name** est obtenue à partir du texte de la fenêtre (ou de la légende) du contrôle, qui est affiché avec la case d’option.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| [**Obtient \_ accParent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent)                     | La propriété **parente** est une fenêtre [**( \_ \_ fenêtre système de rôle**](object-roles.md) ) qui entoure le contrôle et possède les mêmes propriétés de **nom** et nom de classe de fenêtre que le contrôle.                                                                                                                                                                                                                                                                                                                                                                                                                               |
| [**Obtient \_ accRole**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole)                         | La propriété **role** est [**le \_ \_ RadioButton du système de rôle**](object-roles.md).                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| [**Obtient \_ accState**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate)                       | La propriété d' **État** est une combinaison d’une ou plusieurs des [valeurs](object-state-constants.md)suivantes : état du système d’état [**\_ \_ invisible**](object-state-constants.md) système d’état \| [**\_ \_ non disponible**](object-state-constants.md) système d’État Focus système état \| [**\_ \_**](object-state-constants.md) \| [**\_ \_ actif**](object-state-constants.md) système d’état \| [**\_ \_ activé**](object-state-constants.md) \| [**\_ \_ normal**](object-state-constants.md)<br/> |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[IAccessible, interface](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)
</dt> <dt>

[**Case à cocher**](check-box.md)
</dt> <dt>

[**Zone de groupe**](group-box.md)
</dt> <dt>

[**Bouton de commande**](push-button.md)
</dt> </dl>

 

 





