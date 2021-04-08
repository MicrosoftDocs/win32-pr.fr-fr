---
title: IMsRdpClientNonScriptable3 propriété RedirectDynamicDevices
description: Spécifie ou récupère si les périphériques PnP (Plug-and-Play attachés dynamiquement) qui sont énumérés dans une session sont disponibles pour la redirection.
ms.assetid: 8cc5d6a4-108b-4505-8937-f6e790a5c2ba
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la propriété RedirectDynamicDevices
- Services Bureau à distance de la propriété RedirectDynamicDevices, interface IMsRdpClientNonScriptable3
- Services Bureau à distance de l’interface IMsRdpClientNonScriptable3, propriété RedirectDynamicDevices
- Services Bureau à distance de la propriété RedirectDynamicDevices, interface IMsRdpClientNonScriptable4
- Services Bureau à distance de l’interface IMsRdpClientNonScriptable4, propriété RedirectDynamicDevices
- Services Bureau à distance de la propriété RedirectDynamicDevices, interface IMsRdpClientNonScriptable5
- Services Bureau à distance de l’interface IMsRdpClientNonScriptable5, propriété RedirectDynamicDevices
- Services Bureau à distance de la propriété RedirectDynamicDevices, objet MsRdpClient5
- Services Bureau à distance objet MsRdpClient5, propriété RedirectDynamicDevices
- Services Bureau à distance de la propriété RedirectDynamicDevices, objet MsRdpClient6
- Services Bureau à distance objet MsRdpClient6, propriété RedirectDynamicDevices
- Services Bureau à distance de la propriété RedirectDynamicDevices, objet MsRdpClient7
- Services Bureau à distance objet MsRdpClient7, propriété RedirectDynamicDevices
- Services Bureau à distance de la propriété RedirectDynamicDevices, objet MsRdpClient8
- Services Bureau à distance objet MsRdpClient8, propriété RedirectDynamicDevices
- Services Bureau à distance de la propriété RedirectDynamicDevices, objet MsRdpClient9
- Services Bureau à distance objet MsRdpClient9, propriété RedirectDynamicDevices
topic_type:
- apiref
api_name:
- IMsRdpClientNonScriptable3.RedirectDynamicDevices
- IMsRdpClientNonScriptable3.get_RedirectDynamicDevices
- IMsRdpClientNonScriptable3.put_RedirectDynamicDevices
- IMsRdpClientNonScriptable4.RedirectDynamicDevices
- IMsRdpClientNonScriptable4.get_RedirectDynamicDevices
- IMsRdpClientNonScriptable4.put_RedirectDynamicDevices
- IMsRdpClientNonScriptable5.RedirectDynamicDevices
- IMsRdpClientNonScriptable5.get_RedirectDynamicDevices
- IMsRdpClientNonScriptable5.put_RedirectDynamicDevices
- MsRdpClient5.RedirectDynamicDevices
- MsRdpClient6.RedirectDynamicDevices
- MsRdpClient7.RedirectDynamicDevices
- MsRdpClient8.RedirectDynamicDevices
- MsRdpClient9.RedirectDynamicDevices
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 75224d26034e606a7a46943a02845280a092c3b5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740397"
---
# <a name="imsrdpclientnonscriptable3redirectdynamicdevices-property"></a>IMsRdpClientNonScriptable3 :: RedirectDynamicDevices, propriété

Spécifie ou récupère si les périphériques PnP (Plug-and-Play attachés dynamiquement) qui sont énumérés dans une session sont disponibles pour la redirection.

Cette propriété est en lecture/écriture.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT put_RedirectDynamicDevices(
  [in]  VARIANT_BOOL fRedirectDynamicDevices
);

HRESULT get_RedirectDynamicDevices(
  [out] VARIANT_BOOL *pfRedirectDynamicDevices
);
```



## <a name="property-value"></a>Valeur de la propriété

Spécifie si les appareils PnP attachés de manière dynamique et qui sont énumérés dans une session sont disponibles pour la redirection.

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

 

 





