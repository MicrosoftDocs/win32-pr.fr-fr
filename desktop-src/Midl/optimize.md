---
title: optimiser l’attribut
description: L’attribut \ Optimize \ ACF est utilisé pour ajuster le niveau de gradation pour le marshaling des données.
ms.assetid: d636d940-0550-417f-a21a-065bdeaeb5d9
keywords:
- MIDL d’attribut Optimize
topic_type:
- apiref
api_name:
- optimize
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c6025c40465ecf2e8fe7a33dcda50ece07d34b9d
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/25/2019
ms.locfileid: "106531600"
---
# <a name="optimize-attribute"></a><span data-ttu-id="8de8c-104">optimiser l’attribut</span><span class="sxs-lookup"><span data-stu-id="8de8c-104">optimize attribute</span></span>

<span data-ttu-id="8de8c-105">L’attribut **\[ optimize \]** ACF est utilisé pour affiner le niveau de gradation pour le marshaling des données.</span><span class="sxs-lookup"><span data-stu-id="8de8c-105">The **\[optimize\]** ACF attribute is used to fine tune the level of gradation for marshaling data.</span></span>

> [!Note]  
> <span data-ttu-id="8de8c-106">Ce mot clé est superceeded et ne doit pas être utilisé.</span><span class="sxs-lookup"><span data-stu-id="8de8c-106">This keyword is superceeded and should not be used.</span></span> <span data-ttu-id="8de8c-107">Les compilations MIDL actuelles doivent utiliser [**/Oicf**](-oi.md)[**/Robust**](-robust.md) à la place.</span><span class="sxs-lookup"><span data-stu-id="8de8c-107">Current MIDL compilations should use [**/Oicf**](-oi.md)[**/robust**](-robust.md) instead.</span></span>

 

``` syntax
optimize ("optimization-options")
```

## <a name="parameters"></a><span data-ttu-id="8de8c-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="8de8c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8de8c-109">*optimisation-options*</span><span class="sxs-lookup"><span data-stu-id="8de8c-109">*optimization-options*</span></span> 
</dt> <dd>

<span data-ttu-id="8de8c-110">Spécifie la méthode de marshaling des données.</span><span class="sxs-lookup"><span data-stu-id="8de8c-110">Specifies the method of marshaling data.</span></span> <span data-ttu-id="8de8c-111">Utilisez « s » pour le marshaling en mode mixte ou « i » pour le marshaling interprété.</span><span class="sxs-lookup"><span data-stu-id="8de8c-111">Use either "s" for mixed-mode marshaling or "i" for interpreted marshaling.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="8de8c-112">Notes</span><span class="sxs-lookup"><span data-stu-id="8de8c-112">Remarks</span></span>

<span data-ttu-id="8de8c-113">Cette version de RPC fournit deux méthodes pour le marshaling des données : mode mixte (« s ») et interprété (« i »).</span><span class="sxs-lookup"><span data-stu-id="8de8c-113">This version of RPC provides two methods for marshaling data: mixed-mode ("s") and interpreted ("i").</span></span> <span data-ttu-id="8de8c-114">Ces méthodes correspondent aux commutateurs de ligne de commande [**/OS**](-os.md) et [**/OI**](-oi.md) .</span><span class="sxs-lookup"><span data-stu-id="8de8c-114">These methods correspond to the [**/Os**](-os.md) and [**/Oi**](-oi.md) command-line switches.</span></span> <span data-ttu-id="8de8c-115">La méthode interprétée marshale les données complètement hors connexion.</span><span class="sxs-lookup"><span data-stu-id="8de8c-115">The interpreted method marshals data completely offline.</span></span> <span data-ttu-id="8de8c-116">Bien que cela puisse réduire considérablement la taille du stub, les performances peuvent être affectées.</span><span class="sxs-lookup"><span data-stu-id="8de8c-116">While this can reduce the size of the stub considerably, performance can be affected.</span></span>

<span data-ttu-id="8de8c-117">Si les performances posent un problème, la méthode en mode mixte peut être la meilleure approche.</span><span class="sxs-lookup"><span data-stu-id="8de8c-117">If performance is a concern, the mixed-mode method can be the best approach.</span></span> <span data-ttu-id="8de8c-118">Le mode mixte permet au compilateur MIDL d’effectuer la détermination entre les données qui seront marshalées en ligne et qui seront marshalées par un appel à une bibliothèque de liens dynamiques hors connexion.</span><span class="sxs-lookup"><span data-stu-id="8de8c-118">Mixed-mode allows the MIDL compiler to make the determination between which data will be marshaled inline and which will be marshaled by a call to an offline dynamic-link library.</span></span> <span data-ttu-id="8de8c-119">Si de nombreuses procédures utilisent les mêmes types de données, une procédure unique peut être appelée à plusieurs reprises pour marshaler les données.</span><span class="sxs-lookup"><span data-stu-id="8de8c-119">If many procedures use the same data types, a single procedure can be called repeatedly to marshal the data.</span></span> <span data-ttu-id="8de8c-120">De cette façon, les données les plus adaptées au marshaling en ligne sont traitées en ligne, tandis que les autres données peuvent être marshalées plus efficacement en mode hors connexion.</span><span class="sxs-lookup"><span data-stu-id="8de8c-120">In this way, data that is most suited to inline marshaling is processed inline while other data can be more efficiently marshaled offline.</span></span>

<span data-ttu-id="8de8c-121">Notez que l’attribut **\[ optimize \]** peut être utilisé en tant qu’attribut d’interface ou en tant qu’attribut d’opération.</span><span class="sxs-lookup"><span data-stu-id="8de8c-121">Note that the **\[optimize\]** attribute can be used as an interface attribute or as an operation attribute.</span></span> <span data-ttu-id="8de8c-122">S’il est utilisé comme attribut d’interface, il définit la valeur par défaut pour l’interface entière, en remplaçant les commutateurs de ligne de commande.</span><span class="sxs-lookup"><span data-stu-id="8de8c-122">If it is used as an interface attribute, it sets the default for the entire interface, overriding command-line switches.</span></span> <span data-ttu-id="8de8c-123">Toutefois, si elle est utilisée en tant qu’attribut d’opération, elle affecte uniquement cette opération, en remplaçant les commutateurs de ligne de commande et l’interface par défaut.</span><span class="sxs-lookup"><span data-stu-id="8de8c-123">If, however, it is used as an operation attribute, it affects only that operation, overriding command-line switches and the interface default.</span></span>

## <a name="examples"></a><span data-ttu-id="8de8c-124">Exemples</span><span class="sxs-lookup"><span data-stu-id="8de8c-124">Examples</span></span>

``` syntax
optimize ("s") HRESULT FasterProcedure(...); 
optimize ("i") HRESULT SmallerProcedure(...);
```

## <a name="see-also"></a><span data-ttu-id="8de8c-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8de8c-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8de8c-126">Fichier de configuration de l’application (ACF)</span><span class="sxs-lookup"><span data-stu-id="8de8c-126">Application Configuration File (ACF)</span></span>](application-configuration-file-acf-.md)
</dt> <dt>

[<span data-ttu-id="8de8c-127">**/OI**</span><span class="sxs-lookup"><span data-stu-id="8de8c-127">**/Oi**</span></span>](-oi.md)
</dt> <dt>

[<span data-ttu-id="8de8c-128">**/OS**</span><span class="sxs-lookup"><span data-stu-id="8de8c-128">**/Os**</span></span>](-os.md)
</dt> <dt>

[<span data-ttu-id="8de8c-129">**/Robust**</span><span class="sxs-lookup"><span data-stu-id="8de8c-129">**/robust**</span></span>](-robust.md)
</dt> </dl>

 

 




