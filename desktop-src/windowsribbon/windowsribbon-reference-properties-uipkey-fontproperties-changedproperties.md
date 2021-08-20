---
title: UI_PKEY_FontProperties_ChangedProperties
description: Identifie la \_ \_ propriété FontProperties ChangedProperties de l’interface utilisateur \_ .
ms.assetid: d96b89b5-af30-4e76-b6ec-03fbb8d28ab3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2a36262a9acf217e448956f108b68cb0716b5b5080c71f6a2a8e305c9e59478c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119028657"
---
# <a name="ui_pkey_fontproperties_changedproperties"></a>IU \_ \_ FontProperties \_ ChangedProperties

Identifie la \_ \_ propriété FontProperties ChangedProperties de l’interface utilisateur \_ .

```
propertyDescription
   name = UI_PKEY_FontProperties_ChangedProperties
   shellPKey = UI_PKEY_FontProperties_ChangedProperties
   formatID = 00000312-7363-696e-8441798acf5aebb7
   propID = 13
   typeInfo
      type = IUISimplePropertySet
```

## <a name="remarks"></a>Remarques

L’interface utilisateur \_ \_ FontProperties \_ ChangedProperties est utilisée par une application pour interroger uniquement les propriétés modifiées à partir de [l’IU \_ \_ FontProperties](windowsribbon-reference-properties-uipkey-fontproperties.md).

L’appel de la méthode [**IUISimplePropertySet :: GetValue**](/windows/desktop/api/uiribbon/nf-uiribbon-iuisimplepropertyset-getvalue) sur cet objet [**IUISimplePropertySet**](/windows/desktop/api/uiribbon/nn-uiribbon-iuisimplepropertyset) retourne un [IPropertyStore](/windows/win32/api/propsys/nn-propsys-ipropertystore).

L’interface utilisateur \_ \_ FontProperties \_ ChangedProperties est passée en tant que dernier paramètre de l’appel [**IUICommandHandler :: Execute**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-execute) à l’application hôte du ruban.

Cette clé de propriété est en lecture seule.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Propriétés du contrôle de police](windowsribbon-reference-properties-fontcontrol.md)
</dt> <dt>

[**IUISimplePropertySet**](/windows/desktop/api/uiribbon/nn-uiribbon-iuisimplepropertyset)
</dt> <dt>

[Contrôle de police](windowsribbon-controls-fontcontrol.md)
</dt> </dl>

 

 