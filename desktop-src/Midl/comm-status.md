---
title: attribut comm_status
description: L’attribut \ comm \_ Status \ ACF provoque le renvoi d’un code d’erreur lorsqu’une erreur de communication se produit pendant l’exécution d’une fonction.
ms.assetid: 3ea9ce62-8bd4-40fe-b838-bfebd52b5a15
keywords:
- comm_status MIDL de l’attribut
topic_type:
- apiref
api_name:
- comm_status
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dd4952d03a80dbbffb135043d024b0c0eb18966f
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/25/2019
ms.locfileid: "103678718"
---
# <a name="comm_status-attribute"></a><span data-ttu-id="47592-104">\_attribut de statut comm</span><span class="sxs-lookup"><span data-stu-id="47592-104">comm\_status attribute</span></span>

<span data-ttu-id="47592-105">L’attribut CCP **\[ \_ Status \]** ACF provoque le renvoi d’un code d’erreur lorsqu’une erreur de communication se produit pendant l’exécution d’une fonction.</span><span class="sxs-lookup"><span data-stu-id="47592-105">The **\[comm\_status\]** ACF attribute causes an error code to be returned when a communication error occurs during the execution of a function.</span></span>

``` syntax
[comm_status [ , ACF-function-attributes ] ] 
    error_status_t function-name(
        [ [ ACF-parameter-attributes ] ] parameter-name
        , ...);

[ [ ACF-function-attributes ] ] function-name(
    [comm_status [ , ACF-parameter-attributes ] ] error_status_t name
    , ...);
```

## <a name="parameters"></a><span data-ttu-id="47592-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="47592-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="47592-107">*ACF-Function-Attributes*</span><span class="sxs-lookup"><span data-stu-id="47592-107">*ACF-function-attributes*</span></span> 
</dt> <dd>

<span data-ttu-id="47592-108">Spécifie zéro, un ou plusieurs attributs de fonction ACF, tels que l' **\[ \_ état \] comm** et le **\[** [**nocode**](nocode.md) **\]** .</span><span class="sxs-lookup"><span data-stu-id="47592-108">Specifies zero or more ACF function attributes, such as **\[comm\_status\]** and **\[**[**nocode**](nocode.md)**\]**.</span></span> <span data-ttu-id="47592-109">Les attributs de fonction sont placés entre crochets.</span><span class="sxs-lookup"><span data-stu-id="47592-109">Function attributes are enclosed in square brackets.</span></span> <span data-ttu-id="47592-110">Zéro, un ou plusieurs attributs peuvent être appliqués à une fonction.</span><span class="sxs-lookup"><span data-stu-id="47592-110">Zero or more attributes can be applied to a function.</span></span> <span data-ttu-id="47592-111">Séparez plusieurs attributs de fonction par des virgules.</span><span class="sxs-lookup"><span data-stu-id="47592-111">Separate multiple function attributes with commas.</span></span> <span data-ttu-id="47592-112">Notez que si l' **\[ \_ état \]** de la communication apparaît en tant qu’attribut de fonction, il ne peut pas apparaître en tant qu’attribut de paramètre.</span><span class="sxs-lookup"><span data-stu-id="47592-112">Note that if **\[comm\_status\]** appears as a function attribute, it cannot also appear as a parameter attribute.</span></span>

</dd> <dt>

<span data-ttu-id="47592-113">*nom de fonction*</span><span class="sxs-lookup"><span data-stu-id="47592-113">*function-name*</span></span> 
</dt> <dd>

<span data-ttu-id="47592-114">Spécifie le nom de la fonction tel qu’il est défini dans le fichier IDL.</span><span class="sxs-lookup"><span data-stu-id="47592-114">Specifies the name of the function as defined in the IDL file.</span></span>

</dd> <dt>

<span data-ttu-id="47592-115">*ACF-Parameter-Attributes*</span><span class="sxs-lookup"><span data-stu-id="47592-115">*ACF-parameter-attributes*</span></span> 
</dt> <dd>

<span data-ttu-id="47592-116">Spécifie les attributs qui s’appliquent à un paramètre.</span><span class="sxs-lookup"><span data-stu-id="47592-116">Specifies attributes that apply to a parameter.</span></span> <span data-ttu-id="47592-117">Notez que zéro, un ou plusieurs attributs peuvent être appliqués au paramètre.</span><span class="sxs-lookup"><span data-stu-id="47592-117">Note that zero, one, or more attributes can be applied to the parameter.</span></span> <span data-ttu-id="47592-118">Séparez les attributs de plusieurs paramètres par des virgules.</span><span class="sxs-lookup"><span data-stu-id="47592-118">Separate multiple parameter attributes with commas.</span></span> <span data-ttu-id="47592-119">Les attributs de paramètres sont placés entre crochets.</span><span class="sxs-lookup"><span data-stu-id="47592-119">Parameter attributes are enclosed in square brackets.</span></span> <span data-ttu-id="47592-120">Les attributs de paramètres IDL, tels que les attributs directionnels, ne sont pas autorisés dans le CCP.</span><span class="sxs-lookup"><span data-stu-id="47592-120">IDL parameter attributes, such as directional attributes, are not allowed in the ACF.</span></span> <span data-ttu-id="47592-121">Notez que si l' **\[ \_ état \] comm** apparaît en tant qu’attribut de paramètre, il ne peut pas apparaître en tant qu’attribut de fonction.</span><span class="sxs-lookup"><span data-stu-id="47592-121">Note that if **\[comm\_status\]** appears as a parameter attribute, it cannot also appear as a function attribute.</span></span>

</dd> <dt>

<span data-ttu-id="47592-122">*nom du paramètre*</span><span class="sxs-lookup"><span data-stu-id="47592-122">*parameter-name*</span></span> 
</dt> <dd>

<span data-ttu-id="47592-123">Spécifie le paramètre pour la fonction tel qu’il est défini dans le fichier IDL.</span><span class="sxs-lookup"><span data-stu-id="47592-123">Specifies the parameter for the function as defined in the IDL file.</span></span> <span data-ttu-id="47592-124">Chaque paramètre de la fonction doit être spécifié dans la même séquence, en utilisant le même nom que celui défini dans le fichier IDL.</span><span class="sxs-lookup"><span data-stu-id="47592-124">Each parameter for the function must be specified in the same sequence, using the same name as defined in the IDL file.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="47592-125">Notes</span><span class="sxs-lookup"><span data-stu-id="47592-125">Remarks</span></span>

<span data-ttu-id="47592-126">L’attribut **\[ \_ état \] comm** peut être utilisé en tant qu’attribut de fonction ou en tant qu’attribut de paramètre, mais il ne peut apparaître qu’une seule fois par fonction.</span><span class="sxs-lookup"><span data-stu-id="47592-126">The **\[comm\_status\]** attribute can be used as either a function attribute or as a parameter attribute, but it can appear only once per function.</span></span> <span data-ttu-id="47592-127">Elle peut être appliquée à la fonction ou à un paramètre dans chaque fonction.</span><span class="sxs-lookup"><span data-stu-id="47592-127">It can be applied either to the function or to one parameter in each function.</span></span>

<span data-ttu-id="47592-128">L’attribut d' **\[ \_ état \] de communication** peut être appliqué uniquement aux fonctions qui retournent le type d’état d' [**erreur \_ \_ t**](error-status-t.md).</span><span class="sxs-lookup"><span data-stu-id="47592-128">The **\[comm\_status\]** attribute can be applied only to functions that return the type [**error\_status\_t**](error-status-t.md).</span></span> <span data-ttu-id="47592-129">Lorsqu’une erreur de communication se produit pendant l’exécution de la fonction, un code d’erreur est retourné.</span><span class="sxs-lookup"><span data-stu-id="47592-129">When a communication error occurs during the execution of the function, an error code is returned.</span></span>

<span data-ttu-id="47592-130">Lorsque l' **\[ \_ état \] comm** est utilisé en tant qu’attribut de paramètre, le paramètre doit être défini dans le fichier IDL et doit être un **\[** [](out-idl.md) **\]** paramètre out de type [**Error \_ Status \_ t**](error-status-t.md).</span><span class="sxs-lookup"><span data-stu-id="47592-130">When **\[comm\_status\]** is used as a parameter attribute, the parameter must be defined in the IDL file and must be an **\[**[**out**](out-idl.md)**\]** parameter of type [**error\_status\_t**](error-status-t.md).</span></span> <span data-ttu-id="47592-131">Lorsqu’une erreur de communication se produit pendant l’exécution de la fonction, le paramètre est défini sur le code d’erreur.</span><span class="sxs-lookup"><span data-stu-id="47592-131">When a communication error occurs during the execution of the function, the parameter is set to the error code.</span></span> <span data-ttu-id="47592-132">Lorsque l’appel à distance est effectué avec succès, la procédure définit la valeur.</span><span class="sxs-lookup"><span data-stu-id="47592-132">When the remote call is completed successfully, the procedure sets the value.</span></span>

<span data-ttu-id="47592-133">Il est possible que les attributs **\[ \_ état \]** de la communication et **\[** [**\_ État**](fault-status.md) de l’erreur **\]** apparaissent dans une fonction unique, en tant qu’attributs de fonction ou attributs de paramètre.</span><span class="sxs-lookup"><span data-stu-id="47592-133">It is possible for both the **\[comm\_status\]** and **\[**[**fault\_status**](fault-status.md)**\]** attributes to appear in a single function, either as function attributes or parameter attributes.</span></span> <span data-ttu-id="47592-134">Si les deux attributs sont des attributs de fonction ou s’ils s’appliquent au même paramètre et qu’aucune erreur ne se produit, la fonction ou le paramètre a la valeur **État d’erreur \_ \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="47592-134">If both attributes are function attributes or if they apply to the same parameter and no error occurs, the function or parameter has the value **error\_status\_ok**.</span></span> <span data-ttu-id="47592-135">Dans le cas contraire, elle contient la valeur appropriée de l’état de la **\[ communication \_ \]** ou de l' **\[ \_ état \] d’erreur** .</span><span class="sxs-lookup"><span data-stu-id="47592-135">Otherwise, it contains the appropriate **\[comm\_status\]** or **\[fault\_status\]** value.</span></span> <span data-ttu-id="47592-136">Étant donné que les valeurs retournées pour l' **\[ \_ état \] comm** sont différentes des valeurs retournées pour l' **\[ \_ état \] Fault**, les valeurs retournées sont facilement interprétées.</span><span class="sxs-lookup"><span data-stu-id="47592-136">Because values returned for **\[comm\_status\]** are different from the values returned for **\[fault\_status\]**, the returned values are readily interpreted.</span></span>

## <a name="see-also"></a><span data-ttu-id="47592-137">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="47592-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="47592-138">Fichier de configuration de l’application (ACF)</span><span class="sxs-lookup"><span data-stu-id="47592-138">Application Configuration File (ACF)</span></span>](application-configuration-file-acf-.md)
</dt> <dt>

[<span data-ttu-id="47592-139">**État d’erreur \_ \_ t**</span><span class="sxs-lookup"><span data-stu-id="47592-139">**error\_status\_t**</span></span>](error-status-t.md)
</dt> <dt>

[<span data-ttu-id="47592-140">**État de l’erreur \_**</span><span class="sxs-lookup"><span data-stu-id="47592-140">**fault\_status**</span></span>](fault-status.md)
</dt> <dt>

[<span data-ttu-id="47592-141">**SansCode**</span><span class="sxs-lookup"><span data-stu-id="47592-141">**nocode**</span></span>](nocode.md)
</dt> <dt>

[<span data-ttu-id="47592-142">**à**</span><span class="sxs-lookup"><span data-stu-id="47592-142">**out**</span></span>](out-idl.md)
</dt> </dl>

 

 




