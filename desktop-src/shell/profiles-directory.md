---
description: 'Le système stocke les informations de profil utilisateur dans un répertoire spécifique, qui a des noms différents dans différentes versions de Windows : &\# 0034 ; documents and settings&\# 0034 ; dans Windows XP et &\# 0034 ; Les utilisateurs&\# 0034 ; dans Windows Vista et versions ultérieures.'
title: Répertoire des profils
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 41056f40-fa1a-488a-b213-49cbdd8d4fdf
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 3eb310434e5665dd8f28a661785403d72c4c1e46
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104973347"
---
# <a name="profiles-directory"></a><span data-ttu-id="04281-103">Répertoire des profils</span><span class="sxs-lookup"><span data-stu-id="04281-103">Profiles Directory</span></span>

<span data-ttu-id="04281-104">Le système stocke les informations de profil utilisateur dans un répertoire spécifique, qui a des noms différents dans les différentes versions de Windows : « documents and Settings » sous Windows XP et « Users » dans Windows Vista et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="04281-104">The system stores user profile information in a specific directory, which has different names in different versions of Windows: "Documents and Settings" in Windows XP and "Users" in Windows Vista and later.</span></span> <span data-ttu-id="04281-105">Pour obtenir le chemin d’accès du répertoire des profils, utilisez la fonction [**GetProfilesDirectory**](/windows/desktop/api/Userenv/nf-userenv-getprofilesdirectorya) .</span><span class="sxs-lookup"><span data-stu-id="04281-105">To obtain the path of the profiles directory, use the [**GetProfilesDirectory**](/windows/desktop/api/Userenv/nf-userenv-getprofilesdirectorya) function.</span></span>

<span data-ttu-id="04281-106">Le répertoire des profils contient les sous-répertoires suivants pour les profils utilisateur.</span><span class="sxs-lookup"><span data-stu-id="04281-106">The profiles directory contains the following subdirectories for user profiles.</span></span>



| <span data-ttu-id="04281-107">Répertoire</span><span class="sxs-lookup"><span data-stu-id="04281-107">Directory</span></span>                                      | <span data-ttu-id="04281-108">Description</span><span class="sxs-lookup"><span data-stu-id="04281-108">Description</span></span>                                                                                                                                |
|------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="04281-109">ProgramData (Windows Vista ou version ultérieure)/All Users</span><span class="sxs-lookup"><span data-stu-id="04281-109">ProgramData (Windows Vista or later)/All Users</span></span> | <span data-ttu-id="04281-110">Informations de programme qui s’appliquent à tous les utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="04281-110">Program information that applies to all users.</span></span> <span data-ttu-id="04281-111">Le répertoire tous les utilisateurs existe toujours dans Windows Vista ou version ultérieure, pour des raisons de compatibilité descendante.</span><span class="sxs-lookup"><span data-stu-id="04281-111">The All Users directory still exists in Windows Vista or later, for backward compatibility.</span></span> |
| <span data-ttu-id="04281-112">Default</span><span class="sxs-lookup"><span data-stu-id="04281-112">Default</span></span>                                        | <span data-ttu-id="04281-113">Informations de profil qui s’appliquent à l’utilisateur par défaut.</span><span class="sxs-lookup"><span data-stu-id="04281-113">Profile information that applies to the default user.</span></span>                                                                                      |
| <span data-ttu-id="04281-114">*Utilisateur*</span><span class="sxs-lookup"><span data-stu-id="04281-114">*User*</span></span>                                         | <span data-ttu-id="04281-115">Informations de profil qui s’appliquent à l’utilisateur spécifié.</span><span class="sxs-lookup"><span data-stu-id="04281-115">Profile information that applies to the specified user.</span></span> <span data-ttu-id="04281-116">Chaque utilisateur possède son propre sous-répertoire de profil.</span><span class="sxs-lookup"><span data-stu-id="04281-116">Each user has their own profile subdirectory.</span></span>                                      |



 

<span data-ttu-id="04281-117">Pour obtenir l’emplacement du répertoire ProgramData/All Users, appelez la fonction [**GetAllUsersProfileDirectory**](/windows/desktop/api/Userenv/nf-userenv-getallusersprofiledirectorya) .</span><span class="sxs-lookup"><span data-stu-id="04281-117">To obtain the location of the ProgramData/All Users directory, call the [**GetAllUsersProfileDirectory**](/windows/desktop/api/Userenv/nf-userenv-getallusersprofiledirectorya) function.</span></span> <span data-ttu-id="04281-118">Le répertoire contient les sous-répertoires suivants :</span><span class="sxs-lookup"><span data-stu-id="04281-118">This directory contains the following subdirectories:</span></span>



| <span data-ttu-id="04281-119">Répertoire</span><span class="sxs-lookup"><span data-stu-id="04281-119">Directory</span></span>  | <span data-ttu-id="04281-120">Description</span><span class="sxs-lookup"><span data-stu-id="04281-120">Description</span></span>                          |
|------------|--------------------------------------|
| <span data-ttu-id="04281-121">Bureau</span><span class="sxs-lookup"><span data-stu-id="04281-121">Desktop</span></span>    | <span data-ttu-id="04281-122">Raccourcis à afficher sur le bureau.</span><span class="sxs-lookup"><span data-stu-id="04281-122">Shortcuts to display on the desktop.</span></span> |
| <span data-ttu-id="04281-123">Menu Démarrer</span><span class="sxs-lookup"><span data-stu-id="04281-123">Start Menu</span></span> | <span data-ttu-id="04281-124">Éléments de menu du menu **Démarrer** .</span><span class="sxs-lookup"><span data-stu-id="04281-124">Menu items for the **Start** menu.</span></span>   |



 

<span data-ttu-id="04281-125">Pour obtenir l’emplacement de l’annuaire de l’utilisateur par défaut, appelez la fonction [**GetDefaultUserProfileDirectory**](/windows/desktop/api/Userenv/nf-userenv-getdefaultuserprofiledirectorya) .</span><span class="sxs-lookup"><span data-stu-id="04281-125">To obtain the location of the default user's directory, call the [**GetDefaultUserProfileDirectory**](/windows/desktop/api/Userenv/nf-userenv-getdefaultuserprofiledirectorya) function.</span></span> <span data-ttu-id="04281-126">Pour obtenir l’emplacement de l’annuaire d’un utilisateur particulier, appelez la fonction [**GetUserProfileDirectory**](/windows/desktop/api/Userenv/nf-userenv-getuserprofiledirectorya) .</span><span class="sxs-lookup"><span data-stu-id="04281-126">To obtain the location of a particular user's directory, call the [**GetUserProfileDirectory**](/windows/desktop/api/Userenv/nf-userenv-getuserprofiledirectorya) function.</span></span> <span data-ttu-id="04281-127">Les répertoires utilisateur par défaut et utilisateurs spécifiques contiennent les sous-répertoires suivants.</span><span class="sxs-lookup"><span data-stu-id="04281-127">Both the default user and specific user directories contain the following subdirectories.</span></span> <span data-ttu-id="04281-128">Les répertoires en italique indiquent les répertoires qui sont masqués par défaut.</span><span class="sxs-lookup"><span data-stu-id="04281-128">Directories in italics indicate directories that are hidden by default.</span></span> <span data-ttu-id="04281-129">Vous pouvez afficher ces répertoires en sélectionnant l’option **afficher les fichiers, les dossiers et les lecteurs masqués** dans les **Options des dossiers** , élément du panneau de configuration.</span><span class="sxs-lookup"><span data-stu-id="04281-129">You can view these directories by selecting the **Show hidden files, folders, and drives** option in the **Folder Options** control panel item.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="04281-130">Répertoire</span><span class="sxs-lookup"><span data-stu-id="04281-130">Directory</span></span></th>
<th><span data-ttu-id="04281-131">Description</span><span class="sxs-lookup"><span data-stu-id="04281-131">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="04281-132">Données d'application</span><span class="sxs-lookup"><span data-stu-id="04281-132">Application Data</span></span></td>
<td><span data-ttu-id="04281-133">Données spécifiques à l’application.</span><span class="sxs-lookup"><span data-stu-id="04281-133">Application-specific data.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="04281-134">Cookies</span><span class="sxs-lookup"><span data-stu-id="04281-134">Cookies</span></span></td>
<td><span data-ttu-id="04281-135">Cookies Windows Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="04281-135">Windows Internet Explorer cookies.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="04281-136">Bureau</span><span class="sxs-lookup"><span data-stu-id="04281-136">Desktop</span></span></td>
<td><span data-ttu-id="04281-137">Raccourcis à afficher sur le bureau.</span><span class="sxs-lookup"><span data-stu-id="04281-137">Shortcuts to display on the desktop.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="04281-138">Favoris</span><span class="sxs-lookup"><span data-stu-id="04281-138">Favorites</span></span></td>
<td><span data-ttu-id="04281-139">Liens vers les sites Web favoris.</span><span class="sxs-lookup"><span data-stu-id="04281-139">Links to favorite websites.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="04281-140">Paramètres locaux</span><span class="sxs-lookup"><span data-stu-id="04281-140">Local Settings</span></span></td>
<td><span data-ttu-id="04281-141">Paramètres et données d’application qui ne sont pas itinérants avec le profil.</span><span class="sxs-lookup"><span data-stu-id="04281-141">Application settings and data that do not roam with the profile.</span></span> <span data-ttu-id="04281-142">En général, les paramètres ou les données de ce répertoire sont spécifiques à l’ordinateur ou ils sont trop volumineux pour être itinérants efficacement.</span><span class="sxs-lookup"><span data-stu-id="04281-142">Usually the settings or data in this directory are computer-specific, or they are too large to roam effectively.</span></span> <span data-ttu-id="04281-143">Ce répertoire contient les sous-dossiers suivants :</span><span class="sxs-lookup"><span data-stu-id="04281-143">This directory contains the following subfolders:</span></span>
<ul>
<li><span data-ttu-id="04281-144">Données d'application</span><span class="sxs-lookup"><span data-stu-id="04281-144">Application Data</span></span></li>
<li><span data-ttu-id="04281-145">Historique</span><span class="sxs-lookup"><span data-stu-id="04281-145">History</span></span></li>
<li><span data-ttu-id="04281-146">Temp</span><span class="sxs-lookup"><span data-stu-id="04281-146">Temp</span></span></li>
<li><span data-ttu-id="04281-147">Fichiers Internet temporaires</span><span class="sxs-lookup"><span data-stu-id="04281-147">Temporary Internet Files</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="04281-148">Mes documents</span><span class="sxs-lookup"><span data-stu-id="04281-148">My Documents</span></span></td>
<td><span data-ttu-id="04281-149">Emplacement par défaut des documents créés par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="04281-149">The default location for documents that the user creates.</span></span> <span data-ttu-id="04281-150">Les applications doivent enregistrer les fichiers de documents dans ce répertoire par défaut.</span><span class="sxs-lookup"><span data-stu-id="04281-150">Applications should save document files to this directory by default.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="04281-151"><em>Nethotte</em></span><span class="sxs-lookup"><span data-stu-id="04281-151"><em>NetHood</em></span></span></td>
<td><span data-ttu-id="04281-152">Raccourcis vers les éléments du voisinage réseau.</span><span class="sxs-lookup"><span data-stu-id="04281-152">Shortcuts to Network Neighborhood items.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="04281-153"><em>PrintHood</em></span><span class="sxs-lookup"><span data-stu-id="04281-153"><em>PrintHood</em></span></span></td>
<td><span data-ttu-id="04281-154">Raccourcis vers des éléments de dossier d’imprimante.</span><span class="sxs-lookup"><span data-stu-id="04281-154">Shortcuts to printer folder items.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="04281-155"><em>Sources</em></span><span class="sxs-lookup"><span data-stu-id="04281-155"><em>Recent</em></span></span></td>
<td><span data-ttu-id="04281-156">Raccourcis vers les documents les plus récemment utilisés.</span><span class="sxs-lookup"><span data-stu-id="04281-156">Shortcuts to the most recently used documents.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="04281-157">SendTo</span><span class="sxs-lookup"><span data-stu-id="04281-157">SendTo</span></span></td>
<td><span data-ttu-id="04281-158">Raccourcis vers les emplacements auxquels l’utilisateur envoie souvent des fichiers.</span><span class="sxs-lookup"><span data-stu-id="04281-158">Shortcuts to locations to which the user often sends files.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="04281-159">Menu Démarrer</span><span class="sxs-lookup"><span data-stu-id="04281-159">Start Menu</span></span></td>
<td><span data-ttu-id="04281-160">Éléments de menu du menu <strong>Démarrer</strong> .</span><span class="sxs-lookup"><span data-stu-id="04281-160">Menu items for the <strong>Start</strong> menu.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="04281-161"><em>Modèles</em></span><span class="sxs-lookup"><span data-stu-id="04281-161"><em>Templates</em></span></span></td>
<td><span data-ttu-id="04281-162">Raccourcis vers les éléments de modèle.</span><span class="sxs-lookup"><span data-stu-id="04281-162">Shortcuts to template items.</span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="04281-163">Pour obtenir l’emplacement des sous-répertoires de ces répertoires, utilisez les fonctions [**SHGetFolderPath**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetfolderpatha) ou [**SHGetKnownFolderPath**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetknownfolderpath) .</span><span class="sxs-lookup"><span data-stu-id="04281-163">To obtain the location of subdirectories of these directories, use the [**SHGetFolderPath**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetfolderpatha) or [**SHGetKnownFolderPath**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetknownfolderpath) functions.</span></span>

 

 



