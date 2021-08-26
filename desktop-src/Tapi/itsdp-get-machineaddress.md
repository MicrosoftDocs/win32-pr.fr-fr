---
description: La \_ méthode obtenir MachineAddress obtient l’adresse de l’ordinateur hôte d’origine.
ms.assetid: 8a67cc9f-f9fc-4ec3-86f9-ffe34d075830
title: 'ITSdp :: get_MachineAddress, méthode (sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3a4e4d849c17d6c371a6edc927679e2ba6af344fbf8515310eb22b27ba4abeab
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120012929"
---
# <a name="itsdpget_machineaddress-method"></a>ITSdp :: \_ MachineAddress, méthode

\[les interfaces et les contrôles de conférence de téléphonie IP Rendezvous ne sont pas disponibles pour une utilisation dans Windows Vista, Windows Server 2008 et les versions ultérieures du système d’exploitation. L’API cliente RTC offre des fonctionnalités similaires.\]

La méthode **obtenir \_ MachineAddress** obtient l’adresse de l’ordinateur hôte d’origine.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT get_MachineAddress(
  [out] BSTR *ppMachineAddress
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*ppMachineAddress* \[ à\]
</dt> <dd>

Pointeur vers un **BSTR** contenant l’adresse de l’ordinateur hôte de la Conférence.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode peut retourner l’une de ces valeurs.



| Code de retour                                                                                   | Description                                                         |
|-----------------------------------------------------------------------------------------------|---------------------------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>          | La méthode a réussi.<br/>                                        |
| <dl> <dt>**\_pointeur E**</dt> </dl>     | Le paramètre *ppMachineAddres* s n’est pas un pointeur valide.<br/> |
| <dl> <dt>**\_OUTOFMEMORY E**</dt> </dl> | La mémoire disponible est insuffisante pour effectuer l’opération.<br/>     |
| <dl> <dt>**E \_ échec**</dt> </dl>        | Erreur non spécifiée.<br/>                                       |
| <dl> <dt>**\_NOTIMPL E**</dt> </dl>     | Cette méthode n'est pas encore implémentée.<br/>                      |



 

## <a name="remarks"></a>Remarques

L’application doit utiliser [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) pour libérer la mémoire allouée pour le paramètre *ppMachineAddress* .

Le paramètre *ppMachineAddress* peut être retourné sous la forme d’un nom DNS (« johnsmith.workinghard.Microsoft.com ») ou d’une adresse IP (« 10.111.222.111 »).

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
</dt> <dt>

[**ITSdp ::p ut \_ MachineAddress**](itsdp-put-machineaddress.md)
</dt> </dl>

 

