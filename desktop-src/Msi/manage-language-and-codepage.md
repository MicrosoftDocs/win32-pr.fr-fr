---
description: Le WiLangID.vbs de fichiers VBScript est fourni dans les composants SDK Windows pour les développeurs Windows Installer.
ms.assetid: 319e9ffd-ff9f-4b4c-913e-2c571f2ec9ee
title: Gérer la langue et la page de codes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3cbfb96f04d75ed79f32c8a49fe58b8dcc86f184
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106523432"
---
# <a name="manage-language-and-codepage"></a><span data-ttu-id="0b366-103">Gérer la langue et la page de codes</span><span class="sxs-lookup"><span data-stu-id="0b366-103">Manage Language and Codepage</span></span>

<span data-ttu-id="0b366-104">Le WiLangID.vbs de fichiers VBScript est fourni dans les [composants SDK Windows pour les développeurs Windows Installer](platform-sdk-components-for-windows-installer-developers.md).</span><span class="sxs-lookup"><span data-stu-id="0b366-104">The VBScript file WiLangID.vbs is provided in the [Windows SDK Components for Windows Installer Developers](platform-sdk-components-for-windows-installer-developers.md).</span></span> <span data-ttu-id="0b366-105">Cet exemple montre comment le script est utilisé pour accéder aux informations de langage et à la page de codes d’un package.</span><span class="sxs-lookup"><span data-stu-id="0b366-105">This sample shows how script is used to access a package's language information and codepage.</span></span> <span data-ttu-id="0b366-106">Pour plus d’informations, consultez [localisation d’un Package Windows Installer](localizing-a-windows-installer-package.md) et [gestion des pages de codes (Windows Installer)](code-page-handling-windows-installer-.md).</span><span class="sxs-lookup"><span data-stu-id="0b366-106">For more information, see [Localizing a Windows Installer Package](localizing-a-windows-installer-package.md) and [Code Page Handling (Windows Installer)](code-page-handling-windows-installer-.md).</span></span>

<span data-ttu-id="0b366-107">L’exemple illustre l’utilisation de :</span><span class="sxs-lookup"><span data-stu-id="0b366-107">The sample demonstrates the use of:</span></span>

-   [<span data-ttu-id="0b366-108">**OpenDatabase, méthode (objet installer)**</span><span class="sxs-lookup"><span data-stu-id="0b366-108">**OpenDatabase method (Installer Object)**</span></span>](installer-opendatabase.md)
-   [<span data-ttu-id="0b366-109">**Méthode CreateRecord**</span><span class="sxs-lookup"><span data-stu-id="0b366-109">**CreateRecord method**</span></span>](installer-createrecord.md)
-   <span data-ttu-id="0b366-110">[**Méthode LastErrorRecord**](installer-lasterrorrecord.md) de l' [ **objet installer**](installer-object.md)</span><span class="sxs-lookup"><span data-stu-id="0b366-110">[**LastErrorRecord method**](installer-lasterrorrecord.md) of the [**Installer object**](installer-object.md)</span></span>
-   [<span data-ttu-id="0b366-111">**OpenView, méthode**</span><span class="sxs-lookup"><span data-stu-id="0b366-111">**OpenView method**</span></span>](database-openview.md)
-   <span data-ttu-id="0b366-112">[**Propriété SummaryInformation (objet Database)**](database-summaryinformation.md) de l' [ **objet Database**](database-object.md)</span><span class="sxs-lookup"><span data-stu-id="0b366-112">[**SummaryInformation property (Database Object)**](database-summaryinformation.md) of the [**Database object**](database-object.md)</span></span>

<span data-ttu-id="0b366-113">L’utilisation de cet exemple nécessite la version CScript.exe ou WScript.exe de Windows Script Host.</span><span class="sxs-lookup"><span data-stu-id="0b366-113">Using this sample requires the CScript.exe or WScript.exe version of Windows Script Host.</span></span> <span data-ttu-id="0b366-114">Pour utiliser CScript.exe pour exécuter cet exemple, tapez une commande à l’invite de commandes en utilisant la syntaxe suivante.</span><span class="sxs-lookup"><span data-stu-id="0b366-114">To use CScript.exe to run this sample, type a command at the command prompt using the following syntax.</span></span> <span data-ttu-id="0b366-115">L’aide s’affiche si le premier argument est/ ?</span><span class="sxs-lookup"><span data-stu-id="0b366-115">Help is displayed if the first argument is /?</span></span> <span data-ttu-id="0b366-116">ou si le nombre d’arguments spécifié est insuffisant.</span><span class="sxs-lookup"><span data-stu-id="0b366-116">or if too few arguments are specified.</span></span> <span data-ttu-id="0b366-117">Pour rediriger la sortie vers un fichier, terminez la ligne de commande avec VBS > \[ *chemin d’accès au fichier* \] .</span><span class="sxs-lookup"><span data-stu-id="0b366-117">To redirect the output to a file, end the command line with VBS > \[*path to file*\].</span></span> <span data-ttu-id="0b366-118">L’exemple retourne la valeur 0 pour Success, 1 si l’aide est appelée, et 2 si le script échoue.</span><span class="sxs-lookup"><span data-stu-id="0b366-118">The sample returns a value of 0 for success, 1 if help is invoked, and 2 if the script fails.</span></span>

<span data-ttu-id="0b366-119">**cscript WiLangID.vbs \[ chemin d’accès à la \] \[ valeur du mot clé de \] base de données \[\]**</span><span class="sxs-lookup"><span data-stu-id="0b366-119">**cscript WiLangID.vbs \[path to database\]\[keyword\]\[value\]**</span></span>

<span data-ttu-id="0b366-120">Spécifiez le chemin d’accès à la base de données Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="0b366-120">Specify the path to the Windows Installer database.</span></span> <span data-ttu-id="0b366-121">Pour modifier une valeur, spécifiez l’un des mots clés suivants, suivi de la nouvelle valeur.</span><span class="sxs-lookup"><span data-stu-id="0b366-121">To change a value specify one of the following keywords followed by the new value.</span></span> <span data-ttu-id="0b366-122">Si aucune valeur n’est spécifiée, l’exemple retourne la valeur actuelle.</span><span class="sxs-lookup"><span data-stu-id="0b366-122">If no value is specified the sample returns the current value.</span></span>



| <span data-ttu-id="0b366-123">Mot clé</span><span class="sxs-lookup"><span data-stu-id="0b366-123">Keyword</span></span>      | <span data-ttu-id="0b366-124">Description</span><span class="sxs-lookup"><span data-stu-id="0b366-124">Description</span></span>                                                                                                                                                                                |
|--------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0b366-125">**Package**</span><span class="sxs-lookup"><span data-stu-id="0b366-125">**Package**</span></span>  | <span data-ttu-id="0b366-126">Versions de langage prises en charge par la base de données.</span><span class="sxs-lookup"><span data-stu-id="0b366-126">The language versions supported by the database.</span></span> <span data-ttu-id="0b366-127">Pour plus d’informations, consultez la propriété [**Résumé du modèle**](template-summary.md) .</span><span class="sxs-lookup"><span data-stu-id="0b366-127">For information, see [**Template Summary**](template-summary.md) property.</span></span>                                                               |
| <span data-ttu-id="0b366-128">**Produit**</span><span class="sxs-lookup"><span data-stu-id="0b366-128">**Product**</span></span>  | <span data-ttu-id="0b366-129">Langue que le programme d’installation doit utiliser pour toutes les chaînes de l’interface utilisateur qui ne sont pas créées dans la base de données.</span><span class="sxs-lookup"><span data-stu-id="0b366-129">Language the installer should use for any strings in the user interface that are not authored into the database.</span></span> <span data-ttu-id="0b366-130">Pour plus d’informations, consultez propriété [**ProductLanguage**](productlanguage.md) .</span><span class="sxs-lookup"><span data-stu-id="0b366-130">For information, see [**ProductLanguage**](productlanguage.md) property.</span></span> |
| <span data-ttu-id="0b366-131">**Codepage**</span><span class="sxs-lookup"><span data-stu-id="0b366-131">**Codepage**</span></span> | <span data-ttu-id="0b366-132">Page de codes ANSI unique pour le pool de chaînes.</span><span class="sxs-lookup"><span data-stu-id="0b366-132">Single ANSI code page for the string pool.</span></span> <span data-ttu-id="0b366-133">Pour plus d’informations, consultez [gestion des pages de codes (Windows Installer)](code-page-handling-windows-installer-.md).</span><span class="sxs-lookup"><span data-stu-id="0b366-133">For information, see [Code Page Handling (Windows Installer)](code-page-handling-windows-installer-.md).</span></span>                                       |



 

<span data-ttu-id="0b366-134">Pour obtenir des exemples supplémentaires de scripts, consultez [Windows Installer des exemples de scripts](windows-installer-scripting-examples.md).</span><span class="sxs-lookup"><span data-stu-id="0b366-134">For additional scripting examples, see [Windows Installer Scripting Examples](windows-installer-scripting-examples.md).</span></span> <span data-ttu-id="0b366-135">Pour obtenir des exemples d’utilitaires qui ne nécessitent pas Windows Script Host, consultez [Windows Installer outils de développement](windows-installer-development-tools.md).</span><span class="sxs-lookup"><span data-stu-id="0b366-135">For sample utilities that do not require Windows Script Host see [Windows Installer Development Tools](windows-installer-development-tools.md).</span></span>

<span data-ttu-id="0b366-136">Pour plus d’informations, consultez Détermination de la page de codes d’une [base de données d’installation](determining-an-installation-database-s-code-page.md) et [définition de la page de codes d’une base de données](setting-the-code-page-of-a-database.md).</span><span class="sxs-lookup"><span data-stu-id="0b366-136">For more information, see [Determining an Installation Database's Code Page](determining-an-installation-database-s-code-page.md) and [Setting the Code Page of a Database](setting-the-code-page-of-a-database.md).</span></span>

 

 



