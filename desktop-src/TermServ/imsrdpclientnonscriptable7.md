---
title: IMsRdpClientNonScriptable7, interface
description: fournit l’accès aux propriétés qui ne sont pas scriptables de la session à distance d’un client sur le contrôle Bureau à distance ActiveX. Dérive de l’interface IMsRdpClientNonScriptable6.
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de l’interface IMsRdpClientNonScriptable7
- Services Bureau à distance de l’interface IMsRdpClientNonScriptable7, Description
topic_type:
- apiref
api_name:
- IMsRdpClientNonScriptable7
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 12/16/2020
ms.openlocfilehash: 01065ef73d1a23f0ac9416a39c4af74042c883e3b4d7f596cb95f6c01043f662
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117941106"
---
# <a name="imsrdpclientnonscriptable7-interface"></a>IMsRdpClientNonScriptable7, interface

fournit l’accès aux propriétés qui ne sont pas scriptables de la session à distance d’un client sur le contrôle Bureau à distance ActiveX. Dérive de l’interface [**IMsRdpClientNonScriptable6**](imsrdpclientnonscriptable6.md) . Les méthodes de cette interface sont accessibles uniquement par le biais de la vtable ; ils ne peuvent pas être utilisés pour des clients scriptables.

Une instance de cette interface est obtenue en appelant [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) sur l’objet [**IMsTscAx**](imstscax-interface.md) , en passant **IID \_ IMsRdpClientNonScriptable7**.

## <a name="members"></a>Membres

L’interface **IMsRdpClientNonScriptable7** hérite de [**IMsRdpClientNonScriptable6**](imsrdpclientnonscriptable5.md). **IMsRdpClientNonScriptable7** a également les types de membres suivants :

- [Méthodes](#methods)
- [Propriétés](#properties)

### <a name="methods"></a>Méthodes

L’interface **IMsRdpClientNonScriptable7** possède ces méthodes.


| Méthode            | Description              |
|:------------------|:-------------------------|
| [**DisableDpiCursorScalingForProcess**](imsrdpclientnonscriptable7-disabledpicursorscalingforprocess.md)       |  Désactive la mise à l’échelle locale du curseur de la souris reçue du serveur, garantissant ainsi un rendu correct de la forme du curseur sans modification.                   |

### <a name="properties"></a>Propriétés

L’interface **IMsRdpClientNonScriptable7** possède les propriétés suivantes.

| Propriété         | Type d’accès           | Description            |
|:-----------------|:----------------------|:-----------------------|
| [**CameraRedirConfigCollection**](imsrdpclientnonscriptable7-cameraredirconfigcollection.md)      | Lecture seule |  Obtient la collection des appareils photo (et les configurations associées) qui sont disponibles pour la redirection.   |
| [**Papier**](imsrdpclientnonscriptable7-clipboard.md)                       | Lecture seule |    Obtient le contrôleur du presse-papiers utilisé pour synchroniser les presse-papiers locaux et distants si la synchronisation manuelle du presse-papiers est activée.    |

## <a name="requirements"></a>Configuration requise

| Condition requise | Valeur |
|-------------------------------------|---------------------------------------|
| Client minimal pris en charge| Windows 10, version 1803 (build 17134)      |
| Bibliothèque de types            | MsTscAx.dll                        |
| DLL                  | MsTscAx.dll     |
| CLSID                    | Le CLSID \_ MsRdpClient12 est défini en tant que 0BDA33B8-9AF1-4065-989E-5A7F1ACF09D8<br/> Le CLSID \_ MsRdpClient12NotSafeForScripting est défini en tant que 3BB805C2-D9E2-4174-8A1E-C87D69563662<br/> Le CLSID \_ MsRdpClient11 est défini en tant que 22A7E88C-5BF5-4DE6-B687-60F7331DF190<br/> Le CLSID \_ MsRdpClient11NotSafeForScripting est défini en tant que 1DF7C823-B2D4-4B54-975A-F2AC5D7CF8B8<br/>  |
| IID                      | IID \_ IMsRdpClientNonScriptable7 est défini en tant que 71B4A60A-fe21-46D8-A39B-8E32BA0C5ECC            |

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IMsRdpClientNonScriptable6**](imsrdpclientnonscriptable6.md)
</dt> </dl>
