---
description: Récupère une valeur qui indique si le ConfirmationType passé à cette méthode a été défini sur ce IContextNode.
ms.assetid: 4a96bc46-b627-4784-ad1d-1079f49592e5
title: 'IContextNode :: IsConfirmed, méthode (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNode.IsConfirmed
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 2e378aaf344e177514115c82b1179f8d1ebe25faefa0d5d840d5a0af62ff1c07
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118967358"
---
# <a name="icontextnodeisconfirmed-method"></a>IContextNode :: IsConfirmed, méthode

Récupère une valeur qui indique si le ConfirmationType passé à cette méthode a été défini sur ce IContextNode.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT IsConfirmed(
  [in]  ConfirmationType confirmedType,
  [out] VARIANT_BOOL     *pfTypeConfirmed
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*confirmedType* \[ dans\]
</dt> <dd>

Type de confirmation pour lequel le test est effectué.

</dd> <dt>

*pfTypeConfirmed* \[ à\]
</dt> <dd>

**Variante \_ TRUE** si le type passé dans confirmedType a été défini sur cet objet [**IContextNode**](icontextnode.md) ; Sinon, **Variant \_ false**.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Pour obtenir une description des valeurs de retour, consultez [classes et interfaces-analyse](classes-and-interfaces---ink-analysis.md)de l’encre.

## <a name="remarks"></a>Remarques

Cette valeur est définie par la méthode [**IContextNode :: Confirm**](icontextnode-confirm.md) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Applications de bureau XP Édition Tablet PC \[ uniquement\]<br/>                                                 |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                                                                                     |
| En-tête<br/>                   | <dl> <dt>IACom. h (nécessite également IACom \_ i. c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IContextNode**](icontextnode.md)
</dt> <dt>

[**IContextNode :: Confirm**](icontextnode-confirm.md)
</dt> <dt>

[Référence de l’analyse de l’encre](ink-analysis-reference.md)
</dt> </dl>

 

 




