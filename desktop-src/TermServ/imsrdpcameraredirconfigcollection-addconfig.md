---
title: IMsRdpCameraRedirConfigCollection AddConfig, méthode
description: Ajoute un objet IMsRdpCameraRedirConfig à la collection (la caméra correspondante n’a pas besoin d’être connectée).
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode AddConfig
- Méthode AddConfig Services Bureau à distance, interface IMsRdpCameraRedirConfigCollection
- Services Bureau à distance de l’interface IMsRdpCameraRedirConfigCollection, méthode AddConfig
topic_type:
- apiref
api_name:
- IMsRdpCameraRedirConfigCollection.AddConfig
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 12/16/2020
ms.openlocfilehash: e8c954b710c3f35bca9685d461e478104dac9039
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126917003"
---
# <a name="imsrdpcameraredirconfigcollectionaddconfig-method"></a>IMsRdpCameraRedirConfigCollection :: AddConfig, méthode

Ajoute un objet [IMsRdpCameraRedirConfig](imsrdpcameraredirconfig.md) à la collection (la caméra correspondante n’a pas besoin d’être connectée).

## <a name="syntax"></a>Syntaxe

```C++
HRESULT AddConfig(
    [in] BSTR symbolicLink,
    [in] VARIANT_BOOL fRedirected
);
```

## <a name="parameters"></a>Paramètres

*symbolicLink* \[ dans\]

Lien symbolique pour le nouvel objet [IMsRdpCameraRedirConfig](imsrdpcameraredirconfig.md) .

*fRedirected* \[ dans\]

Spécifie si la nouvelle caméra est redirigée par défaut.

## <a name="return-value"></a>Valeur de retour

Retourne **S \_ OK** en cas de réussite.

## <a name="requirements"></a>Spécifications

| Condition requise | Valeur |
|-------------------------------------|---------------------------------------|
| Client minimal pris en charge| Windows 10, version 1803 (build 17134)      |
| Bibliothèque de types            | MsTscAx.dll                        |
| DLL                  | MsTscAx.dll     |
| IID                      | IID \_ IMsRdpCameraRedirConfigCollection est défini en tant que AE45252B-aaab-4504-B681-649D6073A37A          |

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IMsRdpCameraRedirConfigCollection**](imsrdpcameraredirconfigcollection.md)
</dt> </dl>