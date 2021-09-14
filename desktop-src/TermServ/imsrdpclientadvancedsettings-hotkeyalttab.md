---
title: IMsRdpClientAdvancedSettings propriété HotKeyAltTab
description: Spécifie le code de la touche virtuelle à ajouter à la touche ALT pour déterminer le remplacement du raccourci clavier pour ALT + TAB.
ms.assetid: d7066fb4-f53f-4e55-ba12-fb4078ece144
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la propriété HotKeyAltTab
- Services Bureau à distance de la propriété HotKeyAltTab, interface IMsRdpClientAdvancedSettings
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings, propriété HotKeyAltTab
- Services Bureau à distance de la propriété HotKeyAltTab, interface IMsRdpClientAdvancedSettings2
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings2, propriété HotKeyAltTab
- Services Bureau à distance de la propriété HotKeyAltTab, interface IMsRdpClientAdvancedSettings3
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings3, propriété HotKeyAltTab
- Services Bureau à distance de la propriété HotKeyAltTab, interface IMsRdpClientAdvancedSettings4
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings4, propriété HotKeyAltTab
- Services Bureau à distance de la propriété HotKeyAltTab, interface IMsRdpClientAdvancedSettings5
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings5, propriété HotKeyAltTab
- Services Bureau à distance de la propriété HotKeyAltTab, interface IMsRdpClientAdvancedSettings6
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings6, propriété HotKeyAltTab
- Services Bureau à distance de la propriété HotKeyAltTab, interface IMsRdpClientAdvancedSettings7
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings7, propriété HotKeyAltTab
- Services Bureau à distance de la propriété HotKeyAltTab, interface IMsRdpClientAdvancedSettings8
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings8, propriété HotKeyAltTab
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings.HotKeyAltTab
- IMsRdpClientAdvancedSettings.get_HotKeyAltTab
- IMsRdpClientAdvancedSettings.put_HotKeyAltTab
- IMsRdpClientAdvancedSettings2.HotKeyAltTab
- IMsRdpClientAdvancedSettings2.get_HotKeyAltTab
- IMsRdpClientAdvancedSettings2.put_HotKeyAltTab
- IMsRdpClientAdvancedSettings3.HotKeyAltTab
- IMsRdpClientAdvancedSettings3.get_HotKeyAltTab
- IMsRdpClientAdvancedSettings3.put_HotKeyAltTab
- IMsRdpClientAdvancedSettings4.HotKeyAltTab
- IMsRdpClientAdvancedSettings4.get_HotKeyAltTab
- IMsRdpClientAdvancedSettings4.put_HotKeyAltTab
- IMsRdpClientAdvancedSettings5.HotKeyAltTab
- IMsRdpClientAdvancedSettings5.get_HotKeyAltTab
- IMsRdpClientAdvancedSettings5.put_HotKeyAltTab
- IMsRdpClientAdvancedSettings6.HotKeyAltTab
- IMsRdpClientAdvancedSettings6.get_HotKeyAltTab
- IMsRdpClientAdvancedSettings6.put_HotKeyAltTab
- IMsRdpClientAdvancedSettings7.HotKeyAltTab
- IMsRdpClientAdvancedSettings7.get_HotKeyAltTab
- IMsRdpClientAdvancedSettings7.put_HotKeyAltTab
- IMsRdpClientAdvancedSettings8.HotKeyAltTab
- IMsRdpClientAdvancedSettings8.get_HotKeyAltTab
- IMsRdpClientAdvancedSettings8.put_HotKeyAltTab
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eec7834a95b83ec43553d0ced1e056860cfb5abe
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127008629"
---
# <a name="imsrdpclientadvancedsettingshotkeyalttab-property"></a>IMsRdpClientAdvancedSettings :: HotKeyAltTab, propriété

Spécifie le code de la touche virtuelle à ajouter à la touche ALT pour déterminer le remplacement du raccourci clavier pour ALT + TAB.

Cette propriété est valide uniquement lorsque la propriété [**KeyboardHookMode**](imsrdpclientsecuredsettings-keyboardhookmode.md) n’est pas activée.

Cette propriété est en lecture/écriture.

## <a name="syntax"></a>Syntax


```C++
HRESULT put_HotKeyAltTab(
  [in]  LONG hotKeyAltTab
);

HRESULT get_HotKeyAltTab(
  [out] LONG *photKeyAltTab
);
```



## <a name="property-value"></a>Valeur de la propriété

Nouveau code de la clé virtuelle. **VK \_ AVANT** , il s’agit de la valeur par défaut, avec Alt + Pg. précédent comme séquence résultante.

## <a name="error-codes"></a>Codes d’erreur

Retourne **S \_ OK** en cas de réussite.

## <a name="remarks"></a>Remarques

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

 

 





