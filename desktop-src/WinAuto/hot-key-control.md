---
title: Contrôle de touche d’accès rapide (référence des éléments d’interface utilisateur MSAA)
description: Les contrôles de touche d’accès rapide permettent aux utilisateurs d’entrer une combinaison de touches utilisées comme touche d’accès rapide, ce qui leur permet d’exécuter une action rapidement. Un contrôle de touche d’accès rapide affiche les séquences de touches entrées par l’utilisateur et s’assure que l’utilisateur sélectionne une combinaison de touches valide.
ms.assetid: 56c9fee4-f3d3-4f61-8587-bf80186aa5b3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5aed12ce64fe25c091f6204d9143a0c6ebefb65a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104310758"
---
# <a name="hot-key-control-msaa-ui-element-reference"></a>Contrôle de touche d’accès rapide (référence des éléments d’interface utilisateur MSAA)

Les contrôles de touche d’accès rapide permettent aux utilisateurs d’entrer une combinaison de touches utilisées comme touche d’accès rapide, ce qui leur permet d’exécuter une action rapidement. Un contrôle de touche d’accès rapide affiche les séquences de touches entrées par l’utilisateur et s’assure que l’utilisateur sélectionne une combinaison de touches valide.

Le nom de la classe de fenêtre pour un contrôle de touche d’accès rapide est la \_ classe Hotkey, qui est définie comme « msctls \_ hotkey32 » dans commctrl. h.

## <a name="iaccessible-methods"></a>Méthodes IAccessible

Les contrôles de touche d’accès rapide prennent en charge les méthodes [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) suivantes :

-   [**accHitTest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)
-   [**accLocation**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation)
-   [**accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)
-   [**accSelect**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect)

## <a name="iaccessible-properties"></a>Propriétés IAccessible

Les contrôles de touche d’accès rapide prennent en charge les propriétés [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) suivantes :



| Propriété                                                                             | Commentaires                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|--------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Obtient \_ accChildCount**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchildcount)             | La propriété **ChildCount** est toujours égale à zéro.                                                                                                                                                                                                                                                                                                                                                                                                                              |
| [**Obtient \_ accFocus**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accfocus)                       |                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| [**Obtient \_ accKeyboardShortcut**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acckeyboardshortcut) | La propriété **KeyboardShortcut** est la clé d’accès du contrôle de touche d’accès rapide, qui est un caractère souligné dans le texte de l’étiquette du contrôle de touche d’accès rapide. La chaîne retournée contient le caractère clé d’accès ajouté à la chaîne « ALT + ».                                                                                                                                                                                                                                 |
| [**Obtient \_ accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)                         | La propriété **Name** est le texte d’un contrôle de texte statique qui étiquette le contrôle de touche d’accès rapide.                                                                                                                                                                                                                                                                                                                                                                            |
| [**Obtient \_ accParent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent)                     | La propriété **parente** est une fenêtre [**( \_ \_ fenêtre système de rôle**](object-roles.md) ) qui entoure le contrôle et possède les mêmes propriétés de **nom** et nom de classe de fenêtre que le contrôle.                                                                                                                                                                                                                                                              |
| [**Obtient \_ accRole**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole)                         | La propriété **role** est le [**système de rôle \_ \_ HOTKEYFIELD**](object-roles.md).                                                                                                                                                                                                                                                                                                                                                                      |
| [**Obtient \_ accState**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate)                       | La propriété d' **État** est une combinaison d’une ou plusieurs des [valeurs](object-state-constants.md)suivantes : état du système d’état [**\_ \_ invisible**](object-state-constants.md) système d’état \| [**\_ \_ non disponible**](object-state-constants.md) système \| [**\_ \_**](object-state-constants.md) \| [**\_ \_**](object-state-constants.md)<br/> |
| [**Obtient \_ accValue**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accvalue)                       | La propriété **valeur** est une chaîne qui contient le texte dans le champ clé d’accès.                                                                                                                                                                                                                                                                                                                                                                                          |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[IAccessible, interface](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)
</dt> </dl>

 

 





