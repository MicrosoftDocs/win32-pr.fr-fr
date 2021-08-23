---
description: La méthode SetPhoneNumbers définit un tableau de numéros de téléphone associés à un objet blob de conférence.
ms.assetid: 674c08df-7e91-4f19-9d65-4bc6e7af117b
title: 'ITSdp :: SetPhoneNumbers, méthode (sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 733dfbe4752281abf4063f308a05aec73203d361e3c9c5dcebf413eb4ba2af72
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119140212"
---
# <a name="itsdpsetphonenumbers-method"></a>ITSdp :: SetPhoneNumbers, méthode

\[les interfaces et les contrôles de conférence de téléphonie IP Rendezvous ne sont pas disponibles pour une utilisation dans Windows Vista, Windows Server 2008 et les versions ultérieures du système d’exploitation. L’API cliente RTC offre des fonctionnalités similaires.\]

La méthode **SetPhoneNumbers** définit un tableau de numéros de téléphone associés à un objet blob de conférence.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT SetPhoneNumbers(
  [in] VARIANT Numbers,
  [in] VARIANT Names
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Nombres* \[ dans\]
</dt> <dd>

SAFEARRAY de **BSTR** répertoriant les numéros de téléphone.

</dd> <dt>

*Noms* \[ dans\]
</dt> <dd>

SAFEARRAY de noms de liste de **BSTR**.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode peut retourner l’une de ces valeurs.



| Code de retour                                                                                   | Description                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>          | La méthode a réussi.<br/>                                    |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | Le paramètre *numbers* ou *Names* n’est pas valide.<br/>     |
| <dl> <dt>**\_OUTOFMEMORY E**</dt> </dl> | La mémoire disponible est insuffisante pour effectuer l’opération.<br/> |
| <dl> <dt>**E \_ échec**</dt> </dl>        | Erreur non spécifiée.<br/>                                   |
| <dl> <dt>**\_NOTIMPL E**</dt> </dl>     | Cette méthode n'est pas encore implémentée.<br/>                  |



 

## <a name="remarks"></a>Remarques

Les listes dont les *nombres* et les *noms* pointent sont de la même longueur.

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

 

 




