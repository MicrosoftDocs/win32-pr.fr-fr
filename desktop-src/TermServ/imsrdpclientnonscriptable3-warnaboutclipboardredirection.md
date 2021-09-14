---
title: IMsRdpClientNonScriptable3 propriété WarnAboutClipboardRedirection
description: Spécifie ou récupère une valeur indiquant si la boîte de dialogue d’avertissement de sécurité doit être affichée pour avertir les utilisateurs de la redirection du presse-papiers.
ms.assetid: 2f3ca58b-3c89-4251-ae15-2c0aaf308893
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la propriété WarnAboutClipboardRedirection
- Services Bureau à distance de la propriété WarnAboutClipboardRedirection, interface IMsRdpClientNonScriptable3
- Services Bureau à distance de l’interface IMsRdpClientNonScriptable3, propriété WarnAboutClipboardRedirection
- Services Bureau à distance de la propriété WarnAboutClipboardRedirection, interface IMsRdpClientNonScriptable4
- Services Bureau à distance de l’interface IMsRdpClientNonScriptable4, propriété WarnAboutClipboardRedirection
- Services Bureau à distance de la propriété WarnAboutClipboardRedirection, interface IMsRdpClientNonScriptable5
- Services Bureau à distance de l’interface IMsRdpClientNonScriptable5, propriété WarnAboutClipboardRedirection
- Services Bureau à distance de la propriété WarnAboutClipboardRedirection, objet MsRdpClient5
- Services Bureau à distance objet MsRdpClient5, propriété WarnAboutClipboardRedirection
- Services Bureau à distance de la propriété WarnAboutClipboardRedirection, objet MsRdpClient6
- Services Bureau à distance objet MsRdpClient6, propriété WarnAboutClipboardRedirection
- Services Bureau à distance de la propriété WarnAboutClipboardRedirection, objet MsRdpClient7
- Services Bureau à distance objet MsRdpClient7, propriété WarnAboutClipboardRedirection
- Services Bureau à distance de la propriété WarnAboutClipboardRedirection, objet MsRdpClient8
- Services Bureau à distance objet MsRdpClient8, propriété WarnAboutClipboardRedirection
- Services Bureau à distance de la propriété WarnAboutClipboardRedirection, objet MsRdpClient9
- Services Bureau à distance objet MsRdpClient9, propriété WarnAboutClipboardRedirection
topic_type:
- apiref
api_name:
- IMsRdpClientNonScriptable3.WarnAboutClipboardRedirection
- IMsRdpClientNonScriptable3.get_WarnAboutClipboardRedirection
- IMsRdpClientNonScriptable3.put_WarnAboutClipboardRedirection
- IMsRdpClientNonScriptable4.WarnAboutClipboardRedirection
- IMsRdpClientNonScriptable4.get_WarnAboutClipboardRedirection
- IMsRdpClientNonScriptable4.put_WarnAboutClipboardRedirection
- IMsRdpClientNonScriptable5.WarnAboutClipboardRedirection
- IMsRdpClientNonScriptable5.get_WarnAboutClipboardRedirection
- IMsRdpClientNonScriptable5.put_WarnAboutClipboardRedirection
- MsRdpClient5.WarnAboutClipboardRedirection
- MsRdpClient6.WarnAboutClipboardRedirection
- MsRdpClient7.WarnAboutClipboardRedirection
- MsRdpClient8.WarnAboutClipboardRedirection
- MsRdpClient9.WarnAboutClipboardRedirection
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d8da6fa2f7fb36a110666c8b14a818264813d816
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127008628"
---
# <a name="imsrdpclientnonscriptable3warnaboutclipboardredirection-property"></a>IMsRdpClientNonScriptable3 :: WarnAboutClipboardRedirection, propriété

Spécifie ou récupère une valeur indiquant si la boîte de dialogue d’avertissement de sécurité doit être affichée pour avertir les utilisateurs de la redirection du presse-papiers.

Cette propriété est en lecture/écriture.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT put_WarnAboutClipboardRedirection(
  [in]  VARIANT_BOOL fWarn
);

HRESULT get_WarnAboutClipboardRedirection(
  [out] VARIANT_BOOL *pfWarn
);
```



## <a name="property-value"></a>Valeur de la propriété

Spécifie si la boîte de dialogue d’avertissement de sécurité doit être affichée pour avertir les utilisateurs de la redirection du presse-papiers.

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

 

 





