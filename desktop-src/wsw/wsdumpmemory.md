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
ms.openlocfilehash: b92941603b78c25db06415fec42524d978a90953d0c15eaea191a8874e6b34fb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119770889"
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
| Client minimal pris en charge<br/> | applications de \[ bureau Windows 7 \| applications UWP\]<br/>                                             |
| Serveur minimal pris en charge<br/> | Windows Applications du serveur 2008 R2 \[ Desktop Apps \| UWP\]<br/>                                |
| En-tête<br/>                   | <dl> <dt>WebServicesDebug. h</dt> </dl> |



 

 





