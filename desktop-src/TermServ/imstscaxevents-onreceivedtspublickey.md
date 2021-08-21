---
title: Méthode IMsTscAxEvents OnReceivedTSPublicKey
description: Appelé pendant la séquence de connexion lorsque le client récupère la clé publique du serveur. Cet événement est appelé uniquement si la propriété NotifyTSPublicKey a la \_ valeur variant true.
ms.assetid: 1db98b8b-2f08-4252-ad8b-6764fa25b300
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode OnReceivedTSPublicKey
- Méthode OnReceivedTSPublicKey Services Bureau à distance, interface IMsTscAxEvents
- Services Bureau à distance de l’interface IMsTscAxEvents, méthode OnReceivedTSPublicKey
topic_type:
- apiref
api_name:
- IMsTscAxEvents.OnReceivedTSPublicKey
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 73f2b12b59cbe8e6b7c5f8e614e2aed047d4f467117fa211839521fedc7f333b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120009479"
---
# <a name="imstscaxeventsonreceivedtspublickey-method"></a>IMsTscAxEvents :: OnReceivedTSPublicKey, méthode

Appelé pendant la séquence de connexion lorsque le client récupère la clé publique du serveur. Cet événement est appelé uniquement si la propriété **NotifyTSPublicKey** a **la \_ valeur variant true**. Cela se fait après [**OnConnecting**](imstscaxevents-onconnecting.md), mais avant [**OnAuthenticationWarningDisplayed**](imstscaxevents-onauthenticationwarningdisplayed.md) et [**OnConnected**](imstscaxevents-onconnected.md).

## <a name="syntax"></a>Syntaxe


```C++
void OnReceivedTSPublicKey(
  [in]  BSTR         publicKey,
  [out] VARIANT_BOOL *pfContinueLogon
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*PublicKey* \[ dans\]
</dt> <dd>

Contient la clé publique de l’ordinateur distant.

</dd> <dt>

*pfContinueLogon* \[ à\]
</dt> <dd>

Pointeur vers une variable **Variant \_ booléenne** qui reçoit une valeur indiquant si le processus d’ouverture de session doit continuer.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode ne retourne pas de valeur.

## <a name="remarks"></a>Remarques

Pour plus d’informations sur la Connexion Bureau à distance par le Web, consultez [Requirements for connexion Bureau à distance par le Web](requirements-for-remote-desktop-web-connection.md).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Vista<br/>                                                               |
| Serveur minimal pris en charge<br/> | Windows serveur 2008, Windows server 2008 avec SP1<br/>                           |
| Bibliothèque de types<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |
| IID<br/>                      | IMsTscAxEvents est défini en tant que 336d5562-efa8-482e-8cb3-c5c0fc7a7db6<br/>           |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IMsTscAxEvents**](imstscaxevents-interface.md)
</dt> </dl>

 

 





