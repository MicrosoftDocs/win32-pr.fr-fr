---
description: Le WiFilVer.vbs de fichiers VBScript est fourni dans les composants SDK Windows pour les développeurs Windows Installer. L’exemple vous montre comment vous pouvez utiliser un script pour signaler ou mettre à jour la version de fichier, la taille et les informations de langue.
ms.assetid: 21550eea-c30b-4738-9201-ab500356fabf
title: Gérer les tailles et les versions des fichiers
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 426acf71956d87fe1458447119d79bc142f1ee75
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103752773"
---
# <a name="manage-file-sizes-and-versions"></a><span data-ttu-id="e1fef-104">Gérer les tailles et les versions des fichiers</span><span class="sxs-lookup"><span data-stu-id="e1fef-104">Manage File Sizes and Versions</span></span>

<span data-ttu-id="e1fef-105">Le WiFilVer.vbs de fichiers VBScript est fourni dans les [composants SDK Windows pour les développeurs Windows Installer](platform-sdk-components-for-windows-installer-developers.md).</span><span class="sxs-lookup"><span data-stu-id="e1fef-105">The VBScript file WiFilVer.vbs is provided in the [Windows SDK Components for Windows Installer Developers](platform-sdk-components-for-windows-installer-developers.md).</span></span> <span data-ttu-id="e1fef-106">L’exemple vous montre comment vous pouvez utiliser un script pour signaler ou mettre à jour la version de fichier, la taille et les informations de langue.</span><span class="sxs-lookup"><span data-stu-id="e1fef-106">The sample shows you how you can use a script to report or update the file version, size, and language information.</span></span>

<span data-ttu-id="e1fef-107">L’exemple montre également Windows Installer actions, comment accéder à une base de données Windows Installer et utiliser les éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="e1fef-107">The sample also shows you Windows Installer actions, how to access a Windows Installer database, and the use of the following:</span></span>

-   <span data-ttu-id="e1fef-108">Méthode [**installer. OpenDatabase**](installer-opendatabase.md) de l' [ **objet installer**](installer-object.md)</span><span class="sxs-lookup"><span data-stu-id="e1fef-108">[**Installer.OpenDatabase**](installer-opendatabase.md) method of the [**Installer Object**](installer-object.md)</span></span>
-   <span data-ttu-id="e1fef-109">[**Installer. FileAttributes,**](installer-fileattributes.md) propriété</span><span class="sxs-lookup"><span data-stu-id="e1fef-109">[**Installer.FileAttributes**](installer-fileattributes.md) property</span></span>
-   <span data-ttu-id="e1fef-110">[**Installer. FileHash,**](installer-filehash.md) méthode</span><span class="sxs-lookup"><span data-stu-id="e1fef-110">[**Installer.FileHash**](installer-filehash.md) method</span></span>
-   <span data-ttu-id="e1fef-111">[**Installer. FileVersion,**](installer-fileversion.md) méthode</span><span class="sxs-lookup"><span data-stu-id="e1fef-111">[**Installer.FileVersion**](installer-fileversion.md) method</span></span>
-   <span data-ttu-id="e1fef-112">Méthode [**installer. LastErrorRecord**](installer-lasterrorrecord.md) de l' [ **objet installer**](installer-object.md)</span><span class="sxs-lookup"><span data-stu-id="e1fef-112">[**Installer.LastErrorRecord**](installer-lasterrorrecord.md) method of the [**Installer Object**](installer-object.md)</span></span>
-   <span data-ttu-id="e1fef-113">[**Database. OpenView,**](database-openview.md) méthode</span><span class="sxs-lookup"><span data-stu-id="e1fef-113">[**Database.OpenView**](database-openview.md) method</span></span>
-   <span data-ttu-id="e1fef-114">Propriété [**Database. SummaryInformation**](database-summaryinformation.md) de l' [ **objet Database**](database-object.md)</span><span class="sxs-lookup"><span data-stu-id="e1fef-114">[**Database.SummaryInformation**](database-summaryinformation.md) property of the [**Database Object**](database-object.md)</span></span>
-   <span data-ttu-id="e1fef-115">[**Session. subaction,**](session-doaction.md) méthode</span><span class="sxs-lookup"><span data-stu-id="e1fef-115">[**Session.DoAction**](session-doaction.md) method</span></span>
-   [<span data-ttu-id="e1fef-116">**Session. Property**</span><span class="sxs-lookup"><span data-stu-id="e1fef-116">**Session.Property**</span></span>](session-session.md)
-   <span data-ttu-id="e1fef-117">[**Session. SourcePath,**](session-sourcepath.md) propriété</span><span class="sxs-lookup"><span data-stu-id="e1fef-117">[**Session.SourcePath**](session-sourcepath.md) property</span></span>
-   <span data-ttu-id="e1fef-118">Propriété [**session. mode**](session-mode.md) de l' [ **objet session**](session-object.md)</span><span class="sxs-lookup"><span data-stu-id="e1fef-118">[**Session.Mode**](session-mode.md) property of the [**Session Object**](session-object.md)</span></span>
-   <span data-ttu-id="e1fef-119">[**Record. StringData,**](record-stringdata.md) propriété</span><span class="sxs-lookup"><span data-stu-id="e1fef-119">[**Record.StringData**](record-stringdata.md) property</span></span>
-   <span data-ttu-id="e1fef-120">Propriété [**record. IntegerData**](record-integerdata.md) de l' [ **objet record**](record-object.md)</span><span class="sxs-lookup"><span data-stu-id="e1fef-120">[**Record.IntegerData**](record-integerdata.md) property of the [**Record Object**](record-object.md)</span></span>

<span data-ttu-id="e1fef-121">L’utilisation de cet exemple nécessite la version CScript.exe ou WScript.exe de Windows Script Host.</span><span class="sxs-lookup"><span data-stu-id="e1fef-121">Using this sample requires the CScript.exe or WScript.exe version of Windows Script Host.</span></span> <span data-ttu-id="e1fef-122">Pour utiliser CScript.exe pour exécuter cet exemple, tapez une commande à l’invite de commandes en utilisant la syntaxe suivante :</span><span class="sxs-lookup"><span data-stu-id="e1fef-122">To use CScript.exe to run this sample, type a command at the command prompt by using the following syntax:</span></span>

<span data-ttu-id="e1fef-123">**cscript WiFilVer.vbs \[ chemin d’accès à la base de données \] \[ emplacements sources facultatifs\]**</span><span class="sxs-lookup"><span data-stu-id="e1fef-123">**cscript WiFilVer.vbs \[path to database\]\[optional source locations\]**</span></span>

<span data-ttu-id="e1fef-124">Tenez également compte des éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="e1fef-124">Also be aware of the following:</span></span>

-   <span data-ttu-id="e1fef-125">L’aide s’affiche si le premier argument est/ ?</span><span class="sxs-lookup"><span data-stu-id="e1fef-125">Help is displayed if the first argument is /?</span></span> <span data-ttu-id="e1fef-126">ou si le nombre d’arguments spécifié est insuffisant.</span><span class="sxs-lookup"><span data-stu-id="e1fef-126">or if too few arguments are specified.</span></span>
-   <span data-ttu-id="e1fef-127">Pour rediriger la sortie vers un fichier, terminez la ligne de commande avec VBS > \[ *chemin d’accès au fichier* \] .</span><span class="sxs-lookup"><span data-stu-id="e1fef-127">To redirect the output to a file, end the command line with VBS > \[*path to file*\].</span></span>
-   <span data-ttu-id="e1fef-128">L’exemple retourne la valeur 0 (zéro) pour Success, 1 (un) si l’aide est appelée, et 2 (deux) si le script échoue.</span><span class="sxs-lookup"><span data-stu-id="e1fef-128">The sample returns a value of 0 (zero) for success, 1 (one) if help is invoked, and 2 (two) if the script fails.</span></span>

<span data-ttu-id="e1fef-129">Spécifiez la base de données Windows Installer que vous souhaitez mettre à jour, qui doit se trouver à la racine du fichier source.</span><span class="sxs-lookup"><span data-stu-id="e1fef-129">Specify the Windows Installer database that you want to be updated, which must be located at the source file root.</span></span> <span data-ttu-id="e1fef-130">Toutefois, vous pouvez spécifier des sources pour la base de données à des emplacements distincts.</span><span class="sxs-lookup"><span data-stu-id="e1fef-130">However, you can specify sources for the database at separate locations.</span></span> <span data-ttu-id="e1fef-131">Si la source est compressée, tous les fichiers sont ouverts à la racine.</span><span class="sxs-lookup"><span data-stu-id="e1fef-131">If the source is compressed, all the files are opened at the root.</span></span>

<span data-ttu-id="e1fef-132">Les options suivantes peuvent être spécifiées à n’importe quel emplacement sur la ligne de commande.</span><span class="sxs-lookup"><span data-stu-id="e1fef-132">The following options can be specified at any location on the command line.</span></span>



| <span data-ttu-id="e1fef-133">Option</span><span class="sxs-lookup"><span data-stu-id="e1fef-133">Option</span></span>                | <span data-ttu-id="e1fef-134">Description</span><span class="sxs-lookup"><span data-stu-id="e1fef-134">Description</span></span>                                                                              |
|-----------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="e1fef-135">*aucune option spécifiée*</span><span class="sxs-lookup"><span data-stu-id="e1fef-135">*no option specified*</span></span> | <span data-ttu-id="e1fef-136">Affichez les informations de fichier de la base de données.</span><span class="sxs-lookup"><span data-stu-id="e1fef-136">Display the file information of the database.</span></span>                                            |
| <span data-ttu-id="e1fef-137">/U</span><span class="sxs-lookup"><span data-stu-id="e1fef-137">/u</span></span>                    | <span data-ttu-id="e1fef-138">Mettez à jour la taille du fichier, la version et les informations de langue dans la base de données à partir de la source.</span><span class="sxs-lookup"><span data-stu-id="e1fef-138">Update the file size, version, and language information in the database from the source.</span></span> |



 

<span data-ttu-id="e1fef-139">Pour plus d’informations, consultez [Windows Installer des exemples de scripts](windows-installer-scripting-examples.md) et [Windows Installer outils de développement](windows-installer-development-tools.md).</span><span class="sxs-lookup"><span data-stu-id="e1fef-139">For more information, see [Windows Installer Scripting Examples](windows-installer-scripting-examples.md) and [Windows Installer Development Tools](windows-installer-development-tools.md).</span></span>

 

 



