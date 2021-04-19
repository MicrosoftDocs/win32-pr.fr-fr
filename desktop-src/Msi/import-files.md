---
description: Le WiImport.vbs de fichiers VBScript est fourni dans les composants SDK Windows pour les développeurs Windows Installer. Cet exemple montre comment écrire un script pour importer des tables dans une base de données Windows Installer.
ms.assetid: 37580bd6-30c7-4239-9717-223a381ba021
title: Importer des fichiers
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8508ee4e385e3edc737515f1b524de074489fb2b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106521444"
---
# <a name="import-files"></a><span data-ttu-id="39e61-104">Importer des fichiers</span><span class="sxs-lookup"><span data-stu-id="39e61-104">Import Files</span></span>

<span data-ttu-id="39e61-105">Le WiImport.vbs de fichiers VBScript est fourni dans les [composants SDK Windows pour les développeurs Windows Installer](platform-sdk-components-for-windows-installer-developers.md).</span><span class="sxs-lookup"><span data-stu-id="39e61-105">The VBScript file WiImport.vbs is provided in the [Windows SDK Components for Windows Installer Developers](platform-sdk-components-for-windows-installer-developers.md).</span></span> <span data-ttu-id="39e61-106">Cet exemple montre comment écrire un script pour importer des tables dans une base de données Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="39e61-106">This sample shows how to write a script to import tables into a Windows Installer database.</span></span>

<span data-ttu-id="39e61-107">Le script se connecte à un objet [**installer**](installer-object.md) , ouvre une base de données, traite une liste de fichiers et valide les modifications avant de fermer la base de données.</span><span class="sxs-lookup"><span data-stu-id="39e61-107">The script connects to an [**Installer**](installer-object.md) object, opens a database, processes a list of files, and commits the changes before closing the database.</span></span>

<span data-ttu-id="39e61-108">L’exemple illustre l’utilisation de :</span><span class="sxs-lookup"><span data-stu-id="39e61-108">The sample demonstrates the use of:</span></span>

-   [<span data-ttu-id="39e61-109">**OpenDatabase, méthode (objet installer)**</span><span class="sxs-lookup"><span data-stu-id="39e61-109">**OpenDatabase Method (Installer Object)**</span></span>](installer-opendatabase.md)
-   <span data-ttu-id="39e61-110">[**Méthode LastErrorRecord**](installer-lasterrorrecord.md) de l' [ **objet installer**](installer-object.md)</span><span class="sxs-lookup"><span data-stu-id="39e61-110">[**LastErrorRecord method**](installer-lasterrorrecord.md) of the [**Installer object**](installer-object.md)</span></span>
-   [<span data-ttu-id="39e61-111">**Import, méthode**</span><span class="sxs-lookup"><span data-stu-id="39e61-111">**Import method**</span></span>](database-import.md)
-   <span data-ttu-id="39e61-112">[**Méthode Commit**](database-commit.md) de l' [ **objet Database**](database-object.md)</span><span class="sxs-lookup"><span data-stu-id="39e61-112">[**Commit method**](database-commit.md) of the [**Database object**](database-object.md)</span></span>

<span data-ttu-id="39e61-113">Vous aurez besoin de la version CScript.exe ou WScript.exe de Windows Script Host pour utiliser cet exemple.</span><span class="sxs-lookup"><span data-stu-id="39e61-113">You'll require the CScript.exe or WScript.exe version of Windows Script Host to use this sample.</span></span> <span data-ttu-id="39e61-114">Pour utiliser CScript.exe pour exécuter cet exemple, utilisez la syntaxe suivante à l’invite de commandes.</span><span class="sxs-lookup"><span data-stu-id="39e61-114">To use CScript.exe to run this sample, use the following syntax at the command prompt.</span></span>

<span data-ttu-id="39e61-115">**cscript WiImport.vbs \[ chemin de la base de données \] \[ chemin d’accès aux options de dossier \] \[ liste des fichiers d' \] \[ Archive**\]</span><span class="sxs-lookup"><span data-stu-id="39e61-115">**cscript WiImport.vbs \[path to database\]\[path to folder\]\[options\] \[archive file list**\]</span></span>

<span data-ttu-id="39e61-116">L’aide s’affiche si le premier argument est/ ?</span><span class="sxs-lookup"><span data-stu-id="39e61-116">Help is displayed if the first argument is /?</span></span> <span data-ttu-id="39e61-117">ou si le nombre d’arguments spécifié est insuffisant.</span><span class="sxs-lookup"><span data-stu-id="39e61-117">or if too few arguments are specified.</span></span> <span data-ttu-id="39e61-118">Pour rediriger la sortie vers un fichier, terminez la ligne de commande avec VBS > \[ chemin d’accès au fichier \] . L’exemple retourne la valeur 0 pour Success, 1 si l’aide est appelée, et 2 si le script échoue.</span><span class="sxs-lookup"><span data-stu-id="39e61-118">To redirect the output to a file, end the command line with VBS > \[path to file\].The sample returns a value of 0 for success, 1 if help is invoked, and 2 if the script fails.</span></span>

<span data-ttu-id="39e61-119">Spécifiez le chemin d’accès à une base de données Windows Installer qui doit être créée ou qui doit recevoir les tables importées.</span><span class="sxs-lookup"><span data-stu-id="39e61-119">Specify the path to a Windows installer database that is to be created or that is to receive the imported tables.</span></span> <span data-ttu-id="39e61-120">Spécifiez le chemin d’accès au dossier contenant les fichiers d’archive des tables en cours d’importation.</span><span class="sxs-lookup"><span data-stu-id="39e61-120">Specify the path to the folder containing the archive files of the tables that are being imported.</span></span> <span data-ttu-id="39e61-121">Répertoriez les noms des fichiers d’archive en cours d’importation.</span><span class="sxs-lookup"><span data-stu-id="39e61-121">List the names of the archive files that are being imported.</span></span> <span data-ttu-id="39e61-122">Les noms de fichiers génériques, tels que \* . IDT, peuvent être utilisés pour importer plusieurs fichiers.</span><span class="sxs-lookup"><span data-stu-id="39e61-122">Wildcard file names, such as \*.idt, can be used to import multiple files.</span></span>

<span data-ttu-id="39e61-123">Les options suivantes peuvent être spécifiées n’importe où sur la ligne de commande avant la liste des fichiers.</span><span class="sxs-lookup"><span data-stu-id="39e61-123">The following options may be specified anywhere on the command line before the file list.</span></span>



| <span data-ttu-id="39e61-124">Option</span><span class="sxs-lookup"><span data-stu-id="39e61-124">Option</span></span>              | <span data-ttu-id="39e61-125">Description</span><span class="sxs-lookup"><span data-stu-id="39e61-125">Description</span></span>                                                                                                                          |
|---------------------|--------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="39e61-126">aucune option spécifiée</span><span class="sxs-lookup"><span data-stu-id="39e61-126">no option specified</span></span> | <span data-ttu-id="39e61-127">Importez la liste des fichiers d’archive de table à partir du dossier spécifié dans la base de données Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="39e61-127">Import the list of table archive files from the specified folder into the Windows Installer database.</span></span>                                |
| <span data-ttu-id="39e61-128">/C</span><span class="sxs-lookup"><span data-stu-id="39e61-128">/c</span></span>                  | <span data-ttu-id="39e61-129">Créez un Windows Installer base de données, puis importez la liste des fichiers d’archive de table à partir du dossier spécifié dans la nouvelle base de données.</span><span class="sxs-lookup"><span data-stu-id="39e61-129">Create a Windows Installer database and then import the list of table archive files from the specified folder into the new database.</span></span> |



 

<span data-ttu-id="39e61-130">Pour plus d’informations, consultez [Windows Installer des exemples de scripts](windows-installer-scripting-examples.md) pour des exemples de scripts supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="39e61-130">For more information, see [Windows Installer Scripting Examples](windows-installer-scripting-examples.md) for additional scripting examples.</span></span> <span data-ttu-id="39e61-131">Pour obtenir des exemples d’utilitaires qui ne nécessitent pas Windows Script Host, consultez [Windows Installer les outils de développement](windows-installer-development-tools.md).</span><span class="sxs-lookup"><span data-stu-id="39e61-131">For sample utilities that do not require Windows Script Host, see [Windows Installer Development Tools](windows-installer-development-tools.md).</span></span>

<span data-ttu-id="39e61-132">Notez qu' [un exemple de localisation](a-localization-example.md) illustre également l' [importation de tables Error et ActionText localisées](importing-localized-error-and-actiontext-tables.md).</span><span class="sxs-lookup"><span data-stu-id="39e61-132">Note that [A Localization Example](a-localization-example.md) also demonstrates [Importing Localized Error and ActionText Tables](importing-localized-error-and-actiontext-tables.md).</span></span>

 

 



