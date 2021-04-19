---
description: Écrit un élément de données dans le stockage protégé.
ms.assetid: d940470c-b881-4e05-8e52-f804eac11e45
title: 'IPStore :: WriteItem, méthode (PStore. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPStore.WriteItem
api_type:
- COM
api_location:
- Pstorec.dll
ms.openlocfilehash: b11436ca5a884b7d45c853433c3203b219e0527c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106545602"
---
# <a name="ipstorewriteitem-method"></a>IPStore :: WriteItem, méthode

\[Le stockage protégé (PStore) peut être utilisé dans Windows Server 2003 et Windows XP. Elle est uniquement disponible pour les opérations en lecture seule dans Windows Server 2008 et Windows Vista, mais elle peut ne pas être disponible dans les versions ultérieures. Pstore utilise une implémentation plus ancienne de la protection des données. Les développeurs sont vivement encouragés à tirer parti de la protection renforcée des données fournie par les fonctions [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) et [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) .\]

Écrit un élément de données dans le stockage protégé.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT WriteItem(
  [in]        PST_KEY        Key,
  [in]  const GUID           *pItemType,
  [in]  const GUID           *pItemSubtype,
  [in]        LPCWSTR        *szItemName,
  [out]       DWORD          *cbData,
  [out]       BYTE           ppbData,
  [in]        PPST_PROMPTIFO pProomptInfo,
  [in]        DWORD          dwDefaultConfirmationStyle,
  [in]        DWORD          dwFlags
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

*pItemType* \[ dans\]
</dt> <dd>

Pointeur vers un **GUID** qui identifie le type de données de l’élément de données en cours d’écriture.

</dd> <dt>

*pItemSubtype* \[ dans\]
</dt> <dd>

Pointeur vers un **GUID** qui identifie le sous-type de données de l’élément de données en cours d’écriture.

</dd> <dt>

*szItemName* \[ dans\]
</dt> <dd>

Pointeur vers une chaîne qui contient le nom assigné à l’élément de données stocké.

</dd> <dt>

*cbData* \[ à\]
</dt> <dd>

Pointeur vers une **valeur DWORD** qui indique la taille de la mémoire tampon qui contient l’élément de données stockées.

</dd> <dt>

*ppbData* \[ à\]
</dt> <dd>

Pointeur vers une mémoire tampon qui contient l’élément de données en cours d’écriture.

</dd> <dt>

*pProomptInfo* \[ dans\]
</dt> <dd>

Pointeur vers une [**structure \_ PROMPTINFO PST**](pst-promptinfo.md) .

</dd> <dt>

*dwDefaultConfirmationStyle* \[ dans\]
</dt> <dd>

Style de confirmation par défaut.



| Valeur                                                                                                                                                                                                                             | Signification                                                       |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------|
| <span id="PST_CF_DEFAULT"></span><span id="pst_cf_default"></span><dl> <dt>**Fichier PST \_ CF \_ par défaut**</dt> <dt>0x00000000</dt> </dl> | Permet à l’utilisateur de choisir le style de confirmation. <br/> |
| <span id="PST_CF_NONE"></span><span id="pst_cf_none"></span><dl> <dt>**Fichier PST \_ CF \_ aucun**</dt> <dt>0x00000001</dt> </dl>          | Force la création d’un élément silencieux. <br/>                      |



 

</dd> <dt>

*dwFlags* \[ dans\]
</dt> <dd>

L’interface utilisateur et les comportements de sécurité pour l’opération d’écriture.



| Valeur                                                                                                                                                                                                                                                              | Signification                                                                                                            |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------|
| <span id="PST_NO_OVERWRITE"></span><span id="pst_no_overwrite"></span><dl> <dt>**Fichier PST \_ AUCUN \_ remplacement**</dt> <dt>0x00000002</dt> </dl>                            | Spécifie que l’élément doit être créé dans un stockage protégé. Le remplacement d’un élément existant n’est pas autorisé.<br/> |
| <span id="PST_UNRESTRICTED_ITEMDATA"></span><span id="pst_unrestricted_itemdata"></span><dl> <dt>**Fichier PST \_ \_ITEMDATA**</dt> <dt>0x00000004</dt> non restreint </dl> | Spécifie que le flux de données n’est pas sécurisé. Par défaut, les appels d’élément sont sécurisés.<br/>                         |



 

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
</dt> <dt>

[**\_PROMPTINFO PST**](pst-promptinfo.md)
</dt> </dl>

 

 
