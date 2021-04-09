---
description: Les rubriques suivantes décrivent les fichiers de symboles et les fonctionnalités fournies par les fonctions DbgHelp.
ms.assetid: 1bae2f0a-94a4-4152-bccc-b4deb1291a09
title: À propos de DbgHelp
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 634633d44d0c9e8202d99fd16140dd0a506453ec
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104110331"
---
# <a name="about-dbghelp"></a><span data-ttu-id="1a3e4-103">À propos de DbgHelp</span><span class="sxs-lookup"><span data-stu-id="1a3e4-103">About DbgHelp</span></span>

<span data-ttu-id="1a3e4-104">Les rubriques suivantes décrivent les fichiers de symboles et les fonctionnalités fournies par les [fonctions dbghelp](dbghelp-functions.md).</span><span class="sxs-lookup"><span data-stu-id="1a3e4-104">The following topics describe symbol files and the functionality provided by the [DbgHelp functions](dbghelp-functions.md).</span></span>

-   [<span data-ttu-id="1a3e4-105">Versions de DbgHelp</span><span class="sxs-lookup"><span data-stu-id="1a3e4-105">DbgHelp Versions</span></span>](dbghelp-versions.md)
-   [<span data-ttu-id="1a3e4-106">Fichiers de symboles</span><span class="sxs-lookup"><span data-stu-id="1a3e4-106">Symbol Files</span></span>](symbol-files.md)
-   [<span data-ttu-id="1a3e4-107">Gestion des symboles</span><span class="sxs-lookup"><span data-stu-id="1a3e4-107">Symbol Handling</span></span>](symbol-handling.md)
-   [<span data-ttu-id="1a3e4-108">Serveurs de symboles et magasins de symboles</span><span class="sxs-lookup"><span data-stu-id="1a3e4-108">Symbol Servers and Symbol Stores</span></span>](symbol-servers-and-symbol-stores.md)
-   [<span data-ttu-id="1a3e4-109">Fichiers minidump</span><span class="sxs-lookup"><span data-stu-id="1a3e4-109">Minidump Files</span></span>](minidump-files.md)
-   [<span data-ttu-id="1a3e4-110">Serveur source</span><span class="sxs-lookup"><span data-stu-id="1a3e4-110">Source Server</span></span>](source-server-and-source-indexing.md)
-   [<span data-ttu-id="1a3e4-111">Plateforme d'appui améliorée</span><span class="sxs-lookup"><span data-stu-id="1a3e4-111">Updated Platform Support</span></span>](updated-platform-support.md)

<span data-ttu-id="1a3e4-112">Notez que toutes les [fonctions dbghelp](dbghelp-functions.md) sont à thread unique.</span><span class="sxs-lookup"><span data-stu-id="1a3e4-112">Note that all [DbgHelp functions](dbghelp-functions.md) are single threaded.</span></span> <span data-ttu-id="1a3e4-113">Par conséquent, les appels à partir de plusieurs threads à cette fonction entraîneront probablement un comportement inattendu ou une altération de la mémoire.</span><span class="sxs-lookup"><span data-stu-id="1a3e4-113">Therefore, calls from more than one thread to this function will likely result in unexpected behavior or memory corruption.</span></span> <span data-ttu-id="1a3e4-114">Pour éviter cela, vous devez synchroniser tous les appels simultanés à partir de plusieurs threads à cette fonction.</span><span class="sxs-lookup"><span data-stu-id="1a3e4-114">To avoid this, you must synchronize all concurrent calls from more than one thread to this function.</span></span>

 

 



