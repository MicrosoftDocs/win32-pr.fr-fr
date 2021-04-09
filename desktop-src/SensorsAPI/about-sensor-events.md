---
description: L’API de capteur peut fournir des notifications d’événements.
ms.assetid: 2400619c-ee9c-4662-ae57-6d4bc317e730
title: À propos des événements d’API de capteur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e941dca86d5b7ec3aa9922220c1232b10429f60a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103867621"
---
# <a name="about-sensor-api-events"></a>À propos des événements d’API de capteur

L’API de capteur peut fournir des notifications d’événements.

Lorsque vous vous inscrivez pour recevoir des événements, par l’intermédiaire de [**ISensor :: SetEventSink**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensor-seteventsink) ou [**ISensorManager :: SetEventSink**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensormanager-seteventsink), vous devez fournir un pointeur vers une interface de rappel. Vous devez implémenter les méthodes de l’interface de rappel dans votre code. L’API Sensor définit les interfaces de rappel suivantes :

-   [**ISensorEvents**](/windows/desktop/api/sensorsapi/nn-sensorsapi-isensorevents). Implémentez cette interface pour recevoir des événements des capteurs. Les capteurs peuvent informer votre application sur les nouvelles données, les modifications de l’état du capteur, la déconnexion du capteur et les événements personnalisés définis par le fabricant du capteur.
-   [**ISensorManagerEvents**](/windows/desktop/api/sensorsapi/nn-sensorsapi-isensormanagerevents). Implémentez cette interface pour recevoir des événements du gestionnaire de capteurs. Le gestionnaire de capteurs peut notifier votre application lorsqu’un capteur se connecte et peut donc être utilisé.

Vous pouvez annuler les notifications d’événements en appelant à nouveau [**SetEventSink**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensor-seteventsink) , cette fois-ci, en passant une valeur **null** par le biais du paramètre.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Utilisation d’événements d’API de capteur](using-sensor-api-events.md)
</dt> </dl>

 

 
