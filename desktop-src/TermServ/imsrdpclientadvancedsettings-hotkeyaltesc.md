---
title: IMsRdpClientAdvancedSettings propriété HotKeyAltEsc
description: Spécifie le code de la touche virtuelle à ajouter à la touche ALT pour déterminer le remplacement du raccourci clavier ALT + ÉCHAP.
ms.assetid: 17cae4ca-8e97-4713-bb4e-ac9a9876c16c
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la propriété HotKeyAltEsc
- Services Bureau à distance de la propriété HotKeyAltEsc, interface IMsRdpClientAdvancedSettings
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings, propriété HotKeyAltEsc
- Services Bureau à distance de la propriété HotKeyAltEsc, interface IMsRdpClientAdvancedSettings2
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings2, propriété HotKeyAltEsc
- Services Bureau à distance de la propriété HotKeyAltEsc, interface IMsRdpClientAdvancedSettings3
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings3, propriété HotKeyAltEsc
- Services Bureau à distance de la propriété HotKeyAltEsc, interface IMsRdpClientAdvancedSettings4
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings4, propriété HotKeyAltEsc
- Services Bureau à distance de la propriété HotKeyAltEsc, interface IMsRdpClientAdvancedSettings5
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings5, propriété HotKeyAltEsc
- Services Bureau à distance de la propriété HotKeyAltEsc, interface IMsRdpClientAdvancedSettings6
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings6, propriété HotKeyAltEsc
- Services Bureau à distance de la propriété HotKeyAltEsc, interface IMsRdpClientAdvancedSettings7
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings7, propriété HotKeyAltEsc
- Services Bureau à distance de la propriété HotKeyAltEsc, interface IMsRdpClientAdvancedSettings8
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings8, propriété HotKeyAltEsc
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings.HotKeyAltEsc
- IMsRdpClientAdvancedSettings.get_HotKeyAltEsc
- IMsRdpClientAdvancedSettings.put_HotKeyAltEsc
- IMsRdpClientAdvancedSettings2.HotKeyAltEsc
- IMsRdpClientAdvancedSettings2.get_HotKeyAltEsc
- IMsRdpClientAdvancedSettings2.put_HotKeyAltEsc
- IMsRdpClientAdvancedSettings3.HotKeyAltEsc
- IMsRdpClientAdvancedSettings3.get_HotKeyAltEsc
- IMsRdpClientAdvancedSettings3.put_HotKeyAltEsc
- IMsRdpClientAdvancedSettings4.HotKeyAltEsc
- IMsRdpClientAdvancedSettings4.get_HotKeyAltEsc
- IMsRdpClientAdvancedSettings4.put_HotKeyAltEsc
- IMsRdpClientAdvancedSettings5.HotKeyAltEsc
- IMsRdpClientAdvancedSettings5.get_HotKeyAltEsc
- IMsRdpClientAdvancedSettings5.put_HotKeyAltEsc
- IMsRdpClientAdvancedSettings6.HotKeyAltEsc
- IMsRdpClientAdvancedSettings6.get_HotKeyAltEsc
- IMsRdpClientAdvancedSettings6.put_HotKeyAltEsc
- IMsRdpClientAdvancedSettings7.HotKeyAltEsc
- IMsRdpClientAdvancedSettings7.get_HotKeyAltEsc
- IMsRdpClientAdvancedSettings7.put_HotKeyAltEsc
- IMsRdpClientAdvancedSettings8.HotKeyAltEsc
- IMsRdpClientAdvancedSettings8.get_HotKeyAltEsc
- IMsRdpClientAdvancedSettings8.put_HotKeyAltEsc
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8757a2c8ba35ad2ba3080f340126fd689704769682a72389806eb905ecbf9aae
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119475459"
---
# <a name="imsrdpclientadvancedsettingshotkeyaltesc-property"></a>IMsRdpClientAdvancedSettings :: HotKeyAltEsc, propriété

Spécifie le code de la touche virtuelle à ajouter à la touche ALT pour déterminer le remplacement du raccourci clavier ALT + ÉCHAP.

Cette propriété est valide uniquement lorsque la propriété [**KeyboardHookMode**](imsrdpclientsecuredsettings-keyboardhookmode.md) n’est pas activée.

Cette propriété est en lecture/écriture.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT put_HotKeyAltEsc(
  [in]  LONG hotKeyAltEsc
);

HRESULT get_HotKeyAltEsc(
  [out] LONG *photKeyAltEsc
);
```



## <a name="property-value"></a>Valeur de la propriété

Nouveau code de la clé virtuelle. **VK \_ INSERT** est la valeur par défaut, avec Alt + Inser comme séquence résultante.

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

 

 





