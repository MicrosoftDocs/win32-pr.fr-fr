---
title: Attributs ACF de gestion de la mémoire
description: Les attributs figurant dans le tableau suivant vous permettent d’effectuer la gestion de la mémoire du côté client.
ms.assetid: ca03c7fe-6649-431b-89dc-5d07a3c8d591
keywords:
- ACF MIDL, attributs, gestion de la mémoire
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d12a0ee6d11a2b10e1c0fad7cd1a42411670b508
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "103940936"
---
# <a name="memory-management-acf-attributes"></a><span data-ttu-id="40160-104">Attributs ACF de gestion de la mémoire</span><span class="sxs-lookup"><span data-stu-id="40160-104">Memory Management ACF Attributes</span></span>

<span data-ttu-id="40160-105">Les attributs figurant dans le tableau suivant vous permettent d’effectuer la gestion de la mémoire du côté client.</span><span class="sxs-lookup"><span data-stu-id="40160-105">The attributes listed in the following table enable you to perform memory management from the client side.</span></span>



| <span data-ttu-id="40160-106">Attribut</span><span class="sxs-lookup"><span data-stu-id="40160-106">Attribute</span></span>                                   | <span data-ttu-id="40160-107">Utilisation</span><span class="sxs-lookup"><span data-stu-id="40160-107">Usage</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
|---------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="40160-108">**lui**</span><span class="sxs-lookup"><span data-stu-id="40160-108">**allocate**</span></span>](allocate.md)                | <span data-ttu-id="40160-109">Spécifie la façon dont l’application cliente et le stub allouent et libèrent de la mémoire pour les pointeurs.</span><span class="sxs-lookup"><span data-stu-id="40160-109">Specifies the way the client application and stub allocate and release memory for pointers.</span></span> <span data-ttu-id="40160-110">Cet attribut est particulièrement utile lorsque vous souhaitez que certaines structures de pointeur restent accessibles à l’application serveur après que l’appel de procédure distante a été retourné au client.</span><span class="sxs-lookup"><span data-stu-id="40160-110">This attribute is particularly useful when you want certain pointer structures to remain accessible to the server application after the remote procedure call returns to the client.</span></span> <span data-ttu-id="40160-111">Vous pouvez également utiliser l’attribut [**allocate**](allocate.md) pour indiquer au stub de calculer la taille de la mémoire référencée par le pointeur du type spécifié et d’effectuer un appel unique à [**l' \_ \_ allocation d’utilisateur MIDL**](/windows/desktop/Rpc/the-midl-user-allocate-function).</span><span class="sxs-lookup"><span data-stu-id="40160-111">You can also use the [**allocate**](allocate.md) attribute to direct the stub to compute the size of all memory referenced through the pointer of the specified type and to make a single call to [**midl\_user\_allocate**](/windows/desktop/Rpc/the-midl-user-allocate-function).</span></span> |
| [<span data-ttu-id="40160-112">**nombre d’octets \_**</span><span class="sxs-lookup"><span data-stu-id="40160-112">**byte\_count**</span></span>](byte-count.md)           | <span data-ttu-id="40160-113">Vous permet de créer un bloc de mémoire persistant et contigu qui peut être réutilisé sur plusieurs appels de procédure distante.</span><span class="sxs-lookup"><span data-stu-id="40160-113">Enables you to create a persistent, contiguous block of memory that can be reused over multiple remote procedure calls.</span></span> <span data-ttu-id="40160-114">Cela libère l’application cliente de la surcharge d’allocation et de libération de mémoire qui peut inclure plusieurs pointeurs et d’autres structures de données complexes.</span><span class="sxs-lookup"><span data-stu-id="40160-114">This frees the client application from the overhead of repeatedly allocating and releasing memory that may include multiple pointers and other complex data structures.</span></span>                                                                                                                                                                                                                                                      |
| [<span data-ttu-id="40160-115">**activer l' \_ allocation**</span><span class="sxs-lookup"><span data-stu-id="40160-115">**enable\_allocate**</span></span>](enable-allocate.md) | <span data-ttu-id="40160-116">Spécifie que le code stub du serveur doit activer l’environnement de gestion de mémoire stub.</span><span class="sxs-lookup"><span data-stu-id="40160-116">Specifies that the server stub code should enable the stub memory-management environment.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                            |



 

 

 