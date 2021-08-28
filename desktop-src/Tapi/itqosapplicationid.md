---
description: L’interface ITQOSApplicationID expose une méthode qui permet à une application d’obtenir l’identificateur de QOS pour l’appel en cours.
ms.assetid: 1df50b3a-bd16-4e9b-afca-b025bfe537a4
title: Interface ITQOSApplicationID (Ipmsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7d4067d7a476e2a402c278b22dcee21b6542919396178350e73017d56ba92258
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120126279"
---
# <a name="itqosapplicationid-interface"></a>Interface ITQOSApplicationID

\[cette interface n’est pas disponible pour une utilisation dans Windows Vista, Windows Server 2008 et les versions ultérieures du système d’exploitation. L’API cliente RTC offre des fonctionnalités similaires.\]

L’interface **ITQOSApplicationID** expose une méthode qui permet à une application d’obtenir l’identificateur de QoS pour l’appel en cours.

Cette interface est implémentée par le [MSP ipconf](ipconf-msp.md) et est exposée uniquement lorsqu’un appel utilise la conférence IP.

## <a name="members"></a>Membres

L’interface **ITQOSApplicationID** hérite de l’interface [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) . **ITQOSApplicationID** a également les types de membres suivants :

-   [Méthodes](#methods)

### <a name="methods"></a>Méthodes

L’interface **ITQOSApplicationID** possède ces méthodes.



| Méthode                                                                | Description                         |
|:----------------------------------------------------------------------|:------------------------------------|
| [**SetQOSApplicationID**](itqosapplicationid-setqosapplicationid.md) | Définit l’identificateur de QOS.<br/> |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------|--------------------------------------------------------------------------------------|
| Version TAPI<br/> | Nécessite TAPI 3,1<br/>                                                         |
| En-tête<br/>       | <dl> <dt>Ipmsp. h</dt> </dl>   |
| Bibliothèque<br/>      | <dl> <dt>UUID. lib</dt> </dl>  |
| DLL<br/>          | <dl> <dt>Tapi3.dll</dt> </dl> |



 

