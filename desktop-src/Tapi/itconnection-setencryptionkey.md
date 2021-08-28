---
description: La méthode SetEncryptionKey définit la clé de chiffrement nécessaire pour déchiffrer la session ou une indication à un mécanisme pour obtenir une clé utilisable par un moyen externe.
ms.assetid: 9efcf90e-3645-49f4-b27d-9a8246637310
title: 'ITConnection :: SetEncryptionKey, méthode (sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c36b3fc9e37338b17aa00d19213118b1243ec70d2f21d21060fdd43894121566
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119406129"
---
# <a name="itconnectionsetencryptionkey-method"></a>ITConnection :: SetEncryptionKey, méthode

\[les interfaces et les contrôles de conférence de téléphonie IP Rendezvous ne sont pas disponibles pour une utilisation dans Windows Vista, Windows Server 2008 et les versions ultérieures du système d’exploitation. L’API cliente RTC offre des fonctionnalités similaires.\]

La méthode **SetEncryptionKey** définit la clé de chiffrement nécessaire pour déchiffrer la session ou une indication à un mécanisme pour obtenir une clé utilisable par un moyen externe.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT SetEncryptionKey(
  [in] BSTR pKeyType,
  [in] BSTR *ppKeyData
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pKeyType* \[ dans\]
</dt> <dd>

Pointeur vers un **BSTR** contenant le type de clé de chiffrement.

</dd> <dt>

*ppKeyData* \[ dans\]
</dt> <dd>

Pointeur vers un **BSTR** contenant des informations sur la clé de chiffrement.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode peut retourner l’une de ces valeurs.



| Code de retour                                                                          | Description                  |
|--------------------------------------------------------------------------------------|------------------------------|
| <dl> <dt>**\_OK**</dt> </dl> | La méthode a réussi.<br/> |



 

## <a name="remarks"></a>Remarques

L’application doit utiliser [**SysAllocString**](/windows/win32/api/oleauto/nf-oleauto-sysallocstring) pour allouer de la mémoire pour les paramètres *pKeyType* et *ppKeyData* . L’application doit utiliser [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) pour libérer la mémoire lorsque les variables ne sont plus nécessaires.

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

 

