---
title: UI_PKEY_QuickAccessToolbarDock
description: Identifie la propriété QuickAccessToolbarDock de l’interface utilisateur \_ \_ .
ms.assetid: 77f7b0a8-f276-4501-9d53-fb5a3185edcc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2b9011cceb9b2ec96680ea3badd0ad40ae6121c14a70e065cfbfff5f5fe8e1f9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118201375"
---
# <a name="ui_pkey_quickaccesstoolbardock"></a>IU \_ \_ QuickAccessToolbarDock

Identifie la propriété QuickAccessToolbarDock de l’interface utilisateur \_ \_ .

```
propertyDescription
   name = UI_PKEY_QuickAccessToolbarDock
   shellPKey = UI_PKEY_QuickAccessToolbarDock
   formatID = 00001002-7363-696e-8441798acf5aebb7
   propID = 1002
   typeInfo
      type = UI_CONTROLDOCK
```

## <a name="remarks"></a>Remarques

L’interface utilisateur \_ \_ QuickAccessToolbarDock est utilisée par une application pour interroger l’état d’ancrage de la barre d’outils accès rapide (qat).

La valeur de la propriété provient de l’énumération [**\_ CONTROLDOCK de l’interface utilisateur**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_controldock) .



|    Énumération                     |    Description                                                                                                                                                                                                                                                   |
|-------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| CONTROLDOCK de l’interface utilisateur \_ \_ haut    | Le QAT est ancré dans la zone non cliente de l’application hôte du ruban, comme illustré dans la capture d’écran suivante.![capture d’écran de la barre d’outils accès rapide ancrée au-dessus du ruban dans la zone non cliente.](images/properties/qat-docktop.png)<br/> |
| \_CONTROLDOCK \_ bas de l’interface utilisateur | Le QAT est ancré sous la forme d’une bande intégrale visuelle sous le ruban, comme illustré dans la capture d’écran suivante. ![capture d’écran de la barre d’outils accès rapide ancrée sous le ruban.](images/properties/qat-dockbottom.png)<br/>                           |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Propriétés du ruban](windowsribbon-reference-properties-ribbon.md)
</dt> </dl>

 

