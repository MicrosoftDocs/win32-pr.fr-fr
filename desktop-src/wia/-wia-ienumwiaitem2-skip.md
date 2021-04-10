---
description: Ignore le nombre spécifié d’éléments au cours d’une énumération des objets IWiaItem2 disponibles.
ms.assetid: 7a5e9e1c-1e6e-4de0-9499-bf89e35c19aa
title: 'IEnumWiaItem2 :: Skip, méthode (WIA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEnumWiaItem2.Skip
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: 7618aad923136a9a32d8b7fb935050fefe07bff1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103951340"
---
# <a name="ienumwiaitem2skip-method"></a>IEnumWiaItem2 :: Skip, méthode

Ignore le nombre spécifié d’éléments au cours d’une énumération des objets [**IWiaItem2**](-wia-iwiaitem2.md) disponibles.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT Skip(
  [in] ULONG cElt
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*cElt* \[ dans\]
</dt> <dd>

Type : **ULong**

Spécifie le nombre d’éléments à ignorer.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **HRESULT**

Si cette méthode est réussie, elle retourne la valeur **\_ OK**. Sinon, elle retourne un code d’erreur **HRESULT** .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                     |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/>                               |
| En-tête<br/>                   | <dl> <dt>WIA. h</dt> </dl>   |
| MIDL<br/>                      | <dl> <dt>WIA. idl</dt> </dl> |



 

 




