---
description: Pendant une installation Windows Installer, le programme d’installation peut rechercher un fichier sur tous les lecteurs fixes.
ms.assetid: c8aa84a8-5525-4a12-898f-63dc30113b13
title: Recherche d’un fichier sur tous les lecteurs fixes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 83b79c7f2999d4ee7937790dc68470210f1d4b2c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106536376"
---
# <a name="searching-all-fixed-drives-for-a-file"></a><span data-ttu-id="50ced-103">Recherche d’un fichier sur tous les lecteurs fixes</span><span class="sxs-lookup"><span data-stu-id="50ced-103">Searching All Fixed Drives for a File</span></span>

<span data-ttu-id="50ced-104">**Pour rechercher un fichier sur tous les lecteurs fixes**</span><span class="sxs-lookup"><span data-stu-id="50ced-104">**To search all fixed drives for a file**</span></span>

1.  <span data-ttu-id="50ced-105">Entrez la signature et le nom du fichier dans la [table de signatures](signature-table.md).</span><span class="sxs-lookup"><span data-stu-id="50ced-105">Enter the file signature and name in the [Signature Table](signature-table.md).</span></span> <span data-ttu-id="50ced-106">Les champs restants de cet enregistrement peuvent avoir la valeur null pour rechercher n’importe quelle version de MyApp.exe.</span><span class="sxs-lookup"><span data-stu-id="50ced-106">The remaining fields in this record can be null to search for any version of MyApp.exe.</span></span>

    <span data-ttu-id="50ced-107">[Table de signature](signature-table.md) (partielle)</span><span class="sxs-lookup"><span data-stu-id="50ced-107">[Signature Table](signature-table.md) (partial)</span></span>

    

    | <span data-ttu-id="50ced-108">Signature</span><span class="sxs-lookup"><span data-stu-id="50ced-108">Signature</span></span>          | <span data-ttu-id="50ced-109">Nom de fichier</span><span class="sxs-lookup"><span data-stu-id="50ced-109">File Name</span></span>            |
    |--------------------|----------------------|
    | <span data-ttu-id="50ced-110">AppFile</span><span class="sxs-lookup"><span data-stu-id="50ced-110">AppFile</span></span><br/> | <span data-ttu-id="50ced-111">MyApp.exe</span><span class="sxs-lookup"><span data-stu-id="50ced-111">MyApp.exe</span></span><br/> |

    

     

2.  <span data-ttu-id="50ced-112">Entrez la propriété que le programme d’installation doit définir si MyApp.exe est installé.</span><span class="sxs-lookup"><span data-stu-id="50ced-112">Enter the property that the Installer is to set if MyApp.exe is installed.</span></span>

    [<span data-ttu-id="50ced-113">Table AppSearch</span><span class="sxs-lookup"><span data-stu-id="50ced-113">AppSearch Table</span></span>](appsearch-table.md)

    

    | <span data-ttu-id="50ced-114">Propriété</span><span class="sxs-lookup"><span data-stu-id="50ced-114">Property</span></span>         | <span data-ttu-id="50ced-115">Signature</span><span class="sxs-lookup"><span data-stu-id="50ced-115">Signature</span></span>          |
    |------------------|--------------------|
    | <span data-ttu-id="50ced-116">MYAPP</span><span class="sxs-lookup"><span data-stu-id="50ced-116">MYAPP</span></span><br/> | <span data-ttu-id="50ced-117">AppFile</span><span class="sxs-lookup"><span data-stu-id="50ced-117">AppFile</span></span><br/> |

    

     

3.  <span data-ttu-id="50ced-118">Utilisez la [table DrLocator](drlocator-table.md).</span><span class="sxs-lookup"><span data-stu-id="50ced-118">Use the [DrLocator Table](drlocator-table.md).</span></span> <span data-ttu-id="50ced-119">Laissez les champs parent et chemin vides pour rechercher tous les lecteurs fixes du système utilisateur.</span><span class="sxs-lookup"><span data-stu-id="50ced-119">Leave the Parent and Path fields empty to search all fixed drives of the user system.</span></span> <span data-ttu-id="50ced-120">Spécifiez dans la colonne profondeur le nombre de niveaux de sous-répertoires à rechercher.</span><span class="sxs-lookup"><span data-stu-id="50ced-120">Specify in the Depth column the number of subdirectory levels to search.</span></span> <span data-ttu-id="50ced-121">Par exemple, l’affectation de la valeur 0 à Depth détecte c : \\MyApp.exe, mais ne détecte pas le fichier à une profondeur de 2, par exemple : c : \\ Program Files \\ myapps \\MyApp.exe.</span><span class="sxs-lookup"><span data-stu-id="50ced-121">For example, setting Depth to 0 detects c:\\MyApp.exe, but does not detect the file at a depth of 2, for example: c:\\Program Files\\MyApps\\MyApp.exe.</span></span>

    [<span data-ttu-id="50ced-122">Table DrLocator</span><span class="sxs-lookup"><span data-stu-id="50ced-122">DrLocator Table</span></span>](drlocator-table.md)

    

    | <span data-ttu-id="50ced-123">Signature</span><span class="sxs-lookup"><span data-stu-id="50ced-123">Signature</span></span>          | <span data-ttu-id="50ced-124">Parent</span><span class="sxs-lookup"><span data-stu-id="50ced-124">Parent</span></span> | <span data-ttu-id="50ced-125">Chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="50ced-125">Path</span></span> | <span data-ttu-id="50ced-126">Profondeur</span><span class="sxs-lookup"><span data-stu-id="50ced-126">Depth</span></span>        |
    |--------------------|--------|------|--------------|
    | <span data-ttu-id="50ced-127">AppFile</span><span class="sxs-lookup"><span data-stu-id="50ced-127">AppFile</span></span><br/> |        |      | <span data-ttu-id="50ced-128">3</span><span class="sxs-lookup"><span data-stu-id="50ced-128">3</span></span><br/> |

    

     

4.  <span data-ttu-id="50ced-129">Inclure l’action AppSearch dans la séquence d’action.</span><span class="sxs-lookup"><span data-stu-id="50ced-129">Include the AppSearch action in the action sequence.</span></span> <span data-ttu-id="50ced-130">Si MyApp.exe est installé, le programme d’installation définit la propriété MYAPP à l’emplacement du fichier.</span><span class="sxs-lookup"><span data-stu-id="50ced-130">If MyApp.exe is installed, the Installer sets the property MYAPP to the location of the file.</span></span> <span data-ttu-id="50ced-131">Si le fichier est installé, MYAPP prend la valeur true dans une expression conditionnelle.</span><span class="sxs-lookup"><span data-stu-id="50ced-131">If the file is installed, MYAPP evaluates as True in a conditional expression.</span></span>

 

 




