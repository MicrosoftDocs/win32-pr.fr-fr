---
title: Méthode IMsRdpClient SetVirtualChannelOptions
description: définit les options de canal virtuel pour le contrôle de ActiveX Bureau à distance.
ms.assetid: c74c3917-5766-4d5b-8458-b051eb91cb28
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode SetVirtualChannelOptions
- Méthode SetVirtualChannelOptions Services Bureau à distance, interface IMsRdpClient
- Services Bureau à distance de l’interface IMsRdpClient, méthode SetVirtualChannelOptions
- Méthode SetVirtualChannelOptions Services Bureau à distance, interface IMsRdpClient2
- Services Bureau à distance de l’interface IMsRdpClient2, méthode SetVirtualChannelOptions
- Méthode SetVirtualChannelOptions Services Bureau à distance, interface IMsRdpClient3
- Services Bureau à distance de l’interface IMsRdpClient3, méthode SetVirtualChannelOptions
- Méthode SetVirtualChannelOptions Services Bureau à distance, interface IMsRdpClient4
- Services Bureau à distance de l’interface IMsRdpClient4, méthode SetVirtualChannelOptions
- Méthode SetVirtualChannelOptions Services Bureau à distance, interface IMsRdpClient5
- Services Bureau à distance de l’interface IMsRdpClient5, méthode SetVirtualChannelOptions
- Méthode SetVirtualChannelOptions Services Bureau à distance, interface IMsRdpClient6
- Services Bureau à distance de l’interface IMsRdpClient6, méthode SetVirtualChannelOptions
- Méthode SetVirtualChannelOptions Services Bureau à distance, interface IMsRdpClient7
- Services Bureau à distance de l’interface IMsRdpClient7, méthode SetVirtualChannelOptions
- Méthode SetVirtualChannelOptions Services Bureau à distance, interface IMsRdpClient8
- Services Bureau à distance de l’interface IMsRdpClient8, méthode SetVirtualChannelOptions
- Méthode SetVirtualChannelOptions Services Bureau à distance, interface IMsRdpClient9
- Services Bureau à distance de l’interface IMsRdpClient9, méthode SetVirtualChannelOptions
- Méthode SetVirtualChannelOptions Services Bureau à distance, interface IMsRdpClient10
- Services Bureau à distance de l’interface IMsRdpClient10, méthode SetVirtualChannelOptions
topic_type:
- apiref
api_name:
- IMsRdpClient.SetVirtualChannelOptions
- IMsRdpClient2.SetVirtualChannelOptions
- IMsRdpClient3.SetVirtualChannelOptions
- IMsRdpClient4.SetVirtualChannelOptions
- IMsRdpClient5.SetVirtualChannelOptions
- IMsRdpClient6.SetVirtualChannelOptions
- IMsRdpClient7.SetVirtualChannelOptions
- IMsRdpClient8.SetVirtualChannelOptions
- IMsRdpClient9.SetVirtualChannelOptions
- IMsRdpClient10.SetVirtualChannelOptions
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 804d4bde2fec9cb6273cc78f79d733f61a08772746439aa1cbb6e7b2d3c29716
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119871580"
---
# <a name="imsrdpclientsetvirtualchanneloptions-method"></a>IMsRdpClient :: SetVirtualChannelOptions, méthode

définit les options de canal virtuel pour le contrôle de ActiveX Bureau à distance.

appelez cette méthode après avoir appelé la méthode [**CreateVirtualChannels**](imstscax-createvirtualchannels.md) , mais avant d’établir une connexion à l’aide de la méthode [**Connecter**](imstscax-connect.md) . Cette méthode définit des options supplémentaires sur les canaux virtuels qui ont été créés avec **CreateVirtualChannels**.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT SetVirtualChannelOptions(
  [in] BSTR ChanName,
  [in] LONG chanOptions
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*ChanName* \[ dans\]
</dt> <dd>

Nom du canal virtuel qui a été spécifié dans l’appel à la méthode [**CreateVirtualChannels**](imstscax-createvirtualchannels.md) .

</dd> <dt>

*chanOptions* \[ dans\]
</dt> <dd>

Options à définir pour le canal virtuel spécifié par le paramètre *ChanName* . Pour obtenir une description des options possibles, consultez la page [**\_ définition de canal**](/windows/desktop/api/Pchannel/ns-pchannel-tagchannel_def). Pour plus d'informations, consultez la section Notes qui suit.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne **S \_ OK** en cas de réussite.

## <a name="remarks"></a>Remarques

Un exemple d’utilisation de cette méthode serait de déclarer le canal comme un contrôle à distance persistant en définissant l' **option de canal indicateur \_ \_ \_ \_ permanent de contrôle à distance** . Cela signifie que le canal n’est pas fermé lorsqu’un contrôle à distance se connecte à ou se déconnecte de la session connectée au client. Pour plus d’informations, consultez [contrôle à distance des canaux virtuels persistants](remote-control-persistent-virtual-channels.md).

Pour plus d’informations sur la Connexion Bureau à distance par le Web, consultez [Requirements for connexion Bureau à distance par le Web](requirements-for-remote-desktop-web-connection.md).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Vista<br/>                                                               |
| Serveur minimal pris en charge<br/> | Windows Server 2008<br/>                                                         |
| Bibliothèque de types<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |
| IID<br/>                      | IID \_ IMsRdpClient est défini en tant que 92b4a539-7115-4b7c-a5a9-e5d9efc2780a<br/>        |



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

[**IMsRdpClient10**](imsrdpclient10.md)
</dt> <dt>

[**définition de canal \_**](/windows/desktop/api/Pchannel/ns-pchannel-tagchannel_def)
</dt> <dt>

[**CreateVirtualChannels**](imstscax-createvirtualchannels.md)
</dt> <dt>

[**GetVirtualChannelOptions**](imsrdpclient-getvirtualchanneloptions.md)
</dt> </dl>

 

 





