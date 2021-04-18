---
description: Ce document décrit les interfaces qui fournissent des méthodes qui permettent à un MSP d’interagir avec l’environnement de téléphonie Microsoft et permettent à une application TAPI 3 d’utiliser des contrôles de média MSP.
ms.assetid: e67d4941-ce0f-48b9-8099-b62659ad33e0
title: Informations de référence sur l’interface MSPI (Media Service Provider Interface)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a30b961fff4d8a9e50fb35573633cc2dc06e370c
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/03/2021
ms.locfileid: "106522883"
---
# <a name="media-service-provider-interface-mspi-reference"></a>Informations de référence sur l’interface MSPI (Media Service Provider Interface)

Ce document décrit les interfaces qui fournissent des méthodes qui permettent à un MSP d’interagir avec l’environnement de téléphonie Microsoft et permettent à une application TAPI 3 d’utiliser les contrôles de média d’un MSP.



| Interfaces d’interface du fournisseur de services de média      | Description                                                                                                                                                                            | Requis ? |
|--------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------|
| [**ITMSPAddress**](/windows/desktop/api/msp/nn-msp-itmspaddress)             | Exposé uniquement à l’interface TAPI. Interface MSP principale pour la DLL TAPI. TAPI 3 appelle **CoCreateInstance** sur cette interface pour créer l’objet MSP.                                               | Oui       |
| [**ITStream**](/windows/win32/api/tapi3if/nn-tapi3if-itstream)                     | Exposés aux applications. Fournit des méthodes qui permettent à une application de récupérer des informations sur un flux, de le démarrer, de l’interrompre ou de l’arrêter, ainsi que de sélectionner ou désélectionner des terminaux dans un flux. | Oui       |
| [**ITStreamControl**](/windows/win32/api/tapi3if/nn-tapi3if-itstreamcontrol)       | Exposés aux applications. Fournit des méthodes qui permettent à une application de créer ou de supprimer des flux.                                                                                       | Oui       |
| [**IEnumStream**](/windows/desktop/api/tapi3if/nn-tapi3if-ienumstream)               | Exposés aux applications. Interface d’énumérateur pour [**ITStream**](/windows/win32/api/tapi3if/nn-tapi3if-itstream).                                                                                                        | Oui       |
| [**ITSubStream**](/windows/win32/api/tapi3if/nn-tapi3if-itsubstream)               | Exposés aux applications. Fournit des méthodes qui permettent à une application de récupérer des informations sur un sous-flux, de le démarrer, de l’interrompre ou de l’arrêter, ainsi que de sélectionner ou désélectionner des terminaux.          | Facultatif  |
| [**ITSubStreamControl**](/windows/win32/api/tapi3if/nn-tapi3if-itsubstreamcontrol) | Exposés aux applications. Fournit des méthodes qui permettent à une application de créer ou de supprimer des sous-flux.                                                                                    | Facultatif  |
| [**IEnumSubStream**](/windows/desktop/api/tapi3if/nn-tapi3if-ienumsubstream)         | Exposés aux applications. Interface d’énumérateur pour [**ITSubStream**](/windows/win32/api/tapi3if/nn-tapi3if-itsubstream).                                                                                                  | Facultatif  |
| [**ITTerminal**](/windows/win32/api/tapi3if/nn-tapi3if-itterminal)                 | Exposés aux applications. Obtient des informations sur l' [objet terminal](terminal-object.md), telles que l’appel de terminal et le support pris en charge.                                                    | Oui       |
| [**ITTerminalSupport**](/windows/win32/api/tapi3if/nn-tapi3if-itterminalsupport)   | Exposés aux applications. Fournit des méthodes pour interroger des terminaux disponibles et créer des terminaux supplémentaires.                                                                             | Oui       |
| [**ITTerminalSupport2**](/windows/desktop/api/tapi3if/nn-tapi3if-itterminalsupport2) | Exposés aux applications. Récupère des informations sur les classes terminal enfichables et les superclasses. dérive de l’interface [**ITTerminalSupport**](/windows/win32/api/tapi3if/nn-tapi3if-itterminalsupport) .           | Oui       |



 

## <a name="media-service-provider-interface-types"></a>Types d’interface du fournisseur de services multimédia

-   [**\_événement d’adresse MSP \_**](/windows/win32/api/msp/ne-msp-msp_address_event)
-   [**\_événement d’appel MSP \_**](/windows/win32/api/msp/ne-msp-msp_call_event)
-   [**\_événement MSP**](/windows/win32/api/msp/ne-msp-msp_event)
-   [**\_informations sur l’événement MSP \_**](/windows/win32/api/msp/ns-msp-msp_event_info)

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[MSPI (Media Service Provider Interface)](media-service-provider-interface-mspi-.md)
</dt> </dl>

 

 
