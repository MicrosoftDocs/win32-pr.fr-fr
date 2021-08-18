---
title: IMsRdpClientNonScriptable5 propriété RemoteMonitorLayoutMatchesLocal
description: Spécifie si la disposition du moniteur distant est identique à la disposition du moniteur local.
ms.assetid: 8F3C6650-870C-417C-82FC-E145FC360012
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la propriété RemoteMonitorLayoutMatchesLocal
- Services Bureau à distance de la propriété RemoteMonitorLayoutMatchesLocal, interface IMsRdpClientNonScriptable5
- Services Bureau à distance de l’interface IMsRdpClientNonScriptable5, propriété RemoteMonitorLayoutMatchesLocal
topic_type:
- apiref
api_name:
- IMsRdpClientNonScriptable5.RemoteMonitorLayoutMatchesLocal
- IMsRdpClientNonScriptable5.get_RemoteMonitorLayoutMatchesLocal
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 235879a80e7e2a90207ee9b7852e73a26874c0961d7394fa80f2cf85e7452362
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119138722"
---
# <a name="imsrdpclientnonscriptable5remotemonitorlayoutmatcheslocal-property"></a>IMsRdpClientNonScriptable5 :: RemoteMonitorLayoutMatchesLocal, propriété

Spécifie si la disposition du moniteur distant est identique à la disposition du moniteur local. Si cette propriété contient **la \_ valeur true**, la disposition du moniteur distant est identique à la disposition du moniteur local. Si cette propriété contient **la \_ valeur false**, les analyses locales et distantes ont des dispositions différentes.

Cette propriété est en lecture seule.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT get_RemoteMonitorLayoutMatchesLocal(
  [out, retval] VARIANT_BOOL *pfRemoteMatchesLocal
);
```



## <a name="property-value"></a>Valeur de la propriété

Reçoit la valeur de la propriété.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 7<br/>                                                                          |
| Serveur minimal pris en charge<br/> | Windows Server 2008 R2<br/>                                                             |
| Bibliothèque de types<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>        |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>        |
| IID<br/>                      | IID \_ IMsRdpClientNonScriptable5 est défini en tant que 4f6996d5-d7b1-412c-b0ff-063718566907<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IMsRdpClientNonScriptable5**](imsrdpclientnonscriptable5.md)
</dt> </dl>

 

 





