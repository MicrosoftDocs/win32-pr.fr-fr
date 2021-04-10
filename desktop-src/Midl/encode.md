---
title: Encode (attribut)
description: L’attribut \ encode \ ACF spécifie qu’une procédure ou un type de données a besoin de la prise en charge de la sérialisation.
ms.assetid: 2661021d-8a26-4216-935b-ca40b6f8b9ec
keywords:
- code MIDL de l’attribut encode
topic_type:
- apiref
api_name:
- encode
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7c2a35c6d6910229a9e14026f6727db5c3176050
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "103940871"
---
# <a name="encode-attribute"></a><span data-ttu-id="bea23-104">Encode (attribut)</span><span class="sxs-lookup"><span data-stu-id="bea23-104">encode attribute</span></span>

<span data-ttu-id="bea23-105">L’attribut **\[ encode \]** ACF spécifie qu’une procédure ou un type de données a besoin de la prise en charge de la sérialisation.</span><span class="sxs-lookup"><span data-stu-id="bea23-105">The **\[encode\]** ACF attribute specifies that a procedure or a data type needs serialization support.</span></span>

``` syntax
[ 
    encode 
    [ , interface-attribute-list] 
] 
interface interface-name
{
    interface-definition
}

[ encode [ , op-attribute-list] ] proc-name

typedef [encode [ , type-attribute-list] ] type-name
```

## <a name="parameters"></a><span data-ttu-id="bea23-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="bea23-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bea23-107">*interface-attribut-List*</span><span class="sxs-lookup"><span data-stu-id="bea23-107">*interface-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="bea23-108">Spécifie d’autres attributs qui s’appliquent à l’ensemble de l’interface.</span><span class="sxs-lookup"><span data-stu-id="bea23-108">Specifies other attributes that apply to the interface as a whole.</span></span>

</dd> <dt>

<span data-ttu-id="bea23-109">*nom de l’interface*</span><span class="sxs-lookup"><span data-stu-id="bea23-109">*interface-name*</span></span> 
</dt> <dd>

<span data-ttu-id="bea23-110">Spécifie le nom de l’interface.</span><span class="sxs-lookup"><span data-stu-id="bea23-110">Specifies the name of the interface.</span></span>

</dd> <dt>

<span data-ttu-id="bea23-111">*définition d’interface*</span><span class="sxs-lookup"><span data-stu-id="bea23-111">*interface-definition*</span></span> 
</dt> <dd>

<span data-ttu-id="bea23-112">Spécifie les instructions IDL qui forment la définition de l’interface.</span><span class="sxs-lookup"><span data-stu-id="bea23-112">Specifies IDL statements which form the definition of the interface.</span></span>

</dd> <dt>

<span data-ttu-id="bea23-113">*op-attribut-List*</span><span class="sxs-lookup"><span data-stu-id="bea23-113">*op-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="bea23-114">Spécifie d’autres attributs opérationnels qui s’appliquent à la procédure, tels que **\[** [**Decode**](decode.md) **\]** .</span><span class="sxs-lookup"><span data-stu-id="bea23-114">Specifies other operational attributes that apply to the procedure such as **\[**[**decode**](decode.md)**\]**.</span></span>

</dd> <dt>

<span data-ttu-id="bea23-115">*nom de la procédure*</span><span class="sxs-lookup"><span data-stu-id="bea23-115">*proc-name*</span></span> 
</dt> <dd>

<span data-ttu-id="bea23-116">Spécifie le nom de la procédure.</span><span class="sxs-lookup"><span data-stu-id="bea23-116">Specifies the name of the procedure.</span></span>

</dd> <dt>

<span data-ttu-id="bea23-117">*type-attribut-List*</span><span class="sxs-lookup"><span data-stu-id="bea23-117">*type-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="bea23-118">Spécifie d’autres attributs qui s’appliquent au type, par exemple **\[** [**Decode**](decode.md) **\]** et **\[** [**allocate**](allocate.md) **\]** .</span><span class="sxs-lookup"><span data-stu-id="bea23-118">Specifies other attributes that apply to the type such as **\[**[**decode**](decode.md)**\]** and **\[**[**allocate**](allocate.md)**\]**.</span></span>

</dd> <dt>

<span data-ttu-id="bea23-119">*nom du type*</span><span class="sxs-lookup"><span data-stu-id="bea23-119">*type-name*</span></span> 
</dt> <dd>

<span data-ttu-id="bea23-120">Spécifie un type défini dans le fichier IDL.</span><span class="sxs-lookup"><span data-stu-id="bea23-120">Specifies a type defined in the IDL file.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="bea23-121">Notes</span><span class="sxs-lookup"><span data-stu-id="bea23-121">Remarks</span></span>

<span data-ttu-id="bea23-122">L’attribut **\[ encode \]** fait en sorte que le compilateur MIDL génère du code qu’une application peut utiliser pour sérialiser des données dans une mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="bea23-122">The **\[encode\]** attribute causes the MIDL compiler to generate code that an application can use to serialize data into a buffer.</span></span> <span data-ttu-id="bea23-123">L' **\[** attribut [**Decode**](decode.md) **\]** génère le code pour démarshaler les données d’une mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="bea23-123">The **\[**[**decode**](decode.md)**\]** attribute generates the code for unmarshaling data from a buffer.</span></span>

<span data-ttu-id="bea23-124">Utilisez les attributs **\[ encode \]** et **\[** [**Decode**](decode.md) **\]** dans un CCP pour générer le code de sérialisation des procédures ou des types définis dans le fichier IDL d’une interface.</span><span class="sxs-lookup"><span data-stu-id="bea23-124">Use the **\[encode\]** and **\[**[**decode**](decode.md)**\]** attributes in an ACF to generate serialization code for procedures or types defined in the IDL file of an interface.</span></span> <span data-ttu-id="bea23-125">Lorsqu’il est utilisé comme attribut d’interface, **\[ encode \]** s’applique à tous les types et procédures définis dans le fichier IDL.</span><span class="sxs-lookup"><span data-stu-id="bea23-125">When used as an interface attribute, **\[encode\]** applies to all the types and procedures defined in the IDL file.</span></span> <span data-ttu-id="bea23-126">En cas d’utilisation comme attribut opérationnel, **\[ encode \]** s’applique uniquement à la procédure spécifiée.</span><span class="sxs-lookup"><span data-stu-id="bea23-126">When used as an operational attribute, **\[encode\]** applies only to the specified procedure.</span></span> <span data-ttu-id="bea23-127">Lorsqu’il est utilisé en tant qu’attribut de type, **\[ encode \]** s’applique uniquement au type spécifié.</span><span class="sxs-lookup"><span data-stu-id="bea23-127">When used as a type attribute, **\[encode\]** applies only to the specified type.</span></span>

<span data-ttu-id="bea23-128">Lorsque l’attribut **\[ \] encode** ou **\[** [**Decode**](decode.md) **\]** est appliqué à une procédure, le compilateur MIDL génère un stub de sérialisation de la même façon que les stubs distants pour les routines distantes.</span><span class="sxs-lookup"><span data-stu-id="bea23-128">When the **\[encode\]** or **\[**[**decode**](decode.md)**\]** attribute is applied to a procedure, the MIDL compiler generates a serialization stub in a similar fashion as remote stubs are generated for remote routines.</span></span> <span data-ttu-id="bea23-129">Une procédure peut être une procédure distante ou de sérialisation, mais elle ne peut pas être à la fois.</span><span class="sxs-lookup"><span data-stu-id="bea23-129">A procedure can be either a remote or a serializing procedure, but it cannot be both.</span></span> <span data-ttu-id="bea23-130">Le prototype de la routine générée est envoyé au STUB. Fichier H alors que le stub est placé dans le \_ fichier c. c du stub.</span><span class="sxs-lookup"><span data-stu-id="bea23-130">The prototype of the generated routine is sent to the STUB.H file while the stub itself goes into the STUB\_C.C file.</span></span>

<span data-ttu-id="bea23-131">Le compilateur MIDL génère deux fonctions pour chaque type auquel s’applique l’attribut **\[ encode \]** et une fonction supplémentaire pour chaque type auquel **\[** s’applique l’attribut [**Decode**](decode.md) **\]** .</span><span class="sxs-lookup"><span data-stu-id="bea23-131">The MIDL compiler generates two functions for each type the **\[encode\]** attribute applies to, and one additional function for each type the **\[**[**decode**](decode.md)**\]** attribute applies to.</span></span> <span data-ttu-id="bea23-132">Par exemple, pour un type défini par l’utilisateur nommé MyType, le compilateur génère du code pour les \_ fonctions de décodage MyType, MyType \_ et MyType \_ AlignSize.</span><span class="sxs-lookup"><span data-stu-id="bea23-132">For example, for a user-defined type named MyType, the compiler generates code for the MyType\_Encode, MyType\_Decode, and MyType\_AlignSize functions.</span></span> <span data-ttu-id="bea23-133">Pour ces fonctions, le compilateur écrit des prototypes dans STUB. H et code source pour STUB \_ C.C.</span><span class="sxs-lookup"><span data-stu-id="bea23-133">For these functions, the compiler writes prototypes to STUB.H and source code to STUB\_C.C.</span></span>

<span data-ttu-id="bea23-134">Pour plus d’informations sur les handles de sérialisation et l’encodage ou le décodage des données, consultez [services de sérialisation](/windows/desktop/Rpc/serialization-services).</span><span class="sxs-lookup"><span data-stu-id="bea23-134">For additional information about serialization handles and encoding or decoding data, see [Serialization Services](/windows/desktop/Rpc/serialization-services).</span></span>

## <a name="examples"></a><span data-ttu-id="bea23-135">Exemples</span><span class="sxs-lookup"><span data-stu-id="bea23-135">Examples</span></span>

``` syntax
/* 
    ACF file example; 
    Assumes MyType1, MyType2, MyType3, MyProc1, MyProc2, MyProc3 defined 
    in IDL file  
    MyType1, MyType2, MyProc1, MyProc2 have encode and decode 
    serialization support 
    MyType3 and MyProc3 have encode serialization support only 
*/ 
[ 
    encode, 
    implicit_handle(handle_t bh) 
]    
interface regress 
{ 
    typedef [ decode ] MyType1; 
    typedef [ encode, decode ] MyType2; 
    [ decode ] MyProcc1(); 
    [ encode ] MyProc2(); 
}
```

## <a name="see-also"></a><span data-ttu-id="bea23-136">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="bea23-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bea23-137">Fichier de configuration de l’application (ACF)</span><span class="sxs-lookup"><span data-stu-id="bea23-137">Application Configuration File (ACF)</span></span>](application-configuration-file-acf-.md)
</dt> <dt>

[<span data-ttu-id="bea23-138">**lui**</span><span class="sxs-lookup"><span data-stu-id="bea23-138">**allocate**</span></span>](allocate.md)
</dt> <dt>

[<span data-ttu-id="bea23-139">**décoder**</span><span class="sxs-lookup"><span data-stu-id="bea23-139">**decode**</span></span>](decode.md)
</dt> </dl>

 

 