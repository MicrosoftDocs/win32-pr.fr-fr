---
title: attribut peut-être
description: Le mot clé \ Maybe \ indique que l’appel de procédure distante n’a pas besoin d’être exécuté à chaque fois qu’il est appelé et que le client n’attend pas de réponse. Notez que le protocole \ Maybe \ n’assure ni la remise, ni l’achèvement de l’appel.
ms.assetid: 163b9fd5-7dce-493e-95bc-63807f42a498
keywords:
- MIDL d’attribut peut-être
topic_type:
- apiref
api_name:
- maybe
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 68704e19d421150444933d74f6b78fc5bada46f6
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/25/2019
ms.locfileid: "104030066"
---
# <a name="maybe-attribute"></a><span data-ttu-id="48e74-105">attribut peut-être</span><span class="sxs-lookup"><span data-stu-id="48e74-105">maybe attribute</span></span>

<span data-ttu-id="48e74-106">Le mot clé **\[ peut \]** indiquer que l’appel de procédure distante n’a pas besoin d’être exécuté à chaque fois qu’il est appelé et que le client n’attend pas de réponse.</span><span class="sxs-lookup"><span data-stu-id="48e74-106">The keyword **\[maybe\]** indicates that the remote procedure call does not need to execute every time it is called and the client does not expect a response.</span></span> <span data-ttu-id="48e74-107">Notez que le protocole **\[ peut \]** ne pas s’assurer de la remise ni de la fin de l’appel.</span><span class="sxs-lookup"><span data-stu-id="48e74-107">Note that the **\[maybe\]** protocol ensures neither delivery nor completion of the call.</span></span>

``` syntax
[
    interface-attribute-list
] 
interface interface-name 
{
    [maybe [, attribute-list]] returntype function-name(params)
}
```

## <a name="parameters"></a><span data-ttu-id="48e74-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="48e74-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="48e74-109">*interface-attribut-List*</span><span class="sxs-lookup"><span data-stu-id="48e74-109">*interface-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="48e74-110">Spécifie une liste de zéro ou plusieurs attributs IDL qui s’appliquent à l’ensemble de l’interface.</span><span class="sxs-lookup"><span data-stu-id="48e74-110">Specifies a list of zero or more IDL attributes that apply to the interface as a whole.</span></span> <span data-ttu-id="48e74-111">Lorsque deux attributs d’interface ou plus sont présents, ils doivent être séparés par des virgules.</span><span class="sxs-lookup"><span data-stu-id="48e74-111">When two or more interface attributes are present, they must be separated by commas.</span></span>

</dd> <dt>

<span data-ttu-id="48e74-112">*nom de l’interface*</span><span class="sxs-lookup"><span data-stu-id="48e74-112">*interface-name*</span></span> 
</dt> <dd>

<span data-ttu-id="48e74-113">Spécifie le nom de l’interface.</span><span class="sxs-lookup"><span data-stu-id="48e74-113">Specifies the name of the interface.</span></span>

</dd> <dt>

<span data-ttu-id="48e74-114">*liste d’attributs*</span><span class="sxs-lookup"><span data-stu-id="48e74-114">*attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="48e74-115">Spécifie des attributs supplémentaires à appliquer à la fonction.</span><span class="sxs-lookup"><span data-stu-id="48e74-115">Specifies additional attributes to be applied to the function.</span></span> <span data-ttu-id="48e74-116">Séparez plusieurs attributs par des virgules.</span><span class="sxs-lookup"><span data-stu-id="48e74-116">Separate multiple attributes with commas.</span></span>

</dd> <dt>

<span data-ttu-id="48e74-117">*ReturnType*</span><span class="sxs-lookup"><span data-stu-id="48e74-117">*returntype*</span></span> 
</dt> <dd>

<span data-ttu-id="48e74-118">Spécifie le type de retour de la fonction.</span><span class="sxs-lookup"><span data-stu-id="48e74-118">Specifies the return type of the function.</span></span>

</dd> <dt>

<span data-ttu-id="48e74-119">*nom de fonction*</span><span class="sxs-lookup"><span data-stu-id="48e74-119">*function-name*</span></span> 
</dt> <dd>

<span data-ttu-id="48e74-120">Spécifie le nom de la fonction à laquelle l’attribut **\[ peut \]** s’appliquer.</span><span class="sxs-lookup"><span data-stu-id="48e74-120">Specifies the name of the function to which the **\[maybe\]** attribute will be applied.</span></span>

</dd> <dt>

<span data-ttu-id="48e74-121">*params*</span><span class="sxs-lookup"><span data-stu-id="48e74-121">*params*</span></span> 
</dt> <dd>

<span data-ttu-id="48e74-122">Liste des paramètres de la fonction.</span><span class="sxs-lookup"><span data-stu-id="48e74-122">Function parameter list.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="48e74-123">Notes</span><span class="sxs-lookup"><span data-stu-id="48e74-123">Remarks</span></span>

<span data-ttu-id="48e74-124">Un appel avec l' **\[ \] attribut peut ne** pas contenir de paramètres de sortie et est implicitement un **\[** [](idempotent.md) **\]** appel idempotent.</span><span class="sxs-lookup"><span data-stu-id="48e74-124">A call with the **\[maybe\]** attribute cannot contain output parameters and is implicitly an **\[**[**idempotent**](idempotent.md)**\]** call.</span></span>

## <a name="see-also"></a><span data-ttu-id="48e74-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="48e74-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="48e74-126">**diffusion**</span><span class="sxs-lookup"><span data-stu-id="48e74-126">**broadcast**</span></span>](broadcast.md)
</dt> <dt>

[<span data-ttu-id="48e74-127">**idempotent**</span><span class="sxs-lookup"><span data-stu-id="48e74-127">**idempotent**</span></span>](idempotent.md)
</dt> <dt>

[<span data-ttu-id="48e74-128">Fichier de définition d’interface (IDL)</span><span class="sxs-lookup"><span data-stu-id="48e74-128">Interface Definition (IDL) File</span></span>](interface-definition-idl-file.md)
</dt> </dl>

 

 




