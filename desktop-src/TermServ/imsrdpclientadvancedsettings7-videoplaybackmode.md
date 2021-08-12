---
title: IMsRdpClientAdvancedSettings7 propriété VideoPlaybackMode
description: Spécifie ou récupère une valeur qui indique le mode de lecture vidéo.
ms.assetid: 83f0baa3-3ac2-47ee-b106-5beaf60d73d2
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la propriété VideoPlaybackMode
- Services Bureau à distance de la propriété VideoPlaybackMode, interface IMsRdpClientAdvancedSettings7
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings7, propriété VideoPlaybackMode
- Services Bureau à distance de la propriété VideoPlaybackMode, interface IMsRdpClientAdvancedSettings8
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings8, propriété VideoPlaybackMode
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings7.VideoPlaybackMode
- IMsRdpClientAdvancedSettings7.get_VideoPlaybackMode
- IMsRdpClientAdvancedSettings7.put_VideoPlaybackMode
- IMsRdpClientAdvancedSettings8.VideoPlaybackMode
- IMsRdpClientAdvancedSettings8.get_VideoPlaybackMode
- IMsRdpClientAdvancedSettings8.put_VideoPlaybackMode
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 353cf72822ac91686cb5a08edf5ca6a5e25b24ff8e544ff79bdd8a2085f761fc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118607816"
---
# <a name="imsrdpclientadvancedsettings7videoplaybackmode-property"></a>IMsRdpClientAdvancedSettings7 :: VideoPlaybackMode, propriété

Spécifie ou récupère une valeur qui indique le mode de lecture vidéo.

Cette propriété est en lecture/écriture.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT put_VideoPlaybackMode(
  [in]          UINT videoPlaybackMode
);

HRESULT get_VideoPlaybackMode(
  [out, retval] UINT *pVideoPlaybackMode
);
```



## <a name="property-value"></a>Valeur de la propriété

Valeur qui spécifie le mode de lecture de la vidéo.

Les valeurs possibles sont les suivantes :

<dt>

1
</dt> <dd>

Mode de lecture vidéo par défaut. Lorsque le mode de lecture vidéo est défini sur cette valeur, la redirection vidéo est contrôlée par la propriété [**AudioRedirectionMode**](imsrdpclientsecuredsettings-autoredirectionmode.md) . Lorsque la propriété **AudioRedirectionMode** est définie sur **\_ \_ redirect mode audio**, la vidéo est décodée et rendue sur le client.

</dd> <dt>

0
</dt> <dd>

La redirection de lecture vidéo est désactivée, même si [**AudioRedirectionMode**](imsrdpclientsecuredsettings-autoredirectionmode.md) est défini sur **\_ \_ redirection audio mode**. Dans ce mode, la vidéo est décodée et rendue sur le serveur hôte de session Bureau à distance.

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 7<br/>                                                                             |
| Serveur minimal pris en charge<br/> | Windows Server 2008 R2<br/>                                                                |
| Bibliothèque de types<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>           |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>           |
| IID<br/>                      | IID \_ IMsRdpClientAdvancedSettings7 est défini en tant que 26036036-4010-4578-8091-0db9a1edf9c3<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IMsRdpClientAdvancedSettings8**](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings7**](imsrdpclientadvancedsettings7.md)
</dt> </dl>

 

 





