---
title: IMsRdpClientNonScriptable3 propriété RedirectDynamicDrives
description: Spécifie ou récupère si les lecteurs PnP (Plug-and-Play attachés dynamiquement) qui sont énumérés dans une session sont disponibles pour la redirection.
ms.assetid: 11eb19fc-9711-4293-8054-f7975dadb492
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la propriété RedirectDynamicDrives
- Services Bureau à distance de la propriété RedirectDynamicDrives, interface IMsRdpClientNonScriptable3
- Services Bureau à distance de l’interface IMsRdpClientNonScriptable3, propriété RedirectDynamicDrives
- Services Bureau à distance de la propriété RedirectDynamicDrives, interface IMsRdpClientNonScriptable4
- Services Bureau à distance de l’interface IMsRdpClientNonScriptable4, propriété RedirectDynamicDrives
- Services Bureau à distance de la propriété RedirectDynamicDrives, interface IMsRdpClientNonScriptable5
- Services Bureau à distance de l’interface IMsRdpClientNonScriptable5, propriété RedirectDynamicDrives
- Services Bureau à distance de la propriété RedirectDynamicDrives, objet MsRdpClient5
- Services Bureau à distance objet MsRdpClient5, propriété RedirectDynamicDrives
- Services Bureau à distance de la propriété RedirectDynamicDrives, objet MsRdpClient6
- Services Bureau à distance objet MsRdpClient6, propriété RedirectDynamicDrives
- Services Bureau à distance de la propriété RedirectDynamicDrives, objet MsRdpClient7
- Services Bureau à distance objet MsRdpClient7, propriété RedirectDynamicDrives
- Services Bureau à distance de la propriété RedirectDynamicDrives, objet MsRdpClient8
- Services Bureau à distance objet MsRdpClient8, propriété RedirectDynamicDrives
- Services Bureau à distance de la propriété RedirectDynamicDrives, objet MsRdpClient9
- Services Bureau à distance objet MsRdpClient9, propriété RedirectDynamicDrives
topic_type:
- apiref
api_name:
- IMsRdpClientNonScriptable3.RedirectDynamicDrives
- IMsRdpClientNonScriptable3.get_RedirectDynamicDrives
- IMsRdpClientNonScriptable3.put_RedirectDynamicDrives
- IMsRdpClientNonScriptable4.RedirectDynamicDrives
- IMsRdpClientNonScriptable4.get_RedirectDynamicDrives
- IMsRdpClientNonScriptable4.put_RedirectDynamicDrives
- IMsRdpClientNonScriptable5.RedirectDynamicDrives
- IMsRdpClientNonScriptable5.get_RedirectDynamicDrives
- IMsRdpClientNonScriptable5.put_RedirectDynamicDrives
- MsRdpClient5.RedirectDynamicDrives
- MsRdpClient6.RedirectDynamicDrives
- MsRdpClient7.RedirectDynamicDrives
- MsRdpClient8.RedirectDynamicDrives
- MsRdpClient9.RedirectDynamicDrives
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5199f8fcf8e114cfb8febd05631e49de97aab01a69ca9397bc7d15539ad819d6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119001102"
---
# <a name="imsrdpclientnonscriptable3redirectdynamicdrives-property"></a>IMsRdpClientNonScriptable3 :: RedirectDynamicDrives, propriété

Spécifie ou récupère si les lecteurs PnP (Plug-and-Play attachés dynamiquement) qui sont énumérés dans une session sont disponibles pour la redirection.

Cette propriété est en lecture/écriture.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT put_RedirectDynamicDrives(
  [in]  VARIANT_BOOL fRedirectDynamicDrives
);

HRESULT get_RedirectDynamicDrives(
  [out] VARIANT_BOOL *pfRedirectDynamicDrives
);
```



## <a name="property-value"></a>Valeur de la propriété

Spécifie si les lecteurs PnP attachés de manière dynamique et qui sont énumérés dans une session sont disponibles pour la redirection.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Vista<br/>                                                                      |
| Serveur minimal pris en charge<br/> | Windows Server 2008<br/>                                                                |
| Bibliothèque de types<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>        |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>        |
| IID<br/>                      | IID \_ IMsRdpClientNonScriptable3 est défini en tant que b3378d90-0728-45c7-8ed7-b6159fb92219<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IMsRdpClientNonScriptable4**](imsrdpclientnonscriptable4.md)
</dt> <dt>

[**IMsRdpClientNonScriptable5**](imsrdpclientnonscriptable5.md)
</dt> <dt>

[**IMsRdpClientNonScriptable3**](imsrdpclientnonscriptable3.md)
</dt> </dl>

 

 





