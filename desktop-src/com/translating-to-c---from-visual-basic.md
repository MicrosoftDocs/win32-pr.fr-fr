---
title: Conversion en C++ à partir de Visual Basic
description: Visual Basic gère les pointeurs implicitement. En C++, votre application est chargée d’effectuer les opérations arithmétiques de pointeur nécessaires.
ms.assetid: bbbcaba1-cf5a-4768-ad1d-22a040bfe384
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 53de112f19b51be92657fb3293bb35e1d41ff9b7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104196732"
---
# <a name="translating-to-c-from-visual-basic"></a><span data-ttu-id="80504-104">Conversion en C++ à partir de Visual Basic</span><span class="sxs-lookup"><span data-stu-id="80504-104">Translating to C++ from Visual Basic</span></span>

<span data-ttu-id="80504-105">Visual Basic gère les pointeurs implicitement.</span><span class="sxs-lookup"><span data-stu-id="80504-105">Visual Basic handles pointers implicitly.</span></span> <span data-ttu-id="80504-106">En C++, votre application est chargée d’effectuer les opérations arithmétiques de pointeur nécessaires.</span><span class="sxs-lookup"><span data-stu-id="80504-106">In C++, your application is responsible for performing any necessary pointer arithmetic.</span></span>

<span data-ttu-id="80504-107">Par défaut, Visual Basic transmet les paramètres par référence (en tant que pointeurs).</span><span class="sxs-lookup"><span data-stu-id="80504-107">By default, Visual Basic passes parameters by reference (as pointers).</span></span> <span data-ttu-id="80504-108">Les paramètres qui sont destinés à être passés par valeur uniquement sont spécifiés par le mot clé **ByVal**.</span><span class="sxs-lookup"><span data-stu-id="80504-108">Parameters that are meant to be passed by value only are specified by the keyword **ByVal**.</span></span> <span data-ttu-id="80504-109">Par exemple, un paramètre de  **type entier** **ByVal** â dans Visual Basic équivaut à un paramètre **short** en C++, alors qu’un paramètre de  **type entier** **ByRef** â dans Visual Basic équivaut à un paramètre **short \*** .</span><span class="sxs-lookup"><span data-stu-id="80504-109">For example, a **ByVal** Â  **Integer** parameter in Visual Basic is equivalent to a **short** parameter in C++, whereas a **ByRef** Â  **Integer** parameter in Visual Basic is equivalent to a **short\*** parameter.</span></span>

<span data-ttu-id="80504-110">Un paramètre déclaré **comme chaîne** dans Visual Basic est déclaré en tant que pointeur vers un **BSTR** en C++.</span><span class="sxs-lookup"><span data-stu-id="80504-110">A parameter that is declared **As String** in Visual Basic is declared as a pointer to a **BSTR** in C++.</span></span> <span data-ttu-id="80504-111">La définition d’un pointeur de chaîne sur **null** en C++ équivaut à définir la chaîne sur la constante **vbNullString** dans Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="80504-111">Setting a string pointer to **NULL** in C++ is equivalent to setting the string to the **vbNullString** constant in Visual Basic.</span></span> <span data-ttu-id="80504-112">La transmission d’une chaîne de longueur nulle ("") à une fonction conçue pour recevoir la **valeur null** ne fonctionne pas, car elle passe un pointeur vers une chaîne de longueur nulle au lieu d’un pointeur zéro.</span><span class="sxs-lookup"><span data-stu-id="80504-112">Passing a zero-length string ("") to a function designed to receive **NULL** does not work, because this passes a pointer to a zero-length string instead of a zero pointer.</span></span>

<span data-ttu-id="80504-113">C++ et Visual Basic diffèrent légèrement dans la façon dont ils représentent des propriétés.</span><span class="sxs-lookup"><span data-stu-id="80504-113">C++ and Visual Basic differ slightly in how they represent properties.</span></span> <span data-ttu-id="80504-114">En C++, les propriétés sont représentées sous la forme d’un ensemble de fonctions d’accesseur, une qui définit la valeur de la propriété et une qui récupère la valeur de la propriété.</span><span class="sxs-lookup"><span data-stu-id="80504-114">In C++, properties are represented as a set of accessor functions, one that sets the property value and one that retrieves the property value.</span></span> <span data-ttu-id="80504-115">Dans Visual Basic, les propriétés sont représentées sous la forme d’un seul élément qui peut être utilisé pour récupérer ou définir la valeur de la propriété.</span><span class="sxs-lookup"><span data-stu-id="80504-115">In Visual Basic, properties are represented as a single item that can be used to retrieve or set the property value.</span></span>

## <a name="related-topics"></a><span data-ttu-id="80504-116">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="80504-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="80504-117">Traduire en C++</span><span class="sxs-lookup"><span data-stu-id="80504-117">Translating to C++</span></span>](translating-to-c--.md)
</dt> </dl>

 

 




