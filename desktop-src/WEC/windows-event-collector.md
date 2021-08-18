---
title: Collecteur d'événements de Windows
description: Vous pouvez vous abonner pour recevoir et stocker des événements sur un ordinateur local (collecteur d’événements) qui sont transférés à partir d’un ordinateur distant (source d’événement).
ms.assetid: 7725e06d-4df1-4b3e-9f2f-2b8bdd805cb6
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1efa767ecb80960fc3461380435ea1d44992656d7c67df990574f7155ee976fd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118997879"
---
# <a name="windows-event-collector"></a>Collecteur d'événements de Windows

Vous pouvez vous abonner pour recevoir et stocker des événements sur un ordinateur local (collecteur d’événements) qui sont transférés à partir d’un ordinateur distant (source d’événement). les [fonctions du collecteur d’événements Windows](windows-event-collector-functions.md) prennent en charge l’abonnement aux événements à l’aide du protocole WS-Management. pour plus d’informations sur la gestion des services web, consultez [à propos de Windows Remote Management](/windows/desktop/WinRM/about-windows-remote-management).

## <a name="event-forwarding-and-event-collection-architecture"></a>Transfert d’événements et architecture de la collecte d’événements

La collecte d’événements permet aux administrateurs d’obtenir des événements à partir d’ordinateurs distants et de les stocker dans un journal des événements local sur l’ordinateur collecteur. Le chemin d’accès du journal de destination pour les événements est une propriété de l’abonnement. Toutes les données de l’événement transféré sont enregistrées dans le journal des événements de l’ordinateur collecteur (aucune information n’est perdue). Des informations supplémentaires relatives au transfert d’événements sont également ajoutées à l’événement. Pour plus d’informations sur la façon d’activer un ordinateur pour recevoir des événements collectés ou transférer des événements, consultez [configurer des ordinateurs pour transférer et collecter des événements](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc748890(v=ws.11)).

## <a name="subscriptions"></a>Abonnements

La liste suivante décrit les types d’abonnements aux événements :

-   Abonnements initiés par la source : vous permet de définir un abonnement aux événements sur un ordinateur du collecteur d’événements sans définir les ordinateurs source des événements. Plusieurs ordinateurs sources d’événements distants peuvent être configurés (à l’aide d’un paramètre de stratégie de groupe) pour transférer les événements à l’ordinateur du collecteur d’événements. Pour plus d’informations, consultez [configuration d’un abonnement initié par la source](setting-up-a-source-initiated-subscription.md). Ce type d’abonnement est utile lorsque vous ne connaissez pas ou si vous ne souhaitez pas spécifier toutes les sources d’événements que les ordinateurs qui transféreront les événements.
-   Abonnements déclenchés par le collecteur : vous permet de créer un abonnement aux événements si vous connaissez tous les ordinateurs source d’événements qui transféreront les événements. Vous spécifiez toutes les sources d’événements au moment de la création de l’abonnement. Pour plus d’informations, consultez [création d’un abonnement initié par le collecteur](creating-an-event-collector-subscription.md).

## <a name="windows-event-collector-functions"></a>Windows Fonctions du collecteur d’événements

pour plus d’informations et des exemples de code qui utilisent les fonctions du collecteur d’événements, consultez [utilisation de Windows collecteur d’événements](using-windows-event-collector.md).

pour plus d’informations sur les fonctions utilisées pour collecter et transférer des événements, consultez [Windows fonctions du collecteur d’événements](windows-event-collector-functions.md).

 

 