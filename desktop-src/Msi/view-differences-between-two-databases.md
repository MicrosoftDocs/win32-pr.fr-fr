---
description: Le WiDiffDb.vbs de fichiers VBScript est fourni dans les composants SDK Windows pour les développeurs Windows Installer. Cet exemple de script génère un fichier de transformation temporaire entre deux Windows Installer bases de données et affiche la transformation.
ms.assetid: 9750ddc6-de8d-48e9-a984-892f0cf4ac3b
title: Afficher les différences entre deux bases de données
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b0c97afc0bd7145170209ed87497b6af90e64d6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525875"
---
# <a name="view-differences-between-two-databases"></a><span data-ttu-id="8adf7-104">Afficher les différences entre deux bases de données</span><span class="sxs-lookup"><span data-stu-id="8adf7-104">View Differences Between Two Databases</span></span>

<span data-ttu-id="8adf7-105">Le WiDiffDb.vbs de fichiers VBScript est fourni dans les [composants SDK Windows pour les développeurs Windows Installer](platform-sdk-components-for-windows-installer-developers.md).</span><span class="sxs-lookup"><span data-stu-id="8adf7-105">The VBScript file WiDiffDb.vbs is provided in the [Windows SDK Components for Windows Installer Developers](platform-sdk-components-for-windows-installer-developers.md).</span></span> <span data-ttu-id="8adf7-106">Cet exemple de script génère un fichier de transformation temporaire entre deux Windows Installer bases de données et affiche la transformation.</span><span class="sxs-lookup"><span data-stu-id="8adf7-106">This sample script generates a temporary transform file between two Windows Installer databases and displays the transform.</span></span>

<span data-ttu-id="8adf7-107">L’exemple illustre l’utilisation de :</span><span class="sxs-lookup"><span data-stu-id="8adf7-107">The sample demonstrates the use of:</span></span>

-   [<span data-ttu-id="8adf7-108">**OpenDatabase, méthode (objet installer)**</span><span class="sxs-lookup"><span data-stu-id="8adf7-108">**OpenDatabase method (Installer Object)**</span></span>](installer-opendatabase.md)
-   <span data-ttu-id="8adf7-109">[**Méthode LastErrorRecord**](installer-lasterrorrecord.md) de l' [ **objet installer**](installer-object.md)</span><span class="sxs-lookup"><span data-stu-id="8adf7-109">[**LastErrorRecord method**](installer-lasterrorrecord.md) of the [**Installer object**](installer-object.md)</span></span>
-   [<span data-ttu-id="8adf7-110">**OpenView, méthode**</span><span class="sxs-lookup"><span data-stu-id="8adf7-110">**OpenView method**</span></span>](database-openview.md)
-   [<span data-ttu-id="8adf7-111">**Propriété SummaryInformation (objet Database)**</span><span class="sxs-lookup"><span data-stu-id="8adf7-111">**SummaryInformation property (Database Object)**</span></span>](database-summaryinformation.md)
-   [<span data-ttu-id="8adf7-112">**GenerateTransform, méthode**</span><span class="sxs-lookup"><span data-stu-id="8adf7-112">**GenerateTransform method**</span></span>](database-generatetransform.md)
-   [<span data-ttu-id="8adf7-113">**Méthode ApplyTransform**</span><span class="sxs-lookup"><span data-stu-id="8adf7-113">**ApplyTransform method**</span></span>](database-applytransform.md)
-   [<span data-ttu-id="8adf7-114">**Objet de base de données**</span><span class="sxs-lookup"><span data-stu-id="8adf7-114">**Database object**</span></span>](database-object.md)
-   <span data-ttu-id="8adf7-115">[**Méthode fetch**](view-fetch.md) de l' [ **objet View**](view-object.md)</span><span class="sxs-lookup"><span data-stu-id="8adf7-115">[**Fetch method**](view-fetch.md) of the [**View object**](view-object.md)</span></span>
-   [<span data-ttu-id="8adf7-116">**IsNull, propriété**</span><span class="sxs-lookup"><span data-stu-id="8adf7-116">**IsNull property**</span></span>](record-isnull.md)
-   <span data-ttu-id="8adf7-117">[**Propriété StringData**](record-stringdata.md) de l' [ **objet record**](record-object.md)</span><span class="sxs-lookup"><span data-stu-id="8adf7-117">[**StringData property**](record-stringdata.md) of the [**Record object**](record-object.md)</span></span>
-   [<span data-ttu-id="8adf7-118">\_Table TransformView</span><span class="sxs-lookup"><span data-stu-id="8adf7-118">\_TransformView table</span></span>](-transformview-table.md)

<span data-ttu-id="8adf7-119">L’utilisation de cet exemple nécessite la version CScript.exe de Windows Script Host.</span><span class="sxs-lookup"><span data-stu-id="8adf7-119">Using this sample requires the CScript.exe version of Windows Script Host.</span></span> <span data-ttu-id="8adf7-120">Pour utiliser CScript.exe pour exécuter cet exemple, tapez une commande à l’invite de commandes en utilisant la syntaxe suivante.</span><span class="sxs-lookup"><span data-stu-id="8adf7-120">To use CScript.exe to run this sample, type a command at the command prompt using the following syntax.</span></span> <span data-ttu-id="8adf7-121">L’aide s’affiche si le premier argument est/ ?</span><span class="sxs-lookup"><span data-stu-id="8adf7-121">Help is displayed if the first argument is /?</span></span> <span data-ttu-id="8adf7-122">ou si le nombre d’arguments spécifié est insuffisant.</span><span class="sxs-lookup"><span data-stu-id="8adf7-122">or if too few arguments are specified.</span></span> <span data-ttu-id="8adf7-123">Pour rediriger la sortie vers un fichier, terminez la ligne de commande avec VBS > \[ *chemin d’accès au fichier* \] .</span><span class="sxs-lookup"><span data-stu-id="8adf7-123">To redirect the output to a file, end the command line with VBS > \[*path to file*\].</span></span> <span data-ttu-id="8adf7-124">L’exemple retourne la valeur 0 pour Success, 1 si l’aide est appelée, et 2 si le script échoue.</span><span class="sxs-lookup"><span data-stu-id="8adf7-124">The sample returns a value of 0 for success, 1 if help is invoked, and 2 if the script fails.</span></span>

<span data-ttu-id="8adf7-125">**cscript WiDiffDb.vbs** chemin d’accès *\[ au \] \[ chemin d’accès \] de la base* de données modifiée</span><span class="sxs-lookup"><span data-stu-id="8adf7-125">**cscript WiDiffDb.vbs** *\[path to original database\]\[path to revised database\]*</span></span>

<span data-ttu-id="8adf7-126">Spécifiez le chemin d’accès à la base de données d’Windows Installer d’origine.</span><span class="sxs-lookup"><span data-stu-id="8adf7-126">Specify the path to the original Windows Installer database.</span></span> <span data-ttu-id="8adf7-127">Spécifiez le chemin d’accès à la base de données modifiée.</span><span class="sxs-lookup"><span data-stu-id="8adf7-127">Specify the path to the revised database.</span></span> <span data-ttu-id="8adf7-128">L’exemple de script affiche la transformation.</span><span class="sxs-lookup"><span data-stu-id="8adf7-128">The sample script will display the transform.</span></span>

<span data-ttu-id="8adf7-129">Pour obtenir des exemples supplémentaires de scripts, consultez [Windows Installer des exemples de scripts](windows-installer-scripting-examples.md).</span><span class="sxs-lookup"><span data-stu-id="8adf7-129">For additional scripting examples, see [Windows Installer Scripting Examples](windows-installer-scripting-examples.md).</span></span> <span data-ttu-id="8adf7-130">Pour obtenir des exemples d’utilitaires qui ne nécessitent pas Windows Script Host, consultez [Windows Installer les outils de développement](windows-installer-development-tools.md).</span><span class="sxs-lookup"><span data-stu-id="8adf7-130">For sample utilities that do not require Windows Script Host, see [Windows Installer Development Tools](windows-installer-development-tools.md).</span></span>

 

 



