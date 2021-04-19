---
description: Fournit une brève introduction à quelques types de situations de dépassement de mémoire tampon et propose des idées et des ressources pour vous aider à éviter de créer de nouveaux risques et à atténuer les risques existants.
ms.assetid: 713fd6de-16af-49d2-8940-763c4a6e414b
title: Éviter les dépassements de mémoire tampon
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3c8a3456384e799380fa0041172fb2b2ea09c0c3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106527229"
---
# <a name="avoiding-buffer-overruns"></a><span data-ttu-id="83086-103">Éviter les dépassements de mémoire tampon</span><span class="sxs-lookup"><span data-stu-id="83086-103">Avoiding Buffer Overruns</span></span>

<span data-ttu-id="83086-104">Un dépassement de mémoire tampon est l’une des sources les plus courantes de risque de sécurité.</span><span class="sxs-lookup"><span data-stu-id="83086-104">A buffer overrun is one of the most common sources of security risk.</span></span> <span data-ttu-id="83086-105">Un dépassement de mémoire tampon est essentiellement causé par le traitement d’une entrée externe non vérifiée en tant que données dignes de confiance.</span><span class="sxs-lookup"><span data-stu-id="83086-105">A buffer overrun is essentially caused by treating unchecked, external input as trustworthy data.</span></span> <span data-ttu-id="83086-106">Le fait de copier ces données, à l’aide d’opérations telles que [**CopyMemory**](/previous-versions/windows/desktop/legacy/aa366535(v=vs.85)), **strcat**, **strcpy** ou **wcscpy**, peut créer des résultats imprévus, ce qui permet d’endommager le système.</span><span class="sxs-lookup"><span data-stu-id="83086-106">The act of copying this data, using operations such as [**CopyMemory**](/previous-versions/windows/desktop/legacy/aa366535(v=vs.85)), **strcat**, **strcpy**, or **wcscpy**, can create unanticipated results, which allows for system corruption.</span></span> <span data-ttu-id="83086-107">Dans le meilleur des cas, votre application s’arrête avec un vidage de base, une erreur de segmentation ou une violation d’accès.</span><span class="sxs-lookup"><span data-stu-id="83086-107">In the best of cases, your application will abort with a core dump, segmentation fault, or access violation.</span></span> <span data-ttu-id="83086-108">Dans le pire des cas, une personne malveillante peut exploiter le dépassement de mémoire tampon en introduisant et en exécutant d’autres codes malveillants dans votre processus.</span><span class="sxs-lookup"><span data-stu-id="83086-108">In the worst of cases, an attacker can exploit the buffer overrun by introducing and executing other malicious code in your process.</span></span> <span data-ttu-id="83086-109">La copie non vérifiée, les données d’entrée dans une mémoire tampon basée sur la pile est la cause la plus courante d’erreurs exploitables.</span><span class="sxs-lookup"><span data-stu-id="83086-109">Copying unchecked, input data into a stack-based buffer is the most common cause of exploitable faults.</span></span>

<span data-ttu-id="83086-110">Les dépassements de mémoire tampon peuvent se produire de différentes façons.</span><span class="sxs-lookup"><span data-stu-id="83086-110">Buffer overruns can occur in a variety of ways.</span></span> <span data-ttu-id="83086-111">La liste suivante fournit une brève introduction à quelques types de situations de dépassement de mémoire tampon et propose des idées et des ressources pour vous aider à éviter de créer de nouveaux risques et à atténuer les risques existants :</span><span class="sxs-lookup"><span data-stu-id="83086-111">The following list provides a brief introduction to a few types of buffer overrun situations and offers some ideas and resources to help you avoid creating new risks and mitigate existing ones:</span></span>

<dl> <dt>

<span data-ttu-id="83086-112"><span id="Static_buffer_overruns"></span><span id="static_buffer_overruns"></span><span id="STATIC_BUFFER_OVERRUNS"></span>Dépassements de mémoire tampon statiques</span><span class="sxs-lookup"><span data-stu-id="83086-112"><span id="Static_buffer_overruns"></span><span id="static_buffer_overruns"></span><span id="STATIC_BUFFER_OVERRUNS"></span>Static buffer overruns</span></span>
</dt> <dd>

<span data-ttu-id="83086-113">Un dépassement de mémoire tampon statique se produit lorsqu’une mémoire tampon, qui a été déclarée sur la pile, est écrite dans avec plus de données qu’elle n’a été allouée à conserver.</span><span class="sxs-lookup"><span data-stu-id="83086-113">A static buffer overrun occurs when a buffer, which has been declared on the stack, is written to with more data than it was allocated to hold.</span></span> <span data-ttu-id="83086-114">Les versions moins évidentes de cette erreur se produisent lorsque des données d’entrée utilisateur non vérifiées sont copiées directement dans une variable statique, provoquant ainsi une corruption potentielle de la pile.</span><span class="sxs-lookup"><span data-stu-id="83086-114">The less apparent versions of this error occur when unverified user input data is copied directly to a static variable, causing potential stack corruption.</span></span>

</dd> <dt>

<span data-ttu-id="83086-115"><span id="Heap_overruns"></span><span id="heap_overruns"></span><span id="HEAP_OVERRUNS"></span>Dépassements de tas</span><span class="sxs-lookup"><span data-stu-id="83086-115"><span id="Heap_overruns"></span><span id="heap_overruns"></span><span id="HEAP_OVERRUNS"></span>Heap overruns</span></span>
</dt> <dd>

<span data-ttu-id="83086-116">Les dépassements de tas, comme les dépassements de mémoire tampon statiques, peuvent entraîner une altération de la mémoire et de la pile.</span><span class="sxs-lookup"><span data-stu-id="83086-116">Heap overruns, like static buffer overruns, can lead to memory and stack corruption.</span></span> <span data-ttu-id="83086-117">Étant donné que les dépassements de tas se produisent dans la mémoire du tas plutôt que sur la pile, certaines personnes les considèrent comme étant moins capables de provoquer de sérieux problèmes. Néanmoins, les dépassements de tas requièrent des soins de programmation réels et sont tout aussi capables d’autoriser les risques système en cas de dépassements de mémoire tampon statique.</span><span class="sxs-lookup"><span data-stu-id="83086-117">Because heap overruns occur in heap memory rather than on the stack, some people consider them to be less able to cause serious problems; nevertheless, heap overruns require real programming care and are just as able to allow system risks as static buffer overruns.</span></span>

</dd> <dt>

<span data-ttu-id="83086-118"><span id="Array_indexing_errors"></span><span id="array_indexing_errors"></span><span id="ARRAY_INDEXING_ERRORS"></span>Erreurs d’indexation de tableau</span><span class="sxs-lookup"><span data-stu-id="83086-118"><span id="Array_indexing_errors"></span><span id="array_indexing_errors"></span><span id="ARRAY_INDEXING_ERRORS"></span>Array indexing errors</span></span>
</dt> <dd>

<span data-ttu-id="83086-119">Les erreurs d’indexation de tableau sont également une source de dépassements de mémoire.</span><span class="sxs-lookup"><span data-stu-id="83086-119">Array indexing errors also are a source of memory overruns.</span></span> <span data-ttu-id="83086-120">La vérification des limites soignées et la gestion des index vous aideront à éviter ce type de dépassement de mémoire.</span><span class="sxs-lookup"><span data-stu-id="83086-120">Careful bounds checking and index management will help prevent this type of memory overrun.</span></span>

</dd> </dl>

<span data-ttu-id="83086-121">La prévention des dépassements de mémoire tampon consiste principalement à écrire un code correct.</span><span class="sxs-lookup"><span data-stu-id="83086-121">Preventing buffer overruns is primarily about writing good code.</span></span> <span data-ttu-id="83086-122">Validez toujours toutes vos entrées et effectuez une défaillance normale si nécessaire.</span><span class="sxs-lookup"><span data-stu-id="83086-122">Always validate all your inputs and fail gracefully when necessary.</span></span> <span data-ttu-id="83086-123">Pour plus d’informations sur l’écriture de code sécurisé, consultez les ressources suivantes :</span><span class="sxs-lookup"><span data-stu-id="83086-123">For more information about writing secure code, see the following resources:</span></span>

-   <span data-ttu-id="83086-124">Maguire, Steve \[ 1993 \] , *écrivant du code solide*, ISBN 1-55615-551-4, Microsoft Press, Redmond, Washington.</span><span class="sxs-lookup"><span data-stu-id="83086-124">Maguire, Steve \[1993\], *Writing Solid Code*, ISBN 1-55615-551-4, Microsoft Press, Redmond, Washington.</span></span>
-   <span data-ttu-id="83086-125">Howard, Michael et LeBlanc, David \[ 2003 \] , *écriture de code sécurisé*, 2d ed., ISBN 0-7356-1722-8, Microsoft Press, Redmond, Washington.</span><span class="sxs-lookup"><span data-stu-id="83086-125">Howard, Michael and LeBlanc, David \[2003\], *Writing Secure Code*, 2d ed., ISBN 0-7356-1722-8, Microsoft Press, Redmond, Washington.</span></span>

> [!Note]  
> <span data-ttu-id="83086-126">Ces ressources peuvent ne pas être disponibles dans certains langages et pays.</span><span class="sxs-lookup"><span data-stu-id="83086-126">These resources may not be available in some languages and countries.</span></span>

 

<span data-ttu-id="83086-127">La gestion sécurisée des chaînes est un problème à long terme qui continue à être résolu à la fois en suivant les bonnes pratiques de programmation et souvent en utilisant et en réservant les systèmes existants avec des fonctions de gestion de chaînes sécurisées.</span><span class="sxs-lookup"><span data-stu-id="83086-127">Safe string handling is a long-standing issue that continues to be addressed both by following good programming practices and often by using and retrofitting existing systems with secure, string-handling functions.</span></span> <span data-ttu-id="83086-128">Un exemple d’un tel ensemble de fonctions pour le shell Windows commence par [**StringCbCat**](/windows/win32/api/strsafe/nf-strsafe-stringcbcata).</span><span class="sxs-lookup"><span data-stu-id="83086-128">An example of such a set of functions for the Windows shell starts with [**StringCbCat**](/windows/win32/api/strsafe/nf-strsafe-stringcbcata).</span></span>

 

 
