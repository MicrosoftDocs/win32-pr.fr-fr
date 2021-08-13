---
description: Retourne des informations sur le fournisseur de stockage.
ms.assetid: bdacb5bb-a37a-4970-add7-57625bec1ce0
title: 'IPStore :: GetInfo, méthode (PStore. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPStore.GetInfo
api_type:
- COM
api_location:
- Pstorec.dll
ms.openlocfilehash: 118f346acf550a8d4835931102a26d70f0c41fad7cc23ac706268b7778c31b56
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118667270"
---
# <a name="ipstoregetinfo-method"></a>IPStore :: GetInfo, méthode

\[le Stockage protégé (Pstore) peut être utilisé dans Windows Server 2003 et Windows XP. elle est uniquement disponible pour les opérations en lecture seule dans Windows Server 2008 et Windows Vista, mais elle peut ne pas être disponible dans les versions ultérieures. Pstore utilise une implémentation plus ancienne de la protection des données. Les développeurs sont vivement encouragés à tirer parti de la protection renforcée des données fournie par les fonctions [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) et [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) .\]

Retourne des informations sur le fournisseur de stockage.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetInfo(
  [out] PPST_PROVIDERINFO *ppProperties
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*ppProperties* \[ à\]
</dt> <dd>

Pointeur vers une structure **PPST \_ providerinfo retourné par** qui contient des informations sur le fournisseur de stockage.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

La valeur de retour est une valeur **HRESULT** . La valeur **PST \_ E \_ OK** indique que la fonction a réussi.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|----------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>Pstore. h</dt> </dl>    |
| DLL<br/>    | <dl> <dt>Pstorec.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IPStore**](ipstore.md)
</dt> </dl>

 

 
