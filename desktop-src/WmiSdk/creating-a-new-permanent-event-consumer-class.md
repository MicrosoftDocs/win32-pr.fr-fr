---
description: L’une des premières étapes de la création d’un consommateur d’événements permanent consiste à créer la classe WMI qui décrit le consommateur d’événements. Plus précisément, la classe de consommateur d’événements permanent définit les paramètres de l’action implémentée par le consommateur physique.
ms.assetid: a5b6d0b9-8df1-47e3-bb3b-cc69db6d9c0e
ms.tgt_platform: multiple
title: Création d’une classe de consommateur d’événements permanente
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 03f8ae8e1e83abcf3b340398d45aefde4c7141e2
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127520213"
---
# <a name="creating-a-new-permanent-event-consumer-class"></a>Création d’une classe de consommateur d’événements permanente

L’une des premières étapes de la création d’un consommateur d’événements permanent consiste à créer la classe WMI qui décrit le consommateur d’événements. Plus précisément, la classe de consommateur d’événements permanent définit les paramètres de l’action implémentée par le consommateur physique.

La procédure suivante décrit comment créer une classe de consommateur d’événements permanente.

**Pour créer une classe de consommateur d’événements permanente**

1.  Dérivez une classe de la classe système [**\_ \_ EventConsumer**](--eventconsumer.md) .
2.  Implémentez les paramètres nécessaires pour traiter une notification d’événements.

L’exemple suivant illustre la syntaxe utilisée pour créer la classe SMTPConsumerEvent. Vous pouvez l’utiliser comme exemple pour créer votre nouvelle classe. La classe [**SMTPEventConsumer**](smtpeventconsumer.md) envoie un message électronique à l’aide du protocole SMTP (Simple Mail Transfer Protocol) chaque fois qu’un événement lui est remis. Cette classe est définie dans smtpcons. mof.

``` syntax
class SMTPEventConsumer : __EventConsumer
{
  [key] string Name;
  [not_null] string SMTPServer;
  [Template] string Subject;
  [Template] string FromLine;
  [Template] string ReplyToLine;
  [Template] string Message;
  [Template] string ToLine;
  [Template] string CcLine;
  [Template] string BccLine;
  string HeaderFields[];
};
```

Vous devez être en mesure de créer des instances de votre classe de consommateur d’événements permanent pour décrire une ou plusieurs manières d’envoyer des événements à votre consommateur physique. Pour plus d’informations, consultez [création d’un consommateur logique](creating-a-logical-consumer.md).

 

 



