---
description: Un tableau d’associations est une liste ordonnée d’emplacements de Registre utilisée pour stocker des informations sur un type d’élément, y compris les gestionnaires, les verbes et d’autres attributs, tels que l’icône et le nom d’affichage du type.
title: Tableaux d’association
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 9ECD19CA-833E-4565-A0EF-FB16BF7B3F44
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 75d42a8758e5c6380414c7b93979b4f93cafd013
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104112771"
---
# <a name="association-arrays"></a><span data-ttu-id="101db-103">Tableaux d’association</span><span class="sxs-lookup"><span data-stu-id="101db-103">Association Arrays</span></span>

<span data-ttu-id="101db-104">Un tableau d’associations est une liste ordonnée d’emplacements de Registre utilisée pour stocker des informations sur un type d’élément, y compris les gestionnaires, les verbes et d’autres attributs, tels que l’icône et le nom d’affichage du type.</span><span class="sxs-lookup"><span data-stu-id="101db-104">An association array is an ordered list of registry locations used to store information about an item type, including handlers, verbs, and other attributes like the icon and display name of the type.</span></span> <span data-ttu-id="101db-105">L’interpréteur de commandes utilise des tableaux d’association pour interroger un ensemble prédéfini d’emplacements de Registre qui peut contenir des informations sur un élément de Shell.</span><span class="sxs-lookup"><span data-stu-id="101db-105">The Shell uses association arrays to query a predefined set of registry locations that might contain information about a Shell item.</span></span>

<span data-ttu-id="101db-106">Cette rubrique est organisée comme suit :</span><span class="sxs-lookup"><span data-stu-id="101db-106">This topic is organized as follows:</span></span>

-   [<span data-ttu-id="101db-107">À propos des tableaux d’association</span><span class="sxs-lookup"><span data-stu-id="101db-107">About Association Arrays</span></span>](#about-association-arrays)
-   [<span data-ttu-id="101db-108">Interrogation des tableaux d’association</span><span class="sxs-lookup"><span data-stu-id="101db-108">Querying Association Arrays</span></span>](#querying-association-arrays)
-   [<span data-ttu-id="101db-109">Utilisation de tableaux d’association pour une source de données Shell particulière</span><span class="sxs-lookup"><span data-stu-id="101db-109">Working with Association Arrays for a Particular Shell Data Source</span></span>](#working-with-association-arrays-for-a-particular-shell-data-source)
    -   [<span data-ttu-id="101db-110">Groupes d’associations de la source de données Shell</span><span class="sxs-lookup"><span data-stu-id="101db-110">Shell Data Source Association Arrays</span></span>](#shell-data-source-association-arrays)
-   [<span data-ttu-id="101db-111">Ressources supplémentaires</span><span class="sxs-lookup"><span data-stu-id="101db-111">Additional Resources</span></span>](#additional-resources)
-   [<span data-ttu-id="101db-112">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="101db-112">Related topics</span></span>](#related-topics)

## <a name="about-association-arrays"></a><span data-ttu-id="101db-113">À propos des tableaux d’association</span><span class="sxs-lookup"><span data-stu-id="101db-113">About Association Arrays</span></span>

<span data-ttu-id="101db-114">Un tableau d’associations est une liste ordonnée d’emplacements de Registre qui contiennent des informations sur un type d’élément, y compris les gestionnaires, les verbes et d’autres attributs tels que l’icône et le nom d’affichage du type.</span><span class="sxs-lookup"><span data-stu-id="101db-114">An association array is an ordered list of registry locations that contain information about an item type, including handlers, verbs, and other attributes such as the icon and display name of the type.</span></span> <span data-ttu-id="101db-115">Ces informations sur le type d’élément peuvent être enregistrées à différents niveaux de spécificité.</span><span class="sxs-lookup"><span data-stu-id="101db-115">This information about the item type can be registered at varying levels of specificity.</span></span> <span data-ttu-id="101db-116">Par exemple, vous pouvez inscrire un verbe qui s’affichera uniquement pour un type de fichier spécifique (tel que. jpg) ou pour tous les éléments ayant le même System. Kind (par exemple, System. Kind = image) ou pour tous les éléments.</span><span class="sxs-lookup"><span data-stu-id="101db-116">For example, you can register a verb that will show up only for a specific file type (such as .jpg), or for all items with the same System.Kind (for example, System.kind = picture), or for all items.</span></span>

<span data-ttu-id="101db-117">L’interpréteur de commandes utilise des tableaux d’association pour interroger un ensemble prédéfini d’emplacements du Registre susceptibles de contenir des informations sur l’élément.</span><span class="sxs-lookup"><span data-stu-id="101db-117">The Shell uses association arrays to query a predefined set of registry locations that might potentially contain information about the item.</span></span> <span data-ttu-id="101db-118">Les API de tableau d’association peuvent être utilisées pour extraire de la sous-clé de Registre une valeur unique qui contient les informations demandées, avec cette valeur provenant de la première entrée du tableau qui le fournit.</span><span class="sxs-lookup"><span data-stu-id="101db-118">The association array APIs can be used to retrieve from the registry subkey a single value that contains the requested information, with that value coming from the first entry in the array that provides it.</span></span> <span data-ttu-id="101db-119">Par exemple, la valeur de l’icône par défaut est Récupérée de cette façon.</span><span class="sxs-lookup"><span data-stu-id="101db-119">For example, the default icon value is retrieved this way.</span></span> <span data-ttu-id="101db-120">Le tableau d’association peut également être utilisé pour récupérer un ensemble de valeurs stockées dans les sous-clés du Registre.</span><span class="sxs-lookup"><span data-stu-id="101db-120">The association array can also be used to retrieve a set of values that are stored in the registry subkeys.</span></span> <span data-ttu-id="101db-121">Par exemple, la liste de verbes est créée à partir de ces verbes inscrits sous toutes les sous-clés.</span><span class="sxs-lookup"><span data-stu-id="101db-121">For example, the list of verbs is built from those verbs that are registered under all the subkeys.</span></span>

<span data-ttu-id="101db-122">Une fois que l’interpréteur de commandes a retenu un ensemble prédéfini d’emplacements de Registre pour obtenir des informations sur un élément de Shell, il place les emplacements du Registre dans un tableau dans l’ordre de l’emplacement le plus spécifique au plus général.</span><span class="sxs-lookup"><span data-stu-id="101db-122">After the Shell queries a predefined set of registry locations for information about a Shell item, it puts the registry locations into an array in order from the most specific location to the most general.</span></span>

<span data-ttu-id="101db-123">Étant donné que les tableaux d’association sont des listes triées, ils fournissent aux développeurs d’applications un mécanisme permettant d’ajouter des informations au registre qui seront retournées pour un type d’élément spécifique.</span><span class="sxs-lookup"><span data-stu-id="101db-123">Because association arrays are ordered lists, they provide application developers with a mechanism for adding information to the registry that will be returned for a specific type of item.</span></span> <span data-ttu-id="101db-124">De même, les tableaux d’association permettent aux développeurs d’applications d’ajouter des informations au registre pour un groupe spécifique d’éléments lorsque ces éléments sont inscrits à un emplacement plus général.</span><span class="sxs-lookup"><span data-stu-id="101db-124">Likewise, association arrays permit application developers to add information to the registry for a specific group of items when those items are registered at a more general location.</span></span> <span data-ttu-id="101db-125">Cette logique informe votre décision sur l’emplacement le plus approprié dans le registre pour stocker des informations sur les éléments de l’interpréteur de commandes.</span><span class="sxs-lookup"><span data-stu-id="101db-125">This logic informs your decision about the most appropriate location in the registry to store information about Shell items.</span></span>

<span data-ttu-id="101db-126">Sur un système Windows par défaut, un fichier. jpg contient le tableau d’association suivant :</span><span class="sxs-lookup"><span data-stu-id="101db-126">On a default Windows system a .jpg file has the following association array:</span></span>

-   <span data-ttu-id="101db-127">**HKEY \_ Jpgfile \_ racine des classes** \\ </span><span class="sxs-lookup"><span data-stu-id="101db-127">**HKEY\_CLASSES\_ROOT**\\**jpgfile**</span></span>
-   <span data-ttu-id="101db-128">**HKEY \_ CLASSES \_ racine** \\ **SystemFileAssociations** \\ **. jpg**</span><span class="sxs-lookup"><span data-stu-id="101db-128">**HKEY\_CLASSES\_ROOT**\\**SystemFileAssociations**\\ **.jpg**</span></span>
-   <span data-ttu-id="101db-129">**HKEY \_ Image \_ racine des classes** \\ </span><span class="sxs-lookup"><span data-stu-id="101db-129">**HKEY\_CLASSES\_ROOT**\\**image**</span></span>
-   <span data-ttu-id="101db-130">**HKEY \_ CLASSES \_ racine** \\ \* *\** _</span><span class="sxs-lookup"><span data-stu-id="101db-130">**HKEY\_CLASSES\_ROOT**\\**\** _</span></span>
-   <span data-ttu-id="101db-131">_ *\_ \_ **\\** AllFilesystemObjects racine des classes HKEY*\*</span><span class="sxs-lookup"><span data-stu-id="101db-131">_ *HKEY\_CLASSES\_ROOT **\\** AllFilesystemObjects*\*</span></span>

<span data-ttu-id="101db-132">Pour plus d’informations sur l’inscription des tableaux [d'](app-registration.md)Association, consultez inscription des applications.</span><span class="sxs-lookup"><span data-stu-id="101db-132">For information on registering association arrays, see [Application Registration](app-registration.md).</span></span>

## <a name="querying-association-arrays"></a><span data-ttu-id="101db-133">Interrogation des tableaux d’association</span><span class="sxs-lookup"><span data-stu-id="101db-133">Querying Association Arrays</span></span>

<span data-ttu-id="101db-134">Il existe des API Shell permettant de récupérer des informations à partir d’une plage de sous-clés de Registre, de la sous-clé de registre la plus spécifique à un sur-ensemble des informations sur toutes les sous-clés du Registre.</span><span class="sxs-lookup"><span data-stu-id="101db-134">There are Shell APIs to retrieve information from a range of registry subkeys, from the most specific registry subkey to a superset of the information across all registry subkeys.</span></span>

<span data-ttu-id="101db-135">L’utilisation la plus courante d’un tableau d’association consiste à interroger une valeur unique que l’interpréteur de commandes retourne à partir de l’élément le plus spécifique dans le tableau qui contient les informations demandées.</span><span class="sxs-lookup"><span data-stu-id="101db-135">The most common use of an association array is to query for a single value that the Shell returns from the most specific element in the array that has the requested information.</span></span> <span data-ttu-id="101db-136">L’exemple de code suivant montre comment procéder.</span><span class="sxs-lookup"><span data-stu-id="101db-136">The following code example shows how to do that.</span></span>


```
IQueryAssociations *pqa;

// pShellItem is assumed to be an existing IShellItem object.
hr = pShellItem->BindToHandler(NULL, BHID_AssociationArray, IID_PPV_ARGS(&pqa));
if (SUCCEEDED(hr))
{
    wchar_t szValue[256];
    DWORD cbValue = sizeof(szValue);      // Count of bytes in the array

    hr = pqa->GetData(0, ASSOCDATA_VALUE, L"InfoTip", szValue, &cbValue);
    if (SUCCEEDED(hr))
    {
        // The "InfoTip" value is used to compute the infotip string from
        // properties of an item.
    }
    pqa->Release();
}
```



<span data-ttu-id="101db-137">Les API suivantes peuvent être utilisées pour interroger un tableau d’association ou pour construire un objet [**IQueryAssociations**](/windows/win32/api/shlwapi/nn-shlwapi-iqueryassociations) de tableau d’association pouvant être interrogé :</span><span class="sxs-lookup"><span data-stu-id="101db-137">The following APIs can be used to query an association array or to construct an association array [**IQueryAssociations**](/windows/win32/api/shlwapi/nn-shlwapi-iqueryassociations) object that can be queried:</span></span>

-   <span data-ttu-id="101db-138">[**AssocCreate**](/windows/desktop/api/Shlwapi/nf-shlwapi-assoccreate) (avant Windows Vista)</span><span class="sxs-lookup"><span data-stu-id="101db-138">[**AssocCreate**](/windows/desktop/api/Shlwapi/nf-shlwapi-assoccreate) (prior to Windows Vista)</span></span>
-   [<span data-ttu-id="101db-139">**AssocCreateForClasses**</span><span class="sxs-lookup"><span data-stu-id="101db-139">**AssocCreateForClasses**</span></span>](/windows/desktop/api/Shellapi/nf-shellapi-assoccreateforclasses)
-   [<span data-ttu-id="101db-140">**AssocQueryString**</span><span class="sxs-lookup"><span data-stu-id="101db-140">**AssocQueryString**</span></span>](/windows/desktop/api/Shlwapi/nf-shlwapi-assocquerystringa)

## <a name="working-with-association-arrays-for-a-particular-shell-data-source"></a><span data-ttu-id="101db-141">Utilisation de tableaux d’association pour une source de données Shell particulière</span><span class="sxs-lookup"><span data-stu-id="101db-141">Working with Association Arrays for a Particular Shell Data Source</span></span>

<span data-ttu-id="101db-142">Chaque source de données de Shell définit le tableau d’association pour ses éléments.</span><span class="sxs-lookup"><span data-stu-id="101db-142">Each Shell data source defines the association array for its items.</span></span> <span data-ttu-id="101db-143">La définition d’un tableau d’associations est généralement une fonction du type d’élément.</span><span class="sxs-lookup"><span data-stu-id="101db-143">Defining an association array is usually a function of the type of item.</span></span> <span data-ttu-id="101db-144">Les implémenteurs de sources de données Shell doivent définir et documenter les tableaux d’association pour permettre aux applications d’étendre le comportement de ces types, par exemple pour inscrire des verbes ou d’autres informations.</span><span class="sxs-lookup"><span data-stu-id="101db-144">Shell data source implementers should define and document the association arrays to enable applications to extend the behavior of those types, such as for registering verbs or other information.</span></span> <span data-ttu-id="101db-145">Les applications peuvent étendre le comportement des éléments en fonction de l’ajout de données aux sous-clés du tableau d’association, telles que l’ajout de verbes pour les éléments.</span><span class="sxs-lookup"><span data-stu-id="101db-145">Applications can extend the behavior of items based on adding data to the association array subkeys, such as adding verbs for items.</span></span>

<span data-ttu-id="101db-146">La source de données du système de fichiers crée un tableau d’association pour les fichiers basés sur les sous-clés de Registre suivantes et les ProgID spéciaux :</span><span class="sxs-lookup"><span data-stu-id="101db-146">The file system data source builds an association array for files based on the following registry subkeys and special ProgIDs:</span></span>

-   <span data-ttu-id="101db-147">Si le fichier contient un ProgID enregistré, le ProgID **\_ \_ racine de la classe HKEY** \\  est utilisé.</span><span class="sxs-lookup"><span data-stu-id="101db-147">If the file has a registered ProgID, **HKEY\_CLASSES\_ROOT**\\*ProgID* is used.</span></span> <span data-ttu-id="101db-148">Sinon, la racine de la racine de la **\_ \_ classe HKEY** \\  est utilisée.</span><span class="sxs-lookup"><span data-stu-id="101db-148">Otherwise **HKEY\_CLASSES\_ROOT**\\**Unknown** is used.</span></span>
-   <span data-ttu-id="101db-149">L’extension de nom de fichier est inscrite sous la **\_ \_** \\  \\ sous-clé SystemFileAssociations *. FileExtension* racine de la classe HKEY.</span><span class="sxs-lookup"><span data-stu-id="101db-149">The file name extension is registered under **HKEY\_CLASSES\_ROOT**\\**SystemFileAssociations**\\ *.fileExtension* subkey.</span></span>
-   <span data-ttu-id="101db-150">Les ProgID spéciaux sont répertoriés dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="101db-150">Special ProgIDs are shown in the following table.</span></span> 

    | <span data-ttu-id="101db-151">ProgID spécial</span><span class="sxs-lookup"><span data-stu-id="101db-151">Special progID</span></span>                                    | <span data-ttu-id="101db-152">Description</span><span class="sxs-lookup"><span data-stu-id="101db-152">Description</span></span>                   |
    |---------------------------------------------------|-------------------------------|
    | <span data-ttu-id="101db-153">**HKEY \_ CLASSES \_ racine** \\ \* *\** _</span><span class="sxs-lookup"><span data-stu-id="101db-153">**HKEY\_CLASSES\_ROOT**\\**\** _</span></span>                   | <span data-ttu-id="101db-154">Tous les fichiers (sans dossiers)</span><span class="sxs-lookup"><span data-stu-id="101db-154">All files (non-folders)</span></span>       |
    | <span data-ttu-id="101db-155">_ *\_ \_ **\\** AllFilesystemObjects racine des classes HKEY*\*</span><span class="sxs-lookup"><span data-stu-id="101db-155">_ *HKEY\_CLASSES\_ROOT **\\** AllFilesystemObjects*\*</span></span> | <span data-ttu-id="101db-156">Fichiers et dossiers du système de fichiers</span><span class="sxs-lookup"><span data-stu-id="101db-156">Files and file system folders</span></span> |
    | <span data-ttu-id="101db-157">**HKEY \_ Répertoire \_ racine des classes** \\ </span><span class="sxs-lookup"><span data-stu-id="101db-157">**HKEY\_CLASSES\_ROOT**\\**Directory**</span></span>            | <span data-ttu-id="101db-158">Dossiers du système de fichiers</span><span class="sxs-lookup"><span data-stu-id="101db-158">File system folders</span></span>           |
    | <span data-ttu-id="101db-159">**HKEY \_ Dossier \_ racine des classes** \\ </span><span class="sxs-lookup"><span data-stu-id="101db-159">**HKEY\_CLASSES\_ROOT**\\**Folder**</span></span>               | <span data-ttu-id="101db-160">Conteneurs de Shell</span><span class="sxs-lookup"><span data-stu-id="101db-160">Shell containers</span></span>              |

    

     

### <a name="shell-data-source-association-arrays"></a><span data-ttu-id="101db-161">Groupes d’associations de la source de données Shell</span><span class="sxs-lookup"><span data-stu-id="101db-161">Shell Data Source Association Arrays</span></span>

<span data-ttu-id="101db-162">La liste suivante représente certains des tableaux d’association du magasin de données Shell qui peuvent être utilisés pour les opérations décrites dans cette rubrique :</span><span class="sxs-lookup"><span data-stu-id="101db-162">The following list represents some of the Shell data store association arrays that can be used for the purposes described in this topic:</span></span>

-   <span data-ttu-id="101db-163">**HKEY \_ CLASSES \_ racine** \\ \* *\** _</span><span class="sxs-lookup"><span data-stu-id="101db-163">**HKEY\_CLASSES\_ROOT**\\**\** _</span></span>
-   <span data-ttu-id="101db-164">_ *\_ \_ **\\** AllFilesystemObjects racine des classes HKEY*\*</span><span class="sxs-lookup"><span data-stu-id="101db-164">_ *HKEY\_CLASSES\_ROOT **\\** AllFilesystemObjects*\*</span></span>
-   <span data-ttu-id="101db-165">**HKEY \_ CLASSES \_ racine** \\ **Kind.Document**</span><span class="sxs-lookup"><span data-stu-id="101db-165">**HKEY\_CLASSES\_ROOT**\\**Kind.Document**</span></span>
-   <span data-ttu-id="101db-166">**HKEY \_ Résultats des classes \_ racine** \\ </span><span class="sxs-lookup"><span data-stu-id="101db-166">**HKEY\_CLASSES\_ROOT**\\**Results**</span></span>
-   <span data-ttu-id="101db-167">**HKEY \_ CLASSES \_ racine** \\ **SystemFileAssociations** \\ **. docx**</span><span class="sxs-lookup"><span data-stu-id="101db-167">**HKEY\_CLASSES\_ROOT**\\**SystemFileAssociations**\\ **.docx**</span></span>
-   <span data-ttu-id="101db-168">**HKEY \_ CLASSES \_ racine** \\ **Word.Document. 12**</span><span class="sxs-lookup"><span data-stu-id="101db-168">**HKEY\_CLASSES\_ROOT**\\**Word.Document.12**</span></span>

<span data-ttu-id="101db-169">Les tableaux d’association de la source de données Shell qui peuvent être utilisés pour DBFolder (un magasin de données Shell qui représente des éléments dans les résultats de recherche et les vues basées sur des requêtes) sont les suivants :</span><span class="sxs-lookup"><span data-stu-id="101db-169">Shell data source association arrays that can be used for DBFolder (a Shell data store that represents items in search results and query-based views) are as follows:</span></span>

-   <span data-ttu-id="101db-170">Lecteurs</span><span class="sxs-lookup"><span data-stu-id="101db-170">Drives</span></span>
-   <span data-ttu-id="101db-171">Réseau</span><span class="sxs-lookup"><span data-stu-id="101db-171">Network</span></span>
-   <span data-ttu-id="101db-172">RegItems</span><span class="sxs-lookup"><span data-stu-id="101db-172">RegItems</span></span>
-   <span data-ttu-id="101db-173">Exemples :</span><span class="sxs-lookup"><span data-stu-id="101db-173">Examples:</span></span>
    -   <span data-ttu-id="101db-174">ContentView</span><span class="sxs-lookup"><span data-stu-id="101db-174">ContentView</span></span>
    -   <span data-ttu-id="101db-175">Verbes et adverbes</span><span class="sxs-lookup"><span data-stu-id="101db-175">Verbs</span></span>

<span data-ttu-id="101db-176">D’autres groupes d’associations communs incluent le dossier et les imprimantes.</span><span class="sxs-lookup"><span data-stu-id="101db-176">Other common association arrays include Folder and Printers.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="101db-177">Ressources supplémentaires</span><span class="sxs-lookup"><span data-stu-id="101db-177">Additional Resources</span></span>

-   <span data-ttu-id="101db-178">Pour créer un magasin de données Shell, consultez [implémentation des interfaces d’objet de dossier de base](nse-implement.md).</span><span class="sxs-lookup"><span data-stu-id="101db-178">To create a Shell data store, see [Implementing the Basic Folder Object Interfaces](nse-implement.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="101db-179">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="101db-179">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="101db-180">Inscription de l’application</span><span class="sxs-lookup"><span data-stu-id="101db-180">Application Registration</span></span>](app-registration.md)
</dt> <dt>

[<span data-ttu-id="101db-181">Types de fichiers</span><span class="sxs-lookup"><span data-stu-id="101db-181">File Types</span></span>](fa-file-types.md)
</dt> <dt>

[<span data-ttu-id="101db-182">Fonctionnement des associations de fichiers</span><span class="sxs-lookup"><span data-stu-id="101db-182">How File Associations Work</span></span>](fa-how-work.md)
</dt> <dt>

[<span data-ttu-id="101db-183">Affichage du contenu par type de fichier ou par type</span><span class="sxs-lookup"><span data-stu-id="101db-183">Content View By File Type or Kind</span></span>](prophand-content-view.md)
</dt> <dt>

[<span data-ttu-id="101db-184">Vérificateur de type de fichier</span><span class="sxs-lookup"><span data-stu-id="101db-184">File Type Verifier</span></span>](file-type-verifier.md)
</dt> <dt>

[<span data-ttu-id="101db-185">Gestionnaires de types de fichiers</span><span class="sxs-lookup"><span data-stu-id="101db-185">File Type Handlers</span></span>](fa-file-extensions.md)
</dt> <dt>

[<span data-ttu-id="101db-186">Identificateurs programmatiques</span><span class="sxs-lookup"><span data-stu-id="101db-186">Programmatic Identifiers</span></span>](fa-progids.md)
</dt> <dt>

[<span data-ttu-id="101db-187">Types perçus</span><span class="sxs-lookup"><span data-stu-id="101db-187">Perceived Types</span></span>](fa-perceivedtypes.md)
</dt> </dl>

 

 
