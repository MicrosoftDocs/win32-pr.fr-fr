---
description: Le WiLstScr.vbs de fichiers VBScript est fourni dans les composants SDK Windows pour les développeurs Windows Installer. Cet exemple de script illustre la Windows Installer script Viewer.
ms.assetid: 18989c16-e0c8-4d11-b915-730951b6845b
title: Afficher le script du programme d’installation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 56888f478bb7cdd43ebcee817c86f6f9f163840e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106527345"
---
# <a name="view-installer-script"></a><span data-ttu-id="2b1a9-104">Afficher le script du programme d’installation</span><span class="sxs-lookup"><span data-stu-id="2b1a9-104">View Installer Script</span></span>

<span data-ttu-id="2b1a9-105">Le WiLstScr.vbs de fichiers VBScript est fourni dans les [composants SDK Windows pour les développeurs Windows Installer](platform-sdk-components-for-windows-installer-developers.md).</span><span class="sxs-lookup"><span data-stu-id="2b1a9-105">The VBScript file WiLstScr.vbs is provided in the [Windows SDK Components for Windows Installer Developers](platform-sdk-components-for-windows-installer-developers.md).</span></span> <span data-ttu-id="2b1a9-106">Cet exemple de script illustre la Windows Installer script Viewer.</span><span class="sxs-lookup"><span data-stu-id="2b1a9-106">This sample script demonstrates the Windows Installer script viewer.</span></span>

<span data-ttu-id="2b1a9-107">L’exemple illustre l’utilisation de :</span><span class="sxs-lookup"><span data-stu-id="2b1a9-107">The sample demonstrates the use of:</span></span>

-   [<span data-ttu-id="2b1a9-108">**OpenDatabase, méthode (objet installer)**</span><span class="sxs-lookup"><span data-stu-id="2b1a9-108">**OpenDatabase method (Installer Object)**</span></span>](installer-opendatabase.md)
-   <span data-ttu-id="2b1a9-109">Méthode [**LastErrorRecord**](installer-lasterrorrecord.md) de l’objet [**installer**](installer-object.md)</span><span class="sxs-lookup"><span data-stu-id="2b1a9-109">[**LastErrorRecord**](installer-lasterrorrecord.md) method of the [**Installer**](installer-object.md) object</span></span>
-   <span data-ttu-id="2b1a9-110">Méthode [**OpenView**](database-openview.md) de l’objet [**Database**](database-object.md)</span><span class="sxs-lookup"><span data-stu-id="2b1a9-110">[**OpenView**](database-openview.md) method of the [**Database**](database-object.md) object</span></span>
-   <span data-ttu-id="2b1a9-111">Méthode [**Fetch**](view-fetch.md) de l’objet [**View**](view-object.md)</span><span class="sxs-lookup"><span data-stu-id="2b1a9-111">[**Fetch**](view-fetch.md) method of the [**View**](view-object.md) object</span></span>
-   <span data-ttu-id="2b1a9-112">Méthode [**FormatText**](record-formattext.md)</span><span class="sxs-lookup"><span data-stu-id="2b1a9-112">[**FormatText**](record-formattext.md) method</span></span>
-   <span data-ttu-id="2b1a9-113">[**FieldCount**](record-fieldcount.md) , propriété</span><span class="sxs-lookup"><span data-stu-id="2b1a9-113">[**FieldCount**](record-fieldcount.md) property</span></span>
-   <span data-ttu-id="2b1a9-114">Propriété [**StringData**](record-stringdata.md) de l’objet [**Record**](record-object.md)</span><span class="sxs-lookup"><span data-stu-id="2b1a9-114">[**StringData**](record-stringdata.md) property of the [**Record**](record-object.md) object</span></span>
-   [<span data-ttu-id="2b1a9-115">\_Table TransformView</span><span class="sxs-lookup"><span data-stu-id="2b1a9-115">\_TransformView table</span></span>](-transformview-table.md)

<span data-ttu-id="2b1a9-116">L’utilisation de cet exemple nécessite la version CScript.exe de Windows Script Host.</span><span class="sxs-lookup"><span data-stu-id="2b1a9-116">Using this sample requires the CScript.exe version of Windows Script Host.</span></span> <span data-ttu-id="2b1a9-117">Pour utiliser CScript.exe pour exécuter cet exemple, tapez une commande à l’invite de commandes en utilisant la syntaxe suivante.</span><span class="sxs-lookup"><span data-stu-id="2b1a9-117">To use CScript.exe to run this sample, type a command at the command prompt using the following syntax.</span></span> <span data-ttu-id="2b1a9-118">L’aide s’affiche si le premier argument est/ ?</span><span class="sxs-lookup"><span data-stu-id="2b1a9-118">Help is displayed if the first argument is /?</span></span> <span data-ttu-id="2b1a9-119">ou si le nombre d’arguments spécifié est insuffisant.</span><span class="sxs-lookup"><span data-stu-id="2b1a9-119">or if too few arguments are specified.</span></span> <span data-ttu-id="2b1a9-120">Pour rediriger la sortie vers un fichier, terminez la ligne de commande avec VBS > \[ *chemin d’accès au fichier* \] .</span><span class="sxs-lookup"><span data-stu-id="2b1a9-120">To redirect the output to a file, end the command line with VBS > \[*path to file*\].</span></span> <span data-ttu-id="2b1a9-121">L’exemple retourne la valeur 0 pour Success, 1 si l’aide est appelée, et 2 si le script échoue.</span><span class="sxs-lookup"><span data-stu-id="2b1a9-121">The sample returns a value of 0 for success, 1 if help is invoked, and 2 if the script fails.</span></span>

<span data-ttu-id="2b1a9-122">**cscript WiLstScr.vbs** *\[ chemin d’accès au script \] d’exécution de Windows Installer*</span><span class="sxs-lookup"><span data-stu-id="2b1a9-122">**cscript WiLstScr.vbs** *\[path to Windows Installer execution script\]*</span></span>

<span data-ttu-id="2b1a9-123">Spécifiez le chemin d’accès au script d’exécution du programme d’installation.</span><span class="sxs-lookup"><span data-stu-id="2b1a9-123">Specify the path to the installer execution script.</span></span>

<span data-ttu-id="2b1a9-124">Pour obtenir des exemples supplémentaires de scripts, consultez [Windows Installer des exemples de scripts](windows-installer-scripting-examples.md).</span><span class="sxs-lookup"><span data-stu-id="2b1a9-124">For additional scripting examples, see [Windows Installer Scripting Examples](windows-installer-scripting-examples.md).</span></span> <span data-ttu-id="2b1a9-125">Pour obtenir des exemples d’utilitaires qui ne nécessitent pas Windows Script Host, consultez [Windows Installer les outils de développement](windows-installer-development-tools.md).</span><span class="sxs-lookup"><span data-stu-id="2b1a9-125">For sample utilities that do not require Windows Script Host, see [Windows Installer Development Tools](windows-installer-development-tools.md).</span></span>

 

 



