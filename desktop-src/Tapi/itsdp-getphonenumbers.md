---
description: La méthode GetPhoneNumbers obtient un tableau de numéros de téléphone associés à un objet blob de conférence.
ms.assetid: c4ad6c5a-e15c-45ae-94de-763a843554bb
title: 'ITSdp :: GetPhoneNumbers, méthode (sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 465bc6b2d2167ca17d25b8f50466f111724ea3b5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106525639"
---
# <a name="itsdpgetphonenumbers-method"></a>ITSdp :: GetPhoneNumbers, méthode

\[ Les interfaces et les contrôles de conférence de téléphonie IP Rendezvous ne peuvent pas être utilisés dans Windows Vista, Windows Server 2008 et les versions ultérieures du système d’exploitation. L’API cliente RTC offre des fonctionnalités similaires.\]

La méthode **GetPhoneNumbers** obtient un tableau de numéros de téléphone associés à un objet blob de conférence.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetPhoneNumbers(
  [out] VARIANT *pNumbers,
  [out] VARIANT *pNames
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pNumbers* \[ à\]
</dt> <dd>

Pointeur de **type Variant** vers un SafeArray de **BSTR** qui répertorie les numéros de téléphone.

</dd> <dt>

*pNames* \[ à\]
</dt> <dd>

Pointeur de **type Variant** vers un SafeArray de noms de liste de **BSTR**.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode peut retourner l’une de ces valeurs.



| Code de retour                                                                                   | Description                                                             |
|-----------------------------------------------------------------------------------------------|-------------------------------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>          | La méthode a réussi.<br/>                                            |
| <dl> <dt>**\_pointeur E**</dt> </dl>     | Le paramètre *pNumbers* ou *pNames* n’est pas un pointeur valide.<br/> |
| <dl> <dt>**\_OUTOFMEMORY E**</dt> </dl> | La mémoire disponible est insuffisante pour effectuer l’opération.<br/>         |
| <dl> <dt>**E \_ échec**</dt> </dl>        | Erreur non spécifiée.<br/>                                           |
| <dl> <dt>**\_NOTIMPL E**</dt> </dl>     | Cette méthode n'est pas encore implémentée.<br/>                          |



 

## <a name="remarks"></a>Notes

Les listes que *pNumbers* et *pNames* pointent sont de la même longueur.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------|---------------------------------------------------------------------------------------|
| Version TAPI<br/> | Nécessite TAPI 3,0 ou une version ultérieure<br/>                                                 |
| En-tête<br/>       | <dl> <dt>Sdpblb. h</dt> </dl>   |
| Bibliothèque<br/>      | <dl> <dt>UUID. lib</dt> </dl>   |
| DLL<br/>          | <dl> <dt>Sdpblb.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**ITSdp**](itsdp.md)
</dt> </dl>

 

 




