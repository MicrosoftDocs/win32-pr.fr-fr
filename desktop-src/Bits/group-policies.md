---
title: Stratégies de groupe
description: Service de transfert intelligent en arrière-plan (BITS) utilise les stratégies de groupe suivantes pour configurer les paramètres et les transferts BITS. pour plus d’informations sur la version de BITS utilisée par les différentes versions de Windows, consultez la rubrique nouveautés.
ms.assetid: 32c7e2b1-bac2-4708-a30c-f6b2a816c1a4
ms.topic: article
ms.date: 10/04/2018
ms.openlocfilehash: f3ff0070c489759055bdaae1d2e68d8718a7bae5
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127296983"
---
# <a name="group-policies"></a>Stratégies de groupe

> [!NOTE]
> Pour plus d’informations sur l’utilisation de la gestion des appareils mobiles (MDM) pour définir des stratégies pour Service de transfert intelligent en arrière-plan (BITS), consultez la page [CSP de stratégie](/windows/client-management/mdm/policy-configuration-service-provider).

Service de transfert intelligent en arrière-plan (BITS) utilise les stratégies de groupe suivantes pour configurer les paramètres et les transferts BITS. pour plus d’informations sur la version de BITS utilisée par les différentes versions de Windows, consultez la rubrique [nouveautés](what-s-new.md) .

> [!NOTE]  
> Si la valeur de stratégie n’est pas définie, BITS utilise la valeur de stratégie par défaut.

**Pour activer une stratégie BITS**

1.  Ouvrez Stratégie de groupe en entrant **gpedit. msc/gpcomputer : «**_ComputerName_*_»_* dans la fenêtre **exécuter** ou à l’invite de commandes dans une fenêtre cmd.
2.  Les stratégies BITS se trouvent sous **Configuration ordinateur**, **modèles d’administration**, **réseau**, **service de transfert intelligent en arrière-plan**.
3.  Cliquez avec le bouton droit sur la stratégie, puis sélectionnez **modifier**.
4.  Suivez les instructions relatives à l’activation et à la définition de la stratégie.

les stratégies de groupe pour BITS se trouvent dans le registre à l’adresse **HKEY \_ LOCAL \_ MACHINE** \\ **Software** \\ **policies** \\ **Microsoft** \\ **Windows** \\ **BITS**. Notez que seules les stratégies configurées sont répertoriées dans le registre.

|Stratégie|Description|
|-|-|
|Paramètre jobinactivitytimeout<br/>BITS 1,0|Par défaut, le service BITS conserve les informations relatives à un travail pendant 90 jours. S’il n’y a aucune activité sur le travail pour cette période, BITS annule le travail. La progression du transfert ou les modifications de propriété réinitialisent la minuterie.<br/> Vous devrez peut-être ajuster cette stratégie si l’utilisateur ne se connecte pas ou ne gère pas une connexion réseau pendant de longues périodes.|
|MaxInternetBandwidth<br/>BITS 2,0|Limite la bande passante réseau utilisée par BITS pour les transferts en arrière-plan (cette stratégie n’affecte pas les transferts de premier plan).<br/>Spécifiez une limite à utiliser pendant un intervalle de temps spécifique et une limite à utiliser à tout moment. Par exemple, limitez l’utilisation de la bande passante réseau à 10 kilobits par seconde (Kbits/s) à 8:00 h 00. à 5:00 h 00 et utilisent toute la bande passante disponible inutilisée le reste du temps.<br/>**Remarque**: la modification de l’horloge système n’affecte pas l’intervalle de temps de limitation de bande passante. Par exemple, si l’heure actuelle est 2:00 P.M. et l’intervalle de limitation de la bande passante commence à 3:00 P.M., le déplacement de l’horloge système vers l’avant une heure ne signifie pas que le service BITS applique la limitation de bande passante. une heure au début de la limitation de bande passante se produira toujours en une heure. Pour refléter la modification de l’horloge système dans BITS, vous devez redémarrer l’ordinateur ou le service BITS.<br/>Spécifiez la limite en kilobits par seconde. Basez la limite de la taille de la liaison réseau, et non la taille de la carte d’interface réseau (NIC) de l’ordinateur. BITS utilise approximativement deux kilobits si vous spécifiez une valeur inférieure à 2 kilobits. Pour empêcher les transferts BITS, spécifiez une limite de zéro. Si vous spécifiez une limite égale à zéro, le service BITS place toutes les tâches en arrière-plan dans un état d’erreur temporaire. (Le code d’erreur est défini sur BG_E_BLOCKED_BY_POLICY.) Le service BITS place les tâches dans l’État en file d’attente après l’expiration de l’intervalle de temps.<br/> Si vous désactivez ou ne configurez pas cette stratégie, BITS utilise toute la bande passante disponible inutilisée.<br/> En règle générale, vous utilisez cette stratégie pour empêcher les transferts BITS de concurrence pour la bande passante réseau lorsque le client dispose d’une carte réseau rapide (10 Mbits/s), mais qu’il est connecté au réseau via une liaison lente (56 Kbits/s).<br/> Pour plus d’informations sur la façon dont le service BITS utilise la bande passante réseau, consultez [bande passante réseau](network-bandwidth.md).|
|MaxDownloadTime<br/>BITS 3,0|Détermine la durée pendant laquelle le service BITS peut transférer activement les fichiers du travail. La valeur par défaut est de 90 jours.<br/> Pour remplacer cette stratégie pour un travail spécifique, appelez la méthode [**IBackgroundCopyJob4 :: SetMaximumDownloadTime**](/windows/desktop/api/bits3_0/nf-bits3_0-ibackgroundcopyjob4-setmaximumdownloadtime) .|
|MaxJobsPerMachine<br/>BITS 3,0|Limite le nombre de travaux que les utilisateurs peuvent créer sur l’ordinateur. La valeur par défaut est 300 travaux. Cette stratégie ne s’applique pas à un utilisateur disposant de privilèges d’administrateur ou de comptes de service.|
|MaxJobsPerUser<br/>BITS 3,0|Limite le nombre de travaux qu’un utilisateur peut créer sur l’ordinateur. La valeur par défaut est 60 travaux par utilisateur. Cette stratégie ne s’applique pas à un utilisateur disposant de privilèges d’administrateur ou de comptes de service.|
|MaxFilesPerJob<br/>BITS 3,0|Limite le nombre de fichiers qu’un utilisateur peut ajouter à un travail. La valeur par défaut est 200 fichiers par travail. Cette stratégie ne s’applique pas à un utilisateur disposant de privilèges d’administrateur ou de comptes de service.|
|MaxRangesPerFile<br/>BITS 3,0|Limite le nombre de plages qu’un utilisateur peut spécifier pour un fichier. La valeur par défaut est 500 plages. Cette stratégie ne s’applique pas à un utilisateur disposant de privilèges d’administrateur ou de comptes de service.|

BITS utilise les stratégies de groupe suivantes pour activer et configurer la manière dont le service BITS interagit avec BranchCache.

|Stratégie|Description|
|-|-|
|DisableBranchCache<br/>BITS 4,0|par défaut, la fonctionnalité Windows BranchCache est activée. définissez cette stratégie pour empêcher les clients BITS de transférer du contenu à l’aide de la Windows BranchCache.<br/>**remarque**: ce paramètre n’affecte pas l’utilisation de Windows BranchCache par les applications autres que BITS. Cette stratégie ne s’applique pas aux transferts BITS par le biais du protocole SMB (Server Message Block). ce paramètre n’a aucun effet si les paramètres d’administration de l’ordinateur pour Windows Branch Cache désactivent son utilisation complète.|

Le service BITS utilise les stratégies de groupe suivantes pour configurer la limitation de bande passante.

|Stratégie|Description|
|-|-|
|EnableMaintenanceLimits<br/>BITS 4,0|Limite la bande passante réseau utilisée par BITS pour les transferts en arrière-plan pendant les jours et les heures de maintenance. Les planifications de maintenance limitent davantage la bande passante réseau utilisée pour les transferts en arrière-plan.<br/> Spécifiez une limite à utiliser pour les tâches en arrière-plan pendant une planification de maintenance. Par exemple, si les tâches de priorité normale sont actuellement limitées à 256 kbits/s sur une planification de travail, vous pouvez limiter la bande passante réseau des tâches de priorité normale à 0 kbit/s à partir de 8:00 h 00. à 10h00. dans le cas d’une planification de maintenance.<br/>**Remarque**: les limites de bande passante définies pour la période de maintenance remplacent toutes les limites définies pour le travail et d’autres planifications.|
|EnableBandwidthLimits<br/>BITS 4,0|Limite la bande passante réseau utilisée par BITS pour les transferts en arrière-plan pendant les jours et les heures de travail et non-travail. La planification des tâches est définie à l’aide d’un calendrier hebdomadaire, qui comprend les jours de la semaine et les heures de la journée. Toutes les heures et tous les jours qui ne sont pas définis dans une planification de travail sont considérés comme des heures chômées.<br/> Spécifiez une limite à utiliser pour les tâches en arrière-plan pendant une planification de travail. Par exemple, vous pouvez limiter la bande passante réseau des tâches à faible priorité à 128 Kbits/s à partir de 8:00 h 00. à 5:00 h 00 du lundi au vendredi, puis définissez la limite à 512 kbits/s pour les heures chômées.|


## <a name="related-topics"></a>Rubriques connexes
* [Fournisseur CSP Policy](/windows/client-management/mdm/policy-configuration-service-provider)
