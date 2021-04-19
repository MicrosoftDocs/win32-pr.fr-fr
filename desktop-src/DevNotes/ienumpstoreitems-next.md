---
description: Obtient le nombre spécifié de noms d’éléments de données suivant dans la séquence d’énumération.
ms.assetid: 6f30bf64-bd63-43d7-ab7e-f64e372c723b
title: 'IEnumPStoreItems :: Next, méthode (PStore. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEnumPStoreItems.Next
api_type:
- COM
api_location:
- Pstorec.dll
ms.openlocfilehash: 967f2f84553b87965d5b2c92d99e347cb259264b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106526632"
---
# <a name="ienumpstoreitemsnext-method"></a>IEnumPStoreItems :: Next, méthode

\[Le stockage protégé (PStore) peut être utilisé dans Windows Server 2003 et Windows XP. Elle est uniquement disponible pour les opérations en lecture seule dans Windows Server 2008 et Windows Vista, mais elle peut ne pas être disponible dans les versions ultérieures. Pstore utilise une implémentation plus ancienne de la protection des données. Les développeurs sont vivement encouragés à tirer parti de la protection renforcée des données fournie par les fonctions [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) et [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) .\]

Obtient le nombre spécifié de noms d’éléments de données suivant dans la séquence d’énumération.

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

Nombre d’éléments de données demandés.

</dd> <dt>

*rgelt* \[ à\]
</dt> <dd>

Pointeur vers une chaîne dans laquelle retourner le nom de l’élément de données.

</dd> <dt>

*pceltFetched* \[ in, out\]
</dt> <dd>

Pointeur vers le nombre de noms d’éléments de données réellement fournis.

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

[**IEnumPStoreItems**](ienumpstoreitems.md)
</dt> </dl>

 

 
