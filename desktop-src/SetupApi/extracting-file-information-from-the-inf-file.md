---
description: Une fois le fichier INF ouvert, vous pouvez recueillir des informations à partir de celui-ci pour créer l’interface utilisateur ou pour diriger le processus d’installation. Les fonctions d’installation offrent plusieurs niveaux de fonctionnalités pour collecter des informations à partir d’un fichier INF.
ms.assetid: 3ef2768b-8c73-4258-937c-77a40963ffe4
title: Extraction d’informations de fichier à partir du fichier INF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: be4b404f44ca7d1d92fe0ce8eab08b73012ff144
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862998"
---
# <a name="extracting-file-information-from-the-inf-file"></a><span data-ttu-id="fe9ce-104">Extraction d’informations de fichier à partir du fichier INF</span><span class="sxs-lookup"><span data-stu-id="fe9ce-104">Extracting File Information from the INF file</span></span>

<span data-ttu-id="fe9ce-105">Une fois le fichier INF ouvert, vous pouvez recueillir des informations à partir de celui-ci pour créer l’interface utilisateur ou pour diriger le processus d’installation.</span><span class="sxs-lookup"><span data-stu-id="fe9ce-105">After the INF file is opened, you can gather information from it to build the user interface, or to direct the installation process.</span></span> <span data-ttu-id="fe9ce-106">Les fonctions d’installation offrent plusieurs niveaux de fonctionnalités pour collecter des informations à partir d’un fichier INF.</span><span class="sxs-lookup"><span data-stu-id="fe9ce-106">The setup functions provide several levels of functionality for gathering information from an INF file.</span></span>



| <span data-ttu-id="fe9ce-107">Pour collecter des informations...</span><span class="sxs-lookup"><span data-stu-id="fe9ce-107">To gather information…</span></span>                | <span data-ttu-id="fe9ce-108">Utilisez ces fonctions...</span><span class="sxs-lookup"><span data-stu-id="fe9ce-108">Use these functions…</span></span>                                                        |
|---------------------------------------|-----------------------------------------------------------------------------|
| <span data-ttu-id="fe9ce-109">À propos du fichier INF</span><span class="sxs-lookup"><span data-stu-id="fe9ce-109">About the INF file</span></span>                    | [<span data-ttu-id="fe9ce-110">**SetupGetInfInformation**</span><span class="sxs-lookup"><span data-stu-id="fe9ce-110">**SetupGetInfInformation**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupgetinfinformationa)                    |
|                                       | [<span data-ttu-id="fe9ce-111">**SetupQueryInfFileInformation**</span><span class="sxs-lookup"><span data-stu-id="fe9ce-111">**SetupQueryInfFileInformation**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupqueryinffileinformationa)        |
|                                       | <span data-ttu-id="fe9ce-112">[**SetupQueryInfVersionInformation**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueryinfversioninformationa).</span><span class="sxs-lookup"><span data-stu-id="fe9ce-112">[**SetupQueryInfVersionInformation**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueryinfversioninformationa).</span></span> |
| <span data-ttu-id="fe9ce-113">À propos des fichiers source et cible</span><span class="sxs-lookup"><span data-stu-id="fe9ce-113">About source and target files</span></span>         | [<span data-ttu-id="fe9ce-114">**SetupGetSourceFileLocation**</span><span class="sxs-lookup"><span data-stu-id="fe9ce-114">**SetupGetSourceFileLocation**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupgetsourcefilelocationa)            |
|                                       | [<span data-ttu-id="fe9ce-115">**SetupGetSourceFileSize**</span><span class="sxs-lookup"><span data-stu-id="fe9ce-115">**SetupGetSourceFileSize**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupgetsourcefilesizea)                    |
|                                       | [<span data-ttu-id="fe9ce-116">**SetupGetTargetPath**</span><span class="sxs-lookup"><span data-stu-id="fe9ce-116">**SetupGetTargetPath**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupgettargetpatha)                            |
|                                       | [<span data-ttu-id="fe9ce-117">**SetupGetSourceInfo**</span><span class="sxs-lookup"><span data-stu-id="fe9ce-117">**SetupGetSourceInfo**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupgetsourceinfoa)                            |
| <span data-ttu-id="fe9ce-118">À partir d’une ligne d’un fichier INF</span><span class="sxs-lookup"><span data-stu-id="fe9ce-118">From a line of an INF file</span></span>            | [<span data-ttu-id="fe9ce-119">**SetupGetLineText**</span><span class="sxs-lookup"><span data-stu-id="fe9ce-119">**SetupGetLineText**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupgetlinetexta)                                |
|                                       | [<span data-ttu-id="fe9ce-120">**SetupFindNextLine**</span><span class="sxs-lookup"><span data-stu-id="fe9ce-120">**SetupFindNextLine**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupfindnextline)                              |
|                                       | [<span data-ttu-id="fe9ce-121">**SetupFindNextMatchLine**</span><span class="sxs-lookup"><span data-stu-id="fe9ce-121">**SetupFindNextMatchLine**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupfindnextmatchlinea)                    |
|                                       | [<span data-ttu-id="fe9ce-122">**SetupGetLineByIndex**</span><span class="sxs-lookup"><span data-stu-id="fe9ce-122">**SetupGetLineByIndex**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupgetlinebyindexa)                          |
|                                       | [<span data-ttu-id="fe9ce-123">**SetupFindFirstLine**</span><span class="sxs-lookup"><span data-stu-id="fe9ce-123">**SetupFindFirstLine**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupfindfirstlinea)                            |
| <span data-ttu-id="fe9ce-124">À partir d’un champ d’une ligne dans un fichier INF</span><span class="sxs-lookup"><span data-stu-id="fe9ce-124">From a field of a line in an INF file</span></span> | [<span data-ttu-id="fe9ce-125">**SetupGetStringField**</span><span class="sxs-lookup"><span data-stu-id="fe9ce-125">**SetupGetStringField**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupgetstringfielda)                          |
|                                       | [<span data-ttu-id="fe9ce-126">**SetupGetIntField**</span><span class="sxs-lookup"><span data-stu-id="fe9ce-126">**SetupGetIntField**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupgetintfield)                                |
|                                       | [<span data-ttu-id="fe9ce-127">**SetupGetBinaryField**</span><span class="sxs-lookup"><span data-stu-id="fe9ce-127">**SetupGetBinaryField**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupgetbinaryfield)                          |
|                                       | [<span data-ttu-id="fe9ce-128">**SetupGetMultiSzField**</span><span class="sxs-lookup"><span data-stu-id="fe9ce-128">**SetupGetMultiSzField**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupgetmultiszfielda)                        |



 

<span data-ttu-id="fe9ce-129">L’exemple suivant utilise la fonction [**SetupGetSourceInfo**](/windows/desktop/api/Setupapi/nf-setupapi-setupgetsourceinfoa) pour récupérer la description explicite d’un média source à partir d’un fichier INF.</span><span class="sxs-lookup"><span data-stu-id="fe9ce-129">The following example uses the [**SetupGetSourceInfo**](/windows/desktop/api/Setupapi/nf-setupapi-setupgetsourceinfoa) function to retrieve the human-readable description of a source media from an INF file.</span></span>


```C++
#include <windows.h>
#include <setupapi.h>

BOOL test;  
HINF MyInf;
UINT SourceId;
PTSTR Buffer;
DWORD MaxBufSize;
DWORD BufSize;

int main()  
{ 

test = SetupGetSourceInfo (
     MyInf,   //Handle to the INF file to access                
     SourceId, //Id of the source media                 
     SRCINFO_DESCRIPTION, //which information to retrieve     
     Buffer, //a pointer to the buffer to receive the information                     
     MaxBufSize,  //the size allocated for the buffer 
     &BufSize    //buffer size actually needed
);
  
return 0;
}
```



<span data-ttu-id="fe9ce-130">Dans l’exemple, MyInf est le descripteur du fichier INF ouvert.</span><span class="sxs-lookup"><span data-stu-id="fe9ce-130">In the example, MyInf is the handle to the open INF file.</span></span> <span data-ttu-id="fe9ce-131">SourceId est l’identificateur d’un média source spécifique.</span><span class="sxs-lookup"><span data-stu-id="fe9ce-131">SourceId is the identifier for a specific source media.</span></span> <span data-ttu-id="fe9ce-132">La valeur SRCINFO \_ Description spécifie que la fonction [**SetupGetSourceInfo**](/windows/desktop/api/Setupapi/nf-setupapi-setupgetsourceinfoa) doit récupérer la description du média source.</span><span class="sxs-lookup"><span data-stu-id="fe9ce-132">The value SRCINFO\_DESCRIPTION specifies that the [**SetupGetSourceInfo**](/windows/desktop/api/Setupapi/nf-setupapi-setupgetsourceinfoa) function should retrieve the source media description.</span></span> <span data-ttu-id="fe9ce-133">La mémoire tampon pointe vers une chaîne qui reçoit la description, MaxBufSize indique les ressources allouées à la mémoire tampon, et BufSize indique les ressources nécessaires pour stocker la mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="fe9ce-133">Buffer points to a string that will receive the description, MaxBufSize indicates the resources allocated to the buffer, and BufSize indicates the resources necessary to store the buffer.</span></span>

<span data-ttu-id="fe9ce-134">Si BufSize est supérieur à MaxBufSize, la fonction retourne **false** et un appel suivant à [**GETLASTERROR**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) retourne l’erreur \_ mémoire tampon insuffisante \_ .</span><span class="sxs-lookup"><span data-stu-id="fe9ce-134">If BufSize is greater than MaxBufSize, the function will return **FALSE**, and a subsequent call to [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) will return ERROR\_INSUFFICIENT\_BUFFER.</span></span>

 

 
