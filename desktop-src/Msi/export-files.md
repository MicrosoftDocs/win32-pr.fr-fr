---
description: Le WiExport.vbs de fichiers VBScript est fourni dans les composants SDK Windows pour les développeurs Windows Installer.
ms.assetid: 3ff7bd48-cb22-4d5b-a607-39eaeb67c55b
title: Exporter des fichiers
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1512650ee144fc00c2de851051b9bbb4d98a21e0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106519803"
---
# <a name="export-files"></a><span data-ttu-id="a6443-103">Exporter des fichiers</span><span class="sxs-lookup"><span data-stu-id="a6443-103">Export Files</span></span>

<span data-ttu-id="a6443-104">Le WiExport.vbs de fichiers VBScript est fourni dans les [composants SDK Windows pour les développeurs Windows Installer](platform-sdk-components-for-windows-installer-developers.md).</span><span class="sxs-lookup"><span data-stu-id="a6443-104">The VBScript file WiExport.vbs is provided in the [Windows SDK Components for Windows Installer Developers](platform-sdk-components-for-windows-installer-developers.md).</span></span> <span data-ttu-id="a6443-105">Cet exemple montre comment écrire un script pour exporter des tables dans une base de données Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="a6443-105">This sample shows how to write script to export tables into a Windows Installer database.</span></span> <span data-ttu-id="a6443-106">L’exemple de script se connecte à un objet [**installer**](installer-object.md) , ouvre une base de données et exporte des tables vers des fichiers d’archive.</span><span class="sxs-lookup"><span data-stu-id="a6443-106">The script sample connects to an [**Installer**](installer-object.md) object, opens a database and exports tables to archive files.</span></span>

<span data-ttu-id="a6443-107">L’exemple illustre l’utilisation de :</span><span class="sxs-lookup"><span data-stu-id="a6443-107">The sample demonstrates the use of:</span></span>

-   [<span data-ttu-id="a6443-108">**OpenDatabase, méthode (objet installer)**</span><span class="sxs-lookup"><span data-stu-id="a6443-108">**OpenDatabase Method (Installer Object)**</span></span>](installer-opendatabase.md)
-   <span data-ttu-id="a6443-109">[**Méthode LastErrorRecord**](installer-lasterrorrecord.md) de l' [ **objet installer**](installer-object.md)</span><span class="sxs-lookup"><span data-stu-id="a6443-109">[**LastErrorRecord method**](installer-lasterrorrecord.md) of the [**Installer object**](installer-object.md)</span></span>
-   [<span data-ttu-id="a6443-110">**Méthode d’exportation**</span><span class="sxs-lookup"><span data-stu-id="a6443-110">**Export method**</span></span>](database-export.md)
-   <span data-ttu-id="a6443-111">[**Méthode OpenView**](database-openview.md) de l' [ **objet Database**](database-object.md)</span><span class="sxs-lookup"><span data-stu-id="a6443-111">[**OpenView method**](database-openview.md) of the [**Database object**](database-object.md)</span></span>
-   <span data-ttu-id="a6443-112">[**Méthode fetch**](view-fetch.md) de l' [ **objet View**](view-object.md)</span><span class="sxs-lookup"><span data-stu-id="a6443-112">[**Fetch method**](view-fetch.md) of the [**View object**](view-object.md)</span></span>
-   <span data-ttu-id="a6443-113">[**Propriété StringData**](record-stringdata.md) de l' [ **objet record**](record-object.md)</span><span class="sxs-lookup"><span data-stu-id="a6443-113">[**StringData property**](record-stringdata.md) of the [**Record object**](record-object.md)</span></span>

<span data-ttu-id="a6443-114">Vous aurez besoin de la version CScript.exe ou WScript.exe de Windows Script Host pour utiliser cet exemple.</span><span class="sxs-lookup"><span data-stu-id="a6443-114">You'll require the CScript.exe or WScript.exe version of Windows Script Host to use this sample.</span></span> <span data-ttu-id="a6443-115">Pour utiliser CScript.exe pour exécuter cet exemple, tapez une ligne de commande à l’invite de commandes en utilisant la syntaxe suivante.</span><span class="sxs-lookup"><span data-stu-id="a6443-115">To use CScript.exe to run this sample, type a command line at the command prompt using the following syntax.</span></span> <span data-ttu-id="a6443-116">L’aide s’affiche si le premier argument est/ ?</span><span class="sxs-lookup"><span data-stu-id="a6443-116">Help is displayed if the first argument is /?</span></span> <span data-ttu-id="a6443-117">ou si le nombre d’arguments spécifié est insuffisant.</span><span class="sxs-lookup"><span data-stu-id="a6443-117">or if too few arguments are specified.</span></span> <span data-ttu-id="a6443-118">Pour rediriger la sortie vers un fichier, terminez la ligne de commande avec VBS > \[ *chemin d’accès au fichier* \] .</span><span class="sxs-lookup"><span data-stu-id="a6443-118">To redirect the output to a file, end the command line with VBS > \[*path to file*\].</span></span> <span data-ttu-id="a6443-119">L’exemple retourne la valeur 0 pour Success, 1 si l’aide est appelée, et 2 si le script échoue.</span><span class="sxs-lookup"><span data-stu-id="a6443-119">The sample returns a value of 0 for success, 1 if help is invoked, and 2 if the script fails.</span></span>

<span data-ttu-id="a6443-120">**cscript WiExport.vbs chemin d’accès de la \[ base de données \] \[ aux options du dossier \] \[ liste des noms de \] \[ table\]**</span><span class="sxs-lookup"><span data-stu-id="a6443-120">**cscript WiExport.vbs \[path to database\]\[path to folder\]\[options\]\[table name list\]**</span></span>

<span data-ttu-id="a6443-121">Spécifiez le chemin d’accès à la base de données du programme d’installation à partir de laquelle les tables sont exportées.</span><span class="sxs-lookup"><span data-stu-id="a6443-121">Specify the path to the installer database from which the tables are being exported.</span></span> <span data-ttu-id="a6443-122">Spécifiez le chemin d’accès au dossier dans lequel les fichiers d’archive exportés doivent être copiés.</span><span class="sxs-lookup"><span data-stu-id="a6443-122">Specify the path to the folder into which the exported archive files are to be copied.</span></span> <span data-ttu-id="a6443-123">Répertorie les noms qui respectent la casse des [tables de base de données](database-tables.md) en cours d’exportation.</span><span class="sxs-lookup"><span data-stu-id="a6443-123">List the case-sensitive names of the [database tables](database-tables.md) being exported.</span></span> <span data-ttu-id="a6443-124">Spécifiez « \* » pour exporter toutes les tables, y compris \_ SummaryInformation.</span><span class="sxs-lookup"><span data-stu-id="a6443-124">Specify '\*' to export all the tables including \_SummaryInformation.</span></span>

<span data-ttu-id="a6443-125">Les options suivantes peuvent être spécifiées n’importe où sur la ligne de commande avant la liste nom de la table.</span><span class="sxs-lookup"><span data-stu-id="a6443-125">The following options may be specified anywhere on the command line before the table name list.</span></span>



| <span data-ttu-id="a6443-126">Option</span><span class="sxs-lookup"><span data-stu-id="a6443-126">Option</span></span>              | <span data-ttu-id="a6443-127">Description</span><span class="sxs-lookup"><span data-stu-id="a6443-127">Description</span></span>                                            |
|---------------------|--------------------------------------------------------|
| <span data-ttu-id="a6443-128">aucune option spécifiée</span><span class="sxs-lookup"><span data-stu-id="a6443-128">no option specified</span></span> | <span data-ttu-id="a6443-129">Les fichiers d’archive exportés peuvent avoir un nom de fichier long.</span><span class="sxs-lookup"><span data-stu-id="a6443-129">Exported archive files may have a long file name.</span></span>      |
| <span data-ttu-id="a6443-130">/s</span><span class="sxs-lookup"><span data-stu-id="a6443-130">/s</span></span>                  | <span data-ttu-id="a6443-131">Obliger les fichiers d’archive exportés à avoir des noms de fichiers courts.</span><span class="sxs-lookup"><span data-stu-id="a6443-131">Force exported archive files to have short file names.</span></span> |



 

<span data-ttu-id="a6443-132">Pour obtenir des exemples supplémentaires de scripts, consultez [Windows Installer des exemples de scripts](windows-installer-scripting-examples.md).</span><span class="sxs-lookup"><span data-stu-id="a6443-132">For additional scripting examples, see [Windows Installer Scripting Examples](windows-installer-scripting-examples.md).</span></span> <span data-ttu-id="a6443-133">Pour obtenir des exemples d’utilitaires qui ne nécessitent pas Windows Script Host, consultez [Windows Installer les outils de développement](windows-installer-development-tools.md).</span><span class="sxs-lookup"><span data-stu-id="a6443-133">For sample utilities that do not require Windows Script Host, see [Windows Installer Development Tools](windows-installer-development-tools.md).</span></span>

 

 



