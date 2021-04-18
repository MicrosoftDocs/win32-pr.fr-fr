---
description: L’interface IKeyFrameControl est implémentée par le MSP H. 323 et n’est disponible que sur les objets de flux H. 323.
ms.assetid: 68cb1df1-f7fa-447a-8ea5-80dc1e802760
title: Interface IKeyFrameControl (H323priv. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6c326c6a492777d7c41ae450a1c502c343aeb8cb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106540328"
---
# <a name="ikeyframecontrol-interface"></a>Interface IKeyFrameControl

\[**IKeyFrameControl** n’est pas disponible pour une utilisation dans Windows Vista, windows Server 2008 et les versions ultérieures du système d’exploitation. L’API cliente RTC offre des fonctionnalités similaires.\]

L’interface **IKeyFrameControl** est implémentée par le [MSP h. 323](h323-msp.md) et n’est disponible que sur les objets de flux h. 323. Cette interface expose des méthodes qui permettent la création et la manipulation de terminaux qui peuvent communiquer entre des clients H323 et SDP. Il a deux méthodes qui permettent à l’application de demander au point de terminaison distant de mettre à jour l’image vidéo avec une image clé.

## <a name="members"></a>Membres

L’interface **IKeyFrameControl** hérite de l’interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **IKeyFrameControl** a également les types de membres suivants :

-   [Méthodes](#methods)

### <a name="methods"></a>Méthodes

L’interface **IKeyFrameControl** possède ces méthodes.



| Méthode                                                                  | Description                                                                                 |
|:------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------|
| [**PeriodicUpdatePicture**](ikeyframecontrol-periodicupdatepicture.md) | Configure un minuteur dans le flux qui demandera régulièrement des mises à jour d’images.<br/> |
| [**UpdatePicture**](ikeyframecontrol-updatepicture.md)                 | Demande à l’expéditeur vidéo de mettre à jour l’image.<br/>                                     |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------|---------------------------------------------------------------------------------------|
| Version TAPI<br/> | Nécessite TAPI 3,0 ou une version ultérieure<br/>                                                 |
| En-tête<br/>       | <dl> <dt>H323priv. h</dt> </dl> |
| Bibliothèque<br/>      | <dl> <dt>UUID. lib</dt> </dl>   |
| DLL<br/>          | <dl> <dt>Tapi3.dll</dt> </dl>  |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[MSP H323](h323-msp.md)
</dt> </dl>

 

