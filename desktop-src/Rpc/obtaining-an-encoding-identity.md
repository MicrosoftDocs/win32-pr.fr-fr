---
title: Obtention d’une identité d’encodage
description: Une application qui décode des données encodées peut obtenir l’identité de la routine utilisée pour encoder les données, avant d’appeler une routine pour la décoder. La routine MesInqProcEncodingId fournit cette identité.
ms.assetid: 53cbd6c5-b267-4ff1-a45b-7e22093f41a5
keywords:
- Appel de procédure distante RPC, tâches, obtention de l’identité d’encodage
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8591e030913d659fb48034e4c386295773227f7f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103674914"
---
# <a name="obtaining-an-encoding-identity"></a>Obtention d’une identité d’encodage

Une application qui décode des données encodées peut obtenir l’identité de la routine utilisée pour encoder les données, avant d’appeler une routine pour la décoder. La routine [**MesInqProcEncodingId**](/windows/desktop/api/Midles/nf-midles-mesinqprocencodingid) fournit cette identité.

Chaque procédure dans une interface est assignée à un numéro d’identification entier, appelé *identificateur de procédure* ou *ID de processus*, par le compilateur MIDL. La numérotation commence par zéro. Les bibliothèques Runtime RPC ne sont pas impliquées dans la conversion de l’ID de procédure en appel de procédure réel. Dans le cas d’un ID de procédure donné, votre application doit fournir un moyen d’appeler la procédure appropriée. En règle générale, les développeurs d’applications utilisent une série d’instructions **If** , ou (lors de l’utilisation de C/C++) une instruction **switch** à cet effet.

 

 




