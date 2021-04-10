---
description: Réinitialise la référence d’énumération au premier objet IWiaItem2.
ms.assetid: 392e3471-f7fc-456f-a1cc-ab4eb6d3fe18
title: 'IEnumWiaItem2 :: Reset, méthode (WIA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEnumWiaItem2.Reset
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: ab4d5a9effbcb003265da53ddc753f63630df51a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104201672"
---
# <a name="ienumwiaitem2reset-method"></a>IEnumWiaItem2 :: Reset, méthode

Réinitialise la référence d’énumération au premier objet [**IWiaItem2**](-wia-iwiaitem2.md) .

## <a name="syntax"></a>Syntaxe


```C++
HRESULT Reset();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

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



 

 




