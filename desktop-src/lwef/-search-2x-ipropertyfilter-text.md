---
title: Propriété Text IPropertyFilter (WdsSharedIDL. h)
description: Texte du filtre.
ms.assetid: 1e0bf432-6d6b-4c29-bb2f-64fb91f5faaf
keywords:
- Propriétés de texte héritées fonctionnalités de l’environnement Windows
- Propriétés de texte héritées fonctionnalités de l’environnement Windows, interface IPropertyFilter
- Interface IPropertyFilter fonctionnalités de l’environnement Windows héritées, propriété Text
topic_type:
- apiref
api_name:
- IPropertyFilter.Text
- IPropertyFilter.get_Text
- IPropertyFilter.put_Text
api_location:
- WdsSharedIDL.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2b30614f63cbcd766ca843f1b793632502f8e114
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104508933"
---
# <a name="ipropertyfiltertext-property"></a>IPropertyFilter :: Text, propriété

> [!NOTE]
> Windows Desktop Search 2. x est une technologie obsolète qui était à l’origine disponible en tant que complément pour Windows XP et Windows Server 2003. Dans les versions ultérieures, utilisez plutôt l' [API Windows Search](../search/-search-reference-entry-page.md) . 

Texte du filtre.

Cette propriété est en lecture/écriture.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT put_Text(
  [in]          BSTR text
);

HRESULT get_Text(
  [out, retval] BSTR *text
);
```



## <a name="property-value"></a>Valeur de la propriété

Définit le texte du filtre.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows XP avec les \[ applications de bureau SP2 uniquement\]<br/>                                      |
| Serveur minimal pris en charge<br/> | Windows Server 2003 avec les \[ applications de bureau SP1 uniquement\]<br/>                             |
| Composant redistribuable<br/>          | Windows Desktop Search (WDS) 2.6.5<br/>                                             |
| En-tête<br/>                   | <dl> <dt>WdsSharedIDL. h</dt> </dl> |



 

 





