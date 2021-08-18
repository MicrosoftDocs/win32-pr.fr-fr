---
description: Obtient le nombre spécifié de types de fournisseurs suivant dans la séquence d’énumération.
ms.assetid: 9a1d0db0-1e9b-48f8-b373-2a82a48e4f63
title: 'IEnumPStoreTypes :: Next, méthode (PStore. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEnumPStoreTypes.Next
api_type:
- COM
api_location:
- Pstorec.dll
ms.openlocfilehash: 72086d7f56c673af693e34bcb8a658bb02ea5c60976aaf813bb350e3335c403e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120002139"
---
# <a name="ienumpstoretypesnext-method"></a>IEnumPStoreTypes :: Next, méthode

\[le Stockage protégé (Pstore) peut être utilisé dans Windows Server 2003 et Windows XP. elle est uniquement disponible pour les opérations en lecture seule dans Windows Server 2008 et Windows Vista, mais elle peut ne pas être disponible dans les versions ultérieures. Pstore utilise une implémentation plus ancienne de la protection des données. Les développeurs sont vivement encouragés à tirer parti de la protection renforcée des données fournie par les fonctions [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) et [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) .\]

Obtient le nombre spécifié de types de fournisseurs suivant dans la séquence d’énumération.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT Next(
  [in]      DWORD  celt,
  [out]     LPWSTR *rgelt,
  [in, out] DWORD  *pceltFetched
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*celt* \[ dans\]
</dt> <dd>

Nombre de types de fournisseurs demandés.

</dd> <dt>

*rgelt* \[ à\]
</dt> <dd>

Pointeur vers une chaîne dans laquelle retourner le nom du type de fournisseur.

</dd> <dt>

*pceltFetched* \[ in, out\]
</dt> <dd>

Pointeur vers le nombre de types de fournisseurs réellement fournis.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

La valeur de retour est une valeur **HRESULT** .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|----------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>Pstore. h</dt> </dl>    |
| DLL<br/>    | <dl> <dt>Pstorec.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IEnumPStoreTypes**](ienumpstoretypes.md)
</dt> </dl>

 

 
