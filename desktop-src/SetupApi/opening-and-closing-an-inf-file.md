---
description: Pour que les fonctions d’installation puissent accéder aux informations contenues dans le fichier INF, vous devez l’ouvrir avec un appel à la fonction SetupOpenInfFile. Cette fonction renvoie un descripteur au fichier INF.
ms.assetid: d838c05c-51e4-49a8-b773-af4924bff7e2
title: Ouverture et fermeture d’un fichier INF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 893b72d000f433fb4da7ecfee0db4d856f878814
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104529325"
---
# <a name="opening-and-closing-an-inf-file"></a><span data-ttu-id="518af-104">Ouverture et fermeture d’un fichier INF</span><span class="sxs-lookup"><span data-stu-id="518af-104">Opening and Closing an INF file</span></span>

<span data-ttu-id="518af-105">Pour que les fonctions d’installation puissent accéder aux informations contenues dans le fichier INF, vous devez l’ouvrir avec un appel à la fonction [**SetupOpenInfFile**](/windows/desktop/api/Setupapi/nf-setupapi-setupopeninffilea) .</span><span class="sxs-lookup"><span data-stu-id="518af-105">Before the setup functions can access information in the INF, you must open it with a call to the [**SetupOpenInfFile**](/windows/desktop/api/Setupapi/nf-setupapi-setupopeninffilea) function.</span></span> <span data-ttu-id="518af-106">Cette fonction renvoie un descripteur au fichier INF.</span><span class="sxs-lookup"><span data-stu-id="518af-106">This function returns a handle to the INF file.</span></span>

<span data-ttu-id="518af-107">Si vous ne connaissez pas le nom du fichier INF que vous devez ouvrir, vous pouvez utiliser la fonction [**SetupGetInfFileList**](/windows/desktop/api/Setupapi/nf-setupapi-setupgetinffilelista) pour obtenir la liste des fichiers INF dans un répertoire.</span><span class="sxs-lookup"><span data-stu-id="518af-107">If you do not know the name of the INF file that you need to open, you can use the [**SetupGetInfFileList**](/windows/desktop/api/Setupapi/nf-setupapi-setupgetinffilelista) function to obtain a list of INF files in a directory.</span></span>

<span data-ttu-id="518af-108">Après avoir ouvert un fichier INF, vous pouvez ajouter des fichiers INF supplémentaires au fichier INF ouvert à l’aide de la fonction [**SetupOpenAppendInfFile**](/windows/desktop/api/Setupapi/nf-setupapi-setupopenappendinffilea) .</span><span class="sxs-lookup"><span data-stu-id="518af-108">After you open an INF file, you can append additional INF files to the opened INF file by using the [**SetupOpenAppendInfFile**](/windows/desktop/api/Setupapi/nf-setupapi-setupopenappendinffilea) function.</span></span> <span data-ttu-id="518af-109">Cette fonction est similaire à une instruction include.</span><span class="sxs-lookup"><span data-stu-id="518af-109">This is functionally similar to an include statement.</span></span> <span data-ttu-id="518af-110">Lorsque les fonctions de configuration suivantes font référence à un fichier INF ouvert, elles peuvent également accéder à toutes les informations stockées dans les fichiers ajoutés.</span><span class="sxs-lookup"><span data-stu-id="518af-110">When subsequent setup functions reference an open INF file, they will also be able to access any information stored in the appended files.</span></span>

<span data-ttu-id="518af-111">Si vous ne spécifiez pas de fichier INF lors de l’appel à la fonction [**SetupOpenAppendInfFile**](/windows/desktop/api/Setupapi/nf-setupapi-setupopenappendinffilea) , **SetupOpenAppendInfFile** ajoute le ou les fichiers spécifiés par la clé **LayoutFile** dans la section **version** du fichier INF ouvert.</span><span class="sxs-lookup"><span data-stu-id="518af-111">If you do not specify an INF file during the call to the [**SetupOpenAppendInfFile**](/windows/desktop/api/Setupapi/nf-setupapi-setupopenappendinffilea) function, **SetupOpenAppendInfFile** appends the file(s) specified by the **LayoutFile** key in the **Version** section of the open INF file.</span></span>

<span data-ttu-id="518af-112">Lorsque vous n’avez plus besoin des informations contenues dans le fichier INF, appelez la fonction [**SetupCloseInfFile**](/windows/desktop/api/Setupapi/nf-setupapi-setupcloseinffile) pour libérer les ressources allouées pendant l’appel à [**SetupOpenAppendInfFile**](/windows/desktop/api/Setupapi/nf-setupapi-setupopenappendinffilea).</span><span class="sxs-lookup"><span data-stu-id="518af-112">When you no longer need the information in the INF file, call the [**SetupCloseInfFile**](/windows/desktop/api/Setupapi/nf-setupapi-setupcloseinffile) function to release resources allocated during the call to [**SetupOpenAppendInfFile**](/windows/desktop/api/Setupapi/nf-setupapi-setupopenappendinffilea).</span></span>

 

 



