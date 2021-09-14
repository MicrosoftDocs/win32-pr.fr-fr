---
title: Méthode de reconnexion IMsRdpClient8
description: Se reconnecte à la session à distance avec la largeur et la hauteur du nouveau bureau.
ms.assetid: A2C4101D-780A-4973-B87C-025D9140C4BC
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode de reconnexion
- Services Bureau à distance de la méthode de reconnexion, interface IMsRdpClient8
- Services Bureau à distance de l’interface IMsRdpClient8, méthode de reconnexion
- Services Bureau à distance de la méthode de reconnexion, interface IMsRdpClient9
- Services Bureau à distance de l’interface IMsRdpClient9, méthode de reconnexion
- Services Bureau à distance de la méthode de reconnexion, interface IMsRdpClient10
- Services Bureau à distance de l’interface IMsRdpClient10, méthode de reconnexion
topic_type:
- apiref
api_name:
- IMsRdpClient8.Reconnect
- IMsRdpClient9.Reconnect
- IMsRdpClient10.Reconnect
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d62072c56852af6be2965ce63aecf4634de87d11
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126920027"
---
# <a name="imsrdpclient8reconnect-method"></a>IMsRdpClient8 :: reconnect, méthode

Se reconnecte à la session à distance avec la largeur et la hauteur du nouveau bureau. Le contrôle doit déjà être connecté à une session distante pour que cette méthode aboutisse.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT Reconnect(
  [in]          ULONG                  ulWidth,
  [in]          ULONG                  ulHeight,
  [out, retval] ControlReconnectStatus *pReconnectStatus
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*ulWidth* \[ dans\]
</dt> <dd>

Type : **ULong**

Nouvelle largeur du bureau, en pixels. Consultez la propriété [**DesktopWidth**](imstscax-desktopwidth.md) pour connaître les restrictions de valeur.

</dd> <dt>

*ulHeight* \[ dans\]
</dt> <dd>

Type : **ULong**

Nouvelle hauteur du bureau, en pixels. Consultez la propriété [**DesktopHeight**](imstscax-desktopheight.md) pour connaître les restrictions de valeur.

</dd> <dt>

*pReconnectStatus* \[ out, retval\]
</dt> <dd>

Type : **[ **ControlReconnectStatus**](controlreconnectstatus.md)\***

Pointeur vers une variable [**ControlReconnectStatus**](controlreconnectstatus.md) qui reçoit l’état de l’opération de reconnexion.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Type : **HRESULT**

Si cette méthode est réussie, elle retourne la valeur **\_ OK**. Sinon, elle retourne un code d’erreur **HRESULT** .

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 8<br/>                                                                   |
| Serveur minimal pris en charge<br/> | Windows Server 2012<br/>                                                         |
| Bibliothèque de types<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |
| IID<br/>                      | IID \_ IMsRdpClient8 est défini en tant que 4247E044-9271-43A9-BC49-E2AD9E855D62<br/>       |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IMsRdpClient8**](imsrdpclient8.md)
</dt> <dt>

[**IMsRdpClient9**](imsrdpclient9.md)
</dt> <dt>

[**IMsRdpClient10**](imsrdpclient10.md)
</dt> <dt>

[**ControlReconnectStatus**](controlreconnectstatus.md)
</dt> </dl>

 

 





