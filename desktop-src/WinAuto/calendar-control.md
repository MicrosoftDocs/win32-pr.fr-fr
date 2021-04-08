---
title: Calendar, contrôle (référence des éléments d’interface utilisateur MSAA)
description: Les contrôles Calendar offrent un moyen simple et intuitif pour un utilisateur de sélectionner une date à partir d’une interface familière.
ms.assetid: cfb1e420-bb8f-4100-9c83-304d11573c0e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 63acb3ca83f6b7e71740acee4232e081e11594e4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103839665"
---
# <a name="calendar-control-msaa-ui-element-reference"></a>Calendar, contrôle (référence des éléments d’interface utilisateur MSAA)

> [!Note]  
> Cette rubrique décrit les objets de **contrôle de calendrier** à des fins de référence d’élément d’interface utilisateur MSAA. La procédure de création d’objets de **contrôle Calendar** dans différentes infrastructures d’interface utilisateur n’est pas décrite ici. Consultez la documentation de référence sur les API pour l’infrastructure d’interface utilisateur que vous utilisez.

 

Les contrôles Calendar offrent un moyen simple et intuitif pour un utilisateur de sélectionner une date à partir d’une interface familière.

Le nom de la classe de fenêtre pour un contrôle Month Calendar est la \_ classe calendrier monthcal, qui est définie comme « SysMonthCal32 » dans commctrl. h. Les informations contenues dans cette rubrique s’appliquent au contrôle Month Calendar dans la version 5 de commctrl. h.

## <a name="iaccessible-methods"></a>Méthodes IAccessible

Les contrôles Calendar prennent en charge les méthodes [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) suivantes :

-   [**accHitTest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)
-   [**accLocation**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation)
-   [**accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)
-   [**accSelect**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect)

## <a name="iaccessible-properties"></a>Propriétés IAccessible

Les contrôles Calendar prennent en charge les propriétés [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) suivantes :



| Propriété                                                                 | Commentaires                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
|--------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Obtient \_ accChildCount**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchildcount) | La propriété **ChildCount** est égale à zéro.                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| [**Obtient \_ accFocus**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accfocus)           |                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| [**Obtient \_ accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)             | La propriété **Name** est obtenue à partir du contrôle texte statique qui étiquette le contrôle calendrier. Lors de la création de contrôles, les développeurs de serveur doivent s’assurer qu’un contrôle de texte statique précède immédiatement le contrôle qu’il étiquette dans l’ordre de tabulation.                                                                                                                                                                                                                 |
| [**Obtient \_ accParent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent)         | La propriété **parente** est une fenêtre [**( \_ \_ fenêtre système de rôle**](object-roles.md) ) qui entoure le contrôle et possède les mêmes propriétés de **nom** et nom de classe de fenêtre que le contrôle.                                                                                                                                                                                                                                                             |
| [**Obtient \_ accRole**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole)             | La propriété de **rôle** est [**client de \_ système \_ de rôle**](object-roles.md).                                                                                                                                                                                                                                                                                                                                                                               |
| [**Obtient \_ accState**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate)           | La propriété **State** est une combinaison d’une ou plusieurs des valeurs suivantes [](object-state-constants.md)[**état système \_ état \_**](object-state-constants.md) indisponible système d’état \| [**\_ \_ indisponible**](object-state-constants.md) système d’état \| [**\_ \_**](object-state-constants.md) \| [**\_ \_ focus**](object-state-constants.md) système<br/> |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[IAccessible, interface](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)
</dt> </dl>

 

 





