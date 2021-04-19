---
title: IMsTscAdvancedSettings propriété DisableRdpdr
description: Spécifie si l’imprimante et la redirection du presse-papiers sont activées.
ms.assetid: 63e0e024-4792-4efe-a6c5-d122f8adcb0a
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la propriété DisableRdpdr
- Services Bureau à distance de la propriété DisableRdpdr, interface IMsTscAdvancedSettings
- Services Bureau à distance de l’interface IMsTscAdvancedSettings, propriété DisableRdpdr
- Services Bureau à distance de la propriété DisableRdpdr, interface IMsRdpClientAdvancedSettings
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings, propriété DisableRdpdr
- Services Bureau à distance de la propriété DisableRdpdr, interface IMsRdpClientAdvancedSettings2
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings2, propriété DisableRdpdr
- Services Bureau à distance de la propriété DisableRdpdr, interface IMsRdpClientAdvancedSettings3
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings3, propriété DisableRdpdr
- Services Bureau à distance de la propriété DisableRdpdr, interface IMsRdpClientAdvancedSettings4
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings4, propriété DisableRdpdr
- Services Bureau à distance de la propriété DisableRdpdr, interface IMsRdpClientAdvancedSettings5
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings5, propriété DisableRdpdr
- Services Bureau à distance de la propriété DisableRdpdr, interface IMsRdpClientAdvancedSettings6
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings6, propriété DisableRdpdr
- Services Bureau à distance de la propriété DisableRdpdr, interface IMsRdpClientAdvancedSettings7
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings7, propriété DisableRdpdr
- Services Bureau à distance de la propriété DisableRdpdr, interface IMsRdpClientAdvancedSettings8
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings8, propriété DisableRdpdr
topic_type:
- apiref
api_name:
- IMsTscAdvancedSettings.DisableRdpdr
- IMsTscAdvancedSettings.get_DisableRdpdr
- IMsTscAdvancedSettings.put_DisableRdpdr
- IMsRdpClientAdvancedSettings.DisableRdpdr
- IMsRdpClientAdvancedSettings.get_DisableRdpdr
- IMsRdpClientAdvancedSettings.put_DisableRdpdr
- IMsRdpClientAdvancedSettings2.DisableRdpdr
- IMsRdpClientAdvancedSettings2.get_DisableRdpdr
- IMsRdpClientAdvancedSettings2.put_DisableRdpdr
- IMsRdpClientAdvancedSettings3.DisableRdpdr
- IMsRdpClientAdvancedSettings3.get_DisableRdpdr
- IMsRdpClientAdvancedSettings3.put_DisableRdpdr
- IMsRdpClientAdvancedSettings4.DisableRdpdr
- IMsRdpClientAdvancedSettings4.get_DisableRdpdr
- IMsRdpClientAdvancedSettings4.put_DisableRdpdr
- IMsRdpClientAdvancedSettings5.DisableRdpdr
- IMsRdpClientAdvancedSettings5.get_DisableRdpdr
- IMsRdpClientAdvancedSettings5.put_DisableRdpdr
- IMsRdpClientAdvancedSettings6.DisableRdpdr
- IMsRdpClientAdvancedSettings6.get_DisableRdpdr
- IMsRdpClientAdvancedSettings6.put_DisableRdpdr
- IMsRdpClientAdvancedSettings7.DisableRdpdr
- IMsRdpClientAdvancedSettings7.get_DisableRdpdr
- IMsRdpClientAdvancedSettings7.put_DisableRdpdr
- IMsRdpClientAdvancedSettings8.DisableRdpdr
- IMsRdpClientAdvancedSettings8.get_DisableRdpdr
- IMsRdpClientAdvancedSettings8.put_DisableRdpdr
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0747f37cd5e85c62946c9b8e3a1587f736dd8af9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106518086"
---
# <a name="imstscadvancedsettingsdisablerdpdr-property"></a>IMsTscAdvancedSettings ::D propriété isableRdpdr

Spécifie si l’imprimante et la redirection du presse-papiers sont activées.

Cette propriété est en lecture/écriture.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT put_DisableRdpdr(
  [in]  BOOL DisableRdpdr
);

HRESULT get_DisableRdpdr(
  [out] BOOL *pDisableRdpdr
);
```



## <a name="property-value"></a>Valeur de la propriété

Affectez la valeur **true** à ce paramètre pour désactiver la redirection ou **false** pour activer la redirection.

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

 

 





