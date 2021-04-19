---
title: Conversion en Visual Basic à partir de C++
description: Conversion en Visual Basic à partir de C++
ms.assetid: fce7ea25-cb24-4cc4-8f36-0e8aed2f3ada
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ffba519cbdb0305fe3a2eae4cc8e658fdde1eac3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106538579"
---
# <a name="translating-to-visual-basic-from-c"></a><span data-ttu-id="1d6cd-103">Conversion en Visual Basic à partir de C++</span><span class="sxs-lookup"><span data-stu-id="1d6cd-103">Translating to Visual Basic from C++</span></span>

<span data-ttu-id="1d6cd-104">À l’aide du langage de programmation C++, les développeurs peuvent accéder directement à la mémoire qui stocke une variable particulière.</span><span class="sxs-lookup"><span data-stu-id="1d6cd-104">Using the C++ programming language, developers can directly access the memory that stores a particular variable.</span></span> <span data-ttu-id="1d6cd-105">Les pointeurs de mémoire fournissent cet accès direct.</span><span class="sxs-lookup"><span data-stu-id="1d6cd-105">Memory pointers provide this direct access.</span></span> <span data-ttu-id="1d6cd-106">Dans Visual Basic, les pointeurs sont gérés pour vous.</span><span class="sxs-lookup"><span data-stu-id="1d6cd-106">In Visual Basic, pointers are handled for you.</span></span> <span data-ttu-id="1d6cd-107">Par exemple, un paramètre déclaré en tant que pointeur vers un **int** en C++ est équivalent à un paramètre déclaré dans Visual Basic en tant qu' **entier** **ByRef**.</span><span class="sxs-lookup"><span data-stu-id="1d6cd-107">For example, a parameter declared as a pointer to an **int** in C++ is equivalent to a parameter declared in Visual Basic as a **ByRef** **Integer**.</span></span>

<span data-ttu-id="1d6cd-108">Un paramètre déclaré **comme chaîne** dans Visual Basic est déclaré en tant que pointeur vers un **BSTR** en C++.</span><span class="sxs-lookup"><span data-stu-id="1d6cd-108">A parameter that is declared **As String** in Visual Basic is declared as a pointer to a **BSTR** in C++.</span></span> <span data-ttu-id="1d6cd-109">La définition d’un pointeur de chaîne sur **null** en C++ équivaut à définir la chaîne sur la constante **vbNullString** dans Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="1d6cd-109">Setting a string pointer to **NULL** in C++ is equivalent to setting the string to the **vbNullString** constant in Visual Basic.</span></span> <span data-ttu-id="1d6cd-110">Le passage d’une chaîne de longueur nulle ("") à une fonction conçue pour recevoir la **valeur null** ne fonctionne pas, car il passe un pointeur vers une chaîne de longueur nulle au lieu d’un pointeur zéro.</span><span class="sxs-lookup"><span data-stu-id="1d6cd-110">Passing in a zero-length string ("") to a function designed to receive **NULL** does not work, as this passes a pointer to a zero-length string instead of a zero pointer.</span></span>

<span data-ttu-id="1d6cd-111">C++ prend en charge les conteneurs de données, à savoir les structures et les unions, qui n’ont pas d’équivalent dans les premières versions de Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="1d6cd-111">C++ supports data containers, namely structures and unions, that have no equivalent in early versions of Visual Basic.</span></span> <span data-ttu-id="1d6cd-112">C’est la raison pour laquelle les objets COM encapsulent généralement des informations qui sont généralement stockées dans des structures et des unions dans des classes d’objets.</span><span class="sxs-lookup"><span data-stu-id="1d6cd-112">For this reason, COM objects typically wrap information that usually is stored in structures and unions in object classes.</span></span> <span data-ttu-id="1d6cd-113">Toutefois, certains objets COM peuvent contenir des structures, ce qui entraîne l’inaccessibilité des parties de la fonctionnalité ou des méthodes de l’objet pour Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="1d6cd-113">Some COM objects, however, may contain structures, causing portions of the object's methods or functionality to be inaccessible to Visual Basic.</span></span>

<span data-ttu-id="1d6cd-114">Certains types de données C++ ne sont pas pris en charge dans Visual Basic, par exemple les types non signés et les types **HWND** .</span><span class="sxs-lookup"><span data-stu-id="1d6cd-114">Some C++ data types are not supported in Visual Basic, for example unsigned types and **HWND** types.</span></span> <span data-ttu-id="1d6cd-115">Les méthodes qui acceptent ou retournent ces types de données ne sont pas disponibles dans Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="1d6cd-115">Methods that accept or return these data types are not available in Visual Basic.</span></span>

<span data-ttu-id="1d6cd-116">Visual Basic utilise des types de données compatibles Automation en tant que types de données internes.</span><span class="sxs-lookup"><span data-stu-id="1d6cd-116">Visual Basic uses Automation-compatible data types as its internal data types.</span></span> <span data-ttu-id="1d6cd-117">Ainsi, les types de données C++ compatibles Automation sont également compatibles avec Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="1d6cd-117">Thus, C++ data types that are Automation-compatible are also compatible with Visual Basic.</span></span> <span data-ttu-id="1d6cd-118">Les types de données qui ne sont pas compatibles Automation risquent de ne pas pouvoir être convertis en Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="1d6cd-118">Data types that are not Automation-compatible may not be able to be converted to Visual Basic.</span></span>

<span data-ttu-id="1d6cd-119">Le tableau suivant répertorie les types de données pris en charge par Visual Basic et leurs équivalents **VarType** .</span><span class="sxs-lookup"><span data-stu-id="1d6cd-119">The following table lists the data types are supported by Visual Basic and their **VARTYPE** equivalents.</span></span> <span data-ttu-id="1d6cd-120">**VarType** est une énumération qui répertorie les types variant Automation.</span><span class="sxs-lookup"><span data-stu-id="1d6cd-120">**VARTYPE** is an enumeration that lists the Automation variant types.</span></span>



| <span data-ttu-id="1d6cd-121">Type de données Visual Basic</span><span class="sxs-lookup"><span data-stu-id="1d6cd-121">Visual Basic data type</span></span>  | <span data-ttu-id="1d6cd-122">Équivalent VARTYPE</span><span class="sxs-lookup"><span data-stu-id="1d6cd-122">VARTYPE equivalent</span></span>                |
|-------------------------|-----------------------------------|
| <span data-ttu-id="1d6cd-123">**Integer**</span><span class="sxs-lookup"><span data-stu-id="1d6cd-123">**Integer**</span></span><br/>  | <span data-ttu-id="1d6cd-124">16 bits, signé, VT \_ I2</span><span class="sxs-lookup"><span data-stu-id="1d6cd-124">16 bit, signed, VT\_I2</span></span><br/> |
| <span data-ttu-id="1d6cd-125">**Long**</span><span class="sxs-lookup"><span data-stu-id="1d6cd-125">**Long**</span></span><br/>     | <span data-ttu-id="1d6cd-126">32 bits, signés, VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="1d6cd-126">32 bit, signed, VT\_I4</span></span><br/> |
| <span data-ttu-id="1d6cd-127">**Date**</span><span class="sxs-lookup"><span data-stu-id="1d6cd-127">**Date**</span></span><br/>     | <span data-ttu-id="1d6cd-128">\_Date VT</span><span class="sxs-lookup"><span data-stu-id="1d6cd-128">VT\_DATE</span></span><br/>               |
| <span data-ttu-id="1d6cd-129">**Devise**</span><span class="sxs-lookup"><span data-stu-id="1d6cd-129">**Currency**</span></span><br/> | <span data-ttu-id="1d6cd-130">VT \_ ca</span><span class="sxs-lookup"><span data-stu-id="1d6cd-130">VT\_CY</span></span><br/>                 |
| <span data-ttu-id="1d6cd-131">**Object**</span><span class="sxs-lookup"><span data-stu-id="1d6cd-131">**Object**</span></span><br/>   | <span data-ttu-id="1d6cd-132">\*\_distribution vt</span><span class="sxs-lookup"><span data-stu-id="1d6cd-132">\*VT\_DISPATCH</span></span><br/>         |
| <span data-ttu-id="1d6cd-133">**Chaîne**</span><span class="sxs-lookup"><span data-stu-id="1d6cd-133">**String**</span></span><br/>   | <span data-ttu-id="1d6cd-134">VT \_ BSTR</span><span class="sxs-lookup"><span data-stu-id="1d6cd-134">VT\_BSTR</span></span><br/>               |
| <span data-ttu-id="1d6cd-135">**Booléen**</span><span class="sxs-lookup"><span data-stu-id="1d6cd-135">**Boolean**</span></span><br/>  | <span data-ttu-id="1d6cd-136">VT \_ bool</span><span class="sxs-lookup"><span data-stu-id="1d6cd-136">VT\_BOOL</span></span><br/>               |
| <span data-ttu-id="1d6cd-137">**Devise**</span><span class="sxs-lookup"><span data-stu-id="1d6cd-137">**Currency**</span></span><br/> | <span data-ttu-id="1d6cd-138">\_valeur décimale VT</span><span class="sxs-lookup"><span data-stu-id="1d6cd-138">VT\_DECIMAL</span></span><br/>            |
| <span data-ttu-id="1d6cd-139">**Unique**</span><span class="sxs-lookup"><span data-stu-id="1d6cd-139">**Single**</span></span><br/>   | <span data-ttu-id="1d6cd-140">VT \_ R4</span><span class="sxs-lookup"><span data-stu-id="1d6cd-140">VT\_R4</span></span><br/>                 |
| <span data-ttu-id="1d6cd-141">**Double**</span><span class="sxs-lookup"><span data-stu-id="1d6cd-141">**Double**</span></span><br/>   | <span data-ttu-id="1d6cd-142">VT \_ R8</span><span class="sxs-lookup"><span data-stu-id="1d6cd-142">VT\_R8</span></span><br/>                 |
| <span data-ttu-id="1d6cd-143">**Décimal**</span><span class="sxs-lookup"><span data-stu-id="1d6cd-143">**Decimal**</span></span><br/>  | <span data-ttu-id="1d6cd-144">\_valeur décimale VT</span><span class="sxs-lookup"><span data-stu-id="1d6cd-144">VT\_DECIMAL</span></span><br/>            |
| <span data-ttu-id="1d6cd-145">**Byte**</span><span class="sxs-lookup"><span data-stu-id="1d6cd-145">**Byte**</span></span><br/>     | <span data-ttu-id="1d6cd-146">\_valeur décimale VT</span><span class="sxs-lookup"><span data-stu-id="1d6cd-146">VT\_DECIMAL</span></span><br/>            |
| <span data-ttu-id="1d6cd-147">**Différent**</span><span class="sxs-lookup"><span data-stu-id="1d6cd-147">**Variant**</span></span><br/>  | <span data-ttu-id="1d6cd-148">\_variante VT</span><span class="sxs-lookup"><span data-stu-id="1d6cd-148">VT\_VARIANT</span></span><br/>            |



 

<span data-ttu-id="1d6cd-149">Tous les paramètres de Visual Basic, sauf s’ils sont étiquetés avec le mot clé **ByVal**, sont passés par référence (en tant que pointeurs) et non par valeur.</span><span class="sxs-lookup"><span data-stu-id="1d6cd-149">All parameters in Visual Basic, unless labeled with the keyword **ByVal**, are passed by reference (as pointers) instead of by value.</span></span>

<span data-ttu-id="1d6cd-150">C++ et Visual Basic diffèrent légèrement dans la façon dont ils représentent des propriétés.</span><span class="sxs-lookup"><span data-stu-id="1d6cd-150">C++ and Visual Basic differ slightly in how they represent properties.</span></span> <span data-ttu-id="1d6cd-151">En C++, les propriétés sont représentées sous la forme d’un ensemble de fonctions d’accesseur, une qui définit la valeur de la propriété et une qui récupère la valeur de la propriété.</span><span class="sxs-lookup"><span data-stu-id="1d6cd-151">In C++, properties are represented as a set of accessor functions, one that sets the property value and one that retrieves the property value.</span></span> <span data-ttu-id="1d6cd-152">Dans Visual Basic, les propriétés sont représentées sous la forme d’un seul élément qui peut être utilisé pour récupérer ou définir la valeur de la propriété.</span><span class="sxs-lookup"><span data-stu-id="1d6cd-152">In Visual Basic, properties are represented as a single item that can be used to retrieve or set the property value.</span></span>

## <a name="related-topics"></a><span data-ttu-id="1d6cd-153">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="1d6cd-153">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1d6cd-154">Conversion en Visual Basic</span><span class="sxs-lookup"><span data-stu-id="1d6cd-154">Translating to Visual Basic</span></span>](translating-to-visual-basic.md)
</dt> </dl>

 

 





