---
description: Pendant une installation Windows Installer, le programme d’installation peut rechercher un fichier et créer une propriété contenant le chemin d’accès du fichier.
ms.assetid: 6587b349-852d-4d4e-a8d4-76dfb0ef0f0b
title: Recherche d’un fichier et création d’une propriété contenant le chemin d’accès du fichier
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ed742ee874c2e4b76137e9f17e90fbf54e9729f1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103866065"
---
# <a name="searching-for-a-file-and-creating-a-property-holding-the-files-path"></a><span data-ttu-id="62f11-103">Recherche d’un fichier et création d’une propriété contenant le chemin d’accès du fichier</span><span class="sxs-lookup"><span data-stu-id="62f11-103">Searching for a File and Creating a Property Holding the File's Path</span></span>

<span data-ttu-id="62f11-104">**Pour rechercher un fichier et créer une propriété contenant le chemin d’accès de ce fichier**</span><span class="sxs-lookup"><span data-stu-id="62f11-104">**To search for a file and create a property holding the path of that file**</span></span>

1.  <span data-ttu-id="62f11-105">Commencez par Rechercher le fichier en répertoriant la signature et le nom de fichier dans la [table de signatures](signature-table.md).</span><span class="sxs-lookup"><span data-stu-id="62f11-105">First do a search for the file by listing the file signature and name in the [Signature Table](signature-table.md).</span></span>

    <span data-ttu-id="62f11-106">Les champs restants de cet enregistrement peuvent être laissés vides pour permettre la recherche d’une version de MyApp.exe.</span><span class="sxs-lookup"><span data-stu-id="62f11-106">The remaining fields of this record can be left empty to specify a search for any version of MyApp.exe.</span></span>

    <span data-ttu-id="62f11-107">[Table de signature](signature-table.md) (partielle)</span><span class="sxs-lookup"><span data-stu-id="62f11-107">[Signature Table](signature-table.md) (partial)</span></span>

    

    | <span data-ttu-id="62f11-108">Signature</span><span class="sxs-lookup"><span data-stu-id="62f11-108">Signature</span></span>          | <span data-ttu-id="62f11-109">Nom de fichier</span><span class="sxs-lookup"><span data-stu-id="62f11-109">File name</span></span>            |
    |--------------------|----------------------|
    | <span data-ttu-id="62f11-110">AppFile</span><span class="sxs-lookup"><span data-stu-id="62f11-110">AppFile</span></span><br/> | <span data-ttu-id="62f11-111">MyApp.exe</span><span class="sxs-lookup"><span data-stu-id="62f11-111">MyApp.exe</span></span><br/> |

    

     

2.  <span data-ttu-id="62f11-112">Ensuite, spécifiez le chemin d’accès du fichier recherché dans la [table DrLocator](drlocator-table.md).</span><span class="sxs-lookup"><span data-stu-id="62f11-112">Next, specify the path of the file that is being searched for in the [DrLocator Table](drlocator-table.md).</span></span>

    <span data-ttu-id="62f11-113">Comme AppFolder n’est pas listé dans la [table de signatures](signature-table.md), le programme d’installation détermine que AppFolder est un dossier plutôt qu’un fichier.</span><span class="sxs-lookup"><span data-stu-id="62f11-113">Because AppFolder is not listed in the [Signature Table](signature-table.md), the Installer determines that AppFolder is a folder rather than a file.</span></span>

    [<span data-ttu-id="62f11-114">Table DrLocator</span><span class="sxs-lookup"><span data-stu-id="62f11-114">DrLocator Table</span></span>](drlocator-table.md)

    

    | <span data-ttu-id="62f11-115">Signature</span><span class="sxs-lookup"><span data-stu-id="62f11-115">Signature</span></span>            | <span data-ttu-id="62f11-116">Parent</span><span class="sxs-lookup"><span data-stu-id="62f11-116">Parent</span></span>             | <span data-ttu-id="62f11-117">Chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="62f11-117">Path</span></span> | <span data-ttu-id="62f11-118">Profondeur</span><span class="sxs-lookup"><span data-stu-id="62f11-118">Depth</span></span> |
    |----------------------|--------------------|------|-------|
    | <span data-ttu-id="62f11-119">AppFile</span><span class="sxs-lookup"><span data-stu-id="62f11-119">AppFile</span></span><br/>   |                    |      |       |
    | <span data-ttu-id="62f11-120">AppFolder</span><span class="sxs-lookup"><span data-stu-id="62f11-120">AppFolder</span></span><br/> | <span data-ttu-id="62f11-121">AppFile</span><span class="sxs-lookup"><span data-stu-id="62f11-121">AppFile</span></span><br/> |      |       |

    

     

3.  <span data-ttu-id="62f11-122">Enfin, remplissez la [table AppSearch](appsearch-table.md) afin que l' [action AppSearch](appsearch-action.md) retourne le chemin d’accès de AppFolder.</span><span class="sxs-lookup"><span data-stu-id="62f11-122">Finally, populate the [AppSearch Table](appsearch-table.md) so that the [AppSearch Action](appsearch-action.md) returns the path of AppFolder.</span></span>

    <span data-ttu-id="62f11-123">Une fois que le programme d’installation a exécuté l’action AppSearch, la valeur de MONDOSSIER est le chemin d’accès complet de AppFolder.</span><span class="sxs-lookup"><span data-stu-id="62f11-123">After the Installer executes the AppSearch action, the value of MYFOLDER is the full path of AppFolder.</span></span>

    <span data-ttu-id="62f11-124">[Table AppSearch](appsearch-table.md) (partielle)</span><span class="sxs-lookup"><span data-stu-id="62f11-124">[AppSearch Table](appsearch-table.md) (partial)</span></span>

    

    | <span data-ttu-id="62f11-125">Propriété</span><span class="sxs-lookup"><span data-stu-id="62f11-125">Property</span></span>            | <span data-ttu-id="62f11-126">Signature</span><span class="sxs-lookup"><span data-stu-id="62f11-126">Signature</span></span>            |
    |---------------------|----------------------|
    | <span data-ttu-id="62f11-127">MONDOSSIER</span><span class="sxs-lookup"><span data-stu-id="62f11-127">MYFOLDER</span></span><br/> | <span data-ttu-id="62f11-128">AppFolder</span><span class="sxs-lookup"><span data-stu-id="62f11-128">AppFolder</span></span><br/> |

    

     

 

 




