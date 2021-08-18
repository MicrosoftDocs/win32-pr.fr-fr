---
description: L’interface ITAudioSettings expose des méthodes qui permettent à une application d’obtenir et de définir des paramètres pour le contrôle d’un périphérique audio.
ms.assetid: 56607024-255d-4d1b-9ca0-6086eff7b7b2
title: Interface ITAudioSettings (Ipmsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 85ce0c7a92e34583947be983ed4d28391eb70c02697313aedee21a7158c9c3b3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119140382"
---
# <a name="itaudiosettings-interface"></a>Interface ITAudioSettings

\[cette interface n’est pas disponible pour une utilisation dans Windows Vista, Windows Server 2008 et les versions ultérieures du système d’exploitation. L’API cliente RTC offre des fonctionnalités similaires.\]

L’interface **ITAudioSettings** expose des méthodes qui permettent à une application d’obtenir et de définir des paramètres pour le contrôle d’un périphérique audio.

Cette interface est implémentée par le [MSP ipconf](ipconf-msp.md) et le [MSP H323](h323-msp.md). Elle est exposée uniquement lorsqu’un appel utilise ces fournisseurs de services.

## <a name="members"></a>Membres

L’interface **ITAudioSettings** hérite de l’interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **ITAudioSettings** a également les types de membres suivants :

-   [Méthodes](#methods)

### <a name="methods"></a>Méthodes

L’interface **ITAudioSettings** possède ces méthodes.



| Méthode                                              | Description                                                                                                |
|:----------------------------------------------------|:-----------------------------------------------------------------------------------------------------------|
| [**Télécharger**](/windows/desktop/api/tapi3if/nf-tapi3if-itasrterminalevent-get_call)          | Obtient la valeur d’une [propriété de paramètre audio](audiosettingsproperty.md)donnée.<br/>                  |
| [**GetRange**](/windows/desktop/api/tapi3if/nf-tapi3if-itasrterminalevent-get_terminal) | Obtient la plage de valeurs valides pour une [propriété de paramètre audio](audiosettingsproperty.md)donnée.<br/> |
| [**Définie**](/windows/desktop/api/tapi3if/nf-tapi3if-itasrterminalevent-get_error)         | Définit la valeur d’une [propriété de paramètre audio](audiosettingsproperty.md)donnée.<br/>                  |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------|--------------------------------------------------------------------------------------|
| Version TAPI<br/> | Nécessite TAPI 3,1<br/>                                                         |
| En-tête<br/>       | <dl> <dt>Ipmsp. h</dt> </dl>   |
| Bibliothèque<br/>      | <dl> <dt>UUID. lib</dt> </dl>  |
| DLL<br/>          | <dl> <dt>Tapi3.dll</dt> </dl> |



 

