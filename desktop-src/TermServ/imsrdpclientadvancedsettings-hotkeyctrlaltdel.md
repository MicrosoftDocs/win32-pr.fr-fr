---
title: IMsRdpClientAdvancedSettings propriété HotKeyCtrlAltDel
description: Spécifie le code de la touche virtuelle à ajouter à CTRL + ALT pour déterminer le remplacement de la touche d’accès rapide pour CTRL + ALT + SUPPR, également appelé « séquence de sécurité sécurisée » (SAS).
ms.assetid: bce55cdb-4444-4291-b443-9bc1b3743e23
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la propriété HotKeyCtrlAltDel
- Services Bureau à distance de la propriété HotKeyCtrlAltDel, interface IMsRdpClientAdvancedSettings
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings, propriété HotKeyCtrlAltDel
- Services Bureau à distance de la propriété HotKeyCtrlAltDel, interface IMsRdpClientAdvancedSettings2
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings2, propriété HotKeyCtrlAltDel
- Services Bureau à distance de la propriété HotKeyCtrlAltDel, interface IMsRdpClientAdvancedSettings3
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings3, propriété HotKeyCtrlAltDel
- Services Bureau à distance de la propriété HotKeyCtrlAltDel, interface IMsRdpClientAdvancedSettings4
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings4, propriété HotKeyCtrlAltDel
- Services Bureau à distance de la propriété HotKeyCtrlAltDel, interface IMsRdpClientAdvancedSettings5
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings5, propriété HotKeyCtrlAltDel
- Services Bureau à distance de la propriété HotKeyCtrlAltDel, interface IMsRdpClientAdvancedSettings6
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings6, propriété HotKeyCtrlAltDel
- Services Bureau à distance de la propriété HotKeyCtrlAltDel, interface IMsRdpClientAdvancedSettings7
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings7, propriété HotKeyCtrlAltDel
- Services Bureau à distance de la propriété HotKeyCtrlAltDel, interface IMsRdpClientAdvancedSettings8
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings8, propriété HotKeyCtrlAltDel
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings.HotKeyCtrlAltDel
- IMsRdpClientAdvancedSettings.get_HotKeyCtrlAltDel
- IMsRdpClientAdvancedSettings.put_HotKeyCtrlAltDel
- IMsRdpClientAdvancedSettings2.HotKeyCtrlAltDel
- IMsRdpClientAdvancedSettings2.get_HotKeyCtrlAltDel
- IMsRdpClientAdvancedSettings2.put_HotKeyCtrlAltDel
- IMsRdpClientAdvancedSettings3.HotKeyCtrlAltDel
- IMsRdpClientAdvancedSettings3.get_HotKeyCtrlAltDel
- IMsRdpClientAdvancedSettings3.put_HotKeyCtrlAltDel
- IMsRdpClientAdvancedSettings4.HotKeyCtrlAltDel
- IMsRdpClientAdvancedSettings4.get_HotKeyCtrlAltDel
- IMsRdpClientAdvancedSettings4.put_HotKeyCtrlAltDel
- IMsRdpClientAdvancedSettings5.HotKeyCtrlAltDel
- IMsRdpClientAdvancedSettings5.get_HotKeyCtrlAltDel
- IMsRdpClientAdvancedSettings5.put_HotKeyCtrlAltDel
- IMsRdpClientAdvancedSettings6.HotKeyCtrlAltDel
- IMsRdpClientAdvancedSettings6.get_HotKeyCtrlAltDel
- IMsRdpClientAdvancedSettings6.put_HotKeyCtrlAltDel
- IMsRdpClientAdvancedSettings7.HotKeyCtrlAltDel
- IMsRdpClientAdvancedSettings7.get_HotKeyCtrlAltDel
- IMsRdpClientAdvancedSettings7.put_HotKeyCtrlAltDel
- IMsRdpClientAdvancedSettings8.HotKeyCtrlAltDel
- IMsRdpClientAdvancedSettings8.get_HotKeyCtrlAltDel
- IMsRdpClientAdvancedSettings8.put_HotKeyCtrlAltDel
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 47975b2c4586728fc4727044b7340d87c275c5a5f47aac1c68ab3d9fdafbda6c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119424409"
---
# <a name="imsrdpclientadvancedsettingshotkeyctrlaltdel-property"></a>IMsRdpClientAdvancedSettings :: HotKeyCtrlAltDel, propriété

Spécifie le code de la touche virtuelle à ajouter à CTRL + ALT pour déterminer le remplacement de la touche d’accès rapide pour CTRL + ALT + SUPPR, également appelé « séquence de sécurité sécurisée » (SAS).

> [!Note]  
> Les touches CTRL + ALT + SUPPR ne sont jamais redirigées vers le serveur distant, même lorsque la propriété [KeyboardHookMode](imsrdpclientsecuredsettings-keyboardhookmode.md) est activée ; CTRL + ALT + SUPPR est la séquence SAS locale.

 

Cette propriété est en lecture/écriture.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT put_HotKeyCtrlAltDel(
  [in]  LONG hotKeyCtrlAltDel
);

HRESULT get_HotKeyCtrlAltDel(
  [out] LONG *photKeyCtrlAltDel
);
```



## <a name="property-value"></a>Valeur de la propriété

Nouveau code de la clé virtuelle. **VK \_ END** est la valeur par défaut.

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

 

 





