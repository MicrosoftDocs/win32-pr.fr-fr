---
title: Notifications d’opérations du système de fichiers
description: Décrit comment un fournisseur peut recevoir des notifications d’opérations du système de fichiers.
ms.assetid: <GUID-GOES-HERE>
ms.date: 10/04/2018
ms.topic: article
ms.openlocfilehash: 9eae9bde6d56592f371dcd48c24fef96a9eecbdf
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103727805"
---
# <a name="file-system-operation-notifications"></a><span data-ttu-id="13eff-103">Notifications d’opérations du système de fichiers</span><span class="sxs-lookup"><span data-stu-id="13eff-103">File System Operation Notifications</span></span>

<span data-ttu-id="13eff-104">En plus des rappels requis pour la gestion de l’énumération, le retour de métadonnées de fichier et le contenu du fichier, un fournisseur peut éventuellement inscrire un rappel **[PRJ_NOTIFICATION_CB]()** dans son appel à **[PrjStartVirtualizing]()**.</span><span class="sxs-lookup"><span data-stu-id="13eff-104">In addition to required callbacks for handling enumeration, returning file metadata, and file contents, a provider may optionally register a **[PRJ_NOTIFICATION_CB]()** callback in its call to **[PrjStartVirtualizing]()**.</span></span>  <span data-ttu-id="13eff-105">Ce rappel reçoit les notifications des opérations du système de fichiers effectuées sur les fichiers et les répertoires sous la racine de virtualisation de l’instance.</span><span class="sxs-lookup"><span data-stu-id="13eff-105">This callback receives notifications of file system operations performed on files and directories beneath the instance's virtualization root.</span></span>  <span data-ttu-id="13eff-106">Certaines notifications sont des notifications « après opération », qui indiquent au fournisseur qu’une opération vient d’être terminée.</span><span class="sxs-lookup"><span data-stu-id="13eff-106">Some of the notifications are "post-operation" notifications, which tell the provider that an operation has just completed.</span></span>  <span data-ttu-id="13eff-107">Les autres notifications sont des notifications de « pré-opération », ce qui signifie que le fournisseur est averti avant que l’opération ne se produise.</span><span class="sxs-lookup"><span data-stu-id="13eff-107">The other notifications are "pre-operation" notifications, meaning that the provider is notified before the operation happens.</span></span>  <span data-ttu-id="13eff-108">Dans une notification de pré-opération, le fournisseur peut refuser l’opération en retournant un code d’erreur à partir du rappel.</span><span class="sxs-lookup"><span data-stu-id="13eff-108">In a pre-operation notification the provider can veto the operation by returning an error code from the callback.</span></span>  <span data-ttu-id="13eff-109">Cela provoque l’échec de l’opération avec le code d’erreur retourné.</span><span class="sxs-lookup"><span data-stu-id="13eff-109">This causes the operation to fail with the returned error code.</span></span>

## <a name="how-to-specify-notifications-to-receive"></a><span data-ttu-id="13eff-110">Comment spécifier les notifications à recevoir</span><span class="sxs-lookup"><span data-stu-id="13eff-110">How to Specify Notifications to Receive</span></span>

<span data-ttu-id="13eff-111">Si le fournisseur fournit une implémentation de **PRJ_NOTIFICATION_CB** lorsqu’il démarre une instance de virtualisation, il doit également spécifier les notifications qu’il souhaite recevoir.</span><span class="sxs-lookup"><span data-stu-id="13eff-111">If the provider supplies an implementation of **PRJ_NOTIFICATION_CB** when it starts a virtualization instance, it should also specify which notifications it wishes to receive.</span></span>  <span data-ttu-id="13eff-112">Les notifications que le fournisseur peut inscrire sont définies dans l’énumération [PRJ_NOTIFICATION](/windows/win32/api/projectedfslib/ne-projectedfslib-prj_notification) .</span><span class="sxs-lookup"><span data-stu-id="13eff-112">The notifications for which the provider can register are defined in the [PRJ_NOTIFICATION](/windows/win32/api/projectedfslib/ne-projectedfslib-prj_notification) enum.</span></span>

<span data-ttu-id="13eff-113">Lorsque le fournisseur spécifie les notifications qu’il souhaite recevoir, il utilise un tableau d’une ou plusieurs structures de [PRJ_NOTIFICATION_MAPPING](/windows/desktop/api/projectedfslib/ns-projectedfslib-prj_notification_mapping) .</span><span class="sxs-lookup"><span data-stu-id="13eff-113">When the provider specifies the notifications it wishes to receive, it does so using an array of one or more [PRJ_NOTIFICATION_MAPPING](/windows/desktop/api/projectedfslib/ns-projectedfslib-prj_notification_mapping) structures.</span></span>  <span data-ttu-id="13eff-114">Celles-ci définissent des « mappages de notification ».</span><span class="sxs-lookup"><span data-stu-id="13eff-114">These define "notification mappings".</span></span>  <span data-ttu-id="13eff-115">Un mappage de notification est un jumelage entre un répertoire, appelé « racine de notification » et un ensemble de notifications, exprimé sous la forme d’un masque de bits, que ProjFS doit envoyer pour ce répertoire et ses descendants.</span><span class="sxs-lookup"><span data-stu-id="13eff-115">A notification mapping is a pairing between a directory, referred to as a "notification root", and a set of notifications, expressed as a bit mask, which ProjFS should send for that directory and its descendants.</span></span>  <span data-ttu-id="13eff-116">Un mappage de notification peut également être établi pour un seul fichier.</span><span class="sxs-lookup"><span data-stu-id="13eff-116">A notification mapping can also be established for a single file.</span></span>  <span data-ttu-id="13eff-117">Un fichier ou un répertoire spécifié dans un mappage de notification n’a pas besoin d’exister au moment où le fournisseur appelle **PrjStartVirtualizing**, le fournisseur peut spécifier n’importe quel chemin d’accès et le mappage s’appliquera s’il est déjà créé.</span><span class="sxs-lookup"><span data-stu-id="13eff-117">A file or directory specified in a notification mapping does not have to exist already at the time the provider calls **PrjStartVirtualizing**, the provider can specify any path and the mapping will apply to it if it is ever created.</span></span>

<span data-ttu-id="13eff-118">Si le fournisseur spécifie plusieurs mappages de notification et que d’autres sont des descendants d’autres, les mappages doivent être spécifiés par ordre décroissant.</span><span class="sxs-lookup"><span data-stu-id="13eff-118">If the provider specifies multiple notification mappings, and some are descendants of others, the mappings must be specified in descending depth.</span></span>  <span data-ttu-id="13eff-119">Les mappages de notification à des niveaux plus profonds remplacent ceux de niveau supérieur pour leurs descendants.</span><span class="sxs-lookup"><span data-stu-id="13eff-119">Notification mappings at deeper levels override higher-level ones for their descendants.</span></span>

<span data-ttu-id="13eff-120">Si le fournisseur ne spécifie pas un ensemble de mappages de notification, ProjFS l’envoie par défaut PRJ_NOTIFY_FILE_OPENED, PRJ_NOTIFY_NEW_FILE_CREATED et PRJ_NOTIFY_FILE_OVERWRITTEN pour tous les fichiers et répertoires situés sous la racine de virtualisation.</span><span class="sxs-lookup"><span data-stu-id="13eff-120">If the provider does not specify a set of notification mappings, ProjFS will default to sending it PRJ_NOTIFY_FILE_OPENED, PRJ_NOTIFY_NEW_FILE_CREATED, and PRJ_NOTIFY_FILE_OVERWRITTEN for all files and directories beneath the virtualization root.</span></span>

<span data-ttu-id="13eff-121">L’extrait de code suivant montre comment inscrire un ensemble de notifications lors du démarrage d’une instance de virtualisation.</span><span class="sxs-lookup"><span data-stu-id="13eff-121">The following code snippet illustrates how to register a set of notifications when starting a virtualization instance.</span></span>

```C++
PRJ_CALLBACKS callbackTable;

// Supply required callbacks.
callbackTable.StartDirectoryEnumerationCallback = MyStartEnumCallback;
callbackTable.EndDirectoryEnumerationCallback = MyEndEnumCallback;
callbackTable.GetDirectoryEnumerationCallback = MyGetEnumCallback;
callbackTable.GetPlaceholderInfoCallback = MyGetPlaceholderInfoCallback;
callbackTable.GetFileDataCallback = MyGetFileDataCallback;

// The rest of the callbacks are optional.  We want notifications, so specify
// our notification callback.
callbackTable.QueryFileNameCallback = nullptr;
callbackTable.NotificationCallback = MyNotificationCallback;
callbackTable.CancelCommandCallback = nullptr;

// Assume the provider has created a new virtualization root at C:\VirtRoot and
// initialized it with this layout:
//
//     C:\VirtRoot
//     +--- baz
//     \--- foo
//          +--- subdir1
//          \--- subdir2
//
// The provider wants these notifications:
// * Notification of new file/directory creates for all locations within the
//   virtualization root that are not subject to one of the following more
//   specific notification mappings.
// * Notification of new file/directory creates, file opens, post-renames, and
//   pre- and post-deletes for C:\VirtRoot\foo
// * No notifications for C:\VirtRoot\foo\subdir1
PRJ_STARTVIRTUALIZING_OPTIONS startOpts = {};
PRJ_VIRTUALIZATION_MAPPING notificationMappings[3];

// Configure default notifications - notify of new files for most of the tree.
notificationMappings[0].NotificationRoot = L"";
notificationMappings[0].NotificationBitMask = PRJ_NOTIFY_NEW_FILE_CREATED;

// Override default notifications - notify of new files, opened files, and file
// deletes for C:\VirtRoot\foo and its descendants.
notificationMappings[1].NotificationRoot = L"foo";
notificationMappings[1].NotificationBitMask = PRJ_NOTIFY_NEW_FILE_CREATED |
                                              PRJ_NOTIFY_FILE_OPENED |
                                              PRJ_NOTIFY_PRE_DELETE |
                                              PRJ_NOTIFY_FILE_HANDLE_CLOSED_FILE_DELETED |
                                              PRJ_NOTIFY_FILE_RENAMED;

// Override all notifications for C:\VirtRoot\foo\subdir1 and its descendants.
notificationMappings[2].NotificationRoot = L"foo\\subdir1";
notificationMappings[2].NotificationBitMask = PRJ_NOTIFY_SUPPRESS_NOTIFICATIONS;

startOpts.NotificationMappings = notificationMappings;
startOpts.NotificationMappingsCount = ARRAYSIZE(notificationMapping);

// Start the instance and provide our notification mappings.
HRESULT hr;
PRJ_NAMESPACE_VIRTUALIZATION_CONTEXT instanceHandle;
hr = PrjStartVirtualizing(rootName,
                          &callbackTable,
                          nullptr,
                          &startOpts,
                          &instanceHandle);
if (FAILED(hr))
{
    wprintf(L"Failed to start the virtualization instance (0x%08x)\n", hr);
    return;
}
```

## <a name="receiving-notifications"></a><span data-ttu-id="13eff-122">Réception des notifications</span><span class="sxs-lookup"><span data-stu-id="13eff-122">Receiving Notifications</span></span>

<span data-ttu-id="13eff-123">ProjFS envoie des notifications d’opérations du système de fichiers en appelant le rappel **PRJ_NOTIFICATION_CB** du fournisseur.</span><span class="sxs-lookup"><span data-stu-id="13eff-123">ProjFS sends notifications of file system operations by calling the provider's **PRJ_NOTIFICATION_CB** callback.</span></span>  <span data-ttu-id="13eff-124">C’est le cas pour chaque opération pour laquelle le fournisseur s’est inscrit.</span><span class="sxs-lookup"><span data-stu-id="13eff-124">It does this for each operation the provider has registered for.</span></span>  <span data-ttu-id="13eff-125">Si, comme dans l’exemple ci-dessus, le fournisseur inscrit pour PRJ_NOTIFY_NEW_FILE_CREATED | PRJ_NOTIFY_FILE_OPENED | PRJ_NOTIFY_PRE_DELETE | PRJ_NOTIFY_FILE_HANDLE_CLOSED_FILE_DELETED | PRJ_NOTIFY_FILE_RENAMED, et une application a créé un nouveau fichier dans la racine de notification, ProjFS appelle le rappel **PRJ_NOTIFICATION_CB** avec le nom de chemin d’accès du nouveau fichier et le paramètre de _notification_ défini sur PRJ_NOTIFICATION_NEW_FILE_CREATED.</span><span class="sxs-lookup"><span data-stu-id="13eff-125">If, as in the above example, the provider registered for PRJ_NOTIFY_NEW_FILE_CREATED | PRJ_NOTIFY_FILE_OPENED | PRJ_NOTIFY_PRE_DELETE | PRJ_NOTIFY_FILE_HANDLE_CLOSED_FILE_DELETED | PRJ_NOTIFY_FILE_RENAMED, and an application created a new file in the notification root, ProjFS would call the **PRJ_NOTIFICATION_CB** callback with the new file's path name and the _notification_ parameter set to PRJ_NOTIFICATION_NEW_FILE_CREATED.</span></span>

<span data-ttu-id="13eff-126">ProjFS envoie les notifications dans la liste suivante avant que l’opération de système de fichiers associée ait lieu.</span><span class="sxs-lookup"><span data-stu-id="13eff-126">ProjFS sends the notifications in the following list before the associated file system operation takes place.</span></span>  <span data-ttu-id="13eff-127">Si le fournisseur retourne un code d’échec à partir du rappel **PRJ_NOTIFICATION_CB** , l’opération de système de fichiers échoue et retourne le code d’erreur spécifié par le fournisseur.</span><span class="sxs-lookup"><span data-stu-id="13eff-127">If the provider returns a failure code from the **PRJ_NOTIFICATION_CB** callback, the file system operation will fail and return the failure code the provider specified.</span></span>

* <span data-ttu-id="13eff-128">PRJ_NOTIFICATION_PRE_DELETE-le fichier va être supprimé.</span><span class="sxs-lookup"><span data-stu-id="13eff-128">PRJ_NOTIFICATION_PRE_DELETE - The file is about to be deleted.</span></span>
* <span data-ttu-id="13eff-129">PRJ_NOTIFICATION_PRE_RENAME-le fichier va être renommé.</span><span class="sxs-lookup"><span data-stu-id="13eff-129">PRJ_NOTIFICATION_PRE_RENAME - The file is about to be renamed.</span></span>
* <span data-ttu-id="13eff-130">PRJ_NOTIFICATION_PRE_SET_HARDLINK-un lien physique est sur le point d’être créé pour le fichier.</span><span class="sxs-lookup"><span data-stu-id="13eff-130">PRJ_NOTIFICATION_PRE_SET_HARDLINK - A hard link is about to be created for the file.</span></span>
* <span data-ttu-id="13eff-131">PRJ_NOTIFICATION_FILE_PRE_CONVERT_TO_FULL : un fichier est sur le point d’être développé à partir d’un espace réservé dans un fichier complet, ce qui indique que son contenu est susceptible d’être modifié.</span><span class="sxs-lookup"><span data-stu-id="13eff-131">PRJ_NOTIFICATION_FILE_PRE_CONVERT_TO_FULL - A file is about to be expanded from a placeholder to a full file, which indicates its contents are likely to be modified.</span></span>

<span data-ttu-id="13eff-132">ProjFS envoie les notifications dans la liste suivante après la fin de l’opération de système de fichiers associée.</span><span class="sxs-lookup"><span data-stu-id="13eff-132">ProjFS sends the notifications in the following list after the associated file system operation has completed.</span></span>

* <span data-ttu-id="13eff-133">PRJ_NOTIFICATION_FILE_OPENED-un fichier existant a été ouvert.</span><span class="sxs-lookup"><span data-stu-id="13eff-133">PRJ_NOTIFICATION_FILE_OPENED - An existing file has been opened.</span></span>
  * <span data-ttu-id="13eff-134">Même si cette notification est envoyée après l’ouverture du fichier, le fournisseur peut retourner un code d’échec.</span><span class="sxs-lookup"><span data-stu-id="13eff-134">Even though this notification is sent after the file has been opened, the provider can return a failure code.</span></span>  <span data-ttu-id="13eff-135">En réponse, ProjFS annule l’ouverture et retourne l’échec à l’appelant.</span><span class="sxs-lookup"><span data-stu-id="13eff-135">In response, ProjFS will cancel the open and return the failure to the caller.</span></span>
* <span data-ttu-id="13eff-136">PRJ_NOTIFICATION_NEW_FILE_CREATED : un nouveau fichier a été créé.</span><span class="sxs-lookup"><span data-stu-id="13eff-136">PRJ_NOTIFICATION_NEW_FILE_CREATED - A new file has been created.</span></span>
* <span data-ttu-id="13eff-137">PRJ_NOTIFICATION_FILE_OVERWRITTEN : un fichier existant a été remplacé, par exemple en appelant [CreateFileW](/windows/desktop/api/fileapi/nf-fileapi-createfilew) avec l’indicateur **CREATE_ALWAYS** _dwCreationDisposition_ .</span><span class="sxs-lookup"><span data-stu-id="13eff-137">PRJ_NOTIFICATION_FILE_OVERWRITTEN - An existing file has been overwritten, for example by calling [CreateFileW](/windows/desktop/api/fileapi/nf-fileapi-createfilew) with the **CREATE_ALWAYS** _dwCreationDisposition_ flag.</span></span>
* <span data-ttu-id="13eff-138">PRJ_NOTIFICATION_FILE_RENAMED-un fichier a été renommé.</span><span class="sxs-lookup"><span data-stu-id="13eff-138">PRJ_NOTIFICATION_FILE_RENAMED - A file has been renamed.</span></span>
* <span data-ttu-id="13eff-139">PRJ_NOTIFICATION_HARDLINK_CREATED-un [lien physique](/windows/desktop/FileIO/hard-links-and-junctions#hard-links) a été créé pour un fichier.</span><span class="sxs-lookup"><span data-stu-id="13eff-139">PRJ_NOTIFICATION_HARDLINK_CREATED - A [hard link](/windows/desktop/FileIO/hard-links-and-junctions#hard-links) has been created for a file.</span></span>
* <span data-ttu-id="13eff-140">PRJ_NOTIFICATION_FILE_HANDLE_CLOSED_NO_MODIFICATION : un descripteur de fichier a été fermé et le contenu du fichier n’a pas été modifié, et le fichier a été supprimé.</span><span class="sxs-lookup"><span data-stu-id="13eff-140">PRJ_NOTIFICATION_FILE_HANDLE_CLOSED_NO_MODIFICATION - A file handle has been closed, and the file's content was not modified, nor was the file deleted.</span></span>
* <span data-ttu-id="13eff-141">PRJ_NOTIFICATION_FILE_HANLDE_CLOSED_FILE_MODIFIED : un descripteur de fichier a été fermé et le contenu du fichier a été modifié.</span><span class="sxs-lookup"><span data-stu-id="13eff-141">PRJ_NOTIFICATION_FILE_HANLDE_CLOSED_FILE_MODIFIED - A file handle has been closed, and the file's content has been modified.</span></span>
* <span data-ttu-id="13eff-142">PRJ_NOTIFICATION_FILE_HANDLE_CLOSED_FILE_DELETED : un handle de fichier a été fermé et le fichier a été supprimé dans le cadre de la fermeture du handle.</span><span class="sxs-lookup"><span data-stu-id="13eff-142">PRJ_NOTIFICATION_FILE_HANDLE_CLOSED_FILE_DELETED - A file handle has been closed, and the file was deleted as part of closing the handle.</span></span>

<span data-ttu-id="13eff-143">Pour plus d’informations sur chaque notification, reportez-vous à la documentation de **[PRJ_NOTIFICATION](/windows/desktop/api/projectedfslib/ne-projectedfslib-prj_notification)**.</span><span class="sxs-lookup"><span data-stu-id="13eff-143">For more details on each notification refer to the documentation for **[PRJ_NOTIFICATION](/windows/desktop/api/projectedfslib/ne-projectedfslib-prj_notification)**.</span></span>

<span data-ttu-id="13eff-144">Le paramètre _notificationParameters_ du rappel de **PRJ_NOTIFICATION_CB** spécifie des paramètres supplémentaires pour certaines notifications.</span><span class="sxs-lookup"><span data-stu-id="13eff-144">The **PRJ_NOTIFICATION_CB** callback's _notificationParameters_ parameter specifies extra parameters for certain notifications.</span></span>  <span data-ttu-id="13eff-145">Si un fournisseur reçoit une notification PRJ_NOTIFICATION_FILE_OPENED, PRJ_NOTIFICATION_NEW_FILE_CREATED ou PRJ_NOTIFICATION_FILE_OVERWRITTEN ou PRJ_NOTIFICATION_FILE_RENAMED, le fournisseur peut spécifier un nouvel ensemble de notifications à recevoir pour le fichier.</span><span class="sxs-lookup"><span data-stu-id="13eff-145">If a provider receives a PRJ_NOTIFICATION_FILE_OPENED, PRJ_NOTIFICATION_NEW_FILE_CREATED, or PRJ_NOTIFICATION_FILE_OVERWRITTEN, or PRJ_NOTIFICATION_FILE_RENAMED notification, the provider can specify a new set of notifications to receive for the file.</span></span> <span data-ttu-id="13eff-146">Pour plus d’informations, reportez-vous à la documentation de **[PRJ_NOTIFICATION_CB](/windows/desktop/api/projectedfslib/nc-projectedfslib-prj_notification_cb)**.</span><span class="sxs-lookup"><span data-stu-id="13eff-146">For further details, refer to the documentation for **[PRJ_NOTIFICATION_CB](/windows/desktop/api/projectedfslib/nc-projectedfslib-prj_notification_cb)**.</span></span>

<span data-ttu-id="13eff-147">L’exemple suivant montre comment un fournisseur peut traiter les notifications qu’il a inscrites pour dans l’extrait de code ci-dessus.</span><span class="sxs-lookup"><span data-stu-id="13eff-147">The following sample shows simple examples of how a provider might process the notifications it registered for in the code snippet above.</span></span>

```C++
#include <windows.h>

HRESULT
MyNotificationCallback(
    _In_ const PRJ_CALLBACK_DATA* callbackData,
    _In_ BOOLEAN isDirectory,
    _In_ PRJ_NOTIFICATION notification,
    _In_opt_z_ PCWSTR destinationFileName,
    _Inout_ PRJ_NOTIFICATION_PARAMETERS* operationParameters
    )
{
    HRESULT hr = S_OK;

    switch (notification)
    {
    case PRJ_NOTIFY_NEW_FILE_CREATED:

        wprintf(L"A new %ls was created at [%ls].\n",
                isDirectory ? L"directory" : L"file",
                callbackData->FilePathName);

        // Let's stop getting notifications inside newly-created directories.
        if (isDirectory)
        {
            operationParameters->PostCreate.NotificationMask = PRJ_NOTIFY_SUPPRESS_NOTIFICATIONS;
        }
        break;

    case PRJ_NOTIFY_FILE_OPENED:

        wprintf(L"Handle opened to %ls [%ls].\n",
                isDirectory ? L"directory": L"file",
                callbackData->FilePathName);
        break;

    case PRJ_NOTIFY_PRE_DELETE:

        wprintf(L"Attempt to delete %ls [%ls]: ",
                isDirectory ? L"directory": L"file",
                callbackData->FilePathName);

        // MyAllowDelete is a routine the provider might implement to decide
        // whether to allow a given file/directory to be deleted.
        if (!MyAllowDelete(callbackData->FilePathName, isDirectory))
        {
            wprintf(L"DENIED\n");
            hr = HRESULT_FROM_WIN32(ERROR_ACCESS_DENIED);
        }
        else
        {
            wprintf(L"ALLOWED\n");
        }
        break;

    case PRJ_NOTIFY_FILE_HANDLE_CLOSED_FILE_DELETED:

        wprintf(L"The %ls [%ls] was deleted.\n",
                isDirectory ? L"directory": L"file",
                callbackData->FilePathName);
        break;

    case PRJ_NOTIFY_FILE_RENAMED:

        if (wcslen(callbackData->FilePathName) == 0)
        {
            // If callbackData->FilePathName is an empty string, then the item
            // that was renamed was originally in a location not under the
            // virtualization root.
            wprintf(L"A %ls was renamed into the virtualization root,\n",
                    isDirectory ? L"directory": L"file");
            wprintf(L"Its new location is [%ls].\n",
                    destinationFileName);
        }
        else if (wcslen(destinationFileName) == 0)
        {
            // If destinationFileName is an empty string, then the item that was
            // renamed is now in a location not under the virtualization root.
            wprintf(L"A %ls was renamed out of the virtualization root.\n",
                    isDirectory ? L"directory": L"file");
            wprintf(L"Its original location was [%ls].\n",
                    callbackData->FilePathName);
        }
        else
        {
            // If both names are specified, both the new and old names are under
            // the virtualization root (it is never the case that nether name is
            // specified).
            wprintf(L"A %ls [%ls] was renamed.\n",
                    isDirectory ? L"directory": L"file",
                    callbackData->FilePathName);
            wprintf(L"Its new name is [%ls].\n", destinationFileName);
        }
        break;

    default:
        wprintf(L"Unrecognized notification: 0x%08x");
    }

    // Note that this may be a failure code from MyAllowDelete().
    return hr;
}
```