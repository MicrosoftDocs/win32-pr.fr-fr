---
title: Méthode IMsRdpClient7 GetStatusText (OpenService. h)
description: Récupère le texte d’État pour le code d’état spécifié.
ms.assetid: 1da2280a-c26d-4caa-b227-c289055f3aa9
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode GetStatusText
- Méthode GetStatusText Services Bureau à distance, interface IMsRdpClient7
- Services Bureau à distance de l’interface IMsRdpClient7, méthode GetStatusText
- Méthode GetStatusText Services Bureau à distance, interface IMsRdpClient8
- Services Bureau à distance de l’interface IMsRdpClient8, méthode GetStatusText
- Méthode GetStatusText Services Bureau à distance, interface IMsRdpClient9
- Services Bureau à distance de l’interface IMsRdpClient9, méthode GetStatusText
- Méthode GetStatusText Services Bureau à distance, interface IMsRdpClient10
- Services Bureau à distance de l’interface IMsRdpClient10, méthode GetStatusText
topic_type:
- apiref
api_name:
- IMsRdpClient7.GetStatusText
- IMsRdpClient8.GetStatusText
- IMsRdpClient9.GetStatusText
- IMsRdpClient10.GetStatusText
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 42ecccb6535afec2d32ff0466428af36c432bc981a1bc23cfa24161ca969a80e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119285189"
---
# <a name="imsrdpclient7getstatustext-method"></a>IMsRdpClient7 :: GetStatusText, méthode

Récupère le texte d’État pour le code d’état spécifié.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetStatusText(
  [in]          UINT statusCode,
  [out, retval] BSTR *pBstrStatusText
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*statusCode* \[ dans\]
</dt> <dd>

**Uint** qui spécifie le code d’État pour lequel récupérer le texte.

</dd> <dt>

*pBstrStatusText* \[ out, retval\]
</dt> <dd>

Adresse d’un **BSTR** qui reçoit le texte d’État.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si cette méthode est réussie, elle retourne la valeur **\_ OK**. Sinon, elle retourne un code d’erreur **HRESULT** .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 7<br/>                                                                     |
| Serveur minimal pris en charge<br/> | Windows Server 2008 R2<br/>                                                        |
| En-tête<br/>                   | <dl> <dt>OpenService. h</dt> </dl> |
| Bibliothèque de types<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>   |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>   |
| IID<br/>                      | IID \_ IMsRdpClient7 est défini en tant que b2a5b5ce-3461-444A-91D4-add26d070638<br/>         |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IMsRdpClient7**](imsrdpclient7.md)
</dt> <dt>

[**IMsRdpClient8**](imsrdpclient8.md)
</dt> <dt>

[**IMsRdpClient9**](imsrdpclient9.md)
</dt> <dt>

[**IMsRdpClient10**](imsrdpclient10.md)
</dt> </dl>

 

 





