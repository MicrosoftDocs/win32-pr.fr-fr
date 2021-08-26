---
title: Démarrage de la demande sur la version 2,0 files d’attente de demandes
description: Démarrage de la demande sur la version 2,0 files d’attente de demandes
ms.assetid: 84a744b7-1b0e-4fa7-8015-4840251aa856
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f7ec5f0d2d973cfb7d4d0a3f23a5d1f6b6c6055dd9aff19521ed9ff100879c43
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120050789"
---
# <a name="demand-start-on-version-20-request-queues"></a>Démarrage de la demande sur la version 2,0 files d’attente de demandes

La fonctionnalité de démarrage à la demande des files d’attente de requêtes de l’API de la version 2,0 du serveur HTTP permet à l’application de contrôleur de retarder l’instanciation du processus de travail jusqu’à ce que la première requête arrive dans la file Ainsi, les applications peuvent éviter de consommer des ressources jusqu’à ce qu’elles soient nécessaires. Pour plus d’informations sur l’application de contrôleur, consultez la rubrique [file d’attente des demandes nommées](named-request-queue.md) .

## <a name="asynchronous-demand-start"></a>Démarrage à la demande asynchrone

L’application de contrôleur appelle [**HttpWaitForDemandStart**](/windows/desktop/api/Http/nf-http-httpwaitfordemandstart) avec le descripteur de la file d’attente des demandes pour lancer une notification de démarrage de la demande. Pour la saisie semi-automatique asynchrone, l’application fournit la structure OVERLAPPED dans le paramètre *pOverlapped* . Quand **HttpWaitForDemandStart** est appelé de façon asynchrone, l’application de contrôleur est avertie lorsque la première demande arrive dans la file d’attente de demandes. Une fois la notification de démarrage de la demande terminée, l’application de contrôleur peut s’inscrire pour une autre notification de démarrage de la demande dans la file d’attente des demandes.

L’API du serveur HTTP n’autorise pas plus d’une notification de démarrage de demande simultanée pour une file d’attente de demandes. Toutefois, lorsque la notification de démarrage de la demande en suspens se termine, l’application appelle à nouveau [**HttpWaitForDemandStart**](/windows/desktop/api/Http/nf-http-httpwaitfordemandstart) pour démarrer plusieurs processus de travail dans la file d’attente des demandes. HTTP n’applique pas de limitations sur le nombre de notifications de démarrage de la demande ou le nombre de processus de travail en attente dans la file d’attente des demandes. Toutefois, les applications de contrôleur peuvent appliquer le nombre de processus de travail autorisés dans une file d’attente de demandes.

L’API du serveur HTTP prend en charge l’annulation des appels [**HttpWaitForDemandStart**](/windows/desktop/api/Http/nf-http-httpwaitfordemandstart) asynchrones. Les applications peuvent utiliser [**CancelIoEx**](/windows/desktop/FileIO/cancelioex-func) avec la structure OVERLAPPED fournie dans *pOverlapped*, pour annuler un appel **HttpWaitForDemandStart** en suspens.

## <a name="synchronous-demand-start"></a>Démarrage à la demande synchrone

Le démarrage de la demande synchrone n’est pas recommandé, car l’application se bloque jusqu’à ce qu’une requête arrive dans la file d’attente des demandes.

 

 
