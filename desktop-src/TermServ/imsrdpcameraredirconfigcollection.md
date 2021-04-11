---
title: IMsRdpCameraRedirConfigCollection, interface
description: Représente la collection d’appareils photo (et les configurations associées) qui sont disponibles pour la redirection.
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de l’interface IMsRdpCameraRedirConfigCollection
- Services Bureau à distance de l’interface IMsRdpCameraRedirConfigCollection, Description
topic_type:
- apiref
api_name:
- IMsRdpCameraRedirConfigCollection
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 12/16/2020
ms.openlocfilehash: 3d97249a7485ec024ee3611809c87c5b6ed41143
ms.sourcegitcommit: 04e801237156e90b48111d60bddf437f87f5cdfe
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/19/2020
ms.locfileid: "104108355"
---
# <a name="imsrdpcameraredirconfigcollection-interface"></a>IMsRdpCameraRedirConfigCollection, interface

 Représente la collection d’appareils photo (et les configurations associées) qui sont disponibles pour la redirection.

## <a name="members"></a>Membres

L’interface **IMsRdpCameraRedirConfigCollection** hérite de **IUnknown**. **IMsRdpCameraRedirConfigCollection** a également les types de membres suivants :

- [Méthodes](#methods)
- [Propriétés](#properties)

### <a name="methods"></a>Méthodes

L’interface **IMsRdpCameraRedirConfigCollection** possède ces méthodes.

| Méthode            | Description              |
|:------------------|:-------------------------|
| [**AddConfig**](imsrdpcameraredirconfigcollection-addconfig.md)       |  Ajoute un objet [IMsRdpCameraRedirConfig](imsrdpcameraredirconfig.md) à la collection (la caméra correspondante n’a pas besoin d’être connectée).                   |
| [**Relancer**](imsrdpcameraredirconfigcollection-rescan.md)       |  Énumère les appareils photo connectés.                   |

### <a name="properties"></a>Propriétés

L’interface **IMsRdpCameraRedirConfigCollection** possède les propriétés suivantes.

| Propriété         | Type d’accès           | Description            |
|:-----------------|:----------------------|:-----------------------|
| [**ByIndex**](imsrdpcameraredirconfigcollection-byindex.md)      | Lecture seule |  Retourne un objet [IMsRdpCameraRedirConfig](imsrdpcameraredirconfig.md) par son index dans la collection.   |
| [**ByInstanceId**](imsrdpcameraredirconfigcollection-byinstanceid.md)                       | Lecture seule |    Retourne un objet [IMsRdpCameraRedirConfig](imsrdpcameraredirconfig.md) de la collection qui correspond à l’ID d’instance spécifié.    |
| [**BySymbolicLink**](imsrdpcameraredirconfigcollection-bysymboliclink.md)      | Lecture seule |  Retourne un objet [IMsRdpCameraRedirConfig](imsrdpcameraredirconfig.md) de la collection qui correspond au lien symbolique donné de l’interface **KSCATEGORY_VIDEO_CAMERA** pour l’appareil photo.  |
| [**Saut**](imsrdpcameraredirconfigcollection-count.md)                       | Lecture seule |    Retourne le nombre d’objets [IMsRdpCameraRedirConfig](imsrdpcameraredirconfig.md) dans la collection.   |
| [**EncodeVideo**](imsrdpcameraredirconfigcollection-encodevideo.md)      | Lecture/écriture |  Spécifie si le flux vidéo est au format H. 264 encodé.  |
| [**EncodingQuality**](imsrdpcameraredirconfigcollection-encodingquality.md)                       | Lecture/écriture |    Spécifie la qualité d’encodage (vitesse de transmission).   |
| [**RedirectByDefault**](imsrdpcameraredirconfigcollection-redirectbydefault.md)                       | Lecture/écriture |   Spécifie si une nouvelle caméra est redirigée par défaut.    |

## <a name="requirements"></a>Configuration requise

| Condition requise | Valeur |
|-------------------------------------|---------------------------------------|
| Client minimal pris en charge| Windows 10, version 1803 (build 17134)      |
| Bibliothèque de types            | MsTscAx.dll                        |
| DLL                  | MsTscAx.dll     |
| IID                      | IID \_ IMsRdpCameraRedirConfigCollection est défini en tant que AE45252B-aaab-4504-B681-649D6073A37A            |

## <a name="see-also"></a>Voir aussi

- [**IMsRdpCameraRedirConfig**](imsrdpcameraredirconfig.md)
- [**IMsRdpClientNonScriptable7::CameraRedirConfigCollection**](imsrdpclientnonscriptable7-cameraredirconfigcollection.md)
