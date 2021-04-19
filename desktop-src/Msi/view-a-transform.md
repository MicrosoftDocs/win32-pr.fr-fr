---
description: Le WiLstXfm.vbs de fichiers VBScript est fourni dans les composants SDK Windows pour les développeurs Windows Installer. Cet exemple de script peut être utilisé pour afficher un fichier de transformation.
ms.assetid: c2e3dd56-b0e5-481a-b7b8-5000fa686850
title: Afficher une transformation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 69f4a858f8deb115de967da3b4d485b596f85cee
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106515634"
---
# <a name="view-a-transform"></a><span data-ttu-id="7fc9d-104">Afficher une transformation</span><span class="sxs-lookup"><span data-stu-id="7fc9d-104">View a Transform</span></span>

<span data-ttu-id="7fc9d-105">Le WiLstXfm.vbs de fichiers VBScript est fourni dans les [composants SDK Windows pour les développeurs Windows Installer](platform-sdk-components-for-windows-installer-developers.md).</span><span class="sxs-lookup"><span data-stu-id="7fc9d-105">The VBScript file WiLstXfm.vbs is provided in the [Windows SDK Components for Windows Installer Developers](platform-sdk-components-for-windows-installer-developers.md).</span></span> <span data-ttu-id="7fc9d-106">Cet exemple de script peut être utilisé pour afficher un fichier de transformation.</span><span class="sxs-lookup"><span data-stu-id="7fc9d-106">This script sample can be used to view a transform file.</span></span>

<span data-ttu-id="7fc9d-107">L’exemple illustre l’utilisation de :</span><span class="sxs-lookup"><span data-stu-id="7fc9d-107">The sample demonstrates the use of:</span></span>

-   [<span data-ttu-id="7fc9d-108">\_Table TransformView</span><span class="sxs-lookup"><span data-stu-id="7fc9d-108">\_TransformView table</span></span>](-transformview-table.md)
-   [<span data-ttu-id="7fc9d-109">**OpenDatabase, méthode (objet installer)**</span><span class="sxs-lookup"><span data-stu-id="7fc9d-109">**OpenDatabase method (Installer Object)**</span></span>](installer-opendatabase.md)
-   <span data-ttu-id="7fc9d-110">[**Méthode LastErrorRecord**](installer-lasterrorrecord.md) de l' [ **objet installer**](installer-object.md)</span><span class="sxs-lookup"><span data-stu-id="7fc9d-110">[**LastErrorRecord method**](installer-lasterrorrecord.md) of the [**Installer object**](installer-object.md)</span></span>
-   [<span data-ttu-id="7fc9d-111">**Méthode ApplyTransform**</span><span class="sxs-lookup"><span data-stu-id="7fc9d-111">**ApplyTransform method**</span></span>](database-applytransform.md)
-   [<span data-ttu-id="7fc9d-112">**OpenView, méthode**</span><span class="sxs-lookup"><span data-stu-id="7fc9d-112">**OpenView method**</span></span>](database-openview.md)
-   <span data-ttu-id="7fc9d-113">[**Méthode Commit**](database-commit.md) de l' [ **objet Database**](database-object.md)</span><span class="sxs-lookup"><span data-stu-id="7fc9d-113">[**Commit method**](database-commit.md) of the [**Database object**](database-object.md)</span></span>
-   [<span data-ttu-id="7fc9d-114">**IsNull, propriété**</span><span class="sxs-lookup"><span data-stu-id="7fc9d-114">**IsNull property**</span></span>](record-isnull.md)
-   <span data-ttu-id="7fc9d-115">[**Propriété StringData**](record-stringdata.md) de l' [ **objet record**](record-object.md)</span><span class="sxs-lookup"><span data-stu-id="7fc9d-115">[**StringData property**](record-stringdata.md) of the [**Record object**](record-object.md)</span></span>

<span data-ttu-id="7fc9d-116">L’utilisation de cet exemple nécessite la version CScript.exe de Windows Script Host.</span><span class="sxs-lookup"><span data-stu-id="7fc9d-116">Using this sample requires the CScript.exe version of Windows Script Host.</span></span> <span data-ttu-id="7fc9d-117">Pour utiliser CScript.exe pour exécuter cet exemple, tapez une commande à l’invite de commandes en utilisant la syntaxe suivante.</span><span class="sxs-lookup"><span data-stu-id="7fc9d-117">To use CScript.exe to run this sample, type a command at the command prompt using the following syntax.</span></span> <span data-ttu-id="7fc9d-118">L’aide s’affiche si le premier argument est/ ?</span><span class="sxs-lookup"><span data-stu-id="7fc9d-118">Help is displayed if the first argument is /?</span></span> <span data-ttu-id="7fc9d-119">ou si le nombre d’arguments spécifié est insuffisant.</span><span class="sxs-lookup"><span data-stu-id="7fc9d-119">or if too few arguments are specified.</span></span> <span data-ttu-id="7fc9d-120">Pour rediriger la sortie vers un fichier, terminez la ligne de commande avec VBS > \[ *chemin d’accès au fichier* \] .</span><span class="sxs-lookup"><span data-stu-id="7fc9d-120">To redirect the output to a file, end the command line with VBS > \[*path to file*\].</span></span> <span data-ttu-id="7fc9d-121">L’exemple retourne la valeur 0 pour Success, 1 si l’aide est appelée, et 2 si le script échoue.</span><span class="sxs-lookup"><span data-stu-id="7fc9d-121">The sample returns a value of 0 for success, 1 if help is invoked, and 2 if the script fails.</span></span>

<span data-ttu-id="7fc9d-122">**cscript WiLstXfm.vbs** chemin d’accès de l' *\[ option de base de données de référence à \] \[ \] \[ transformer à afficher \]*</span><span class="sxs-lookup"><span data-stu-id="7fc9d-122">**cscript WiLstXfm.vbs** *\[path to reference database\]\[option\]\[path to transform to be viewed\]*</span></span>

<span data-ttu-id="7fc9d-123">Spécifiez le chemin d’accès à la base de données de référence Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="7fc9d-123">Specify the path to the reference Windows Installer database.</span></span> <span data-ttu-id="7fc9d-124">Spécifiez une liste de chemins d’accès pour transformer les fichiers en cours d’affichage.</span><span class="sxs-lookup"><span data-stu-id="7fc9d-124">Specify a list of paths to transform files that are being viewed.</span></span> <span data-ttu-id="7fc9d-125">Chaque chemin d’accès dans la liste peut être précédé d’une valeur numérique facultative.</span><span class="sxs-lookup"><span data-stu-id="7fc9d-125">Each path in the list may by preceded by an optional numeric value.</span></span> <span data-ttu-id="7fc9d-126">Cette valeur spécifie un ensemble de conditions d’erreur qui doivent être supprimées.</span><span class="sxs-lookup"><span data-stu-id="7fc9d-126">This value specifies a set of error conditions that are to be suppressed.</span></span> <span data-ttu-id="7fc9d-127">Vous pouvez ajouter ces valeurs ensemble pour supprimer plusieurs conditions.</span><span class="sxs-lookup"><span data-stu-id="7fc9d-127">You may add these values together to suppress multiple conditions.</span></span> <span data-ttu-id="7fc9d-128">Si aucune option numérique n’est spécifiée, toutes les conditions d’erreur sont supprimées.</span><span class="sxs-lookup"><span data-stu-id="7fc9d-128">If no numeric option is specified, all the error conditions are suppressed.</span></span> <span data-ttu-id="7fc9d-129">Les arguments de cette liste sont exécutés dans l’ordre de gauche à droite dans lequel ils apparaissent sur la ligne de commande.</span><span class="sxs-lookup"><span data-stu-id="7fc9d-129">The arguments in this list are executed in the left-to-right order in which they appear on the command line.</span></span>



| <span data-ttu-id="7fc9d-130">Valeur</span><span class="sxs-lookup"><span data-stu-id="7fc9d-130">Value</span></span> | <span data-ttu-id="7fc9d-131">Condition d’erreur à supprimer</span><span class="sxs-lookup"><span data-stu-id="7fc9d-131">Error condition to suppress</span></span>                   |
|-------|-----------------------------------------------|
| <span data-ttu-id="7fc9d-132">1</span><span class="sxs-lookup"><span data-stu-id="7fc9d-132">1</span></span>     | <span data-ttu-id="7fc9d-133">Ajout d’une ligne qui existe déjà.</span><span class="sxs-lookup"><span data-stu-id="7fc9d-133">Adding a row that already exists.</span></span>             |
| <span data-ttu-id="7fc9d-134">2</span><span class="sxs-lookup"><span data-stu-id="7fc9d-134">2</span></span>     | <span data-ttu-id="7fc9d-135">Suppression d’une ligne qui n’existe pas.</span><span class="sxs-lookup"><span data-stu-id="7fc9d-135">Deleting a row that does not exist.</span></span>           |
| <span data-ttu-id="7fc9d-136">4</span><span class="sxs-lookup"><span data-stu-id="7fc9d-136">4</span></span>     | <span data-ttu-id="7fc9d-137">Ajout d’une table qui existe déjà.</span><span class="sxs-lookup"><span data-stu-id="7fc9d-137">Adding a table that already exists.</span></span>           |
| <span data-ttu-id="7fc9d-138">8</span><span class="sxs-lookup"><span data-stu-id="7fc9d-138">8</span></span>     | <span data-ttu-id="7fc9d-139">Suppression d’une table qui n’existe pas.</span><span class="sxs-lookup"><span data-stu-id="7fc9d-139">Deleting a table that does not exist.</span></span>         |
| <span data-ttu-id="7fc9d-140">16</span><span class="sxs-lookup"><span data-stu-id="7fc9d-140">16</span></span>    | <span data-ttu-id="7fc9d-141">Mise à jour d’une ligne qui n’existe pas.</span><span class="sxs-lookup"><span data-stu-id="7fc9d-141">Updating a row that does not exist.</span></span>           |
| <span data-ttu-id="7fc9d-142">256</span><span class="sxs-lookup"><span data-stu-id="7fc9d-142">256</span></span>   | <span data-ttu-id="7fc9d-143">Incompatibilité de la base de données et transformation de pages.</span><span class="sxs-lookup"><span data-stu-id="7fc9d-143">Mismatch of database and transform codepages.</span></span> |



 

<span data-ttu-id="7fc9d-144">Pour obtenir des exemples supplémentaires de scripts, consultez [Windows Installer des exemples de scripts](windows-installer-scripting-examples.md).</span><span class="sxs-lookup"><span data-stu-id="7fc9d-144">For additional scripting examples, see [Windows Installer Scripting Examples](windows-installer-scripting-examples.md).</span></span> <span data-ttu-id="7fc9d-145">Pour obtenir des exemples d’utilitaires qui ne nécessitent pas Windows Script Host, consultez [Windows Installer les outils de développement](windows-installer-development-tools.md).</span><span class="sxs-lookup"><span data-stu-id="7fc9d-145">For sample utilities that do not require Windows Script Host, see [Windows Installer Development Tools](windows-installer-development-tools.md).</span></span>

 

 



