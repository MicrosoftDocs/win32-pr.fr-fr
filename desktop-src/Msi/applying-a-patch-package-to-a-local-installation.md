---
description: Vous pouvez appliquer la petite mise à jour à une installation locale de MNP2000 avec l’exemple de patch MNPpatch. msp créé lors de la génération d’un package de correctifs.
ms.assetid: 928182ae-5ddb-446f-a9b8-e8b3aa4ce49c
title: Application d’un package de correctifs à une installation locale
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a09ca0372870d46db67b49c0571045aadabf54c9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104202559"
---
# <a name="applying-a-patch-package-to-a-local-installation"></a><span data-ttu-id="26f71-103">Application d’un package de correctifs à une installation locale</span><span class="sxs-lookup"><span data-stu-id="26f71-103">Applying a Patch Package to a Local Installation</span></span>

<span data-ttu-id="26f71-104">Vous pouvez appliquer la petite mise à jour à une installation locale de MNP2000 avec l’exemple de patch MNPpatch. msp créé lors de la [génération d’un package de correctifs](generating-a-patch-package.md).</span><span class="sxs-lookup"><span data-stu-id="26f71-104">You may apply the small update to a local installation of MNP2000 with the sample patch MNPpatch.msp created in [Generating a Patch Package](generating-a-patch-package.md).</span></span> <span data-ttu-id="26f71-105">La procédure générale est décrite dans la section [application de petites mises à jour en appliquant des correctifs à l’installation locale du produit](applying-small-updates-by-patching-the-local-installation-of-the-product.md).</span><span class="sxs-lookup"><span data-stu-id="26f71-105">The general procedure is discussed in the section [Applying Small Updates by Patching the Local Installation of the Product](applying-small-updates-by-patching-the-local-installation-of-the-product.md).</span></span>

<span data-ttu-id="26f71-106">Installez le produit MNP2000 d’origine localement sur votre ordinateur.</span><span class="sxs-lookup"><span data-stu-id="26f71-106">Install the original MNP2000 product locally on your computer.</span></span> <span data-ttu-id="26f71-107">Vérifiez que cette erreur est Concert.txt que la mise à jour doit être corrigée.</span><span class="sxs-lookup"><span data-stu-id="26f71-107">Verify that this has the error Concert.txt that the small update is to fix.</span></span> <span data-ttu-id="26f71-108">Ensuite, lancez l’installation en entrant la ligne de commande suivante.</span><span class="sxs-lookup"><span data-stu-id="26f71-108">Next launch the installation by entering the following command line.</span></span>

<span data-ttu-id="26f71-109">**msiexec/p MNP2000. msp REINSTALL = ALL REINSTALLMODE = omus**</span><span class="sxs-lookup"><span data-stu-id="26f71-109">**msiexec /p MNP2000.msp REINSTALL=ALL REINSTALLMODE=omus**</span></span>

<span data-ttu-id="26f71-110">Réexaminez les Concert.txt appartenant à MNP2000 pour vérifier que le programme d’installation a appliqué la petite mise à jour pour corriger ce fichier.</span><span class="sxs-lookup"><span data-stu-id="26f71-110">Reexamine the Concert.txt belonging to MNP2000 to verify that the installer has applied the small update to fix this file.</span></span>

<span data-ttu-id="26f71-111">Pour appliquer la petite mise à jour à une image administrative, consultez [application d’un package de correctifs à une installation d’administration](applying-a-patch-package-to-an-administrative-installation.md).</span><span class="sxs-lookup"><span data-stu-id="26f71-111">To apply the small update to an administrative image, see [Applying a Patch Package to an Administrative Installation](applying-a-patch-package-to-an-administrative-installation.md).</span></span>

[<span data-ttu-id="26f71-112">Continuer</span><span class="sxs-lookup"><span data-stu-id="26f71-112">Continue</span></span>](applying-a-patch-package-to-an-administrative-installation.md)

 

 



