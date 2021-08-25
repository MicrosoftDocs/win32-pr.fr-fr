---
title: IMsRdpClientNonScriptable3 propriété EnableCredSspSupport
description: Spécifie ou récupère si le fournisseur de services de sécurité des informations d’identification (CredSSP) est activé pour cette connexion.
ms.assetid: 770da50b-2a93-4274-9b6f-c24c13f08549
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la propriété EnableCredSspSupport
- Services Bureau à distance de la propriété EnableCredSspSupport, interface IMsRdpClientNonScriptable3
- Services Bureau à distance de l’interface IMsRdpClientNonScriptable3, propriété EnableCredSspSupport
- Services Bureau à distance de la propriété EnableCredSspSupport, interface IMsRdpClientNonScriptable4
- Services Bureau à distance de l’interface IMsRdpClientNonScriptable4, propriété EnableCredSspSupport
- Services Bureau à distance de la propriété EnableCredSspSupport, interface IMsRdpClientNonScriptable5
- Services Bureau à distance de l’interface IMsRdpClientNonScriptable5, propriété EnableCredSspSupport
- Services Bureau à distance de la propriété EnableCredSspSupport, objet MsRdpClient5
- Services Bureau à distance objet MsRdpClient5, propriété EnableCredSspSupport
- Services Bureau à distance de la propriété EnableCredSspSupport, objet MsRdpClient6
- Services Bureau à distance objet MsRdpClient6, propriété EnableCredSspSupport
- Services Bureau à distance de la propriété EnableCredSspSupport, objet MsRdpClient7
- Services Bureau à distance objet MsRdpClient7, propriété EnableCredSspSupport
- Services Bureau à distance de la propriété EnableCredSspSupport, objet MsRdpClient8
- Services Bureau à distance objet MsRdpClient8, propriété EnableCredSspSupport
- Services Bureau à distance de la propriété EnableCredSspSupport, objet MsRdpClient9
- Services Bureau à distance objet MsRdpClient9, propriété EnableCredSspSupport
topic_type:
- apiref
api_name:
- IMsRdpClientNonScriptable3.EnableCredSspSupport
- IMsRdpClientNonScriptable3.get_EnableCredSspSupport
- IMsRdpClientNonScriptable3.put_EnableCredSspSupport
- IMsRdpClientNonScriptable4.EnableCredSspSupport
- IMsRdpClientNonScriptable4.get_EnableCredSspSupport
- IMsRdpClientNonScriptable4.put_EnableCredSspSupport
- IMsRdpClientNonScriptable5.EnableCredSspSupport
- IMsRdpClientNonScriptable5.get_EnableCredSspSupport
- IMsRdpClientNonScriptable5.put_EnableCredSspSupport
- MsRdpClient5.EnableCredSspSupport
- MsRdpClient6.EnableCredSspSupport
- MsRdpClient7.EnableCredSspSupport
- MsRdpClient8.EnableCredSspSupport
- MsRdpClient9.EnableCredSspSupport
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2f682fe85de22bcffad42d5da80c2f565f4690373629a804c7bbb4fefafa23b2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120125689"
---
# <a name="imsrdpclientnonscriptable3enablecredsspsupport-property"></a>IMsRdpClientNonScriptable3 :: EnableCredSspSupport, propriété

Spécifie ou récupère si le fournisseur de services de sécurité des informations d’identification (CredSSP) est activé pour cette connexion.

Cette propriété est en lecture/écriture.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT put_EnableCredSspSupport(
  [in]  VARIANT_BOOL fEnableSupport
);

HRESULT get_EnableCredSspSupport(
  [out] VARIANT_BOOL *pfEnableSupport
);
```



## <a name="property-value"></a>Valeur de la propriété

Spécifie si CredSSP est activé pour cette connexion.

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

 

 





