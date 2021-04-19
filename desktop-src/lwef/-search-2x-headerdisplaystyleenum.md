---
title: Énumération HeaderDisplayStyle
description: Utilisé par IResultsViewer HeaderStyle pour définir ou retourner le style d’en-tête actuel.
ms.assetid: 13ae6317-d990-4ccf-83b3-275caf953611
keywords:
- HeaderDisplayStyle, énumération des fonctionnalités d’environnement Windows héritées
topic_type:
- apiref
api_name:
- HeaderDisplayStyle
api_location:
- WdsView.idl
api_type:
- IDLDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bc65b17fa61b799fc9ab8ea7cc1b01380a5843c7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106537091"
---
# <a name="headerdisplaystyle-enumeration"></a>Énumération HeaderDisplayStyle

> [!NOTE]
> Windows Desktop Search 2. x est une technologie obsolète qui était à l’origine disponible en tant que complément pour Windows XP et Windows Server 2003. Dans les versions ultérieures, utilisez plutôt l' [API Windows Search](../search/-search-reference-entry-page.md) . 

Utilisé par [**IResultsViewer :: HeaderStyle**](-search-2x-iresultsviewer-headerstyle.md) pour définir ou retourner le style d’en-tête actuel.

## <a name="syntax"></a>Syntaxe


```C++
typedef enum HeaderDisplayStyleEnum { 
  FullHeader     = 0,
  CompactHeader  = 1,
  NoHeader       = 2
} HeaderDisplayStyle;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="FullHeader"></span><span id="fullheader"></span><span id="FULLHEADER"></span>**FullHeader**
</dt> <dd>

Indique ou définit l’utilisation des en-têtes complets.

</dd> <dt>

<span id="CompactHeader"></span><span id="compactheader"></span><span id="COMPACTHEADER"></span>**CompactHeader**
</dt> <dd>

Indique ou définit l’utilisation des en-têtes compacts.

</dd> <dt>

<span id="NoHeader"></span><span id="noheader"></span><span id="NOHEADER"></span>**Noen-tête**
</dt> <dd>

Indique ou définit l’utilisation d’aucun en-tête.

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|----------------|----------------------------------------------------------------------------------------|
| MIDL<br/> | <dl> <dt>WdsView. idl</dt> </dl> |



 

 





