---
title: Opérateur de résolution de portée en C++
description: Opérateur de résolution de portée en C++
ms.assetid: 908cf2b0-41d2-442d-aba8-82f3328c72c1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cb888fa9d56b6a84f8ecbc5efb2c235d1a38be03
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103840086"
---
# <a name="the-scope-resolution-operator-in-c"></a><span data-ttu-id="0137f-103">Opérateur de résolution de portée en C++</span><span class="sxs-lookup"><span data-stu-id="0137f-103">The Scope Resolution Operator in C++</span></span>

<span data-ttu-id="0137f-104">Deux signes deux-points ( ::) sont utilisés en C++ comme opérateur de *résolution de portée* .</span><span class="sxs-lookup"><span data-stu-id="0137f-104">Two colons (::) are used in C++ as a *scope resolution* operator.</span></span> <span data-ttu-id="0137f-105">Cet opérateur vous offre plus de liberté pour nommer vos variables en vous permettant de faire la distinction entre les variables portant le même nom.</span><span class="sxs-lookup"><span data-stu-id="0137f-105">This operator gives you more freedom in naming your variables by letting you distinguish between variables with the same name.</span></span> <span data-ttu-id="0137f-106">Par exemple, *MyFile :: Read* fait référence à la méthode *Read* de la classe *MyFile* des objets, par opposition à *YourFile :: Read*, qui fait référence à une méthode *Read* dans la classe *YourFile* .</span><span class="sxs-lookup"><span data-stu-id="0137f-106">For example, *MyFile::Read* refers to the *Read* method of the *MyFile* class of objects, as opposed to *YourFile::Read*, which refers to a *Read* method in the *YourFile* class.</span></span>

 

 




