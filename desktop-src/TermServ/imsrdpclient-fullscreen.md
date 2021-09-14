---
title: Propriété FullScreen IMsRdpClient
description: Détermine si le contrôle client est en mode plein écran.
ms.assetid: 64fe2835-c00e-4d21-812d-dcf160147d93
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de propriété FullScreen
- Services Bureau à distance de propriété FullScreen, interface IMsRdpClient
- Services Bureau à distance de l’interface IMsRdpClient, propriété FullScreen
- Services Bureau à distance de propriété FullScreen, interface IMsRdpClient2
- Services Bureau à distance de l’interface IMsRdpClient2, propriété FullScreen
- Services Bureau à distance de propriété FullScreen, interface IMsRdpClient3
- Services Bureau à distance de l’interface IMsRdpClient3, propriété FullScreen
- Services Bureau à distance de propriété FullScreen, interface IMsRdpClient4
- Services Bureau à distance de l’interface IMsRdpClient4, propriété FullScreen
- Services Bureau à distance de propriété FullScreen, interface IMsRdpClient5
- Services Bureau à distance de l’interface IMsRdpClient5, propriété FullScreen
- Services Bureau à distance de propriété FullScreen, interface IMsRdpClient6
- Services Bureau à distance de l’interface IMsRdpClient6, propriété FullScreen
- Services Bureau à distance de propriété FullScreen, interface IMsRdpClient7
- Services Bureau à distance de l’interface IMsRdpClient7, propriété FullScreen
- Services Bureau à distance de propriété FullScreen, interface IMsRdpClient8
- Services Bureau à distance de l’interface IMsRdpClient8, propriété FullScreen
- Services Bureau à distance de propriété FullScreen, interface IMsRdpClient9
- Services Bureau à distance de l’interface IMsRdpClient9, propriété FullScreen
- Services Bureau à distance de propriété FullScreen, interface IMsRdpClient10
- Services Bureau à distance de l’interface IMsRdpClient10, propriété FullScreen
topic_type:
- apiref
api_name:
- IMsRdpClient.FullScreen
- IMsRdpClient.get_FullScreen
- IMsRdpClient.put_FullScreen
- IMsRdpClient2.FullScreen
- IMsRdpClient2.get_FullScreen
- IMsRdpClient2.put_FullScreen
- IMsRdpClient3.FullScreen
- IMsRdpClient3.get_FullScreen
- IMsRdpClient3.put_FullScreen
- IMsRdpClient4.FullScreen
- IMsRdpClient4.get_FullScreen
- IMsRdpClient4.put_FullScreen
- IMsRdpClient5.FullScreen
- IMsRdpClient5.get_FullScreen
- IMsRdpClient5.put_FullScreen
- IMsRdpClient6.FullScreen
- IMsRdpClient6.get_FullScreen
- IMsRdpClient6.put_FullScreen
- IMsRdpClient7.FullScreen
- IMsRdpClient7.get_FullScreen
- IMsRdpClient7.put_FullScreen
- IMsRdpClient8.FullScreen
- IMsRdpClient8.get_FullScreen
- IMsRdpClient8.put_FullScreen
- IMsRdpClient9.FullScreen
- IMsRdpClient9.get_FullScreen
- IMsRdpClient9.put_FullScreen
- IMsRdpClient10.FullScreen
- IMsRdpClient10.get_FullScreen
- IMsRdpClient10.put_FullScreen
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1adbc8e11d2cc4fb4a8071372777a01d81b5edad
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126856972"
---
# <a name="imsrdpclientfullscreen-property"></a>IMsRdpClient :: FullScreen, propriété

Détermine si le contrôle client est en mode plein écran.

Cette propriété est en lecture/écriture.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT put_FullScreen(
  [in]  VARIANT_BOOL fFullScreen
);

HRESULT get_FullScreen(
  [out] VARIANT_BOOL *pfFullScreen
);
```



## <a name="property-value"></a>Valeur de la propriété

**True** pour passer en mode plein écran, **false** pour conserver le mode plein écran et revenir en mode fenêtre.

## <a name="error-codes"></a>Codes d’erreur

Si les méthodes sont correctement exécutées, la méthode **S \_ OK** est retournée. Toute autre valeur **HRESULT** indique que l’appel a échoué.

## <a name="remarks"></a>Notes

Vous pouvez définir cette propriété lorsque le contrôle est connecté.

Vous devez appeler la méthode [**IMsRdpClientNonScriptable3 ::p ut \_ ConnectionBarText**](imsrdpclientnonscriptable3-connectionbartext.md) avant d’appeler la méthode [**IMsTscSecuredSettings ::P ut \_ fullscreen**](imstscsecuredsettings-fullscreen.md) ou **IMsRdpClient ::p ut \_ fullscreen** .

Pour plus d’informations sur la Connexion Bureau à distance par le Web, consultez [Requirements for connexion Bureau à distance par le Web](requirements-for-remote-desktop-web-connection.md).

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Vista<br/>                                                               |
| Serveur minimal pris en charge<br/> | Windows Server 2008<br/>                                                         |
| Bibliothèque de types<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |
| IID<br/>                      | IID \_ IMsRdpClient est défini en tant que 92b4a539-7115-4b7c-a5a9-e5d9efc2780a<br/>        |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IMsRdpClient**](imsrdpclient-interface.md)
</dt> <dt>

[**IMsRdpClient2**](imsrdpclient2.md)
</dt> <dt>

[**IMsRdpClient3**](imsrdpclient3.md)
</dt> <dt>

[**IMsRdpClient4**](imsrdpclient4.md)
</dt> <dt>

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

 

 





