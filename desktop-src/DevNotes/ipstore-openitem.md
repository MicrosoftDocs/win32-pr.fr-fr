---
description: Ouvre un élément pour plusieurs accès.
ms.assetid: b0602abd-dbda-40d0-befa-348c1179fa4f
title: 'IPStore :: OpenItem, méthode (PStore. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPStore.OpenItem
api_type:
- COM
api_location:
- Pstorec.dll
ms.openlocfilehash: 065b98c1f302596ce5a4a428ef2486e7cdcc2320
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106537354"
---
# <a name="ipstoreopenitem-method"></a>IPStore :: OpenItem, méthode

\[Le stockage protégé (PStore) peut être utilisé dans Windows Server 2003 et Windows XP. Elle est uniquement disponible pour les opérations en lecture seule dans Windows Server 2008 et Windows Vista, mais elle peut ne pas être disponible dans les versions ultérieures. Pstore utilise une implémentation plus ancienne de la protection des données. Les développeurs sont vivement encouragés à tirer parti de la protection renforcée des données fournie par les fonctions [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) et [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) .\]

Ouvre un élément pour plusieurs accès.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT OpenItem(
  [in]       PST_KEY        Key,
  [in] const PSGUID         *pItemType,
  [in] const GUID           *pItemSubtype,
  [in]       LPCWSTR        *szItemName,
  [in]       PST_ACCESSMODE ModeFlags,
  [in]       PPST_PROMPTIFO pProomptInfo,
  [in]       DWORD          dwFlags
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

Pointeur vers un GUID qui identifie le type de données de l’élément à ouvrir.

</dd> <dt>

*pItemSubtype* \[ dans\]
</dt> <dd>

Pointeur vers un GUID qui indique le sous-type d’élément à ouvrir.

</dd> <dt>

*szItemName* \[ dans\]
</dt> <dd>

Chaîne qui contient le nom de l’élément à ouvrir.

</dd> <dt>

*ModeFlags* \[ dans\]
</dt> <dd>

Décrit les modes d’accès auxquels appartient un ensemble spécifié de clauses d’accès. Pour plus d’informations, consultez [**types Pstore**](pstore-types.md).



| Valeur                                                                                                                                                                                                         | Signification                       |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------|
| <span id="PST_READ"></span><span id="pst_read"></span><dl> <dt>**Fichier PST \_ LIRE**</dt> <dt>0x0001</dt> </dl>    | Mode d’accès en lecture.<br/>  |
| <span id="PST_WRITE"></span><span id="pst_write"></span><dl> <dt>**Fichier PST \_ ÉCRIRE**</dt> <dt>0x0002</dt> </dl> | Mode d’accès en écriture.<br/> |



 

</dd> <dt>

*pProomptInfo* \[ dans\]
</dt> <dd>

Pointeur vers une structure [**\_ PROMPTINFO PST**](pst-promptinfo.md) .

</dd> <dt>

*dwFlags* \[ dans\]
</dt> <dd>

Réservé : doit être défini à zéro.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

La valeur de retour est une valeur **HRESULT** . La valeur **PST \_ E \_ OK** indique que la fonction a réussi.

## <a name="remarks"></a>Notes

L’utilisation de **OpenItem** pour ouvrir un élément dans la base de données de stockage protégée requiert qu’il soit fermé à l’aide de [**IPStore :: CloseItem**](ipstore-closeitem.md) pour empêcher une fuite de mémoire.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|----------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>Pstore. h</dt> </dl>    |
| DLL<br/>    | <dl> <dt>Pstorec.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IPStore**](ipstore.md)
</dt> <dt>

[**\_PROMPTINFO PST**](pst-promptinfo.md)
</dt> </dl>

 

 
