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
# <a name="virtualization-instance-lifecycle"></a><span data-ttu-id="0c773-103">Cycle de vie des instances de virtualisation</span><span class="sxs-lookup"><span data-stu-id="0c773-103">Virtualization Instance Lifecycle</span></span>

<span data-ttu-id="0c773-104">L’application fournisseur gère une ou plusieurs instances de virtualisation.</span><span class="sxs-lookup"><span data-stu-id="0c773-104">The provider application maintains one or more virtualization instances.</span></span>  <span data-ttu-id="0c773-105">Chaque instance de virtualisation passe par quatre étapes dans son cycle de vie :</span><span class="sxs-lookup"><span data-stu-id="0c773-105">Each virtualization instance goes through four stages in its lifecycle:</span></span>

1. <span data-ttu-id="0c773-106">Création</span><span class="sxs-lookup"><span data-stu-id="0c773-106">Creation</span></span>
2. <span data-ttu-id="0c773-107">Démarrage</span><span class="sxs-lookup"><span data-stu-id="0c773-107">Startup</span></span>
3. <span data-ttu-id="0c773-108">Runtime</span><span class="sxs-lookup"><span data-stu-id="0c773-108">Runtime</span></span>
4. <span data-ttu-id="0c773-109">Éteindre</span><span class="sxs-lookup"><span data-stu-id="0c773-109">Shutdown</span></span>

<span data-ttu-id="0c773-110">Notez qu’après l’arrêt d’une instance de virtualisation, le fournisseur n’a pas besoin de le recréer pour le réutiliser.</span><span class="sxs-lookup"><span data-stu-id="0c773-110">Note that after shutting down a virtualization instance the provider does not need to re-create it to reuse it.</span></span>  <span data-ttu-id="0c773-111">Il peut tout simplement le relancer.</span><span class="sxs-lookup"><span data-stu-id="0c773-111">It can simply start it up again.</span></span>

> <span data-ttu-id="0c773-112">**Remarque**: cette section présente des exemples d’API ProjFS.</span><span class="sxs-lookup"><span data-stu-id="0c773-112">**Note**: This section shows examples of ProjFS APIs.</span></span>  <span data-ttu-id="0c773-113">Chaque exemple est destiné à illustrer l’utilisation de l’API de base.</span><span class="sxs-lookup"><span data-stu-id="0c773-113">Each example is meant to illustrate basic API usage.</span></span>  <span data-ttu-id="0c773-114">Pour obtenir la documentation des options inutilisées dans ces exemples, consultez la référence de l' [API ProjFS](/windows/desktop/api/_projfs).</span><span class="sxs-lookup"><span data-stu-id="0c773-114">For documentation of options unused in these examples please consult the [ProjFS API reference](/windows/desktop/api/_projfs).</span></span>

## <a name="creating-a-virtualization-root"></a><span data-ttu-id="0c773-115">Création d’une racine de virtualisation</span><span class="sxs-lookup"><span data-stu-id="0c773-115">Creating a virtualization root</span></span>

<span data-ttu-id="0c773-116">Avant qu’un fournisseur puisse démarrer l’instance de virtualisation qui projette les éléments dans le système de fichiers local, il doit créer la racine de virtualisation.</span><span class="sxs-lookup"><span data-stu-id="0c773-116">Before a provider can start up the virtualization instance that will project items into the local file system, it must create the virtualization root.</span></span>  <span data-ttu-id="0c773-117">La racine de virtualisation est le répertoire sous lequel le fournisseur projette une arborescence de répertoires et de fichiers.</span><span class="sxs-lookup"><span data-stu-id="0c773-117">The virtualization root is the directory under which the provider projects a tree of directories and files.</span></span>

<span data-ttu-id="0c773-118">Pour créer une racine de virtualisation, le fournisseur doit :</span><span class="sxs-lookup"><span data-stu-id="0c773-118">To create a virtualization root the provider must:</span></span>

1. <span data-ttu-id="0c773-119">Créez un répertoire qui servira de racine de virtualisation.</span><span class="sxs-lookup"><span data-stu-id="0c773-119">Create a directory to serve as the virtualization root.</span></span>

    <span data-ttu-id="0c773-120">Le fournisseur crée un répertoire qui servira de racine de virtualisation à l’aide de, par exemple **[CreateDirectory](/windows/desktop/api/fileapi/nf-fileapi-createdirectoryw)**:</span><span class="sxs-lookup"><span data-stu-id="0c773-120">The provider creates a directory to serve as the virtualization root using, for example **[CreateDirectory](/windows/desktop/api/fileapi/nf-fileapi-createdirectoryw)**:</span></span>

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

1. <span data-ttu-id="0c773-121">Créez un ID d’instance de virtualisation.</span><span class="sxs-lookup"><span data-stu-id="0c773-121">Create a virtualization instance ID.</span></span>

    <span data-ttu-id="0c773-122">Chaque instance de virtualisation a un ID unique appelé _ID d’instance de virtualisation_.</span><span class="sxs-lookup"><span data-stu-id="0c773-122">Every virtualization instance has a unique ID called the _virtualization instance ID_.</span></span>  <span data-ttu-id="0c773-123">Le système utilise cette valeur pour identifier l’instance de virtualisation à laquelle son contenu est associé.</span><span class="sxs-lookup"><span data-stu-id="0c773-123">The system uses this value to identify which virtualization instance its contents are associated to.</span></span>

    ```C++
    GUID instanceId;
    hr = CoCreateGuid(&instanceId);
    if (FAILED(hr))
    {
        wprintf(L"Failed to create instance ID (0x%08x)\n", hr);
        return;
    }
    ```

1. <span data-ttu-id="0c773-124">Marquez le nouveau répertoire comme racine de virtualisation.</span><span class="sxs-lookup"><span data-stu-id="0c773-124">Mark the new directory as the virtualization root.</span></span>

    <span data-ttu-id="0c773-125">Le fournisseur appelle **[PrjMarkDirectoryAsPlaceholder](/windows/desktop/api/projectedfslib/nf-projectedfslib-prjmarkdirectoryasplaceholder)** pour marquer le nouveau répertoire comme racine de virtualisation et l’assigner à l’instance de virtualisation.</span><span class="sxs-lookup"><span data-stu-id="0c773-125">The provider calls **[PrjMarkDirectoryAsPlaceholder](/windows/desktop/api/projectedfslib/nf-projectedfslib-prjmarkdirectoryasplaceholder)** to mark the new directory as the virtualization root and assign it to the virtualization instance.</span></span>

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

<span data-ttu-id="0c773-126">Le fournisseur a uniquement besoin de créer la racine de virtualisation une seule fois pour chaque instance de virtualisation.</span><span class="sxs-lookup"><span data-stu-id="0c773-126">The provider only needs to create the virtualization root once for each virtualization instance.</span></span>  <span data-ttu-id="0c773-127">Une fois la racine créée, son instance associée peut être démarrée et arrêtée à plusieurs reprises sans recréer la racine.</span><span class="sxs-lookup"><span data-stu-id="0c773-127">Once a root has been created, its associated instance can be repeatedly started and stopped without recreating the root.</span></span>

## <a name="starting-a-virtualization-instance"></a><span data-ttu-id="0c773-128">Démarrage d’une instance de virtualisation</span><span class="sxs-lookup"><span data-stu-id="0c773-128">Starting a virtualization instance</span></span>

<span data-ttu-id="0c773-129">Une fois la racine de virtualisation créée, le fournisseur doit démarrer l’instance de virtualisation.</span><span class="sxs-lookup"><span data-stu-id="0c773-129">Once the virtualization root has been created the provider must start the virtualization instance.</span></span>  <span data-ttu-id="0c773-130">Cela indique à ProjFS que le fournisseur est prêt à recevoir des rappels et à fournir des données.</span><span class="sxs-lookup"><span data-stu-id="0c773-130">This signals ProjFS that the provider is ready to receive callbacks and provide data.</span></span>

<span data-ttu-id="0c773-131">Pour démarrer l’instance de virtualisation, le fournisseur doit :</span><span class="sxs-lookup"><span data-stu-id="0c773-131">To start the virtualization instance the provider must:</span></span>

1. <span data-ttu-id="0c773-132">Configurez la table de rappel.</span><span class="sxs-lookup"><span data-stu-id="0c773-132">Set up the callback table.</span></span>

    <span data-ttu-id="0c773-133">ProjFS communique avec le fournisseur en appelant les routines de rappel implémentées par le fournisseur.</span><span class="sxs-lookup"><span data-stu-id="0c773-133">ProjFS communicates with the provider by invoking callback routines implemented by the provider.</span></span>  <span data-ttu-id="0c773-134">Le fournisseur remplit un struct [PRJ_CALLBACKS](/windows/desktop/api/projectedfslib/ns-projectedfslib-prj_callbacks) avec des pointeurs vers ses routines de rappel.</span><span class="sxs-lookup"><span data-stu-id="0c773-134">The provider populates a [PRJ_CALLBACKS](/windows/desktop/api/projectedfslib/ns-projectedfslib-prj_callbacks) struct with pointers to its callback routines.</span></span>

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

1. <span data-ttu-id="0c773-135">Démarrez l’instance de.</span><span class="sxs-lookup"><span data-stu-id="0c773-135">Start the instance.</span></span>

    <span data-ttu-id="0c773-136">Le fournisseur appelle **[PrjStartVirtualizing](/windows/desktop/api/projectedfslib/nf-projectedfslib-prjstartvirtualizing)** pour démarrer l’instance de virtualisation.</span><span class="sxs-lookup"><span data-stu-id="0c773-136">The provider calls **[PrjStartVirtualizing](/windows/desktop/api/projectedfslib/nf-projectedfslib-prjstartvirtualizing)** to start the virtualization instance.</span></span>

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
    <span data-ttu-id="0c773-137">Le paramètre _instanceHandle_ de **PrjStartVirtualizing** retourne un handle vers l’instance de virtualisation.</span><span class="sxs-lookup"><span data-stu-id="0c773-137">**PrjStartVirtualizing**'s _instanceHandle_ parameter returns a handle to the virtualization instance.</span></span>  <span data-ttu-id="0c773-138">Le fournisseur utilise ce handle lors de l’appel d’autres API ProjFS.</span><span class="sxs-lookup"><span data-stu-id="0c773-138">The provider uses this handle when calling other ProjFS APIs.</span></span>

## <a name="virtualization-instance-runtime"></a><span data-ttu-id="0c773-139">Runtime de l’instance de virtualisation</span><span class="sxs-lookup"><span data-stu-id="0c773-139">Virtualization instance runtime</span></span>

<span data-ttu-id="0c773-140">Une fois l’appel à **PrjStartVirtualizing** retourné, ProjFS appellera les routines de rappel du fournisseur en réponse aux opérations du système de fichiers dans l’instance de virtualisation.</span><span class="sxs-lookup"><span data-stu-id="0c773-140">Once the call to **PrjStartVirtualizing** returns, ProjFS will invoke the provider's callback routines in response to file system operations in the virtualization instance.</span></span>  <span data-ttu-id="0c773-141">Pour plus d’informations sur la façon dont le fournisseur peut gérer différentes opérations du système de fichiers, reportez-vous aux sections suivantes :</span><span class="sxs-lookup"><span data-stu-id="0c773-141">For information on how the provider can handle various file system operations, refer to the following sections:</span></span>

* [<span data-ttu-id="0c773-142">Énumération de fichiers et de répertoires</span><span class="sxs-lookup"><span data-stu-id="0c773-142">Enumerating Files and Directories</span></span>](enumerating-files-and-directories.md)
* [<span data-ttu-id="0c773-143">Envoi de données de fichier</span><span class="sxs-lookup"><span data-stu-id="0c773-143">Providing File Data</span></span>](providing-file-data.md)
* [<span data-ttu-id="0c773-144">Notifications d’opérations du système de fichiers</span><span class="sxs-lookup"><span data-stu-id="0c773-144">File System Operation Notifications</span></span>](file-system-operation-notifications.md)
* [<span data-ttu-id="0c773-145">Gestion des modifications d’affichage</span><span class="sxs-lookup"><span data-stu-id="0c773-145">Handling View Changes</span></span>](handling-view-changes.md)

## <a name="shutting-down-a-virtualization-instance"></a><span data-ttu-id="0c773-146">Arrêt d’une instance de virtualisation</span><span class="sxs-lookup"><span data-stu-id="0c773-146">Shutting down a virtualization instance</span></span>

<span data-ttu-id="0c773-147">Pour signaler à ProjFS que le fournisseur souhaite cesser de recevoir des rappels et fournir des données, le fournisseur doit arrêter l’instance de virtualisation.</span><span class="sxs-lookup"><span data-stu-id="0c773-147">To signal ProjFS that the provider wants to stop receiving callbacks and providing data, the provider must stop the virtualization instance.</span></span>  <span data-ttu-id="0c773-148">Pour ce faire, le fournisseur appelle **[PrjStopVirtualizing](/windows/desktop/api/projectedfslib/nf-projectedfslib-prjstopvirtualizing)**, en lui passant le handle de l’instance de virtualisation qu’il a reçue de l’appel à **PrjStartVirtualizing**.</span><span class="sxs-lookup"><span data-stu-id="0c773-148">To do this the provider calls **[PrjStopVirtualizing](/windows/desktop/api/projectedfslib/nf-projectedfslib-prjstopvirtualizing)**, passing it the handle to the virtualization instance that it received from the call to **PrjStartVirtualizing**.</span></span>

```C++
PrjStopVirtualizing(instanceHandle);
```

<span data-ttu-id="0c773-149">Notez que jusqu’à ce que cet appel retourne, ProjFS peut continuer à appeler les routines de rappel du fournisseur.</span><span class="sxs-lookup"><span data-stu-id="0c773-149">Note that until this call returns, ProjFS may continue to invoke the provider's callback routines.</span></span>