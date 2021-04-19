---
description: Opérations de Pseudo-blocage Pseudoblocking dans Windows Sockets (Winsock).
ms.assetid: fa8f29f1-bb4f-4814-ab8a-52d3c83232bb
title: Pseudo-blocage et blocage réel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 082992aba884aebec30d35bc65d2cb6c49e29051
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106518612"
---
# <a name="pseudo-blocking-and-true-blocking"></a><span data-ttu-id="297d6-103">Pseudo-blocage et blocage réel</span><span class="sxs-lookup"><span data-stu-id="297d6-103">Pseudo Blocking and True Blocking</span></span>

<span data-ttu-id="297d6-104">Dans 16 environnements Windows, le blocage réel n’est pas pris en charge par le système d’exploitation. par conséquent, une opération de blocage qui ne peut pas être effectuée immédiatement est gérée comme suit :</span><span class="sxs-lookup"><span data-stu-id="297d6-104">In 16 Windows environments, true blocking is not supported by the operating system; therefore, a blocking operation that cannot be completed immediately is handled as follows:</span></span>

-   <span data-ttu-id="297d6-105">Le fournisseur de services lance l’opération, puis entre une boucle au cours de laquelle il distribue les messages Windows (ce qui produit le processeur à un autre thread si nécessaire)</span><span class="sxs-lookup"><span data-stu-id="297d6-105">The service provider initiates the operation, and then enters a loop during which it dispatches any Windows messages (yielding the processor to another thread if necessary)</span></span>
-   <span data-ttu-id="297d6-106">Il vérifie ensuite la fin de la fonction Windows Sockets.</span><span class="sxs-lookup"><span data-stu-id="297d6-106">It then checks for the completion of the Windows Sockets function.</span></span>
-   <span data-ttu-id="297d6-107">Si la fonction est terminée, ou si [**WSPCancelBlockingCall**](/previous-versions/windows/desktop/legacy/ms742269(v=vs.85)) a été appelé, la boucle est arrêtée et la fonction de blocage se termine avec un résultat approprié.</span><span class="sxs-lookup"><span data-stu-id="297d6-107">If the function has completed, or if [**WSPCancelBlockingCall**](/previous-versions/windows/desktop/legacy/ms742269(v=vs.85)) has been invoked, the loop is terminated and the blocking function completes with an appropriate result.</span></span>

<span data-ttu-id="297d6-108">C’est ce que signifie le terme Pseudo-blocage, et la boucle mentionnée ci-dessus est connue sous le nom de hook de blocage par défaut.</span><span class="sxs-lookup"><span data-stu-id="297d6-108">This is what is meant by the term pseudo blocking, and the loop referred to above is known as the default blocking hook.</span></span>

 

 
