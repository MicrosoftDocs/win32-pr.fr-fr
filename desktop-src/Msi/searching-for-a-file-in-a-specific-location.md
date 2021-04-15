---
description: Pendant une installation Windows Installer, le programme d’installation peut rechercher un fichier dans un emplacement spécifique sur le système de l’utilisateur.
ms.assetid: 127d83a2-b651-42ef-ac7c-a7fa1b15cf27
title: Recherche d’un fichier dans un emplacement spécifique
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 72ad4e456d331119b698d8e6e696e86b953006eb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104529499"
---
# <a name="searching-for-a-file-in-a-specific-location"></a><span data-ttu-id="2260c-103">Recherche d’un fichier dans un emplacement spécifique</span><span class="sxs-lookup"><span data-stu-id="2260c-103">Searching for a File in a Specific Location</span></span>

<span data-ttu-id="2260c-104">**Pour rechercher un fichier dans un emplacement spécifique sur un système utilisateur**</span><span class="sxs-lookup"><span data-stu-id="2260c-104">**To search for a file in a specific location on a user system**</span></span>

1.  <span data-ttu-id="2260c-105">Répertorie la signature et le nom de fichier dans la [table de signatures](signature-table.md).</span><span class="sxs-lookup"><span data-stu-id="2260c-105">List the file signature and name in the [Signature Table](signature-table.md).</span></span> <span data-ttu-id="2260c-106">Les champs restants de cet enregistrement peuvent avoir la valeur null pour rechercher n’importe quelle version de MyApp.exe.</span><span class="sxs-lookup"><span data-stu-id="2260c-106">The remaining fields in this record can be null to search for any version of MyApp.exe.</span></span>

    [<span data-ttu-id="2260c-107">Table de signature</span><span class="sxs-lookup"><span data-stu-id="2260c-107">Signature Table</span></span>](signature-table.md)

    

    | <span data-ttu-id="2260c-108">Signature</span><span class="sxs-lookup"><span data-stu-id="2260c-108">Signature</span></span>          | <span data-ttu-id="2260c-109">Nom de fichier</span><span class="sxs-lookup"><span data-stu-id="2260c-109">File name</span></span>            |
    |--------------------|----------------------|
    | <span data-ttu-id="2260c-110">AppFile</span><span class="sxs-lookup"><span data-stu-id="2260c-110">AppFile</span></span><br/> | <span data-ttu-id="2260c-111">MyApp.exe</span><span class="sxs-lookup"><span data-stu-id="2260c-111">MyApp.exe</span></span><br/> |

    

     

2.  <span data-ttu-id="2260c-112">Entrez la propriété que le programme d’installation doit définir si MyApp.exe est installé.</span><span class="sxs-lookup"><span data-stu-id="2260c-112">Enter the property that the Installer is to set if MyApp.exe is installed.</span></span>

    <span data-ttu-id="2260c-113">[Table AppSearch](appsearch-table.md) (partielle)</span><span class="sxs-lookup"><span data-stu-id="2260c-113">[AppSearch Table](appsearch-table.md) (partial)</span></span>

    

    | <span data-ttu-id="2260c-114">Propriété</span><span class="sxs-lookup"><span data-stu-id="2260c-114">Property</span></span>         | <span data-ttu-id="2260c-115">Signature</span><span class="sxs-lookup"><span data-stu-id="2260c-115">Signature</span></span>          |
    |------------------|--------------------|
    | <span data-ttu-id="2260c-116">MYAPP</span><span class="sxs-lookup"><span data-stu-id="2260c-116">MYAPP</span></span><br/> | <span data-ttu-id="2260c-117">AppFile</span><span class="sxs-lookup"><span data-stu-id="2260c-117">AppFile</span></span><br/> |

    

     

3.  <span data-ttu-id="2260c-118">Utilisez la [table DrLocator](drlocator-table.md).</span><span class="sxs-lookup"><span data-stu-id="2260c-118">Use the [DrLocator Table](drlocator-table.md).</span></span> <span data-ttu-id="2260c-119">Entrez le chemin d’accès complet au fichier sur le système de l’utilisateur dans le champ chemin d’accès.</span><span class="sxs-lookup"><span data-stu-id="2260c-119">Enter the full path to the file on the user system in the Path field.</span></span> <span data-ttu-id="2260c-120">Entrez la valeur 0 dans la colonne profondeur pour rechercher dans le dossier bin.</span><span class="sxs-lookup"><span data-stu-id="2260c-120">Enter a value of 0 into the Depth column to search the bin folder.</span></span>

    [<span data-ttu-id="2260c-121">Table DrLocator</span><span class="sxs-lookup"><span data-stu-id="2260c-121">DrLocator Table</span></span>](drlocator-table.md)

    

    | <span data-ttu-id="2260c-122">Signature</span><span class="sxs-lookup"><span data-stu-id="2260c-122">Signature</span></span>          | <span data-ttu-id="2260c-123">Parent</span><span class="sxs-lookup"><span data-stu-id="2260c-123">Parent</span></span> | <span data-ttu-id="2260c-124">Chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="2260c-124">Path</span></span>                                                    | <span data-ttu-id="2260c-125">Profondeur</span><span class="sxs-lookup"><span data-stu-id="2260c-125">Depth</span></span>        |
    |--------------------|--------|---------------------------------------------------------|--------------|
    | <span data-ttu-id="2260c-126">AppFile</span><span class="sxs-lookup"><span data-stu-id="2260c-126">AppFile</span></span><br/> |        | <span data-ttu-id="2260c-127">C : \\ Program Files \\ MyProducts \\ bin de projets \\</span><span class="sxs-lookup"><span data-stu-id="2260c-127">C:\\Program Files\\MyProducts\\Projects\\bin</span></span><br/> | <span data-ttu-id="2260c-128">0</span><span class="sxs-lookup"><span data-stu-id="2260c-128">0</span></span><br/> |

    

     

4.  <span data-ttu-id="2260c-129">Inclure l’action AppSearch dans la séquence d’action.</span><span class="sxs-lookup"><span data-stu-id="2260c-129">Include the AppSearch action in the action sequence.</span></span> <span data-ttu-id="2260c-130">Si MyApp.exe est installé dans le dossier C : \\ Program Files \\ MyProducts \\ projects \\ , le programme d’installation définit la propriété MyApp sur l’emplacement du fichier.</span><span class="sxs-lookup"><span data-stu-id="2260c-130">If MyApp.exe is installed in C:\\Program Files\\MyProducts\\Projects\\bin, the Installer sets the property MYAPP to the location of file.</span></span>

 

 




