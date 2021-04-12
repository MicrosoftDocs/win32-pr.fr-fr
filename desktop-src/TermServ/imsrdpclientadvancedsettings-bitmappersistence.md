---
title: IMsRdpClientAdvancedSettings propriété BitmapPersistence
description: Spécifie si la mise en cache des bitmaps persistante doit être utilisée. La mise en cache persistante peut améliorer les performances, mais nécessite de l’espace disque supplémentaire.
ms.assetid: ffaa9277-9dd7-4b2a-9de5-009b7e8766bc
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la propriété BitmapPersistence
- Services Bureau à distance de la propriété BitmapPersistence, interface IMsRdpClientAdvancedSettings
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings, propriété BitmapPersistence
- Services Bureau à distance de la propriété BitmapPersistence, interface IMsRdpClientAdvancedSettings2
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings2, propriété BitmapPersistence
- Services Bureau à distance de la propriété BitmapPersistence, interface IMsRdpClientAdvancedSettings3
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings3, propriété BitmapPersistence
- Services Bureau à distance de la propriété BitmapPersistence, interface IMsRdpClientAdvancedSettings4
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings4, propriété BitmapPersistence
- Services Bureau à distance de la propriété BitmapPersistence, interface IMsRdpClientAdvancedSettings5
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings5, propriété BitmapPersistence
- Services Bureau à distance de la propriété BitmapPersistence, interface IMsRdpClientAdvancedSettings6
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings6, propriété BitmapPersistence
- Services Bureau à distance de la propriété BitmapPersistence, interface IMsRdpClientAdvancedSettings7
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings7, propriété BitmapPersistence
- Services Bureau à distance de la propriété BitmapPersistence, interface IMsRdpClientAdvancedSettings8
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings8, propriété BitmapPersistence
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings.BitmapPersistence
- IMsRdpClientAdvancedSettings.get_BitmapPersistence
- IMsRdpClientAdvancedSettings.put_BitmapPersistence
- IMsRdpClientAdvancedSettings2.BitmapPersistence
- IMsRdpClientAdvancedSettings2.get_BitmapPersistence
- IMsRdpClientAdvancedSettings2.put_BitmapPersistence
- IMsRdpClientAdvancedSettings3.BitmapPersistence
- IMsRdpClientAdvancedSettings3.get_BitmapPersistence
- IMsRdpClientAdvancedSettings3.put_BitmapPersistence
- IMsRdpClientAdvancedSettings4.BitmapPersistence
- IMsRdpClientAdvancedSettings4.get_BitmapPersistence
- IMsRdpClientAdvancedSettings4.put_BitmapPersistence
- IMsRdpClientAdvancedSettings5.BitmapPersistence
- IMsRdpClientAdvancedSettings5.get_BitmapPersistence
- IMsRdpClientAdvancedSettings5.put_BitmapPersistence
- IMsRdpClientAdvancedSettings6.BitmapPersistence
- IMsRdpClientAdvancedSettings6.get_BitmapPersistence
- IMsRdpClientAdvancedSettings6.put_BitmapPersistence
- IMsRdpClientAdvancedSettings7.BitmapPersistence
- IMsRdpClientAdvancedSettings7.get_BitmapPersistence
- IMsRdpClientAdvancedSettings7.put_BitmapPersistence
- IMsRdpClientAdvancedSettings8.BitmapPersistence
- IMsRdpClientAdvancedSettings8.get_BitmapPersistence
- IMsRdpClientAdvancedSettings8.put_BitmapPersistence
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 65795b5217c785befe0db6ac529d5760a6211d4d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384323"
---
# <a name="imsrdpclientadvancedsettingsbitmappersistence-property"></a>IMsRdpClientAdvancedSettings :: BitmapPersistence, propriété

Spécifie si la mise en cache des bitmaps persistante doit être utilisée. La mise en cache persistante peut améliorer les performances, mais nécessite de l’espace disque supplémentaire.

Cette propriété est en lecture/écriture.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT put_BitmapPersistence(
  [in]  LONG bitmapPeristence
);

HRESULT get_BitmapPersistence(
  [out] LONG *pbitmapPeristence
);
```



## <a name="property-value"></a>Valeur de la propriété

Affectez à ce paramètre la valeur 0 pour désactiver la mise en cache ou une valeur différente de zéro pour activer la mise en cache.

> [!Note]  
> La faute d’orthographe dans le nom du paramètre se trouve dans la version finale du contrôle.

 

## <a name="error-codes"></a>Codes d’erreur

Retourne **S \_ OK** en cas de réussite.

## <a name="remarks"></a>Notes

Pour plus d’informations sur la Connexion Bureau à distance par le Web, consultez [Requirements for connexion Bureau à distance par le Web](requirements-for-remote-desktop-web-connection.md).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Vista<br/>                                                                        |
| Serveur minimal pris en charge<br/> | Windows Server 2008<br/>                                                                  |
| Bibliothèque de types<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>          |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>          |
| IID<br/>                      | IID \_ IMsRdpClientAdvancedSettings est défini en tant que 3c65b4ab-12b3-465B-ACD4-b8dad3bff9e2<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IMsRdpClientAdvancedSettings2**](imsrdpclientadvancedsettings2.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings3**](imstscadvancedsettings-interface.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings4**](imsrdpclientadvancedsettings4.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings5**](imsrdpclientadvancedsettings5.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings6**](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings7**](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings8**](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings**](imsrdpclientadvancedsettings-interface.md)
</dt> </dl>

 

 





