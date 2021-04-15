---
title: idempotent (attribut)
description: L’attribut \ idempotent \ spécifie qu’une opération ne modifie pas les informations d’État et retourne les mêmes résultats chaque fois qu’elle est exécutée. L’exécution de la routine plusieurs fois a le même effet que l’exécution d’une seule fois.
ms.assetid: 876a40b5-8165-4b5c-bd62-9c43a9eb4b2b
keywords:
- attribut idempotent MIDL
topic_type:
- apiref
api_name:
- idempotent
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 82364c6222f6b566ef6aacb5b71a72b49c213f5a
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/25/2019
ms.locfileid: "104507535"
---
# <a name="idempotent-attribute"></a><span data-ttu-id="46140-105">idempotent (attribut)</span><span class="sxs-lookup"><span data-stu-id="46140-105">idempotent attribute</span></span>

<span data-ttu-id="46140-106">L’attribut **\[ idempotent \]** spécifie qu’une opération ne modifie pas les informations d’État et retourne les mêmes résultats chaque fois qu’elle est exécutée.</span><span class="sxs-lookup"><span data-stu-id="46140-106">The **\[idempotent\]** attribute specifies that an operation does not modify state information and returns the same results each time it is performed.</span></span> <span data-ttu-id="46140-107">L’exécution de la routine plusieurs fois a le même effet que l’exécution d’une seule fois.</span><span class="sxs-lookup"><span data-stu-id="46140-107">Performing the routine more than once has the same effect as performing it once.</span></span>

``` syntax
[
    interface-attribute-list
] 
interface interface-name 
{
    [idempotent [, attribute-list]] returntype function-name(params)
}
```

## <a name="parameters"></a><span data-ttu-id="46140-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="46140-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="46140-109">*interface-attribut-List*</span><span class="sxs-lookup"><span data-stu-id="46140-109">*interface-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="46140-110">Spécifie une liste de zéro ou plusieurs attributs IDL qui s’appliquent à l’ensemble de l’interface.</span><span class="sxs-lookup"><span data-stu-id="46140-110">Specifies a list of zero or more IDL attributes that apply to the interface as a whole.</span></span> <span data-ttu-id="46140-111">Lorsque deux attributs d’interface ou plus sont présents, ils doivent être séparés par des virgules.</span><span class="sxs-lookup"><span data-stu-id="46140-111">When two or more interface attributes are present, they must be separated by commas.</span></span>

</dd> <dt>

<span data-ttu-id="46140-112">*nom de l’interface*</span><span class="sxs-lookup"><span data-stu-id="46140-112">*interface-name*</span></span> 
</dt> <dd>

<span data-ttu-id="46140-113">Spécifie le nom de l’interface.</span><span class="sxs-lookup"><span data-stu-id="46140-113">Specifies the name of the interface.</span></span>

</dd> <dt>

<span data-ttu-id="46140-114">*liste d’attributs*</span><span class="sxs-lookup"><span data-stu-id="46140-114">*attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="46140-115">Spécifie des attributs supplémentaires à appliquer à la fonction.</span><span class="sxs-lookup"><span data-stu-id="46140-115">Specifies additional attributes to be applied to the function.</span></span> <span data-ttu-id="46140-116">Séparez plusieurs attributs par des virgules.</span><span class="sxs-lookup"><span data-stu-id="46140-116">Separate multiple attributes with commas.</span></span>

</dd> <dt>

<span data-ttu-id="46140-117">*ReturnType*</span><span class="sxs-lookup"><span data-stu-id="46140-117">*returntype*</span></span> 
</dt> <dd>

<span data-ttu-id="46140-118">Spécifie le type de retour de la fonction.</span><span class="sxs-lookup"><span data-stu-id="46140-118">Specifies the return type of the function.</span></span>

</dd> <dt>

<span data-ttu-id="46140-119">*nom de fonction*</span><span class="sxs-lookup"><span data-stu-id="46140-119">*function-name*</span></span> 
</dt> <dd>

<span data-ttu-id="46140-120">Spécifie le nom de la fonction à laquelle l’attribut **\[ idempotent \]** sera appliqué.</span><span class="sxs-lookup"><span data-stu-id="46140-120">Specifies the name of the function to which the **\[idempotent\]** attribute will be applied.</span></span>

</dd> <dt>

<span data-ttu-id="46140-121">*params*</span><span class="sxs-lookup"><span data-stu-id="46140-121">*params*</span></span> 
</dt> <dd>

<span data-ttu-id="46140-122">Liste des paramètres de la fonction.</span><span class="sxs-lookup"><span data-stu-id="46140-122">Function parameter list.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="46140-123">Notes</span><span class="sxs-lookup"><span data-stu-id="46140-123">Remarks</span></span>

<span data-ttu-id="46140-124">RPC prend en charge deux types de sémantiques d’appel à distance : les appels aux opérations avec l’attribut **\[ idempotent \]** et les appels aux opérations (opérations *idempotent* ) sans l’attribut **\[ idempotent \]** (opérations *non-idempotent* ).</span><span class="sxs-lookup"><span data-stu-id="46140-124">RPC supports two types of remote call semantics: calls to operations with the **\[idempotent\]** attribute and calls to operations (*idempotent* operations) without the **\[idempotent\]** attribute (*non-idempotent* operations).</span></span> <span data-ttu-id="46140-125">Une opération idempotent peut être exécutée plusieurs fois sans effet.</span><span class="sxs-lookup"><span data-stu-id="46140-125">An idempotent operation can be carried out more than once with no ill effect.</span></span> <span data-ttu-id="46140-126">À l’inverse, une opération non-idempotent ne peut pas être exécutée plus d’une fois, car elle retourne des résultats différents chaque fois ou car elle modifie un État.</span><span class="sxs-lookup"><span data-stu-id="46140-126">Conversely, a non-idempotent operation cannot be executed more than once because it will either return different results each time or because it modifies some state.</span></span>

<span data-ttu-id="46140-127">Pour garantir la réexécution automatique d’une procédure si l’appel n’est pas terminé, utilisez l’attribut **\[ idempotent \]** .</span><span class="sxs-lookup"><span data-stu-id="46140-127">To ensure that a procedure is automatically re-executed if the call does not complete, use the **\[idempotent\]** attribute.</span></span> <span data-ttu-id="46140-128">Si les attributs **\[ idempotent \]**, **\[** [**Broadcast**](broadcast.md) **\]** ou **\[** [**Maybe**](maybe.md) ne **\]** sont pas présents, la procédure utilise la sémantique non idempotent par défaut.</span><span class="sxs-lookup"><span data-stu-id="46140-128">If the **\[idempotent\]**, **\[**[**broadcast**](broadcast.md)**\]**, or **\[**[**maybe**](maybe.md)**\]** attributes are not present, the procedure will use non-idempotent semantics by default.</span></span> <span data-ttu-id="46140-129">Dans ce cas, l’opération n’est exécutée qu’une seule fois.</span><span class="sxs-lookup"><span data-stu-id="46140-129">In this case, the operation is executed only once.</span></span>

## <a name="see-also"></a><span data-ttu-id="46140-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="46140-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="46140-131">**diffusion**</span><span class="sxs-lookup"><span data-stu-id="46140-131">**broadcast**</span></span>](broadcast.md)
</dt> <dt>

[<span data-ttu-id="46140-132">Fichier de définition d’interface (IDL)</span><span class="sxs-lookup"><span data-stu-id="46140-132">Interface Definition (IDL) File</span></span>](interface-definition-idl-file.md)
</dt> <dt>

[<span data-ttu-id="46140-133">**environ**</span><span class="sxs-lookup"><span data-stu-id="46140-133">**maybe**</span></span>](maybe.md)
</dt> </dl>

 

 




