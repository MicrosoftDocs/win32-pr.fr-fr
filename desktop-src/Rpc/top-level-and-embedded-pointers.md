---
title: Pointeurs Top-Level et incorporés
description: Pour comprendre comment les pointeurs et leurs éléments de données associés sont alloués dans Microsoft RPC, vous devez faire la différence entre les pointeurs de niveau supérieur et les pointeurs incorporés.
ms.assetid: 217b9200-827c-4d36-9412-5e65858b8a97
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ee84fcecdb70c67d7c99b4bbd3753c244a87cd07
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104462423"
---
# <a name="top-level-and-embedded-pointers"></a><span data-ttu-id="a3ebc-103">Pointeurs Top-Level et incorporés</span><span class="sxs-lookup"><span data-stu-id="a3ebc-103">Top-Level and Embedded Pointers</span></span>

<span data-ttu-id="a3ebc-104">Pour comprendre comment les pointeurs et leurs éléments de données associés sont alloués dans Microsoft RPC, vous devez faire la différence entre les *pointeurs de niveau supérieur* et les *pointeurs incorporés*.</span><span class="sxs-lookup"><span data-stu-id="a3ebc-104">To understand how pointers and their associated data elements are allocated in Microsoft RPC, you have to differentiate between *top-level pointers* and *embedded pointers*.</span></span> <span data-ttu-id="a3ebc-105">Il est également utile de faire référence au jeu de tous les pointeurs qui ne sont pas des pointeurs de niveau supérieur.</span><span class="sxs-lookup"><span data-stu-id="a3ebc-105">It is also useful to refer to the set of all pointers that are not top-level pointers.</span></span>

<span data-ttu-id="a3ebc-106">Les *pointeurs de niveau supérieur* sont ceux qui sont spécifiés en tant que noms de paramètres dans les prototypes de fonction.</span><span class="sxs-lookup"><span data-stu-id="a3ebc-106">*Top-level pointers* are those that are specified as the names of parameters in function prototypes.</span></span> <span data-ttu-id="a3ebc-107">Les pointeurs de niveau supérieur et leurs référents sont toujours alloués sur le serveur.</span><span class="sxs-lookup"><span data-stu-id="a3ebc-107">Top-level pointers and their referents are always allocated on the server.</span></span>

<span data-ttu-id="a3ebc-108">Les *pointeurs incorporés* sont des pointeurs incorporés dans les structures de données telles que les tableaux, les structures et les unions.</span><span class="sxs-lookup"><span data-stu-id="a3ebc-108">*Embedded pointers* are pointers that are embedded in data structures such as arrays, structures, and unions.</span></span> <span data-ttu-id="a3ebc-109">Lorsque les pointeurs incorporés écrivent uniquement la sortie dans une mémoire tampon et que la valeur est null en entrée, l’application serveur peut modifier leurs valeurs en valeur non null.</span><span class="sxs-lookup"><span data-stu-id="a3ebc-109">When embedded pointers only write output to a buffer and are null on input, the server application can change their values to non-null.</span></span> <span data-ttu-id="a3ebc-110">Dans ce cas, les stubs du client allouent une nouvelle mémoire pour ces données.</span><span class="sxs-lookup"><span data-stu-id="a3ebc-110">In this case, the client stubs allocate new memory for this data.</span></span>

<span data-ttu-id="a3ebc-111">Si le pointeur incorporé n’est pas null sur le client avant l’appel, les stubs n’allouent pas de mémoire sur le client lors du retour.</span><span class="sxs-lookup"><span data-stu-id="a3ebc-111">If the embedded pointer is not null on the client before the call, the stubs do not allocate memory on the client on return.</span></span> <span data-ttu-id="a3ebc-112">Au lieu de cela, les stubs essaient d’écrire la mémoire associée au pointeur incorporé dans la mémoire existante sur le client associé à ce pointeur, en remplaçant les données déjà présentes.</span><span class="sxs-lookup"><span data-stu-id="a3ebc-112">Instead, the stubs attempt to write the memory associated with the embedded pointer into the existing memory on the client associated with that pointer, overwriting the data already there.</span></span>

> [!Note]  
> <span data-ttu-id="a3ebc-113">Pour les données lues ou écrites dans une mémoire tampon, et qui ne spécifie pas la taille de la mémoire tampon, la longueur de sortie doit être inférieure ou égale à la longueur d’entrée.</span><span class="sxs-lookup"><span data-stu-id="a3ebc-113">For data read from or writen to a buffer, and which does not specify the buffer size, output length must be less than or equal to input length.</span></span> <span data-ttu-id="a3ebc-114">Une exception RPC est levée quand un dépassement de capacité est détecté.</span><span class="sxs-lookup"><span data-stu-id="a3ebc-114">An RPC exception is raised when overflow is detected.</span></span> <span data-ttu-id="a3ebc-115">Pour les données de type chaîne, la longueur de sortie est déterminée en vérifiant la longueur de la chaîne d’entrée.</span><span class="sxs-lookup"><span data-stu-id="a3ebc-115">For string data, output length is determined by checking length of the input string.</span></span> <span data-ttu-id="a3ebc-116">Par conséquent, les chaînes de sortie ne peuvent pas dépasser la longueur des chaînes d’entrée.</span><span class="sxs-lookup"><span data-stu-id="a3ebc-116">Therefore, output strings cannot exceed length of input strings.</span></span> <span data-ttu-id="a3ebc-117">La meilleure pratique consiste à éviter cela en incluant toujours un paramètre de taille spécifié pour indiquer la taille de la mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="a3ebc-117">Best practice guidance is to avoid this by always including a size-specified parameter to indicate size of the buffer.</span></span>

 

<span data-ttu-id="a3ebc-118">Les pointeurs incorporés en écriture seule sont décrits dans la [combinaison d’attributs pointeur et directionnel](combining-pointer-and-directional-attributes.md).</span><span class="sxs-lookup"><span data-stu-id="a3ebc-118">Embedded write-only pointers are discussed in [Combining Pointer and Directional Attributes](combining-pointer-and-directional-attributes.md).</span></span>

<span data-ttu-id="a3ebc-119">Le terme *pointeurs de niveau nontop* fait référence à tous les pointeurs qui ne sont pas spécifiés en tant que noms de paramètres dans le prototype de fonction, y compris les pointeurs incorporés et les différents niveaux de pointeurs imbriqués.</span><span class="sxs-lookup"><span data-stu-id="a3ebc-119">The term *nontop-level pointers* refers to all pointers that are not specified as parameter names in the function prototype, including both embedded pointers and multiple levels of nested pointers.</span></span>

 

 




