---
title: Notifications d’opérations du système de fichiers
description: Décrit comment un fournisseur peut recevoir des notifications d’opérations du système de fichiers.
ms.assetid: <GUID-GOES-HERE>
ms.date: 10/04/2018
ms.topic: article
ms.openlocfilehash: 2e09efcc9d1a1aea99f79b70446162df5e3ef924067ac6619a443aa15e06e9df
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120031239"
---
# <a name="file-system-operation-notifications"></a>Notifications d’opérations du système de fichiers

En plus des rappels requis pour la gestion de l’énumération, le retour de métadonnées de fichier et le contenu du fichier, un fournisseur peut éventuellement inscrire un rappel **[PRJ_NOTIFICATION_CB]()** dans son appel à **[PrjStartVirtualizing]()**.  Ce rappel reçoit les notifications des opérations du système de fichiers effectuées sur les fichiers et les répertoires sous la racine de virtualisation de l’instance.  Certaines notifications sont des notifications « après opération », qui indiquent au fournisseur qu’une opération vient d’être terminée.  Les autres notifications sont des notifications de « pré-opération », ce qui signifie que le fournisseur est averti avant que l’opération ne se produise.  Dans une notification de pré-opération, le fournisseur peut refuser l’opération en retournant un code d’erreur à partir du rappel.  Cela provoque l’échec de l’opération avec le code d’erreur retourné.

## <a name="how-to-specify-notifications-to-receive"></a>Comment spécifier les notifications à recevoir

Si le fournisseur fournit une implémentation de **PRJ_NOTIFICATION_CB** lorsqu’il démarre une instance de virtualisation, il doit également spécifier les notifications qu’il souhaite recevoir.  Les notifications que le fournisseur peut inscrire sont définies dans l’énumération [PRJ_NOTIFICATION](/windows/win32/api/projectedfslib/ne-projectedfslib-prj_notification) .

Lorsque le fournisseur spécifie les notifications qu’il souhaite recevoir, il utilise un tableau d’une ou plusieurs structures de [PRJ_NOTIFICATION_MAPPING](/windows/desktop/api/projectedfslib/ns-projectedfslib-prj_notification_mapping) .  Celles-ci définissent des « mappages de notification ».  Un mappage de notification est un jumelage entre un répertoire, appelé « racine de notification » et un ensemble de notifications, exprimé sous la forme d’un masque de bits, que ProjFS doit envoyer pour ce répertoire et ses descendants.  Un mappage de notification peut également être établi pour un seul fichier.  Un fichier ou un répertoire spécifié dans un mappage de notification n’a pas besoin d’exister au moment où le fournisseur appelle **PrjStartVirtualizing**, le fournisseur peut spécifier n’importe quel chemin d’accès et le mappage s’appliquera s’il est déjà créé.

Si le fournisseur spécifie plusieurs mappages de notification et que d’autres sont des descendants d’autres, les mappages doivent être spécifiés par ordre décroissant.  Les mappages de notification à des niveaux plus profonds remplacent ceux de niveau supérieur pour leurs descendants.

Si le fournisseur ne spécifie pas un ensemble de mappages de notification, ProjFS l’envoie par défaut PRJ_NOTIFY_FILE_OPENED, PRJ_NOTIFY_NEW_FILE_CREATED et PRJ_NOTIFY_FILE_OVERWRITTEN pour tous les fichiers et répertoires situés sous la racine de virtualisation.

L’extrait de code suivant montre comment inscrire un ensemble de notifications lors du démarrage d’une instance de virtualisation.

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

## <a name="receiving-notifications"></a>Réception des notifications

ProjFS envoie des notifications d’opérations du système de fichiers en appelant le rappel **PRJ_NOTIFICATION_CB** du fournisseur.  C’est le cas pour chaque opération pour laquelle le fournisseur s’est inscrit.  Si, comme dans l’exemple ci-dessus, le fournisseur inscrit pour PRJ_NOTIFY_NEW_FILE_CREATED | PRJ_NOTIFY_FILE_OPENED | PRJ_NOTIFY_PRE_DELETE | PRJ_NOTIFY_FILE_HANDLE_CLOSED_FILE_DELETED | PRJ_NOTIFY_FILE_RENAMED, et une application a créé un nouveau fichier dans la racine de notification, ProjFS appelle le rappel **PRJ_NOTIFICATION_CB** avec le nom de chemin d’accès du nouveau fichier et le paramètre de _notification_ défini sur PRJ_NOTIFICATION_NEW_FILE_CREATED.

ProjFS envoie les notifications dans la liste suivante avant que l’opération de système de fichiers associée ait lieu.  Si le fournisseur retourne un code d’échec à partir du rappel **PRJ_NOTIFICATION_CB** , l’opération de système de fichiers échoue et retourne le code d’erreur spécifié par le fournisseur.

* PRJ_NOTIFICATION_PRE_DELETE-le fichier va être supprimé.
* PRJ_NOTIFICATION_PRE_RENAME-le fichier va être renommé.
* PRJ_NOTIFICATION_PRE_SET_HARDLINK-un lien physique est sur le point d’être créé pour le fichier.
* PRJ_NOTIFICATION_FILE_PRE_CONVERT_TO_FULL : un fichier est sur le point d’être développé à partir d’un espace réservé dans un fichier complet, ce qui indique que son contenu est susceptible d’être modifié.

ProjFS envoie les notifications dans la liste suivante après la fin de l’opération de système de fichiers associée.

* PRJ_NOTIFICATION_FILE_OPENED-un fichier existant a été ouvert.
  * Même si cette notification est envoyée après l’ouverture du fichier, le fournisseur peut retourner un code d’échec.  En réponse, ProjFS annule l’ouverture et retourne l’échec à l’appelant.
* PRJ_NOTIFICATION_NEW_FILE_CREATED : un nouveau fichier a été créé.
* PRJ_NOTIFICATION_FILE_OVERWRITTEN : un fichier existant a été remplacé, par exemple en appelant [CreateFileW](/windows/desktop/api/fileapi/nf-fileapi-createfilew) avec l’indicateur **CREATE_ALWAYS** _dwCreationDisposition_ .
* PRJ_NOTIFICATION_FILE_RENAMED-un fichier a été renommé.
* PRJ_NOTIFICATION_HARDLINK_CREATED-un [lien physique](/windows/desktop/FileIO/hard-links-and-junctions#hard-links) a été créé pour un fichier.
* PRJ_NOTIFICATION_FILE_HANDLE_CLOSED_NO_MODIFICATION : un descripteur de fichier a été fermé et le contenu du fichier n’a pas été modifié, et le fichier a été supprimé.
* PRJ_NOTIFICATION_FILE_HANLDE_CLOSED_FILE_MODIFIED : un descripteur de fichier a été fermé et le contenu du fichier a été modifié.
* PRJ_NOTIFICATION_FILE_HANDLE_CLOSED_FILE_DELETED : un handle de fichier a été fermé et le fichier a été supprimé dans le cadre de la fermeture du handle.

Pour plus d’informations sur chaque notification, reportez-vous à la documentation de **[PRJ_NOTIFICATION](/windows/desktop/api/projectedfslib/ne-projectedfslib-prj_notification)**.

Le paramètre _notificationParameters_ du rappel de **PRJ_NOTIFICATION_CB** spécifie des paramètres supplémentaires pour certaines notifications.  Si un fournisseur reçoit une notification PRJ_NOTIFICATION_FILE_OPENED, PRJ_NOTIFICATION_NEW_FILE_CREATED ou PRJ_NOTIFICATION_FILE_OVERWRITTEN ou PRJ_NOTIFICATION_FILE_RENAMED, le fournisseur peut spécifier un nouvel ensemble de notifications à recevoir pour le fichier. Pour plus d’informations, reportez-vous à la documentation de **[PRJ_NOTIFICATION_CB](/windows/desktop/api/projectedfslib/nc-projectedfslib-prj_notification_cb)**.

L’exemple suivant montre comment un fournisseur peut traiter les notifications qu’il a inscrites pour dans l’extrait de code ci-dessus.

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