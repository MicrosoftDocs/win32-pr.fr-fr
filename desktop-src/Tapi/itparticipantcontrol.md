---
description: L’interface ITParticipantControl est implémentée par le MSP IPConf.
ms.assetid: e617f2a4-6be8-4cb1-9f03-470c5100b834
title: Interface ITParticipantControl (Confpriv. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 96075748f0c35cbc5af3c6cd07277d15222e0658
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106537528"
---
# <a name="itparticipantcontrol-interface"></a>Interface ITParticipantControl

\[**ITParticipantControl** n’est pas disponible pour une utilisation dans Windows Vista, windows Server 2008 et les versions ultérieures du système d’exploitation. L’API cliente RTC offre des fonctionnalités similaires.\]

L’interface **ITParticipantControl** est implémentée par le MSP ipconf. Cette interface est exposée sur l’objet d’appel. Cette interface permet à une application de récupérer des pointeurs vers les participants d’une conférence. L’interface **ITParticipantControl** est créée en appelant **QueryInterface** sur [**ITCallInfo**](/windows/desktop/api/tapi3if/nn-tapi3if-itcallinfo).

## <a name="members"></a>Membres

L’interface **ITParticipantControl** hérite de l’interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **ITParticipantControl** a également les types de membres suivants :

-   [Méthodes](#methods)

### <a name="methods"></a>Méthodes

L’interface **ITParticipantControl** possède ces méthodes.



| Méthode                                                                      | Description                                                                                                                                                                 |
|:----------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**EnumerateParticipants**](itparticipantcontrol-enumerateparticipants.md) | Énumère les participants actuellement impliqués dans la Conférence.<br/>                                                                                                    |
| [**accéder aux \_ participants**](itparticipantcontrol-get-participants.md)          | Crée une collection de participants associés à la Conférence en cours. Fourni pour les applications clientes Automation, telles que celles écrites en Visual Basic.<br/> |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------|---------------------------------------------------------------------------------------|
| Version TAPI<br/> | Nécessite TAPI 3,0 ou une version ultérieure<br/>                                                 |
| En-tête<br/>       | <dl> <dt>Confpriv. h</dt> </dl> |
| Bibliothèque<br/>      | <dl> <dt>UUID. lib</dt> </dl>   |
| DLL<br/>          | <dl> <dt>Tapi3.dll</dt> </dl>  |



 

