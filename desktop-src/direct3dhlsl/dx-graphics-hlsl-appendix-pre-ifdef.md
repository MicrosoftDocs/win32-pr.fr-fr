---
title: " Directives ifdef et ifndef"
description: Directives de préprocesseur qui déterminent si une constante ou une macro de préprocesseur spécifique est définie.
ms.assetid: c1cc2e1d-2599-45ec-9629-56c4b42e0d0e
keywords:
- ifdef et ifndef directives HLSL
topic_type:
- apiref
api_name:
- ifdef and ifndef Directives
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 338308b58f1cdc68ec78984e65ffbf056a36b10b
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/25/2019
ms.locfileid: "104030238"
---
# <a name="ifdef-and-ifndef-directives"></a><span data-ttu-id="e7280-104">\#Directives ifdef et \# ifndef</span><span class="sxs-lookup"><span data-stu-id="e7280-104">\#ifdef and \#ifndef Directives</span></span>

<span data-ttu-id="e7280-105">Directives de préprocesseur qui déterminent si une constante ou une macro de préprocesseur spécifique est définie.</span><span class="sxs-lookup"><span data-stu-id="e7280-105">Preprocessor directives that determine whether a specific preprocessor constant or macro is defined.</span></span>



| <span data-ttu-id="e7280-106">\#*identificateur* ifdef...</span><span class="sxs-lookup"><span data-stu-id="e7280-106">\#ifdef *identifier* ...</span></span>  |
|---------------------------|
| <span data-ttu-id="e7280-107">\#endif</span><span class="sxs-lookup"><span data-stu-id="e7280-107">\#endif</span></span>                   |
| <span data-ttu-id="e7280-108">\#ifndef *identificateur* ...</span><span class="sxs-lookup"><span data-stu-id="e7280-108">\#ifndef *identifier* ...</span></span> |
| <span data-ttu-id="e7280-109">\#endif</span><span class="sxs-lookup"><span data-stu-id="e7280-109">\#endif</span></span>                   |



 

## <a name="parameters"></a><span data-ttu-id="e7280-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e7280-110">Parameters</span></span>



| <span data-ttu-id="e7280-111">Élément</span><span class="sxs-lookup"><span data-stu-id="e7280-111">Item</span></span>                                                                              | <span data-ttu-id="e7280-112">Description</span><span class="sxs-lookup"><span data-stu-id="e7280-112">Description</span></span>                                               |
|-----------------------------------------------------------------------------------|-----------------------------------------------------------|
| <span data-ttu-id="e7280-113"><span id="identifier"></span><span id="IDENTIFIER"></span>*identificateur*</span><span class="sxs-lookup"><span data-stu-id="e7280-113"><span id="identifier"></span><span id="IDENTIFIER"></span>*identifier*</span></span><br/> | <span data-ttu-id="e7280-114">Identificateur de la constante ou de la macro à vérifier.</span><span class="sxs-lookup"><span data-stu-id="e7280-114">Identifier of the constant or macro to check.</span></span> <br/> |



 

## <a name="remarks"></a><span data-ttu-id="e7280-115">Notes</span><span class="sxs-lookup"><span data-stu-id="e7280-115">Remarks</span></span>

<span data-ttu-id="e7280-116">Vous pouvez utiliser les \# directives ifdef et \# ifndef partout où peut [ \# ](dx-graphics-hlsl-appendix-pre-if.md) être utilisé.</span><span class="sxs-lookup"><span data-stu-id="e7280-116">You can use the \#ifdef and \#ifndef directives anywhere that the [\#if](dx-graphics-hlsl-appendix-pre-if.md) can be used.</span></span> <span data-ttu-id="e7280-117">L' \# instruction ifdef est équivalente à la directive.</span><span class="sxs-lookup"><span data-stu-id="e7280-117">The \#ifdef statement is equivalent to ) directive.</span></span> <span data-ttu-id="e7280-118">Ces directives vérifient uniquement la présence ou l’absence d’identificateurs définis à l’aide de la directive [ \# define](dx-graphics-hlsl-appendix-pre-define.md) , et non des identificateurs déclarés dans le code source C ou C++.</span><span class="sxs-lookup"><span data-stu-id="e7280-118">These directives check only for the presence or absence of identifiers defined using the [\#define](dx-graphics-hlsl-appendix-pre-define.md) directive, not for identifiers declared in the C or C++ source code.</span></span>

<span data-ttu-id="e7280-119">Ces directives sont fournies uniquement pour des raisons de compatibilité avec les versions antérieures du langage.</span><span class="sxs-lookup"><span data-stu-id="e7280-119">These directives are provided only for compatibility with previous versions of the language.</span></span> <span data-ttu-id="e7280-120">L’utilisation de l’opérateur [défini](dx-graphics-hlsl-appendix-pre-if.md) avec la \# directive if est recommandée.</span><span class="sxs-lookup"><span data-stu-id="e7280-120">The use of the [defined](dx-graphics-hlsl-appendix-pre-if.md) operator with the \#if directive is preferred.</span></span>

<span data-ttu-id="e7280-121">La \# directive ifndef vérifie l’inverse de la condition vérifiée par \# ifdef.</span><span class="sxs-lookup"><span data-stu-id="e7280-121">The \#ifndef directive checks for the opposite of the condition checked by \#ifdef.</span></span> <span data-ttu-id="e7280-122">Si l’identificateur n’est pas défini, la condition est vraie (différente de zéro); dans le cas contraire, la condition est false (zéro).</span><span class="sxs-lookup"><span data-stu-id="e7280-122">If the identifier is not defined, the condition is true (nonzero); otherwise, the condition is false (zero).</span></span>

## <a name="examples"></a><span data-ttu-id="e7280-123">Exemples</span><span class="sxs-lookup"><span data-stu-id="e7280-123">Examples</span></span>

<span data-ttu-id="e7280-124">identifier peut être passé à partir de la ligne de commande à l'aide de l'option /D.</span><span class="sxs-lookup"><span data-stu-id="e7280-124">The identifier can be passed from the command line using the /D option.</span></span> <span data-ttu-id="e7280-125">Jusqu'à 30 macros peuvent être spécifiées avec /D.</span><span class="sxs-lookup"><span data-stu-id="e7280-125">Up to 30 macros can be specified with /D.</span></span> <span data-ttu-id="e7280-126">Cela est utile pour vérifier si une définition existe, car une définition peut être transmise à partir de la ligne de commande.</span><span class="sxs-lookup"><span data-stu-id="e7280-126">This is useful for checking whether a definition exists, because a definition can be passed from the command line.</span></span> <span data-ttu-id="e7280-127">L’exemple suivant utilise ce comportement pour déterminer s’il faut exécuter une application en mode test.</span><span class="sxs-lookup"><span data-stu-id="e7280-127">The following example uses this behavior to determine whether to run an application in test mode.</span></span>


```
// PROG.CPP
#ifndef test
  #define final
#endif
int main()
{
}
```



<span data-ttu-id="e7280-128">En cas de compilation à l’aide de la commande suivante, Prog. cpp est compilé en mode test. dans le cas contraire, elle sera compilée en mode final.</span><span class="sxs-lookup"><span data-stu-id="e7280-128">When compiled using the following command, prog.cpp will compile in test mode; otherwise, it will compile in final mode.</span></span>


```
CL.EXE /Dtest prog.cpp
```



## <a name="see-also"></a><span data-ttu-id="e7280-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e7280-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e7280-130">Directives de préprocesseur (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="e7280-130">Preprocessor Directives (DirectX HLSL)</span></span>](dx-graphics-hlsl-appendix-preprocessor.md)
</dt> <dt>

[<span data-ttu-id="e7280-131">\#Si,)</span><span class="sxs-lookup"><span data-stu-id="e7280-131">\#if, )</span></span>](dx-graphics-hlsl-appendix-pre-if.md)
</dt> </dl>

 

 





