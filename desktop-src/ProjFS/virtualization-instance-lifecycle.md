---
title: Cycle de vie des instances de virtualisation
description: Vue d’ensemble du cycle de vie d’une instance de virtualisation ProjFS.
ms.assetid: <GUID-GOES-HERE>
ms.date: 09/17/2018
ms.topic: article
ms.openlocfilehash: 567eff1f7b8acf330dba7c652e2e12b724072b9b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104507958"
---
# <a name="virtualization-instance-lifecycle"></a>Cycle de vie des instances de virtualisation

L’application fournisseur gère une ou plusieurs instances de virtualisation.  Chaque instance de virtualisation passe par quatre étapes dans son cycle de vie :

1. Création
2. Démarrage
3. Runtime
4. Éteindre

Notez qu’après l’arrêt d’une instance de virtualisation, le fournisseur n’a pas besoin de le recréer pour le réutiliser.  Il peut tout simplement le relancer.

> **Remarque**: cette section présente des exemples d’API ProjFS.  Chaque exemple est destiné à illustrer l’utilisation de l’API de base.  Pour obtenir la documentation des options inutilisées dans ces exemples, consultez la référence de l' [API ProjFS](/windows/desktop/api/_projfs).

## <a name="creating-a-virtualization-root"></a>Création d’une racine de virtualisation

Avant qu’un fournisseur puisse démarrer l’instance de virtualisation qui projette les éléments dans le système de fichiers local, il doit créer la racine de virtualisation.  La racine de virtualisation est le répertoire sous lequel le fournisseur projette une arborescence de répertoires et de fichiers.

Pour créer une racine de virtualisation, le fournisseur doit :

1. Créez un répertoire qui servira de racine de virtualisation.

    Le fournisseur crée un répertoire qui servira de racine de virtualisation à l’aide de, par exemple **[CreateDirectory](/windows/desktop/api/fileapi/nf-fileapi-createdirectoryw)**:

    ```C++
    HRESULT hr;
    const wchar_t* rootName = LR"(C:\virtRoot)";
    if (!CreateDirectoryW(rootName, nullptr))
    {
        hr = HRESULT_FROM_WIN32(GetLastError());
        wprintf(L"Failed to create virtualization root (0x%08x)\n", hr);
        return;
    }
    ```

1. Créez un ID d’instance de virtualisation.

    Chaque instance de virtualisation a un ID unique appelé _ID d’instance de virtualisation_.  Le système utilise cette valeur pour identifier l’instance de virtualisation à laquelle son contenu est associé.

    ```C++
    GUID instanceId;
    hr = CoCreateGuid(&instanceId);
    if (FAILED(hr))
    {
        wprintf(L"Failed to create instance ID (0x%08x)\n", hr);
        return;
    }
    ```

1. Marquez le nouveau répertoire comme racine de virtualisation.

    Le fournisseur appelle **[PrjMarkDirectoryAsPlaceholder](/windows/desktop/api/projectedfslib/nf-projectedfslib-prjmarkdirectoryasplaceholder)** pour marquer le nouveau répertoire comme racine de virtualisation et l’assigner à l’instance de virtualisation.

    ```C++
    hr = PrjMarkDirectoryAsPlaceholder(rootName,
                                       nullptr,
                                       nullptr,
                                       &instanceId);
    if (FAILED(hr))
    {
        wprintf(L"Failed to mark virtualization root (0x%08x)\n", hr);
        return;
    }
    ```

Le fournisseur a uniquement besoin de créer la racine de virtualisation une seule fois pour chaque instance de virtualisation.  Une fois la racine créée, son instance associée peut être démarrée et arrêtée à plusieurs reprises sans recréer la racine.

## <a name="starting-a-virtualization-instance"></a>Démarrage d’une instance de virtualisation

Une fois la racine de virtualisation créée, le fournisseur doit démarrer l’instance de virtualisation.  Cela indique à ProjFS que le fournisseur est prêt à recevoir des rappels et à fournir des données.

Pour démarrer l’instance de virtualisation, le fournisseur doit :

1. Configurez la table de rappel.

    ProjFS communique avec le fournisseur en appelant les routines de rappel implémentées par le fournisseur.  Le fournisseur remplit un struct [PRJ_CALLBACKS](/windows/desktop/api/projectedfslib/ns-projectedfslib-prj_callbacks) avec des pointeurs vers ses routines de rappel.

    ```C++
    PRJ_CALLBACKS callbackTable;

    // Supply required callbacks.
    callbackTable.StartDirectoryEnumerationCallback = MyStartEnumCallback;
    callbackTable.EndDirectoryEnumerationCallback = MyEndEnumCallback;
    callbackTable.GetDirectoryEnumerationCallback = MyGetEnumCallback;
    callbackTable.GetPlaceholderInfoCallback = MyGetPlaceholderInfoCallback;
    callbackTable.GetFileDataCallback = MyGetFileDataCallback;

    // The rest of the callbacks are optional.
    callbackTable.QueryFileNameCallback = nullptr;
    callbackTable.NotificationCallback = nullptr;
    callbackTable.CancelCommandCallback = nullptr;
    ```

1. Démarrez l’instance de.

    Le fournisseur appelle **[PrjStartVirtualizing](/windows/desktop/api/projectedfslib/nf-projectedfslib-prjstartvirtualizing)** pour démarrer l’instance de virtualisation.

    ```C++
    PRJ_NAMESPACE_VIRTUALIZATION_CONTEXT instanceHandle;
    hr = PrjStartVirtualizing(rootName,
                              &callbackTable,
                              nullptr,
                              nullptr,
                              &instanceHandle);
    if (FAILED(hr))
    {
        wprintf(L"Failed to start the virtualization instance (0x%08x)\n", hr);
        return;
    }
    ```
    Le paramètre _instanceHandle_ de **PrjStartVirtualizing** retourne un handle vers l’instance de virtualisation.  Le fournisseur utilise ce handle lors de l’appel d’autres API ProjFS.

## <a name="virtualization-instance-runtime"></a>Runtime de l’instance de virtualisation

Une fois l’appel à **PrjStartVirtualizing** retourné, ProjFS appellera les routines de rappel du fournisseur en réponse aux opérations du système de fichiers dans l’instance de virtualisation.  Pour plus d’informations sur la façon dont le fournisseur peut gérer différentes opérations du système de fichiers, reportez-vous aux sections suivantes :

* [Énumération de fichiers et de répertoires](enumerating-files-and-directories.md)
* [Envoi de données de fichier](providing-file-data.md)
* [Notifications d’opérations du système de fichiers](file-system-operation-notifications.md)
* [Gestion des modifications d’affichage](handling-view-changes.md)

## <a name="shutting-down-a-virtualization-instance"></a>Arrêt d’une instance de virtualisation

Pour signaler à ProjFS que le fournisseur souhaite cesser de recevoir des rappels et fournir des données, le fournisseur doit arrêter l’instance de virtualisation.  Pour ce faire, le fournisseur appelle **[PrjStopVirtualizing](/windows/desktop/api/projectedfslib/nf-projectedfslib-prjstopvirtualizing)**, en lui passant le handle de l’instance de virtualisation qu’il a reçue de l’appel à **PrjStartVirtualizing**.

```C++
PrjStopVirtualizing(instanceHandle);
```

Notez que jusqu’à ce que cet appel retourne, ProjFS peut continuer à appeler les routines de rappel du fournisseur.