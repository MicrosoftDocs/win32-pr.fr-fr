---
description: Une attention particulière doit être accordée aux expéditeurs ou aux destinataires PGM multirésidents. Cette page décrit les considérations et fournit des instructions pour les meilleures pratiques de programmation.
ms.assetid: 10fb56dd-3c96-4944-9b53-aee76c269528
title: Hébergement multiple et PGM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e19ab149c8068c1a13f2c8089a567157618ef7287e8ef632145e5b934d626c4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118112083"
---
# <a name="multihoming-and-pgm"></a>Hébergement multiple et PGM

Une attention particulière doit être accordée aux expéditeurs ou aux destinataires PGM multirésidents. Cette page décrit les considérations et fournit des instructions pour les meilleures pratiques de programmation.

## <a name="multihomed-pgm-sender"></a>Expéditeur PGM multirésident

Quand une application ne parvient pas à spécifier une interface lors de l’appel de la fonction [**Connect**](/windows/desktop/api/Winsock2/nf-winsock2-connect) , la première interface disponible est utilisée. Si aucune interface n’est disponible, la **connexion** échoue.

Lorsqu’une application spécifie une interface à l’aide de l’option [RM \_ Set \_ Send \_ If](socket-options.md) Socket, une tentative de [**liaison**](/windows/desktop/api/winsock/nf-winsock-bind) est effectuée implicitement vers cette interface à l’aide du protocole TCP/IP, et échoue si le protocole TCP/IP échoue à la demande de liaison. Si l’interface est définie à l’aide de RM \_ Set Send s’il y a \_ \_ plusieurs fois, seul le dernier ensemble d’interfaces est applicable.

Windows Sockets gère l’interface définie et, si cette interface disparaît, la session est déconnectée.

## <a name="multihomed-pgm-receiver"></a>Récepteur PGM multirésident

Quand une application ne parvient pas à spécifier une interface lors de l’appel de la fonction [**Listen**](/windows/desktop/api/Winsock2/nf-winsock2-listen) , l’interface par défaut est utilisée. Si aucune interface n’est disponible, la [**liaison**](/windows/desktop/api/winsock/nf-winsock-bind) échoue.

lorsqu’une application spécifie une ou plusieurs interfaces sur lesquelles écouter, à l’aide de [RM \_ ADD \_ RECEIVE \_ si](socket-options.md), Windows sockets tente de lier à l’interface ou aux interfaces demandées à l’aide de TCP/IP. Toute erreur de TCP/IP entraîne l’échec de cette requête. Contrairement au cas de l’expéditeur PGM, l’ajout de plusieurs fois à une interface de réception entraîne la publication de l’écoute sur toutes les interfaces ajoutées avec succès. Utilisez l' \_ \_ option recevoir si le socket RM del \_ pour arrêter l’écoute sur une interface.

Windows Les sockets ne maintiennent pas l’État sur plusieurs interfaces d’écoute spécifiées et s’appuient sur le protocole TCP/IP pour le faire. toutefois, une fois qu’une session est en cours, Windows sockets effectue le suivi de l’interface entrante pour cette session et, si cette interface disparaît, Windows sockets déconnecte la session.

 

 



