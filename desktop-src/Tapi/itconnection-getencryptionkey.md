---
description: La méthode GetEncryptionKey obtient la clé de chiffrement.
ms.assetid: a80d8660-d13e-483f-b1d7-ee2043ef5cab
title: 'ITConnection :: GetEncryptionKey, méthode (sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2a237073d4842cd26797b046a4d973390ff5ef254b574bcafbc6f10abca932aa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119060977"
---
# <a name="itconnectiongetencryptionkey-method"></a>ITConnection :: GetEncryptionKey, méthode

\[les interfaces et les contrôles de conférence de téléphonie IP Rendezvous ne sont pas disponibles pour une utilisation dans Windows Vista, Windows Server 2008 et les versions ultérieures du système d’exploitation. L’API cliente RTC offre des fonctionnalités similaires.\]

La méthode **GetEncryptionKey** obtient la clé de chiffrement.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetEncryptionKey(
  [out] BSTR         *ppKeyType,
  [out] VARIANT_BOOL *pfValidKeyData,
  [out] BSTR         *ppKeyData
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*ppKeyType* \[ à\]
</dt> <dd>

Pointeur vers un **BSTR** contenant le type de clé de chiffrement.

</dd> <dt>

*pfValidKeyData* \[ à\]
</dt> <dd>

Indique la validité des données de clé de chiffrement.

</dd> <dt>

*ppKeyData* \[ à\]
</dt> <dd>

Pointeur vers un **BSTR** contenant les données de clé de chiffrement.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode peut retourner l’une de ces valeurs.



| Code de retour                                                                                   | Description                                                                                  |
|-----------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>          | La méthode a réussi.<br/>                                                                 |
| <dl> <dt>**\_pointeur E**</dt> </dl>     | Le paramètre *ppKeyType, pfValidKeyData* ou *ppKeyData* n’est pas un pointeur valide.<br/> |
| <dl> <dt>**\_OUTOFMEMORY E**</dt> </dl> | La mémoire disponible est insuffisante pour effectuer l’opération.<br/>                              |
| <dl> <dt>**E \_ échec**</dt> </dl>        | Erreur non spécifiée.<br/>                                                                |
| <dl> <dt>**\_NOTIMPL E**</dt> </dl>     | Cette méthode n'est pas encore implémentée.<br/>                                               |



 

## <a name="remarks"></a>Remarques

L’application doit utiliser [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) pour libérer la mémoire allouée pour les paramètres *ppKeyType* et *ppKeyData* .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------|---------------------------------------------------------------------------------------|
| Version TAPI<br/> | Nécessite TAPI 3,0 ou une version ultérieure<br/>                                                 |
| En-tête<br/>       | <dl> <dt>Sdpblb. h</dt> </dl>   |
| Bibliothèque<br/>      | <dl> <dt>UUID. lib</dt> </dl>   |
| DLL<br/>          | <dl> <dt>Sdpblb.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**ITConnection**](itconnection.md)
</dt> </dl>

 

