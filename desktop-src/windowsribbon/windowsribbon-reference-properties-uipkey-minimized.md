---
title: UI_PKEY_Minimized
description: Identifie la \_ \_ propriété minimisée de l’interface utilisateur.
ms.assetid: 52f3558b-f8a0-45d7-9eb4-b63993ae8cac
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 68f820203bfc405259811e212e53460afabb9f300279c4e20d10c9b593a030b8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118706172"
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

## <a name="remarks"></a>Remarques

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

 

 




