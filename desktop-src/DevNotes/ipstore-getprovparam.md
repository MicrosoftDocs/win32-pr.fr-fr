---
description: Destiné à définir les informations de paramètre spécifiées.
ms.assetid: e1a5766f-a303-47f1-a4bb-33f4253a5464
title: 'IPStore :: GetProvParam, méthode (PStore. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPStore.GetProvParam
api_type:
- COM
api_location:
- Pstorec.dll
ms.openlocfilehash: de18c4452456ed98f7e5214a33445a0780189f7864d96cfb05e08123a3b42cc0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118955908"
---
# <a name="ipstoregetprovparam-method"></a>IPStore :: GetProvParam, méthode

\[le Stockage protégé (Pstore) peut être utilisé dans Windows Server 2003 et Windows XP. elle est uniquement disponible pour les opérations en lecture seule dans Windows Server 2008 et Windows Vista, mais elle peut ne pas être disponible dans les versions ultérieures. Pstore utilise une implémentation plus ancienne de la protection des données. Les développeurs sont vivement encouragés à tirer parti de la protection renforcée des données fournie par les fonctions [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) et [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) .\]

\[Cette méthode n’est pas implémentée.\]

Destiné à définir les informations de paramètre spécifiées. Notez, toutefois, qu’elle n’est pas implémentée et échouera toujours.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetProvParam(
  [in]  DWORD dwParam,
  [out] DWORD *pcbData,
  [out] BYTE  **ppbData,
  [in]  DWORD dwFlags
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*dwParam* \[ dans\]
</dt> <dd>

Réservé.

</dd> <dt>

*pcbData* \[ à\]
</dt> <dd>

Réservé.

</dd> <dt>

*ppbData* \[ à\]
</dt> <dd>

Réservé.

</dd> <dt>

*dwFlags* \[ dans\]
</dt> <dd>

Réservé.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Les appels à cette méthode échouent toujours.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|----------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>Pstore. h</dt> </dl>    |
| DLL<br/>    | <dl> <dt>Pstorec.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IPStore**](ipstore.md)
</dt> </dl>

 

 
