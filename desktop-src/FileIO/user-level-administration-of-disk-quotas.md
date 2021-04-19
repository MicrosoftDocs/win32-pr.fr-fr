---
description: Comment obtenir davantage d’espace disque disponible après avoir dépassé le quota alloué.
ms.assetid: a73b6a11-36f1-4437-a83d-e89918b1b0ae
title: Administration au niveau de l’utilisateur des quotas de disque
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0cc130cf925899ccf0a86af20ff6772689ecdfbd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106521914"
---
# <a name="user-level-administration-of-disk-quotas"></a><span data-ttu-id="6b7cf-103">Administration au niveau de l’utilisateur des quotas de disque</span><span class="sxs-lookup"><span data-stu-id="6b7cf-103">User-level Administration of Disk Quotas</span></span>

<span data-ttu-id="6b7cf-104">Les quotas de disque sont transparents pour l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="6b7cf-104">Disk quotas are transparent to the user.</span></span> <span data-ttu-id="6b7cf-105">Lorsqu’un utilisateur demande la quantité d’espace libre sur un disque, le système signale uniquement l’allocation de quota disponible que l’utilisateur a disponible.</span><span class="sxs-lookup"><span data-stu-id="6b7cf-105">When a user asks how much space is free on a disk, the system reports only the available quota allowance the user has available.</span></span> <span data-ttu-id="6b7cf-106">Si l’utilisateur dépasse cette limite, le système renvoie une erreur de **\_ \_ saturation du disque** , tout comme pour indiquer que le disque est plein.</span><span class="sxs-lookup"><span data-stu-id="6b7cf-106">If the user exceeds this allowance, the system returns the **ERROR\_DISK\_FULL** error, just as it would to indicate that the disk was full.</span></span>

<span data-ttu-id="6b7cf-107">Pour obtenir plus d’espace disque disponible après avoir dépassé le quota alloué, l’utilisateur doit effectuer l’une des opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="6b7cf-107">To obtain more free disk space after exceeding the quota allowance, the user must do one of the following:</span></span>

-   <span data-ttu-id="6b7cf-108">Supprimez certains fichiers.</span><span class="sxs-lookup"><span data-stu-id="6b7cf-108">Delete some files.</span></span>
-   <span data-ttu-id="6b7cf-109">Demandez à un autre utilisateur de réclamer la propriété de certains fichiers.</span><span class="sxs-lookup"><span data-stu-id="6b7cf-109">Have another user claim ownership of some files.</span></span>
-   <span data-ttu-id="6b7cf-110">Demander à l’administrateur d’augmenter le quota alloué.</span><span class="sxs-lookup"><span data-stu-id="6b7cf-110">Have the administrator increase the quota allowance.</span></span>

<span data-ttu-id="6b7cf-111">Les programmes qui doivent récupérer la quantité réelle d’espace disque libre peuvent appeler la fonction [**GetDiskFreeSpaceEx**](/windows/desktop/api/FileAPI/nf-fileapi-getdiskfreespaceexa) et examiner le paramètre *TotalNumberOfFreeBytes* .</span><span class="sxs-lookup"><span data-stu-id="6b7cf-111">Programs that need to retrieve the actual amount of free disk space can call the [**GetDiskFreeSpaceEx**](/windows/desktop/api/FileAPI/nf-fileapi-getdiskfreespaceexa) function and look at the *TotalNumberOfFreeBytes* parameter.</span></span>

 

 



