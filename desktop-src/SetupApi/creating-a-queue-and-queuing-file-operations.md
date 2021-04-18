---
description: La mise en file d’attente des opérations de fichier est utile, car elle vous permet de traiter l’installation dans son ensemble, plutôt que par la section INF.
ms.assetid: 6519c2fb-142d-4071-865f-c00a98c2fe35
title: Création d’une file d’attente et mise en file d’attente des opérations de fichiers
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f344e9d1c36ecac2d3cd3293196e1d08ff81a05
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106533656"
---
# <a name="creating-a-queue-and-queuing-file-operations"></a><span data-ttu-id="fab08-103">Création d’une file d’attente et mise en file d’attente des opérations de fichiers</span><span class="sxs-lookup"><span data-stu-id="fab08-103">Creating a Queue and Queuing File Operations</span></span>

<span data-ttu-id="fab08-104">La mise en file d’attente des opérations de fichier est utile, car elle vous permet de traiter l’installation dans son ensemble, plutôt que par la section INF.</span><span class="sxs-lookup"><span data-stu-id="fab08-104">Queuing the file operations is useful because it enables you to process the installation as a whole, instead of by INF section.</span></span>

<span data-ttu-id="fab08-105">Pour créer une file d’attente de fichiers, déclarez une variable pour stocker le descripteur de file d’attente, puis appelez la fonction [**SetupOpenFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupopenfilequeue) .</span><span class="sxs-lookup"><span data-stu-id="fab08-105">To create a file queue, declare a variable to store the queue handle, then call the [**SetupOpenFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupopenfilequeue) function.</span></span> <span data-ttu-id="fab08-106">Une fois la file d’attente créée, vous pouvez effectuer des opérations de copie, de renommage et de suppression, ainsi que d’analyser la file d’attente de fichiers pour vérifier les opérations mises en file d’attente.</span><span class="sxs-lookup"><span data-stu-id="fab08-106">After the queue is created, you can queue copy, rename, and delete operations, as well as scan the file queue to verify enqueued operations.</span></span>

<span data-ttu-id="fab08-107">Pour ajouter des opérations de fichier unique à la file d’attente, utilisez les fonctions [**SetupQueueCopy**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueuecopya), [**SetupQueueRename**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueuerenamea)et [**SetupQueueDelete**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueuedeletea) .</span><span class="sxs-lookup"><span data-stu-id="fab08-107">To add single file operations to the queue, use the [**SetupQueueCopy**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueuecopya), [**SetupQueueRename**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueuerenamea), and [**SetupQueueDelete**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueuedeletea) functions.</span></span>

<span data-ttu-id="fab08-108">Toutes les opérations de fichiers listées dans une section **copier** des fichiers, **supprimer des fichiers** ou **Renommer des fichiers** peuvent être ajoutées à la file d’attente à l’aide de [**SetupQueueCopySection**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueuecopysectiona), [**SetupQueueDeleteSection**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueuedeletesectiona)ou [**SetupQueueRenameSection**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueuerenamesectiona), respectivement.</span><span class="sxs-lookup"><span data-stu-id="fab08-108">All the file operations listed in a **Copy Files**, **Delete Files**, or **Rename Files** section can be added to the queue by using [**SetupQueueCopySection**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueuecopysectiona), [**SetupQueueDeleteSection**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueuedeletesectiona), or [**SetupQueueRenameSection**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueuerenamesectiona), respectively.</span></span>

<span data-ttu-id="fab08-109">Une autre façon de faire la file d’attente de tous les fichiers dans les sections **copier les fichiers** figurant dans une section d' **installation** d’un fichier INF consiste à utiliser la fonction [**SetupInstallFilesFromInfSection**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfilesfrominfsectiona).</span><span class="sxs-lookup"><span data-stu-id="fab08-109">Another way to queue all the files in the **Copy Files** sections listed in an **Install** section of an INF is to use the function, [**SetupInstallFilesFromInfSection**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfilesfrominfsectiona).</span></span>

<span data-ttu-id="fab08-110">L’exemple suivant utilise la fonction [**SetupQueueCopySection**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueuecopysectiona) pour empiler les opérations de copie de tous les fichiers listés dans une section **copier des fichiers** d’un fichier INF.</span><span class="sxs-lookup"><span data-stu-id="fab08-110">The following example uses the [**SetupQueueCopySection**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueuecopysectiona) function to enqueue copy operations for all the files listed in a **Copy Files** section of an INF file.</span></span>

``` syntax
test = SetupQueueCopySection(
     MyQueue,                  \\Handle to the open queue
     "A:\",                    \\Source root path
     MyInf,                    \\Inf containing the source info
     NULL,                     \\specifies that MyInf contains 
                               \\  the section to copy as well
     MySection,                \\the name of the section to queue
  
                               \\flags specifying the copy style
     SP_COPY_NOSKIP | SP_COPY_NOBROWSE,
);
```

<span data-ttu-id="fab08-111">Dans l’exemple, MyQueue est la file d’attente dans laquelle ajouter des opérations de copie, « A : \\ » spécifie le chemin d’accès à la source, et MyInf est le descripteur du fichier INF ouvert.</span><span class="sxs-lookup"><span data-stu-id="fab08-111">In the example, MyQueue is the queue to add copy operations to, "A:\\" specifies the path to the source, and MyInf is the handle to the open INF file.</span></span> <span data-ttu-id="fab08-112">Le paramètre *ListInfHandle* a la valeur **null**, ce qui indique que la section pour la copie se trouve dans MyInf.</span><span class="sxs-lookup"><span data-stu-id="fab08-112">The parameter *ListInfHandle* is set to **NULL**, indicating that the section for copying is in MyInf.</span></span> <span data-ttu-id="fab08-113">MySection est la section de MyInf contenant les fichiers à la file d’attente pour la copie.</span><span class="sxs-lookup"><span data-stu-id="fab08-113">MySection is the section in MyInf containing the files to queue for copying.</span></span>

<span data-ttu-id="fab08-114">Les indicateurs SP de \_ copie \_ NOSKIP et SP # \_ \_ Browse ont été combinés à l’aide d’un opérateur or pour indiquer que l’utilisateur ne doit pas être proposé d’options pour ignorer ou Rechercher des fichiers si des erreurs se produisent.</span><span class="sxs-lookup"><span data-stu-id="fab08-114">The flags SP\_COPY\_NOSKIP and SP\_COPY\_NOBROWSE have been combined using an OR operator to indicate that the user should not be offered options to skip or browse for files if errors occur.</span></span>

 

 



