---
description: L’interface utilisateur de Windows permet aux utilisateurs d’accéder à un large éventail d’objets nécessaires pour exécuter des applications et gérer le système d’exploitation.
title: Guide du développeur de l’interpréteur de commandes
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 8f88ef25-3645-4f54-9453-41f919c0fc0a
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 1be17ca90b7138294be3e1b34fa3fcb4dcb4227a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104991149"
---
# <a name="shell-developers-guide"></a><span data-ttu-id="403ca-103">Guide du développeur de l’interpréteur de commandes</span><span class="sxs-lookup"><span data-stu-id="403ca-103">Shell Developer's Guide</span></span>

<span data-ttu-id="403ca-104">L’interface utilisateur de Windows permet aux utilisateurs d’accéder à un large éventail d’objets nécessaires pour exécuter des applications et gérer le système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="403ca-104">The Windows UI provides users with access to a wide variety of objects necessary to run applications and manage the operating system.</span></span> <span data-ttu-id="403ca-105">Les plus nombreux et les plus familiers de ces objets sont les dossiers et les fichiers qui résident sur les lecteurs de disque de l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="403ca-105">The most numerous and familiar of these objects are the folders and files that reside on computer disk drives.</span></span> <span data-ttu-id="403ca-106">Il existe également un certain nombre d’objets virtuels qui permettent à l’utilisateur d’effectuer des tâches telles que l’envoi de fichiers à des imprimantes distantes ou l’accès à la corbeille.</span><span class="sxs-lookup"><span data-stu-id="403ca-106">There are also a number of virtual objects that allow the user to do tasks such as sending files to remote printers or accessing the Recycle Bin.</span></span> <span data-ttu-id="403ca-107">L’interpréteur de commandes organise ces objets dans un espace de noms hiérarchique et fournit aux utilisateurs et aux applications un moyen cohérent et efficace d’accéder aux objets et de les gérer.</span><span class="sxs-lookup"><span data-stu-id="403ca-107">The Shell organizes these objects into a hierarchical namespace, and provides users and applications with a consistent and efficient way to access and manage objects.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="403ca-108">Dans cette section</span><span class="sxs-lookup"><span data-stu-id="403ca-108">In this section</span></span>

-   [<span data-ttu-id="403ca-109">Considérations relatives à la sécurité : Microsoft Windows Shell</span><span class="sxs-lookup"><span data-stu-id="403ca-109">Security Considerations: Microsoft Windows Shell</span></span>](sec-shell.md)
-   [<span data-ttu-id="403ca-110">Conseils pour l’implémentation des extensions de In-Process</span><span class="sxs-lookup"><span data-stu-id="403ca-110">Guidance for Implementing In-Process Extensions</span></span>](shell-and-managed-code.md)
-   [<span data-ttu-id="403ca-111">Versions de l’interpréteur de commandes et des contrôles communs</span><span class="sxs-lookup"><span data-stu-id="403ca-111">Shell and Common Controls Versions</span></span>](versions.md)
-   [<span data-ttu-id="403ca-112">Implémentation des interfaces d’objets de dossier de base</span><span class="sxs-lookup"><span data-stu-id="403ca-112">Implementing the Basic Folder Object Interfaces</span></span>](nse-implement.md)
-   [<span data-ttu-id="403ca-113">Implémentation d’un format de fichier personnalisé</span><span class="sxs-lookup"><span data-stu-id="403ca-113">Implementing a Custom File Format</span></span>](customizing-file-types-bumper.md)
-   [<span data-ttu-id="403ca-114">Extensibilité de l’interpréteur de commandes (création d’une source de données)</span><span class="sxs-lookup"><span data-stu-id="403ca-114">Shell Extensibility (Creating a Data Source)</span></span>](shell-extensibility-bumper.md)
-   [<span data-ttu-id="403ca-115">Implémentation des éléments du panneau de configuration</span><span class="sxs-lookup"><span data-stu-id="403ca-115">Implementing Control Panel Items</span></span>](control-panel-applications.md)
-   [<span data-ttu-id="403ca-116">Prise en charge des applications Shell</span><span class="sxs-lookup"><span data-stu-id="403ca-116">Supporting Shell Applications</span></span>](application-support-bumper.md)
-   [<span data-ttu-id="403ca-117">Rubriques sur l’interpréteur de commandes hérité</span><span class="sxs-lookup"><span data-stu-id="403ca-117">Legacy Shell Topics</span></span>](miscellaneous-topics-bumper.md)

## <a name="document-conventions"></a><span data-ttu-id="403ca-118">Conventions de document</span><span class="sxs-lookup"><span data-stu-id="403ca-118">Document Conventions</span></span>

<span data-ttu-id="403ca-119">Le guide des développeurs de Shell suit les conventions de document du kit de développement logiciel (SDK) Windows habituel.</span><span class="sxs-lookup"><span data-stu-id="403ca-119">The Shell Developers's Guide follows the usual Windows Software Development Kit (SDK) document conventions.</span></span> <span data-ttu-id="403ca-120">Deux conventions en particulier doivent être indiquées :</span><span class="sxs-lookup"><span data-stu-id="403ca-120">Two conventions in particular should be noted:</span></span>

-   <span data-ttu-id="403ca-121">L’exemple de code omet le code de correction des erreurs normal.</span><span class="sxs-lookup"><span data-stu-id="403ca-121">Sample code omits normal error-correction code.</span></span> <span data-ttu-id="403ca-122">Ce code a été supprimé uniquement pour rendre le code plus lisible.</span><span class="sxs-lookup"><span data-stu-id="403ca-122">This code has been removed only to make the code more readable.</span></span> <span data-ttu-id="403ca-123">Vous devez inclure tous les codes de correction des erreurs appropriés dans vos propres applications.</span><span class="sxs-lookup"><span data-stu-id="403ca-123">You should include all appropriate error-correction code in your own applications.</span></span>
-   <span data-ttu-id="403ca-124">Pour afficher des exemples d’entrées de Registre, les noms de clé, de sous-clé et d’entrée, ainsi que les valeurs sont affichés avec une police standard.</span><span class="sxs-lookup"><span data-stu-id="403ca-124">To make sample registry entries clear, key, subkey, and entry names as well as values are displayed with a standard font.</span></span> <span data-ttu-id="403ca-125">Les noms d’éléments définis par l’utilisateur ou l’application sont en italique.</span><span class="sxs-lookup"><span data-stu-id="403ca-125">User or application-defined item names are italicized.</span></span>

 

 



