---
description: Le WiStream.vbs de fichiers VBScript est fourni dans les composants SDK Windows pour les développeurs Windows Installer.
ms.assetid: f96d1fdd-81c8-4fb2-a23e-fda49ace8bef
title: Gérer les flux binaires
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 877631a40157a5d286ef0c2575732a6d561eefb8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106532143"
---
# <a name="manage-binary-streams"></a><span data-ttu-id="e1bea-103">Gérer les flux binaires</span><span class="sxs-lookup"><span data-stu-id="e1bea-103">Manage Binary Streams</span></span>

<span data-ttu-id="e1bea-104">Le WiStream.vbs de fichiers VBScript est fourni dans les [composants SDK Windows pour les développeurs Windows Installer](platform-sdk-components-for-windows-installer-developers.md).</span><span class="sxs-lookup"><span data-stu-id="e1bea-104">The VBScript file WiStream.vbs is provided in the [Windows SDK Components for Windows Installer Developers](platform-sdk-components-for-windows-installer-developers.md).</span></span> <span data-ttu-id="e1bea-105">Cet exemple montre comment le script peut être utilisé pour gérer des flux binaires dans une base de données Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="e1bea-105">This sample shows how script can be used to manage binary streams in a Windows Installer database.</span></span> <span data-ttu-id="e1bea-106">L’exemple peut être utilisé pour entrer des fichiers CAB compressés dans une base de données.</span><span class="sxs-lookup"><span data-stu-id="e1bea-106">The sample may be used to enter compressed file cabinets into a database.</span></span> <span data-ttu-id="e1bea-107">Cet exemple illustre l’opération de la [ \_ table Streams](-streams-table.md) dans la base de données Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="e1bea-107">This sample demonstrates the operation of the [\_Streams table](-streams-table.md) in the Windows Installer database.</span></span>

<span data-ttu-id="e1bea-108">L’exemple illustre également l’utilisation de :</span><span class="sxs-lookup"><span data-stu-id="e1bea-108">The sample also demonstrates the use of:</span></span>

-   [<span data-ttu-id="e1bea-109">**OpenDatabase, méthode (objet installer)**</span><span class="sxs-lookup"><span data-stu-id="e1bea-109">**OpenDatabase method (Installer Object)**</span></span>](installer-opendatabase.md)
-   [<span data-ttu-id="e1bea-110">**Méthode CreateRecord**</span><span class="sxs-lookup"><span data-stu-id="e1bea-110">**CreateRecord method**</span></span>](installer-createrecord.md)
-   <span data-ttu-id="e1bea-111">[**Méthode LastErrorRecord**](installer-lasterrorrecord.md) de l' [ **objet installer**](installer-object.md)</span><span class="sxs-lookup"><span data-stu-id="e1bea-111">[**LastErrorRecord method**](installer-lasterrorrecord.md) of the [**Installer object**](installer-object.md)</span></span>
-   [<span data-ttu-id="e1bea-112">**OpenView, méthode**</span><span class="sxs-lookup"><span data-stu-id="e1bea-112">**OpenView method**</span></span>](database-openview.md)
-   <span data-ttu-id="e1bea-113">[**Méthode Commit**](database-commit.md) de l' [ **objet Database**](database-object.md)</span><span class="sxs-lookup"><span data-stu-id="e1bea-113">[**Commit method**](database-commit.md) of the [**Database object**](database-object.md)</span></span>
-   [<span data-ttu-id="e1bea-114">**Méthode fetch**</span><span class="sxs-lookup"><span data-stu-id="e1bea-114">**Fetch method**</span></span>](view-fetch.md)
-   [<span data-ttu-id="e1bea-115">**Modify, méthode**</span><span class="sxs-lookup"><span data-stu-id="e1bea-115">**Modify method**</span></span>](view-modify.md)
-   <span data-ttu-id="e1bea-116">[**Méthode Execute**](view-execute.md) de l' [ **objet View**](view-object.md)</span><span class="sxs-lookup"><span data-stu-id="e1bea-116">[**Execute method**](view-execute.md) of the [**View object**](view-object.md)</span></span>
-   [<span data-ttu-id="e1bea-117">**StringData, propriété**</span><span class="sxs-lookup"><span data-stu-id="e1bea-117">**StringData property**</span></span>](record-stringdata.md)
-   <span data-ttu-id="e1bea-118">[**Méthode SetStream**](record-setstream.md) de l' [ **objet record**](record-object.md)</span><span class="sxs-lookup"><span data-stu-id="e1bea-118">[**SetStream method**](record-setstream.md) of the [**Record object**](record-object.md)</span></span>

<span data-ttu-id="e1bea-119">Vous aurez besoin de la version CScript.exe ou WScript.exe de Windows Script Host pour utiliser cet exemple.</span><span class="sxs-lookup"><span data-stu-id="e1bea-119">You'll require the CScript.exe or WScript.exe version of Windows Script Host to use this sample.</span></span> <span data-ttu-id="e1bea-120">Pour utiliser CScript.exe pour exécuter cet exemple, tapez une ligne de commande à l’invite de commandes en utilisant la syntaxe suivante.</span><span class="sxs-lookup"><span data-stu-id="e1bea-120">To use CScript.exe to run this sample, type a command line at the command prompt using the following syntax.</span></span> <span data-ttu-id="e1bea-121">L’aide s’affiche si le premier argument est/ ?</span><span class="sxs-lookup"><span data-stu-id="e1bea-121">Help is displayed if the first argument is /?</span></span> <span data-ttu-id="e1bea-122">ou si le nombre d’arguments spécifié est insuffisant.</span><span class="sxs-lookup"><span data-stu-id="e1bea-122">or if too few arguments are specified.</span></span> <span data-ttu-id="e1bea-123">Pour rediriger la sortie vers un fichier, terminez la ligne de commande avec VBS > \[ *chemin d’accès au fichier* \] .</span><span class="sxs-lookup"><span data-stu-id="e1bea-123">To redirect the output to a file, end the command line with VBS > \[*path to file*\].</span></span> <span data-ttu-id="e1bea-124">L’exemple retourne la valeur 0 pour Success, 1 si l’aide est appelée, et 2 si le script échoue.</span><span class="sxs-lookup"><span data-stu-id="e1bea-124">The sample returns a value of 0 for success, 1 if help is invoked, and 2 if the script fails.</span></span>

<span data-ttu-id="e1bea-125">**cscript WiStream.vbs \[ chemin d’accès au chemin de la base de données \] \[ Options du fichier \] \[ nom du \] \[ flux\]**</span><span class="sxs-lookup"><span data-stu-id="e1bea-125">**cscript WiStream.vbs \[path to database\]\[path to file\]\[options\]\[stream name\]**</span></span>

<span data-ttu-id="e1bea-126">Spécifiez le chemin d’accès à la base de données Windows Installer qui doit recevoir le flux.</span><span class="sxs-lookup"><span data-stu-id="e1bea-126">Specify the path to the Windows Installer database that is to receive the stream.</span></span> <span data-ttu-id="e1bea-127">Spécifiez un chemin d’accès au fichier binaire contenant les données de flux.</span><span class="sxs-lookup"><span data-stu-id="e1bea-127">Specify a path to the binary file containing the stream data.</span></span> <span data-ttu-id="e1bea-128">Pour afficher la liste des flux dans la base de données du programme d’installation, omettez ce chemin.</span><span class="sxs-lookup"><span data-stu-id="e1bea-128">To list the streams in the installer database, omit this path.</span></span> <span data-ttu-id="e1bea-129">Vous pouvez spécifier un nom de flux facultatif. si ce paramètre est omis, le nom de fichier est utilisé par défaut.</span><span class="sxs-lookup"><span data-stu-id="e1bea-129">You may specify an optional stream name, if this is omitted it defaults to the file name.</span></span>

<span data-ttu-id="e1bea-130">L’option suivante peut être spécifiée.</span><span class="sxs-lookup"><span data-stu-id="e1bea-130">The following option may be specified.</span></span>



| <span data-ttu-id="e1bea-131">Option</span><span class="sxs-lookup"><span data-stu-id="e1bea-131">Option</span></span>              | <span data-ttu-id="e1bea-132">Description</span><span class="sxs-lookup"><span data-stu-id="e1bea-132">Description</span></span>                                                                                     |
|---------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e1bea-133">aucune option spécifiée</span><span class="sxs-lookup"><span data-stu-id="e1bea-133">no option specified</span></span> | <span data-ttu-id="e1bea-134">Ajoutez un flux à la base de données Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="e1bea-134">Add a stream to the Windows Installer database.</span></span>                                                 |
| <span data-ttu-id="e1bea-135">/d</span><span class="sxs-lookup"><span data-stu-id="e1bea-135">/d</span></span>                  | <span data-ttu-id="e1bea-136">Supprimer un flux.</span><span class="sxs-lookup"><span data-stu-id="e1bea-136">Remove a stream.</span></span> <span data-ttu-id="e1bea-137">Cet indicateur d’option doit être suivi du nom du sous-stockage en cours de suppression.</span><span class="sxs-lookup"><span data-stu-id="e1bea-137">This option flag must be followed by the name of the substorage being removed.</span></span> |



 

<span data-ttu-id="e1bea-138">Pour obtenir des exemples supplémentaires de scripts, consultez [Windows Installer des exemples de scripts](windows-installer-scripting-examples.md).</span><span class="sxs-lookup"><span data-stu-id="e1bea-138">For additional scripting examples, see [Windows Installer Scripting Examples](windows-installer-scripting-examples.md).</span></span> <span data-ttu-id="e1bea-139">Pour obtenir des exemples d’utilitaires qui ne nécessitent pas Windows Script Host, consultez [Windows Installer les outils de développement](windows-installer-development-tools.md).</span><span class="sxs-lookup"><span data-stu-id="e1bea-139">For sample utilities that do not require Windows Script Host, see [Windows Installer Development Tools](windows-installer-development-tools.md).</span></span>

 

 



