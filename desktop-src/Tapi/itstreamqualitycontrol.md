---
description: Le ITStreamQualityControl expose des méthodes qui permettent à une application d’obtenir et de définir des paramètres pour le contrôle qualité du flux.
ms.assetid: b9ecf24a-c87e-44a6-9e20-aa7bf7619314
title: Interface ITStreamQualityControl (Ipmsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 98a85eccc907ef2c8f4c0b67c2a32244004dbdca
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127013475"
---
# <a name="itstreamqualitycontrol-interface"></a>Interface ITStreamQualityControl

\[cette interface n’est pas disponible pour une utilisation dans Windows Vista, Windows Server 2008 et les versions ultérieures du système d’exploitation. L’API cliente RTC offre des fonctionnalités similaires.\]

Le **ITStreamQualityControl** expose des méthodes qui permettent à une application d’obtenir et de définir des paramètres pour le contrôle qualité du flux.

Cette interface est implémentée par le [MSP ipconf](ipconf-msp.md) et le [MSP H323](h323-msp.md). Elle est exposée uniquement lorsqu’un appel utilise ces fournisseurs de services.

## <a name="members"></a>Membres

L’interface **ITStreamQualityControl** hérite de l’interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **ITStreamQualityControl** a également les types de membres suivants :

-   [Méthodes](#methods)

### <a name="methods"></a>Méthodes

L’interface **ITStreamQualityControl** possède ces méthodes.



| Méthode                                              | Description                                                                                                 |
|:----------------------------------------------------|:------------------------------------------------------------------------------------------------------------|
| [**Télécharger**](itstreamqualitycontrol-get.md)           | Obtient la valeur d’une [propriété de qualité de flux](streamqualityproperty.md)donnée.<br/>                  |
| [**GetRange**](itstreamqualitycontrol-getrange.md) | Obtient la plage de valeurs valides pour une [propriété de qualité de flux](streamqualityproperty.md)donnée.<br/> |
| [**Définie**](itstreamqualitycontrol-set.md)           | Définit la valeur d’une [propriété de qualité de flux](streamqualityproperty.md)donnée.<br/>                  |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------|--------------------------------------------------------------------------------------|
| Version TAPI<br/> | Nécessite TAPI 3,1<br/>                                                         |
| En-tête<br/>       | <dl> <dt>Ipmsp. h</dt> </dl>   |
| Bibliothèque<br/>      | <dl> <dt>UUID. lib</dt> </dl>  |
| DLL<br/>          | <dl> <dt>Tapi3.dll</dt> </dl> |



 

