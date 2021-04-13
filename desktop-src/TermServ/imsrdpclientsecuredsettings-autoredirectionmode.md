---
title: IMsRdpClientSecuredSettings propriété AudioRedirectionMode
description: Spécifie les paramètres de redirection audio, qui spécifient s’il faut rediriger les sons ou lire des sons sur le serveur hôte de session Bureau à distance (hôte de session Bureau à distance).
ms.assetid: 6aa63a50-a714-4a9b-a4ec-c0551920467a
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la propriété AudioRedirectionMode
- Services Bureau à distance de la propriété AudioRedirectionMode, interface IMsRdpClientSecuredSettings
- Services Bureau à distance de l’interface IMsRdpClientSecuredSettings, propriété AudioRedirectionMode
topic_type:
- apiref
api_name:
- IMsRdpClientSecuredSettings.AudioRedirectionMode
- IMsRdpClientSecuredSettings.get_AudioRedirectionMode
- IMsRdpClientSecuredSettings.put_AudioRedirectionMode
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 858342811ec97def95031ebed0605b5a81cf80fc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104519226"
---
# <a name="imsrdpclientsecuredsettingsaudioredirectionmode-property"></a>IMsRdpClientSecuredSettings :: AudioRedirectionMode, propriété

Spécifie les paramètres de redirection audio, qui spécifient s’il faut rediriger les sons ou lire des sons sur le serveur hôte de session Bureau à distance (hôte de session Bureau à distance).

Cette propriété est en lecture/écriture.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT put_AudioRedirectionMode(
  [in]  LONG audioRedirectionMode
);

HRESULT get_AudioRedirectionMode(
  [out] LONG *paudioRedirectionMode
);
```



## <a name="property-value"></a>Valeur de la propriété

Nouveaux paramètres. Ce paramètre peut prendre les valeurs suivantes.

<dt>

0
</dt> <dd>

Rediriger les sons vers le client. Il s’agit de la valeur par défaut.

</dd> <dt>

1
</dt> <dd>

Émettre des sons sur l’ordinateur distant.

</dd> <dt>

2
</dt> <dd>

Désactiver la redirection du son ; ne lisez pas les sons sur le serveur.

</dd> </dl>

## <a name="error-codes"></a>Codes d’erreur

Retourne **S \_ OK** en cas de réussite.

## <a name="remarks"></a>Notes

Ces propriétés ne peuvent pas être définies lorsque le contrôle est connecté.

Pour plus d’informations, consultez la rubrique [fourniture de la sécurité du client RDP](providing-for-rdp-client-security.md) .

Pour plus d’informations sur la Connexion Bureau à distance par le Web, consultez [Requirements for connexion Bureau à distance par le Web](requirements-for-remote-desktop-web-connection.md).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Vista<br/>                                                                       |
| Serveur minimal pris en charge<br/> | Windows Server 2008<br/>                                                                 |
| Bibliothèque de types<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>         |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>         |
| IID<br/>                      | IID \_ IMsRdpClientSecuredSettings est défini en tant que 605befcf-39c1-45cc-A811-068fb7be346d<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IMsRdpClientSecuredSettings**](imsrdpclientsecuredsettings-interface.md)
</dt> </dl>

 

 





