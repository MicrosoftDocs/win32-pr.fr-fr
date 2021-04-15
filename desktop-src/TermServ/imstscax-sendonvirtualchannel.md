---
title: Méthode IMsTscAx SendOnVirtualChannel
description: Envoie des données au serveur de l’hôte de session Bureau à distance (hôte de session Bureau à distance) sur un canal virtuel qui a été créé précédemment à l’aide de la méthode CreateVirtualChannels.
ms.assetid: 795ef508-bdf7-4897-84b1-931615262293
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode SendOnVirtualChannel
- Méthode SendOnVirtualChannel Services Bureau à distance, interface IMsTscAx
- Services Bureau à distance de l’interface IMsTscAx, méthode SendOnVirtualChannel
- Méthode SendOnVirtualChannel Services Bureau à distance, interface IMsRdpClient
- Services Bureau à distance de l’interface IMsRdpClient, méthode SendOnVirtualChannel
- Méthode SendOnVirtualChannel Services Bureau à distance, interface IMsRdpClient2
- Services Bureau à distance de l’interface IMsRdpClient2, méthode SendOnVirtualChannel
- Méthode SendOnVirtualChannel Services Bureau à distance, interface IMsRdpClient3
- Services Bureau à distance de l’interface IMsRdpClient3, méthode SendOnVirtualChannel
- Méthode SendOnVirtualChannel Services Bureau à distance, interface IMsRdpClient4
- Services Bureau à distance de l’interface IMsRdpClient4, méthode SendOnVirtualChannel
- Méthode SendOnVirtualChannel Services Bureau à distance, interface IMsRdpClient5
- Services Bureau à distance de l’interface IMsRdpClient5, méthode SendOnVirtualChannel
- Méthode SendOnVirtualChannel Services Bureau à distance, interface IMsRdpClient6
- Services Bureau à distance de l’interface IMsRdpClient6, méthode SendOnVirtualChannel
- Méthode SendOnVirtualChannel Services Bureau à distance, interface IMsRdpClient7
- Services Bureau à distance de l’interface IMsRdpClient7, méthode SendOnVirtualChannel
- Méthode SendOnVirtualChannel Services Bureau à distance, interface IMsRdpClient8
- Services Bureau à distance de l’interface IMsRdpClient8, méthode SendOnVirtualChannel
- Méthode SendOnVirtualChannel Services Bureau à distance, interface IMsRdpClient9
- Services Bureau à distance de l’interface IMsRdpClient9, méthode SendOnVirtualChannel
topic_type:
- apiref
api_name:
- IMsTscAx.SendOnVirtualChannel
- IMsRdpClient.SendOnVirtualChannel
- IMsRdpClient2.SendOnVirtualChannel
- IMsRdpClient3.SendOnVirtualChannel
- IMsRdpClient4.SendOnVirtualChannel
- IMsRdpClient5.SendOnVirtualChannel
- IMsRdpClient6.SendOnVirtualChannel
- IMsRdpClient7.SendOnVirtualChannel
- IMsRdpClient8.SendOnVirtualChannel
- IMsRdpClient9.SendOnVirtualChannel
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c1371ae17978601a3194f755dd364d9227b8fc28
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464571"
---
# <a name="imstscaxsendonvirtualchannel-method"></a>IMsTscAx :: SendOnVirtualChannel, méthode

Envoie des données au serveur de l’hôte de session Bureau à distance (hôte de session Bureau à distance) sur un canal virtuel qui a été créé précédemment à l’aide de la méthode [**CreateVirtualChannels**](imstscax-createvirtualchannels.md) .

## <a name="syntax"></a>Syntaxe


```C++
HRESULT SendOnVirtualChannel(
  [in] BSTR ChanName,
  [in] BSTR ChanData
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*ChanName* \[ dans\]
</dt> <dd>

Nom du canal virtuel qui a été spécifié dans l’appel à [**CreateVirtualChannels**](imstscax-createvirtualchannels.md).

</dd> <dt>

*ChanData* \[ dans\]
</dt> <dd>

Données à envoyer sur le canal virtuel, sous forme **BSTR** . Il n’existe aucune restriction indiquant que ces données doivent être des chaînes terminées par le caractère null.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne **S \_ OK** en cas de réussite.

## <a name="remarks"></a>Notes

Pour plus d’informations sur les restrictions de nom de canal virtuel, consultez [inscription du client du canal virtuel](virtual-channel-client-registration.md) .

Pour plus d’informations sur la Connexion Bureau à distance par le Web, consultez [Requirements for connexion Bureau à distance par le Web](requirements-for-remote-desktop-web-connection.md).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Vista<br/>                                                               |
| Serveur minimal pris en charge<br/> | Windows Server 2008<br/>                                                         |
| Bibliothèque de types<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |
| IID<br/>                      | IID \_ IMsTscAx est défini en tant que 8C11EFAE-92C3-11D1-BC1E-00C04FA31489<br/>            |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IMsRdpClient**](imsrdpclient-interface.md)
</dt> <dt>

[**IMsRdpClient2**](imsrdpclient2.md)
</dt> <dt>

[**IMsRdpClient3**](imsrdpclient3.md)
</dt> <dt>

[**IMsRdpClient4**](imsrdpclient4.md)
</dt> <dt>

[**IMsRdpClient5**](imsrdpclient5.md)
</dt> <dt>

[**IMsRdpClient6**](imsrdpclient6.md)
</dt> <dt>

[**IMsRdpClient7**](imsrdpclient7.md)
</dt> <dt>

[**IMsRdpClient8**](imsrdpclient8.md)
</dt> <dt>

[**IMsRdpClient9**](imsrdpclient9.md)
</dt> <dt>

[**CreateVirtualChannels**](imstscax-createvirtualchannels.md)
</dt> <dt>

[**IMsTscAx**](imstscax-interface.md)
</dt> </dl>

 

 





