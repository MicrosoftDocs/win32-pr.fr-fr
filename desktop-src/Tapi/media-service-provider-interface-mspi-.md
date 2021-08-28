---
description: L’interface MSPI (Media Service Provider Interface) est un ensemble d’interfaces et de méthodes implémentées par un MSP pour permettre au contrôle de l’application TAPI 3 sur le transport multimédia au cours d’une session de communication.
ms.assetid: 53b7bcbd-571a-44da-a6db-10d4c3e5d30a
title: MSPI (Media Service Provider Interface)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 83b99f78d62c0784e38ede7a4019eef40cf8a48cf9480a4326c5d7b7129ca971
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120073009"
---
# <a name="media-service-provider-interface-mspi"></a>MSPI (Media Service Provider Interface)

L’interface MSPI (Media Service Provider Interface) est un ensemble d’interfaces et de méthodes implémentées par un MSP pour permettre au contrôle de l’application TAPI 3 sur le transport multimédia au cours d’une session de communication. Un MSP gère les mécanismes spécifiques à l’appareil et spécifiques au protocole nécessaires pour mettre en œuvre ces contrôles, et communique avec son PVC couplé ou une application à l’aide des méthodes fournies dans le MSPI.

La section suivante ( [référence MspI (Media Service Provider Interface)](media-service-provider-interface-mspi-reference.md)) détaille les interfaces qu’un MSP expose afin d’interagir avec l’environnement de téléphonie Microsoft.

En outre, un MSP peut exposer des interfaces et des méthodes privées spécifiques au fournisseur pour faciliter le contrôle multimédia. Par exemple, le [MSP de conférence IP](ipconf-msp.md) expose des interfaces qui fournissent un contrôle de participant. Pour plus d’informations sur la façon dont les objets privés fonctionnent et les [interfaces MSP ipconf](ipconf-msp-interfaces.md) pour une liste de références de ipconf, consultez [interfaces spécifiques au fournisseur](provider-specific-interfaces.md) .

La majeure partie de l’effort de programmation pour la création d’un MSP est très spécifique à une plateforme, un appareil et un protocole de transport donnés, et sort du cadre de ce document. Toutefois, Microsoft fournit un ensemble de classes de base MSP, qui sera utile pour la plupart des auteurs MSP. Pour plus d’informations sur l’utilisation de ces classes, consultez [classes de base TAPI 3 MSP](tapi-3-msp-base-classes.md) .

L’interface [**ITMSPAddress**](/windows/desktop/api/msp/nn-msp-itmspaddress) représente un fournisseur de services multimédia pour la dll TAPI. Cette interface n’est pas utilisée par ou exposée à une application d’utilisateur final. La DLL TAPI 3 appelle **CoCreateInstance** sur cette interface pour créer l’objet principal MSP. Les méthodes de cet objet permettent à une application de charger et décharger le MSP, de recevoir des informations d’un TSP et de créer l’interface [**ITStreamControl**](/windows/win32/api/tapi3if/nn-tapi3if-itstreamcontrol) , qui est exposée sur l’objet d’appel.

Les interfaces [**ITSubStreamControl**](/windows/win32/api/tapi3if/nn-tapi3if-itsubstreamcontrol) et [**ITSubStream**](/windows/win32/api/tapi3if/nn-tapi3if-itsubstream) fournissent des méthodes parallèles en ce qui concerne les sous-flux. La prise en charge des sous-flux est facultative. Toutes les autres interfaces doivent être implémentées par un MSP.

> [!Note]  
> Les opérations implémentées par une paire TSP/MSP doivent se trouver dans une DLL pour permettre à un utilisateur de mettre à jour le fournisseur de services sans redémarrer son système.

 

 

 
