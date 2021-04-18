---
title: IMsTscAx propriété SecuredSettingsEnabled
description: Indique si l’interface IMsTscSecuredSettings est disponible. Autrement dit, si la page Web contenant le contrôle se trouve actuellement dans l’une des zones de sécurité d’URL Internet Explorer autorisées.
ms.assetid: 0747eab0-9d62-4c10-b02d-fc65ca2f752e
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la propriété SecuredSettingsEnabled
- Services Bureau à distance de la propriété SecuredSettingsEnabled, interface IMsTscAx
- Services Bureau à distance de l’interface IMsTscAx, propriété SecuredSettingsEnabled
- Services Bureau à distance de la propriété SecuredSettingsEnabled, interface IMsRdpClient
- Services Bureau à distance de l’interface IMsRdpClient, propriété SecuredSettingsEnabled
- Services Bureau à distance de la propriété SecuredSettingsEnabled, interface IMsRdpClient2
- Services Bureau à distance de l’interface IMsRdpClient2, propriété SecuredSettingsEnabled
- Services Bureau à distance de la propriété SecuredSettingsEnabled, interface IMsRdpClient3
- Services Bureau à distance de l’interface IMsRdpClient3, propriété SecuredSettingsEnabled
- Services Bureau à distance de la propriété SecuredSettingsEnabled, interface IMsRdpClient4
- Services Bureau à distance de l’interface IMsRdpClient4, propriété SecuredSettingsEnabled
- Services Bureau à distance de la propriété SecuredSettingsEnabled, interface IMsRdpClient5
- Services Bureau à distance de l’interface IMsRdpClient5, propriété SecuredSettingsEnabled
- Services Bureau à distance de la propriété SecuredSettingsEnabled, interface IMsRdpClient6
- Services Bureau à distance de l’interface IMsRdpClient6, propriété SecuredSettingsEnabled
- Services Bureau à distance de la propriété SecuredSettingsEnabled, interface IMsRdpClient7
- Services Bureau à distance de l’interface IMsRdpClient7, propriété SecuredSettingsEnabled
- Services Bureau à distance de la propriété SecuredSettingsEnabled, interface IMsRdpClient8
- Services Bureau à distance de l’interface IMsRdpClient8, propriété SecuredSettingsEnabled
- Services Bureau à distance de la propriété SecuredSettingsEnabled, interface IMsRdpClient9
- Services Bureau à distance de l’interface IMsRdpClient9, propriété SecuredSettingsEnabled
topic_type:
- apiref
api_name:
- IMsTscAx.SecuredSettingsEnabled
- IMsTscAx.get_SecuredSettingsEnabled
- IMsRdpClient.SecuredSettingsEnabled
- IMsRdpClient.get_SecuredSettingsEnabled
- IMsRdpClient2.SecuredSettingsEnabled
- IMsRdpClient2.get_SecuredSettingsEnabled
- IMsRdpClient3.SecuredSettingsEnabled
- IMsRdpClient3.get_SecuredSettingsEnabled
- IMsRdpClient4.SecuredSettingsEnabled
- IMsRdpClient4.get_SecuredSettingsEnabled
- IMsRdpClient5.SecuredSettingsEnabled
- IMsRdpClient5.get_SecuredSettingsEnabled
- IMsRdpClient6.SecuredSettingsEnabled
- IMsRdpClient6.get_SecuredSettingsEnabled
- IMsRdpClient7.SecuredSettingsEnabled
- IMsRdpClient7.get_SecuredSettingsEnabled
- IMsRdpClient8.SecuredSettingsEnabled
- IMsRdpClient8.get_SecuredSettingsEnabled
- IMsRdpClient9.SecuredSettingsEnabled
- IMsRdpClient9.get_SecuredSettingsEnabled
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: de0601ac64ab0ca55f3d92ec460861a4347f70b7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106511968"
---
# <a name="imstscaxsecuredsettingsenabled-property"></a>IMsTscAx :: SecuredSettingsEnabled, propriété

Indique si l’interface [**IMsTscSecuredSettings**](imstscsecuredsettings-interface.md) est disponible. Autrement dit, si la page Web contenant le contrôle se trouve actuellement dans l’une des zones de sécurité d’URL Internet Explorer autorisées.

Cette propriété est en lecture seule.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT get_SecuredSettingsEnabled(
  [out] BOOL *pSecuredSettingsEnabled
);
```



## <a name="property-value"></a>Valeur de la propriété

La valeur de ce paramètre est **true** si l’interface est disponible ; sinon, **false** .

## <a name="error-codes"></a>Codes d’erreur

Retourne **S \_ OK** en cas de réussite.

## <a name="remarks"></a>Notes

Utilisez cette méthode pour demander si l’interface [**IMsTscSecuredSettings**](imstscsecuredsettings-interface.md) est disponible avant de récupérer la propriété [**SecuredSettings**](imstscax-securedsettings.md) .

Pour obtenir la liste des zones de sécurité d’URL restreintes, consultez la rubrique [fourniture de RDP Client Security](providing-for-rdp-client-security.md) .

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

 

 





