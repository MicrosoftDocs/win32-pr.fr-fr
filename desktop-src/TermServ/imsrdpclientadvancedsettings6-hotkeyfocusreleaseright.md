---
title: IMsRdpClientAdvancedSettings6 propriété HotKeyFocusReleaseRight
description: Spécifie le code de la touche virtuelle à ajouter à Ctrl + Alt pour déterminer le remplacement des raccourcis clavier pour Ctrl + Alt + droite.
ms.assetid: 9AEEB712-E4C4-435E-A847-40C2B3A41C15
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la propriété HotKeyFocusReleaseRight
- Services Bureau à distance de la propriété HotKeyFocusReleaseRight, interface IMsRdpClientAdvancedSettings6
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings6, propriété HotKeyFocusReleaseRight
- Services Bureau à distance de la propriété HotKeyFocusReleaseRight, interface IMsRdpClientAdvancedSettings7
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings7, propriété HotKeyFocusReleaseRight
- Services Bureau à distance de la propriété HotKeyFocusReleaseRight, interface IMsRdpClientAdvancedSettings8
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings8, propriété HotKeyFocusReleaseRight
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings6.HotKeyFocusReleaseRight
- IMsRdpClientAdvancedSettings6.get_HotKeyFocusReleaseRight
- IMsRdpClientAdvancedSettings6.put_HotKeyFocusReleaseRight
- IMsRdpClientAdvancedSettings7.HotKeyFocusReleaseRight
- IMsRdpClientAdvancedSettings7.get_HotKeyFocusReleaseRight
- IMsRdpClientAdvancedSettings7.put_HotKeyFocusReleaseRight
- IMsRdpClientAdvancedSettings8.HotKeyFocusReleaseRight
- IMsRdpClientAdvancedSettings8.get_HotKeyFocusReleaseRight
- IMsRdpClientAdvancedSettings8.put_HotKeyFocusReleaseRight
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c2ce11df170b8b0a0a9a3f58a625955cecb41973
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106513036"
---
# <a name="imsrdpclientadvancedsettings6hotkeyfocusreleaseright-property"></a>IMsRdpClientAdvancedSettings6 :: HotKeyFocusReleaseRight, propriété

Spécifie le code de la touche virtuelle à ajouter à Ctrl + Alt pour déterminer le remplacement des raccourcis clavier pour Ctrl + Alt + droite.

Cette propriété est en lecture/écriture.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT put_HotKeyFocusReleaseRight(
  [in]  LONG hotKeyFocusReleaseRight
);

HRESULT get_HotKeyFocusReleaseRight(
  [out] LONG *hotKeyFocusReleaseRight
);
```



## <a name="property-value"></a>Valeur de la propriété

Nouveau code de la clé virtuelle.

## <a name="remarks"></a>Notes

Cette propriété est uniquement prise en charge par les clients Connexion Bureau à distance 6,1 et 7,0.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Vista<br/>                                                                         |
| Serveur minimal pris en charge<br/> | Windows Server 2008<br/>                                                                   |
| Bibliothèque de types<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>           |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>           |
| IID<br/>                      | IID \_ IMsRdpClientAdvancedSettings6 est défini en tant que 222c4b5d-45d9-4DF0-a7c6-60cf9089d285<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IMsRdpClientAdvancedSettings7**](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings8**](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings6**](imsrdpclientadvancedsettings6.md)
</dt> </dl>

 

 





