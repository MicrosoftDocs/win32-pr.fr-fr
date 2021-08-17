---
description: Récupère le PROPVARIANT et la chaîne d’entrée qui représente un segment de données. L’appel de cette méthode est identique à l’appel de GetData.
ms.assetid: 78846D1D-923F-4FEA-8BF2-B16BB1B21BB3
title: 'IRichChunk :: RemoteGetData, méthode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IRichChunk.RemoteGetData
api_type:
- COM
api_location: ''
ms.openlocfilehash: caaa4ab9688ab8169bd0955c8abb1e976e7eb318e94875be1486e61b32e13207
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117862793"
---
# <a name="irichchunkremotegetdata-method"></a>IRichChunk :: RemoteGetData, méthode

Récupère le [PROPVARIANT](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) et la chaîne d’entrée qui représente un segment de données. L’appel de cette méthode est identique à l’appel de [**GetData**](/windows/desktop/api/StructuredQueryCondition/nf-structuredquerycondition-irichchunk-getdata).

## <a name="syntax"></a>Syntaxe


```C++
HRESULT RemoteGetData(
  [out] ULONG       *pFirstPos,
  [out] ULONG       *pLength,
  [out] LPWSTR      *ppsz,
  [out] PROPVARIANT *pValue
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pFirstPos* \[ à\]
</dt> <dd>

Reçoit la position de départ de base zéro de la plage. Ce paramètre peut être **NULL**.

</dd> <dt>

*PLength* \[ à\]
</dt> <dd>

Reçoit la longueur de la plage. Ce paramètre peut être **NULL**.

</dd> <dt>

*ppsz* \[ à\]
</dt> <dd>

Reçoit la valeur de chaîne Unicode associée, ou **null** si elle n’est pas disponible.

</dd> <dt>

*pValue* \[ à\]
</dt> <dd>

Reçoit la valeur [PROPVARIANT](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) associée, ou **VT \_ vide** s’il n’est pas disponible. Ce paramètre peut être **NULL**.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si cette méthode est réussie, elle retourne la valeur **\_ OK**. Sinon, elle retourne un code d’erreur **HRESULT** .

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IRichChunk**](/windows/desktop/api/Structuredquerycondition/nn-structuredquerycondition-irichchunk)
</dt> </dl>

 

 
