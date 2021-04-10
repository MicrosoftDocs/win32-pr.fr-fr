---
title: IMsRdpClientNonScriptable4 propriété WarnAboutPrinterRedirection
description: Contrôle si la boîte de dialogue de redirection affiche un message sur la redirection de l’imprimante avant de démarrer une session.
ms.assetid: 12c5bc8d-7bc1-4a94-a9b8-6b852772c936
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la propriété WarnAboutPrinterRedirection
- Services Bureau à distance de la propriété WarnAboutPrinterRedirection, interface IMsRdpClientNonScriptable4
- Services Bureau à distance de l’interface IMsRdpClientNonScriptable4, propriété WarnAboutPrinterRedirection
- Services Bureau à distance de la propriété WarnAboutPrinterRedirection, interface IMsRdpClientNonScriptable5
- Services Bureau à distance de l’interface IMsRdpClientNonScriptable5, propriété WarnAboutPrinterRedirection
- Services Bureau à distance de la propriété WarnAboutPrinterRedirection, objet MsRdpClient6
- Services Bureau à distance objet MsRdpClient6, propriété WarnAboutPrinterRedirection
- Services Bureau à distance de la propriété WarnAboutPrinterRedirection, objet MsRdpClient7
- Services Bureau à distance objet MsRdpClient7, propriété WarnAboutPrinterRedirection
- Services Bureau à distance de la propriété WarnAboutPrinterRedirection, objet MsRdpClient8
- Services Bureau à distance objet MsRdpClient8, propriété WarnAboutPrinterRedirection
- Services Bureau à distance de la propriété WarnAboutPrinterRedirection, objet MsRdpClient9
- Services Bureau à distance objet MsRdpClient9, propriété WarnAboutPrinterRedirection
topic_type:
- apiref
api_name:
- IMsRdpClientNonScriptable4.WarnAboutPrinterRedirection
- IMsRdpClientNonScriptable4.get_WarnAboutPrinterRedirection
- IMsRdpClientNonScriptable4.put_WarnAboutPrinterRedirection
- IMsRdpClientNonScriptable5.WarnAboutPrinterRedirection
- IMsRdpClientNonScriptable5.get_WarnAboutPrinterRedirection
- IMsRdpClientNonScriptable5.put_WarnAboutPrinterRedirection
- MsRdpClient6.WarnAboutPrinterRedirection
- MsRdpClient7.WarnAboutPrinterRedirection
- MsRdpClient8.WarnAboutPrinterRedirection
- MsRdpClient9.WarnAboutPrinterRedirection
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 24e2fa93995946e741caa76f1ee5b84be79d9c90
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104317298"
---
# <a name="imsrdpclientnonscriptable4warnaboutprinterredirection-property"></a>IMsRdpClientNonScriptable4 :: WarnAboutPrinterRedirection, propriété

Contrôle si la boîte de dialogue de redirection affiche un message sur la redirection de l’imprimante avant de démarrer une session.

Cette propriété est en lecture/écriture.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT put_WarnAboutPrinterRedirection(
  [in]  VARIANT_BOOL fWarn
);

HRESULT get_WarnAboutPrinterRedirection(
  [out] VARIANT_BOOL *pfWarn
);
```



## <a name="property-value"></a>Valeur de la propriété

Définit si la boîte de dialogue de redirection affiche un message sur la redirection de l’imprimante.

## <a name="error-codes"></a>Codes d’erreur

Retourne **S \_ OK** en cas de réussite.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Vista<br/>                                                                 |
| Serveur minimal pris en charge<br/> | Windows Server 2008<br/>                                                           |
| Bibliothèque de types<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>   |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>   |
| IID<br/>                      | IMsRdpClientNonScriptable4 est défini en tant que f50fa8aa-1c7d-4f59-B15C-a90cacae1fcb<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IMsRdpClientNonScriptable5**](imsrdpclientnonscriptable5.md)
</dt> <dt>

[**IMsRdpClientNonScriptable4**](imsrdpclientnonscriptable4.md)
</dt> </dl>

 

 





