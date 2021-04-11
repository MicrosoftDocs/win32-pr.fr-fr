---
title: IMsRdpClient ColorDepth, propriété
description: Profondeur de couleur (en bits par pixel) de la connexion du contrôle.
ms.assetid: 9ba4d8fe-20cd-40e9-a71a-0dce0ddd29fc
ms.tgt_platform: multiple
keywords:
- ColorDepth, propriété Services Bureau à distance
- ColorDepth Property Services Bureau à distance, IMsRdpClient, interface
- Services Bureau à distance de l’interface IMsRdpClient, propriété ColorDepth
- ColorDepth Property Services Bureau à distance, IMsRdpClient2, interface
- Services Bureau à distance de l’interface IMsRdpClient2, propriété ColorDepth
- ColorDepth Property Services Bureau à distance, IMsRdpClient3, interface
- Services Bureau à distance de l’interface IMsRdpClient3, propriété ColorDepth
- ColorDepth Property Services Bureau à distance, IMsRdpClient4, interface
- Services Bureau à distance de l’interface IMsRdpClient4, propriété ColorDepth
- ColorDepth Property Services Bureau à distance, IMsRdpClient5, interface
- Services Bureau à distance de l’interface IMsRdpClient5, propriété ColorDepth
- ColorDepth Property Services Bureau à distance, IMsRdpClient6, interface
- Services Bureau à distance de l’interface IMsRdpClient6, propriété ColorDepth
- ColorDepth Property Services Bureau à distance, IMsRdpClient7, interface
- Services Bureau à distance de l’interface IMsRdpClient7, propriété ColorDepth
- ColorDepth Property Services Bureau à distance, IMsRdpClient8, interface
- Services Bureau à distance de l’interface IMsRdpClient8, propriété ColorDepth
- ColorDepth Property Services Bureau à distance, IMsRdpClient9, interface
- Services Bureau à distance de l’interface IMsRdpClient9, propriété ColorDepth
- ColorDepth Property Services Bureau à distance, IMsRdpClient10, interface
- Services Bureau à distance de l’interface IMsRdpClient10, propriété ColorDepth
topic_type:
- apiref
api_name:
- IMsRdpClient.ColorDepth
- IMsRdpClient.get_ColorDepth
- IMsRdpClient.put_ColorDepth
- IMsRdpClient2.ColorDepth
- IMsRdpClient2.get_ColorDepth
- IMsRdpClient2.put_ColorDepth
- IMsRdpClient3.ColorDepth
- IMsRdpClient3.get_ColorDepth
- IMsRdpClient3.put_ColorDepth
- IMsRdpClient4.ColorDepth
- IMsRdpClient4.get_ColorDepth
- IMsRdpClient4.put_ColorDepth
- IMsRdpClient5.ColorDepth
- IMsRdpClient5.get_ColorDepth
- IMsRdpClient5.put_ColorDepth
- IMsRdpClient6.ColorDepth
- IMsRdpClient6.get_ColorDepth
- IMsRdpClient6.put_ColorDepth
- IMsRdpClient7.ColorDepth
- IMsRdpClient7.get_ColorDepth
- IMsRdpClient7.put_ColorDepth
- IMsRdpClient8.ColorDepth
- IMsRdpClient8.get_ColorDepth
- IMsRdpClient8.put_ColorDepth
- IMsRdpClient9.ColorDepth
- IMsRdpClient9.get_ColorDepth
- IMsRdpClient9.put_ColorDepth
- IMsRdpClient10.ColorDepth
- IMsRdpClient10.get_ColorDepth
- IMsRdpClient10.put_ColorDepth
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d5099deff3913d23173a466245cbf08fd5b95a6a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105877"
---
# <a name="imsrdpclientcolordepth-property"></a>IMsRdpClient :: ColorDepth, propriété

Profondeur de couleur (en bits par pixel) de la connexion du contrôle.

Cette propriété est en lecture/écriture.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT put_ColorDepth(
  [in]  LONG colorDepth
);

HRESULT get_ColorDepth(
  [out] LONG pcolorDepth
);
```



## <a name="property-value"></a>Valeur de la propriété

Profondeur de couleur. Les valeurs incluent 8, 15, 16, 24 et 32 bits par pixel.

## <a name="error-codes"></a>Codes d’erreur

Si les méthodes sont correctement exécutées, la méthode **S \_ OK** est retournée. Toute autre valeur **HRESULT** indique que l’appel a échoué.

## <a name="remarks"></a>Notes

Cette propriété ne peut pas être définie lorsque le contrôle est connecté.

Pour plus d’informations sur la Connexion Bureau à distance par le Web, consultez [Requirements for connexion Bureau à distance par le Web](requirements-for-remote-desktop-web-connection.md).

## <a name="requirements"></a>Configuration requise



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

 

 





