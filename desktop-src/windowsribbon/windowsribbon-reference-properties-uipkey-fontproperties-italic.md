---
title: UI_PKEY_FontProperties_Italic
description: Identifie la \_ \_ propriété FontProperties italique de l’interface utilisateur \_ .
ms.assetid: 53edd88e-ed7e-4385-9fd9-bfa90be348cd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8d0dfa07b5112e91d8c25a4ff8c4f31175adf9b7
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/04/2021
ms.locfileid: "111443810"
---
# <a name="ui_pkey_fontproperties_italic"></a>IU \_ \_ FontProperties \_ italique

Identifie la \_ \_ propriété FontProperties italique de l’interface utilisateur \_ .

```
propertyDescription
   name = UI_PKEY_FontProperties_Italic
   shellPKey = UI_PKEY_FontProperties_Italic
   formatID = 00000304-7363-696e-8441798acf5aebb7
   propID = 304
   typeInfo
      type = UI_FONTPROPERTIES
```

## <a name="remarks"></a>Remarques

IU \_ \_ FontProperties \_ italique est utilisé par une application pour interroger l’état du bouton **italique** .

La valeur de la propriété provient de l’énumération [**\_ FONTPROPERTIES de l’interface utilisateur**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_fontproperties) .

La valeur par défaut est `UI_FONTPROPERTIES_NOTSET`.

Le tableau suivant décrit les propriétés et le résultat de l’interface utilisateur.



|    Propriété                      |       Résultat de l’interface utilisateur                                                       |
|----------------------------------|-----------------------------------------------------------------------|
| `UI_FONTPROPERTIES_NOTAVAILABLE` | Le bouton **italique** est désactivé et ne peut être défini que par l’application. |
| `UI_FONTPROPERTIES_NOTSET`       | Le bouton **italique** n’est pas sélectionné.                                    |
| `UI_FONTPROPERTIES_SET`          | Le bouton **italique** est sélectionné.                                        |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Propriétés du contrôle de police](windowsribbon-reference-properties-fontcontrol.md)
</dt> <dt>

[**interface utilisateur \_ FONTPROPERTIES**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_fontproperties)
</dt> <dt>

[Contrôle de police](windowsribbon-controls-fontcontrol.md)
</dt> </dl>

 

 