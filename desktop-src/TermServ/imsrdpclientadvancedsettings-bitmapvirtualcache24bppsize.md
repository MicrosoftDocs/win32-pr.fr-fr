---
title: IMsRdpClientAdvancedSettings propriété BitmapVirtualCache24BppSize
description: Spécifie la taille, en mégaoctets, du fichier cache de bitmaps persistant à utiliser pour le paramètre de haute couleur 24 bits par pixel.
ms.assetid: 5891c90d-f463-4f27-b212-351ebf21ae00
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la propriété BitmapVirtualCache24BppSize
- Services Bureau à distance de la propriété BitmapVirtualCache24BppSize, interface IMsRdpClientAdvancedSettings
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings, propriété BitmapVirtualCache24BppSize
- Services Bureau à distance de la propriété BitmapVirtualCache24BppSize, interface IMsRdpClientAdvancedSettings2
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings2, propriété BitmapVirtualCache24BppSize
- Services Bureau à distance de la propriété BitmapVirtualCache24BppSize, interface IMsRdpClientAdvancedSettings3
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings3, propriété BitmapVirtualCache24BppSize
- Services Bureau à distance de la propriété BitmapVirtualCache24BppSize, interface IMsRdpClientAdvancedSettings4
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings4, propriété BitmapVirtualCache24BppSize
- Services Bureau à distance de la propriété BitmapVirtualCache24BppSize, interface IMsRdpClientAdvancedSettings5
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings5, propriété BitmapVirtualCache24BppSize
- Services Bureau à distance de la propriété BitmapVirtualCache24BppSize, interface IMsRdpClientAdvancedSettings6
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings6, propriété BitmapVirtualCache24BppSize
- Services Bureau à distance de la propriété BitmapVirtualCache24BppSize, interface IMsRdpClientAdvancedSettings7
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings7, propriété BitmapVirtualCache24BppSize
- Services Bureau à distance de la propriété BitmapVirtualCache24BppSize, interface IMsRdpClientAdvancedSettings8
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings8, propriété BitmapVirtualCache24BppSize
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings.BitmapVirtualCache24BppSize
- IMsRdpClientAdvancedSettings.get_BitmapVirtualCache24BppSize
- IMsRdpClientAdvancedSettings.put_BitmapVirtualCache24BppSize
- IMsRdpClientAdvancedSettings2.BitmapVirtualCache24BppSize
- IMsRdpClientAdvancedSettings2.get_BitmapVirtualCache24BppSize
- IMsRdpClientAdvancedSettings2.put_BitmapVirtualCache24BppSize
- IMsRdpClientAdvancedSettings3.BitmapVirtualCache24BppSize
- IMsRdpClientAdvancedSettings3.get_BitmapVirtualCache24BppSize
- IMsRdpClientAdvancedSettings3.put_BitmapVirtualCache24BppSize
- IMsRdpClientAdvancedSettings4.BitmapVirtualCache24BppSize
- IMsRdpClientAdvancedSettings4.get_BitmapVirtualCache24BppSize
- IMsRdpClientAdvancedSettings4.put_BitmapVirtualCache24BppSize
- IMsRdpClientAdvancedSettings5.BitmapVirtualCache24BppSize
- IMsRdpClientAdvancedSettings5.get_BitmapVirtualCache24BppSize
- IMsRdpClientAdvancedSettings5.put_BitmapVirtualCache24BppSize
- IMsRdpClientAdvancedSettings6.BitmapVirtualCache24BppSize
- IMsRdpClientAdvancedSettings6.get_BitmapVirtualCache24BppSize
- IMsRdpClientAdvancedSettings6.put_BitmapVirtualCache24BppSize
- IMsRdpClientAdvancedSettings7.BitmapVirtualCache24BppSize
- IMsRdpClientAdvancedSettings7.get_BitmapVirtualCache24BppSize
- IMsRdpClientAdvancedSettings7.put_BitmapVirtualCache24BppSize
- IMsRdpClientAdvancedSettings8.BitmapVirtualCache24BppSize
- IMsRdpClientAdvancedSettings8.get_BitmapVirtualCache24BppSize
- IMsRdpClientAdvancedSettings8.put_BitmapVirtualCache24BppSize
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d0fc31954ff191f795146e3894b0394b29484fb1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106540781"
---
# <a name="imsrdpclientadvancedsettingsbitmapvirtualcache24bppsize-property"></a>IMsRdpClientAdvancedSettings :: BitmapVirtualCache24BppSize, propriété

Spécifie la taille, en mégaoctets, du fichier cache de bitmaps persistant à utiliser pour le paramètre de haute couleur 24 bits par pixel.

Cette propriété est en lecture/écriture.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT put_BitmapVirtualCache24BppSize(
  [in]  LONG bitmapVirtualCache24BppSize
);

HRESULT get_BitmapVirtualCache24BppSize(
  [out] LONG *pbitmapVirtualCache24BppSize
);
```



## <a name="property-value"></a>Valeur de la propriété

Nouvelle taille du cache. Les valeurs valides sont comprises entre 1 et 32 inclus, et la valeur par défaut est 30. Notez que la taille maximale de tous les fichiers de cache virtuel est de 128 Mo.

## <a name="error-codes"></a>Codes d’erreur

Retourne **S \_ OK** en cas de réussite.

## <a name="remarks"></a>Notes

Les propriétés associées incluent les propriétés **BitmapVirtualCacheSize** et **BitmapVirtualCache16BppSize** .

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

 

 





