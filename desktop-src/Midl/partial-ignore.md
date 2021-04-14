---
title: attribut partial_ignore
description: L’attribut ACF \ partial \_ ignore \ définit une version spécialisée de \ pointeurs uniques \ qui fournissent une sémantique de sortie facultative.
ms.assetid: 8a8f88b0-4a12-496d-bf77-ee57241b577b
keywords:
- partial_ignore MIDL de l’attribut
topic_type:
- apiref
api_name:
- partial_ignore
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 82d133275ca77032341d160b51b95b20235c8f2a
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/25/2019
ms.locfileid: "104380913"
---
# <a name="partial_ignore-attribute"></a><span data-ttu-id="f0343-104">\_attribut ignore partiel</span><span class="sxs-lookup"><span data-stu-id="f0343-104">partial\_ignore attribute</span></span>

<span data-ttu-id="f0343-105">L’attribut CCP **\[ Partial \_ ignore \]** définit une version spécialisée de pointeurs **\[ uniques \]** qui fournit une sémantique de sortie facultative.</span><span class="sxs-lookup"><span data-stu-id="f0343-105">The ACF attribute **\[partial\_ignore\]** defines a specialized version of **\[unique\]** pointers that provides optional-out semantics.</span></span>

``` syntax
[ [function-attribute-list <>] ] type-specifier <> [pointer- <>declarator <>] function-name <>( [ partial_ignore [ , parameter-attribute-list <> ] ] type-specifier <> [declarator <>] , ...);
```

## <a name="remarks"></a><span data-ttu-id="f0343-106">Notes</span><span class="sxs-lookup"><span data-stu-id="f0343-106">Remarks</span></span>

<span data-ttu-id="f0343-107">Lors de la création d’une fonction, il est courant de permettre aux utilisateurs de spécifier un pointeur non **null** vers des données de retour facultatives, souvent appelées pointeur facultatif-out.</span><span class="sxs-lookup"><span data-stu-id="f0343-107">When creating a function, it is common to allow users to specify a non-**NULL** pointer to optional return data, often referred to as an optional-out pointer.</span></span> <span data-ttu-id="f0343-108">La mémoire vers laquelle pointe l’utilisateur n’est généralement pas obligatoirement initialisée.</span><span class="sxs-lookup"><span data-stu-id="f0343-108">The memory pointed to by the user is not typically required to be initialized.</span></span> <span data-ttu-id="f0343-109">Cette technique représente un problème lorsque la fonction est utilisée sur RPC.</span><span class="sxs-lookup"><span data-stu-id="f0343-109">This technique represents a problem when the function is used over RPC.</span></span>

<span data-ttu-id="f0343-110">Si le pointeur facultatif-out est valide, mais qu’il pointe vers des données non initialisées, RPC tente de marshaler ces données et de les envoyer au serveur, ce qui peut entraîner l’échec du marshaling et l’abandon de l’appel.</span><span class="sxs-lookup"><span data-stu-id="f0343-110">If the optional-out pointer is valid, but points to uninitialized data, RPC attempts to marshal that data and send it to the server, which can cause the marshaling to fail and abort the call.</span></span> <span data-ttu-id="f0343-111">Même si le marshaling s’effectue correctement, un nombre potentiellement important de données inutiles sont envoyées au serveur.</span><span class="sxs-lookup"><span data-stu-id="f0343-111">Even if the marshaling succeeds, a potentially large amount of useless data is sent to the server.</span></span>

<span data-ttu-id="f0343-112">Ces problèmes sont résolus en marquant le pointeur **\[ sur in, out, unique et \_ Partial \] ignore**.</span><span class="sxs-lookup"><span data-stu-id="f0343-112">These problems are solved by marking the pointer as **\[in, out, unique, partial\_ignore\]**.</span></span> <span data-ttu-id="f0343-113">Les quatre attributs doivent être présents.</span><span class="sxs-lookup"><span data-stu-id="f0343-113">All four attributes must be present.</span></span> <span data-ttu-id="f0343-114">Lorsqu’un pointeur **\[ \_ ignore \] partiellement** est marshalé côté client, les seules données envoyées au serveur sont un indicateur qui indique si le pointeur est **null**.</span><span class="sxs-lookup"><span data-stu-id="f0343-114">When a **\[partial\_ignore\]** pointer is marshaled on the client side, the only data sent to the server is an indicator showing whether the pointer is **NULL**.</span></span> <span data-ttu-id="f0343-115">Si le pointeur n’est pas **null**, la routine côté serveur reçoit un pointeur valide vers un bloc de mémoire qui a été initialisé avec des zéros.</span><span class="sxs-lookup"><span data-stu-id="f0343-115">If the pointer is non-**NULL**, the server-side routine receives a valid pointer to a block of memory that has been initialized with zeros.</span></span> <span data-ttu-id="f0343-116">Si le pointeur a la **valeur null**, la routine côté serveur reçoit un pointeur **null** .</span><span class="sxs-lookup"><span data-stu-id="f0343-116">If the pointer is **NULL**, the server-side routine receives a **NULL** pointer.</span></span>

<span data-ttu-id="f0343-117">Dans ce cas, la taille maximale du pointeur doit être bien définie au moment de la compilation ou en fonction des paramètres d’entrée, car le serveur doit allouer de l’espace pour l’emplacement de la mémoire vers lequel pointe.</span><span class="sxs-lookup"><span data-stu-id="f0343-117">In this situation, the maximum size of the pointer must be well defined either at compile time or based on input parameters, because the server needs to allocate space for the memory location being pointed to.</span></span> <span data-ttu-id="f0343-118">Par exemple, un pointeur de **\[ chaîne \]** simple n’a pas une taille bien définie, car la chaîne se termine implicitement par un caractère null.</span><span class="sxs-lookup"><span data-stu-id="f0343-118">For example, a simple **\[string\]** pointer does not have a well defined size because the string is implicitly terminated by a NULL character.</span></span> <span data-ttu-id="f0343-119">Dans ce cas, la spécification de la taille maximale de la chaîne par l’ajout d’une **\[ taille \_ est \]** que l’attribut permet d’obtenir la taille requise bien définie.</span><span class="sxs-lookup"><span data-stu-id="f0343-119">In this case, specifying the maximum size of the string by adding a **\[size\_is\]** attribute would achieve the well defined size requirement.</span></span>

## <a name="examples"></a><span data-ttu-id="f0343-120">Exemples</span><span class="sxs-lookup"><span data-stu-id="f0343-120">Examples</span></span>

``` syntax
/* The MoveLeft function will move one position to the left and optionally return the previous position */
void MoveLeft([in, out, unique, partial_ignore] long *pPrevPosition);
```

## <a name="see-also"></a><span data-ttu-id="f0343-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f0343-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f0343-122">**unique**</span><span class="sxs-lookup"><span data-stu-id="f0343-122">**unique**</span></span>](unique.md)
</dt> </dl>

 

 




