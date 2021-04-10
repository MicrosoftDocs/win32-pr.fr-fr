---
description: Un fichier partiellement alloué affecte les quotas de l’utilisateur par la taille nominale du fichier, et non par la quantité réelle d’espace disque allouée.
ms.assetid: 7dbe1133-f5cb-4925-9448-5d40f1c553ff
title: Fichiers partiellement alloués et quotas de disque
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 326780e2b2c5119256272c0d297613d2c32e6e6e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104113642"
---
# <a name="sparse-files-and-disk-quotas"></a><span data-ttu-id="7ebd1-103">Fichiers partiellement alloués et quotas de disque</span><span class="sxs-lookup"><span data-stu-id="7ebd1-103">Sparse Files and Disk Quotas</span></span>

<span data-ttu-id="7ebd1-104">Un fichier partiellement alloué affecte les quotas de l’utilisateur par la taille nominale du fichier, et non par la quantité réelle d’espace disque allouée.</span><span class="sxs-lookup"><span data-stu-id="7ebd1-104">A sparse file affects user quotas by the nominal size of the file, not the actual allocated amount of disk space.</span></span> <span data-ttu-id="7ebd1-105">Autrement dit, la création d’un fichier de 50 Mo avec zéro octet consomme 50 Mo du quota de cet utilisateur.</span><span class="sxs-lookup"><span data-stu-id="7ebd1-105">That is, creating a 50-MB file with all zero bytes consumes 50 MB of that user's quota.</span></span> <span data-ttu-id="7ebd1-106">Cela signifie que lorsque l’utilisateur écrit des données dans le fichier partiellement alloué, il n’a pas besoin de se soucier du dépassement de sa limite de quota, car il a déjà été facturé pour l’espace.</span><span class="sxs-lookup"><span data-stu-id="7ebd1-106">This means that as the user writes data to the sparse file, he need not worry about exceeding his hard quota limit, because he has already been charged for the space.</span></span> <span data-ttu-id="7ebd1-107">Les administrateurs système ne doivent pas compter sur la taille d’un fichier partiellement alloué restant.</span><span class="sxs-lookup"><span data-stu-id="7ebd1-107">System administrators should not count on the size of a sparse file remaining small.</span></span> <span data-ttu-id="7ebd1-108">Par conséquent, ils ne doivent pas accorder à leurs utilisateurs des limites de quota en dur qui dépassent l’espace physique disponible, malgré l’utilisation de fichiers partiellement alloués.</span><span class="sxs-lookup"><span data-stu-id="7ebd1-108">Therefore they should not grant their users hard quota limits that exceed the physical space available, despite the use of sparse files.</span></span>

 

 



