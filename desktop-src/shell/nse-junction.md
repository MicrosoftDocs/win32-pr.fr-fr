---
description: La racine d’une extension d’espace de noms est normalement affichée par l’Explorateur Windows comme un dossier dans les vues d’arborescence et de dossier.
title: Spécification de l’emplacement d’une extension d’espace de noms
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 2c1fdd5d-b359-4d5c-a20e-0622f3a1cb1d
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 7617c7361c5f2ae76331c5f1b59eb845f6806395
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103866161"
---
# <a name="specifying-a-namespace-extensions-location"></a><span data-ttu-id="8d765-103">Spécification de l’emplacement d’une extension d’espace de noms</span><span class="sxs-lookup"><span data-stu-id="8d765-103">Specifying a Namespace Extension's Location</span></span>

<span data-ttu-id="8d765-104">La racine d’une extension d’espace de noms est normalement affichée par l’Explorateur Windows comme un dossier dans les vues d’arborescence et de dossier.</span><span class="sxs-lookup"><span data-stu-id="8d765-104">The root of a namespace extension is normally displayed by Windows Explorer as a folder in both tree and folder views.</span></span> <span data-ttu-id="8d765-105">Pour que l’Explorateur Windows affiche les fichiers et les sous-dossiers de votre extension, vous devez spécifier l’emplacement du dossier racine dans la hiérarchie d’espace de noms de l’interpréteur de commandes.</span><span class="sxs-lookup"><span data-stu-id="8d765-105">For Windows Explorer to display your extension's files and subfolders, you must specify where the root folder is located in the Shell namespace hierarchy.</span></span> <span data-ttu-id="8d765-106">Cet emplacement est désigné sous le terme de *point de jonction*.</span><span class="sxs-lookup"><span data-stu-id="8d765-106">This location is referred to as a *junction point*.</span></span>

-   [<span data-ttu-id="8d765-107">Utilisation de dossiers virtuels comme points de jonction</span><span class="sxs-lookup"><span data-stu-id="8d765-107">Using Virtual Folders as Junction Points</span></span>](#using-virtual-folders-as-junction-points)
-   [<span data-ttu-id="8d765-108">Utilisation des dossiers du système de fichiers en tant que points de jonction</span><span class="sxs-lookup"><span data-stu-id="8d765-108">Using File System Folders as Junction Points</span></span>](#using-file-system-folders-as-junction-points)
-   [<span data-ttu-id="8d765-109">Ouverture d’une vue d’une extension d’espace de noms</span><span class="sxs-lookup"><span data-stu-id="8d765-109">Opening a View of a Namespace Extension</span></span>](#opening-a-view-of-a-namespace-extension)

## <a name="using-virtual-folders-as-junction-points"></a><span data-ttu-id="8d765-110">Utilisation de dossiers virtuels comme points de jonction</span><span class="sxs-lookup"><span data-stu-id="8d765-110">Using Virtual Folders as Junction Points</span></span>

<span data-ttu-id="8d765-111">La façon la plus simple de définir le point de jonction d’une extension consiste à faire du dossier racine un sous-dossier d’un dossier virtuel système.</span><span class="sxs-lookup"><span data-stu-id="8d765-111">The simplest way to define an extension's junction point is to make the root folder a subfolder of a system virtual folder.</span></span> <span data-ttu-id="8d765-112">Ce type de point de jonction est désigné sous le terme de *point de jonction virtuel*.</span><span class="sxs-lookup"><span data-stu-id="8d765-112">This type of junction point is referred to as a *virtual junction point*.</span></span> <span data-ttu-id="8d765-113">Les dossiers **Bureau** et **poste de travail** sont les emplacements typiques des points de jonction virtuels, mais vous pouvez également définir un point de jonction virtuel sur un ordinateur distant ou sous les dossiers favoris **réseau**, **Internet Explorer** et **panneau de configuration** .</span><span class="sxs-lookup"><span data-stu-id="8d765-113">The **Desktop** and **My Computer** folders are the typical locations for virtual junction points, but you can also define a virtual junction point on a remote computer or under the **My Network Places**, **Internet Explorer**, and **Control Panel** folders.</span></span>

<span data-ttu-id="8d765-114">Pour définir un point de jonction virtuel, créez une sous-clé de la clé qui représente le dossier virtuel approprié et nommez-la avec la chaîne de l’identificateur de classe (CLSID) de l’extension.</span><span class="sxs-lookup"><span data-stu-id="8d765-114">To define a virtual junction point, create a subkey of the key that represents the appropriate virtual folder and name it with the string form of your extension's class identifier (CLSID).</span></span> <span data-ttu-id="8d765-115">Le CLSID inscrit s’affiche comme suit.</span><span class="sxs-lookup"><span data-stu-id="8d765-115">The registered CLSID would appear as follows.</span></span>

```
HKEY_LOCAL_MACHINE or HKEY_CURRENT_USER
   Software
      Microsoft
         Windows
            CurrentVersion
               Explorer
                  Virtual Folder Name
                     NameSpace
                        {Extension CLSID}
                           (Default) = Junction Point Name
```

<span data-ttu-id="8d765-116">Le *nom du dossier virtuel* est l’une des sous-clés du tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="8d765-116">*Virtual Folder Name* is one of the subkeys in the following table.</span></span>



| <span data-ttu-id="8d765-117">Emplacement</span><span class="sxs-lookup"><span data-stu-id="8d765-117">Location</span></span>          | <span data-ttu-id="8d765-118">Nom du dossier virtuel</span><span class="sxs-lookup"><span data-stu-id="8d765-118">Virtual Folder Name</span></span>                        |
|-------------------|--------------------------------------------|
| <span data-ttu-id="8d765-119">Control panel</span><span class="sxs-lookup"><span data-stu-id="8d765-119">Control Panel</span></span>     | <span data-ttu-id="8d765-120">**ControlPanel**</span><span class="sxs-lookup"><span data-stu-id="8d765-120">**ControlPanel**</span></span>                           |
| <span data-ttu-id="8d765-121">Bureau</span><span class="sxs-lookup"><span data-stu-id="8d765-121">Desktop</span></span>           | <span data-ttu-id="8d765-122">**Bureau**</span><span class="sxs-lookup"><span data-stu-id="8d765-122">**Desktop**</span></span>                                |
| <span data-ttu-id="8d765-123">Réseau entier</span><span class="sxs-lookup"><span data-stu-id="8d765-123">Entire Network</span></span>    | <span data-ttu-id="8d765-124">**NetworkNeighborhood** \\ **EntireNetwork**</span><span class="sxs-lookup"><span data-stu-id="8d765-124">**NetworkNeighborhood**\\**EntireNetwork**</span></span> |
| <span data-ttu-id="8d765-125">Poste de travail</span><span class="sxs-lookup"><span data-stu-id="8d765-125">My Computer</span></span>       | <span data-ttu-id="8d765-126">**MyComputer**</span><span class="sxs-lookup"><span data-stu-id="8d765-126">**MyComputer**</span></span>                             |
| <span data-ttu-id="8d765-127">Favoris réseau</span><span class="sxs-lookup"><span data-stu-id="8d765-127">My Network Places</span></span> | <span data-ttu-id="8d765-128">**NetworkNeighborhood**</span><span class="sxs-lookup"><span data-stu-id="8d765-128">**NetworkNeighborhood**</span></span>                    |
| <span data-ttu-id="8d765-129">Ordinateur distant</span><span class="sxs-lookup"><span data-stu-id="8d765-129">Remote Computer</span></span>   | <span data-ttu-id="8d765-130">**Ordinateur_distant**</span><span class="sxs-lookup"><span data-stu-id="8d765-130">**RemoteComputer**</span></span>                         |
| <span data-ttu-id="8d765-131">Fichiers utilisateurs</span><span class="sxs-lookup"><span data-stu-id="8d765-131">Users Files</span></span>       | <span data-ttu-id="8d765-132">**UsersFiles**</span><span class="sxs-lookup"><span data-stu-id="8d765-132">**UsersFiles**</span></span>                             |



 

<span data-ttu-id="8d765-133">Les extensions distantes doivent être initialisées avec [**IRemoteComputer**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iremotecomputer).</span><span class="sxs-lookup"><span data-stu-id="8d765-133">Remote extensions must be initialized with [**IRemoteComputer**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iremotecomputer).</span></span>

## <a name="using-file-system-folders-as-junction-points"></a><span data-ttu-id="8d765-134">Utilisation des dossiers du système de fichiers en tant que points de jonction</span><span class="sxs-lookup"><span data-stu-id="8d765-134">Using File System Folders as Junction Points</span></span>

<span data-ttu-id="8d765-135">Il existe deux façons de définir des dossiers de système de fichiers en tant que points de jonction.</span><span class="sxs-lookup"><span data-stu-id="8d765-135">There are two ways to define file system folders as junction points.</span></span> <span data-ttu-id="8d765-136">L’approche la plus simple consiste à créer un dossier à l’emplacement approprié et à ajouter un point au nom du dossier, suivi du format de chaîne du CLSID de votre extension.</span><span class="sxs-lookup"><span data-stu-id="8d765-136">The simplest approach is to create a folder in the appropriate location and append a period to the folder's name, followed by the string form of the CLSID of your extension.</span></span> <span data-ttu-id="8d765-137">Seul le nom du dossier sera visible dans l’Explorateur Windows.</span><span class="sxs-lookup"><span data-stu-id="8d765-137">Only the folder name will be visible in Windows Explorer.</span></span> <span data-ttu-id="8d765-138">L’exemple suivant crée un point de jonction avec un nom d’affichage de mondossier.</span><span class="sxs-lookup"><span data-stu-id="8d765-138">The following example creates a junction point with a display name of MyFolder.</span></span>


```
MyFolder.{Extension CLSID}
```



<span data-ttu-id="8d765-139">Vous pouvez également définir un dossier nommé de façon conventionnelle comme point de jonction en :</span><span class="sxs-lookup"><span data-stu-id="8d765-139">Alternatively, you can define a conventionally named folder as a junction point by:</span></span>

-   <span data-ttu-id="8d765-140">Définition du dossier en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="8d765-140">Making the folder read-only.</span></span>
-   <span data-ttu-id="8d765-141">Création du dossier dans un dossier système en appelant [**PathMakeSystemFolder**](/windows/desktop/api/Shlwapi/nf-shlwapi-pathmakesystemfoldera).</span><span class="sxs-lookup"><span data-stu-id="8d765-141">Making the folder a system folder by calling [**PathMakeSystemFolder**](/windows/desktop/api/Shlwapi/nf-shlwapi-pathmakesystemfoldera).</span></span>
-   <span data-ttu-id="8d765-142">Placer un fichier Desktop.ini masqué dans le dossier qui comprend le CLSID de l’extension.</span><span class="sxs-lookup"><span data-stu-id="8d765-142">Placing a hidden Desktop.ini file in the folder that includes the extension's CLSID.</span></span>

<span data-ttu-id="8d765-143">Desktop.ini est un fichier texte standard qui peut être ajouté à n’importe quel dossier pour personnaliser certains aspects du comportement du dossier.</span><span class="sxs-lookup"><span data-stu-id="8d765-143">Desktop.ini is a standard text file that can be added to any folder to customize certain aspects of the folder's behavior.</span></span> <span data-ttu-id="8d765-144">Pour une présentation générale de l’utilisation de ce fichier, consultez [Comment personnaliser des dossiers avec Desktop.ini](how-to-customize-folders-with-desktop-ini.md).</span><span class="sxs-lookup"><span data-stu-id="8d765-144">For a general discussion of how to use this file, see [How to Customize Folders with Desktop.ini](how-to-customize-folders-with-desktop-ini.md).</span></span> <span data-ttu-id="8d765-145">Pour définir un dossier comme point de jonction, le \[ . \] La section ShellClassInfo de Desktop.ini doit contenir le CLSID de l’extension, comme suit :</span><span class="sxs-lookup"><span data-stu-id="8d765-145">To define a folder as a junction point, the \[.ShellClassInfo\] section of Desktop.ini must contain the extension's CLSID as follows:</span></span>


```
[.ShellClassInfo]
CLSID={Extension CLSID}
```



## <a name="opening-a-view-of-a-namespace-extension"></a><span data-ttu-id="8d765-146">Ouverture d’une vue d’une extension d’espace de noms</span><span class="sxs-lookup"><span data-stu-id="8d765-146">Opening a View of a Namespace Extension</span></span>

<span data-ttu-id="8d765-147">Quand un utilisateur accède à un point de jonction, l’Explorateur Windows crée automatiquement une vue du dossier racine.</span><span class="sxs-lookup"><span data-stu-id="8d765-147">When a user browses into a junction point, Windows Explorer automatically creates a view of the root folder.</span></span> <span data-ttu-id="8d765-148">Vous pouvez également créer une vue en lançant explicitement Explorer.exe avec le CLSID de l’extension comme argument.</span><span class="sxs-lookup"><span data-stu-id="8d765-148">You can also create a view by explicitly launching Explorer.exe with the extension's CLSID as an argument.</span></span> <span data-ttu-id="8d765-149">Vous pouvez, par exemple, utiliser cette approche pour lancer une vue d’une extension à partir d’un menu contextuel ou d’un raccourci.</span><span class="sxs-lookup"><span data-stu-id="8d765-149">You can, for instance, use this approach to launch a view of an extension from a shortcut menu or shortcut.</span></span> <span data-ttu-id="8d765-150">Par exemple, pour lancer une vue de MyExtension qui comprend une arborescence, vous pouvez utiliser la chaîne de commande suivante.</span><span class="sxs-lookup"><span data-stu-id="8d765-150">For example, to launch a view of MyExtension that includes a tree view, you can use the following command string.</span></span>


```
%SystemRoot%\Explorer.exe /e,::{MyExtension CLSID}
```



<span data-ttu-id="8d765-151">Une autre chaîne de commande peut être utilisée pour lancer une vue d’un objet dans l’extension.</span><span class="sxs-lookup"><span data-stu-id="8d765-151">An alternative command string can be used to launch a view of an object within the extension.</span></span> <span data-ttu-id="8d765-152">Cette fonctionnalité est utile, par exemple, pour une extension qui utilise un affichage des dossiers pour permettre aux utilisateurs d’afficher le contenu de l’un des nombreux fichiers compressés.</span><span class="sxs-lookup"><span data-stu-id="8d765-152">This feature would be useful, for instance, for an extension that uses a folder view to allow users to view the contents of one of a number of compressed files.</span></span>


```
%SystemRoot%\Explorer.exe /e,::{MyExtension CLSID},objectname
```



<span data-ttu-id="8d765-153">Le paramètre *ObjectName* est le nom de l’objet qui doit être affiché.</span><span class="sxs-lookup"><span data-stu-id="8d765-153">The *objectname* parameter is the name of the object that is to be viewed.</span></span> <span data-ttu-id="8d765-154">L’Explorateur Windows convertit le nom en PIDL correspondant et transmet le PIDL à la méthode [**IPersistFolder :: Initialize**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ipersistfolder-initialize) de l’objet du nouveau dossier.</span><span class="sxs-lookup"><span data-stu-id="8d765-154">Windows Explorer converts the name to its corresponding PIDL and passes the PIDL to the new folder object's [**IPersistFolder::Initialize**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ipersistfolder-initialize) method.</span></span>

> [!Note]  
> <span data-ttu-id="8d765-155">La chaîne CLSID doit être précédée d’une paire de signes deux-points ( ::) Sinon, la commande échoue.</span><span class="sxs-lookup"><span data-stu-id="8d765-155">The CLSID string must be preceded by a pair of colons (::) or the command will fail.</span></span> <span data-ttu-id="8d765-156">L’indicateur barre oblique e (/e) utilisé dans les deux exemples de lignes de commande indiqué ci-dessus demande à l’Explorateur Windows d’afficher une arborescence.</span><span class="sxs-lookup"><span data-stu-id="8d765-156">The slash-e (/e) flag used in the two sample command lines shown previously instructs Windows Explorer to display a tree view.</span></span> <span data-ttu-id="8d765-157">L’indicateur doit être séparé des deux signes deux-points par une virgule.</span><span class="sxs-lookup"><span data-stu-id="8d765-157">The flag must be separated from the two colons by a comma.</span></span> <span data-ttu-id="8d765-158">Si vous ne souhaitez pas une arborescence, omettez l’indicateur/e et la virgule.</span><span class="sxs-lookup"><span data-stu-id="8d765-158">If you do not want a tree view, omit the /e flag and the comma.</span></span>

 

 

 



