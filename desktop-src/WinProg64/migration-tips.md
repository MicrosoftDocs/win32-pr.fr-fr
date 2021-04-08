---
title: Conseils de migration
description: Il est important de prendre en compte les calculs d’adresses et les opérations arithmétiques de pointeur lors du Portage de votre code vers Windows 64 bits.
ms.assetid: ae562a85-d6ea-4595-b54c-0a28e6532cf5
keywords:
- Guide de programmation Windows 64 bits-programmation Windows 64 bits, conseils sur la migration
- conseils de migration 64 bits de la programmation Windows
- compatibilité avec la programmation Windows 64 bits
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5236012b84ee880b53f8d7e50b01694181e71112
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103674006"
---
# <a name="migration-tips"></a><span data-ttu-id="2bc5b-106">Conseils de migration</span><span class="sxs-lookup"><span data-stu-id="2bc5b-106">Migration Tips</span></span>

<span data-ttu-id="2bc5b-107">Les deux principaux points à se poser lors de l’examen de votre code pour la compatibilité 64 bits sont les suivants :</span><span class="sxs-lookup"><span data-stu-id="2bc5b-107">The two primary areas of concern when examining your code for 64-bit compatibility are as follows:</span></span>

-   <span data-ttu-id="2bc5b-108">Calculs d’adresses</span><span class="sxs-lookup"><span data-stu-id="2bc5b-108">Address calculations</span></span>
-   <span data-ttu-id="2bc5b-109">Arithmétique des pointeurs</span><span class="sxs-lookup"><span data-stu-id="2bc5b-109">Pointer arithmetic</span></span>

<span data-ttu-id="2bc5b-110">Pour de nombreuses raisons, les développeurs ont des adresses stockées en tant que valeur **ULong** .</span><span class="sxs-lookup"><span data-stu-id="2bc5b-110">For many reasons, developers have stored addresses as a **ULONG** value.</span></span> <span data-ttu-id="2bc5b-111">Après tout, sur Windows 32 bits, une adresse, un pointeur et une valeur **ULong** sont tous les 32 bits de long.</span><span class="sxs-lookup"><span data-stu-id="2bc5b-111">After all, on 32-bit Windows, an address, a pointer, and a **ULONG** value are all 32 bits long.</span></span> <span data-ttu-id="2bc5b-112">Toutefois, sur Windows 64 bits, une adresse et un **ULong** ne sont pas de la même longueur.</span><span class="sxs-lookup"><span data-stu-id="2bc5b-112">However, on 64-bit Windows, an address and a **ULONG** are not the same length.</span></span> <span data-ttu-id="2bc5b-113">Alors qu’un **ULong** reste une valeur 32 bits, tous les pointeurs sont maintenant des valeurs de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="2bc5b-113">While a **ULONG** remains a 32-bit value, all pointers are now 64-bit values.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="2bc5b-114">Dans cette section</span><span class="sxs-lookup"><span data-stu-id="2bc5b-114">In this Section</span></span>

-   [<span data-ttu-id="2bc5b-115">Instructions générales sur le portage</span><span class="sxs-lookup"><span data-stu-id="2bc5b-115">General Porting Guidelines</span></span>](general-porting-guidelines.md)
-   [<span data-ttu-id="2bc5b-116">Stockage d’une valeur 64 bits</span><span class="sxs-lookup"><span data-stu-id="2bc5b-116">Storing a 64-bit Value</span></span>](storing-a-64-bit-value.md)
-   [<span data-ttu-id="2bc5b-117">Erreurs courantes du compilateur</span><span class="sxs-lookup"><span data-stu-id="2bc5b-117">Common Compiler Errors</span></span>](common-compiler-errors.md)
-   [<span data-ttu-id="2bc5b-118">Considérations supplémentaires</span><span class="sxs-lookup"><span data-stu-id="2bc5b-118">Additional Considerations</span></span>](additional-considerations.md)

 

 




