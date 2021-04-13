---
title: WsSetAutoFail, fonction (WebServicesDebug. h)
description: Définit le point suivant pour injecter un échec. Il s’agit d’une fonction de débogage uniquement.
ms.assetid: b453dbc5-01ff-486d-8767-254b74cc5b6e
keywords:
- Services Web de fonction WsSetAutoFail pour Windows
topic_type:
- apiref
api_name:
- WsSetAutoFail
api_location:
- WebServicesDebug.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0ba10b8b038f270f764b064fac1cb81e675f5239
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104509082"
---
# <a name="wssetautofail-function"></a>WsSetAutoFail fonction)

Définit le point suivant pour injecter un échec. Il s’agit d’une fonction de débogage uniquement.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT WINAPI  WsSetAutoFail(
  _In_     ULONG     count,
  _In_opt_ WS_ERROR* error
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*nombre* \[ dans\]
</dt> <dd>

Spécifie combien d’opérations avant les échecs commencent à se produire.

</dd> <dt>

*erreur* \[ dans, facultatif\]
</dt> <dd>

Pointeur vers un objet [d' \_ erreur WS](ws-error.md) où des informations supplémentaires sur l’erreur doivent être stockées si la fonction échoue.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si cette fonction est correctement exécutée, elle retourne la valeur **\_ OK**. Sinon, elle retourne un code d’erreur **HRESULT** .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows 7 uniquement\]<br/>                                                    |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 R2 \[ uniquement\]<br/>                                       |
| En-tête<br/>                   | <dl> <dt>WebServicesDebug. h</dt> </dl> |



 

 





