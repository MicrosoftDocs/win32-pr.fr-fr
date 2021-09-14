---
title: Push Button (référence des éléments d’interface utilisateur MSAA)
description: Un bouton de commande est un petit objet rectangulaire utilisé pour effectuer une action. Par exemple, les boutons OK et annuler d’une boîte de dialogue sont des boutons de commande.
ms.assetid: 26dbe4a0-4110-4569-bac6-fa0a95c785dd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e188b58501509fd934ab6396a21beb209857661
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127010661"
---
# <a name="push-button-msaa-ui-element-reference"></a>Push Button (référence des éléments d’interface utilisateur MSAA)

Un bouton de commande est un petit objet rectangulaire utilisé pour effectuer une action. Par exemple, les boutons **OK** et **Annuler** d’une boîte de dialogue sont des boutons de commande.

Le nom de la classe de fenêtre pour un bouton de commande est « BUTTON ».

## <a name="iaccessible-methods"></a>Méthodes IAccessible

Un bouton de commande prend en charge les méthodes [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) suivantes :



| Méthode                                                                    | Commentaires                                                                                                     |
|---------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------|
| [**accDoDefaultAction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accdodefaultaction) | La méthode [**accDoDefaultAction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accdodefaultaction) clique sur le bouton de commande. |
| [**accHitTest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)                 |                                                                                                              |
| [**accLocation**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation)               |                                                                                                              |
| [**accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)               |                                                                                                              |
| [**accSelect**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect)                   |                                                                                                              |



 

## <a name="iaccessible-properties"></a>Propriétés IAccessible

Un bouton de commande prend en charge les propriétés [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) suivantes :



| Propriété                                                                             | Commentaires                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
|--------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Obtient \_ accChild**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchild)                       |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| [**Obtient \_ accChildCount**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchildcount)             | La propriété **ChildCount** est égale à zéro ou plus.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| [**Obtient \_ accDefaultAction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accdefaultaction)       | La propriété **DefaultAction** est « Press ».                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| [**Obtient \_ accDescription**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accdescription)           |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| [**Obtient \_ accKeyboardShortcut**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acckeyboardshortcut) | La propriété **KeyboardShortcut** est la clé d’accès du bouton, qui est un caractère souligné dans le texte du texte de la fenêtre du bouton. Par exemple, « Alt + o » est la propriété **KeyboardShortcut** d’un bouton **OK** .                                                                                                                                                                                                                                                                                                                                                                                                                     |
| [**Obtient \_ accFocus**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accfocus)                       |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| [**Obtient \_ accHelp**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acchelp)                         |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| [**Obtient \_ accHelpTopic**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acchelptopic)               |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| [**Obtient \_ accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)                         | La propriété **Name** est obtenue à partir du texte de la fenêtre (ou de la légende) du contrôle, qui est affiché dans le bouton de commande. Par exemple, « OK » est la propriété de **nom** d’un bouton **OK** .                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| [**Obtient \_ accParent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent)                     | La propriété **parente** est une fenêtre [**( \_ \_ fenêtre système de rôle**](object-roles.md) ) qui entoure le contrôle et possède les mêmes propriétés de **nom** et nom de classe de fenêtre que le contrôle.                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| [**Obtient \_ accRole**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole)                         | La propriété **role** est [**role \_ - \_ PUSHBUTTON système**](object-roles.md).                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| [**Obtient \_ accState**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate)                       | La propriété d' **État** est une combinaison d’une ou plusieurs des [valeurs](object-state-constants.md)suivantes : [**état \_ système \_**](object-state-constants.md) indisponible système d’état \| [**\_ \_ indisponible**](object-state-constants.md) système État Focus système état \| [**\_ \_**](object-state-constants.md) \| [**\_ \_ focus**](object-state-constants.md) système \| [**\_ \_**](object-state-constants.md) \| [**\_ \_**](object-state-constants.md) État du système d’état activé par défaut<br/> |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[IAccessible, interface](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)
</dt> <dt>

[**Case à cocher**](check-box.md)
</dt> <dt>

[**Zone de groupe**](group-box.md)
</dt> <dt>

[**RadioButton**](radio-button.md)
</dt> </dl>

 

 





