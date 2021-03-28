---
description: Page de glossaire
ROBOTS: NOINDEX, NOFOLLOW
title: Glossaire de l’interpréteur de commandes
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 2F463941-A4BA-4b34-B391-7E599E87BEEA
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: e6ec49f808f6c6dea74d3c8c2ac4408bc5d1a26e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104319134"
---
# <a name="shell-glossary"></a><span data-ttu-id="fd161-103">Glossaire de l’interpréteur de commandes</span><span class="sxs-lookup"><span data-stu-id="fd161-103">Shell Glossary</span></span>

## <a name="a"></a><span data-ttu-id="fd161-104">Un</span><span class="sxs-lookup"><span data-stu-id="fd161-104">A</span></span>

<dl> <dt>

<span data-ttu-id="fd161-105">**Association**</span><span class="sxs-lookup"><span data-stu-id="fd161-105">**association**</span></span>
</dt> <dd>

<span data-ttu-id="fd161-106">Mappage d’une extension de nom de fichier (par exemple,. mp3) ou d’un protocole (par exemple, http) à un identificateur programmatique (ProgID).</span><span class="sxs-lookup"><span data-stu-id="fd161-106">A mapping of a file name extension (for example, .mp3) or protocol (for example, http) to a programmatic identifier (ProgID).</span></span> <span data-ttu-id="fd161-107">Ce mappage est stocké dans le Registre sous la forme d’un paramètre par utilisateur avec une solution de secours pour chaque ordinateur.</span><span class="sxs-lookup"><span data-stu-id="fd161-107">This mapping is stored in the registry as a per-user setting with a per-computer fallback.</span></span> <span data-ttu-id="fd161-108">Les applications qui participent au système de programmes par défaut définissent le mappage d’association pour l’extension de nom de fichier ou le protocole de manière à pointer vers les clés ProgID dont ils sont propriétaires.</span><span class="sxs-lookup"><span data-stu-id="fd161-108">Applications that participate in the Default Programs system set the association mapping for the file name extension or protocol to point to the ProgID keys that they own.</span></span>

</dd> <dt>

<span data-ttu-id="fd161-109">**Tableau d’association**</span><span class="sxs-lookup"><span data-stu-id="fd161-109">**association array**</span></span>
</dt> <dd>

<span data-ttu-id="fd161-110">Liste ordonnée d’emplacements du Registre utilisée pour stocker des informations sur un type d’élément, y compris les gestionnaires, les verbes et d’autres attributs, tels que l’icône et le nom d’affichage du type.</span><span class="sxs-lookup"><span data-stu-id="fd161-110">An ordered list of registry locations used to store information about an item type, including handlers, verbs, and other attributes like the icon and display name of the type.</span></span> <span data-ttu-id="fd161-111">Par exemple, un fichier. jpg possède le tableau d’association suivant sur un système Windows par défaut : « HKCR \\ jpgfile », « HKCR \\ SystemFileAssociations \\ . jpg », « HKCR \\ SystemFileAssociations \\ image », « HKCR \\ \* », « HKCR \\ AllFileSystemObjects ».</span><span class="sxs-lookup"><span data-stu-id="fd161-111">For example, a .jpg file has the following association array on a default Windows system: "HKCR\\jpgfile", "HKCR\\SystemFileAssociations\\.jpg", "HKCR\\SystemFileAssociations\\image", "HKCR\\\*", "HKCR\\AllFileSystemObjects".</span></span>

</dd> </dl>

## <a name="b"></a><span data-ttu-id="fd161-112">B</span><span class="sxs-lookup"><span data-stu-id="fd161-112">B</span></span>

<dl> <dt>

<span data-ttu-id="fd161-113">**bind**</span><span class="sxs-lookup"><span data-stu-id="fd161-113">**bind**</span></span>
</dt> <dd>

<span data-ttu-id="fd161-114">Pour charger ou associer du code à des données.</span><span class="sxs-lookup"><span data-stu-id="fd161-114">To load or associate code with data.</span></span> <span data-ttu-id="fd161-115">Par exemple, un gestionnaire peut être associé à une source de données Shell.</span><span class="sxs-lookup"><span data-stu-id="fd161-115">For example, a handler may be associated with a Shell data source.</span></span>

</dd> </dl>

## <a name="c"></a><span data-ttu-id="fd161-116">C</span><span class="sxs-lookup"><span data-stu-id="fd161-116">C</span></span>

<dl> <dt>

<span data-ttu-id="fd161-117">**nom canonique**</span><span class="sxs-lookup"><span data-stu-id="fd161-117">**canonical name**</span></span>
</dt> <dd>

<span data-ttu-id="fd161-118">Nom unique d’une ressource.</span><span class="sxs-lookup"><span data-stu-id="fd161-118">The unique name of a resource.</span></span> <span data-ttu-id="fd161-119">Canonique signifie « selon les règles ».</span><span class="sxs-lookup"><span data-stu-id="fd161-119">Canonical means "according to the rules."</span></span> <span data-ttu-id="fd161-120">Voir aussi : nom de verbe canonique.</span><span class="sxs-lookup"><span data-stu-id="fd161-120">See also: canonical verb name.</span></span>

</dd> <dt>

<span data-ttu-id="fd161-121">**nom de verbe canonique**</span><span class="sxs-lookup"><span data-stu-id="fd161-121">**canonical verb name**</span></span>
</dt> <dd>

<span data-ttu-id="fd161-122">Nom indépendant du langage qui peut être utilisé par programme pour faire référence à un verbe, quelle que soit la chaîne localisée dans l’interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="fd161-122">A language-neutral name that can be used programmatically to refer to a verb, regardless of the localized string in the user interface.</span></span> <span data-ttu-id="fd161-123">Voir aussi : nom canonique, verbe.</span><span class="sxs-lookup"><span data-stu-id="fd161-123">See also: canonical name, verb.</span></span>

</dd> <dt>

<span data-ttu-id="fd161-124">**container**</span><span class="sxs-lookup"><span data-stu-id="fd161-124">**container**</span></span>
</dt> <dd>

<span data-ttu-id="fd161-125">Type d’élément de Shell qui peut contenir d’autres éléments.</span><span class="sxs-lookup"><span data-stu-id="fd161-125">A type of Shell item that can contain other items.</span></span> <span data-ttu-id="fd161-126">Les éléments d’un conteneur sont exposés à l’espace de noms Shell à l’aide d’une source de données Shell.</span><span class="sxs-lookup"><span data-stu-id="fd161-126">Items in a container are exposed to the Shell namespace by using a Shell data source.</span></span> <span data-ttu-id="fd161-127">Les exemples incluent les dossiers, les lecteurs, les serveurs réseau et les fichiers compressés avec une extension de nom de fichier. zip.</span><span class="sxs-lookup"><span data-stu-id="fd161-127">Examples include folders, drives, network servers, and compressed files with a .zip file name extension.</span></span> <span data-ttu-id="fd161-128">Voir aussi : source de données Shell, dossier, élément Shell.</span><span class="sxs-lookup"><span data-stu-id="fd161-128">See also: Shell data source, folder, Shell item.</span></span>

</dd> <dt>

<span data-ttu-id="fd161-129">**content**</span><span class="sxs-lookup"><span data-stu-id="fd161-129">**content**</span></span>
</dt> <dd>

<span data-ttu-id="fd161-130">Texte et propriétés associés à un élément de Shell ou à une source de contenu qui peut être indexée.</span><span class="sxs-lookup"><span data-stu-id="fd161-130">Text and properties associated with a Shell item or a content source that can be indexed.</span></span>

</dd> <dt>

<span data-ttu-id="fd161-131">**source du contenu**</span><span class="sxs-lookup"><span data-stu-id="fd161-131">**content source**</span></span>
</dt> <dd>

<span data-ttu-id="fd161-132">Élément auquel l’indexeur peut accéder.</span><span class="sxs-lookup"><span data-stu-id="fd161-132">An item that can be accessed by the indexer.</span></span> <span data-ttu-id="fd161-133">Les sources de contenu sont adressables par une URL et sont fournies à l’indexeur par un gestionnaire de protocole.</span><span class="sxs-lookup"><span data-stu-id="fd161-133">Content sources are addressable by a URL and are provided to the indexer by a protocol handler.</span></span> <span data-ttu-id="fd161-134">Voici quelques exemples : fichiers et dossiers du système de fichiers, éléments et dossiers Microsoft Outlook, enregistrements de base de données et éléments stockés dans Microsoft SharePoint.</span><span class="sxs-lookup"><span data-stu-id="fd161-134">Examples include: file system files and folders, Microsoft Outlook items and folders, database records, and Microsoft SharePoint stored items.</span></span> <span data-ttu-id="fd161-135">Une source de contenu peut être exposée en tant qu’élément de Shell en implémentant une source de données Shell.</span><span class="sxs-lookup"><span data-stu-id="fd161-135">A content source can be exposed as Shell items by implementing a Shell data source.</span></span> <span data-ttu-id="fd161-136">Voir aussi : contenu, élément de Shell.</span><span class="sxs-lookup"><span data-stu-id="fd161-136">See also: content, Shell item.</span></span>

</dd> <dt>

<span data-ttu-id="fd161-137">**content view (affichage du contenu)**</span><span class="sxs-lookup"><span data-stu-id="fd161-137">**content view**</span></span>
</dt> <dd>

<span data-ttu-id="fd161-138">Vue dans l’Explorateur Windows (proposée dans Windows 7 et versions ultérieures) qui affiche le contenu le plus pertinent pour chaque élément de la liste en fonction de son extension de nom de fichier ou de son association de type.</span><span class="sxs-lookup"><span data-stu-id="fd161-138">A view in Windows Explorer (offered in Windows 7 and later) that displays the most relevant content for each item in the list based on its file name extension or Kind association.</span></span> <span data-ttu-id="fd161-139">L’affichage du contenu utilise une logique de redimensionnement qui supprime des propriétés lorsque la taille de la fenêtre diminue pour s’assurer que les propriétés les plus critiques disposent toujours de suffisamment de place pour être clairement lisibles.</span><span class="sxs-lookup"><span data-stu-id="fd161-139">Content view uses a resizing logic that drops properties when the window size decreases to ensure that the most critical properties still have room to be clearly readable.</span></span> <span data-ttu-id="fd161-140">Voir aussi : modèle de disposition, genre, Association de genres.</span><span class="sxs-lookup"><span data-stu-id="fd161-140">See also: layout pattern, Kind, Kind association.</span></span>

</dd> <dt>

<span data-ttu-id="fd161-141">**mode d’affichage du contenu**</span><span class="sxs-lookup"><span data-stu-id="fd161-141">**content view mode**</span></span>
</dt> <dd>

<span data-ttu-id="fd161-142">Consultez la définition de : vue de contenu.</span><span class="sxs-lookup"><span data-stu-id="fd161-142">See definition for: content view.</span></span>

</dd> <dt>

<span data-ttu-id="fd161-143">**menu contextuel**</span><span class="sxs-lookup"><span data-stu-id="fd161-143">**context menu**</span></span>
</dt> <dd>

<span data-ttu-id="fd161-144">Ce terme est parfois utilisé pour signifier le menu contextuel.</span><span class="sxs-lookup"><span data-stu-id="fd161-144">This term is sometimes used to mean shortcut menu.</span></span> <span data-ttu-id="fd161-145">Consultez la définition de : menu contextuel.</span><span class="sxs-lookup"><span data-stu-id="fd161-145">See definition for: shortcut menu.</span></span>

</dd> <dt>

<span data-ttu-id="fd161-146">**Gestionnaire de menu contextuel**</span><span class="sxs-lookup"><span data-stu-id="fd161-146">**context menu handler**</span></span>
</dt> <dd>

<span data-ttu-id="fd161-147">Ce terme est parfois utilisé pour signifier le gestionnaire de menu contextuel.</span><span class="sxs-lookup"><span data-stu-id="fd161-147">This term is sometimes used to mean shortcut menu handler.</span></span> <span data-ttu-id="fd161-148">Consultez la définition de : gestionnaire de menu contextuel.</span><span class="sxs-lookup"><span data-stu-id="fd161-148">See definition for: shortcut menu handler.</span></span>

</dd> </dl>

## <a name="d"></a><span data-ttu-id="fd161-149">D</span><span class="sxs-lookup"><span data-stu-id="fd161-149">D</span></span>

<dl> <dt>

<span data-ttu-id="fd161-150">**gestionnaire d’objets de données**</span><span class="sxs-lookup"><span data-stu-id="fd161-150">**data object handler**</span></span>
</dt> <dd>

<span data-ttu-id="fd161-151">Gestionnaire qui fournit des formats de presse-papiers supplémentaires pour l’objet de données (IDataObject) d’un élément.</span><span class="sxs-lookup"><span data-stu-id="fd161-151">A handler that provides additional clipboard formats for the data object (IDataObject) of an item.</span></span> <span data-ttu-id="fd161-152">Les objets de données sont utilisés dans les scénarios de glisser-déplacer et de copier/coller.</span><span class="sxs-lookup"><span data-stu-id="fd161-152">Data objects are used in drag-and-drop and copy/paste scenarios.</span></span>

</dd> <dt>

<span data-ttu-id="fd161-153">**source de données**</span><span class="sxs-lookup"><span data-stu-id="fd161-153">**data source**</span></span>
</dt> <dd>

<span data-ttu-id="fd161-154">Ce terme est parfois utilisé pour signifier le magasin de données ou la source de données Shell.</span><span class="sxs-lookup"><span data-stu-id="fd161-154">This term is sometimes used to mean data store or Shell data source.</span></span> <span data-ttu-id="fd161-155">Consultez la définition de : magasin de données, source de données Shell.</span><span class="sxs-lookup"><span data-stu-id="fd161-155">See definition for: data store, Shell data source.</span></span>

</dd> <dt>

<span data-ttu-id="fd161-156">**magasin de données**</span><span class="sxs-lookup"><span data-stu-id="fd161-156">**data store**</span></span>
</dt> <dd>

<span data-ttu-id="fd161-157">Référentiel de données.</span><span class="sxs-lookup"><span data-stu-id="fd161-157">A repository of data.</span></span> <span data-ttu-id="fd161-158">Un magasin de données peut être exposé au modèle de programmation de l’interpréteur de commandes en tant que conteneur à l’aide d’une source de données Shell.</span><span class="sxs-lookup"><span data-stu-id="fd161-158">A data store can be exposed to the Shell programming model as a container using a Shell data source.</span></span> <span data-ttu-id="fd161-159">Les éléments d’un magasin de données peuvent être indexés par le système de recherche Windows à l’aide d’un gestionnaire de protocole.</span><span class="sxs-lookup"><span data-stu-id="fd161-159">The items in a data store can be indexed by the Windows Search system using a protocol handler.</span></span>

</dd> <dt>

<span data-ttu-id="fd161-160">**composition du Bureau**</span><span class="sxs-lookup"><span data-stu-id="fd161-160">**desktop composition**</span></span>
</dt> <dd>

<span data-ttu-id="fd161-161">Fonctionnalité Windows Vista qui permet aux fenêtres individuelles d’être dessinées sur des surfaces hors écran dans la mémoire vidéo au lieu d’être directement dessinées sur le périphérique d’affichage principal.</span><span class="sxs-lookup"><span data-stu-id="fd161-161">A Windows Vista feature that enables individual windows to be drawn to off-screen surfaces in video memory instead of the being drawn directly to the primary display device.</span></span>

</dd> <dt>

<span data-ttu-id="fd161-162">**document**</span><span class="sxs-lookup"><span data-stu-id="fd161-162">**document**</span></span>
</dt> <dd>

<span data-ttu-id="fd161-163">Élément de Shell qui contient du texte et pour lequel l’interface IFilter peut être implémentée.</span><span class="sxs-lookup"><span data-stu-id="fd161-163">A Shell item that contains text, and for which the IFilter interface could be implemented.</span></span>

</dd> <dt>

<span data-ttu-id="fd161-164">**supprimer le gestionnaire**</span><span class="sxs-lookup"><span data-stu-id="fd161-164">**drop handler**</span></span>
</dt> <dd>

<span data-ttu-id="fd161-165">Gestionnaire qui permet à un type d’élément particulier de prendre en charge les scénarios de glisser-déplacer et de copier/coller.</span><span class="sxs-lookup"><span data-stu-id="fd161-165">A handler that enables a particular item type to support drag-and-drop and copy/paste scenarios.</span></span>

</dd> <dt>

<span data-ttu-id="fd161-166">**déplacer la cible**</span><span class="sxs-lookup"><span data-stu-id="fd161-166">**drop target**</span></span>
</dt> <dd>

<span data-ttu-id="fd161-167">Objet de données qui est glissé et déposé dans un fichier.</span><span class="sxs-lookup"><span data-stu-id="fd161-167">A data object that is dragged and dropped onto a file.</span></span> <span data-ttu-id="fd161-168">Voir aussi : gestionnaire de données, Drop handler.</span><span class="sxs-lookup"><span data-stu-id="fd161-168">See also: data handler, drop handler.</span></span>

</dd> <dt>

<span data-ttu-id="fd161-169">**verbe dynamique**</span><span class="sxs-lookup"><span data-stu-id="fd161-169">**dynamic verb**</span></span>
</dt> <dd>

<span data-ttu-id="fd161-170">Verbe qui dépend de l’état d’un élément de Shell ou du système ; l’apparence de l’élément est basée sur l’État et requiert que le code en cours d’exécution détermine si l’élément doit apparaître.</span><span class="sxs-lookup"><span data-stu-id="fd161-170">A verb that depends on the state of a Shell item or of the system; the appearance of the item is state based and requires that the executing code determine whether the item should appear.</span></span> <span data-ttu-id="fd161-171">Voir aussi : gestionnaire de menu contextuel, verbe statique, verbe.</span><span class="sxs-lookup"><span data-stu-id="fd161-171">See also: shortcut menu handler, static verb, verb.</span></span>

</dd> </dl>

## <a name="e"></a><span data-ttu-id="fd161-172">E</span><span class="sxs-lookup"><span data-stu-id="fd161-172">E</span></span>

<dl> <dt>

<span data-ttu-id="fd161-173">**Commande Explorer**</span><span class="sxs-lookup"><span data-stu-id="fd161-173">**Explorer command**</span></span>
</dt> <dd>

<span data-ttu-id="fd161-174">Objet qui peut être présenté sous la forme d’un bouton près du haut de la fenêtre de l’Explorateur Windows qui fournit des fonctionnalités pour les éléments et les conteneurs de cette fenêtre.</span><span class="sxs-lookup"><span data-stu-id="fd161-174">An object that can be presented as a button near the top of the Windows Explorer window that provides functionality for items and containers in that window.</span></span> <span data-ttu-id="fd161-175">Une source de données Shell fournit les objets de commande de l’Explorateur Windows pour un élément de conteneur particulier.</span><span class="sxs-lookup"><span data-stu-id="fd161-175">A Shell data source provides the Windows Explorer command objects for a particular container item.</span></span> <span data-ttu-id="fd161-176">Les commandes sont parfois utilisées comme verbes.</span><span class="sxs-lookup"><span data-stu-id="fd161-176">Commands are sometimes used as verbs.</span></span>

</dd> </dl>

## <a name="f"></a><span data-ttu-id="fd161-177">F</span><span class="sxs-lookup"><span data-stu-id="fd161-177">F</span></span>

<dl> <dt>

<span data-ttu-id="fd161-178">**Association de fichiers**</span><span class="sxs-lookup"><span data-stu-id="fd161-178">**file association**</span></span>
</dt> <dd>

<span data-ttu-id="fd161-179">Consultez la définition de : Association de types de fichiers.</span><span class="sxs-lookup"><span data-stu-id="fd161-179">See definition for: file type association.</span></span>

</dd> <dt>

<span data-ttu-id="fd161-180">**format de fichier**</span><span class="sxs-lookup"><span data-stu-id="fd161-180">**file format**</span></span>
</dt> <dd>

<span data-ttu-id="fd161-181">Format des données stockées dans un fichier dont la spécification de format est documentée.</span><span class="sxs-lookup"><span data-stu-id="fd161-181">A format for data stored in a file that has a documented format specification.</span></span> <span data-ttu-id="fd161-182">Les exemples incluent OLE DocFile, OPC, XML, ZIP et d’autres spécifications de format de fichier connues.</span><span class="sxs-lookup"><span data-stu-id="fd161-182">Examples include OLE DocFile, OPC, XML, ZIP and other well known file format specifications.</span></span> <span data-ttu-id="fd161-183">Les créateurs de type de fichier utilisent généralement un format de fichier existant comme base d’un nouveau type de fichier.</span><span class="sxs-lookup"><span data-stu-id="fd161-183">File type creators generally use an existing file format as the basis of a new file type.</span></span> <span data-ttu-id="fd161-184">Un format de fichier peut être simplement une définition qui n’est pas instanciée en tant que type de fichier.</span><span class="sxs-lookup"><span data-stu-id="fd161-184">A file format can be simply a definition that is not instantiated as a file type.</span></span>

</dd> <dt>

<span data-ttu-id="fd161-185">**Gestionnaire de format de fichier**</span><span class="sxs-lookup"><span data-stu-id="fd161-185">**file format handler**</span></span>
</dt> <dd>

<span data-ttu-id="fd161-186">Ce terme est un synonyme du gestionnaire de type de fichier.</span><span class="sxs-lookup"><span data-stu-id="fd161-186">This term is a synonym for file type handler.</span></span> <span data-ttu-id="fd161-187">Consultez la définition de : gestionnaire de type de fichier.</span><span class="sxs-lookup"><span data-stu-id="fd161-187">See definition for: file type handler.</span></span>

</dd> <dt>

<span data-ttu-id="fd161-188">**extension de nom de fichier**</span><span class="sxs-lookup"><span data-stu-id="fd161-188">**file name extension**</span></span>
</dt> <dd>

<span data-ttu-id="fd161-189">Indicateur principal d’un type de fichier pour les éléments du système de fichiers. il s’agit de la partie du nom de fichier qui suit le point final.</span><span class="sxs-lookup"><span data-stu-id="fd161-189">The primary indicator of a file type for file system items, it is the portion of the file name that follows the final dot.</span></span> <span data-ttu-id="fd161-190">L’extension de nom de fichier ne peut pas contenir d’espaces ou de caractères non ASCII et s’applique uniquement aux fichiers (et non aux dossiers).</span><span class="sxs-lookup"><span data-stu-id="fd161-190">The file name extension cannot contain spaces or non-ASCII characters and applies only to files (not folders).</span></span> <span data-ttu-id="fd161-191">Les extensions de nom de fichier sont comparées à l’aide d’une fonction de comparaison qui ne respecte pas la casse ou les paramètres régionaux.</span><span class="sxs-lookup"><span data-stu-id="fd161-191">File name extensions are compared using a comparison function that is not sensitive to case or locale.</span></span> <span data-ttu-id="fd161-192">Voir aussi : format de fichier, type de fichier.</span><span class="sxs-lookup"><span data-stu-id="fd161-192">See also: file format, file type.</span></span>

</dd> <dt>

<span data-ttu-id="fd161-193">**type de fichier**</span><span class="sxs-lookup"><span data-stu-id="fd161-193">**file type**</span></span>
</dt> <dd>

<span data-ttu-id="fd161-194">Une valeur d’extension de nom de fichier particulière, telle que « . htm » ou « . jpg », définit une classe de fichiers qui sont du même type et qui ont un ensemble commun d’associations.</span><span class="sxs-lookup"><span data-stu-id="fd161-194">A particular file name extension value, like ".htm" or ".jpg", that defines a class of files that are of the same type and have a common set of associations.</span></span> <span data-ttu-id="fd161-195">Voir aussi : genre, Association de type de fichier.</span><span class="sxs-lookup"><span data-stu-id="fd161-195">See also: Kind, file type association.</span></span>

</dd> <dt>

<span data-ttu-id="fd161-196">**association de types de fichier**</span><span class="sxs-lookup"><span data-stu-id="fd161-196">**file type association**</span></span>
</dt> <dd>

<span data-ttu-id="fd161-197">Pour une extension de nom de fichier particulière, les éléments de tableau d’association qui définissent où les gestionnaires et d’autres attributs peuvent être inscrits.</span><span class="sxs-lookup"><span data-stu-id="fd161-197">For a particular file name extension, the association array elements that define where handlers and other attributes can be registered.</span></span> <span data-ttu-id="fd161-198">Voir aussi : tableau d’association, type de fichier.</span><span class="sxs-lookup"><span data-stu-id="fd161-198">See also: association array, file type.</span></span>

</dd> <dt>

<span data-ttu-id="fd161-199">**personnalisation du type de fichier**</span><span class="sxs-lookup"><span data-stu-id="fd161-199">**file type customization**</span></span>
</dt> <dd>

<span data-ttu-id="fd161-200">Association qui permet à Shell de personnaliser la manière dont l’interpréteur de commandes traite un type de fichier.</span><span class="sxs-lookup"><span data-stu-id="fd161-200">An association that enables Shell to customize how Shell treats a file type.</span></span> <span data-ttu-id="fd161-201">Les personnalisations de type de fichier incluent la spécification de l’application utilisée pour ouvrir le fichier lorsque vous double-cliquez dessus, l’ajout de commandes au menu contextuel pour un type de fichier, la spécification d’une icône personnalisée, la spécification d’un type de contenu MIME à associer à un type de fichier, la spécification d’un type perçu et la spécification d’une ou plusieurs applications associées à un type</span><span class="sxs-lookup"><span data-stu-id="fd161-201">File type customizations include: specifying the application used to open the file when double-clicked, adding commands to the shortcut menu for a file type, specifying a custom icon, specifying a MIME content type to associate with a file type, specifying a perceived type, and specifying one or more applications associated by file type with the Open With dialog box.</span></span> <span data-ttu-id="fd161-202">Voir aussi : PerceivedType.</span><span class="sxs-lookup"><span data-stu-id="fd161-202">See also: PerceivedType.</span></span>

</dd> <dt>

<span data-ttu-id="fd161-203">**Gestionnaire de type de fichier**</span><span class="sxs-lookup"><span data-stu-id="fd161-203">**file type handler**</span></span>
</dt> <dd>

<span data-ttu-id="fd161-204">Gestionnaire inscrit pour un type de fichier.</span><span class="sxs-lookup"><span data-stu-id="fd161-204">A handler registered for a file type.</span></span> <span data-ttu-id="fd161-205">Voir aussi : handler.</span><span class="sxs-lookup"><span data-stu-id="fd161-205">See also: handler.</span></span>

</dd> <dt>

<span data-ttu-id="fd161-206">**Répertoire**</span><span class="sxs-lookup"><span data-stu-id="fd161-206">**folder**</span></span>
</dt> <dd>

<span data-ttu-id="fd161-207">Consultez la définition de : Container.</span><span class="sxs-lookup"><span data-stu-id="fd161-207">See definition for: container.</span></span>

</dd> <dt>

<span data-ttu-id="fd161-208">**PIDL complet**</span><span class="sxs-lookup"><span data-stu-id="fd161-208">**full PIDL**</span></span>
</dt> <dd>

<span data-ttu-id="fd161-209">PIDL qui décrit de façon unique un objet par rapport au dossier Desktop.</span><span class="sxs-lookup"><span data-stu-id="fd161-209">A PIDL that uniquely describes an object relative to the desktop folder.</span></span>

</dd> </dl>

## <a name="h"></a><span data-ttu-id="fd161-210">H</span><span class="sxs-lookup"><span data-stu-id="fd161-210">H</span></span>

<dl> <dt>

<span data-ttu-id="fd161-211">**d**</span><span class="sxs-lookup"><span data-stu-id="fd161-211">**handler**</span></span>
</dt> <dd>

<span data-ttu-id="fd161-212">Objet COM qui fournit les fonctionnalités d’un élément de Shell.</span><span class="sxs-lookup"><span data-stu-id="fd161-212">A COM object that provides functionality for a Shell item.</span></span> <span data-ttu-id="fd161-213">La plupart des sources de données Shell offrent un système extensible pour lier les gestionnaires aux éléments.</span><span class="sxs-lookup"><span data-stu-id="fd161-213">Most Shell data sources offer an extensible system for binding handlers to items.</span></span> <span data-ttu-id="fd161-214">Par exemple, le dossier de système de fichiers utilise le système d’association pour rechercher les gestionnaires pour un type de fichier particulier.</span><span class="sxs-lookup"><span data-stu-id="fd161-214">For example, the file system folder uses the association system to look up the handlers for a particular file type.</span></span> <span data-ttu-id="fd161-215">Voir aussi : Association de fichier, type de fichier, personnalisation de type de fichier.</span><span class="sxs-lookup"><span data-stu-id="fd161-215">See also: file association, file type, file type customization.</span></span>

</dd> </dl>

## <a name="i"></a><span data-ttu-id="fd161-216">I</span><span class="sxs-lookup"><span data-stu-id="fd161-216">I</span></span>

<dl> <dt>

<span data-ttu-id="fd161-217">**gestionnaire d’icône**</span><span class="sxs-lookup"><span data-stu-id="fd161-217">**icon handler**</span></span>
</dt> <dd>

<span data-ttu-id="fd161-218">Gestionnaire qui fournit les informations nécessaires pour générer et mettre en cache une icône pour un élément.</span><span class="sxs-lookup"><span data-stu-id="fd161-218">A handler that provides the information needed to generate and cache an icon for an item.</span></span> <span data-ttu-id="fd161-219">Le magasin de données du système de fichiers prend en charge le chargement d’un gestionnaire d’icône pour un élément en fonction du type de fichier, ce qui permet à ce gestionnaire de fournir une icône qui est utilisée pour toutes les instances de ce type de fichier.</span><span class="sxs-lookup"><span data-stu-id="fd161-219">The file system data store supports loading an icon handler for an item based on the file type, enabling that handler to provide an icon that is used for all instances of that file type.</span></span>

</dd> <dt>

<span data-ttu-id="fd161-220">**gestionnaire d’info-bulle**</span><span class="sxs-lookup"><span data-stu-id="fd161-220">**infotip handler**</span></span>
</dt> <dd>

<span data-ttu-id="fd161-221">Gestionnaire qui fournit le texte contextuel lorsque l’utilisateur place le pointeur de la souris sur un objet d’interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="fd161-221">A handler that provides pop-up text when the user hovers the mouse pointer over a user interface object.</span></span>

</dd> <dt>

<span data-ttu-id="fd161-222">**item**</span><span class="sxs-lookup"><span data-stu-id="fd161-222">**item**</span></span>
</dt> <dd>

<span data-ttu-id="fd161-223">Consultez la définition de : élément de Shell.</span><span class="sxs-lookup"><span data-stu-id="fd161-223">See definition for: Shell item.</span></span>

</dd> <dt>

<span data-ttu-id="fd161-224">**Item (classe)**</span><span class="sxs-lookup"><span data-stu-id="fd161-224">**item class**</span></span>
</dt> <dd>

<span data-ttu-id="fd161-225">Consultez la définition de : type de fichier.</span><span class="sxs-lookup"><span data-stu-id="fd161-225">See definition for: file type.</span></span>

</dd> <dt>

<span data-ttu-id="fd161-226">**liste d’identificateurs d’éléments**</span><span class="sxs-lookup"><span data-stu-id="fd161-226">**item identifier list**</span></span>
</dt> <dd>

<span data-ttu-id="fd161-227">Séquence d’une ou plusieurs structures SHITEMID qui définissent de façon unique un objet par rapport à un objet racine.</span><span class="sxs-lookup"><span data-stu-id="fd161-227">Sequence of one or more SHITEMID structures that uniquely defines an object relative to some root object.</span></span>

</dd> </dl>

## <a name="k"></a><span data-ttu-id="fd161-228">K</span><span class="sxs-lookup"><span data-stu-id="fd161-228">K</span></span>

<dl> <dt>

<span data-ttu-id="fd161-229">**Type**</span><span class="sxs-lookup"><span data-stu-id="fd161-229">**Kind**</span></span>
</dt> <dd>

<span data-ttu-id="fd161-230">Propriété qui fournit un nom de genre convivial et qui peut être associée à une liste de propriétés et un modèle de disposition.</span><span class="sxs-lookup"><span data-stu-id="fd161-230">A property that provides a user-friendly Kind name, and can be associated with a list of properties and a layout pattern.</span></span> <span data-ttu-id="fd161-231">Le genre a été introduit dans Windows Vista pour exprimer une notion plus conviviale de type de fichier par l’utilisateur final et il a été défini comme étant une propriété de chaîne à valeurs multiples (valeurs de chaîne canoniques). vous pouvez donc avoir une valeur de type « audio, vidéo » ou « lien ; document ».</span><span class="sxs-lookup"><span data-stu-id="fd161-231">Kind was introduced in Windows Vista to express a more end-user friendly notion of file type and it was defined to be a multi-value string property (canonical string values), thus you can have an "audio;video" or "link;document" Kind value.</span></span> <span data-ttu-id="fd161-232">Certains noms de genres conviviaux sont déjà associés à des propriétés et des modèles de disposition.</span><span class="sxs-lookup"><span data-stu-id="fd161-232">Some user-friendly Kind names are already associated with properties and layout patterns.</span></span> <span data-ttu-id="fd161-233">Par exemple, les éléments associés au type. Picture et aux éléments associés à Kind.Document affichent des propriétés différentes, même s’ils se trouvent dans la même vue.</span><span class="sxs-lookup"><span data-stu-id="fd161-233">For example, items associated with Kind.Picture and items associated with Kind.Document display different properties even when they are in the same view.</span></span> <span data-ttu-id="fd161-234">Chaque genre d’élément peut être associé à l’un des quatre modèles de disposition uniques qui définissent le nombre de propriétés affichées pour chaque élément et leur disposition.</span><span class="sxs-lookup"><span data-stu-id="fd161-234">Each item Kind can be associated with one of four unique layout patterns that define the number of properties displayed for each item and their layout.</span></span> <span data-ttu-id="fd161-235">Voir aussi : Association de genres, vue de contenu, modèle de disposition.</span><span class="sxs-lookup"><span data-stu-id="fd161-235">See also: Kind association, content view, layout pattern.</span></span>

</dd> </dl>

## <a name="l"></a><span data-ttu-id="fd161-236">L</span><span class="sxs-lookup"><span data-stu-id="fd161-236">L</span></span>

<dl> <dt>

<span data-ttu-id="fd161-237">**modèle de disposition**</span><span class="sxs-lookup"><span data-stu-id="fd161-237">**layout pattern**</span></span>
</dt> <dd>

<span data-ttu-id="fd161-238">L’un des nombreux mécanismes d’affichage des propriétés.</span><span class="sxs-lookup"><span data-stu-id="fd161-238">One of several arrangements for displaying properties.</span></span> <span data-ttu-id="fd161-239">Dans Windows 7 et versions ultérieures, lorsque vous inscrivez un nouveau type de fichier, vous pouvez utiliser l’affichage de contenu pour inscrire une liste de propriétés personnalisées et un modèle de disposition pour votre type de fichier.</span><span class="sxs-lookup"><span data-stu-id="fd161-239">In Windows 7 and later, when you are registering a new file type, you can use the content view to register a custom property list and layout pattern for your file type.</span></span> <span data-ttu-id="fd161-240">Vous pouvez choisir parmi quatre modèles de disposition différents : alpha (pour les résultats de recherche de documents qui contiennent des extraits de code), la version bêta (pour les résultats de recherche par courrier électronique avec extraits de code), gamma (semblable à alpha mais avec une disposition sur deux lignes au lieu de quatre) et Delta</span><span class="sxs-lookup"><span data-stu-id="fd161-240">You can choose from four different layout patterns: Alpha (for document search results that contain code snippets), Beta (for email search results with code snippets), Gamma (similar to Alpha but with a two-line layout instead of four), and Delta (for showing many shorter properties, such as with music and pictures).</span></span> <span data-ttu-id="fd161-241">Voir aussi : vue de contenu, genre, Association de genres.</span><span class="sxs-lookup"><span data-stu-id="fd161-241">See also: content view, Kind, Kind association.</span></span>

</dd> </dl>

## <a name="m"></a><span data-ttu-id="fd161-242">M</span><span class="sxs-lookup"><span data-stu-id="fd161-242">M</span></span>

<dl> <dt>

<span data-ttu-id="fd161-243">**Gestionnaire de métadonnées**</span><span class="sxs-lookup"><span data-stu-id="fd161-243">**metadata handler**</span></span>
</dt> <dd>

<span data-ttu-id="fd161-244">Ce terme est parfois utilisé pour signifier le gestionnaire de propriétés.</span><span class="sxs-lookup"><span data-stu-id="fd161-244">This term is sometimes used to mean property handler.</span></span> <span data-ttu-id="fd161-245">Consultez la définition de : gestionnaire de propriétés.</span><span class="sxs-lookup"><span data-stu-id="fd161-245">See definition for: property handler.</span></span>

</dd> </dl>

## <a name="n"></a><span data-ttu-id="fd161-246">N</span><span class="sxs-lookup"><span data-stu-id="fd161-246">N</span></span>

<dl> <dt>

<span data-ttu-id="fd161-247">**extension de l’espace de noms**</span><span class="sxs-lookup"><span data-stu-id="fd161-247">**namespace extension**</span></span>
</dt> <dd>

<span data-ttu-id="fd161-248">Consultez la définition de : source de données Shell.</span><span class="sxs-lookup"><span data-stu-id="fd161-248">See definition for: Shell data source.</span></span>

</dd> </dl>

## <a name="o"></a><span data-ttu-id="fd161-249">O</span><span class="sxs-lookup"><span data-stu-id="fd161-249">O</span></span>

<dl> <dt>

<span data-ttu-id="fd161-250">**Base de données de liaison et d’incorporation d’objets (OLE DB)**</span><span class="sxs-lookup"><span data-stu-id="fd161-250">**Object Linking and Embedding Database (OLE DB)**</span></span>
</dt> <dd>

<span data-ttu-id="fd161-251">Ensemble standard d’interfaces qui fournit un accès hétérogène à des sources disparates d’informations situées n’importe où, comme les systèmes de fichiers, les dossiers de messagerie et les bases de données.</span><span class="sxs-lookup"><span data-stu-id="fd161-251">A standard set of interfaces that provides heterogeneous access to disparate sources of information located anywhere, such as file systems, email folders, and databases.</span></span>

</dd> <dt>

<span data-ttu-id="fd161-252">**OLE DB**</span><span class="sxs-lookup"><span data-stu-id="fd161-252">**OLE DB**</span></span>
</dt> <dd>

<span data-ttu-id="fd161-253">Consultez la définition de : liaison objet et incorporation d’une base de données.</span><span class="sxs-lookup"><span data-stu-id="fd161-253">See definition for: Object Linking and Embedding Database.</span></span>

</dd> </dl>

## <a name="p"></a><span data-ttu-id="fd161-254">P</span><span class="sxs-lookup"><span data-stu-id="fd161-254">P</span></span>

<dl> <dt>

<span data-ttu-id="fd161-255">**PerceivedType**</span><span class="sxs-lookup"><span data-stu-id="fd161-255">**PerceivedType**</span></span>
</dt> <dd>

<span data-ttu-id="fd161-256">Catégorie étendue de types de format de fichier.</span><span class="sxs-lookup"><span data-stu-id="fd161-256">A broad category of file format types.</span></span> <span data-ttu-id="fd161-257">PerceivedType a été introduit dans Windows XP et prend en charge un ensemble limité de types de fichiers connus (par exemple, les types de fichier image, texte, audio et fichiers compressés).</span><span class="sxs-lookup"><span data-stu-id="fd161-257">PerceivedType was introduced in Windows XP, and supports a limited set of known file types (examples include Image, Text, Audio, and Compressed file types).</span></span> <span data-ttu-id="fd161-258">Les types de fichiers, généralement les types de fichiers publics, peuvent également avoir un type perçu.</span><span class="sxs-lookup"><span data-stu-id="fd161-258">File types, generally public file types, can also have a perceived type.</span></span> <span data-ttu-id="fd161-259">Par exemple, les types de fichiers image. bmp,. png,. jpg et. gif sont également du type perçu, image.</span><span class="sxs-lookup"><span data-stu-id="fd161-259">For example, the image file types .bmp, .png, .jpg, and .gif are also of the perceived type, image.</span></span> <span data-ttu-id="fd161-260">Au niveau de la couche de programmation, PerceivedType est exprimé sous la forme d’un entier.</span><span class="sxs-lookup"><span data-stu-id="fd161-260">At the programming layer, PerceivedType is expressed as an integer.</span></span> <span data-ttu-id="fd161-261">Étant donné que du code utilise Kind et PerceivedType, les propriétaires de format de fichier doivent inscrire les deux.</span><span class="sxs-lookup"><span data-stu-id="fd161-261">Because there is code that uses Kind and PerceivedType, file format owners must register both.</span></span> <span data-ttu-id="fd161-262">Par exemple, « lire tout » dépend de PerceivedType.</span><span class="sxs-lookup"><span data-stu-id="fd161-262">For example "play all" depends on PerceivedType.</span></span> <span data-ttu-id="fd161-263">Voir aussi : type de fichier.</span><span class="sxs-lookup"><span data-stu-id="fd161-263">See also: file type.</span></span>

</dd> <dt>

<span data-ttu-id="fd161-264">**gestionnaire d’aperçus**</span><span class="sxs-lookup"><span data-stu-id="fd161-264">**preview handler**</span></span>
</dt> <dd>

<span data-ttu-id="fd161-265">Gestionnaire qui produit rapidement une vue simplifiée en lecture seule de l’élément de Shell à afficher dans le volet de visualisation de l’Explorateur Windows.</span><span class="sxs-lookup"><span data-stu-id="fd161-265">A handler that quickly produces a read-only, simplified view of the Shell item to be displayed in the Windows Explorer preview pane.</span></span>

</dd> <dt>

<span data-ttu-id="fd161-266">**Gestionnaire de propriétés**</span><span class="sxs-lookup"><span data-stu-id="fd161-266">**property handler**</span></span>
</dt> <dd>

<span data-ttu-id="fd161-267">Gestionnaire qui traduit les données stockées dans un fichier dans un schéma structuré qui est reconnu par et qui est accessible par l’Explorateur Windows, la recherche Windows et d’autres applications.</span><span class="sxs-lookup"><span data-stu-id="fd161-267">A handler that translates data stored in a file into a structured schema that is recognized by and can be accessed by Windows Explorer, Windows Search, and other applications.</span></span> <span data-ttu-id="fd161-268">Ces systèmes peuvent ensuite interagir avec le gestionnaire de propriétés pour écrire et lire les propriétés vers et à partir du fichier.</span><span class="sxs-lookup"><span data-stu-id="fd161-268">These systems can then interact with the property handler to write and read properties to and from the file.</span></span> <span data-ttu-id="fd161-269">Les données traduites comprennent la vue détails, info-bulles, le volet Détails, les pages de propriétés, etc.</span><span class="sxs-lookup"><span data-stu-id="fd161-269">The translated data includes details view, infotips, details pane, property pages, and so forth.</span></span> <span data-ttu-id="fd161-270">Chaque gestionnaire de propriétés est associé à un type de fichier particulier, identifié par l’extension de nom de fichier.</span><span class="sxs-lookup"><span data-stu-id="fd161-270">Each property handler is associated with a particular file type, identified by the file name extension.</span></span> <span data-ttu-id="fd161-271">Voir aussi : système de propriétés.</span><span class="sxs-lookup"><span data-stu-id="fd161-271">See also: property system.</span></span>

</dd> <dt>

<span data-ttu-id="fd161-272">**Gestionnaire de feuille de propriétés**</span><span class="sxs-lookup"><span data-stu-id="fd161-272">**property sheet handler**</span></span>
</dt> <dd>

<span data-ttu-id="fd161-273">Gestionnaire utilisé pour créer des feuilles de propriétés personnalisées avec des images et des contrôles d’interface utilisateur qui autorisent une interaction personnalisée avec un type de fichier.</span><span class="sxs-lookup"><span data-stu-id="fd161-273">A handler that is used to create custom property sheets with UI pictures and controls that permit custom interaction with a file type.</span></span>

</dd> <dt>

<span data-ttu-id="fd161-274">**système de propriétés**</span><span class="sxs-lookup"><span data-stu-id="fd161-274">**property system**</span></span>
</dt> <dd>

<span data-ttu-id="fd161-275">Système extensible de lecture/écriture de définitions de données qui utilise des propriétés implémentées en tant que paires nom-valeur.</span><span class="sxs-lookup"><span data-stu-id="fd161-275">An extensible read/write system of data definitions that uses properties implemented as name-value pairs.</span></span> <span data-ttu-id="fd161-276">Voir aussi : gestionnaire de propriétés, élément de Shell.</span><span class="sxs-lookup"><span data-stu-id="fd161-276">See also: property handler, Shell item.</span></span>

</dd> <dt>

<span data-ttu-id="fd161-277">**valeur de la propriété**</span><span class="sxs-lookup"><span data-stu-id="fd161-277">**property value**</span></span>
</dt> <dd>

<span data-ttu-id="fd161-278">Valeur associée à un nom de propriété pour un élément de Shell.</span><span class="sxs-lookup"><span data-stu-id="fd161-278">A value associated with a property name for a Shell item.</span></span> <span data-ttu-id="fd161-279">Par exemple, « auteur », « taille » et « date de prise » sont des propriétés.</span><span class="sxs-lookup"><span data-stu-id="fd161-279">For example, "Author", "Size", and "Date Taken" are properties.</span></span> <span data-ttu-id="fd161-280">Les valeurs de propriété sont exprimées sous la forme d’une structure PROPVARIANT.</span><span class="sxs-lookup"><span data-stu-id="fd161-280">Property values are expressed as a PROPVARIANT structure.</span></span>

</dd> <dt>

<span data-ttu-id="fd161-281">**Gestionnaire de protocole**</span><span class="sxs-lookup"><span data-stu-id="fd161-281">**protocol handler**</span></span>
</dt> <dd>

<span data-ttu-id="fd161-282">Gestionnaire qui accède aux sources de contenu et fournit un objet IUrlAccessor pour un protocole et une URL spécifiés.</span><span class="sxs-lookup"><span data-stu-id="fd161-282">A handler that accesses content sources and provides an IUrlAccessor object for a specified protocol and URL.</span></span> <span data-ttu-id="fd161-283">Les gestionnaires de protocole étendent la fonctionnalité de recherche Windows et peuvent fournir des notifications de modifications aux indexeurs.</span><span class="sxs-lookup"><span data-stu-id="fd161-283">Protocol handlers extend Windows Search functionality, and may provide change notifications to indexers.</span></span> <span data-ttu-id="fd161-284">Différents gestionnaires de protocole sont requis pour indexer des types spécifiques de magasins de données.</span><span class="sxs-lookup"><span data-stu-id="fd161-284">Different protocol handlers are required to index specific types of data stores.</span></span> <span data-ttu-id="fd161-285">Pour fournir une expérience utilisateur raisonnable, vous devez également fournir une source de données Shell pour le magasin de données en plus de l’implémentation de votre gestionnaire de protocole.</span><span class="sxs-lookup"><span data-stu-id="fd161-285">To provide a reasonable user experience, you must also provide a Shell data source for the data store in addition to implementing your protocol handler.</span></span> <span data-ttu-id="fd161-286">Le gestionnaire de protocole expose les éléments de la Banque de données à l’indexeur, tandis que la source de données Shell expose les éléments de la Banque de données au shell.</span><span class="sxs-lookup"><span data-stu-id="fd161-286">The protocol handler exposes the items in the data store to the indexer, while the Shell data source exposes the items in the data store to the Shell.</span></span>

</dd> </dl>

## <a name="r"></a><span data-ttu-id="fd161-287">R</span><span class="sxs-lookup"><span data-stu-id="fd161-287">R</span></span>

<dl> <dt>

<span data-ttu-id="fd161-288">**PIDL relatif**</span><span class="sxs-lookup"><span data-stu-id="fd161-288">**relative PIDL**</span></span>
</dt> <dd>

<span data-ttu-id="fd161-289">PIDL relatif à un objet racine de l’espace de noms Shell autre que le dossier Desktop.</span><span class="sxs-lookup"><span data-stu-id="fd161-289">A PIDL that is relative to some root object in the shell namespace other than the desktop folder.</span></span> <span data-ttu-id="fd161-290">Il s’agit généralement du dossier parent de l’élément.</span><span class="sxs-lookup"><span data-stu-id="fd161-290">This is commonly the parent folder of the item.</span></span>

</dd> </dl>

## <a name="s"></a><span data-ttu-id="fd161-291">S</span><span class="sxs-lookup"><span data-stu-id="fd161-291">S</span></span>

<dl> <dt>

<span data-ttu-id="fd161-292">**Source de données Shell**</span><span class="sxs-lookup"><span data-stu-id="fd161-292">**Shell data source**</span></span>
</dt> <dd>

<span data-ttu-id="fd161-293">Composant utilisé pour étendre l’espace de noms de l’interpréteur de commandes et exposer des éléments dans un magasin de données.</span><span class="sxs-lookup"><span data-stu-id="fd161-293">A component that is used to extend the Shell namespace and expose items in a data store.</span></span> <span data-ttu-id="fd161-294">Dans le passé, la source de données Shell était appelée extension d’espace de noms Shell.</span><span class="sxs-lookup"><span data-stu-id="fd161-294">In the past, the Shell data source was referred to as the Shell namespace extension.</span></span> <span data-ttu-id="fd161-295">Voir aussi : conteneur, gestionnaire, élément de Shell.</span><span class="sxs-lookup"><span data-stu-id="fd161-295">See also: container, handler, Shell item.</span></span>

</dd> <dt>

<span data-ttu-id="fd161-296">**Extension de l’interpréteur de commandes**</span><span class="sxs-lookup"><span data-stu-id="fd161-296">**Shell extension**</span></span>
</dt> <dd>

<span data-ttu-id="fd161-297">Ce terme est parfois utilisé pour signifier un gestionnaire de type de fichier.</span><span class="sxs-lookup"><span data-stu-id="fd161-297">This term is sometimes used to mean file type handler.</span></span> <span data-ttu-id="fd161-298">Consultez la définition de : gestionnaire de type de fichier.</span><span class="sxs-lookup"><span data-stu-id="fd161-298">See definition for: file type handler.</span></span>

</dd> <dt>

<span data-ttu-id="fd161-299">**Gestionnaire d’extensions de Shell**</span><span class="sxs-lookup"><span data-stu-id="fd161-299">**Shell extension handler**</span></span>
</dt> <dd>

<span data-ttu-id="fd161-300">Ce terme est parfois utilisé pour signifier un gestionnaire de type de fichier.</span><span class="sxs-lookup"><span data-stu-id="fd161-300">This term is sometimes used to mean file type handler.</span></span> <span data-ttu-id="fd161-301">Consultez la définition de : gestionnaire de type de fichier.</span><span class="sxs-lookup"><span data-stu-id="fd161-301">See definition for: file type handler.</span></span>

</dd> <dt>

<span data-ttu-id="fd161-302">**Gestionnaire de Shell**</span><span class="sxs-lookup"><span data-stu-id="fd161-302">**Shell handler**</span></span>
</dt> <dd>

<span data-ttu-id="fd161-303">Ce terme est parfois utilisé pour signifier un gestionnaire de type de fichier.</span><span class="sxs-lookup"><span data-stu-id="fd161-303">This term is sometimes used to mean file type handler.</span></span> <span data-ttu-id="fd161-304">Consultez la définition de : gestionnaire de type de fichier.</span><span class="sxs-lookup"><span data-stu-id="fd161-304">See definition for: file type handler.</span></span>

</dd> <dt>

<span data-ttu-id="fd161-305">**Élément de Shell**</span><span class="sxs-lookup"><span data-stu-id="fd161-305">**Shell item**</span></span>
</dt> <dd>

<span data-ttu-id="fd161-306">Une seule partie du contenu.</span><span class="sxs-lookup"><span data-stu-id="fd161-306">A single piece of content.</span></span> <span data-ttu-id="fd161-307">Certains éléments de l’interpréteur de commandes sont des sources de contenu, et d’autres non.</span><span class="sxs-lookup"><span data-stu-id="fd161-307">Some Shell items are content sources, and some are not.</span></span> <span data-ttu-id="fd161-308">Un dossier est une source de contenu, par exemple, mais il ne s’agit pas d’un fichier. jpg.</span><span class="sxs-lookup"><span data-stu-id="fd161-308">A folder is a content source, for example, but a .jpg file is not.</span></span> <span data-ttu-id="fd161-309">Les gestionnaires de types de fichiers exposent les éléments de Shell.</span><span class="sxs-lookup"><span data-stu-id="fd161-309">File type handlers expose Shell items.</span></span> <span data-ttu-id="fd161-310">Dans certains contextes, l’élément est utilisé pour distinguer les conteneurs des non-conteneurs.</span><span class="sxs-lookup"><span data-stu-id="fd161-310">In some contexts "item" is used to distinguish containers from noncontainers.</span></span> <span data-ttu-id="fd161-311">Voir aussi : conteneur, source de contenu, gestionnaire de type de fichier.</span><span class="sxs-lookup"><span data-stu-id="fd161-311">See also: container, content source, file type handler.</span></span>

</dd> <dt>

<span data-ttu-id="fd161-312">**Extension de l’espace de noms Shell**</span><span class="sxs-lookup"><span data-stu-id="fd161-312">**Shell namespace extension**</span></span>
</dt> <dd>

<span data-ttu-id="fd161-313">Ce terme est parfois utilisé pour signifier la source de données Shell.</span><span class="sxs-lookup"><span data-stu-id="fd161-313">This term is sometimes used to mean Shell data source.</span></span> <span data-ttu-id="fd161-314">Consultez la définition de : source de données Shell.</span><span class="sxs-lookup"><span data-stu-id="fd161-314">See definition for: Shell data source.</span></span>

</dd> <dt>

<span data-ttu-id="fd161-315">**menu contextuel**</span><span class="sxs-lookup"><span data-stu-id="fd161-315">**shortcut menu**</span></span>
</dt> <dd>

<span data-ttu-id="fd161-316">Interface utilisateur utilisée pour présenter une collection de verbes associés à un élément d’interface utilisateur, tel qu’un fichier ou un dossier.</span><span class="sxs-lookup"><span data-stu-id="fd161-316">A user interface that is used to present a collection of verbs associated with a user interface element, such as a file or folder.</span></span>

</dd> <dt>

<span data-ttu-id="fd161-317">**Gestionnaire de menu contextuel**</span><span class="sxs-lookup"><span data-stu-id="fd161-317">**Shortcut menu handler**</span></span>
</dt> <dd>

<span data-ttu-id="fd161-318">Gestionnaire qui ajoute des verbes pour un élément ou des éléments.</span><span class="sxs-lookup"><span data-stu-id="fd161-318">A handler that adds verbs for an item or items.</span></span> <span data-ttu-id="fd161-319">Ces verbes sont généralement affichés dans un menu contextuel.</span><span class="sxs-lookup"><span data-stu-id="fd161-319">These verbs are commonly displayed in a shortcut menu.</span></span> <span data-ttu-id="fd161-320">Voir aussi : menu contextuel.</span><span class="sxs-lookup"><span data-stu-id="fd161-320">See also: shortcut menu.</span></span>

</dd> <dt>

<span data-ttu-id="fd161-321">**PIDL simple**</span><span class="sxs-lookup"><span data-stu-id="fd161-321">**simple PIDL**</span></span>
</dt> <dd>

<span data-ttu-id="fd161-322">PIDL analysé sans vérification du disque.</span><span class="sxs-lookup"><span data-stu-id="fd161-322">A PIDL that is parsed without disk verification.</span></span>

</dd> <dt>

<span data-ttu-id="fd161-323">**verbe statique**</span><span class="sxs-lookup"><span data-stu-id="fd161-323">**static verb**</span></span>
</dt> <dd>

<span data-ttu-id="fd161-324">Verbe qui s’applique à un élément de Shell sans avoir à inspecter l’état actuel d’un élément ou d’un système.</span><span class="sxs-lookup"><span data-stu-id="fd161-324">A verb that applies to a Shell item without needing to inspect the current state of an item or system.</span></span> <span data-ttu-id="fd161-325">Un verbe statique est basé sur une inscription statique des éléments associés d’un élément et ne change pas.</span><span class="sxs-lookup"><span data-stu-id="fd161-325">A static verb is based on a static registration of the associated elements of an item, and does not change.</span></span>

</dd> </dl>

## <a name="t"></a><span data-ttu-id="fd161-326">T</span><span class="sxs-lookup"><span data-stu-id="fd161-326">T</span></span>

<dl> <dt>

<span data-ttu-id="fd161-327">**Gestionnaire de miniatures**</span><span class="sxs-lookup"><span data-stu-id="fd161-327">**thumbnail handler**</span></span>
</dt> <dd>

<span data-ttu-id="fd161-328">Gestionnaire qui fournit une image statique pour représenter un élément de Shell.</span><span class="sxs-lookup"><span data-stu-id="fd161-328">A handler that provides a static image to represent a Shell item.</span></span>

</dd> <dt>

<span data-ttu-id="fd161-329">**fournisseur de miniatures**</span><span class="sxs-lookup"><span data-stu-id="fd161-329">**thumbnail provider**</span></span>
</dt> <dd>

<span data-ttu-id="fd161-330">Ce terme est parfois utilisé pour signifier un gestionnaire de miniatures.</span><span class="sxs-lookup"><span data-stu-id="fd161-330">This term is sometimes used to mean thumbnail handler.</span></span> <span data-ttu-id="fd161-331">Consultez la définition de : gestionnaire de miniatures.</span><span class="sxs-lookup"><span data-stu-id="fd161-331">See definition for: thumbnail handler.</span></span>

</dd> </dl>

## <a name="u"></a><span data-ttu-id="fd161-332">U</span><span class="sxs-lookup"><span data-stu-id="fd161-332">U</span></span>

<dl> <dt>

<span data-ttu-id="fd161-333">**nom du type convivial de l’utilisateur**</span><span class="sxs-lookup"><span data-stu-id="fd161-333">**user friendly kind name**</span></span>
</dt> <dd>

<span data-ttu-id="fd161-334">Consultez la définition de : Kind.</span><span class="sxs-lookup"><span data-stu-id="fd161-334">See definition for: Kind.</span></span>

</dd> </dl>

## <a name="v"></a><span data-ttu-id="fd161-335">V</span><span class="sxs-lookup"><span data-stu-id="fd161-335">V</span></span>

<dl> <dt>

<span data-ttu-id="fd161-336">**verbe**</span><span class="sxs-lookup"><span data-stu-id="fd161-336">**verb**</span></span>
</dt> <dd>

<span data-ttu-id="fd161-337">Action individuelle qui peut être appelée par un élément de Shell.</span><span class="sxs-lookup"><span data-stu-id="fd161-337">An individual action that can be called by a Shell item.</span></span> <span data-ttu-id="fd161-338">Exemples : ouvrir et imprimer.</span><span class="sxs-lookup"><span data-stu-id="fd161-338">Examples include open and print.</span></span> <span data-ttu-id="fd161-339">Les verbes sont parfois appelés commandes ou tâches.</span><span class="sxs-lookup"><span data-stu-id="fd161-339">Verbs are sometimes referred to as commands or tasks.</span></span> <span data-ttu-id="fd161-340">Voir aussi : verbe dynamique, gestionnaire de menu contextuel, verbe statique.</span><span class="sxs-lookup"><span data-stu-id="fd161-340">See also: dynamic verb, shortcut menu handler, static verb.</span></span>

</dd> <dt>

<span data-ttu-id="fd161-341">**Gestionnaire de verbes**</span><span class="sxs-lookup"><span data-stu-id="fd161-341">**verb handler**</span></span>
</dt> <dd>

<span data-ttu-id="fd161-342">Ce terme est parfois utilisé pour signifier le gestionnaire de menu contextuel.</span><span class="sxs-lookup"><span data-stu-id="fd161-342">This term is sometimes used to mean shortcut menu handler.</span></span> <span data-ttu-id="fd161-343">Consultez la définition de : gestionnaire de menu contextuel.</span><span class="sxs-lookup"><span data-stu-id="fd161-343">See definition for: shortcut menu handler.</span></span>

</dd> </dl>

 

 



