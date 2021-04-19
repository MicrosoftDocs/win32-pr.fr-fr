---
title: Activation du STRICT
description: Lorsque vous définissez le symbole STRICT, vous activez des fonctionnalités qui requièrent plus de soin pour déclarer et utiliser des types.
ms.assetid: 4029c7a7-108a-40cb-8600-eb23968e9d8a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e0400b67025f11dc9c58553f6835b2a8e2b36b4c
ms.sourcegitcommit: 35bb565804eaeed7ac5503595753f59d120076dd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/09/2021
ms.locfileid: "106531441"
---
# <a name="enabling-strict"></a><span data-ttu-id="4e234-103">Activation du STRICT</span><span class="sxs-lookup"><span data-stu-id="4e234-103">Enabling STRICT</span></span>

<span data-ttu-id="4e234-104">Lorsque vous définissez le symbole **strict** , vous activez des fonctionnalités qui requièrent plus de soin pour déclarer et utiliser des types.</span><span class="sxs-lookup"><span data-stu-id="4e234-104">When you define the **STRICT** symbol, you enable features that require more care in declaring and using types.</span></span> <span data-ttu-id="4e234-105">Cela vous permet d’écrire du code plus portable.</span><span class="sxs-lookup"><span data-stu-id="4e234-105">This helps you write more portable code.</span></span> <span data-ttu-id="4e234-106">Cela permet également de réduire le temps de débogage.</span><span class="sxs-lookup"><span data-stu-id="4e234-106">This extra care will also reduce your debugging time.</span></span> <span data-ttu-id="4e234-107">L’activation de **strict** redéfinit certains types de données afin que le compilateur n’autorise pas l’affectation d’un type à un autre sans cast explicite.</span><span class="sxs-lookup"><span data-stu-id="4e234-107">Enabling **STRICT** redefines certain data types so that the compiler does not permit assignment from one type to another without an explicit cast.</span></span> <span data-ttu-id="4e234-108">Cela s’avère particulièrement utile avec le code Windows.</span><span class="sxs-lookup"><span data-stu-id="4e234-108">This is especially helpful with Windows code.</span></span> <span data-ttu-id="4e234-109">Les erreurs lors du passage de types de données sont signalées au moment de la compilation au lieu de provoquer des erreurs irrécupérables au moment de l’exécution.</span><span class="sxs-lookup"><span data-stu-id="4e234-109">Errors in passing data types are reported at compile time instead of causing fatal errors at run time.</span></span>

<span data-ttu-id="4e234-110">Avec Visual C++, la vérification de type **stricte** est définie par défaut.</span><span class="sxs-lookup"><span data-stu-id="4e234-110">With Visual C++, **STRICT** type checking is defined by default.</span></span>

<span data-ttu-id="4e234-111">Pour définir **strict** au niveau fichier par fichier, insérez une instruction **\# define** avant d’inclure Windows. h :</span><span class="sxs-lookup"><span data-stu-id="4e234-111">To define **STRICT** on a file-by-file basis, insert a **\#define** statement before including Windows.h:</span></span>


```C++
#define STRICT
#include <windows.h>
```



<span data-ttu-id="4e234-112">Lorsque **strict** est défini, les définitions de [type de données](windows-data-types.md) changent comme suit :</span><span class="sxs-lookup"><span data-stu-id="4e234-112">When **STRICT** is defined, [data type](windows-data-types.md) definitions change as follows:</span></span>

-   <span data-ttu-id="4e234-113">Les types de handles spécifiques sont définis comme s’excluant mutuellement ; par exemple, vous ne pourrez pas passer un **HWND** où un argument de type **HDC** est requis.</span><span class="sxs-lookup"><span data-stu-id="4e234-113">Specific handle types are defined to be mutually exclusive; for example, you will not be able to pass an **HWND** where an **HDC** type argument is required.</span></span> <span data-ttu-id="4e234-114">Sans **strict**, tous les handles sont définis comme **handle**, donc le compilateur ne vous empêche pas d’utiliser un type de handle où un autre type est attendu.</span><span class="sxs-lookup"><span data-stu-id="4e234-114">Without **STRICT**, all handles are defined as **HANDLE**, so the compiler does not prevent you from using one type of handle where another type is expected.</span></span>
-   <span data-ttu-id="4e234-115">Tous les types de fonctions de rappel (tels que les procédures de dialogue, les procédures de fenêtre et les procédures de Hook) sont définis avec des prototypes complets.</span><span class="sxs-lookup"><span data-stu-id="4e234-115">All callback function types (such as dialog procedures, window procedures, and hook procedures) are defined with full prototypes.</span></span> <span data-ttu-id="4e234-116">Cela vous empêche de déclarer des fonctions de rappel avec des listes de paramètres incorrectes.</span><span class="sxs-lookup"><span data-stu-id="4e234-116">This prevents you from declaring callback functions with incorrect parameter lists.</span></span>
-   <span data-ttu-id="4e234-117">Les types de paramètre et de valeur de retour qui doivent utiliser un pointeur générique sont déclarés correctement comme **LPVOID** au lieu de **LPSTR** ou d’un autre type de pointeur.</span><span class="sxs-lookup"><span data-stu-id="4e234-117">Parameter and return value types that should use a generic pointer are declared correctly as **LPVOID** instead of as **LPSTR** or another pointer type.</span></span>
-   <span data-ttu-id="4e234-118">La structure [**COMSTAT**](/windows/desktop/api/winbase/ns-winbase-comstat) est déclarée en fonction de la norme ANSI.</span><span class="sxs-lookup"><span data-stu-id="4e234-118">The [**COMSTAT**](/windows/desktop/api/winbase/ns-winbase-comstat) structure is declared according to the ANSI standard.</span></span>

## <a name="related-topics"></a><span data-ttu-id="4e234-119">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="4e234-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4e234-120">Désactivation de STRICT</span><span class="sxs-lookup"><span data-stu-id="4e234-120">Disabling STRICT</span></span>](disabling-strict.md)
</dt> <dt>

[<span data-ttu-id="4e234-121">Conformité STRICTe</span><span class="sxs-lookup"><span data-stu-id="4e234-121">STRICT Compliance</span></span>](strict-compliance.md)
</dt> </dl>

 

 
