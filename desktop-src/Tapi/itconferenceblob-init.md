---
description: La méthode Init Initialise l’objet blob de conférence en fonction d’une chaîne textuelle. Si pBlob a la valeur NULL, les valeurs par défaut sont utilisées.
ms.assetid: ba492503-90ff-45dd-a39f-6d4451e57339
title: 'ITConferenceBlob :: Init, méthode (sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 81bdd512ffeb4b380da04e59deb17315d00b7285
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106528133"
---
# <a name="itconferenceblobinit-method"></a>ITConferenceBlob :: Init, méthode

\[ Les interfaces et les contrôles de conférence de téléphonie IP Rendezvous ne peuvent pas être utilisés dans Windows Vista, Windows Server 2008 et les versions ultérieures du système d’exploitation. L’API cliente RTC offre des fonctionnalités similaires.\]

La méthode **init** Initialise l’objet blob de conférence en fonction d’une chaîne textuelle. Si *pBlob* a la **valeur null**, les valeurs par défaut sont utilisées.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT Init(
  [in] BSTR               pName,
  [in] BLOB_CHARACTER_SET CharacterSet,
  [in] BSTR               pBlob
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pname* \[ dans\]
</dt> <dd>

Pointeur vers une représentation **BSTR** du nom de la Conférence.

</dd> <dt>

*CharacterSet* \[ dans\]
</dt> <dd>

[**Objet BLOB \_ Descripteur du jeu \_ de**](blob-character-set.md) caractères du jeu de caractères.

</dd> <dt>

*pBlob* \[ dans\]
</dt> <dd>

Pointeur vers un **BSTR** contenant l’objet blob de conférence. Si la **valeur est null**, l’objet blob de conférence est initialisé avec les valeurs par défaut. Actuellement, les valeurs de conférence par défaut sont disponibles uniquement si le paramètre *CharacterSet* est défini sur BCS \_ ASCII.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode peut retourner l’une de ces valeurs.



| Valeur                                                                                         | Signification                                                                    |
|-----------------------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>          | La méthode a réussi.<br/>                                               |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | Le paramètre *pname*, *CharacterSet* ou *pBlob* n’est pas valide.<br/> |
| <dl> <dt>**\_OUTOFMEMORY E**</dt> </dl> | La mémoire disponible est insuffisante pour effectuer l’opération.<br/>            |
| <dl> <dt>**E \_ échec**</dt> </dl>        | Erreur non spécifiée.<br/>                                              |
| <dl> <dt>**\_NOTIMPL E**</dt> </dl>     | Cette méthode n'est pas encore implémentée.<br/>                             |



 

## <a name="remarks"></a>Notes

**ITConferenceBlob :: init** retourne un échec si l’objet BLOB a déjà été initialisé.

L’application doit utiliser [**SysAllocString**](/windows/win32/api/oleauto/nf-oleauto-sysallocstring) pour allouer de la mémoire aux paramètres *pname* et *pBlob* . L’application doit utiliser [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) pour libérer la mémoire lorsque les variables ne sont plus nécessaires.

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

 

