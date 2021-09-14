---
title: IMsTscNonScriptable propriété PortableSalt
description: Cette propriété n'est plus prise en charge.
ms.assetid: 1f123ec8-27b6-4637-9c57-fe32a224be8a
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la propriété PortableSalt
- Services Bureau à distance de la propriété PortableSalt, interface IMsTscNonScriptable
- Services Bureau à distance de l’interface IMsTscNonScriptable, propriété PortableSalt
- Propriété PortableSalt Services Bureau à distance, objet MsTscAx
- Objet MsTscAx Services Bureau à distance, propriété PortableSalt
- Services Bureau à distance de la propriété PortableSalt, interface IMsRdpClientNonScriptable
- Services Bureau à distance de l’interface IMsRdpClientNonScriptable, propriété PortableSalt
- Services Bureau à distance de la propriété PortableSalt, interface IMsRdpClientNonScriptable2
- Services Bureau à distance de l’interface IMsRdpClientNonScriptable2, propriété PortableSalt
- Services Bureau à distance de la propriété PortableSalt, interface IMsRdpClientNonScriptable3
- Services Bureau à distance de l’interface IMsRdpClientNonScriptable3, propriété PortableSalt
- Services Bureau à distance de la propriété PortableSalt, interface IMsRdpClientNonScriptable4
- Services Bureau à distance de l’interface IMsRdpClientNonScriptable4, propriété PortableSalt
- Services Bureau à distance de la propriété PortableSalt, interface IMsRdpClientNonScriptable5
- Services Bureau à distance de l’interface IMsRdpClientNonScriptable5, propriété PortableSalt
topic_type:
- apiref
api_name:
- IMsTscNonScriptable.PortableSalt
- IMsTscNonScriptable.get_PortableSalt
- IMsTscNonScriptable.put_PortableSalt
- MsTscAx.PortableSalt
- IMsRdpClientNonScriptable.PortableSalt
- IMsRdpClientNonScriptable.get_PortableSalt
- IMsRdpClientNonScriptable.put_PortableSalt
- IMsRdpClientNonScriptable2.PortableSalt
- IMsRdpClientNonScriptable2.get_PortableSalt
- IMsRdpClientNonScriptable2.put_PortableSalt
- IMsRdpClientNonScriptable3.PortableSalt
- IMsRdpClientNonScriptable3.get_PortableSalt
- IMsRdpClientNonScriptable3.put_PortableSalt
- IMsRdpClientNonScriptable4.PortableSalt
- IMsRdpClientNonScriptable4.get_PortableSalt
- IMsRdpClientNonScriptable4.put_PortableSalt
- IMsRdpClientNonScriptable5.PortableSalt
- IMsRdpClientNonScriptable5.get_PortableSalt
- IMsRdpClientNonScriptable5.put_PortableSalt
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0162073b8361cc89f7ab2e33f60406c0db935bdb
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127095617"
---
# <a name="imstscnonscriptableportablesalt-property"></a>IMsTscNonScriptable ::P propriété ortableSalt

Cette propriété n'est plus prise en charge.

Cette propriété est en lecture/écriture.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT put_PortableSalt(
  [in]  BSTR newPortableSalt
);

HRESULT get_PortableSalt(
  [out] BSTR *pPortableSalt
);
```



## <a name="property-value"></a>Valeur de la propriété

Nouvelle partie Salt portable pour un mot de passe encodé portable.

## <a name="error-codes"></a>Codes d’erreur

Retourne **E \_ NOTIMPL**.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Aucun pris en charge<br/>                                                              |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                                                              |
| Fin de la prise en charge des clients<br/>    | Aucun pris en charge<br/>                                                              |
| Fin de la prise en charge des serveurs<br/>    | Aucun pris en charge<br/>                                                              |
| Bibliothèque de types<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |
| IID<br/>                      | IID \_ IMsTscNonScriptable est défini en tant que c1e6743a-41c1-4a74-832a-0dd06c1c7a0e<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IMsRdpClientNonScriptable**](imsrdpclientnonscriptable-interface.md)
</dt> <dt>

[**IMsRdpClientNonScriptable2**](imsrdpclientnonscriptable2.md)
</dt> <dt>

[**IMsRdpClientNonScriptable3**](imsrdpclientnonscriptable3.md)
</dt> <dt>

[**IMsRdpClientNonScriptable4**](imsrdpclientnonscriptable4.md)
</dt> <dt>

[**IMsRdpClientNonScriptable5**](imsrdpclientnonscriptable5.md)
</dt> <dt>

[**IMsTscNonScriptable**](imstscnonscriptable-interface.md)
</dt> <dt>

[**PortablePassword**](imstscnonscriptable-portablepassword.md)
</dt> </dl>

 

 





