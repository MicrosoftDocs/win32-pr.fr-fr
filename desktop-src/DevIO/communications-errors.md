---
description: Dans d’autres cas, une opération de lecture ou d’écriture peut être effectuée avec un nombre de caractères inférieur au nombre demandé, même si aucun délai d’attente n’a été dépassé.
ms.assetid: 05f84661-34ff-4e1f-9ec8-e4682138dfee
title: Erreurs de communication
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7eeace990620928ce898a3e8a31049a0083cdf07
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104483288"
---
# <a name="communications-errors"></a><span data-ttu-id="d80d0-103">Erreurs de communication</span><span class="sxs-lookup"><span data-stu-id="d80d0-103">Communications Errors</span></span>

<span data-ttu-id="d80d0-104">Dans d’autres cas, une opération de lecture ou d’écriture peut être effectuée avec un nombre de caractères inférieur au nombre demandé, même si aucun délai d’attente n’a été dépassé.</span><span class="sxs-lookup"><span data-stu-id="d80d0-104">There are other circumstances where a read or write operation can be completed with fewer than the requested number of characters, even though a time-out has not occurred.</span></span> <span data-ttu-id="d80d0-105">En voici quelques exemples :</span><span class="sxs-lookup"><span data-stu-id="d80d0-105">Following are some examples:</span></span>

-   <span data-ttu-id="d80d0-106">Certains pilotes prennent en charge l’utilisation de caractères spéciaux, qui effectuent immédiatement une opération de lecture avec uniquement les caractères qui ont été lus jusqu’au moment où ils sont reçus.</span><span class="sxs-lookup"><span data-stu-id="d80d0-106">Some drivers support the use of special characters, which complete a read operation immediately with only the characters that have been read up to the point when they are received.</span></span>
-   <span data-ttu-id="d80d0-107">La fonction [**PurgeComm**](/windows/desktop/api/Winbase/nf-winbase-purgecomm) peut être appelée pour terminer prématurément les opérations de lecture ou d’écriture en attente.</span><span class="sxs-lookup"><span data-stu-id="d80d0-107">The [**PurgeComm**](/windows/desktop/api/Winbase/nf-winbase-purgecomm) function can be called to prematurely terminate pending read or write operations.</span></span> <span data-ttu-id="d80d0-108">Cette fonction peut également supprimer le contenu des mémoires tampons de sortie ou d’entrée, ou les deux.</span><span class="sxs-lookup"><span data-stu-id="d80d0-108">This function can also delete the contents of the output or input buffers, or both.</span></span>
-   <span data-ttu-id="d80d0-109">Si une erreur de communication se produit pendant une opération de lecture ou d’écriture, toutes les opérations d’e/s sur la ressource de communication sont arrêtées.</span><span class="sxs-lookup"><span data-stu-id="d80d0-109">If a communications error occurs during a read or write operation, all I/O operations on the communications resource are terminated.</span></span> <span data-ttu-id="d80d0-110">Les conditions d’arrêt, les erreurs de parité ou les erreurs de trame sont des exemples de telles erreurs.</span><span class="sxs-lookup"><span data-stu-id="d80d0-110">Break conditions, parity errors, or framing errors are examples of such errors.</span></span> <span data-ttu-id="d80d0-111">Lorsqu’une erreur se produit, le processus doit appeler la fonction [**ClearCommError**](/windows/desktop/api/Winbase/nf-winbase-clearcommerror) pour effacer l’indicateur d’erreur avant de pouvoir commencer des opérations d’e/s supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="d80d0-111">When an error occurs, the process must call the [**ClearCommError**](/windows/desktop/api/Winbase/nf-winbase-clearcommerror) function to clear the error flag before it can begin additional I/O operations.</span></span> <span data-ttu-id="d80d0-112">**ClearCommError** signale l’erreur spécifique qui s’est produite et l’état actuel de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="d80d0-112">**ClearCommError** reports the specific error that occurred and the current status of the device.</span></span>

 

 



