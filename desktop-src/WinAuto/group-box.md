---
title: Zone de groupe (référence des éléments d’interface utilisateur MSAA)
description: Une zone de groupe est un rectangle qui entoure un ensemble de contrôles, tels que des cases à cocher ou des cases d’option, et qui contient un texte défini par l’application (étiquette).
ms.assetid: c6cd81a1-76c0-41c5-bb7f-4796ea7e3114
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a105242aabd49d87241a2a49bdaca5c19edd350b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103674581"
---
# <a name="group-box-msaa-ui-element-reference"></a>Zone de groupe (référence des éléments d’interface utilisateur MSAA)

> [!Note]  
> Cette rubrique décrit les objets de **zone de groupe** à des fins de référence d’élément d’interface utilisateur MSAA. La procédure de création d’objets de **zone de groupe** dans différentes infrastructures d’interface utilisateur n’est pas décrite ici. Consultez la documentation de référence sur les API pour l’infrastructure d’interface utilisateur que vous utilisez.

 

Une zone de groupe est un rectangle qui entoure un ensemble de contrôles, tels que des cases à cocher ou des cases d’option, et qui contient un texte défini par l’application (étiquette).

Le seul but d’une zone de groupe est d’organiser les contrôles liés par un objectif commun, indiqué par l’étiquette.

Le nom de la classe de fenêtre pour une zone de groupe est « BUTTON ».

## <a name="iaccessible-methods"></a>Méthodes IAccessible

Une zone de groupe prend en charge les méthodes [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) suivantes :

-   [**accHitTest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)
-   [**accLocation**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation)
-   [**accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)

## <a name="iaccessible-properties"></a>Propriétés IAccessible

Une zone de groupe prend en charge les propriétés [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) suivantes :



| Propriété                                                                             | Commentaires                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|--------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Obtient \_ accChildCount**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchildcount)             | La propriété **ChildCount** est toujours égale à zéro.                                                                                                                                                                                                                                                                                                                                                                                                                              |
| [**Obtient \_ accFocus**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accfocus)                       |                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| [**Obtient \_ accKeyboardShortcut**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acckeyboardshortcut) | Les zones de groupe n’ont pas de raccourcis clavier. Toutefois, si le texte de la fenêtre de la zone de groupe contient un caractère perluète (&), Microsoft Active Accessibility retourne une chaîne non null en tant que propriété **KeyboardShortcut** .                                                                                                                                                                                                                                            |
| [**Obtient \_ accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)                         | La propriété **Name** est obtenue à partir du texte de la fenêtre (ou de la légende) du contrôle, qui est affiché avec la zone de groupe.                                                                                                                                                                                                                                                                                                                                                    |
| [**Obtient \_ accParent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent)                     | La propriété **parente** est une fenêtre [**( \_ \_ fenêtre système de rôle**](object-roles.md) ) qui entoure le contrôle et possède les mêmes propriétés de **nom** et nom de classe de fenêtre que le contrôle.                                                                                                                                                                                                                                                              |
| [**Obtient \_ accRole**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole)                         | La propriété **role** est [**le \_ \_ regroupement du système de rôle**](object-roles.md).                                                                                                                                                                                                                                                                                                                                                                            |
| [**Obtient \_ accState**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate)                       | La propriété d' **État** est une combinaison d’une ou plusieurs des [valeurs](object-state-constants.md)suivantes : état du système d’état [**\_ \_ invisible**](object-state-constants.md) système d’état \| [**\_ \_ non disponible**](object-state-constants.md) système \| [**\_ \_**](object-state-constants.md) \| [**\_ \_**](object-state-constants.md)<br/> |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[IAccessible, interface](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)
</dt> </dl>

 

 





