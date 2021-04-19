---
description: L’interface ITCallQualityControl expose des méthodes qui permettent à une application d’obtenir et de définir des paramètres pour le contrôle qualité des appels.
ms.assetid: 8d33e3b2-6af9-4c2d-bc65-905467f4fc6a
title: Interface ITCallQualityControl (Ipmsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 447e2f34db76ba15ecaec9e7bc03a0d2d398c493
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106537510"
---
# <a name="itcallqualitycontrol-interface"></a>Interface ITCallQualityControl

\[ Cette interface n’est pas disponible pour une utilisation dans Windows Vista, Windows Server 2008 et les versions ultérieures du système d’exploitation. L’API cliente RTC offre des fonctionnalités similaires.\]

L’interface **ITCallQualityControl** expose des méthodes qui permettent à une application d’obtenir et de définir des paramètres pour le contrôle qualité des appels.

Cette interface est implémentée par le [MSP ipconf](ipconf-msp.md) et le [MSP H323](h323-msp.md). Elle est exposée uniquement lorsqu’un appel utilise ces fournisseurs de services.

## <a name="members"></a>Membres

L’interface **ITCallQualityControl** hérite de l’interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **ITCallQualityControl** a également les types de membres suivants :

-   [Méthodes](#methods)

### <a name="methods"></a>Méthodes

L’interface **ITCallQualityControl** possède ces méthodes.



| Méthode                                            | Description                                                                                                     |
|:--------------------------------------------------|:----------------------------------------------------------------------------------------------------------------|
| [**Télécharger**](itcallqualitycontrol-get.md)           | Obtient la valeur d’une [propriété de contrôle de qualité d’appel](callqualityproperty.md)donnée.<br/>                  |
| [**GetRange**](itcallqualitycontrol-getrange.md) | Obtient la plage de valeurs valides pour une [propriété de contrôle de qualité d’appel](callqualityproperty.md)donnée.<br/> |
| [**Définissez**](itcallqualitycontrol-set.md)           | Définit la valeur d’une [propriété de contrôle de qualité d’appel](callqualityproperty.md)donnée.<br/>                  |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------|--------------------------------------------------------------------------------------|
| Version TAPI<br/> | Nécessite TAPI 3,1<br/>                                                         |
| En-tête<br/>       | <dl> <dt>Ipmsp. h</dt> </dl>   |
| Bibliothèque<br/>      | <dl> <dt>UUID. lib</dt> </dl>  |
| DLL<br/>          | <dl> <dt>Tapi3.dll</dt> </dl> |



 

