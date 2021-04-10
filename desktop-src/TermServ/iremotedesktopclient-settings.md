---
title: Propriété des paramètres IRemoteDesktopClient
description: Récupère l’objet de paramètres pour le client de conteneur d’applications protocole RDP (Remote Desktop Protocol) (RDP).
ms.assetid: 59999489-9ad0-4b85-9643-3b8355b817c2
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de propriétés de paramètres
- Propriété de paramètres Services Bureau à distance, interface IRemoteDesktopClient
- Services Bureau à distance de l’interface IRemoteDesktopClient, propriété de paramètres
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
ms.openlocfilehash: 45e84324eaa12610d7ab898cbcb181e7712bc021
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942412"
---
# <a name="iremotedesktopclientsettings-property"></a>IRemoteDesktopClient :: Settings, propriété

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

 

