---
title: Outil de création de package de l’application (MakeAppx.exe)
description: App Packager (MakeAppx.exe) crée un package d’application à partir de fichiers sur le disque ou extrait les fichiers d’un package d’application sur le disque.
ms.assetid: 9B7BF420-8E19-4BFD-B378-D09E61F68A39
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 41595550f3bee7b1149959886ed649e9212224b2
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/17/2020
ms.locfileid: "104101468"
---
# <a name="app-packager-makeappxexe"></a><span data-ttu-id="1afa5-103">Outil de création de package de l’application (MakeAppx.exe)</span><span class="sxs-lookup"><span data-stu-id="1afa5-103">App packager (MakeAppx.exe)</span></span>

> [!Note]  
> <span data-ttu-id="1afa5-104">Pour obtenir des conseils sur l’utilisation de cet outil sur UWP, consultez [créer un package d’application avec l’outil MakeAppx.exe](/windows/msix/package/create-app-package-with-makeappx-tool).</span><span class="sxs-lookup"><span data-stu-id="1afa5-104">For UWP guidance on using this tool, see [Create an app package with the MakeAppx.exe tool](/windows/msix/package/create-app-package-with-makeappx-tool).</span></span>

 

<span data-ttu-id="1afa5-105">App Packager (MakeAppx.exe) crée un package d’application à partir de fichiers sur le disque ou extrait les fichiers d’un package d’application sur le disque.</span><span class="sxs-lookup"><span data-stu-id="1afa5-105">App packager (MakeAppx.exe) creates an app package from files on disk or extracts the files from an app package to disk.</span></span> <span data-ttu-id="1afa5-106">À partir de Windows 8.1, app Packager crée également un lot de packages d’application à partir de packages d’application sur le disque ou extrait les packages d’application d’un bundle de packages d’application sur le disque.</span><span class="sxs-lookup"><span data-stu-id="1afa5-106">Starting with Windows 8.1, App packager also creates an app package bundle from app packages on disk or extracts the app packages from an app package bundle to disk.</span></span> <span data-ttu-id="1afa5-107">Il est inclus dans Microsoft Visual Studio et le kit de développement logiciel (SDK) Windows pour Windows 8 ou le kit de développement logiciel (SDK) Windows pour Windows 8.1.</span><span class="sxs-lookup"><span data-stu-id="1afa5-107">It is included in Microsoft Visual Studio and the Windows Software Development Kit (SDK) for Windows 8 or Windows Software Development Kit (SDK) for Windows 8.1.</span></span> <span data-ttu-id="1afa5-108">Visitez [téléchargements pour les développeurs]( https://msdn.microsoft.com/windows/apps/br229516.aspx) pour les obtenir.</span><span class="sxs-lookup"><span data-stu-id="1afa5-108">Visit [Downloads for developers]( https://msdn.microsoft.com/windows/apps/br229516.aspx) to get them.</span></span>

<span data-ttu-id="1afa5-109">L’outil MakeAppx.exe se trouve généralement à ces emplacements :</span><span class="sxs-lookup"><span data-stu-id="1afa5-109">The MakeAppx.exe tool is typically found at these locations:</span></span>

-   <span data-ttu-id="1afa5-110">Sur x86 : C : \\ Program Files (x86) \\ windows kits \\ 8,0 \\ bin \\ x86 \\makeappx.exe ou C : \\ program files (x86) \\ Windows kits \\ 8,1 \\ bin \\ x86 \\makeappx.exe</span><span class="sxs-lookup"><span data-stu-id="1afa5-110">On x86: C:\\Program Files (x86)\\Windows Kits\\8.0\\bin\\x86\\makeappx.exe or C:\\Program Files (x86)\\Windows Kits\\8.1\\bin\\x86\\makeappx.exe</span></span>
-   <span data-ttu-id="1afa5-111">Sur x64 dans deux emplacements :</span><span class="sxs-lookup"><span data-stu-id="1afa5-111">On x64 in two locations:</span></span>
    -   <span data-ttu-id="1afa5-112">C : \\ Program Files (x86) \\ windows kits \\ 8,0 \\ bin \\ x86 \\makeappx.exe ou C : \\ program files (x86) \\ Windows kits \\ 8,1 \\ bin \\ x86 \\makeappx.exe</span><span class="sxs-lookup"><span data-stu-id="1afa5-112">C:\\Program Files (x86)\\Windows Kits\\8.0\\bin\\x86\\makeappx.exe or C:\\Program Files (x86)\\Windows Kits\\8.1\\bin\\x86\\makeappx.exe</span></span>
    -   <span data-ttu-id="1afa5-113">C : \\ Program Files (x86) \\ windows kits \\ 8,0 \\ bin \\ x64 \\makeappx.exe ou C : \\ program files (x86) \\ Windows kits \\ 8,1 \\ bin \\ x64 \\makeappx.exe</span><span class="sxs-lookup"><span data-stu-id="1afa5-113">C:\\Program Files (x86)\\Windows Kits\\8.0\\bin\\x64\\makeappx.exe or C:\\Program Files (x86)\\Windows Kits\\8.1\\bin\\x64\\makeappx.exe</span></span>

<span data-ttu-id="1afa5-114">Il n’existe aucune version ARM de l’outil.</span><span class="sxs-lookup"><span data-stu-id="1afa5-114">There is no ARM version of the tool.</span></span>

-   [<span data-ttu-id="1afa5-115">Pour créer un package à l’aide d’une structure de répertoires</span><span class="sxs-lookup"><span data-stu-id="1afa5-115">To create a package using a directory structure</span></span>](#to-create-a-package-using-a-directory-structure)
-   [<span data-ttu-id="1afa5-116">Pour créer un package à l’aide d’un fichier de mappage</span><span class="sxs-lookup"><span data-stu-id="1afa5-116">To create a package using a mapping file</span></span>](#to-create-a-package-using-a-mapping-file)
-   [<span data-ttu-id="1afa5-117">Pour signer le package à l’aide de SignTool</span><span class="sxs-lookup"><span data-stu-id="1afa5-117">To sign the package using SignTool</span></span>](#to-sign-the-package-using-signtool)
-   [<span data-ttu-id="1afa5-118">Pour extraire des fichiers d’un package</span><span class="sxs-lookup"><span data-stu-id="1afa5-118">To extract files from a package</span></span>](#to-extract-files-from-a-package)
-   [<span data-ttu-id="1afa5-119">Pour créer un regroupement de packages à l’aide d’une structure de répertoires</span><span class="sxs-lookup"><span data-stu-id="1afa5-119">To create a package bundle using a directory structure</span></span>](#to-create-a-package-bundle-using-a-directory-structure)
-   [<span data-ttu-id="1afa5-120">Pour créer un lot de packages à l’aide d’un fichier de mappage</span><span class="sxs-lookup"><span data-stu-id="1afa5-120">To create a package bundle using a mapping file</span></span>](#to-create-a-package-bundle-using-a-mapping-file)
-   [<span data-ttu-id="1afa5-121">Pour extraire des packages d’un bundle</span><span class="sxs-lookup"><span data-stu-id="1afa5-121">To extract packages from a bundle</span></span>](#to-extract-packages-from-a-bundle)
-   [<span data-ttu-id="1afa5-122">Pour chiffrer un package à l’aide d’un fichier de clé</span><span class="sxs-lookup"><span data-stu-id="1afa5-122">To encrypt a package with a key file</span></span>](#to-encrypt-a-package-with-a-key-file)
-   [<span data-ttu-id="1afa5-123">Pour chiffrer un package à l’aide d’une clé de test globale</span><span class="sxs-lookup"><span data-stu-id="1afa5-123">To encrypt a package with a global test key</span></span>](#to-encrypt-a-package-with-a-global-test-key)
-   [<span data-ttu-id="1afa5-124">Pour déchiffrer un package à l’aide d’un fichier de clé</span><span class="sxs-lookup"><span data-stu-id="1afa5-124">To decrypt a package with a key file</span></span>](#to-decrypt-a-package-with-a-key-file)
-   [<span data-ttu-id="1afa5-125">Pour déchiffrer un package avec une clé de test globale</span><span class="sxs-lookup"><span data-stu-id="1afa5-125">To decrypt a package with a global test key</span></span>](#to-decrypt-a-package-with-a-global-test-key)
-   [<span data-ttu-id="1afa5-126">Utilisation</span><span class="sxs-lookup"><span data-stu-id="1afa5-126">Usage</span></span>](#usage)

## <a name="using-app-packager"></a><span data-ttu-id="1afa5-127">Utilisation d’App packager</span><span class="sxs-lookup"><span data-stu-id="1afa5-127">Using App packager</span></span>

> [!Note]  
> <span data-ttu-id="1afa5-128">Les chemins d’accès relatifs sont pris en charge dans l’ensemble de l’outil.</span><span class="sxs-lookup"><span data-stu-id="1afa5-128">Relative paths are supported throughout the tool.</span></span>

 

### <a name="to-create-a-package-using-a-directory-structure"></a><span data-ttu-id="1afa5-129">Pour créer un package à l’aide d’une structure de répertoires</span><span class="sxs-lookup"><span data-stu-id="1afa5-129">To create a package using a directory structure</span></span>

<span data-ttu-id="1afa5-130">Placez le AppxManifest.xml à la racine d’un répertoire contenant tous les fichiers de charge utile pour votre application.</span><span class="sxs-lookup"><span data-stu-id="1afa5-130">Place the AppxManifest.xml in the root of a directory containing all of the payload files for your app.</span></span> <span data-ttu-id="1afa5-131">Une structure de répertoires identique est créée pour le package d’application et est disponible lorsque le package est extrait au moment du déploiement.</span><span class="sxs-lookup"><span data-stu-id="1afa5-131">An identical directory structure is created for the app package, and will be available when the package is extracted at deployment time.</span></span>

1.  <span data-ttu-id="1afa5-132">Placez tous les fichiers dans une structure de répertoire unique, en créant des sous-répertoires selon vos besoins.</span><span class="sxs-lookup"><span data-stu-id="1afa5-132">Place all files in a single directory structure, creating subdirectories as desired.</span></span>

2.  <span data-ttu-id="1afa5-133">Créez un manifeste de package valide, AppxManifest.xml, et placez-le dans le répertoire racine.</span><span class="sxs-lookup"><span data-stu-id="1afa5-133">Create a valid package manifest, AppxManifest.xml, and place it in the root directory.</span></span>

3.  <span data-ttu-id="1afa5-134">Exécutez cette commande :</span><span class="sxs-lookup"><span data-stu-id="1afa5-134">Run this command:</span></span>

    <span data-ttu-id="1afa5-135">**MakeAppx Pack/d** *entrée \_ DirectoryPath* **/p** _filePath_**. AppX**</span><span class="sxs-lookup"><span data-stu-id="1afa5-135">**MakeAppx pack /d** *input\_directorypath* **/p** _filepath_**.appx**</span></span>

### <a name="to-create-a-package-using-a-mapping-file"></a><span data-ttu-id="1afa5-136">Pour créer un package à l’aide d’un fichier de mappage</span><span class="sxs-lookup"><span data-stu-id="1afa5-136">To create a package using a mapping file</span></span>

1.  <span data-ttu-id="1afa5-137">Créez un manifeste de package valide, AppxManifest.xml.</span><span class="sxs-lookup"><span data-stu-id="1afa5-137">Create a valid package manifest, AppxManifest.xml.</span></span>

2.  <span data-ttu-id="1afa5-138">Créez un fichier de mappage.</span><span class="sxs-lookup"><span data-stu-id="1afa5-138">Create a mapping file.</span></span> <span data-ttu-id="1afa5-139">La première ligne contient les **\[ fichiers \]** de chaîne et les lignes qui suivent spécifient les chemins source (disque) et de destination (package) dans les chaînes entre guillemets.</span><span class="sxs-lookup"><span data-stu-id="1afa5-139">The first line contains the string **\[Files\]**, and the lines that follow specify the source (disk) and destination (package) paths in quoted strings.</span></span>

    ``` syntax
    [Files]
    "C:\MyApp\StartPage.htm"     "default.html"
    "C:\MyApp\readme.txt"        "doc\readme.txt"
    "\\MyServer\path\icon.png"   "icon.png"
    "MyCustomManifest.xml"       "AppxManifest.xml"
    ```

3.  <span data-ttu-id="1afa5-140">Exécutez cette commande :</span><span class="sxs-lookup"><span data-stu-id="1afa5-140">Run this command:</span></span>

    <span data-ttu-id="1afa5-141">**MakeAppx Pack/f** *mappage de \_ filePath* **/p** _filePath_**. AppX**</span><span class="sxs-lookup"><span data-stu-id="1afa5-141">**MakeAppx pack /f** *mapping\_filepath* **/p** _filepath_**.appx**</span></span>

### <a name="to-sign-the-package-using-signtool"></a><span data-ttu-id="1afa5-142">Pour signer le package à l’aide de SignTool</span><span class="sxs-lookup"><span data-stu-id="1afa5-142">To sign the package using SignTool</span></span>

1.  <span data-ttu-id="1afa5-143">Créez le certificat.</span><span class="sxs-lookup"><span data-stu-id="1afa5-143">Create the certificate.</span></span> <span data-ttu-id="1afa5-144">Le serveur de publication figurant dans le manifeste doit correspondre aux informations d’objet du serveur de publication du certificat de signature.</span><span class="sxs-lookup"><span data-stu-id="1afa5-144">The publisher listed in the manifest must match the publisher subject information of the signing certificate.</span></span> <span data-ttu-id="1afa5-145">Pour plus d’informations sur la création d’un certificat de signature, consultez [comment créer un certificat de signature de package d’application](how-to-create-a-package-signing-certificate.md).</span><span class="sxs-lookup"><span data-stu-id="1afa5-145">For more info about creating a signing certificate, see [How to create an app package signing certificate](how-to-create-a-package-signing-certificate.md).</span></span>

2.  <span data-ttu-id="1afa5-146">Exécutez SignTool.exe pour signer le package :</span><span class="sxs-lookup"><span data-stu-id="1afa5-146">Run SignTool.exe to sign the package:</span></span>

    <span data-ttu-id="1afa5-147">Le **signe SignTool/a/v/FD** *HashAlgorithm* **/f** *nomfichiercertificat* _filePath_**. AppX**</span><span class="sxs-lookup"><span data-stu-id="1afa5-147">**SignTool sign /a /v /fd** *hashAlgorithm* **/f** *certFileName* _filepath_**.appx**</span></span>

    <span data-ttu-id="1afa5-148">*HashAlgorithm* doit correspondre à l’algorithme de hachage utilisé pour créer le blockmap lorsque l’application a été empaquetée.</span><span class="sxs-lookup"><span data-stu-id="1afa5-148">The *hashAlgorithm* must match the hash algorithm used to create the blockmap when the app was packaged.</span></span> <span data-ttu-id="1afa5-149">Avec l’utilitaire de Packaging MakeAppx, l’algorithme de hachage du blockmap de l’AppX par défaut est **SHA256**.</span><span class="sxs-lookup"><span data-stu-id="1afa5-149">With the MakeAppx packaging utility, the default Appx blockmap hash algorithm is **SHA256**.</span></span> <span data-ttu-id="1afa5-150">Exécutez SignTool.exe en spécifiant **SHA256** comme algorithme de résumé de fichier (/FD) :</span><span class="sxs-lookup"><span data-stu-id="1afa5-150">Run SignTool.exe specifying **SHA256** as the file digest (/fd) algorithm:</span></span>

    <span data-ttu-id="1afa5-151">Le **signe SignTool/a/v/FD SHA256/F** *nomfichiercertificat* _filePath_**. AppX**</span><span class="sxs-lookup"><span data-stu-id="1afa5-151">**SignTool sign /a /v /fd SHA256 /f** *certFileName* _filepath_**.appx**</span></span>

    <span data-ttu-id="1afa5-152">Pour plus d’informations sur la façon de signer des packages, consultez [Comment signer un package d’application à l’aide de SignTool](how-to-sign-a-package-using-signtool.md).</span><span class="sxs-lookup"><span data-stu-id="1afa5-152">For more info about how to sign packages, see [How to sign an app package using SignTool](how-to-sign-a-package-using-signtool.md).</span></span>

### <a name="to-extract-files-from-a-package"></a><span data-ttu-id="1afa5-153">Pour extraire des fichiers d’un package</span><span class="sxs-lookup"><span data-stu-id="1afa5-153">To extract files from a package</span></span>

1.  <span data-ttu-id="1afa5-154">Exécutez cette commande :</span><span class="sxs-lookup"><span data-stu-id="1afa5-154">Run this command:</span></span>

    <span data-ttu-id="1afa5-155">**MakeAppx décompresser** le _fichier_/p **. AppX/d** *\_ Répertoire de sortie*</span><span class="sxs-lookup"><span data-stu-id="1afa5-155">**MakeAppx unpack /p** _file_**.appx /d** *output\_directory*</span></span>

2.  <span data-ttu-id="1afa5-156">Le package décompressé a la même structure que le package installé.</span><span class="sxs-lookup"><span data-stu-id="1afa5-156">The unpacked package has the same structure as the installed package.</span></span>

### <a name="to-create-a-package-bundle-using-a-directory-structure"></a><span data-ttu-id="1afa5-157">Pour créer un regroupement de packages à l’aide d’une structure de répertoires</span><span class="sxs-lookup"><span data-stu-id="1afa5-157">To create a package bundle using a directory structure</span></span>

<span data-ttu-id="1afa5-158">Nous utilisons la commande **Bundle** pour créer un bundle d’applications à l’adresse</span><span class="sxs-lookup"><span data-stu-id="1afa5-158">We use the **bundle** command to create an app bundle at</span></span> <output bundle name> <span data-ttu-id="1afa5-159">en ajoutant tous les packages de <content directory> (y compris les sous-dossiers).</span><span class="sxs-lookup"><span data-stu-id="1afa5-159">by adding all packages from <content directory> (including subfolders).</span></span> <span data-ttu-id="1afa5-160">Si <content directory> contient un manifeste de Bundle, AppxBundleManifest.xml, il est ignoré.</span><span class="sxs-lookup"><span data-stu-id="1afa5-160">If <content directory> contains a bundle manifest, AppxBundleManifest.xml, it is ignored.</span></span>

1.  <span data-ttu-id="1afa5-161">Placez tous les packages dans une structure de répertoire unique, en créant des sous-répertoires comme vous le souhaitez.</span><span class="sxs-lookup"><span data-stu-id="1afa5-161">Place all packages in a single directory structure, creating subdirectories as desired.</span></span>

2.  <span data-ttu-id="1afa5-162">Exécutez cette commande :</span><span class="sxs-lookup"><span data-stu-id="1afa5-162">Run this command:</span></span>

    <span data-ttu-id="1afa5-163">**Bundle MakeAppx/d** *entrée \_ DirectoryPath* **/p** _filePath_**. appxbundle**</span><span class="sxs-lookup"><span data-stu-id="1afa5-163">**MakeAppx bundle /d** *input\_directorypath* **/p** _filepath_**.appxbundle**</span></span>

### <a name="to-create-a-package-bundle-using-a-mapping-file"></a><span data-ttu-id="1afa5-164">Pour créer un lot de packages à l’aide d’un fichier de mappage</span><span class="sxs-lookup"><span data-stu-id="1afa5-164">To create a package bundle using a mapping file</span></span>

<span data-ttu-id="1afa5-165">Nous utilisons la commande **Bundle** pour créer un bundle d’applications à l’adresse</span><span class="sxs-lookup"><span data-stu-id="1afa5-165">We use the **bundle** command to create an app bundle at</span></span> <output bundle name> <span data-ttu-id="1afa5-166">en ajoutant tous les packages à partir d’une liste de packages dans <mapping file> .</span><span class="sxs-lookup"><span data-stu-id="1afa5-166">by adding all packages from a list of packages within <mapping file>.</span></span> <span data-ttu-id="1afa5-167">Si <mapping file> contient un manifeste de Bundle, AppxBundleManifest.xml, il est ignoré.</span><span class="sxs-lookup"><span data-stu-id="1afa5-167">If <mapping file> contains a bundle manifest, AppxBundleManifest.xml, it is ignored.</span></span>

1.  <span data-ttu-id="1afa5-168">Créez un <mapping file>.</span><span class="sxs-lookup"><span data-stu-id="1afa5-168">Create a <mapping file>.</span></span> <span data-ttu-id="1afa5-169">La première ligne contient les **\[ fichiers \]** de chaîne et les lignes qui suivent spécifient les packages à ajouter au bundle.</span><span class="sxs-lookup"><span data-stu-id="1afa5-169">The first line contains the string **\[Files\]**, and the lines that follow specify the packages to add to the bundle.</span></span> <span data-ttu-id="1afa5-170">Chaque package est décrit par une paire de chemins d’accès entre guillemets, séparés par des espaces ou des tabulations.</span><span class="sxs-lookup"><span data-stu-id="1afa5-170">Each package is described by a pair of paths in quotation marks, separated by spaces or tabs.</span></span> <span data-ttu-id="1afa5-171">La paire de chemins représente la source (sur disque) et la destination du package (dans le cas d’une offre groupée).</span><span class="sxs-lookup"><span data-stu-id="1afa5-171">The pair of paths represents the package's source (on disk) and destination (in bundle).</span></span> <span data-ttu-id="1afa5-172">Tous les noms de package de destination doivent avoir l’extension. Appx.</span><span class="sxs-lookup"><span data-stu-id="1afa5-172">All destination package names must have the .appx extension.</span></span>

    ``` syntax
        [Files]
        "C:\MyApp\MyApp_x86.appx"                 "MyApp_x86.appx"
        "C:\Program Files (x86)\ResPack.appx"    "resources\resPack.appx"
        "\\MyServer\path\ResPack.appx"           "Respack.appx"
        "my app files\respack.appx"              "my app files\respack.appx"
    ```

2.  <span data-ttu-id="1afa5-173">Exécutez cette commande :</span><span class="sxs-lookup"><span data-stu-id="1afa5-173">Run this command:</span></span>

    <span data-ttu-id="1afa5-174">**Package MakeAppx/f** *mappage de \_ filePath* **/p** _filePath_**. appxbundle**</span><span class="sxs-lookup"><span data-stu-id="1afa5-174">**MakeAppx bundle /f** *mapping\_filepath* **/p** _filepath_**.appxbundle**</span></span>

### <a name="to-extract-packages-from-a-bundle"></a><span data-ttu-id="1afa5-175">Pour extraire des packages d’un bundle</span><span class="sxs-lookup"><span data-stu-id="1afa5-175">To extract packages from a bundle</span></span>

1.  <span data-ttu-id="1afa5-176">Exécutez cette commande :</span><span class="sxs-lookup"><span data-stu-id="1afa5-176">Run this command:</span></span>

    <span data-ttu-id="1afa5-177">**MakeAppx désassocier/p** _\_ nom de l’offre groupée_**. appxbundle/d** *\_ Répertoire de sortie*</span><span class="sxs-lookup"><span data-stu-id="1afa5-177">**MakeAppx unbundle /p** _bundle\_name_**.appxbundle /d** *output\_directory*</span></span>

2.  <span data-ttu-id="1afa5-178">L’offre groupée décompressée a la même structure que l’offre groupée de packages installée.</span><span class="sxs-lookup"><span data-stu-id="1afa5-178">The unpacked bundle has the same structure as the installed package bundle.</span></span>

### <a name="to-encrypt-a-package-with-a-key-file"></a><span data-ttu-id="1afa5-179">Pour chiffrer un package à l’aide d’un fichier de clé</span><span class="sxs-lookup"><span data-stu-id="1afa5-179">To encrypt a package with a key file</span></span>

1.  <span data-ttu-id="1afa5-180">Créez un fichier de clé.</span><span class="sxs-lookup"><span data-stu-id="1afa5-180">Create a key file.</span></span> <span data-ttu-id="1afa5-181">Les fichiers de clés doivent commencer par une ligne contenant la chaîne « \[ Keys \] » suivie de lignes décrivant les clés avec lesquelles chiffrer le package.</span><span class="sxs-lookup"><span data-stu-id="1afa5-181">Key files must begin with a line containing the string "\[Keys\]" followed by lines describing the keys to encrypt the package with.</span></span> <span data-ttu-id="1afa5-182">Chaque clé est décrite par une paire de chaînes entre guillemets, en les séparant par des espaces ou des tabulations.</span><span class="sxs-lookup"><span data-stu-id="1afa5-182">Each key is described by a pair of strings in quotation marks, separated by spaces or tabs.</span></span> <span data-ttu-id="1afa5-183">La première chaîne représente l’ID de clé et la deuxième chaîne représente la clé de chiffrement au format hexadécimal.</span><span class="sxs-lookup"><span data-stu-id="1afa5-183">The first string represents the key ID and the second string represents the encryption key in hexadecimal form.</span></span>

    ``` syntax
        [Keys]
        "0"                 "1AC4CDCFF1924D2885A0607269787BA6BF09B7FFEBF74ED4B9D86E423CF9186B"
    ```

2.  <span data-ttu-id="1afa5-184">Exécutez cette commande :</span><span class="sxs-lookup"><span data-stu-id="1afa5-184">Run this command:</span></span>

    <span data-ttu-id="1afa5-185">**MakeAppx.exe chiffrer/p** _\_ nom du package_**. AppX/EP** _\_ \_ nom du package chiffré_**. eappx/KF** _keyfile \_ Name_**. txt**</span><span class="sxs-lookup"><span data-stu-id="1afa5-185">**MakeAppx.exe encrypt /p** _package\_name_**.appx /ep** _encrypted\_package\_name_**.eappx /kf** _keyfile\_name_**.txt**</span></span>

3.  <span data-ttu-id="1afa5-186">Le package d’entrée sera chiffré dans le package chiffré spécifié à l’aide du fichier de clé fourni.</span><span class="sxs-lookup"><span data-stu-id="1afa5-186">The input package will be encrypted into the specified encrypted package using the provided key file.</span></span>

### <a name="to-encrypt-a-package-with-a-global-test-key"></a><span data-ttu-id="1afa5-187">Pour chiffrer un package à l’aide d’une clé de test globale</span><span class="sxs-lookup"><span data-stu-id="1afa5-187">To encrypt a package with a global test key</span></span>

1.  <span data-ttu-id="1afa5-188">Exécutez cette commande :</span><span class="sxs-lookup"><span data-stu-id="1afa5-188">Run this command:</span></span>

    <span data-ttu-id="1afa5-189">**MakeAppx.exe chiffrer/p** _\_ nom du package_**. AppX/EP** _\_ \_ nom du package chiffré_**. eappx/kt**</span><span class="sxs-lookup"><span data-stu-id="1afa5-189">**MakeAppx.exe encrypt /p** _package\_name_**.appx /ep** _encrypted\_package\_name_**.eappx /kt**</span></span>

2.  <span data-ttu-id="1afa5-190">Le package d’entrée sera chiffré dans le package chiffré spécifié à l’aide de la clé de test globale.</span><span class="sxs-lookup"><span data-stu-id="1afa5-190">The input package will be encrypted into the specified encrypted package using the global test key.</span></span>

### <a name="to-decrypt-a-package-with-a-key-file"></a><span data-ttu-id="1afa5-191">Pour déchiffrer un package à l’aide d’un fichier de clé</span><span class="sxs-lookup"><span data-stu-id="1afa5-191">To decrypt a package with a key file</span></span>

1.  <span data-ttu-id="1afa5-192">Créez un fichier de clé.</span><span class="sxs-lookup"><span data-stu-id="1afa5-192">Create a key file.</span></span> <span data-ttu-id="1afa5-193">Les fichiers de clés doivent commencer par une ligne contenant la chaîne « \[ Keys \] » suivie de lignes décrivant les clés avec lesquelles chiffrer le package.</span><span class="sxs-lookup"><span data-stu-id="1afa5-193">Key files must begin with a line containing the string "\[Keys\]" followed by lines describing the keys to encrypt the package with.</span></span> <span data-ttu-id="1afa5-194">Chaque clé est décrite par une paire de chaînes entre guillemets, en les séparant par des espaces ou des tabulations.</span><span class="sxs-lookup"><span data-stu-id="1afa5-194">Each key is described by a pair of strings in quotation marks, separated by spaces or tabs.</span></span> <span data-ttu-id="1afa5-195">La première chaîne représente l’ID de clé de 32 octets encodé en base64, tandis que la deuxième chaîne représente la clé de chiffrement de 32 octets encodée en base64.</span><span class="sxs-lookup"><span data-stu-id="1afa5-195">The first string represents the base64 encoded 32-byte key ID and the second string represents the base64 encoded 32-byte encryption key.</span></span>

    ``` syntax
        [Keys]
        "OWVwSzliRGY1VWt1ODk4N1Q4R2Vqc04zMzIzNnlUREU="                 "MjNFTlFhZGRGZEY2YnVxMTBocjd6THdOdk9pZkpvelc="
    ```

2.  <span data-ttu-id="1afa5-196">Exécutez cette commande :</span><span class="sxs-lookup"><span data-stu-id="1afa5-196">Run this command:</span></span>

    <span data-ttu-id="1afa5-197">**MakeAppx.exe déchiffrer/p** _\_ nom du package_**. AppX/EP** _\_ \_ nom du package non chiffré_**. eappx/KF** _keyfile \_ Name_**. txt**</span><span class="sxs-lookup"><span data-stu-id="1afa5-197">**MakeAppx.exe decrypt /p** _package\_name_**.appx /ep** _unencrypted\_package\_name_**.eappx /kf** _keyfile\_name_**.txt**</span></span>

3.  <span data-ttu-id="1afa5-198">Le package d’entrée sera déchiffré dans le package non chiffré spécifié à l’aide du fichier de clé fourni.</span><span class="sxs-lookup"><span data-stu-id="1afa5-198">The input package will be decrypted into the specified unencrypted package using the provided key file.</span></span>

### <a name="to-decrypt-a-package-with-a-global-test-key"></a><span data-ttu-id="1afa5-199">Pour déchiffrer un package avec une clé de test globale</span><span class="sxs-lookup"><span data-stu-id="1afa5-199">To decrypt a package with a global test key</span></span>

1.  <span data-ttu-id="1afa5-200">Exécutez cette commande :</span><span class="sxs-lookup"><span data-stu-id="1afa5-200">Run this command:</span></span>

    <span data-ttu-id="1afa5-201">**MakeAppx.exe déchiffrer/p** _\_ nom du package_**. AppX/EP** _\_ \_ nom du package non chiffré_**. eappx/kt**</span><span class="sxs-lookup"><span data-stu-id="1afa5-201">**MakeAppx.exe decrypt /p** _package\_name_**.appx /ep** _unencrypted\_package\_name_**.eappx /kt**</span></span>

2.  <span data-ttu-id="1afa5-202">Le package d’entrée sera déchiffré dans le package non chiffré spécifié à l’aide de la clé de test globale.</span><span class="sxs-lookup"><span data-stu-id="1afa5-202">The input package will be decrypted into the specified unencrypted package using the global test key.</span></span>

## <a name="usage"></a><span data-ttu-id="1afa5-203">Utilisation</span><span class="sxs-lookup"><span data-stu-id="1afa5-203">Usage</span></span>

<span data-ttu-id="1afa5-204">L’argument de ligne de commande **/p** est toujours requis, avec **/d**, **/f** ou **/EP**.</span><span class="sxs-lookup"><span data-stu-id="1afa5-204">The command line argument **/p** is always required, with either **/d**, **/f**, or **/ep**.</span></span> <span data-ttu-id="1afa5-205">Notez que **/d**, **/f** et **/EP** s’excluent mutuellement.</span><span class="sxs-lookup"><span data-stu-id="1afa5-205">Note that **/d**, **/f**, and **/ep** are mutually exclusive.</span></span>

<span data-ttu-id="1afa5-206">**\[ Options \] du Pack MakeAppx** **/p** *\<output package name\>* \**/d\*\*\*\<content directory\>*</span><span class="sxs-lookup"><span data-stu-id="1afa5-206">**MakeAppx pack \[options\]** **/p** *\<output package name\>* **/d** *\<content directory\>*</span></span>

<span data-ttu-id="1afa5-207">**\[ Options \] du Pack MakeAppx** **/p** *\<output package name\>* \**/f\*\*\*\<mapping file\>*</span><span class="sxs-lookup"><span data-stu-id="1afa5-207">**MakeAppx pack \[options\]** **/p** *\<output package name\>* **/f** *\<mapping file\>*</span></span>

<span data-ttu-id="1afa5-208">**\[ Options \] de décompression MakeAppx** **/p** *\<input package name\>* \**/d\*\*\*\<output directory\>*</span><span class="sxs-lookup"><span data-stu-id="1afa5-208">**MakeAppx unpack \[options\]** **/p** *\<input package name\>* **/d** *\<output directory\>*</span></span>

<span data-ttu-id="1afa5-209">**\[ Options \] du bundle MakeAppx** **/p** *\<output bundle name\>* \**/d\*\*\*\<content directory\>*</span><span class="sxs-lookup"><span data-stu-id="1afa5-209">**MakeAppx bundle \[options\]** **/p** *\<output bundle name\>* **/d** *\<content directory\>*</span></span>

<span data-ttu-id="1afa5-210">**\[ Options \] du bundle MakeAppx** **/p** *\<output bundle name\>* \**/f\*\*\*\<mapping file\>*</span><span class="sxs-lookup"><span data-stu-id="1afa5-210">**MakeAppx bundle \[options\]** **/p** *\<output bundle name\>* **/f** *\<mapping file\>*</span></span>

<span data-ttu-id="1afa5-211">**MakeAppx dégrouper les \[ options \]** **/p** *\<input bundle name\>* \**/d\*\*\*\<output directory\>*</span><span class="sxs-lookup"><span data-stu-id="1afa5-211">**MakeAppx unbundle \[options\]** **/p** *\<input bundle name\>* **/d** *\<output directory\>*</span></span>

<span data-ttu-id="1afa5-212">**\[ Options \] Encrypt MakeAppx** **/p** *\<input package name\>* \**/EP\*\*\*\<output package name\>*</span><span class="sxs-lookup"><span data-stu-id="1afa5-212">**MakeAppx encrypt \[options\]** **/p** *\<input package name\>* **/ep** *\<output package name\>*</span></span>

<span data-ttu-id="1afa5-213">**\[ Options \] de déchiffrement MakeAppx** **/p** *\<input package name\>* \**/EP\*\*\*\<output package name\>*</span><span class="sxs-lookup"><span data-stu-id="1afa5-213">**MakeAppx decrypt \[options\]** **/p** *\<input package name\>* **/ep** *\<output package name\>*</span></span>

## <a name="command-line-syntax"></a><span data-ttu-id="1afa5-214">Syntaxe de ligne de commande</span><span class="sxs-lookup"><span data-stu-id="1afa5-214">Command-line Syntax</span></span>

<span data-ttu-id="1afa5-215">Voici la syntaxe d’utilisation courante de la ligne de commande pour MakeAppx.</span><span class="sxs-lookup"><span data-stu-id="1afa5-215">Here is the command-line common usage syntax for MakeAppx.</span></span>

<span data-ttu-id="1afa5-216">**MakeAppx \[ Pack \| déballer \| \| dégrouper \| chiffrer/ \| déchiffrer \]** \[ **/h** **/KF** **/kt** **/l** **/o** **/non** **/NV** **/v** **/PFN** **/ ?**\]</span><span class="sxs-lookup"><span data-stu-id="1afa5-216">**MakeAppx \[pack\|unpack\|bundle\|unbundle\|encrypt\|decrypt\]** \[**/h** **/kf** **/kt** **/l** **/o** **/no** **/nv** **/v** **/pfn** **/?**\]</span></span>

<span data-ttu-id="1afa5-217">**MakeAppx** packs ou décompresse les fichiers dans un package, regroupe ou dissocie les packages dans un bundle, ou chiffre ou déchiffre le package d’application ou le bundle dans le répertoire d’entrée ou le fichier de mappage spécifié.</span><span class="sxs-lookup"><span data-stu-id="1afa5-217">**MakeAppx** packs or unpacks the files in a package, bundles or unbundles the packages in a bundle, or encrypts or decrypts the app package or bundle in the specified input directory or mapping file.</span></span> <span data-ttu-id="1afa5-218">Voici la liste des paramètres qui s’appliquent à **MakeAppx Pack**, **MakeAppx décompresser**, **MakeAppx Bundle**, **MakeAppx dégrouper**, **MakeAppx chiffrer** ou **MakeAppx déchiffrer**.</span><span class="sxs-lookup"><span data-stu-id="1afa5-218">Here is the list of parameters that apply to **MakeAppx pack**, **MakeAppx unpack**, **MakeAppx bundle**, **MakeAppx unbundle**, **MakeAppx encrypt**, or **MakeAppx decrypt**.</span></span>

<dl> <dt>

<span data-ttu-id="1afa5-219"><span id="_l"></span><span id="_L"></span>**/l**</span><span class="sxs-lookup"><span data-stu-id="1afa5-219"><span id="_l"></span><span id="_L"></span>**/l**</span></span>
</dt> <dd>

<span data-ttu-id="1afa5-220">Cette option est utilisée pour les packages localisés.</span><span class="sxs-lookup"><span data-stu-id="1afa5-220">This option is used for localized packages.</span></span> <span data-ttu-id="1afa5-221">La valeur par défaut se déclenche sur les packages localisés.</span><span class="sxs-lookup"><span data-stu-id="1afa5-221">The default validation trips on localized packages.</span></span> <span data-ttu-id="1afa5-222">Cette option désactive uniquement cette validation spécifique, sans exiger que toutes les validations soient désactivées.</span><span class="sxs-lookup"><span data-stu-id="1afa5-222">This option disables only that specific validation, without requiring that all validation be disabled.</span></span>

</dd> <dt>

<span data-ttu-id="1afa5-223"><span id="_o"></span><span id="_O"></span>**/o**</span><span class="sxs-lookup"><span data-stu-id="1afa5-223"><span id="_o"></span><span id="_O"></span>**/o**</span></span>
</dt> <dd>

<span data-ttu-id="1afa5-224">Remplacez le fichier de sortie s’il existe.</span><span class="sxs-lookup"><span data-stu-id="1afa5-224">Overwrite the output file if it exists.</span></span> <span data-ttu-id="1afa5-225">Si vous ne spécifiez pas cette option ou l’option **/non** , l’utilisateur est invité à indiquer s’il souhaite remplacer le fichier.</span><span class="sxs-lookup"><span data-stu-id="1afa5-225">If you don't specify this option or the **/no** option, the user is asked whether they want to overwrite the file.</span></span>

<span data-ttu-id="1afa5-226">Vous ne pouvez pas utiliser cette option avec la commande **/non**.</span><span class="sxs-lookup"><span data-stu-id="1afa5-226">You can't use this option with **/no**.</span></span>

</dd> <dt>

<span data-ttu-id="1afa5-227"><span id="_no"></span><span id="_NO"></span>**/non**</span><span class="sxs-lookup"><span data-stu-id="1afa5-227"><span id="_no"></span><span id="_NO"></span>**/no**</span></span>
</dt> <dd>

<span data-ttu-id="1afa5-228">Empêche le remplacement du fichier de sortie s’il existe.</span><span class="sxs-lookup"><span data-stu-id="1afa5-228">Prevents an overwrite of the output file if it exists.</span></span> <span data-ttu-id="1afa5-229">Si vous ne spécifiez pas cette option ou l’option **/o** , l’utilisateur est invité à indiquer s’il souhaite remplacer le fichier.</span><span class="sxs-lookup"><span data-stu-id="1afa5-229">If you don't specify this option or the **/o** option, the user is asked whether they want to overwrite the file.</span></span>

<span data-ttu-id="1afa5-230">Vous ne pouvez pas utiliser cette option avec **/o**.</span><span class="sxs-lookup"><span data-stu-id="1afa5-230">You can't use this option with **/o**.</span></span>

</dd> <dt>

<span data-ttu-id="1afa5-231"><span id="_nv"></span><span id="_NV"></span>**/nv**</span><span class="sxs-lookup"><span data-stu-id="1afa5-231"><span id="_nv"></span><span id="_NV"></span>**/nv**</span></span>
</dt> <dd>

<span data-ttu-id="1afa5-232">Ignore la validation sémantique.</span><span class="sxs-lookup"><span data-stu-id="1afa5-232">Skip semantic validation.</span></span> <span data-ttu-id="1afa5-233">Si vous ne spécifiez pas cette option, l’outil effectue une validation complète du package.</span><span class="sxs-lookup"><span data-stu-id="1afa5-233">If you don't specify this option, the tool performs a full validation of the package.</span></span>

</dd> <dt>

<span data-ttu-id="1afa5-234"><span id="_v"></span><span id="_V"></span>**/f**</span><span class="sxs-lookup"><span data-stu-id="1afa5-234"><span id="_v"></span><span id="_V"></span>**/v**</span></span>
</dt> <dd>

<span data-ttu-id="1afa5-235">Activez la journalisation détaillée dans la console.</span><span class="sxs-lookup"><span data-stu-id="1afa5-235">Enable verbose logging output to the console.</span></span>

</dd> <dt>

<span data-ttu-id="1afa5-236"><span id="__"></span>**/?**</span><span class="sxs-lookup"><span data-stu-id="1afa5-236"><span id="__"></span>**/?**</span></span>
</dt> <dd>

<span data-ttu-id="1afa5-237">Affichez le texte d’aide.</span><span class="sxs-lookup"><span data-stu-id="1afa5-237">Display help text.</span></span>

</dd> </dl>

<span data-ttu-id="1afa5-238">**MakeAppx Pack** , **MakeAppx DEBALLER** , **MakeAppx Bundle**, **MakeAppx debundle**, **MakeAppx Encrypt** et **MakeAppx decrypte** sont des commandes mutuellement exclusives.</span><span class="sxs-lookup"><span data-stu-id="1afa5-238">**MakeAppx pack** , **MakeAppx unpack** , **MakeAppx bundle**, **MakeAppx unbundle**, **MakeAppx encrypt**, and **MakeAppx decrypt** are mutually exclusive commands.</span></span> <span data-ttu-id="1afa5-239">Voici les paramètres de ligne de commande qui s’appliquent spécifiquement à chaque commande :</span><span class="sxs-lookup"><span data-stu-id="1afa5-239">Here are the command-line parameters that apply specifically to each command:</span></span>

<span data-ttu-id="1afa5-240">**Pack MakeAppx** \[ **h**\]</span><span class="sxs-lookup"><span data-stu-id="1afa5-240">**MakeAppx pack** \[**h**\]</span></span>

<span data-ttu-id="1afa5-241">Crée un package.</span><span class="sxs-lookup"><span data-stu-id="1afa5-241">Creates a package.</span></span>

<dl> <dt>

<span data-ttu-id="1afa5-242"><span id="_h_algorithm"></span><span id="_H_ALGORITHM"></span> *algorithme* /h</span><span class="sxs-lookup"><span data-stu-id="1afa5-242"><span id="_h_algorithm"></span><span id="_H_ALGORITHM"></span>**/h** *algorithm*</span></span>
</dt> <dd>

<span data-ttu-id="1afa5-243">Spécifie l’algorithme de hachage à utiliser lors de la création du mappage de bloc.</span><span class="sxs-lookup"><span data-stu-id="1afa5-243">Specifies the hash algorithm to use when creating the block map.</span></span> <span data-ttu-id="1afa5-244">Voici les valeurs valides pour l' *algorithme*:</span><span class="sxs-lookup"><span data-stu-id="1afa5-244">Here are valid values for *algorithm*:</span></span>

<dl> <dd><span data-ttu-id="1afa5-245">SHA256 (par défaut)</span><span class="sxs-lookup"><span data-stu-id="1afa5-245">SHA256 (default)</span></span></dd> <dd><span data-ttu-id="1afa5-246">SHA384</span><span class="sxs-lookup"><span data-stu-id="1afa5-246">SHA384</span></span></dd> <dd><span data-ttu-id="1afa5-247">SHA512</span><span class="sxs-lookup"><span data-stu-id="1afa5-247">SHA512</span></span></dd> </dl>

<span data-ttu-id="1afa5-248">Vous ne pouvez pas utiliser cette option avec la commande **décompresser** .</span><span class="sxs-lookup"><span data-stu-id="1afa5-248">You can't use this option with the **unpack** command.</span></span>

</dd> </dl>

<span data-ttu-id="1afa5-249">**Décompression MakeAppx** \[ **PFN**\]</span><span class="sxs-lookup"><span data-stu-id="1afa5-249">**MakeAppx unpack** \[**pfn**\]</span></span>

<span data-ttu-id="1afa5-250">Extrait tous les fichiers du package spécifié dans le répertoire de sortie spécifié.</span><span class="sxs-lookup"><span data-stu-id="1afa5-250">Extracts all files in the specified package to the specified output directory.</span></span> <span data-ttu-id="1afa5-251">La sortie a la même structure de répertoire que le package.</span><span class="sxs-lookup"><span data-stu-id="1afa5-251">The output has the same directory structure as the package.</span></span>

<dl> <dt>

<span data-ttu-id="1afa5-252"><span id="_pfn"></span><span id="_PFN"></span>**/pfn**</span><span class="sxs-lookup"><span data-stu-id="1afa5-252"><span id="_pfn"></span><span id="_PFN"></span>**/pfn**</span></span>
</dt> <dd>

<span data-ttu-id="1afa5-253">Spécifie un répertoire nommé avec le nom complet du package.</span><span class="sxs-lookup"><span data-stu-id="1afa5-253">Specifies a directory named with the package full name.</span></span> <span data-ttu-id="1afa5-254">Ce répertoire est créé sous l’emplacement de sortie fourni.</span><span class="sxs-lookup"><span data-stu-id="1afa5-254">This directory is created under the provided output location.</span></span> <span data-ttu-id="1afa5-255">Vous ne pouvez pas utiliser cette option avec la commande **Pack** .</span><span class="sxs-lookup"><span data-stu-id="1afa5-255">You can't use this option with the **pack** command.</span></span>

</dd> </dl>

<span data-ttu-id="1afa5-256">**Désassemblage MakeAppx** \[ **PFN**\]</span><span class="sxs-lookup"><span data-stu-id="1afa5-256">**MakeAppx unbundle** \[**pfn**\]</span></span>

<span data-ttu-id="1afa5-257">Décompresse tous les packages dans un sous-répertoire sous le chemin de sortie spécifié, nommé d’après le nom complet du bundle.</span><span class="sxs-lookup"><span data-stu-id="1afa5-257">Unpacks all packages to a subdirectory under the specified output path, named after the bundle full name.</span></span> <span data-ttu-id="1afa5-258">La sortie a la même structure de répertoire que l’offre groupée de packages installée.</span><span class="sxs-lookup"><span data-stu-id="1afa5-258">The output has the same directory structure as the installed package bundle.</span></span>

<dl> <dt>

<span data-ttu-id="1afa5-259"><span id="_pfn"></span><span id="_PFN"></span>**/pfn**</span><span class="sxs-lookup"><span data-stu-id="1afa5-259"><span id="_pfn"></span><span id="_PFN"></span>**/pfn**</span></span>
</dt> <dd>

<span data-ttu-id="1afa5-260">Spécifie un répertoire nommé avec le nom complet du groupement de packages.</span><span class="sxs-lookup"><span data-stu-id="1afa5-260">Specifies a directory named with the package bundle full name.</span></span> <span data-ttu-id="1afa5-261">Ce répertoire est créé sous l’emplacement de sortie fourni.</span><span class="sxs-lookup"><span data-stu-id="1afa5-261">This directory is created under the provided output location.</span></span> <span data-ttu-id="1afa5-262">Vous ne pouvez pas utiliser cette option avec la commande **Bundle** .</span><span class="sxs-lookup"><span data-stu-id="1afa5-262">You can't use this option with the **bundle** command.</span></span>

</dd> </dl>

<span data-ttu-id="1afa5-263">**Chiffrement MakeAppx** \[ **KF**, **kt**\]</span><span class="sxs-lookup"><span data-stu-id="1afa5-263">**MakeAppx encrypt** \[**kf**, **kt**\]</span></span>

<span data-ttu-id="1afa5-264">Crée un package d’application chiffré à partir du package d’application d’entrée spécifié au package de sortie spécifié.</span><span class="sxs-lookup"><span data-stu-id="1afa5-264">Creates an encrypted app package from the specified input app package at the specified output package.</span></span>

<dl> <dt>

<span data-ttu-id="1afa5-265"><span id="_kf__key_file_"></span><span id="_KF__KEY_FILE_"></span>\**/KF\*\*\*<key file>*</span><span class="sxs-lookup"><span data-stu-id="1afa5-265"><span id="_kf__key_file_"></span><span id="_KF__KEY_FILE_"></span>**/kf** *<key file>*</span></span>
</dt> <dd>

<span data-ttu-id="1afa5-266">Chiffre le package ou le bundle à l’aide de la clé du fichier de clé spécifié.</span><span class="sxs-lookup"><span data-stu-id="1afa5-266">Encrypts the package or bundle using the key from the specified key file.</span></span> <span data-ttu-id="1afa5-267">Vous ne pouvez pas utiliser cette option avec **kt**.</span><span class="sxs-lookup"><span data-stu-id="1afa5-267">You can't use this option with **kt**.</span></span>

</dd> <dt>

<span data-ttu-id="1afa5-268"><span id="_kt"></span><span id="_KT"></span>**/kt**</span><span class="sxs-lookup"><span data-stu-id="1afa5-268"><span id="_kt"></span><span id="_KT"></span>**/kt**</span></span>
</dt> <dd>

<span data-ttu-id="1afa5-269">Chiffre le package ou le bundle à l’aide de la clé de test globale.</span><span class="sxs-lookup"><span data-stu-id="1afa5-269">Encrypts the package or bundle using the global test key.</span></span> <span data-ttu-id="1afa5-270">Vous ne pouvez pas utiliser cette option avec **KF**.</span><span class="sxs-lookup"><span data-stu-id="1afa5-270">You can't use this option with **kf**.</span></span>

</dd> </dl>

<span data-ttu-id="1afa5-271">**Déchiffrement MakeAppx** \[ **KF**, **kt**\]</span><span class="sxs-lookup"><span data-stu-id="1afa5-271">**MakeAppx decrypt** \[**kf**, **kt**\]</span></span>

<span data-ttu-id="1afa5-272">Crée un package d’application non chiffré à partir du package d’application d’entrée spécifié au package de sortie spécifié.</span><span class="sxs-lookup"><span data-stu-id="1afa5-272">Creates an unencrypted app package from the specified input app package at the specified output package.</span></span>

<dl> <dt>

<span data-ttu-id="1afa5-273"><span id="_kf__key_file_"></span><span id="_KF__KEY_FILE_"></span>\**/KF\*\*\*<key file>*</span><span class="sxs-lookup"><span data-stu-id="1afa5-273"><span id="_kf__key_file_"></span><span id="_KF__KEY_FILE_"></span>**/kf** *<key file>*</span></span>
</dt> <dd>

<span data-ttu-id="1afa5-274">Déchiffre le package ou l’offre groupée à l’aide de la clé du fichier de clé spécifié.</span><span class="sxs-lookup"><span data-stu-id="1afa5-274">Decrypts the package or bundle using the key from the specified key file.</span></span> <span data-ttu-id="1afa5-275">Vous ne pouvez pas utiliser cette option avec **kt**.</span><span class="sxs-lookup"><span data-stu-id="1afa5-275">You can't use this option with **kt**.</span></span>

</dd> <dt>

<span data-ttu-id="1afa5-276"><span id="_kt"></span><span id="_KT"></span>**/kt**</span><span class="sxs-lookup"><span data-stu-id="1afa5-276"><span id="_kt"></span><span id="_KT"></span>**/kt**</span></span>
</dt> <dd>

<span data-ttu-id="1afa5-277">Déchiffre le package ou le bundle à l’aide de la clé de test globale.</span><span class="sxs-lookup"><span data-stu-id="1afa5-277">Decrypts the package or bundle using the global test key.</span></span> <span data-ttu-id="1afa5-278">Vous ne pouvez pas utiliser cette option avec **KF**.</span><span class="sxs-lookup"><span data-stu-id="1afa5-278">You can't use this option with **kf**.</span></span>

</dd> </dl>

## <a name="semantic-validation-performed-by-makeappx"></a><span data-ttu-id="1afa5-279">Validation sémantique effectuée par MakeAppx</span><span class="sxs-lookup"><span data-stu-id="1afa5-279">Semantic validation performed by MakeAppx</span></span>

<span data-ttu-id="1afa5-280">MakeAppx effectue une validation sémantique limitée qui est conçue pour intercepter les erreurs de déploiement les plus courantes et pour s’assurer que le package d’application est valide.</span><span class="sxs-lookup"><span data-stu-id="1afa5-280">MakeAppx performs limited semantic validation that is designed to catch the most common deployment errors and help ensure that the app package is valid.</span></span>

<span data-ttu-id="1afa5-281">Cette validation vérifie que :</span><span class="sxs-lookup"><span data-stu-id="1afa5-281">This validation ensures that:</span></span>

-   <span data-ttu-id="1afa5-282">tous les fichiers référencés dans le manifeste du package sont inclus dans le package d’application ;</span><span class="sxs-lookup"><span data-stu-id="1afa5-282">All files referenced in the package manifest are included in the app package.</span></span>
-   <span data-ttu-id="1afa5-283">une application n’a pas deux clés identiques ;</span><span class="sxs-lookup"><span data-stu-id="1afa5-283">An application does not have two identical keys.</span></span>
-   <span data-ttu-id="1afa5-284">Une application ne s’inscrit pas pour un protocole interdit dans cette liste : SMB, fichier, MS-WWA-WEB, MS-WWA.</span><span class="sxs-lookup"><span data-stu-id="1afa5-284">An application does not register for a forbidden protocol from this list: SMB , FILE, MS-WWA-WEB, MS-WWA.</span></span>

<span data-ttu-id="1afa5-285">Cette validation sémantique n’est pas terminée, et il n’est pas garanti que les packages générés par MakeAppx soient installés.</span><span class="sxs-lookup"><span data-stu-id="1afa5-285">This semantic validation is not complete, and packages built by MakeAppx are not guaranteed to be installable.</span></span>

 

 