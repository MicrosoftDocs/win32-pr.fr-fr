---
title: Utilisation des affichages en mosaïque
description: Cette rubrique montre comment définir l’affichage en mosaïque pour un contrôle List View.
ms.assetid: BDE17F4B-3A15-48BB-8160-036AD0DC3B41
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 616a9bb8a2c1707d903f0ebe2b6de86511dc6ce4
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/04/2020
ms.locfileid: "103941480"
---
# <a name="how-to-use-tile-views"></a>Utilisation des affichages en mosaïque

Cette rubrique montre comment définir l’affichage en mosaïque pour un contrôle List View. En mode mosaïque, chaque élément est représenté par une grande icône avec une ou plusieurs lignes de texte d’accompagnement. Pour obtenir une illustration, consultez [à propos des contrôles de List-View](list-view-controls-overview.md).

## <a name="what-you-need-to-know"></a>Ce que vous devez savoir

### <a name="technologies"></a>Technologies

-   [Contrôles Windows](window-controls.md)

### <a name="prerequisites"></a>Prérequis

-   C/C++
-   Programmation de l’interface utilisateur Windows

## <a name="instructions"></a>Instructions


Définissez les paramètres d’affichage généraux pour l’affichage en mosaïque à l’aide de la macro [**ListView \_ SetTileViewInfo**](/windows/desktop/api/Commctrl/nf-commctrl-listview_settileviewinfo) . Utilisez la structure [**LVTILEVIEWINFO**](/windows/win32/api/commctrl/ns-commctrl-lvtileviewinfo) qui est passée à cette macro pour spécifier la position du texte par rapport à l’icône, la taille de chaque vignette (y compris le texte d’accompagnement) et le nombre maximal de lignes de texte.

Si vous ne souhaitez pas que les vignettes soient automatiquement dimensionnées, vous devez définir **LVTVIF \_ FIXEDSIZE** dans le membre **dwFlags** et **LVTVIM \_ Tile** dans le membre **dwMask** de [**LVTILEVIEWINFO**](/windows/win32/api/commctrl/ns-commctrl-lvtileviewinfo), ainsi que fournir les dimensions dans le membre **sizeTile** .

L’exemple de code C++ suivant définit les informations d’affichage en mosaïque pour un contrôle d’affichage de liste afin qu’un maximum de deux sous-éléments s’affiche pour chaque élément. Il définit également la taille de chaque vignette.


```C++
    SIZE size = { 100, 50 };
    LVTILEVIEWINFO tileViewInfo = {0};

    tileViewInfo.cbSize   = sizeof(tileViewInfo);
    tileViewInfo.dwFlags  = LVTVIF_FIXEDSIZE;
    tileViewInfo.dwMask   = LVTVIM_COLUMNS | LVTVIM_TILESIZE;
    tileViewInfo.cLines   = 2;
    tileViewInfo.sizeTile = size;

    ListView_SetTileViewInfo(hWndListView, &tileViewInfo);

```



Pour chaque élément de la liste, vous pouvez définir d’autres paramètres lorsque l’élément est inséré dans la liste, ou ultérieurement. La structure [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) utilisée avec [**ListView \_ InsertItem**](/windows/desktop/api/Commctrl/nf-commctrl-listview_insertitem) contient des membres qui spécifient les colonnes de données à afficher sous l’élément, ainsi que leur alignement. Ces mêmes paramètres d’affichage se trouvent également dans la structure [**LVTILEINFO**](/windows/win32/api/commctrl/ns-commctrl-lvtileinfo) utilisée avec [**ListView \_ SetTileInfo**](/windows/desktop/api/Commctrl/nf-commctrl-listview_settileinfo).

> [!Note]  
> Ici, « Columns » fait référence à l’affichage des colonnes dans l’affichage en mosaïque mais plutôt aux sous-éléments qui sont affichés dans les colonnes en mode Détails.

 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Référence du contrôle List-View](bumper-list-view-list-view-control-reference.md)
</dt> <dt>

[À propos des contrôles List-View](list-view-controls-overview.md)
</dt> <dt>

[Utilisation de contrôles List-View](using-list-view-controls.md)
</dt> </dl>

 

 




