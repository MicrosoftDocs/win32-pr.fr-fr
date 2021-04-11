---
description: Les fonctions de mémoire virtuelle manipulent les pages de la mémoire. Les fonctions utilisent la taille d’une page sur l’ordinateur actuel pour arrondir les tailles et les adresses spécifiées.
ms.assetid: 509cd529-ff79-4b07-9e09-3c5ae65f6cba
title: Allocation de mémoire virtuelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 89f42b4f7eb9d5de3c8c5e9339c9e5931a89e371
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104319125"
---
# <a name="allocating-virtual-memory"></a><span data-ttu-id="c3a00-104">Allocation de mémoire virtuelle</span><span class="sxs-lookup"><span data-stu-id="c3a00-104">Allocating Virtual Memory</span></span>

<span data-ttu-id="c3a00-105">Les fonctions de mémoire virtuelle manipulent les pages de la mémoire.</span><span class="sxs-lookup"><span data-stu-id="c3a00-105">The virtual memory functions manipulate pages of memory.</span></span> <span data-ttu-id="c3a00-106">Les fonctions utilisent la taille d’une page sur l’ordinateur actuel pour arrondir les tailles et les adresses spécifiées.</span><span class="sxs-lookup"><span data-stu-id="c3a00-106">The functions use the size of a page on the current computer to round off specified sizes and addresses.</span></span>

<span data-ttu-id="c3a00-107">La fonction [**VirtualAlloc**](/windows/win32/api/memoryapi/nf-memoryapi-virtualalloc) effectue l’une des opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="c3a00-107">The [**VirtualAlloc**](/windows/win32/api/memoryapi/nf-memoryapi-virtualalloc) function performs one of the following operations:</span></span>

-   <span data-ttu-id="c3a00-108">Réserve une ou plusieurs pages gratuites.</span><span class="sxs-lookup"><span data-stu-id="c3a00-108">Reserves one or more free pages.</span></span>
-   <span data-ttu-id="c3a00-109">Valide une ou plusieurs pages réservées.</span><span class="sxs-lookup"><span data-stu-id="c3a00-109">Commits one or more reserved pages.</span></span>
-   <span data-ttu-id="c3a00-110">Réserve et valide une ou plusieurs pages gratuites.</span><span class="sxs-lookup"><span data-stu-id="c3a00-110">Reserves and commits one or more free pages.</span></span>

<span data-ttu-id="c3a00-111">Vous pouvez spécifier l’adresse de départ des pages réservées ou validées, ou vous pouvez autoriser le système à déterminer l’adresse.</span><span class="sxs-lookup"><span data-stu-id="c3a00-111">You can specify the starting address of the pages to be reserved or committed, or you can allow the system to determine the address.</span></span> <span data-ttu-id="c3a00-112">La fonction arrondit l’adresse spécifiée à la limite de page appropriée.</span><span class="sxs-lookup"><span data-stu-id="c3a00-112">The function rounds the specified address to the appropriate page boundary.</span></span> <span data-ttu-id="c3a00-113">Les pages réservées ne sont pas accessibles, mais les pages validées peuvent être allouées avec l’accès à la **page \_ ReadWrite**, **page \_ ReadOnly** ou **page \_ NoAccess** .</span><span class="sxs-lookup"><span data-stu-id="c3a00-113">Reserved pages are not accessible, but committed pages can be allocated with **PAGE\_READWRITE**, **PAGE\_READONLY**, or **PAGE\_NOACCESS** access.</span></span> <span data-ttu-id="c3a00-114">Lorsque les pages sont validées, les frais de mémoire sont alloués à partir de la taille globale de la RAM et des fichiers d’échange sur le disque, mais chaque page est initialisée et chargée dans la mémoire physique uniquement lors de la première tentative de lecture ou d’écriture dans cette page.</span><span class="sxs-lookup"><span data-stu-id="c3a00-114">When pages are committed, memory charges are allocated from the overall size of RAM and paging files on disk, but each page is initialized and loaded into physical memory only at the first attempt to read from or write to that page.</span></span> <span data-ttu-id="c3a00-115">Vous pouvez utiliser des références de pointeur normales pour accéder à la mémoire validée par la fonction [**VirtualAlloc**](/windows/win32/api/memoryapi/nf-memoryapi-virtualalloc) .</span><span class="sxs-lookup"><span data-stu-id="c3a00-115">You can use normal pointer references to access memory committed by the [**VirtualAlloc**](/windows/win32/api/memoryapi/nf-memoryapi-virtualalloc) function.</span></span>

 

 
