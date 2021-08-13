---
title: UI_PKEY_RecentItems
description: Identifie la propriété RecentItems de l’interface utilisateur \_ \_ .
ms.assetid: 54e7ad1f-86b3-45e0-a0f4-5ee0d08e9d4b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c04e18400f297edae1f9a1eda54bccbcd6c31c9f1d9b40408e243b6c275a83ff
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118437955"
---
# <a name="ui_pkey_recentitems"></a>IU \_ \_ RecentItems

Identifie la propriété RecentItems de l’interface utilisateur \_ \_ .

```
propertyDescription
   name = UI_PKEY_RecentItems
   shellPKey = UI_PKEY_RecentItems
   formatID = 00000350-7363-696e-8441798acf5aebb7
   propID = 350
   typeInfo
      type = VT_ARRAY | VT_UNKNOWN
```

## <a name="remarks"></a>Remarques

[Interface utilisateur \_ Le \_ ](windowsribbon-reference-properties-uipkey-pinned.md) groupe de lignes ajouté est utilisé par une application pour interroger le tableau d’éléments dans la collection d’éléments utilisés le plus récemment (MRU) du menu de l' [application](windowsribbon-controls-applicationmenu.md). Les informations de chaque élément MRU sont encapsulées dans un objet [**IUISimplePropertySet**](/windows/desktop/api/uiribbon/nn-uiribbon-iuisimplepropertyset) et incluent les trois clés de propriété suivantes :

-   [\_Étiquette de nom de l’interface utilisateur \_](windowsribbon-reference-properties-uipkey-label.md)
-   [IU \_ \_ LabelDescription](windowsribbon-reference-properties-uipkey-labeldescription.md)
-   [IU de l’IU \_ \_ épinglé](windowsribbon-reference-properties-uipkey-pinned.md)

La liste des éléments utilisés récemment est transmise à l’application hôte du ruban sous la forme d’un **SAFEARRAY** de pointeurs [**IUISimplePropertySet**](/windows/desktop/api/uiribbon/nn-uiribbon-iuisimplepropertyset) pour les implémentations respectives dans l’application hôte.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Propriétés de l’État](windowsribbon-reference-properties-state.md)
</dt> </dl>

 

 