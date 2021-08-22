---
description: La \_ méthode obtenir CharacterSet obtient un \_ \_ descripteur de jeu de caractères BLOB du jeu de caractères utilisé dans l’objet blob de conférence actuel.
ms.assetid: 9783d18c-79f6-4faa-b12d-9504c13d54e3
title: 'ITConferenceBlob :: get_CharacterSet, méthode (sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 20a9dd719d2ae9742a6ec4b3295e3e22ffe871b4a38c55d07e07a3421271553d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119060997"
---
# <a name="itconferenceblobget_characterset-method"></a>ITConferenceBlob :: obtient la \_ méthode CharacterSet

\[les interfaces et les contrôles de conférence de téléphonie IP Rendezvous ne sont pas disponibles pour une utilisation dans Windows Vista, Windows Server 2008 et les versions ultérieures du système d’exploitation. L’API cliente RTC offre des fonctionnalités similaires.\]

La méthode **obtenir \_ CharacterSet** obtient un descripteur de [**\_ \_ jeu de caractères BLOB**](blob-character-set.md) du jeu de caractères utilisé dans l’objet blob de conférence actuel.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT get_CharacterSet(
  [out] BLOB_CHARACTER_SET *pCharacterSet
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pCharacterSet* \[ à\]
</dt> <dd>

Pointeur vers le descripteur d’un [**\_ \_ jeu de caractères BLOB**](blob-character-set.md) du jeu de caractères.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode peut retourner l’une de ces valeurs.



| Code de retour                                                                                                   | Description                                                      |
|---------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>                          | La méthode a réussi.<br/>                                     |
| <dl> <dt>**\_pointeur E**</dt> </dl>                     | Le paramètre *pCharacterSet* n’est pas un pointeur valide.<br/> |
| <dl> <dt>**\_OUTOFMEMORY E**</dt> </dl>                 | La mémoire disponible est insuffisante pour effectuer l’opération.<br/>  |
| <dl> <dt>**E \_ échec**</dt> </dl>                        | Erreur non spécifiée.<br/>                                    |
| <dl> <dt>**\_NOTIMPL E**</dt> </dl>                     | Cette méthode n'est pas encore implémentée.<br/>                   |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>                  | *pCharacterSet* a la **valeur null**.<br/>                          |
| <dl> <dt>**SIGNÉ ERREUR de \_ données non valides \_**</dt> </dl> | Le jeu de caractères actuel n’est pas valide ou n’est pas disponible.<br/>  |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------|---------------------------------------------------------------------------------------|
| Version TAPI<br/> | Nécessite TAPI 3,0 ou une version ultérieure<br/>                                                 |
| En-tête<br/>       | <dl> <dt>Sdpblb. h</dt> </dl>   |
| Bibliothèque<br/>      | <dl> <dt>UUID. lib</dt> </dl>   |
| DLL<br/>          | <dl> <dt>Sdpblb.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**ITConferenceBlob**](itconferenceblob.md)
</dt> <dt>

[**\_jeu de caractères BLOB \_**](blob-character-set.md)
</dt> </dl>

 

 




