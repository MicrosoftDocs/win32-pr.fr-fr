---
description: Écrit les règles d’accès pour le type donné.
ms.assetid: d5cfd782-8d87-45ae-a574-0a294a30ca71
title: 'IPStore :: WriteAccessRuleset, méthode (PStore. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPStore.WriteAccessRuleset
api_type:
- COM
api_location:
- Pstorec.dll
ms.openlocfilehash: a21fac6df5ab4d87e55d71e45f5698251ca4f82b6c93de1072c2ae5bcd7236aa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118955898"
---
# <a name="ipstorewriteaccessruleset-method"></a>IPStore :: WriteAccessRuleset, méthode

\[le Stockage protégé (Pstore) peut être utilisé dans Windows Server 2003 et Windows XP. elle est uniquement disponible pour les opérations en lecture seule dans Windows Server 2008 et Windows Vista, mais elle peut ne pas être disponible dans les versions ultérieures. Pstore utilise une implémentation plus ancienne de la protection des données. Les développeurs sont vivement encouragés à tirer parti de la protection renforcée des données fournie par les fonctions [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) et [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) .\]

\[Cette méthode n’est pas implémentée.\]

Écrit les règles d’accès pour le type donné.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT WriteAccessRuleset(
  [in]       PST_KEY            Key,
  [in] const GUID               *pType,
  [in] const GUID               *pSubtype,
  [in]       PPST_TYPEINFO      pInfo,
  [in]       PPST_ACCESSRULESET pRules,
  [in]       DWORD              dwFlags
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Clé* \[ dans\]
</dt> <dd>

Réservé.

</dd> <dt>

*PTYPE* \[ dans\]
</dt> <dd>

Réservé.

</dd> <dt>

*pSubtype* \[ dans\]
</dt> <dd>

Réservé.

</dd> <dt>

*pinfo* \[ dans\]
</dt> <dd>

Réservé.

</dd> <dt>

*pRules* \[ dans\]
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

 

 
