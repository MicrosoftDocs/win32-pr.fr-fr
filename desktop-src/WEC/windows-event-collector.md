---
title: Collecteur d'événements de Windows
description: Vous pouvez vous abonner pour recevoir et stocker des événements sur un ordinateur local (collecteur d’événements) qui sont transférés à partir d’un ordinateur distant (source d’événement).
ms.assetid: 7725e06d-4df1-4b3e-9f2f-2b8bdd805cb6
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3c4ef9e0cb647236daa55771222f25b7e0e370ef
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "106509852"
---
# <a name="windows-event-collector"></a>Collecteur d'événements de Windows

Vous pouvez vous abonner pour recevoir et stocker des événements sur un ordinateur local (collecteur d’événements) qui sont transférés à partir d’un ordinateur distant (source d’événement). Les [fonctions du collecteur d’événements Windows](windows-event-collector-functions.md) prennent en charge l’abonnement aux événements à l’aide du protocole WS-Management. Pour plus d’informations sur la gestion des services Web, consultez [à propos de Windows Remote Management](/windows/desktop/WinRM/about-windows-remote-management).

## <a name="event-forwarding-and-event-collection-architecture"></a>Transfert d’événements et architecture de la collecte d’événements

La collecte d’événements permet aux administrateurs d’obtenir des événements à partir d’ordinateurs distants et de les stocker dans un journal des événements local sur l’ordinateur collecteur. Le chemin d’accès du journal de destination pour les événements est une propriété de l’abonnement. Toutes les données de l’événement transféré sont enregistrées dans le journal des événements de l’ordinateur collecteur (aucune information n’est perdue). Des informations supplémentaires relatives au transfert d’événements sont également ajoutées à l’événement. Pour plus d’informations sur la façon d’activer un ordinateur pour recevoir des événements collectés ou transférer des événements, consultez [configurer des ordinateurs pour transférer et collecter des événements](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc748890(v=ws.11)).

## <a name="subscriptions"></a>Abonnements

La liste suivante décrit les types d’abonnements aux événements :

-   Abonnements initiés par la source : vous permet de définir un abonnement aux événements sur un ordinateur du collecteur d’événements sans définir les ordinateurs source des événements. Plusieurs ordinateurs sources d’événements distants peuvent être configurés (à l’aide d’un paramètre de stratégie de groupe) pour transférer les événements à l’ordinateur du collecteur d’événements. Pour plus d’informations, consultez [configuration d’un abonnement initié par la source](setting-up-a-source-initiated-subscription.md). Ce type d’abonnement est utile lorsque vous ne connaissez pas ou si vous ne souhaitez pas spécifier toutes les sources d’événements que les ordinateurs qui transféreront les événements.
-   Abonnements déclenchés par le collecteur : vous permet de créer un abonnement aux événements si vous connaissez tous les ordinateurs source d’événements qui transféreront les événements. Vous spécifiez toutes les sources d’événements au moment de la création de l’abonnement. Pour plus d’informations, consultez [création d’un abonnement initié par le collecteur](creating-an-event-collector-subscription.md).

## <a name="windows-event-collector-functions"></a>Fonctions du collecteur d’événements Windows

Pour plus d’informations et des exemples de code qui utilisent les fonctions du collecteur d’événements, consultez [utilisation du collecteur d’événements Windows](using-windows-event-collector.md).

Pour plus d’informations sur les fonctions utilisées pour collecter et transférer des événements, consultez [fonctions du collecteur d’événements Windows](windows-event-collector-functions.md).

 

 