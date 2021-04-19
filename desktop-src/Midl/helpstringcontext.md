---
title: attribut helpstringcontext
description: L’attribut \ helpstringcontext \ spécifie un identificateur de contexte d’aide 32 bits dans le fichier d’aide. Vous pouvez appliquer l’attribut \ helpstringcontext \ à la bibliothèque, à l’interface, à dispinterface, au module, à la coclasse, aux instructions typedef, aux propriétés, aux paramètres et aux méthodes.
ms.assetid: 0ac41bd9-ccc6-4b5c-b925-63bff9254eed
keywords:
- MIDL de l’attribut helpstringcontext
topic_type:
- apiref
api_name:
- helpstringcontext
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 72ddded3beb768543f2f990aa9d656fba1fa8b98
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/25/2019
ms.locfileid: "106542840"
---
# <a name="helpstringcontext-attribute"></a><span data-ttu-id="b8d39-105">attribut helpstringcontext</span><span class="sxs-lookup"><span data-stu-id="b8d39-105">helpstringcontext attribute</span></span>

<span data-ttu-id="b8d39-106">L’attribut **\[ helpstringcontext \]** spécifie un identificateur de contexte d’aide 32 bits dans le fichier d’aide.</span><span class="sxs-lookup"><span data-stu-id="b8d39-106">The **\[helpstringcontext\]** attribute specifies a 32-bit Help context identifier in the Help file.</span></span> <span data-ttu-id="b8d39-107">Vous pouvez appliquer l’attribut **\[ helpstringcontext \]** à la [**bibliothèque**](library.md), à l' [**interface**](interface.md), à [**dispinterface**](dispinterface.md), au [**module**](module.md), à la [**coclasse**](coclass.md), aux instructions [**typedef**](typedef.md) , aux propriétés, aux paramètres et aux méthodes.</span><span class="sxs-lookup"><span data-stu-id="b8d39-107">You can apply the **\[helpstringcontext\]** attribute to [**library**](library.md), [**interface**](interface.md), [**dispinterface**](dispinterface.md), [**module**](module.md), [**coclass**](coclass.md), [**typedef**](typedef.md) statements, properties, parameters and methods.</span></span>

``` syntax
[  helpstringcontext(contextid)[, optional-attribute-list]] idl-statement
```

## <a name="parameters"></a><span data-ttu-id="b8d39-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b8d39-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b8d39-109">*ContextId*</span><span class="sxs-lookup"><span data-stu-id="b8d39-109">*contextid*</span></span> 
</dt> <dd>

<span data-ttu-id="b8d39-110">Entier unique qui identifie le texte d’aide associé à l’instruction MIDL actuelle.</span><span class="sxs-lookup"><span data-stu-id="b8d39-110">A unique integer that identifies the help text associated with the current MIDL statement.</span></span>

</dd> <dt>

<span data-ttu-id="b8d39-111">*Optional-attribute-List*</span><span class="sxs-lookup"><span data-stu-id="b8d39-111">*optional-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="b8d39-112">Zéro, un ou plusieurs attributs MIDL.</span><span class="sxs-lookup"><span data-stu-id="b8d39-112">Zero or more MIDL attributes.</span></span>

</dd> <dt>

<span data-ttu-id="b8d39-113">*IDL-Statement*</span><span class="sxs-lookup"><span data-stu-id="b8d39-113">*idl-statement*</span></span> 
</dt> <dd>

<span data-ttu-id="b8d39-114">Instruction MIDL à laquelle l’attribut **\[ helpstringcontext \]** sera appliqué.</span><span class="sxs-lookup"><span data-stu-id="b8d39-114">The MIDL statement to which the **\[helpstringcontext\]** attribute will be applied.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b8d39-115">Notes</span><span class="sxs-lookup"><span data-stu-id="b8d39-115">Remarks</span></span>

<span data-ttu-id="b8d39-116">Utilisez les fonctions **GetDocumentation2** dans les interfaces **ITypeLib2** et **ITypeInfo2** pour récupérer la chaîne d’aide.</span><span class="sxs-lookup"><span data-stu-id="b8d39-116">Use the **GetDocumentation2** functions in the **ITypeLib2** and **ITypeInfo2** interfaces to retrieve the help string.</span></span>

## <a name="examples"></a><span data-ttu-id="b8d39-117">Exemples</span><span class="sxs-lookup"><span data-stu-id="b8d39-117">Examples</span></span>

``` syntax
[
    uuid(. . .),
    helpstringcontext(103),
    version(1.0)
]
library Lines
{
    [
        uuid(. . .), 
        helpstringcontext(102),
        oleautomation,
        dual
    ]
    interface ILine : IDispatch
    {
        [propget, helpstringcontext(100)] HRESULT Color([out, retval] long* ReturnVal); 
        [propput, helpstringcontext(101)] HRESULT Color([in] long rgb);
    }
};
```

 

 




