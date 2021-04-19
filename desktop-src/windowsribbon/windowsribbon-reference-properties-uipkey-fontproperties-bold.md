---
title: UI_PKEY_FontProperties_Bold
description: Identifie la \_ \_ propriété FontProperties gras de l’interface utilisateur \_ .
ms.assetid: 9d33142a-bd63-423e-ba77-083c86bce1e7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7dca8a58b9c5bfa51cfba8d80a477dafb744dfb8
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "106510696"
---
# <a name="ui_pkey_fontproperties_bold"></a>IU \_ \_ FontProperties \_ gras

Identifie la \_ \_ propriété FontProperties gras de l’interface utilisateur \_ .

```
propertyDescription
   name = UI_PKEY_FontProperties_Bold
   shellPKey = UI_PKEY_FontProperties_Bold
   formatID = 00000303-7363-696e-8441798acf5aebb7
   propID = 303
   typeInfo
      type = UI_FONTPROPERTIES
```

## <a name="remarks"></a>Notes

IU \_ \_ FontProperties \_ gras est utilisé par une application pour interroger l’état du bouton **gras** .

La valeur de la propriété provient de l’énumération [**\_ FONTPROPERTIES de l’interface utilisateur**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_fontproperties) .

La valeur par défaut est `UI_FONTPROPERTIES_NOTSET`.

Le tableau suivant décrit les propriétés et le résultat de l’interface utilisateur.



|                                  |                                                                     |
|----------------------------------|---------------------------------------------------------------------|
| `UI_FONTPROPERTIES_NOTAVAILABLE` | Le bouton **gras** est désactivé et ne peut être défini que par l’application. |
| `UI_FONTPROPERTIES_NOTSET`       | Le bouton **gras** n’est pas sélectionné.                                    |
| `UI_FONTPROPERTIES_SET`          | Le bouton **gras** est sélectionné.                                        |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Propriétés du contrôle de police](windowsribbon-reference-properties-fontcontrol.md)
</dt> <dt>

[**interface utilisateur \_ FONTPROPERTIES**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_fontproperties)
</dt> <dt>

[Contrôle de police](windowsribbon-controls-fontcontrol.md)
</dt> </dl>

 

 