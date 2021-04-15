---
title: IMsRdpCameraRedirConfig, interface
description: Représente les configurations pour une caméra qui est disponible pour la redirection.
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de l’interface IMsRdpCameraRedirConfig
- Services Bureau à distance de l’interface IMsRdpCameraRedirConfig, Description
topic_type:
- apiref
api_name:
- IMsRdpCameraRedirConfig
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 12/16/2020
ms.openlocfilehash: fbb0f3344e0653ea4a87c876bb8ca7b8a67e7d21
ms.sourcegitcommit: 04e801237156e90b48111d60bddf437f87f5cdfe
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/19/2020
ms.locfileid: "104520308"
---
# <a name="imsrdpcameraredirconfig-interface"></a>IMsRdpCameraRedirConfig, interface

Représente les configurations pour une caméra qui est disponible pour la redirection.

## <a name="members"></a>Membres

L’interface **IMsRdpCameraRedirConfig** hérite de **IUnknown**. **IMsRdpCameraRedirConfig** a également les types de membres suivants :

- [Propriétés](#properties)

### <a name="properties"></a>Propriétés

L’interface **IMsRdpCameraRedirConfig** possède les propriétés suivantes.

| Propriété         | Type d’accès           | Description            |
|:-----------------|:----------------------|:-----------------------|
| [**DeviceExists**](imsrdpcameraredirconfig-deviceexists.md)      | Lecture seule | Spécifie si le périphérique de l’appareil photo existe actuellement (c’est-à-dire que l’appareil photo est connecté).   |
| [**FriendlyName**](imsrdpcameraredirconfig-friendlyname.md)                       | Lecture seule |    Obtient le nom convivial de l’appareil photo.    |
| [**InstanceId**](imsrdpcameraredirconfig-instanceid.md)      | Lecture seule |  Obtient l’ID d’instance de l’appareil photo.  |
| [**ParentInstanceId**](imsrdpcameraredirconfig-parentinstanceid.md)                       | Lecture seule |    Obtient l’ID d’instance d’appareil parent de l’appareil photo.   |
| [**Redirected**](imsrdpcameraredirconfig-redirected.md)      | Lecture/écriture |  Spécifie si l’appareil photo est redirigé.  |
| [**SymbolicLink**](imsrdpcameraredirconfig-symboliclink.md)                       | Lecture seule |   Obtient le lien symbolique de l’interface **KSCATEGORY_VIDEO_CAMERA** pour l’appareil photo.   |

## <a name="requirements"></a>Configuration requise

| Condition requise | Valeur |
|-------------------------------------|---------------------------------------|
| Client minimal pris en charge| Windows 10, version 1803 (build 17134)      |
| Bibliothèque de types            | MsTscAx.dll                        |
| DLL                  | MsTscAx.dll     |
| IID                      | IID \_ IMsRdpCameraRedirConfig est défini comme 09750604-D625-47C1-9FCD-F09F735705D7            |

## <a name="see-also"></a>Voir aussi

- [**IMsRdpCameraRedirConfigCollection**](imsrdpcameraredirconfigcollection.md)
- [**IMsRdpClientNonScriptable7::CameraRedirConfigCollection**](imsrdpclientnonscriptable7-cameraredirconfigcollection.md)