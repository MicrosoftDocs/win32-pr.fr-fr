---
description: La section d’installation d’un fichier INF définit les étapes de la procédure d’installation.
ms.assetid: 24d40dc6-ac09-4cf8-9229-f81da2925576
title: Exemple de section d’installation INF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 39c8162dbf06b87faf8a1ce432c361a28befca0d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106543728"
---
# <a name="inf-install-section-example"></a><span data-ttu-id="ada4c-103">Exemple de section d’installation INF</span><span class="sxs-lookup"><span data-stu-id="ada4c-103">INF Install Section Example</span></span>

<span data-ttu-id="ada4c-104">La **section d’installation d'** un fichier INF définit les étapes de la procédure d’installation.</span><span class="sxs-lookup"><span data-stu-id="ada4c-104">The **Install** section of an INF File defines the steps of the installation procedure.</span></span> <span data-ttu-id="ada4c-105">Chaque ligne d’une section d' **installation** comporte deux parties.</span><span class="sxs-lookup"><span data-stu-id="ada4c-105">Each line of an **Install** section has two parts.</span></span> <span data-ttu-id="ada4c-106">À gauche du signe égal (=) est la clé.</span><span class="sxs-lookup"><span data-stu-id="ada4c-106">On the left of the equals sign (=) is the key.</span></span> <span data-ttu-id="ada4c-107">Sur le côté droit, est une liste d’un ou plusieurs titres de section.</span><span class="sxs-lookup"><span data-stu-id="ada4c-107">On the right hand side, is a list of one or more section titles.</span></span> <span data-ttu-id="ada4c-108">La clé spécifie le type des sections répertoriées à droite.</span><span class="sxs-lookup"><span data-stu-id="ada4c-108">The key specifies the type of the sections that are listed on the right.</span></span> <span data-ttu-id="ada4c-109">Pour obtenir une description du format de cette section, consultez les sections et les directives du fichier INF du kit de développement de pilotes Microsoft Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="ada4c-109">For a description of this section's format see the "INF File Sections and Directives" of the Microsoft Windows 2000 Driver Development Kit.</span></span>

<span data-ttu-id="ada4c-110">Voici un exemple de section d' **installation** .</span><span class="sxs-lookup"><span data-stu-id="ada4c-110">The following is an example of an **Install** section.</span></span>

``` syntax
[MyInstallSection]
Copyfiles=DataFiles, ProgramFiles
Delfiles=OldFiles
UpdateInis=NewIniInfo
AddReg=NewRegistryInfo, MoreNewRegistryInfo
DelReg=OldRegistryInfo, MoreOldRegistryInfo
```

<span data-ttu-id="ada4c-111">Dans cet exemple, la clé **CopyFiles** est définie sur les valeurs « fichiers de fichiers » et « ProgramFiles ».</span><span class="sxs-lookup"><span data-stu-id="ada4c-111">In this example the **CopyFiles** key is set to the values "DataFiles" and "ProgramFiles".</span></span> <span data-ttu-id="ada4c-112">Cela spécifie deux sections de **fichiers de copie** dans le fichier INF qui contiennent les noms des fichiers sources utilisés par les opérations de copie.</span><span class="sxs-lookup"><span data-stu-id="ada4c-112">This specifies two **Copy Files** sections in the INF file that contain the names of the source files used by copying operations.</span></span> <span data-ttu-id="ada4c-113">La destination des fichiers copiés est spécifiée dans une section **DestinationDirs** dans le fichier INF.</span><span class="sxs-lookup"><span data-stu-id="ada4c-113">The destination for the copied files would be specified in a **DestinationDirs** section in the INF file.</span></span>

<span data-ttu-id="ada4c-114">La clé **DelFiles** reçoit la valeur « OldFiles ».</span><span class="sxs-lookup"><span data-stu-id="ada4c-114">The **Delfiles** key is given the value "OldFiles".</span></span> <span data-ttu-id="ada4c-115">Cela spécifie une section de **Suppression de fichiers** qui contient des informations relatives aux opérations de suppression de fichiers.</span><span class="sxs-lookup"><span data-stu-id="ada4c-115">This specifies a **Delete Files** section that contains information relevant to file deletion operations.</span></span>

<span data-ttu-id="ada4c-116">La clé **UpdateInis** spécifie la **mise à jour** des sections du fichier ini qui contiennent des informations sur la mise à jour des entrées dans le fichier ini.</span><span class="sxs-lookup"><span data-stu-id="ada4c-116">The **UpdateInis** key specifies **Update INI File** sections that contain information about updating entries in the INI file.</span></span>

<span data-ttu-id="ada4c-117">Les clés **AddReg** et **DelReg** spécifient des sections **Add Registry** et **Delete Registry** qui contiennent des informations sur l’ajout ou la suppression d’informations de registre.</span><span class="sxs-lookup"><span data-stu-id="ada4c-117">The **AddReg** and **DelReg** keys specify **Add Registry** and **Delete Registry** sections that contain information about adding or deleting registry information.</span></span>

 

 



