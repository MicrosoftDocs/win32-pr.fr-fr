---
description: L’opération de réponse est une réponse classique des applications à une session de communication proposée. En cas de réussite, cette opération entraîne la transition d’une session dans l’état connecté.
ms.assetid: 34ac0b34-1d1b-4657-a737-27a4ed9326af
title: Réponse
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2e08081b32b7ba3a3a24cde3ec37c1a6118582cf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104529223"
---
# <a name="answer"></a>Réponse

L’opération de réponse est une réponse classique d’une application à une session de communication proposée. En cas de réussite, cette opération entraîne la transition d’une session dans l’état connecté.

Dans certains environnements de téléphonie (comme RNIS), où les alertes utilisateur sont séparées de l’offre d’appel, l’application a la possibilité d' [accepter](accept-ovr.md) un appel avant de répondre ou de rejeter ([supprimer](drop-ovr.md)) ou de [Rediriger](redirect-ovr.md) l’appel d' *offre* .

Si une opération de réponse est effectuée pour une nouvelle session lorsqu’une session est déjà active, l’effet de cette opération sur la session active existante dépend des fonctionnalités du fournisseur de services. Le premier appel ne peut pas être affecté, il peut être supprimé automatiquement ou placé automatiquement en attente. L’interface TAPI enverra les notifications d’événements appropriées concernant les deux appels.

Dans une situation de pont, si un appel est connecté mais se trouve dans l’état actif, il peut être joint à l’aide de l’opération de réponse.

L’application a la possibilité d’envoyer des informations sur l’utilisateur au moment de la réponse, si le fournisseur de services la prend en charge.

**TAPI 2. x :** Consultez [**lineAnswer**](/windows/win32/api/tapi/nf-tapi-lineanswer).

**TAPI 3. x :** Consultez [**ITBasicCallControl :: Answer**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol-answer).

 

 
