---
description: Pour démarrer un service ou un service de pilote, le programme de contrôle des services utilise la fonction StartService.
ms.assetid: 7d2ee779-1554-436a-a65c-f0322745f46a
title: Démarrage du service
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 17901987581b6a2680e0a70cfe2e0ed80472d293cbe32932f768e9133b6a058d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118888698"
---
# <a name="service-startup"></a>Démarrage du service

Pour démarrer un service ou un service de pilote, le programme de contrôle des services utilise la fonction [**StartService**](/windows/desktop/api/Winsvc/nf-winsvc-startservicea) . La fonction **StartService** échoue si la base de données est verrouillée. Dans ce cas, le programme de contrôle des services doit attendre quelques secondes et appeler à nouveau **StartService** . Il peut vérifier l’état de verrouillage actuel de la base de données en appelant la fonction [**QueryServiceLockStatus**](/windows/desktop/api/Winsvc/nf-winsvc-queryservicelockstatusa) .

Si le programme de contrôle des services démarre un service, il peut utiliser la fonction [**StartService**](/windows/desktop/api/Winsvc/nf-winsvc-startservicea) pour spécifier un tableau d’arguments à passer à la fonction [**ServiceMain**](/windows/win32/api/winsvc/nc-winsvc-lpservice_main_functiona) du service. La fonction **StartService** retourne une valeur après qu’un nouveau thread a été créé pour exécuter la fonction **ServiceMain** . Le programme de contrôle de service peut récupérer l’état du service qui vient d’être démarré dans une structure d' [**\_ État de service**](/windows/desktop/api/Winsvc/ns-winsvc-service_status) en appelant la fonction [**QueryServiceStatus**](/windows/desktop/api/Winsvc/nf-winsvc-queryservicestatus) . Pendant l’initialisation, le membre **dwCurrentState** doit être \_ en attente de démarrage de service \_ . Le membre **dwWaitHint** est un intervalle de temps, en millisecondes, qui indique la durée d’attente du programme de contrôle des services avant d’appeler à nouveau **QueryServiceStatus** . Une fois l’initialisation terminée, le service change **dwCurrentState** en service \_ Running.

Le gestionnaire de contrôle des services ne prend pas en charge la transmission de variables d’environnement personnalisées à un service au démarrage. En outre, le gestionnaire de contrôle des services ne détecte pas les modifications apportées aux variables d’environnement lorsque le service est en cours d’exécution. Au lieu de rendre un service dépendant d’une variable d’environnement, utilisez des valeurs de registre ou des arguments de [**ServiceMain**](/windows/win32/api/winsvc/nc-winsvc-lpservice_main_functiona) .

Voici une vue d’ensemble simplifiée de ce qui se passe quand un service standard est démarré par le gestionnaire de contrôle des services :

-   Le SCM lit le chemin d’accès du service à partir du Registre et prépare le démarrage du service. Cela comprend l’acquisition du verrou de service. Toute tentative de démarrage d’un autre service alors que le verrou de service est maintenu est bloquée jusqu’à ce que le verrou de service soit libéré.
-   Le SCM démarre le processus et attend que le processus enfant se termine (indiquant un échec) ou signale l’état d’exécution du SERVICE \_ .
-   L’application effectue son initialisation très simple et appelle la fonction [**StartServiceCtrlDispatcher**](/windows/desktop/api/Winsvc/nf-winsvc-startservicectrldispatchera) .
-   [**StartServiceCtrlDispatcher**](/windows/desktop/api/Winsvc/nf-winsvc-startservicectrldispatchera) se connecte au gestionnaire de contrôle des services et démarre un deuxième thread qui appelle la fonction [**ServiceMain**](/windows/win32/api/winsvc/nc-winsvc-lpservice_main_functiona) pour le service. La fonction **ServiceMain** doit signaler le service \_ s’exécuter dès que possible.
-   Quand le gestionnaire de contrôle des services est informé que le service est en cours d’exécution, il libère le verrou de service.

Si le service ne met pas à jour son état dans un délai de 80 secondes, plus le dernier indicateur Wait, le gestionnaire de contrôle des services détermine que le service a cessé de répondre. Le gestionnaire de contrôle des services consigne un événement et arrête le service.

Si le programme démarre un service de pilote, [**StartService**](/windows/desktop/api/Winsvc/nf-winsvc-startservicea) retourne une valeur une fois que le pilote de périphérique a terminé son initialisation.

Pour plus d’informations, consultez [démarrage d’un service](starting-a-service.md).

 

 
