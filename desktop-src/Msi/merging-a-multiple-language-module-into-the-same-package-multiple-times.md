---
description: Lorsqu’un module prend en charge plusieurs langues, vous pouvez le fusionner dans la même Windows Installer base de données plusieurs fois, tout en veillant à ce que chaque fusion utilise une langue différente.
ms.assetid: 816b1f52-1ca2-4332-9a9b-462ea372c3bb
title: Fusion multiple d’un module multiple Language dans le même package
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 52552a68643d52c6aad97ed666b7dc1ae4043fd9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106520677"
---
# <a name="merging-a-multiple-language-module-into-the-same-package-multiple-times"></a><span data-ttu-id="e1c4e-103">Fusion multiple d’un module multiple Language dans le même package</span><span class="sxs-lookup"><span data-stu-id="e1c4e-103">Merging a Multiple Language Module into the Same Package Multiple Times</span></span>

<span data-ttu-id="e1c4e-104">Lorsqu’un module prend en charge plusieurs langues, vous pouvez le fusionner dans la même Windows Installer base de données plusieurs fois, tout en veillant à ce que chaque fusion utilise une langue différente.</span><span class="sxs-lookup"><span data-stu-id="e1c4e-104">When a module supports multiple languages, you can merge it into the same Windows Installer database multiple times, but make sure that each merge uses a different language.</span></span> <span data-ttu-id="e1c4e-105">Avant chaque fusion, demandez une autre langue à partir du module.</span><span class="sxs-lookup"><span data-stu-id="e1c4e-105">Before each merge, request a different language from the module.</span></span> <span data-ttu-id="e1c4e-106">La base de données. msi qui en résulte possède ensuite un enregistrement dans la [table ModuleSignature](modulesignature-table.md) pour chaque fusion du module.</span><span class="sxs-lookup"><span data-stu-id="e1c4e-106">The resulting .msi database then has a record in the [ModuleSignature Table](modulesignature-table.md) for each merge of the module.</span></span> <span data-ttu-id="e1c4e-107">Les composants qui sont partagés entre les langages existent une seule fois dans la [table des composants](component-table.md), mais sont associés à chaque langue dans la [table ModuleComponents](modulecomponents-table.md).</span><span class="sxs-lookup"><span data-stu-id="e1c4e-107">Components that are shared between languages exist only one time in the [Component Table](component-table.md), but are associated with each language in the [ModuleComponents Table](modulecomponents-table.md).</span></span>

<span data-ttu-id="e1c4e-108">Lors de la fusion de plusieurs langues d’un module dans le même package, chaque fusion doit respecter les mêmes restrictions sur les pages de code que les modules à une seule langue.</span><span class="sxs-lookup"><span data-stu-id="e1c4e-108">When merging multiple languages of a module into the same package, each merge must satisfy the same restrictions on code pages as single-language modules.</span></span> <span data-ttu-id="e1c4e-109">Les modules ne peuvent pas contenir de chaînes dans différentes pages de codes.</span><span class="sxs-lookup"><span data-stu-id="e1c4e-109">The modules cannot contain strings in different code pages.</span></span>

<span data-ttu-id="e1c4e-110">Lors de la fusion d’un module plusieurs fois dans un seul fichier. msi, vous devrez peut-être modifier l’ordre des fichiers dans la [table de fichiers](file-table.md) pour utiliser le fichier. cab existant à partir du module directement dans votre installation.</span><span class="sxs-lookup"><span data-stu-id="e1c4e-110">When merging a module multiple times into a single .msi file, you may need to modify the order of the files in the [File Table](file-table.md) to use the existing .cab from the module directly in your installation.</span></span> <span data-ttu-id="e1c4e-111">L’ordre des fichiers dans la table de fichiers doit correspondre à l’ordre des fichiers dans le fichier. cab.</span><span class="sxs-lookup"><span data-stu-id="e1c4e-111">The order of files in the File Table must match the order of files in the .cab.</span></span> <span data-ttu-id="e1c4e-112">Lors de la fusion d’un module plusieurs fois dans une base de données d’installation, la séquence peut être modifiée, car les fichiers partagés entre les langues peuvent déjà exister dans le module à partir d’une fusion antérieure, et ils ont un numéro de séquence relatif différent.</span><span class="sxs-lookup"><span data-stu-id="e1c4e-112">When merging a module multiple times into an installation database the sequence may be modified, because files shared between the languages may already exist in the module from a prior merge, and they have a different relative sequence number.</span></span>

 

 



