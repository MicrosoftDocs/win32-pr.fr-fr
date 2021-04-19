---
description: Supprime l’élément spécifié du stockage protégé.
ms.assetid: 1d071245-a563-4fba-9300-c47ca9a9d625
title: IPStore ::D méthode eleteItem (PStore. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPStore.DeleteItem
api_type:
- COM
api_location:
- Pstorec.dll
ms.openlocfilehash: 3a882b9178160e8e82222943501c3317f8f11536
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106537825"
---
# <a name="ipstoredeleteitem-method"></a>IPStore ::D méthode eleteItem

\[Le stockage protégé (PStore) peut être utilisé dans Windows Server 2003 et Windows XP. Elle est uniquement disponible pour les opérations en lecture seule dans Windows Server 2008 et Windows Vista, mais elle peut ne pas être disponible dans les versions ultérieures. Pstore utilise une implémentation plus ancienne de la protection des données. Les développeurs sont vivement encouragés à tirer parti de la protection renforcée des données fournie par les fonctions [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) et [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) .\]

Supprime l’élément spécifié du stockage protégé.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT DeleteItem(
  [in]       PST_KEY         Key,
  [in] const GUID            *pItemType,
  [in] const GUID            *pItemSubType,
  [in]       LPCWSTR         szItemName,
  [in]       PPST_PROMPTINFO pPromptInfo,
  [in]       DWORD           dwFlags
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

Pointeur vers un **GUID** qui identifie le type de données de l’élément à supprimer.

</dd> <dt>

*pItemSubType* \[ dans\]
</dt> <dd>

**GUID** qui indique le sous-type d’élément à supprimer.

</dd> <dt>

*szItemName* \[ dans\]
</dt> <dd>

Chaîne qui contient le nom de l’élément à supprimer.

</dd> <dt>

*pPromptInfo* \[ dans\]
</dt> <dd>

Pointeur vers une structure [**\_ PROMPTINFO PST**](pst-promptinfo.md) .

</dd> <dt>

*dwFlags* \[ dans\]
</dt> <dd>

Spécifie l’interface utilisateur et les comportements de sécurité pour l’opération de suppression.



| Valeur                                                                                                                                                                                                                                             | Signification                                                                     |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------|
| <span id="PST_NO_UI_MIGRATION"></span><span id="pst_no_ui_migration"></span><dl> <dt>**Fichier PST \_ AUCUNE \_ \_ migration de l’interface utilisateur**</dt> <dt>0x00000010</dt> </dl> | N’affiche pas l’interface utilisateur, sauf si un mot de passe personnalisé est requis.<br/> |



 

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

 

 
