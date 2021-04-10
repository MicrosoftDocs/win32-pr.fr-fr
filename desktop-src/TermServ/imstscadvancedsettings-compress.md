---
title: IMsTscAdvancedSettings compression, propriété
description: Spécifie si la compression est activée.
ms.assetid: 274774b3-0442-4a46-95f8-7857f885bfdb
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de propriétés compress
- Compresser la propriété Services Bureau à distance, IMsTscAdvancedSettings, interface
- Services Bureau à distance de l’interface IMsTscAdvancedSettings, propriété Compress
- Compresser la propriété Services Bureau à distance, IMsRdpClientAdvancedSettings, interface
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings, propriété Compress
- Compresser la propriété Services Bureau à distance, IMsRdpClientAdvancedSettings2, interface
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings2, propriété Compress
- Compresser la propriété Services Bureau à distance, IMsRdpClientAdvancedSettings3, interface
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings3, propriété Compress
- Compresser la propriété Services Bureau à distance, IMsRdpClientAdvancedSettings4, interface
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings4, propriété Compress
- Compresser la propriété Services Bureau à distance, IMsRdpClientAdvancedSettings5, interface
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings5, propriété Compress
- Compresser la propriété Services Bureau à distance, IMsRdpClientAdvancedSettings6, interface
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings6, propriété Compress
- Compresser la propriété Services Bureau à distance, IMsRdpClientAdvancedSettings7, interface
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings7, propriété Compress
- Compresser la propriété Services Bureau à distance, IMsRdpClientAdvancedSettings8, interface
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings8, propriété Compress
topic_type:
- apiref
api_name:
- IMsTscAdvancedSettings.Compress
- IMsTscAdvancedSettings.get_Compress
- IMsTscAdvancedSettings.put_Compress
- IMsRdpClientAdvancedSettings.Compress
- IMsRdpClientAdvancedSettings.get_Compress
- IMsRdpClientAdvancedSettings.put_Compress
- IMsRdpClientAdvancedSettings2.Compress
- IMsRdpClientAdvancedSettings2.get_Compress
- IMsRdpClientAdvancedSettings2.put_Compress
- IMsRdpClientAdvancedSettings3.Compress
- IMsRdpClientAdvancedSettings3.get_Compress
- IMsRdpClientAdvancedSettings3.put_Compress
- IMsRdpClientAdvancedSettings4.Compress
- IMsRdpClientAdvancedSettings4.get_Compress
- IMsRdpClientAdvancedSettings4.put_Compress
- IMsRdpClientAdvancedSettings5.Compress
- IMsRdpClientAdvancedSettings5.get_Compress
- IMsRdpClientAdvancedSettings5.put_Compress
- IMsRdpClientAdvancedSettings6.Compress
- IMsRdpClientAdvancedSettings6.get_Compress
- IMsRdpClientAdvancedSettings6.put_Compress
- IMsRdpClientAdvancedSettings7.Compress
- IMsRdpClientAdvancedSettings7.get_Compress
- IMsRdpClientAdvancedSettings7.put_Compress
- IMsRdpClientAdvancedSettings8.Compress
- IMsRdpClientAdvancedSettings8.get_Compress
- IMsRdpClientAdvancedSettings8.put_Compress
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c588784d9b06bd2e8e1605a96c8aa9fd157c10eb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942330"
---
# <a name="imstscadvancedsettingscompress-property"></a>IMsTscAdvancedSettings :: compress, propriété

Spécifie si la compression est activée.

Cette propriété est en lecture/écriture.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT put_Compress(
  [in]  LONG compress
);

HRESULT get_Compress(
  [out] LONG *pcompress
);
```



## <a name="property-value"></a>Valeur de la propriété

Définissez ce paramètre sur 0 pour désactiver la compression ou sur une valeur différente de zéro pour activer la compression.

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

 

 





