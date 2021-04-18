---
title: Achèvement du rappel asynchrone
description: Décrit comment le fournisseur peut les rappels de service asynchrones.
ms.assetid: <GUID-GOES-HERE>
ms.date: 10/12/2018
ms.topic: article
ms.openlocfilehash: 8ec23f5ea6e8ec55be2eaa2811d9dee8b1870edc
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "106512331"
---
# <a name="asynchronous-callback-handling"></a><span data-ttu-id="169ee-103">Gestion asynchrone des rappels</span><span class="sxs-lookup"><span data-stu-id="169ee-103">Asynchronous Callback Handling</span></span>

<span data-ttu-id="169ee-104">Lorsqu’un client interagit avec les fichiers et les répertoires situés sous la racine de virtualisation du fournisseur, ces interactions entraînent généralement l’appel des rappels du fournisseur.</span><span class="sxs-lookup"><span data-stu-id="169ee-104">When a client interacts with the files and directories beneath the provider's virtualization root, these interactions typically result in the provider's callbacks being invoked.</span></span>  <span data-ttu-id="169ee-105">ProjFS appelle les rappels de fournisseur en envoyant un message du mode noyau à la bibliothèque en mode utilisateur ProjFS, où un thread de travail reçoit le message et appelle le rappel approprié.</span><span class="sxs-lookup"><span data-stu-id="169ee-105">ProjFS invokes provider callbacks by sending a message from kernel mode to the ProjFS user-mode library, where a worker thread receives the message and calls the appropriate callback.</span></span>  <span data-ttu-id="169ee-106">Une fois le rappel retourné, le thread de travail attend l’arrivée d’un autre message en mode noyau.</span><span class="sxs-lookup"><span data-stu-id="169ee-106">Once the callback has returned, the worker thread waits for another message to arrive from kernel mode.</span></span>  <span data-ttu-id="169ee-107">Si tous les threads de travail sont occupés à exécuter le code de rappel du fournisseur, toute autre e/s cliente qui déclenche un bloc de rappel jusqu’à ce qu’un thread de travail soit disponible pour recevoir le message et appeler le rappel approprié.</span><span class="sxs-lookup"><span data-stu-id="169ee-107">If all the worker threads are busy executing provider callback code, any further client I/O that triggers a callback blocks until a worker thread becomes available to receive the message and invoke the relevant callback.</span></span>  <span data-ttu-id="169ee-108">Lorsqu’un fournisseur démarre, il peut spécifier le nombre de threads de travail qu’il souhaite que ProjFS crée pour les rappels de service via le paramètre _options_ de **[PrjStartVirtualizing](/windows/desktop/api/projectedfslib/nf-projectedfslib-prjstartvirtualizing)**.</span><span class="sxs-lookup"><span data-stu-id="169ee-108">When a provider starts up, it can specify the number of worker threads it wants ProjFS to create to service callbacks via the _options_ parameter of **[PrjStartVirtualizing](/windows/desktop/api/projectedfslib/nf-projectedfslib-prjstartvirtualizing)**.</span></span>  <span data-ttu-id="169ee-109">Un fournisseur peut améliorer l’efficacité des threads de travail recevant les messages en desservant les rappels de manière asynchrone.</span><span class="sxs-lookup"><span data-stu-id="169ee-109">A provider can improve the efficiency of the message-receiving worker threads by servicing its callbacks asynchronously.</span></span>

> <span data-ttu-id="169ee-110">Si le fournisseur ne spécifie pas le paramètre _options_ à **PrjStartVirtualizing**, ou s’il spécifie 0 pour le membre ConcurrentThreadCount du paramètre _options_ , ProjFS utilise le nombre de processeurs logiques dans le système pour la valeur de ConcurrentThreadCount.</span><span class="sxs-lookup"><span data-stu-id="169ee-110">If the provider does not specify the _options_ parameter to **PrjStartVirtualizing**, or if it specifies 0 for the ConcurrentThreadCount member of the _options_ parameter, ProjFS will use the number of logical processors in the system for the value of ConcurrentThreadCount.</span></span>
>
> <span data-ttu-id="169ee-111">Si le fournisseur ne spécifie pas le paramètre _options_ à **PrjStartVirtualizing**, ou s’il spécifie 0 pour le membre PoolThreadCount du paramètre _options_ , ProjFS utilise deux fois la valeur de ConcurrentThreadCount pour la valeur de PoolThreadCount.</span><span class="sxs-lookup"><span data-stu-id="169ee-111">If the provider does not specify the _options_ parameter to **PrjStartVirtualizing**, or if it specifies 0 for the PoolThreadCount member of the _options_ parameter, ProjFS will use twice the value of ConcurrentThreadCount for the value of PoolThreadCount.</span></span>

<span data-ttu-id="169ee-112">Un fournisseur de services effectue un rappel de façon asynchrone en retournant HRESULT_FROM_WIN32 (ERROR_IO_PENDING) à partir de ses rappels et en les terminant par la suite à l’aide de **[PrjCompleteCommand](/windows/desktop/api/projectedfslib/nf-projectedfslib-prjcompletecommand)**.</span><span class="sxs-lookup"><span data-stu-id="169ee-112">A provider services callbacks asynchronously by returning HRESULT_FROM_WIN32(ERROR_IO_PENDING) from its callbacks and later completing them using **[PrjCompleteCommand](/windows/desktop/api/projectedfslib/nf-projectedfslib-prjcompletecommand)**.</span></span>  <span data-ttu-id="169ee-113">Un fournisseur qui traite les rappels de manière asynchrone doit également prendre en charge l’annulation de rappel en implémentant le rappel **[PRJ_CANCEL_COMMAND_CB](/windows/desktop/api/projectedfslib/nc-projectedfslib-prj_cancel_command_cb)** .</span><span class="sxs-lookup"><span data-stu-id="169ee-113">A provider that processes callbacks asynchronously should also support callback cancellation by implementing the **[PRJ_CANCEL_COMMAND_CB](/windows/desktop/api/projectedfslib/nc-projectedfslib-prj_cancel_command_cb)** callback.</span></span>

<span data-ttu-id="169ee-114">Quand ProjFS appelle le rappel d’un fournisseur, il identifie l’appel spécifique du rappel à l’aide du membre CommandID du paramètre _callbackdata_ du rappel.</span><span class="sxs-lookup"><span data-stu-id="169ee-114">When ProjFS calls a provider's callback, it identifies the specific invocation of the callback using the CommandId member of the callback's _callbackData_ parameter.</span></span>  <span data-ttu-id="169ee-115">Si le fournisseur décide de traiter ce rappel de façon asynchrone, il doit stocker la valeur du membre CommandID et retourner HRESULT_FROM_WIN32 (ERROR_IO_PENDING) à partir du rappel.</span><span class="sxs-lookup"><span data-stu-id="169ee-115">If the provider decides to process that callback asynchronously, it must store the value of the CommandId member and return HRESULT_FROM_WIN32(ERROR_IO_PENDING) from the callback.</span></span>  <span data-ttu-id="169ee-116">Une fois que le fournisseur a terminé de traiter le rappel, il appelle **PrjCompleteCommand**, en transmettant l’identificateur stocké dans le paramètre _CommandID_ .</span><span class="sxs-lookup"><span data-stu-id="169ee-116">Once the provider has finished processing the callback, it calls **PrjCompleteCommand**, passing the stored identifier in the _commandId_ parameter.</span></span>  <span data-ttu-id="169ee-117">Cela indique à ProjFS l’appel de rappel effectué.</span><span class="sxs-lookup"><span data-stu-id="169ee-117">This tells ProjFS which callback invocation has been completed.</span></span>

<span data-ttu-id="169ee-118">Un fournisseur qui implémente le rappel **PRJ_CANCEL_COMMAND_CB** doit suivre les rappels qu’il n’a pas encore terminés.</span><span class="sxs-lookup"><span data-stu-id="169ee-118">A provider that implements the **PRJ_CANCEL_COMMAND_CB** callback must keep track of which callbacks it has not yet completed.</span></span>  <span data-ttu-id="169ee-119">Si le fournisseur reçoit ce rappel, il indique que les e/s qui ont provoqué l’appel de l’un de ces rappels ont été annulées, soit explicitement, soit parce que le thread sur lequel il a été émis s’est arrêté.</span><span class="sxs-lookup"><span data-stu-id="169ee-119">If the provider receives this callback, it indicates that the I/O that caused one of those callbacks to be invoked was canceled, either explicitly or because the thread it was issued on terminated.</span></span> <span data-ttu-id="169ee-120">Le fournisseur doit annuler le traitement de l’appel de rappel identifié par CommandID le plus rapidement possible.</span><span class="sxs-lookup"><span data-stu-id="169ee-120">The provider should cancel processing the callback invocation identified by CommandId as soon as possible.</span></span>

> <span data-ttu-id="169ee-121">Bien que ProjFS appelle **PRJ_CANCEL_COMMAND_CB** pour un objet CommandID donné uniquement une fois que le rappel à annuler est appelé, l’annulation et l’appel d’origine peuvent s’exécuter simultanément dans un fournisseur multithread.</span><span class="sxs-lookup"><span data-stu-id="169ee-121">Although ProjFS will invoke **PRJ_CANCEL_COMMAND_CB** for a given CommandId only after the callback to be canceled is invoked, the cancellation and original invocation may run concurrently in a multithreaded provider.</span></span>  <span data-ttu-id="169ee-122">Le fournisseur doit être en mesure de gérer cette situation de manière appropriée.</span><span class="sxs-lookup"><span data-stu-id="169ee-122">The provider must be able to gracefully handle this situation.</span></span>

<span data-ttu-id="169ee-123">L’exemple suivant est une version de l’exemple donné pour la rubrique [énumération de fichiers et de répertoires](enumerating-files-and-directories.md) , modifiée pour illustrer la gestion asynchrone des rappels.</span><span class="sxs-lookup"><span data-stu-id="169ee-123">The following sample is a version of the sample given for the [Enumerating Files and Directories](enumerating-files-and-directories.md) topic, modified to illustrate asynchronous callback handling.</span></span>

```C++
typedef struct MY_ENUM_ENTRY MY_ENUM_ENTRY;

typedef struct MY_ENUM_ENTRY {
    MY_ENUM_ENTRY* Next;
    PWSTR Name;
    BOOLEAN IsDirectory;
    INT64 FileSize;
} MY_ENUM_ENTRY;

typedef struct MY_ENUM_SESSION {
    GUID EnumerationId;
    PWSTR SearchExpression;
    USHORT SearchExpressionMaxLen;
    BOOLEAN SearchExpressionCaptured;
    MY_ENUM_ENTRY* EnumHead;
    MY_ENUM_ENTRY* LastEnumEntry;
    BOOLEAN EnumCompleted;
} MY_ENUM_SESSION;

typedef struct MY_ENUM_PARAMS {
    GUID EnumerationId;
    PRJ_DIR_ENTRY_BUFFER_HANDLE DirEntryBufferHandle;
    PRJ_NAMESPACE_VIRTUALIZATION_CONTEXT NamespaceVirtualizationContext;
    INT32 CommandId;
    PRJ_CALLBACK_DATA_FLAGS Flags;
    WCHAR SearchExpression[1];
} MY_ENUM_PARAMS;

// Prototype for the enumeration worker routine.  In this example this is a
// ThreadProc.  See https://msdn.microsoft.com/library/windows/desktop/ms686736.aspx
DWORD WINAPI MyGetEnumCallbackWorker(_In_ LPVOID parameter);

#define ROLLBACK_NONE           0
#define ROLLBACK_PARAM_ALLOC    1
#define ROLLBACK_TRACK_ENUM     2

HRESULT
MyGetEnumCallback(
    _In_ const PRJ_CALLBACK_DATA* callbackData,
    _In_ const GUID* enumerationId,
    _In_opt_z_ PCWSTR searchExpression,
    _In_ PRJ_DIR_ENTRY_BUFFER_HANDLE dirEntryBufferHandle
    )
{
    UINT rollback = ROLLBACK_NONE;

    // This example creates a thread to run the enumeration in.  The provider
    // can access callbackData only while the callback is running, so we copy
    // out the fields that the worker thread will need.
    MY_ENUM_PARAMS* enumParams = NULL;
    size_t bufSize = sizeof(MY_ENUM_PARAMS);

    // Allocate enough space for the parameter buffer and the search expression
    // string plus a terminating NULL character.
    if (searchExpression != NULL)
    {
        bufSize += (wcslen(searchExpression) + 1) * sizeof(WCHAR);
    }
    else
    {
        // We'll store "*" as the search expression in this case.
        bufSize += 2 * sizeof(WCHAR);
    }

    enumParams = (MY_ENUM_PARAMS*) calloc(1, bufSize);

    if (enumParams == NULL)
    {
        hr = E_OUTOFMEMORY;
        goto RollbackOnError;
    }

    // enumParams allocated.
    rollback = ROLLBACK_PARAM_ALLOC;

    // Copy the search expression into our parameter buffer.
    if (searchExpression != NULL)
    {
        wcsncpy_s(enumParams->SearchExpression,
                  wcslen(searchExpression),
                  searchExpression,
                  wcslen(searchExpression));
    }
    else
    {
        wcsncpy_s(enumParams->SearchExpression, 1, "*", 1);
    }

    // Copy the other parameters into our parameter buffer.
    enumParams->EnumerationId = enumerationId;
    enumParams->DirEntryBufferHandle = dirEntryBufferHandle;
    enumParams->NamespaceVirtualizationContext = callbackData->NamespaceVirtualizationContext
    enumParams->CommandId = callbackData->CommandId;
    enumParams->Flags = callbackData->Flags;

    // MyTrackEnumForCancellation is a routine the provider might implement to
    // track active enumeration callbacks in case they are cancelled.  It stores
    // the CommandId for the callback in some structure.
    hr = MyTrackEnumForCancellation(callbackData->CommandId);

    if (FAILED(hr))
    {
        goto RollbackOnError;
    }

    // Enum callback tracked.
    rollback = ROLLBACK_TRACK_ENUM;

    // Create the worker thread.
    HANDLE workerThread = NULL;
    workerThread = CreateThread(NULL,
                                0,
                                MyGetEnumCallbackWorker,
                                enumParams,
                                0
                                NULL);

    // We'll treat failure to create the thread as a low-resources error.
    if (workerThread == NULL)
    {
        hr = E_OUTOFMEMORY;
        goto RollbackOnError;
    }

    // Return pending to signal that we'll complete the enumeration later.
    return HRESULT_FROM_WIN32(ERROR_IO_PENDING);

RollbackOnError:

    // Clean up manually.  Note the fall-through structure of the switch, and that
    // we clean up in reverse order.
    switch(rollback)
    {
    case ROLLBACK_TRACK_ENUM:
        // MyUntrackEnumForCancellation removes the CommandId for the callback
        // from the structure that MyTrackEnumForCancellation put it in.
        MyUntrackEnumForCancellation(callbackData->CommandId);

    case ROLLBACK_PARAM_ALLOC:
        free(enumParams);

    default:
        break;
    }

    return hr;
}

DWORD
WINAPI
MyGetEnumCallbackWorker(
    _In_ LPVOID parameter
)
{
    HRESULT hr = S_OK;
    MY_ENUM_PARAMS* enumParams = (MY_ENUM_PARAMS*) parameter;

    // MyCheckEnumForCancellation is a routine the provider might implement to
    // check whether a pended enumeration callback has been cancelled.  Even
    // though the enumeration has been cancelled, ProjFS will still call the
    // provider's end-enumeration callback.  This allows general cleanup, such
    // as tearing down the enumeration session, to always happen in that callback.
    if (MyCheckEnumForCancellation(enumParams->CommandId))
    {
        // The operation has been cancelled.  Clean up and get out.
        free(enumParams);
        return 0;
    }

    // MyGetEnumSession is a routine the provider might implement to find
    // information about the enumeration session that it first stored
    // when processing its PRJ_START_DIRECTORY_ENUMERATION_CB callback.
    //
    // In this example the PRJ_START_DIRECTORY_ENUMERATION_CB callback has
    // already retrieved a list of the items in the backing store located at
    // callbackData->FilePathName, sorted them using PrjFileNameCompare()
    // to determine collation order, and stored the list in session->EnumHead.
    MY_ENUM_SESSION* session = NULL;
    session = MyGetEnumSession(enumParams->EnumerationId);

    if (session == NULL)
    {
        hr = HRESULT_FROM_WIN32(ERROR_INVALID_PARAMETER);
        goto CompleteCallback;
    }

    if (!session->SearchExpressionCaptured ||
        (enumParams->Flags & PRJ_CB_DATA_FLAG_ENUM_RESTART_SCAN))
    {
        if (wcsncpy_s(session->SearchExpression,
                      session->SearchExpressionMaxLen,
                      enumParams->SearchExpression,
                      wcslen(enumParams->SearchExpression)))
        {
            // Failed to copy the search expression; perhaps the provider
            // could try reallocating session->SearchExpression.
        }

        session->SearchExpressionCaptured = TRUE;
    }

    MY_ENUM_ENTRY* enumHead = NULL;

    // We have to start the enumeration from the beginning if we aren't
    // continuing an existing session or if the caller is requesting a restart.
    if (((session->LastEnumEntry == NULL) &&
         !session->EnumCompleted) ||
        (enumParams->Flags & PRJ_CB_DATA_FLAG_ENUM_RESTART_SCAN))
    {
        // Ensure that if the caller is requesting a restart we reset our
        // bookmark of how far we got in the enumeration.
        session->LastEnumEntry = NULL;

        // In case we're restarting ensure we don't think we're done.
        session->EnumCompleted = FALSE;

        // We need to start considering items from the beginning of the list
        // retrieved from the backing store.
        enumHead = session->EnumHead;
    }
    else
    {
        // We are resuming an existing enumeration session.  Note that
        // session->LastEnumEntry may be NULL.  That is okay; it means
        // we got all the entries the last time this callback was invoked.
        // Returning S_OK without adding any new entries to the
        // enumParams->DirEntryBufferHandle buffer signals ProjFS that the
        // enumeration has returned everything it can.
        enumHead = session->LastEnumEntry;
    }

    if (enumHead == NULL)
    {
        // There are no items to return.  Remember that we've returned everything
        // we can.
        session->EnumCompleted = TRUE;
    }
    else
    {
        MY_ENUM_ENTRY* thisEntry = enumHead;
        while (thisEntry != NULL)
        {
            // We'll insert the entry into the return buffer if it matches
            // the search expression captured for this enumeration session.
            if (PrjFileNameMatch(thisEntry->Name, session->SearchExpression))
            {
                PRJ_FILE_BASIC_INFO fileBasicInfo = {};
                fileBasicInfo.IsDirectory = thisEntry->IsDirectory;
                fileBasicInfo.FileSize = thisEntry->FileSize;

                // Format the entry for return to ProjFS.
                if (S_OK != PrjFillDirEntryBuffer(thisEntry->Name,
                                                  &fileBasicInfo,
                                                  enumParams->DirEntryBufferHandle))
                {
                    // We couldn't add this entry to the buffer; remember where we left
                    // off for the next time we're called for this enumeration session.
                    session->LastEnumEntry = thisEntry;
                    hr = S_OK;

                    goto CompleteCallback;
                }
            }

            thisEntry = thisEntry->Next;
        }

        // We reached the end of the list of entries; remember that we've returned
        // everything we can.
        session->EnumCompleted = TRUE;
    }

CompleteCallback:

    // Signal ProjFS that we've completed this callback.  Since this is an enumeration
    // we use the extendedParameters parameter to PrjCompleteCommand.
    PRJ_COMPLETE_COMMAND_EXTENDED_PARAMETERS extendedParams = {};
    extendedParams.CommandType = PRJ_COMPLETE_COMMAND_TYPE_ENUMERATION;
    extendedParams.enumeration.DirEntryBufferHandle = enumParams->DirEntryBufferHandle;

    PrjCompleteCommand(enumParams->NamespaceVirtualizationContext,
                       enumParams->CommandId,
                       hr,
                       &extendedParams);

    MyUntrackEnumForCancellation(enumParams->CommandId);

    free(enumParams);

    // ThreadProc returns 0 on successful completion.
    return 0;
}
```

<span data-ttu-id="169ee-124">Voici un bref exemple PRJ_CANCEL_COMMAND_CB qui fonctionne avec l’exemple de code précédent.</span><span class="sxs-lookup"><span data-stu-id="169ee-124">And here is a brief example PRJ_CANCEL_COMMAND_CB that works with the preceding sample code.</span></span>

```C++
void
MyCancelCommandCallback(
    _In_ const PRJ_CALLBACK_DATA* callbackData
)
{
    // MyMarkEnumForCancellation is a routine the provider might implement to
    // mark a pended enumeration callback as cancelled.  If the given CommandId
    // is not found, it is not an error.  It may not yet have been tracked or
    // it may already have completed and been untracked.
    MyMarkEnumForCancellation(callbackData->CommandId);
}
```