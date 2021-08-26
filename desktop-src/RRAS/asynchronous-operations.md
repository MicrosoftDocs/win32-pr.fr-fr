---
title: Opérations asynchrones
description: Lorsque RasDial est appelé en tant qu’opération asynchrone, la fonction retourne immédiatement.
ms.assetid: f165b4a7-00fb-4888-8225-8fd106e113f2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0db03b1d9d3c98e84bc9a2f4fd80ec7206d9a4524608cdbc96cca83f89d0ea00
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120030559"
---
# <a name="asynchronous-operations"></a>Opérations asynchrones

Lorsque [**rasdial**](/windows/desktop/api/Ras/nf-ras-rasdiala) est appelé en tant qu’opération asynchrone, la fonction retourne immédiatement. En mode asynchrone, l’appel de **rasdial** doit spécifier un [Gestionnaire de notification](notification-handlers.md) que le gestionnaire de connexions d’accès à distance utilise pour informer le client chaque fois que l’opération de connexion change d’État ou qu’une erreur se produit.

Le gestionnaire de notification peut être une fenêtre pour la réception de messages, ou une fonction de rappel [**RasDialFunc**](/windows/desktop/api/Ras/nc-ras-rasdialfunc), [**RasDialFunc1**](/windows/desktop/api/Ras/nc-ras-rasdialfunc1)ou [**RasDialFunc2**](/windows/desktop/api/Ras/nc-ras-rasdialfunc2) . Le gestionnaire de connexions d’accès à distance effectue ses notifications asynchrones dans le contexte du thread qui a effectué l’appel [**rasdial**](/windows/desktop/api/Ras/nf-ras-rasdiala) . Pour cette raison, le thread appelant ne doit se terminer que lorsque l’opération de connexion a été correctement établie ou qu’une erreur se produit. Comme en mode synchrone, l’application cliente peut se terminer en toute sécurité une fois que la connexion a été établie, et elle doit [arrêter l’opération de connexion](disconnecting.md) si une erreur se produit.

 

 




