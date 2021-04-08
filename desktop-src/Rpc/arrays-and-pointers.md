---
title: Tableaux et pointeurs
description: L’appel de procédure distante (RPC) est conçu pour être principalement transparent pour les développeurs.
ms.assetid: 5ad5a51d-a821-44a5-bbc3-14409cb42cb4
keywords:
- Appel de procédure distante RPC, décrit, tableaux et pointeurs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4cb6bc3f4a2ec4af85156bf15160b0ce7d1efc33
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103673757"
---
# <a name="arrays-and-pointers"></a><span data-ttu-id="a4b1e-104">Tableaux et pointeurs</span><span class="sxs-lookup"><span data-stu-id="a4b1e-104">Arrays and Pointers</span></span>

<span data-ttu-id="a4b1e-105">L’appel de procédure distante (RPC) est conçu pour être principalement transparent pour les développeurs.</span><span class="sxs-lookup"><span data-stu-id="a4b1e-105">Remote Procedure Call (RPC) is designed to be mostly transparent to developers.</span></span> <span data-ttu-id="a4b1e-106">Pour atteindre cette transparence, le stub client transmet au serveur le pointeur et l’objet de données vers lequel il pointe.</span><span class="sxs-lookup"><span data-stu-id="a4b1e-106">To achieve this transparency, the client stub transmits to the server both the pointer and the data object to which it points.</span></span> <span data-ttu-id="a4b1e-107">Si la procédure distante modifie les données, le serveur doit transmettre les nouvelles données au client afin que le client puisse copier les nouvelles données sur les données d’origine.</span><span class="sxs-lookup"><span data-stu-id="a4b1e-107">If the remote procedure changes the data, the server must transmit the new data back to the client so that the client can copy the new data over the original data.</span></span>

<span data-ttu-id="a4b1e-108">En général, un appel de procédure distante se comporte comme un appel de procédure local.</span><span class="sxs-lookup"><span data-stu-id="a4b1e-108">In general, a remote procedure call behaves just like a local procedure call.</span></span> <span data-ttu-id="a4b1e-109">Autrement dit, lorsqu’un pointeur est un paramètre, la procédure distante peut accéder à l’objet de données auquel le pointeur fait référence de la même façon qu’une procédure locale.</span><span class="sxs-lookup"><span data-stu-id="a4b1e-109">That is, when a pointer is a parameter, the remote procedure can access the data object the pointer refers to in the same way that a local procedure can.</span></span>

<span data-ttu-id="a4b1e-110">Étant donné que les programmes client et serveur s’exécutent dans différents espaces d’adressage, les développeurs doivent utiliser des attributs Microsoft Interface Definition Language (MIDL) pour décrire la façon dont les données de tableau et de pointeur sont transmises entre le client et le serveur.</span><span class="sxs-lookup"><span data-stu-id="a4b1e-110">Since client and server programs run in different address spaces, developers must use Microsoft Interface Definition Language (MIDL) attributes to describe how array and pointer data is transmitted between the client and the server.</span></span> <span data-ttu-id="a4b1e-111">Cette section présente une vue d’ensemble de l’utilisation des tableaux et des pointeurs dans les applications distribuées, dans les rubriques suivantes :</span><span class="sxs-lookup"><span data-stu-id="a4b1e-111">This section presents an overview of how to use arrays and pointers in distributed applications, in the following topics:</span></span>

-   [<span data-ttu-id="a4b1e-112">Tableaux et RPC</span><span class="sxs-lookup"><span data-stu-id="a4b1e-112">Arrays and RPC</span></span>](arrays-and-rpc.md)
-   [<span data-ttu-id="a4b1e-113">Pointeurs et RPC</span><span class="sxs-lookup"><span data-stu-id="a4b1e-113">Pointers and RPC</span></span>](pointers-and-rpc.md)
-   [<span data-ttu-id="a4b1e-114">Utilisation de tableaux, de chaînes et de pointeurs</span><span class="sxs-lookup"><span data-stu-id="a4b1e-114">Using Arrays, Strings, and Pointers</span></span>](using-arrays-strings-and-pointers.md)

 

 




