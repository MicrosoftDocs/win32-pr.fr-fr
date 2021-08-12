---
description: La classe CAMThread est une classe abstraite pour la gestion des threads de travail.
ms.assetid: c217d879-0203-4566-96ad-7463b05bc990
title: CAMThread, classe (Wxutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAMThread
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ca7182ecc16cd873732b2d39d2659f42017f9e01c1308642af4b8cac7ff2a682
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118662112"
---
# <a name="camthread-class"></a>CAMThread, classe

La `CAMThread` classe est une classe abstraite pour la gestion des threads de travail.



| Variables membres protégées                                 | Description                                                                  |
|------------------------------------------------------------|------------------------------------------------------------------------------|
| [**m \_ hThread**](camthread-m-hthread.md)                  | Handle du thread.                                                        |
| Variables membres publiques                                    | Description                                                                  |
| [**m \_ AccessLock**](camthread-m-accesslock.md)            | Section critique qui empêche l’accès du thread par d’autres threads. |
| [**m \_ WorkerLock**](camthread-m-workerlock.md)            | Section critique qui verrouille les données partagées entre les threads.                       |
| M&#233;thodes publiques                                             | Description                                                                  |
| [**CAMThread**](camthread-camthread.md)                   | Méthode de constructeur.                                                          |
| [**~ CAMThread**](camthread--camthread.md)                | Méthode de destructeur. Virtuels.                                                  |
| [**InitialThreadProc**](camthread-initialthreadproc.md)   | Appelle la méthode ThreadProc lorsque le thread est créé.                      |
| [**Créer**](camthread-create.md)                         | Crée le thread.                                                          |
| [**CallWorker**](camthread-callworker.md)                 | Signale le thread à une demande.                                           |
| [**Plus**](camthread-close.md)                           | Attend que le thread se termine, puis libère ses ressources.                   |
| [**ThreadExists**](camthread-threadexists.md)             | Interroge si le thread existe.                                           |
| [**GetRequest**](camthread-getrequest.md)                 | Attend la requête suivante.                                                  |
| [**CheckRequest**](camthread-checkrequest.md)             | Vérifie s’il existe une demande, sans blocage.                              |
| [**Réponse**](camthread-reply.md)                           | Répond à une demande.                                                        |
| [**GetRequestHandle**](camthread-getrequesthandle.md)     | Récupère un handle vers l’événement signalé par la méthode CallWorker.           |
| [**GetRequestParam**](camthread-getrequestparam.md)       | Récupère la dernière requête.                                                |
| [**CoInitializeHelper**](camthread-coinitializehelper.md) | Appelle CoInitializeEx au début du thread.                             |
| Méthodes virtuelles pures                                       | Description                                                                  |
| [**ThreadProc**](camthread-threadproc.md)                 | Procédure de thread.                                                            |



 

## <a name="remarks"></a>Remarques

Cette classe fournit des méthodes pour la création d’un thread de travail, le passage de demandes au thread et l’attente de la fermeture du thread. Pour utiliser cette classe, procédez comme suit :

-   Dérivez une classe de `CAMThread` et substituez la méthode virtuelle pure [**CAMThread :: ThreadProc**](camthread-threadproc.md). Cette méthode est la procédure de thread qui est appelée au début du thread.
-   Dans votre application, créez une instance de votre classe dérivée. La création de l’objet ne crée pas le thread. Pour créer le thread, appelez la méthode [**CAMThread :: Create**](camthread-create.md) .
-   Pour envoyer des demandes au thread, appelez la méthode [**CAMThread :: CallWorker**](camthread-callworker.md) . Cette méthode prend un paramètre DWORD, dont la signification est définie par votre classe. La méthode se bloque jusqu’à ce que le thread réponde (voir ci-dessous).
-   Dans votre procédure de thread, répondez aux demandes en appelant [**CAMThread :: GetRequest**](camthread-getrequest.md) ou [**CAMThread :: CheckRequest**](camthread-checkrequest.md). La méthode GetRequest se bloque jusqu’à ce qu’un autre thread appelle CallWorker. La méthode CheckRequest est non bloquant, ce qui permet au thread de vérifier les nouvelles demandes en travaillant de manière asynchrone.
-   Lorsque le thread reçoit une demande, appelez [**CAMThread :: reply**](camthread-reply.md) pour débloquer le thread appelant. La méthode reply prend un paramètre DWORD, qui est passé au thread appelant comme valeur de retour pour CallWorker.

Lorsque vous avez terminé avec le thread, appelez la méthode [**CAMThread :: Close**](camthread-close.md) . Cette méthode attend que le thread se termine, puis ferme le handle de thread. La sortie de votre message ThreadProc doit être garantie, soit en soi, soit en réponse à une demande CallWorker. La méthode de destructeur appelle également Close.

L’exemple suivant illustre ces étapes :


```C++
class MyThread : public CAMThread
{
protected:
    DWORD ThreadProc(void);
};

DWORD MyThread::ThreadProc()
{
    BOOL bShutDown = FALSE;
    while (!bShutDown)
    {
        DWORD req = GetRequest();
        printf("Request: %d\n", req);
        bShutDown = (req == 0);
        Reply(bShutDown ? S_FALSE : S_OK);
    }
    printf("Quitting Thread\n");
    return 1;
}

void main()
{
    MyThread thread;
    DWORD reply;
    
    thread.Create();
    reply = thread.CallWorker(3);
    reply = thread.CallWorker(0); // Thread exits.
}
```



Dans votre classe dérivée, vous pouvez également définir des fonctions membres qui valident les paramètres de CallWorker. L’exemple suivant montre une méthode classique pour effectuer cette opération :


```C++
enum Command {CMD_INIT, CMD_RUN, CMD_STOP, CMD_EXIT};

HRESULT Init(void)  { return CallWorker(CMD_INIT); }
HRESULT Run(void)   { return CallWorker(CMD_RUN); }
HRESULT Stop(void)  { return CallWorker(CMD_STOP); }
HRESULT Exit(void)  { return CallWorker(CMD_EXIT); }
```



La `CAMThread` classe fournit deux sections critiques en tant que variables de membre public. Utilisez `CAMThread::m_AccessLock` pour verrouiller l’accès du thread par d’autres threads. (Par exemple, les méthodes Create et CallWorker contiennent ce verrou, pour sérialiser des opérations sur le thread.) Utilisez [**CAMThread :: m \_ WorkerLock**](camthread-m-workerlock.md) pour verrouiller les données partagées entre les threads.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Wxutil. h (inclure Flux. h)</dt> </dl>                                                                                    |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



 

 




