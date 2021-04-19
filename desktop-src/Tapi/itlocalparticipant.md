---
description: L’interface ITLocalParticipant est exposée sur l’objet de flux lorsque le MSP IPConf prend en charge l’appel.
ms.assetid: 64965ae2-e30b-4353-a502-f96018da71a5
title: Interface ITLocalParticipant (Confpriv. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d4017837a0b970cb791cdf454437fe2d48720028
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106537781"
---
# <a name="itlocalparticipant-interface"></a>Interface ITLocalParticipant

L’interface **ITLocalParticipant** est exposée sur l’objet de flux lorsque le MSP ipconf prend en charge l’appel. Le MSP implémente des méthodes qui permettent à une application d’accéder à des informations sur les participants et de les définir. L’interface **ITLocalParticipant** est créée en appelant **QueryInterface** sur [**ITStream**](/windows/win32/api/tapi3if/nn-tapi3if-itstream).

## <a name="members"></a>Membres

L’interface **ITLocalParticipant** hérite de l’interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **ITLocalParticipant** a également les types de membres suivants :

-   [Méthodes](#methods)

### <a name="methods"></a>Méthodes

L’interface **ITLocalParticipant** possède ces méthodes.



| Méthode                                                                                     | Description                                                                            |
|:-------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------|
| [**Obtient \_ LocalParticipantTypedInfo**](itlocalparticipant-get-localparticipanttypedinfo.md) | Obtient des informations sur les participants, telles que le nom du courrier électronique ou l’emplacement géographique.<br/> |
| [**put \_ LocalParticipantTypedInfo**](itlocalparticipant-put-localparticipanttypedinfo.md) | Définit les informations sur le participant.<br/>                                               |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------|---------------------------------------------------------------------------------------|
| Version TAPI<br/> | Nécessite TAPI 3,0 ou une version ultérieure<br/>                                                 |
| En-tête<br/>       | <dl> <dt>Confpriv. h</dt> </dl> |
| Bibliothèque<br/>      | <dl> <dt>UUID. lib</dt> </dl>   |
| DLL<br/>          | <dl> <dt>Tapi3.dll</dt> </dl>  |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**ITStream**](/windows/win32/api/tapi3if/nn-tapi3if-itstream)
</dt> </dl>

 

