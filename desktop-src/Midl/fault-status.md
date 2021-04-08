---
title: attribut fault_status
description: L’attribut \ \_ CCP Status indique qu’un code d’erreur de type Error \_ Status indique qu’il s’agit \_ d’un échec de la procédure distante, plutôt que d’autres types de problèmes tels que des erreurs de communication.
ms.assetid: 9da7bd3d-cef0-4ad4-b2a4-3f8aa156e8e0
keywords:
- fault_status MIDL de l’attribut
topic_type:
- apiref
api_name:
- fault_status
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 134d9772e167fe63e133d569b9985a7735668d3c
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/25/2019
ms.locfileid: "103678250"
---
# <a name="fault_status-attribute"></a><span data-ttu-id="5dc88-104">\_attribut état d’erreur</span><span class="sxs-lookup"><span data-stu-id="5dc88-104">fault\_status attribute</span></span>

<span data-ttu-id="5dc88-105">L’attribut ACF de l' **\[ \_ état \]** d’erreur indique qu’un code d’erreur de type [**erreur \_ \_ t**](error-status-t.md) indique un échec de la procédure distante, plutôt que d’autres types de problèmes tels que des erreurs de communication.</span><span class="sxs-lookup"><span data-stu-id="5dc88-105">The **\[fault\_status\]** ACF attribute specifies that an error code of type [**error\_status\_t**](error-status-t.md) indicates a failure of the remote procedure, rather than other types of problems such as communication errors.</span></span>

``` syntax
[fault_status [ , ACF-function-attributes ] ] function-name(
    [ [ ACF-parameter-attributes ] ] parameter-name
    , ... );

[ [ ACF-function-attributes ] ] function-name(
    [fault_status [ , ACF-parameter-attributes ] ] parameter-name
    , ... );
```

## <a name="parameters"></a><span data-ttu-id="5dc88-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="5dc88-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5dc88-107">*ACF-Function-Attributes*</span><span class="sxs-lookup"><span data-stu-id="5dc88-107">*ACF-function-attributes*</span></span> 
</dt> <dd>

<span data-ttu-id="5dc88-108">Spécifie zéro, un ou plusieurs attributs de fonction ACF tels que l' **\[ \_ état \] d’erreur** et le **\[** [**nocode**](nocode.md) **\]** .</span><span class="sxs-lookup"><span data-stu-id="5dc88-108">Specifies zero or more ACF function attributes such as **\[fault\_status\]** and **\[**[**nocode**](nocode.md)**\]**.</span></span> <span data-ttu-id="5dc88-109">Les attributs de fonction sont placés entre crochets.</span><span class="sxs-lookup"><span data-stu-id="5dc88-109">Function attributes are enclosed in square brackets.</span></span> <span data-ttu-id="5dc88-110">Notez que zéro, un ou plusieurs attributs peuvent être appliqués à une fonction.</span><span class="sxs-lookup"><span data-stu-id="5dc88-110">Note that zero or more attributes can be applied to a function.</span></span> <span data-ttu-id="5dc88-111">Séparez plusieurs attributs de fonction par des virgules.</span><span class="sxs-lookup"><span data-stu-id="5dc88-111">Separate multiple function attributes with commas.</span></span> <span data-ttu-id="5dc88-112">Notez également que si l' **\[ \_ état \] d’erreur** apparaît en tant qu’attribut de fonction, il ne peut pas apparaître en tant qu’attribut de paramètre.</span><span class="sxs-lookup"><span data-stu-id="5dc88-112">Also note that if **\[fault\_status\]** appears as a function attribute, it cannot also appear as a parameter attribute.</span></span>

</dd> <dt>

<span data-ttu-id="5dc88-113">*nom de fonction*</span><span class="sxs-lookup"><span data-stu-id="5dc88-113">*function-name*</span></span> 
</dt> <dd>

<span data-ttu-id="5dc88-114">Spécifie le nom de la fonction tel qu’il est défini dans le fichier IDL.</span><span class="sxs-lookup"><span data-stu-id="5dc88-114">Specifies the name of the function as defined in the IDL file.</span></span>

</dd> <dt>

<span data-ttu-id="5dc88-115">*ACF-Parameter-Attributes*</span><span class="sxs-lookup"><span data-stu-id="5dc88-115">*ACF-parameter-attributes*</span></span> 
</dt> <dd>

<span data-ttu-id="5dc88-116">Spécifie les attributs qui s’appliquent à un paramètre.</span><span class="sxs-lookup"><span data-stu-id="5dc88-116">Specifies attributes that apply to a parameter.</span></span> <span data-ttu-id="5dc88-117">Notez que zéro, un ou plusieurs attributs peuvent être appliqués au paramètre.</span><span class="sxs-lookup"><span data-stu-id="5dc88-117">Note that zero or more attributes can be applied to the parameter.</span></span> <span data-ttu-id="5dc88-118">Les attributs de paramètres sont placés entre crochets.</span><span class="sxs-lookup"><span data-stu-id="5dc88-118">Parameter attributes are enclosed in square brackets.</span></span> <span data-ttu-id="5dc88-119">Séparez les attributs de plusieurs paramètres par des virgules.</span><span class="sxs-lookup"><span data-stu-id="5dc88-119">Separate multiple parameter attributes with commas.</span></span> <span data-ttu-id="5dc88-120">Les attributs de paramètres IDL, tels que les attributs directionnels, ne sont pas autorisés dans le CCP.</span><span class="sxs-lookup"><span data-stu-id="5dc88-120">IDL parameter attributes, such as directional attributes, are not allowed in the ACF.</span></span> <span data-ttu-id="5dc88-121">Notez que si l' **\[ \_ état \] d’erreur** apparaît en tant qu’attribut de paramètre, il ne peut pas apparaître en tant qu’attribut de fonction.</span><span class="sxs-lookup"><span data-stu-id="5dc88-121">Note that if **\[fault\_status\]** appears as a parameter attribute, it cannot also appear as a function attribute.</span></span>

</dd> <dt>

<span data-ttu-id="5dc88-122">*nom du paramètre*</span><span class="sxs-lookup"><span data-stu-id="5dc88-122">*parameter-name*</span></span> 
</dt> <dd>

<span data-ttu-id="5dc88-123">Spécifie le paramètre pour la fonction tel qu’il est défini dans le fichier IDL.</span><span class="sxs-lookup"><span data-stu-id="5dc88-123">Specifies the parameter for the function as defined in the IDL file.</span></span> <span data-ttu-id="5dc88-124">Chaque paramètre de la fonction doit être spécifié dans la même séquence, en utilisant le même nom que celui défini dans le fichier IDL.</span><span class="sxs-lookup"><span data-stu-id="5dc88-124">Each parameter for the function must be specified in the same sequence, using the same name as defined in the IDL file.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="5dc88-125">Notes</span><span class="sxs-lookup"><span data-stu-id="5dc88-125">Remarks</span></span>

<span data-ttu-id="5dc88-126">L’attribut **\[ \_ état \] d’erreur** peut être utilisé en tant qu’attribut de fonction ou en tant qu’attribut de paramètre, mais il ne peut apparaître qu’une seule fois par fonction.</span><span class="sxs-lookup"><span data-stu-id="5dc88-126">The **\[fault\_status\]** attribute can be used as either a function attribute or as a parameter attribute, but it can appear only once per function.</span></span> <span data-ttu-id="5dc88-127">Elle peut être appliquée à la fonction elle-même ou à un paramètre dans chaque fonction.</span><span class="sxs-lookup"><span data-stu-id="5dc88-127">It can be applied either to the function itself or to one parameter in each function.</span></span>

<span data-ttu-id="5dc88-128">L’attribut **\[ \_ état \]** d’erreur peut être appliqué uniquement aux fonctions qui retournent le type d' [**État d’erreur \_ \_ t**](error-status-t.md).</span><span class="sxs-lookup"><span data-stu-id="5dc88-128">The **\[fault\_status\]** attribute can be applied only to functions that return the type [**error\_status\_t**](error-status-t.md).</span></span> <span data-ttu-id="5dc88-129">Lorsque la procédure distante échoue d’une manière qui provoque le retour d’une PDU d’erreur, un code d’erreur est renvoyé.</span><span class="sxs-lookup"><span data-stu-id="5dc88-129">When the remote procedure fails in a way that causes a fault PDU to be returned, an error code is returned.</span></span>

<span data-ttu-id="5dc88-130">Lorsque l' **\[ \_ état \]** de l’erreur est utilisé en tant qu’attribut de paramètre, le paramètre doit être un **\[** [](out-idl.md) **\]** paramètre de sortie de type [**État d’erreur \_ \_ t**](error-status-t.md).</span><span class="sxs-lookup"><span data-stu-id="5dc88-130">When **\[fault\_status\]** is used as a parameter attribute, the parameter must be an **\[**[**out**](out-idl.md)**\]** parameter of type [**error\_status\_t**](error-status-t.md).</span></span> <span data-ttu-id="5dc88-131">Si une erreur de serveur se produit, le paramètre est défini sur le code d’erreur.</span><span class="sxs-lookup"><span data-stu-id="5dc88-131">If a server error occurs, the parameter is set to the error code.</span></span> <span data-ttu-id="5dc88-132">Une fois l’appel distant terminé, la procédure définit la valeur.</span><span class="sxs-lookup"><span data-stu-id="5dc88-132">When the remote call is successfully completed, the procedure sets the value.</span></span>

<span data-ttu-id="5dc88-133">Il n’est pas nécessaire de spécifier le paramètre associé à l’attribut d' **\[ \_ état \] d’erreur** dans le fichier IDL.</span><span class="sxs-lookup"><span data-stu-id="5dc88-133">The parameter associated with the **\[fault\_status\]** attribute does not have to be specified in the IDL file.</span></span> <span data-ttu-id="5dc88-134">Lorsque le paramètre n’est pas spécifié, un nouveau paramètre [**out**](out-idl.md) de type [**Error \_ Status \_ t**](error-status-t.md) est généré à la suite du dernier paramètre défini dans le fichier IDL DCE.</span><span class="sxs-lookup"><span data-stu-id="5dc88-134">When the parameter is not specified, a new [**out**](out-idl.md) parameter of type [**error\_status\_t**](error-status-t.md) is generated following the last parameter defined in the DCE IDL file.</span></span>

<span data-ttu-id="5dc88-135">Il est possible que les attributs **\[ \_ état \]** de l’erreur et **\[** [**\_ État**](comm-status.md) de la communication **\]** apparaissent dans une seule fonction, en tant qu’attributs de fonction ou attributs de paramètre.</span><span class="sxs-lookup"><span data-stu-id="5dc88-135">It is possible for both the **\[fault\_status\]** and **\[**[**comm\_status**](comm-status.md)**\]** attributes to appear in a single function, either as function attributes or parameter attributes.</span></span> <span data-ttu-id="5dc88-136">Si les deux attributs sont des attributs de fonction, ou s’ils s’appliquent au même paramètre et qu’aucune erreur ne se produit, la fonction ou le paramètre a la valeur **« État d’erreur \_ \_ OK »**.</span><span class="sxs-lookup"><span data-stu-id="5dc88-136">If both attributes are function attributes, or if they apply to the same parameter and no error occurs, the function or parameter has the value **error\_status\_ok**.</span></span> <span data-ttu-id="5dc88-137">Dans le cas contraire, elle contient la valeur de code d’État appropriée.</span><span class="sxs-lookup"><span data-stu-id="5dc88-137">Otherwise, it contains the appropriate status code value.</span></span> <span data-ttu-id="5dc88-138">Étant donné que les valeurs retournées pour l' **\[ \_ état \] d’erreur** sont différentes de celles retournées pour l' **\[ \_ état \] comm**, les valeurs retournées sont facilement interprétées.</span><span class="sxs-lookup"><span data-stu-id="5dc88-138">Because values returned for **\[fault\_status\]** are different from the values returned for **\[comm\_status\]**, the returned values are readily interpreted.</span></span>

## <a name="see-also"></a><span data-ttu-id="5dc88-139">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5dc88-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5dc88-140">Fichier de configuration de l’application (ACF)</span><span class="sxs-lookup"><span data-stu-id="5dc88-140">Application Configuration File (ACF)</span></span>](application-configuration-file-acf-.md)
</dt> <dt>

[<span data-ttu-id="5dc88-141">**État comm. \_**</span><span class="sxs-lookup"><span data-stu-id="5dc88-141">**comm\_status**</span></span>](comm-status.md)
</dt> <dt>

[<span data-ttu-id="5dc88-142">**État d’erreur \_ \_ t**</span><span class="sxs-lookup"><span data-stu-id="5dc88-142">**error\_status\_t**</span></span>](error-status-t.md)
</dt> <dt>

[<span data-ttu-id="5dc88-143">**SansCode**</span><span class="sxs-lookup"><span data-stu-id="5dc88-143">**nocode**</span></span>](nocode.md)
</dt> <dt>

[<span data-ttu-id="5dc88-144">**à**</span><span class="sxs-lookup"><span data-stu-id="5dc88-144">**out**</span></span>](out-idl.md)
</dt> </dl>

 

 




