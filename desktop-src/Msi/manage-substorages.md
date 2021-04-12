---
description: Le WiSubStg.vbs de fichiers VBScript est fourni dans les composants SDK Windows pour les développeurs Windows Installer.
ms.assetid: a0248dfb-e406-4ce6-ab11-1e428aa67af4
title: Gérer les sous-stockages
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 01876efdb85bdc89df1b4d64332d44674e5e860e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104320566"
---
# <a name="manage-substorages"></a><span data-ttu-id="a2792-103">Gérer les sous-stockages</span><span class="sxs-lookup"><span data-stu-id="a2792-103">Manage Substorages</span></span>

<span data-ttu-id="a2792-104">Le WiSubStg.vbs de fichiers VBScript est fourni dans les [composants SDK Windows pour les développeurs Windows Installer](platform-sdk-components-for-windows-installer-developers.md).</span><span class="sxs-lookup"><span data-stu-id="a2792-104">The VBScript file WiSubStg.vbs is provided in the [Windows SDK Components for Windows Installer Developers](platform-sdk-components-for-windows-installer-developers.md).</span></span> <span data-ttu-id="a2792-105">Cet exemple montre comment le script peut être utilisé pour gérer les sous-stockages dans une base de données Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="a2792-105">This sample shows how script can be used to manage substorages in a Windows Installer database.</span></span> <span data-ttu-id="a2792-106">Une transformation peut être ajoutée à une base de données Windows Installer existante en tant que sous-stockage.</span><span class="sxs-lookup"><span data-stu-id="a2792-106">A transform can be added to an existing Windows Installer database as a substorage.</span></span>

<span data-ttu-id="a2792-107">L’exemple illustre l’utilisation de :</span><span class="sxs-lookup"><span data-stu-id="a2792-107">The sample demonstrates the use of:</span></span>

-   [<span data-ttu-id="a2792-108">\_Table de stockage</span><span class="sxs-lookup"><span data-stu-id="a2792-108">\_Storages table</span></span>](-storages-table.md)
-   [<span data-ttu-id="a2792-109">**OpenDatabase, méthode (objet installer)**</span><span class="sxs-lookup"><span data-stu-id="a2792-109">**OpenDatabase method (Installer Object)**</span></span>](installer-opendatabase.md)
-   [<span data-ttu-id="a2792-110">**Méthode CreateRecord**</span><span class="sxs-lookup"><span data-stu-id="a2792-110">**CreateRecord method**</span></span>](installer-createrecord.md)
-   <span data-ttu-id="a2792-111">[**Méthode LastErrorRecord**](installer-lasterrorrecord.md) de l' [ **objet installer**](installer-object.md)</span><span class="sxs-lookup"><span data-stu-id="a2792-111">[**LastErrorRecord method**](installer-lasterrorrecord.md) of the [**Installer object**](installer-object.md)</span></span>
-   [<span data-ttu-id="a2792-112">**OpenView, méthode**</span><span class="sxs-lookup"><span data-stu-id="a2792-112">**OpenView method**</span></span>](database-openview.md)
-   <span data-ttu-id="a2792-113">[**Méthode Commit**](database-commit.md) de l' [ **objet Database**](database-object.md)</span><span class="sxs-lookup"><span data-stu-id="a2792-113">[**Commit method**](database-commit.md) of the [**Database object**](database-object.md)</span></span>
-   [<span data-ttu-id="a2792-114">**Méthode fetch**</span><span class="sxs-lookup"><span data-stu-id="a2792-114">**Fetch method**</span></span>](view-fetch.md)
-   [<span data-ttu-id="a2792-115">**Modify, méthode**</span><span class="sxs-lookup"><span data-stu-id="a2792-115">**Modify method**</span></span>](view-modify.md)
-   <span data-ttu-id="a2792-116">[**Méthode Execute**](view-execute.md) de l' [ **objet View**](view-object.md)</span><span class="sxs-lookup"><span data-stu-id="a2792-116">[**Execute method**](view-execute.md) of the [**View object**](view-object.md)</span></span>
-   [<span data-ttu-id="a2792-117">**StringData, propriété**</span><span class="sxs-lookup"><span data-stu-id="a2792-117">**StringData property**</span></span>](record-stringdata.md)
-   <span data-ttu-id="a2792-118">[**Méthode SetStream**](record-setstream.md) de l' [ **objet record**](record-object.md)</span><span class="sxs-lookup"><span data-stu-id="a2792-118">[**SetStream method**](record-setstream.md) of the [**Record object**](record-object.md)</span></span>

<span data-ttu-id="a2792-119">Vous aurez besoin de la version CScript.exe ou WScript.exe de Windows Script Host pour utiliser cet exemple.</span><span class="sxs-lookup"><span data-stu-id="a2792-119">You'll require the CScript.exe or WScript.exe version of Windows Script Host to use this sample.</span></span> <span data-ttu-id="a2792-120">Pour utiliser CScript.exe pour exécuter cet exemple, tapez une ligne de commande à l’invite de commandes en utilisant la syntaxe suivante.</span><span class="sxs-lookup"><span data-stu-id="a2792-120">To use CScript.exe to run this sample, type a command line at the command prompt using the following syntax.</span></span> <span data-ttu-id="a2792-121">L’aide s’affiche si le premier argument est/ ?</span><span class="sxs-lookup"><span data-stu-id="a2792-121">Help is displayed if the first argument is /?</span></span> <span data-ttu-id="a2792-122">ou si le nombre d’arguments spécifié est insuffisant.</span><span class="sxs-lookup"><span data-stu-id="a2792-122">or if too few arguments are specified.</span></span> <span data-ttu-id="a2792-123">Pour rediriger la sortie vers un fichier, terminez la ligne de commande avec VBS > \[ *chemin d’accès au fichier* \] .</span><span class="sxs-lookup"><span data-stu-id="a2792-123">To redirect the output to a file, end the command line with VBS > \[*path to file*\].</span></span> <span data-ttu-id="a2792-124">L’exemple retourne la valeur 0 pour Success, 1 si l’aide est appelée, et 2 si le script échoue.</span><span class="sxs-lookup"><span data-stu-id="a2792-124">The sample returns a value of 0 for success, 1 if help is invoked, and 2 if the script fails.</span></span>

<span data-ttu-id="a2792-125">**cscript WiSubStg.vbs \[ chemin du chemin de la base de données \] \[ vers les options de fichier \] \[ \] \[ nom du sous-stockage\]**</span><span class="sxs-lookup"><span data-stu-id="a2792-125">**cscript WiSubStg.vbs \[path to database\]\[path to file\]\[options\]\[substorage name\]**</span></span>

<span data-ttu-id="a2792-126">Spécifiez le chemin d’accès à la base de données Windows Installer pour ajouter ou supprimer le sous-stockage.</span><span class="sxs-lookup"><span data-stu-id="a2792-126">Specify the path to the Windows Installer database to add or remove substorage.</span></span> <span data-ttu-id="a2792-127">Spécifiez un chemin d’accès à la transformation ou au fichier de base de données qui est ajouté en tant que sous-stockage.</span><span class="sxs-lookup"><span data-stu-id="a2792-127">Specify a path to the transform or database file that is being added as substorage.</span></span> <span data-ttu-id="a2792-128">Pour répertorier les sous-stockages de la base de données Windows Installer, omettez le chemin d’accès à ce fichier.</span><span class="sxs-lookup"><span data-stu-id="a2792-128">To list the substorages in the Windows Installer database, omit the path to this file.</span></span> <span data-ttu-id="a2792-129">Vous pouvez spécifier un nom de sous-stockage facultatif. Si cette valeur est omise, le nom du sous-stockage est par défaut le nom du fichier.</span><span class="sxs-lookup"><span data-stu-id="a2792-129">You may specify an optional substorage name, if this is omitted the substorage name defaults to the file name.</span></span>

<span data-ttu-id="a2792-130">L’option suivante peut être spécifiée.</span><span class="sxs-lookup"><span data-stu-id="a2792-130">The following option may be specified.</span></span>



| <span data-ttu-id="a2792-131">Option</span><span class="sxs-lookup"><span data-stu-id="a2792-131">Option</span></span>              | <span data-ttu-id="a2792-132">Description</span><span class="sxs-lookup"><span data-stu-id="a2792-132">Description</span></span>                                                                                         |
|---------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a2792-133">aucune option spécifiée</span><span class="sxs-lookup"><span data-stu-id="a2792-133">no option specified</span></span> | <span data-ttu-id="a2792-134">Ajoutez un sous-stockage à la base de données Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="a2792-134">Add a substorage to the Windows Installer database.</span></span>                                                 |
| <span data-ttu-id="a2792-135">/d</span><span class="sxs-lookup"><span data-stu-id="a2792-135">/d</span></span>                  | <span data-ttu-id="a2792-136">Supprimer un sous-stockage.</span><span class="sxs-lookup"><span data-stu-id="a2792-136">Remove a substorage.</span></span> <span data-ttu-id="a2792-137">Cet indicateur d’option doit être suivi du nom du sous-stockage à supprimer.</span><span class="sxs-lookup"><span data-stu-id="a2792-137">This option flag must be followed by the name of the substorage to be removed.</span></span> |



 

<span data-ttu-id="a2792-138">Pour obtenir des exemples supplémentaires de scripts, consultez [Windows Installer des exemples de scripts](windows-installer-scripting-examples.md).</span><span class="sxs-lookup"><span data-stu-id="a2792-138">For additional scripting examples, see [Windows Installer Scripting Examples](windows-installer-scripting-examples.md).</span></span> <span data-ttu-id="a2792-139">Pour obtenir des exemples d’utilitaires qui ne nécessitent pas Windows Script Host, consultez [Windows Installer les outils de développement](windows-installer-development-tools.md).</span><span class="sxs-lookup"><span data-stu-id="a2792-139">For sample utilities that do not require Windows Script Host, see [Windows Installer Development Tools](windows-installer-development-tools.md).</span></span>

<span data-ttu-id="a2792-140">Notez qu' [un exemple de localisation](a-localization-example.md) illustre l' [incorporation de transformations de personnalisation en tant que sous-stockage](embedding-customization-transforms-as-substorage.md).</span><span class="sxs-lookup"><span data-stu-id="a2792-140">Note that [A Localization Example](a-localization-example.md) demonstrates [Embedding Customization Transforms as Substorage](embedding-customization-transforms-as-substorage.md).</span></span>

 

 



