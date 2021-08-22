---
description: Obtient le nombre d’objets IContextLink dans cette collection.
ms.assetid: c3becacd-2df0-401c-88c8-5fad3e9f8c02
title: 'IContextLinks :: GetCount, méthode (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextLinks.GetCount
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: c622e3b222aacb2b05b56a4fbe933d0578ee6649b3a5f5d84a3c5d9b6382c629
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119092280"
---
# <a name="icontextlinksgetcount-method"></a>IContextLinks :: GetCount, méthode

Obtient le nombre d’objets [**IContextLink**](icontextlink.md) dans cette collection.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetCount(
  [out, retval] ULONG *pulCount
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pulCount* \[ out, retval\]
</dt> <dd>

Nombre d’objets [**IContextLink**](icontextlink.md) contenus dans cette collection.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Pour obtenir une description des valeurs de retour, consultez [classes et interfaces-analyse](classes-and-interfaces---ink-analysis.md)de l’encre.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Applications de bureau XP Édition Tablet PC \[ uniquement\]<br/>                                                 |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                                                                                     |
| En-tête<br/>                   | <dl> <dt>IACom. h (nécessite également IACom \_ i. c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IContextLinks**](icontextlinks.md)
</dt> <dt>

[Référence de l’analyse de l’encre](ink-analysis-reference.md)
</dt> </dl>

 

 




