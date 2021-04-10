---
title: C/C++-considérations relatives au compilateur
description: Le compilateur MIDL doit interagir avec le compilateur C et le préprocesseur C.
ms.assetid: 3d91d0e4-3a47-4aa2-82d6-c3af11df3a78
keywords:
- MIDL du compilateur MIDL, compilateur C
- C-compilateur MIDL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ebf6968951bbcbb423896f5609092054dfa65f4e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104029607"
---
# <a name="cc-compiler-considerations"></a><span data-ttu-id="1f440-105">C/C++-considérations relatives au compilateur</span><span class="sxs-lookup"><span data-stu-id="1f440-105">C/C++-Compiler Considerations</span></span>

<span data-ttu-id="1f440-106">Le compilateur MIDL doit interagir avec le compilateur C et le préprocesseur C.</span><span class="sxs-lookup"><span data-stu-id="1f440-106">The MIDL compiler must interoperate with the C compiler and C preprocessor.</span></span> <span data-ttu-id="1f440-107">MIDL n’accepte pas la syntaxe C++ sur l’entrée.</span><span class="sxs-lookup"><span data-stu-id="1f440-107">MIDL does not accept C++ syntax on input.</span></span> <span data-ttu-id="1f440-108">Le fichier. h généré contient des définitions de style C et C++ pour les interfaces.</span><span class="sxs-lookup"><span data-stu-id="1f440-108">The generated .h file has both C-style and C++-style definitions for interfaces.</span></span> <span data-ttu-id="1f440-109">Les rubriques suivantes décrivent la configuration requise pour le compilateur C.</span><span class="sxs-lookup"><span data-stu-id="1f440-109">The following topics describe the requirements for the C compiler.</span></span>

-   [<span data-ttu-id="1f440-110">C-problèmes de compression du compilateur</span><span class="sxs-lookup"><span data-stu-id="1f440-110">C-Compiler Packing Issues</span></span>](c-compiler-packing-issues.md)
-   [<span data-ttu-id="1f440-111">C-définitions de compilateur pour les proxys/stubs</span><span class="sxs-lookup"><span data-stu-id="1f440-111">C-Compiler Definitions for Proxy/Stubs</span></span>](c-compiler-definitions-for-proxy-stubs.md)

 

 




