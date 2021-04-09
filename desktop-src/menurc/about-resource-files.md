---
title: À propos des fichiers de ressources
description: Décrit comment inclure des ressources dans votre application Windows avec RC.
ms.assetid: af7c7aed-5d28-40ac-ad00-da0986fd89c1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7c43e9df59cf0b6507b6c6a53c42299b8792634f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104029215"
---
# <a name="about-resource-files"></a><span data-ttu-id="fe6ef-103">À propos des fichiers de ressources</span><span class="sxs-lookup"><span data-stu-id="fe6ef-103">About Resource Files</span></span>

<span data-ttu-id="fe6ef-104">Pour inclure des ressources dans votre application Windows avec RC, procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="fe6ef-104">To include resources in your Windows-based application with RC, do the following:</span></span>

1.  <span data-ttu-id="fe6ef-105">Créez des fichiers individuels pour vos curseurs, icônes, bitmaps, boîtes de dialogue et polices.</span><span class="sxs-lookup"><span data-stu-id="fe6ef-105">Create individual files for your cursors, icons, bitmaps, dialog boxes, and fonts.</span></span>
2.  <span data-ttu-id="fe6ef-106">Créez un script de définition de ressources (fichier. RC) qui décrit les ressources utilisées par votre application.</span><span class="sxs-lookup"><span data-stu-id="fe6ef-106">Create a resource-definition script (.rc file) that describes the resources used by your application.</span></span>
3.  <span data-ttu-id="fe6ef-107">Compilez le script avec RC.</span><span class="sxs-lookup"><span data-stu-id="fe6ef-107">Compile the script with RC.</span></span> <span data-ttu-id="fe6ef-108">Pour plus d’informations, consultez [utilisation de RC (ligne de commande RC)](using-rc-the-rc-command-line-.md).</span><span class="sxs-lookup"><span data-stu-id="fe6ef-108">For more information, see [Using RC (The RC Command Line)](using-rc-the-rc-command-line-.md).</span></span>
4.  <span data-ttu-id="fe6ef-109">Liez le fichier de ressources compilé (. res) au fichier exécutable de l’application avec votre éditeur de liens.</span><span class="sxs-lookup"><span data-stu-id="fe6ef-109">Link the compiled resource (.res) file into the application's executable file with your linker.</span></span>

<span data-ttu-id="fe6ef-110">Un fichier de ressources est un fichier texte avec l’extension. rc.</span><span class="sxs-lookup"><span data-stu-id="fe6ef-110">A resource file is a text file with the extension .rc.</span></span> <span data-ttu-id="fe6ef-111">Le fichier peut utiliser des caractères codés sur un octet, codés sur deux octets ou Unicode.</span><span class="sxs-lookup"><span data-stu-id="fe6ef-111">The file can use single-byte, double-byte, or Unicode characters.</span></span> <span data-ttu-id="fe6ef-112">La syntaxe et la sémantique du préprocesseur RC sont similaires à celles du compilateur Microsoft C/C++.</span><span class="sxs-lookup"><span data-stu-id="fe6ef-112">The syntax and semantics for the RC preprocessor are similar to those of the Microsoft C/C++ compiler.</span></span> <span data-ttu-id="fe6ef-113">Toutefois, RC prend en charge un sous-ensemble des directives de préprocesseur, des définitions et des pragmas dans un script.</span><span class="sxs-lookup"><span data-stu-id="fe6ef-113">However, RC supports a subset of the preprocessor directives, defines, and pragmas in a script.</span></span>

<span data-ttu-id="fe6ef-114">Le fichier de script définit les ressources.</span><span class="sxs-lookup"><span data-stu-id="fe6ef-114">The script file defines resources.</span></span> <span data-ttu-id="fe6ef-115">Pour une ressource qui existe dans un fichier distinct, tel qu’une icône ou un curseur, le script spécifie la ressource et le fichier qui la contient.</span><span class="sxs-lookup"><span data-stu-id="fe6ef-115">For a resource that exists in a separate file, such as an icon or cursor, the script specifies the resource and the file that contains it.</span></span> <span data-ttu-id="fe6ef-116">Pour certaines ressources, telles qu’un menu, la définition complète de la ressource existe dans le script.</span><span class="sxs-lookup"><span data-stu-id="fe6ef-116">For some resources, such as a menu, the entire definition of the resource exists within the script.</span></span>

<span data-ttu-id="fe6ef-117">Les rubriques suivantes décrivent les informations qu’un fichier de script peut contenir :</span><span class="sxs-lookup"><span data-stu-id="fe6ef-117">The following topics describe the information a script file can contain:</span></span>

-   <span data-ttu-id="fe6ef-118">[Commentaires](comments.md), qui sont des remarques à ignorer par RC.</span><span class="sxs-lookup"><span data-stu-id="fe6ef-118">[Comments](comments.md), which are notes to be ignored by RC.</span></span>
-   <span data-ttu-id="fe6ef-119">[Macros prédéfinies](predefined-macros.md), qui ne prennent pas d’arguments et ne peuvent pas être redéfinies.</span><span class="sxs-lookup"><span data-stu-id="fe6ef-119">[Predefined macros](predefined-macros.md), which take no arguments and cannot be redefined.</span></span>
-   <span data-ttu-id="fe6ef-120">Les [directives de préprocesseur](preprocessor-directives.md), qui indiquent à RC d’effectuer des actions sur le script avant de le compiler.</span><span class="sxs-lookup"><span data-stu-id="fe6ef-120">[Preprocessor directives](preprocessor-directives.md), which instruct RC to perform actions on the script before compiling it.</span></span>
-   <span data-ttu-id="fe6ef-121">Les [opérateurs de préprocesseur](preprocessor-operators.md), qui sont utilisés avec la directive **\# define** .</span><span class="sxs-lookup"><span data-stu-id="fe6ef-121">[Preprocessor operators](preprocessor-operators.md), which are used with the **\#define** directive.</span></span>
-   [<span data-ttu-id="fe6ef-122">Directives pragma</span><span class="sxs-lookup"><span data-stu-id="fe6ef-122">Pragma directives</span></span>](pragma-directives.md)
-   <span data-ttu-id="fe6ef-123">Les [instructions de définition de ressource](resource-definition-statements.md), qui renomment et décrivent les ressources.</span><span class="sxs-lookup"><span data-stu-id="fe6ef-123">[Resource-definition statements](resource-definition-statements.md), which name and describe resources.</span></span>

 

 




