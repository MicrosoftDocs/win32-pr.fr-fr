---
title: IMsRdpClient4 propriété AdvancedSettings5
description: Récupère un pointeur vers une interface IMsRdpClientAdvancedSettings4.
ms.assetid: 2dd0cc5f-7822-485f-8b3f-12407af1e091
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la propriété AdvancedSettings5
- Services Bureau à distance de la propriété AdvancedSettings5, interface IMsRdpClient4
- Services Bureau à distance de l’interface IMsRdpClient4, propriété AdvancedSettings5
- Services Bureau à distance de la propriété AdvancedSettings5, interface IMsRdpClient5
- Services Bureau à distance de l’interface IMsRdpClient5, propriété AdvancedSettings5
- Services Bureau à distance de la propriété AdvancedSettings5, interface IMsRdpClient6
- Services Bureau à distance de l’interface IMsRdpClient6, propriété AdvancedSettings5
- Services Bureau à distance de la propriété AdvancedSettings5, interface IMsRdpClient7
- Services Bureau à distance de l’interface IMsRdpClient7, propriété AdvancedSettings5
- Services Bureau à distance de la propriété AdvancedSettings5, interface IMsRdpClient8
- Services Bureau à distance de l’interface IMsRdpClient8, propriété AdvancedSettings5
- Services Bureau à distance de la propriété AdvancedSettings5, interface IMsRdpClient9
- Services Bureau à distance de l’interface IMsRdpClient9, propriété AdvancedSettings5
- Services Bureau à distance de la propriété AdvancedSettings5, interface IMsRdpClient10
- Services Bureau à distance de l’interface IMsRdpClient10, propriété AdvancedSettings5
topic_type:
- apiref
api_name:
- IMsRdpClient4.AdvancedSettings5
- IMsRdpClient4.get_AdvancedSettings5
- IMsRdpClient5.AdvancedSettings5
- IMsRdpClient5.get_AdvancedSettings5
- IMsRdpClient6.AdvancedSettings5
- IMsRdpClient6.get_AdvancedSettings5
- IMsRdpClient7.AdvancedSettings5
- IMsRdpClient7.get_AdvancedSettings5
- IMsRdpClient8.AdvancedSettings5
- IMsRdpClient8.get_AdvancedSettings5
- IMsRdpClient9.AdvancedSettings5
- IMsRdpClient9.get_AdvancedSettings5
- IMsRdpClient10.AdvancedSettings5
- IMsRdpClient10.get_AdvancedSettings5
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6ad96588b2109375aed23c1024ef925936cb3368
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104509402"
---
# <a name="imsrdpclient4advancedsettings5-property"></a>IMsRdpClient4 :: AdvancedSettings5, propriété

Récupère un pointeur vers une interface [**IMsRdpClientAdvancedSettings4**](imsrdpclientadvancedsettings4.md) .

Cette propriété est en lecture seule.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT get_AdvancedSettings5(
  [out] IMsRdpClientAdvancedSettings4 **ppAdvSettings
);
```



## <a name="property-value"></a>Valeur de la propriété

Pointeur vers l’interface [**IMsRdpClientAdvancedSettings4**](imsrdpclientadvancedsettings4.md) . L’interface peut être utilisée pour définir des paramètres avancés pour le contrôle client.

## <a name="error-codes"></a>Codes d’erreur

Si la méthode est réussie, **S \_ OK** est retourné. Toute autre valeur **HRESULT** indique que l’appel a échoué.

## <a name="remarks"></a>Notes

Cette propriété ne peut pas être définie lorsque le contrôle est connecté.

Pour plus d’informations sur la Connexion Bureau à distance par le Web, consultez [Requirements for connexion Bureau à distance par le Web](requirements-for-remote-desktop-web-connection.md).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Vista<br/>                                                               |
| Serveur minimal pris en charge<br/> | Windows Server 2008, Windows Server 2008 avec SP1<br/>                           |
| Bibliothèque de types<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |
| IID<br/>                      | IMsRdpClient4 est défini en tant que 095E0738-D97D-488b-B9F6-DD0E8D66C0DE<br/>            |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

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

 

 





