---
title: UI_PKEY_FontProperties_Family
description: Identifie la propriété de la famille FontProperties de l’interface utilisateur \_ \_ \_ .
ms.assetid: 95064588-9c14-401f-a86e-7b11e86faaf9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0e0574ea4fb104cff29b58c8b1f649bd9287672acef677e3ea4cdc6ad5f91367
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118438658"
---
# <a name="ui_pkey_fontproperties_family"></a>\_Famille de \_ FontProperties de l’interface utilisateur \_

Identifie la propriété de la famille FontProperties de l’interface utilisateur \_ \_ \_ .

```
propertyDescription
   name = UI_PKEY_FontProperties_Family
   shellPKey = UI_PKEY_FontProperties_Family
   formatID = 00000301-7363-696e-8441798acf5aebb7
   propID = 301
   typeInfo
      type = VT_LPWSTR
```

## <a name="remarks"></a>Remarques

L’interface utilisateur \_ \_ FontProperties \_ Family est utilisée par une application pour interroger la valeur de la Galerie de listes déroulantes de la **famille de polices** .

la valeur de la famille FontProperties de l’interface utilisateur est \_ \_ identique à celle d' \_ un Windows nom des [familles de polices GDI](../gdi/font-families.md) récupéré avec la [fonction EnumFontFamilies](/windows/win32/api/wingdi/nf-wingdi-enumfontfamiliesa) ou la [fonction EnumFontFamiliesEx](/windows/win32/api/wingdi/nf-wingdi-enumfontfamiliesexa).

La valeur par défaut est une chaîne vide.

Si une chaîne vide est fournie pour la valeur de la famille FontProperties de l’interface utilisateur \_ \_ \_ , la sélection de la police est désactivée.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Propriétés du contrôle de police](windowsribbon-reference-properties-fontcontrol.md)
</dt> <dt>

[Contrôle de police](windowsribbon-controls-fontcontrol.md)
</dt> </dl>

 

 