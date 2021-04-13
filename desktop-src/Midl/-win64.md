---
title: commutateur/Win64
description: Le commutateur/Win64 indique au compilateur MIDL de générer des fichiers stub, ou un fichier bibliothèque de types, pour un environnement 64 bits. Notez que ce commutateur est obsolète.
ms.assetid: 6f4780d3-6415-42af-a8ee-3884a8cebe26
keywords:
- MIDL du commutateur/Win64
topic_type:
- apiref
api_name:
- /win64
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e61906126607c0a8d4b81ef76805bb4b7e0d4145
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/25/2019
ms.locfileid: "104312298"
---
# <a name="win64-switch"></a><span data-ttu-id="41748-104">commutateur/Win64</span><span class="sxs-lookup"><span data-stu-id="41748-104">/win64 switch</span></span>

<span data-ttu-id="41748-105">Le commutateur **/Win64** indique au compilateur MIDL de générer des fichiers stub, ou un fichier bibliothèque de types, pour un environnement 64 bits.</span><span class="sxs-lookup"><span data-stu-id="41748-105">The **/win64** switch directs the MIDL compiler to generate stub files, or a type library file, for a 64-bit environment.</span></span>

> [!Note]  
> <span data-ttu-id="41748-106">Ce commutateur est obsolète.</span><span class="sxs-lookup"><span data-stu-id="41748-106">This switch is obsolete.</span></span> <span data-ttu-id="41748-107">Utilisez le commutateur [**/ia64**](-ia64.md) ou [**/amd64**](-amd64.md) à la place.</span><span class="sxs-lookup"><span data-stu-id="41748-107">Please use the [**/ia64**](-ia64.md) or [**/amd64**](-amd64.md) switch instead.</span></span> <span data-ttu-id="41748-108">Le commutateur **/Win64** est équivalent au commutateur **/ia64** .</span><span class="sxs-lookup"><span data-stu-id="41748-108">The **/win64** switch is equivalent to the **/ia64** switch.</span></span>

 

``` syntax
midl /win64
```

## <a name="switch-options"></a><span data-ttu-id="41748-109">Options de commutateur</span><span class="sxs-lookup"><span data-stu-id="41748-109">Switch Options</span></span>

<span data-ttu-id="41748-110">Ce commutateur n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="41748-110">This switch has no parameters.</span></span>

## <a name="remarks"></a><span data-ttu-id="41748-111">Notes</span><span class="sxs-lookup"><span data-stu-id="41748-111">Remarks</span></span>

<span data-ttu-id="41748-112">Le commutateur **/Win64** revient à définir le commutateur [**/env**](-env.md) sur Win64.</span><span class="sxs-lookup"><span data-stu-id="41748-112">The **/win64** switch is equivalent to setting the [**/env**](-env.md) switch to win64.</span></span>

> [!Note]  
> <span data-ttu-id="41748-113">Il n’est pas possible d’utiliser MIDL.exe pour produire un TLB 64 bits sur Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="41748-113">It is not possible to use MIDL.exe to produce a 64bit tlb on Windows 2000.</span></span>

 

## <a name="see-also"></a><span data-ttu-id="41748-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="41748-114">See also</span></span>

<dl> <dt>

[<span data-ttu-id="41748-115">**/env**</span><span class="sxs-lookup"><span data-stu-id="41748-115">**/env**</span></span>](-env.md)
</dt> <dt>

[<span data-ttu-id="41748-116">**/ia64**</span><span class="sxs-lookup"><span data-stu-id="41748-116">**/ia64**</span></span>](-ia64.md)
</dt> <dt>

[<span data-ttu-id="41748-117">**/amd64**</span><span class="sxs-lookup"><span data-stu-id="41748-117">**/amd64**</span></span>](-amd64.md)
</dt> </dl>

 

 




