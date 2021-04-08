---
description: L’Explorateur Windows contrôle la création d’un connecteur de recherche pour un gestionnaire de protocole par le biais d’entrées de clé de registre. Par le biais du Registre, les implémenteurs et les tiers peuvent permettre aux gestionnaires de protocoles nouveaux et hérités de participer à la recherche dans Windows 7.
ms.assetid: 79abdcbc-ba60-43bd-9895-18ee8b6c5829
title: Création d’un connecteur de recherche pour un gestionnaire de protocole
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 57b43fd7eac53ca2c89d6c8b0d2cd36fd813e63a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104112482"
---
# <a name="creating-a-search-connector-for-a-protocol-handler"></a><span data-ttu-id="0b95c-104">Création d’un connecteur de recherche pour un gestionnaire de protocole</span><span class="sxs-lookup"><span data-stu-id="0b95c-104">Creating a Search Connector for a Protocol Handler</span></span>

<span data-ttu-id="0b95c-105">L’Explorateur Windows contrôle la création d’un connecteur de recherche pour un gestionnaire de protocole par le biais d’entrées de clé de registre.</span><span class="sxs-lookup"><span data-stu-id="0b95c-105">Windows Explorer controls the creation of a search connector for a protocol handler through registry key entries.</span></span> <span data-ttu-id="0b95c-106">Par le biais du Registre, les implémenteurs et les tiers peuvent permettre aux gestionnaires de protocoles nouveaux et hérités de participer à la recherche dans Windows 7.</span><span class="sxs-lookup"><span data-stu-id="0b95c-106">Through the registry both implementers and third parties can enable new and legacy protocol handlers to participate in Windows 7 Search.</span></span>

<span data-ttu-id="0b95c-107">Cette rubrique est organisée comme suit :</span><span class="sxs-lookup"><span data-stu-id="0b95c-107">This topic is organized as follows:</span></span>

-   [<span data-ttu-id="0b95c-108">À propos des connecteurs de recherche pour les gestionnaires de protocole dans Windows 7</span><span class="sxs-lookup"><span data-stu-id="0b95c-108">About Search Connectors for Protocol Handlers in Windows 7</span></span>](#about-search-connectors-for-protocol-handlers-in-windows-7)
-   [<span data-ttu-id="0b95c-109">Activation des gestionnaires de protocole pour participer à la recherche</span><span class="sxs-lookup"><span data-stu-id="0b95c-109">Enabling Protocol Handlers to Participate in Search</span></span>](#enabling-protocol-handlers-to-participate-in-search)
    -   [<span data-ttu-id="0b95c-110">Désactivation de la création du connecteur de recherche du gestionnaire de protocole</span><span class="sxs-lookup"><span data-stu-id="0b95c-110">Disabling Protocol Handler Search Connector Creation</span></span>](#disabling-protocol-handler-search-connector-creation)
    -   [<span data-ttu-id="0b95c-111">Personnalisation du nom, de la description ou du FolderType pour un connecteur de recherche de gestionnaire de protocole</span><span class="sxs-lookup"><span data-stu-id="0b95c-111">Customizing the Name, Description or FolderType for a Protocol Handler Search Connector</span></span>](#customizing-the-name-description-or-foldertype-for-a-protocol-handler-search-connector)
    -   [<span data-ttu-id="0b95c-112">Utilisation de la redirection de chaînes de Registre</span><span class="sxs-lookup"><span data-stu-id="0b95c-112">Using Registry String Redirection</span></span>](#using-registry-string-redirection)
    -   [<span data-ttu-id="0b95c-113">Restauration d’un connecteur de recherche supprimé du gestionnaire de protocole</span><span class="sxs-lookup"><span data-stu-id="0b95c-113">Restoring a Deleted Protocol Handler Search Connector</span></span>](#restoring-a-deleted-protocol-handler-search-connector)
-   [<span data-ttu-id="0b95c-114">Ressources supplémentaires</span><span class="sxs-lookup"><span data-stu-id="0b95c-114">Additional Resources</span></span>](#additional-resources)
-   [<span data-ttu-id="0b95c-115">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="0b95c-115">Related topics</span></span>](#related-topics)

## <a name="about-search-connectors-for-protocol-handlers-in-windows-7"></a><span data-ttu-id="0b95c-116">À propos des connecteurs de recherche pour les gestionnaires de protocole dans Windows 7</span><span class="sxs-lookup"><span data-stu-id="0b95c-116">About Search Connectors for Protocol Handlers in Windows 7</span></span>

<span data-ttu-id="0b95c-117">Dans Windows 7, les recherches à partir du menu **Démarrer** ou de l’Explorateur Windows incluent uniquement des fichiers situés dans des emplacements indexés, et des éléments de système non-fichier tels que des magasins de données distants ou des éléments de gestionnaire de protocole qui ont un connecteur de recherche.</span><span class="sxs-lookup"><span data-stu-id="0b95c-117">In Windows 7, searches from the **Start** menu or Windows Explorer include only files in indexed locations, and non-file system items such as remote data stores or protocol handler items that have a search connector.</span></span> <span data-ttu-id="0b95c-118">En plus d’inclure les éléments du gestionnaire de protocole dans l’étendue du menu **Démarrer** et les recherches dans le shell, le connecteur de recherche permet au menu **Démarrer** de regrouper les éléments du gestionnaire de protocole dans les résultats du menu **Démarrer** , avec l’avantage qui en résulte que l’utilisateur peut cliquer sur l’en-tête de groupe et afficher les résultats uniquement à partir du gestionnaire de protocole.</span><span class="sxs-lookup"><span data-stu-id="0b95c-118">In addition to including the protocol handler items in the scope of **Start** menu and Shell searches, the search connector enables the **Start** menu to group protocol handler items together in **Start** menu results, with the resulting benefit that the user can click the group header and view results from only the protocol handler.</span></span> <span data-ttu-id="0b95c-119">L’utilisateur peut également accéder au dossier **recherches** , ouvrir le fichier de connecteur de recherche et effectuer une recherche incluant uniquement les éléments du gestionnaire de protocole spécifique associé à ce connecteur de recherche.</span><span class="sxs-lookup"><span data-stu-id="0b95c-119">Alternatively, the user can navigate to the **Searches** folder, open the search connector file, and perform a search that includes only items from the specific protocol handler associated with that search connector.</span></span>

<span data-ttu-id="0b95c-120">Lorsqu’un utilisateur démarre pour la première fois une application qui inscrit un gestionnaire de protocole, l’Explorateur Windows génère un fichier de connecteur de recherche (. searchConnector-ms) pour le gestionnaire de protocole dans le dossier **recherches** de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="0b95c-120">When a user first starts an application that registers a protocol handler, Windows Explorer generates a search connector file (.searchConnector-ms) for the protocol handler in the user's **Searches** folder.</span></span> <span data-ttu-id="0b95c-121">Les applications avec des gestionnaires de protocole peuvent choisir de désactiver ce comportement ou de personnaliser le nom et la description du connecteur de recherche du gestionnaire de protocole.</span><span class="sxs-lookup"><span data-stu-id="0b95c-121">Applications with protocol handlers can choose to disable this behavior or customize the name and description of the protocol handler search connector.</span></span>

> [!Note]  
> <span data-ttu-id="0b95c-122">L’emplacement du dossier **recherches** de l’utilisateur est% USERPROFILE% \\ recherches ou FOLDERID \_ SavedSearches.</span><span class="sxs-lookup"><span data-stu-id="0b95c-122">The location of the user's **Searches** folder is %userprofile%\\Searches, or FOLDERID\_SavedSearches.</span></span> <span data-ttu-id="0b95c-123">Le GUID de FOLDERID \_ SavedSearches est {7d1d3a04-debb-4115-95cf-2f29da2920da}.</span><span class="sxs-lookup"><span data-stu-id="0b95c-123">The GUID for FOLDERID\_SavedSearches is {7d1d3a04-debb-4115-95cf-2f29da2920da}.</span></span>

 

<span data-ttu-id="0b95c-124">L’Explorateur Windows contrôle la création d’un connecteur de recherche pour un gestionnaire de protocole via les entrées de clé de Registre décrites dans les sections suivantes :</span><span class="sxs-lookup"><span data-stu-id="0b95c-124">Windows Explorer controls the creation of a search connector for a protocol handler through registry key entries described in the following sections:</span></span>

-   [<span data-ttu-id="0b95c-125">Activation des gestionnaires de protocole pour participer à la recherche</span><span class="sxs-lookup"><span data-stu-id="0b95c-125">Enabling Protocol Handlers to Participate in Search</span></span>](#enabling-protocol-handlers-to-participate-in-search)
-   [<span data-ttu-id="0b95c-126">Désactivation de la création du connecteur de recherche du gestionnaire de protocole</span><span class="sxs-lookup"><span data-stu-id="0b95c-126">Disabling Protocol Handler Search Connector Creation</span></span>](#disabling-protocol-handler-search-connector-creation)
-   [<span data-ttu-id="0b95c-127">Personnalisation du nom, de la description ou du FolderType pour un connecteur de recherche de gestionnaire de protocole</span><span class="sxs-lookup"><span data-stu-id="0b95c-127">Customizing the Name, Description or FolderType for a Protocol Handler Search Connector</span></span>](#customizing-the-name-description-or-foldertype-for-a-protocol-handler-search-connector)
-   [<span data-ttu-id="0b95c-128">Restauration d’un connecteur de recherche supprimé du gestionnaire de protocole</span><span class="sxs-lookup"><span data-stu-id="0b95c-128">Restoring a Deleted Protocol Handler Search Connector</span></span>](#restoring-a-deleted-protocol-handler-search-connector)

> [!Note]  
> <span data-ttu-id="0b95c-129">Il n’existe aucun moyen de créer un connecteur de recherche pour un gestionnaire de protocole.</span><span class="sxs-lookup"><span data-stu-id="0b95c-129">There are no programmatic means to create a search connector for a protocol handler.</span></span> <span data-ttu-id="0b95c-130">Ils doivent être configurés par le biais du Registre.</span><span class="sxs-lookup"><span data-stu-id="0b95c-130">They must be configured through the registry.</span></span>

 

## <a name="enabling-protocol-handlers-to-participate-in-search"></a><span data-ttu-id="0b95c-131">Activation des gestionnaires de protocole pour participer à la recherche</span><span class="sxs-lookup"><span data-stu-id="0b95c-131">Enabling Protocol Handlers to Participate in Search</span></span>

<span data-ttu-id="0b95c-132">Les clés de Registre et leurs valeurs possibles sont décrites dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="0b95c-132">Registry keys and their possible values are outlined in the following table.</span></span> <span data-ttu-id="0b95c-133">Un gestionnaire de protocole peut remplir une partie ou la totalité de ces clés de Registre <protocol> , où est remplacé par le nom réel de son protocole, par exemple MAPI, file ou CSC, par exemple.</span><span class="sxs-lookup"><span data-stu-id="0b95c-133">A protocol handler can populate some or all of these registry keys where <protocol> is replaced with the actual name of its protocol, such as MAPI, file, or csc, for example.</span></span>



| <span data-ttu-id="0b95c-134">Clé de Registre</span><span class="sxs-lookup"><span data-stu-id="0b95c-134">Registry key</span></span>                                                                                                                 | <span data-ttu-id="0b95c-135">Valeur (s) possible (s)</span><span class="sxs-lookup"><span data-stu-id="0b95c-135">Possible value(s)</span></span>                                                                                                                     | <span data-ttu-id="0b95c-136">Type</span><span class="sxs-lookup"><span data-stu-id="0b95c-136">Type</span></span>       | <span data-ttu-id="0b95c-137">Commentaires</span><span class="sxs-lookup"><span data-stu-id="0b95c-137">Comments</span></span>                                                                                                                                                                                                                                                                                                                                                  |
|------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0b95c-138">HKEY \_ local \_ machine \\ Software \\ Microsoft \\ Windows Search \\ PHSearchConnectors \\ <protocol> \\ version</span><span class="sxs-lookup"><span data-stu-id="0b95c-138">HKEY\_LOCAL\_MACHINE\\Software\\Microsoft\\Windows Search\\PHSearchConnectors\\<protocol>\\Version</span></span>                     | <span data-ttu-id="0b95c-139">N’existe pas (valeur par défaut).</span><span class="sxs-lookup"><span data-stu-id="0b95c-139">Does not exist (default).</span></span> <span data-ttu-id="0b95c-140">Dans le cas contraire, la valeur est supérieure ou égale à 1.</span><span class="sxs-lookup"><span data-stu-id="0b95c-140">Otherwise it is 1 or greater.</span></span>                                                                               | <span data-ttu-id="0b95c-141">\_valeur DWORD reg</span><span class="sxs-lookup"><span data-stu-id="0b95c-141">REG\_DWORD</span></span> | <span data-ttu-id="0b95c-142">Cette valeur est utilisée pour détecter les modifications apportées aux inscriptions de modèles d’emplacement pour les racines de recherche qui ont déjà été traitées.</span><span class="sxs-lookup"><span data-stu-id="0b95c-142">This value is used to detect changes to the location template registrations for search roots that have already been processed.</span></span> <span data-ttu-id="0b95c-143">Si n’existe pas, utilisez 0 comme valeur par défaut.</span><span class="sxs-lookup"><span data-stu-id="0b95c-143">If does not exist, use 0 as a default.</span></span> <span data-ttu-id="0b95c-144">Vous pouvez également incrémenter la version pour informer l’Explorateur Windows que le connecteur de recherche doit être régénéré, car une version plus récente du gestionnaire de protocole a été installée.</span><span class="sxs-lookup"><span data-stu-id="0b95c-144">Alternatively, increment the version to inform Windows Explorer that the search connector should be regenerated because a newer version of the protocol handler has been installed.</span></span> |
| <span data-ttu-id="0b95c-145">HKEY \_ local \_ machine \\ Software \\ Microsoft \\ Windows Search \\ PHSearchConnectors \\ <protocol> \\ DoNotCreateSearchConnectors</span><span class="sxs-lookup"><span data-stu-id="0b95c-145">HKEY\_LOCAL\_MACHINE\\Software\\Microsoft\\Windows Search\\PHSearchConnectors\\<protocol>\\DoNotCreateSearchConnectors</span></span> | <span data-ttu-id="0b95c-146">N’existe pas (valeur par défaut).</span><span class="sxs-lookup"><span data-stu-id="0b95c-146">Does not exist (default).</span></span> <span data-ttu-id="0b95c-147">Sinon, la valeur est 1.</span><span class="sxs-lookup"><span data-stu-id="0b95c-147">Otherwise set to 1.</span></span>                                                                                         | <span data-ttu-id="0b95c-148">\_valeur DWORD reg</span><span class="sxs-lookup"><span data-stu-id="0b95c-148">REG\_DWORD</span></span> | <span data-ttu-id="0b95c-149">S’il n’existe pas, créez un fichier. searchconnector-ms dans le dossier recherches.</span><span class="sxs-lookup"><span data-stu-id="0b95c-149">If it does not exist, create a .searchconnector-ms file in the Searches folder.</span></span> <span data-ttu-id="0b95c-150">Si la valeur est 1, marquer comme traité et ne rien faire.</span><span class="sxs-lookup"><span data-stu-id="0b95c-150">If 1, mark as processed and do nothing.</span></span>                                                                                                                                                                                                                                   |
| <span data-ttu-id="0b95c-151">HKEY \_ local \_ machine \\ Software \\ Microsoft \\ Windows Search \\ PHSearchConnectors- \\ <protocol> \\ Description par défaut \\</span><span class="sxs-lookup"><span data-stu-id="0b95c-151">HKEY\_LOCAL\_MACHINE\\Software\\Microsoft\\Windows Search\\PHSearchConnectors\\<protocol>\\Default\\Description</span></span>        | <span data-ttu-id="0b95c-152">Chaîne localisable contenant la description du connecteur de recherche.</span><span class="sxs-lookup"><span data-stu-id="0b95c-152">A localizable string containing the description of the search connector.</span></span>                                                              | <span data-ttu-id="0b95c-153">SZ de REG \_</span><span class="sxs-lookup"><span data-stu-id="0b95c-153">REG\_SZ</span></span>    | <span data-ttu-id="0b95c-154">Optionnel.</span><span class="sxs-lookup"><span data-stu-id="0b95c-154">Optional.</span></span> <span data-ttu-id="0b95c-155">Elle est utilisée dans l’élément Description du fichier. searchconnector-ms.</span><span class="sxs-lookup"><span data-stu-id="0b95c-155">It is used in the Description element of the .searchconnector-ms file.</span></span>                                                                                                                                                                                                                                                                          |
| <span data-ttu-id="0b95c-156">HKEY \_ local \_ machine \\ Software \\ Microsoft \\ Windows Search \\ PHSearchConnectors \\ <protocol> \\ nom par défaut \\</span><span class="sxs-lookup"><span data-stu-id="0b95c-156">HKEY\_LOCAL\_MACHINE\\Software\\Microsoft\\Windows Search\\PHSearchConnectors\\<protocol>\\Default\\Name</span></span>               | <span data-ttu-id="0b95c-157">Chaîne localisée pour nommer le connecteur de recherche.</span><span class="sxs-lookup"><span data-stu-id="0b95c-157">A localized string to name the search connector.</span></span> <span data-ttu-id="0b95c-158">Utilisé comme nom du fichier. searchconnector-ms.</span><span class="sxs-lookup"><span data-stu-id="0b95c-158">Used as the name of the .searchconnector-ms file.</span></span>                                    | <span data-ttu-id="0b95c-159">SZ de REG \_</span><span class="sxs-lookup"><span data-stu-id="0b95c-159">REG\_SZ</span></span>    | <span data-ttu-id="0b95c-160">Chaque emplacement doit avoir un nom unique.</span><span class="sxs-lookup"><span data-stu-id="0b95c-160">Each location must have a unique name.</span></span> <span data-ttu-id="0b95c-161">En l’absence de cette valeur, le nom complet fourni par l' [interface IShellFolder](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) du gestionnaire de protocole est utilisé.</span><span class="sxs-lookup"><span data-stu-id="0b95c-161">In the absence of this value, the display name provided by the protocol handler's [IShellFolder Interface](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) will be used.</span></span>                                                                                                                             |
| <span data-ttu-id="0b95c-162">HKEY \_ local \_ machine \\ Software \\ Microsoft \\ Windows Search \\ PHSearchConnectors \\ <protocol> \\ par défaut \\ FolderType</span><span class="sxs-lookup"><span data-stu-id="0b95c-162">HKEY\_LOCAL\_MACHINE\\Software\\Microsoft\\Windows Search\\PHSearchConnectors\\<protocol>\\Default\\FolderType</span></span>         | <span data-ttu-id="0b95c-163">GUID identifiant le [FOLDERTYPEID](../shell/foldertypeid.md) à appliquer au connecteur de recherche.</span><span class="sxs-lookup"><span data-stu-id="0b95c-163">A GUID identifying the [FOLDERTYPEID](../shell/foldertypeid.md) to apply to the search connector.</span></span> | <span data-ttu-id="0b95c-164">SZ de REG \_</span><span class="sxs-lookup"><span data-stu-id="0b95c-164">REG\_SZ</span></span>    | <span data-ttu-id="0b95c-165">Optionnel.</span><span class="sxs-lookup"><span data-stu-id="0b95c-165">Optional.</span></span> <span data-ttu-id="0b95c-166">Utilisé dans l’élément folderType du fichier. searchconnector-ms pour indiquer quels modèles doivent être utilisés pour afficher les résultats.</span><span class="sxs-lookup"><span data-stu-id="0b95c-166">Used in the folderType element of the .searchconnector-ms file to indicate what templates should be used to display results.</span></span> <span data-ttu-id="0b95c-167">Par exemple, la valeur GUID de \_ documents FOLDERTYPEID.</span><span class="sxs-lookup"><span data-stu-id="0b95c-167">For example, the GUID value of FOLDERTYPEID\_Documents.</span></span>                                                                                                                                                            |



 

### <a name="disabling-protocol-handler-search-connector-creation"></a><span data-ttu-id="0b95c-168">Désactivation de la création du connecteur de recherche du gestionnaire de protocole</span><span class="sxs-lookup"><span data-stu-id="0b95c-168">Disabling Protocol Handler Search Connector Creation</span></span>

<span data-ttu-id="0b95c-169">Si votre application expose des éléments via un gestionnaire de protocole pour une utilisation dans l’application elle-même et que vous ne souhaitez pas exposer les éléments par le biais de l’interpréteur de commandes (dans le menu **Démarrer** et les recherches dans l’Explorateur Windows), vous devez désactiver la création d’un connecteur de recherche pour votre gestionnaire de protocole.</span><span class="sxs-lookup"><span data-stu-id="0b95c-169">If your application exposes items through a protocol handler for use in the application itself and you do not want to expose the items through the Shell (in **Start** menu and Windows Explorer searches), you need to disable the creation of a search connector for your protocol handler.</span></span>

<span data-ttu-id="0b95c-170">Pour désactiver la création du connecteur de recherche, définissez DoNotCreateSearchConnectors sur 0x00000001 (1), comme indiqué dans l’exemple de clé de Registre suivant.</span><span class="sxs-lookup"><span data-stu-id="0b95c-170">To disable search connector creation set DoNotCreateSearchConnectors to 0x00000001(1), as shown in the following registry key example.</span></span>

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows Search
            PHSearchConnectors
               <protocol>
                  DoNotCreateSearchConnectors
```

<span data-ttu-id="0b95c-171">Si DoNotCreateSearchConnectors a la valeur 1, nous vous recommandons d’exposer la propriété [System. Shell. OmitFromView](/windows/desktop/properties/props-system-shell-omitfromview) sur chaque élément exposé par le gestionnaire de protocole et de définir la valeur de cette propriété sur **true**.</span><span class="sxs-lookup"><span data-stu-id="0b95c-171">If DoNotCreateSearchConnectors is set to 1, then we recommend that you expose the [System.Shell.OmitFromView](/windows/desktop/properties/props-system-shell-omitfromview) property on each item exposed by the protocol handler, and set the value of this property to **TRUE**.</span></span> <span data-ttu-id="0b95c-172">Cela empêchera l’affichage des éléments du gestionnaire de protocole sous le groupe **fichiers** du menu **Démarrer** .</span><span class="sxs-lookup"><span data-stu-id="0b95c-172">Doing so will prevent the protocol handler items from appearing under the **Start** menu **Files** group.</span></span>

<span data-ttu-id="0b95c-173">Si DoNotCreateSearchConnectors est présent et défini à zéro, l’Explorateur Windows crée un connecteur de recherche pour le gestionnaire de protocole et les éléments du gestionnaire de protocole sont retournés dans dans le menu **Démarrer** et les recherches dans l’Explorateur Windows.</span><span class="sxs-lookup"><span data-stu-id="0b95c-173">If DoNotCreateSearchConnectors is present and set to zero, then Windows Explorer will create a search connector for the protocol handler, and the protocol handler items will be returned in in **Start** menu and Windows Explorer searches.</span></span>

### <a name="customizing-the-name-description-or-foldertype-for-a-protocol-handler-search-connector"></a><span data-ttu-id="0b95c-174">Personnalisation du nom, de la description ou du FolderType pour un connecteur de recherche de gestionnaire de protocole</span><span class="sxs-lookup"><span data-stu-id="0b95c-174">Customizing the Name, Description or FolderType for a Protocol Handler Search Connector</span></span>

<span data-ttu-id="0b95c-175">Le nom du connecteur de recherche est utilisé non seulement pour identifier le connecteur de recherche dans le dossier **recherches** , mais comme en-tête de groupe pour les résultats dans les recherches dans le menu **Démarrer** .</span><span class="sxs-lookup"><span data-stu-id="0b95c-175">The search connector name is used not only to identify the search connector in the **Searches** folder, but as the group header for the results in **Start** menu searches.</span></span> <span data-ttu-id="0b95c-176">Par conséquent, il est important de fournir un nom descriptif pour le connecteur de recherche.</span><span class="sxs-lookup"><span data-stu-id="0b95c-176">Hence, it is important to provide a descriptive name for the search connector.</span></span> <span data-ttu-id="0b95c-177">Si aucun nom n’est fourni dans la clé de Registre, l’Explorateur Windows utilise par défaut le nom fourni par l' [interface IShellFolder](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) pour la racine de recherche et la description vide du gestionnaire de protocole.</span><span class="sxs-lookup"><span data-stu-id="0b95c-177">If a name is not provided in the registry key, by default Windows Explorer uses the name provided by [IShellFolder Interface](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) for the protocol handler's search root and blank description.</span></span> <span data-ttu-id="0b95c-178">Vous pouvez remplacer le nom par défaut par une entrée de clé de registre sans avoir à renommer l’interface IShellFolder.</span><span class="sxs-lookup"><span data-stu-id="0b95c-178">You can override the default name through a registry key entry without having to rename the IShellFolder Interface.</span></span> <span data-ttu-id="0b95c-179">Bien qu’il ne soit pas aussi visible que le nom du connecteur de recherche, vous pouvez également remplacer la description du connecteur de recherche en fournissant votre propre description.</span><span class="sxs-lookup"><span data-stu-id="0b95c-179">Although it is not as visible as the search connector name, you can also override the description for the search connector by providing your own description.</span></span>

<span data-ttu-id="0b95c-180">Pour remplacer le nom ou la description par défaut, définissez les entrées comme indiqué dans l’exemple de Registre suivant.</span><span class="sxs-lookup"><span data-stu-id="0b95c-180">To override the default name or description, set the entries as shown in the following registry example.</span></span>

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows Search
            PHSearchConnectors
               <protocol>
                  Default
                     Name
                     Description
```

<span data-ttu-id="0b95c-181">En outre, l’entrée FolderType peut être définie sur l’un des GUID [FOLDERTYPEID](../shell/foldertypeid.md) .</span><span class="sxs-lookup"><span data-stu-id="0b95c-181">In addition, the FolderType entry can be set to one of the [FOLDERTYPEID](../shell/foldertypeid.md) GUIDs.</span></span> <span data-ttu-id="0b95c-182">La valeur doit être le GUID réel et non son nom.</span><span class="sxs-lookup"><span data-stu-id="0b95c-182">The value should be the actual GUID, and not its name.</span></span> <span data-ttu-id="0b95c-183">Par exemple, {94d6ddcc-4a68-4175-A374-bd584a510b78} au lieu de FOLDERTYPEID \_ Music.</span><span class="sxs-lookup"><span data-stu-id="0b95c-183">For example, {94d6ddcc-4a68-4175-a374-bd584a510b78} rather than FOLDERTYPEID\_Music.</span></span> <span data-ttu-id="0b95c-184">Le GUID d’un FOLDERTYPEID peut être obtenu dans le fichier d’en-tête shlguid. h dans le [SDK Windows](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="0b95c-184">The GUID for a FOLDERTYPEID can be obtained in the Shlguid.h header file in the [Windows SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span>

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows Search
            PHSearchConnectors
               <protocol>
                  Default
                     FolderType = {94d6ddcc-4a68-4175-a374-bd584a510b78}
```

### <a name="using-registry-string-redirection"></a><span data-ttu-id="0b95c-185">Utilisation de la redirection de chaînes de Registre</span><span class="sxs-lookup"><span data-stu-id="0b95c-185">Using Registry String Redirection</span></span>

<span data-ttu-id="0b95c-186">Vous pouvez utiliser une [chaîne redirigée](../intl/using-registry-string-redirection.md) pour vous assurer que le nom que vous fournissez pour le connecteur de recherche peut être localisé.</span><span class="sxs-lookup"><span data-stu-id="0b95c-186">You can use a [redirected string](../intl/using-registry-string-redirection.md) to ensure that the name you provide for the search connector can be localized.</span></span> <span data-ttu-id="0b95c-187">Vous pouvez inclure des chaînes localisables pour les clés de Registre Name et description au lieu d’entrer la chaîne réelle dans le registre.</span><span class="sxs-lookup"><span data-stu-id="0b95c-187">You can include localizable strings for the name and description registry keys instead of entering the actual string into the registry.</span></span>

<span data-ttu-id="0b95c-188">Pour inclure une chaîne localisable pour les valeurs de nom ou de description, définissez la valeur comme indiqué dans l’exemple de clé de Registre suivant.</span><span class="sxs-lookup"><span data-stu-id="0b95c-188">To include a localizable string for the Name or Description values, set the value as shown in the following registry key example.</span></span>

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows Search
            PHSearchConnectors
               <protocol>
                  Name = @dllname.dll,-resourceID
```

<span data-ttu-id="0b95c-189">La chaîne localisable prend le format suivant :</span><span class="sxs-lookup"><span data-stu-id="0b95c-189">The localizable string takes the following format:</span></span>

-   <span data-ttu-id="0b95c-190">@dllname.dll,-resourceID, où :</span><span class="sxs-lookup"><span data-stu-id="0b95c-190">@dllname.dll,-resourceID, where:</span></span>
    -   <span data-ttu-id="0b95c-191">@dllname.dll est le chemin d’accès à la DLL qui contient la ressource de type chaîne</span><span class="sxs-lookup"><span data-stu-id="0b95c-191">@dllname.dll is the path to the DLL that contains the string resource</span></span>
    -   <span data-ttu-id="0b95c-192">resourceID est l’ID de ressource entier de la ressource de type chaîne</span><span class="sxs-lookup"><span data-stu-id="0b95c-192">resourceID is the integer resource ID of the string resource</span></span>

<span data-ttu-id="0b95c-193">Le format d’une chaîne indirecte, et une chaîne indirecte ajoutée avec un modificateur de version, est décrit dans la [fonction SHLoadIndirectString](/windows/win32/api/shlwapi/nf-shlwapi-shloadindirectstring).</span><span class="sxs-lookup"><span data-stu-id="0b95c-193">The format for an indirect string, and an indirect string appended with a version modifier, is described in [SHLoadIndirectString Function](/windows/win32/api/shlwapi/nf-shlwapi-shloadindirectstring).</span></span>

### <a name="restoring-a-deleted-protocol-handler-search-connector"></a><span data-ttu-id="0b95c-194">Restauration d’un connecteur de recherche supprimé du gestionnaire de protocole</span><span class="sxs-lookup"><span data-stu-id="0b95c-194">Restoring a Deleted Protocol Handler Search Connector</span></span>

<span data-ttu-id="0b95c-195">Étant donné que les connecteurs de recherche sont des fichiers sur l’ordinateur de l’utilisateur, ils peuvent être supprimés par erreur.</span><span class="sxs-lookup"><span data-stu-id="0b95c-195">Because search connectors are files on the user's computer, they can be mistakenly deleted.</span></span> <span data-ttu-id="0b95c-196">Pour restaurer tous les connecteurs de recherche du gestionnaire de protocole supprimés, restaurez les bibliothèques par défaut.</span><span class="sxs-lookup"><span data-stu-id="0b95c-196">To restore all deleted protocol handler search connectors, restore the default libraries.</span></span> <span data-ttu-id="0b95c-197">Pour ce faire, ouvrez l’Explorateur Windows, cliquez avec le bouton droit sur le dossier **bibliothèques** , puis sélectionnez **restaurer les bibliothèques par défaut**.</span><span class="sxs-lookup"><span data-stu-id="0b95c-197">To so do, open Windows Explorer, right-click the **Libraries** folder, and then select **Restore Default Libraries**.</span></span>

![capture d’écran montrant l’option de menu restaurer les bibliothèques par défaut](images/libraries.png)

## <a name="additional-resources"></a><span data-ttu-id="0b95c-199">Ressources supplémentaires</span><span class="sxs-lookup"><span data-stu-id="0b95c-199">Additional Resources</span></span>

-   [<span data-ttu-id="0b95c-200">IShellItem :: GetDisplayName</span><span class="sxs-lookup"><span data-stu-id="0b95c-200">IShellItem::GetDisplayName</span></span>](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellitem-getdisplayname)
-   [<span data-ttu-id="0b95c-201">SIGDN \_ NORMALDISPLAY</span><span class="sxs-lookup"><span data-stu-id="0b95c-201">SIGDN\_NORMALDISPLAY</span></span>](/windows/win32/api/shobjidl_core/ne-shobjidl_core-sigdn)

## <a name="related-topics"></a><span data-ttu-id="0b95c-202">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="0b95c-202">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="0b95c-203">**Méthodologique**</span><span class="sxs-lookup"><span data-stu-id="0b95c-203">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="0b95c-204">Fonctionnement des gestionnaires de protocole</span><span class="sxs-lookup"><span data-stu-id="0b95c-204">Understanding Protocol Handlers</span></span>](-search-3x-wds-extidx-prot-implementing.md)
</dt> <dt>

[<span data-ttu-id="0b95c-205">Développement de gestionnaires de protocole</span><span class="sxs-lookup"><span data-stu-id="0b95c-205">Developing Protocol Handlers</span></span>](-search-3x-wds-phaddins.md)
</dt> <dt>

[<span data-ttu-id="0b95c-206">Notification de l’index des modifications</span><span class="sxs-lookup"><span data-stu-id="0b95c-206">Notifying the Index of Changes</span></span>](-search-3x-wds-notifyingofchanges.md)
</dt> <dt>

[<span data-ttu-id="0b95c-207">Ajout d’icônes et de menus contextuels</span><span class="sxs-lookup"><span data-stu-id="0b95c-207">Adding Icons and Context Menus</span></span>](-search-3x-wds-ph-ui-extensions.md)
</dt> <dt>

[<span data-ttu-id="0b95c-208">Exemple de code : extensions de Shell pour les gestionnaires de protocole</span><span class="sxs-lookup"><span data-stu-id="0b95c-208">Code Sample: Shell Extensions for Protocol Handlers</span></span>](-search-3x-wds-ph-ui-samplecode.md)
</dt> <dt>

[<span data-ttu-id="0b95c-209">Installation et inscription de gestionnaires de protocole</span><span class="sxs-lookup"><span data-stu-id="0b95c-209">Installing and Registering Protocol Handlers</span></span>](-search-3x-wds-ph-install-registration.md)
</dt> <dt>

[<span data-ttu-id="0b95c-210">Débogage de gestionnaires de protocole</span><span class="sxs-lookup"><span data-stu-id="0b95c-210">Debugging Protocol Handlers</span></span>](-search-ws-protocolhandlertesting.md)
</dt> </dl>

 

 
