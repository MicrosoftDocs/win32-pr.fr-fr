---
title: Contrôle animation (référence des éléments de l’interface utilisateur MSAA)
description: Les contrôles d’animation affichent en mode silencieux un clip vidéo entrelacé (AVI) audio. Les contrôles d’animation sont généralement affichés lorsque des fichiers sont copiés ou lorsqu’une autre tâche qui prend du temps est exécutée.
ms.assetid: 2a31d4ba-a1bd-478b-86a9-726fa93ab714
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 43ca7cf7e4b8a2174dae81b1770b2d877f749502
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103673329"
---
# <a name="animation-control-msaa-ui-element-reference"></a>Contrôle animation (référence des éléments de l’interface utilisateur MSAA)

Les contrôles d’animation affichent en mode silencieux un clip vidéo entrelacé (AVI) audio. Les contrôles d’animation sont généralement affichés lorsque des fichiers sont copiés ou lorsqu’une autre tâche qui prend du temps est exécutée.

Le nom de la classe de fenêtre pour un contrôle d’animation est ANIMEr la \_ classe, qui est défini en tant que « SysAnimate32 » dans commctrl. h.

## <a name="iaccessible-methods"></a>Méthodes IAccessible

Les contrôles d’animation prennent en charge les méthodes [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) suivantes :

-   [**accHitTest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)
-   [**accLocation**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation)
-   [**accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)
-   [**accSelect**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect)

## <a name="iaccessible-properties"></a>Propriétés IAccessible

Les contrôles d’animation prennent en charge les propriétés [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) suivantes :



| Propriété                                                                             | Commentaires                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
|--------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Obtient \_ accChildCount**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchildcount)             | La propriété **ChildCount** est égale à zéro.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| [**Obtient \_ accKeyboardShortcut**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acckeyboardshortcut) | Les contrôles d’animation n’ont pas de raccourcis clavier. Toutefois, si l’étiquette du contrôle contient une touche d’accès (un caractère souligné dans le texte de l’étiquette du contrôle), la méthode [**\_ accKeyboardShortcut**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acckeyboardshortcut) renvoie une chaîne non null. Cette chaîne contient le caractère clé d’accès ajouté à la chaîne « ALT + ». Par exemple, si l’étiquette est « téléchargement de fichiers », **KeyboardShortcut** est « ALT + d ».                                                                                        |
| [**Obtient \_ accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)                         | La propriété **Name** est obtenue à partir du contrôle de texte statique qui étiquette le contrôle d’animation. Lors de la création de contrôles, les développeurs de serveur doivent s’assurer qu’un contrôle de texte statique précède immédiatement le contrôle qu’il étiquette dans l’ordre de tabulation.                                                                                                                                                                                                                                                                                             |
| [**Obtient \_ accParent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent)                     | La propriété **parente** est une fenêtre [**( \_ \_ fenêtre système de rôle**](object-roles.md) ) qui entoure le contrôle et possède les mêmes propriétés de **nom** et nom de classe de fenêtre que le contrôle.                                                                                                                                                                                                                                                                                                                                          |
| [**Obtient \_ accRole**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole)                         | La propriété **role** est [**l' \_ \_ animation du système de rôle**](object-roles.md).                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| [**Obtient \_ accState**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate)                       | La propriété **State** est une combinaison d’une ou plusieurs des constantes d’état d’objet suivantes : état du système d’État indisponible système d’État indisponible système d' [**\_ \_**](object-state-constants.md) état \| [**\_ \_ indisponible**](object-state-constants.md) système \| [**\_ \_**](object-state-constants.md) \| [**\_ \_ animé**](object-state-constants.md)<br/> Pour plus d’informations, consultez [constantes d’état d’objet](object-state-constants.md).<br/> |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[IAccessible, interface](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)
</dt> </dl>

 

 





