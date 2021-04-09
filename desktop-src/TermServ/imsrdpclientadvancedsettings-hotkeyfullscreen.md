---
title: IMsRdpClientAdvancedSettings propriété HotKeyFullScreen
description: Spécifie le code de la touche virtuelle à ajouter à CTRL + ALT pour déterminer le remplacement du raccourci clavier pour passer en mode plein écran.
ms.assetid: 75fda212-ec68-4b68-b7db-2bfcdee7a7de
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la propriété HotKeyFullScreen
- Services Bureau à distance de la propriété HotKeyFullScreen, interface IMsRdpClientAdvancedSettings
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings, propriété HotKeyFullScreen
- Services Bureau à distance de la propriété HotKeyFullScreen, interface IMsRdpClientAdvancedSettings2
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings2, propriété HotKeyFullScreen
- Services Bureau à distance de la propriété HotKeyFullScreen, interface IMsRdpClientAdvancedSettings3
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings3, propriété HotKeyFullScreen
- Services Bureau à distance de la propriété HotKeyFullScreen, interface IMsRdpClientAdvancedSettings4
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings4, propriété HotKeyFullScreen
- Services Bureau à distance de la propriété HotKeyFullScreen, interface IMsRdpClientAdvancedSettings5
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings5, propriété HotKeyFullScreen
- Services Bureau à distance de la propriété HotKeyFullScreen, interface IMsRdpClientAdvancedSettings6
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings6, propriété HotKeyFullScreen
- Services Bureau à distance de la propriété HotKeyFullScreen, interface IMsRdpClientAdvancedSettings7
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings7, propriété HotKeyFullScreen
- Services Bureau à distance de la propriété HotKeyFullScreen, interface IMsRdpClientAdvancedSettings8
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings8, propriété HotKeyFullScreen
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings.HotKeyFullScreen
- IMsRdpClientAdvancedSettings.get_HotKeyFullScreen
- IMsRdpClientAdvancedSettings.put_HotKeyFullScreen
- IMsRdpClientAdvancedSettings2.HotKeyFullScreen
- IMsRdpClientAdvancedSettings2.get_HotKeyFullScreen
- IMsRdpClientAdvancedSettings2.put_HotKeyFullScreen
- IMsRdpClientAdvancedSettings3.HotKeyFullScreen
- IMsRdpClientAdvancedSettings3.get_HotKeyFullScreen
- IMsRdpClientAdvancedSettings3.put_HotKeyFullScreen
- IMsRdpClientAdvancedSettings4.HotKeyFullScreen
- IMsRdpClientAdvancedSettings4.get_HotKeyFullScreen
- IMsRdpClientAdvancedSettings4.put_HotKeyFullScreen
- IMsRdpClientAdvancedSettings5.HotKeyFullScreen
- IMsRdpClientAdvancedSettings5.get_HotKeyFullScreen
- IMsRdpClientAdvancedSettings5.put_HotKeyFullScreen
- IMsRdpClientAdvancedSettings6.HotKeyFullScreen
- IMsRdpClientAdvancedSettings6.get_HotKeyFullScreen
- IMsRdpClientAdvancedSettings6.put_HotKeyFullScreen
- IMsRdpClientAdvancedSettings7.HotKeyFullScreen
- IMsRdpClientAdvancedSettings7.get_HotKeyFullScreen
- IMsRdpClientAdvancedSettings7.put_HotKeyFullScreen
- IMsRdpClientAdvancedSettings8.HotKeyFullScreen
- IMsRdpClientAdvancedSettings8.get_HotKeyFullScreen
- IMsRdpClientAdvancedSettings8.put_HotKeyFullScreen
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ed9c53dd0c6dff9e47b87ea8c8697c20b3613a14
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103941753"
---
# <a name="imsrdpclientadvancedsettingshotkeyfullscreen-property"></a>IMsRdpClientAdvancedSettings :: HotKeyFullScreen, propriété

Spécifie le code de la touche virtuelle à ajouter à CTRL + ALT pour déterminer le remplacement du raccourci clavier pour passer en mode plein écran.

Cette propriété est en lecture/écriture.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT put_HotKeyFullScreen(
  [in]  LONG hotKeyFullScreen
);

HRESULT get_HotKeyFullScreen(
  [out] LONG *photKeyFullScreen
);
```



## <a name="property-value"></a>Valeur de la propriété

Nouveau code de la clé virtuelle. **VK \_ CANCEL** est la valeur par défaut.

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

 

 





