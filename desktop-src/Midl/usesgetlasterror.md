---
title: usesgetlasterror (attribut)
description: L’attribut \ usesgetlasterror \ signale à l’appelant qu’il peut appeler GetLastError pour récupérer le code d’erreur.
ms.assetid: 8e9ab8b5-f446-4aab-bb40-b6f78799e18e
keywords:
- MIDL de l’attribut usesgetlasterror
topic_type:
- apiref
api_name:
- usesgetlasterror
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d0f403430f70fde71696ec2a35a34161f08bada9
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "103725140"
---
# <a name="usesgetlasterror-attribute"></a><span data-ttu-id="13101-104">usesgetlasterror (attribut)</span><span class="sxs-lookup"><span data-stu-id="13101-104">usesgetlasterror attribute</span></span>

<span data-ttu-id="13101-105">L’attribut **\[ \] usesgetlasterror** signale à l’appelant qu’il peut appeler [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) pour récupérer le code d’erreur.</span><span class="sxs-lookup"><span data-stu-id="13101-105">The **\[usesgetlasterror\]** attribute signals the caller that it can call [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) to retrieve the error code.</span></span>

``` syntax
[
    module-attributes
]
module module-name
{
    [entry(entry-id), usesgetlasterror [, other-attributes]] return-type function-name(param-list);
};
```

## <a name="parameters"></a><span data-ttu-id="13101-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="13101-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="13101-107">*module-attributs*</span><span class="sxs-lookup"><span data-stu-id="13101-107">*module-attributes*</span></span> 
</dt> <dd>

<span data-ttu-id="13101-108">Zéro, un ou plusieurs attributs MIDL qui seront appliqués au [**module**](module.md).</span><span class="sxs-lookup"><span data-stu-id="13101-108">Zero or more MIDL attributes that will be applied to the [**module**](module.md).</span></span>

</dd> <dt>

<span data-ttu-id="13101-109">*nom du module*</span><span class="sxs-lookup"><span data-stu-id="13101-109">*module-name*</span></span> 
</dt> <dd>

<span data-ttu-id="13101-110">Nom de l’identificateur du [**module**](module.md).</span><span class="sxs-lookup"><span data-stu-id="13101-110">The identifier name of the [**module**](module.md).</span></span>

</dd> <dt>

<span data-ttu-id="13101-111">*ID d’entrée*</span><span class="sxs-lookup"><span data-stu-id="13101-111">*entry-id*</span></span> 
</dt> <dd>

<span data-ttu-id="13101-112">Spécifie le point d’entrée de module (nom de fonction ou numéro d’identification d’entier).</span><span class="sxs-lookup"><span data-stu-id="13101-112">Specifies the module entry point–function name or integer-identification number.</span></span>

</dd> <dt>

<span data-ttu-id="13101-113">*autres attributs*</span><span class="sxs-lookup"><span data-stu-id="13101-113">*other-attributes*</span></span> 
</dt> <dd>

<span data-ttu-id="13101-114">Zéro, un ou plusieurs attributs MIDL qui seront appliqués à la procédure distante.</span><span class="sxs-lookup"><span data-stu-id="13101-114">Zero or more MIDL attributes that will be applied to the remote procedure.</span></span>

</dd> <dt>

<span data-ttu-id="13101-115">*type de retour*</span><span class="sxs-lookup"><span data-stu-id="13101-115">*return-type*</span></span> 
</dt> <dd>

<span data-ttu-id="13101-116">Type des données retournées par la procédure distante à la fin de l’opération.</span><span class="sxs-lookup"><span data-stu-id="13101-116">The type of the data that the remote procedure will return upon completion.</span></span>

</dd> <dt>

<span data-ttu-id="13101-117">*nom de fonction*</span><span class="sxs-lookup"><span data-stu-id="13101-117">*function-name*</span></span> 
</dt> <dd>

<span data-ttu-id="13101-118">Nom de la procédure distante tel que défini dans le fichier IDL.</span><span class="sxs-lookup"><span data-stu-id="13101-118">The name of the remote procedure as defined in the IDL file.</span></span>

</dd> <dt>

<span data-ttu-id="13101-119">*Param-liste*</span><span class="sxs-lookup"><span data-stu-id="13101-119">*param-list*</span></span> 
</dt> <dd>

<span data-ttu-id="13101-120">Zéro, un ou plusieurs paramètres à la procédure distante.</span><span class="sxs-lookup"><span data-stu-id="13101-120">Zero or more parameters to the remote procedure.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="13101-121">Notes</span><span class="sxs-lookup"><span data-stu-id="13101-121">Remarks</span></span>

<span data-ttu-id="13101-122">L’attribut **\[ \] usesgetlasterror** peut être défini sur un point d’entrée de module, si ce point d’entrée utilise la fonction Windows [**SetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-setlasterror) pour retourner des codes d’erreur.</span><span class="sxs-lookup"><span data-stu-id="13101-122">The **\[usesgetlasterror\]** attribute can be set on a module entry point, if that entry point uses the Windows function [**SetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-setlasterror) to return error codes.</span></span> <span data-ttu-id="13101-123">L’attribut indique à l’appelant que, en cas d’erreur lors de l’appel de cette fonction, l’appelant peut ensuite appeler [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) pour récupérer le code d’erreur.</span><span class="sxs-lookup"><span data-stu-id="13101-123">The attribute tells the caller that, if there is an error when calling that function, the caller can then call [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) to retrieve the error code.</span></span>

## <a name="examples"></a><span data-ttu-id="13101-124">Exemples</span><span class="sxs-lookup"><span data-stu-id="13101-124">Examples</span></span>

``` syntax
[
    dllname("MyOwn.dll")
] 
module MyModule
{
    [entry("One"), usesgetlasterror, bindable, requestedit,
     propputref, defaultbind] HRESULT Func1(
         [in]IUnknown * iParam1, 
         [out] long * Param2) ;
    [entry("TwentyOne"), usesgetlasterror, 
     hidden, vararg] SAFEARRAY (int) Func2(
         [in, out] SAFEARRAY (variant) *varP) ;

    // Other module definition statements.
};
```

## <a name="see-also"></a><span data-ttu-id="13101-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="13101-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="13101-126">Génération d’une bibliothèque de types avec MIDL</span><span class="sxs-lookup"><span data-stu-id="13101-126">Generating a Type Library With MIDL</span></span>](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[<span data-ttu-id="13101-127">Exemple de fichier ODL</span><span class="sxs-lookup"><span data-stu-id="13101-127">ODL File Example</span></span>](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[<span data-ttu-id="13101-128">Syntaxe du fichier ODL</span><span class="sxs-lookup"><span data-stu-id="13101-128">ODL File Syntax</span></span>](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> </dl>

 

 