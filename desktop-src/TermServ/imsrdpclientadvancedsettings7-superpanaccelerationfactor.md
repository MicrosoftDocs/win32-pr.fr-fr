---
title: IMsRdpClientAdvancedSettings7 propriété SuperPanAccelerationFactor
description: Spécifie ou récupère une valeur qui indique le facteur d’accélération SuperPan. Le facteur d’accélération SuperPan détermine la vitesse à laquelle l’écran effectue le panoramique en mode SuperPan.
ms.assetid: ce04f109-8a48-48ee-a553-728f12c09dde
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la propriété SuperPanAccelerationFactor
- Services Bureau à distance de la propriété SuperPanAccelerationFactor, interface IMsRdpClientAdvancedSettings7
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings7, propriété SuperPanAccelerationFactor
- Services Bureau à distance de la propriété SuperPanAccelerationFactor, interface IMsRdpClientAdvancedSettings8
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings8, propriété SuperPanAccelerationFactor
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings7.SuperPanAccelerationFactor
- IMsRdpClientAdvancedSettings7.get_SuperPanAccelerationFactor
- IMsRdpClientAdvancedSettings7.put_SuperPanAccelerationFactor
- IMsRdpClientAdvancedSettings8.SuperPanAccelerationFactor
- IMsRdpClientAdvancedSettings8.get_SuperPanAccelerationFactor
- IMsRdpClientAdvancedSettings8.put_SuperPanAccelerationFactor
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0919f3b1920980790203dc265e840e24a9315ae0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942887"
---
# <a name="imsrdpclientadvancedsettings7superpanaccelerationfactor-property"></a>IMsRdpClientAdvancedSettings7 :: SuperPanAccelerationFactor, propriété

Spécifie ou récupère une valeur qui indique le facteur d’accélération SuperPan. Le facteur d’accélération SuperPan détermine la vitesse à laquelle l’écran effectue le panoramique en mode SuperPan. Le facteur d’accélération est le nombre de pixels que l’affichage de l’écran défile dans une direction donnée pour chaque pixel de déplacement de la souris par le client.

Cette propriété est en lecture/écriture.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT put_SuperPanAccelerationFactor(
  [in]          ULONG uAccelFactor
);

HRESULT get_SuperPanAccelerationFactor(
  [out, retval] ULONG *puAccelFactor
);
```



## <a name="property-value"></a>Valeur de la propriété

Facteur d’accélération SuperPan à définir. Le facteur d’accélération SuperPan est le nombre de pixels que l’affichage de l’écran défile dans une direction donnée pour chaque pixel du mouvement de la souris.

## <a name="remarks"></a>Notes

Pour plus d’informations sur SuperPan, consultez [**EnableSuperPan**](imsrdpclientadvancedsettings7-enablesuperpan.md).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 7<br/>                                                                             |
| Serveur minimal pris en charge<br/> | Windows Server 2008 R2<br/>                                                                |
| Bibliothèque de types<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>           |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>           |
| IID<br/>                      | IID \_ IMsRdpClientAdvancedSettings7 est défini en tant que 26036036-4010-4578-8091-0db9a1edf9c3<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IMsRdpClientAdvancedSettings8**](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings7**](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[**EnableSuperPan**](imsrdpclientadvancedsettings7-enablesuperpan.md)
</dt> </dl>

 

 





