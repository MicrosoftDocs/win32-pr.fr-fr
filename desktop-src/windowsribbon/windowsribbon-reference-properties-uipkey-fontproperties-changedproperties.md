---
title: UI_PKEY_FontProperties_ChangedProperties
description: Identifie la \_ \_ propriété FontProperties ChangedProperties de l’interface utilisateur \_ .
ms.assetid: d96b89b5-af30-4e76-b6ec-03fbb8d28ab3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 124b36d5e24f4e0c0122cffdbbed11669a4ea510
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104382408"
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

## <a name="remarks"></a>Notes

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

 

 