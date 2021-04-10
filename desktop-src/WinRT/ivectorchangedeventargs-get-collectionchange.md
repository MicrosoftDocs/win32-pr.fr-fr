---
description: Obtient le type de modification qui s’est produite dans le vecteur.
ms.assetid: 213f4794-b972-44e3-a400-8a24b1583ddd
title: 'IVectorChangedEventArgs :: get_CollectionChange, méthode (IVectorChangedEventArgs. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IVectorChangedEventArgs.get_CollectionChange
api_type:
- COM
api_location:
- IVectorChangedEventArgs.h
ms.openlocfilehash: a843574bcaf93ec524173ba76800cc15012c89fd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104201442"
---
# <a name="ivectorchangedeventargsget_collectionchange-method"></a>IVectorChangedEventArgs :: obten, \_ méthode CollectionChange

Obtient le type de modification qui s’est produite dans le vecteur.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT get_CollectionChange(
  [out, retval] CollectionChange *value
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*valeur* \[ out, retval\]
</dt> <dd>

Type : **CollectionChange \** _

Valeur de l’énumération [_ *CollectionChange* *](/uwp/api/Windows.Foundation.Collections.CollectionChange?view=winrt-19041) qui décrit la modification.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **HRESULT**

Si cette méthode est réussie, elle retourne la valeur **\_ OK**. Sinon, elle retourne un code d’erreur **HRESULT** .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 8<br/>                                                                                 |
| Serveur minimal pris en charge<br/> | Windows Server 2012<br/>                                                                       |
| En-tête<br/>                   | <dl> <dt>IVectorChangedEventArgs. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IVectorChangedEventArgs**](ivectorchangedeventargs.md)
</dt> </dl>

 

 
