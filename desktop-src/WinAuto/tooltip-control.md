---
title: ToolTip, contrôle (référence des éléments d’interface utilisateur MSAA)
description: Un contrôle ToolTip affiche une petite fenêtre contextuelle qui contient une ligne de texte qui décrit l’objectif d’un outil, représenté sous la forme d’un objet graphique, dans une application.
ms.assetid: d3a65d7b-b882-4a1a-bac2-6995b64cf4af
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 37557fd116084fc9ac53e8567afc90eda339750d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103840045"
---
# <a name="tooltip-control-msaa-ui-element-reference"></a>ToolTip, contrôle (référence des éléments d’interface utilisateur MSAA)

> [!Note]  
> Cette rubrique décrit les objets de **contrôle ToolTip** à des fins de référence des éléments d’interface utilisateur MSAA. La création d’objets de **contrôle ToolTip** dans différentes infrastructures d’interface utilisateur n’est pas décrite ici. Consultez la documentation de référence sur les API pour l’infrastructure d’interface utilisateur que vous utilisez.

 

Un contrôle ToolTip affiche une petite fenêtre contextuelle qui contient une ligne de texte qui décrit l’objectif d’un outil, représenté sous la forme d’un objet graphique, dans une application.

Le nom de la classe de fenêtre pour une info-bulle est la classe info-bulles \_ , qui est définie en tant que « classe info-bulles \_ » dans commctrl. h.

## <a name="iaccessible-methods"></a>Méthodes IAccessible

Un contrôle ToolTip prend en charge les méthodes [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) suivantes :

-   [**accHitTest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)
-   [**accLocation**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation)
-   [**accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)
-   [**accSelect**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect)

## <a name="iaccessible-properties"></a>Propriétés IAccessible

Un contrôle ToolTip prend en charge les propriétés [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) suivantes :



| Propriété                                                                 | Commentaires                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|--------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Obtient \_ accChildCount**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchildcount) | La propriété **ChildCount** est égale à zéro.                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| [**Obtient \_ accFocus**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accfocus)           |                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| [**Obtient \_ accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)             | La propriété **Name** est le texte contenu dans le contrôle ToolTip.                                                                                                                                                                                                                                                                                                                                                                                                       |
| [**Obtient \_ accParent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent)         | La propriété **parente** est une fenêtre [**( \_ \_ fenêtre système de rôle**](object-roles.md) ) qui entoure le contrôle et possède les mêmes propriétés de **nom** et nom de classe de fenêtre que le contrôle.                                                                                                                                                                                                                                                               |
| [**Obtient \_ accRole**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole)             | La propriété **role** est [**l' \_ \_ info-bulle du système Role**](object-roles.md).                                                                                                                                                                                                                                                                                                                                                                               |
| [**Obtient \_ accState**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate)           | La propriété d' **État** est une combinaison d’une ou plusieurs des [valeurs](object-state-constants.md)suivantes : état du système d’état [**\_ \_ invisible**](object-state-constants.md) système d’état \| [**\_ \_ non disponible**](object-state-constants.md) système \| [**\_ \_**](object-state-constants.md) \| [**\_ \_**](object-state-constants.md)<br/> |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[IAccessible, interface](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)
</dt> </dl>

 

 





