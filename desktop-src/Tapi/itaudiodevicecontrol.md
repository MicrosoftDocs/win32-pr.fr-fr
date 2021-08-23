---
description: L’interface ITAudioDeviceControl expose des méthodes qui permettent à une application d’obtenir et de définir des paramètres pour le contrôle d’un périphérique audio.
ms.assetid: 9a557cb2-acad-406c-9a87-18cbe96e8a9f
title: Interface ITAudioDeviceControl (Ipmsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ac06118300d9170f4928d7be5d2cf1bc3b69261f0062d6ffecd403389e564d48
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119003437"
---
# <a name="itaudiodevicecontrol-interface"></a>Interface ITAudioDeviceControl

\[cette interface n’est pas disponible pour une utilisation dans Windows Vista, Windows Server 2008 et les versions ultérieures du système d’exploitation. L’API cliente RTC offre des fonctionnalités similaires.\]

L’interface **ITAudioDeviceControl** expose des méthodes qui permettent à une application d’obtenir et de définir des paramètres pour le contrôle d’un périphérique audio.

Cette interface est implémentée par le [MSP ipconf](ipconf-msp.md) et le [MSP H323](h323-msp.md). Il est exposé lorsqu’un appel utilise ces fournisseurs de services ou un fournisseur de services tiers qui implémente cette interface. Pour obtenir un pointeur vers l’interface **ITAudioDeviceControl** , appelez **QueryInterface** sur l’interface [**ITStream**](/windows/win32/api/tapi3if/nn-tapi3if-itstream) qui contrôle le périphérique audio correspondant au flux. Le type de média de l’interface **ITStream** doit être audio pour que l’interface **ITAudioDeviceControl** soit exposée.

## <a name="members"></a>Membres

L’interface **ITAudioDeviceControl** hérite de l’interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **ITAudioDeviceControl** a également les types de membres suivants :

-   [Méthodes](#methods)

### <a name="methods"></a>Méthodes

L’interface **ITAudioDeviceControl** possède ces méthodes.



| Méthode                                              | Description                                                                                             |
|:----------------------------------------------------|:--------------------------------------------------------------------------------------------------------|
| [**Télécharger**](/windows/desktop/api/tapi3if/nf-tapi3if-itasrterminalevent-get_call)          | Obtient la valeur d’une [propriété de périphérique audio](audiodeviceproperty.md)donnée.<br/>                  |
| [**GetRange**](/windows/desktop/api/tapi3if/nf-tapi3if-itasrterminalevent-get_terminal) | Obtient la plage de valeurs valides pour une [propriété de périphérique audio](audiodeviceproperty.md)donnée.<br/> |
| [**Définie**](/windows/desktop/api/tapi3if/nf-tapi3if-itasrterminalevent-get_error)         | Définit la valeur d’une [propriété de périphérique audio](audiodeviceproperty.md)donnée.<br/>                  |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------|--------------------------------------------------------------------------------------|
| Version TAPI<br/> | Nécessite TAPI 3,1<br/>                                                         |
| En-tête<br/>       | <dl> <dt>Ipmsp. h</dt> </dl>   |
| Bibliothèque<br/>      | <dl> <dt>UUID. lib</dt> </dl>  |
| DLL<br/>          | <dl> <dt>Tapi3.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[MSP IPConf](ipconf-msp.md)
</dt> </dl>

 

