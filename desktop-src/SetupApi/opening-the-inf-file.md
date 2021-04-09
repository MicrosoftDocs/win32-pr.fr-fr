---
description: Vous devez utiliser la fonction SetupOpenInfFile pour ouvrir le fichier INF avant de pouvoir récupérer des informations à partir de celui-ci ou y ajouter d’autres fichiers INF.
ms.assetid: ba4d511a-ad19-4619-a10a-cafef789821b
title: Ouverture du fichier INF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9d8493fda983f2942705b97ea243f6cb95e91c15
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103865718"
---
# <a name="opening-the-inf-file"></a><span data-ttu-id="4df92-103">Ouverture du fichier INF</span><span class="sxs-lookup"><span data-stu-id="4df92-103">Opening the INF File</span></span>

<span data-ttu-id="4df92-104">Vous devez utiliser la fonction [**SetupOpenInfFile**](/windows/desktop/api/Setupapi/nf-setupapi-setupopeninffilea) pour ouvrir le fichier INF avant de pouvoir récupérer des informations à partir de celui-ci ou y ajouter d’autres fichiers INF.</span><span class="sxs-lookup"><span data-stu-id="4df92-104">You must use the [**SetupOpenInfFile**](/windows/desktop/api/Setupapi/nf-setupapi-setupopeninffilea) function to open the INF file before you can retrieve information from it, or append other INF files to it.</span></span>

<span data-ttu-id="4df92-105">L’exemple suivant ouvre un fichier INF à l’aide de [**SetupOpenInfFile**](/windows/desktop/api/Setupapi/nf-setupapi-setupopeninffilea) et retourne un descripteur, MyInf, au fichier INF ouvert.</span><span class="sxs-lookup"><span data-stu-id="4df92-105">The following opens an INF file using [**SetupOpenInfFile**](/windows/desktop/api/Setupapi/nf-setupapi-setupopeninffilea) and returns a handle, MyInf, to the opened INF file.</span></span> <span data-ttu-id="4df92-106">Le paramètre *InfClass* de **SetupOpenInfFile** est spécifié comme **null** pour indiquer que la classe du fichier INF doit être ignorée.</span><span class="sxs-lookup"><span data-stu-id="4df92-106">The *InfClass* parameter of **SetupOpenInfFile** is specified as **NULL** to indicate that the Class of the INF file should be ignored.</span></span>


```C++
HINF MyInf;                //variable to hold the INF handle
UINT ErrorLine;            //variable to hold errors returned
BOOL test=0;                 //variable to receive function success
 
MyInf = SetupOpenInfFile (
      szInfFileName,       //the filename of the inf file to open
      NULL,                //optional class information
      INF_STYLE_WIN4,      //the inf style
      &ErrorLine           //line number of the syntax error
);
```



<span data-ttu-id="4df92-107">Après l’ouverture d’un fichier INF, vous pouvez appeler la fonction [**SetupOpenAppendInfFile**](/windows/desktop/api/Setupapi/nf-setupapi-setupopenappendinffilea) pour ajouter un fichier au fichier INF ouvert.</span><span class="sxs-lookup"><span data-stu-id="4df92-107">After an INF file is opened, you can call the [**SetupOpenAppendInfFile**](/windows/desktop/api/Setupapi/nf-setupapi-setupopenappendinffilea) function to append a file to the open INF file.</span></span> <span data-ttu-id="4df92-108">Pour ajouter plusieurs fichiers, répétez ce processus.</span><span class="sxs-lookup"><span data-stu-id="4df92-108">To append several files, repeat this process.</span></span> <span data-ttu-id="4df92-109">Si vous appelez la fonction **SetupOpenAppendInfFile** et que le nom de fichier qui lui est transmis est **null**, la fonction recherchera la section version du fichier INF ouvert (ainsi que tous les fichiers INF ajoutés) pour une clé LayoutFile.</span><span class="sxs-lookup"><span data-stu-id="4df92-109">If you call the **SetupOpenAppendInfFile** function and the filename passed to it is **NULL**, then the function will search the Version section of the open INF file (and any appended INF files) for a LayoutFile key.</span></span> <span data-ttu-id="4df92-110">Si la fonction trouve une clé, elle ajoute le fichier spécifié par cette clé (généralement la disposition. INF).</span><span class="sxs-lookup"><span data-stu-id="4df92-110">If the function finds a key, it will append the file specified by that key (usually LAYOUT.INF).</span></span> <span data-ttu-id="4df92-111">Lorsque plusieurs fichiers INF ont été combinés, **SetupOpenAppendInfFile** commence par le dernier fichier INF ajouté lors de la recherche d’une section de version.</span><span class="sxs-lookup"><span data-stu-id="4df92-111">When multiple INF files have been combined, **SetupOpenAppendInfFile** starts with the last appended INF file when it searches for a Version section.</span></span>

 

 



