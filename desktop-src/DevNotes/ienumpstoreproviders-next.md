---
description: Obtient le nombre spécifié de fournisseurs suivant dans la séquence d’énumération.
ms.assetid: 9ef8d330-6f78-4063-825c-9cf5b4f283cf
title: 'IEnumPStoreProviders :: Next, méthode (PStore. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEnumPStoreProviders.Next
api_type:
- COM
api_location:
- Pstorec.dll
ms.openlocfilehash: ad35f76622abd61c6830f338a670c42a2c2f9178d0d6692044eec62621617976
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119691289"
---
# <a name="ienumpstoreprovidersnext-method"></a>IEnumPStoreProviders :: Next, méthode

\[le Stockage protégé (Pstore) peut être utilisé dans Windows Server 2003 et Windows XP. elle est uniquement disponible pour les opérations en lecture seule dans Windows Server 2008 et Windows Vista, mais elle peut ne pas être disponible dans les versions ultérieures. Pstore utilise une implémentation plus ancienne de la protection des données. Les développeurs sont vivement encouragés à tirer parti de la protection renforcée des données fournie par les fonctions [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) et [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) .\]

Obtient le nombre spécifié de fournisseurs suivant dans la séquence d’énumération.

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

[**IEnumPStoreProviders**](ienumpstoreproviders.md)
</dt> </dl>

 

 
