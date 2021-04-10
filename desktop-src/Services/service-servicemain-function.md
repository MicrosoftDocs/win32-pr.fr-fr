---
description: Lorsqu’un programme de contrôle de service demande l’exécution d’un nouveau service, le gestionnaire de contrôle des services (SCM) démarre le service et envoie une demande de démarrage au répartiteur de contrôle.
ms.assetid: e55e056f-7628-4e3d-9aea-b55c371b4287
title: Fonction de service ServiceMain
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ed50f0f378f348415e56827a09fcf17eea7fc330
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103952879"
---
# <a name="service-servicemain-function"></a>Fonction de service ServiceMain

Lorsqu’un programme de contrôle de service demande l’exécution d’un nouveau service, le gestionnaire de contrôle des services (SCM) démarre le service et envoie une demande de démarrage au répartiteur de contrôle. Le répartiteur de contrôle crée un nouveau thread pour exécuter la fonction [**ServiceMain**](/windows/win32/api/winsvc/nc-winsvc-lpservice_main_functiona) pour le service. Pour obtenir un exemple, consultez [écriture d’une fonction ServiceMain](writing-a-servicemain-function.md).

La fonction [**ServiceMain**](/windows/win32/api/winsvc/nc-winsvc-lpservice_main_functiona) doit effectuer les tâches suivantes :

1.  Initialiser toutes les variables globales.
2.  Appelez la fonction [**RegisterServiceCtrlHandler**](/windows/desktop/api/Winsvc/nf-winsvc-registerservicectrlhandlera) immédiatement pour inscrire une fonction de [**Gestionnaire**](/windows/desktop/api/Winsvc/nc-winsvc-lphandler_function) afin de gérer les demandes de contrôle pour le service. La valeur de retour de **RegisterServiceCtrlHandler** est un *handle d’état de service* qui sera utilisé dans les appels pour notifier le SCM de l’état du service.
3.  Effectuez l’initialisation. Si la durée d’exécution du code d’initialisation est supposée être très brève (moins d’une seconde), l’initialisation peut être effectuée directement dans [**ServiceMain**](/windows/win32/api/winsvc/nc-winsvc-lpservice_main_functiona).

    Si la durée d’initialisation est supposée être supérieure à une seconde, le service doit utiliser l’une des techniques d’initialisation suivantes :

    -   Appelez la fonction [**SetServiceStatus**](/windows/desktop/api/Winsvc/nf-winsvc-setservicestatus) pour signaler l' \_ exécution du service, mais n’acceptez aucun contrôle tant que l’initialisation n’est pas terminée. Pour ce faire, le service appelle **SetServiceStatus** avec **DWCURRENTSTATE** défini sur service \_ Running et **dwControlsAccepted** défini sur 0 dans la structure d' [**\_ État du service**](/windows/desktop/api/Winsvc/ns-winsvc-service_status) . Cela garantit que le SCM n’enverra pas de demandes de contrôle au service avant qu’il ne soit prêt et libère le SCM pour gérer d’autres services. Cette approche de l’initialisation est recommandée pour les performances, en particulier pour les services de démarrage automatique.
    -   Démarrage du \_ service \_ de rapport en attente, aucun contrôle n’est accepté et spécifiez un indicateur d’attente. Si le code d’initialisation de votre service exécute des tâches qui sont censées durer plus longtemps que la valeur de l’indicateur d’attente initial, votre code doit appeler la fonction [**SetServiceStatus**](/windows/desktop/api/Winsvc/nf-winsvc-setservicestatus) régulièrement (éventuellement avec un indicateur d’attente révisé) pour indiquer que la progression est en cours. Veillez à appeler **SetServiceStatus** uniquement si l’initialisation progresse. Dans le cas contraire, le SCM peut attendre que votre service passe à l’état d’exécution du SERVICE en \_ supposant que votre service progresse et bloque le démarrage d’autres services. N’appelez pas **SetServiceStatus** à partir d’un thread séparé, sauf si vous êtes sûr que le thread effectuant l’initialisation est réellement en cours de réalisation.

        Un service qui utilise cette approche peut également spécifier une valeur de point d’enregistrement et incrémenter la valeur périodiquement au cours d’une initialisation longue. Le programme qui a démarré le service peut appeler [**QueryServiceStatus**](/windows/desktop/api/Winsvc/nf-winsvc-queryservicestatus) ou [**QueryServiceStatusEx**](/windows/desktop/api/Winsvc/nf-winsvc-queryservicestatusex) pour obtenir la dernière valeur de point d’enregistrement auprès du SCM et utiliser la valeur pour signaler la progression incrémentielle à l’utilisateur.

4.  Une fois l’initialisation terminée, appelez [**SetServiceStatus**](/windows/desktop/api/Winsvc/nf-winsvc-setservicestatus) pour définir l’état du SERVICE sur service \_ Running et spécifiez les contrôles que le service est prêt à accepter. Pour obtenir la liste des contrôles, consultez la structure de l' [**\_ État du service**](/windows/desktop/api/Winsvc/ns-winsvc-service_status) .
5.  Effectuez les tâches du service ou, si aucune tâche n’est en attente, retournez le contrôle à l’appelant. Toute modification de l’état du service justifie un appel à [**SetServiceStatus**](/windows/desktop/api/Winsvc/nf-winsvc-setservicestatus) pour signaler de nouvelles informations d’État.
6.  Si une erreur se produit pendant que le service est en cours d’initialisation ou en cours d’exécution, le service doit appeler [**SetServiceStatus**](/windows/desktop/api/Winsvc/nf-winsvc-setservicestatus) pour définir l’état du service sur l’arrêt du service \_ \_ en attente si le nettoyage est long. Une fois le nettoyage terminé, appelez **SetServiceStatus** pour définir l’état du SERVICE sur service \_ arrêté à partir du dernier thread à terminer. Veillez à définir les membres **dwServiceSpecificExitCode** et **dwWin32ExitCode** de la structure d' [**\_ État du service**](/windows/desktop/api/Winsvc/ns-winsvc-service_status) pour identifier l’erreur.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Écriture d’une fonction ServiceMain](writing-a-servicemain-function.md)
</dt> </dl>

 

 
