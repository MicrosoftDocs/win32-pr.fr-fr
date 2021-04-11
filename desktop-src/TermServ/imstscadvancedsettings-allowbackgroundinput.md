---
title: IMsTscAdvancedSettings propriété allowBackgroundInput
description: Spécifie si le mode d’entrée d’arrière-plan est activé.
ms.assetid: 2b57ebe9-3aad-400c-bcfb-d01c759b453d
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la propriété allowBackgroundInput
- Services Bureau à distance de la propriété allowBackgroundInput, interface IMsTscAdvancedSettings
- Services Bureau à distance de l’interface IMsTscAdvancedSettings, propriété allowBackgroundInput
- Services Bureau à distance de la propriété allowBackgroundInput, interface IMsRdpClientAdvancedSettings
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings, propriété allowBackgroundInput
- Services Bureau à distance de la propriété allowBackgroundInput, interface IMsRdpClientAdvancedSettings2
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings2, propriété allowBackgroundInput
- Services Bureau à distance de la propriété allowBackgroundInput, interface IMsRdpClientAdvancedSettings3
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings3, propriété allowBackgroundInput
- Services Bureau à distance de la propriété allowBackgroundInput, interface IMsRdpClientAdvancedSettings4
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings4, propriété allowBackgroundInput
- Services Bureau à distance de la propriété allowBackgroundInput, interface IMsRdpClientAdvancedSettings5
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings5, propriété allowBackgroundInput
- Services Bureau à distance de la propriété allowBackgroundInput, interface IMsRdpClientAdvancedSettings6
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings6, propriété allowBackgroundInput
- Services Bureau à distance de la propriété allowBackgroundInput, interface IMsRdpClientAdvancedSettings7
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings7, propriété allowBackgroundInput
- Services Bureau à distance de la propriété allowBackgroundInput, interface IMsRdpClientAdvancedSettings8
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings8, propriété allowBackgroundInput
topic_type:
- apiref
api_name:
- IMsTscAdvancedSettings.allowBackgroundInput
- IMsTscAdvancedSettings.get_allowBackgroundInput
- IMsTscAdvancedSettings.put_allowBackgroundInput
- IMsRdpClientAdvancedSettings.allowBackgroundInput
- IMsRdpClientAdvancedSettings.get_allowBackgroundInput
- IMsRdpClientAdvancedSettings.put_allowBackgroundInput
- IMsRdpClientAdvancedSettings2.allowBackgroundInput
- IMsRdpClientAdvancedSettings2.get_allowBackgroundInput
- IMsRdpClientAdvancedSettings2.put_allowBackgroundInput
- IMsRdpClientAdvancedSettings3.allowBackgroundInput
- IMsRdpClientAdvancedSettings3.get_allowBackgroundInput
- IMsRdpClientAdvancedSettings3.put_allowBackgroundInput
- IMsRdpClientAdvancedSettings4.allowBackgroundInput
- IMsRdpClientAdvancedSettings4.get_allowBackgroundInput
- IMsRdpClientAdvancedSettings4.put_allowBackgroundInput
- IMsRdpClientAdvancedSettings5.allowBackgroundInput
- IMsRdpClientAdvancedSettings5.get_allowBackgroundInput
- IMsRdpClientAdvancedSettings5.put_allowBackgroundInput
- IMsRdpClientAdvancedSettings6.allowBackgroundInput
- IMsRdpClientAdvancedSettings6.get_allowBackgroundInput
- IMsRdpClientAdvancedSettings6.put_allowBackgroundInput
- IMsRdpClientAdvancedSettings7.allowBackgroundInput
- IMsRdpClientAdvancedSettings7.get_allowBackgroundInput
- IMsRdpClientAdvancedSettings7.put_allowBackgroundInput
- IMsRdpClientAdvancedSettings8.allowBackgroundInput
- IMsRdpClientAdvancedSettings8.get_allowBackgroundInput
- IMsRdpClientAdvancedSettings8.put_allowBackgroundInput
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 938725ea1aa3d774d5993be695ac8568963897fb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104385247"
---
# <a name="imstscadvancedsettingsallowbackgroundinput-property"></a>IMsTscAdvancedSettings :: allowBackgroundInput, propriété

Spécifie si le mode d’entrée d’arrière-plan est activé. Lorsque l’entrée d’arrière-plan est activée, le client peut accepter l’entrée lorsque le client n’a pas le focus.

Cette propriété est en lecture/écriture.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT put_allowBackgroundInput(
  [in]  LONG allowBackgroundInput
);

HRESULT get_allowBackgroundInput(
  [out] LONG *pallowBackgroundInput
);
```



## <a name="property-value"></a>Valeur de la propriété

Affectez à ce paramètre la valeur 0 pour désactiver le mode de saisie en arrière-plan ou une valeur différente de zéro pour activer le mode d’entrée d’arrière-plan.

## <a name="error-codes"></a>Codes d’erreur

Retourne **S \_ OK** en cas de réussite.

## <a name="remarks"></a>Notes

Pour plus d’informations sur la Connexion Bureau à distance par le Web, consultez [Requirements for connexion Bureau à distance par le Web](requirements-for-remote-desktop-web-connection.md).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Vista<br/>                                                                  |
| Serveur minimal pris en charge<br/> | Windows Server 2008<br/>                                                            |
| Bibliothèque de types<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>    |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>    |
| IID<br/>                      | IID \_ IMsTscAdvancedSettings est défini en tant que 809945cc-4b3b-4a92-a6b0-dbf9b5f2ef2d<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IMsRdpClientAdvancedSettings**](imsrdpclientadvancedsettings-interface.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings2**](imsrdpclientadvancedsettings2.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings3**](imsrdpclientadvancedsettings3.md)
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

[**IMsTscAdvancedSettings**](imstscadvancedsettings-interface.md)
</dt> </dl>

 

 





