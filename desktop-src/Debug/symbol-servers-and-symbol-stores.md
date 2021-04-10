---
description: La configuration correcte des symboles pour le débogage peut être une tâche difficile, en particulier pour le débogage du noyau.
ms.assetid: 96b2c9db-58fb-4c28-b17c-3b1cc06ed96b
title: "  Serveur de symboles et magasins de symboles"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 644410fcb929308a259c5fc752f55742bfb23bae
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104200941"
---
# <a name="symbol-server-and-symbol-stores"></a><span data-ttu-id="e3c0d-103">  Serveur de symboles et magasins de symboles</span><span class="sxs-lookup"><span data-stu-id="e3c0d-103">Symbol Server and Symbol Stores</span></span>

<span data-ttu-id="e3c0d-104">La configuration correcte des symboles pour le débogage peut être une tâche difficile, en particulier pour le débogage du noyau.</span><span class="sxs-lookup"><span data-stu-id="e3c0d-104">Setting up symbols correctly for debugging can be a challenging task, particularly for kernel debugging.</span></span> <span data-ttu-id="e3c0d-105">Il est souvent nécessaire de connaître les noms et les versions de tous les produits sur votre ordinateur.</span><span class="sxs-lookup"><span data-stu-id="e3c0d-105">It often requires that you know the names and releases of all products on your computer.</span></span> <span data-ttu-id="e3c0d-106">Le débogueur doit être en mesure de localiser les fichiers de symboles qui correspondent à chaque version de produit et Service Pack.</span><span class="sxs-lookup"><span data-stu-id="e3c0d-106">The debugger must be able to locate the symbol files that correspond to each product release and service pack.</span></span> <span data-ttu-id="e3c0d-107">Cela peut aboutir à un chemin d’accès de symboles extrêmement long composé d’une longue liste de répertoires.</span><span class="sxs-lookup"><span data-stu-id="e3c0d-107">This can result in an extremely long symbol path consisting of a long list of directories.</span></span>

<span data-ttu-id="e3c0d-108">Pour simplifier ces difficultés dans la coordination des fichiers de symboles, utilisez le *serveur de symboles*.</span><span class="sxs-lookup"><span data-stu-id="e3c0d-108">To simplify these difficulties in coordinating symbol files, use the *symbol server*.</span></span> <span data-ttu-id="e3c0d-109">Le serveur de symboles permet aux débogueurs de récupérer automatiquement les fichiers de symboles appropriés sans les noms de produits, les mises en production ou les numéros de Build.</span><span class="sxs-lookup"><span data-stu-id="e3c0d-109">The symbol server enables the debuggers to automatically retrieve the correct symbol files without product names, releases, or build numbers.</span></span> <span data-ttu-id="e3c0d-110">Outils de débogage pour Windows contient le serveur de symboles SymSrv.</span><span class="sxs-lookup"><span data-stu-id="e3c0d-110">Debugging Tools for Windows contains the SymSrv symbol server.</span></span>

<span data-ttu-id="e3c0d-111">Le serveur de symboles est activé en incluant une certaine chaîne de texte dans le chemin d’accès aux symboles.</span><span class="sxs-lookup"><span data-stu-id="e3c0d-111">The symbol server is activated by including a certain text string in the symbol path.</span></span> <span data-ttu-id="e3c0d-112">Chaque fois que le débogueur doit charger des symboles pour un module qui vient d’être chargé, il appelle le serveur de symboles pour localiser les fichiers de symboles appropriés.</span><span class="sxs-lookup"><span data-stu-id="e3c0d-112">Each time the debugger needs to load symbols for a newly loaded module, it calls the symbol server to locate the appropriate symbol files.</span></span> <span data-ttu-id="e3c0d-113">Le serveur de symboles localise les fichiers dans un *magasin de symboles*.</span><span class="sxs-lookup"><span data-stu-id="e3c0d-113">The symbol server locates the files in a *symbol store*.</span></span> <span data-ttu-id="e3c0d-114">Il s’agit d’une collection de fichiers de symboles, d’un index et d’un outil qui peut être utilisé par un administrateur pour ajouter et supprimer des fichiers.</span><span class="sxs-lookup"><span data-stu-id="e3c0d-114">This is a collection of symbol files, an index, and a tool that can be used by an administrator to add and delete files.</span></span> <span data-ttu-id="e3c0d-115">Les fichiers sont indexés selon des paramètres uniques, tels que l’horodatage et la taille de l’image.</span><span class="sxs-lookup"><span data-stu-id="e3c0d-115">The files are indexed according to unique parameters such as the time stamp and image size.</span></span> <span data-ttu-id="e3c0d-116">Les outils de débogage pour Windows contiennent un outil de magasin de symboles appelé SymStore.</span><span class="sxs-lookup"><span data-stu-id="e3c0d-116">Debugging Tools for Windows contains a symbol store tool called SymStore.</span></span>

<span data-ttu-id="e3c0d-117">Pour plus d’informations, consultez :</span><span class="sxs-lookup"><span data-stu-id="e3c0d-117">For more information, see:</span></span>

-   [<span data-ttu-id="e3c0d-118">Utilisation de SymSrv</span><span class="sxs-lookup"><span data-stu-id="e3c0d-118">Using SymSrv</span></span>](using-symsrv.md)
-   [<span data-ttu-id="e3c0d-119">Utilisation de SymStore</span><span class="sxs-lookup"><span data-stu-id="e3c0d-119">Using SymStore</span></span>](using-symstore.md)
-   [<span data-ttu-id="e3c0d-120">Utilisation d’autres magasins de symboles</span><span class="sxs-lookup"><span data-stu-id="e3c0d-120">Using Other Symbol Stores</span></span>](using-other-symbol-stores.md)
-   [<span data-ttu-id="e3c0d-121">Options de Command-Line SymStore</span><span class="sxs-lookup"><span data-stu-id="e3c0d-121">SymStore Command-Line Options</span></span>](symstore-command-line-options.md)
-   [<span data-ttu-id="e3c0d-122">Serveur de symboles et pare-feu Internet</span><span class="sxs-lookup"><span data-stu-id="e3c0d-122">Symbol Server and Internet Firewalls</span></span>](symbol-servers-and-internet-firewalls.md)

## <a name="related-topics"></a><span data-ttu-id="e3c0d-123">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="e3c0d-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e3c0d-124">Fichiers de symboles</span><span class="sxs-lookup"><span data-stu-id="e3c0d-124">Symbol Files</span></span>](symbol-files.md)
</dt> </dl>

 

 



