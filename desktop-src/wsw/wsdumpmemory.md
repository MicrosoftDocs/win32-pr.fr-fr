---
title: WsDumpMemory, fonction (WebServicesDebug. h)
description: Cette fonction vide toutes les allocations de mémoire dans la console.
ms.assetid: 84a4f1e7-7d62-48c2-a8a3-ee4573bde5e4
keywords:
- Services Web de fonction WsDumpMemory pour Windows
topic_type:
- apiref
api_name:
- WsDumpMemory
api_location:
- WebServicesDebug.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 70af8d34b3ee04a9db4128ce1063bd31e81306eb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942602"
---
# <a name="wsdumpmemory-function"></a>WsDumpMemory fonction)

Cette fonction vide toutes les allocations de mémoire dans la console.

> [!Note]  
> Cette fonction est destinée uniquement au débogage.

 

## <a name="syntax"></a>Syntaxe


```C++
HRESULT WINAPI  WsDumpMemory(
  _In_opt_ WS_ERROR* error
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*erreur* \[ dans, facultatif\]
</dt> <dd>

Pointeur vers un objet [d' \_ erreur WS](ws-error.md) où des informations supplémentaires sur l’erreur doivent être stockées si la fonction échoue.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si cette fonction est correctement exécutée, elle retourne la valeur **\_ OK**. Sinon, elle retourne un code d’erreur **HRESULT** .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications Windows 7 \[ Desktop Apps \| UWP\]<br/>                                             |
| Serveur minimal pris en charge<br/> | Applications Windows Server 2008 R2 \[ Desktop Apps \| UWP\]<br/>                                |
| En-tête<br/>                   | <dl> <dt>WebServicesDebug. h</dt> </dl> |



 

 





