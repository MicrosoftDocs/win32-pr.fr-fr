---
description: Pour déterminer si un compteur est installé sur un ordinateur particulier, appelez PdhValidatePath avec le chemin d’accès complet du compteur. La fonction retourne une erreur \_ de réussite si le compteur se trouve sur l’ordinateur spécifié.
ms.assetid: 5533a8d8-3621-4ce7-984c-c3895adef531
title: Détermination de l’emplacement d’un compteur sur un ordinateur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 795878e2f9c97989fe924737ec7f8e7f14bdc67c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103952013"
---
# <a name="determining-whether-a-counter-is-located-on-a-computer"></a><span data-ttu-id="5615c-104">Détermination de l’emplacement d’un compteur sur un ordinateur</span><span class="sxs-lookup"><span data-stu-id="5615c-104">Determining Whether a Counter Is Located on a Computer</span></span>

<span data-ttu-id="5615c-105">Pour déterminer si un compteur est installé sur un ordinateur particulier, appelez [**PdhValidatePath**](/windows/desktop/api/Pdh/nf-pdh-pdhvalidatepatha) avec le chemin d’accès complet du compteur.</span><span class="sxs-lookup"><span data-stu-id="5615c-105">To determine if a counter is installed on a particular computer, call [**PdhValidatePath**](/windows/desktop/api/Pdh/nf-pdh-pdhvalidatepatha) with the fully qualified counter path.</span></span> <span data-ttu-id="5615c-106">La fonction retourne une erreur \_ de réussite si le compteur se trouve sur l’ordinateur spécifié.</span><span class="sxs-lookup"><span data-stu-id="5615c-106">The function returns ERROR\_SUCCESS if the counter is located on the specified computer.</span></span>

<span data-ttu-id="5615c-107">[**PdhValidatePath**](/windows/desktop/api/Pdh/nf-pdh-pdhvalidatepatha) valide le chemin d’accès entier ; par conséquent, si un objet, une instance ou un compteur du chemin d’accès n’existe pas, la valeur de retour le indique.</span><span class="sxs-lookup"><span data-stu-id="5615c-107">[**PdhValidatePath**](/windows/desktop/api/Pdh/nf-pdh-pdhvalidatepatha) validates the entire path; therefore, if any object, instance, or counter in the path does not exist, the return value indicates so.</span></span> <span data-ttu-id="5615c-108">**PdhValidatePath** vérifie le chemin d’accès au compteur spécifié dans cet ordre : ordinateur, objet de performance, instance et compteur.</span><span class="sxs-lookup"><span data-stu-id="5615c-108">**PdhValidatePath** verifies the specified counter path in this order: computer, performance object, instance, and counter.</span></span>

 

 



