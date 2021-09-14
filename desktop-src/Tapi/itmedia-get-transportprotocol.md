---
description: La \_ méthode obtenir TransportProtocol obtient le protocole de transport.
ms.assetid: d270d6f4-bdcf-4cf4-970b-65f0be706171
title: 'ITMedia :: get_TransportProtocol, méthode (sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7cf2bc66a98e181674bbf6f7956579bbaa0b5a72
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127217924"
---
# <a name="itmediaget_transportprotocol-method"></a>ITMedia :: \_ TransportProtocol, méthode

\[les interfaces et les contrôles de conférence de téléphonie IP Rendezvous ne sont pas disponibles pour une utilisation dans Windows Vista, Windows Server 2008 et les versions ultérieures du système d’exploitation. L’API cliente RTC offre des fonctionnalités similaires.\]

La méthode **obtenir \_ TransportProtocol** obtient le protocole de transport. Cela est spécifié en plus du format de média, de sorte que le même format de média standard peut être utilisé sur différents protocoles de transport, même lorsque le protocole réseau est le même, par exemple avec les signaux audio de TVA PCM et audio PCM RTP.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT get_TransportProtocol(
  [out] BSTR *ppProtocol
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*ppProtocol* \[ à\]
</dt> <dd>

Pointeur vers la représentation **BSTR** du protocole de transport.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Cette méthode peut retourner l’une de ces valeurs.



| Code de retour                                                                                   | Description                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>          | La méthode a réussi.<br/>                                    |
| <dl> <dt>**\_pointeur E**</dt> </dl>     | Le paramètre *ppProtocol* n’est pas un pointeur valide.<br/>   |
| <dl> <dt>**\_OUTOFMEMORY E**</dt> </dl> | La mémoire disponible est insuffisante pour effectuer l’opération.<br/> |
| <dl> <dt>**E \_ échec**</dt> </dl>        | Erreur non spécifiée.<br/>                                   |
| <dl> <dt>**\_NOTIMPL E**</dt> </dl>     | Cette méthode n'est pas encore implémentée.<br/>                  |



 

## <a name="remarks"></a>Notes

L’application doit utiliser [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) pour libérer la mémoire allouée pour le paramètre *ppProtocol* .

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------|---------------------------------------------------------------------------------------|
| Version TAPI<br/> | Nécessite TAPI 3,0 ou une version ultérieure<br/>                                                 |
| En-tête<br/>       | <dl> <dt>Sdpblb. h</dt> </dl>   |
| Bibliothèque<br/>      | <dl> <dt>UUID. lib</dt> </dl>   |
| DLL<br/>          | <dl> <dt>Sdpblb.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**ITMedia**](itmedia.md)
</dt> <dt>

[**ITMedia ::p ut \_ TransportProtocol**](itmedia-put-transportprotocol.md)
</dt> </dl>

 

