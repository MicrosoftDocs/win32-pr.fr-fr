---
description: Les développeurs créent un package de correctifs en générant un fichier de création de correctifs et en utilisant Msimsp.exe pour appeler la fonction UiCreatePatchPackageEx dans Patchwiz.dll.
ms.assetid: 8a163653-6ba1-46ea-9832-f998749d29ae
title: Création d’un package de correctifs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2561cb6729dc7b4e0e48acd13b6338f08a8ba943
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104203217"
---
# <a name="creating-a-patch-package"></a><span data-ttu-id="88337-103">Création d’un package de correctifs</span><span class="sxs-lookup"><span data-stu-id="88337-103">Creating a Patch Package</span></span>

<span data-ttu-id="88337-104">Les développeurs créent un package de correctifs en générant un fichier de création de correctifs et en utilisant [Msimsp.exe](msimsp-exe.md) pour appeler la fonction [UiCreatePatchPackageEx](uicreatepatchpackageex--patchwiz-dll-.md) dans [Patchwiz.dll](patchwiz-dll.md).</span><span class="sxs-lookup"><span data-stu-id="88337-104">Developers create a patch package by generating a patch creation file and using [Msimsp.exe](msimsp-exe.md) to call the [UiCreatePatchPackageEx](uicreatepatchpackageex--patchwiz-dll-.md) function in [Patchwiz.dll](patchwiz-dll.md).</span></span> <span data-ttu-id="88337-105">Msimsp.exe et Patchwiz.dll sont fournis dans le kit de développement logiciel (SDK) Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="88337-105">Msimsp.exe and Patchwiz.dll are provided in the Windows Installer SDK.</span></span> <span data-ttu-id="88337-106">Pour plus d’informations, consultez [un exemple de mise à jour corrective de petite taille](a-small-update-patching-example.md).</span><span class="sxs-lookup"><span data-stu-id="88337-106">For more information, see [A Small Update Patching Example](a-small-update-patching-example.md).</span></span>

<span data-ttu-id="88337-107">Étant donné que l’application d’un correctif à un package Windows Installer entraîne l’installation des sources d’origine à l’aide d’un nouveau fichier. msi, le nouveau fichier. msi doit rester compatible avec la disposition de la source d’origine.</span><span class="sxs-lookup"><span data-stu-id="88337-107">Because the application of a patch to a Windows Installer package results in the installation of the original sources using a new .msi file, the new .msi file must remain compatible with the layout of the original source.</span></span>

<span data-ttu-id="88337-108">Lorsque vous créez un package de correctifs, vous devez utiliser une image d’installation non compressée pour créer un correctif, par exemple une image administrative ou une image d’installation non compressée à partir d’un CD-ROM.</span><span class="sxs-lookup"><span data-stu-id="88337-108">When you author a patch package you must use an uncompressed setup image to create a patch, for example, an administrative image or an uncompressed setup image from a CD-ROM.</span></span> <span data-ttu-id="88337-109">Vous devez également respecter les restrictions suivantes :</span><span class="sxs-lookup"><span data-stu-id="88337-109">You must also adhere to the following restrictions:</span></span>

-   <span data-ttu-id="88337-110">Ne déplacez pas les fichiers d’un dossier vers un autre.</span><span class="sxs-lookup"><span data-stu-id="88337-110">Do not move files from one folder to another.</span></span>
-   <span data-ttu-id="88337-111">Ne déplacez pas les fichiers d’un fichier CAB vers un autre.</span><span class="sxs-lookup"><span data-stu-id="88337-111">Do not move files from one cabinet to another.</span></span>
-   <span data-ttu-id="88337-112">Ne modifiez pas l’ordre des fichiers dans un fichier CAB.</span><span class="sxs-lookup"><span data-stu-id="88337-112">Do not change the order of files in a cabinet.</span></span>
-   <span data-ttu-id="88337-113">Ne modifiez pas le numéro de séquence des fichiers existants.</span><span class="sxs-lookup"><span data-stu-id="88337-113">Do not change the sequence number of existing files.</span></span> <span data-ttu-id="88337-114">Le numéro de séquence est la valeur spécifiée dans la colonne séquence de la [table file](file-table.md).</span><span class="sxs-lookup"><span data-stu-id="88337-114">The sequence number is the value specified in the Sequence column of the [File Table](file-table.md).</span></span>
-   <span data-ttu-id="88337-115">Tout nouveau fichier ajouté par le correctif doit être placé à la fin de la séquence de fichiers existante.</span><span class="sxs-lookup"><span data-stu-id="88337-115">Any new files that are added by the patch must be placed at the end of the existing file sequence.</span></span> <span data-ttu-id="88337-116">Le numéro de séquence de tout nouveau fichier dans l’image mise à niveau doit être supérieur au numéro de séquence le plus élevé des fichiers existants dans l’image cible.</span><span class="sxs-lookup"><span data-stu-id="88337-116">The sequence number of any new file in the upgraded image must be greater than the largest sequence number of existing files in the target image.</span></span>
-   <span data-ttu-id="88337-117">Ne modifiez pas les clés primaires dans la [table de fichiers](file-table.md) entre les versions du fichier. msi d’origine et du nouveau fichier. msi.</span><span class="sxs-lookup"><span data-stu-id="88337-117">Do not change the primary keys in the [File Table](file-table.md) between the original and new .msi file versions.</span></span>
    > [!Note]  
    > <span data-ttu-id="88337-118">Le fichier doit avoir la même clé dans la [table de fichiers](file-table.md) de l’image cible et de l’image mise à jour.</span><span class="sxs-lookup"><span data-stu-id="88337-118">The file must have the same key in the [File Table](file-table.md) of both the target image and the updated image.</span></span> <span data-ttu-id="88337-119">Les valeurs de chaîne dans la colonne file des deux tables doivent être identiques, y compris le cas.</span><span class="sxs-lookup"><span data-stu-id="88337-119">The string values in the File column of both tables must be identical, including the case.</span></span>

     

-   <span data-ttu-id="88337-120">Ne créez pas de package avec des clés de [table de fichiers](file-table.md) qui diffèrent uniquement par la casse, par exemple, évitez l’exemple de table suivant.</span><span class="sxs-lookup"><span data-stu-id="88337-120">Do not author a package with [File Table](file-table.md) keys that differ only in case, for example, avoid the following table example.</span></span>

    

    | <span data-ttu-id="88337-121">Fichier</span><span class="sxs-lookup"><span data-stu-id="88337-121">File</span></span>       | <span data-ttu-id="88337-122">-\_</span><span class="sxs-lookup"><span data-stu-id="88337-122">Component\_</span></span> | <span data-ttu-id="88337-123">FileName</span><span class="sxs-lookup"><span data-stu-id="88337-123">FileName</span></span>   |
    |------------|-------------|------------|
    | <span data-ttu-id="88337-124">readme.txt</span><span class="sxs-lookup"><span data-stu-id="88337-124">readme.txt</span></span> | <span data-ttu-id="88337-125">COMP1</span><span class="sxs-lookup"><span data-stu-id="88337-125">Comp1</span></span>       | <span data-ttu-id="88337-126">readme.txt</span><span class="sxs-lookup"><span data-stu-id="88337-126">readme.txt</span></span> |
    | <span data-ttu-id="88337-127">ReadMe.txt</span><span class="sxs-lookup"><span data-stu-id="88337-127">ReadMe.txt</span></span> | <span data-ttu-id="88337-128">COMP2</span><span class="sxs-lookup"><span data-stu-id="88337-128">Comp2</span></span>       | <span data-ttu-id="88337-129">readme.txt</span><span class="sxs-lookup"><span data-stu-id="88337-129">readme.txt</span></span> |

    

     

    <span data-ttu-id="88337-130">Les Windows Installer peuvent autoriser l’exemple de table précédent lorsque COMP1 et Comp2 sont installés sur des répertoires différents, mais que vous ne pouvez pas utiliser [Msimsp.exe](msimsp-exe.md) ou [Patchwiz.dll](patchwiz-dll.md) pour générer un correctif pour le package.</span><span class="sxs-lookup"><span data-stu-id="88337-130">The Windows Installer can allow the previous table example when Comp1 and Comp2 are installed on different directories, but then you cannot use [Msimsp.exe](msimsp-exe.md) or [Patchwiz.dll](patchwiz-dll.md) to generate a patch for the package.</span></span> <span data-ttu-id="88337-131">Msimsp.exe et Patchwiz.dll appel de Makecab.exe, qui ne respecte pas la casse et qui échoue.</span><span class="sxs-lookup"><span data-stu-id="88337-131">Msimsp.exe and Patchwiz.dll call Makecab.exe, which is case-insensitive and fails.</span></span>

    <span data-ttu-id="88337-132">Lorsque vous utilisez des modules de fusion dans le programme d’installation, assurez-vous que les numéros de séquence et la disposition des fichiers adhèrent aux indications ci-dessus.</span><span class="sxs-lookup"><span data-stu-id="88337-132">When using merge modules in the setup, ensure that file sequence numbers and layout adhere to the above guidelines.</span></span>

 

 



