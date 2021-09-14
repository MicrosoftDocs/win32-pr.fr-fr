---
title: IMsRdpClientNonScriptable7 CameraRedirConfigCollection, propriété
description: Obtient la collection des appareils photo (et les configurations associées) qui sont disponibles pour la redirection.
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la propriété CameraRedirConfigCollection
- Services Bureau à distance de la propriété CameraRedirConfigCollection, interface IMsRdpClientNonScriptable7
- Services Bureau à distance de l’interface IMsRdpClientNonScriptable7, propriété CameraRedirConfigCollection
topic_type:
- apiref
api_name:
- IMsRdpClientNonScriptable7.CameraRedirConfigCollection
- IMsRdpClientNonScriptable7.get_CameraRedirConfigCollection
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 12/16/2020
ms.openlocfilehash: 817d3d73b4abbf8aa8b4126fd99ed7d11c3fff51
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126919912"
---
# <a name="imsrdpclientnonscriptable7cameraredirconfigcollection-property"></a>IMsRdpClientNonScriptable7 :: CameraRedirConfigCollection, propriété

Obtient la collection des appareils photo (et les configurations associées) qui sont disponibles pour la redirection.

Cette propriété est en lecture seule.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT get_CameraRedirConfigCollection(
  [out, retval] IMsRdpCameraRedirConfigCollection** ppCameraCollection
);
```

## <a name="property-value"></a>Valeur de la propriété

Un [IMsRdpCameraRedirConfigCollection](imsrdpcameraredirconfigcollection.md) qui représente la collection d’appareils photo (et les configurations associées) qui sont disponibles pour la redirection.

## <a name="requirements"></a>Spécifications

| Condition requise | Valeur |
|-------------------------------------|---------------------------------------|
| Client minimal pris en charge| Windows 10, version 1803 (build 17134)      |
| Bibliothèque de types            | MsTscAx.dll                        |
| DLL                  | MsTscAx.dll     |
| IID                      | IID \_ IMsRdpClientNonScriptable7 est défini en tant que 71B4A60A-fe21-46D8-A39B-8E32BA0C5ECC          |

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IMsRdpClientNonScriptable7**](imsrdpclientnonscriptable7.md)
</dt> </dl>