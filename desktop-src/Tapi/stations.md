---
description: Les ensembles de stations analysés par le biais d’un lien tiers sont modélisés comme un appareil de ligne et éventuellement un appareil téléphonique associé.
ms.assetid: 1d116734-cd8f-40f1-9069-2dad351a24bf
title: Stations
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6ad9874542a63f05e124ea5df833aa0a433c03713cc3a2d7bb1ca3a471174e86
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117760715"
---
# <a name="stations"></a>Stations

Les ensembles de stations analysés par le biais d’un lien tiers sont modélisés comme un appareil de ligne et éventuellement un appareil téléphonique associé. Le périphérique de ligne peut avoir plusieurs adresses, si le terminal modélisé prend en charge plusieurs numéros de répertoire (DN). Plusieurs apparences d’appel sur le même DN peuvent être modélisées comme une adresse unique qui prend en charge plusieurs appels.

Les appels entre deux stations sur le commutateur ont deux handles d’appel, l’un donnant la vue d’appel à partir de la première station (sur son périphérique de ligne) et l’autre qui donne la vue d’appel à partir de la deuxième station (sur son appareil de ligne). Par exemple, un [**lineMakeCall**](/windows/desktop/api/Tapi/nf-tapi-linemakecall) tiers placé par une application sur le serveur est dirigé vers le périphérique de ligne associé à la station à partir de laquelle l’appel doit être composé ; un descripteur d’appel est créé sur cette ligne, sur l’adresse spécifiée dans [**LINECALLPARAMS**](/windows/desktop/api/Tapi/ns-tapi-linecallparams) (ce qui permet de contrôler le DN utilisé sur un téléphone qui prend en charge plusieurs DNS). Lorsque l’appel est offert à l’adresse de destination, un nouveau descripteur d’appel présentant un appel dans l’état d' *offre* est créé ; les applications savent qu’il s’agissait d’une autre vue du même appel par le membre **dwCallID** dans [**LINECALLINFO**](/windows/desktop/api/Tapi/ns-tapi-linecallinfo) étant égal pour les deux appels. Les deux appels sont *inactifs* lors de la suppression de l’appel ; un appel peut être supprimé de l’application tierce en procédant à un [**lineDrop**](/windows/desktop/api/Tapi/nf-tapi-linedrop) sur l’un ou l’autre des handles d’appel.

 

 



