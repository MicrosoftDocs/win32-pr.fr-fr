---
description: Le WiGenXfm.vbs de fichiers VBScript est fourni dans les composants SDK Windows pour les développeurs Windows Installer. Cet exemple de script peut générer une transformation de deux bases de données Windows Installer. Pour plus d’informations, consultez transformations de base de données.
ms.assetid: bfa918b8-8d90-4e14-8a06-6c3d5b5dc13b
title: Générer une transformation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 92617c2e007b9deb01685679d4940095285b8218
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103757642"
---
# <a name="generate-a-transform"></a><span data-ttu-id="3871b-105">Générer une transformation</span><span class="sxs-lookup"><span data-stu-id="3871b-105">Generate a Transform</span></span>

<span data-ttu-id="3871b-106">Le WiGenXfm.vbs de fichiers VBScript est fourni dans les [composants SDK Windows pour les développeurs Windows Installer](platform-sdk-components-for-windows-installer-developers.md).</span><span class="sxs-lookup"><span data-stu-id="3871b-106">The VBScript file WiGenXfm.vbs is provided in the [Windows SDK Components for Windows Installer Developers](platform-sdk-components-for-windows-installer-developers.md).</span></span> <span data-ttu-id="3871b-107">Cet exemple de script peut générer une transformation de deux bases de données Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="3871b-107">This sample script can generate a transform from two Windows Installer databases.</span></span> <span data-ttu-id="3871b-108">Pour plus d’informations, consultez [transformations de base de données](database-transforms.md).</span><span class="sxs-lookup"><span data-stu-id="3871b-108">For more information see [Database Transforms](database-transforms.md).</span></span>

<span data-ttu-id="3871b-109">L’exemple illustre l’utilisation de :</span><span class="sxs-lookup"><span data-stu-id="3871b-109">The sample demonstrates the use of:</span></span>

[<span data-ttu-id="3871b-110">**OpenDatabase, méthode (objet installer)**</span><span class="sxs-lookup"><span data-stu-id="3871b-110">**OpenDatabase method (Installer Object)**</span></span>](installer-opendatabase.md)

<span data-ttu-id="3871b-111">[**Méthode LastErrorRecord**](installer-lasterrorrecord.md) de l' [ **objet installer**](installer-object.md)</span><span class="sxs-lookup"><span data-stu-id="3871b-111">[**LastErrorRecord method**](installer-lasterrorrecord.md) of the [**Installer object**](installer-object.md)</span></span>

<span data-ttu-id="3871b-112">[**Méthode GenerateTransform**](database-generatetransform.md) de l' [ **objet de base de données**](database-object.md)</span><span class="sxs-lookup"><span data-stu-id="3871b-112">[**GenerateTransform method**](database-generatetransform.md) of the [**Database object**](database-object.md)</span></span>

<span data-ttu-id="3871b-113">Vous aurez besoin de la version CScript.exe ou WScript.exe de Windows Script Host pour utiliser cet exemple.</span><span class="sxs-lookup"><span data-stu-id="3871b-113">You'll require the CScript.exe or WScript.exe version of Windows Script Host to use this sample.</span></span> <span data-ttu-id="3871b-114">Pour utiliser CScript.exe pour exécuter cet exemple, tapez une ligne de commande à l’invite de commandes en utilisant la syntaxe suivante.</span><span class="sxs-lookup"><span data-stu-id="3871b-114">To use CScript.exe to run this sample, type a command line at the command prompt using the following syntax.</span></span> <span data-ttu-id="3871b-115">L’aide s’affiche si le premier argument est/ ?</span><span class="sxs-lookup"><span data-stu-id="3871b-115">Help is displayed if the first argument is /?</span></span> <span data-ttu-id="3871b-116">ou si le nombre d’arguments spécifié est insuffisant.</span><span class="sxs-lookup"><span data-stu-id="3871b-116">or if too few arguments are specified.</span></span> <span data-ttu-id="3871b-117">Pour rediriger la sortie vers un fichier, terminez la ligne de commande avec VBS > \[ *chemin d’accès au fichier* \] .</span><span class="sxs-lookup"><span data-stu-id="3871b-117">To redirect the output to a file, end the command line with VBS > \[*path to file*\].</span></span> <span data-ttu-id="3871b-118">L’exemple retourne la valeur 0 pour Success, 1 si l’aide est appelée, et 2 si le script échoue.</span><span class="sxs-lookup"><span data-stu-id="3871b-118">The sample returns a value of 0 for success, 1 if help is invoked, and 2 if the script fails.</span></span>

<span data-ttu-id="3871b-119">**cscript WiGenXfm.vbs chemin du chemin de la base de données d’origine vers le chemin \[ \] \[ de la base de données modifiée \] \[ pour transformer le fichier\]**</span><span class="sxs-lookup"><span data-stu-id="3871b-119">**cscript WiGenXfm.vbs \[path to original database\]\[path to revised database\]\[path to transform file\]**</span></span>

<span data-ttu-id="3871b-120">Spécifiez le chemin d’accès à la base de données d’Windows Installer d’origine.</span><span class="sxs-lookup"><span data-stu-id="3871b-120">Specify the path to the original Windows Installer database.</span></span> <span data-ttu-id="3871b-121">Spécifiez le chemin d’accès à la base de données modifiée.</span><span class="sxs-lookup"><span data-stu-id="3871b-121">Specify the path to the revised database.</span></span> <span data-ttu-id="3871b-122">Spécifiez le chemin d’accès au fichier de transformation à créer.</span><span class="sxs-lookup"><span data-stu-id="3871b-122">Specify the path to the transform file to be created.</span></span> <span data-ttu-id="3871b-123">Si le chemin d’accès au fichier de transformation est omis, les deux bases de données sont comparées uniquement.</span><span class="sxs-lookup"><span data-stu-id="3871b-123">If the path to the transform file is omitted, the two databases are only compared.</span></span>

<span data-ttu-id="3871b-124">Pour obtenir des exemples supplémentaires de scripts, consultez [Windows Installer des exemples de scripts](windows-installer-scripting-examples.md).</span><span class="sxs-lookup"><span data-stu-id="3871b-124">For additional scripting examples, see [Windows Installer Scripting Examples](windows-installer-scripting-examples.md).</span></span> <span data-ttu-id="3871b-125">Pour obtenir des exemples d’utilitaires qui ne nécessitent pas Windows Script Host, consultez [Windows Installer les outils de développement](windows-installer-development-tools.md).</span><span class="sxs-lookup"><span data-stu-id="3871b-125">For sample utilities that do not require Windows Script Host, see [Windows Installer Development Tools](windows-installer-development-tools.md).</span></span>

<span data-ttu-id="3871b-126">Notez qu' [un exemple de localisation](a-localization-example.md) illustre la [génération d’une transformation de personnalisation](generating-a-customization-transform.md).</span><span class="sxs-lookup"><span data-stu-id="3871b-126">Note that [A Localization Example](a-localization-example.md) demonstrates [Generating a Customization Transform](generating-a-customization-transform.md).</span></span>

 

 



