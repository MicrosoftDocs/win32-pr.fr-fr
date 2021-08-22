---
title: Fenêtre du Bureau (référence des éléments d’interface utilisateur MSAA)
description: La fenêtre bureau affiche la vue Liste du Bureau (qui contient des icônes comme Poste de travail) et la barre des tâches qui contient le bouton Démarrer.
ms.assetid: 3668c26e-6462-4219-95d3-507811ed7f3c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c0a1c096ea759f9df2115a35e79e72fe7257e93b9d9a21d9f596b890644a6a67
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118994219"
---
# <a name="desktop-window-msaa-ui-element-reference"></a>Fenêtre du Bureau (référence des éléments d’interface utilisateur MSAA)

La fenêtre bureau affiche la vue Liste du Bureau (qui contient des icônes comme Poste de travail) et la barre des tâches qui contient le bouton **Démarrer** .

Cet objet est rarement interrogé par les clients, car l’affichage de liste et la barre des tâches couvrent tout le bureau. L’objet Desktop est récupéré lorsque vous vous connectez, avant que l’interpréteur de commandes du système d’exploitation affiche le mode liste et la barre des tâches. Dans certains cas, le bureau est obtenu lors de la navigation à partir d’autres objets.

Le nom de la classe de fenêtre de la fenêtre du Bureau est « \# 32769 ».

## <a name="iaccessible-methods"></a>Méthodes IAccessible

La fenêtre du Bureau prend en charge les méthodes [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) suivantes :

-   [**accHitTest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)
-   [**accLocation**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation)
-   [**accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)
-   [**accSelect**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect)

## <a name="iaccessible-properties"></a>Propriétés IAccessible

La fenêtre du Bureau prend en charge les propriétés [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) suivantes :



| Propriété                                                                 | Commentaires                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|--------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Obtient \_ accChildCount**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchildcount) |                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| [**Obtient \_ accFocus**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accfocus)           |                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| [**Obtient \_ accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)             | La propriété Name est « Desktop ».                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| [**Obtient \_ accRole**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole)             | La propriété de **rôle** est [**client de \_ système \_ de rôle**](object-roles.md).                                                                                                                                                                                                                                                                                                                                                                                |
| [**Obtient \_ accSelection**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accselection)   |                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| [**Obtient \_ accState**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate)           | La propriété d' **État** est une combinaison d’une ou plusieurs des [valeurs](object-state-constants.md)suivantes : état du système d’état [**\_ \_ invisible**](object-state-constants.md) système d’état \| [**\_ \_ non disponible**](object-state-constants.md) système \| [**\_ \_**](object-state-constants.md) \| [**\_ \_**](object-state-constants.md)<br/> |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[IAccessible, interface](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)
</dt> </dl>

 

 





