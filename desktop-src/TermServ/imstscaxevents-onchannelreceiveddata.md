---
title: Méthode IMsTscAxEvents OnChannelReceivedData
description: Appelé lorsque le client reçoit des données sur un canal virtuel scriptable.
ms.assetid: 38e6c33c-6a79-4760-818e-445e33d8e0ec
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode OnChannelReceivedData
- Méthode OnChannelReceivedData Services Bureau à distance, interface IMsTscAxEvents
- Services Bureau à distance de l’interface IMsTscAxEvents, méthode OnChannelReceivedData
topic_type:
- apiref
api_name:
- IMsTscAxEvents.OnChannelReceivedData
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 72f411eae7e03f134f4adfd6fdc6108634e4e58c06bb8645e9f97f27e8489a3e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120125189"
---
# <a name="imstscaxeventsonchannelreceiveddata-method"></a>IMsTscAxEvents :: OnChannelReceivedData, méthode

Appelé lorsque le client reçoit des données sur un canal virtuel scriptable.

## <a name="syntax"></a>Syntaxe


```C++
void OnChannelReceivedData(
  [in] BSTR chanName,
  [in] BSTR data
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*chanName* \[ dans\]
</dt> <dd>

Nom du canal virtuel sur lequel les données ont été reçues. Ce nom correspond à l’un des canaux créés par l’appel à [**IMsTscAx :: CreateVirtualChannels**](imstscax-createvirtualchannels.md).

</dd> <dt>

*données* \[ dans\]
</dt> <dd>

Données reçues sur le canal virtuel scriptable.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode ne retourne pas de valeur.

## <a name="remarks"></a>Remarques

Pour plus d’informations sur cet événement, consultez [implémentation de canaux virtuels scriptables à l’aide de connexion Bureau à distance par le Web](implementing-scriptable-virtual-channels-using-remote-desktop-web-connection.md) .

Pour plus d’informations sur la Connexion Bureau à distance par le Web, consultez [Requirements for connexion Bureau à distance par le Web](requirements-for-remote-desktop-web-connection.md).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Vista<br/>                                                               |
| Serveur minimal pris en charge<br/> | Windows Server 2008<br/>                                                         |
| Bibliothèque de types<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |
| IID<br/>                      | IMsTscAxEvents est défini en tant que 336d5562-efa8-482e-8cb3-c5c0fc7a7db6<br/>           |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IMsTscAxEvents**](imstscaxevents-interface.md)
</dt> </dl>

 

 





