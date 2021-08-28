---
description: L’état de l’alimentation du système indique si la source d’alimentation d’un ordinateur est une batterie du système ou une alimentation secteur. Pour les ordinateurs qui utilisent des batteries, l’état de l’alimentation du système indique également la durée de vie de la batterie et la charge de la batterie.
ms.assetid: b9a5e7de-a603-4bd9-b854-1e58572c3b2b
title: État de l’alimentation du système
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1bc73f022d54536272b51c58f8fa601e65a2c1b042968d2db8324bfb63449f40
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119143292"
---
# <a name="system-power-status"></a>État de l’alimentation du système

L’état de l’alimentation du système indique si la source d’alimentation d’un ordinateur est une batterie du système ou une alimentation secteur. Pour les ordinateurs qui utilisent des batteries, l’état de l’alimentation du système indique également la durée de vie de la batterie et la charge de la batterie.

Les informations d’alimentation sont récupérées en s’inscrivant pour les notifications de paramètre d’alimentation via la fonction [**RegisterPowerSettingNotification**](/windows/desktop/api/WinUser/nf-winuser-registerpowersettingnotification) . Cette fonction permet aux applications de s’inscrire pour des paramètres d’alimentation spécifiques et de recevoir une notification en cas de changement.

> [!Note]  
> Pour rechercher des informations sur l’état de l’alimentation sans notifications, utilisez [**CallNtPowerInformation**](/windows/desktop/api/Powerbase/nf-powerbase-callntpowerinformation).

 

Les applications et les pilotes installables utilisent généralement l’état de l’alimentation du système pour déterminer si la poursuite de l’opération est possible. Par exemple, avant qu’une application effectue des opérations en arrière-plan, telles que la compression ou la pagination d’un fichier, elle doit vérifier si le système se trouve sur batteries. Autre exemple : une application qui commence une longue opération doit vérifier l’État pour déterminer s’il existe suffisamment de batterie pour terminer l’opération.

Par défaut, le système n’interroge pas les applications ou les pilotes pendant les transitions de veille.

> [!Note]  
> Si la puissance est faible, une application peut demander l’intervention de l’utilisateur ou demander que le système s’interrompt. Vous pouvez suspendre le fonctionnement du système à l’aide de la fonction [**SetSuspendState**](/windows/desktop/api/PowrProf/nf-powrprof-setsuspendstate) .

 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[À propos de la gestion de l’alimentation](about-power-management.md)
</dt> </dl>

 

 



