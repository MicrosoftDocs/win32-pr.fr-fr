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
# <a name="enumerating-files-and-directories"></a>Énumération de fichiers et de répertoires

Lorsqu’un fournisseur crée d’abord une racine de virtualisation, il est vide sur le système local.  Autrement dit, aucun des éléments de la Banque de données de stockage n’a encore été mis en cache sur le disque.  À mesure que chaque élément est ouvert, il est mis en cache, mais jusqu’à l’ouverture d’un élément, il existe uniquement dans le magasin de données de stockage.

Étant donné que les éléments non ouverts n’ont pas de présence locale, l’énumération normale des répertoires ne révèle pas leur existence pour l’utilisateur.  Par conséquent, le fournisseur doit participer à l’énumération de répertoires en renvoyant des informations à ProjFS sur les éléments de sa banque de données de stockage.  ProjFS fusionne les informations du fournisseur avec celles du système de fichiers local à présenter à l’utilisateur une liste unifiée du contenu d’un répertoire.

## <a name="directory-enumeration-callbacks"></a>Rappels d’énumération de répertoire

Pour participer à l’énumération de répertoires, le fournisseur doit implémenter les rappels **[PRJ_START_DIRECTORY_ENUMERATION_CB](/windows/win32/api/projectedfslib/nc-projectedfslib-prj_start_directory_enumeration_cb)**, **[PRJ_GET_DIRECTORY_ENUMERATION_CB](/windows/win32/api/projectedfslib/nc-projectedfslib-prj_get_directory_enumeration_cb)** et **[PRJ_END_DIRECTORY_ENUMERATION_CB](/windows/win32/api/projectedfslib/nc-projectedfslib-prj_end_directory_enumeration_cb)** .  Lorsqu’un répertoire situé sous la racine de virtualisation du fournisseur est énuméré, ProjFS effectue les actions suivantes :

1. ProjFS appelle le rappel **PRJ_START_DIRECTORY_ENUMERATION_CB** du fournisseur pour démarrer une session d’énumération.

    Dans le cadre du traitement de ce rappel, le fournisseur doit préparer l’exécution de l’énumération.  Par exemple, il doit allouer toute la mémoire dont il a besoin pour suivre la progression de l’énumération dans son magasin de données de stockage.

    ProjFS identifie le répertoire qui est énuméré dans le membre **FilePathName** du paramètre _callbackdata_ du rappel.  Cela est spécifié en tant que chemin d’accès relatif à la racine de virtualisation.  Par exemple, si la racine de virtualisation se trouve dans `C:\virtRoot` et que le répertoire énuméré est `C:\virtRoot\dir1\dir2` , le membre **FilePathName** contient `dir1\dir2` .  Le fournisseur se prépare à énumérer ce chemin dans son magasin de données de stockage.  Selon les fonctionnalités du magasin de stockage d’un fournisseur, il peut être judicieux d’effectuer l’énumération du magasin de stockage dans le rappel **PRJ_START_DIRECTORY_ENUMERATION_CB** .

    Étant donné que plusieurs énumérations peuvent se produire en parallèle dans le même répertoire, chaque rappel d’énumération a un argument _enumerationId_ pour permettre au fournisseur d’associer les appels de rappel dans une session d’énumération unique.

    Si le fournisseur retourne S_OK à partir du rappel **PRJ_START_DIRECTORY_ENUMERATION_CB** , il doit gérer les informations de session d’énumération qu’il possède jusqu’à ce que ProjFS appelle le rappel **PRJ_END_DIRECTORY_ENUMERATION_CB** avec la même valeur pour _enumerationId_.  Si le fournisseur retourne une erreur à partir de **PRJ_START_DIRECTORY_ENUMERATION_CB**, ProjFS n’appellera pas le rappel **PRJ_END_DIRECTORY_ENUMERATION_CB** pour ce _enumerationId_.

1. ProjFS appelle le rappel **PRJ_GET_DIRECTORY_ENUMERATION_CB** du fournisseur une ou plusieurs fois pour obtenir le contenu du répertoire auprès du fournisseur.

    En réponse à ce rappel, le fournisseur retourne une liste triée d’éléments à partir de sa banque de données de stockage.

    Le rappel peut fournir une expression de recherche dans son paramètre _searchExpression_ que le fournisseur utilise pour définir la portée des résultats de l’énumération.  Si _searchExpression_ a la valeur null, le fournisseur retourne toutes les entrées dans le répertoire énuméré.  Si la valeur n’est pas NULL, le fournisseur peut utiliser **[PrjDoesNameContainWildCards](/windows/win32/api/projectedfslib/nf-projectedfslib-prjdoesnamecontainwildcards)** pour déterminer s’il existe des caractères génériques dans l’expression.  Si c’est le cas, le fournisseur utilise **[PrjFileNameMatch](/windows/win32/api/projectedfslib/nf-projectedfslib-prjfilenamematch)** pour déterminer si une entrée du répertoire correspond à l’expression de recherche.

    Le fournisseur doit capturer la valeur de _searchExpression_ lors du premier appel de ce rappel.  Elle utilise la valeur capturée pour tout appel ultérieur du rappel dans la même session d’énumération, sauf si PRJ_CB_DATA_FLAG_ENUM_RESTART_SCAN est définie dans le champ **Flags** du paramètre _callbackdata_ du rappel.  Dans ce cas, il doit recapturer la valeur de _searchExpression_.

    S’il n’y a pas d’entrées correspondantes dans le magasin de stockage, le fournisseur retourne simplement S_OK à partir du rappel.  Dans le cas contraire, le fournisseur met en forme chaque entrée correspondante de son magasin de stockage dans une structure **[PRJ_FILE_BASIC_INFO](/windows/win32/api/projectedfslib/ns-projectedfslib-prj_file_basic_info)** , puis utilise **[PrjFillDirEntryBuffer](/windows/win32/api/projectedfslib/nf-projectedfslib-prjfilldirentrybuffer)** pour remplir la mémoire tampon fournie par le paramètre _dirEntryBufferHandle_ du rappel.  Le fournisseur continue à ajouter des entrées jusqu’à ce qu’il les ait ajoutées ou jusqu’à ce que **PrjFillDirEntryBuffer** retourne HRESULT_FROM_WIN32 (ERROR_INSUFFICIENT_BUFFER).  Ensuite, le fournisseur retourne S_OK à partir du rappel.  Notez que le fournisseur doit ajouter les entrées à la mémoire tampon _dirEntryBufferHandle_ dans l’ordre de tri approprié.  Le fournisseur doit utiliser **[PrjFileNameCompare](/windows/win32/api/projectedfslib/nf-projectedfslib-prjfilenamecompare)** pour déterminer l’ordre de tri correct.

    > Le fournisseur doit fournir une valeur pour le membre **IsDirectory** de **PRJ_FILE_BASIC_INFO**.  Si **IsDirectory** a la valeur false, le fournisseur doit également fournir une valeur pour le membre **FileSize** .
    >
    > Si le fournisseur ne fournit pas de valeurs pour les membres **CreationTime**, **LastAccessTime**, **LastWriteTime** et **ChangeTime** , ProjFS utilise l’heure système actuelle.
    >
    > ProjFS utilise le FILE_ATTRIBUTE indicateurs que le fournisseur définit dans le membre **FileAttributes** , à l’exception de FILE_ATTRIBUTE_DIRECTORY ; Elle définit la valeur correcte pour FILE_ATTRIBUTE_DIRECTORY dans le membre **FileAttributes** en fonction de la valeur fournie du membre **IsDirectory** .

    Si **PrjFillDirEntryBuffer** retourne HRESULT_FROM_WIN32 (ERROR_INSUFFICIENT_BUFFER) avant que le fournisseur n’ait plus d’entrées à y ajouter, le fournisseur doit effectuer le suivi de l’entrée qu’il essayait d’ajouter lorsqu’il a reçu l’erreur.  La prochaine fois que ProjFS appelle le rappel **PRJ_GET_DIRECTORY_ENUMERATION_CB** pour la même session d’énumération, le fournisseur doit reprendre l’ajout d’entrées à la mémoire tampon _dirEntryBufferHandle_ avec l’entrée qu’il essayait d’ajouter.

    > Si le magasin de stockage prend en charge les liens symboliques, le fournisseur doit utiliser **[PrjFillDirEntryBuffer2](/windows/win32/api/projectedfslib/nf-projectedfslib-prjfilldirentrybuffer2)** pour remplir la mémoire tampon fournie par le paramètre _dirEntryBufferHandle_ du rappel.  **PrjFillDirEntryBuffer2** prend en charge une entrée de mémoire tampon supplémentaire qui permet au fournisseur de spécifier que l’entrée d’énumération est un lien symbolique et quelle est sa cible.  Elle se comporte autrement comme décrit ci-dessus pour **PrjFillDirEntryBuffer**.  L’exemple suivant utilise **PrjFillDirEntryBuffer2** pour illustrer la prise en charge des liens symboliques.
    >
    > Notez que **PrjFillDirEntryBuffer2** est pris en charge à partir de Windows 10, version 2004.  Un fournisseur doit détecter l’existence de **PrjFillDirEntryBuffer2**, par exemple à l’aide de **[GetProcAddress](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress)**.

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

1. ProjFS appelle le rappel **PRJ_END_DIRECTORY_ENUMERATION_CB** du fournisseur pour terminer la session d’énumération.

    Le fournisseur doit effectuer tout nettoyage qu’il doit effectuer pour terminer la session d’énumération, par exemple libérer de la mémoire allouée dans le cadre du traitement **PRJ_START_DIRECTORY_ENUMERATION_CB**.
