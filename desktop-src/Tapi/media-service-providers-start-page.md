---
description: Un fournisseur de services de média (MSP) permet à une application de contrôler le média pour un mécanisme de transport particulier.
ms.assetid: f886380f-d970-4511-bf71-fb1eb767e4f4
title: Fournisseurs de services de média
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3dd78f5ff4a13da4365f99bd2cb539738b6f3fd6
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/03/2021
ms.locfileid: "106525793"
---
# <a name="media-service-providers"></a>Fournisseurs de services de média

## <a name="purpose"></a>Objectif

Un fournisseur de services de média (MSP) permet à une application de contrôler le média pour un mécanisme de transport particulier. Un MSP est toujours associé à un fournisseur de services de téléphonie (TSP).

L’interface MSPI (Media Service Provider Interface) est un ensemble d’interfaces et de méthodes implémentées par un MSP pour permettre à une application de contrôler le transport multimédia au cours d’une session de communication. Un MSP gère les mécanismes spécifiques à l’appareil et spécifiques au protocole requis pour mettre en œuvre ces contrôles, et communique avec son PVC couplé ou une application à l’aide des méthodes fournies dans le MSPI.

## <a name="developer-audience"></a>Développeurs concernés

Vous devez vous familiariser avec COM. L’expérience de développement avec les télécommunications ou d’autres applications de téléphonie est utile, mais pas nécessaire.

## <a name="run-time-requirements"></a>Conditions d’exécution

MSPI permet le développement de fournisseurs de services multimédias pour des protocoles ou des appareils spécifiques s’exécutant sur des systèmes d’exploitation Windows Server 2003, Windows XP et Windows 2000.

## <a name="in-this-section"></a>Contenu de cette section



| Rubrique                                                                       | Description                                                           |
|-----------------------------------------------------------------------------|-----------------------------------------------------------------------|
| [Vue d'ensemble](about-the-media-service-provider-msp-.md)<br/>            | Informations générales sur l’architecture et les composants MSP.<br/> |
| [Référence](media-service-provider-interface-mspi-reference.md)<br/> | Documentation pour les interfaces MSPI.<br/>                     |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Vue d’ensemble de la téléphonie Microsoft](microsoft-telephony-overview.md)
</dt> <dt>

[TAPI 3,1](tapi-3-1-start-page.md)
</dt> <dt>

[Fournisseurs de services de téléphonie](./telephony-service-providers-start-page.md)
</dt> </dl>

 

