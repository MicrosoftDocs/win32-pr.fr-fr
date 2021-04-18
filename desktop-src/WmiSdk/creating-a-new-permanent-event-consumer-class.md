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
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106522685"
---
# <a name="creating-a-new-permanent-event-consumer-class"></a><span data-ttu-id="ec0ce-104">Création d’une classe de consommateur d’événements permanente</span><span class="sxs-lookup"><span data-stu-id="ec0ce-104">Creating a New Permanent Event Consumer Class</span></span>

<span data-ttu-id="ec0ce-105">L’une des premières étapes de la création d’un consommateur d’événements permanent consiste à créer la classe WMI qui décrit le consommateur d’événements.</span><span class="sxs-lookup"><span data-stu-id="ec0ce-105">One of the first steps in creating a permanent event consumer is to create the WMI class that describes the event consumer.</span></span> <span data-ttu-id="ec0ce-106">Plus précisément, la classe de consommateur d’événements permanent définit les paramètres de l’action implémentée par le consommateur physique.</span><span class="sxs-lookup"><span data-stu-id="ec0ce-106">Specifically, the permanent event consumer class defines the parameters of the action implemented by the physical consumer.</span></span>

<span data-ttu-id="ec0ce-107">La procédure suivante décrit comment créer une classe de consommateur d’événements permanente.</span><span class="sxs-lookup"><span data-stu-id="ec0ce-107">The following procedure describes how to create a permanent event consumer class.</span></span>

<span data-ttu-id="ec0ce-108">**Pour créer une classe de consommateur d’événements permanente**</span><span class="sxs-lookup"><span data-stu-id="ec0ce-108">**To create a permanent event consumer class**</span></span>

1.  <span data-ttu-id="ec0ce-109">Dérivez une classe de la classe système [**\_ \_ EventConsumer**](--eventconsumer.md) .</span><span class="sxs-lookup"><span data-stu-id="ec0ce-109">Derive a class from the [**\_\_EventConsumer**](--eventconsumer.md) system class.</span></span>
2.  <span data-ttu-id="ec0ce-110">Implémentez les paramètres nécessaires pour traiter une notification d’événements.</span><span class="sxs-lookup"><span data-stu-id="ec0ce-110">Implement any parameters necessary to process an event notification.</span></span>

<span data-ttu-id="ec0ce-111">L’exemple suivant illustre la syntaxe utilisée pour créer la classe SMTPConsumerEvent.</span><span class="sxs-lookup"><span data-stu-id="ec0ce-111">The following example shows the syntax used to create the SMTPConsumerEvent class.</span></span> <span data-ttu-id="ec0ce-112">Vous pouvez l’utiliser comme exemple pour créer votre nouvelle classe.</span><span class="sxs-lookup"><span data-stu-id="ec0ce-112">You can use this as an example for creating your new class.</span></span> <span data-ttu-id="ec0ce-113">La classe [**SMTPEventConsumer**](smtpeventconsumer.md) envoie un message électronique à l’aide du protocole SMTP (Simple Mail Transfer Protocol) chaque fois qu’un événement lui est remis.</span><span class="sxs-lookup"><span data-stu-id="ec0ce-113">The [**SMTPEventConsumer**](smtpeventconsumer.md) class sends an email message by using Simple Mail Transfer Protocol (SMTP) each time an event is delivered to it.</span></span> <span data-ttu-id="ec0ce-114">Cette classe est définie dans smtpcons. mof.</span><span class="sxs-lookup"><span data-stu-id="ec0ce-114">This class is defined in smtpcons.mof.</span></span>

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

<span data-ttu-id="ec0ce-115">Vous devez être en mesure de créer des instances de votre classe de consommateur d’événements permanent pour décrire une ou plusieurs manières d’envoyer des événements à votre consommateur physique.</span><span class="sxs-lookup"><span data-stu-id="ec0ce-115">You should be able to create instances of your permanent event consumer class to describe one or more ways to send events to your physical consumer.</span></span> <span data-ttu-id="ec0ce-116">Pour plus d’informations, consultez [création d’un consommateur logique](creating-a-logical-consumer.md).</span><span class="sxs-lookup"><span data-stu-id="ec0ce-116">For more information, see [Creating a Logical Consumer](creating-a-logical-consumer.md).</span></span>

 

 



