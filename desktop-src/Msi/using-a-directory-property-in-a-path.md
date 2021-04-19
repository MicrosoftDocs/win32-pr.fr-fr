---
description: Les répertoires de la table Directory spécifient la disposition d’une installation.
ms.assetid: 59f6ae09-d013-46d7-a1a7-0543f31ac487
title: Utilisation d’une propriété de répertoire dans un chemin d’accès
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2789f6442072f3db6a96c0abb7db301038673f83
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106542022"
---
# <a name="using-a-directory-property-in-a-path"></a><span data-ttu-id="eb203-103">Utilisation d’une propriété de répertoire dans un chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="eb203-103">Using a Directory Property in a Path</span></span>

<span data-ttu-id="eb203-104">Les répertoires de la [table Directory](directory-table.md) spécifient la disposition d’une installation.</span><span class="sxs-lookup"><span data-stu-id="eb203-104">The directories in the [Directory table](directory-table.md) specify the layout of an installation.</span></span> <span data-ttu-id="eb203-105">Lorsque le Windows Installer résout ces répertoires au cours de l' [action CostFinalize](costfinalize-action.md), les clés de la table Directory deviennent des [Propriétés](properties.md) définies sur des chemins d’accès aux répertoires.</span><span class="sxs-lookup"><span data-stu-id="eb203-105">When the Windows Installer resolves these directories during the [CostFinalize action](costfinalize-action.md), the keys in the Directory table become [properties](properties.md) set to directory paths.</span></span> <span data-ttu-id="eb203-106">Le programme d’installation définit également toujours un certain nombre de propriétés standard du [dossier système](property-reference.md) pour les chemins d’accès des dossiers système.</span><span class="sxs-lookup"><span data-stu-id="eb203-106">The installer also always sets a number of standard [System Folder Properties](property-reference.md) to system folder paths.</span></span>

<span data-ttu-id="eb203-107">Il est garanti que les valeurs des [Propriétés du dossier système](property-reference.md) se terminent dans un séparateur de répertoire.</span><span class="sxs-lookup"><span data-stu-id="eb203-107">The values of the [System Folder Properties](property-reference.md) are guaranteed to end in a directory separator.</span></span> <span data-ttu-id="eb203-108">Les valeurs de toutes les autres propriétés entrées dans la [table Directory](directory-table.md) sont garanties uniquement dans un séparateur de répertoire après que le programme d’installation a exécuté l' [action CostFinalize](costfinalize-action.md).</span><span class="sxs-lookup"><span data-stu-id="eb203-108">The values of all other properties entered in the [Directory table](directory-table.md) are only guaranteed to end in a directory separator after the installer has run the [CostFinalize action](costfinalize-action.md).</span></span> <span data-ttu-id="eb203-109">Avant la fin de l’évaluation des coûts, les valeurs des propriétés entrées dans la table de répertoires qui ne sont pas des [Propriétés de dossier système](property-reference.md) peuvent ne pas se terminer par un séparateur de répertoire.</span><span class="sxs-lookup"><span data-stu-id="eb203-109">Before costing has completed, the values of properties entered in the Directory table which are not [System Folder Properties](property-reference.md) may not end in a directory separator.</span></span> <span data-ttu-id="eb203-110">Par conséquent, si votre installation définit des propriétés de répertoire à l’aide d' [actions personnalisées](custom-actions.md) dans le package, les valeurs de référence peuvent ne pas se terminer par un séparateur de répertoire.</span><span class="sxs-lookup"><span data-stu-id="eb203-110">Therefore, if your installation sets directory properties using [custom actions](custom-actions.md) in the package, the values on reference might not end with a directory separator.</span></span>

<span data-ttu-id="eb203-111">Les propriétés de répertoire se terminant par un séparateur de répertoire peuvent donc être utilisées dans une chaîne de chemin d’accès sans inclure explicitement le séparateur de répertoire.</span><span class="sxs-lookup"><span data-stu-id="eb203-111">Directory properties ending with a directory separator can therefore be used in a path string without explicitly including the directory separator.</span></span> <span data-ttu-id="eb203-112">Par exemple, si la valeur de DirectoryProperty se termine par un séparateur de répertoire, la chaîne suivante spécifie correctement le chemin d’accès au *fichier* dans le *sous-répertoire*</span><span class="sxs-lookup"><span data-stu-id="eb203-112">For example, if the value of DirectoryProperty ends with a directory separator, the following string correctly specifies the path to *file* in *subdirectory*</span></span>

``` syntax
[DirectoryProperty]subdirectory\file
```

<span data-ttu-id="eb203-113">et la chaîne de chemin d’accès suivante est incorrecte.</span><span class="sxs-lookup"><span data-stu-id="eb203-113">and the following path string is incorrect.</span></span>

``` syntax
[DirectoryProperty]\subdirectory\file
```

 

 



