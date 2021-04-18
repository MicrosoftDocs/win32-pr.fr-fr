---
title: Référence de fonction
description: Cette section décrit les fonctions d’exécution de l’appel de procédure distante (RPC) prises en charge dans Microsoft RPC.
ms.assetid: 135bef8d-1794-420e-a111-604d02dbcc06
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 163c68f56a483d3eb7f62596c4a3d78ba2b5774a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104462246"
---
# <a name="function-reference"></a><span data-ttu-id="4e42b-103">Référence de fonction</span><span class="sxs-lookup"><span data-stu-id="4e42b-103">Function Reference</span></span>

<span data-ttu-id="4e42b-104">Cette section décrit les fonctions d’exécution de l’appel de procédure distante (RPC) prises en charge dans Microsoft RPC.</span><span class="sxs-lookup"><span data-stu-id="4e42b-104">This section documents the Remote Procedure Call (RPC) run-time functions supported in Microsoft RPC.</span></span> <span data-ttu-id="4e42b-105">Cette section décrit le rôle, la syntaxe, les paramètres d’entrée et les valeurs de retour de chaque fonction.</span><span class="sxs-lookup"><span data-stu-id="4e42b-105">This section describes each function's purpose, syntax, input parameters, and return values.</span></span> <span data-ttu-id="4e42b-106">Il fournit également des informations supplémentaires pour vous aider à utiliser les fonctions RPC dans une application.</span><span class="sxs-lookup"><span data-stu-id="4e42b-106">It also provides additional information to help you use RPC functions in an application.</span></span>

<span data-ttu-id="4e42b-107">Tous les pointeurs passés aux fonctions RPC doivent inclure l’attribut **\_ \_ RPC \_ Far** .</span><span class="sxs-lookup"><span data-stu-id="4e42b-107">All pointers passed to RPC functions must include the **\_ \_RPC\_FAR** attribute.</span></span> <span data-ttu-id="4e42b-108">Par exemple, le **\_ \_ handle \* de liaison RPC** du pointeur devient le **handle de liaison RPC \_ \_ \_ \_ \_ \*** **\* \***   **\_ \_ \_ \* \_ \_ \_ FAR et char PTR devient char RPC Far Far PTR. \***</span><span class="sxs-lookup"><span data-stu-id="4e42b-108">For example, the pointer **RPC\_BINDING\_HANDLE \*** becomes **RPC\_BINDING\_HANDLE \_ \_RPC\_FAR \*** and **char \* \*** *Ptr* becomes **char \_ \_RPC\_FAR \* \_ \_RPC\_FAR \*** *Ptr*.</span></span>

<span data-ttu-id="4e42b-109">Cette section présente les références de fonction dans les groupes suivants :</span><span class="sxs-lookup"><span data-stu-id="4e42b-109">This section presents the function references in the following groups:</span></span>

-   [<span data-ttu-id="4e42b-110">Fonctions RPC</span><span class="sxs-lookup"><span data-stu-id="4e42b-110">RPC Functions</span></span>](rpc-functions.md)
-   [<span data-ttu-id="4e42b-111">Fonctions de rappel et de notification RPC</span><span class="sxs-lookup"><span data-stu-id="4e42b-111">RPC Callback and Notification Functions</span></span>](rpc-callback-and-notification-functions.md)

 

 




