---
description: Cet exemple montre comment localiser le package Windows Installer décrit dans un exemple d’installation. Le package d’installation d’origine passe d’une version anglaise à une version en langue française.
ms.assetid: b14787fe-3179-47d7-8a15-da45987d613f
title: Exemple de localisation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8d5ae0b04e65383d665e2532d45f0cc2eed856a6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106518210"
---
# <a name="a-localization-example"></a><span data-ttu-id="3abcc-104">Exemple de localisation</span><span class="sxs-lookup"><span data-stu-id="3abcc-104">A Localization Example</span></span>

<span data-ttu-id="3abcc-105">Cet exemple montre comment localiser le package Windows Installer décrit dans [un exemple d’installation](an-installation-example.md).</span><span class="sxs-lookup"><span data-stu-id="3abcc-105">This example illustrates how to localize the Windows Installer package described in [An Installation Example](an-installation-example.md).</span></span> <span data-ttu-id="3abcc-106">Le package d’installation d’origine passe d’une version anglaise à une version en langue française.</span><span class="sxs-lookup"><span data-stu-id="3abcc-106">The original installation package is changed from an English into French language version.</span></span>

<span data-ttu-id="3abcc-107">L’exemple Localization présente les spécifications suivantes :</span><span class="sxs-lookup"><span data-stu-id="3abcc-107">The localization sample has the following specifications:</span></span>

-   <span data-ttu-id="3abcc-108">L’interface utilisateur d’installation de l’application MNP2000 doit passer de l’anglais au français.</span><span class="sxs-lookup"><span data-stu-id="3abcc-108">The installation UI for the application MNP2000 should be changed from English to French.</span></span>
-   <span data-ttu-id="3abcc-109">La version française de MNP2000 comprend des fichiers Readme.txt et Help.txt écrits en français.</span><span class="sxs-lookup"><span data-stu-id="3abcc-109">The French version of MNP2000 includes Readme.txt and Help.txt files written in the French language.</span></span>
-   <span data-ttu-id="3abcc-110">La version française comprend une liste d’agents de voyage en France qui peuvent fournir des tickets à la place de parc rouge.</span><span class="sxs-lookup"><span data-stu-id="3abcc-110">The French version includes a list of travel agents in France that can provide tickets to Red Park Arena.</span></span> <span data-ttu-id="3abcc-111">Cette liste (fournie sous la forme d’un nouveau fichier, Fre.txt) ne fait pas partie de la version anglaise.</span><span class="sxs-lookup"><span data-stu-id="3abcc-111">This list (provided as a new file, Fre.txt) is not a part of the English version.</span></span>

<span data-ttu-id="3abcc-112">La procédure générale pour la localisation d’une installation est décrite dans la section [Localizing a Windows Installer Package](localizing-a-windows-installer-package.md).</span><span class="sxs-lookup"><span data-stu-id="3abcc-112">The general procedure for localizing an installation is described in the section [Localizing a Windows Installer Package](localizing-a-windows-installer-package.md).</span></span>

<span data-ttu-id="3abcc-113">Copiez la version anglaise de MNP2000.msi et tous les fichiers sources décrits dans [planification de l’installation](planning-the-installation.md) dans un nouveau dossier.</span><span class="sxs-lookup"><span data-stu-id="3abcc-113">Copy the English version of MNP2000.msi and all the source files described in [Planning the Installation](planning-the-installation.md) into a new folder.</span></span> <span data-ttu-id="3abcc-114">Remplacez le nom de l' MNP2000.msi dans le dossier par MNPFren.msi.</span><span class="sxs-lookup"><span data-stu-id="3abcc-114">Change the name of the MNP2000.msi in the folder to MNPFren.msi.</span></span> <span data-ttu-id="3abcc-115">Dans les sections suivantes, vous allez modifier cette copie pour localiser l’application en français.</span><span class="sxs-lookup"><span data-stu-id="3abcc-115">In the following sections you will modify this copy to localize the application into French.</span></span>

[<span data-ttu-id="3abcc-116">Continuer</span><span class="sxs-lookup"><span data-stu-id="3abcc-116">Continue</span></span>](checking-the-installation-database-code-page.md)

 

 



