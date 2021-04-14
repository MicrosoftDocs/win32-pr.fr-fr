---
title: Gestion des erreurs dans COM (COM)
description: Gestion des erreurs dans COM
ms.assetid: 15f3ae3e-1794-4948-a7aa-6309a703364b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 19af496eabf50833c99d462ff074254bc39bb7a0
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/10/2020
ms.locfileid: "104464170"
---
# <a name="error-handling-in-com-com"></a><span data-ttu-id="ead62-103">Gestion des erreurs dans COM (COM)</span><span class="sxs-lookup"><span data-stu-id="ead62-103">Error Handling in COM (COM)</span></span>

<span data-ttu-id="ead62-104">Presque toutes les fonctions COM et les méthodes d’interface retournent une valeur de type **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="ead62-104">Almost all COM functions and interface methods return a value of the type **HRESULT**.</span></span> <span data-ttu-id="ead62-105">La valeur **HRESULT** (pour la *poignée de résultat*) est un moyen de retourner des valeurs de réussite, d’avertissement et d’erreur.</span><span class="sxs-lookup"><span data-stu-id="ead62-105">The **HRESULT** (for *result handle*) is a way of returning success, warning, and error values.</span></span> <span data-ttu-id="ead62-106">Les **HRESULT** s ne sont pas des handles de tout ; Il s’agit uniquement de valeurs avec plusieurs champs encodés dans la valeur.</span><span class="sxs-lookup"><span data-stu-id="ead62-106">**HRESULT** s are really not handles to anything; they are only values with several fields encoded in the value.</span></span> <span data-ttu-id="ead62-107">Conformément à la spécification COM, un résultat de zéro indique Success et un résultat différent de zéro indique un échec.</span><span class="sxs-lookup"><span data-stu-id="ead62-107">As per the COM specification, a result of zero indicates success and a nonzero result indicates failure.</span></span>

<span data-ttu-id="ead62-108">Au niveau du code source, toutes les valeurs d’erreur se composent de trois parties, séparées par des traits de soulignement.</span><span class="sxs-lookup"><span data-stu-id="ead62-108">At the source code level, all error values consist of three parts, separated by underscores.</span></span> <span data-ttu-id="ead62-109">La première partie est le préfixe qui identifie la fonction associée à l’erreur, la deuxième partie est E pour erreur et la troisième partie est une chaîne qui décrit la condition réelle.</span><span class="sxs-lookup"><span data-stu-id="ead62-109">The first part is the prefix that identifies the facility associated with the error, the second part is E for error, and the third part is a string that describes the actual condition.</span></span> <span data-ttu-id="ead62-110">Par exemple, **STG \_ E \_ MEDIUMFULL** est retourné lorsqu’il n’y a pas d’espace libre sur un disque dur.</span><span class="sxs-lookup"><span data-stu-id="ead62-110">For example, **STG\_E\_MEDIUMFULL** is returned when there is no space left on a hard disk.</span></span> <span data-ttu-id="ead62-111">Le préfixe **STG** indique la fonctionnalité de stockage, le **E** indique que le code d’état représente une erreur et **MEDIUMFULL** fournit des informations spécifiques sur l’erreur.</span><span class="sxs-lookup"><span data-stu-id="ead62-111">The **STG** prefix indicates the storage facility, the **E** indicates that the status code represents an error, and the **MEDIUMFULL** provides specific information about the error.</span></span> <span data-ttu-id="ead62-112">La plupart des valeurs que vous pouvez souhaiter retourner à partir d’une méthode ou d’une fonction d’interface sont définies dans Winerror. h.</span><span class="sxs-lookup"><span data-stu-id="ead62-112">Many of the values that you might want to return from an interface method or function are defined in Winerror.h.</span></span>

<span data-ttu-id="ead62-113">Pour plus d’informations sur la gestion des erreurs, consultez les sections suivantes :</span><span class="sxs-lookup"><span data-stu-id="ead62-113">For more information about error handling, see the following sections:</span></span>

-   [<span data-ttu-id="ead62-114">Structure des codes d’erreur COM</span><span class="sxs-lookup"><span data-stu-id="ead62-114">Structure of COM Error Codes</span></span>](structure-of-com-error-codes.md)
-   [<span data-ttu-id="ead62-115">Codes dans ITF d’usine \_</span><span class="sxs-lookup"><span data-stu-id="ead62-115">Codes in FACILITY\_ITF</span></span>](codes-in-facility-itf.md)
-   [<span data-ttu-id="ead62-116">Utilisation de macros pour la gestion des erreurs</span><span class="sxs-lookup"><span data-stu-id="ead62-116">Using Macros for Error Handling</span></span>](using-macros-for-error-handling.md)
-   [<span data-ttu-id="ead62-117">Gestion des erreurs COM dans Java et Visual Basic</span><span class="sxs-lookup"><span data-stu-id="ead62-117">COM Error Handling in Java and Visual Basic</span></span>](com-error-handling-in-java-and-visual-basic.md)
-   [<span data-ttu-id="ead62-118">Stratégies de gestion des erreurs</span><span class="sxs-lookup"><span data-stu-id="ead62-118">Error Handling Strategies</span></span>](error-handling-strategies.md)
-   [<span data-ttu-id="ead62-119">Gestion des erreurs inconnues</span><span class="sxs-lookup"><span data-stu-id="ead62-119">Handling Unknown Errors</span></span>](handling-unknown-errors.md)

## <a name="related-topics"></a><span data-ttu-id="ead62-120">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="ead62-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ead62-121">Codes d’erreur COM</span><span class="sxs-lookup"><span data-stu-id="ead62-121">COM Error Codes</span></span>](com-error-codes.md)
</dt> </dl>

 

 




