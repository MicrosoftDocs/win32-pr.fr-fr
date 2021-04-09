---
description: Obtient la position dans le vecteur où la modification s’est produite.
ms.assetid: 00756d77-aae0-45f0-8bd4-cf68af9bdc7c
title: 'IVectorChangedEventArgs :: get_Index, méthode (IVectorChangedEventArgs. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IVectorChangedEventArgs.get_Index
api_type:
- COM
api_location:
- IVectorChangedEventArgs.h
ms.openlocfilehash: 5c131567ec7fc2861ce11db9e5d7ec581f6f663a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104033988"
---
# <a name="ivectorchangedeventargsget_index-method"></a>IVectorChangedEventArgs :: obtient l' \_ index, méthode

Obtient la position dans le vecteur où la modification s’est produite.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT get_Index(
  [out, retval] unsigned *value
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*valeur* \[ out, retval\]
</dt> <dd>

Tapez : **unsigned \** _

Position de base zéro dans le vecteur où la modification s’est produite, le cas échéant.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : _ *HRESULT**

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

 

 




