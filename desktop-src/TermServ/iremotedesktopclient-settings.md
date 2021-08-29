---
title: propriété Paramètres IRemoteDesktopClient
description: Récupère l’objet de paramètres pour le client de conteneur d’applications protocole RDP (Remote Desktop Protocol) (RDP).
ms.assetid: 59999489-9ad0-4b85-9643-3b8355b817c2
ms.tgt_platform: multiple
keywords:
- propriété Paramètres Services Bureau à distance
- Paramètres de propriété Services Bureau à distance, interface IRemoteDesktopClient
- Services Bureau à distance de l’interface IRemoteDesktopClient, Paramètres propriété
topic_type:
- apiref
api_name:
- IRemoteDesktopClient.Settings
- IRemoteDesktopClient.get_Settings
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3e6f3369948cb99e67a345348c79073109ff5a9f929a2ff09b1acb510930bb2a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120125019"
---
# <a name="iremotedesktopclientsettings-property"></a>IRemoteDesktopClient :: Paramètres, propriété

Récupère l’objet de paramètres pour le client de conteneur d’applications protocole RDP (Remote Desktop Protocol) (RDP).

Cette propriété est en lecture seule.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT get_Settings(
  [out, retval] IRemoteDesktopClientSettings **Settings
);
```



## <a name="property-value"></a>Valeur de la propriété

Objet de paramètres pour le client RDP.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 8<br/>                                                                    |
| Serveur minimal pris en charge<br/> | Windows Server 2012<br/>                                                          |
| Bibliothèque de types<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>  |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>  |
| IID<br/>                      | IID \_ IRemoteDesktopClient est défini en tant que 57D25668-625A-4905-BE4E-304CAA13F89C<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IRemoteDesktopClient**](/windows/win32/api/rdpappcontainerclient/nn-rdpappcontainerclient-iremotedesktopclient)
</dt> </dl>

 

