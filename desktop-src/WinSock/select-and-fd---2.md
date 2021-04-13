---
description: Étant donné que les sockets ne sont pas représentés par l’entier de style UNIX, petit et non négatif, l’implémentation de la fonction Select a été modifiée dans Windows Sockets.
ms.assetid: 97c7996c-c541-4673-b26f-d66f3fc0b62e
title: Macros Select, FD_SET et FD_XXX
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b9bce15e921bf6566717a30114af73530406e5e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104528629"
---
# <a name="select-fd_set-and-fd_xxx-macros"></a><span data-ttu-id="63aba-103">Macros Select, FD \_ set et FD \_ xxx</span><span class="sxs-lookup"><span data-stu-id="63aba-103">Select, FD\_SET, and FD\_XXX Macros</span></span>

<span data-ttu-id="63aba-104">Étant donné que les sockets ne sont pas représentés par l’entier de style UNIX, petit et non négatif, l’implémentation de la fonction [**Select**](/windows/desktop/api/Winsock2/nf-winsock2-select) a été modifiée dans Windows Sockets.</span><span class="sxs-lookup"><span data-stu-id="63aba-104">Since sockets are not represented by the UNIX-style, small, non-negative integer, the implementation of the [**select**](/windows/desktop/api/Winsock2/nf-winsock2-select) function was changed in Windows Sockets.</span></span> <span data-ttu-id="63aba-105">Chaque ensemble de sockets est toujours représenté par la structure **FD \_ Set** , mais au lieu d’être stocké en tant que masque de masque, l’ensemble est implémenté en tant que tableau de Sockets.</span><span class="sxs-lookup"><span data-stu-id="63aba-105">Each set of sockets is still represented by the **FD\_SET** structure, but instead of being stored as a bitmask, the set is implemented as an array of sockets.</span></span> <span data-ttu-id="63aba-106">Pour éviter d’éventuels problèmes, les applications doivent adhérer à l’utilisation des \_ macros FD xxx pour définir, initialiser, effacer et vérifier les structures du [**\_ jeu FD**](/windows/desktop/api/winsock/nf-winsock-fd_set) .</span><span class="sxs-lookup"><span data-stu-id="63aba-106">To avoid potential problems, applications must adhere to the use of the FD\_XXX macros to set, initialize, clear, and check the [**FD\_SET**](/windows/desktop/api/winsock/nf-winsock-fd_set) structures.</span></span>

## <a name="related-topics"></a><span data-ttu-id="63aba-107">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="63aba-107">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="63aba-108">Portage d’applications de socket vers Winsock</span><span class="sxs-lookup"><span data-stu-id="63aba-108">Porting Socket Applications to Winsock</span></span>](porting-socket-applications-to-winsock.md)
</dt> <dt>

[<span data-ttu-id="63aba-109">Considérations sur la programmation Winsock</span><span class="sxs-lookup"><span data-stu-id="63aba-109">Winsock Programming Considerations</span></span>](winsock-programming-considerations.md)
</dt> </dl>

 

 



