---
description: Vous pouvez extraire des fichiers d’un fichier CAB de deux manières. La méthode la plus simple et la plus simple consiste à tirer parti du traitement automatique des fichiers CAB intégré aux fonctions d’installation.
ms.assetid: 113333c8-28d1-4b0e-8da4-0c94389d8038
title: Extraction de fichiers à partir d’armoires
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d94f413b4ad0ee1511dde21af747cd2665a4704
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106516293"
---
# <a name="extracting-files-from-cabinets"></a><span data-ttu-id="23247-104">Extraction de fichiers à partir d’armoires</span><span class="sxs-lookup"><span data-stu-id="23247-104">Extracting Files from Cabinets</span></span>

<span data-ttu-id="23247-105">Vous pouvez extraire des fichiers d’un fichier CAB de deux manières.</span><span class="sxs-lookup"><span data-stu-id="23247-105">You can extract files from a cabinet in two ways.</span></span> <span data-ttu-id="23247-106">La méthode la plus simple et la plus simple consiste à tirer parti du traitement automatique des fichiers CAB intégré aux fonctions d’installation.</span><span class="sxs-lookup"><span data-stu-id="23247-106">The first and simplest way is to take advantage of the automatic cabinet processing built into the setup functions.</span></span>

<span data-ttu-id="23247-107">Les fonctions d’installation, telles que [**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea), [**SetupInstallFile**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfilea)et [**SetupInstallFromInfSection**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfrominfsectiona), vérifient la compression sur chaque fichier.</span><span class="sxs-lookup"><span data-stu-id="23247-107">The installation functions, such as [**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea), [**SetupInstallFile**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfilea), and [**SetupInstallFromInfSection**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfrominfsectiona), check the compression on each file.</span></span> <span data-ttu-id="23247-108">Si le fichier se trouve dans un fichier CAB, les fonctions recherchent d’abord un fichier de ce nom en dehors de l’armoire.</span><span class="sxs-lookup"><span data-stu-id="23247-108">If the file is in a cabinet, the functions first search for a file of that name outside the cabinet.</span></span> <span data-ttu-id="23247-109">S’il est trouvé, les fonctions installent le fichier externe, en ignorant le fichier à l’intérieur du fichier CAB.</span><span class="sxs-lookup"><span data-stu-id="23247-109">If found, the functions install the external file, ignoring the file inside the cabinet.</span></span> <span data-ttu-id="23247-110">Cela vous permet de mettre à jour un seul fichier à l’intérieur du cabinet sans recréer le fichier CAB.</span><span class="sxs-lookup"><span data-stu-id="23247-110">This enables you to update a single file inside the cabinet without rebuilding the cabinet.</span></span>

<span data-ttu-id="23247-111">Les fonctions d’installation suivent également les fichiers d’un fichier CAB qui ont été récupérés, de sorte qu’un fichier n’est extrait qu’une seule fois, même s’il est installé plusieurs fois.</span><span class="sxs-lookup"><span data-stu-id="23247-111">The setup functions also track which files in a cabinet have been retrieved, so that a file is extracted only once, even if it is installed several times.</span></span>

<span data-ttu-id="23247-112">La deuxième méthode pour extraire des fichiers d’un fichier CAB consiste à utiliser [**SetupIterateCabinet**](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta).</span><span class="sxs-lookup"><span data-stu-id="23247-112">The second way to extract files from a cabinet is by using [**SetupIterateCabinet**](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta).</span></span> <span data-ttu-id="23247-113">Cette fonction itère au sein de chaque fichier d’un fichier CAB, en envoyant une notification à une routine de rappel pour chaque fichier trouvé.</span><span class="sxs-lookup"><span data-stu-id="23247-113">This function iterates through each file in a cabinet, sending a notification to a callback routine for each file found.</span></span> <span data-ttu-id="23247-114">La routine de rappel retourne ensuite une valeur qui indique si le fichier doit être extrait ou ignoré.</span><span class="sxs-lookup"><span data-stu-id="23247-114">The callback routine then returns a value that indicates whether the file should be extracted or skipped.</span></span>

> [!Note]  
> <span data-ttu-id="23247-115">L’API d’installation ne fournit pas de routine de rappel par défaut pour gérer les notifications de fichier CAB.</span><span class="sxs-lookup"><span data-stu-id="23247-115">The Setup API does not supply a default callback routine to handle cabinet notifications.</span></span> <span data-ttu-id="23247-116">Si vous appelez [**SetupIterateCabinet**](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta) de manière explicite, vous devez fournir une routine de rappel pour traiter les notifications d’armoire retournées par la fonction.</span><span class="sxs-lookup"><span data-stu-id="23247-116">If you call [**SetupIterateCabinet**](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta) explicitly, you must supply a callback routine to process the cabinet notifications that the function returns.</span></span>

 

 

 



