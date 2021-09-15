---
title: Contrôle header (référence des éléments d’interface utilisateur MSAA)
description: Un contrôle header affiche des en-têtes en haut des colonnes d’informations et permet à l’utilisateur de trier les informations en cliquant sur les en-têtes. Windows L’Explorateur utilise un contrôle d’en-tête lorsque le mode Détails est sélectionné.
ms.assetid: 669d6bb8-7bc4-4e6f-bf4f-207887f44b83
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e6d069770b14ad3ba58022af28ad07fc78cb8c5b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127403691"
---
# <a name="header-control-msaa-ui-element-reference"></a>Contrôle header (référence des éléments d’interface utilisateur MSAA)

> [!Note]  
> Cette rubrique décrit les objets de **contrôle header** à des fins de référence des éléments d’interface utilisateur MSAA. La procédure de création d’objets de **contrôle header** dans différentes infrastructures d’interface utilisateur n’est pas décrite ici. Consultez la documentation de référence sur les API pour l’infrastructure d’interface utilisateur que vous utilisez.

 

Un contrôle header affiche des en-têtes en haut des colonnes d’informations et permet à l’utilisateur de trier les informations en cliquant sur les en-têtes. Windows L’Explorateur utilise un contrôle d’en-tête lorsque le mode Détails est sélectionné.

Le nom de la classe de fenêtre pour un contrôle header est l' \_ en-tête WC, qui est défini comme « SysHeader32 » dans commctrl. h.

## <a name="iaccessible-methods"></a>Méthodes IAccessible

Un contrôle header prend en charge les méthodes [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) suivantes :



| Méthode                                                                    | Commentaires                                                        |
|---------------------------------------------------------------------------|-----------------------------------------------------------------|
| [**accDoDefaultAction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accdodefaultaction) | Cette méthode effectue l’action par défaut en cliquant sur l’en-tête. |
| [**accHitTest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)                 |                                                                 |
| [**accLocation**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation)               |                                                                 |
| [**accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)               |                                                                 |
| [**accSelect**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect)                   |                                                                 |



 

## <a name="iaccessible-properties"></a>Propriétés IAccessible

Un contrôle header prend en charge les propriétés [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) suivantes :



| Propriété                                                                       | Commentaires                                                                                                                                                                                                                               |
|--------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Obtient \_ accChildCount**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchildcount)       | La propriété **ChildCount** est égale à zéro.                                                                                                                                                                                                   |
| [**Obtient \_ accDefaultAction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accdefaultaction) | La propriété **DefaultAction** est « Click ».                                                                                                                                                                                             |
| [**Obtient \_ accFocus**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accfocus)                 |                                                                                                                                                                                                                                        |
| [**Obtient \_ accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)                   | La propriété **Name** est identique au nom de l’en-tête de colonne.                                                                                                                                                                    |
| [**Obtient \_ accParent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent)               | La propriété **parent** est une fenêtre ( [**\_ \_ liste système de rôles**](object-roles.md) ) qui entoure le contrôle et possède le même nom de classe de fenêtre que le contrôle.                                                      |
| [**Obtient \_ accRole**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole)                   | La propriété **role** est le [**système de rôle \_ \_ COLUMNHEADER**](object-roles.md).                                                                                                                                  |
| [**Obtient \_ accState**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate)                 | La valeur de la propriété **State** est toujours le [**système d’état \_ \_ ReadOnly**](object-state-constants.md) et peut également inclure le [**système d’état \_ \_ invisible**](object-state-constants.md). |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[IAccessible, interface](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)
</dt> </dl>

 

 




