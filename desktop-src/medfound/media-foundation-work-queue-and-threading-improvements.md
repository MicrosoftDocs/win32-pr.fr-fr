---
description: cette rubrique décrit les améliorations apportées à Windows 8 pour les files d’attente de travail et les threads dans la plateforme Microsoft Media Foundation.
ms.assetid: 9E2A1D94-BF82-488E-8297-D524683ABE17
title: Améliorations de la file d’attente de travail et du thread
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 07b307cb00316696e075e9e9cc2a138e98e149be
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127524257"
---
# <a name="work-queue-and-threading-improvements"></a>Améliorations de la file d’attente de travail et du thread

cette rubrique décrit les améliorations apportées à Windows 8 pour les files d’attente de travail et les threads dans la plateforme Microsoft Media Foundation.

-   [comportement de Windows 7](#windows-7-behavior)
    -   [Files d’attente de travail](#work-queues)
    -   [Prise en charge de MMCSS](#mmcss-support)
    -   [IMFRealTimeClient](#imfrealtimeclientex)
-   [Windows 8 Optimisation](#windows-8-improvements)
    -   [Files d’attente de travail multithread](#multithreaded-work-queues)
    -   [Files d’attente de travail des tâches partagées](#shared-task-work-queues)
    -   [File d’attente](#wait-queue)
    -   [Améliorations apportées à la prise en charge de MMCSS](#enhancements-to-mmcss-support)
    -   [IMFRealTimeClientEx](#imfrealtimeclientex)
    -   [Branches de topologie](#topology-branches)
-   [Recommandations](#recommendations)
-   [Résumé](#summary)
-   [Rubriques connexes](#related-topics)

## <a name="windows-7-behavior"></a>comportement de Windows 7

cette section résume le comportement de Media Foundation files d’attente de travail dans Windows 7.

### <a name="work-queues"></a>Files d’attente de travail

La plateforme Media Foundation crée plusieurs files d’attente de travail standard. Seules deux sont documentées comme étant destinées à une utilisation générale des applications :

-   **\_ \_ file d’attente de rappel MFASYNC \_ standard**
-   **\_fonction longue de la \_ file d’attente de rappel MFASYNC \_ \_**

Une application ou un composant peut allouer de nouvelles files d’attente de travail en appelant [**MFAllocateWorkQueue**](/windows/desktop/api/mfapi/nf-mfapi-mfallocateworkqueue) ou [**MFAllocateWorkQueueEx**](/windows/desktop/api/mfapi/nf-mfapi-mfallocateworkqueueex). La fonction **MFAllocateWorkQueueEx** définit deux types de file d’attente de travail :

-   **MF \_ \_WORKQUEUE standard** crée une file d’attente de travail sans boucle de message.
-   **MF \_ La fenêtre \_ WORKQUEUE** crée une file d’attente de travail avec une boucle de message.

Pour effectuer la mise en file d’attente d’un élément de travail, appelez [**MFPutWorkItem**](/windows/desktop/api/mfapi/nf-mfapi-mfputworkitem) ou [**MFPutWorkItemEx**](/windows/desktop/api/mfapi/nf-mfapi-mfputworkitemex). La plateforme exécute l’élément de travail en appelant l’implémentation fournie par l’appelant de [**IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback). dans Windows 7 et les versions antérieures, la plateforme crée un thread par file d’attente de travail.

### <a name="mmcss-support"></a>Prise en charge de MMCSS

Le [service Planificateur de classes multimédias](../procthread/multimedia-class-scheduler-service.md) (MMCSS) gère les priorités des threads afin que les applications multimédias reçoivent des tranches régulières du temps processeur, sans refuser les ressources du processeur aux applications de faible priorité. MMCSS définit un ensemble de *tâches* qui ont des profils d’utilisation de l’UC différents. Quand un thread rejoint une tâche MMCSS, MMCSS définit la priorité du thread en fonction de plusieurs facteurs :

-   Priorité de base de la tâche, qui est définie dans le registre.
-   Priorité de thread relative, qui est définie au moment de l’exécution en appelant [**AvSetMmThreadPriority**](/windows/win32/api/avrt/nf-avrt-avsetmmthreadpriority).
-   Différentes caractéristiques d’exécution, par exemple si l’application est au premier plan, et la quantité de temps processeur consommée par les threads dans chaque classe MMCSS.

Une application peut inscrire une file d’attente de travail avec MMCSS en appelant [**MFBeginRegisterWorkQueueWithMMCSS**](/windows/desktop/api/mfapi/nf-mfapi-mfbeginregisterworkqueuewithmmcss). Cette fonction prend un ID de file d’attente de travail, une classe MMCSS (nom de tâche) et l’identificateur de tâche MMCSS. En interne, il appelle [**AvSetMmThreadCharacteristics**](/windows/win32/api/avrt/nf-avrt-avsetmmthreadcharacteristicsa) avec le nom de tâche et l’ID de tâche. Une fois qu’une file d’attente de travail est inscrite auprès de MMCSS, vous pouvez obtenir la classe et l’ID de tâche en appelant [**MFGetWorkQueueMMCSSClass**](/windows/desktop/api/mfapi/nf-mfapi-mfgetworkqueuemmcssclass) et [**MFGetWorkQueueMMCSSTaskId**](/windows/desktop/api/mfapi/nf-mfapi-mfgetworkqueuemmcsstaskid).

La [session multimédia](media-session.md) fournit un accès de niveau plus élevé à ces API, via l’interface [**IMFWorkQueueServices**](/windows/desktop/api/mfidl/nn-mfidl-imfworkqueueservices) . Cette interface fournit deux méthodes principales :

| Méthode                                                                                                            | Description                                                                                                                                                                                                                                                                                   |
|-------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**BeginRegisterPlatformWorkQueueWithMMCSS**](/windows/desktop/api/mfidl/nf-mfidl-imfworkqueueservices-beginregisterplatformworkqueuewithmmcss)   | Inscrit une file d’attente de travail avec une tâche MMCSS. Cette méthode est essentiellement un wrapper fin autour de [**MFBeginRegisterWorkQueueWithMMCSS**](/windows/desktop/api/mfapi/nf-mfapi-mfbeginregisterworkqueuewithmmcss), mais vous pouvez passer la valeur MFASYNC de la **\_ \_ file d’attente de rappel \_ All** pour inscrire toutes les files d’attente de travail de la plateforme à la fois. |
| [**BeginRegisterTopologyWorkQueuesWithMMCSS**](/windows/desktop/api/mfidl/nf-mfidl-imfworkqueueservices-beginregistertopologyworkqueueswithmmcss) | Inscrit une branche de la topologie avec une file d’attente de travail.                                                                                                                                                                                                                                         |



 

Pour inscrire une branche de topologie, procédez comme suit.

1.  Définissez l’attribut [MF \_ TOPONODE \_ WORKQUEUE \_ ID](mf-toponode-workqueue-id-attribute.md) sur le nœud source de la branche. Utilisez n’importe quelle valeur définie par l’application.
2.  Si vous le souhaitez, définissez la **\_ classe MF TOPONODE \_ WORKQUEUE \_ MMCSS \_** pour joindre la file d’attente de travail à une tâche mmcss.
3.  Appelez [**BeginRegisterTopologyWorkQueuesWithMMCSS**](/windows/desktop/api/mfidl/nf-mfidl-imfworkqueueservices-beginregistertopologyworkqueueswithmmcss) sur la topologie résolue.

La session multimédia alloue une nouvelle file d’attente de travail pour chaque valeur unique de l' [ \_ \_ \_ ID MF TOPONODE WORKQUEUE](mf-toponode-workqueue-id-attribute.md). Pour chaque branche de topologie, les opérations de pipeline asynchrones sont effectuées sur la file d’attente de travail qui est assignée à la branche.

### <a name="imfrealtimeclient"></a>IMFRealTimeClient

L’interface [**IMFRealTimeClient**](/windows/desktop/api/mfidl/nn-mfidl-imfrealtimeclient) est destinée aux composants de pipeline qui créent leurs propres threads ou utilisent des files d’attente de travail pour les opérations asynchrones. La session multimédia utilise cette interface pour notifier le composant de pipeline du comportement correct, comme suit :

-   Si le composant de pipeline crée un thread de travail, la méthode [**IMFRealTimeClient :: RegisterThreads**](/windows/desktop/api/mfidl/nf-mfidl-imfrealtimeclient-registerthreads) avertit le composant de la classe MMCSS à joindre.
-   Si le composant de pipeline utilise une file d’attente de travail, la méthode [**IMFRealTimeClient :: SetWorkQueue**](/windows/desktop/api/mfidl/nf-mfidl-imfrealtimeclient-setworkqueue) indique au composant la file d’attente de travail à utiliser.

En règle générale, un composant de pipeline utilise un thread ou une file d’attente de travail pour effectuer des tâches asynchrones, mais pas les deux.

## <a name="windows-8-improvements"></a>Windows 8 Optimisation

### <a name="multithreaded-work-queues"></a>Files d’attente de travail multithread

dans Windows 8, Media Foundation prend en charge un nouveau type de file d’attente de travail appelé *file d’attente multithread*. Une file d’attente multithread utilise un pool de threads système pour distribuer des éléments de travail. La file d’attente multithread est mieux adaptée que les files d’attente monothread précédentes. Par exemple,

-   Plusieurs composants peuvent partager une file d’attente multithread sans se bloquer l’un l’autre, ce qui nécessite la création de moins de threads.

-   Les éléments de travail sont optimisés pour éviter les changements de contexte si un événement est déjà défini. Cela est plus efficace que la création de vos propres threads pour attendre les événements.

Quand vous utilisez [**IMFRealTimeClientEx**](/windows/desktop/api/mfidl/nn-mfidl-imfrealtimeclientex), les applications doivent éviter de tourner les threads et doivent utiliser les files d’attente de travail. Pour ce faire, les applications doivent implémenter [**SetWorkQueueEx**](/windows/desktop/api/mfidl/nf-mfidl-imfrealtimeclientex-setworkqueueex) et ne pas utiliser [**RegisterThreads**](/windows/desktop/api/mfidl/nf-mfidl-imfrealtimeclientex-registerthreadsex) et [**UnregisterThreads**](/windows/desktop/api/mfidl/nf-mfidl-imfrealtimeclientex-unregisterthreads).

Lorsque la plateforme Media Foundation est initialisée, elle crée une file d’attente multithread avec l’identificateur **MFASYNC de \_ la \_ file \_ d’attente de rappel multithread**.

Une file d’attente multithread ne sérialise pas les éléments de travail. Chaque fois qu’un thread du pool de threads devient disponible, l’élément de travail suivant de la file d’attente est distribué. L’appelant doit s’assurer que le travail est correctement sérialisé. Pour faciliter cette opération, Media Foundation définit une *file d’attente de travail en série*. Une file d’attente série encapsule une autre file d’attente de travail, mais garantit une exécution entièrement sérialisée. L’élément suivant de la file d’attente n’est pas distribué tant que l’élément précédent n’est pas terminé.

Le code suivant crée une file d’attente de sérialiseur sur la file d’attente multithread de la plateforme.


```C++
DWORD workQueueID;
hr = MFAllocateSerialWorkQueue(MFASYNC_CALLBACK_QUEUE_MULTITHREADED, &workQueueID); 
```



Plusieurs files d’attente série peuvent encapsuler la même file d’attente multithread. Les files d’attente série partagent ensuite le même pool de threads, et l’exécution sérialisée est appliquée dans chaque file d’attente.

les files d’attente de travail standard qui existaient avant Windows 8 sont désormais implémentées en tant que files d’attente de travail en série qui encapsulent la file d’attente multithread de la plateforme. Cette modification préserve la compatibilité descendante.

### <a name="shared-task-work-queues"></a>Files d’attente de travail des tâches partagées

Pour fonctionner correctement avec le planificateur de noyau, il doit y avoir une file d’attente de travail multithread pour chaque tâche MMCSS que vous utilisez. La plate-forme Media Foundation les alloue en fonction des besoins, jusqu’à un par tâche MMCSS, par processus. Pour obtenir la file d’attente de travail partagée pour une tâche MMCSS particulière, appelez [**MFLockSharedWorkQueue**](/windows/desktop/api/mfapi/nf-mfapi-mflocksharedworkqueue) et spécifiez le nom de la tâche. La fonction recherche le nom de la tâche dans une table. Si une file d’attente de travail n’existe pas déjà pour cette tâche, la fonction alloue une nouvelle file d’attente de travail MT et la joint immédiatement à la tâche MMCSS. Si une file d’attente de travail existe déjà pour cette tâche, la fonction retourne l’identificateur de la file d’attente de travail existante.

### <a name="wait-queue"></a>File d’attente

La *file d'* attente est une file d’attente de travail de plateforme spéciale qui attend les événements à signaler. Si un composant doit attendre qu’un événement soit signalé, il peut utiliser la file d’attente au lieu de créer un thread de travail pour attendre l’événement.

Pour utiliser la file d’attente, appelez [**MFPutWaitingWorkItem**](/windows/desktop/api/mfapi/nf-mfapi-mfputwaitingworkitem). Les paramètres incluent le descripteur d’événement et un pointeur [**IMFAsyncResult**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasyncresult) . Lorsque l’événement est signalé, la file d’attente d’attente appelle votre rappel. Il existe une seule file d’attente de la plateforme. les applications ne peuvent pas créer leurs propres files d’attente d’attente.

### <a name="enhancements-to-mmcss-support"></a>Améliorations apportées à la prise en charge de MMCSS

Les nouvelles fonctions de plateforme de Media Foundation suivantes sont liées à MMCSS.



| Fonction                                                                           | Description                                                                                                                                                                                                                                                                                                                                                                                           |
|------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**MFBeginRegisterWorkQueueWithMMCSSEx**](/windows/desktop/api/mfapi/nf-mfapi-mfbeginregisterworkqueuewithmmcssex) | Inscrit une file d’attente de travail avec MMCSS. Cette fonction comprend un paramètre permettant de spécifier la priorité relative des threads. En interne, cette valeur est convertie en un appel à [**AvSetMmThreadPriority**](/windows/win32/api/avrt/nf-avrt-avsetmmthreadpriority).                                                                                                                                                                               |
| [**MFGetWorkQueueMMCSSPriority**](/windows/desktop/api/mfapi/nf-mfapi-mfgetworkqueuemmcsspriority)                 | Interroge la priorité d’une file d’attente de travail.                                                                                                                                                                                                                                                                                                                                                                 |
| [**MFRegisterPlatformWithMMCSS**](/windows/desktop/api/mfapi/nf-mfapi-mfregisterplatformwithmmcss)                 | Inscrit toutes les files d’attente de travail de plateforme avec une tâche MMCSS. Cette fonction est similaire à la méthode [**IMFWorkQueueServices :: BeginRegisterPlatformWorkQueueWithMMCSS**](/windows/desktop/api/mfidl/nf-mfidl-imfworkqueueservices-beginregisterplatformworkqueuewithmmcss) , mais elle peut être utilisée sans créer d’instance de la session multimédia. En outre, la fonction comprend un paramètre pour spécifier la priorité de thread de base. |



 

Les applications qui utilisent la session multimédia doivent définir l’attribut de [ \_ classe MF TOPONODE \_ WORKQUEUE \_ MMCSS \_ ](mf-toponode-workqueue-mmcss-class-attribute.md) sur « audio » pour la branche de rendu audio. Affectez à l’attribut la valeur « playback » pour la branche de rendu vidéo.

### <a name="imfrealtimeclientex"></a>IMFRealTimeClientEx

L’interface [**IMFRealTimeClientEx**](/windows/desktop/api/mfidl/nn-mfidl-imfrealtimeclientex) pour remplacer IMFRealTimeClient, pour les composants de pipeline qui effectuent des opérations asynchrones.



| Méthode                                                             | Description                                                                                                                                                                                                                    |
|--------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**RegisterThreadsEx**](/windows/desktop/api/mfidl/nf-mfidl-imfrealtimeclientex-registerthreadsex) | Notifie le composant d’inscrire ses threads avec MMCSS. Cette méthode est équivalente à [**IMFRealTimeClient :: RegisterThreads**](/windows/desktop/api/mfidl/nf-mfidl-imfrealtimeclient-registerthreads), mais elle ajoute un paramètre pour la priorité de thread de base. |
| [**SetWorkQueueEx**](/windows/desktop/api/mfidl/nf-mfidl-imfrealtimeclientex-setworkqueueex)       | Notifie le composant d’utiliser une file d’attente de travail spécifique. Cette méthode est équivalente à [**IMFReadTimeClient :: SetWorkQueue**](/windows/desktop/api/mfidl/nf-mfidl-imfrealtimeclient-setworkqueue), mais elle ajoute un paramètre pour la priorité de l’élément de travail.               |
| [**UnregisterThreads**](/windows/desktop/api/mfidl/nf-mfidl-imfrealtimeclientex-unregisterthreads) | Indique au composant d’annuler l’inscription de ses threads dans MMCSS. Cette méthode est identique à la méthode [**IMFRealTimeClient :: UnregisterThreads**](/windows/desktop/api/mfidl/nf-mfidl-imfrealtimeclient-unregisterthreads) .                                       |



 

Les composants de pipeline doivent utiliser des files d’attente de travail et ne doivent pas créer de threads de travail, pour les raisons suivantes :

-   Les files d’attente de travail évoluent mieux, car elles utilisent les pools de threads du système d’exploitation.
-   La plateforme gère les détails de l’inscription des files d’attente de travail avec MMCSS.
-   Un thread de travail peut facilement provoquer un blocage difficile à déboguer.

En outre, envisagez d’utiliser la file d’attente de travail du sérialiseur si vous devez sérialiser vos opérations asynchrones.

### <a name="topology-branches"></a>Branches de topologie

si l’attribut de [ \_ classe TOPONODE MF \_ WORKQUEUE \_ mmcss \_ ](mf-toponode-workqueue-mmcss-class-attribute.md) inscrit une branche de topologie avec MMCSS, dans Windows 8 la Session multimédia utilise les files d’attente de travail MT partagées. dans les versions antérieures de Windows, la Session multimédia a alloué une nouvelle file d’attente de travail.

Deux nouveaux attributs sont définis pour inscrire une branche de topologie avec MMCSS.



| Attribut                                                                            | Description                         |
|--------------------------------------------------------------------------------------|-------------------------------------|
| [MF \_ TOPONODE \_ WORKQUEUE \_ MMCSS \_ Priority](mf-toponode-workqueue-mmcss-priority.md) | Spécifie la priorité de thread de base. |
| [\_priorité de \_ l' \_ élément WORKQUEUE TOPONODE \_ MF](mf-toponode-workqueue-item-priority.md)   | Spécifie la priorité de l’élément de travail.   |



 

## <a name="recommendations"></a>Recommandations

-   Les applications qui utilisent la session multimédia doivent définir la [ \_ classe MF TOPONODE \_ WORKQUEUE \_ MMCSS \_ ](mf-toponode-workqueue-mmcss-class-attribute.md) sur « audio » pour la branche de rendu audio et la « lecture » pour la branche de rendu vidéo.
-   Les applications qui utilisent la session multimédia doivent appeler [**IMFWorkQueueServices :: BeginRegisterTopologyWorkQueuesWithMMCSS**](/windows/desktop/api/mfidl/nf-mfidl-imfworkqueueservices-beginregistertopologyworkqueueswithmmcss) sur la topologie.
-   Pour les composants de pipeline, les files d’attente de travail sont recommandées plutôt que les threads de travail. Si le composant utilise des files d’attente de travail ou des threads de travail, implémentez [**IMFRealTimeClientEx**](/windows/desktop/api/mfidl/nn-mfidl-imfrealtimeclientex).
-   Ne créez pas de files d’attente de travail privées, car cela a pour effet de détourner l’objectif des files d’attente de travail de la plateforme. Utilisez la file d’attente multithread de la plateforme ou une file d’attente série qui encapsule la file d’attente multithread de la plateforme.
-   Si vous devez sérialiser des opérations asynchrones, utilisez une file d’attente série.

## <a name="summary"></a>Résumé

Les API de plateforme de Media Foundation suivantes qui sont liées aux threads et aux files d’attente de travail sont nouvelles pour les Windows 8.

-   [\_priorité de \_ l' \_ élément WORKQUEUE TOPONODE \_ MF](mf-toponode-workqueue-item-priority.md)
-   [MF \_ TOPONODE \_ WORKQUEUE \_ MMCSS \_ Priority](mf-toponode-workqueue-mmcss-priority.md)
-   [**MFAllocateSerialWorkQueue**](/windows/desktop/api/mfapi/nf-mfapi-mfallocateserialworkqueue)
-   [**MFBeginRegisterWorkQueueWithMMCSSEx**](/windows/desktop/api/mfapi/nf-mfapi-mfbeginregisterworkqueuewithmmcssex)
-   [**MFGetWorkQueueMMCSSPriority**](/windows/desktop/api/mfapi/nf-mfapi-mfgetworkqueuemmcsspriority)
-   [**MFPutWaitingWorkItem**](/windows/desktop/api/mfapi/nf-mfapi-mfputwaitingworkitem)
-   [**MFPutWorkItem2**](/windows/desktop/api/mfapi/nf-mfapi-mfputworkitem2)
-   [**MFPutWorkItemEx2**](/windows/desktop/api/mfapi/nf-mfapi-mfputworkitemex2)
-   [**MFRegisterPlatformWithMMCSS**](/windows/desktop/api/mfapi/nf-mfapi-mfregisterplatformwithmmcss)
-   [**MFUnregisterPlatformFromMMCSS**](/windows/desktop/api/mfapi/nf-mfapi-mfunregisterplatformfrommmcss)
-   [**MFLockSharedWorkQueue**](/windows/desktop/api/mfapi/nf-mfapi-mflocksharedworkqueue)
-   [**IMFRealTimeClientEx**](/windows/desktop/api/mfidl/nn-mfidl-imfrealtimeclientex)

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Files d’attente de travail](work-queues.md)
</dt> </dl>

 

 
