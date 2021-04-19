---
title: Contrôle Up-Down (référence des éléments d’interface utilisateur MSAA)
description: Un contrôle up-down, également appelé contrôle spin, combine une paire de boutons affichée sous forme de flèches avec un contrôle d’édition associé. Un clic sur les flèches incrémente ou décrémente la valeur dans le contrôle d’édition.
ms.assetid: 45e56c0f-4ac6-4731-b9a6-be4613bf40ae
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6fd2d28acc4c14a89ec73f5994ed0af47202145a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106541813"
---
# <a name="up-down-control-msaa-ui-element-reference"></a>Contrôle Up-Down (référence des éléments d’interface utilisateur MSAA)

> [!Note]  
> Cette rubrique décrit **les objets de contrôle up-up dans le** cadre de la référence à l’élément d’interface utilisateur MSAA. La création d’objets de **contrôle up-up** dans diverses infrastructures d’interface utilisateur n’est pas décrite ici. Consultez la documentation de référence sur les API pour l’infrastructure d’interface utilisateur que vous utilisez.

 

Un contrôle up-down, également appelé contrôle spin, combine une paire de boutons affichée sous forme de flèches avec un contrôle d’édition associé. Un clic sur les flèches incrémente ou décrémente la valeur dans le contrôle d’édition.

Le nom de la classe de fenêtre pour un contrôle up-UpDown est la \_ classe, qui est définie comme « msctls \_ updown32 » dans commctrl. h.

## <a name="iaccessible-methods"></a>Méthodes IAccessible

Un contrôle up-out prend en charge les méthodes [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) suivantes :

-   [**accHitTest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)
-   [**accLocation**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation)
-   [**accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)
-   [**accSelect**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect)

## <a name="iaccessible-properties"></a>Propriétés IAccessible

Un contrôle up-out prend en charge les propriétés [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) suivantes :



| Propriété                                                                 | Commentaires                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
|--------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Obtient \_ accChild**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchild)           |                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| [**Obtient \_ accChildCount**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchildcount) | La propriété **ChildCount** est « 2 » (flèches haut et bas).                                                                                                                                                                                                                                                                                                                                                                                                           |
| [**Obtient \_ accFocus**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accfocus)           |                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| [**Obtient \_ accHelp**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acchelp)             |                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| [**Obtient \_ accHelpTopic**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acchelptopic)   |                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| [**Obtient \_ accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)             | La propriété **Name** de l’objet contrôle up-up est obtenue à partir du texte de la fenêtre (ou de la légende) du contrôle. Ce texte n’est pas affiché avec le contrôle up-out, afin que les développeurs de serveur doivent fournir un texte explicite dans l’instruction de définition de ressource du contrôle pour aider les utilisateurs des utilitaires clients à identifier le contrôle. La propriété **Name** pour le bouton de flèche supérieure dans le contrôle up-up est « More », et la propriété **Name** pour le bouton flèche bas est « Less ». |
| [**Obtient \_ accParent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent)         | La propriété **parent** du contrôle up-UpDown est une fenêtre ( [**\_ \_ fenêtre système de rôle**](object-roles.md) ) qui entoure le contrôle et qui a les mêmes nom de propriété de **nom** et de classe de fenêtre que le contrôle. La propriété **parent** des boutons de direction haut et bas est l’objet de contrôle up-up.                                                                                                                                                    |
| [**Obtient \_ accRole**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole)             | La propriété de **rôle** pour l’objet de contrôle up-out est le [**\_ système Role \_ SPINBUTTON**](object-roles.md). La propriété **role** pour les boutons fléchés est [**role \_ système \_ PUSHBUTTON**](object-roles.md).                                                                                                                                                                                                                          |
| [**Obtient \_ accState**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate)           | La propriété d’État pour l’objet de contrôle up-up est l’une des [valeurs](object-state-constants.md)suivantes : système d’État axé sur le [**\_ système \_ d’État**](object-state-constants.md) pouvant être \| [**\_ \_ actif**](object-state-constants.md)<br/>                                                                                                                                                                                      |
| [**Obtient \_ accValue**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accvalue)           |                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |



 

## <a name="notes"></a>Notes

Microsoft Active Accessibility expose le contrôle d’édition associé en tant qu’objet distinct.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[IAccessible, interface](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)
</dt> </dl>

 

 





