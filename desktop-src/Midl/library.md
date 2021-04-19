---
title: attribut de bibliothèque
description: L’instruction Library contient toutes les informations que le compilateur MIDL utilise pour générer une bibliothèque de types.
ms.assetid: d73acb17-abe4-4c31-a264-a131d1f9fa51
keywords:
- attribut de bibliothèque MIDL
topic_type:
- apiref
api_name:
- library
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 100c901c6b5d86ed3420d51e459627bdb5b461b8
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "106509845"
---
# <a name="library-attribute"></a><span data-ttu-id="88770-104">attribut de bibliothèque</span><span class="sxs-lookup"><span data-stu-id="88770-104">library attribute</span></span>

<span data-ttu-id="88770-105">L’instruction **Library** contient toutes les informations que le compilateur MIDL utilise pour générer une bibliothèque de types.</span><span class="sxs-lookup"><span data-stu-id="88770-105">The **library** statement contains all the information that the MIDL compiler uses to generate a type library.</span></span>

``` syntax
[
    uuid(uuid-number), 
    [, optional-attribute-list]
] 
library library-name
{ 
    library-definition-statements
}
```

## <a name="parameters"></a><span data-ttu-id="88770-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="88770-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="88770-107">*UUID-Number*</span><span class="sxs-lookup"><span data-stu-id="88770-107">*uuid-number*</span></span> 
</dt> <dd>

<span data-ttu-id="88770-108">Spécifie un numéro d’identification unique universel pour la bibliothèque.</span><span class="sxs-lookup"><span data-stu-id="88770-108">Specifies a universally unique identification number for the library.</span></span>

</dd> <dt>

<span data-ttu-id="88770-109">*Optional-attribute-List*</span><span class="sxs-lookup"><span data-stu-id="88770-109">*optional-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="88770-110">Spécifie des attributs supplémentaires qui s’appliquent à l’intégralité de l’instruction **Library** .</span><span class="sxs-lookup"><span data-stu-id="88770-110">Specifies additional attributes that apply to the entire **library** statement.</span></span> <span data-ttu-id="88770-111">Les attributs autorisés sont les suivants : **\[** [**Control**](control.md) **\]** , **\[** [**HelpContext**](helpcontext.md) **\]** , **\[** [**HelpFile**](helpfile.md) **\]** , **\[** [**helpString**](helpstring.md) **\]** , **\[** [**Hidden**](hidden.md) **\]** , **\[** [**LCID**](lcid.md) **\]** , **\[** [**Restricted**](restricted.md) **\]** et **\[** [**version**](version.md) **\]** .</span><span class="sxs-lookup"><span data-stu-id="88770-111">Allowable attributes include **\[**[**control**](control.md)**\]**, **\[**[**helpcontext**](helpcontext.md)**\]**, **\[**[**helpfile**](helpfile.md)**\]**, **\[**[**helpstring**](helpstring.md)**\]**, **\[**[**hidden**](hidden.md)**\]**, **\[**[**lcid**](lcid.md)**\]**, **\[**[**restricted**](restricted.md)**\]**, and **\[**[**version**](version.md)**\]**.</span></span>

</dd> <dt>

<span data-ttu-id="88770-112">*nom de la bibliothèque*</span><span class="sxs-lookup"><span data-stu-id="88770-112">*library-name*</span></span> 
</dt> <dd>

<span data-ttu-id="88770-113">Nom par lequel les composants logiciels font référence à la **bibliothèque**.</span><span class="sxs-lookup"><span data-stu-id="88770-113">The name by which software components refer to the **library**.</span></span>

</dd> <dt>

<span data-ttu-id="88770-114">*Bibliothèque-définition-instructions*</span><span class="sxs-lookup"><span data-stu-id="88770-114">*library-definition-statements*</span></span> 
</dt> <dd>

<span data-ttu-id="88770-115">Une ou plusieurs instructions MIDL qui définissent le contenu de la **bibliothèque**.</span><span class="sxs-lookup"><span data-stu-id="88770-115">One or more MIDL statements which define the contents of the **library**.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="88770-116">Notes</span><span class="sxs-lookup"><span data-stu-id="88770-116">Remarks</span></span>

<span data-ttu-id="88770-117">Les instructions à l’intérieur du bloc de bibliothèque peuvent utiliser des éléments déclarés à l’intérieur ou à l’extérieur du bloc de bibliothèque.</span><span class="sxs-lookup"><span data-stu-id="88770-117">Statements inside the library block can use elements that are declared inside or outside of the library block.</span></span> <span data-ttu-id="88770-118">Les instructions de bibliothèque peuvent utiliser ces éléments comme types de base, héritant de ces éléments ou simplement en les référençant sur une ligne, comme suit :</span><span class="sxs-lookup"><span data-stu-id="88770-118">Library statements can use those elements as base types, inheriting from those elements, or by simply referencing them on a line, as follows:</span></span>

``` syntax
interface MyFace 
{
    // Interface definition statements
};

[
    // library attributes
] 
library
{
    interface MyFace;

    // Other library definition statements.
};
```

<span data-ttu-id="88770-119">Le compilateur MIDL crée une bibliothèque de types qui comprend des définitions pour chaque élément à l’intérieur du bloc de bibliothèque, ainsi que des définitions pour tous les éléments définis en dehors de et référencés à partir du bloc de bibliothèque.</span><span class="sxs-lookup"><span data-stu-id="88770-119">The MIDL compiler will create a type library that includes definitions for every element inside the library block, plus definitions for any elements defined outside and referenced from within the library block.</span></span>

<span data-ttu-id="88770-120">Pour plus d’informations sur la génération d’une bibliothèque de types et de proxy stubs et d’en-têtes à partir d’un seul fichier IDL, consultez [génération d’une dll de proxy et d’une bibliothèque de types à partir d’un seul fichier IDL](generating-a-proxy-dll-and-a-type-library-from-a-single-idl-file-2.md).</span><span class="sxs-lookup"><span data-stu-id="88770-120">For information on generating both a type library and proxy stubs and headers from a single IDL file see [Generating a Proxy DLL and a Type Library From a Single IDL File](generating-a-proxy-dll-and-a-type-library-from-a-single-idl-file-2.md).</span></span>

## <a name="examples"></a><span data-ttu-id="88770-121">Exemples</span><span class="sxs-lookup"><span data-stu-id="88770-121">Examples</span></span>

``` syntax
[
    uuid(12345678-1234-1234-1234-123456789ABC), 
    helpstring("Hello 2.0 Type Library"), 
    lcid(0x0409), 
    version(2.0)
] 
library Hello 
{
    /* Library definition statements */
};
```

## <a name="see-also"></a><span data-ttu-id="88770-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="88770-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="88770-123">Contenu d’une bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="88770-123">Contents of a Type Library</span></span>](/previous-versions/windows/desktop/automat/contents-of-a-type-library)
</dt> <dt>

[<span data-ttu-id="88770-124">**régulation**</span><span class="sxs-lookup"><span data-stu-id="88770-124">**control**</span></span>](control.md)
</dt> <dt>

[<span data-ttu-id="88770-125">Génération d’une bibliothèque de types avec MIDL</span><span class="sxs-lookup"><span data-stu-id="88770-125">Generating a Type Library With MIDL</span></span>](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[<span data-ttu-id="88770-126">**helpcontext**</span><span class="sxs-lookup"><span data-stu-id="88770-126">**helpcontext**</span></span>](helpcontext.md)
</dt> <dt>

[<span data-ttu-id="88770-127">**helpfile**</span><span class="sxs-lookup"><span data-stu-id="88770-127">**helpfile**</span></span>](helpfile.md)
</dt> <dt>

[<span data-ttu-id="88770-128">**helpstring**</span><span class="sxs-lookup"><span data-stu-id="88770-128">**helpstring**</span></span>](helpstring.md)
</dt> <dt>

[<span data-ttu-id="88770-129">**masquer**</span><span class="sxs-lookup"><span data-stu-id="88770-129">**hidden**</span></span>](hidden.md)
</dt> <dt>

[<span data-ttu-id="88770-130">**LCID**</span><span class="sxs-lookup"><span data-stu-id="88770-130">**lcid**</span></span>](lcid.md)
</dt> <dt>

[<span data-ttu-id="88770-131">Syntaxe du fichier ODL</span><span class="sxs-lookup"><span data-stu-id="88770-131">ODL File Syntax</span></span>](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[<span data-ttu-id="88770-132">**sensible**</span><span class="sxs-lookup"><span data-stu-id="88770-132">**restricted**</span></span>](restricted.md)
</dt> <dt>

[<span data-ttu-id="88770-133">**Version**</span><span class="sxs-lookup"><span data-stu-id="88770-133">**version**</span></span>](version.md)
</dt> </dl>

 

 