---
description: Un nom de symbole décoré comprend des caractères qui différencient la manière dont un symbole public a été déclaré.
ms.assetid: f02fa21d-3fe9-4838-a938-3136c34bc0e8
title: Noms de symboles décorés
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 791fe2220b24dfb73b314a91d1797edd739cb74f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104482729"
---
# <a name="decorated-symbol-names"></a><span data-ttu-id="876d5-103">Noms de symboles décorés</span><span class="sxs-lookup"><span data-stu-id="876d5-103">Decorated Symbol Names</span></span>

<span data-ttu-id="876d5-104">Un nom de symbole décoré comprend des caractères qui différencient la manière dont un symbole public a été déclaré.</span><span class="sxs-lookup"><span data-stu-id="876d5-104">A decorated symbol name includes characters that distinguish how a public symbol has been declared.</span></span> <span data-ttu-id="876d5-105">Pour les \_ \_ fonctions stdcall, les noms incluent le caractère « @ » et un nombre décimal qui spécifie le nombre d’octets dans ses paramètres de fonction.</span><span class="sxs-lookup"><span data-stu-id="876d5-105">For \_\_stdcall functions, names include the "@" character and a decimal number that specifies the number of bytes in its function parameters.</span></span> <span data-ttu-id="876d5-106">Par exemple, le nom décoré de la fonction [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) est LoadLibrary@4 .</span><span class="sxs-lookup"><span data-stu-id="876d5-106">For example, the decorated name of the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) function is LoadLibrary@4.</span></span> <span data-ttu-id="876d5-107">Pour les fonctions C++, la décoration de noms est plus complexe et varie d’un compilateur à l’autre.</span><span class="sxs-lookup"><span data-stu-id="876d5-107">For C++ functions the name decoration is more complex and varies from compiler to compiler.</span></span>

<span data-ttu-id="876d5-108">Pour récupérer le nom du symbole non décoré, utilisez la fonction [**UnDecorateSymbolName**](/windows/desktop/api/Dbghelp/nf-dbghelp-undecoratesymbolname) .</span><span class="sxs-lookup"><span data-stu-id="876d5-108">To retrieve the undecorated symbol name, use the [**UnDecorateSymbolName**](/windows/desktop/api/Dbghelp/nf-dbghelp-undecoratesymbolname) function.</span></span> <span data-ttu-id="876d5-109">Vous pouvez également appeler la fonction [**SymSetOptions**](/windows/desktop/api/Dbghelp/nf-dbghelp-symsetoptions) pour demander que le gestionnaire de symboles présente toujours des symboles avec des noms non décorés.</span><span class="sxs-lookup"><span data-stu-id="876d5-109">Alternatively, you can call the [**SymSetOptions**](/windows/desktop/api/Dbghelp/nf-dbghelp-symsetoptions) function to request that the symbol handler always present symbols with undecorated names.</span></span> <span data-ttu-id="876d5-110">Vous devez définir cette option avant de charger les symboles, car le gestionnaire de symboles crée les tables de noms de symboles au moment du chargement.</span><span class="sxs-lookup"><span data-stu-id="876d5-110">You must set this option before loading the symbols because the symbol handler creates the symbol name tables at load time.</span></span>

 

 
