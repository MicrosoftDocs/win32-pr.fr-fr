---
title: Instructions pour les services
description: Les services doivent adhérer à ces instructions pour s’assurer que le gestionnaire de redémarrage peut arrêter et redémarrer les services si nécessaire pour installer les mises à jour. Les applications peuvent utiliser les instructions décrites dans instructions pour les applications.
ms.assetid: 69a98f82-71bb-4780-8a3f-294cc5629900
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a6198da0d4f6f7887aaf37c858d98f3eb48e72c0d7722a1b5785a1cb280c96fa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119010137"
---
# <a name="guidelines-for-services"></a>Instructions pour les services

Les services doivent adhérer à ces instructions pour s’assurer que le gestionnaire de redémarrage peut arrêter et redémarrer les services si nécessaire pour installer les mises à jour. Les applications peuvent utiliser les instructions décrites dans [instructions pour les applications](guidelines-for-applications.md).

-   Les services doivent pouvoir être arrêtés et redémarrés à l’aide du [Gestionnaire de contrôle des services](/windows/desktop/Services/service-control-manager) sans nécessiter un redémarrage du système. Les exceptions à cette règle sont des processus système critiques qui s’exécutent dans le contexte d' lsass.exe ou de services.exe.
-   Le gestionnaire de redémarrage honore les dépendances de service. Lorsqu’un service est arrêté et redémarré, ses services dépendants sont arrêtés et redémarrés.
-   Les services doivent spécifier l’intervalle de récupération et la période de réinitialisation dans le [Gestionnaire de contrôle des services](/windows/desktop/Services/service-control-manager). L’intervalle de récupération est le temps, en millisecondes, après le dernier échec que le SCM attend avant d’effectuer l’action de récupération. La période de réinitialisation est le temps, en secondes, après le dernier échec que le gestionnaire de contrôle des services attend avant de réinitialiser le nombre d’échecs à 0. Les services peuvent utiliser la fonction [**ChangeServiceConfig2**](/windows/desktop/api/winsvc/nf-winsvc-changeserviceconfig2a) pour modifier les paramètres de configuration.

    Les [services critiques](critical-system-services.md) doivent utiliser les paramètres de récupération suivants pour spécifier que le service doit être redémarré une minute après le premier échec du redémarrage du service, redémarré deux minutes après le deuxième échec et que l’ordinateur doit être redémarré une minute après le troisième échec. Le nombre d’échecs est réinitialisé à 0 après 300 secondes.

    <dl> Actions de récupération : Restart/60000/restart/120000/reboot/60000 & Reset = 300  
    </dl>

    Les [services critiques](critical-system-services.md) doivent être démarrés avant les services non critiques. Les services qui ne sont pas des services essentiels doivent utiliser les paramètres de récupération suivants pour spécifier que le service doit être redémarré deux minutes après le premier échec de redémarrage du service. Le service n’est pas redémarré après la deuxième défaillance et un administrateur doit intervenir dans ce cas. Le nombre d’échecs est réinitialisé à 0 après 900 secondes.

    <dl> Actions de récupération : Restart/120000/restart/300000/None/0 & Reset = 900  
    </dl>

 

 