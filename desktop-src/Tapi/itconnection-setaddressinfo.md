---
description: La méthode SetAddressInfo définit les informations d’adresse.
ms.assetid: 100b96af-e6ba-4496-9978-4df133e1c2b5
title: 'ITConnection :: SetAddressInfo, méthode (sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ae181911527c22639c8c2da3038c0377734fd1da
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106543597"
---
# <a name="itconnectionsetaddressinfo-method"></a>ITConnection :: SetAddressInfo, méthode

\[ Les interfaces et les contrôles de conférence de téléphonie IP Rendezvous ne peuvent pas être utilisés dans Windows Vista, Windows Server 2008 et les versions ultérieures du système d’exploitation. L’API cliente RTC offre des fonctionnalités similaires.\]

La méthode **SetAddressInfo** définit les informations d’adresse.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT SetAddressInfo(
  [in] BSTR          pStartAddress,
  [in] LONG          NumAddresses,
  [in] unsigned char Ttl
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pStartAddress* \[ dans\]
</dt> <dd>

Pointeur vers un **BSTR** contenant l’adresse de début.

</dd> <dt>

*NumAddresses* \[ dans\]
</dt> <dd>

Nombre d’adresses à utiliser pour la session.

</dd> <dt>

*TTL* \[ dans\]
</dt> <dd>

étendue de la [*durée*](t-tapgloss.md) de vie (TTL) pour les transmissions sur les adresses.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode peut retourner l’une de ces valeurs.



| Valeur                                                                                         | Signification                                                                          |
|-----------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>          | La méthode a réussi.<br/>                                                     |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | Le paramètre *pStartAddress*, *NumAddresses* ou *TTL* n’est pas valide.<br/> |
| <dl> <dt>**\_OUTOFMEMORY E**</dt> </dl> | La mémoire disponible est insuffisante pour effectuer l’opération.<br/>                  |
| <dl> <dt>**E \_ échec**</dt> </dl>        | Erreur non spécifiée.<br/>                                                    |
| <dl> <dt>**\_NOTIMPL E**</dt> </dl>     | Cette méthode n'est pas encore implémentée.<br/>                                   |



 

## <a name="remarks"></a>Notes

L’application doit utiliser [**SysAllocString**](/windows/win32/api/oleauto/nf-oleauto-sysallocstring) pour allouer de la mémoire pour le paramètre *PStartAddress* et utiliser [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) pour libérer la mémoire lorsque la variable n’est plus nécessaire.

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

 

