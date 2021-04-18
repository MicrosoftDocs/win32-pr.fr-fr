---
description: Est semblable à un commutateur de ligne de commande. Toutefois, vous n’avez pas besoin de réentrer une \# commande pragma chaque fois que vous compilez un fichier MOF.
ms.assetid: 3cf22686-dd56-43a3-9584-3d707a20a3a0
ms.tgt_platform: multiple
title: '#pragma'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 62ae13d5f960e0b415f34dce97a40cff6cba8056
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106519525"
---
# <a name="pragma"></a><span data-ttu-id="f3118-104">\#pragma</span><span class="sxs-lookup"><span data-stu-id="f3118-104">\#pragma</span></span>

<span data-ttu-id="f3118-105">La commande de préprocesseur **\# pragma** est semblable à un commutateur de ligne de commande.</span><span class="sxs-lookup"><span data-stu-id="f3118-105">The **\#pragma** preprocessor command is similar to a command-line switch.</span></span> <span data-ttu-id="f3118-106">Toutefois, vous n’avez pas besoin de réentrer une commande **\# pragma** chaque fois que vous compilez un fichier MOF.</span><span class="sxs-lookup"><span data-stu-id="f3118-106">However, you do not need to reenter a **\#pragma** command each time you compile a MOF file.</span></span> <span data-ttu-id="f3118-107">L’exemple suivant illustre la syntaxe de commande **\# pragma** :</span><span class="sxs-lookup"><span data-stu-id="f3118-107">The following example illustrates **\#pragma** command syntax:</span></span>


```mof
#pragma [command]
```



<span data-ttu-id="f3118-108">En général, vous placez une commande **\# pragma** au début d’un fichier MOF.</span><span class="sxs-lookup"><span data-stu-id="f3118-108">You usually place a **\#pragma** command at the beginning of a MOF file.</span></span> <span data-ttu-id="f3118-109">Toutefois, vous pouvez placer des commandes, telles que la commande **\# pragma** , dans le corps de votre code MOF.</span><span class="sxs-lookup"><span data-stu-id="f3118-109">However, you can place some commands, such as the **\#pragma** command, in the body of your MOF code.</span></span> <span data-ttu-id="f3118-110">L’exemple suivant montre des commandes **\# pragma** qui indiquent au compilateur MOF qu’il doit placer des classes et des instances dans l' \\ espace de noms CIMV2 racine et compiler le fichier dans lequel les commandes sont incluses pendant la récupération du référentiel :</span><span class="sxs-lookup"><span data-stu-id="f3118-110">The following example shows **\#pragma** commands that indicate to the MOF compiler that it must place classes and instances in the root\\cimv2 namespace and compile the file in which the commands are included during repository recovery:</span></span>


```mof
#pragma autorecover
#pragma namespace ("\\\\.\\root\\cimv2")
```



<span data-ttu-id="f3118-111">La liste suivante répertorie les commandes **\# pragma** disponibles.</span><span class="sxs-lookup"><span data-stu-id="f3118-111">The following lists the available **\#pragma** commands.</span></span>



| <span data-ttu-id="f3118-112">Commande</span><span class="sxs-lookup"><span data-stu-id="f3118-112">Command</span></span>                                         | <span data-ttu-id="f3118-113">Description</span><span class="sxs-lookup"><span data-stu-id="f3118-113">Description</span></span>                                                                                           |
|-------------------------------------------------|-------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f3118-114">**Amendement**</span><span class="sxs-lookup"><span data-stu-id="f3118-114">**amendment**</span></span>](pragma-amendment.md)           | <span data-ttu-id="f3118-115">Indique au compilateur MOF de séparer un fichier MOF en versions indépendantes du langage et spécifiques à la langue.</span><span class="sxs-lookup"><span data-stu-id="f3118-115">Directs the MOF compiler to separate a MOF file into language-neutral and language-specific versions.</span></span> |
| [<span data-ttu-id="f3118-116">**récupération automatique**</span><span class="sxs-lookup"><span data-stu-id="f3118-116">**autorecover**</span></span>](pragma-autorecover.md)       | <span data-ttu-id="f3118-117">Ajoute un fichier MOF à la liste des fichiers compilés au cours de la récupération du référentiel.</span><span class="sxs-lookup"><span data-stu-id="f3118-117">Adds a MOF file to the list of files compiled during repository recovery.</span></span>                             |
| [<span data-ttu-id="f3118-118">**classflags**</span><span class="sxs-lookup"><span data-stu-id="f3118-118">**classflags**</span></span>](pragma-classflags.md)         | <span data-ttu-id="f3118-119">Contrôle la façon dont les classes sont créées ou mises à jour en fonction des indicateurs spécifiés.</span><span class="sxs-lookup"><span data-stu-id="f3118-119">Controls the way classes are created or updated depending on the flags specified.</span></span>                     |
| [<span data-ttu-id="f3118-120">**deleteclass**</span><span class="sxs-lookup"><span data-stu-id="f3118-120">**deleteclass**</span></span>](pragma-deleteclass.md)       | <span data-ttu-id="f3118-121">Supprime une classe existante et ses instances du référentiel.</span><span class="sxs-lookup"><span data-stu-id="f3118-121">Deletes an existing class and its instances from the repository.</span></span>                                      |
| [<span data-ttu-id="f3118-122">**DeleteInstance**</span><span class="sxs-lookup"><span data-stu-id="f3118-122">**deleteinstance**</span></span>](pragma-deleteinstance.md) | <span data-ttu-id="f3118-123">Supprime une instance existante d’une classe du référentiel.</span><span class="sxs-lookup"><span data-stu-id="f3118-123">Deletes an existing instance of a class from the repository.</span></span>                                          |
| [<span data-ttu-id="f3118-124">**instanceflags**</span><span class="sxs-lookup"><span data-stu-id="f3118-124">**instanceflags**</span></span>](pragma-instanceflags.md)   | <span data-ttu-id="f3118-125">Contrôle la façon dont les instances sont créées ou mises à jour en fonction des indicateurs spécifiés.</span><span class="sxs-lookup"><span data-stu-id="f3118-125">Controls the way instances are created or updated depending on the flags specified.</span></span>                   |
| [<span data-ttu-id="f3118-126">**joint**</span><span class="sxs-lookup"><span data-stu-id="f3118-126">**namespace**</span></span>](pragma-namespace.md)           | <span data-ttu-id="f3118-127">Demande que le compilateur charge le fichier MOF dans l’espace de noms spécifié en tant que *NamespacePath*.</span><span class="sxs-lookup"><span data-stu-id="f3118-127">Requests that the compiler load the MOF file into the namespace specified as *namespacepath*.</span></span>         |



 

## <a name="related-topics"></a><span data-ttu-id="f3118-128">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="f3118-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f3118-129">Commandes de préprocesseur</span><span class="sxs-lookup"><span data-stu-id="f3118-129">Preprocessor Commands</span></span>](preprocessor-commands.md)
</dt> </dl>

 

 



