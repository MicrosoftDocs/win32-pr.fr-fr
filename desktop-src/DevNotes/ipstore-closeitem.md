---
description: Ferme un élément de données spécifié à partir du stockage protégé.
ms.assetid: 74919354-5e31-4ab5-9326-9f9aae206bd7
title: 'IPStore :: CloseItem, méthode (PStore. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPStore.CloseItem
api_type:
- COM
api_location:
- Pstorec.dll
ms.openlocfilehash: 54ebcc20686a09344990af5dc742d018f4e2a19d9ca8669b6a90bd4563014173
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120001629"
---
# <a name="ipstorecloseitem-method"></a>IPStore :: CloseItem, méthode

\[le Stockage protégé (Pstore) peut être utilisé dans Windows Server 2003 et Windows XP. elle est uniquement disponible pour les opérations en lecture seule dans Windows Server 2008 et Windows Vista, mais elle peut ne pas être disponible dans les versions ultérieures. Pstore utilise une implémentation plus ancienne de la protection des données. Les développeurs sont vivement encouragés à tirer parti de la protection renforcée des données fournie par les fonctions [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) et [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) .\]

Ferme un élément de données spécifié à partir du stockage protégé.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT CloseItem(
  [in]       PST_KEY Key,
  [in] const PSGUID  *pItemType,
  [in] const GUID    *pItemSubtype,
  [in]       LPCWSTR *szItemName,
  [in]       DWORD   dwFlags
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Clé* \[ dans\]
</dt> <dd>

Spécifie si le type est local sur l’ordinateur ou s’il est associé uniquement à l’utilisateur en train de créer.



| Valeur                                                                                                                                                                                                                                                   | Signification                                                                            |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <span id="PST_KEY_CURRENT_USER"></span><span id="pst_key_current_user"></span><dl> <dt>**Fichier PST \_ \_ \_ Utilisateur actuel**</dt> <dt>0x00000000</dt> </dl>    | Le stockage est conservé dans la section utilisateur actuel du Registre.<br/>  |
| <span id="PST_KEY_LOCAL_MACHINE"></span><span id="pst_key_local_machine"></span><dl> <dt>**Fichier PST \_ \_ \_ Ordinateur local**</dt> de la clé <dt>0x00000001</dt> </dl> | Le stockage est conservé dans la section ordinateur local du Registre.<br/> |



 

</dd> <dt>

*pItemType* \[ dans\]
</dt> <dd>

Pointeur vers un **GUID** qui identifie le type de données de l’élément à fermer.

</dd> <dt>

*pItemSubtype* \[ dans\]
</dt> <dd>

Pointeur vers un **GUID** qui indique le sous-type d’élément à fermer.

</dd> <dt>

*szItemName* \[ dans\]
</dt> <dd>

Chaîne qui contient le nom de l’élément à fermer.

</dd> <dt>

*dwFlags* \[ dans\]
</dt> <dd>

Réservé : doit être défini à zéro.

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

 

 
