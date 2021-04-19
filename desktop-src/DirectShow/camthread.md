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
ms.openlocfilehash: e5c2bde058267ae4c530f33a96778792d5fe247b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106525220"
---
# <a name="camthread-class"></a><span data-ttu-id="310ab-103">CAMThread, classe</span><span class="sxs-lookup"><span data-stu-id="310ab-103">CAMThread class</span></span>

<span data-ttu-id="310ab-104">La `CAMThread` classe est une classe abstraite pour la gestion des threads de travail.</span><span class="sxs-lookup"><span data-stu-id="310ab-104">The `CAMThread` class is an abstract class for managing worker threads.</span></span>



| <span data-ttu-id="310ab-105">Variables membres protégées</span><span class="sxs-lookup"><span data-stu-id="310ab-105">Protected Member Variables</span></span>                                 | <span data-ttu-id="310ab-106">Description</span><span class="sxs-lookup"><span data-stu-id="310ab-106">Description</span></span>                                                                  |
|------------------------------------------------------------|------------------------------------------------------------------------------|
| [<span data-ttu-id="310ab-107">**m \_ hThread**</span><span class="sxs-lookup"><span data-stu-id="310ab-107">**m\_hThread**</span></span>](camthread-m-hthread.md)                  | <span data-ttu-id="310ab-108">Handle du thread.</span><span class="sxs-lookup"><span data-stu-id="310ab-108">Handle to the thread.</span></span>                                                        |
| <span data-ttu-id="310ab-109">Variables membres publiques</span><span class="sxs-lookup"><span data-stu-id="310ab-109">Public Member Variables</span></span>                                    | <span data-ttu-id="310ab-110">Description</span><span class="sxs-lookup"><span data-stu-id="310ab-110">Description</span></span>                                                                  |
| [<span data-ttu-id="310ab-111">**m \_ AccessLock**</span><span class="sxs-lookup"><span data-stu-id="310ab-111">**m\_AccessLock**</span></span>](camthread-m-accesslock.md)            | <span data-ttu-id="310ab-112">Section critique qui empêche l’accès du thread par d’autres threads.</span><span class="sxs-lookup"><span data-stu-id="310ab-112">Critical section that locks the thread from being accessed by other threads.</span></span> |
| [<span data-ttu-id="310ab-113">**m \_ WorkerLock**</span><span class="sxs-lookup"><span data-stu-id="310ab-113">**m\_WorkerLock**</span></span>](camthread-m-workerlock.md)            | <span data-ttu-id="310ab-114">Section critique qui verrouille les données partagées entre les threads.</span><span class="sxs-lookup"><span data-stu-id="310ab-114">Critical section that locks data shared among threads.</span></span>                       |
| <span data-ttu-id="310ab-115">M&#233;thodes publiques</span><span class="sxs-lookup"><span data-stu-id="310ab-115">Public Methods</span></span>                                             | <span data-ttu-id="310ab-116">Description</span><span class="sxs-lookup"><span data-stu-id="310ab-116">Description</span></span>                                                                  |
| [<span data-ttu-id="310ab-117">**CAMThread**</span><span class="sxs-lookup"><span data-stu-id="310ab-117">**CAMThread**</span></span>](camthread-camthread.md)                   | <span data-ttu-id="310ab-118">Méthode de constructeur.</span><span class="sxs-lookup"><span data-stu-id="310ab-118">Constructor method.</span></span>                                                          |
| [<span data-ttu-id="310ab-119">**~ CAMThread**</span><span class="sxs-lookup"><span data-stu-id="310ab-119">**~ CAMThread**</span></span>](camthread--camthread.md)                | <span data-ttu-id="310ab-120">Méthode de destructeur.</span><span class="sxs-lookup"><span data-stu-id="310ab-120">Destructor method.</span></span> <span data-ttu-id="310ab-121">Virtuels.</span><span class="sxs-lookup"><span data-stu-id="310ab-121">Virtual.</span></span>                                                  |
| [<span data-ttu-id="310ab-122">**InitialThreadProc**</span><span class="sxs-lookup"><span data-stu-id="310ab-122">**InitialThreadProc**</span></span>](camthread-initialthreadproc.md)   | <span data-ttu-id="310ab-123">Appelle la méthode ThreadProc lorsque le thread est créé.</span><span class="sxs-lookup"><span data-stu-id="310ab-123">Calls the ThreadProc method when the thread is created.</span></span>                      |
| [<span data-ttu-id="310ab-124">**Créés**</span><span class="sxs-lookup"><span data-stu-id="310ab-124">**Create**</span></span>](camthread-create.md)                         | <span data-ttu-id="310ab-125">Crée le thread.</span><span class="sxs-lookup"><span data-stu-id="310ab-125">Creates the thread.</span></span>                                                          |
| [<span data-ttu-id="310ab-126">**CallWorker**</span><span class="sxs-lookup"><span data-stu-id="310ab-126">**CallWorker**</span></span>](camthread-callworker.md)                 | <span data-ttu-id="310ab-127">Signale le thread à une demande.</span><span class="sxs-lookup"><span data-stu-id="310ab-127">Signals the thread with a request.</span></span>                                           |
| [<span data-ttu-id="310ab-128">**Fermer**</span><span class="sxs-lookup"><span data-stu-id="310ab-128">**Close**</span></span>](camthread-close.md)                           | <span data-ttu-id="310ab-129">Attend que le thread se termine, puis libère ses ressources.</span><span class="sxs-lookup"><span data-stu-id="310ab-129">Waits for the thread to exit, then releases its resources.</span></span>                   |
| [<span data-ttu-id="310ab-130">**ThreadExists**</span><span class="sxs-lookup"><span data-stu-id="310ab-130">**ThreadExists**</span></span>](camthread-threadexists.md)             | <span data-ttu-id="310ab-131">Interroge si le thread existe.</span><span class="sxs-lookup"><span data-stu-id="310ab-131">Queries whether the thread exists.</span></span>                                           |
| [<span data-ttu-id="310ab-132">**GetRequest**</span><span class="sxs-lookup"><span data-stu-id="310ab-132">**GetRequest**</span></span>](camthread-getrequest.md)                 | <span data-ttu-id="310ab-133">Attend la requête suivante.</span><span class="sxs-lookup"><span data-stu-id="310ab-133">Waits for the next request.</span></span>                                                  |
| [<span data-ttu-id="310ab-134">**CheckRequest**</span><span class="sxs-lookup"><span data-stu-id="310ab-134">**CheckRequest**</span></span>](camthread-checkrequest.md)             | <span data-ttu-id="310ab-135">Vérifie s’il existe une demande, sans blocage.</span><span class="sxs-lookup"><span data-stu-id="310ab-135">Checks if there is a request, without blocking.</span></span>                              |
| [<span data-ttu-id="310ab-136">**Réponse**</span><span class="sxs-lookup"><span data-stu-id="310ab-136">**Reply**</span></span>](camthread-reply.md)                           | <span data-ttu-id="310ab-137">Répond à une demande.</span><span class="sxs-lookup"><span data-stu-id="310ab-137">Replies to a request.</span></span>                                                        |
| [<span data-ttu-id="310ab-138">**GetRequestHandle**</span><span class="sxs-lookup"><span data-stu-id="310ab-138">**GetRequestHandle**</span></span>](camthread-getrequesthandle.md)     | <span data-ttu-id="310ab-139">Récupère un handle vers l’événement signalé par la méthode CallWorker.</span><span class="sxs-lookup"><span data-stu-id="310ab-139">Retrieves a handle to the event signaled by the CallWorker method.</span></span>           |
| [<span data-ttu-id="310ab-140">**GetRequestParam**</span><span class="sxs-lookup"><span data-stu-id="310ab-140">**GetRequestParam**</span></span>](camthread-getrequestparam.md)       | <span data-ttu-id="310ab-141">Récupère la dernière requête.</span><span class="sxs-lookup"><span data-stu-id="310ab-141">Retrieves the latest request.</span></span>                                                |
| [<span data-ttu-id="310ab-142">**CoInitializeHelper**</span><span class="sxs-lookup"><span data-stu-id="310ab-142">**CoInitializeHelper**</span></span>](camthread-coinitializehelper.md) | <span data-ttu-id="310ab-143">Appelle CoInitializeEx au début du thread.</span><span class="sxs-lookup"><span data-stu-id="310ab-143">Calls CoInitializeEx at the start of the thread.</span></span>                             |
| <span data-ttu-id="310ab-144">Méthodes virtuelles pures</span><span class="sxs-lookup"><span data-stu-id="310ab-144">Pure Virtual Methods</span></span>                                       | <span data-ttu-id="310ab-145">Description</span><span class="sxs-lookup"><span data-stu-id="310ab-145">Description</span></span>                                                                  |
| [<span data-ttu-id="310ab-146">**ThreadProc**</span><span class="sxs-lookup"><span data-stu-id="310ab-146">**ThreadProc**</span></span>](camthread-threadproc.md)                 | <span data-ttu-id="310ab-147">Procédure de thread.</span><span class="sxs-lookup"><span data-stu-id="310ab-147">Thread procedure.</span></span>                                                            |



 

## <a name="remarks"></a><span data-ttu-id="310ab-148">Notes</span><span class="sxs-lookup"><span data-stu-id="310ab-148">Remarks</span></span>

<span data-ttu-id="310ab-149">Cette classe fournit des méthodes pour la création d’un thread de travail, le passage de demandes au thread et l’attente de la fermeture du thread.</span><span class="sxs-lookup"><span data-stu-id="310ab-149">This class provides methods for creating a worker thread, passing requests to the thread, and waiting for the thread to exit.</span></span> <span data-ttu-id="310ab-150">Pour utiliser cette classe, procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="310ab-150">To use this class, do the following:</span></span>

-   <span data-ttu-id="310ab-151">Dérivez une classe de `CAMThread` et substituez la méthode virtuelle pure [**CAMThread :: ThreadProc**](camthread-threadproc.md).</span><span class="sxs-lookup"><span data-stu-id="310ab-151">Derive a class from `CAMThread` and override the pure virtual method [**CAMThread::ThreadProc**](camthread-threadproc.md).</span></span> <span data-ttu-id="310ab-152">Cette méthode est la procédure de thread qui est appelée au début du thread.</span><span class="sxs-lookup"><span data-stu-id="310ab-152">This method is the thread procedure that gets called at the start of the thread.</span></span>
-   <span data-ttu-id="310ab-153">Dans votre application, créez une instance de votre classe dérivée.</span><span class="sxs-lookup"><span data-stu-id="310ab-153">In your application, create an instance of your derived class.</span></span> <span data-ttu-id="310ab-154">La création de l’objet ne crée pas le thread.</span><span class="sxs-lookup"><span data-stu-id="310ab-154">Creating the object does not create the thread.</span></span> <span data-ttu-id="310ab-155">Pour créer le thread, appelez la méthode [**CAMThread :: Create**](camthread-create.md) .</span><span class="sxs-lookup"><span data-stu-id="310ab-155">To create the thread, call the [**CAMThread::Create**](camthread-create.md) method.</span></span>
-   <span data-ttu-id="310ab-156">Pour envoyer des demandes au thread, appelez la méthode [**CAMThread :: CallWorker**](camthread-callworker.md) .</span><span class="sxs-lookup"><span data-stu-id="310ab-156">To send requests to the thread, call the [**CAMThread::CallWorker**](camthread-callworker.md) method.</span></span> <span data-ttu-id="310ab-157">Cette méthode prend un paramètre DWORD, dont la signification est définie par votre classe.</span><span class="sxs-lookup"><span data-stu-id="310ab-157">This method takes a DWORD parameter, whose meaning is defined by your class.</span></span> <span data-ttu-id="310ab-158">La méthode se bloque jusqu’à ce que le thread réponde (voir ci-dessous).</span><span class="sxs-lookup"><span data-stu-id="310ab-158">The method blocks until the thread responds (see below).</span></span>
-   <span data-ttu-id="310ab-159">Dans votre procédure de thread, répondez aux demandes en appelant [**CAMThread :: GetRequest**](camthread-getrequest.md) ou [**CAMThread :: CheckRequest**](camthread-checkrequest.md).</span><span class="sxs-lookup"><span data-stu-id="310ab-159">In your thread procedure, respond to requests by calling either [**CAMThread::GetRequest**](camthread-getrequest.md) or [**CAMThread::CheckRequest**](camthread-checkrequest.md).</span></span> <span data-ttu-id="310ab-160">La méthode GetRequest se bloque jusqu’à ce qu’un autre thread appelle CallWorker.</span><span class="sxs-lookup"><span data-stu-id="310ab-160">The GetRequest method blocks until another thread calls CallWorker.</span></span> <span data-ttu-id="310ab-161">La méthode CheckRequest est non bloquant, ce qui permet au thread de vérifier les nouvelles demandes en travaillant de manière asynchrone.</span><span class="sxs-lookup"><span data-stu-id="310ab-161">The CheckRequest method is non-blocking, which enables the thread to check for new requests while working asynchronously.</span></span>
-   <span data-ttu-id="310ab-162">Lorsque le thread reçoit une demande, appelez [**CAMThread :: reply**](camthread-reply.md) pour débloquer le thread appelant.</span><span class="sxs-lookup"><span data-stu-id="310ab-162">When the thread receives a request, call [**CAMThread::Reply**](camthread-reply.md) to unblock the calling thread.</span></span> <span data-ttu-id="310ab-163">La méthode reply prend un paramètre DWORD, qui est passé au thread appelant comme valeur de retour pour CallWorker.</span><span class="sxs-lookup"><span data-stu-id="310ab-163">The Reply method takes a DWORD parameter, which is passed to the calling thread as the return value for CallWorker.</span></span>

<span data-ttu-id="310ab-164">Lorsque vous avez terminé avec le thread, appelez la méthode [**CAMThread :: Close**](camthread-close.md) .</span><span class="sxs-lookup"><span data-stu-id="310ab-164">When you are done with the thread, call the [**CAMThread::Close**](camthread-close.md) method.</span></span> <span data-ttu-id="310ab-165">Cette méthode attend que le thread se termine, puis ferme le handle de thread.</span><span class="sxs-lookup"><span data-stu-id="310ab-165">This method waits for the thread to exit, and then closes the thread handle.</span></span> <span data-ttu-id="310ab-166">La sortie de votre message ThreadProc doit être garantie, soit en soi, soit en réponse à une demande CallWorker.</span><span class="sxs-lookup"><span data-stu-id="310ab-166">Your ThreadProc message must be guaranteed to exit, either on its own or in response to a CallWorker request.</span></span> <span data-ttu-id="310ab-167">La méthode de destructeur appelle également Close.</span><span class="sxs-lookup"><span data-stu-id="310ab-167">The destructor method also calls Close.</span></span>

<span data-ttu-id="310ab-168">L’exemple suivant illustre ces étapes :</span><span class="sxs-lookup"><span data-stu-id="310ab-168">The following example illustrates these steps:</span></span>


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



<span data-ttu-id="310ab-169">Dans votre classe dérivée, vous pouvez également définir des fonctions membres qui valident les paramètres de CallWorker.</span><span class="sxs-lookup"><span data-stu-id="310ab-169">In your derived class, you can also define member functions that validate the parameters to CallWorker.</span></span> <span data-ttu-id="310ab-170">L’exemple suivant montre une méthode classique pour effectuer cette opération :</span><span class="sxs-lookup"><span data-stu-id="310ab-170">The following example shows a typical way to do this:</span></span>


```C++
enum Command {CMD_INIT, CMD_RUN, CMD_STOP, CMD_EXIT};

HRESULT Init(void)  { return CallWorker(CMD_INIT); }
HRESULT Run(void)   { return CallWorker(CMD_RUN); }
HRESULT Stop(void)  { return CallWorker(CMD_STOP); }
HRESULT Exit(void)  { return CallWorker(CMD_EXIT); }
```



<span data-ttu-id="310ab-171">La `CAMThread` classe fournit deux sections critiques en tant que variables de membre public.</span><span class="sxs-lookup"><span data-stu-id="310ab-171">The `CAMThread` class provides two critical sections as public member variables.</span></span> <span data-ttu-id="310ab-172">Utilisez `CAMThread::m_AccessLock` pour verrouiller l’accès du thread par d’autres threads.</span><span class="sxs-lookup"><span data-stu-id="310ab-172">Use `CAMThread::m_AccessLock` to lock the thread from being accessed by other threads.</span></span> <span data-ttu-id="310ab-173">(Par exemple, les méthodes Create et CallWorker contiennent ce verrou, pour sérialiser des opérations sur le thread.) Utilisez [**CAMThread :: m \_ WorkerLock**](camthread-m-workerlock.md) pour verrouiller les données partagées entre les threads.</span><span class="sxs-lookup"><span data-stu-id="310ab-173">(For example, the Create and CallWorker methods hold this lock, to serialize operations on the thread.) Use [**CAMThread::m\_WorkerLock**](camthread-m-workerlock.md) to lock data that is shared among threads.</span></span>

## <a name="requirements"></a><span data-ttu-id="310ab-174">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="310ab-174">Requirements</span></span>



| <span data-ttu-id="310ab-175">Condition requise</span><span class="sxs-lookup"><span data-stu-id="310ab-175">Requirement</span></span> | <span data-ttu-id="310ab-176">Valeur</span><span class="sxs-lookup"><span data-stu-id="310ab-176">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="310ab-177">En-tête</span><span class="sxs-lookup"><span data-stu-id="310ab-177">Header</span></span><br/>  | <dl> <span data-ttu-id="310ab-178"><dt>Wxutil. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="310ab-178"><dt>Wxutil.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="310ab-179">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="310ab-179">Library</span></span><br/> | <dl> <span data-ttu-id="310ab-180"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="310ab-180"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




