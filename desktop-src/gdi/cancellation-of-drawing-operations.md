---
description: Lorsque des applications de dessin complexes effectuent des opérations graphiques de longue durée, elles consomment des ressources système précieuses.
ms.assetid: 3beef852-27fe-4ee2-b38b-3dc50e5d2fcf
title: Annulation des opérations de dessin
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 98e3bdb7a57c7c427e7cd15ffddb62b1c492c25b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104991276"
---
# <a name="cancellation-of-drawing-operations"></a><span data-ttu-id="a118e-103">Annulation des opérations de dessin</span><span class="sxs-lookup"><span data-stu-id="a118e-103">Cancellation of Drawing Operations</span></span>

<span data-ttu-id="a118e-104">Lorsque des applications de dessin complexes effectuent des opérations graphiques de longue durée, elles consomment des ressources système précieuses.</span><span class="sxs-lookup"><span data-stu-id="a118e-104">When complex drawing applications perform lengthy graphics operations, they consume valuable system resources.</span></span> <span data-ttu-id="a118e-105">En tirant parti des fonctionnalités multitâches du système, une application peut utiliser des threads et la fonction [**CancelDC**](/windows/desktop/api/Wingdi/nf-wingdi-canceldc) pour gérer ces opérations.</span><span class="sxs-lookup"><span data-stu-id="a118e-105">By taking advantage of the system's multitasking features, an application can use threads and the [**CancelDC**](/windows/desktop/api/Wingdi/nf-wingdi-canceldc) function to manage these operations.</span></span> <span data-ttu-id="a118e-106">Par exemple, si l’opération graphique effectuée par le thread A consomme les ressources nécessaires, thread B peut appeler la fonction CancelDC pour arrêter cette opération.</span><span class="sxs-lookup"><span data-stu-id="a118e-106">For example, if the graphics operation performed by thread A is consuming needed resources, thread B can call the CancelDC function to halt that operation.</span></span>

 

 



