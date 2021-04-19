---
title: Méthode IMsTscAxEvents OnNetworkStatusChanged
description: Appelé lorsque l’état du réseau a changé. | Méthode IMsTscAxEvents OnNetworkStatusChanged
ms.assetid: 177A410E-2449-4FC7-8DE5-21F83A6DD028
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode OnNetworkStatusChanged
- Méthode OnNetworkStatusChanged Services Bureau à distance, interface IMsTscAxEvents
- Services Bureau à distance de l’interface IMsTscAxEvents, méthode OnNetworkStatusChanged
topic_type:
- apiref
api_name:
- IMsTscAxEvents.OnNetworkStatusChanged
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c2b9bdcd7774493fcc54e1390ad199a6a56a7c51
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "106535760"
---
# <a name="imstscaxeventsonnetworkstatuschanged-method"></a>IMsTscAxEvents :: OnNetworkStatusChanged, méthode

Appelé lorsque l’état du réseau a changé.

## <a name="syntax"></a>Syntaxe


```C++
void OnNetworkStatusChanged(
  [in] ULONG qualityLevel,
  [in] LONG  bandwidth,
  [in] LONG  rtt
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*qualityLevel* \[ dans\]
</dt> <dd>

Spécifie la nouvelle vitesse de connexion. Il s’agit de l’une des valeurs suivantes.

<dt>

1
</dt> <dd>

Moins de 512 kilo-octets par seconde (Kbits/s).

</dd> <dt>

2
</dt> <dd>

de 512 à 1 999 KBps.

</dd> <dt>

3
</dt> <dd>

de 2 000 à 9 999 KBps.

</dd> <dt>

4
</dt> <dd>

Supérieur ou égal à 10 000 Kbits/s.

</dd> </dl> </dd> <dt>

*bande passante* \[ dans\]
</dt> <dd>

Spécifie la bande passante de la connexion.

</dd> <dt>

*RTT* \[ dans\]
</dt> <dd>

Spécifie la latence de la connexion.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode ne retourne pas de valeur.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 8<br/>                                                                   |
| Serveur minimal pris en charge<br/> | Windows Server 2012<br/>                                                         |
| Bibliothèque de types<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |
| IID<br/>                      | IMsTscAxEvents est défini en tant que 336d5562-efa8-482e-8cb3-c5c0fc7a7db6<br/>           |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IMsTscAxEvents**](imstscaxevents-interface.md)
</dt> </dl>

 

 





