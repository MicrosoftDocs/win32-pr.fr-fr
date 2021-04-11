---
title: Codes dans FACILITY_ITF
description: Codes dans ITF d’usine \_
ms.assetid: 1f9f7b2c-a4e4-41c0-9ba5-b8bbf722e077
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4fc4375b5956502dbaee97057d347aff1da77e3a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103939799"
---
# <a name="codes-in-facility_itf"></a><span data-ttu-id="0fe24-103">Codes dans ITF d’usine \_</span><span class="sxs-lookup"><span data-stu-id="0fe24-103">Codes in FACILITY\_ITF</span></span>

<span data-ttu-id="0fe24-104">Les **HRESULT** s avec des fonctionnalités telles que la \_ valeur null de la base de connaissances et le RPC de la fonction \_ ont une signification universelle, car ils sont définis au niveau d’une seule source : Microsoft.</span><span class="sxs-lookup"><span data-stu-id="0fe24-104">**HRESULT** s with facilities such as FACILITY\_NULL and FACILITY\_RPC have universal meaning because they are defined at a single source: Microsoft.</span></span> <span data-ttu-id="0fe24-105">Toutefois, **HRESULT** s dans ITF d’installation \_ sont déterminés par la fonction ou la méthode d’interface à partir de laquelle ils sont retournés.</span><span class="sxs-lookup"><span data-stu-id="0fe24-105">However, **HRESULT** s in FACILITY\_ITF are determined by the function or interface method from which they are returned.</span></span> <span data-ttu-id="0fe24-106">Cela signifie que la même valeur 32 bits dans ITF d’installation \_ retournée à partir de deux méthodes d’interface différentes peut avoir des significations différentes.</span><span class="sxs-lookup"><span data-stu-id="0fe24-106">This means that the same 32-bit value in FACILITY\_ITF returned from two different interface methods might have different meanings.</span></span>

<span data-ttu-id="0fe24-107">La raison pour laquelle les savesets **HRESULT** dans \_ ITF peuvent avoir des significations différentes dans des interfaces différentes est que les **HRESULT** s sont conservés à une taille de type de données efficace de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="0fe24-107">The reason **HRESULT** s in FACILITY\_ITF can have different meanings in different interfaces is that **HRESULT** s are kept to an efficient data type size of 32 bits.</span></span> <span data-ttu-id="0fe24-108">Malheureusement, 32 bits n’est pas assez grand pour le développement d’un système d’allocation de code d’erreur qui évite les codes conflictuels alloués par différents programmeurs à des moments différents (contrairement à la gestion des identificateurs d’interface et des CLSID).</span><span class="sxs-lookup"><span data-stu-id="0fe24-108">Unfortunately, 32 bits is not large enough for the development of an error code allocation system that avoids conflicting codes allocated by different programmers at different times in different places (unlike the handling of interface identifiers and CLSIDs).</span></span> <span data-ttu-id="0fe24-109">Par conséquent, la valeur **HRESULT** 32 bits est structurée de sorte que Microsoft peut définir plusieurs codes d’erreur universels, tout en permettant à d’autres programmeurs de définir de nouveaux codes d’erreur sans crainte de conflit.</span><span class="sxs-lookup"><span data-stu-id="0fe24-109">As a result, the 32-bit **HRESULT** is structured such that Microsoft can define several universal error codes, while allowing other programmers to define new error codes without fear of conflict.</span></span> <span data-ttu-id="0fe24-110">La Convention du code d’État est la suivante :</span><span class="sxs-lookup"><span data-stu-id="0fe24-110">The status code convention is as follows:</span></span>

-   <span data-ttu-id="0fe24-111">Les codes d’État dans des services autres que les ITF de service \_ ne peuvent être définis que par Microsoft.</span><span class="sxs-lookup"><span data-stu-id="0fe24-111">Status codes in facilities other than FACILITY\_ITF can be defined only by Microsoft.</span></span>
-   <span data-ttu-id="0fe24-112">Les codes d’État dans les ITF d’installation de service \_ sont définis uniquement par le développeur de l’interface ou de la fonction qui retourne le code d’État.</span><span class="sxs-lookup"><span data-stu-id="0fe24-112">Status codes in facility FACILITY\_ITF are defined solely by the developer of the interface or function that returns the status code.</span></span> <span data-ttu-id="0fe24-113">Pour éviter les codes d’erreur conflictuels, toute personne qui définit l’interface est chargée de coordonner et de publier les \_ codes d’État ITF d’installation associés à cette interface.</span><span class="sxs-lookup"><span data-stu-id="0fe24-113">To avoid conflicting error codes, whoever defines the interface is responsible for coordinating and publishing the FACILITY\_ITF status codes associated with that interface.</span></span>

<span data-ttu-id="0fe24-114">Tous les codes ITF de l’infrastructure définie par COM \_ ont une valeur de code comprise dans la plage 0x0000-0x01FF.</span><span class="sxs-lookup"><span data-stu-id="0fe24-114">All the COM-defined FACILITY\_ITF codes have a code value in the range of 0x0000-0x01FF.</span></span> <span data-ttu-id="0fe24-115">Bien qu’il soit légal d’utiliser des codes dans \_ ITF d’installation, il est recommandé d’utiliser uniquement des valeurs de code dans la plage de 0x0200-0xFFFF.</span><span class="sxs-lookup"><span data-stu-id="0fe24-115">While it is legal to use any codes in FACILITY\_ITF, it is recommended that only code values in the range of 0x0200-0xFFFF be used.</span></span> <span data-ttu-id="0fe24-116">Cette recommandation est un moyen de réduire la confusion avec les erreurs définies par COM.</span><span class="sxs-lookup"><span data-stu-id="0fe24-116">This recommendation is made as a means of reducing confusion with any COM-defined errors.</span></span>

<span data-ttu-id="0fe24-117">Il est également recommandé que les développeurs définissent de nouvelles fonctions et interfaces pour retourner des codes d’erreur tels que définis par COM et dans des installations autres que \_ ITF.</span><span class="sxs-lookup"><span data-stu-id="0fe24-117">It is also recommended that developers define new functions and interfaces to return error codes as defined by COM and in facilities other than FACILITY\_ITF.</span></span> <span data-ttu-id="0fe24-118">En particulier, les interfaces qui ont des chances d’être à distance à l’aide de RPC dans le futur doivent définir les codes RPC de l’installation \_ comme valides.</span><span class="sxs-lookup"><span data-stu-id="0fe24-118">In particular, interfaces that have any chance of being remoted using RPC in the future should define the FACILITY\_RPC codes as legal.</span></span> <span data-ttu-id="0fe24-119">E \_ inattendue est un code d’erreur spécifique que la plupart des développeurs souhaitent rendre universellement légaux.</span><span class="sxs-lookup"><span data-stu-id="0fe24-119">E\_UNEXPECTED is a specific error code that most developers will want to make universally legal.</span></span>

## <a name="related-topics"></a><span data-ttu-id="0fe24-120">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="0fe24-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0fe24-121">Gestion des erreurs dans COM</span><span class="sxs-lookup"><span data-stu-id="0fe24-121">Error Handling in COM</span></span>](error-handling-in-com.md)
</dt> </dl>

 

 




