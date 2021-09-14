---
title: IMsRdpClientAdvancedSettings propriété CachePersistenceActive
description: Spécifie si la mise en cache des bitmaps persistante doit être utilisée. La mise en cache persistante peut améliorer les performances, mais nécessite de l’espace disque supplémentaire.
ms.assetid: 5eb986c4-98dd-426f-8d55-d3a9a526e1b2
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la propriété CachePersistenceActive
- Services Bureau à distance de la propriété CachePersistenceActive, interface IMsRdpClientAdvancedSettings
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings, propriété CachePersistenceActive
- Services Bureau à distance de la propriété CachePersistenceActive, interface IMsRdpClientAdvancedSettings2
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings2, propriété CachePersistenceActive
- Services Bureau à distance de la propriété CachePersistenceActive, interface IMsRdpClientAdvancedSettings3
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings3, propriété CachePersistenceActive
- Services Bureau à distance de la propriété CachePersistenceActive, interface IMsRdpClientAdvancedSettings4
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings4, propriété CachePersistenceActive
- Services Bureau à distance de la propriété CachePersistenceActive, interface IMsRdpClientAdvancedSettings5
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings5, propriété CachePersistenceActive
- Services Bureau à distance de la propriété CachePersistenceActive, interface IMsRdpClientAdvancedSettings6
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings6, propriété CachePersistenceActive
- Services Bureau à distance de la propriété CachePersistenceActive, interface IMsRdpClientAdvancedSettings7
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings7, propriété CachePersistenceActive
- Services Bureau à distance de la propriété CachePersistenceActive, interface IMsRdpClientAdvancedSettings8
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings8, propriété CachePersistenceActive
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings.CachePersistenceActive
- IMsRdpClientAdvancedSettings.get_CachePersistenceActive
- IMsRdpClientAdvancedSettings.put_CachePersistenceActive
- IMsRdpClientAdvancedSettings2.CachePersistenceActive
- IMsRdpClientAdvancedSettings2.get_CachePersistenceActive
- IMsRdpClientAdvancedSettings2.put_CachePersistenceActive
- IMsRdpClientAdvancedSettings3.CachePersistenceActive
- IMsRdpClientAdvancedSettings3.get_CachePersistenceActive
- IMsRdpClientAdvancedSettings3.put_CachePersistenceActive
- IMsRdpClientAdvancedSettings4.CachePersistenceActive
- IMsRdpClientAdvancedSettings4.get_CachePersistenceActive
- IMsRdpClientAdvancedSettings4.put_CachePersistenceActive
- IMsRdpClientAdvancedSettings5.CachePersistenceActive
- IMsRdpClientAdvancedSettings5.get_CachePersistenceActive
- IMsRdpClientAdvancedSettings5.put_CachePersistenceActive
- IMsRdpClientAdvancedSettings6.CachePersistenceActive
- IMsRdpClientAdvancedSettings6.get_CachePersistenceActive
- IMsRdpClientAdvancedSettings6.put_CachePersistenceActive
- IMsRdpClientAdvancedSettings7.CachePersistenceActive
- IMsRdpClientAdvancedSettings7.get_CachePersistenceActive
- IMsRdpClientAdvancedSettings7.put_CachePersistenceActive
- IMsRdpClientAdvancedSettings8.CachePersistenceActive
- IMsRdpClientAdvancedSettings8.get_CachePersistenceActive
- IMsRdpClientAdvancedSettings8.put_CachePersistenceActive
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fb34e90cc028e95c750a444d53f42c9c0ab77400
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127414601"
---
# <a name="imsrdpclientadvancedsettingscachepersistenceactive-property"></a>IMsRdpClientAdvancedSettings :: CachePersistenceActive, propriété

Spécifie si la mise en cache des bitmaps persistante doit être utilisée. La mise en cache persistante peut améliorer les performances, mais nécessite de l’espace disque supplémentaire.

Cette propriété est en lecture/écriture.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT put_CachePersistenceActive(
  [in]  LONG cachePersistenceActive
);

HRESULT get_CachePersistenceActive(
  [out] LONG *pcachePersistenceActive
);
```



## <a name="property-value"></a>Valeur de la propriété

Affectez à ce paramètre la valeur 0 pour désactiver la fonctionnalité ou une valeur différente de zéro pour activer la fonctionnalité.

## <a name="error-codes"></a>Codes d’erreur

Retourne **S \_ OK** en cas de réussite.

## <a name="remarks"></a>Notes

Pour plus d’informations sur la Connexion Bureau à distance par le Web, consultez [Requirements for connexion Bureau à distance par le Web](requirements-for-remote-desktop-web-connection.md).

## <a name="requirements"></a>Spécifications



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

 

 





