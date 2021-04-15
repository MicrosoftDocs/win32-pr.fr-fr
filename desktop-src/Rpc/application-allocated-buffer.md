---
title: Mémoire tampon de Application-Allocated
description: L’attribut ACF \ Byte \_ Count \ indique aux stubs d’utiliser une mémoire tampon préallouée qui n’est pas allouée ou libérée par les routines de prise en charge du client.
ms.assetid: 1b370f74-394e-4e57-9749-83334be50f28
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db533495f16d37aca0bdae96035783650573a60f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104463543"
---
# <a name="application-allocated-buffer"></a><span data-ttu-id="d1ba9-103">Mémoire tampon de Application-Allocated</span><span class="sxs-lookup"><span data-stu-id="d1ba9-103">Application-Allocated Buffer</span></span>

<span data-ttu-id="d1ba9-104">Le \[ [**\_ nombre d’octets**](/windows/desktop/Midl/byte-count) de l’attribut ACF \] indique aux stubs d’utiliser une mémoire tampon préallouée qui n’est pas allouée ou libérée par les routines de prise en charge du client.</span><span class="sxs-lookup"><span data-stu-id="d1ba9-104">The ACF attribute \[[**byte\_count**](/windows/desktop/Midl/byte-count)\] directs the stubs to use a preallocated buffer that is not allocated or freed by the client support routines.</span></span> <span data-ttu-id="d1ba9-105">L' \[ **attribut \_ nombre** \] d’octets est appliqué à un pointeur ou à un paramètre de tableau qui pointe vers la mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="d1ba9-105">The \[**byte\_count**\] attribute is applied to a pointer or array parameter that points to the buffer.</span></span> <span data-ttu-id="d1ba9-106">Elle nécessite un paramètre qui spécifie la taille de la mémoire tampon en octets.</span><span class="sxs-lookup"><span data-stu-id="d1ba9-106">It requires a parameter that specifies the buffer size in bytes.</span></span>

<span data-ttu-id="d1ba9-107">La zone mémoire allouée par le client peut contenir des structures de données complexes avec plusieurs pointeurs.</span><span class="sxs-lookup"><span data-stu-id="d1ba9-107">The client-allocated memory area can contain complex data structures with multiple pointers.</span></span> <span data-ttu-id="d1ba9-108">Étant donné que la zone mémoire est contiguë, l’application n’a pas besoin d’effectuer plusieurs appels pour libérer individuellement chaque pointeur et toute structure.</span><span class="sxs-lookup"><span data-stu-id="d1ba9-108">Because the memory area is contiguous, the application does not have to make several calls to free each pointer and structure individually.</span></span> <span data-ttu-id="d1ba9-109">Comme lorsque vous utilisez l' \[ attribut [**allocate (tous les \_ nœuds)**](/windows/desktop/Midl/allocate) \] , la zone de mémoire peut être allouée ou libérée à l’aide d’un appel à la routine d’allocation de mémoire ou à la routine libre.</span><span class="sxs-lookup"><span data-stu-id="d1ba9-109">As when using the \[[**allocate(all\_nodes)**](/windows/desktop/Midl/allocate)\] attribute, the memory area can be allocated or freed with one call to the memory-allocation routine or the free routine.</span></span> <span data-ttu-id="d1ba9-110">Toutefois, contrairement à l’utilisation de l' \[ attribut **allocate (tous les \_ nœuds)** \] , le paramètre buffer n’est pas géré par le stub client, mais par l’application cliente.</span><span class="sxs-lookup"><span data-stu-id="d1ba9-110">However, unlike using the \[**allocate(all\_nodes)**\] attribute, the buffer parameter is not managed by the client stub but by the client application.</span></span>

<span data-ttu-id="d1ba9-111">La mémoire tampon doit être un \[ [](/windows/desktop/Midl/out-idl) \] paramètre en sortie seule et la longueur de la mémoire tampon en octets doit être un \[ [](/windows/desktop/Midl/in) \] paramètre en uniquement.</span><span class="sxs-lookup"><span data-stu-id="d1ba9-111">The buffer must be an \[[**out**](/windows/desktop/Midl/out-idl)\]-only parameter and the buffer length in bytes must be an \[[**in**](/windows/desktop/Midl/in)\]-only parameter.</span></span> <span data-ttu-id="d1ba9-112">L' \[ [**attribut \_ nombre**](/windows/desktop/Midl/byte-count) \] d’octets ne peut être appliqué qu’aux types pointeur.</span><span class="sxs-lookup"><span data-stu-id="d1ba9-112">The \[[**byte\_count**](/windows/desktop/Midl/byte-count)\] attribute can only be applied to pointer types.</span></span> <span data-ttu-id="d1ba9-113">L' \[ attribut ACF du **\_ nombre d’octets** \] est une extension Microsoft de l’IDL DCE et, par conséquent, n’est pas disponible si vous compilez à l’aide du commutateur [**/OSF**](/windows/desktop/Midl/-osf) MIDL.</span><span class="sxs-lookup"><span data-stu-id="d1ba9-113">The \[**byte\_count**\] ACF attribute is a Microsoft extension to DCE IDL and, as such, is not available if you compile using the MIDL [**/osf**](/windows/desktop/Midl/-osf) switch.</span></span>

<span data-ttu-id="d1ba9-114">Dans l’exemple suivant, le paramètre *pRoot* utilise le nombre d’octets :</span><span class="sxs-lookup"><span data-stu-id="d1ba9-114">In the following example, the parameter *pRoot* uses byte count:</span></span>

``` syntax
/* function prototype in IDL file (fragment) */
void SortNames(
    [in] short cNames,
    [in, size_is(cNames)] STRINGTYPE pszArray[],
    [in] short cBytes,
    [out, ref] P_TREE_TYPE pRoot  /* tree with sorted data */
);
```

<span data-ttu-id="d1ba9-115">L' \[ [**attribut \_ nombre**](/windows/desktop/Midl/byte-count) \] d’octets apparaît dans le CCP en tant que :</span><span class="sxs-lookup"><span data-stu-id="d1ba9-115">The \[[**byte\_count**](/windows/desktop/Midl/byte-count)\] attribute appears in the ACF as:</span></span>

``` syntax
/* ACF file (fragment) */
SortNames([byte_count(cBytes)] pRoot);
```

<span data-ttu-id="d1ba9-116">Le stub client généré à partir de ces fichiers IDL et ACF n’alloue pas ou ne libère pas la mémoire pour cette mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="d1ba9-116">The client stub generated from these IDL and ACF files does not allocate or free the memory for this buffer.</span></span> <span data-ttu-id="d1ba9-117">Le stub serveur alloue et libère la mémoire tampon dans un appel unique à l’aide du paramètre de taille fourni.</span><span class="sxs-lookup"><span data-stu-id="d1ba9-117">The server stub allocates and frees the buffer in a single call using the provided size parameter.</span></span> <span data-ttu-id="d1ba9-118">Si les données sont trop volumineuses pour la taille de la mémoire tampon spécifiée, une exception est levée.</span><span class="sxs-lookup"><span data-stu-id="d1ba9-118">If the data is too large for the specified buffer size, an exception is raised.</span></span>

 

 