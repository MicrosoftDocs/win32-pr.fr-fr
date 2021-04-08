---
description: Le WiUseXfm.vbs de fichiers VBScript est fourni dans les composants SDK Windows pour les développeurs Windows Installer. Cet exemple montre comment le script peut être utilisé pour appliquer une transformation à une base de données Windows Installer.
ms.assetid: e647388e-5211-463d-9e3e-b502af01fc0c
title: Appliquer une transformation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f9e86acc495fc2a0bb8dff562832e58d29483256
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103864486"
---
# <a name="apply-a-transform"></a><span data-ttu-id="30104-104">Appliquer une transformation</span><span class="sxs-lookup"><span data-stu-id="30104-104">Apply a Transform</span></span>

<span data-ttu-id="30104-105">Le WiUseXfm.vbs de fichiers VBScript est fourni dans les [composants SDK Windows pour les développeurs Windows Installer](platform-sdk-components-for-windows-installer-developers.md).</span><span class="sxs-lookup"><span data-stu-id="30104-105">The VBScript file WiUseXfm.vbs is provided in the [Windows SDK Components for Windows Installer Developers](platform-sdk-components-for-windows-installer-developers.md).</span></span> <span data-ttu-id="30104-106">Cet exemple montre comment le script peut être utilisé pour appliquer une transformation à une base de données Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="30104-106">This sample shows how script can be used to apply a transform to a Windows Installer database.</span></span>

<span data-ttu-id="30104-107">L’exemple illustre l’utilisation de</span><span class="sxs-lookup"><span data-stu-id="30104-107">The sample demonstrates the use of</span></span>

-   [<span data-ttu-id="30104-108">**OpenDatabase, méthode (objet installer)**</span><span class="sxs-lookup"><span data-stu-id="30104-108">**OpenDatabase method (Installer Object)**</span></span>](installer-opendatabase.md)
-   <span data-ttu-id="30104-109">[**Méthode LastErrorRecord**](installer-lasterrorrecord.md) de l' [ **objet installer**](installer-object.md)</span><span class="sxs-lookup"><span data-stu-id="30104-109">[**LastErrorRecord method**](installer-lasterrorrecord.md) of the [**Installer object**](installer-object.md)</span></span>
-   [<span data-ttu-id="30104-110">**Méthode ApplyTransform**</span><span class="sxs-lookup"><span data-stu-id="30104-110">**ApplyTransform method**</span></span>](database-applytransform.md)
-   <span data-ttu-id="30104-111">[**Méthode Commit**](database-commit.md) de l' [ **objet Database**](database-object.md)</span><span class="sxs-lookup"><span data-stu-id="30104-111">[**Commit method**](database-commit.md) of the [**Database object**](database-object.md)</span></span>

<span data-ttu-id="30104-112">Vous aurez besoin de la version CScript.exe ou WScript.exe de Windows Script Host pour utiliser cet exemple.</span><span class="sxs-lookup"><span data-stu-id="30104-112">You'll require the CScript.exe or WScript.exe version of Windows Script Host to use this sample.</span></span> <span data-ttu-id="30104-113">Pour utiliser CScript.exe pour exécuter cet exemple, tapez une ligne de commande à l’invite de commandes en utilisant la syntaxe suivante.</span><span class="sxs-lookup"><span data-stu-id="30104-113">To use CScript.exe to run this sample, type a command line at the command prompt using the following syntax.</span></span> <span data-ttu-id="30104-114">L’aide s’affiche si le premier argument est/ ?</span><span class="sxs-lookup"><span data-stu-id="30104-114">Help is displayed if the first argument is /?</span></span> <span data-ttu-id="30104-115">ou si le nombre d’arguments spécifié est insuffisant.</span><span class="sxs-lookup"><span data-stu-id="30104-115">or if too few arguments are specified.</span></span> <span data-ttu-id="30104-116">Pour rediriger la sortie vers un fichier, terminez la ligne de commande avec VBS > \[ *chemin d’accès au fichier* \] .</span><span class="sxs-lookup"><span data-stu-id="30104-116">To redirect the output to a file, end the command line with VBS > \[*path to file*\].</span></span> <span data-ttu-id="30104-117">L’exemple retourne la valeur 0 pour Success, 1 si l’aide est appelée, et 2 si le script échoue.</span><span class="sxs-lookup"><span data-stu-id="30104-117">The sample returns a value of 0 for success, 1 if help is invoked, and 2 if the script fails.</span></span>

<span data-ttu-id="30104-118">**cscript WiUseXfm.vbs \[ chemin d’accès au chemin d’accès de la base de données d’origine \] \[ pour transformer les \] \[ Options du fichier\]**</span><span class="sxs-lookup"><span data-stu-id="30104-118">**cscript WiUseXfm.vbs \[path to original database\]\[path to transform file\]\[options\]**</span></span>

<span data-ttu-id="30104-119">Spécifiez le chemin d’accès à la base de données Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="30104-119">Specify the path to the Windows Installer database.</span></span> <span data-ttu-id="30104-120">Spécifiez le chemin d’accès au fichier de transformation.</span><span class="sxs-lookup"><span data-stu-id="30104-120">Specify the path to the transform file.</span></span> <span data-ttu-id="30104-121">Si le chemin d’accès au fichier de transformation est omis, les deux bases de données sont comparées uniquement.</span><span class="sxs-lookup"><span data-stu-id="30104-121">If the path to the transform file is omitted, the two databases are only compared.</span></span> <span data-ttu-id="30104-122">Le troisième argument est une valeur numérique facultative qui spécifie un jeu de conditions d’erreur qui doivent être supprimées.</span><span class="sxs-lookup"><span data-stu-id="30104-122">The third argument is an optional numeric value that specifies a set of error conditions that are to be suppressed.</span></span> <span data-ttu-id="30104-123">Ajoutez ces valeurs ensemble pour supprimer plusieurs conditions.</span><span class="sxs-lookup"><span data-stu-id="30104-123">Add these values together to suppress multiple conditions.</span></span>



| <span data-ttu-id="30104-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="30104-124">Value</span></span> | <span data-ttu-id="30104-125">Condition d’erreur à supprimer</span><span class="sxs-lookup"><span data-stu-id="30104-125">Error condition to suppress</span></span>                   |
|-------|-----------------------------------------------|
| <span data-ttu-id="30104-126">1</span><span class="sxs-lookup"><span data-stu-id="30104-126">1</span></span>     | <span data-ttu-id="30104-127">Ajout d’une ligne qui existe déjà.</span><span class="sxs-lookup"><span data-stu-id="30104-127">Adding a row that already exists.</span></span>             |
| <span data-ttu-id="30104-128">2</span><span class="sxs-lookup"><span data-stu-id="30104-128">2</span></span>     | <span data-ttu-id="30104-129">Suppression d’une ligne qui n’existe pas.</span><span class="sxs-lookup"><span data-stu-id="30104-129">Deleting a row that does not exist.</span></span>           |
| <span data-ttu-id="30104-130">4</span><span class="sxs-lookup"><span data-stu-id="30104-130">4</span></span>     | <span data-ttu-id="30104-131">Ajout d’une table qui existe déjà.</span><span class="sxs-lookup"><span data-stu-id="30104-131">Adding a table that already exists.</span></span>           |
| <span data-ttu-id="30104-132">8</span><span class="sxs-lookup"><span data-stu-id="30104-132">8</span></span>     | <span data-ttu-id="30104-133">Suppression d’une table qui n’existe pas.</span><span class="sxs-lookup"><span data-stu-id="30104-133">Deleting a table that does not exist.</span></span>         |
| <span data-ttu-id="30104-134">16</span><span class="sxs-lookup"><span data-stu-id="30104-134">16</span></span>    | <span data-ttu-id="30104-135">Mise à jour d’une ligne qui n’existe pas.</span><span class="sxs-lookup"><span data-stu-id="30104-135">Updating a row that does not exist.</span></span>           |
| <span data-ttu-id="30104-136">256</span><span class="sxs-lookup"><span data-stu-id="30104-136">256</span></span>   | <span data-ttu-id="30104-137">Incompatibilité de la base de données et transformation de pages.</span><span class="sxs-lookup"><span data-stu-id="30104-137">Mismatch of database and transform codepages.</span></span> |



 

<span data-ttu-id="30104-138">Pour obtenir des exemples supplémentaires de scripts, consultez [Windows Installer des exemples de scripts](windows-installer-scripting-examples.md).</span><span class="sxs-lookup"><span data-stu-id="30104-138">For additional scripting examples, see [Windows Installer Scripting Examples](windows-installer-scripting-examples.md).</span></span> <span data-ttu-id="30104-139">Pour obtenir des exemples d’utilitaires qui ne nécessitent pas Windows Script Host, consultez [Windows Installer les outils de développement](windows-installer-development-tools.md).</span><span class="sxs-lookup"><span data-stu-id="30104-139">For sample utilities that do not require Windows Script Host, see [Windows Installer Development Tools](windows-installer-development-tools.md).</span></span>

 

 



