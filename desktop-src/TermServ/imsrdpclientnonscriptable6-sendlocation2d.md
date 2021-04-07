---
title: IMsRdpClientNonScriptable6 SendLocation2D, méthode
description: Envoie une valeur de latitude et de longitude au serveur afin que l’emplacement géographique du client puisse être reflété dans la session à distance.
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode SendLocation2D
- Méthode SendLocation2D Services Bureau à distance, interface IMsRdpClientNonScriptable6
- Services Bureau à distance de l’interface IMsRdpClientNonScriptable6, méthode SendLocation2D
topic_type:
- apiref
api_name:
- IMsRdpClientNonScriptable6.SendLocation2D
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 12/16/2020
ms.openlocfilehash: b706fdb35ba8360b294d25021c0c1a18bbe90188
ms.sourcegitcommit: 04e801237156e90b48111d60bddf437f87f5cdfe
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/19/2020
ms.locfileid: "103745341"
---
# <a name="imsrdpclientnonscriptable6sendlocation2d-method"></a>IMsRdpClientNonScriptable6 :: SendLocation2D, méthode

Envoie une valeur de latitude et de longitude au serveur afin que l’emplacement géographique du client puisse être reflété dans la session à distance.

## <a name="syntax"></a>Syntaxe

```C++
HRESULT SendLocation2D(
  [in] DOUBLE latitude,
  [in] DOUBLE longitude
);
```

## <a name="parameters"></a>Paramètres

*Latitude* \[ dans\]

Latitude d’un lieu géographique. La plage valide des valeurs de latitude est comprise entre-90,0 et 90,0 degrés.

*longitude* \[ dans\]

Longitude d’un emplacement géographique. La plage valide des valeurs de latitude est comprise entre-180,0 et 180,0 degrés.

## <a name="return-value"></a>Valeur retournée

Retourne **S \_ OK** en cas de réussite.

## <a name="requirements"></a>Configuration requise

| Condition requise | Valeur |
|-------------------------------------|---------------------------------------|
| Client minimal pris en charge| Windows 10, version 1709 (build 16299)      |
| Bibliothèque de types            | MsTscAx.dll                        |
| DLL                  | MsTscAx.dll     |
| IID                      | IID \_ IMsRdpClientNonScriptable6 est défini comme 05293249-B28B-4db8-BE64-1B2F496B910E            |

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IMsRdpClientNonScriptable6**](imsrdpclientnonscriptable6.md)
</dt> </dl>
