---
description: Lit l’élément de données spécifié à partir du stockage protégé.
ms.assetid: e565a0ea-5d8e-4706-a176-2305a95f0d67
title: 'IPStore :: ReadItem, méthode (PStore. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPStore.ReadItem
api_type:
- COM
api_location:
- Pstorec.dll
ms.openlocfilehash: 516eb55772e375d09d3b134dee456c090cf11d6ef0d10905f99a822b1df0d9e5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120001488"
---
# <a name="ipstorereaditem-method"></a>IPStore :: ReadItem, méthode

\[le Stockage protégé (Pstore) peut être utilisé dans Windows Server 2003 et Windows XP. elle est uniquement disponible pour les opérations en lecture seule dans Windows Server 2008 et Windows Vista, mais elle peut ne pas être disponible dans les versions ultérieures. Pstore utilise une implémentation plus ancienne de la protection des données. Les développeurs sont vivement encouragés à tirer parti de la protection renforcée des données fournie par les fonctions [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) et [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) .\]

Lit l’élément de données spécifié à partir du stockage protégé.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT ReadItem(
  [in]       PST_KEY        Key,
  [in] const PSGUID         *pItemType,
  [in] const GUID           *pItemSubtype,
  [in]       LPCWSTR        *szItemName,
  [in]       DWORD          cbData,
  [in]       BYTE_RPC_FAR   *pbData,
  [in]       PPST_PROMPTIFO pPromptInfo,
  [in]       DWORD          dwFlags
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

Pointeur vers un GUID qui identifie le type de données de l’élément à lire.

</dd> <dt>

*pItemSubtype* \[ dans\]
</dt> <dd>

Pointeur vers un GUID qui identifie le sous-type de données de l’élément à lire.

</dd> <dt>

*szItemName* \[ dans\]
</dt> <dd>

Pointeur vers une chaîne qui contient le nom assigné à l’élément de données stocké.

</dd> <dt>

*cbData* \[ dans\]
</dt> <dd>

**Valeur DWORD** qui indique la taille de la mémoire tampon qui contient l’élément de données stockées.

</dd> <dt>

*pbData* \[ dans\]
</dt> <dd>

Pointeur vers une mémoire tampon qui contient l’élément de données stockées.

</dd> <dt>

*pPromptInfo* \[ dans\]
</dt> <dd>

Pointeur vers une structure [**\_ PROMPTINFO PST**](pst-promptinfo.md) .

</dd> <dt>

*dwFlags* \[ dans\]
</dt> <dd>

Spécifie l’interface utilisateur et les comportements de sécurité pour l’opération de lecture.

Les valeurs d’indicateur peuvent être combinées avec un opérateur logique OR.



| Valeur                                                                                                                                                                                                                                                              | Signification                                                                                                                                                                                                                                |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="PST_UNRESTRICTED_ITEMDATA"></span><span id="pst_unrestricted_itemdata"></span><dl> <dt>**Fichier PST \_ \_ITEMDATA**</dt> <dt>0x00000004</dt> non restreint </dl> | Spécifie que le flux de données n’est pas sécurisé. Par défaut, les appels d’élément sont sécurisés.<br/>                                                                                                                                             |
| <span id="PST_PROMPT_QUERY"></span><span id="pst_prompt_query"></span><dl> <dt>**Fichier PST \_ INVITE de \_ requête**</dt> <dt>0x00000008</dt> </dl>                            | Spécifie que la confirmation doit être retournée en cas de réussite. Si l’interface utilisateur est activée, la réussite du **fichier PST \_ E \_ OK** est retournée. Si l’interface utilisateur n’est pas activée, la valeur de l' **\_ \_ élément \_ PST E** est retournée.<br/> |
| <span id="PST_NO_UI_MIGRATION"></span><span id="pst_no_ui_migration"></span><dl> <dt>**Fichier PST \_ AUCUNE \_ \_ migration de l’interface utilisateur**</dt> <dt>0x00000010</dt> </dl>                  | N’affiche pas l’interface utilisateur, sauf si un mot de passe personnalisé est requis.<br/>                                                                                                                                                            |



 

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

La valeur de retour est une valeur **HRESULT** . La valeur **PST \_ E \_ OK** indique que la fonction a réussi.

## <a name="remarks"></a>Remarques

Si **ReadItem** se termine correctement, l’application est chargée de libérer la mémoire tampon de données retournée à l’aide de la fonction [**CoTaskMemFree**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree) .

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

 

 
