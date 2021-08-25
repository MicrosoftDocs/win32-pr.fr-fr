---
description: La \_ méthode put NetworkType définit le type de réseau.
ms.assetid: 747e3133-d103-44dc-b119-5a4cb4ed7f18
title: ITConnection ::p ut_NetworkType, méthode (sdpblb. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 87f9d14090d04db639c95df59b051da77f2631064becff5bbb1873b37e82c745
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119774989"
---
# <a name="itconnectionput_networktype-method"></a>ITConnection ::p ut \_ NetworkType, méthode

\[les interfaces et les contrôles de conférence de téléphonie IP Rendezvous ne sont pas disponibles pour une utilisation dans Windows Vista, Windows Server 2008 et les versions ultérieures du système d’exploitation. L’API cliente RTC offre des fonctionnalités similaires.\]

La méthode **put \_ NetworkType** définit le type de réseau.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT put_NetworkType(
  [in] BSTR pNetworkType
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pNetworkType* \[ dans\]
</dt> <dd>

Pointeur vers un **BSTR** contenant le type de réseau.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode peut retourner l’une de ces valeurs.



| Code de retour                                                                                   | Description                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>          | La méthode a réussi.<br/>                                    |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | Le paramètre *pNetworkType* n’est pas valide.<br/>           |
| <dl> <dt>**\_OUTOFMEMORY E**</dt> </dl> | La mémoire disponible est insuffisante pour effectuer l’opération.<br/> |
| <dl> <dt>**E \_ échec**</dt> </dl>        | Erreur non spécifiée.<br/>                                   |
| <dl> <dt>**\_NOTIMPL E**</dt> </dl>     | Cette méthode n'est pas encore implémentée.<br/>                  |



 

## <a name="remarks"></a>Remarques

L’application doit utiliser [**SysAllocString**](/windows/win32/api/oleauto/nf-oleauto-sysallocstring) pour allouer de la mémoire pour le paramètre *PNetworkType* et utiliser [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) pour libérer la mémoire lorsque la variable n’est plus nécessaire.

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
</dt> <dt>

[**ITConnection :: obtient \_ NetworkType**](itconnection-get-networktype.md)
</dt> </dl>

 

