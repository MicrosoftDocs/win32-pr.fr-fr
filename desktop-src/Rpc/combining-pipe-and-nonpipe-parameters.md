---
title: Combinaison de paramètres de canal et de pas de canal
description: Combinaison de paramètres de canal et de canalisation dans un appel de procédure distante (RPC).
ms.assetid: 52109ba9-4e10-4426-8dfc-e3052d403e9a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0776f995dacb4d477724b0ee1e5c2fa969723199
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103842586"
---
# <a name="combining-pipe-and-nonpipe-parameters"></a><span data-ttu-id="a9dac-103">Combinaison de paramètres de canal et de pas de canal</span><span class="sxs-lookup"><span data-stu-id="a9dac-103">Combining Pipe and Nonpipe Parameters</span></span>

<span data-ttu-id="a9dac-104">Lorsque vous combinez des types de canal et d’autres types dans un appel de procédure distante, les données sont transmises en fonction de la direction du paramètre :</span><span class="sxs-lookup"><span data-stu-id="a9dac-104">When you combine pipe types and other types in a remote procedure call, the data is transmitted according to the direction of the parameter:</span></span>

-   <span data-ttu-id="a9dac-105">Dans le **\[ \] sens,** les données de tous les arguments non-pipe sont transmises en premier, suivies des données de canal.</span><span class="sxs-lookup"><span data-stu-id="a9dac-105">In the **\[in\]** direction, the data for all nonpipe arguments is transmitted first, followed by pipe data.</span></span>
-   <span data-ttu-id="a9dac-106">Dans le **\[ \] sens inverse, le serveur** envoie d’abord les données de canal.</span><span class="sxs-lookup"><span data-stu-id="a9dac-106">In the **\[out\]** direction, the server sends the pipe data first.</span></span> <span data-ttu-id="a9dac-107">Une fois que la routine Manager a été retournée, le serveur transmet les données sans canal.</span><span class="sxs-lookup"><span data-stu-id="a9dac-107">After the manager routine returns, the server transmits the nonpipe data.</span></span>
-   <span data-ttu-id="a9dac-108">Lorsqu’il y a **\[ dans, \]** les arguments de canal sortant combinés avec **\[ in, out \]** arguments sans canal, d’abord les données d’entrée sont transmises dans son intégralité, comme décrit précédemment.</span><span class="sxs-lookup"><span data-stu-id="a9dac-108">When there are **\[in,out\]** pipe arguments combined with **\[in,out\]** non-pipe arguments, first the input data is transmitted in its entirety, as previously described.</span></span> <span data-ttu-id="a9dac-109">Ensuite, les données de sortie sont transmises comme décrit précédemment.</span><span class="sxs-lookup"><span data-stu-id="a9dac-109">Then, the output data is transmitted as previously described.</span></span>

<span data-ttu-id="a9dac-110">La restriction suivante s’applique à cette implémentation (MIDL 3,0) de canaux : quand vous combinez des types de canal et d’autres types dans un appel de procédure distante unique, les paramètres non-pipe doivent avoir une taille bien définie pour permettre au compilateur MIDL de calculer la taille de la mémoire tampon nécessaire.</span><span class="sxs-lookup"><span data-stu-id="a9dac-110">The following restriction applies to this (MIDL 3.0) implementation of pipes: When you combine pipe types and other types in a single remote procedure call, the nonpipe parameters must have a well-defined size in order to allow the MIDL compiler to calculate the buffer size needed.</span></span> <span data-ttu-id="a9dac-111">Par exemple, vous ne pouvez pas combiner des paramètres de canal à l’aide d’un \[ [](/windows/desktop/Midl/unique) \] pointeur unique ou d’une structure conforme, car leur taille ne peut pas être déterminée au moment de la compilation.</span><span class="sxs-lookup"><span data-stu-id="a9dac-111">For example, you cannot combine pipe parameters with a \[ [unique](/windows/desktop/Midl/unique)\] pointer or a conformant structure, since their sizes cannot be determined at compile time.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a9dac-112">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="a9dac-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a9dac-113">canal</span><span class="sxs-lookup"><span data-stu-id="a9dac-113">pipe</span></span>](/windows/desktop/Midl/pipe)
</dt> <dt>

[<span data-ttu-id="a9dac-114">/Oi</span><span class="sxs-lookup"><span data-stu-id="a9dac-114">/Oi</span></span>](/windows/desktop/Midl/-oi)
</dt> </dl>

 

 