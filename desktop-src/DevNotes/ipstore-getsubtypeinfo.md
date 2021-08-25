---
description: Récupère les informations associées à un sous-type.
ms.assetid: 3daf5f37-9e7f-4ce1-bd35-d7e3c2ef5c28
title: 'IPStore :: GetSubtypeInfo, méthode (PStore. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPStore.GetSubtypeInfo
api_type:
- COM
api_location:
- Pstorec.dll
ms.openlocfilehash: d97b1f710344acf2c635adb5109175d017fc568d87673f5565e1be5b22e06cf8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119749839"
---
# <a name="ipstoregetsubtypeinfo-method"></a>IPStore :: GetSubtypeInfo, méthode

\[le Stockage protégé (Pstore) peut être utilisé dans Windows Server 2003 et Windows XP. elle est uniquement disponible pour les opérations en lecture seule dans Windows Server 2008 et Windows Vista, mais elle peut ne pas être disponible dans les versions ultérieures. Pstore utilise une implémentation plus ancienne de la protection des données. Les développeurs sont vivement encouragés à tirer parti de la protection renforcée des données fournie par les fonctions [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) et [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) .\]

Récupère les informations associées à un sous-type.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetSubtypeInfo(
  [in]       PST_KEY       Key,
  [in] const GUID          *pType,
  [in] const GUID          *pSubtype,
  [in]       PPST_TYPEINFO **ppInfo,
  [in]       DWORD         dwFlags
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Clé* \[ dans\]
</dt> <dd>

Zone de stockage du fournisseur.



| Valeur                                                                                                                                                                                                                                                   | Signification                                                                            |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <span id="PST_KEY_CURRENT_USER"></span><span id="pst_key_current_user"></span><dl> <dt>**Fichier PST \_ \_ \_ Utilisateur actuel**</dt> <dt>0x00000000</dt> </dl>    | Le stockage est conservé dans la section utilisateur actuel du Registre.<br/>  |
| <span id="PST_KEY_LOCAL_MACHINE"></span><span id="pst_key_local_machine"></span><dl> <dt>**Fichier PST \_ \_ \_ Ordinateur local**</dt> de la clé <dt>0x00000001</dt> </dl> | Le stockage est conservé dans la section ordinateur local du Registre.<br/> |



 

</dd> <dt>

*PTYPE* \[ dans\]
</dt> <dd>

Pointeur vers un GUID qui identifie le type de données du stockage.

</dd> <dt>

*pSubtype* \[ dans\]
</dt> <dd>

Pointeur vers un GUID qui identifie le sous-type de données du stockage.

</dd> <dt>

*ppInfo* \[ dans\]
</dt> <dd>

Pointeur vers une structure [**\_ TypeInfo PST**](pst-typeinfo.md) .

</dd> <dt>

*dwFlags* \[ dans\]
</dt> <dd>

Réservé : doit être défini à zéro.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

La valeur de retour est une valeur **HRESULT** . La valeur PST \_ E \_ OK indique que la fonction a réussi.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|----------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>Pstore. h</dt> </dl>    |
| DLL<br/>    | <dl> <dt>Pstorec.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IPStore**](ipstore.md)
</dt> <dt>

[**\_TypeInfo PST**](pst-typeinfo.md)
</dt> </dl>

 

 
