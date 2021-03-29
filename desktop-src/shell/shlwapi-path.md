---
description: Cette section décrit les fonctions de gestion du chemin d’accès de l’interpréteur de commandes Windows. Les éléments de programmation expliqués dans cette documentation sont exportés par Shlwapi.dll et définis dans Shlwapi. h et Shlwapi. lib.
title: Fonctions de gestion du chemin de Shell
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 31c4afa9-2030-4714-a98b-ed895c9c28a0
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 8ed0a5e0f2e91a2e647af461ee6679a5542d28b7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104991760"
---
# <a name="shell-path-handling-functions"></a><span data-ttu-id="b4f66-104">Fonctions de gestion du chemin de Shell</span><span class="sxs-lookup"><span data-stu-id="b4f66-104">Shell Path Handling Functions</span></span>

<span data-ttu-id="b4f66-105">Cette section décrit les fonctions de gestion du chemin d’accès de l’interpréteur de commandes Windows.</span><span class="sxs-lookup"><span data-stu-id="b4f66-105">This section describes the Windows Shell path handling functions.</span></span> <span data-ttu-id="b4f66-106">Les éléments de programmation expliqués dans cette documentation sont exportés par Shlwapi.dll et définis dans Shlwapi. h et Shlwapi. lib.</span><span class="sxs-lookup"><span data-stu-id="b4f66-106">The programming elements explained in this documentation are exported by Shlwapi.dll and defined in Shlwapi.h and Shlwapi.lib.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="b4f66-107">Contenu de cette section</span><span class="sxs-lookup"><span data-stu-id="b4f66-107">In this section</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="b4f66-108">Rubrique</span><span class="sxs-lookup"><span data-stu-id="b4f66-108">Topic</span></span></th>
<th><span data-ttu-id="b4f66-109">Description</span><span class="sxs-lookup"><span data-stu-id="b4f66-109">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="b4f66-110"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathaddbackslasha"><strong>PathAddBackslash</strong></a></span><span class="sxs-lookup"><span data-stu-id="b4f66-110"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathaddbackslasha"><strong>PathAddBackslash</strong></a></span></span><br/></td>
<td><span data-ttu-id="b4f66-111">Ajoute une barre oblique inverse à la fin d’une chaîne pour créer la syntaxe correcte pour un chemin d’accès.</span><span class="sxs-lookup"><span data-stu-id="b4f66-111">Adds a backslash to the end of a string to create the correct syntax for a path.</span></span> <span data-ttu-id="b4f66-112">Si le chemin d’accès source contient déjà une barre oblique inverse de fin, aucune barre oblique inverse n’est ajoutée.</span><span class="sxs-lookup"><span data-stu-id="b4f66-112">If the source path already has a trailing backslash, no backslash will be added.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="b4f66-113">Une utilisation incorrecte de cette fonction peut entraîner un dépassement de mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="b4f66-113">Misuse of this function can lead to a buffer overrun.</span></span> <span data-ttu-id="b4f66-114">Nous vous recommandons d’utiliser la fonction <a href="/windows/desktop/api/pathcch/nf-pathcch-pathcchaddbackslash"><strong>PathCchAddBackslash</strong></a> ou <a href="/windows/desktop/api/pathcch/nf-pathcch-pathcchaddbackslashex"><strong>PathCchAddBackslashEx</strong></a> plus sûre à la place.</span><span class="sxs-lookup"><span data-stu-id="b4f66-114">We recommend the use of the safer <a href="/windows/desktop/api/pathcch/nf-pathcch-pathcchaddbackslash"><strong>PathCchAddBackslash</strong></a> or <a href="/windows/desktop/api/pathcch/nf-pathcch-pathcchaddbackslashex"><strong>PathCchAddBackslashEx</strong></a> function in its place.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b4f66-115"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathaddextensiona"><strong>PathAddExtension</strong></a></span><span class="sxs-lookup"><span data-stu-id="b4f66-115"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathaddextensiona"><strong>PathAddExtension</strong></a></span></span><br/></td>
<td><span data-ttu-id="b4f66-116">Ajoute une extension de nom de fichier à une chaîne de chemin d’accès.</span><span class="sxs-lookup"><span data-stu-id="b4f66-116">Adds a file name extension to a path string.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="b4f66-117">Une utilisation incorrecte de cette fonction peut entraîner un dépassement de mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="b4f66-117">Misuse of this function can lead to a buffer overrun.</span></span> <span data-ttu-id="b4f66-118">Nous vous recommandons d’utiliser la fonction <a href="/windows/desktop/api/pathcch/nf-pathcch-pathcchaddextension"><strong>PathCchAddExtension</strong></a> plus sûre à la place.</span><span class="sxs-lookup"><span data-stu-id="b4f66-118">We recommend the use of the safer <a href="/windows/desktop/api/pathcch/nf-pathcch-pathcchaddextension"><strong>PathCchAddExtension</strong></a> function in its place.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b4f66-119"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathappenda"><strong>PathAppend</strong></a></span><span class="sxs-lookup"><span data-stu-id="b4f66-119"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathappenda"><strong>PathAppend</strong></a></span></span><br/></td>
<td><span data-ttu-id="b4f66-120">Ajoute un chemin d’accès à la fin d’un autre.</span><span class="sxs-lookup"><span data-stu-id="b4f66-120">Appends one path to the end of another.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="b4f66-121">Une utilisation incorrecte de cette fonction peut entraîner un dépassement de mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="b4f66-121">Misuse of this function can lead to a buffer overrun.</span></span> <span data-ttu-id="b4f66-122">Nous vous recommandons d’utiliser la fonction <a href="/windows/desktop/api/pathcch/nf-pathcch-pathcchappend"><strong>PathCchAppend</strong></a> ou <a href="/windows/desktop/api/pathcch/nf-pathcch-pathcchappendex"><strong>PathCchAppendEx</strong></a> plus sûre à la place.</span><span class="sxs-lookup"><span data-stu-id="b4f66-122">We recommend the use of the safer <a href="/windows/desktop/api/pathcch/nf-pathcch-pathcchappend"><strong>PathCchAppend</strong></a> or <a href="/windows/desktop/api/pathcch/nf-pathcch-pathcchappendex"><strong>PathCchAppendEx</strong></a> function in its place.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b4f66-123"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathbuildroota"><strong>PathBuildRoot</strong></a></span><span class="sxs-lookup"><span data-stu-id="b4f66-123"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathbuildroota"><strong>PathBuildRoot</strong></a></span></span><br/></td>
<td><span data-ttu-id="b4f66-124">Crée un chemin d’accès racine à partir d’un numéro de lecteur donné.</span><span class="sxs-lookup"><span data-stu-id="b4f66-124">Creates a root path from a given drive number.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b4f66-125"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathcanonicalizea"><strong>PathCanonicalize</strong></a></span><span class="sxs-lookup"><span data-stu-id="b4f66-125"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathcanonicalizea"><strong>PathCanonicalize</strong></a></span></span><br/></td>
<td><span data-ttu-id="b4f66-126">Simplifie un tracé en supprimant des éléments de navigation tels que &quot; . &quot; et &quot; .. &quot; pour produire un chemin d’accès direct et correctement formé.</span><span class="sxs-lookup"><span data-stu-id="b4f66-126">Simplifies a path by removing navigation elements such as &quot;.&quot; and &quot;..&quot; to produce a direct, well-formed path.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b4f66-127"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathcombinea"><strong>PathCombine</strong></a></span><span class="sxs-lookup"><span data-stu-id="b4f66-127"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathcombinea"><strong>PathCombine</strong></a></span></span><br/></td>
<td><span data-ttu-id="b4f66-128">Concatène deux chaînes qui représentent les chemins d’accès formés correctement dans un chemin d’accès ; concatène également tous les éléments de chemin d’accès relatifs.</span><span class="sxs-lookup"><span data-stu-id="b4f66-128">Concatenates two strings that represent properly formed paths into one path; also concatenates any relative path elements.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="b4f66-129">Une utilisation incorrecte de cette fonction peut entraîner un dépassement de mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="b4f66-129">Misuse of this function can lead to a buffer overrun.</span></span> <span data-ttu-id="b4f66-130">Nous vous recommandons d’utiliser la fonction <a href="/windows/desktop/api/pathcch/nf-pathcch-pathcchcombine"><strong>PathCchCombine</strong></a> ou <a href="/windows/desktop/api/pathcch/nf-pathcch-pathcchcombineex"><strong>PathCchCombineEx</strong></a> plus sûre à la place.</span><span class="sxs-lookup"><span data-stu-id="b4f66-130">We recommend the use of the safer <a href="/windows/desktop/api/pathcch/nf-pathcch-pathcchcombine"><strong>PathCchCombine</strong></a> or <a href="/windows/desktop/api/pathcch/nf-pathcch-pathcchcombineex"><strong>PathCchCombineEx</strong></a> function in its place.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b4f66-131"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathcommonprefixa"><strong>PathCommonPrefix</strong></a></span><span class="sxs-lookup"><span data-stu-id="b4f66-131"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathcommonprefixa"><strong>PathCommonPrefix</strong></a></span></span><br/></td>
<td><span data-ttu-id="b4f66-132">Compare deux chemins d’accès pour déterminer s’ils partagent un préfixe commun.</span><span class="sxs-lookup"><span data-stu-id="b4f66-132">Compares two paths to determine if they share a common prefix.</span></span> <span data-ttu-id="b4f66-133">Un préfixe est l’un des types suivants : &quot; C : \\ &quot; , &quot; . &quot; , &quot; .. &quot; , &quot; .. \\ &quot; .</span><span class="sxs-lookup"><span data-stu-id="b4f66-133">A prefix is one of these types: &quot;C:\\&quot;, &quot;.&quot;, &quot;..&quot;, &quot;..\\&quot;.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b4f66-134"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathcompactpatha"><strong>PathCompactPath</strong></a></span><span class="sxs-lookup"><span data-stu-id="b4f66-134"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathcompactpatha"><strong>PathCompactPath</strong></a></span></span><br/></td>
<td><span data-ttu-id="b4f66-135">Tronque un chemin d’accès de fichier pour qu’il s’ajuste à une largeur de pixel donnée en remplaçant les composants de tracé par des ellipses.</span><span class="sxs-lookup"><span data-stu-id="b4f66-135">Truncates a file path to fit within a given pixel width by replacing path components with ellipses.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b4f66-136"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathcompactpathexa"><strong>PathCompactPathEx</strong></a></span><span class="sxs-lookup"><span data-stu-id="b4f66-136"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathcompactpathexa"><strong>PathCompactPathEx</strong></a></span></span><br/></td>
<td><span data-ttu-id="b4f66-137">Tronque un tracé pour qu’il s’ajuste à un certain nombre de caractères en remplaçant les composants du tracé par des ellipses.</span><span class="sxs-lookup"><span data-stu-id="b4f66-137">Truncates a path to fit within a certain number of characters by replacing path components with ellipses.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b4f66-138"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathcreatefromurla"><strong>PathCreateFromUrl</strong></a></span><span class="sxs-lookup"><span data-stu-id="b4f66-138"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathcreatefromurla"><strong>PathCreateFromUrl</strong></a></span></span><br/></td>
<td><span data-ttu-id="b4f66-139">Convertit une URL de fichier en un chemin d’accès Microsoft MS-DOS.</span><span class="sxs-lookup"><span data-stu-id="b4f66-139">Converts a file URL to a Microsoft MS-DOS path.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b4f66-140"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathcreatefromurlalloc"><strong>PathCreateFromUrlAlloc</strong></a></span><span class="sxs-lookup"><span data-stu-id="b4f66-140"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathcreatefromurlalloc"><strong>PathCreateFromUrlAlloc</strong></a></span></span><br/></td>
<td><span data-ttu-id="b4f66-141">Crée un chemin d’accès à partir d’une URL de fichier.</span><span class="sxs-lookup"><span data-stu-id="b4f66-141">Creates a path from a file URL.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b4f66-142"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathfileexistsa"><strong>PathFileExists</strong></a></span><span class="sxs-lookup"><span data-stu-id="b4f66-142"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathfileexistsa"><strong>PathFileExists</strong></a></span></span><br/></td>
<td><span data-ttu-id="b4f66-143">Détermine si un chemin d’accès à un objet de système de fichiers, tel qu’un fichier ou un dossier, est valide.</span><span class="sxs-lookup"><span data-stu-id="b4f66-143">Determines whether a path to a file system object such as a file or folder is valid.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b4f66-144"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathfindextensiona"><strong>PathFindExtension</strong></a></span><span class="sxs-lookup"><span data-stu-id="b4f66-144"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathfindextensiona"><strong>PathFindExtension</strong></a></span></span><br/></td>
<td><span data-ttu-id="b4f66-145">Recherche une extension dans un chemin d’accès.</span><span class="sxs-lookup"><span data-stu-id="b4f66-145">Searches a path for an extension.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b4f66-146"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathfindfilenamea"><strong>PathFindFileName</strong></a></span><span class="sxs-lookup"><span data-stu-id="b4f66-146"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathfindfilenamea"><strong>PathFindFileName</strong></a></span></span><br/></td>
<td><span data-ttu-id="b4f66-147">Recherche un nom de fichier dans un chemin d’accès.</span><span class="sxs-lookup"><span data-stu-id="b4f66-147">Searches a path for a file name.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b4f66-148"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathfindnextcomponenta"><strong>PathFindNextComponent</strong></a></span><span class="sxs-lookup"><span data-stu-id="b4f66-148"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathfindnextcomponenta"><strong>PathFindNextComponent</strong></a></span></span><br/></td>
<td><span data-ttu-id="b4f66-149">Analyse un chemin d’accès et retourne la partie de ce chemin d’accès qui suit la première barre oblique inverse.</span><span class="sxs-lookup"><span data-stu-id="b4f66-149">Parses a path and returns the portion of that path that follows the first backslash.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b4f66-150"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathfindonpatha"><strong>PathFindOnPath</strong></a></span><span class="sxs-lookup"><span data-stu-id="b4f66-150"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathfindonpatha"><strong>PathFindOnPath</strong></a></span></span><br/></td>
<td><span data-ttu-id="b4f66-151">Recherche un fichier.</span><span class="sxs-lookup"><span data-stu-id="b4f66-151">Searches for a file.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b4f66-152"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathfindsuffixarraya"><strong>PathFindSuffixArray</strong></a></span><span class="sxs-lookup"><span data-stu-id="b4f66-152"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathfindsuffixarraya"><strong>PathFindSuffixArray</strong></a></span></span><br/></td>
<td><span data-ttu-id="b4f66-153">Détermine si un nom de fichier donné a une liste de suffixes.</span><span class="sxs-lookup"><span data-stu-id="b4f66-153">Determines whether a given file name has one of a list of suffixes.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b4f66-154"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathgetargsa"><strong>PathGetArgs</strong></a></span><span class="sxs-lookup"><span data-stu-id="b4f66-154"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathgetargsa"><strong>PathGetArgs</strong></a></span></span><br/></td>
<td><span data-ttu-id="b4f66-155">Recherche les arguments de ligne de commande dans un chemin d’accès donné.</span><span class="sxs-lookup"><span data-stu-id="b4f66-155">Finds the command line arguments within a given path.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b4f66-156"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathgetchartypea"><strong>PathGetCharType</strong></a></span><span class="sxs-lookup"><span data-stu-id="b4f66-156"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathgetchartypea"><strong>PathGetCharType</strong></a></span></span><br/></td>
<td><span data-ttu-id="b4f66-157">Détermine le type de caractère par rapport à un chemin d’accès.</span><span class="sxs-lookup"><span data-stu-id="b4f66-157">Determines the type of character in relation to a path.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b4f66-158"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathgetdrivenumbera"><strong>PathGetDriveNumber</strong></a></span><span class="sxs-lookup"><span data-stu-id="b4f66-158"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathgetdrivenumbera"><strong>PathGetDriveNumber</strong></a></span></span><br/></td>
<td><span data-ttu-id="b4f66-159">Recherche dans un chemin d’accès une lettre de lecteur comprise entre « A » et « Z » et retourne le numéro de lecteur correspondant.</span><span class="sxs-lookup"><span data-stu-id="b4f66-159">Searches a path for a drive letter within the range of 'A' to 'Z' and returns the corresponding drive number.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b4f66-160"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathiscontenttypea"><strong>PathIsContentType</strong></a></span><span class="sxs-lookup"><span data-stu-id="b4f66-160"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathiscontenttypea"><strong>PathIsContentType</strong></a></span></span><br/></td>
<td><span data-ttu-id="b4f66-161">Détermine si le type de contenu inscrit d’un fichier correspond au type de contenu spécifié.</span><span class="sxs-lookup"><span data-stu-id="b4f66-161">Determines if a file's registered content type matches the specified content type.</span></span> <span data-ttu-id="b4f66-162">Cette fonction obtient le type de contenu pour le type de fichier spécifié et compare cette chaîne avec le <em>pszContentType</em>.</span><span class="sxs-lookup"><span data-stu-id="b4f66-162">This function obtains the content type for the specified file type and compares that string with the <em>pszContentType</em>.</span></span> <span data-ttu-id="b4f66-163">La comparaison ne respecte pas la casse.</span><span class="sxs-lookup"><span data-stu-id="b4f66-163">The comparison is not case-sensitive.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b4f66-164"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathisdirectorya"><strong>PathIsDirectory</strong></a></span><span class="sxs-lookup"><span data-stu-id="b4f66-164"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathisdirectorya"><strong>PathIsDirectory</strong></a></span></span><br/></td>
<td><span data-ttu-id="b4f66-165">Vérifie qu’un chemin d’accès est un répertoire valide.</span><span class="sxs-lookup"><span data-stu-id="b4f66-165">Verifies that a path is a valid directory.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b4f66-166"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathisdirectoryemptya"><strong>PathIsDirectoryEmpty</strong></a></span><span class="sxs-lookup"><span data-stu-id="b4f66-166"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathisdirectoryemptya"><strong>PathIsDirectoryEmpty</strong></a></span></span><br/></td>
<td><span data-ttu-id="b4f66-167">Détermine si un chemin d’accès spécifié est un répertoire vide.</span><span class="sxs-lookup"><span data-stu-id="b4f66-167">Determines whether a specified path is an empty directory.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b4f66-168"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathisfilespeca"><strong>PathIsFileSpec</strong></a></span><span class="sxs-lookup"><span data-stu-id="b4f66-168"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathisfilespeca"><strong>PathIsFileSpec</strong></a></span></span><br/></td>
<td><span data-ttu-id="b4f66-169">Recherche un chemin d’accès pour tous les caractères délimitant les chemins d’accès (par exemple, ' : 'ou' \' ).</span><span class="sxs-lookup"><span data-stu-id="b4f66-169">Searches a path for any path-delimiting characters (for example, ':' or '\' ).</span></span> <span data-ttu-id="b4f66-170">Si aucun caractère de délimitation de chemin d’accès n’est présent, le chemin d’accès est considéré comme un chemin d’accès de spécifications de fichier.</span><span class="sxs-lookup"><span data-stu-id="b4f66-170">If there are no path-delimiting characters present, the path is considered to be a File Spec path.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b4f66-171"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathishtmlfilea"><strong>PathIsHTMLFile</strong></a></span><span class="sxs-lookup"><span data-stu-id="b4f66-171"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathishtmlfilea"><strong>PathIsHTMLFile</strong></a></span></span><br/></td>
<td><span data-ttu-id="b4f66-172">Détermine si un fichier est un fichier HTML.</span><span class="sxs-lookup"><span data-stu-id="b4f66-172">Determines if a file is an HTML file.</span></span> <span data-ttu-id="b4f66-173">La détermination est effectuée en fonction du type de contenu inscrit pour l’extension du fichier.</span><span class="sxs-lookup"><span data-stu-id="b4f66-173">The determination is made based on the content type that is registered for the file's extension.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b4f66-174"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathislfnfilespeca"><strong>PathIsLFNFileSpec</strong></a></span><span class="sxs-lookup"><span data-stu-id="b4f66-174"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathislfnfilespeca"><strong>PathIsLFNFileSpec</strong></a></span></span><br/></td>
<td><span data-ttu-id="b4f66-175">Détermine si un nom de fichier est au format long.</span><span class="sxs-lookup"><span data-stu-id="b4f66-175">Determines whether a file name is in long format.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b4f66-176"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathisnetworkpatha"><strong>PathIsNetworkPath</strong></a></span><span class="sxs-lookup"><span data-stu-id="b4f66-176"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathisnetworkpatha"><strong>PathIsNetworkPath</strong></a></span></span><br/></td>
<td><span data-ttu-id="b4f66-177">Détermine si une chaîne de chemin d’accès représente une ressource réseau.</span><span class="sxs-lookup"><span data-stu-id="b4f66-177">Determines whether a path string represents a network resource.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b4f66-178"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathisprefixa"><strong>PathIsPrefix</strong></a></span><span class="sxs-lookup"><span data-stu-id="b4f66-178"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathisprefixa"><strong>PathIsPrefix</strong></a></span></span><br/></td>
<td><span data-ttu-id="b4f66-179">Recherche un chemin d’accès pour déterminer s’il contient un préfixe valide du type passé par <em>pszPrefix</em>.</span><span class="sxs-lookup"><span data-stu-id="b4f66-179">Searches a path to determine if it contains a valid prefix of the type passed by <em>pszPrefix</em>.</span></span> <span data-ttu-id="b4f66-180">Un préfixe est l’un des types suivants : &quot; C : \\ &quot; , &quot; . &quot; , &quot; .. &quot; , &quot; .. \\ &quot; .</span><span class="sxs-lookup"><span data-stu-id="b4f66-180">A prefix is one of these types: &quot;C:\\&quot;, &quot;.&quot;, &quot;..&quot;, &quot;..\\&quot;.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b4f66-181"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathisrelativea"><strong>PathIsRelative</strong></a></span><span class="sxs-lookup"><span data-stu-id="b4f66-181"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathisrelativea"><strong>PathIsRelative</strong></a></span></span><br/></td>
<td><span data-ttu-id="b4f66-182">Recherche un chemin d’accès et détermine s’il est relatif.</span><span class="sxs-lookup"><span data-stu-id="b4f66-182">Searches a path and determines if it is relative.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b4f66-183"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathisroota"><strong>PathIsRoot</strong></a></span><span class="sxs-lookup"><span data-stu-id="b4f66-183"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathisroota"><strong>PathIsRoot</strong></a></span></span><br/></td>
<td><span data-ttu-id="b4f66-184">Détermine si une chaîne de chemin d’accès fait référence à la racine d’un volume.</span><span class="sxs-lookup"><span data-stu-id="b4f66-184">Determines whether a path string refers to the root of a volume.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b4f66-185"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathissameroota"><strong>PathIsSameRoot</strong></a></span><span class="sxs-lookup"><span data-stu-id="b4f66-185"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathissameroota"><strong>PathIsSameRoot</strong></a></span></span><br/></td>
<td><span data-ttu-id="b4f66-186">Compare deux chemins d’accès pour déterminer s’ils ont un composant racine commun.</span><span class="sxs-lookup"><span data-stu-id="b4f66-186">Compares two paths to determine if they have a common root component.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b4f66-187"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathissystemfoldera"><strong>PathIsSystemFolder</strong></a></span><span class="sxs-lookup"><span data-stu-id="b4f66-187"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathissystemfoldera"><strong>PathIsSystemFolder</strong></a></span></span><br/></td>
<td><span data-ttu-id="b4f66-188">Détermine si un dossier existant contient les attributs qui en font un dossier système.</span><span class="sxs-lookup"><span data-stu-id="b4f66-188">Determines if an existing folder contains the attributes that make it a system folder.</span></span> <span data-ttu-id="b4f66-189">Cette fonction indique également si certains attributs qualifient un dossier comme dossier système.</span><span class="sxs-lookup"><span data-stu-id="b4f66-189">Alternately, this function indicates if certain attributes qualify a folder to be a system folder.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b4f66-190"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathisunca"><strong>PathIsUNC</strong></a></span><span class="sxs-lookup"><span data-stu-id="b4f66-190"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathisunca"><strong>PathIsUNC</strong></a></span></span><br/></td>
<td><span data-ttu-id="b4f66-191">Détermine si une chaîne de chemin d’accès est un chemin d’accès UNC (Universal Naming Convention) valide, par opposition à un chemin d’accès basé sur une lettre de lecteur.</span><span class="sxs-lookup"><span data-stu-id="b4f66-191">Determines if a path string is a valid Universal Naming Convention (UNC) path, as opposed to a path based on a drive letter.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b4f66-192"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathisuncservera"><strong>PathIsUNCServer</strong></a></span><span class="sxs-lookup"><span data-stu-id="b4f66-192"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathisuncservera"><strong>PathIsUNCServer</strong></a></span></span><br/></td>
<td><span data-ttu-id="b4f66-193">Détermine si une chaîne est un UNC valide pour un chemin d’accès de serveur uniquement.</span><span class="sxs-lookup"><span data-stu-id="b4f66-193">Determines if a string is a valid UNC for a server path only.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b4f66-194"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathisuncserversharea"><strong>PathIsUNCServerShare</strong></a></span><span class="sxs-lookup"><span data-stu-id="b4f66-194"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathisuncserversharea"><strong>PathIsUNCServerShare</strong></a></span></span><br/></td>
<td><span data-ttu-id="b4f66-195">Détermine si une chaîne est un chemin d’accès de partage UNC valide, un partage de \\ <em>serveur</em> \ <em></em>.</span><span class="sxs-lookup"><span data-stu-id="b4f66-195">Determines if a string is a valid UNC share path, \\<em>server</em>\<em>share</em>.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b4f66-196"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathisurla"><strong>PathIsURL</strong></a></span><span class="sxs-lookup"><span data-stu-id="b4f66-196"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathisurla"><strong>PathIsURL</strong></a></span></span><br/></td>
<td><span data-ttu-id="b4f66-197">Teste une chaîne donnée pour déterminer si elle est conforme à un format d’URL valide.</span><span class="sxs-lookup"><span data-stu-id="b4f66-197">Tests a given string to determine if it conforms to a valid URL format.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b4f66-198"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathmakeprettya"><strong>PathMakePretty</strong></a></span><span class="sxs-lookup"><span data-stu-id="b4f66-198"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathmakeprettya"><strong>PathMakePretty</strong></a></span></span><br/></td>
<td><span data-ttu-id="b4f66-199">Convertit un chemin tout en majuscules en caractères minuscules pour que le chemin d’accès soit une apparence cohérente.</span><span class="sxs-lookup"><span data-stu-id="b4f66-199">Converts an all-uppercase path to all lowercase characters to give the path a consistent appearance.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b4f66-200"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathmakesystemfoldera"><strong>PathMakeSystemFolder</strong></a></span><span class="sxs-lookup"><span data-stu-id="b4f66-200"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathmakesystemfoldera"><strong>PathMakeSystemFolder</strong></a></span></span><br/></td>
<td><span data-ttu-id="b4f66-201">Donne à un dossier existant les attributs appropriés pour devenir un dossier système.</span><span class="sxs-lookup"><span data-stu-id="b4f66-201">Gives an existing folder the proper attributes to become a system folder.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b4f66-202"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathmatchspeca"><strong>PathMatchSpec</strong></a></span><span class="sxs-lookup"><span data-stu-id="b4f66-202"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathmatchspeca"><strong>PathMatchSpec</strong></a></span></span><br/></td>
<td><span data-ttu-id="b4f66-203">Recherche une chaîne à l’aide d’un type de correspondance de caractère générique MS-DOS.</span><span class="sxs-lookup"><span data-stu-id="b4f66-203">Searches a string using a MS-DOS wildcard match type.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b4f66-204"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathmatchspecexa"><strong>PathMatchSpecEx</strong></a></span><span class="sxs-lookup"><span data-stu-id="b4f66-204"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathmatchspecexa"><strong>PathMatchSpecEx</strong></a></span></span><br/></td>
<td><span data-ttu-id="b4f66-205">Correspond à un nom de fichier à partir d’un chemin d’accès par rapport à un ou plusieurs modèles de nom de fichier.</span><span class="sxs-lookup"><span data-stu-id="b4f66-205">Matches a file name from a path against one or more file name patterns.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b4f66-206"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathparseiconlocationa"><strong>PathParseIconLocation</strong></a></span><span class="sxs-lookup"><span data-stu-id="b4f66-206"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathparseiconlocationa"><strong>PathParseIconLocation</strong></a></span></span><br/></td>
<td><span data-ttu-id="b4f66-207">Analyse une chaîne d’emplacement de fichier qui contient un emplacement de fichier et un index d’icône, et retourne des valeurs distinctes.</span><span class="sxs-lookup"><span data-stu-id="b4f66-207">Parses a file location string that contains a file location and icon index, and returns separate values.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b4f66-208"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathquotespacesa"><strong>PathQuoteSpaces</strong></a></span><span class="sxs-lookup"><span data-stu-id="b4f66-208"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathquotespacesa"><strong>PathQuoteSpaces</strong></a></span></span><br/></td>
<td><span data-ttu-id="b4f66-209">Recherche des espaces dans un chemin d’accès.</span><span class="sxs-lookup"><span data-stu-id="b4f66-209">Searches a path for spaces.</span></span> <span data-ttu-id="b4f66-210">Si des espaces sont trouvés, le chemin d’accès entier est placé entre guillemets.</span><span class="sxs-lookup"><span data-stu-id="b4f66-210">If spaces are found, the entire path is enclosed in quotation marks.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b4f66-211"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathrelativepathtoa"><strong>PathRelativePathTo</strong></a></span><span class="sxs-lookup"><span data-stu-id="b4f66-211"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathrelativepathtoa"><strong>PathRelativePathTo</strong></a></span></span><br/></td>
<td><span data-ttu-id="b4f66-212">Crée un chemin d’accès relatif d’un fichier ou dossier à un autre.</span><span class="sxs-lookup"><span data-stu-id="b4f66-212">Creates a relative path from one file or folder to another.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b4f66-213"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathremoveargsa"><strong>PathRemoveArgs</strong></a></span><span class="sxs-lookup"><span data-stu-id="b4f66-213"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathremoveargsa"><strong>PathRemoveArgs</strong></a></span></span><br/></td>
<td><span data-ttu-id="b4f66-214">Supprime tous les arguments d’un chemin d’accès donné.</span><span class="sxs-lookup"><span data-stu-id="b4f66-214">Removes any arguments from a given path.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b4f66-215"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathremovebackslasha"><strong>PathRemoveBackslash</strong></a></span><span class="sxs-lookup"><span data-stu-id="b4f66-215"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathremovebackslasha"><strong>PathRemoveBackslash</strong></a></span></span><br/></td>
<td><span data-ttu-id="b4f66-216">Supprime la barre oblique inverse de fin d’un chemin d’accès donné.</span><span class="sxs-lookup"><span data-stu-id="b4f66-216">Removes the trailing backslash from a given path.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="b4f66-217">Cette fonction est déconseillée.</span><span class="sxs-lookup"><span data-stu-id="b4f66-217">This function is deprecated.</span></span> <span data-ttu-id="b4f66-218">Nous vous recommandons d’utiliser la fonction <a href="/windows/desktop/api/pathcch/nf-pathcch-pathcchremovebackslash"><strong>PathCchRemoveBackslash</strong></a> ou <a href="/windows/desktop/api/pathcch/nf-pathcch-pathcchremovebackslashex"><strong>PathCchRemoveBackslashEx</strong></a> à la place.</span><span class="sxs-lookup"><span data-stu-id="b4f66-218">We recommend the use of the <a href="/windows/desktop/api/pathcch/nf-pathcch-pathcchremovebackslash"><strong>PathCchRemoveBackslash</strong></a> or <a href="/windows/desktop/api/pathcch/nf-pathcch-pathcchremovebackslashex"><strong>PathCchRemoveBackslashEx</strong></a> function in its place.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b4f66-219"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathremoveblanksa"><strong>PathRemoveBlanks</strong></a></span><span class="sxs-lookup"><span data-stu-id="b4f66-219"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathremoveblanksa"><strong>PathRemoveBlanks</strong></a></span></span><br/></td>
<td><span data-ttu-id="b4f66-220">Supprime tous les espaces de début et de fin d’une chaîne.</span><span class="sxs-lookup"><span data-stu-id="b4f66-220">Removes all leading and trailing spaces from a string.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b4f66-221"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathremoveextensiona"><strong>PathRemoveExtension</strong></a></span><span class="sxs-lookup"><span data-stu-id="b4f66-221"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathremoveextensiona"><strong>PathRemoveExtension</strong></a></span></span><br/></td>
<td><span data-ttu-id="b4f66-222">Supprime l’extension de nom de fichier d’un chemin d’accès, si celle-ci est présente.</span><span class="sxs-lookup"><span data-stu-id="b4f66-222">Removes the file name extension from a path, if one is present.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="b4f66-223">Cette fonction est déconseillée.</span><span class="sxs-lookup"><span data-stu-id="b4f66-223">This function is deprecated.</span></span> <span data-ttu-id="b4f66-224">Nous vous recommandons d’utiliser <a href="/windows/desktop/api/pathcch/nf-pathcch-pathcchremoveextension"><strong>PathCchRemoveExtension</strong></a> à la place.</span><span class="sxs-lookup"><span data-stu-id="b4f66-224">We recommend the use of the <a href="/windows/desktop/api/pathcch/nf-pathcch-pathcchremoveextension"><strong>PathCchRemoveExtension</strong></a> in its place.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b4f66-225"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathremovefilespeca"><strong>PathRemoveFileSpec</strong></a></span><span class="sxs-lookup"><span data-stu-id="b4f66-225"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathremovefilespeca"><strong>PathRemoveFileSpec</strong></a></span></span><br/></td>
<td><span data-ttu-id="b4f66-226">Supprime le nom de fichier de fin et la barre oblique inverse d’un chemin d’accès, s’ils sont présents.</span><span class="sxs-lookup"><span data-stu-id="b4f66-226">Removes the trailing file name and backslash from a path, if they are present.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="b4f66-227">Cette fonction est déconseillée.</span><span class="sxs-lookup"><span data-stu-id="b4f66-227">This function is deprecated.</span></span> <span data-ttu-id="b4f66-228">Nous vous recommandons d’utiliser la fonction <a href="/windows/desktop/api/pathcch/nf-pathcch-pathcchremovefilespec"><strong>PathCchRemoveFileSpec</strong></a> à la place.</span><span class="sxs-lookup"><span data-stu-id="b4f66-228">We recommend the use of the <a href="/windows/desktop/api/pathcch/nf-pathcch-pathcchremovefilespec"><strong>PathCchRemoveFileSpec</strong></a> function in its place.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b4f66-229"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathrenameextensiona"><strong>PathRenameExtension</strong></a></span><span class="sxs-lookup"><span data-stu-id="b4f66-229"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathrenameextensiona"><strong>PathRenameExtension</strong></a></span></span><br/></td>
<td><span data-ttu-id="b4f66-230">Remplace l’extension d’un nom de fichier par une nouvelle extension.</span><span class="sxs-lookup"><span data-stu-id="b4f66-230">Replaces the extension of a file name with a new extension.</span></span> <span data-ttu-id="b4f66-231">Si le nom de fichier ne contient pas d’extension, l’extension est attachée à la fin de la chaîne.</span><span class="sxs-lookup"><span data-stu-id="b4f66-231">If the file name does not contain an extension, the extension will be attached to the end of the string.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="b4f66-232">Une utilisation incorrecte de cette fonction peut entraîner un dépassement de mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="b4f66-232">Misuse of this function can lead to a buffer overrun.</span></span> <span data-ttu-id="b4f66-233">Nous vous recommandons d’utiliser la fonction <a href="/windows/desktop/api/pathcch/nf-pathcch-pathcchrenameextension"><strong>PathCchRenameExtension</strong></a> plus sûre à la place.</span><span class="sxs-lookup"><span data-stu-id="b4f66-233">We recommend the use of the safer <a href="/windows/desktop/api/pathcch/nf-pathcch-pathcchrenameextension"><strong>PathCchRenameExtension</strong></a> function in its place.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b4f66-234"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathsearchandqualifya"><strong>PathSearchAndQualify</strong></a></span><span class="sxs-lookup"><span data-stu-id="b4f66-234"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathsearchandqualifya"><strong>PathSearchAndQualify</strong></a></span></span><br/></td>
<td><span data-ttu-id="b4f66-235">Détermine si un chemin d’accès donné est correctement mis en forme et complet.</span><span class="sxs-lookup"><span data-stu-id="b4f66-235">Determines if a given path is correctly formatted and fully qualified.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b4f66-236"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathsetdlgitempatha"><strong>PathSetDlgItemPath</strong></a></span><span class="sxs-lookup"><span data-stu-id="b4f66-236"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathsetdlgitempatha"><strong>PathSetDlgItemPath</strong></a></span></span><br/></td>
<td><span data-ttu-id="b4f66-237">Définit le texte d’un contrôle enfant dans une fenêtre ou une boîte de dialogue, à l’aide de <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathcompactpatha"><strong>PathCompactPath</strong></a> pour garantir que le chemin d’accès est ajusté dans le contrôle.</span><span class="sxs-lookup"><span data-stu-id="b4f66-237">Sets the text of a child control in a window or dialog box, using <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathcompactpatha"><strong>PathCompactPath</strong></a> to ensure the path fits in the control.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b4f66-238"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathskiproota"><strong>PathSkipRoot</strong></a></span><span class="sxs-lookup"><span data-stu-id="b4f66-238"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathskiproota"><strong>PathSkipRoot</strong></a></span></span><br/></td>
<td><span data-ttu-id="b4f66-239">Récupère un pointeur désignant le premier caractère d’un chemin d’accès qui suit les éléments de lettre de lecteur ou de chemin d’accès de partage/serveur UNC.</span><span class="sxs-lookup"><span data-stu-id="b4f66-239">Retrieves a pointer to the first character in a path following the drive letter or UNC server/share path elements.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b4f66-240"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathstrippatha"><strong>PathStripPath</strong></a></span><span class="sxs-lookup"><span data-stu-id="b4f66-240"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathstrippatha"><strong>PathStripPath</strong></a></span></span><br/></td>
<td><span data-ttu-id="b4f66-241">Supprime la partie chemin d’accès d’un fichier et d’un chemin d’accès qualifiés complets.</span><span class="sxs-lookup"><span data-stu-id="b4f66-241">Removes the path portion of a fully qualified path and file.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b4f66-242"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathstriptoroota"><strong>PathStripToRoot</strong></a></span><span class="sxs-lookup"><span data-stu-id="b4f66-242"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathstriptoroota"><strong>PathStripToRoot</strong></a></span></span><br/></td>
<td><span data-ttu-id="b4f66-243">Supprime tous les éléments de fichier et de répertoire dans un chemin d’accès à l’exception des informations de racine.</span><span class="sxs-lookup"><span data-stu-id="b4f66-243">Removes all file and directory elements in a path except for the root information.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="b4f66-244">Une utilisation incorrecte de cette fonction peut entraîner un dépassement de mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="b4f66-244">Misuse of this function can lead to a buffer overrun.</span></span> <span data-ttu-id="b4f66-245">Nous vous recommandons d’utiliser la fonction <a href="/windows/desktop/api/pathcch/nf-pathcch-pathcchstriptoroot"><strong>PathCchStripToRoot</strong></a> plus sûre à la place.</span><span class="sxs-lookup"><span data-stu-id="b4f66-245">We recommend the use of the safer <a href="/windows/desktop/api/pathcch/nf-pathcch-pathcchstriptoroot"><strong>PathCchStripToRoot</strong></a> function in its place.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b4f66-246"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathundecoratea"><strong>PathUndecorate</strong></a></span><span class="sxs-lookup"><span data-stu-id="b4f66-246"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathundecoratea"><strong>PathUndecorate</strong></a></span></span><br/></td>
<td><span data-ttu-id="b4f66-247">Supprime la décoration d’une chaîne de chemin d’accès.</span><span class="sxs-lookup"><span data-stu-id="b4f66-247">Removes the decoration from a path string.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b4f66-248"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathunexpandenvstringsa"><strong>PathUnExpandEnvStrings</strong></a></span><span class="sxs-lookup"><span data-stu-id="b4f66-248"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathunexpandenvstringsa"><strong>PathUnExpandEnvStrings</strong></a></span></span><br/></td>
<td><span data-ttu-id="b4f66-249">Remplace certains noms de dossiers dans un chemin d’accès qualifié complet par la chaîne d’environnement qui leur est associée.</span><span class="sxs-lookup"><span data-stu-id="b4f66-249">Replaces certain folder names in a fully qualified path with their associated environment string.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b4f66-250"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathunmakesystemfoldera"><strong>PathUnmakeSystemFolder</strong></a></span><span class="sxs-lookup"><span data-stu-id="b4f66-250"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathunmakesystemfoldera"><strong>PathUnmakeSystemFolder</strong></a></span></span><br/></td>
<td><span data-ttu-id="b4f66-251">Supprime les attributs d’un dossier qui en fait un dossier système.</span><span class="sxs-lookup"><span data-stu-id="b4f66-251">Removes the attributes from a folder that make it a system folder.</span></span> <span data-ttu-id="b4f66-252">Ce dossier doit réellement exister dans le système de fichiers.</span><span class="sxs-lookup"><span data-stu-id="b4f66-252">This folder must actually exist in the file system.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b4f66-253"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathunquotespacesa"><strong>PathUnquoteSpaces</strong></a></span><span class="sxs-lookup"><span data-stu-id="b4f66-253"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-pathunquotespacesa"><strong>PathUnquoteSpaces</strong></a></span></span><br/></td>
<td><span data-ttu-id="b4f66-254">Supprime les guillemets à partir du début et de la fin d’un chemin d’accès.</span><span class="sxs-lookup"><span data-stu-id="b4f66-254">Removes quotes from the beginning and end of a path.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b4f66-255"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-shskipjunction"><strong>SHSkipJunction</strong></a></span><span class="sxs-lookup"><span data-stu-id="b4f66-255"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-shskipjunction"><strong>SHSkipJunction</strong></a></span></span><br/></td>
<td><span data-ttu-id="b4f66-256">Vérifie un contexte de liaison pour voir s’il est possible de lier en toute sécurité à un objet de composant particulier.</span><span class="sxs-lookup"><span data-stu-id="b4f66-256">Checks a bind context to see if it is safe to bind to a particular component object.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b4f66-257"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-urlapplyschemea"><strong>UrlApplyScheme</strong></a></span><span class="sxs-lookup"><span data-stu-id="b4f66-257"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-urlapplyschemea"><strong>UrlApplyScheme</strong></a></span></span><br/></td>
<td><span data-ttu-id="b4f66-258">Détermine un schéma pour une chaîne d’URL spécifiée et retourne une chaîne avec un préfixe approprié.</span><span class="sxs-lookup"><span data-stu-id="b4f66-258">Determines a scheme for a specified URL string, and returns a string with an appropriate prefix.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b4f66-259"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-urlcanonicalizea"><strong>UrlCanonicalize</strong></a></span><span class="sxs-lookup"><span data-stu-id="b4f66-259"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-urlcanonicalizea"><strong>UrlCanonicalize</strong></a></span></span><br/></td>
<td><span data-ttu-id="b4f66-260">Convertit une chaîne d’URL en forme canonique.</span><span class="sxs-lookup"><span data-stu-id="b4f66-260">Converts a URL string into canonical form.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b4f66-261"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-urlcombinea"><strong>UrlCombine</strong></a></span><span class="sxs-lookup"><span data-stu-id="b4f66-261"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-urlcombinea"><strong>UrlCombine</strong></a></span></span><br/></td>
<td><span data-ttu-id="b4f66-262">Lorsqu’il est fourni avec une URL relative et sa base, retourne une URL sous forme canonique.</span><span class="sxs-lookup"><span data-stu-id="b4f66-262">When provided with a relative URL and its base, returns a URL in canonical form.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b4f66-263"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-urlcomparea"><strong>UrlCompare</strong></a></span><span class="sxs-lookup"><span data-stu-id="b4f66-263"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-urlcomparea"><strong>UrlCompare</strong></a></span></span><br/></td>
<td><span data-ttu-id="b4f66-264">Effectue une comparaison sensible à la casse de deux chaînes d’URL.</span><span class="sxs-lookup"><span data-stu-id="b4f66-264">Makes a case-sensitive comparison of two URL strings.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b4f66-265"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-urlcreatefrompatha"><strong>UrlCreateFromPath</strong></a></span><span class="sxs-lookup"><span data-stu-id="b4f66-265"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-urlcreatefrompatha"><strong>UrlCreateFromPath</strong></a></span></span><br/></td>
<td><span data-ttu-id="b4f66-266">Convertit un chemin d’accès MS-DOS en URL canonique.</span><span class="sxs-lookup"><span data-stu-id="b4f66-266">Converts a MS-DOS path to a canonicalized URL.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b4f66-267"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-urlescapea"><strong>UrlEscape</strong></a></span><span class="sxs-lookup"><span data-stu-id="b4f66-267"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-urlescapea"><strong>UrlEscape</strong></a></span></span><br/></td>
<td><span data-ttu-id="b4f66-268">Convertit des caractères ou des paires de substitution dans une URL qui peuvent être modifiées pendant le transport sur Internet ( &quot; caractères non sécurisés &quot; ) en leurs séquences d’échappement correspondantes.</span><span class="sxs-lookup"><span data-stu-id="b4f66-268">Converts characters or surrogate pairs in a URL that might be altered during transport across the Internet (&quot;unsafe&quot; characters) into their corresponding escape sequences.</span></span> <span data-ttu-id="b4f66-269">Les paires de substitution sont des caractères compris entre U + 10000 et U + 10FFFF (au format UTF-32) ou entre DC00 et et DFFF (UTF-16).</span><span class="sxs-lookup"><span data-stu-id="b4f66-269">Surrogate pairs are characters between U+10000 to U+10FFFF (in UTF-32) or between DC00 to DFFF (in UTF-16).</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b4f66-270"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-urlescapespaces"><strong>UrlEscapeSpaces</strong></a></span><span class="sxs-lookup"><span data-stu-id="b4f66-270"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-urlescapespaces"><strong>UrlEscapeSpaces</strong></a></span></span><br/></td>
<td><span data-ttu-id="b4f66-271">Macro qui convertit les espaces en séquence d’échappement correspondante.</span><span class="sxs-lookup"><span data-stu-id="b4f66-271">A macro that converts space characters into their corresponding escape sequence.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b4f66-272"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-urlgetlocationa"><strong>UrlGetLocation</strong></a></span><span class="sxs-lookup"><span data-stu-id="b4f66-272"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-urlgetlocationa"><strong>UrlGetLocation</strong></a></span></span><br/></td>
<td><span data-ttu-id="b4f66-273">Récupère l’emplacement à partir d’une URL.</span><span class="sxs-lookup"><span data-stu-id="b4f66-273">Retrieves the location from a URL.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b4f66-274"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-urlgetparta"><strong>UrlGetPart</strong></a></span><span class="sxs-lookup"><span data-stu-id="b4f66-274"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-urlgetparta"><strong>UrlGetPart</strong></a></span></span><br/></td>
<td><span data-ttu-id="b4f66-275">Accepte une chaîne d’URL et retourne une partie spécifiée de cette URL.</span><span class="sxs-lookup"><span data-stu-id="b4f66-275">Accepts a URL string and returns a specified part of that URL.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b4f66-276"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-urlhasha"><strong>UrlHash</strong></a></span><span class="sxs-lookup"><span data-stu-id="b4f66-276"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-urlhasha"><strong>UrlHash</strong></a></span></span><br/></td>
<td><span data-ttu-id="b4f66-277">Hache une chaîne d’URL.</span><span class="sxs-lookup"><span data-stu-id="b4f66-277">Hashes a URL string.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b4f66-278"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-urlisa"><strong>UrlIs</strong></a></span><span class="sxs-lookup"><span data-stu-id="b4f66-278"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-urlisa"><strong>UrlIs</strong></a></span></span><br/></td>
<td><span data-ttu-id="b4f66-279">Teste si une URL est un type spécifié.</span><span class="sxs-lookup"><span data-stu-id="b4f66-279">Tests whether a URL is a specified type.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b4f66-280"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-urlisfileurla"><strong>UrlIsFileUrl</strong></a></span><span class="sxs-lookup"><span data-stu-id="b4f66-280"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-urlisfileurla"><strong>UrlIsFileUrl</strong></a></span></span><br/></td>
<td><span data-ttu-id="b4f66-281">Teste une URL pour déterminer s’il s’agit d’une URL de fichier.</span><span class="sxs-lookup"><span data-stu-id="b4f66-281">Tests a URL to determine if it is a file URL.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b4f66-282"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-urlisnohistorya"><strong>UrlIsNoHistory</strong></a></span><span class="sxs-lookup"><span data-stu-id="b4f66-282"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-urlisnohistorya"><strong>UrlIsNoHistory</strong></a></span></span><br/></td>
<td><span data-ttu-id="b4f66-283">Retourne une valeur indiquant si une URL est une URL que les navigateurs n’incluent généralement pas dans l’historique de navigation.</span><span class="sxs-lookup"><span data-stu-id="b4f66-283">Returns whether a URL is a URL that browsers typically do not include in navigation history.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b4f66-284"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-urlisopaquea"><strong>UrlIsOpaque</strong></a></span><span class="sxs-lookup"><span data-stu-id="b4f66-284"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-urlisopaquea"><strong>UrlIsOpaque</strong></a></span></span><br/></td>
<td><span data-ttu-id="b4f66-285">Retourne une valeur indiquant si une URL est opaque.</span><span class="sxs-lookup"><span data-stu-id="b4f66-285">Returns whether a URL is opaque.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b4f66-286"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-urlunescapea"><strong>UrlUnescape</strong></a></span><span class="sxs-lookup"><span data-stu-id="b4f66-286"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-urlunescapea"><strong>UrlUnescape</strong></a></span></span><br/></td>
<td><span data-ttu-id="b4f66-287">Convertit les séquences d’échappement en caractères ordinaires.</span><span class="sxs-lookup"><span data-stu-id="b4f66-287">Converts escape sequences back into ordinary characters.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b4f66-288"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-urlunescapeinplace"><strong>UrlUnescapeInPlace</strong></a></span><span class="sxs-lookup"><span data-stu-id="b4f66-288"><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-urlunescapeinplace"><strong>UrlUnescapeInPlace</strong></a></span></span><br/></td>
<td><span data-ttu-id="b4f66-289">Convertit les séquences d’échappement en caractères ordinaires et remplace la chaîne d’origine.</span><span class="sxs-lookup"><span data-stu-id="b4f66-289">Converts escape sequences back into ordinary characters and overwrites the original string.</span></span><br/></td>
</tr>
</tbody>
</table>



 

 

 




