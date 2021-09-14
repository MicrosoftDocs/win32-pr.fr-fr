---
title: Propriété fullscreen IMsTscSecuredSettings
description: Spécifie l’État plein écran du contrôle client.
ms.assetid: f65c2fa3-b2d0-4e64-bf1e-08394c91eda8
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de propriété fullscreen
- Services Bureau à distance de propriété fullscreen, interface IMsTscSecuredSettings
- Services Bureau à distance de l’interface IMsTscSecuredSettings, propriété fullscreen
- Services Bureau à distance de propriété fullscreen, interface IMsRdpClientSecuredSettings
- Services Bureau à distance de l’interface IMsRdpClientSecuredSettings, propriété fullscreen
topic_type:
- apiref
api_name:
- IMsTscSecuredSettings.Fullscreen
- IMsTscSecuredSettings.get_Fullscreen
- IMsTscSecuredSettings.put_Fullscreen
- IMsRdpClientSecuredSettings.Fullscreen
- IMsRdpClientSecuredSettings.get_Fullscreen
- IMsRdpClientSecuredSettings.put_Fullscreen
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 22c3b3208edf3476fcd110d7729d97d9817cb929
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127118665"
---
# <a name="imstscsecuredsettingsfullscreen-property"></a>IMsTscSecuredSettings :: fullscreen, propriété

Spécifie l’État plein écran du contrôle client.

Cette propriété est en lecture/écriture.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT put_Fullscreen(
  [in]  BOOL fFullScreen
);

HRESULT get_Fullscreen(
  [out] BOOL *pfFullScreen
);
```



## <a name="property-value"></a>Valeur de la propriété

Affectez la valeur **true** à ce paramètre si le contrôle doit utiliser le mode plein écran et **false** dans le cas contraire.

## <a name="error-codes"></a>Codes d’erreur

Retourne **S \_ OK** en cas de réussite.

## <a name="remarks"></a>Notes

Pour plus d’informations sur cette méthode, consultez la page [fourniture de la sécurité du client RDP](providing-for-rdp-client-security.md).

Pour plus d’informations sur la Connexion Bureau à distance par le Web, consultez [Requirements for connexion Bureau à distance par le Web](requirements-for-remote-desktop-web-connection.md).

Notez que, bien que l’utilisation de cette propriété soit limitée aux zones de sécurité des URL d’Internet Explorer autorisées, un utilisateur peut toujours passer en mode plein écran après l’établissement de la connexion en appuyant sur la combinaison de [touches de raccourci](terminal-services-shortcut-keys.md) du mode plein écran (Ctrl + Alt + Attn).

Cette méthode peut être appelée pendant l’établissement de la connexion cliente.

Vous devez appeler la méthode [**IMsRdpClientNonScriptable3 ::p ut \_ ConnectionBarText**](imsrdpclientnonscriptable3-connectionbartext.md) avant d’appeler la méthode **IMsTscSecuredSettings ::P ut \_ fullscreen** ou [**IMsRdpClient ::p ut \_ fullscreen**](imsrdpclient-fullscreen.md) .

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Vista<br/>                                                                 |
| Serveur minimal pris en charge<br/> | Windows Server 2008<br/>                                                           |
| Bibliothèque de types<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>   |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>   |
| IID<br/>                      | IID \_ IMsTscSecuredSettings est défini en tant que c9d65442-A0F9-45b2-8f73-d61d2db8cbb6<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IMsRdpClientSecuredSettings**](imsrdpclientsecuredsettings-interface.md)
</dt> <dt>

[**IMsTscSecuredSettings**](imstscsecuredsettings-interface.md)
</dt> </dl>

 

 





