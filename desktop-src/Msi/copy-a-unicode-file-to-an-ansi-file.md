---
description: Le WiToAnsi.vbs de fichiers VBScript est fourni dans les composants SDK Windows pour les développeurs Windows Installer. Cet exemple montre comment le script est utilisé pour réécrire un fichier texte Unicode sous la forme d’un fichier texte ANSI.
ms.assetid: cb22495f-968c-470a-a2f1-d0e068133956
title: Copier un fichier Unicode dans un fichier ANSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bde68c60eaa5a007aee7d2ca2d79159c9b7fce20
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103866093"
---
# <a name="copy-a-unicode-file-to-an-ansi-file"></a><span data-ttu-id="71a26-104">Copier un fichier Unicode dans un fichier ANSI</span><span class="sxs-lookup"><span data-stu-id="71a26-104">Copy a Unicode File to an ANSI File</span></span>

<span data-ttu-id="71a26-105">Le WiToAnsi.vbs de fichiers VBScript est fourni dans les [composants SDK Windows pour les développeurs Windows Installer](platform-sdk-components-for-windows-installer-developers.md).</span><span class="sxs-lookup"><span data-stu-id="71a26-105">The VBScript file WiToAnsi.vbs is provided in the [Windows SDK Components for Windows Installer Developers](platform-sdk-components-for-windows-installer-developers.md).</span></span> <span data-ttu-id="71a26-106">Cet exemple montre comment le script est utilisé pour réécrire un fichier texte Unicode sous la forme d’un fichier texte ANSI.</span><span class="sxs-lookup"><span data-stu-id="71a26-106">This sample shows how script is used to rewrite a Unicode text file as an ANSI text file.</span></span>

<span data-ttu-id="71a26-107">L’utilisation de cet exemple nécessite la version CScript.exe ou WScript.exe de Windows Script Host.</span><span class="sxs-lookup"><span data-stu-id="71a26-107">Using this sample requires the CScript.exe or WScript.exe version of Windows Script Host.</span></span> <span data-ttu-id="71a26-108">Pour utiliser CScript.exe pour exécuter cet exemple, tapez une ligne de commande à l’invite de commandes en utilisant la syntaxe suivante.</span><span class="sxs-lookup"><span data-stu-id="71a26-108">To use CScript.exe to run this sample, type a command line at the command prompt using the following syntax.</span></span> <span data-ttu-id="71a26-109">L’aide s’affiche si le premier argument est/ ?</span><span class="sxs-lookup"><span data-stu-id="71a26-109">Help is displayed if the first argument is /?</span></span> <span data-ttu-id="71a26-110">ou si le nombre d’arguments spécifié est insuffisant.</span><span class="sxs-lookup"><span data-stu-id="71a26-110">or if too few arguments are specified.</span></span> <span data-ttu-id="71a26-111">Pour rediriger la sortie vers un fichier, terminez la ligne de commande avec VBS > \[ *chemin d’accès au fichier* \] .</span><span class="sxs-lookup"><span data-stu-id="71a26-111">To redirect the output to a file, end the command line with VBS > \[*path to file*\].</span></span> <span data-ttu-id="71a26-112">L’exemple retourne la valeur 0 pour Success, 1 si l’aide est appelée, et 2 si le script échoue.</span><span class="sxs-lookup"><span data-stu-id="71a26-112">The sample returns a value of 0 for success, 1 if help is invoked, and 2 if the script fails.</span></span>

<span data-ttu-id="71a26-113">**cscript WiToAnsi.vbs \[ chemin d’accès du fichier Unicode \] \[ au fichier ANSI\]**</span><span class="sxs-lookup"><span data-stu-id="71a26-113">**cscript WiToAnsi.vbs \[path to Unicode file\]\[path to ANSI file\]**</span></span>

<span data-ttu-id="71a26-114">Spécifiez le fichier texte Unicode en cours de conversion.</span><span class="sxs-lookup"><span data-stu-id="71a26-114">Specify the Unicode text file that is being converted.</span></span> <span data-ttu-id="71a26-115">Spécifiez le fichier texte ANSI en cours de création.</span><span class="sxs-lookup"><span data-stu-id="71a26-115">Specify the ANSI text file that is being created.</span></span> <span data-ttu-id="71a26-116">Si aucun fichier ANSI n’est spécifié, le fichier Unicode est remplacé.</span><span class="sxs-lookup"><span data-stu-id="71a26-116">If no ANSI file is specified, the Unicode file is replaced.</span></span>

<span data-ttu-id="71a26-117">Pour obtenir des exemples supplémentaires de scripts, consultez [Windows Installer des exemples de scripts](windows-installer-scripting-examples.md).</span><span class="sxs-lookup"><span data-stu-id="71a26-117">For additional scripting examples, see [Windows Installer Scripting Examples](windows-installer-scripting-examples.md).</span></span> <span data-ttu-id="71a26-118">Pour obtenir des exemples d’utilitaires qui ne nécessitent pas Windows Script Host, consultez [Windows Installer outils de développement](windows-installer-development-tools.md).</span><span class="sxs-lookup"><span data-stu-id="71a26-118">For sample utilities that do not require Windows Script Host see [Windows Installer Development Tools](windows-installer-development-tools.md).</span></span>

 

 



