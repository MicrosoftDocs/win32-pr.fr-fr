---
description: Votre gestionnaire de filtres doit être inscrit. Vous pouvez également trouver un gestionnaire de filtres pour une extension de nom de fichier donnée par le biais du registre ou à l’aide de l’interface ILoadFilter.
ms.assetid: 3478b948-73c7-4533-974a-d9b5186a651b
title: Inscription des gestionnaires de filtres
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 18f39688bbea3bb0dd73ef28a0ba6e8b0dcf7977
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104112450"
---
# <a name="registering-filter-handlers"></a><span data-ttu-id="9faf3-104">Inscription des gestionnaires de filtres</span><span class="sxs-lookup"><span data-stu-id="9faf3-104">Registering Filter Handlers</span></span>

<span data-ttu-id="9faf3-105">Votre gestionnaire de filtres doit être inscrit.</span><span class="sxs-lookup"><span data-stu-id="9faf3-105">Your filter handler must be registered.</span></span> <span data-ttu-id="9faf3-106">Vous pouvez également trouver un gestionnaire de filtres pour une extension de nom de fichier donnée par le biais du registre ou à l’aide de l’interface [**ILoadFilter**](/windows/desktop/api/filtereg/nn-filtereg-iloadfilter) .</span><span class="sxs-lookup"><span data-stu-id="9faf3-106">You can also locate an existing filter handler for a given file name extension either through the registry or by using the [**ILoadFilter**](/windows/desktop/api/filtereg/nn-filtereg-iloadfilter) interface.</span></span>

<span data-ttu-id="9faf3-107">Cette rubrique est organisée comme suit :</span><span class="sxs-lookup"><span data-stu-id="9faf3-107">This topic is organized as follows:</span></span>

- [<span data-ttu-id="9faf3-108">Inscription des gestionnaires de filtres pour Windows Search</span><span class="sxs-lookup"><span data-stu-id="9faf3-108">Registering Filters Handlers for Windows Search</span></span>](#registering-filter-handlers)
  - [<span data-ttu-id="9faf3-109">Approche obsolète pour l’inscription des gestionnaires de filtres</span><span class="sxs-lookup"><span data-stu-id="9faf3-109">Obsolete Approach for Registering Filters Handlers</span></span>](#obsolete-approach-for-registering-filters-handlers)
- [<span data-ttu-id="9faf3-110">Remplacement de gestionnaires de filtres existants</span><span class="sxs-lookup"><span data-stu-id="9faf3-110">Replacing Existing Filter Handlers</span></span>](#replacing-existing-filter-handlers)
- [<span data-ttu-id="9faf3-111">Recherche d’un gestionnaire de filtres pour une extension de fichier donnée</span><span class="sxs-lookup"><span data-stu-id="9faf3-111">Finding a Filter Handler for a Given File Extension</span></span>](#finding-a-filter-handler-for-a-given-file-extension)
- [<span data-ttu-id="9faf3-112">Ressources supplémentaires</span><span class="sxs-lookup"><span data-stu-id="9faf3-112">Additional Resources</span></span>](#additional-resources)
- [<span data-ttu-id="9faf3-113">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="9faf3-113">Related topics</span></span>](#related-topics)

> [!NOTE]  
> <span data-ttu-id="9faf3-114">Un gestionnaire de filtres est une implémentation de l’interface [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) .</span><span class="sxs-lookup"><span data-stu-id="9faf3-114">A filter handler is an implementation of the [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) interface.</span></span>

## <a name="registering-filters-handlers-for-windows-search"></a><span data-ttu-id="9faf3-115">Inscription des gestionnaires de filtres pour Windows Search</span><span class="sxs-lookup"><span data-stu-id="9faf3-115">Registering Filters Handlers for Windows Search</span></span>

<span data-ttu-id="9faf3-116">Les GUID dont vous avez besoin pour l’inscription d’un nouveau gestionnaire de protocole ou pour rechercher un gestionnaire de protocole existant sont répertoriés dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="9faf3-116">The GUIDs you need for registering a new protocol handler or to find an existing protocol handler are listed in the following table.</span></span>

| <span data-ttu-id="9faf3-117">GUID</span><span class="sxs-lookup"><span data-stu-id="9faf3-117">GUID</span></span>                                     | <span data-ttu-id="9faf3-118">Défini par l’utilisateur ou l’application</span><span class="sxs-lookup"><span data-stu-id="9faf3-118">User or application defined</span></span> | <span data-ttu-id="9faf3-119">Description</span><span class="sxs-lookup"><span data-stu-id="9faf3-119">Description</span></span>                                                                                               |
|------------------------------------------|-----------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9faf3-120">**89BCB740-6119-101A-BCB7-00DD010655AF**</span><span class="sxs-lookup"><span data-stu-id="9faf3-120">**89BCB740-6119-101A-BCB7-00DD010655AF**</span></span> | <span data-ttu-id="9faf3-121">Application</span><span class="sxs-lookup"><span data-stu-id="9faf3-121">Application</span></span>                 | <span data-ttu-id="9faf3-122">Le GUID de l’interface [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) est une constante de clé de Registre pour tous les gestionnaires de filtres.</span><span class="sxs-lookup"><span data-stu-id="9faf3-122">The [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) interface GUID is a registry key constant for all filter handlers.</span></span> |
| <span data-ttu-id="9faf3-123">**{PersistentHandlerGUID}**</span><span class="sxs-lookup"><span data-stu-id="9faf3-123">**{PersistentHandlerGUID}**</span></span>              | <span data-ttu-id="9faf3-124">Utilisateur</span><span class="sxs-lookup"><span data-stu-id="9faf3-124">User</span></span>                        | <span data-ttu-id="9faf3-125">Il s’agit du GUID du gestionnaire persistant.</span><span class="sxs-lookup"><span data-stu-id="9faf3-125">This is the GUID for the persistent handler.</span></span>                                                              |
| <span data-ttu-id="9faf3-126">**{FilterHandlerCLSID}**</span><span class="sxs-lookup"><span data-stu-id="9faf3-126">**{FilterHandlerCLSID}**</span></span>                 | <span data-ttu-id="9faf3-127">Utilisateur</span><span class="sxs-lookup"><span data-stu-id="9faf3-127">User</span></span>                        | <span data-ttu-id="9faf3-128">Il s’agit de l’identificateur de classe (CLSID) pour le gestionnaire de filtres.</span><span class="sxs-lookup"><span data-stu-id="9faf3-128">This is the class identifier (CLSID) for the filter handler.</span></span>                                              |
| <span data-ttu-id="9faf3-129">**{ApplicationGUID}**</span><span class="sxs-lookup"><span data-stu-id="9faf3-129">**{ApplicationGUID}**</span></span>                    | <span data-ttu-id="9faf3-130">Utilisateur</span><span class="sxs-lookup"><span data-stu-id="9faf3-130">User</span></span>                        | <span data-ttu-id="9faf3-131">Il s’agit d’un GUID intermédiaire (agrégé).</span><span class="sxs-lookup"><span data-stu-id="9faf3-131">This is an intermediate (aggregated) GUID.</span></span>                                                                |

<span data-ttu-id="9faf3-132">Les gestionnaires de filtres doivent être inscrits dans HKEY \_ local \_ machine, car SearchFilterHost.exe s’exécute sous le compte système et ne peut donc pas accéder aux clés de Registre pour HKEY \_ Current \_ User pour l’utilisateur connecté.</span><span class="sxs-lookup"><span data-stu-id="9faf3-132">Filter handlers must be registered in HKEY\_LOCAL\_MACHINE because SearchFilterHost.exe is running under the SYSTEM account and therefore cannot access registry keys for HKEY\_CURRENT\_USER for the logged-on user.</span></span> <span data-ttu-id="9faf3-133">En outre, le groupe utilisateurs doit avoir un accès en lecture et en exécution au gestionnaire de filtres. dll proprement dit, car SearchFilterHost.exe supprime tous les droits d’administrateur et n’autorise que les droits non-administrateurs.</span><span class="sxs-lookup"><span data-stu-id="9faf3-133">In addition, the Users group must have read-and-execute access to the filter handler .dll itself because SearchFilterHost.exe removes all administrator rights and permits only non-administrator rights.</span></span> <span data-ttu-id="9faf3-134">Étant donné que l’emplacement de projet Visual Studio par défaut se trouve dans le répertoire de l’utilisateur actuel et n’accorde donc pas d’autorisations de lecture au groupe utilisateurs, vous devez déplacer le fichier. dll ou modifier les listes de contrôle d’accès pour autoriser l’accès SearchFilterHost.exe.</span><span class="sxs-lookup"><span data-stu-id="9faf3-134">Because the default Visual Studio project location is in the current user's directory, and so does not give read permissions to the Users group, you must either move the .dll or change the ACLs to allow SearchFilterHost.exe access.</span></span>

<span data-ttu-id="9faf3-135">Lorsque vous inscrivez un nouveau gestionnaire de filtres, nous vous recommandons d’utiliser un nom descriptif, par exemple HTML IFilter.</span><span class="sxs-lookup"><span data-stu-id="9faf3-135">When you register a new filter handler, we recommend that you use a descriptive name, for example, HTML IFilter.</span></span>

<span data-ttu-id="9faf3-136">**Pour inscrire votre nouveau gestionnaire de filtres :**</span><span class="sxs-lookup"><span data-stu-id="9faf3-136">**To register your new filter handler:**</span></span>

1. <span data-ttu-id="9faf3-137">Spécifiez l’extension et le GUID du gestionnaire persistant qui utiliseront le gestionnaire de filtres :</span><span class="sxs-lookup"><span data-stu-id="9faf3-137">Specify the extension and persistent handler GUID that will use the filter handler:</span></span>

```
    HKEY_LOCAL_MACHINE
       Software
          Classes
             .txt
                PersistentHandler
                   (Default) = {PersistentHandlerGUID}
```

```
    HKEY_LOCAL_MACHINE
       Software
          Classes
             .txt
                CLSID
                   {PersistentHandlerGUID}
                      PersistentAddinsRegistered
                         {89BCB740-6119-101A-BCB7-00DD010655AF}l
                            (Default) = {FilterHandlerCLSID}
```

2. <span data-ttu-id="9faf3-138">Inscrivez votre gestionnaire de filtres avec les clés et valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="9faf3-138">Register your filter handler with the following keys and values:</span></span>

```
    HKEY_LOCAL_MACHINE
       Software
          Classes
             .txt
                CLSID
                   {FilterHandlerCLSID}
                      (Default) = {DescriptiveFilterHandlerName}
                      InprocServer32
                         (Default) = DLL Install Path
                         ThreadingModel = Both
```

### <a name="obsolete-approach-for-registering-filters-handlers"></a><span data-ttu-id="9faf3-139">Approche obsolète pour l’inscription des gestionnaires de filtres</span><span class="sxs-lookup"><span data-stu-id="9faf3-139">Obsolete Approach for Registering Filters Handlers</span></span>

<span data-ttu-id="9faf3-140">Cette approche n’est pas recommandée pour une utilisation.</span><span class="sxs-lookup"><span data-stu-id="9faf3-140">This approach is not recommended for use.</span></span> <span data-ttu-id="9faf3-141">Les filtres peuvent être inscrits pour un CLSID qui représente une classe COM (Component Object Model) et/ou pour une extension de nom de fichier.</span><span class="sxs-lookup"><span data-stu-id="9faf3-141">Filters can be registered for a CLSID that represents a Component Object Model (COM) class, and/or for a file name extension.</span></span> <span data-ttu-id="9faf3-142">Vous pouvez inscrire les deux filtres si vous devez enregistrer un gestionnaire de filtres pour une classe et un autre gestionnaire de filtre pour une extension de nom de fichier dans la classe.</span><span class="sxs-lookup"><span data-stu-id="9faf3-142">You could register both filters if you need to register a filter handler for a class, and a different filter handler for a file name extension within the class.</span></span> <span data-ttu-id="9faf3-143">Notez qu’un gestionnaire de filtre inscrit pour une extension de nom de fichier est prioritaire sur un gestionnaire de filtre pour un CLSID.</span><span class="sxs-lookup"><span data-stu-id="9faf3-143">Note that a filter handler registered for a file name extension takes precedence over a filter handler for a CLSID.</span></span>

<span data-ttu-id="9faf3-144">Ces entrées sont des entrées de Registre OLE standard jusqu’à et y compris l’entrée de la classe **CLSID \\ {ApplicationGUID}**.</span><span class="sxs-lookup"><span data-stu-id="9faf3-144">These entries are standard OLE registry entries up to and including the entry for the class **CLSID\\{ApplicationGUID}**.</span></span> <span data-ttu-id="9faf3-145">La DLL sample.dll implémente le comportement de l’objet en cours d’exécution pour la classe. txt.</span><span class="sxs-lookup"><span data-stu-id="9faf3-145">The DLL sample.dll implements running object behavior for the .txt class.</span></span> <span data-ttu-id="9faf3-146">Notez l’entrée supplémentaire, PersistentHandler.</span><span class="sxs-lookup"><span data-stu-id="9faf3-146">Note the extra entry, PersistentHandler.</span></span> <span data-ttu-id="9faf3-147">Cette entrée spécifie la classe qui est responsable de la négociation des demandes vers les objets persistants de l’exemple de classe.</span><span class="sxs-lookup"><span data-stu-id="9faf3-147">This entry specifies the class that is responsible for brokering requests to the persistent objects of the sample class.</span></span> <span data-ttu-id="9faf3-148">L’entrée sous **PersistentAddinsRegistered** identifie l’implémentation responsable de l’interface nommée **89BCB740-6119-101A-BCB7-00DD010655AF**(IID \_ IFilter).</span><span class="sxs-lookup"><span data-stu-id="9faf3-148">The entry under **PersistentAddinsRegistered** identifies the implementation responsible for the interface named **89BCB740-6119-101A-BCB7-00DD010655AF**(IID\_IFilter).</span></span> <span data-ttu-id="9faf3-149">La classe implémentant **IID \_ IFilter** a des entrées de Registre OLE standard.</span><span class="sxs-lookup"><span data-stu-id="9faf3-149">The class implementing **IID\_IFilter** has standard OLE registry entries.</span></span> <span data-ttu-id="9faf3-150">La DLL InprocServer32 est chargée par le biais du mécanisme OLE standard.</span><span class="sxs-lookup"><span data-stu-id="9faf3-150">The InprocServer32 DLL is loaded through the standard OLE mechanism.</span></span>

<span data-ttu-id="9faf3-151">Windows Search observe le modèle de thread spécifié pour le gestionnaire de filtres.</span><span class="sxs-lookup"><span data-stu-id="9faf3-151">Windows Search observes the threading model specified for the filter handler.</span></span> <span data-ttu-id="9faf3-152">Lorsque le modèle de thread est défini sur **both**, le gestionnaire de filtres doit être thread-safe ; Sinon, si elle n’est pas thread-safe, spécifiez **Apartment**.</span><span class="sxs-lookup"><span data-stu-id="9faf3-152">When the threading model is set to **Both**, the filter handler must be thread safe; otherwise, if it is not thread safe, specify **Apartment**.</span></span> <span data-ttu-id="9faf3-153">Notez que les gestionnaires de filtres doivent toujours être thread-safe.</span><span class="sxs-lookup"><span data-stu-id="9faf3-153">Note that filter handlers should always be thread safe.</span></span>

<span data-ttu-id="9faf3-154">Les exemples d’entrées de registre suivants concernent un gestionnaire de filtres inscrit pour une classe et une extension de nom de fichier.</span><span class="sxs-lookup"><span data-stu-id="9faf3-154">The following example registry entries are for a filter handler registered for a class and file name extension.</span></span> <span data-ttu-id="9faf3-155">**{PersistentHandlerGUID}** et **{FilterHandlerCLSID}** sont utilisés comme variables indiquant les valeurs qui doivent être spécifiées par le créateur du gestionnaire de filtres.</span><span class="sxs-lookup"><span data-stu-id="9faf3-155">**{PersistentHandlerGUID}** and **{FilterHandlerCLSID}** are used as variables indicating values that need to be specified by the creator of the filter handler.</span></span> <span data-ttu-id="9faf3-156">Les valeurs sont de type REG \_ sz.</span><span class="sxs-lookup"><span data-stu-id="9faf3-156">The values are of type REG\_SZ.</span></span>

```
HKEY_LOCAL_MACHINE
   Software
      Classes
         .txt
            (Default) = SampleFile
         SampleFile
            (Default) = Class for Sample Files
            CLSID
               (Default) = {ApplicationGUID}
         CLSID
            {ApplicationGUID}
               (Default) = Sample Files
               InprocServer32
                  (Default) = sample.dll
               PersistentHandler
                  (Default) = {PersistentHandlerGUID}
            {PersistentHandlerGUID}
               (Default) = Sample file persistent handler
               PersistentAddinsRegistered
                  {89BCB740-6119-101A-BCB7-00DD010655AF}l
                     (Default) = {FilterHandlerCLSID}
            {FilterHandlerCLSID}
               (Default) = Sample Files
               InprocServer32
                  (Default) = sampfilt.dll
                  ThreadingModel = Both
```

## <a name="replacing-existing-filter-handlers"></a><span data-ttu-id="9faf3-157">Remplacement de gestionnaires de filtres existants</span><span class="sxs-lookup"><span data-stu-id="9faf3-157">Replacing Existing Filter Handlers</span></span>

<span data-ttu-id="9faf3-158">Nous vous recommandons de ne pas remplacer les gestionnaires de filtres intégrés pour les types de fichiers courants tels que. txt,. doc,. html,. URL, et ainsi de suite, car cela peut avoir des effets indésirables sur d’autres composants système.</span><span class="sxs-lookup"><span data-stu-id="9faf3-158">We recommend that you do not replace the built-in filter handlers for common file types such as .txt, .doc, .html, .url, and so forth, because doing so can have undesired effects on other system components.</span></span> <span data-ttu-id="9faf3-159">L’indexation des corps des messages électroniques dépend des gestionnaires de filtres. txt,. html et. rtf, par exemple.</span><span class="sxs-lookup"><span data-stu-id="9faf3-159">Indexing email message bodies depends on the .txt, .html, and .rtf filter handlers, for example.</span></span>

<span data-ttu-id="9faf3-160">Si un nouveau gestionnaire de filtres pour un type de fichier est en cours d’installation en remplacement d’une inscription de filtre existante, le programme d’installation doit enregistrer l’inscription actuelle et la restaurer si le nouveau gestionnaire de filtres est désinstallé.</span><span class="sxs-lookup"><span data-stu-id="9faf3-160">If a new filter handler for a file type is being installed as a replacement for an existing filter registration, the installer should save the current registration and restore it if the new filter handler is uninstalled.</span></span> <span data-ttu-id="9faf3-161">Il n’existe aucun mécanisme pour la chaîne de filtres.</span><span class="sxs-lookup"><span data-stu-id="9faf3-161">There is no mechanism to chain filters.</span></span> <span data-ttu-id="9faf3-162">Par conséquent, le nouveau gestionnaire de filtres est chargé de répliquer toutes les fonctionnalités nécessaires de l’ancien filtre.</span><span class="sxs-lookup"><span data-stu-id="9faf3-162">Hence, the new filter handler is responsible for replicating any necessary functionality of the old filter.</span></span>

## <a name="finding-a-filter-handler-for-a-given-file-extension"></a><span data-ttu-id="9faf3-163">Recherche d’un gestionnaire de filtres pour une extension de fichier donnée</span><span class="sxs-lookup"><span data-stu-id="9faf3-163">Finding a Filter Handler for a Given File Extension</span></span>

<span data-ttu-id="9faf3-164">Vous pouvez utiliser l’interface [**ILoadFilter**](/windows/desktop/api/filtereg/nn-filtereg-iloadfilter) pour rechercher un gestionnaire de filtres pour une extension de nom de fichier donnée.</span><span class="sxs-lookup"><span data-stu-id="9faf3-164">You can use the [**ILoadFilter**](/windows/desktop/api/filtereg/nn-filtereg-iloadfilter) interface to find a filter handler for a given file name extension.</span></span> <span data-ttu-id="9faf3-165">Les exemples d’entrées de registre suivants montrent comment procéder pour les fichiers HTML.</span><span class="sxs-lookup"><span data-stu-id="9faf3-165">The following example registry entries illustrate how to do so for HTML files.</span></span> <span data-ttu-id="9faf3-166">Dans cet exemple, le gestionnaire de filtres pour les documents HTML est nlhtml.dll.</span><span class="sxs-lookup"><span data-stu-id="9faf3-166">In this example, the filter handler for HTML documents is nlhtml.dll.</span></span> <span data-ttu-id="9faf3-167">Les valeurs sont de type REG \_ sz.</span><span class="sxs-lookup"><span data-stu-id="9faf3-167">The values are of type REG\_SZ.</span></span>

<span data-ttu-id="9faf3-168">**Pour rechercher le gestionnaire de filtres pour une extension de nom de fichier donnée :**</span><span class="sxs-lookup"><span data-stu-id="9faf3-168">**To find the filter handler for a given file name extension:**</span></span>

1. <span data-ttu-id="9faf3-169">Vérifiez si l’extension pour le type de fichiers filtrés a un gestionnaire persistant inscrit sous l’entrée de Registre \\ HKEY \_ local \_ machine \\ Software \\ classes. extension.</span><span class="sxs-lookup"><span data-stu-id="9faf3-169">Check whether the extension for the type of files that are filtered has a persistent handler registered under the registry entry \\HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Classes.extension.</span></span> <span data-ttu-id="9faf3-170">Si c’est le cas, laissez cette clé être {PersistentHandlerGUID}.</span><span class="sxs-lookup"><span data-stu-id="9faf3-170">If so, let this key be {PersistentHandlerGUID}.</span></span>

```
    HKEY_LOCAL_MACHINE
       SOFTWARE
          Classes
             .htm
                PersistentHandler
                   {PersistentHandlerGUID}
```

2. <span data-ttu-id="9faf3-171">Si aucun gestionnaire persistant n’est inscrit pour l’extension, recherchez le CLSID associé au type de document sous l’entrée de Registre \\ HKEY \_ local \_ machine \\ Software \\ classes.</span><span class="sxs-lookup"><span data-stu-id="9faf3-171">If there is not a persistent handler registered for the extension, find the CLSID associated with the document type under the registry entry \\HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Classes.</span></span> <span data-ttu-id="9faf3-172">Laissez cette clé être {ApplicationGUID}.</span><span class="sxs-lookup"><span data-stu-id="9faf3-172">Let this key be {ApplicationGUID}.</span></span> <span data-ttu-id="9faf3-173">Déterminez ensuite si un gestionnaire persistant est inscrit pour le CLSID : à l’aide de {ApplicationGUID}, localisez le gestionnaire persistant pour l' \\ entrée HKEY de l' \_ ordinateur local de l' \_ \\ \\ \\ identificateur CLSID \\ {ApplicationGUID}.</span><span class="sxs-lookup"><span data-stu-id="9faf3-173">Then determine whether a persistent handler is registered for the CLSID: using {ApplicationGUID} locate the persistent handler for the \\HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Classes\\CLSID\\{ApplicationGUID} entry.</span></span> <span data-ttu-id="9faf3-174">Laissez cette clé être {PersistentHandlerGUID}.</span><span class="sxs-lookup"><span data-stu-id="9faf3-174">Let this key be {PersistentHandlerGUID}.</span></span>

```
    HKEY_LOCAL_MACHINE
       SOFTWARE
          Classes
             htmlfile
                (Default) = Class for WWW HTML files
                CLSID
                   (Default) = {25336920-03F9-11CF-8FD0-00AA00686F13}
             CLSID
                {25336920-03F9-11CF-8FD0-00AA00686F13}
                   PersistentHandler
                      (Default) = {PersistentHandlerGUID}
```

3. <span data-ttu-id="9faf3-175">Déterminez le GUID du gestionnaire persistant : à l’aide de {PersistentHandlerGUID}, recherchez le GUID du gestionnaire persistant pour le type de document.</span><span class="sxs-lookup"><span data-stu-id="9faf3-175">Determine the GUID of the persistent handler: using {PersistentHandlerGUID} find the persistent handler GUID for the document type.</span></span> <span data-ttu-id="9faf3-176">La valeur sous l’entrée de Registre HKEY \_ local \_ machine \\ Software \\ classes \\ CLSID \\ {PERSISTENTHANDLERGUID} \\ PersistentAddinsRegistered \\ 89BCB740-6119-101A-BCB7-00DD010655AF génère le GUID du gestionnaire persistant pour ce type de document.</span><span class="sxs-lookup"><span data-stu-id="9faf3-176">The value under the registry entry HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Classes\\CLSID\\{PersistentHandlerGUID}\\PersistentAddinsRegistered\\ 89BCB740-6119-101A-BCB7-00DD010655AF yields the persistent handler GUID for this document type.</span></span> <span data-ttu-id="9faf3-177">Laissez cette clé être {FilterHandlerCLSID}.</span><span class="sxs-lookup"><span data-stu-id="9faf3-177">Let this key be {FilterHandlerCLSID}.</span></span>

```
    HKEY_LOCAL_MACHINE
       SOFTWARE
          Classes
             {PersistentHandlerGUID}
                (Default) = HTML File Persistent Handler<dl>
                    REG_SZ     {89BCB740-6119-101A-BCB7-00DD010655AF}
                    REG_SZ     (Default) = {EEC97550-47A9-11CF-B952-00AA0051FE20}
```

4. <span data-ttu-id="9faf3-178">Déterminez le gestionnaire de filtres : à l’aide de {FilterHandlerCLSID} qui a été déterminé à l’étape précédente, recherchez le gestionnaire de filtre sous l’entrée \\ HKEY \_ local \_ machine \\ Software \\ classes \\ CLSID \\ {FilterHandlerCLSID} \\ InprocServer32.</span><span class="sxs-lookup"><span data-stu-id="9faf3-178">Determine the filter handler: using {FilterHandlerCLSID} that was determined in the previous step locate the filter handler under the entry \\HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Classes\\CLSID\\{FilterHandlerCLSID}\\InprocServer32.</span></span> <span data-ttu-id="9faf3-179">Dans cet exemple, le nom du gestionnaire de filtres descriptifs utilisé est HTML IFilter.</span><span class="sxs-lookup"><span data-stu-id="9faf3-179">In this example the descriptive filter handler name used is HTML IFilter.</span></span>

```
    HKEY_LOCAL_MACHINE
       SOFTWARE
          Classes
             CLSID
                {EEC97550-47A9-11CF-B952-00AA0051FE20}
                   (Default) = HTML IFilter
                    Data type  REG_SZ
                    InprocServer32
                    nlhtml.dll
```

## <a name="additional-resources"></a><span data-ttu-id="9faf3-180">Ressources supplémentaires</span><span class="sxs-lookup"><span data-stu-id="9faf3-180">Additional Resources</span></span>

- <span data-ttu-id="9faf3-181">L’exemple de code [IFilterSample](-search-sample-ifiltersample.md) , disponible sur [GitHub](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/WindowsSearch/IFilterSample), montre comment créer une classe de base [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) pour l’implémentation de l’interface **IFilter** .</span><span class="sxs-lookup"><span data-stu-id="9faf3-181">The [IFilterSample](-search-sample-ifiltersample.md) code sample, available on [GitHub](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/WindowsSearch/IFilterSample), demonstrates how to create an [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) base class for implementing the **IFilter** interface.</span></span>
- <span data-ttu-id="9faf3-182">Pour obtenir une vue d’ensemble du processus d’indexation, consultez [processus d’indexation](-search-indexing-process-overview.md).</span><span class="sxs-lookup"><span data-stu-id="9faf3-182">For an overview of the indexing process, see [The Indexing Process](-search-indexing-process-overview.md).</span></span>
- <span data-ttu-id="9faf3-183">Pour obtenir une vue d’ensemble des types de fichiers, consultez [types de fichiers](../shell/fa-file-types.md).</span><span class="sxs-lookup"><span data-stu-id="9faf3-183">For an overview of file types, see [File Types](../shell/fa-file-types.md).</span></span>
- <span data-ttu-id="9faf3-184">Pour interroger des attributs d’association de fichiers pour un type de fichier, consultez [PerceivedTypes, SystemFileAssociations et inscription d’application](/previous-versions/windows/desktop/legacy/cc144150(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="9faf3-184">To query file association attributes for a file type, see [PerceivedTypes, SystemFileAssociations, and Application Registration](/previous-versions/windows/desktop/legacy/cc144150(v=vs.85)).</span></span>

## <a name="related-topics"></a><span data-ttu-id="9faf3-185">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="9faf3-185">Related topics</span></span>

[<span data-ttu-id="9faf3-186">Développement de gestionnaires de filtres</span><span class="sxs-lookup"><span data-stu-id="9faf3-186">Developing Filter Handlers</span></span>](-search-ifilter-conceptual.md)

[<span data-ttu-id="9faf3-187">À propos des gestionnaires de filtres dans Windows Search</span><span class="sxs-lookup"><span data-stu-id="9faf3-187">About Filter Handlers in Windows Search</span></span>](-search-ifilter-about.md)

[<span data-ttu-id="9faf3-188">Meilleures pratiques pour la création de gestionnaires de filtres dans Windows Search</span><span class="sxs-lookup"><span data-stu-id="9faf3-188">Best Practices for Creating Filter Handlers in Windows Search</span></span>](-search-3x-wds-extidx-filters.md)

[<span data-ttu-id="9faf3-189">Retour des propriétés d’un gestionnaire de filtres</span><span class="sxs-lookup"><span data-stu-id="9faf3-189">Returning Properties from a Filter Handler</span></span>](-search-ifilter-property-filtering.md)

[<span data-ttu-id="9faf3-190">Gestionnaires de filtres fournis avec Windows</span><span class="sxs-lookup"><span data-stu-id="9faf3-190">Filter Handlers that Ship with Windows</span></span>](-search-ifilter-implementations.md)

[<span data-ttu-id="9faf3-191">Implémentation de gestionnaires de filtres dans Windows Search</span><span class="sxs-lookup"><span data-stu-id="9faf3-191">Implementing Filter Handlers in Windows Search</span></span>](-search-ifilter-constructing-filters.md)

[<span data-ttu-id="9faf3-192">Test des gestionnaires de filtres</span><span class="sxs-lookup"><span data-stu-id="9faf3-192">Testing Filter Handlers</span></span>](-search-ifilter-testing-filters.md)
