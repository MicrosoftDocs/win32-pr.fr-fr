---
title: Propriété HelpText IResultVerb (WdsSharedIDL. h)
description: Cette propriété retourne un pointeur vers la chaîne d’aide localisée pour le verbe.
ms.assetid: 14e91101-5ee2-459a-97d7-35c76d3ba990
keywords:
- Propriété HelpText fonctionnalités d’environnement Windows héritées
- Propriété HelpText fonctionnalités d’environnement Windows héritées, interface IResultVerb
- Interface IResultVerb fonctionnalités de l’environnement Windows héritées, propriété HelpText
topic_type:
- apiref
api_name:
- IResultVerb.HelpText
- IResultVerb.get_HelpText
api_location:
- WdsSharedIDL.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3a0615ea9cc62f3a5f207e7be2c2c4e80987239c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741036"
---
# <a name="iresultverbhelptext-property"></a>IResultVerb :: HelpText, propriété

> [!NOTE]
> Windows Desktop Search 2. x est une technologie obsolète qui était à l’origine disponible en tant que complément pour Windows XP et Windows Server 2003. Dans les versions ultérieures, utilisez plutôt l' [API Windows Search](../search/-search-reference-entry-page.md) . 

Cette propriété retourne un pointeur vers la chaîne d’aide localisée pour le verbe.

Cette propriété est en lecture seule.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT get_HelpText(
  [out, retval] BSTR *text
);
```



## <a name="property-value"></a>Valeur de la propriété

La valeur de cette propriété est un pointeur vers la chaîne d’aide localisée pour ce verbe.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows XP avec les \[ applications de bureau SP2 uniquement\]<br/>                                      |
| Serveur minimal pris en charge<br/> | Windows Server 2003 avec les \[ applications de bureau SP1 uniquement\]<br/>                             |
| Composant redistribuable<br/>          | Windows Desktop Search (WDS) 2.6.5<br/>                                             |
| En-tête<br/>                   | <dl> <dt>WdsSharedIDL. h</dt> </dl> |



 

 





