---
title: attribut de plage
description: L’attribut \ Range \ vous permet de spécifier une plage de valeurs autorisées pour les arguments ou les champs dont les valeurs sont définies au moment de l’exécution. Lorsqu’il est utilisé avec un type de canal, l’attribut spécifie la plage autorisée pour le nombre d’éléments dans les segments de canal.
ms.assetid: 1609fea5-e82c-4389-b4f4-2cd8d0622cde
keywords:
- attribut de plage MIDL
topic_type:
- apiref
api_name:
- range
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e095d420afc433c1f01a63dff51868e57efc50f4
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "106512723"
---
# <a name="range-attribute"></a><span data-ttu-id="e53c3-105">attribut de plage</span><span class="sxs-lookup"><span data-stu-id="e53c3-105">range attribute</span></span>

<span data-ttu-id="e53c3-106">L’attribut **\[ Range \]** vous permet de spécifier une plage de valeurs autorisées pour les arguments ou les champs dont les valeurs sont définies au moment de l’exécution.</span><span class="sxs-lookup"><span data-stu-id="e53c3-106">The **\[range\]** attribute lets you specify a range of allowable values for arguments or fields whose values are set at run time.</span></span> <span data-ttu-id="e53c3-107">Lorsqu’il est utilisé avec un type de canal, l’attribut spécifie la plage autorisée pour le nombre d’éléments dans les segments de canal.</span><span class="sxs-lookup"><span data-stu-id="e53c3-107">When used with a pipe type, the attribute specifies the allowable range for the count of elements in the pipe chunks.</span></span>

``` syntax
[range(low-val,high-val)] type-specifier declarator
```

## <a name="parameters"></a><span data-ttu-id="e53c3-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e53c3-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e53c3-109">*faible Val*</span><span class="sxs-lookup"><span data-stu-id="e53c3-109">*low-val*</span></span> 
</dt> <dd>

<span data-ttu-id="e53c3-110">Valeur autorisée la plus basse que le paramètre ou le champ peut contenir.</span><span class="sxs-lookup"><span data-stu-id="e53c3-110">The lowest allowable value that the parameter or field can hold.</span></span>

</dd> <dt>

<span data-ttu-id="e53c3-111">*haute-Val*</span><span class="sxs-lookup"><span data-stu-id="e53c3-111">*high-val*</span></span> 
</dt> <dd>

<span data-ttu-id="e53c3-112">Valeur autorisée la plus élevée que le paramètre ou le champ peut contenir.</span><span class="sxs-lookup"><span data-stu-id="e53c3-112">The highest allowable value that the parameter or field can hold.</span></span>

</dd> <dt>

<span data-ttu-id="e53c3-113">*spécificateur de type*</span><span class="sxs-lookup"><span data-stu-id="e53c3-113">*type-specifier*</span></span> 
</dt> <dd>

<span data-ttu-id="e53c3-114">Type intégral autre que [**hyper**](hyper.md) ou [**\_ \_ Int64**](--int64.md), un identificateur de type à un type intégral, un type [**enum**](enum.md) ou un nom de type de canal.</span><span class="sxs-lookup"><span data-stu-id="e53c3-114">An integral type other than [**hyper**](hyper.md) or [**\_\_int64**](--int64.md), a type identifier to an integral type, an [**enum**](enum.md) type, or a pipe type name.</span></span>

</dd> <dt>

<span data-ttu-id="e53c3-115">*declarator*</span><span class="sxs-lookup"><span data-stu-id="e53c3-115">*declarator*</span></span> 
</dt> <dd>

<span data-ttu-id="e53c3-116">Déclarateur C standard, tel qu’un identificateur.</span><span class="sxs-lookup"><span data-stu-id="e53c3-116">A standard C declarator, such as an identifier.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e53c3-117">Notes</span><span class="sxs-lookup"><span data-stu-id="e53c3-117">Remarks</span></span>

<span data-ttu-id="e53c3-118">Utilisez l’attribut **\[ Range \]** pour modifier la signification des paramètres ou des champs sensibles, tels que ceux utilisés pour la taille ou la longueur, avec des tableaux conformes ou variables, ou chaque fois que vous souhaitez vérifier un paramètre ou une valeur de champ par rapport à une plage de valeurs valides.</span><span class="sxs-lookup"><span data-stu-id="e53c3-118">Use the **\[range\]** attribute to modify the meaning of sensitive parameters or fields, such as those used for size or length, with conformant or varying arrays; or whenever you want to check a parameter or field value against a range of valid values.</span></span> <span data-ttu-id="e53c3-119">L’attribut s’applique aux paramètres de niveau supérieur, ainsi qu’aux paramètres et champs de niveau inférieur.</span><span class="sxs-lookup"><span data-stu-id="e53c3-119">The attribute is applicable to top-level parameters as well as lower-level parameters and fields.</span></span> <span data-ttu-id="e53c3-120">L’ajout de l’attribut de **\[ plage \]** à un type ne change pas son format de câble, donc n’affecte pas la compatibilité descendante.</span><span class="sxs-lookup"><span data-stu-id="e53c3-120">Adding the **\[range\]** attribute to a type does not change its wire format, thus does not affect backward compatibility.</span></span>

<span data-ttu-id="e53c3-121">L’attribut **\[ Range \]** peut également être utilisé sur des données conformes, telles que des mémoires tampons ou des tableaux, avec un attribut de conformité.</span><span class="sxs-lookup"><span data-stu-id="e53c3-121">The **\[range\]** attribute can also be used on conformant data such as buffers or arrays with a conformance attribute.</span></span> <span data-ttu-id="e53c3-122">L’effet est de limiter toutes les tailles de conformité pour les données conformes à la plage spécifiée.</span><span class="sxs-lookup"><span data-stu-id="e53c3-122">The effect is to limit all conformance sizes for the conformant data to the specified range.</span></span> <span data-ttu-id="e53c3-123">Si les données conformes sont un tableau multidimensionnel, chaque dimension de tableau est limitée à la plage spécifiée.</span><span class="sxs-lookup"><span data-stu-id="e53c3-123">If the conformant data is a multi-dimensional array, each array dimension is limited to the specified range.</span></span>

<span data-ttu-id="e53c3-124">L’utilisation de **\[ Range \]** sur des données conformes nécessite que la cible de compilation soit â «Target nt60 ou version ultérieure.</span><span class="sxs-lookup"><span data-stu-id="e53c3-124">Use of **\[range\]** on conformant data requires that the compilation target be â€“target NT60 or higher.</span></span>

<span data-ttu-id="e53c3-125">Notez que vous devez utiliser l’option du compilateur [**/Robust**](-robust.md) quand vous compilez votre fichier IDL afin de générer le code stub qui effectuera ces vérifications.</span><span class="sxs-lookup"><span data-stu-id="e53c3-125">Note that you must use the [**/robust**](-robust.md) compiler option when you compile your IDL file in order to generate the stub code that will perform these checks.</span></span> <span data-ttu-id="e53c3-126">Sans le commutateur **/Robust** , le compilateur MIDL ignore cet attribut.</span><span class="sxs-lookup"><span data-stu-id="e53c3-126">Without the **/robust** switch, the MIDL compiler ignores this attribute.</span></span>

## <a name="examples"></a><span data-ttu-id="e53c3-127">Exemples</span><span class="sxs-lookup"><span data-stu-id="e53c3-127">Examples</span></span>

``` syntax
HRESULT Method1(
    [in, range(0,100)] ULONG m,
    [in, range(0,100)] ULONG n,
    [size_is(m,n)] ULONG **pplong);

void InPipe(
    [in, range(0, MAX_CHUNK) LONG_PIPE pipe_date);
```

## <a name="see-also"></a><span data-ttu-id="e53c3-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e53c3-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e53c3-129">Fichier de définition d’interface (IDL)</span><span class="sxs-lookup"><span data-stu-id="e53c3-129">Interface Definition (IDL) File</span></span>](interface-definition-idl-file.md)
</dt> <dt>

[<span data-ttu-id="e53c3-130">Tableaux</span><span class="sxs-lookup"><span data-stu-id="e53c3-130">arrays</span></span>](/windows/desktop/Rpc/arrays)
</dt> <dt>

[<span data-ttu-id="e53c3-131">**tout d’abord, \_**</span><span class="sxs-lookup"><span data-stu-id="e53c3-131">**first\_is**</span></span>](first-is.md)
</dt> <dt>

[<span data-ttu-id="e53c3-132">**la dernière \_ est**</span><span class="sxs-lookup"><span data-stu-id="e53c3-132">**last\_is**</span></span>](last-is.md)
</dt> <dt>

[<span data-ttu-id="e53c3-133">**la longueur \_ est**</span><span class="sxs-lookup"><span data-stu-id="e53c3-133">**length\_is**</span></span>](length-is.md)
</dt> <dt>

[<span data-ttu-id="e53c3-134">**le nombre maximal \_ est**</span><span class="sxs-lookup"><span data-stu-id="e53c3-134">**max\_is**</span></span>](max-is.md)
</dt> <dt>

[<span data-ttu-id="e53c3-135">**/Robust**</span><span class="sxs-lookup"><span data-stu-id="e53c3-135">**/robust**</span></span>](-robust.md)
</dt> <dt>

[<span data-ttu-id="e53c3-136">**la taille \_ est**</span><span class="sxs-lookup"><span data-stu-id="e53c3-136">**size\_is**</span></span>](size-is.md)
</dt> <dt>

[<span data-ttu-id="e53c3-137">**le commutateur \_ est**</span><span class="sxs-lookup"><span data-stu-id="e53c3-137">**switch\_is**</span></span>](switch-is.md)
</dt> </dl>

 

 