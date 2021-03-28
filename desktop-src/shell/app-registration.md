---
description: Cette rubrique explique comment les applications peuvent exposer les informations nécessaires pour activer certains scénarios.
ms.assetid: F88AA3E6-6F7B-442d-935A-7D2CB4958E6B
title: Inscription de l’application
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 857e96893d2fe717f1a4939d06c77af043ead318
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103951025"
---
# <a name="application-registration"></a><span data-ttu-id="763c7-103">Inscription de l’application</span><span class="sxs-lookup"><span data-stu-id="763c7-103">Application Registration</span></span>

<span data-ttu-id="763c7-104">Cette rubrique explique comment les applications peuvent exposer les informations nécessaires pour activer certains scénarios.</span><span class="sxs-lookup"><span data-stu-id="763c7-104">This topic discusses how applications can expose information about themselves necessary to enable certain scenarios.</span></span> <span data-ttu-id="763c7-105">Cela comprend les informations nécessaires pour localiser l’application, les verbes pris en charge par l’application et les types de fichiers qu’une application peut gérer.</span><span class="sxs-lookup"><span data-stu-id="763c7-105">This includes information needed to locate the application, the verbs that the application supports and the types of files that an application can handle.</span></span>

<span data-ttu-id="763c7-106">Cette rubrique est organisée comme suit :</span><span class="sxs-lookup"><span data-stu-id="763c7-106">This topic is organized as follows:</span></span>

-   [<span data-ttu-id="763c7-107">Recherche d’un exécutable d’application</span><span class="sxs-lookup"><span data-stu-id="763c7-107">Finding an Application Executable</span></span>](#finding-an-application-executable)
-   [<span data-ttu-id="763c7-108">Inscription des applications</span><span class="sxs-lookup"><span data-stu-id="763c7-108">Registering Applications</span></span>](#registering-applications)
    -   [<span data-ttu-id="763c7-109">Utilisation de la sous-clé Paths de l’application</span><span class="sxs-lookup"><span data-stu-id="763c7-109">Using the App Paths Subkey</span></span>](#using-the-app-paths-subkey)
    -   [<span data-ttu-id="763c7-110">Utilisation de la sous-clé applications</span><span class="sxs-lookup"><span data-stu-id="763c7-110">Using the Applications Subkey</span></span>](#using-the-applications-subkey)
-   [<span data-ttu-id="763c7-111">Inscription de verbes et d’autres informations d’association de fichiers</span><span class="sxs-lookup"><span data-stu-id="763c7-111">Registering Verbs and Other File Association Information</span></span>](#registering-verbs-and-other-file-association-information)
-   [<span data-ttu-id="763c7-112">Inscription d’un type perçu</span><span class="sxs-lookup"><span data-stu-id="763c7-112">Registering a Perceived Type</span></span>](#registering-a-perceived-type)
-   [<span data-ttu-id="763c7-113">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="763c7-113">Related topics</span></span>](#related-topics)

> [!Note]  
> <span data-ttu-id="763c7-114">Les applications peuvent également être inscrites dans les applications configurer les paramètres d’accès aux programmes et les paramètres par défaut de l’ordinateur (SPAD) et définir les applications du panneau de configuration des programmes par défaut (SYDP).</span><span class="sxs-lookup"><span data-stu-id="763c7-114">Applications can also be registered in the Set Program Access and Computer Defaults (SPAD) and Set Your Default Programs (SYDP) control panel applications.</span></span> <span data-ttu-id="763c7-115">Pour plus d’informations sur SPAD et l’inscription des applications SYDP, consultez [instructions pour les associations de fichiers et les programmes par défaut](appguide-fa-defpro.md), et [définir les paramètres par défaut de l’accès aux programmes et des ordinateurs (SPAD)](cpl-setprogramaccess.md).</span><span class="sxs-lookup"><span data-stu-id="763c7-115">For information about SPAD and SYDP application registration, see [Guidelines for File Associations and Default Programs](appguide-fa-defpro.md), and [Set Program Access and Computer Defaults (SPAD)](cpl-setprogramaccess.md).</span></span>

 

## <a name="finding-an-application-executable"></a><span data-ttu-id="763c7-116">Recherche d’un exécutable d’application</span><span class="sxs-lookup"><span data-stu-id="763c7-116">Finding an Application Executable</span></span>

<span data-ttu-id="763c7-117">Lorsque la fonction [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa) est appelée avec le nom d’un fichier exécutable dans son paramètre *lpFile* , il y a plusieurs emplacements où la fonction recherche le fichier.</span><span class="sxs-lookup"><span data-stu-id="763c7-117">When the [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa) function is called with the name of an executable file in its *lpFile* parameter, there are several places where the function looks for the file.</span></span> <span data-ttu-id="763c7-118">Nous vous recommandons d’inscrire votre application dans la sous-clé de Registre **App Paths** .</span><span class="sxs-lookup"><span data-stu-id="763c7-118">We recommend registering your application in the **App Paths** registry subkey.</span></span> <span data-ttu-id="763c7-119">Cela permet d’éviter que des applications modifient la variable d’environnement du chemin d’accès système.</span><span class="sxs-lookup"><span data-stu-id="763c7-119">Doing so avoids the need for applications to modify the system PATH environment variable.</span></span>

<span data-ttu-id="763c7-120">Le fichier est recherché dans les emplacements suivants :</span><span class="sxs-lookup"><span data-stu-id="763c7-120">The file is sought in the following locations:</span></span>

-   <span data-ttu-id="763c7-121">Le répertoire de travail actuel</span><span class="sxs-lookup"><span data-stu-id="763c7-121">The current working directory.</span></span>
-   <span data-ttu-id="763c7-122">Répertoire **Windows** uniquement (aucun sous-répertoire n’est recherché).</span><span class="sxs-lookup"><span data-stu-id="763c7-122">The **Windows** directory only (no subdirectories are searched).</span></span>
-   <span data-ttu-id="763c7-123">Répertoire **\\ system32 de Windows** .</span><span class="sxs-lookup"><span data-stu-id="763c7-123">The **Windows\\System32** directory.</span></span>
-   <span data-ttu-id="763c7-124">Répertoires figurant dans la variable d’environnement PATH.</span><span class="sxs-lookup"><span data-stu-id="763c7-124">Directories listed in the PATH environment variable.</span></span>
-   <span data-ttu-id="763c7-125">Recommandé : **HKEY \_ local \_ machine** \\ **Software** \\ **Microsoft** \\ **Windows** \\ **CurrentVersion** \\ **app Path**</span><span class="sxs-lookup"><span data-stu-id="763c7-125">Recommended: **HKEY\_LOCAL\_MACHINE**\\**SOFTWARE**\\**Microsoft**\\**Windows**\\**CurrentVersion**\\**App Paths**</span></span>

## <a name="registering-applications"></a><span data-ttu-id="763c7-126">Inscription des applications</span><span class="sxs-lookup"><span data-stu-id="763c7-126">Registering Applications</span></span>

<span data-ttu-id="763c7-127">Les sous-clés de registre des **applications** et des **chemins d’application** sont utilisées pour enregistrer et contrôler le comportement du système pour le compte des applications.</span><span class="sxs-lookup"><span data-stu-id="763c7-127">Both the **App Paths** and **Applications** registry subkeys are used to register and control the behavior of the system on behalf of applications.</span></span> <span data-ttu-id="763c7-128">La sous-clé **paths** de l’application est l’emplacement par défaut.</span><span class="sxs-lookup"><span data-stu-id="763c7-128">The **App Paths** subkey is the preferred location.</span></span>

### <a name="using-the-app-paths-subkey"></a><span data-ttu-id="763c7-129">Utilisation de la sous-clé Paths de l’application</span><span class="sxs-lookup"><span data-stu-id="763c7-129">Using the App Paths Subkey</span></span>

<span data-ttu-id="763c7-130">Dans Windows 7 et versions ultérieures, nous vous recommandons vivement d’installer les applications par utilisateur plutôt qu’par ordinateur.</span><span class="sxs-lookup"><span data-stu-id="763c7-130">In Windows 7 and later, we strongly recommend you install applications per user rather than per machine.</span></span> <span data-ttu-id="763c7-131">Une application installée pour par utilisateur peut être inscrite sous **HKEY \_ Current \_ User** \\ **Software** \\ **Microsoft** \\ **Windows** \\ **CurrentVersion** \\ **App Paths**.</span><span class="sxs-lookup"><span data-stu-id="763c7-131">An application that is installed for per user can be registered under **HKEY\_CURRENT\_USER**\\**Software**\\**Microsoft**\\**Windows**\\**CurrentVersion**\\**App Paths**.</span></span> <span data-ttu-id="763c7-132">Une application installée pour tous les utilisateurs de l’ordinateur peut être inscrite sous **HKEY \_ local \_ machine** \\ **Software** \\ **Microsoft** \\ **Windows** \\ **CurrentVersion** \\ **App Paths**.</span><span class="sxs-lookup"><span data-stu-id="763c7-132">An application that is installed for all users of the computer can be registered under **HKEY\_LOCAL\_MACHINE**\\**Software**\\**Microsoft**\\**Windows**\\**CurrentVersion**\\**App Paths**.</span></span>

<span data-ttu-id="763c7-133">Les entrées trouvées sous les **chemins d’accès aux applications** sont principalement utilisées pour les opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="763c7-133">The entries found under **App Paths** are used primarily for the following purposes:</span></span>

-   <span data-ttu-id="763c7-134">Pour mapper le nom du fichier exécutable d’une application au chemin d’accès complet de ce fichier.</span><span class="sxs-lookup"><span data-stu-id="763c7-134">To map an application's executable file name to that file's fully qualified path.</span></span>
-   <span data-ttu-id="763c7-135">Pour prédéfinir les informations de la variable d’environnement PATH pour chaque application, par processus.</span><span class="sxs-lookup"><span data-stu-id="763c7-135">To pre-pend information to the PATH environment variable on a per-application, per-process basis.</span></span>

<span data-ttu-id="763c7-136">Si le nom d’une sous-clé de **chemins d’accès d’application** correspond au nom de fichier, l’interpréteur de commandes effectue deux actions :</span><span class="sxs-lookup"><span data-stu-id="763c7-136">If the name of a subkey of **App Paths** matches the file name, the Shell performs two actions:</span></span>

-   <span data-ttu-id="763c7-137">L’entrée (par défaut) est utilisée en tant que chemin d’accès qualifié complet du fichier.</span><span class="sxs-lookup"><span data-stu-id="763c7-137">The (Default) entry is used as the file's fully qualified path.</span></span>
-   <span data-ttu-id="763c7-138">L’entrée de chemin d’accès de cette sous-clé est précédée de la variable d’environnement PATH de ce processus.</span><span class="sxs-lookup"><span data-stu-id="763c7-138">The Path entry for that subkey is pre-pended to the PATH environment variable of that process.</span></span> <span data-ttu-id="763c7-139">Si ce n’est pas nécessaire, la valeur du chemin d’accès peut être omise.</span><span class="sxs-lookup"><span data-stu-id="763c7-139">If this is not required, the Path value can be omitted.</span></span>

<span data-ttu-id="763c7-140">Les problèmes potentiels à prendre en compte sont les suivants :</span><span class="sxs-lookup"><span data-stu-id="763c7-140">Potential issues to be aware of include:</span></span>

-   <span data-ttu-id="763c7-141">L’interpréteur de commandes limite la longueur d’une ligne de commande à un chemin d’accès maximal de \_ \* 2 caractères.</span><span class="sxs-lookup"><span data-stu-id="763c7-141">The Shell limits the length of a command line to MAX\_PATH \* 2 characters.</span></span> <span data-ttu-id="763c7-142">Si de nombreux fichiers sont répertoriés comme entrées de registre ou si leurs chemins d’accès sont longs, les noms de fichiers plus loin dans la liste peuvent être perdus lorsque la ligne de commande est tronquée.</span><span class="sxs-lookup"><span data-stu-id="763c7-142">If there are many files listed as registry entries or their paths are long, file names later in the list could be lost as the command line is truncated.</span></span>
-   <span data-ttu-id="763c7-143">Certaines applications n’acceptent pas plusieurs noms de fichiers dans une ligne de commande.</span><span class="sxs-lookup"><span data-stu-id="763c7-143">Some applications do not accept multiple file names in a command line.</span></span>
-   <span data-ttu-id="763c7-144">Certaines applications qui acceptent plusieurs noms de fichiers ne reconnaissent pas le format dans lequel l’interpréteur de commandes les fournit.</span><span class="sxs-lookup"><span data-stu-id="763c7-144">Some applications that accept multiple file names do not recognize the format in which the Shell provides them.</span></span> <span data-ttu-id="763c7-145">L’interpréteur de commandes fournit la liste de paramètres sous la forme d’une chaîne entre guillemets, mais certaines applications peuvent nécessiter des chaînes sans guillemets.</span><span class="sxs-lookup"><span data-stu-id="763c7-145">The Shell provides the parameter list as a quoted string, but some applications might require strings without quotes.</span></span>
-   <span data-ttu-id="763c7-146">Tous les éléments qui peuvent être déplacés ne font pas partie du système de fichiers. par exemple, imprimantes.</span><span class="sxs-lookup"><span data-stu-id="763c7-146">Not all items that can be dragged are part of the file system; for example, printers.</span></span> <span data-ttu-id="763c7-147">Comme ces éléments n’ont pas de chemin d’accès Win32 standard, il n’est pas possible de fournir une valeur *lpParameters* significative à [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa).</span><span class="sxs-lookup"><span data-stu-id="763c7-147">These items do not have a standard Win32 path, so there is no way to provide a meaningful *lpParameters* value to [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa).</span></span>

<span data-ttu-id="763c7-148">L’utilisation de l’entrée DropTarget permet d’éviter ces problèmes potentiels en fournissant un accès à tous les formats de presse-papiers, y compris [CFSTR \_ SHELLIDLIST](clipboard.md) (pour les listes de fichiers longues) et [CFSTR \_ FILECONTENTS](clipboard.md) (pour les objets non-système de fichiers).</span><span class="sxs-lookup"><span data-stu-id="763c7-148">Using the DropTarget entry avoids these potential issues by providing access to all of the clipboard formats, including [CFSTR\_SHELLIDLIST](clipboard.md) (for long file lists) and [CFSTR\_FILECONTENTS](clipboard.md) (for non-file-system objects).</span></span>

<span data-ttu-id="763c7-149">**Pour inscrire et contrôler le comportement de vos applications avec la sous-clé chemins d’accès de l’application**:</span><span class="sxs-lookup"><span data-stu-id="763c7-149">**To register and control the behavior of your applications with the App Paths subkey**:</span></span>

1.  <span data-ttu-id="763c7-150">Ajoutez une sous-clé portant le même nom que votre fichier exécutable à la sous-clé **chemins d’accès** de l’application, comme indiqué dans l’entrée de Registre suivante.</span><span class="sxs-lookup"><span data-stu-id="763c7-150">Add a subkey with the same name as your executable file to the **App Paths** subkey, as shown in the following registry entry.</span></span>

    ```
    HKEY_LOCAL_MACHINE or HKEY_CURRENT_USER
       SOFTWARE
          Microsoft
             Windows
                CurrentVersion
                   App Paths
                      file.exe
                         (Default)
                         DontUseDesktopChangeRouter
                         DropTarget
                         Path
                         UseUrl
    ```

2.  <span data-ttu-id="763c7-151">Consultez le tableau suivant pour plus d’informations sur les entrées de la sous-clé **paths** de l’application.</span><span class="sxs-lookup"><span data-stu-id="763c7-151">See the following table for details of the **App Paths** subkey entries.</span></span> 

    <table>
    <colgroup>
    <col style="width: 50%" />
    <col style="width: 50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th><span data-ttu-id="763c7-152">Entrée de Registre</span><span class="sxs-lookup"><span data-stu-id="763c7-152">Registry entry</span></span></th>
    <th><span data-ttu-id="763c7-153">Détails</span><span class="sxs-lookup"><span data-stu-id="763c7-153">Details</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td><span data-ttu-id="763c7-154">(Par défaut)</span><span class="sxs-lookup"><span data-stu-id="763c7-154">(Default)</span></span></td>
    <td><span data-ttu-id="763c7-155">Est le chemin d’accès complet à l’application.</span><span class="sxs-lookup"><span data-stu-id="763c7-155">Is the fully qualified path to the application.</span></span> <span data-ttu-id="763c7-156">Le nom de l’application fourni dans l’entrée (valeur par défaut) peut être indiqué avec ou sans l’extension. exe.</span><span class="sxs-lookup"><span data-stu-id="763c7-156">The application name provided in the (Default) entry can be stated with or without its .exe extension.</span></span> <span data-ttu-id="763c7-157">Si nécessaire, la fonction <a href="/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa"><strong>ShellExecuteEx</strong></a> ajoute l’extension lors de la recherche de la sous-clé <strong>chemins d’accès</strong> de l’application.</span><span class="sxs-lookup"><span data-stu-id="763c7-157">If necessary, the <a href="/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa"><strong>ShellExecuteEx</strong></a> function adds the extension when searching <strong>App Paths</strong> subkey.</span></span> <span data-ttu-id="763c7-158">L’entrée est du type de <strong>REG_SZ</strong> .</span><span class="sxs-lookup"><span data-stu-id="763c7-158">The entry is of the <strong>REG_SZ</strong> type.</span></span></td>
    </tr>
    <tr class="even">
    <td><span data-ttu-id="763c7-159">DontUseDesktopChangeRouter</span><span class="sxs-lookup"><span data-stu-id="763c7-159">DontUseDesktopChangeRouter</span></span></td>
    <td><span data-ttu-id="763c7-160">Est obligatoire pour les applications du débogueur afin d’éviter les blocages de boîtes de dialogue de fichier lors du débogage du processus de l’Explorateur Windows.</span><span class="sxs-lookup"><span data-stu-id="763c7-160">Is mandatory for debugger applications to avoid file dialog deadlocks when debugging the Windows Explorer process.</span></span> <span data-ttu-id="763c7-161">Toutefois, la définition de l’entrée DontUseDesktopChangeRouter produit une gestion légèrement moins efficace des notifications de modification.</span><span class="sxs-lookup"><span data-stu-id="763c7-161">Setting the DontUseDesktopChangeRouter entry produces a slightly less efficient handling of the change notifications, however.</span></span> <span data-ttu-id="763c7-162">L’entrée est du type de <strong>REG_DWORD</strong> et la valeur est 0x1.</span><span class="sxs-lookup"><span data-stu-id="763c7-162">The entry is of the <strong>REG_DWORD</strong> type and the value is 0x1.</span></span></td>
    </tr>
    <tr class="odd">
    <td><span data-ttu-id="763c7-163">DropTarget</span><span class="sxs-lookup"><span data-stu-id="763c7-163">DropTarget</span></span></td>
    <td><span data-ttu-id="763c7-164">Identificateur de classe (CLSID).</span><span class="sxs-lookup"><span data-stu-id="763c7-164">Is a class identifier (CLSID).</span></span> <span data-ttu-id="763c7-165">L’entrée DropTarget contient le CLSID d’un objet (généralement un serveur local plutôt qu’un serveur in-process) qui implémente <a href="/windows/desktop/api/oleidl/nn-oleidl-idroptarget"><strong>IDropTarget</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="763c7-165">The DropTarget entry contains the CLSID of an object (usually a local server rather than an in-process server) that implements <a href="/windows/desktop/api/oleidl/nn-oleidl-idroptarget"><strong>IDropTarget</strong></a>.</span></span> <span data-ttu-id="763c7-166">Par défaut, lorsque la cible de déplacement est un fichier exécutable et qu’aucune valeur DropTarget n’est fournie, l’interpréteur de commandes convertit la liste des fichiers déplacés en un paramètre de ligne de commande et le transmet à <a href="/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa"><strong>ShellExecuteEx</strong></a> via <em>lpParameters</em>.</span><span class="sxs-lookup"><span data-stu-id="763c7-166">By default, when the drop target is an executable file, and no DropTarget value is provided, the Shell converts the list of dropped files into a command-line parameter and passes it to <a href="/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa"><strong>ShellExecuteEx</strong></a> through <em>lpParameters</em>.</span></span></td>
    </tr>
    <tr class="even">
    <td><span data-ttu-id="763c7-167">Path</span><span class="sxs-lookup"><span data-stu-id="763c7-167">Path</span></span></td>
    <td><span data-ttu-id="763c7-168">Fournit une chaîne (sous la forme d’une liste de répertoires séparés par des points-virgules) à ajouter à la variable d’environnement PATH quand une application est lancée en appelant <a href="/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa"><strong>ShellExecuteEx</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="763c7-168">Supplies a string (in the form of a semicolon-separated list of directories) to append to the PATH environment variable when an application is launched by calling <a href="/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa"><strong>ShellExecuteEx</strong></a>.</span></span> <span data-ttu-id="763c7-169">Il s’agit du chemin d’accès complet au fichier. exe.</span><span class="sxs-lookup"><span data-stu-id="763c7-169">It is the fully qualified path to the .exe.</span></span> <span data-ttu-id="763c7-170">Elle est de <strong>REG_SZ</strong>.</span><span class="sxs-lookup"><span data-stu-id="763c7-170">It is of <strong>REG_SZ</strong>.</span></span> <span data-ttu-id="763c7-171">Dans <strong>Windows 7 et versions ultérieures</strong>, le type peut être <strong>REG_EXPAND_SZ</strong>, et est généralement <strong>REG_EXPAND_SZ</strong> % ProgramFiles%.</span><span class="sxs-lookup"><span data-stu-id="763c7-171">In <strong>Windows 7 and later</strong>, the type can be <strong>REG_EXPAND_SZ</strong>, and is commonly <strong>REG_EXPAND_SZ</strong> %ProgramFiles%.</span></span>
    <blockquote>
    [!Note]<br />
<span data-ttu-id="763c7-172">En plus des entrées (par défaut), path et DropTarget reconnues par l’interpréteur de commandes, une application peut également ajouter des valeurs personnalisées à la sous-clé <strong>chemins d’accès</strong> de l’application de son fichier exécutable.</span><span class="sxs-lookup"><span data-stu-id="763c7-172">In addition to the (Default), Path, and DropTarget entries recognized by the Shell, an application can also add custom values to its executable file's <strong>App Paths</strong> subkey.</span></span> <span data-ttu-id="763c7-173">Nous encourageons les développeurs d’applications à utiliser la sous-clé <strong>paths</strong> de l’application pour fournir un chemin d’accès spécifique à l’application au lieu d’apporter des ajouts au chemin d’accès du système global.</span><span class="sxs-lookup"><span data-stu-id="763c7-173">We encourage application developers to use the <strong>App Paths</strong> subkey to provide an application-specific path instead of making additions to the global system path.</span></span>
    </blockquote>
    <br/></td>
    </tr>
    <tr class="odd">
    <td><span data-ttu-id="763c7-174">SupportedProtocols</span><span class="sxs-lookup"><span data-stu-id="763c7-174">SupportedProtocols</span></span></td>
    <td><span data-ttu-id="763c7-175">Crée une chaîne qui contient les schémas de protocole d’URL pour une clé donnée.</span><span class="sxs-lookup"><span data-stu-id="763c7-175">Creates a string that contains the URL protocol schemes for a given key.</span></span> <span data-ttu-id="763c7-176">Peut contenir plusieurs valeurs de Registre pour indiquer les schémas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="763c7-176">This can contain multiple registry values to indicate which schemes are supported.</span></span> <span data-ttu-id="763c7-177">Cette chaîne suit le format <strong>scheme1 : scheme2</strong>.</span><span class="sxs-lookup"><span data-stu-id="763c7-177">This string follows the format of <strong>scheme1:scheme2</strong>.</span></span> <span data-ttu-id="763c7-178">Si cette liste n’est pas vide, le <strong>fichier :</strong> sera ajouté à la chaîne.</span><span class="sxs-lookup"><span data-stu-id="763c7-178">If this list is not empty, <strong>file:</strong> will be added to the string.</span></span> <span data-ttu-id="763c7-179">Ce protocole est pris en charge implicitement quand <em>SupportedProtocols</em> est défini.</span><span class="sxs-lookup"><span data-stu-id="763c7-179">This protocol is implicitly supported when <em>SupportedProtocols</em> is defined.</span></span> <br/></td>
    </tr>
    <tr class="even">
    <td><span data-ttu-id="763c7-180">UseUrl</span><span class="sxs-lookup"><span data-stu-id="763c7-180">UseUrl</span></span></td>
    <td><span data-ttu-id="763c7-181">Indique que votre application peut accepter une URL (au lieu d’un nom de fichier) sur la ligne de commande.</span><span class="sxs-lookup"><span data-stu-id="763c7-181">Indicates that your application can accept a URL (instead of a file name) on the command line.</span></span> <span data-ttu-id="763c7-182">Les applications qui peuvent ouvrir des documents directement à partir d’Internet, comme les navigateurs Web et les lecteurs multimédias, doivent définir cette entrée.</span><span class="sxs-lookup"><span data-stu-id="763c7-182">Applications that can open documents directly from the internet, like web browsers and media players, should set this entry.</span></span> <br/> <span data-ttu-id="763c7-183">Lorsque la fonction <a href="/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa"><strong>ShellExecuteEx</strong></a> démarre une application et que la valeur UseUrl = 1 n’est pas définie, <strong>ShellExecuteEx</strong> télécharge le document dans un fichier local et appelle le gestionnaire sur la copie locale.</span><span class="sxs-lookup"><span data-stu-id="763c7-183">When the <a href="/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa"><strong>ShellExecuteEx</strong></a> function starts an application and the UseUrl=1 value is not set, <strong>ShellExecuteEx</strong> downloads the document to a local file and invokes the handler on the local copy.</span></span><br/> <span data-ttu-id="763c7-184">Par exemple, si cette entrée est définie pour l’application et qu’un utilisateur clique avec le bouton droit sur un fichier stocké sur un serveur Web, le verbe Open est rendu disponible.</span><span class="sxs-lookup"><span data-stu-id="763c7-184">For example, if the application has this entry set and a user right-clicks on a file stored on a web server, the Open verb will be made available.</span></span> <span data-ttu-id="763c7-185">Si ce n’est pas le cas, l’utilisateur doit télécharger le fichier et ouvrir la copie locale.</span><span class="sxs-lookup"><span data-stu-id="763c7-185">If not, the user will have to download the file and open the local copy.</span></span> <br/> <span data-ttu-id="763c7-186">L’entrée UseUrl est de type <strong>REG_DWORD</strong> , et la valeur est 0x1.</span><span class="sxs-lookup"><span data-stu-id="763c7-186">The UseUrl entry is of <strong>REG_DWORD</strong> type, and the value is 0x1.</span></span><br/> <span data-ttu-id="763c7-187">Dans Windows Vista et les versions antérieures, cette entrée indique que l’URL doit être transmise à l’application avec un nom de fichier local, lorsqu’elle est appelée via ShellExecuteEx.</span><span class="sxs-lookup"><span data-stu-id="763c7-187">In Windows Vista and earlier, this entry indicated that the URL should be passed to the application along with a local file name, when called via ShellExecuteEx.</span></span> <span data-ttu-id="763c7-188">Dans Windows 7, il indique que l’application peut comprendre toute URL http ou HTTPS qui lui est transmise, sans avoir à fournir également le nom du fichier cache.</span><span class="sxs-lookup"><span data-stu-id="763c7-188">In Windows 7, it indicates that the application can understand any http or https url that is passed to it, without having to supply the cache file name as well.</span></span> <span data-ttu-id="763c7-189">Cette clé de Registre est associée à la clé <em>SupportedProtocols</em> .</span><span class="sxs-lookup"><span data-stu-id="763c7-189">This registry key is associated with the <em>SupportedProtocols</em> key.</span></span><br/></td>
    </tr>
    </tbody>
    </table>

    

     

### <a name="using-the-applications-subkey"></a><span data-ttu-id="763c7-190">Utilisation de la sous-clé applications</span><span class="sxs-lookup"><span data-stu-id="763c7-190">Using the Applications Subkey</span></span>

<span data-ttu-id="763c7-191">Grâce à l’inclusion d’entrées de Registre sous la sous-clé de l’application **\_ \_ racine HKEY classes** \\  \\ *ApplicationName.exe* , les applications peuvent fournir les informations spécifiques à l’application, comme indiqué dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="763c7-191">Through the inclusion of registry entries under the **HKEY\_CLASSES\_ROOT**\\**Applications**\\*ApplicationName.exe* subkey, applications can provide the application-specific information shown in the following table.</span></span>



| <span data-ttu-id="763c7-192">Entrée de Registre</span><span class="sxs-lookup"><span data-stu-id="763c7-192">Registry entry</span></span>                   | <span data-ttu-id="763c7-193">Description</span><span class="sxs-lookup"><span data-stu-id="763c7-193">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|----------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="763c7-194">verbe de Shell \\</span><span class="sxs-lookup"><span data-stu-id="763c7-194">shell\\verb</span></span>                      | <span data-ttu-id="763c7-195">Fournit la méthode Verb pour appeler l’application à partir de OpenWith.</span><span class="sxs-lookup"><span data-stu-id="763c7-195">Provides the verb method for calling the application from OpenWith.</span></span> <span data-ttu-id="763c7-196">Sans définition de verbe spécifiée ici, le système suppose que l’application prend en charge [**CreateProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa)et transmet le nom de fichier sur la ligne de commande.</span><span class="sxs-lookup"><span data-stu-id="763c7-196">Without a verb definition specified here, the system assumes that the application supports [**CreateProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa), and passes the file name on the command line.</span></span> <span data-ttu-id="763c7-197">Cette fonctionnalité s’applique à toutes les méthodes de verbe, notamment DropTarget, ExecuteCommand et échange dynamique de données (DDE).</span><span class="sxs-lookup"><span data-stu-id="763c7-197">This functionality applies to all the verb methods, including DropTarget, ExecuteCommand, and Dynamic Data Exchange (DDE).</span></span>                                                                                                                                                                                                                                                                                                                            |
| <span data-ttu-id="763c7-198">DefaultIcon</span><span class="sxs-lookup"><span data-stu-id="763c7-198">DefaultIcon</span></span>                      | <span data-ttu-id="763c7-199">Permet à une application de fournir une icône spécifique pour représenter l’application au lieu de la première icône stockée dans le fichier. exe.</span><span class="sxs-lookup"><span data-stu-id="763c7-199">Enables an application to provide a specific icon to represent the application instead of the first icon stored in the .exe file.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| <span data-ttu-id="763c7-200">FriendlyAppName</span><span class="sxs-lookup"><span data-stu-id="763c7-200">FriendlyAppName</span></span>                  | <span data-ttu-id="763c7-201">Fournit un moyen d’obtenir un nom localisable à afficher pour une application au lieu de simplement les informations de version qui apparaissent, qui peuvent ne pas être localisables.</span><span class="sxs-lookup"><span data-stu-id="763c7-201">Provides a way to get a localizable name to display for an application instead of just the version information appearing, which may not be localizable.</span></span> <span data-ttu-id="763c7-202">La requête d’association [**ASSOCSTR**](/windows/desktop/api/Shlwapi/ne-shlwapi-assocstr) lit cette valeur d’entrée de Registre et revient à utiliser le nom de FileDescription dans les informations de version.</span><span class="sxs-lookup"><span data-stu-id="763c7-202">The association query [**ASSOCSTR**](/windows/desktop/api/Shlwapi/ne-shlwapi-assocstr) reads this registry entry value and falls back to use the FileDescription name in the version information.</span></span> <span data-ttu-id="763c7-203">Si ce nom est manquant, la requête d’association prend par défaut le nom d’affichage du fichier.</span><span class="sxs-lookup"><span data-stu-id="763c7-203">If that name is missing, the association query defaults to the display name of the file.</span></span> <span data-ttu-id="763c7-204">Les applications doivent utiliser **ASSOCSTR \_ FRIENDLYAPPNAME** pour récupérer ces informations afin d’obtenir le comportement approprié.</span><span class="sxs-lookup"><span data-stu-id="763c7-204">Applications should use **ASSOCSTR\_FRIENDLYAPPNAME** to retrieve this information to obtain the proper behavior.</span></span>                                                                                                                                                                        |
| <span data-ttu-id="763c7-205">SupportedTypes</span><span class="sxs-lookup"><span data-stu-id="763c7-205">SupportedTypes</span></span>                   | <span data-ttu-id="763c7-206">Répertorie les types de fichiers pris en charge par l’application.</span><span class="sxs-lookup"><span data-stu-id="763c7-206">Lists the file types that the application supports.</span></span> <span data-ttu-id="763c7-207">Cela permet à l’application d’être listée dans le menu cascade de la boîte de dialogue **Ouvrir avec** .</span><span class="sxs-lookup"><span data-stu-id="763c7-207">Doing so enables the application to be listed in the cascade menu of the **Open with** dialog box.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span data-ttu-id="763c7-208">NoOpenWith</span><span class="sxs-lookup"><span data-stu-id="763c7-208">NoOpenWith</span></span>                       | <span data-ttu-id="763c7-209">Indique qu’aucune application n’est spécifiée pour l’ouverture de ce type de fichier.</span><span class="sxs-lookup"><span data-stu-id="763c7-209">Indicates that no application is specified for opening this file type.</span></span> <span data-ttu-id="763c7-210">Sachez que si une sous-clé OpenWithProgIDs a été définie pour une application par type de fichier et que la sous-clé ProgID elle-même n’a pas d’entrée NoOpenWith, celle-ci apparaît dans la liste des applications recommandées ou disponibles, même si elle a spécifié l’entrée NoOpenWith.</span><span class="sxs-lookup"><span data-stu-id="763c7-210">Be aware that if an OpenWithProgIDs subkey has been set for an application by file type, and the ProgID subkey itself does not also have a NoOpenWith entry, that application will appear in the list of recommended or available applications even if it has specified the NoOpenWith entry.</span></span> <span data-ttu-id="763c7-211">Pour plus d’informations, consultez [Comment inclure une application dans la boîte de dialogue Ouvrir avec](how-to-include-an-application-on-the-open-with-dialog-box.md) et [Comment exclure une application de la boîte de dialogue Ouvrir avec](how-to-exclude-an-application-from-the-open-with-dialog-box-for-unassociated-file-types.md).</span><span class="sxs-lookup"><span data-stu-id="763c7-211">For more information, see [How to How to Include an Application in the Open With Dialog Box](how-to-include-an-application-on-the-open-with-dialog-box.md) and [How to exclude an Application from the Open with Dialog Box](how-to-exclude-an-application-from-the-open-with-dialog-box-for-unassociated-file-types.md).</span></span><br/> |
| <span data-ttu-id="763c7-212">IsHostApp</span><span class="sxs-lookup"><span data-stu-id="763c7-212">IsHostApp</span></span>                        | <span data-ttu-id="763c7-213">Indique que le processus est un processus hôte, par exemple Rundll32.exe ou Dllhost.exe, et qu’il ne doit pas être pris en compte pour l’épinglage du menu **Démarrer** ou pour l’inclusion dans la liste la plus fréquemment utilisée (MFU).</span><span class="sxs-lookup"><span data-stu-id="763c7-213">Indicates that the process is a host process, such as Rundll32.exe or Dllhost.exe, and should not be considered for **Start** menu pinning or inclusion in the Most Frequently Used (MFU) list.</span></span> <span data-ttu-id="763c7-214">Lorsqu’il est lancé avec un raccourci qui contient une liste d’arguments non null ou un [ID de modèle d’utilisateur d’application explicite (AppUserModelIDs)](appids.md), le processus peut être épinglé (comme ce raccourci).</span><span class="sxs-lookup"><span data-stu-id="763c7-214">When launched with a shortcut that contains a non-null argument list or an explicit [Application User Model IDs (AppUserModelIDs)](appids.md), the process can be pinned (as that shortcut).</span></span> <span data-ttu-id="763c7-215">Ces raccourcis sont des candidats à inclure dans la liste des MFU.</span><span class="sxs-lookup"><span data-stu-id="763c7-215">Such shortcuts are candidates for inclusion in the MFU list.</span></span>                                                                                                                                                                                                                                                  |
| <span data-ttu-id="763c7-216">NoStartPage</span><span class="sxs-lookup"><span data-stu-id="763c7-216">NoStartPage</span></span>                      | <span data-ttu-id="763c7-217">Indique que l’exécutable et les raccourcis de l’application doivent être exclus du menu **Démarrer** et de l’épinglage ou de l’inclusion dans la liste des applications les plus fréquemment exécutées.</span><span class="sxs-lookup"><span data-stu-id="763c7-217">Indicates that the application executable and shortcuts should be excluded from the **Start** menu and from pinning or inclusion in the MFU list.</span></span> <span data-ttu-id="763c7-218">Cette entrée est généralement utilisée pour exclure les outils système, les programmes d’installation et les programmes de désinstallation, ainsi que les fichiers Lisez-moi.</span><span class="sxs-lookup"><span data-stu-id="763c7-218">This entry is typically used to exclude system tools, installers and uninstallers, and readme files.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span data-ttu-id="763c7-219">UseExecutableForTaskbarGroupIcon</span><span class="sxs-lookup"><span data-stu-id="763c7-219">UseExecutableForTaskbarGroupIcon</span></span> | <span data-ttu-id="763c7-220">Fait en sorte que la barre des tâches utilise l’icône par défaut de cet exécutable s’il n’y a aucun raccourci regroupement pour cette application, et au lieu de l’icône de la fenêtre qui a été rencontrée pour la première fois.</span><span class="sxs-lookup"><span data-stu-id="763c7-220">Causes the taskbar to use the default icon of this executable if there is no pinnable shortcut for this application, and instead of the icon of the window that was first encountered.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span data-ttu-id="763c7-221">TaskbarGroupIcon</span><span class="sxs-lookup"><span data-stu-id="763c7-221">TaskbarGroupIcon</span></span>                 | <span data-ttu-id="763c7-222">Spécifie l’icône utilisée pour remplacer l’icône de la barre des tâches.</span><span class="sxs-lookup"><span data-stu-id="763c7-222">Specifies the icon used to override the taskbar icon.</span></span> <span data-ttu-id="763c7-223">L’icône de la fenêtre est normalement utilisée pour la barre des tâches.</span><span class="sxs-lookup"><span data-stu-id="763c7-223">The window icon is normally used for the taskbar.</span></span> <span data-ttu-id="763c7-224">La définition de l’entrée TaskbarGroupIcon fait en sorte que le système utilise l’icône du fichier. exe de l’application à la place.</span><span class="sxs-lookup"><span data-stu-id="763c7-224">Setting the TaskbarGroupIcon entry causes the system to use the icon from the .exe for the application instead.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |



 

### <a name="examples"></a><span data-ttu-id="763c7-225">Exemples</span><span class="sxs-lookup"><span data-stu-id="763c7-225">Examples</span></span>

<span data-ttu-id="763c7-226">Voici quelques exemples d’inscriptions d’applications par le biais des applications **\_ \_ racines HKEY classes** \\  \\ *ApplicationName.exe* sous-clé.</span><span class="sxs-lookup"><span data-stu-id="763c7-226">Some examples of application registrations through the **HKEY\_CLASSES\_ROOT**\\**Applications**\\*ApplicationName.exe* subkey are as follows.</span></span> <span data-ttu-id="763c7-227">Toutes les valeurs d’entrée de Registre sont de type de Registre **\_ SZ** , à l’exception de **DefaultIcon** , qui est de type reg de type **\_ \_ SZ** .</span><span class="sxs-lookup"><span data-stu-id="763c7-227">All registry entry values are of **REG\_SZ** type, with the exception of **DefaultIcon** which is of **REG\_EXPAND\_SZ** type.</span></span>

```
HKEY_CLASSES_ROOT
   Applications
      wordpad.exe
         FriendlyAppName = @%SystemRoot%\System32\shell32.dll,-22069
```

```
HKEY_CLASSES_ROOT
   Applications
      wmplayer.exe
         SupportedTypes
            .3gp2
```

```
HKEY_CLASSES_ROOT
   Applications
      wmplayer.exe
         DefaultIcon
            (Default) = %SystemRoot%\system32\wmploc.dll,-730
```

```
HKEY_CLASSES_ROOT
   Applications
      WScript.exe
         NoOpenWith
```

```
HKEY_CLASSES_ROOT
   Applications
      photoviewer.dll
         shell
            open
               DropTarget
                  Clsid = {FFE2A43C-56B9-4bf5-9A79-CC6D4285608A}
```

```
HKEY_CLASSES_ROOT
   Applications
      mspaint.exe
         SupportedTypes
            .bmp
            .dib
            .rle
            .jpg
            .jpeg
            .jpe
            .jfif
            .gif
            .emf
            .wmf
            .tif
            .tiff
            .png
            .ico
```

## <a name="registering-verbs-and-other-file-association-information"></a><span data-ttu-id="763c7-228">Inscription de verbes et d’autres informations d’association de fichiers</span><span class="sxs-lookup"><span data-stu-id="763c7-228">Registering Verbs and Other File Association Information</span></span>

<span data-ttu-id="763c7-229">Les sous-clés inscrites sous les SystemFileAssociations **\_ \_ racines de la classe HKEY** \\  permettent à l’interpréteur de commandes de définir le comportement par défaut des attributs pour les types de fichiers et d’activer les associations de fichiers partagés.</span><span class="sxs-lookup"><span data-stu-id="763c7-229">Subkeys registered under **HKEY\_CLASSES\_ROOT**\\**SystemFileAssociations** enable the Shell to define the default behavior of attributes for file types and enable shared file associations.</span></span> <span data-ttu-id="763c7-230">Lorsque les utilisateurs modifient l’application par défaut pour un type de fichier, le ProgID de la nouvelle application par défaut a la priorité dans la fourniture de verbes et d’autres informations d’association.</span><span class="sxs-lookup"><span data-stu-id="763c7-230">When users change the default application for a file type, the ProgID of the new default application has priority in providing verbs and other association information.</span></span> <span data-ttu-id="763c7-231">Cette priorité est due à la première entrée dans le tableau d’association.</span><span class="sxs-lookup"><span data-stu-id="763c7-231">This priority is due to it being the first entry in the association array.</span></span> <span data-ttu-id="763c7-232">Si le programme par défaut est modifié, les informations sous le ProgID précédent ne sont plus disponibles.</span><span class="sxs-lookup"><span data-stu-id="763c7-232">If the default program is changed, the information under the previous ProgID is no longer available.</span></span>

<span data-ttu-id="763c7-233">Pour traiter de manière proactive avec les conséquences d’une modification apportée aux programmes par défaut, vous pouvez utiliser les **\_ classes HKEY \_ root** \\ **SystemFileAssociations** pour enregistrer les verbes et d’autres informations d’association.</span><span class="sxs-lookup"><span data-stu-id="763c7-233">To deal proactively with the consequences of a change to default programs, you can use **HKEY\_CLASSES\_ROOT**\\**SystemFileAssociations** to register verbs and other association information.</span></span> <span data-ttu-id="763c7-234">En raison de leur emplacement après le ProgID dans le tableau d’association, ces inscriptions ont une priorité plus faible.</span><span class="sxs-lookup"><span data-stu-id="763c7-234">Due to their location after the ProgID in the association array, these registrations are lower priority.</span></span> <span data-ttu-id="763c7-235">Ces SystemFileAssociationsregistrations sont stables même lorsque les utilisateurs modifient les programmes par défaut et fournissent un emplacement pour enregistrer les verbes secondaires qui seront toujours disponibles pour un type de fichier particulier.</span><span class="sxs-lookup"><span data-stu-id="763c7-235">These SystemFileAssociationsregistrations are stable even when users change the default programs, and provide a location to register secondary verbs that will always be available for a particular file type.</span></span> <span data-ttu-id="763c7-236">Pour obtenir un exemple de Registre, consultez [inscription d’un type perçu](#registering-a-perceived-type) plus loin dans cette rubrique.</span><span class="sxs-lookup"><span data-stu-id="763c7-236">For a registry example, see [Registering a Perceived Type](#registering-a-perceived-type) later in this topic.</span></span>

<span data-ttu-id="763c7-237">L’exemple de Registre suivant montre ce qui se produit lorsque l’utilisateur exécute l’élément **programmes par défaut** dans le panneau de configuration pour modifier la valeur par défaut pour les fichiers. mp3 en App2ProgID.</span><span class="sxs-lookup"><span data-stu-id="763c7-237">The following registry example shows what happens when the user runs the **Default Programs** item in Control Panel to change the default for .mp3 files to App2ProgID.</span></span> <span data-ttu-id="763c7-238">Après avoir modifié la valeur par défaut, Verb1 n’est plus disponible et Verb2 devient la valeur par défaut.</span><span class="sxs-lookup"><span data-stu-id="763c7-238">After changing the default, Verb1 is no longer available, and Verb2 becomes the default.</span></span>

```
HKEY_CLASSES_ROOT
   .mp3
      (Default) = App1ProgID
```

```
HKEY_CLASSES_ROOT
   App1ProgID
      shell
         Verb1
```

```
HKEY_CLASSES_ROOT
   App2ProgID
      shell
         Verb2
```

## <a name="registering-a-perceived-type"></a><span data-ttu-id="763c7-239">Inscription d’un type perçu</span><span class="sxs-lookup"><span data-stu-id="763c7-239">Registering a Perceived Type</span></span>

<span data-ttu-id="763c7-240">Les valeurs de Registre pour les types perçus sont définies en tant que sous-clés de la sous-clé de Registre **HKEY \_ classes \_ racine** \\ **SystemFileAssociations** .</span><span class="sxs-lookup"><span data-stu-id="763c7-240">Registry values for perceived types are defined as subkeys of the **HKEY\_CLASSES\_ROOT**\\**SystemFileAssociations** registry subkey.</span></span> <span data-ttu-id="763c7-241">Par exemple, le **texte** du type perçu est inscrit comme suit :</span><span class="sxs-lookup"><span data-stu-id="763c7-241">For example, the perceived type **text** is registered as follows:</span></span>

```
HKEY_CLASSES_ROOT
   SystemFileAssociations
      text
         shell
            edit
               command
                  (Default) = "%SystemRoot%\system32\NOTEPAD.EXE" "%1"
            open
               command
                  (Default) = "%SystemRoot%\system32\NOTEPAD.EXE" "%1"
```

<span data-ttu-id="763c7-242">Le type perçu d’un type de fichier est indiqué par l’inclusion d’une valeur PerceivedType dans la sous-clé du type de fichier.</span><span class="sxs-lookup"><span data-stu-id="763c7-242">A file type's perceived type is indicated by including a PerceivedType value in the file type's subkey.</span></span> <span data-ttu-id="763c7-243">La valeur PerceivedType est définie sur le nom du type perçu inscrit sous la sous-clé de Registre **\_ \_ racine** SystemFileAssociations de la classe HKEY \\  , comme indiqué dans l’exemple précédent du Registre.</span><span class="sxs-lookup"><span data-stu-id="763c7-243">The PerceivedType value is set to the name of the perceived type registered under **HKEY\_CLASSES\_ROOT**\\**SystemFileAssociations** registry subkey, as shown in the previous registry example.</span></span> <span data-ttu-id="763c7-244">Pour déclarer des fichiers. cpp comme étant du type « text », par exemple, ajoutez l’entrée de Registre suivante :</span><span class="sxs-lookup"><span data-stu-id="763c7-244">To declare .cpp files as being of perceived type "text", for example, add the following registry entry:</span></span>

```
HKEY_CLASSES_ROOT
   .cpp
      PerceivedType = text
```

## <a name="related-topics"></a><span data-ttu-id="763c7-245">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="763c7-245">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="763c7-246">Types de fichiers</span><span class="sxs-lookup"><span data-stu-id="763c7-246">File Types</span></span>](fa-file-types.md)
</dt> <dt>

[<span data-ttu-id="763c7-247">Fonctionnement des associations de fichiers</span><span class="sxs-lookup"><span data-stu-id="763c7-247">How File Associations Work</span></span>](fa-how-work.md)
</dt> <dt>

[<span data-ttu-id="763c7-248">Affichage du contenu par type de fichier ou par type</span><span class="sxs-lookup"><span data-stu-id="763c7-248">Content View By File Type or Kind</span></span>](prophand-content-view.md)
</dt> <dt>

[<span data-ttu-id="763c7-249">Vérificateur de type de fichier</span><span class="sxs-lookup"><span data-stu-id="763c7-249">File Type Verifier</span></span>](file-type-verifier.md)
</dt> <dt>

[<span data-ttu-id="763c7-250">Gestionnaires de types de fichiers</span><span class="sxs-lookup"><span data-stu-id="763c7-250">File Type Handlers</span></span>](fa-file-extensions.md)
</dt> <dt>

[<span data-ttu-id="763c7-251">Identificateurs programmatiques</span><span class="sxs-lookup"><span data-stu-id="763c7-251">Programmatic Identifiers</span></span>](fa-progids.md)
</dt> <dt>

[<span data-ttu-id="763c7-252">Types perçus</span><span class="sxs-lookup"><span data-stu-id="763c7-252">Perceived Types</span></span>](fa-perceivedtypes.md)
</dt> <dt>

[<span data-ttu-id="763c7-253">Tableaux d’association</span><span class="sxs-lookup"><span data-stu-id="763c7-253">Association Arrays</span></span>](fa-associationarray.md)
</dt> </dl>

