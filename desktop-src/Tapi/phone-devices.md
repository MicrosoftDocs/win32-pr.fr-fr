---
description: Téléphone la prise en charge des appareils est supplémentaire plutôt que basique, les fournisseurs de services ne sont donc pas tenus de prendre en charge les appareils téléphoniques.
ms.assetid: 4d9f3b32-20d0-4550-9b3d-db97df8ea289
title: Téléphone Appareil
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7d11aa269e17d74fbaf74c701c954ced734ef33900198a7c9e30a044f5ebd32e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119873279"
---
# <a name="phone-devices"></a>Téléphone Appareil

Téléphone la prise en charge des appareils est supplémentaire plutôt que basique, les fournisseurs de services ne sont donc pas tenus de prendre en charge les appareils téléphoniques.

Tout comme une classe de périphérique en ligne est une abstraction d’un périphérique de ligne physique, la classe de périphérique téléphonique représente une abstraction indépendante du périphérique d’un ensemble de téléphones. L’interface TAPI traite les appareils téléphoniques et de ligne comme des appareils indépendants les uns des autres. En d’autres termes, vous pouvez utiliser un téléphone (appareil) sans utiliser de ligne associée, et vous pouvez utiliser une ligne (appareil) sans utiliser de téléphone.

Les fournisseurs de services qui implémentent pleinement cette indépendance peuvent offrir des utilisations pour ces appareils qui ne sont pas définis par les protocoles de téléphonie traditionnels. Par exemple, une personne peut utiliser le combiné du téléphone du bureau comme un périphérique audio Wave pour l’enregistrement ou la lecture vocal, peut-être sans que le commutateur soit en cours d’utilisation. Dans une telle implémentation, le levage du téléphone local n’a pas besoin d’envoyer automatiquement un signal offhook au commutateur.

Cette indépendance permet également à une application d’appeler le téléphone local d’une manière indépendante des appels entrants. Les fonctionnalités des fournisseurs de services sont limitées par les fonctionnalités du matériel et des logiciels utilisés pour interconnecter le commutateur, le téléphone et l’ordinateur.

L’interface TAPI comprend des fonctions permettant de récupérer des fonctionnalités d’appareil qui permettent aux clients de déterminer si un tel modèle d’utilisation est pris en charge.

Cette section décrit les appareils téléphoniques et explique comment utiliser les fonctions de téléphonie TAPI pour accéder à ces appareils.

-   [Téléphone Passerelle](phone-device-elements.md)
-   [Initialisation et arrêt](initialization-and-shutdown.md)

 

 



