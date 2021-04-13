---
title: attribut error_status_t
description: Le \_ mot clé Error Status \_ t désigne un type pour un objet qui contient des informations relatives à l’état de la communication ou de l’erreur.
ms.assetid: 7eff0d20-c058-4f16-a3db-0b4c82303135
keywords:
- error_status_t MIDL de l’attribut
topic_type:
- apiref
api_name:
- error_status_t
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c0d017b4eaf460b5d5b7ecb8a0bd79201ac8bdee
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/25/2019
ms.locfileid: "104312217"
---
# <a name="error_status_t-attribute"></a><span data-ttu-id="dd720-104">attribut d’état d’erreur \_ \_ t</span><span class="sxs-lookup"><span data-stu-id="dd720-104">error\_status\_t attribute</span></span>

<span data-ttu-id="dd720-105">Le mot clé **Error \_ Status \_ t** désigne un type pour un objet qui contient des informations relatives à l’état de la communication ou de l’erreur.</span><span class="sxs-lookup"><span data-stu-id="dd720-105">The **error\_status\_t** keyword designates a type for an object that contains communication-status or fault-status information.</span></span>

``` syntax
[ [ , ACF-function-attributes ] ] error_status_t function-name(
        [ [ ACF-parameter-attributes ] ] parameter-name
        , ...);

[ [ ACF-function-attributes ] ] function-name(
    [ [ ACF-parameter-attributes ] ] error_status_t parameter-name
    , ...);
```

## <a name="parameters"></a><span data-ttu-id="dd720-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="dd720-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dd720-107">*ACF-Function-Attributes*</span><span class="sxs-lookup"><span data-stu-id="dd720-107">*ACF-function-attributes*</span></span> 
</dt> <dd>

<span data-ttu-id="dd720-108">Spécifie zéro, un ou plusieurs attributs de fonction ACF, tels que l' **\[** [**\_ État comm**](comm-status.md) **\]** , l' **\[** [**\_ État d’erreur**](fault-status.md) **\]** ou **\[** [**nocode**](nocode.md) **\]** .</span><span class="sxs-lookup"><span data-stu-id="dd720-108">Specifies zero or more ACF function attributes, such as **\[**[**comm\_status**](comm-status.md)**\]**, **\[**[**fault\_status**](fault-status.md)**\]**, or **\[**[**nocode**](nocode.md)**\]**.</span></span> <span data-ttu-id="dd720-109">Les attributs de fonction sont placés entre crochets.</span><span class="sxs-lookup"><span data-stu-id="dd720-109">Function attributes are enclosed in square brackets.</span></span> <span data-ttu-id="dd720-110">Zéro, un ou plusieurs attributs peuvent être appliqués à une fonction.</span><span class="sxs-lookup"><span data-stu-id="dd720-110">Zero or more attributes can be applied to a function.</span></span> <span data-ttu-id="dd720-111">Séparez plusieurs attributs de fonction par des virgules.</span><span class="sxs-lookup"><span data-stu-id="dd720-111">Separate multiple function attributes with commas.</span></span>

</dd> <dt>

<span data-ttu-id="dd720-112">*nom de fonction*</span><span class="sxs-lookup"><span data-stu-id="dd720-112">*function-name*</span></span> 
</dt> <dd>

<span data-ttu-id="dd720-113">Spécifie le nom de la fonction tel qu’il est défini dans le fichier IDL.</span><span class="sxs-lookup"><span data-stu-id="dd720-113">Specifies the name of the function as defined in the IDL file.</span></span>

</dd> <dt>

<span data-ttu-id="dd720-114">*ACF-Parameter-Attributes*</span><span class="sxs-lookup"><span data-stu-id="dd720-114">*ACF-parameter-attributes*</span></span> 
</dt> <dd>

<span data-ttu-id="dd720-115">Spécifie les attributs qui s’appliquent à un paramètre.</span><span class="sxs-lookup"><span data-stu-id="dd720-115">Specifies attributes that apply to a parameter.</span></span> <span data-ttu-id="dd720-116">Notez que zéro, un ou plusieurs attributs peuvent être appliqués au paramètre.</span><span class="sxs-lookup"><span data-stu-id="dd720-116">Note that zero, one, or more attributes can be applied to the parameter.</span></span> <span data-ttu-id="dd720-117">Séparez les attributs de plusieurs paramètres par des virgules.</span><span class="sxs-lookup"><span data-stu-id="dd720-117">Separate multiple parameter attributes with commas.</span></span> <span data-ttu-id="dd720-118">Les attributs de paramètres sont placés entre crochets.</span><span class="sxs-lookup"><span data-stu-id="dd720-118">Parameter attributes are enclosed in square brackets.</span></span> <span data-ttu-id="dd720-119">Les attributs de paramètres IDL, tels que les attributs directionnels, ne sont pas autorisés dans le CCP.</span><span class="sxs-lookup"><span data-stu-id="dd720-119">IDL parameter attributes, such as directional attributes, are not allowed in the ACF.</span></span>

</dd> <dt>

<span data-ttu-id="dd720-120">*nom du paramètre*</span><span class="sxs-lookup"><span data-stu-id="dd720-120">*parameter-name*</span></span> 
</dt> <dd>

<span data-ttu-id="dd720-121">Spécifie le paramètre pour la fonction tel qu’il est défini dans le fichier IDL.</span><span class="sxs-lookup"><span data-stu-id="dd720-121">Specifies the parameter for the function as defined in the IDL file.</span></span> <span data-ttu-id="dd720-122">Chaque paramètre de la fonction doit être spécifié dans la même séquence, en utilisant le même nom que celui défini dans le fichier IDL.</span><span class="sxs-lookup"><span data-stu-id="dd720-122">Each parameter for the function must be specified in the same sequence, using the same name as defined in the IDL file.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="dd720-123">Notes</span><span class="sxs-lookup"><span data-stu-id="dd720-123">Remarks</span></span>

<span data-ttu-id="dd720-124">Le type d' **État d’erreur \_ \_ t** est utilisé dans le cadre de l’architecture de gestion des exceptions dans IDL.</span><span class="sxs-lookup"><span data-stu-id="dd720-124">The **error\_status\_t** type is used as a part of the exception handling architecture in IDL.</span></span> <span data-ttu-id="dd720-125">Ce type est mappé à un entier [**long**](long.md) [**non signé**](unsigned.md) .</span><span class="sxs-lookup"><span data-stu-id="dd720-125">This type maps to an [**unsigned**](unsigned.md) [**long**](long.md).</span></span> <span data-ttu-id="dd720-126">Les applications qui interceptent des situations d’erreur ont un **\[** [](out-idl.md) **\]** paramètre de sortie ou un type de retour d’une procédure spécifié en tant qu' **État d’erreur \_ \_ t**, et qualifient l' **État d’erreur \_ \_ t** avec les attributs état de la **\[** [**communication \_**](comm-status.md) **\]** ou **\[** [**\_ État**](fault-status.md) **\]** de l’erreur dans le CCP.</span><span class="sxs-lookup"><span data-stu-id="dd720-126">Applications that catch error situations have an **\[**[**out**](out-idl.md)**\]** parameter or a return type of a procedure specified as **error\_status\_t**, and qualify the **error\_status\_t** with the **\[**[**comm\_status**](comm-status.md)**\]** or **\[**[**fault\_status**](fault-status.md)**\]** attributes in the ACF.</span></span> <span data-ttu-id="dd720-127">Si le paramètre ou le type de retour n’est pas qualifié avec les attributs d’état de **\[ communication \_ \]** ou d' **\[ \_ état \] d’erreur** , le paramètre fonctionne comme s’il s’agissait d’un entier long non signé.</span><span class="sxs-lookup"><span data-stu-id="dd720-127">If the parameter or return type was not qualified with the **\[comm\_status\]** or **\[fault\_status\]** attributes, then the parameter operates as though it were an unsigned long.</span></span>

<span data-ttu-id="dd720-128">À partir de la version 2,0, le compilateur MIDL génère des stubs qui contiennent l’architecture de gestion des erreurs appropriée.</span><span class="sxs-lookup"><span data-stu-id="dd720-128">Beginning with version 2.0, the MIDL compiler generates stubs that contain the proper error handling architecture.</span></span> <span data-ttu-id="dd720-129">Toutefois, les versions antérieures du compilateur MIDL géraient un paramètre ou un type de retour de l' **État d’erreur \_ \_ t** comme si les **\[** attributs [**\_ État comm**](comm-status.md) **\]** et **\[** [**\_ État**](fault-status.md) d’erreur **\]** étaient appliqués, même si ce n’est pas le cas.</span><span class="sxs-lookup"><span data-stu-id="dd720-129">However, earlier versions of the MIDL compiler handled a parameter or return type of **error\_status\_t** as though the **\[**[**comm\_status**](comm-status.md)**\]** and **\[**[**fault\_status**](fault-status.md)**\]** attributes were applied, even if they were not.</span></span> <span data-ttu-id="dd720-130">Avec MIDL 2,0 ou version ultérieure, vous devez appliquer explicitement les attributs **\[ \_ état \] comm** et **\[ \_ état \] d’erreur** au paramètre ou à la procédure dans le CCP.</span><span class="sxs-lookup"><span data-stu-id="dd720-130">With MIDL 2.0 or later, you must explicitly apply the **\[comm\_status\]** and **\[fault\_status\]** attributes to the parameter or procedure in the ACF.</span></span>

<span data-ttu-id="dd720-131">Le type d' **État d’erreur \_ \_ t** est l’un des types prédéfinis du langage de définition d’interface.</span><span class="sxs-lookup"><span data-stu-id="dd720-131">The **error\_status\_t** type is one of the predefined types of the interface definition language.</span></span> <span data-ttu-id="dd720-132">Les types prédéfinis peuvent apparaître en tant que spécificateurs de type dans les déclarations [**typedef**](typedef.md) , en déclarations générales et dans les déclarateurs de fonction (comme les spécificateurs de type fonction-retour ou en tant que spécificateurs de type paramètre).</span><span class="sxs-lookup"><span data-stu-id="dd720-132">Predefined types can appear as type specifiers in [**typedef**](typedef.md) declarations, in general declarations, and in function declarators (either as the function-return-type or as parameter-type specifiers).</span></span>

## <a name="see-also"></a><span data-ttu-id="dd720-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="dd720-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dd720-134">**État comm. \_**</span><span class="sxs-lookup"><span data-stu-id="dd720-134">**comm\_status**</span></span>](comm-status.md)
</dt> <dt>

[<span data-ttu-id="dd720-135">**État de l’erreur \_**</span><span class="sxs-lookup"><span data-stu-id="dd720-135">**fault\_status**</span></span>](fault-status.md)
</dt> <dt>

[<span data-ttu-id="dd720-136">Fichier de définition d’interface (IDL)</span><span class="sxs-lookup"><span data-stu-id="dd720-136">Interface Definition (IDL) File</span></span>](interface-definition-idl-file.md)
</dt> <dt>

[<span data-ttu-id="dd720-137">**long**</span><span class="sxs-lookup"><span data-stu-id="dd720-137">**long**</span></span>](long.md)
</dt> <dt>

[<span data-ttu-id="dd720-138">**à**</span><span class="sxs-lookup"><span data-stu-id="dd720-138">**out**</span></span>](out-idl.md)
</dt> <dt>

[<span data-ttu-id="dd720-139">**typedef**</span><span class="sxs-lookup"><span data-stu-id="dd720-139">**typedef**</span></span>](typedef.md)
</dt> <dt>

[<span data-ttu-id="dd720-140">**non signé**</span><span class="sxs-lookup"><span data-stu-id="dd720-140">**unsigned**</span></span>](unsigned.md)
</dt> </dl>

 

 




