---
title: UI_PKEY_Minimized
description: Identifie la \_ \_ propriété minimisée de l’interface utilisateur.
ms.assetid: 52f3558b-f8a0-45d7-9eb4-b63993ae8cac
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a8e2eb286727c9810196a31f0df79f98f4f3d2a0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104029373"
---
# <a name="ui_pkey_minimized"></a>IU-au-dessus \_ \_ minimisé

Identifie la \_ \_ propriété minimisée de l’interface utilisateur.

```
propertyDescription
   name = UI_PKEY_Minimized
   shellPKey = UI_PKEY_Minimized
   formatID = 00001001-7363-696e-8441798acf5aebb7
   propID = 1001
   typeInfo
      type = VT_BOOL
   booleanFormat
      formatAs = VARIANT_TRUE=-1, VARIANT_FALSE=0
```

## <a name="remarks"></a>Notes

L’interface utilisateur au-dessus \_ \_ réduite est utilisée par une application pour interroger l’État réduit ou développé de l’interface ruban.



| État d’affichage | Valeur de la clé de propriété |
|---------------|--------------------|
| Développé      | **false**          |
| Collapsed     | **true**           |



 

Lorsque l’interface utilisateur du ruban est dans un État réduit, la ligne de l’onglet du ruban reste visible et entièrement fonctionnelle.

La capture d’écran suivante montre le ruban dans un État réduit.

![capture d’écran montrant l’interface utilisateur du ruban réduite.](images/overviews/ribbon-minimized.png)

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Propriétés du ruban](windowsribbon-reference-properties-ribbon.md)
</dt> <dt>

[Affichage du ruban](ribbon-visibility.md)
</dt> </dl>

 

 




