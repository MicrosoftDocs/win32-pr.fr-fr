---
title: Méthode IMsTscAx CreateVirtualChannels
description: Crée un objet de canal virtuel côté client pour chaque nom de canal virtuel spécifié.
ms.assetid: 3afd2f1c-abd5-4f85-93fb-6d1173f09b07
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode CreateVirtualChannels
- Méthode CreateVirtualChannels Services Bureau à distance, interface IMsTscAx
- Services Bureau à distance de l’interface IMsTscAx, méthode CreateVirtualChannels
- Méthode CreateVirtualChannels Services Bureau à distance, interface IMsRdpClient
- Services Bureau à distance de l’interface IMsRdpClient, méthode CreateVirtualChannels
- Méthode CreateVirtualChannels Services Bureau à distance, interface IMsRdpClient2
- Services Bureau à distance de l’interface IMsRdpClient2, méthode CreateVirtualChannels
- Méthode CreateVirtualChannels Services Bureau à distance, interface IMsRdpClient3
- Services Bureau à distance de l’interface IMsRdpClient3, méthode CreateVirtualChannels
- Méthode CreateVirtualChannels Services Bureau à distance, interface IMsRdpClient4
- Services Bureau à distance de l’interface IMsRdpClient4, méthode CreateVirtualChannels
- Méthode CreateVirtualChannels Services Bureau à distance, interface IMsRdpClient5
- Services Bureau à distance de l’interface IMsRdpClient5, méthode CreateVirtualChannels
- Méthode CreateVirtualChannels Services Bureau à distance, interface IMsRdpClient6
- Services Bureau à distance de l’interface IMsRdpClient6, méthode CreateVirtualChannels
- Méthode CreateVirtualChannels Services Bureau à distance, interface IMsRdpClient7
- Services Bureau à distance de l’interface IMsRdpClient7, méthode CreateVirtualChannels
- Méthode CreateVirtualChannels Services Bureau à distance, interface IMsRdpClient8
- Services Bureau à distance de l’interface IMsRdpClient8, méthode CreateVirtualChannels
- Méthode CreateVirtualChannels Services Bureau à distance, interface IMsRdpClient9
- Services Bureau à distance de l’interface IMsRdpClient9, méthode CreateVirtualChannels
topic_type:
- apiref
api_name:
- IMsTscAx.CreateVirtualChannels
- IMsRdpClient.CreateVirtualChannels
- IMsRdpClient2.CreateVirtualChannels
- IMsRdpClient3.CreateVirtualChannels
- IMsRdpClient4.CreateVirtualChannels
- IMsRdpClient5.CreateVirtualChannels
- IMsRdpClient6.CreateVirtualChannels
- IMsRdpClient7.CreateVirtualChannels
- IMsRdpClient8.CreateVirtualChannels
- IMsRdpClient9.CreateVirtualChannels
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8d3ef4e7c8471c655d4ecfaf54a1c4b0f35b2362c67c334bd94e57da8e99d390
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119138482"
---
# <a name="imstscaxcreatevirtualchannels-method"></a>IMsTscAx :: CreateVirtualChannels, méthode

Crée un objet de canal virtuel côté client pour chaque nom de canal virtuel spécifié.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT CreateVirtualChannels(
  [in] BSTR newVal
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*newVal* \[ dans\]
</dt> <dd>

Liste séparée par des virgules de noms de canaux virtuels valides. La longueur de chaque nom de cette liste peut être au minimum un et un maximum de sept caractères alphabétiques. La longueur de la chaîne entière peut être au minimum un et un maximum de 300 caractères alphabétiques.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne **S \_ OK** en cas de réussite. Retourne **E \_ INVALIDARG** si le paramètre passé ne répond pas aux critères spécifiés.

## <a name="remarks"></a>Remarques

appelez cette méthode avant d’appeler la méthode [**Connecter**](imstscax-connect.md) .

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

[**IMsTscAx**](imstscax-interface.md)
</dt> </dl>

 

 





