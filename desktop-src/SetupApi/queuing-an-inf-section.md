---
description: Outre la mise en file d’attente des opérations de fichiers individuellement, vous pouvez également mettre en file d’attente tous les fichiers listés dans une section INF.
ms.assetid: 456e1a19-7e9b-40c8-9295-42bb8f740f58
title: Mise en file d’attente d’une section INF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e5566931131885cf6f300b5a6386639bbd564e1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104529776"
---
# <a name="queuing-an-inf-section"></a><span data-ttu-id="59c27-103">Mise en file d’attente d’une section INF</span><span class="sxs-lookup"><span data-stu-id="59c27-103">Queuing an INF Section</span></span>

<span data-ttu-id="59c27-104">Outre la mise en file d’attente des opérations de fichiers individuellement, vous pouvez également mettre en file d’attente tous les fichiers listés dans une section INF.</span><span class="sxs-lookup"><span data-stu-id="59c27-104">In addition to queuing file operations individually, you can also queue all the files listed in an INF section.</span></span>

<span data-ttu-id="59c27-105">Vous pouvez faire la file d’attente de tous les fichiers listés dans une section **copier des fichiers** d’un fichier INF en appelant [**SetupQueueCopySection**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueuecopysectiona).</span><span class="sxs-lookup"><span data-stu-id="59c27-105">You can queue all the files listed in a **Copy Files** section of an INF file by calling [**SetupQueueCopySection**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueuecopysectiona).</span></span> <span data-ttu-id="59c27-106">Pour que cette fonction aboutisse, la section **copier les fichiers** doit être au format approprié et le fichier INF, ou l’un de ses fichiers ajoutés, doit contenir les sections **SourceDisksFiles** et **SourceDisksNames** .</span><span class="sxs-lookup"><span data-stu-id="59c27-106">For this function to be successful, the **Copy Files** section must be in the proper format and the INF file, or one of its appended files, must contain the **SourceDisksFiles** and **SourceDisksNames** sections.</span></span>

<span data-ttu-id="59c27-107">De même, si vous souhaitez supprimer tous les fichiers spécifiés dans la section **supprimer des fichiers** d’un fichier INF, vous pouvez appeler [**SetupQueueDeleteSection**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueuedeletesectiona).</span><span class="sxs-lookup"><span data-stu-id="59c27-107">Similarly, if you want to delete all the files specified in a **Delete Files** section of an INF file, you can call [**SetupQueueDeleteSection**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueuedeletesectiona).</span></span> <span data-ttu-id="59c27-108">Pour renommer tous les fichiers d’une section **Renommer des fichiers** d’un fichier INF, utilisez [**SetupQueueRenameSection**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueuerenamesectiona).</span><span class="sxs-lookup"><span data-stu-id="59c27-108">To rename all the files in a **Rename Files** section of an INF file use [**SetupQueueRenameSection**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueuerenamesectiona).</span></span>

 

 



