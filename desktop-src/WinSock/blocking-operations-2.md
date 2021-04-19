---
description: La notion de blocage dans un environnement Windows a été historiquement très importante.
ms.assetid: bd2ede96-34a4-4912-b9d2-ef11d37d2292
title: Opérations bloquantes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8040865b4c6ededab925279e15d67cb89f7bc6a0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106515455"
---
# <a name="blocking-operations"></a><span data-ttu-id="c8c2a-103">Opérations bloquantes</span><span class="sxs-lookup"><span data-stu-id="c8c2a-103">Blocking Operations</span></span>

<span data-ttu-id="c8c2a-104">La notion de blocage dans un environnement Windows a été historiquement très importante.</span><span class="sxs-lookup"><span data-stu-id="c8c2a-104">The notion of blocking in a Windows environment has historically been a very important one.</span></span> <span data-ttu-id="c8c2a-105">Dans les environnements Windows Sockets 1,1, les appels bloquants ont été déconseillés, car ils ont tendance à désactiver l’interaction continue avec le système.</span><span class="sxs-lookup"><span data-stu-id="c8c2a-105">In Windows Sockets 1.1 environments, blocking calls were discouraged since they tended to disable ongoing interaction with the system.</span></span> <span data-ttu-id="c8c2a-106">En outre, ils utilisent une technique pseudoblocking qui, pour diverses raisons, ne fonctionne pas toujours comme prévu.</span><span class="sxs-lookup"><span data-stu-id="c8c2a-106">Additionally, they employ a pseudoblocking technique which, for a variety of reasons, does not always work as intended.</span></span> <span data-ttu-id="c8c2a-107">Toutefois, dans les environnements Windows préprogrammés, les appels bloquants sont bien plus parlants, peuvent être implémentés par les services du système d’exploitation natif et sont en fait un mécanisme généralement préféré.</span><span class="sxs-lookup"><span data-stu-id="c8c2a-107">However, in preemptively scheduled Windows environments, blocking calls make much more sense, can be implemented by native operating system services, and are in fact a generally preferred mechanism.</span></span> <span data-ttu-id="c8c2a-108">L’API Winsock 2 ne prend plus en charge psuedoblocking, mais étant donné que les shims de compatibilité Windows Sockets 1,1 doivent continuer à émuler ce comportement, les fournisseurs de services doivent le prendre en charge comme décrit dans les éléments suivants.</span><span class="sxs-lookup"><span data-stu-id="c8c2a-108">The Winsock 2 API no longer supports psuedoblocking, but because the Windows Sockets 1.1 compatibility shims must continue to emulate this behavior, service providers must support this as described in the following.</span></span>

 

 



