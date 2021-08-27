---
title: Comment utiliser des groupes dans un List-View
description: Cette rubrique explique comment créer une instance d’un groupe et l’ajouter à un contrôle List View.
ms.assetid: 8486B9A2-C519-4912-9E88-3BAFCC4D51CF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: edaad657d9ea6b71bac1d06a34a0aa29b99c26e204629e503a9e55531da162b7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120132119"
---
# <a name="how-to-use-groups-in-a-list-view"></a>Comment utiliser des groupes dans un List-View

Cette rubrique explique comment créer une instance d’un groupe et l’ajouter à un contrôle List View. Le regroupement permet à un utilisateur de réorganiser des listes en groupes d’éléments qui sont répartis visuellement sur la page, à l’aide d’un séparateur horizontal et d’un titre de groupe.

## <a name="what-you-need-to-know"></a>Bon à savoir

### <a name="technologies"></a>Technologies

-   [Windows Commandes](window-controls.md)

### <a name="prerequisites"></a>Prérequis

-   C/C++
-   Windows Programmation de l’interface utilisateur

## <a name="instructions"></a>Instructions


Pour utiliser des groupes dans un contrôle List-View, assurez-vous que le contrôle comprend le style de fenêtre [**LVS \_ ALIGNTOP**](list-view-window-styles.md) .

Lorsque vous ajoutez un élément à la liste, vous l’affectez à un groupe en définissant le membre **iGroupId** de la structure [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) de l’élément sur la valeur du membre **iGroupId** de la structure [**LVGROUP**](/windows/win32/api/commctrl/ns-commctrl-lvgroup) du groupe. Un élément qui n’est pas assigné à un groupe n’apparaît pas dans la liste lorsque la vue de groupe est activée. Pour activer ou désactiver la vue de groupe, utilisez la macro [**ListView \_ EnableGroupView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_enablegroupview) .

L’exemple suivant montre comment créer un groupe avec un en-tête et l’ajouter à un contrôle List-View.


```C++
    LVGROUP group;

    group.cbSize    = sizeof(LVGROUP);
    group.mask      = LVGF_HEADER | LVGF_GROUPID;
    group.pszHeader = TEXT("Dogs");
    group.iGroupId  = 1;

    ListView_InsertGroup(hWndListView, -1, &group);

```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Référence du contrôle List-View](bumper-list-view-list-view-control-reference.md)
</dt> <dt>

[À propos des contrôles List-View](list-view-controls-overview.md)
</dt> <dt>

[Utilisation de contrôles List-View](using-list-view-controls.md)
</dt> </dl>

 

 




