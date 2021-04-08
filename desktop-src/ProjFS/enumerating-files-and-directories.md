---
title: Énumération de fichiers et de répertoires
description: Décrit comment un fournisseur ProjFS participe à l’énumération de répertoires.
ms.assetid: <GUID-GOES-HERE>
ms.date: 09/25/2018
ms.topic: article
ms.openlocfilehash: e0712ceb927388b090a84a89f80f0e2d3a1befbb
ms.sourcegitcommit: 80d74c0bf4fc402865a1ad223480abe1ce4d1115
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/12/2020
ms.locfileid: "103723993"
---
# <a name="enumerating-files-and-directories"></a><span data-ttu-id="d66ea-103">Énumération de fichiers et de répertoires</span><span class="sxs-lookup"><span data-stu-id="d66ea-103">Enumerating Files and Directories</span></span>

<span data-ttu-id="d66ea-104">Lorsqu’un fournisseur crée d’abord une racine de virtualisation, il est vide sur le système local.</span><span class="sxs-lookup"><span data-stu-id="d66ea-104">When a provider first creates a virtualization root it is empty on the local system.</span></span>  <span data-ttu-id="d66ea-105">Autrement dit, aucun des éléments de la Banque de données de stockage n’a encore été mis en cache sur le disque.</span><span class="sxs-lookup"><span data-stu-id="d66ea-105">That is, none of the items in the backing data store have yet been cached to disk.</span></span>  <span data-ttu-id="d66ea-106">À mesure que chaque élément est ouvert, il est mis en cache, mais jusqu’à l’ouverture d’un élément, il existe uniquement dans le magasin de données de stockage.</span><span class="sxs-lookup"><span data-stu-id="d66ea-106">As each item is opened it is cached, but until an item is opened it only exists in the backing data store.</span></span>

<span data-ttu-id="d66ea-107">Étant donné que les éléments non ouverts n’ont pas de présence locale, l’énumération normale des répertoires ne révèle pas leur existence pour l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="d66ea-107">Since unopened items have no local presence, normal directory enumeration would not reveal their existence to the user.</span></span>  <span data-ttu-id="d66ea-108">Par conséquent, le fournisseur doit participer à l’énumération de répertoires en renvoyant des informations à ProjFS sur les éléments de sa banque de données de stockage.</span><span class="sxs-lookup"><span data-stu-id="d66ea-108">Therefore the provider must participate in directory enumeration by returning information to ProjFS about items in its backing data store.</span></span>  <span data-ttu-id="d66ea-109">ProjFS fusionne les informations du fournisseur avec celles du système de fichiers local à présenter à l’utilisateur une liste unifiée du contenu d’un répertoire.</span><span class="sxs-lookup"><span data-stu-id="d66ea-109">ProjFS merges the information from the provider with what is on the local file system to present to the user a unified list of the contents of a directory.</span></span>

## <a name="directory-enumeration-callbacks"></a><span data-ttu-id="d66ea-110">Rappels d’énumération de répertoire</span><span class="sxs-lookup"><span data-stu-id="d66ea-110">Directory Enumeration Callbacks</span></span>

<span data-ttu-id="d66ea-111">Pour participer à l’énumération de répertoires, le fournisseur doit implémenter les rappels **[PRJ_START_DIRECTORY_ENUMERATION_CB](/windows/win32/api/projectedfslib/nc-projectedfslib-prj_start_directory_enumeration_cb)**, **[PRJ_GET_DIRECTORY_ENUMERATION_CB](/windows/win32/api/projectedfslib/nc-projectedfslib-prj_get_directory_enumeration_cb)** et **[PRJ_END_DIRECTORY_ENUMERATION_CB](/windows/win32/api/projectedfslib/nc-projectedfslib-prj_end_directory_enumeration_cb)** .</span><span class="sxs-lookup"><span data-stu-id="d66ea-111">To participate in directory enumeration the provider must implement the **[PRJ_START_DIRECTORY_ENUMERATION_CB](/windows/win32/api/projectedfslib/nc-projectedfslib-prj_start_directory_enumeration_cb)**, **[PRJ_GET_DIRECTORY_ENUMERATION_CB](/windows/win32/api/projectedfslib/nc-projectedfslib-prj_get_directory_enumeration_cb)**, and **[PRJ_END_DIRECTORY_ENUMERATION_CB](/windows/win32/api/projectedfslib/nc-projectedfslib-prj_end_directory_enumeration_cb)** callbacks.</span></span>  <span data-ttu-id="d66ea-112">Lorsqu’un répertoire situé sous la racine de virtualisation du fournisseur est énuméré, ProjFS effectue les actions suivantes :</span><span class="sxs-lookup"><span data-stu-id="d66ea-112">When a directory under the provider's virtualization root gets enumerated, ProjFS performs the following actions:</span></span>

1. <span data-ttu-id="d66ea-113">ProjFS appelle le rappel **PRJ_START_DIRECTORY_ENUMERATION_CB** du fournisseur pour démarrer une session d’énumération.</span><span class="sxs-lookup"><span data-stu-id="d66ea-113">ProjFS calls the provider's **PRJ_START_DIRECTORY_ENUMERATION_CB** callback to start an enumeration session.</span></span>

    <span data-ttu-id="d66ea-114">Dans le cadre du traitement de ce rappel, le fournisseur doit préparer l’exécution de l’énumération.</span><span class="sxs-lookup"><span data-stu-id="d66ea-114">As part of processing this callback the provider should prepare to perform the enumeration.</span></span>  <span data-ttu-id="d66ea-115">Par exemple, il doit allouer toute la mémoire dont il a besoin pour suivre la progression de l’énumération dans son magasin de données de stockage.</span><span class="sxs-lookup"><span data-stu-id="d66ea-115">For example, it should allocate any memory it may need to track the progress of the enumeration in its backing data store.</span></span>

    <span data-ttu-id="d66ea-116">ProjFS identifie le répertoire qui est énuméré dans le membre **FilePathName** du paramètre _callbackdata_ du rappel.</span><span class="sxs-lookup"><span data-stu-id="d66ea-116">ProjFS identifies the directory being enumerated in the **FilePathName** member of the callback's _callbackData_ parameter.</span></span>  <span data-ttu-id="d66ea-117">Cela est spécifié en tant que chemin d’accès relatif à la racine de virtualisation.</span><span class="sxs-lookup"><span data-stu-id="d66ea-117">This is specified as a path relative to the virtualization root.</span></span>  <span data-ttu-id="d66ea-118">Par exemple, si la racine de virtualisation se trouve dans `C:\virtRoot` et que le répertoire énuméré est `C:\virtRoot\dir1\dir2` , le membre **FilePathName** contient `dir1\dir2` .</span><span class="sxs-lookup"><span data-stu-id="d66ea-118">For example, if the virtualization root is located at `C:\virtRoot`, and the directory being enumerated is `C:\virtRoot\dir1\dir2`, the **FilePathName** member will contain `dir1\dir2`.</span></span>  <span data-ttu-id="d66ea-119">Le fournisseur se prépare à énumérer ce chemin dans son magasin de données de stockage.</span><span class="sxs-lookup"><span data-stu-id="d66ea-119">The provider will prepare to enumerate that path in its backing data store.</span></span>  <span data-ttu-id="d66ea-120">Selon les fonctionnalités du magasin de stockage d’un fournisseur, il peut être judicieux d’effectuer l’énumération du magasin de stockage dans le rappel **PRJ_START_DIRECTORY_ENUMERATION_CB** .</span><span class="sxs-lookup"><span data-stu-id="d66ea-120">Depending on the capabilities of a provider's backing store it may make sense to perform the backing store enumeration in the **PRJ_START_DIRECTORY_ENUMERATION_CB** callback.</span></span>

    <span data-ttu-id="d66ea-121">Étant donné que plusieurs énumérations peuvent se produire en parallèle dans le même répertoire, chaque rappel d’énumération a un argument _enumerationId_ pour permettre au fournisseur d’associer les appels de rappel dans une session d’énumération unique.</span><span class="sxs-lookup"><span data-stu-id="d66ea-121">Because multiple enumerations may occur in parallel in the same directory, each enumeration callback has an _enumerationId_ argument to enable the provider to associate the callback invocations into a single enumeration session.</span></span>

    <span data-ttu-id="d66ea-122">Si le fournisseur retourne S_OK à partir du rappel **PRJ_START_DIRECTORY_ENUMERATION_CB** , il doit gérer les informations de session d’énumération qu’il possède jusqu’à ce que ProjFS appelle le rappel **PRJ_END_DIRECTORY_ENUMERATION_CB** avec la même valeur pour _enumerationId_.</span><span class="sxs-lookup"><span data-stu-id="d66ea-122">If the provider returns S_OK from the **PRJ_START_DIRECTORY_ENUMERATION_CB** callback, it must maintain any enumeration session information it has until ProjFS invokes the **PRJ_END_DIRECTORY_ENUMERATION_CB** callback with the same value for _enumerationId_.</span></span>  <span data-ttu-id="d66ea-123">Si le fournisseur retourne une erreur à partir de **PRJ_START_DIRECTORY_ENUMERATION_CB**, ProjFS n’appellera pas le rappel **PRJ_END_DIRECTORY_ENUMERATION_CB** pour ce _enumerationId_.</span><span class="sxs-lookup"><span data-stu-id="d66ea-123">If the provider returns an error from **PRJ_START_DIRECTORY_ENUMERATION_CB**, ProjFS will not invoke the **PRJ_END_DIRECTORY_ENUMERATION_CB** callback for that _enumerationId_.</span></span>

1. <span data-ttu-id="d66ea-124">ProjFS appelle le rappel **PRJ_GET_DIRECTORY_ENUMERATION_CB** du fournisseur une ou plusieurs fois pour obtenir le contenu du répertoire auprès du fournisseur.</span><span class="sxs-lookup"><span data-stu-id="d66ea-124">ProjFS calls the provider's **PRJ_GET_DIRECTORY_ENUMERATION_CB** callback one or more times to get the directory contents from the provider.</span></span>

    <span data-ttu-id="d66ea-125">En réponse à ce rappel, le fournisseur retourne une liste triée d’éléments à partir de sa banque de données de stockage.</span><span class="sxs-lookup"><span data-stu-id="d66ea-125">In response to this callback the provider returns a sorted list of items from its backing data store.</span></span>

    <span data-ttu-id="d66ea-126">Le rappel peut fournir une expression de recherche dans son paramètre _searchExpression_ que le fournisseur utilise pour définir la portée des résultats de l’énumération.</span><span class="sxs-lookup"><span data-stu-id="d66ea-126">The callback may provide a search expression in its _searchExpression_ parameter that the provider uses to scope the results of the enumeration.</span></span>  <span data-ttu-id="d66ea-127">Si _searchExpression_ a la valeur null, le fournisseur retourne toutes les entrées dans le répertoire énuméré.</span><span class="sxs-lookup"><span data-stu-id="d66ea-127">If _searchExpression_ is NULL, the provider returns all the entries in the directory being enumerated.</span></span>  <span data-ttu-id="d66ea-128">Si la valeur n’est pas NULL, le fournisseur peut utiliser **[PrjDoesNameContainWildCards](/windows/win32/api/projectedfslib/nf-projectedfslib-prjdoesnamecontainwildcards)** pour déterminer s’il existe des caractères génériques dans l’expression.</span><span class="sxs-lookup"><span data-stu-id="d66ea-128">If it is non-NULL, the provider can use **[PrjDoesNameContainWildCards](/windows/win32/api/projectedfslib/nf-projectedfslib-prjdoesnamecontainwildcards)** to determine whether there are wildcards in the expression.</span></span>  <span data-ttu-id="d66ea-129">Si c’est le cas, le fournisseur utilise **[PrjFileNameMatch](/windows/win32/api/projectedfslib/nf-projectedfslib-prjfilenamematch)** pour déterminer si une entrée du répertoire correspond à l’expression de recherche.</span><span class="sxs-lookup"><span data-stu-id="d66ea-129">If there are, the provider uses **[PrjFileNameMatch](/windows/win32/api/projectedfslib/nf-projectedfslib-prjfilenamematch)** to determine whether an entry in the directory matches the search expression.</span></span>

    <span data-ttu-id="d66ea-130">Le fournisseur doit capturer la valeur de _searchExpression_ lors du premier appel de ce rappel.</span><span class="sxs-lookup"><span data-stu-id="d66ea-130">The provider should capture the value of _searchExpression_ on the first invocation of this callback.</span></span>  <span data-ttu-id="d66ea-131">Elle utilise la valeur capturée pour tout appel ultérieur du rappel dans la même session d’énumération, sauf si PRJ_CB_DATA_FLAG_ENUM_RESTART_SCAN est définie dans le champ **Flags** du paramètre _callbackdata_ du rappel.</span><span class="sxs-lookup"><span data-stu-id="d66ea-131">It uses the captured value on any subsequent invocation of the callback in the same enumeration session, unless PRJ_CB_DATA_FLAG_ENUM_RESTART_SCAN is set in the **Flags** field of the callback's _callbackData_ parameter.</span></span>  <span data-ttu-id="d66ea-132">Dans ce cas, il doit recapturer la valeur de _searchExpression_.</span><span class="sxs-lookup"><span data-stu-id="d66ea-132">In that case it should recapture the value of _searchExpression_.</span></span>

    <span data-ttu-id="d66ea-133">S’il n’y a pas d’entrées correspondantes dans le magasin de stockage, le fournisseur retourne simplement S_OK à partir du rappel.</span><span class="sxs-lookup"><span data-stu-id="d66ea-133">If there are no matching entries in its backing store, the provider simply returns S_OK from the callback.</span></span>  <span data-ttu-id="d66ea-134">Dans le cas contraire, le fournisseur met en forme chaque entrée correspondante de son magasin de stockage dans une structure **[PRJ_FILE_BASIC_INFO](/windows/win32/api/projectedfslib/ns-projectedfslib-prj_file_basic_info)** , puis utilise **[PrjFillDirEntryBuffer](/windows/win32/api/projectedfslib/nf-projectedfslib-prjfilldirentrybuffer)** pour remplir la mémoire tampon fournie par le paramètre _dirEntryBufferHandle_ du rappel.</span><span class="sxs-lookup"><span data-stu-id="d66ea-134">Otherwise the provider formats each matching entry from its backing store into a **[PRJ_FILE_BASIC_INFO](/windows/win32/api/projectedfslib/ns-projectedfslib-prj_file_basic_info)** structure, and then uses **[PrjFillDirEntryBuffer](/windows/win32/api/projectedfslib/nf-projectedfslib-prjfilldirentrybuffer)** to fill the buffer provided by the callback's _dirEntryBufferHandle_ parameter.</span></span>  <span data-ttu-id="d66ea-135">Le fournisseur continue à ajouter des entrées jusqu’à ce qu’il les ait ajoutées ou jusqu’à ce que **PrjFillDirEntryBuffer** retourne HRESULT_FROM_WIN32 (ERROR_INSUFFICIENT_BUFFER).</span><span class="sxs-lookup"><span data-stu-id="d66ea-135">The provider keeps adding entries until it has added them all or until **PrjFillDirEntryBuffer** returns HRESULT_FROM_WIN32(ERROR_INSUFFICIENT_BUFFER).</span></span>  <span data-ttu-id="d66ea-136">Ensuite, le fournisseur retourne S_OK à partir du rappel.</span><span class="sxs-lookup"><span data-stu-id="d66ea-136">Then the provider returns S_OK from the callback.</span></span>  <span data-ttu-id="d66ea-137">Notez que le fournisseur doit ajouter les entrées à la mémoire tampon _dirEntryBufferHandle_ dans l’ordre de tri approprié.</span><span class="sxs-lookup"><span data-stu-id="d66ea-137">Note that the provider must add the entries to the _dirEntryBufferHandle_ buffer in the correct sort order.</span></span>  <span data-ttu-id="d66ea-138">Le fournisseur doit utiliser **[PrjFileNameCompare](/windows/win32/api/projectedfslib/nf-projectedfslib-prjfilenamecompare)** pour déterminer l’ordre de tri correct.</span><span class="sxs-lookup"><span data-stu-id="d66ea-138">The provider should use **[PrjFileNameCompare](/windows/win32/api/projectedfslib/nf-projectedfslib-prjfilenamecompare)** to determine the correct sort order.</span></span>

    > <span data-ttu-id="d66ea-139">Le fournisseur doit fournir une valeur pour le membre **IsDirectory** de **PRJ_FILE_BASIC_INFO**.</span><span class="sxs-lookup"><span data-stu-id="d66ea-139">The provider must supply a value for the **IsDirectory** member of **PRJ_FILE_BASIC_INFO**.</span></span>  <span data-ttu-id="d66ea-140">Si **IsDirectory** a la valeur false, le fournisseur doit également fournir une valeur pour le membre **FileSize** .</span><span class="sxs-lookup"><span data-stu-id="d66ea-140">If **IsDirectory** is FALSE, the provider must also supply a value for the **FileSize** member.</span></span>
    >
    > <span data-ttu-id="d66ea-141">Si le fournisseur ne fournit pas de valeurs pour les membres **CreationTime**, **LastAccessTime**, **LastWriteTime** et **ChangeTime** , ProjFS utilise l’heure système actuelle.</span><span class="sxs-lookup"><span data-stu-id="d66ea-141">If the provider does not supply values for the **CreationTime**, **LastAccessTime**, **LastWriteTime**, and **ChangeTime** members, ProjFS will use the current system time.</span></span>
    >
    > <span data-ttu-id="d66ea-142">ProjFS utilise le FILE_ATTRIBUTE indicateurs que le fournisseur définit dans le membre **FileAttributes** , à l’exception de FILE_ATTRIBUTE_DIRECTORY ; Elle définit la valeur correcte pour FILE_ATTRIBUTE_DIRECTORY dans le membre **FileAttributes** en fonction de la valeur fournie du membre **IsDirectory** .</span><span class="sxs-lookup"><span data-stu-id="d66ea-142">ProjFS will use whatever FILE_ATTRIBUTE flags the provider sets in the **FileAttributes** member except for FILE_ATTRIBUTE_DIRECTORY; it will set the correct value for FILE_ATTRIBUTE_DIRECTORY in the **FileAttributes** member according to the supplied value of the **IsDirectory** member.</span></span>

    <span data-ttu-id="d66ea-143">Si **PrjFillDirEntryBuffer** retourne HRESULT_FROM_WIN32 (ERROR_INSUFFICIENT_BUFFER) avant que le fournisseur n’ait plus d’entrées à y ajouter, le fournisseur doit effectuer le suivi de l’entrée qu’il essayait d’ajouter lorsqu’il a reçu l’erreur.</span><span class="sxs-lookup"><span data-stu-id="d66ea-143">If **PrjFillDirEntryBuffer** returns HRESULT_FROM_WIN32(ERROR_INSUFFICIENT_BUFFER) before the provider runs out of entries to add to it, the provider must keep track of the entry it was trying to add when it received the error.</span></span>  <span data-ttu-id="d66ea-144">La prochaine fois que ProjFS appelle le rappel **PRJ_GET_DIRECTORY_ENUMERATION_CB** pour la même session d’énumération, le fournisseur doit reprendre l’ajout d’entrées à la mémoire tampon _dirEntryBufferHandle_ avec l’entrée qu’il essayait d’ajouter.</span><span class="sxs-lookup"><span data-stu-id="d66ea-144">The next time ProjFS calls the **PRJ_GET_DIRECTORY_ENUMERATION_CB** callback for the same enumeration session, the provider must resume adding entries to the _dirEntryBufferHandle_ buffer with the entry it was trying to add.</span></span>

    > <span data-ttu-id="d66ea-145">Si le magasin de stockage prend en charge les liens symboliques, le fournisseur doit utiliser **[PrjFillDirEntryBuffer2](/windows/win32/api/projectedfslib/nf-projectedfslib-prjfilldirentrybuffer2)** pour remplir la mémoire tampon fournie par le paramètre _dirEntryBufferHandle_ du rappel.</span><span class="sxs-lookup"><span data-stu-id="d66ea-145">If the backing store supports symbolic links, the provider must use **[PrjFillDirEntryBuffer2](/windows/win32/api/projectedfslib/nf-projectedfslib-prjfilldirentrybuffer2)** to fill the buffer provided by the callback's _dirEntryBufferHandle_ parameter.</span></span>  <span data-ttu-id="d66ea-146">**PrjFillDirEntryBuffer2** prend en charge une entrée de mémoire tampon supplémentaire qui permet au fournisseur de spécifier que l’entrée d’énumération est un lien symbolique et quelle est sa cible.</span><span class="sxs-lookup"><span data-stu-id="d66ea-146">**PrjFillDirEntryBuffer2** supports an extra buffer input that allows the provider to specify that the enumeration entry is a symbolic link and what its target is.</span></span>  <span data-ttu-id="d66ea-147">Elle se comporte autrement comme décrit ci-dessus pour **PrjFillDirEntryBuffer**.</span><span class="sxs-lookup"><span data-stu-id="d66ea-147">It otherwise behaves as described above for **PrjFillDirEntryBuffer**.</span></span>  <span data-ttu-id="d66ea-148">L’exemple suivant utilise **PrjFillDirEntryBuffer2** pour illustrer la prise en charge des liens symboliques.</span><span class="sxs-lookup"><span data-stu-id="d66ea-148">The following sample uses **PrjFillDirEntryBuffer2** to illustrate support for symbolic links.</span></span>
    >
    > <span data-ttu-id="d66ea-149">Notez que **PrjFillDirEntryBuffer2** est pris en charge à partir de Windows 10, version 2004.</span><span class="sxs-lookup"><span data-stu-id="d66ea-149">Note that **PrjFillDirEntryBuffer2** is supported as of Windows 10, version 2004.</span></span>  <span data-ttu-id="d66ea-150">Un fournisseur doit détecter l’existence de **PrjFillDirEntryBuffer2**, par exemple à l’aide de **[GetProcAddress](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress)**.</span><span class="sxs-lookup"><span data-stu-id="d66ea-150">A provider should probe for the existence of **PrjFillDirEntryBuffer2**, for instance by using **[GetProcAddress](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress)**.</span></span>

    ```C++
    typedef struct MY_ENUM_ENTRY MY_ENUM_ENTRY;

    typedef struct MY_ENUM_ENTRY {
        MY_ENUM_ENTRY* Next;
        PWSTR Name;
        BOOLEAN IsDirectory;
        INT64 FileSize;
        BOOLEAN IsSymlink;
        PWSTR SymlinkTarget;
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

    HRESULT
    MyGetEnumCallback(
        _In_ const PRJ_CALLBACK_DATA* callbackData,
        _In_ const GUID* enumerationId,
        _In_opt_z_ PCWSTR searchExpression,
        _In_ PRJ_DIR_ENTRY_BUFFER_HANDLE dirEntryBufferHandle
        )
    {
        // MyGetEnumSession is a routine the provider might implement to find
        // information about the enumeration session that it first stored
        // when processing its PRJ_START_DIRECTORY_ENUMERATION_CB callback.
        //
        // In this example the PRJ_START_DIRECTORY_ENUMERATION_CB callback has
        // already retrieved a list of the items in the backing store located at
        // callbackData->FilePathName, sorted them using PrjFileNameCompare()
        // to determine collation order, and stored the list in session->EnumHead.
        MY_ENUM_SESSION* session = NULL;
        session = MyGetEnumSession(enumerationId);

        if (session == NULL)
        {
            return HRESULT_FROM_WIN32(ERROR_INVALID_PARAMETER);
        }

        if (!session->SearchExpressionCaptured ||
            (callbackData->Flags & PRJ_CB_DATA_FLAG_ENUM_RESTART_SCAN))
        {
            if (searchExpression != NULL)
            {
                if (wcsncpy_s(session->SearchExpression,
                              session->SearchExpressionMaxLen,
                              searchExpression,
                              wcslen(searchExpression)))
                {
                    // Failed to copy the search expression; perhaps the provider
                    // could try reallocating session->SearchExpression.
                }
            }
            else
            {
                if (wcsncpy_s(session->SearchExpression,
                              session->SearchExpressionMaxLen,
                              "*",
                              1))
                {
                    // Failed to copy the search expression; perhaps the provider
                    // could try reallocating session->SearchExpression.
                }
            }
            session->SearchExpressionCaptured = TRUE;
        }

        MY_ENUM_ENTRY* enumHead = NULL;

        // We have to start the enumeration from the beginning if we aren't
        // continuing an existing session or if the caller is requesting a restart.
        if (((session->LastEnumEntry == NULL) &&
             !session->EnumCompleted) ||
            (callbackData->Flags & PRJ_CB_DATA_FLAG_ENUM_RESTART_SCAN))
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
            // dirEntryBufferHandle buffer signals ProjFS that the enumeration
            // has returned everything it can.
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

                    // If our backing store says this is really a symbolic link,
                    // set up to tell ProjFS that it is a symlink and what its
                    // target is.
                    PRJ_EXTENDED_INFO extraInfo = {};
                    if (thisEntry->IsSymlink)
                    {
                        extraInfo.InfoType = PRJ_EXT_INFO_SYMLINK;
                        extraInfo.Symlink.TargetName = thisEntry->SymlinkTarget;
                    }

                    // Format the entry for return to ProjFS.
                    HRESULT fillResult = PrjFillDirEntryBuffer2(dirEntryBufferHandle,
                                                                thisEntry->Name,
                                                                &fileBasicInfo,
                                                                thisEntry->IsSymlink ? &extraInfo : NULL);

                    if (fillResult == HRESULT_FROM_WIN32(ERROR_INSUFFICIENT_BUFFER))
                    {
                        // We couldn't add this entry to the buffer; remember where we left
                        // off for the next time we're called for this enumeration session.
                        session->LastEnumEntry = thisEntry;
                        return S_OK;
                    }
                }

                thisEntry = thisEntry->Next;
            }

            // We reached the end of the list of entries; remember that we've returned
            // everything we can.
            session->EnumCompleted = TRUE;
        }

        return S_OK;
    }
    ```

1. <span data-ttu-id="d66ea-151">ProjFS appelle le rappel **PRJ_END_DIRECTORY_ENUMERATION_CB** du fournisseur pour terminer la session d’énumération.</span><span class="sxs-lookup"><span data-stu-id="d66ea-151">ProjFS calls the provider's **PRJ_END_DIRECTORY_ENUMERATION_CB** callback to end the enumeration session.</span></span>

    <span data-ttu-id="d66ea-152">Le fournisseur doit effectuer tout nettoyage qu’il doit effectuer pour terminer la session d’énumération, par exemple libérer de la mémoire allouée dans le cadre du traitement **PRJ_START_DIRECTORY_ENUMERATION_CB**.</span><span class="sxs-lookup"><span data-stu-id="d66ea-152">The provider should perform any cleanup it needs to do to end the enumeration session, such as deallocate memory allocated as part of processing **PRJ_START_DIRECTORY_ENUMERATION_CB**.</span></span>
