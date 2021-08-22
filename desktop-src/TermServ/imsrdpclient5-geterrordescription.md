---
title: Méthode IMsRdpClient5 GetErrorDescription
description: Récupère la description de l’erreur pour les événements de déconnexion de la session.
ms.assetid: 8c8f7b10-7f79-4586-845e-e99f5ca81905
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode GetErrorDescription
- Méthode GetErrorDescription Services Bureau à distance, interface IMsRdpClient5
- Services Bureau à distance de l’interface IMsRdpClient5, méthode GetErrorDescription
- Méthode GetErrorDescription Services Bureau à distance, interface IMsRdpClient6
- Services Bureau à distance de l’interface IMsRdpClient6, méthode GetErrorDescription
- Méthode GetErrorDescription Services Bureau à distance, interface IMsRdpClient7
- Services Bureau à distance de l’interface IMsRdpClient7, méthode GetErrorDescription
- Méthode GetErrorDescription Services Bureau à distance, interface IMsRdpClient8
- Services Bureau à distance de l’interface IMsRdpClient8, méthode GetErrorDescription
- Méthode GetErrorDescription Services Bureau à distance, interface IMsRdpClient9
- Services Bureau à distance de l’interface IMsRdpClient9, méthode GetErrorDescription
- Méthode GetErrorDescription Services Bureau à distance, interface IMsRdpClient10
- Services Bureau à distance de l’interface IMsRdpClient10, méthode GetErrorDescription
topic_type:
- apiref
api_name:
- IMsRdpClient5.GetErrorDescription
- IMsRdpClient6.GetErrorDescription
- IMsRdpClient7.GetErrorDescription
- IMsRdpClient8.GetErrorDescription
- IMsRdpClient9.GetErrorDescription
- IMsRdpClient10.GetErrorDescription
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 197025b4cfb842cf4ca38af64124c02415240ac6fc878f9c121d4e228b77f5b1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119001487"
---
# <a name="imsrdpclient5geterrordescription-method"></a>IMsRdpClient5 :: GetErrorDescription, méthode

Récupère la description de l’erreur pour les événements de déconnexion de la session.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetErrorDescription(
  [in]  UINT disconnectReason,
  [in]  UINT extendedDisconnectReason,
  [out] BSTR *pBstrErrorMsg
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*disconnectReason* \[ dans\]
</dt> <dd>

Raison de la déconnexion.

</dd> <dt>

*extendedDisconnectReason* \[ dans\]
</dt> <dd>

Fournit des informations détaillées sur la raison pour laquelle une déconnexion a été lancée.

</dd> <dt>

*pBstrErrorMsg* \[ à\]
</dt> <dd>

Pointeur vers une variable **BSTR** qui reçoit le texte du message d’erreur.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode ne retourne pas de valeur.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Vista<br/>                                                               |
| Serveur minimal pris en charge<br/> | Windows Server 2008<br/>                                                         |
| Bibliothèque de types<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |
| IID<br/>                      | IID \_ IMsRdpClient5 est défini en tant que 4eb5335b-6429-477D-B922-e06a28ecd8bf<br/>       |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IMsRdpClient5**](imsrdpclient5.md)
</dt> <dt>

[**IMsRdpClient6**](imsrdpclient6.md)
</dt> <dt>

[**IMsRdpClient7**](imsrdpclient7.md)
</dt> <dt>

[**IMsRdpClient8**](imsrdpclient8.md)
</dt> <dt>

[**IMsRdpClient9**](imsrdpclient9.md)
</dt> <dt>

[**IMsRdpClient10**](imsrdpclient10.md)
</dt> </dl>

 

 





