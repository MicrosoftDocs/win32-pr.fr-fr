---
title: Attribut disable_consistency_check
description: Indique à RPC de ne pas appliquer la vérification de cohérence de corrélation.
ms.assetid: 33ba331d-56e5-4965-a844-7780ea81623d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc55197b5eb680533745a09d4fca4f5827574a7c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104309565"
---
# <a name="disable_consistency_check-attribute"></a><span data-ttu-id="b2674-103">désactiver \_ l' \_ attribut de vérification de cohérence</span><span class="sxs-lookup"><span data-stu-id="b2674-103">disable\_consistency\_check Attribute</span></span>

<span data-ttu-id="b2674-104">Indique à RPC de ne pas appliquer la vérification de cohérence de corrélation.</span><span class="sxs-lookup"><span data-stu-id="b2674-104">Directs RPC to not enforce correlation consistency checking.</span></span>

``` syntax
interface interface-name
{
  return-type function-name(
        [[attribute-list,] disable_consistency_check] param-type param-name
}
```

<span data-ttu-id="b2674-105">Pour les paramètres corrélés, RPC s’impose qu’une mémoire tampon non null est transmise lorsque la variable de nombre de corrélations est non null.</span><span class="sxs-lookup"><span data-stu-id="b2674-105">For correlated parameters, RPC will enforce that a non-null buffer is passed when the correlation count variable is non-null.</span></span>

## <a name="example"></a><span data-ttu-id="b2674-106">Exemple</span><span class="sxs-lookup"><span data-stu-id="b2674-106">Example</span></span>

``` syntax
HRESULT PassString( [in] DWORD Length, [in, unique, string, 
    size_is( Length )]LPWSTR MyString );
```

<span data-ttu-id="b2674-107">Si *myString* a la **valeur null**, RPC rejette l’appel, sauf si length a la valeur 0.</span><span class="sxs-lookup"><span data-stu-id="b2674-107">If *MyString* is **NULL**, RPC will reject the call unless Length is set to 0.</span></span> <span data-ttu-id="b2674-108">Notez que RPC autorise la *longueur* à être égale à 0 alors que *MYSTRING* est non null et que RPC traite *myString* comme une allocation de mémoire tampon de longueur 0.</span><span class="sxs-lookup"><span data-stu-id="b2674-108">Note that RPC will allow *Length* to be 0 while *MyString* is non-NULL, and RPC will treat *MyString* as a 0-length buffer allocation.</span></span>

## <a name="remarks"></a><span data-ttu-id="b2674-109">Notes</span><span class="sxs-lookup"><span data-stu-id="b2674-109">Remarks</span></span>

<span data-ttu-id="b2674-110">Pour désactiver cette vérification, l’IDL peut contenir l' \[ attribut désactiver la \_ \_ vérification \] de cohérence sur un type de paramètre, typedef ou pointeur.</span><span class="sxs-lookup"><span data-stu-id="b2674-110">To disable this checking, the IDL can contain the \[disable\_consistency\_check\] attribute on a parameter, typedef, or pointer type.</span></span> <span data-ttu-id="b2674-111">Cela permet à RPC de ne pas appliquer la cohérence entre le pointeur de mémoire tampon et la variable de corrélation pour la mémoire tampon vers laquelle pointe le paramètre ou le pointeur.</span><span class="sxs-lookup"><span data-stu-id="b2674-111">This will direct RPC to not enforce the consistency between the buffer pointer and the correlation variable for the buffer pointed to by the parameter or pointer.</span></span>

<span data-ttu-id="b2674-112">Pour désactiver la vérification de cohérence pour l’intégralité de la compilation MIDL (et désactiver l’application de la vérification dans tous les cas), vous pouvez utiliser le commutateur de ligne de commande MIDL [/Backward \_ compat MAYBENULL \_ Size](-backward-compat.md) .</span><span class="sxs-lookup"><span data-stu-id="b2674-112">To disable consistency checking for an entire MIDL compilation (and disable enforcement of the checking in all cases), the MIDL command line switch [/backward\_compat maybenull\_sizeis](-backward-compat.md) can be used.</span></span> <span data-ttu-id="b2674-113">Cela requiert que la cible de la compilation MIDL soit au moins â € «Target NT60.</span><span class="sxs-lookup"><span data-stu-id="b2674-113">This requires that the target of the MIDL compilation be at least â€“target NT60.</span></span>

 

 




