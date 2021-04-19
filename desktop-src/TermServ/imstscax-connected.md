---
title: Propriété Connected IMsTscAx (Tsvirtualchannels. h)
description: Récupère l’état de connexion du contrôle actuel.
ms.assetid: f6f65ef6-d321-4362-b192-1ea5ffd2b712
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de propriété connectée
- Services Bureau à distance de propriété connected, interface IMsTscAx
- Services Bureau à distance de l’interface IMsTscAx, propriété connectée
- Services Bureau à distance de propriété connected, interface IMsRdpClient
- Services Bureau à distance de l’interface IMsRdpClient, propriété connectée
- Services Bureau à distance de propriété connected, interface IMsRdpClient2
- Services Bureau à distance de l’interface IMsRdpClient2, propriété connectée
- Services Bureau à distance de propriété connected, interface IMsRdpClient3
- Services Bureau à distance de l’interface IMsRdpClient3, propriété connectée
- Services Bureau à distance de propriété connected, interface IMsRdpClient4
- Services Bureau à distance de l’interface IMsRdpClient4, propriété connectée
- Services Bureau à distance de propriété connected, interface IMsRdpClient5
- Services Bureau à distance de l’interface IMsRdpClient5, propriété connectée
- Services Bureau à distance de propriété connected, interface IMsRdpClient6
- Services Bureau à distance de l’interface IMsRdpClient6, propriété connectée
- Services Bureau à distance de propriété connected, interface IMsRdpClient7
- Services Bureau à distance de l’interface IMsRdpClient7, propriété connectée
- Services Bureau à distance de propriété connected, interface IMsRdpClient8
- Services Bureau à distance de l’interface IMsRdpClient8, propriété connectée
- Services Bureau à distance de propriété connected, interface IMsRdpClient9
- Services Bureau à distance de l’interface IMsRdpClient9, propriété connectée
topic_type:
- apiref
api_name:
- IMsTscAx.Connected
- IMsTscAx.get_Connected
- IMsRdpClient.Connected
- IMsRdpClient.get_Connected
- IMsRdpClient2.Connected
- IMsRdpClient2.get_Connected
- IMsRdpClient3.Connected
- IMsRdpClient3.get_Connected
- IMsRdpClient4.Connected
- IMsRdpClient4.get_Connected
- IMsRdpClient5.Connected
- IMsRdpClient5.get_Connected
- IMsRdpClient6.Connected
- IMsRdpClient6.get_Connected
- IMsRdpClient7.Connected
- IMsRdpClient7.get_Connected
- IMsRdpClient8.Connected
- IMsRdpClient8.get_Connected
- IMsRdpClient9.Connected
- IMsRdpClient9.get_Connected
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 883ba670ab9a6b5d4e4a065c35f263734929ba02
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106543428"
---
# <a name="imstscaxconnected-property"></a>IMsTscAx :: connected, propriété

Récupère l’état de connexion du contrôle actuel.

Cette propriété est en lecture seule.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT get_Connected(
  [out] short *pIsConnected
);
```



## <a name="property-value"></a>Valeur de la propriété

Indique l’état de la connexion du contrôle. Il peut s’agir de l’une des valeurs suivantes.

<dt>

0
</dt> <dd>

Le contrôle n’est pas connecté.

</dd> <dt>

1
</dt> <dd>

Le contrôle est connecté.

</dd> <dt>

2
</dt> <dd>

Le contrôle établit une connexion.

</dd> </dl>

## <a name="error-codes"></a>Codes d’erreur

Retourne **S \_ OK** en cas de réussite.

## <a name="remarks"></a>Notes

La meilleure façon de déterminer l’état de la connexion du contrôle consiste à répondre aux événements de connexion dans [**IMsTscAxEvents**](imstscaxevents-interface.md).

Pour plus d’informations sur la Connexion Bureau à distance par le Web, consultez [Requirements for connexion Bureau à distance par le Web](requirements-for-remote-desktop-web-connection.md).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Vista<br/>                                                                       |
| Serveur minimal pris en charge<br/> | Windows Server 2008<br/>                                                                 |
| En-tête<br/>                   | <dl> <dt>Tsvirtualchannels. h</dt> </dl> |
| Bibliothèque de types<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>         |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>         |
| IID<br/>                      | IID \_ IMsTscAx est défini en tant que 8C11EFAE-92C3-11D1-BC1E-00C04FA31489<br/>                    |



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

[**IMsTscAx**](imstscax-interface.md)
</dt> </dl>

 

 





