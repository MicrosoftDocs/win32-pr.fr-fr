---
title: Énumération PreviewDisplayStyle
description: Utilisé par IResultsViewer PreviewStyle pour définir ou déterminer le style d’affichage en cours d’utilisation.
ms.assetid: ccbbfe38-0719-41e0-9331-cc0c1be651eb
keywords:
- PreviewDisplayStyle, énumération des fonctionnalités d’environnement Windows héritées
topic_type:
- apiref
api_name:
- PreviewDisplayStyle
api_location:
- WdsView.idl
api_type:
- IDLDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 11902821ec9fdbbaa9ab8d3fda8971f42fc28c1f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106541503"
---
# <a name="previewdisplaystyle-enumeration"></a>Énumération PreviewDisplayStyle

> [!NOTE]
> Windows Desktop Search 2. x est une technologie obsolète qui était à l’origine disponible en tant que complément pour Windows XP et Windows Server 2003. Dans les versions ultérieures, utilisez plutôt l' [API Windows Search](../search/-search-reference-entry-page.md) . 

Utilisé par [**IResultsViewer ::P reviewstyle**](-search-2x-iresultsviewer-previewstyle.md) pour définir ou déterminer le style d’affichage en cours d’utilisation.

## <a name="syntax"></a>Syntaxe


```C++
typedef enum PreviewDisplayStyleEnum { 
  AutoPreview    = 0,
  RightPreview   = 1,
  BottomPreview  = 2,
  NoPreview      = 3
} PreviewDisplayStyle;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="AutoPreview"></span><span id="autopreview"></span><span id="AUTOPREVIEW"></span>**Aperçu partiel**
</dt> <dd>

Indique l’aperçu partiel.

</dd> <dt>

<span id="RightPreview"></span><span id="rightpreview"></span><span id="RIGHTPREVIEW"></span>**RightPreview**
</dt> <dd>

Indique RightPreview.

</dd> <dt>

<span id="BottomPreview"></span><span id="bottompreview"></span><span id="BOTTOMPREVIEW"></span>**BottomPreview**
</dt> <dd>

Indique BottomPreview.

</dd> <dt>

<span id="NoPreview"></span><span id="nopreview"></span><span id="NOPREVIEW"></span>**Nopreview**
</dt> <dd>

Indique nopreview.

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|----------------|----------------------------------------------------------------------------------------|
| MIDL<br/> | <dl> <dt>WdsView. idl</dt> </dl> |



 

 





