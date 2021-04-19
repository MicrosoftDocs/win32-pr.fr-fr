---
description: Une attention particulière doit être accordée aux expéditeurs ou aux destinataires PGM multirésidents. Cette page décrit les considérations et fournit des instructions pour les meilleures pratiques de programmation.
ms.assetid: 10fb56dd-3c96-4944-9b53-aee76c269528
title: Hébergement multiple et PGM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 142527c7fdf3e5d34d80c51e4002bc21ad47691c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106516871"
---
# <a name="multihoming-and-pgm"></a>Hébergement multiple et PGM

Une attention particulière doit être accordée aux expéditeurs ou aux destinataires PGM multirésidents. Cette page décrit les considérations et fournit des instructions pour les meilleures pratiques de programmation.

## <a name="multihomed-pgm-sender"></a>Expéditeur PGM multirésident

Quand une application ne parvient pas à spécifier une interface lors de l’appel de la fonction [**Connect**](/windows/desktop/api/Winsock2/nf-winsock2-connect) , la première interface disponible est utilisée. Si aucune interface n’est disponible, la **connexion** échoue.

Lorsqu’une application spécifie une interface à l’aide de l’option [RM \_ Set \_ Send \_ If](socket-options.md) Socket, une tentative de [**liaison**](/windows/desktop/api/winsock/nf-winsock-bind) est effectuée implicitement vers cette interface à l’aide du protocole TCP/IP, et échoue si le protocole TCP/IP échoue à la demande de liaison. Si l’interface est définie à l’aide de RM \_ Set Send s’il y a \_ \_ plusieurs fois, seul le dernier ensemble d’interfaces est applicable.

Windows Sockets gère l’interface définie et, si cette interface disparaît, la session est déconnectée.

## <a name="multihomed-pgm-receiver"></a>Récepteur PGM multirésident

Quand une application ne parvient pas à spécifier une interface lors de l’appel de la fonction [**Listen**](/windows/desktop/api/Winsock2/nf-winsock2-listen) , l’interface par défaut est utilisée. Si aucune interface n’est disponible, la [**liaison**](/windows/desktop/api/winsock/nf-winsock-bind) échoue.

Lorsqu’une application spécifie une ou plusieurs interfaces sur lesquelles écouter, à l’aide de [RM \_ Add \_ Receive \_ si](socket-options.md), Windows Sockets tente de se lier à l’interface ou aux interfaces demandées à l’aide de TCP/IP. Toute erreur de TCP/IP entraîne l’échec de cette requête. Contrairement au cas de l’expéditeur PGM, l’ajout de plusieurs fois à une interface de réception entraîne la publication de l’écoute sur toutes les interfaces ajoutées avec succès. Utilisez l' \_ \_ option recevoir si le socket RM del \_ pour arrêter l’écoute sur une interface.

Windows Sockets ne conserve pas l’État sur plusieurs interfaces d’écoute spécifiées et s’appuie plutôt sur le protocole TCP/IP pour le faire. Toutefois, une fois qu’une session est en cours, les sockets Windows effectuent le suivi de l’interface entrante pour cette session et, si cette interface disparaît, Windows Sockets déconnecte la session.

 

 



