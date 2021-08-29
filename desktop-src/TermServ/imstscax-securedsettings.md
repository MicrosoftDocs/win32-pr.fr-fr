---
title: IMsTscAx propriété SecuredSettings
description: Récupère un pointeur d’interface IMsTscSecuredSettings.
ms.assetid: 64d4059b-e617-449d-a733-c19c1d281132
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la propriété SecuredSettings
- Services Bureau à distance de la propriété SecuredSettings, interface IMsTscAx
- Services Bureau à distance de l’interface IMsTscAx, propriété SecuredSettings
- Services Bureau à distance de la propriété SecuredSettings, interface IMsRdpClient
- Services Bureau à distance de l’interface IMsRdpClient, propriété SecuredSettings
- Services Bureau à distance de la propriété SecuredSettings, interface IMsRdpClient2
- Services Bureau à distance de l’interface IMsRdpClient2, propriété SecuredSettings
- Services Bureau à distance de la propriété SecuredSettings, interface IMsRdpClient3
- Services Bureau à distance de l’interface IMsRdpClient3, propriété SecuredSettings
- Services Bureau à distance de la propriété SecuredSettings, interface IMsRdpClient4
- Services Bureau à distance de l’interface IMsRdpClient4, propriété SecuredSettings
- Services Bureau à distance de la propriété SecuredSettings, interface IMsRdpClient5
- Services Bureau à distance de l’interface IMsRdpClient5, propriété SecuredSettings
- Services Bureau à distance de la propriété SecuredSettings, interface IMsRdpClient6
- Services Bureau à distance de l’interface IMsRdpClient6, propriété SecuredSettings
- Services Bureau à distance de la propriété SecuredSettings, interface IMsRdpClient7
- Services Bureau à distance de l’interface IMsRdpClient7, propriété SecuredSettings
- Services Bureau à distance de la propriété SecuredSettings, interface IMsRdpClient8
- Services Bureau à distance de l’interface IMsRdpClient8, propriété SecuredSettings
- Services Bureau à distance de la propriété SecuredSettings, interface IMsRdpClient9
- Services Bureau à distance de l’interface IMsRdpClient9, propriété SecuredSettings
topic_type:
- apiref
api_name:
- IMsTscAx.SecuredSettings
- IMsTscAx.get_SecuredSettings
- IMsRdpClient.SecuredSettings
- IMsRdpClient.get_SecuredSettings
- IMsRdpClient2.SecuredSettings
- IMsRdpClient2.get_SecuredSettings
- IMsRdpClient3.SecuredSettings
- IMsRdpClient3.get_SecuredSettings
- IMsRdpClient4.SecuredSettings
- IMsRdpClient4.get_SecuredSettings
- IMsRdpClient5.SecuredSettings
- IMsRdpClient5.get_SecuredSettings
- IMsRdpClient6.SecuredSettings
- IMsRdpClient6.get_SecuredSettings
- IMsRdpClient7.SecuredSettings
- IMsRdpClient7.get_SecuredSettings
- IMsRdpClient8.SecuredSettings
- IMsRdpClient8.get_SecuredSettings
- IMsRdpClient9.SecuredSettings
- IMsRdpClient9.get_SecuredSettings
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d4f43a089092919124ed3031bafd12a70af1e1ffa0850bf058a91cc9dfd66125
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119771089"
---
# <a name="imstscaxsecuredsettings-property"></a>IMsTscAx :: SecuredSettings, propriété

Récupère un pointeur d’interface [**IMsTscSecuredSettings**](imstscsecuredsettings-interface.md) .

Cette propriété est en lecture seule.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT get_SecuredSettings(
  [out] IMsTscSecuredSettings **ppSecuredSettings
);
```



## <a name="property-value"></a>Valeur de la propriété

Pointeur d’interface [**IMsTscSecuredSettings**](imstscsecuredsettings-interface.md) .

## <a name="error-codes"></a>Codes d’erreur

Retourne **S \_ OK** en cas de réussite.

## <a name="remarks"></a>Remarques

Si le contrôle est hébergé dans une page Web et que la zone de sécurité URL d’Internet Explorer actuelle n’autorise pas la récupération de l’adresse de l’interface, cette méthode retourne **E \_ Fail**.

Reportez-vous à [**SecuredSettingsEnabled**](imstscax-securedsettingsenabled.md) pour des restrictions sur la disponibilité de l’interface [**IMsTscSecuredSettings**](imstscsecuredsettings-interface.md) .

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
</dt> <dt>

[**IMsTscSecuredSettings**](imstscsecuredsettings-interface.md)
</dt> </dl>

 

 





