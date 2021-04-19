---
title: IMsRdpClientAdvancedSettings propriété HotKeyCtrlEsc
description: Spécifie le code de la touche virtuelle à ajouter à la touche ALT pour déterminer le remplacement du raccourci clavier pour CTRL + ESC.
ms.assetid: 55d20a97-ce6e-4394-bfdf-c5bc880e7e2f
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la propriété HotKeyCtrlEsc
- Services Bureau à distance de la propriété HotKeyCtrlEsc, interface IMsRdpClientAdvancedSettings
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings, propriété HotKeyCtrlEsc
- Services Bureau à distance de la propriété HotKeyCtrlEsc, interface IMsRdpClientAdvancedSettings2
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings2, propriété HotKeyCtrlEsc
- Services Bureau à distance de la propriété HotKeyCtrlEsc, interface IMsRdpClientAdvancedSettings3
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings3, propriété HotKeyCtrlEsc
- Services Bureau à distance de la propriété HotKeyCtrlEsc, interface IMsRdpClientAdvancedSettings4
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings4, propriété HotKeyCtrlEsc
- Services Bureau à distance de la propriété HotKeyCtrlEsc, interface IMsRdpClientAdvancedSettings5
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings5, propriété HotKeyCtrlEsc
- Services Bureau à distance de la propriété HotKeyCtrlEsc, interface IMsRdpClientAdvancedSettings6
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings6, propriété HotKeyCtrlEsc
- Services Bureau à distance de la propriété HotKeyCtrlEsc, interface IMsRdpClientAdvancedSettings7
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings7, propriété HotKeyCtrlEsc
- Services Bureau à distance de la propriété HotKeyCtrlEsc, interface IMsRdpClientAdvancedSettings8
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings8, propriété HotKeyCtrlEsc
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings.HotKeyCtrlEsc
- IMsRdpClientAdvancedSettings.get_HotKeyCtrlEsc
- IMsRdpClientAdvancedSettings.put_HotKeyCtrlEsc
- IMsRdpClientAdvancedSettings2.HotKeyCtrlEsc
- IMsRdpClientAdvancedSettings2.get_HotKeyCtrlEsc
- IMsRdpClientAdvancedSettings2.put_HotKeyCtrlEsc
- IMsRdpClientAdvancedSettings3.HotKeyCtrlEsc
- IMsRdpClientAdvancedSettings3.get_HotKeyCtrlEsc
- IMsRdpClientAdvancedSettings3.put_HotKeyCtrlEsc
- IMsRdpClientAdvancedSettings4.HotKeyCtrlEsc
- IMsRdpClientAdvancedSettings4.get_HotKeyCtrlEsc
- IMsRdpClientAdvancedSettings4.put_HotKeyCtrlEsc
- IMsRdpClientAdvancedSettings5.HotKeyCtrlEsc
- IMsRdpClientAdvancedSettings5.get_HotKeyCtrlEsc
- IMsRdpClientAdvancedSettings5.put_HotKeyCtrlEsc
- IMsRdpClientAdvancedSettings6.HotKeyCtrlEsc
- IMsRdpClientAdvancedSettings6.get_HotKeyCtrlEsc
- IMsRdpClientAdvancedSettings6.put_HotKeyCtrlEsc
- IMsRdpClientAdvancedSettings7.HotKeyCtrlEsc
- IMsRdpClientAdvancedSettings7.get_HotKeyCtrlEsc
- IMsRdpClientAdvancedSettings7.put_HotKeyCtrlEsc
- IMsRdpClientAdvancedSettings8.HotKeyCtrlEsc
- IMsRdpClientAdvancedSettings8.get_HotKeyCtrlEsc
- IMsRdpClientAdvancedSettings8.put_HotKeyCtrlEsc
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cf1a806430e8b93503c7cdc0fef04ba3f0a59b20
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106510535"
---
# <a name="imsrdpclientadvancedsettingshotkeyctrlesc-property"></a>IMsRdpClientAdvancedSettings :: HotKeyCtrlEsc, propriété

Spécifie le code de la touche virtuelle à ajouter à la touche ALT pour déterminer le remplacement du raccourci clavier pour CTRL + ESC.

Cette propriété est valide uniquement lorsque la propriété [**KeyboardHookMode**](imsrdpclientsecuredsettings-keyboardhookmode.md) n’est pas activée.

Cette propriété est en lecture/écriture.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT put_HotKeyCtrlEsc(
  [in]  LONG hotKeyCtrlEsc
);

HRESULT get_HotKeyCtrlEsc(
  [out] LONG *photKeyCtrlEsc
);
```



## <a name="property-value"></a>Valeur de la propriété

Nouveau code de la clé virtuelle. **VK \_ Page d’hébergement** est la valeur par défaut, avec Alt + début comme séquence résultante.

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

 

 





