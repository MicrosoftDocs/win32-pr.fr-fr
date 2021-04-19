---
description: L’interface ITQOSApplicationID expose une méthode qui permet à une application d’obtenir l’identificateur de QOS pour l’appel en cours.
ms.assetid: 1df50b3a-bd16-4e9b-afca-b025bfe537a4
title: Interface ITQOSApplicationID (Ipmsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 23df8da80798cc52ecd73b4f29288812f3774d9f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106543976"
---
# <a name="itqosapplicationid-interface"></a>Interface ITQOSApplicationID

\[ Cette interface n’est pas disponible pour une utilisation dans Windows Vista, Windows Server 2008 et les versions ultérieures du système d’exploitation. L’API cliente RTC offre des fonctionnalités similaires.\]

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



 

