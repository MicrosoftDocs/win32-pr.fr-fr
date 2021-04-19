---
description: Les fonctions de configuration gèrent les armoires en interne. Pour énumérer et extraire explicitement des fichiers d’un fichier CAB, vous pouvez appeler la fonction SetupIterateCabinet.
ms.assetid: 14bd925a-e7fe-48a3-9ed6-4e42ce796290
title: Utilisation des fichiers CAB
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 03467f6591b4503cb13935cca550f8c1ba1dff81
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106541930"
---
# <a name="using-cabinet-files"></a><span data-ttu-id="a0695-104">Utilisation des fichiers CAB</span><span class="sxs-lookup"><span data-stu-id="a0695-104">Using Cabinet Files</span></span>

<span data-ttu-id="a0695-105">Les fonctions de configuration gèrent les armoires en interne.</span><span class="sxs-lookup"><span data-stu-id="a0695-105">The setup functions handle cabinets internally.</span></span> <span data-ttu-id="a0695-106">Pour énumérer et extraire explicitement des fichiers d’un fichier CAB, vous pouvez appeler la fonction [**SetupIterateCabinet**](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta) .</span><span class="sxs-lookup"><span data-stu-id="a0695-106">To explicitly enumerate and extract files from a cabinet, you can call the [**SetupIterateCabinet**](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta) function.</span></span>

<span data-ttu-id="a0695-107">La rubrique suivante décrit le traitement du fichier CAB interne aux fonctions d’installation et l’utilisation de [**SetupIterateCabinet**](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta).</span><span class="sxs-lookup"><span data-stu-id="a0695-107">The following topic describes the cabinet processing internal to the setup functions and how to use [**SetupIterateCabinet**](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta).</span></span> <span data-ttu-id="a0695-108">Les notifications envoyées par **SetupIterateCabinet** et le format requis d’une routine de rappel d’armoire pour traiter ces notifications sont également abordés.</span><span class="sxs-lookup"><span data-stu-id="a0695-108">Also discussed are the notifications sent by **SetupIterateCabinet** and the required format of a cabinet callback routine to process those notifications.</span></span>

-   [<span data-ttu-id="a0695-109">Extraction de fichiers à partir d’armoires</span><span class="sxs-lookup"><span data-stu-id="a0695-109">Extracting Files From Cabinets</span></span>](extracting-files-from-cabinets.md)
-   [<span data-ttu-id="a0695-110">Création d’une routine de rappel d’armoire</span><span class="sxs-lookup"><span data-stu-id="a0695-110">Creating a Cabinet Callback Routine</span></span>](creating-a-cabinet-callback-routine.md)

 

 



