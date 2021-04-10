---
description: Les applications peuvent écouter les événements système à l’aide de l’objet InkCollector et en écoutant l’événement SystemGesture.
ms.assetid: 141afdbe-b5a7-47dc-b505-46089a5eda75
title: Écoute des événements système
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f1429e652140cc9624d324401edef7817dad40ef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104042780"
---
# <a name="listening-to-system-events"></a>Écoute des événements système

Les applications peuvent écouter les événements système à l’aide de l’objet [**InkCollector**](inkcollector-class.md) et en écoutant l’événement [**SystemGesture**](inkcollector-systemgesture.md) . Vous pouvez définir les événements que l’application écoute. Lorsqu’une action de stylet de tablette se produit, l’événement **SystemGesture** correspondant est envoyé à l’application sur son objet **InkCollector** . Une application peut annuler le message de souris qui correspond à un événement **SystemGesture** donné lorsqu’il reçoit l’événement. Pour plus d’informations sur l’annulation des messages de la souris, consultez événement **SystemGesture** .

 

 



